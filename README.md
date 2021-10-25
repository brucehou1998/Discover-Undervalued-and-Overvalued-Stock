# Discover-Undervalued-and-Overvalued-Stock

Value investing, an investment strategy that originates from Benjamin Graham and Warren Buffet, picks stock based on its ‘intrinsic value’. Investors who follow this approach calculate ideal stock price with the analysis of financial ratios, internal, and other external factors; and compare it to current stock price. They invest 'undervalued stock', whose ideal price is higher than current price, while divest ‘overvalued stock’, whose ideal price is lower. However, increasing numbers of companies’ disclosures and news make manually reviewing all related information impossible. This project aims to automate all stock selection processes with unsupervised machine learning models. Our analysis could generally define both overvalue and undervalue stocks with data analytics approach.

### Method

The dataset contains 500+ US companies and 30+ financial ratios. We first clean our dataset by filling null values with 0. Next, we compute correlation between financial variables and stock price. Financial factors that are moderately (0.4 < r < 0.7) or highly (r > 0.7) correlated with stock price will be selected to feed into unsupervised machine learning model. (For more information, please check Fig. 1 in the pdf file.) Within the model, we conduct various types of clustering methods. We choose “Cosine” + “Complete” for categorizations of stocks and separate stocks into 8 groups given their well-performed clustering results. 

### Result

After completion of stock categorization, we analyze stock’s intrinsic value based on its relationships with highly and moderately correlated financial ratios. Within the measurement of highly correlated variables, stocks in cluster 2 possess the highest financial ratios (EPS, Book value of equity per share, free cash flow per share) on average, and the highest stock price on average. As large values of financial ratios stick to high stock price and vice versa, no undervalued or overvalued stocks is detected in this case. (For more information, please check Fig. 2 in the pdf file.)

Moderately correlated variables indicate a different result, however. Shareholders’ equity, Earnings available for common stockholders, and Earnings are high in cluster 7 while its stock price is relatively low. Given that high financial ratios do not reflect on stock price, we may regard stock in cluster 7 as undervalued. Comparatively, financial ratios appear low in cluster 2 while its stock price is abnormally high. We may consider stock in cluster 2 overvalued. (For more information, please check Fig. 3 in the pdf file.)

### Challenges of Analysis and Business Suggestions

Evaluation of stocks with listed financial factors may be biased and could not precisely reflect ‘true value’ of stocks. Though we already proved those variables are positively correlated with stock price, we are unsure if they make sense from an investment perspective. Also, we calculate ‘average’ of stock price and financial factors for each group while do not capture the ‘range’ and ‘standard deviation’ of data. Thus, result regarding overall value of a cluster may differ from value of individual company. 

Even though cluster 7 is indeed undervalued and cluster 2 is truly overvalued, we could not recommend investing in the former while divesting the latter. Undervalued stock could remain undervalued for a long period of time, which will not generate profit. Similar theory applies to overvalued stock, these companies could stay at a high price, which gives no persuasive reasons to sell. Moreover, our analysis does not measure factors other than finance, including but not limited to business model, future growth, and industry. These factors could play an equally important role in changes in stock price.

Overall, this model can merely pre-screen overvalued and undervalued stocks. We will recommend investment firm commence further analysis for individual stocks before making investment decisions.
