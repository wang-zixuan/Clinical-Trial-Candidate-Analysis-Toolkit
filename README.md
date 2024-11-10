# Sentiment Analysis and Personalized Messaging for Clinical Trial Recruitment

## Objective
The objective of this project is to ethically scrape and analyze Reddit web data, utilize sentiment analysis, and leverage AI to personalize communication. In this project, we will focus on identifying potential participants for a clinical trial by analyzing sentiments expressed on his/her posts.

## Running the code
I use Jupyter notebook for development. To run the code, click inside the cell and press `Shift + Enter` or use the "Run" button in the toolbar. The cell output will appear below the code.

## Methodology
### Data Collection
Scraping Reddit: I used the PRAW (Python Reddit API Wrapper) library to access and scrape posts and comments from subreddits related to clinical trials and health conditions. Specific subreddits targeted included r/health, r/clinicaltrials, r/clinicalresearch, and r/medicine. To ensure that the subreddits were related to health conditions relevant to the clinical trial, I implemented keyword-based filters such as diabetes, hypertension, insulin, blood pressure, clinical trial, treatment, and side effects to extract posts and comments.

### Sentiment Analysis
I employed `NTLK`'s `SentimentIntensityAnalyzer` (VADER) for sentiment analysis due to its effectiveness with social media data.

I calculated sentiment scores for posts and comments. The compound score was used to categorize user opinions into positive, negative, or neutral. The average score was 0.1, and the maximum score is 0.8176. 


### Message Generation
I integrated the OpenAI GPT-3.5 model to generate personalized messages based on the sentiment analysis results. I set the threshold to be 0.3 to identify potential participants. For each participant, I generated a unique tailored message.

### Challenges Faced
The main challenge was data collection. I needed to figure out which subreddits to choose. To address this, I manually explored various health-related subreddits and evaluated their relevance to clinical trial discussions. This process involved reviewing subreddit descriptions, browsing recent posts, and identifying active discussions that aligned with the project’s focus. Additionally, I ensured that selected subreddits had sufficient activity and user engagement to provide meaningful data.

## Examples
### Post Title
Webinar Tomorrow: Hear how experiential data and feedback from the patient's point of view can shape the future of clinical trials in a free 15-minute FLASH webinar 11/2 at 12pm EST.

### Sentiment Analysis Result
The compound score for this post is 0.5106.

### Generated Message
Hello! I wanted to share an exciting opportunity with you - tomorrow there's a FLASH webinar discussing how experiential data and patient feedback can revolutionize clinical trials. Your perspective is incredibly valuable in shaping the future of healthcare. Join us for a free 15-minute session on 11/2 at 12pm EST and be a part of this impactful discussion. Your insights could make a real difference. Hope to see you there! #PatientEmpowerment #ClinicalTrials #FutureOfHealthcare


## Ethical considerations
I ensured compliance with Reddit’s API terms of service by only using publicly available data and not storing any personally identifiable information (PII). Also, the generated messages were crafted to be supportive and informative, avoiding coercive language. Collected data was solely used for this assignment and not shared or used for any other purposes.
