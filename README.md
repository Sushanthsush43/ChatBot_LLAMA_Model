# Web Scraper & Chatbot

This project is a web scraper and chatbot that extracts textual data from a given website and uses a Hugging Face language model to generate responses based on user queries.

## Features
- Scrapes textual content (headings and paragraphs) from a specified website.
- Uses a Hugging Face model (LLaMA 2) to generate responses.
- Implements a recursive scraping function to fetch multiple linked pages.
- Simple chatbot interface that allows users to interact with the model.

## Requirements
Ensure you have the following dependencies installed:
- Python 3.9+
- `requests`
- `beautifulsoup4`
- `transformers`
- `torch`

To install the dependencies, run:
```sh
pip install requests beautifulsoup4 transformers torch
```

## How to Use

1. Clone this repository:
   ```sh
   git clone <repository_url>
   cd <repository_directory>
   ```

2. Update the `website_url` variable in `main()` with the website you want to scrape.

3. Ensure you have a valid Hugging Face API token and update the `hf_token` variable.

4. Run the script:
   ```sh
   python script.py
   ```

5. Start chatting with the bot. Type `exit` or `quit` to end the conversation.

## Code Overview

### `scrape_website(url)`
Recursively scrapes the given website and extracts textual data from `<p>`, `<h1>`, `<h2>`, and `<h3>` elements.

### `load_model(model_name, token)`
Loads the specified Hugging Face model and tokenizer.

### `generate_response(user_query, scraped_data, tokenizer, model)`
Generates a response based on user input and scraped data using the language model.

### `main()`
- Defines the website URL and Hugging Face token.
- Scrapes the website for content.
- Loads the model.
- Starts a chatbot loop for user interaction.

## Notes
- Ensure you have a stable internet connection while running the script.
- Avoid scraping websites that prohibit web scraping in their `robots.txt`.
- Using large models like LLaMA 2 may require high computational resources.

