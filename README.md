<!-- #
## **E-Marketplace**

**Minor Project**

Submitted By

**Yash Jalan 9919103035**

**Manas Dalakoti 9919103037**

**Kushagra Singh 9919103052**

**Yash Dixit 9919103055**

Under Supervision of

**Dr. Mukta Goyal**

![](RackMultipart20220507-1-iir91l_html_cd3aa35caf075e58.jpg)

**Department of CSE/IT**

**Jaypee Institute of Information Technology University, Noida**

**December 2021**

# ACKNOWLEDGEMENT ![Shape2](RackMultipart20220507-1-iir91l_html_d3dfebf0caf3fa8f.gif)

I would like to place on record my deep sense of gratitude to Mukta Goyal, Assistant Professor (Senior Grade), Jaypee Institute of Information Technology University, Noida, India for her generous guidance, help, and useful suggestions.

I express my sincere gratitude to Dr. Raju Pal and Dr. Himanshu Agarwal, Dept. of CS and IT Jaypee Institute of Information Technology University, Noida, India, for their stimulating guidance, continuous encouragement, and supervision throughout the course of the project.

I also wish to extend my thanks to our seniors, mentors and other classmates for their insightful comments and constructive suggestions to improve the quality of this project work.

**Yash Jalan 9919103035**

**Manas Dalakoti 9919103037**

**Kushagra Singh 9919103052**

**Yash Dixit 9199103055**

#

#


# DECLARATION ![Shape3](RackMultipart20220507-1-iir91l_html_d3dfebf0caf3fa8f.gif)

We hereby declare that this submission is our own work and that, to the best of our knowledge and beliefs, it contains no material previously published or written by another person nor material which has been accepted for the award of any other degree or diploma from a university or other institute of higher learning, except where due acknowledgment has been made in the text.

**Yash Jalan 9919103035**

**Manas Dalakoti 9919103037**

**Kushagra Singh 9919103052**

**Yash Dixit 9199103055**

Date:1/12/2021

#


#


#


#


#


#


# CERTIFICATE ![Shape4](RackMultipart20220507-1-iir91l_html_d3dfebf0caf3fa8f.gif)

This is to certify that the work titled &quot;E-Marketplace&quot; submitted by Yash Jalan, Manas Dalakoti, Kushagra Singh, and Yash Dixit of B.Tech of Jaypee Institute of Information Technology University, Noida has been carried out under my supervision. This work has not been submitted partially or wholly to any other University or Institute for the award of any other degree or diploma.

**Dr. Mukta Goyal**

**Assistant Professor (Senior Grade)**

Date: 1/12/2021 -->

# ABSTRACT
The objective of this project is to stimulate and represent real-world e-commerce problems and present their solution on a feasible scale. Initial steps included collection and organization of Raw data by creating a web scraper and extracting information through various concerned marketplaces websites, converting the quasi structured data into a more structured and definite form by using various data cleaning tools, and processing the filtered data for building our model.

We made use of various tools for visualizing and analyzing the data and finding patterns and trends in our dataset. For training our model we used various advanced machine learning and deep learning algorithms for the achievement of higher accuracy of price prediction.

Finally, for deploying our web application we used Python framework and libraries (Django/Flask) to project our model on a web application for providing a good user interface and reflecting the various trends in the e-commerce market.


**TABLE OF CONTENTS**


_ABSTRACT 1_

_TABLE OF CONTENTS 2_

_INTRODUCTION 3_

_BACKGROUND STUDY 4_

_IMPLEMENTATION 5_

_DEPENDENCIES AND REQUIREMENT ANALYSIS 6_

_DETAILED DESIGN 7_

_CONCLUSION AND FUTURE SCOPE 8_

_REFERENCES 9_


# INTRODUCTION 
This project is stimulation and the representation of the real world E-commerce problems and presentation of their solution on a feasible scale.

This project is completely built from scratch and even the work comprising the data collection is also performed on our own using web scraping. This involves the collection and organization of raw data by creating a web scraper and extracting information through various concerned marketplaces websites.

