# Snowflake_Intelligence_Web_Content_Analysis
Test the comprehensive capabilities of Snowflake Intelligence, with a focus on web content analysis

This repository is a shortened version of the following [repository](https://github.com/NickAkincilar/Snowflake_AI_DEMO/blob/main/README.md), by Nick Akincilar. Take a look at the full repository if you are interested to explore more capabilities of Snowflake Intelligence.

**Copy, Paste, Run & Done in less than 10 mins!**

**Just run the SQL script as an ACCOUNTADMIN as-is & your are done!**

This project demonstrates the comprehensive Snowflake Intelligence capabilities including:
- **Cortex Analyst** (Text-to-SQL via semantic views)
- **Cortex Search** (Vector search for unstructured documents)  
- **Snowflake Intelligence Agent** (Multi-tool AI agent with orchestration)
- **Git Integration** (Automated data loading from GitHub repository)

## Demo video showing some of what you can do!

![Snowflake Intelligence Demo Video](https://i9.ytimg.com/vi_webp/7T8LI5wIfDk/maxresdefault.webp?v=68ec51c9&sqp=COzkwckG&rs=AOn4CLBsQvKImaMig2cBnoNgogsrZ1BrPg)(https://youtu.be/7T8LI5wIfDk)

## Demo video generating streamlit apps from conversations!
![Snowflake Intelligence Demo Video](https://i9.ytimg.com/vi_webp/zNVx3hwKbyc/maxresdefault.webp?v=68eec089&sqp=CJjnwckG&rs=AOn4CLAU_RZKFbJnWxrXd2lOeGZgsk-XYw)(https://youtu.be/zNVx3hwKbyc)


## Key Components

### 1. Data Infrastructure
- **Star Schema Design**: 13 dimension tables and 4 fact tables covering Finance, Sales, Marketing, HR
- **Salesforce CRM Integration**: 3 Salesforce tables (Accounts, Opportunities, Contacts) with 62,000+ CRM records
- **Automated Data Loading**: Git integration pulls data from GitHub repository
- **Realistic Sample Data**: 210,000+ records across all business domains with complete customer journey
- **Database**: `SF_AI_DEMO` with schema `DEMO_SCHEMA`
- **Warehouse**: `Snow_Intelligence_demo_wh` (XSMALL with auto-suspend/resume)

### 2. Semantic Views (4 Business Domains)
- **Finance Semantic View**: Financial transactions, accounts, departments, vendors
- **Sales Semantic View**: Sales data, customers, products, regions, sales reps
- **Marketing Semantic View**: Campaign performance, channels, leads, impressions + **Revenue Attribution** (Salesforce CRM integration)
- **HR Semantic View**: Employee data, departments, jobs, locations, attrition

### 3. Cortex Search Services (4 Domain-Specific)
- **Finance Documents**: Expense policies, financial reports, vendor contracts
- **HR Documents**: Employee handbook, performance guidelines, department overviews
- **Marketing Documents**: Campaign strategies, performance reports, marketing plans
- **Sales Documents**: Sales playbooks, customer success stories, performance data

### 4. Snowflake Intelligence Agent
- **Multi-Tool Agent**: Combines Cortex Search, Cortex Analyst, Web Scraping, and File Access capabilities
- **Cross-Domain Analysis**: Can query all business domains and documents
- **Web Content Analysis**: Can scrape and analyze content from any web URL
- **File Sharing**: Can generate presigned URLs for temporary access to internal stage files
- **Natural Language Interface**: Responds to business questions across all departments
- **Visualization Support**: Generates charts and visualizations for data insights


## Setup Instructions

**Single Script Setup**: The entire demo environment is created with one script:
1. **Run the complete setup script**:
   ```sql
   -- Execute in Snowflake worksheet
   @SF_IntelligenceDemo_Full/sql_scripts/demo_setup.sql
   ```

2. **What the script creates**:
   - `SF_Intelligence_Demo` role and permissions
   - `Snow_Intelligence_demo_wh` warehouse
   - `SF_AI_DEMO.DEMO_SCHEMA` database and schema
   - Git repository integration
   - All dimension and fact tables with data
   - 4 semantic views for Cortex Analyst
   - 4 Cortex Search services for documents
   - Web scraping function with external access integration
   - Presigned URL function for secure file access
   - 1 Snowflake Intelligence Agent with multi-tool capabilities

3. **Post-Setup Verification**:
   - Run `SHOW TABLES;` to verify 20 tables created (17 original + 3 Salesforce CRM)
   - Run `SHOW SEMANTIC VIEWS;` to verify 4 semantic views
   - Run `SHOW CORTEX SEARCH SERVICES;` to verify 4 search services
   - Run `SHOW FUNCTIONS LIKE 'WEB_SCRAPE';` to verify web scraping function
   - Run `SHOW FUNCTIONS LIKE 'GET_FILE_PRESIGNED_URL';` to verify presigned URL function



## Agent Capabilities

The Company Chatbot Agent can:
- **Analyze structured data** across Finance, Sales, Marketing, and HR domains
- **Perform revenue attribution** from marketing campaigns to closed deals via Salesforce CRM integration
- **Search unstructured documents** to provide context and policy information
- **Scrape and analyze web content** from any URL to incorporate external data and insights
- **Generate presigned URLs** for secure, temporary access to files stored in internal stages
- **Generate visualizations** including trend lines, bar charts, and analytics
- **Combine insights** from multiple data sources for comprehensive answers
- **Calculate marketing ROI** and customer acquisition costs across the complete customer journey
- **Understand business context** and provide domain-specific insights

## Demo Script: Cross-Functional Insights and External Data 

**Web Content Analysis Questions**  
1. **Competitive Intelligence**  
   "Analyze the content from [competitor website URL] and compare their product offerings to our product catalog."

2. **Market Research**  
   "Scrape content from [industry report URL] and analyze how it relates to our sales performance and market positioning."

3. **External Data Integration**  
   "Get the latest information from [company news URL] and analyze its potential impact on our sales forecast."
