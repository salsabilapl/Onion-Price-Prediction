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