For data collection, we have used various python libraries such as BeautifulSoup, Selenium, and Scrappy.

We have stored the raw data in CSV files using the CSV library, for the creation of DataFrame and to perform Exploratory Data Analysis (EDA) on it.

File Handling in Python was used for image collection storage which has been downloaded in JPEG format from the respective sites with the respective titles. We did the cleaning of data collected through scrapping and organizing it in a structured order and making a data frame of it. For the above-said tasks, we have used various python modules and libraries such as Numpy, Pandas, Regex for cleaning of strings and pattern formation, NLTK, and general concepts of NLP and various python functionalities.

Heavy emphasis was applied to the use of pandas for the creation and working on the data frame.

The data has been thoroughly cleaned and processed and is now ready for Exploratory Data Analysis (EDA) and model Training.

The further steps involved merging the dataset from the two websites namely Amazon and Flipkart by merging their respective columns so that the data can be collectively analyzed.

We analyzed the price feature and segregated the price based on the quartiles and visualized them in the form of a bar plot using libraries like seaborn and matplotlib.

We analyzed the frequency distribution of the dataset based on the brand of the product.

We analyzed and visualized the areas with a higher concentration of frequency

to get the idea of complete distribution using a heatmap.

Finally, we integrated all of our work into the web framework using HTML, and CSS.


**BACKGROUND STUDY**

While building this project we have gained knowledge about some processes like Web Scraping, Exploratory Data Analysis, Data Cleaning tools used in python, . We also got insight about Machine learning and algorithms, we also touched on some concepts of Web Development as we have used Flask for our Frontend development.

For this project, we made use of several technology stacks, which required their background study and analysis of every one of the techniques, had extensive documentation, and required dwelling in their background working.

1. **Web Scraping** : Before diving into crawling a website, we should develop an understanding of the scale and structure of our target website. The website itself can help us through their robots.txt and Sitemap files, and there are also external tools available to provide further details such as Google Search and WHOIS.

**1.1.**  **Checking robots.txt**

Most websites define a robots.txt file to let crawlers know of any restrictions about crawling their website. These restrictions are just a suggestion but good web citizens will follow them. The robots.txt file is a valuable resource to check before crawling to minimize the chance of being blocked, and also to discover hints about a website&#39;s structure.

### **1.2. Examining the Sitemap**

