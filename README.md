# UC Berkeley Datathon
**September 12, 2020**

This workshop was designed for UC Berkeley's PiE Datathon, sponsored by Microsoft.

Team: Gaurav Shah, Andy Fang, Rafael Ostrea

Overview: Our team analyzed different trends within a customer service dataset, making use of Azure to conduct sentiment analysis of product reviews and complaints as well as Pandas and Seaborn to generate user-friendly graphs of our findings. Our presentation won the Microsoft Best EDA (Exploratory Data Analysis) Award.

Presentation: https://docs.google.com/presentation/d/1nEv2cX69ds4IBE1wGlQrflimhIB4CgeZ0N0IbvaPtCc/edit?usp=sharing


## Setup Requirements
- [Free Azure student subscription](https://azure.microsoft.com/en-us/free/students/)
- Python
- Anaconda (Pandas, Numpy)
- Jupyter Notebooks (such as [Azure Notebooks](https://notebooks.azure.com/)) or your preferred IDE
- Git

## Setup

### Import requests
Run the command `pip install --upgrade requests` in your terminal.

Add `import requests` at the top of your Python file in order to call the Azure text analytics API.

### Create a Text Analytics resource in the Azure Portal
It is recommended that you create a Text Analytics resource for your project (team members can share an API key). You are welcome to incorporate other [Azure Cognitive Services](https://azure.microsoft.com/en-us/services/cognitive-services/?&ef_id=CjwKCAjw19z6BRAYEiwAmo64LVDAg0XDqkMIu9giSdrSMtEj62pCT0xpuv43pOjooX0xCO6kF1_3choC4wYQAvD_BwE:G:s&OCID=AID2100131_SEM_CjwKCAjw19z6BRAYEiwAmo64LVDAg0XDqkMIu9giSdrSMtEj62pCT0xpuv43pOjooX0xCO6kF1_3choC4wYQAvD_BwE:G:s&gclid=CjwKCAjw19z6BRAYEiwAmo64LVDAg0XDqkMIu9giSdrSMtEj62pCT0xpuv43pOjooX0xCO6kF1_3choC4wYQAvD_BwE) as appropriate for the scope of your project!

Learn more about the Text Analytics API and what it offers in [the Azure documentation](https://docs.microsoft.com/en-us/azure/cognitive-services/text-analytics/).

**Creating an Azure resource**

Follow [this tutorial](https://docs.microsoft.com/en-us/azure/cognitive-services/cognitive-services-apis-create-account?tabs=multiservice%2Cwindows) for creating a resource in Azure and accessing its API key.

When creating your resource, set the following configuration:
- `Subscription`: your Azure student subscription
- `Location`: this [depends on your team's general location](https://azure.microsoft.com/en-us/global-infrastructure/geographies/). We recommend selecting "(US) West US" from the dropdown menu if you are on the west coast or "(US) East US" if you are on the east coast. 
- `Pricing Tier`: Standard S if available or Free
- `Resource group`: Create a new [resource group](https://docs.microsoft.com/en-us/azure/azure-resource-manager/management/manage-resource-groups-portal) that will contain all of your Azure resources



## The datasets

### Customer Service Data
Description: These are records of support tickets that a fictitious hardware general store has received in the form of emails or audio converted to text.

Column descriptions
- `SupportTicket`: unique ID of support issue received
- `CustomerID`: unique ID of customer submitting issue
- `DateCreated`: date of when issue was submitted and received
- `DateCompleted`: date of closing the support ticket
- `Escalated`: binary variable of whether a ticket was escalated to another team due to urgency (0 - no, 1 - yes)
- `Theme`: category of support ticket
- `Text`: text of customer ticket

Theme descriptions
- price: cost of the goods to customers,  comparison to competitors, sales, discounts
- speed: delivery speed
- features: product or website features
- design: product or website design
- reliability: product, website, and delivery reliability
- support: tech, customer, and product support
- security: payment info, login info
- services: delivery, account, payment, and installation services
- other

Credit: Azure tutorial and datasets created by the Microsoft OCP Azure Data & AI Team
