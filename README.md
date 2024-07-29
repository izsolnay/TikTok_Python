![](TikTok.jpg)
# TikTok Video Classification Project
### Purpose
TikTok is a platform for producing and viewing short-term mobile videos. Users of the platform can report videos and comments that contain claims versus opinions. With the high number of submissions and interactions on TikTok each day, it is challenging for human moderators to review efficiently each video, comment, and claim concerning content. TikTok wants to reduce the backlog of user reports and prioritize `claim` reports. **The goal of this project is to mitigate misinformation in videos on the TikTok platform by building a reliable machine learning model which will help reduce report backlog**.

* An *opinion* is a personal or group belief or thought concerning any information, action, thought, person, or group, place, or thing
* A *claim* is unqualified information concerning any information, action, thought, person, or group, place, or thing

As presented by TikTok: “any answers, responses, comments, opinions, analysis or recommendations that you are not properly licensed or otherwise qualified to provide (https://www.tiktok.com/legal/page/us/terms-of-service/en ).” \
TikTok safety: https://newsroom.tiktok.com/en-us/safety

### Deliverables
* **Notebook Part I: Exploratory Data Analysis (EDA)**\
Notebook I contains the organization and preparation of the data set, statistical analyses, and visualizations of the data set. The statistical analyses include considerations of which variables will be most useful for model building by providing plots which visualize variables and relationships between variables.


* **Notebook Part II: Binomial Logistic Regression Model**\
This section contains a binomial logistic regression model built to predict whether a posted video comes from a verified or not verified author. EDA results suggest that if a video is posted by a verified author, it is more likely to contain an *opinion*. The built model provides a ranking of how different variables are associated with whether a user is verified (the feature `verified_status`); how video characteristics relate to `verified_status`. Of particular interest is the predictive power of the feature `claim_status`. `claim_status` labels videos as either claims or opinions.


* **Notebook Part III: Random Forest and XGBoost Machine Learning models**\
In Part III, the  For these tree-based models the goal is to predict a binary outcome, this time using the variable `claim_status`. Like the logistic regression model contained in Notebook II, these models produce rankings of the predictive power of each variable in estimating the `claim_status` of a video: Opinion or Claim. Although the feature `verified_status` is highly correlated with `claim_status`, confirming if it is the most predictive feature is of chief importance.


* **Appendix 1: Hypothesis Testing, Two-sample t-tests**\
Several two-sample hypothesis tests (t-test) to ascertain if there is a statistically significant difference or a random sampling occurrence in *mean* in `video_view_count` and the statuses: `verified_status`, `claim_status`, and `author_ban_status`.


* **Appendix 2: Tokenize Text Column**\
In this section, the Random Forest and XGBoost machine learning models are redeveloped, leveraging the tokenization feature `video_transcription_text`. Tokenization involves breaking down text into smaller components, or tokens, such as words, phrases, or symbols. This process not only facilitates sentiment analysis but also improves the preparation of data for machine learning models, ultimately enhancing the ability to derive actionable insights from video content.


### Data
The data set used here comes from the Google Advanced Data Analytics Professional Certificate course on the Coursera platform: https://www.coursera.org/google-certificates/advanced-data-analytics-certificate

### Code and Reports
All code and reports for this project are located at: https://github.com/izsolnay/TikTok_Python
