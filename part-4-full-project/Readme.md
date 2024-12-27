# Loan Counselor Agent

This project is a Flask-based REST API for a loan counseling chatbot that helps students understand their loan options. It leverages AI models to provide personalized loan recommendations and maintain contextual conversations with students.

## Features

- **Chat Endpoint**: Converse with the loan counselor to get loan recommendations.
- **Request Validation**: Ensures all necessary student information is provided.
- **Conversation Memory**: Maintains context across interactions.
- **Error Handling**: Robust error handling and logging.
- **CORS Support**: Allows cross-origin requests.
- **Asynchronous Processing**: Utilizes thread pools for efficient request handling.

## Setup

### Prerequisites

- Python 3.8+
- pip (Python package manager)

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/Chandan7323/AI_Powered_Call_Centre.git
   cd loan-counselor-agent
   ```

2. Create a virtual environment:
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows use `venv\Scripts\activate`
   ```

3. Install the dependencies:
   ```bash
   pip install -r requirements.txt
   ```

4. Set up environment variables:
   - Create a `.env` file in the root directory.
   - Add the necessary environment variables, such as `FLASK_SECRET_KEY`, `OPENAI_API_KEY`, etc.

### Running the Application

1. Start the Flask application:
   ```bash
   python wsgi.py
   ```

2. The application will be available at `http://0.0.0.0:8000`.

## Usage

- **Chat with the Loan Counselor**: Send POST requests to `/chat` with the required student details to receive loan recommendations.
- **Reset Conversation**: Send POST requests to `/reset` to clear conversation history.

## API Endpoints

- **POST /chat**: Interact with the loan counselor.
- **POST /reset**: Reset the conversation memory for a user.

## Project Structure

- **app.py**: Main application file.
- **wsgi.py**: WSGI configuration for running the app.
- **vector_store/**: Contains modules for storing and retrieving vector-based data.
- **utils/**: Utility modules and constants.
- **helpers.py**: Helper functions for formatting data.
- **prompts.py**: Contains prompt templates for AI interactions.

## Contributing

Contributions are welcome! Please fork the repository and submit a pull request for any enhancements or bug fixes.

## License

MIT License

Copyright (c) 2024 Infosys

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.
