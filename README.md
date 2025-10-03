# Synthetic Data Generator

An AI-powered tool to generate realistic test datasets for development and testing purposes.

## What It Does

This tool uses OpenAI's GPT models to generate synthetic (fake but realistic) data for testing. Perfect for:
- Testing your applications without real user data
- Creating demo datasets
- Populating databases for development
- Training and learning projects

## Features

- AI-Powered Generation: Uses GPT-4 to create realistic data
- Flexible Formats: Export as JSON or CSV
- Customizable: Specify domain, field types, and record count
- Easy Interface: User-friendly Gradio UI
- Batch Generation: Create 10, 25, or 50 records at once

## Technologies Used

- Python 3.11+
- OpenAI API - For AI data generation
- Gradio - Web interface
- python-dotenv - Environment variable management

## Prerequisites

Before you start, you need:
1. Python 3.11 or higher installed
2. An OpenAI API key (Get one at https://platform.openai.com/api-keys)
3. Basic knowledge of using the terminal/command line

## Installation

### Step 1: Clone the Repository
```bash
git clone https://github.com/ofek-wasserman/synthetic-data-generator.git
cd synthetic-data-generator
```

### Step 2: Create Virtual Environment (Optional but Recommended)
```bash
# On Mac/Linux:
python3 -m venv venv
source venv/bin/activate

# On Windows:
python -m venv venv
venv\Scripts\activate
```

### Step 3: Install Dependencies
```bash
pip install -r requirements.txt
```

### Step 4: Set Up Environment Variables
1. Copy the example environment file and rename it to .env
2. Open the .env file in a text editor
3. Replace your_openai_api_key_here with your actual OpenAI API key
4. Save the file

## Usage

### Using the Script (Recommended)

Run the main Python script:
```bash
python src/synthetic_data_generator.py
```

This will:
1. Launch a web interface in your browser
2. Allow you to specify the domain, description, format, and record count
3. Generate and download your dataset


## Example Usage

Example 1: E-commerce Data
- Domain: ecommerce
- Description: Product data with name, price, category, stock_quantity, and rating
- Format: JSON
- Count: 25

Example 2: Customer Data
- Domain: business
- Description: Customer records with full_name, email, phone, city, signup_date, and total_purchases
- Format: CSV
- Count: 50

## Project Structure

```
synthetic-data-generator/
├── src/                    		# Source code
│   └── synthetic_data_generator.py	# Main application script
├── notebooks/              		# Jupyter notebooks
│   └── synthetic_data_generator_notebook.ipynb
├── output/                 		# Generated datasets saved here
├── screenshots/            		# Demo images
├── .env.example            		# Example environment variables
├── .gitignore             		# Files to ignore in Git
├── requirements.txt        		# Python dependencies
└── README.md              		# This file
```

## Important Notes

- Never share your .env file - It contains your API key
- API costs: OpenAI API is not free. Check pricing at https://openai.com/pricing
- Rate limits: OpenAI has rate limits. Large datasets may take time
- Generated data is synthetic - Not real data, for testing only

## Troubleshooting

### OpenAI API Key not set error
- Make sure .env file exists in the project root
- Check that OPENAI_API_KEY is spelled correctly
- Verify your API key is valid

### Module not found error
- Run pip install -r requirements.txt again
- Make sure you're using Python 3.11+

### Web interface doesn't open
- Check if port 7860 is already in use
- Try closing other applications
- Look at terminal for error messages

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Author

**Ofek Wasserman**
- GitHub: [@ofek-wasserman](https://github.com/ofek-wasserman)
- Email: ofek.wass@gmail.com

## About This Project

This project was created as part of the "LLM Engineering: Master AI and Large Language Models" course by Ed Donner on Udemy. It demonstrates practical application of:
- Working with LLM APIs (OpenAI GPT-4)
- Building user interfaces for AI tools with Gradio
- Handling API keys securely with environment variables
- Prompt engineering for data generation tasks
- Creating production-ready Python applications

This is one of several hands-on projects I completed while learning LLM engineering concepts including RAG systems, AI agents, and prompt optimization.

## Acknowledgments

- Course: [LLM Engineering: Master AI and Large Language Models](https://www.udemy.com/course/llm-engineering-master-ai-and-large-language-models/) by Ed Donner
- Built with [OpenAI API](https://openai.com)
- UI powered by [Gradio](https://gradio.app)
- Part of my LLM Engineering learning journey
