# Video Game Sales – Data Analysis & Prediction

This project explores global video game sales, platforms, critic and user scores, and age ratings.  
We analyze sales trends, investigate key factors behind successful games, and build a machine learning model to predict sales.

## Dataset

The dataset comes from [**Kaggle – Video Game Sales with Ratings**](https://www.kaggle.com/datasets/rush4ratio/video-game-sales-with-ratings).  
It includes details such as:
- **Name** – title of the game  
- **Platform** – console/platform released on  
- **Year_of_Release**  
- **Genre**  
- **Global_Sales** (in millions)  
- **Critic_Score**, **User_Score**  
- **Rating** (ESRB age rating)  

Specifically, this project asks and answers the following Research Questions (RQ):

#### RQ1: Which genres were the most successful?  
#### RQ2: Which platform was the sales leader by year?  
#### RQ3: Is there a relationship between critic scores and sales?  
#### RQ4: How are games distributed across ESRB ratings?  

## Tools and Libraries Used
- [Jupyter Notebooks](https://jupyter.org)
- [Python 3](https://www.python.org)
- [Pandas](https://pandas.pydata.org)  
- [NumPy](https://numpy.org)  
- [Matplotlib](https://matplotlib.org)  
- [Seaborn](https://seaborn.pydata.org)  
- [Scikit-learn](https://scikit-learn.org)  
- [XGBoost](https://xgboost.ai)  

## Requirements
Install the latest versions:
```bash
pip install -r requirements.txt
```

## Files
- `Video_Games_Sales.csv` – dataset (from Kaggle)  
- `video_game_analysis.ipynb` – Jupyter Notebook with analysis and ML pipeline  
- `README.md` – project documentation  
- `requirements.txt` – dependencies list  

## Visualizations Used
- **Line plots:** Show sales trends over time and by platform.  
- **Bar plots:** Compare distributions of genres and platforms.  
- **Pie Charts:** Explore distribution by ESRB ratings.  

## Results (Short Version)
**RQ1:** Genres like Action, Sports and Shooter were the most popular.    
**RQ2:** Leadership shifted across console generations: PS2 → Wii → PS3/X360.  
**RQ3:** Higher critic scores often mean higher sales, though correlation is not strong.  
**RQ4:** Most games are rated E, T, M, or E10+. Others are rare.  


## Results (Detailed)
**RQ1:** Since target audience are men genres like Action, Sports and Shooters being the most popular is justified with Global Sales over 1000 Million copies each.

**RQ2:** Sales leaders varied by generation. PlayStation 2 dominated the early 2000s, Wii led during 2006–2009, while PS3 and Xbox 360 later shared the lead. This highlights the role of console changed in shaping sales patterns.   

**RQ3:** Line plots confirm a weak but positive correlation: games with higher critic scores tend to sell more, though many exceptions exist.  

**RQ4:** ESRB ratings distribution shows dominance of E (Everyone), T (Teen), M (Mature), and E10+, with other categories being less than 1%.  

---

## Machine Learning Part
I built a regression model to predict `Global_Sales`:  
- **Pipeline:** preprocessing (scaling numeric + one-hot encoding categorical) + model.  
- **Model:** XGBoost Regressor with early stopping.  
- **Metrics:** MAE = 0.42 , R² = 0.28.  
- **Insights:** Critic/User score, Critic/User Count, platform and release year have big influence to Global Sales.  
- **Comments:** Since some games can hit Box Office it makes machine extreamly hard to predict it with MAE less than 0.4 millions
## What You’ll Learn
By studying this project, you’ll gain skills in:  
- Cleaning and transforming datasets  
- Visualizing categorical and numerical data  
- Asking and answering analytical questions  
- Building and evaluating regression models   

### Author :
### Shokirov Said
