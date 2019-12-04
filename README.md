# Predicting Avalanche Season Ticket Renewal
![picture](https://cdn.vox-cdn.com/thumbor/bWRoJBG0GQDKzy0_jwDojxmtJ4A=/0x0:1099x733/1820x1213/filters:focal(0x0:1099x733):format(webp)/cdn.vox-cdn.com/uploads/chorus_image/image/16269859/3d_photo_conc_pepsi_center_avalanche_final.0.jpg)
Photo from [milehighhockey.com](https://www.milehighhockey.com/2013/7/11/4514554/pepsi-center-gets-digital-overhaul)

### Authored by: Jeff Thomas

# Problem Statement:
- The purpose of this project is to create a classification model to predict whether a current Avalanche season ticket holder will renew for next season. I will measure success of the model against the baseline (majority class).

# Background research:

       
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
    - Cleaning and EDA
    - Multiple Models
- data
    - csv with all posts
- README
- plots
- presentation slides

# Executive Summary:
- 

# Findings/Conclusions:
- My RMSE baseline score was 0.0060.
- My best performing model gave me about 0.0033.
- Year and CPI were the most highly correlated features
- When using year alone as a feature, I achieved about half the test score of all features combined

# Recommendations/Further Steps:
- In further iterations of this project, I would like to spend more time aquiring more data. I would like to have features such as tax rates, average income, average savings, interest rates, etc.
- I would also like to take some time to perform an A/B test to see if my findings are significant.
