### Kevin Regan
# TEU Growth Rate by Ports


#### Abstract:
90% of the world’s goods are transported on shipping containers which are incredibly heavy weighing upwards of 4k to 9k pounds. As a result, repositioning, repairing and storing a shipping container can be costly, if at the end of their contract or useful life are not redelivered to (i) high resale locations and (ii) low repair cost locations. This study seeks to determine whether Annual TEU volume can be predicted accurately and to discover which ports offer the greatest growth potential. 

#### Dataset: 
The dataset was comprised of the top ~90 port locations throughout the world in terms of annual TEU (20ft equivalent Shipping Containers) volume ranging from 1.67 million to 50 million TEU per annum from 2020 to 2024. As a proxy for labor cost and property values local wages in USD and median home values were used. The intention of these proxies is to approximate repair labor costs and facilities costs. All values are in USD. Additionally, this data includes TEU growth rates for each year as well as the CAGR (Cumulative Annual Growth Rate). One leading source of information was from www.worldshipping.org/top-50-ports

#### Methodology:
Data Collection: Most of the top ports in the world list their annual TEU publicly although there are various sources that collate/ aggregate this information. Including [Source 1] and [Source 2]
Analysis: Used pythons in-built descriptive statistics to obtain median, skew and kurtosis. As well as produced a variety of kernel density plots to understand the distribution of shipping container TEU, in addition I also computed a correlation Matrix, where I was surprised to see that the yoy correlation for all four years is nearly 1.0 with the minimum being .99. As a result of the high correlation it appears that ports maintain their TEU rank and magnitude consistently year over year. It also means, that recent history will be an excellent predictor of next year’s TEU. See Exhibit 1 for more information.  

#### Results: 
Regression(s) on historic port volume yielded an average R2 ranging between .68 and .81 in the aggregate.  
•	Individual R2 scores were upwards of .99 indicating a high degree of predictability and stability especially with our outlier classified groups which including multiple ports in China and one in Singapore.
•	Quanzhou Port in China is notable for three reasons. 
o	Its cumulative annual growth rate is 23%, the highest of the observed population
o	Its monthly local wage cost is the lowest of the observed population
o	Its median home value is among the lowest in the observed population
Principal component analysis identified 4 distinct groups (Accelerating, Moderate Growth, Flat and Declining)

#### Usage:
Nearly all of the analysis was conducting using Google Colab which is a free python interpreter. However, to access it you will need a gmail account. 


#### Description of Files
TEU Growth Rates.IPYNB is the Colab file that walks through the python scripts needed for the presentation. 
TOP_90_Ports_Uploaded is the 90 ports where TEU information was obtained. It's the input file needed for the 
