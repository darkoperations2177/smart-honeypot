# Scam Detection Honeypot

A honeypot application designed to detect and waste the time of scammers by simulating a confused elderly victim ("Ramesh"). It extracts intelligence (UPI IDs, bank accounts) from scammer messages.

## Features

- **Persona Simulation**: Acts as "Ramesh", a 68-year-old retired teacher.
- **Intelligence Extraction**: Identifies UPI IDs, phone numbers, and bank details.
- **Smart Response**: Uses LLMs (via OpenRouter) to generate context-aware responses.
- **Reporting**: Automatically sends reports of detected scams to a callback URL.

## Setup

1.  **Clone the repository**
2.  **Install dependencies**:
    ```bash
    pip install -r requirements.txt
    ```
3.  **Configure Environment**:
    - Rename `.env.example` to `.env`.
    - Edit `.env` and add your `OPENROUTER_API_KEY`.
    ```bash
    mv .env.example .env
    ```

## Usage

1.  **Run the server**:
    ```bash
    uvicorn main:app --reload
    ```
2.  **Open the interface**:
    - Visit `http://localhost:8000` in your browser.

## API Endpoints

- `GET /`: Serves the chat interface.
- `POST /scam-detect`: Main endpoint for processing messages.

## License

MIT