Sitemap files are provided by websites to help crawlers locate their updated content without needing to crawl every web page. For further details, the sitemap standard is defined at [http://www.sitemaps.org/protocol.html](http://www.sitemaps.org/protocol.html). Here is the content of the Sitemap file discovered in the robots.txt file:

\&lt;?xml version=&quot;1.0&quot; encoding=&quot;UTF-8&quot;?\&gt;

\&lt;urlset xmlns=&quot;http://www.sitemaps.org/schemas/sitemap/0.9&quot;\&gt;

\&lt;url\&gt;\&lt;loc\&gt;http://example.webscraping.com/view/Afghanistan-1\&lt;/loc\&gt;\&lt;/url\&gt;

\&lt;url\&gt;\&lt;loc\&gt;http://example.webscraping.com/view/Aland-Islands-2\&lt;/loc\&gt;\&lt;/url\&gt;

\&lt;url\&gt;\&lt;loc\&gt;http://example.webscraping.com/view/Albania-3\&lt;/loc\&gt;\&lt;/url\&gt;

...

\&lt;/urlset\&gt;

This sitemap provides links to all the web pages, which will be used in the next section to build our first crawler. Sitemap files provide an efficient way to crawl a website but need to be treated carefully because they are often missing, out of date, or incomplete.

We scrapped the data from the sites Flipkart and Amazon, inspecting their pages for sitemaps

![Flipkart_image](/images_readme/1.jpg "Flipkart") 


![Sitemap](/images_readme/2.jpg "Sitemap")


**For Sitemap:**


**Amazon Interface:**


![Amazon_image](/images_readme/3.jpg "Amazon")


![Sitemap](/images_readme/4.jpg "Interface")


1. **Data Cleaning and processing:** Data pre-processing is an often neglected but important step in the data mining process. The phrase Garbage In, Garbage Out is particularly applicable to data mining and machine learning. Data gathering methods are often loosely controlled, resulting in out-of-range values (e.g., Income: -100), impossible data combinations (e.g., Gender: Male, Pregnant: Yes), missing values, etc. Analyzing data that has not been carefully screened for such problems can produce misleading results. Thus, the representation and quality of data are first and foremost before running an analysis. In this paper, the sources of errors are identified and presented. The data cleaning and its methods are discussed.


**Data Before Cleaning:**


**Amazon:**


![Amazon_data](/images_readme/5.jpg "Amazon_Data")


**Flipkart:**


![Flipkart_data](/images_readme/6.jpg "Flipkart data")


**Data After Cleaning:**


**Amazon:**


![Cleaned_data_amazon](/images_readme/7.jpg "Cleaned")


**Flipkart:**


![Cleaned_data_flipkart](/images_readme/8.jpg "Cleaned")


1. **Exploratory Data Analysis** :


Exploratory data analysis or &quot;EDA&quot; is a critical first step in analyzing the data from an experiment. Here are the main reasons we use EDA: • detection of mistakes • checking of assumptions • preliminary selection of appropriate models • determining relationships among the explanatory variables, and • assessing the direction and rough size of relationships between explanatory and outcome variables. Loosely speaking, any method of looking at data that does not include formal statistical modelling and inference falls under the term exploratory data analysis.

The data from an experiment are generally collected into a rectangular array (e.g., spreadsheet or database), most commonly with one row per experimental subject 61 62 CHAPTER 4. EXPLORATORY DATA ANALYSIS and one column for each subject identifier, outcome variable, and explanatory variable. Each column contains the numeric values for a particular quantitative variable or the levels for a categorical variable. (Some more complicated experiments require a more complex data layout.) People are not very good at looking at a column of numbers or a whole spreadsheet and then determining important characteristics of the data. They find looking at numbers to be tedious, boring, and/or overwhelming.

Exploratory data analysis techniques have been devised as an aid in this situation. Exploratory data analysis is generally cross-classified in two ways. First, each method is either non-graphical or graphical. And second, each method is either univariate or multivariate (usually just bivariate).

Non-graphical methods generally involve the calculation of summary statistics, while graphical methods summarize the data in a diagrammatic or pictorial way. Univariate methods look at one variable (data column) at a time, while multivariate methods look at two or more variables at a time to explore relationships.

Usually, our multivariate EDA will be bivariate (looking at exactly two variables), but occasionally it will involve three or more variables. It is almost always a good idea to perform a univariate EDA on each of the components of a multivariate EDA before performing the multivariate EDA. Beyond the four categories created by the above cross-classification, each of the categories of EDA has further divisions based on the role (outcome or explanatory) and type (categorical or quantitative) of the variable(s) being examined.

**Some results of EDA of the project are as follows:**

**TV dataset:**

**Noise level count plot**

![Count_plot](/images_readme/9.jpg "1st")

![Count_plot](/images_readme/10.jpg "2nd")

**Heatmap of size with budget**

![Heatmap](/images_readme/11.jpg "Heatmap of size with budget")

**Laptop Dataset:-**

We have performed EDA on various specifications of different brands of laptops. 

![Laptops](/images_readme/12.jpg "Laptop")

**Brand price**

![Laptop_brand](/images_readme/13.jpg "Price")

**Brand vs budget**

1. **Modelling:** For the purpose of modelling our dataset, after the cleaning and preprocessing of data, we used some state of the art algorithms and made our model.

The algorithms were all regression as this was the need of the project.

**Algorithms Used:**

**i) Lasso Regression:**  **Lasso regression** is a type of **[linear regression](https://www.statisticshowto.com/probability-and-statistics/regression-analysis/find-a-linear-regression-equation/)**that uses [shrinkage](https://www.statisticshowto.com/shrinkage-estimator/). Shrinkage is where data values are shrunk towards a central point, like the [mean](https://www.statisticshowto.com/mean/). The lasso procedure encourages simple, sparse models (i.e. models with fewer parameters). This particular type of regression is well-suited for models showing high levels of [multicollinearity](https://www.statisticshowto.com/multicollinearity/) or when you want to automate certain parts of model selection, like variable selection/parameter elimination.

The acronym &quot;LASSO&quot; stands for **L** east **A** bsolute **S** hrinkage and **S** election **O** perator.

Lasso regression performs L1 [regularization](https://www.statisticshowto.com/regularization/), which adds a penalty equal to the[absolute value](https://www.statisticshowto.com/integer/#abs)of the magnitude of coefficients.This type of regularization can result in sparse models with few coefficients; Some coefficients can become zero and eliminated from the model. Larger penalties result in coefficient values closer to zero, which is the ideal for producing simpler models. On the other hand, L2 regularization (e.g. [Ridge regression](https://www.statisticshowto.com/ridge-regression/)) _doesn&#39;t_ result in elimination of coefficients or sparse models. This makes the Lasso far easier to interpret than the Ridge.

![Performing_Regression](/images_readme/14.jpg "Regression Ss")

i**i) K-means Regressor:**K-means clustering as the name itself suggests, is a clustering algorithm, with no predetermined labels defined ,like we had for Linear Regression model, thus called as an Unsupervised Learning algorithm.

## **Logic and working:** K-means simply partitions the given dataset into various clusters(groups) with different features.

**How exactly?**

K refers to the total number of clusters to be defined in the entire dataset.There is a centroid chosen for a given cluster type which is used to calculate the distance of a given data point.The distance essentially represents the similarity of features of a data point to a cluster type.

**Constraints:**

Only **numerical data** can be used. Generally k-means works best for 2 dimensional numerical data. Visualization is possible in 2d or 3d data. But in reality there are always multiple features to be considered at a time.

Thus multi-dimensional data can be used but dimensionality reduction has to be performed to the data before using it for k-means.

**Choosing K:**

There is no exact way of determining the perfect value of K(total number of clusters for division). We have to try different values of K for the given dataset and compare the results thus obtained.

**Why to use K-means?**

Using k-means, the data is clustered after analyzing the data and not primitively defining it under a group based on pre-defined labels. Each centroid is a collection of features that essentially represent the type of cluster it belongs to. Thus a centroid can be used to interpret the type of cluster formed.

i**ii) XGBoost Regressor:**

