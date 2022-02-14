
---
title: "Potential Struggles of Upstate Biotechnology Companies"
linkTitle: "Potential Struggles of Upstate Biotechnology Companies"
date: 2022-02-13
description: >
  Competition outside NYS and Conglomerates raise concerns of Biotechnology Startups
author: Eric Deopersaud
---

The disparity between New York State-based biotechnology companies and those out of state can be found in one recent investment round.

Alnylam Pharmaceuticals, located in Massachusetts and founded in 2002, [received $2 billion for research](https://www.biopharmadive.com/news/blackstone-alnylam-investment-inclisiran-heart-drug/575917/) and development of RNAi-based therapeutics for cardiovascular disease. Six hours away, Athenex, a biotech company located in Buffalo, N.Y., and created a year later, is also in the research and development market for novel therapies for treatment of cancer.

It had a [75.7% decrease in stock price](https://finance.yahoo.com/news/athenex-atnx-reports-q3-loss-144502496.html#:~:text=Athenex%20shares%20have%20lost%20about%2075.7%25%20since%20the%20beginning%20of%20the%20year%20versus%20the%20S%26P%20500%27s%20gain%20of%2024.1%25.) in this year alone.

According to [a November 2021 Crunchbase article by Janice Bitters Turi](https://news.crunchbase.com/news/biotech-vc-funding-startups-covid-vaccine/?utm_source=cb_daily&utm_medium=email&utm_campaign=20211115&utm_content=intro&utm_term=content&utm_source=cb_daily&utm_medium=email&utm_campaign=20211115), it can be said that, “investments into biosciences boomed with Covid.” This article highlights that since the start of the Covid-19 pandemic, global investments into biotech and healthcare industries drastically increased from $60 billion in 2019 to $82 billion in 2020 and through 2021 increased to $108 billion in investments. That’s an 80 percent increase in two years.

As the scope of biotech increased due to the Covid-19 pandemic, it still should be noted by investors what products a biotech company is developing and what unmet need is the biotech company fulfilling. It is apparent that the biotech sector needs investment to fuel research and development. Blackstone is a global investment firm which in recent years has piggy backed off the idea of biotech’s fulfilling an unmet need to the public.

It is clear that more importantly [what drives investment](https://www.biopharmadive.com/news/blackstone-autolus-cell-therapy-investment/609627/#:~:text=Now%20Blackstone%20is,increasingly%20crowded%20field.) into a biotech company is [knowing the science](https://www.forbes.com/sites/forbesbusinesscouncil/2021/10/28/biotech-investing-is-hope-fueling-hype/?sh=53f3a7827a05#:~:text=If%20one%20doesn%E2%80%99t%20have%20a%20strong%20background%20in%20either%20science%2C%20medicine%20or%20finance%2C%20investing%20in%20life%20science%20companies%20carries%20risks%20most%20people%20don%E2%80%99t%20understand.) behind effectiveness of a drug, vaccine, and therapy. Proper research is needed and even more so without a proper background in science, investment into a biotech will carry risks most people wouldn’t recognize without being directly involved in this field.

### METHODOLOGY

For this analysis, our main insight is to research biotech sectors along the supply chain from manufacturing to research and development to distribution. With this in mind, the NAICS code for each sector was used to produce a comparison of companies within and outside New York State. A NAICS code stands for the North American Industry Classification System in which companies are assigned based on their business activity. 

For the purpose of this research, the supply chain is defined with the following five NAICS codes:

- 325411 – Medicinal and Botanical Manufacturing
- 325412 – Pharmaceutical Preparation Manufacturing
- 541714 – Research and Development in Biotechnology
- 541715 – Research and development in Physical, Engineering and Life Sciences
- 446110 – Pharmacy and Drug Stores

To compare the companies outside New York State to those within New York State, a binary column was added manually along with the NAICS code and company names to distinguish them. A “0” was given to those companies outside New York State and a “1” to those within New York State. This binary column is acting as the dependent variable for this analysis. Along with these variables, the sales bracket of each company was taken from Bizminer.com, which gave a total of 20 different sales brackets ranging from $0 to more than $500 million.
	
From our preliminary exploratory data analysis, it was found that all five NAICS across the U.S. had 1,159 of 1,744 companies below the $5 million sales bracket, which is 66% of all the data points given. Of those found below the $5 million bracket, we also found a clear cluster of these companies happened to be chain pharmacies. These chain pharmacies included Walgreens, CVS, and Walmart.

{{< imgproc cluster Resize "660x340" >}}
{{< /imgproc >}}

With these duplicates of chain pharmacies included in the data, dimensionality reduction proved to be beneficial to our modeling. This technique is used to reduce the number of data variables in an attempt to retain the weight of the certain data on a predictive model. The removal of the pharmacy NAICS would yield a stronger accuracy outcome as it can be seen as possible competition for those companies not part of a chain within a predictive model.

### MODELING

The two strongest classification models for this analysis are K-Nearest Neighbors and decision tree algorithms. Classification models such as these are useful in categorizing labeled variables, which can then be trained and tested upon a new given data point. Using these classification models within this dataset will show that given the variables of sales bracket and NAICS code, we can assess if there is a clear distinction between companies within and outside New York State. 

Proceeding with the models, both classification models produced an accuracy of 67%. This initial model represented the entire dataset containing 1,744 companies along the biotechnology supply chain of the five NAICS codes represented. Given the variables of NAICS codes and sales brackets, each algorithm could predict that along the supply chain roughly 7 out of 10 biotechnology companies could be correctly predicted to be in or out of the New York State area. 

From the preliminary exploratory data analysis of the dataset it was shown that 27% (110/408)  of the pharmacy NAICS: 446110 belonged to chain pharmacies such as Walgreens, CVS, Walmart. Additionally, these chain stores also were seen to be at or below the sales bracket of $5 million - $7.49 million. The exploratory data analysis also showed 96 of the 110 chain pharmacies to be at or below the $5 million-$7.49 million sales bracket. The influence of these chain pharmacies may have perhaps been affecting the model as a whole. As a result of this finding, the pharmacy NAICS was removed in an effort to enhance the classification models.

With the removal of the pharmacy NAICS, the dataset had been reduced to four NAICS from the original five to incorporate dimensionality reduction, bringing the dataset without the pharmacy NAICS to a total of 1,336 records. This concept will reduce the dataset of the multiple chain pharmacies inhibiting the model, while still retaining the important parts of the data. 

The same classification models were then run on the reduced dataset and produced an accuracy of 72% for the K-Nearest Neighbors algorithm and 70% for the decision tree algorithm. The removal of the pharmacy NAICS enhanced the models by 5% and 3%, respectively. This finding further supports that the pharmacy NAICS was indeed an inhibiting factor on the classification models.

### DIMENSIONALITY REDUCTION

Reducing the data set has been shown to provide a more accurate model. Given the exploratory data analysis regarding the sales clusters, we see that 66% of  the companies as part of the supply chain reside in the bottom of the sales clusters. These sales clusters only contain six clusters below the $5 million mark as opposed to those companies producing more than $5 million in sales with 14 sales bracket clusters.

Noting this as we again run the classification models of K-Nearest Neighbors and decision tree; the accuracy for the models for the under $5 million brackets of K-Nearest Neighbors gave a result of 78% while that of the decision tree gave an accuracy of 75%. This final dimensionality reduction improved the accuracy of the models by 11% for K-NN and 8% for the decision tree model. 

**_As both models are classification models this shows that if a new startup were introduced into the supply chain we would be able to correctly predict if that company would be in or out of state 78% of the time given the K-NN model and 75% of the time given the decision tree model with annual sales being below the $5 million sales bracket._**

These models were able to increase in accuracy given the dimensionality reduction from the original five NAICS containing a total of 1,744 companies to four NAICS containing 1,336 companies. After the implementation of dimensional reduction was shown to improve the model; further reduction was found to be needed through exploratory data analysis given the compactness of companies on the lower end of the sales brackets. From here we found a total of 824 companies within the four NAICS to be under the $5 million bracket out of the 1,336 provided (62%). With those 62% of companies we then attained results that enhanced our accuracies from the original models by 11% and 8%.
	
The remaining 512 companies of the 1,336 (38%) were over the $5 million sales bracket. The accuracy for the remaining 38% of companies for both classification models results in a finding of 67% when trying to classify between New York State and out of state. This model did not differ from the model which contained all five NAICS and all 20 sales brackets. For the technique of dimensionality reduction, using four NAICS amongst those 14 sales brackets above $5 million did not show to improve the model. This finding substantiates that companies under that $5 million sales bracket are easier to distinguish to be in or out of New York State.

### CONCLUSION

From dimensionality reduction, the K-NN algorithm produced an accuracy of 78% while the decision tree algorithm produced an accuracy of 75%. These classification models calculated coupled with the graphs listed provide a telling story that New York State is lacking in the supply chain when it comes to the biotechnology sector.

While the models increased with dimensionality reduction, this shows that the classification of a new company into the market will be mostly out of New York State as most companies below the $5 million sales level were shown to be out of state. As we see from the strip plot, there is a telling sign of limited companies within the New York State area as most companies along the supply chain were shown to be outside New York State.       


{{< imgproc naics Resize "596x340" >}}
{{< /imgproc >}}

{{< imgproc us-nys Resize "595x275" >}}
{{< /imgproc >}}

The strip plot along with the violin plot show the distribution of the sales brackets between each NAICS code. From the violin plot showing the national breakdown of NAICS codes, we see the bulk of violin to be at the categorical number 4 Sales bracket. This sales bracket was for sales from $1-$1.99 million, which can be inferred as to why our models produced a much accurate rate when only below the $5 million sales bracket, indicating that the classification was leaning more towards out of state. Comparing this violin plot to that of NAICS within the New York State area there is a much slender look to the graph. This distribution shows that not only does New York State have to deal with companies outside the state but will also have to deal with major corporations within the state to be viable for success.

[Adagio Therapeutics](https://seekingalpha.com/article/4472270-adagio-therapeutics-market-crowded-lead-drug-candidate) is a prime example of a rather new company that has made its way in the market with breakthrough antibody based solutions against Covid-19. The struggle for Adagio Therapeutics is that they already may be late to the game. Conglomerates such as Pfizer, Johnson & Johnson and Moderna have already had their vaccines approved, while newly IPO companies like [Adagio are still waiting for FDA approval](https://seekingalpha.com/article/4472270-adagio-therapeutics-market-crowded-lead-drug-candidate#:~:text=The%20other%20big%20risk%20other%20than%20not%20getting%20FDA%20approval%20is%20the%20steep%20competition%20in%20the%20COVID%2D19%20space.%20It%20seems%20as%20if%20every%20single%20biotech%20company%20at%20least%20tried%20to%20do%20something%20for%20COVID%2D19). Even then it is not a certainty that their methods will get approved and the competition with big pharmaceutical companies will still exist.

_Eric Deopersaud is a fall research fellow in the New York State Entrepreneurial Ecosystem Group. He is a graduate of the Utica College Data Science Master’s Program. You can reach him at erdeoper@utica.edu or on [LinkedIn](https://www.linkedin.com/in/eric-deopersaud-1a50a4b5/)._
