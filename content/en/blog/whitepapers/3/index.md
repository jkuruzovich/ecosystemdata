
---
title: "Cybersecurity Growth is Accelerating — In Some Places"
linkTitle: "Cybersecurity Growth is Accelerating — In Some Places"
date: 2022-02-13
description: >
  The Complexities in Predicting Investment Success is Cybersecurity Startups 
author: Aaron Harold
---

During the COVID-19 pandemic, companies in every industry turned to technology to ensure their survival. According to a December 2020 survey by the Pew Research Center, work from home (WFH) increased 51% from 20% to 71% for workers who said they could perform their job responsibilities at home. However, as companies shifted to a more technology-driven, WFH business model, they inadvertently increased the attack surface for cyber criminals.

Cyber criminals [overwhelmingly employ ransomware](https://atlasvpn.com/blog/ransomware-accounts-for-81-of-all-financially-motivated-cyberattacks-in-2020) as the means to extort companies of funds. According to cybersecurity vendors BitDefender and CoveWare, the number of ransomware attacks [increased by 485% from 2019 to 2020](https://www.bitdefender.com/files/News/CaseStudies/study/395/Bitdefender-2020-Consumer-Threat-Landscape-Report.pdf) while the average ransom payment increased [43% from Q4 2020 to $220,298](https://www.coveware.com/blog/ransomware-attack-vectors-shift-as-new-software-vulnerability-exploits-abound). Most concerningly, [75% of companies](https://purplesec.us/cyber-security-trends-2021/#Ransomware) that were victims of ransomware attacks were running up-to-date endpoint protection on their systems. Overall, the [total cost of a successful ransomware breach](https://atlasvpn.com/blog/ransomware-accounts-for-81-of-all-financially-motivated-cyberattacks-in-2020) in 2020 was $4.44 million.

The cybersecurity industry has been innovating at a record pace to adapt to the increased technology demands of customers. According to Crunchbase, U.S.-based cybersecurity companies raised [$5.9 billion](https://about.crunchbase.com/cybersecurity-research-report-2021/) in 2020 while total global venture funding was [$7.8 billion](https://about.crunchbase.com/cybersecurity-research-report-2021/). Six new cybersecurity unicorns emerged with five located in the United States and one in New York City. This five-year old unicorn, BigID, specializes in private data management and has raised over $200 million in funding.

The pace has not slowed in 2021. According to Crunchbase, [$9 billion and 309 deals](https://news.crunchbase.com/news/funding-pours-into-cybersecurity-as-first-half-numbers-eclipse-last-years-total/?utm_source=cb_daily&utm_medium=email&utm_campaign=20210720&utm_content=intro&utm_term=content&utm_source=cb_daily&utm_medium=email&utm_campaign=20210720) have flooded the cybersecurity market. Nine new cybersecurity unicorns were minted, two of which are located in New York City and possessed a [total valuation of $2.6 billion](https://about.crunchbase.com/cybersecurity-research-report-2021/). [Socure](https://about.crunchbase.com/cybersecurity-research-report-2021/) is eight years old and provides asset management and security policy enforcement while [Axonius](https://about.crunchbase.com/cybersecurity-research-report-2021/) is only four years old and provides digital customer identity verification.

Cybersecurity is an extremely broad field. As the cyber attack surface grows due to the global increase in reliance on technology, cybersecurity companies that can counter these new threats and meet customer needs will continue to grow and profit for years to come.

### Cybersecurity Revenue Growth in New York is Accelerating — Just Not in Upstate

According to Crunchbase, cybersecurity funding in New York State increased 63% from 2019 and accounted for [15% of total US cybersecurity venture funding](https://about.crunchbase.com/cybersecurity-research-report-2021/). However, tracking the activity of cyber-specific companies is problematic. Unfortunately, cybersecurity [does not have a dedicated NAICS code](https://defensecraft.net/cybersecurity-and-naics-codes/) because NAICS codes (North American Industry Classification System) are production-oriented while cybersecurity is process-driven.

Through our research, we found that cybersecurity companies are mainly distributed among four different NAICS: 511210: Software Publishers; 518210: Data Processing, Hosting, and Related Services; 541511: Computer Programming Services; and 541512: Computer Design Services.

We used Bizminer, a financial and market analysis company, to gather data for this analysis. Bizminer provides a snapshot of a NAICS’s sales performance and 250 companies within a certain Metropolitan Statistical Area (MSA). We aggregated companies from New York City, Rochester, Syracuse, Utica, Buffalo, and Albany for our analysis. The key variables for our methodology were sales brackets, company filing date, and the company county location. We further reduced the company county location to three areas: Upstate New York, which encompassed the entirety of upstate; TriState New York, which encompassed the eight major counties in the New York City MSA (New York, Kings, Queens, Bronx, Suffolk, Nassau, Westchester, and Richmond); and global, which encompassed any company that was not founded in New York but operates an office within New York City.

We transformed the sales brackets into categorical values which were used for the analysis. The sales bracket categories are listed below.


{{< imgproc sales-bracket Resize "404x420" >}}
{{< /imgproc >}}

### Snapshot: Upstate New York

Upstate New York has not seen much growth from companies in the four cybersecurity NAICS. Since 1995, the region has not been a hub for cybersecurity companies that generate large amounts of sales compared to other parts of the country, even with a [robust and growing higher education sector](https://www.govtech.com/education/higher-ed/cybersecurity-studies-increasingly-popular-at-us-colleges) focused on this discipline. The rate of new companies being founded has slowed while median sales have hovered between $1-$2 million for the last decade. Mean sales rose 433% from $600,000 to $2.6 million between 2016 and 2018 but have since declined back to $600,000.

{{< imgproc company-count-mean-upstate Resize "660x373" >}}
{{< /imgproc >}}

{{< imgproc company-count-median-upstate Resize "660x373" >}}
{{< /imgproc >}}

### Modeling Results

We ran Poisson regression and found that total and mean sales were both significant independent variables when determining the number of companies being founded per year. Poisson regression uses model count data and contingency tables in its analysis. The model had a deviance squared (D2) score of 0.9154% meaning 91.54% of deviance found was explainable by the two independent variables. The model indicated that company counts are higher in years when total sales are high but yearly sales mean is low. The model and data additionally showed that after a year with mean sales lower than 2.3 ($500k-$999k), the subsequent year experienced a double-digit number of companies being founded.

After evaluating the last 25 years, the algorithm can predict that there will be over 10 new startup companies founded within the four NAICS that encompass cybersecurity in 2021 in Upstate New York that will generate sales. These companies will achieve a mean sales rate between $500k and $999k. This may allow more targeted investment and help with conserative estimates and expectations.

### Snapshot: Tri-State New York

The rate of new companies being founded in the New York Tri-State area (New York, Kings, Queens, Bronx, Suffolk, Nassau, Westchester, and Richmond) also slowed. However, mean sales generated by companies founded during 2019 increased by 350%, from a mean of $2.5-$8.75 million, according to the analysis. These same companies generated a median sales growth of 500% from $2-3 to $10-15 million. Mean sales retreated by 8% for companies founded in 2020 while median sales shrank by 60% but still remained 100% higher than the 2018 median rate.

{{< imgproc company-count-mean-tristate Resize "660x373" >}}
{{< /imgproc >}}

{{< imgproc company-count-median-tristate Resize "660x373" >}}
{{< /imgproc >}}

### Modeling Results

Similar to the Upstate area, both total and mean sales were found to be significant when used to determine companies founded year-over-year in the Tristate area. The D2 score was slightly higher at 91.87%. The modeling results were similar to Upstate in that company counts were higher in years when total sales were high while sales mean was low. However, a higher sales mean had less of a deleterious effect on company founding rate as it did in the Upstate area.

After evaluating the last 25 years, the algorithm can predict that there will be at least a 60% increase in startups within these four NAICS in 2021 that will generate sales. These companies will have a mean sales range between $7.5 and $15 million. This may allow more targeted investment and help with investment strategies to determine the optimal number of companies to invest in.

### Probability of Cyber Startup Success

While predicting yearly company founding rates is useful, what is the probability these companies will be successful? For our analysis, we created a random forest model that assessed whether a company within each NAICS would surpass $5 million in sales. We chose the random forest algorithm because of its usefulness when evaluating non-linear data and its resilience to outliers. We further separated the probability into Upstate, Tristate, and global subcategories, with global being a national or international company that possesses an office in New York. This last cluster is important to include because it illustrates the difference in sales impact between companies that were founded in New York versus pre-existing companies that simply set up a satellite office in New York City. It’s expected that a national or global company’s office in New York would have a revenue-generation advantage because they possess name recognition and a proven track record of sales in other locales. 

The random forest algorithm achieved an accuracy of 80.67% when predicting whether a startup company in New York State would hit $5 million sales. The following table indicates the probability of a company within one of the four cybersecurity NAICS achieving $5 million or more in sales in each geographic region:

|  	| Software Publishers-<br>511210 	| Data Processing, Hosting, and Related Services-<br>518210 	| Computer Programming Services-<br>541511 	| Computer System Design Services-<br>541512 	| Overall Probability Regardless of NAICS 	|
|---	|---	|---	|---	|---	|---	|
| Global 	| 49.77% 	| 12.60% 	| 12.59% 	| 19% 	| 23.49% 	|
| Tristate 	| 52.52%<br> 	| 20.73% 	| 16.38% 	| 26.21% 	| 28.96% 	|
| Upstate 	| 16.42% 	| 3.08% 	| 7.85% 	| 9.19% 	| 9.14% 	|

Modeling revealed that companies founded in the Tri-State area of New York had the best chance of achieving sales of $5 million or more with an average probability of 28.96% regardless of NAICS. This is 19% more likely than a global company’s office within New York and 69.54% more likely than a company founded in Upstate New York. 

The Upstate result was expected because large profit-generating cybersecurity companies target New York due to the large potential client base and global exposure. However, it defies conventional thought that Tri-State founded companies outperform companies that already have a national or global presence and decide to open an office in New York. 

### Future Projections and Research

The models that were used were based on Bizminer reporting which only displays 250 companies per MSA. Additionally, revenue growth was only published as a year-over-year figure. Future analysts could aggregate more companies from these four NAICS into the model and incorporate quarterly earnings instead of yearly numbers to more accurately reflect revenue growth over time. Given enough time and additional data, this model could be used across the country to analyze bifurcated entrepreneurial communities such as NYC cybersecurity startups versus cybersecurity startups in the rest of New York State.

This is important to note because the entirety of the cybersecurity market has not yet begun to mature. In an April 2021 cybersecurity market analysis report, Grand View Research asserted that the cybersecurity industry will increase at a [steady 10.9% compound annual growth rate (CAGR) from a 2021 revenue of $179.96 billion to a 2028 revenue of $372.04 billion](https://www.grandviewresearch.com/industry-analysis/cyber-security-market).

Evidence of this growth is readily present in New York State. New companies are achieving higher sales revenues faster and startups have a higher percentage chance of reaching over $5 million in sales than already established national/global companies. However, this trend is only reflected in the Tristate area. Upstate New York cybersecurity markets remain stagnant as money flows toward Tristate area startups and unicorns. The Upstate cybersecurity market is still developing but is hindered by the profit potential of establishing an office within New York City limits.

_Aaron Harold is a summer research fellow in the New York State Entrepreneurial Ecosystem Group. He is a Navy veteran and graduate of the Utica College Cybersecurity Master’s Program._