Extreme Gradient Boosting (XGBoost) is an open-source library that provides an efficient and effective implementation of the gradient boosting algorithm.

Shortly after its development and initial release, XGBoost became the go-to method and often the key component in winning solutions for a range of problems in machine learning competitions.

Regression predictive modeling problems involve predicting a numerical value such as a dollar amount or a height. **XGBoost** can be used directly for **regression predictive modeling**.

Working of XGBoost Regressor has been depicted by the below diagram.

![XG_BOOST_WORKING](/images_readme/15.jpg "XG Boost Regressor")

1. **Flask:**

Flask stands out from other frameworks because it lets developers take the driver&#39;s seat and have full creative control of their applications. The key to this freedom is that Flask was designed from the start to be extended. It comes with a robust core that includes the basic functionality that all web applications need and expects the rest to be provided by some of the many third-party extensions in the ecosystem and, of course, by you. Flask is a small framework by most standards, small enough to be called a &quot;microframework.&quot; It is small enough that once you become familiar with it, you will likely be able to read and understand all of its source code. But being small does not mean that it does less than other frameworks. Flask was de‐ signed as an extensible framework from the ground up; it provides a solid core with the basic services, while extensions provide the rest. Because you can pick and choose the extension packages that you want, you end up with a lean stack that has no bloat and does exactly what you need. Flask has two main dependencies. The routing, debugging, and Web Server Gateway Interface (WSGI) subsystems come from Werkzeug, while template support is provided by Jinja2. Flask is a lightweight WSGI web application framework. It is designed to make getting started quick and easy, with the ability to scale up to complex applications. It began as a simple wrapper around Werkzeug and Jinja and has become one of the most popular Python web application frameworks. Flask offers suggestions, but doesn&#39;t enforce any dependencies or project layout. It is up to the developer to choose the tools and libraries they want to use. There are many extensions provided by the community that make adding new functionality easy.

