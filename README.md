# Spotify Song Popularity: Predicting Trends and Success Factors

**Category**: Predictive Modeling, Sentiment Analysis, Feature Engineering  
**Tools Used**: Python, VADER Sentiment Analysis, Latent Dirichlet Allocation (LDA), Hugging Face, Random Forest  

## Overview
This project aims to analyze and predict Spotify song popularity using audio, lyrical, and sentiment features. By understanding trends and factors influencing song popularity, the goal is to provide actionable insights for artists, composers, Spotify, and record labels to enhance their strategies and offerings.

## Business Value & Goals
1. **For Artists**: Boost chances of creating hit songs by aligning with listener trends and preferences.
2. **For Spotify**: Improve recommendation systems and user engagement while targeting ads effectively.
3. **For Record Labels**: Allocate resources efficiently to promising artists and songs.

## Dataset
The dataset contains features categorized as:
- **Track Features**: Track name, album, artists, genre, popularity score (0–100).
- **Audio Features**: Danceability, energy, acousticness, tempo, and more.
- **Lyrics Features**: Language and emotional attributes (joy, sadness, etc.).

### Data Preprocessing
- **Text Translation**: Spanish lyrics were translated to English using the Google Translator API.
- **Popularity Labeling**: Tracks with a popularity score above 62 (75th percentile) were labeled as popular.
- **Missing Values**: Missing months were filled with "January" for records with only year data.
- **Sentiment Analysis**: VADER Lexicon was used to assess overall sentiment.
- **Emotion Analysis**: Hugging Face’s distilroberta model identified fine-grained emotions in lyrics.
- **Topic Modeling**: LDA extracted key themes from lyrics.

## Methodology
1. **Exploratory Data Analysis (EDA)**:
   - Investigated categorical and numerical variables.
   - Analyzed sentiment and emotions in lyrics.
   - Assessed correlations among audio features and their relationship with popularity.

2. **Feature Engineering**:
   - Combined audio, sentiment, and lyrical features.
   - Selected variables based on insights from EDA and correlation analysis.

3. **Modeling**:
   - Applied Random Forest to predict song popularity.
   - Evaluated model performance with a focus on recall for popular songs.

## Key Findings
1. **Popular Song Attributes**:
   - High danceability and loudness significantly influence popularity.
   - Emotional attributes like joy and sadness are major drivers of success.
2. **Model Performance**:
   - For every 100 popular songs predicted, 62 were correctly identified as likely to become popular.
   - Trade-off: Some non-popular songs were misclassified, suggesting room for precision improvements.
3. **Strategic Insights**:
   - Aligning songs with popular trends can enhance success.
   - Insights benefit artists, Spotify, and record labels by focusing resources on promising tracks.

## Suggestions for Stakeholders
- **Artists**: Use insights on danceability and emotional trends to create commercially viable songs.
- **Composers**: Align compositions with popular attributes like joy and danceability.
- **Spotify**:
  - Enhance recommendation systems with predictive analytics.
  - Focus promotional efforts on songs identified as likely to succeed.
- **Record Labels**: Invest in artists and songs aligned with success factors like danceability and emotional appeal.

## Future Recommendations
1. Enhance lyric analysis with Large Language Models (LLMs) to handle slang and informal phrases.
2. Investigate social trends and timing variables that influence popularity.
3. Explore interactions between audio and lyrical features for deeper insights.

## How to Run
1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/spotify-song-popularity.git
