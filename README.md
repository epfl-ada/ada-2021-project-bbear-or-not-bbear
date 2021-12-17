# Title: Analyze gender differences and seasonal changes in negative emotion expression
# Abstract
A growing body of evidence shows that people in negative mood use language differently. Many studies have unveiled a class of words that can help accurately detect whether someone is in negative emotions. Furthermore, mental disorders have been found to be positively associated with temperature. Moreover, gender differences were expected for different emotion and social process words, and overall word use.

# Research Questions
Under this context, we have applied sentiment analysis to automatically sort text data from Quotebank by positive, negative, and neutral sentiments. The further goals of our project are the following:

* Analyze the trend of negative experience
* Analyze the seasonal effect on negative emotions
* Analyze gender effect on negative emotions

# Website 
[Here!!!](https://93155.github.io/bbear_bbear/)

# Method
To look into this topic, we analyzed the dataset from Quotebank, which is a corpus of quotations from a decade of news. We mainly focused on the data from 2015 to 2019 (excluding 2016 since the data in 2016 is not equally distributed in each month) and in 2020, it only covers until April. In this project, we applied two libraries, TextBlob and gender-guesser, to analyze the dataset.

TextBlob is a Python library for prossing textual data, is useful for sentiment analysis by a pre-defined dictionary classifying negative and positive words. TextBlob assigns a score, between [-1, 1] to each word in a sentence, then by operations, for example, multipys and takes average, to get the final results. TextBlob returns polarity and subjectivity of a sentence which we can further analyze. Gender-guesser predicts the gender of a given first name with six different output: unknown (name not found), andy (androgynous), male, female, mostly_male, or mostly_female. In our project, we take male and mostly_male as man, female and mostly_female as women, while discard the data that gives output as unknown and andy.

For all the analysis, we randomly collect 1 million quotes from 2017, 2018, and 2019 for 30 times to decrease bias and variation.

## Negative emotion trend
1. 1 million data set 
2. Feature engineering by negative wordbank
3. Calculate negative counts annually
4. Plot neg counts vs. time

## Seasonal effect on negative emotions
1. Take 1 million quotes for each year in 2017 - 2019
2. Divided the 1 million quotes into 12 months, that is 12 pools.
3. Bootstrapping (Randomly sampling) 10 thousands quotes from every month pool, so that each month pool contains 10 thousands quotes
4. Calculate the negative count/polarity scores of each month pool.
5. Repeat steps 3 and step 4 with replication n = 30, so we can calculate the median and standard deviation of the negative quotes for each month.
6. Draw box plots of spring, summer, autumn and winter

## Gender differences in negative emotions
1. Take 1 million quotes for each year in 2017 – 2019
2. Append the polarity scores for each quotes
3. Apply genderize library to categorize the quotes by the gender of the first names
4. Divided the quotations in two gender types each year
5. Bootstrapping (Randomly sampling) 10000 quotes from every gender type
6. Calculate the negative count of each gender type(‘negative count’ here means quotations with anxious words and the polarity scores <=0)
7. Repeat steps 5 and step 6 with replication n = 30, so we can calculate the median and standard deviation of the negative quotes for each month.
8. Draw box plots over time, and compare the gender means and variation over time

# Organization within the team
Cheng-Hua Huang: data story, Coming up with algorithm, Wrap up of the whole project

Han-Yun Jhang: data story, Coming up with algorithm, Data analysis, Wrap up of the whole project

Hongyu Gu: data story, Creating website and data story, Wrap up of the whole project

Si-Ying Lai: data story, Data analysis, Creating website and data story, Wrap up of the whole project

# DataSet
[Here!!!](https://drive.google.com/drive/folders/1tiHh5bbhHg_iOJOo_1WkB92htXfz3Cgm?usp=sharing)
