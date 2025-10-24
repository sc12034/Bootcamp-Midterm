# Bootcamp-Midterm
Group members: Isabella Gu, Thomas Liu, Josh Cho

# Intro 
Our overall goal was to see if 1) there was a relationship among the prices of eggs, milk, and bread, and 2) there was a relationship between the interest rates and the prices of these items. Our rationale was that these are common goods that American consumers regularly purchase, so we wanted to explore whether their prices were related to one another. Additionally, interest rates are usually a signal of the economy’s strength. Thus, we wanted to see if the prices of these commodities would change in conjunction with interest rates. As essential household consumables, these items typically exhibit inelastic demand; regardless of economic conditions or price changes, consumers are likely to continue purchasing them. 

We had two initial predictions. First, we hypothesized that there would be a strong relationship between interest rates and commodities’ prices. The reasoning was that higher interest rates would be associated with lower spending on these items because households would have less disposable income. Second, we predicted a strong correlation among egg, milk, and bread prices, as they are all basic food staples, with their costs influenced by similar factors affecting supply, such as production costs, transportation, and agricultural innovations.


# Methods
To analyze the relationships, we used two datasets for interest rates and commodity prices. The interest rate data, specifically Treasury Inflation Protected Securities (TIPS), were extracted from the US Treasury website. This data was downloaded in JSON format and processed to create a pandas dataframe of observation dates and corresponding interest rates. Data on commodity prices were downloaded from the St. Louis FRED database via a Drive path. This included the yearly average prices for a dozen eggs, a gallon of milk, and a loaf of bread in the United States from 1980 to 2025. We then merged these data on dates to create a dataframe that allowed us to compare dates, interest rates, and item prices directly.

After loading and cleaning the data in Python, we first graphed the individual trends of each commodity, which showed the overall trend and could later be used for further analysis. We then aimed to compare the prices of the commodities; thus, we plotted all three on the same graph and created scatter plots comparing each pair: eggs vs milk, eggs vs bread, and milk vs bread. Additionally, after calculating the correlation between the items, we crafted a correlation heatmap to better visualize our findings. 

To compare the interest rate to each of the commodity prices, we merged the two datasets by year, and proceeded to create three scatter plots, which had the interest rate on the x-axis and each of the commodity prices on the y-axis. This allowed us to analyze the correlation (if any) between each commodity and the interest rate, thereby preventing us from generalizing, as different goods may have other relationships with the interest rate. We then computed the correlation coefficients and p-values to test whether a correlation existed and whether our hypothesis was true.


# Results/Findings

After accessing and loading data, we first visualized the prices of all three together to see if there were any prominent trends. We then produced scatter plots to illustrate the prices of all three items against each other, one-on-one. From these graphs, it was clear that there existed a strong correlation among item prices.
	
Although all three commodities exhibit significant volatility, our line graphs show that the prices of all three commodities rose significantly from 1980 to 2025, suggesting the effects of inflation and rising production costs. Moreover, the volatility of egg prices was notable, with significant spikes during the early 2020s, likely due to nationwide bird flu that reduced supply. In contrast, milk and bread prices rose steadily, with few spikes. However, when all three goods were plotted together, they followed a similar pattern, which indicated that items in similar categories respond to similar market forces.

We found that the prices of eggs, milk, and bread are highly correlated, as confirmed by correlation matrices and hypothesis tests. We quantified these relationships by generating correlation matrices, which confirmed that there were indeed strong correlations among item prices, with many coefficients close to 1. To rigorously determine whether there was indeed an association between commodity prices, we also ran a hypothesis test to assess whether the correlations between the variables were significant, and found that all yielded substantial results. Therefore, it is apparent that there is a clear connection between eggs, milk, and bread products. 

In terms of correlation with interest rates, the studied commodities, eggs, bread, and milk, show extremely low correlations. The correlations with interest rates for eggs, milk, and bread are 0.035, -0.021, and 0.028, respectively, with p-values of 0.879, 0.926, and 0.902. This indicates that the null hypothesis is that interest rates do not significantly affect eggs, milk, or bread. 

 Why does this make sense? Once inflation occurs, interest rates fluctuate in response to the Federal Reserve's efforts to target it. This means that there is an implementation and decision lag for the Federal Reserve to react to inflation. This would result in periods when inflation is high, and the interest rate increases shortly after, even though higher interest rates should decrease inflation. This also means that the implementation of interest rates is highly bureaucratic and inconsistent, leading to a lower correlation between these commodities and interest rates. However, this doesn’t fully interact with or disprove our original prediction that interest rates affect price changes, as interest rates simply take time to have their effects. 

Overall, we found that the three items had high internal correlation, likely due to their similar production systems, and low external correlation, as the price did not change significantly in response to policy changes. 



# Applications of Findings
	Given that the goods are linked, policymakers and consumers can monitor food affordability. For example, eggs can be used as a proxy to determine the general price of food. This means that when determining fiscal and monetary policy, policymakers can examine egg prices to measure the overall health and affordability of groceries. Consumers may also find utility in these findings because if the price of one item changes, they can have an approximation for how the price of another item will be affected. Other products, such as cakes and those containing eggs and milk, will also change and can be inferred from this correlation. Small businesses can also use the correlation proxy to adjust prices to gain a competitive advantage across multiple products. 

# Limitations
There are a couple of limitations in our modeling and findings. First, when analyzing the affordability of basic goods like milk, eggs, and bread, inflation isn’t the sole determinant. For example, in 2008, inflation was surprisingly low at around 1-2%. Still, goods were increasingly unaffordable as people lost their pensions, their jobs, and, obviously, their homes, so they still couldn’t afford them. 
Second, there are many possible alternatives to explain the correlation between the commodities that aren’t causal. The most obvious one is that inflation affects all of them equally, as inflation is economy-wide. This results in them all fluctuating similarly over a timeframe. Second, commodities (such as milk, bread, and eggs) are produced on farms and are subject to those supply constraints and shocks. So, insofar as these explanations have some validity, they potentially discredit the causality indicated in the correlation matrix. 

# Future Exploration of Data
	One thing we wanted to analyze but ran out of time to do was create regression models for the prices of individual items against each other. For example, we wanted to create a model that could estimate egg prices based on bread prices. This would be helpful for consumers who wish to predict, with a relatively high degree of accuracy, the cost of certain goods based on fluctuations in other items. We were also considering comparing these to other economic indicators to see what affects the average American consumer. These include economic growth, unemployment, and potentially labor statistics such as wages and participation rates. 



