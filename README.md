# Onion-Price-Prediction-In-Tegal-Jawa-Tengah
Indonesia, one of the world's largest red onion producers, relies significantly on Tegal, Jawa Tengah, for this essential agricultural commodity. However, the fluctuating red onion prices in this region can impact both farmers and consumers. Predicting these price fluctuations is crucial for effective farm planning and risk mitigation. Utilizing technology and data analysis, Onion Price Prediction in Tegal, Jawa Tengah, can provide valuable insights to farmers and stakeholders in the supply chain, enabling better decision-making regarding planting, harvesting, storage, and sales.

## Description
By utilizing IBM AutoAI, you can streamline and automate the entire process of constructing predictive models to cater to diverse needs. This powerful tool expedites the generation of exceptional models, effectively minimizing the time and energy required while facilitating prompt decision-making. In this context, you can leverage AutoAI to create a model that accurately predicts the adaptability level of students in online education by considering various data points such as age, gender, region, institution type, network type, and more.

Upon completing this code pattern, you will gain proficiency in the following:

* Rapidly setting up services on IBM Cloud to build model development.
* Importing data and initiating the AutoAI process effortlessly.
* Constructing multiple models using AutoAI and assessing their performance.
* Selecting the optimal model and successfully deploying it.
* Generating predictions by making REST calls to the deployed model.

### Architecture Components

