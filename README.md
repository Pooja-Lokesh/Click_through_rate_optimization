# Customer fit ad 

## Steps followed 

* We have n number of ads that we display to users each time they connect to a web page.
* Each time a user connects to the web page, that counts as a round.
* At each round r, we choose one ad to diplay to the user.
* At each round r, ad i gives a reward. The reward is 1 if the user clicked the ad, if not the reward is 0.
* Our goal is to maximize the total reward we get over many rounds 


## Upper confidence bound 

- This is a deterministic algorithm.
- Every ad has a distribution, which the model is trying to determine.
- The algorithm explores and exploits the ads in order to choose the ad with the highest return.
- The algorithm constructs a confidence band, and a random value for the highest return of the ad.
- With series of rounds of exploring and exploiting the confidence interval gets smaller, i.e. we get more confident about the distribution of that particular ad, and the learned distrubution of the ad gets closer to the actual distribution.
- This algorithm requires update at every round. 


## Thompson sampling 

- It is a probabilistic algorithm.
- By taking into consideration some trials made on that particular ad, i.e. considering some returns on that ad, the model constructs a distribution for it (it is where the model "thinks" the mean value lies).
- The model exploits the ad which has the highest return according to the current distribution constructed.
- It takes in the returns from every round or even when there is a delayed feedback, and alters it's distribution accordingly. 
- This way the model changes its perception for every round and constructs a narrower distribution which is close to the actual distribution
