# CAHSRA Public Sentiment Analysis Dashboard

## Project Overview

This honors project analyzes public sentiment toward the California High-Speed Rail Authority (CAHSRA) by collecting and processing social media data from Reddit and YouTube. Using natural language processing techniques and visualization tools, the dashboard provides real-time insights into how people perceive CAHSR’s funding, governance, construction progress, and overall public image.

---

## 🔗 View the Live Dashboard

You can view the live Streamlit dashboard here (no setup required):

**[https://cahsra-sjsu.streamlit.app](https://cahsra-sjsu.streamlit.app/)**

---

## 🛠 Run Locally (For Developers or Contributors)

If you want to run the dashboard locally on your own machine (for development or offline use), follow these steps:

1. **Clone the repository**

   ```bash
   git clone https://github.com/your-username/cahsra-sentiment-dashboard.git
   cd cahsra-sentiment-dashboard
   ```

2. **Set up your Azure secrets**  
   This app uses Azure Blob Storage to read sentiment data. To run the dashboard locally, you will need:
   - An Azure Storage account
   - A container named `visualizationdata`
   - CSV files structured as described below (see “Azure Blob Structure”)

   Then create a `.streamlit/secrets.toml` file and insert your connection string:

   ```toml
   [default]
   AZURE_CONNECTION_STRING = "your_connection_string_here"
   ```
   ⚠️ *Note: If you don’t have access to the original data files, the dashboard won’t work as expected.*

3. **Install dependencies**  
   The `requirements.txt` file lists all necessary Python packages. Install them with:

   ```bash
   pip install -r requirements.txt
   ```

4. **Launch the dashboard locally**

   ```bash
   streamlit run streamlit_dashboard.py
   ```

---

## Azure Blob Structure

Container: `visualizationdata`

- `reddit_analysis.csv` — Sentiment scores and categories for Reddit comments  
- `reddit_time_series.csv` — Daily sentiment trends from Reddit  
- `reddit_post_word_cloud.csv` — Word frequencies for Reddit word clouds  
- `youtube_analysis.csv` — Sentiment scores and categories for YouTube comments  
- `youtube_time_series.csv` — Daily sentiment trends from YouTube  
- `youtube_post_word_cloud.csv` — Word frequencies for YouTube word clouds  

---

## Dashboard Features

- 📈 **Sentiment Over Time**: Tracks average daily sentiment per topic  
- 🔥 **Volume Trends**: Shows comment/post frequency across time  
- 🌐 **Word Clouds**: Visualizes most frequent words by platform  
- 🧩 **Correlation Heatmap**: Displays category relationships  
- 📊 **Cross-Platform Comparison**: Combined Reddit & YouTube view  

---

## Technologies Used

- Python  
- Streamlit  
- Azure Blob Storage  
- Plotly  
- Transformers (for sentiment analysis)  
- PRAW (Reddit API), YouTube Data API  

---

## Authors

**Iakona Nakanishi, Nikolas Perez Linggi, Yun-Hsuan Ku, Mei-Chi Chen**  
Honors Practicum in Marketing and Business Analytics Project – Spring 2025  
San Jose State University  

---

## Acknowledgments

We sincerely thank the **California High-Speed Rail Authority (CAHSRA)** for providing access to Instagram and YouTube engagement data. Their support made it possible to conduct a more comprehensive and meaningful sentiment analysis across multiple social media platforms.