![Architecture Components](https://upload.wikimedia.org/wikipedia/commons/b/bb/AutoAI-ml-process.png)

## Flow Description
1. The user creates an IBM Watson Studio Service on IBM Cloud.
2. The user creates an IBM Cloud Object Storage Service and adds that to Watson Studio.
3. The user uploads the student adaptability level in online education data file into Watson Studio.
4. The user creates an AutoAI Experiment to predict student adaptability level on Watson Studio
5. AutoAI uses Watson Machine Learning to create several models, and the user deploys the best performing model.

## Included components
*	[IBM Watson Studio](https://cloud.ibm.com/catalog/services/watson-studio) - IBM Watson® Studio helps data scientists and analysts prepare data and build models at scale across any cloud.
*	[IBM Watson Machine Learning](https://cloud.ibm.com/catalog/services/machine-learning) - IBM Watson® Machine Learning helps data scientists and developers accelerate AI and machine-learning deployment. 
*	[IBM Cloud Object Storage](https://cloud.ibm.com/catalog/services/cloud-object-storage) - IBM Cloud™ Object Storage makes it possible to store practically limitless amounts of data, simply and cost effectively.

## Featured technologies
+ [artificial-intelligence](https://developer.ibm.com/technologies/artificial-intelligence/) - Build and train models, and create apps, with a trusted AI-infused platform.
+ [Python](https://www.python.org/) - Python is an interpreted, high-level, general-purpose programming language.

## Prerequisites

This Cloud pattern assumes you have an **IBM Cloud** account. Go to the 
create account in link below 
  - [IBM Cloud account](https://cloud.ibm.com)
  - [Python 3.11.0](https://www.python.org/downloads/release/python-3110/)

# Steps
0. [Prepare the dataset](#step-0-Prepare-the-dataset)
1. [Explore the data (recommended)](#step-2-explore-the-data-recommended)
2. [Create IBM Cloud services and the AutoAI](#step-3-create-ibm-cloud-services-and-the-AutoAI)
3. [Run AutoAI experiment](#step-4-run-autoai-experiment)
4. [Create a deployment and test your model](#step-5-create-a-deployment-and-test-your-model)
5. [Create a notebook from your model (optional)](#step-6-create-a-notebook-from-your-model-optional)

## Step 0. Download the data set 
We will use a dataset obtained from the research center at our university. This dataset provides crucial insights into onion pricing trends in the Tegal, Central of Java. Additionally, we possess an IoT dataset encompassing weather and environmental data for the Kabupaten Tegal area, including variables such as air humidity and wind speed. It's important to note that both datasets have been acquired with proper authorization and collaboration from local authorities in Kabupaten Tegal. All data used in this research will be treated with the utmost confidentiality and will solely be employed for research and analytical purposes. We respect data privacy and confidentiality and will adhere to all relevant regulations governing data usage.

## Step 1. Explore the data
#### If you want to run the notebook that include the Exploratory Data Analysis below, go to [here](

*

* see the data into a data frame, and call the `df_.head()` function, you will see the first 5 rows of the data set also the 8 data features.
![github-1](https://github.com/salsabilapl/Onion-Price-Prediction/assets/74218691/700501eb-01f0-4541-aef3-00ca7855da58)

* see the data into a data frame, and call the `df_.head()` function, see the first 5 rows of the data set also the 8 data features.
![github-1](https://github.com/salsabilapl/Onion-Price-Prediction/assets/74218691/700501eb-01f0-4541-aef3-00ca7855da58)

* see analysis descriptive of the data, call the `data.describe()`function.
![github-2](https://github.com/salsabilapl/Onion-Price-Prediction-Auto-AI/assets/74218691/4f70a7c3-019d-447e-b2cd-d42b8eeca35a)
 
* How the distribution of every variable?
![github-3](https://github.com/salsabilapl/Onion-Price-Prediction-Auto-AI/assets/74218691/05074af1-9ce8-47e6-81e6-5ea55a6adc49)

* How the correlation every variables?
![github-4](https://github.com/salsabilapl/Onion-Price-Prediction-Auto-AI/assets/74218691/34161c5f-97ea-450d-a645-5b5737ba4adc)

* How the onion price over time?
![github-5](https://github.com/salsabilapl/Onion-Price-Prediction-Auto-AI/assets/74218691/57b5e44e-7984-4440-b035-e97cca1735da)

* How distribution the frequency of price?
![github-6](https://github.com/salsabilapl/Onion-Price-Prediction-Auto-AI/assets/74218691/61d2780f-381d-4062-befe-afdce91fa1b4)

* How the price visualization in the boxplot?

![github-7](https://github.com/salsabilapl/Onion-Price-Prediction-Auto-AI/assets/74218691/df4cd030-b7c9-4eb5-9f9a-79438e1e6af3)

* Average price in every month
![github-8](https://github.com/salsabilapl/Onion-Price-Prediction-Auto-AI/assets/74218691/69e4b734-a806-4230-9e48-e9d38fa37b7c)

* Average price in every year
![github-9](https://github.com/salsabilapl/Onion-Price-Prediction-Auto-AI/assets/74218691/548efc03-449d-4e87-85fd-e215824fa732)

* Dickey Fuller Check for the time series purpose
![github-10](https://github.com/salsabilapl/Onion-Price-Prediction-Auto-AI/assets/74218691/7ac77f1b-5893-41e0-9f72-166604cd730a)

<b>If you want to see all of the Exploratory Data Analysis code, and run the notebook yourself, go to [here](https://github.com/omidiyanto/student-adaptability-prediction/blob/main/Exploratory%20Data%20Analysis/notebooks.ipynb)</b>

## Step 3. Create IBM Cloud services and the AutoAI
1.	Login to your IBM Cloud account: https://cloud.ibm.com 

2.	Within your IBM Cloud account, click on the top search bar to search for cloud services and offerings. Search and create this services: <b>Watson Studio</b>, <b>Watson Machine Learning</b>, and <b>Cloud Object Storage</b>

3.	 Once all the services instance is ready, redirect to the Watson Studio page. Click on the “Launch in IBM Cloud Pak for Data” button to launch Watson Studio in a new tab.

4.  Create new project that says, “New Project”. Next, click on “Create an empty project”.

5.  On the new project page, give your project a name. You will also need to associate an IBM Cloud Object Storage instance to store the data set.

6. Go to Manage Tab, in the Service & Integrations option, associate the <b>Watson Machine Learning</b> service.

7.  Upload the `data_bawang.csv` dataset that you have downloaded it previously. Watson Studio takes a couple of seconds to load the data, and then you should see the import has completed. To make sure it has worked properly, you can click on “Assets” on the top of the page, and you should see your insurance file under “Data Assets”.

8.  Once you have added the data set, click on the “New Asset” button on the top right corner. This time select “AutoAI”.




