# Predicting when NBA Stars will rest

*This was orginially a class project that I've been interested in continuing. All work is my own.*

![alt text](https://i.insider.com/5dc5e1623afd3701a027c603?width=1260&format=jpeg&auto=webp)
## Problem
Inactivity among NBA players has been on the rise in the past 5 years. While injury risk has remained relatively constant, the recent seasons have seen an uptick in star players electing not to take the court during regular-season games to mitigate the risks of injury and fatigue during the playoffs. Modeling the likelihood that a player takes the court for a given game can be advantageous for opposing teams who can develop gameplans around the lineup they’re most likely to face as opposed to the best lineup their opponents can assemble. It also has applications in sports betting and fan experience, where fantasy lineups are set with this information in mind, and insurance policies are being offered to those who purchased tickets in the event a given player does not take the court. Our goal is to utilize neural networks to build a model that predicts whether a given player will sit out for a particular game. Currently, similar existing models rely on logistic regression but could be developed using any machine learning solution aimed at binary classification, including neural networks.

## Research
- [Load management is the NBA’s hottest term. What does it mean?](https://www.sbnation.com/nba/2019/11/8/20954096/load-management-definition-kawhi-leonard-lebron-james-fines-controversy) (Matt Ellentuck, SBNation (2019))

This article details the creation of the DNP-rest tactic started by the San Antonio Spurs in 2012 and the backlash received from the league and its fans, but, more importantly, describes how and when it is utilized. With the league’s grueling 82 game schedule combined with constant traveling and time-zone changes, **teams with good positions to make the playoffs are more inclined to bench their top players in hopes of improving future playoff game chances.** Factors like nationally broadcasted games may take affect if stars are less likely to be benched, but star players still occasionally rest these games nonetheless. Compromises of improving the league’s schedule are nowhere in sight and the loosening grip of league fines means coaches will be more likely to bench their stars while fans are at greater risk of missing out on watching their favorite athletes play. 

- [Game injuries in relation to game schedules in the National Basketball Association](https://www-sciencedirect-com.proxy01.its.virginia.edu/science/article/pii/S1440244016301633) (Teramoto et al (2017))

This study set out to examine the association between NBA players’ game schedules and their injuries experienced during the 2012-13 & 2014-15 regular seasons. A Poisson regression analysis was used to predict the number of injuries sustained by each player based on game schedules and the players’ profiles. They found that playing **back-to-back away games were significant predictors of frequent game injuries (p < 0.05)** and the **odds of such injuries were 3.5 times higher than the odds of those occurring in home games.** Working under the assumption that team coaches are aware of the added injury risk from back-to-back away games, we felt that incorporating this information into our model design is critical. 

