# Predicting Avalanche Season Ticket Renewal
![picture](https://cdn.vox-cdn.com/thumbor/bWRoJBG0GQDKzy0_jwDojxmtJ4A=/0x0:1099x733/1820x1213/filters:focal(0x0:1099x733):format(webp)/cdn.vox-cdn.com/uploads/chorus_image/image/16269859/3d_photo_conc_pepsi_center_avalanche_final.0.jpg)
Photo from [milehighhockey.com](https://www.milehighhockey.com/2013/7/11/4514554/pepsi-center-gets-digital-overhaul)

### Authored by: Jeff Thomas

# Problem Statement:
- The purpose of this project is to create a classification model to predict whether a current Avalanche season ticket holder will renew for next season. I will measure success of the model against the baseline (majority class) of 79.5%. I aim to give Kroenke Sports & Entertainment insights into which factors contribute the most to season ticket renewal, as well as offer a predictive model to help them better market to these valuable customers.

# Background research:
- Season ticket holders offer a unique source of revenue for sports teams. They offer an enormous upfront investment to the company. While they do not account for many of the customers, they do offer immense value. These customers tend to stay loyal, as long as they feel like they are getting a return on investment. These customers are more loyal to their brand than customers in other industries. Maintaining these assets, and obtaining more should be a major focus.

       
# Data Dictionary:
|Feature|Type|Description|
|---|---|---|
|**id**|int|contact ID number|
|**seat_end**|int|ending seat number|
|**seat_start**|int|beginning seat number|
|**number_seats**|int|number of seats|
|**num_years**|int|number of seats held|
|**renewed**|int|1 if the contact renewed, 0 if they did note renew|
|**attendance**|float|percent of games attended|
|**performance**|float|team overall performance|
|**tix_num**|int|number of tickets|
|**distance**|float|distance in miles from Pepsi center|
|**multiple_sections**|int|1 if contact had seats in multiple locations, 0 if only in one section|
|**lower_level**|int|1 if seats are in lower level|
|**club_level**|int|1 if seats in club level|
|**upper_level**|int|1 if seats in upper level|
|**gender_num**|int|0 if unknown gender, 1 if female, 2 if male|
|**season_years**|int|season years|
|**wins**|int|number of wins for that season|
|**ot_losses**|int|number of losses in overtime|
|**tenure**|int|number of consecutive years holding season tickets|
|**percent_total_used**|float|percent of tickets used by contact or given away by contact|
|**paid_in_full**|int|1 if paid in full, 0 if not|
|**flash_profit_loss**|float|profit made by selling tickets|


# Repository Structure:
> Included in this repository:
- Jupyter Notebooks
    - Season 5 cleaning
    - All seasons cleaning
    - EDA
    - Multiple Models
- data
    - csv with all posts
- README
- plots
- presentation slides

# Executive Summary:
- Data was obtained by Kroenke Sports & entertainment
- Raw data that was given was all tickets held by season ticket holders for seasons '14-'15,'15-'16,'16-'17,'17-'18,'18-'19. I began by aggregating all ticket data held by each contact for season '14-'15. I then created functions based on these methods to handle all seasons.
- Next I included season performance from [www.hockey-reference.com](www.hockey-reference.com) for each season. This included total points, wins, and overtime losses.
- I also included some additional contact info obtained from Kroenke, such as: percent of total tickets used, tenure, flash profit, and renewal for season '18-'19. This data was not attainable from the initial datasets.
- I then moved on to exploratory data analysis, looking at correlations and trends.
- Finally I created a few statistical models
       - Logistic Regression
       - Random Forest
       - Voting Classifier
              - Random Forest
              - Gradient Boost
              - ADABoost
              - Descision Tree
       - Neural Network
- I modeled using a training set of the first four seasons, testing on season '18-'19. This was my main method of modeling, as it is the most applicable, allowing Kroenke to predict next seasons renewals. These models performed at around 80-90% accuracy.
- I also tried modeling with randomly selected training and testing sets. These models performed significantly better (up to 98% accurate). However, these offered less value to the stake-holders.

# Findings/Conclusions:
- My majority class baseline score was about 79.5%.
- My best performing model gave me about 90% accuracy (when predicting next season).
- I was able to predict more accurately when randomly assigning testing and training sets.
- Some of the most important factors to season ticket renewal were: team performance, tenure, years holding season tickets, and distance from the Pepsi Center 

# Recommendations/Further Steps:
- In further iterations of this project, I would like to have access to more demographic data for the customers. I would also like to include weather data, and revenue/pricing information. Also, more data from other seasons would help as well.
- I would recommend focusing on finding ways to decrease the burden of commuting to the Pepsi Center. I would also find ways to attract new season ticket holders, as they tend to stay loyal. Obviously the performance of the team is a more complicated matter, but it remains of the utmost importance.