![Flask](/images_readme/16.jpg "Flask")

**6) HTML CSS:**

Hypertext Markup Language and CSS (Cascading Style Sheets) are two of the core technologies for building Web pages. HTML provides the structure of the page, CSS the (visual and aural) layout, for a variety of devices. Along with graphics and scripting, HTML and CSS are the basis of building Web pages and Web Applications.

What is CSS? CSS is the language for describing the presentation of Web pages, including colors, layout, and fonts. It allows one to adapt the presentation to different types of devices, such as large screens, small screens, or printers. CSS is independent of HTML and can be used with any XML-based markup language. The separation of HTML from CSS makes it easier to maintain sites, share style sheets across pages, and tailor pages to different environments. This is referred to as the separation of structure (or: content) from presentation.

**IMPLEMENTATION**

![Shape9](RackMultipart20220507-1-iir91l_html_d3dfebf0caf3fa8f.gif)

- Collection and organization of Raw data by creating a web scraper and extracting information through various concerned marketplaces websites.
- Web Scraping was performed on Flipkart and amazon to collect the raw data.

**DATA BEFORE CLEANING**

![Data_before_cleaning](/images_readme/17.jpg "Before Cleaning")

**DATA AFTER CLEANING**

![Data_after_cleaning](/images_readme/18.jpg "After Cleaning")

- Converting the quasi-structured data into a more structured and definite form by using various data cleaning tools.

- This processing is done using regex and other data cleaning tools for making it suitable in order to do further processing.
- Processing the filtered data for building our model.

**Data Visualisation**

![Data_Visualization](/images_readme/19.jpg "Visualization")

- Making use of various tools for visualizing and analyzing the data and finding patterns and trends in our dataset.

- Training our model using various advanced machine learning and deep learning algorithms for the achievement of higher accuracy of price prediction.

![Box](/images_readme/20.jpg "Box plot")

**REPRESENTING THE MODEL ON WEB FRAMEWORK**

![Web_Layout](/images_readme/21.jpg "Web Layout")

- Using HTML , CSS and Javascript to design the home page and the integrate all our work done till now in the web framework.

- Making use of Python framework and libraries (Django/Flask) to project our model on a web application for proving a good user interface and reflecting the various trends in the e-commerce market.

![Laptop_EDA](/images_readme/22.jpg "Laptop EDA")

**PRICE PREDICTION MODEL**

![Price_prediction](/images_readme/23.jpg "Predict Price")

**EXPLORATORY DATA ANALYSIS**

![](RackMultipart20220507-1-iir91l_html_fa8752483c22c5f.png)

**DEPENDENCIES AND REQUIREMENTS ANALYSIS**![Shape10](RackMultipart20220507-1-iir91l_html_d3dfebf0caf3fa8f.gif)

