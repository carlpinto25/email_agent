# LangChain Email Agent

This project is an AI-powered email agent built with [LangChain](https://github.com/langchain-ai/langchain), [Ollama](https://ollama.com/), and [Gradio](https://gradio.app/).  
It allows you to send emails by describing the recipient, subject, and body in natural language. The agent can generate the email content and send it using your Gmail account.

---

## Features

- Uses a local Mistral model via Ollama for language understanding.
- Sends emails using Gmail SMTP.
- Simple web interface powered by Gradio.
- Secure: Email credentials are loaded from a `.env` file.

---

## Setup

1. **Clone the repository**

    ```sh
    git clone https://github.com/yourusername/your-repo.git
    cd your-repo
    ```

2. **Install dependencies**

    ```sh
    pip install -r requirements.txt
    ```

3. **Install and run Ollama**

    - Download and install Ollama from [https://ollama.com/download](https://ollama.com/download)
    - Pull the Mistral model:
      ```sh
      ollama pull mistral
      ```
    - Start the Ollama server:
      ```sh
      ollama run mistral
      ```

4. **Set up your `.env` file**

    Create a `.env` file in the project root with:
    ```
    EMAIL_SENDER=your_email@gmail.com
    EMAIL_PASSWORD=your_app_password
    ```

    > **Note:** For Gmail, you must use an [App Password](https://support.google.com/accounts/answer/185833?hl=en) if 2FA is enabled.

---

## Usage

1. **Run the app**

    ```sh
    python email_agent.py
    ```

2. **Open the Gradio interface**

    - Visit the local URL shown in your terminal (usually http://127.0.0.1:7860).

3. **Send an email**

    - Enter your request in the textbox.  
      Example input:
      ```
      send an email to ....@gmail.com with a body of 100 words
      ```

## Acknowledgements

- [LangChain](https://github.com/langchain-ai/langchain)
- [Ollama](https://ollama.com/)
- [Gradio]
