# fare_vs_survival

I was tasked with predicting the survival of passengers using their fare, gender, and child status.

To tackle this challenge, I trained a logistic regression model using R. But here's the exciting part: during the project, I discovered how a skewed variable could significantly affect the performance of the model. In this case, the fare variable was right-skewed, so I had to transform it with a log.

To test the impact of this transformation, I trained two logit models. The first one used the original fare variable, while the second one used the transformed fare variable. Thanks to R's powerful statistical tools, I could evaluate the performance of both models. And guess what? The second model (Model 2) using the transformed fare variable performed better than Model 1, with a higher log-likelihood and lower AIC value.

But that's not all! I was also able to visualize the effects of the fare variable on both models using the effects package in R. The graph with the original fare variable suggested that the effect of fare on survival was more linear. That is, for every one-unit increase in fare, the log odds of survival increase by a constant amount (or that the change in the dependent variable, survival, is proportional to the change in the independent variable, fare). However, the graph with the transformed fare variable revealed that the effect of fare was non-linear, with the log odds of survival increasing at a high rate as fare increased. Based on these findings, I found the second story more plausible.

To confirm if the fare variable was crucial to the model's performance, I retrained two models. The first model only used the female and child variables, while the second model included the log(fare) variable. The second model had a higher log-likelihood and lower Akaike Inf. Crit. value, indicating better performance. To further evaluate the performance of both models, I used a ROC curve. The curve for the model with the fare variable was higher and closer to the top left corner of the graph, demonstrating better performance.

Overall, working on this project was an exciting and rewarding experience. I improved my R skills and learned a lot about statistics. It just goes to show how even a simple variable transformation can make a significant difference in the performance of a model.
