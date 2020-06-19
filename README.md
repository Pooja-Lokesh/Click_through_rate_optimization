# Reinforcemnet_learning


* we have n number of ads that we display to users each time they connect
to a web page 
* each time a user connects to the web page, that makes round
* at each round r, we choose one ad to diplay to the user
* at each round r, ad i gives a reward. it is 1 if the user
clicks on the ad i, 0 if the user didn't.
* our goal is to maximize the total reward we get over many rounds 


UPPER CONFIDENCE BOUND 

every ad has a distribution, the algorithm explores and exploits 
the ads in order to choose the ad with the highest return 
the algorithm constructs a confidence band , and a random value for the distribution
of the ad.
the confidence interval gets smaller, that is we get more confident about the distribution 
that particular ad has, and the predicted distrubution of the ad gets closer to the actual distribution 
with series of rounds of exploring and exploiting 
it is a deterministic algorithm 
requires update at every round 


THOMPSON SAMPLING 

every ad has a distribution, the algorithm explores and exploits 
we have no prior knwledge of the distribution
by taking into consideration some trials made on that particular ad,
that is considering some returns on that ad, the model constructs a distribution for it (it is where the model thinks the mean value lies)
it is a probabilistic algorithm 
the model exploits the ad which has the highest return according to the 
current distribution cosntructed.
it takes in the returns from every round , and alters it's distribution
accordingly. This way the model changes its perception for every round
and constructs a narrower distribution which is close to the actual distribution
this can accomodate delayed feedback 
