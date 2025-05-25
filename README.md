# Duplicate Question Detection System

A machine learning-powered web application that intelligently identifies whether two questions are duplicates or paraphrases of each other using advanced natural language processing techniques and comprehensive feature engineering.

## 🚀 Overview

This project implements a sophisticated duplicate question detection system that combines multiple NLP approaches including statistical analysis, fuzzy string matching, and bag-of-words vectorization to achieve accurate similarity predictions. The system is deployed as an interactive web application using Streamlit.

## ✨ Features

- **Intelligent Text Processing**: Advanced preprocessing pipeline handling contractions, special characters, HTML tags, and text normalization
- **Multi-Modal Feature Engineering**: 22+ engineered features combining lexical, syntactic, and semantic similarities
- **Fuzzy String Matching**: Implementation of multiple fuzzy matching algorithms (QRatio, Partial Ratio, Token Sort/Set Ratios)
- **Real-time Prediction**: Instant duplicate detection through an intuitive web interface
- **Robust Architecture**: Production-ready code with proper error handling and modular design

## 🛠️ Technology Stack

- **Frontend**: Streamlit
- **Backend**: Python
- **ML Libraries**: Scikit-learn, NumPy
- **NLP Libraries**: NLTK, FuzzyWuzzy
- **Text Processing**: BeautifulSoup, Regular Expressions
- **Model Persistence**: Pickle

## 📦 Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/duplicate-question-detection.git
   cd duplicate-question-detection
   ```

2. **Create a virtual environment** (recommended)
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install required dependencies**
   ```bash
   pip install streamlit
   pip install nltk
   pip install fuzzywuzzy
   pip install beautifulsoup4
   pip install distance
   pip install scikit-learn
   pip install numpy
   pip install python-levenshtein  # For faster fuzzy matching
   ```

4. **Download NLTK data**
   ```python
   import nltk
   nltk.download('stopwords')
   ```

## 🚀 Usage

1. **Start the Streamlit application**
   ```bash
   streamlit run app.py
   ```

2. **Open your web browser** and navigate to `http://localhost:8501`

3. **Enter two questions** in the input fields

4. **Click "Find"** to get the duplicate detection result

### Example Usage

```
Question 1: "How do I learn Python programming?"
Question 2: "What's the best way to learn Python?"
Result: Duplicate ✅

Question 1: "What is machine learning?"
Question 2: "How do I cook pasta?"
Result: Not Duplicate ❌
```

## 🏗️ Project Structure

```
duplicate-question-detection/
│
├── app.py                 # Main Streamlit application
├── helper.py             # Feature engineering and preprocessing
├── model.pkl             # Pre-trained machine learning model
├── cv.pkl               # CountVectorizer for BoW features
├── README.md            # Project documentation
└── requirements.txt     # Dependencies (create this file)
```

## 🔧 Core Components

### Feature Engineering Pipeline

The system extracts 22+ features across multiple categories:

#### **Basic Statistical Features (7 features)**
- Character and word lengths
- Common word counts and ratios
- Total vocabulary overlap

#### **Advanced Token Features (8 features)**
- Common word/stopword ratios (min/max normalized)
- First/last word similarity
- Token intersection analysis

#### **Length-Based Features (3 features)**
- Word count differences
- Average lengths
- Longest common substring ratios

#### **Fuzzy String Matching (4 features)**
- QRatio: Overall similarity score
- Partial Ratio: Best substring match
- Token Sort/Set Ratios: Order-independent similarity

#### **Bag of Words Features**
- TF-IDF vectorization for semantic content
- High-dimensional sparse feature representation

### Text Preprocessing

- **Normalization**: Lowercase conversion, special character handling
- **Contraction Expansion**: 100+ contraction mappings (can't → cannot)
- **Number Standardization**: Large number formatting (1,000,000 → 1m)
- **HTML Cleaning**: Tag removal using BeautifulSoup
- **Punctuation Stripping**: Non-alphanumeric character removal

## 🎯 Use Cases

- **Q&A Platforms**: Stack Overflow, Quora duplicate detection
- **Customer Support**: Identifying repetitive support tickets
- **Content Moderation**: Detecting duplicate posts in forums
- **Search Enhancement**: Improving search result quality
- **Data Cleaning**: Removing duplicate entries from datasets

## 📊 Model Performance

The system uses a pre-trained machine learning model that combines all engineered features for binary classification. The model demonstrates strong performance across various question types and domains.

## 🤝 Contributing

Contributions are welcome! Here are some ways you can contribute:

1. **Fork the repository**
2. **Create a feature branch** (`git checkout -b feature/AmazingFeature`)
3. **Commit your changes** (`git commit -m 'Add some AmazingFeature'`)
4. **Push to the branch** (`git push origin feature/AmazingFeature`)
5. **Open a Pull Request**

### Areas for Enhancement

- [ ] Deep learning embeddings (BERT, RoBERTa)
- [ ] Ensemble model implementations
- [ ] API endpoint development
- [ ] Batch processing capabilities
- [ ] Performance monitoring dashboard
- [ ] Unit test coverage
- [ ] Docker containerization

## 📝 Requirements

Create a `requirements.txt` file with the following dependencies:

```
streamlit>=1.28.0
nltk>=3.8
fuzzywuzzy>=0.18.0
beautifulsoup4>=4.12.0
distance>=0.1.3
scikit-learn>=1.3.0
numpy>=1.24.0
python-levenshtein>=0.21.0
```

## 🐛 Troubleshooting

### Common Issues

1. **NLTK Data Error**: Run `nltk.download('stopwords')` in Python
2. **Module Not Found**: Ensure all dependencies are installed in your virtual environment
3. **Model Loading Error**: Verify `model.pkl` and `cv.pkl` files are in the project directory

### Performance Tips

- Use `python-levenshtein` for faster fuzzy matching
- Consider preprocessing questions in batches for better performance
- Monitor memory usage with large datasets

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 👨‍💻 Author

**Your Name**
- **Name**: Tanvi Konde
- **GitHub**: [@tanvikonde](https://github.com/tanvikonde)
- **Email**: kondetanvi@gmail.com
## 🙏 Acknowledgments

- NLTK team for natural language processing tools
- FuzzyWuzzy library for string matching algorithms
- Streamlit team for the amazing web framework
- Scikit-learn community for machine learning utilities

## 📈 Future Roadmap

- [ ] Integration with transformer-based models (BERT, RoBERTa)
- [ ] Real-time learning capabilities
- [ ] Multi-language support
- [ ] REST API development
- [ ] Docker deployment
- [ ] Cloud hosting integration
- [ ] Performance benchmarking suite

---

⭐ **Star this repository** if you find it helpful!

🔄 **Fork and contribute** to make it even better!
