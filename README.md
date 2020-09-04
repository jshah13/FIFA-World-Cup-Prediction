# 2018 FIFA World Cup Predictor

![image](https://user-images.githubusercontent.com/45533954/92206834-0e380b80-ee80-11ea-8bda-abfd95769dc0.png)

## Objective
To predict the outcome of the 2018 Fifa World Cup.

## Data and Model
The data used incudes historical results from international football since the 1993-94 season till the end of the 2017-18 season i.e. the lead up to the world cup. The model used here is a logistic regression to predict the outcome of individual matches. I selected this model since this is a multilabel classification problem (win; draw; loss) where the features used are the results between matches between different ranked sides. This gives the probability of the home team winning - if over 60%, it predicts a win; between 40-60% is considered a draw in the group stage. In the knockout stages there are no draws so if the probability is over 50% for either side it will predict a win.

![image](https://user-images.githubusercontent.com/45533954/92206978-548d6a80-ee80-11ea-933e-250cfbdd1950.png)

## Results

As you can see below, the prediction was a little off since Germany actually got knocked out at the group stage of the tournament and France won the tournament, while Brazil were knocked out by Belgium in the quarter finals. The reasons for this relatively poor performance are two-fold:
- Firstly, the model and data used were overly simplistic since it used the FIFA ranking of the nations in order to predict which team would win, which explains why the two top ranked teams prior to the tournament were predicted to reach the finals with the number one ranked team winning. Whilst this may be a good way to predict results between teams that are far apart in rankings such as Germany and South Korea (albeit there was a shock this time), when two top ranked teams face off the differences are far more nuanced and so a simple model such as this would be insufficient for predicting the result accurately.
- Secondly, this world cup had a lot of shocks - no one could've expected Germany to be knocked so early in the tournament. This was the first time since the 1930s where Germany was knocked out at the group stage for example. Shocks are difficult to factor into models.

**Prediction**

![image](https://user-images.githubusercontent.com/45533954/92147181-a39cb680-ee12-11ea-980a-0ffd3e33fcf5.png)

**Actual**

![image](https://user-images.githubusercontent.com/45533954/92147630-4f460680-ee13-11ea-9744-11a3fc403f41.png)

## Next Steps
As mentioned above, this model is overly simplistic as it uses the relative rankings of the teams to predict the winner and so in order to progress this model, it would be best to include some other features related to each team's strengths and weaknesses such as the average age, international caps, or some other player specific features such as football manager ratings to establish the quality of the players. Alternatively, we could perform some sentiment analysis based on recent newspaper articles to determine how the world media sees each team's chances (no one predicted Germany to go out that early though!).

