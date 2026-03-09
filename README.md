# WhatsApp Chat Sentiment Analyzer 

A modern, interactive Streamlit application for analyzing WhatsApp chat sentiment using NLTK's VADER sentiment analyzer.

## Features

✨ **Interactive Dashboard**
- Upload and analyze WhatsApp chat exports
- Real-time sentiment analysis
- Interactive visualizations

📊 **Analytics**
- Sentiment distribution (Positive, Negative, Neutral)
- Per-sender activity and statistics
- Sentiment trends over time
- Word count and message length analysis

🎨 **Visualizations**
- Sentiment distribution charts
- Pie charts showing sentiment percentages
- Top active senders bar chart
- Daily sentiment trend line graph
- Message length distribution

🔍 **Detailed Analysis**
- Filter messages by sender and sentiment
- View individual messages with sentiment labels
- Detailed sender statistics

## Installation

### Prerequisites
- Python 3.8+
- pip (Python package manager)

### Setup Steps
### 🚀 Running the Streamlit Application

#### ✅ If Python is already installed

1. Check Python version

```bash
py --version
```

2. Install required libraries

```bash
py -m pip install streamlit pandas nltk matplotlib seaborn numpy
```

3. Run the Streamlit application

```bash
py -m streamlit run streamlit_app.py
```

The application will open in your browser at:

```
http://localhost:8501
```

---

#### ⚠️ If Python is not installed

1. Download and install Python from the official website:
   https://www.python.org/downloads/

2. After installation, open the project folder in VS Code and run:

```bash
py --version
py -m pip install streamlit pandas nltk matplotlib seaborn numpy
py -m streamlit run streamlit_app.py
```

The Streamlit app will start and open in your browser at:

```
http://localhost:8501
```



The app will open in your default web browser at `http://localhost:8501`

## How to Export WhatsApp Chat

### On Android:
1. Open WhatsApp
2. Go to the chat you want to export
3. Tap the menu (three dots) → More → Export chat
4. Choose "Without Media" to reduce file size
5. Save the .txt file

### On iPhone:
1. Open WhatsApp
2. Swipe left on the chat
3. Tap "More" → "Export Chat"
4. Choose "Without Media"
5. Save the .txt file

## Usage

1. **Upload Chat File**: Click on "Upload WhatsApp chat (.txt)" in the sidebar
2. **Wait for Analysis**: The app will parse and analyze the chat
3. **Explore Results**: Navigate through different sections:
   - Chat Overview: Basic statistics
   - Sentiment Analysis: Distribution and percentages
   - Activity by Sender: Who's most active
   - Sentiment Trend: How sentiment changes over time
   - Message Details: Individual messages with filters
   - Word Statistics: Message length analysis

## Features Explained

### Sentiment Analysis
- **Positive**: Messages with positive emotional content
- **Negative**: Messages with negative emotional content
- **Neutral**: Messages with neutral tone

### Sender Statistics
- **Messages**: Total message count per sender
- **Avg Words**: Average word count per message
- **Positive Messages**: Count of positive-sentiment messages

### Filters
- Filter messages by specific senders
- Filter by sentiment category
- View top 50 matching messages

## Requirements File

Create a `requirements_streamlit.txt` file with:

```
streamlit==1.28.1
pandas==2.0.3
nltk==3.8.1
matplotlib==3.7.2
seaborn==0.12.2
numpy==1.24.3
```

## Troubleshooting

### Issue: "ModuleNotFoundError: No module named 'streamlit'"
**Solution**: Run `pip install streamlit`

### Issue: NLTK data not found
**Solution**: The app automatically downloads required NLTK data. If issues persist, run:
```python
import nltk
nltk.download('vader_lexicon')
nltk.download('punkt')
nltk.download('stopwords')
nltk.download('wordnet')
```

### Issue: Chat not parsing correctly
**Ensure**:
- File is exported from WhatsApp as .txt
- File encoding is UTF-8
- Chat format follows standard WhatsApp export format

## Performance Notes

- For large chats (>5000 messages), the app may take 30-60 seconds to analyze
- The analysis is cached in memory while the app is running
- Refresh the page to reload the app with a new file

## Limitations

- Text only (media files are ignored)
- Sentiment analysis based on English language
- Time zone information depends on phone settings at export time
- Group chat changes (member additions/removals) are filtered out

## Future Improvements

- Multi-language support
- Advanced NLP models (BERT, RoBERTa)
- Export analysis results as PDF
- Real-time chat monitoring
- Emoji sentiment analysis
- Topic modeling

## License

This project is based on the WhatsApp-Chat-Analyzer project.

## Support

For issues or feature requests, please check the project repository or create an issue.

---

**Enjoy analyzing your WhatsApp chats! 🚀**

