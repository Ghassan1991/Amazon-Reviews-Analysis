Introduction
This project demonstrates a complete data science workflow using the Amazon Polarity Reviews dataset, with a focus on data wrangling, exploratory data analysis (EDA), and initial preparation for text-based machine learning tasks. The notebook guides data scientists through essential steps: from loading real-world data, performing basic EDA, visualizing text distributions, to preparing the data for downstream NLP modeling and fine-tuning.

What Was Done
Environment and Library Setup
Installs key Python libraries needed for data science and natural language processing, specifically:
- datasets (Hugging Face)
- pandas
- matplotlib

Data Loading
Utilizes the Hugging Face datasets library to load the Amazon Polarity Reviews dataset.
Loads a manageable subset of 10,000 rows to optimize for speed and demonstration purposes.
Converts the dataset into a pandas DataFrame for flexible data manipulation.

Basic Exploratory Data Analysis (EDA)
Examines the distribution of the label (sentiment class) to understand class balance.
Checks for missing values in the DataFrame to assess data quality.
Samples a few entries to inspect the structure and contents of the dataset.

Text Feature Engineering
Adds a new column, word_count, representing the number of words in each review’s content.
Computes summary statistics (count, mean, std, etc.) for word_count to better understand review length distribution.

Visualization
Plots a histogram of review lengths (number of words per review) to visualize text distribution, using matplotlib.
(Optional/Preparation) - Fine-Tuning Preparation
The notebook lays the groundwork for subsequent steps such as data cleaning, preprocessing, and fine-tuning language models (though these steps may be further developed in future versions).

References & Dataset Source
Amazon Polarity Reviews Dataset – Hugging Face: https://huggingface.co/datasets/amazon_polarity
pandas documentation: https://pandas.pydata.org/docs/
matplotlib documentation: https://matplotlib.org/stable/users/index.html
Hugging Face Datasets documentation: https://huggingface.co/docs/datasets
