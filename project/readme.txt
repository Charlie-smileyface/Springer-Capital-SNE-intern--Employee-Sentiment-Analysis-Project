# Project: Employee Sentiment Analysis

## Project Summary

This project analyzes an unlabeled dataset of employee email messages to assess sentiment and engagement. Using Python with libraries such as Pandas, Transformers (Hugging Face), and Scikit-learn, the project performs several key tasks: automated sentiment labeling of messages, exploratory data analysis to identify trends, calculation of monthly sentiment scores for each employee, ranking of employees based on sentiment, identification of potential flight risks, and the development of a linear regression model to predict sentiment scores. The goal is to derive actionable insights from unstructured text data to better understand employee morale and engagement.

## Key Highlights

### Top Employees (Overall)

Based on the frequency of appearing in the top/bottom 3 monthly rankings over a two-year period:

*   **Top Positive Employee:** `johnny.palmer@enron.com` (appeared in the top 3 positive list 14 times)
*   **Top Negative Employee:** `patti.thompson@enron.com` (appeared in the top 3 negative list 12 times)

### List of Employees Flagged as Flight Risks

The following employees were identified as potential flight risks, having sent 4 or more negative emails in a rolling 30-day window:

*   kayne.coulter@enron.com
*   rhonda.denton@enron.com
*   john.arnold@enron.com
*   bobette.riner@ipgdirect.com
*   johnny.palmer@enron.com
*   lydia.delgado@enron.com
*   patti.thompson@enron.com
*   sally.beck@enron.com
*   don.baughman@enron.com
*   eric.bass@enron.com

### Key Insights and Recommendations

1.  **Predominantly Negative Sentiment:** The overall sentiment across the dataset is heavily skewed towards negative. This was a consistent trend across both years analyzed.
    *   **Recommendation:** Management should investigate the root causes of the negative communication environment. This could involve surveys, focus groups, or direct engagement with employees to understand key pain points.

2.  **Flight Risk Criteria:** The current flight risk criteria (4+ negative emails in 30 days) flagged a large number of active employees.
    *   **Recommendation:** The sensitivity of the flight risk model should be adjusted. Consider increasing the threshold for negative messages or shortening the rolling window to identify more acute periods of dissatisfaction. This metric should be used as an early warning indicator in conjunction with other HR data (e.g., absenteeism, performance reviews).

3.  **Predictive Model Limitations:** The linear regression model built to predict monthly sentiment scores showed very low predictive power (R-squared of 0.108).
    *   **Recommendation:** For future predictive efforts, a richer dataset is required. Incorporating features beyond email data, such as HR information, project involvement, and team structure, would likely yield a more accurate model. The current features alone are insufficient to capture the complexity of employee sentiment.