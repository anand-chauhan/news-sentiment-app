# News Summarisation and Text-to-Speech Application

## Project Overview
This project is a web-based application that extracts news articles related to a given company, performs sentiment analysis, conducts a comparative analysis, and generates a text-to-speech (TTS) output in Hindi. Users can input a company name and receive a structured sentiment report along with an audio summary.

## Features
- **News Extraction:** Extracts and displays titles, summaries, and metadata from at least 10 unique news articles.
- **Sentiment Analysis:** Categorises each article as Positive, Negative, or Neutral.
- **Comparative Analysis:** Highlights differences in news coverage across multiple articles.
- **Text-to-Speech (TTS):** Converts the summarised content into Hindi speech.
- **User Interface:** Built using Streamlit for easy interaction.
- **API Development:** Frontend and backend communication via Flask APIs.
- **Deployment:** Hosted on Hugging Face Spaces for public access.

## Project Setup
### 1️⃣ Prerequisites
- Python 3.8+
- Virtual environment (optional but recommended)
- `pip` installed

### 2️⃣ Installation Steps
```bash
# Clone the repository
git clone https://github.com/anand-chauhan/AIProjectOptimizer
cd news-sentiment-app

# Install dependencies
pip install -r requirements.txt
```

### 3️⃣ Running the Application
```bash
# Start the Flask API
python api.py &

# Run the Streamlit app
streamlit run app.py
```

## Model Details
- **News Extraction:** Uses BeautifulSoup to scrape and parse RSS feeds.
- **Sentiment Analysis:** Uses TextBlob for sentiment polarity scoring.
- **Topic Extraction:** YAKE (Yet Another Keyword Extractor) is used for meaningful keyword identification.
- **Text-to-Speech:** Uses Google Text-to-Speech (`gTTS`) for generating Hindi speech.

## API Development
### Available Endpoints
| Method | Endpoint | Description |
|--------|-------------|-------------|
| POST   | `/get_news` | Fetches news articles, analyses sentiment, extracts keywords, and generates speech |

### Sample API Request
```json
{
  "company": "Tesla"
}
```

### Sample API Response
```json
{
  "articles": [...],
  "sentiment_summary": {"Positive": 1, "Negative": 1, "Neutral": 8},
  "topics": ["Electric Vehicles", "Stock Market", "Innovation"],
  "audio": "static/output.mp3"
}
```

## API Usage
- API can be tested using **Postman** or **cURL**.
- Ensure the Flask server is running before making API requests.

## Assumptions & Limitations
- **Static dataset** is used for news articles in Hugging Face due to live API restrictions.
- Sentiment analysis is based on **TextBlob**, which may not always be 100% accurate.
- TTS output is limited to **Hindi** using `gTTS`.

## Deployment
- The project is hosted on **Hugging Face Spaces**.
- Ensure all dependencies are correctly listed in `requirements.txt` before deployment.

## Evaluation Criteria
✅ **Correctness** - Extracts and processes information accurately.
✅ **Efficiency** - Optimised for faster response time.
✅ **Robustness** - Handles errors and edge cases.
✅ **Deployment** - Accessible via Hugging Face Spaces.
✅ **Code Quality** - Follows PEP8 guidelines and includes meaningful comments.

## Submission Details
- **Hugging Face Spaces Deployment:** https://huggingface.co/spaces/anandsinghc22/news-sentiment-app
- **Demo Video:** [Upload & Share Link]

## Deadline
📅 **Submission Deadline:** 1 week from the starting time.

---
🚀 *Developed with Python, Flask, Streamlit, and NLP Technologies!*