| **Beautiful Soup** | It is a [Python](https://en.wikipedia.org/wiki/Python_(programming_language)) package for parsing [HTML](https://en.wikipedia.org/wiki/HTML) and [XML](https://en.wikipedia.org/wiki/XML) documents (including having malformed markup, i.e. non-closed tags, so named after [tag soup](https://en.wikipedia.org/wiki/Tag_soup)). It creates a parse tree for parsed pages that can be used to extract data from HTML, which is useful for [web scraping](https://en.wikipedia.org/wiki/Web_scraping). |
| --- | --- |
| **Scrapy** | Scrapy is a free and open-source web-crawling framework written in Python. Originally designed for web scraping, it can also be used to extract data using APIs or as a general-purpose web crawler. It is currently maintained by Zyte, formerly Scrapinghub, a web-scraping development, and services company. |
| **Regex** | A regular expression is a sequence of characters that specifies a search pattern. Usually, such patterns are used by string-searching algorithms for &quot;find&quot; or &quot;find and replace&quot; operations on strings, or for input validation. It is a technique developed in theoretical computer science and formal language theory |
| **Pandas** | Pandas is a software library written for the Python programming language for data manipulation and analysis. In particular, it offers data structures and operations for manipulating numerical tables and time series. It is free software released under the three-clause BSD license. |
| **Scikit Learn** | Scikit-learn is a free software machine learning library for the Python programming language. It features various classification, regression and clustering algorithms including support vector machines |
| **NumPy** | NumPy is a library for the Python programming language, adding support for large, multi-dimensional arrays and matrices, along with a large collection of high-level mathematical functions to operate on these arrays |
| **XGBoost** | XGBoost is an open-source software library that provides a regularizing gradient boosting framework for C++, Java, Python, R, Julia, Perl, and Scala. It works on Linux, Windows, and macOS. |
| **Beautiful Soup** | Beautiful Soup is a Python package for parsing HTML and XML documents. It creates a parse tree for parsed pages that can be used to extract data from HTML, which is useful for web scraping. |

Table 1.0 (Python Dependencies)

**DETAILED DESIGN**

![Shape11](RackMultipart20220507-1-iir91l_html_d3dfebf0caf3fa8f.gif)

![Detailed_Design](/images_readme/24.jpg "Detailed Design")

The entire project comprises three major parts namely the dataset, models, and web design.

The project started with the collection of the datasets and cleaning.

1. **Data Collection** : Collection and organization of Raw data by creating a web scraper and extracting information through various concerned marketplaces websites.

1. **Data Cleaning** : Converting the quasi-structured data into a more structured and definite form by using various data cleaning tools.

1. **Data Preprocessing** : Processing the filtered data for building our model.

1. **Exploratory Data Analysis** : Making use of various tools for visualizing and analyzing the data and finding patterns and trends in our dataset.

1. **Applying Machine Learning/ Deep Learning Algorithms** : Training our model using various advanced machine learning and deep learning algorithms for the achievement of higher accuracy of price prediction.

1. **Building Web Application** : Making use of Python framework and libraries (Django/Flask) to project our model on a web application for proving a good user interface and reflecting the various trends in the e-commerce market.

**CONCLUSION AND FUTURE SCOPE**

![Shape12](RackMultipart20220507-1-iir91l_html_d3dfebf0caf3fa8f.gif)

This project is stimulation and the representation of the real world E-commerce problems and presentation of their solution on a feasible scale.

The Exploratory Data Analysis shines all and out with it&#39;s accurate graphs and visualizations. The dataset is prepared and modelled in such a way that in future if more features are added then also it can work just fine.

The project can be extended to various domains namely the medical, automation, and other sectors

that requires the visualization of the data and making proper predictions for their respective causes.It can very well act as a background foundation for prediction and cleaning of various other datasets and real world problems as of prediction of various other devices or things pertaining to different industries as well.

#


# REFERENCES ![Shape13](RackMultipart20220507-1-iir91l_html_d3dfebf0caf3fa8f.gif)

**Websites Scraped**** :**

1. [_https://www.amazon.com_](https://www.amazon.com/)
2. [_https://www.flipkart.com_](https://www.flipkart.com/)
3. _https://www.olx.in_

**Study Material**** :**

**Books:**

1. Tukey, J.W., 1977. _Exploratory data analysis_ (Vol. 2, pp. 131-160).
2. Lawson, Richard. _Web scraping with Python_. Packt Publishing Ltd, 2015.
3. García, Salvador, Julián Luengo, and Francisco Herrera. _Data preprocessing in data mining_. Vol. 72. Cham, Switzerland: Springer International Publishing, 2015.
4. Flask Web Development by Miguel Grinberg, Published by O&#39;Reilly Media, Inc., 1005 Gravenstein Highway North, Sebastopol, CA 95472.

**Journal:**

1.Behrens, John T. &quot;Principles and procedures of exploratory data analysis.&quot; _Psychological Methods_ 2.2 (1997): 131.

2. Hillen, Judith. &quot;Web scraping for food price research.&quot; _British Food Journal_ (2019).

#
