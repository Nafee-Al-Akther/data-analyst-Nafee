# Projects
Phase 1

Project Title: Descriptive Analysis of Water Systems — Water Quality Reports in the City of Vancouver

Objective: To analyze water quality in Vancouver by examining turbidity levels relative to temperature, identifying key trends, and providing actionable insights for system optimization. This analysis aims to support decision-making for infrastructure improvements and policy adjustments by leveraging cloud-based data analytics and visualization tools.

Dataset: Data from the City of Vancouver on issued operating permit water systems, containing 1228 instances with 22 schema attributes, including operating permit number, address, mechanical system type, current system status, permit renewal date, water quality reports, temperature, and turbidity data. The dataset is structured to facilitate large-scale data processing and analysis, ensuring accuracy and consistency in reporting water quality trends over time.

Methodology

Data Collection and Preparation:

Data stored in Amazon S3 buckets: raw (cov-raw-naf), transformed (cov-trf-naf), and curated (cov-cur-naf).
![image](https://github.com/user-attachments/assets/048dd681-9a6f-404e-99ce-33c122f8d70b)


AWS Glue Data Brew used for data cleaning, handling missing values, and normalizing schemas to ensure consistency in data attributes. AWS Glue Crawler used to catalog and structure data in a cloud database, allowing for efficient querying and integration with other analytical tools. AWS Glue Crawler used to catalog and structure data in a cloud database.
![image](https://github.com/user-attachments/assets/f4e6cb91-7db8-45af-ba8b-354b4b5604fe)

Descriptive Statistics:

Summary of turbidity values: minimum, average, and trends relative to temperature. Identifying patterns in water quality through statistical measures. Comparative analysis of seasonal variations in turbidity and temperature fluctuations across different geo-local areas. Identification of outlier values that could indicate errors in data collection or significant water quality anomalies.



Data Visualization:
![image](https://github.com/user-attachments/assets/7dd979be-ebd3-47e7-9709-15dad5245a46)

Graphs illustrating temperature vs. turbidity relationships. Trend lines showing changes in turbidity levels based on temperature fluctuations.

Business Questions:

1. What is the average total temperature of all active issued water permits based on the Geo Local Area?

2. What is the average total turbidity of all active issued water permits based on the Geo Local Area?

Insights and Findings:
![image](https://github.com/user-attachments/assets/fe991452-b6d8-432b-aeb4-ca31ad8425d9)

The average recorded turbidity in different areas named Mount Pleasant, Downtown, West End, Riley Park, Fairview, Kensington-Cedar Cottage, Renfrew-Collingwood, Shaughnessy, Dunbar-Southlands, Hastings-Sunrise, Kerrisdale, South Cambie, Kitsilano, Grandview-Woodland, Killarney, Oakridge, Strathcona, West Point Grey, Sunset, Victoria-Fraserview, Marpole, Arbutus Ridge. 0.12 at the area of Shaughnessy which was the lowest by recored.

![image](https://github.com/user-attachments/assets/eb5fe22e-6959-4dd3-9bc2-86f469b6bd27)

The average recorded temperature in different areas named Mount Pleasant, Downtown, West End, Riley Park, Fairview, Kensington-Cedar Cottage, Renfrew-Collingwood, Shaughnessy, Dunbar-Southlands, Hastings-Sunrise, Kerrisdale, South Cambie, Kitsilano, Grandview-Woodland, Killarney, Oakridge, Strathcona, West Point Grey, Sunset, Victoria-Fraserview, Marpole, Arbutus Ridge.

Recommendations:

1. Monitor water quality closely in areas with high turbidity at lower temperatures.

2. Adjust filtration and treatment processes based on seasonal temperature shifts.

3. Improve data collection processes to minimize missing values and improve predictions.

Tools and Techniques:

1. AWS Services: S3, Glue Data Brew, Glue Crawler, ETL pipelines.

2. Data Processing: ETL pipeline with AWS Glue, Data Cleaning with Data Brew.

3. Data Storage: Cloud-based AWS databases, S3 buckets.

4. Visualization: Graphical representation of trends using data visualization tools.

Deliverables:

Cleaned and processed dataset stored in S3 with CSV and Parquet outputs. Descriptive Analysis Report detailing water quality trends.Visualizations and dashboards for turbidity analysis based on temperature. Recommendations document for improving water quality monitoring.

Phase 2

Project Title: Diagnostic Analysis of Water System Issues in Vancouver

Objective: CConduct a diagnostic analysis of the water system in Vancouver to identify underlying issues affecting water quality and system infrastructure. This includes examining active and inactive mechanical systems, assessing permit renewal trends, and ensuring proper security and governance measures for data integrity. The goal is to develop actionable strategies to improve overall system reliability and prevent potential water quality crises.

Dataset:

Water System Data: Information on geolocal are maximum turbifity and temperature.
![image](https://github.com/user-attachments/assets/233bdd47-8f50-471c-a1c6-42fa0d1af6bd)
![image](https://github.com/user-attachments/assets/b3e1938b-a3db-4bcd-87ed-fe3fefac89ca)

Permit Status Data: Trends in permit renewals dates and expired permits, indicating potential risks in water system maintenance.
![image](https://github.com/user-attachments/assets/fcebde1e-f823-43fa-9916-082c834d34fc)

Security Implementation Data: Logs related to encryption, replication, and governance measures applied to protect data integrity.
![image](https://github.com/user-attachments/assets/6fec5e72-51f7-441e-b09b-ade90e9403b6)

Governance and Monitoring Data: Compliance checks, data completeness assessments, and AWS monitoring logs to track changes and anomalies.
![image](https://github.com/user-attachments/assets/3e0b170f-04c7-4679-aac3-c10aee7f171d)

Methodology

1. Data Collection and Preparation: Gather and clean datasets from multiple sources, ensuring accuracy and consistency. Normalize data for analysis.

2. Trend Analysis: Analyze trends in active versus inactive mechanical systems. Identify water features with the lowest active percentages and potential operational inefficiencies. Examine permit renewal patterns to highlight areas with frequent expirations or gaps in permit compliance.

3. Correlation Analysis: Identify relationships between inactive systems and their impact on water quality. Use statistical methods such as regression analysis to quantify the impact of inactive systems on infrastructure reliability.

4. Root Cause Analysis: Investigate the factors leading to inactive systems  potential technical failures as well as expired permit . Identify high-risk zones where permit non-compliance is recurrent.

5. Segmentation Analysis: Segment mechanical systems based on their activity levels and operational efficiency. Categorize permit compliance levels by geographic region and system type.

Security Implementation:

1. AWS Key Management Service (KMS): Implemented symmetric encryption for S3 bucket protection.

2. Bucket Versioning & Replication Rules: Enabled versioning and cross-region replication to prevent data loss.

3. Governance & Monitoring:

  Quality Checks: Evaluated completeness, uniqueness, and freshness of data.

  AWS Monitoring Tools: Set up alarms to track anomalies and unauthorized access.

Synthesis of Findings:

1. Integrate quantitative and qualitative data to identify critical patterns and key insights.

2. Summarize actionable recommendations to address issues in water quality, system infrastructure, and permit compliance.

Tools and Techniques:

1. Data Analysis Tools: SQL (Amazon Athena), Python (Pandas, Scikit-learn) for data extraction and correlation analysis.

2. Data Security Tools: AWS Key Management Services (KMS), S3 encryption, and bucket versioning for data protection.

3. Monitoring Tools: AWS monitoring systems for anomaly detection and alert generation.

4. Visualization Tools: Tableau or Power BI for presenting trends and insights.

Deliverables:

1. A comprehensive diagnostic report detailing analysis results, key findings, and identified issues.

2. Visualizations and dashboards summarizing water system trends and permit compliance risks.

3. Actionable recommendations for improving water system quality and security measures.

Timeline:

Week 1-2: Data collection, cleaning, and initial trend analysis.

Week 3: Correlation analysis and root cause investigation.

Week 4: Segmentation and synthesis of findings.

Week 5: Development of recommendations and report preparation.

Week 6: Final review, stakeholder presentations, and implementation planning.

Conclusion:

This diagnostic analysis aims to provide a structured understanding of the challenges within the Vancouver water system, guiding the City towards effective solutions to enhance water quality, infrastructure reliability, and permit compliance. This extended analysis seeks to not only diagnose current issues but also anticipate future risks, providing a roadmap for long-term improvements in water quality monitoring, regulatory enforcement, and infrastructure investments. By integrating data-driven insights with operational strategies, the City of Vancouver can develop more robust policies to ensure safe and sustainable water distribution.


