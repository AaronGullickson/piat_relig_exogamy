# Data Source Description

The data we will use for this project come from the [General Social Survey](https://gss.norc.org/)(GSS) waves of 2010, 2012, 2014, 2016, and 2018. The GSS is a nationally representative survey of US adults conducted every two years by the National Opinion Research Council. It is a major source of data on political attitudes in the US and is one of the best sources of information on religious affiliation and participation (because the US government cannot collect data on religion). 

For respondents who report being married, the GSS asks a variety of questions about the spouse of the respondent, including their religious affiliation. The GSS also asks a question on marital happiness. Our sample consists of all married individuals from the GSS between 2010-2018, for a total of 4710 respondents.

From the full GSS data, I have extracted and recoded the following variables for our use as an analytical dataset. To load this dataset in R, you just need to run the setup code chunk in the full_report.Rmd R Markdown document. The name of the dataset in R is `gss`. 

* **mar_happy_cat**: A categorical variable indicating the happiness of the current marriage, according to the respondent. The choice were very happy, pretty happy, and not too happy. Keep in mind that we are only getting one partner's report about the happiness of the marriage.
* **mar_happy_score**: Because we need a quantitative variable for the models, I converted the categorical variable into a score from 1-3, where a high number indicates a happier marriage.
* **relig_mar**: Based on the reported religion of both the respondent and their spouses, I have created a binary variable indicating whether the marriage is religiously endogamous (spouses same religion) or religiously exogamous (spouses different religion). Religions are broadly defined, but within the Christian category, I do distinguish between fundamentalist Protestants, mainline Protestants, Catholics, and Orthodox. So, for exmaple, a marraige between a fundamenalist and mainline Protestant would be considered religiously exogamous.
* **age**: age of the respondent.
* **region**: region of the country in four categories of Northeast, Midwest, South, West.
* **num_child**: Number of children the respondent has ever had.
* **family_work**: the employment situation of both the respondent and spouse. Categories are both partners out of the labor force, one partner working, or both partners working.
* **ed_homog**: This variable measures educational homogamy. It is based on the respondent's and the spouse's highest educational attainment. The categories are neither partner college educated, one partner college educated, both partners college educated.
