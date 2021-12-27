# Green Stocks Analysis

## Overview

This analysis seeks to identify publicly traded green energy companies whose stocks yield promising returns. The intent is to advise the average investor on which green energy companies may be worth investing in based on the companies' return performance over the course of a given year. A secondary purpose of this report is to note the improvements in run time of the analysis provided by refactored VBA code.
## Results

### Stock Performance

For this report, stock performance for twelve companies was analyzed for calendar years 2017 and 2018:    

![VB_Challenge_2017_table.png](https://github.com/jamariethomp/stock-analysis/blob/main/images/VB_Challenge_2017_table.png)
![VB_Challenge_2018_table.png](https://github.com/jamariethomp/stock-analysis/blob/main/images/VB_Challenge_2018_table.png)

As seen above, the two companies with consistently positive rates of return for their stock value are ENPH and RUN.  Both appear to be worthy companies in which to invest. 

While many of the other stocks appeared to have substantial returns in 2017, such as DQ and FSLR, returns in 2018 showed some volatility in these and several other stocks that performed much better in 2017 than they did in 2018. Investment in these stocks would not be recommended for the average investor seeking low-risk investments.

### Refactored code

A secondary purpose of this report is to summarize the success of the refactored code used to run analyses on both sets of data.  With the original code, the run time was a bit sluggish:

!(https://1drv.ms/u/s!Atn0xQEMWw1l2hl4MkrIbMWhATo1)

Under the refactored code the run time improved significantly, which will come in especially handy once more data needs to be analyzed:

!(https://1drv.ms/u/s!Atn0xQEMWw1l2hrqPI9uTKrqa2vt)

One significant change that was made was to the code was the removal of nested loops in favor of reiterating the ticker index by increasing the value at the end of each loop:

!(https://1drv.ms/u/s!Atn0xQEMWw1l2hfKJVkqoKj4JSTy)

Initializing the output arrays as dynamic variables also aided in the improvement of the run time:

!(https://1drv.ms/u/s!Atn0xQEMWw1l2hiodGh6ilFWu-b5)

Clearly, where loops can be reduced, code can potentially be more efficient.
## Summary
-	Overall, less volatile stocks with consistently positive returns would be recommended for the average investor. ENPH and RUN are particularly recommended.
-	While refactoring code can be a timesaver at the end of the day, it might require a lot of time and patience to refactor particularly complex code. Before refactoring already usable code, an analyst would want to weigh the costs and benefits of spending a significant amount of time on refactoring. Indeed, with particularly large datasets, refactoring long-running code could quickly become a necessity.
-	The original code for this analysis performed well for the datasets at hand and is relatively simple for the average data analyst to comprehend. This is beneficial especially if multiple people are needed to analyze and tweak the code. The refactored code is shorter and more concise, yet more difficult to comprehend. Depending on what changes might need to be made to accommodate new information, one code may easily be preferable over the other.
