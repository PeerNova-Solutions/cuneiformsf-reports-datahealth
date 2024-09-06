# cuneiformsf-reports

# Free Data Health Reports for Salesforce Customers
Powered by [Cuneiform for Salesforce](https://jira-peernova.atlassian.net/wiki/spaces/CFCPD/pages/2962358316/PeerNova+s+Cuneiform+for+Salesforce+Products).  Over 110+ Salesforce Reports across 17 Data Health and Reliability Categories. 100% Free for the Salesforce ecosystem.

This repository manages our collection of thoughtfully curated data quality and technical health reports.  Use these reports
with any Cuneiform for Salesforce product to help you get started with your data quality journey.  
> These reports are 100% free and are designed to be customized and adapted to meet your organization's specific needs. [Install Cuneiform for CRM today](https://jira-peernova.atlassian.net/wiki/spaces/CFCPD/pages/2956001507/Setup+Field+and+Data+Management) and use these reports to explore the shape, health, and reliability in your data.

![Cuneiform for Salesforce: Comparing Overall vs. Populated Duplicate Density](img/dupe-density-comparison.gif)

> This report compares the overall duplicate density of a Salesforce org with the duplicate density of populated fields.  It is designed to help you understand which fields have the highest amount of duplicate values and compares the duplicate density of populated records against profiled records.

## What Is Cuneiform for Salesforce?

[Cuneiform for Salesforce](https://jira-peernova.atlassian.net/wiki/spaces/CFCPD/overview) is the Salesforce ecosystem's first line of high-performance data quality, data reliability, and data management products for Salesforce CRM and Data Cloud.  

Use our products to quickly assess the data health, reliability, and AI readiness of your CRM and Data Cloud data securely from within your Salesforce org (visit our [Cuneiform for Salesforce and Trust](https://jira-peernova.atlassian.net/wiki/spaces/CFCPD/pages/2625699908) page for more details).  Assess the reliability of millions of records in minutes with the most comprehensive collection of utilization, metadata, and data quality / reliability insights [available in the Salesforce AppExchange](https://appexchange.salesforce.com/appxListingDetail?listingId=a0N4V00000IPSsZUAX).

![Cuneiform for Salesforce: Measure the Reliability of Your Salesforce Org's Data](img/kpis-trend.gif)

> This display shows a Lead Completeness % Data Quality KPI in Cuneiform for CRM. It tracks the percentage of completeness of lead records over time -- with the graph showing variations in lead completeness against record volume profiled. Use this chart to monitor trends and assess whether KPI averages are increasing or decreasing, allowing for quick evaluation of data quality changes based on how records are added or removed from the Lead Object in your Salesforce org.

## How to Use These Reports

These reports are designed to accelerate the analysis process for Salesforce administrators, data quality professionals, and data stewards.  Use these reports to quickly assess the health, reliability, and quality of your Salesforce data.  

> Each report is designed to provide a specific set of insights into your Salesforce data, and can be customized to meet your specific data quality needs.  Use these reports to inspect profiling results, identify data quality issues, and prioritize data governance initiatives.

![Cuneiform for Salesforce: Understanding the Profiling Process](img/profiling-process.gif)

In our data reliability process, you can use these reports to inspect profiling results across each of the seventeen (17) report categories included in this repository.  Use these reports to identify unused fields, assess duplicate density, explore which fields have the highest default value usage, and more.  

> Each report is designed to provide a specific set of insights into your Salesforce data, and can be customized to meet your specific data quality needs.

## Installation Prerequisites
To use these reports, you must have a Salesforce org and a [Cuneiform for Salesforce](https://jira-peernova.atlassian.net/wiki/spaces/CFCPD/pages/2623373382/Introducing+Cuneiform+for+Salesforce) product installed in a development, production, or sandbox org. You can find our [latest releases](https://jira-peernova.atlassian.net/wiki/spaces/CFCPD/pages/2618130783/Latest+Product+Releases) via our [Product Documentation](https://jira-peernova.atlassian.net/wiki/spaces/CFCPD/overview).  

- Review our [product pre-requisites](https://jira-peernova.atlassian.net/wiki/spaces/CFCPD/pages/2621800476/Installation+Prerequisites) to confirm you can install Cuneiform for Salesforce products
- Install [Cuneiform for CRM: Field and Data Management](https://jira-peernova.atlassian.net/wiki/spaces/CFCPD/pages/2956001507/Setup+Field+and+Data+Management) to get started with data quality assessments and monitoring.
- Complete your [setup of Cuneiform for CRM](https://jira-peernova.atlassian.net/wiki/spaces/CFCPD/pages/2596241458/Configuring+Cuneiform+for+CRM+FDM) in minutes and [validate your configuration](https://jira-peernova.atlassian.net/wiki/spaces/CFCPD/pages/2615214099/Verify+Your+Cuneiform+for+CRM+FDM+Configuration).
- [Profile your Salesforce Standard and Custom Objects](https://jira-peernova.atlassian.net/wiki/spaces/CFCPD/pages/2623373435/Get+Started+with+Data+Profiling) to collect the profiling insights and data governance evidence to drive data initiative priorities

## Deployment Instructions
We recommend [cloning this repository](https://docs.github.com/en/repositories/creating-and-managing-repositories/cloning-a-repository) and using SFDX to deploy these reports to your Salesforce org.  You can also use the Salesforce UI to manually deploy these reports (not recommended, but certainly an option).

> Please follow the git clone instructions below to get started with deploying these reports to your Salesforce org.  The following guidance is dependent on you having [SFDX installed](https://developer.salesforce.com/docs/atlas.en-us.sfdx_setup.meta/sfdx_setup/sfdx_setup_install_cli.htm) on your local machine and cloned this repository to your local workstation.

### Install SFDX
If you don't have SFDX installed, you can install it by following the instructions on the [Salesforce Developer site](https://developer.salesforce.com/docs/atlas.en-us.sfdx_setup.meta/sfdx_setup/sfdx_setup_install_cli.htm). You can verify your installation by entering the following command in your terminal at the directory where this repository was cloned.  
> ```sf version```

This will return the version number of your SFDX installation (ex., @salesforce/cli/2.56.7 darwin-arm64 node-v20.16.0).

### Authenticate Against Your Target Org
Before deploying the reports, you must authenticate against the Salesforce org where you [Cuneiform for CRM is installed](https://jira-peernova.atlassian.net/wiki/spaces/CFCPD/pages/2956001507/Setup+Field+and+Data+Management).  You can do this by entering the following command in your terminal and replace `<mydomain-url>` with the myDomain version of your org's url (ex. https://mydomainname.my.salesforce.com).
> ```sf auth web login --instance-url=https://mydomainname.my.salesforce.com```.  
 
This will open a browser window where you can authenticate against your Salesforce org.  Once authenticated, you can close the browser window and return to your terminal.

### Deploy the Reports to Your Target Org
To deploy the reports to your Salesforce org, you can use the following command in your terminal.
> ```sf project deploy start --source-dir=force-app/main/default```

This command will deploy the reports to your Salesforce org.  Please [review our sample output](SAMPLE_DEPLOYMENTOUTPUT.md) that depicts a successful deployment via SFDX.  This page includes guidance on how to [validate the deployment](SAMPLE_DEPLOYMENTOUTPUT.md) from within Salesforce setup.

### Verify the Reports in Your Salesforce Org
You can verify the deployment by logging into your Salesforce org and navigating to the Reports tab.  You should see the reports in the `Cuneiform for CRM: Data Health Reports` folder.  Please ensure that you have access to reports prior to validating the deployment.

![Cuneiform for Salesforce: Data Health Reports Folder](img/report-folders.gif)

> This screenshot shows the `Cuneiform for CRM: Data Health Reports` folder in the Salesforce Reports tab.  This is where you will find the reports after a successful deployment.  If you do not see the reports, please first verify that the deployment was successful and ensure you have access to reports in your Salesforce org.

### Using the Cuneiform for Salesforce Reports
Each report is designed to display profiling results for multiple Salesforce objects and has a set of filter parameters that control the profiling results displayed.  The following table contains the base parameters that are used to limit the records displayed in each of the reports.

| Parameter Name                | Description                                                                                                                                                                                                          | Default Value |
|-------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------|
| Is Latest Summary             | Describes if a profiling summary the latest summary created for a given Profiling Definition. The reports in this collection only include the latest profiling summary results for qualifying Profiling Definitions. | true          |
| Profiling Definition Category | Describes the Profiling Category assigned to a given Profiling Definition.  The reports in this collection only include summaries belonging to Profiling Definitions that have a category value of `Baseline`.       | `Baseline`    |

![Cuneiform for Salesforce: Report Parameters](img/filter-criteria.gif)

These reports are designed to display single summary results for multiple Profiling Definitions. Ensure that these parameters are configured correctly to see results (reports that display none or too many results may need to have these parameters adjusted).
> Customize these parameters to change the scope of results rendered in these reports, and extend the filter criteria with new filters to include or filter out specific profiling results.  Review the filter criteria in each report for examples of how to extend the filter criteria.

## Report Categories
Each of these reports can be copied and customized to fit specific reporting needs, providing a robust foundation for comprehensive data quality analysis in Salesforce.

### Cuneiform for Salesforce Reporting Templates

#### Object, Field, and Field Value Templates (7 Reports)
This category offers a suite of pre-built report templates designed for comprehensive data quality and reliability assessments in Salesforce. Leveraging profiling statistics generated by Cuneiform for Salesforce, these templates provide a solid foundation for in-depth data analysis.
> Salesforce professionals can use these templates to rapidly build custom reports and dashboard for use-case specific data reliability scenarios.
 
![Cuneiform for Salesforce: Profiled Picklist Values | TEMPLATE](img/reports/templates-picklistvalues.gif)

> The `Profiled Picklist Values | TEMPLATE` report provides an analysis of picklist field usage across various Salesforce objects. It offers key metrics such as total picklist values, active and inactive values, and field utilization statistics with a visual breakdown of picklist fields by object. 

#### Profiling Exceptions Analysis (8 Reports)
The Profiling Exceptions Analysis category offers a set of reports designed to examine and categorize exceptions that occur during the data profiling process. These reports provide detailed insights into various types of exceptions, including those associated with profiling definitions, specific fields, objects, and unassociated exceptions -- grouped by different criteria such as class or object.
> Salesforce administrators and data quality teams can use this report to explore the exceptions captured during the data profiling processes. This granular view enables swift identification of recurring issues and facilitates targeted troubleshooting with Cuneiform Support.

![Cuneiform for Salesforce: Exception Logs | Definitions](img/reports/exceptions-bydefinition.gif)

> The `Exception Logs | Definitions` report provides a detailed overview of exceptions that occur during the profiling process. It displays exception details by definition and includes specific details for each exception -- including as the definition key, exception type, and summary description. 

### Data Reliability Analysis Reports

#### Data Governance Analysis (6 Reports)
Explore your Salesforce data governance landscape with this set of specialized reports. From field usage and compliance categories to data ownership and sensitivity levels, these analyses shed light on crucial aspects of your data classification and governance framework.
> These reports empower data architects and administrators to fortify their organization's data governance strategies. By identifying fields that lack data classification properties and aligning practices with regulatory requirements, teams can create a lightweight governance structure tailored to their business needs.

![Cuneiform for Salesforce: Fields | Data Gov | Missing](img/reports/datagov-missing.gif)

> The `Fields | Data Gov | Missing` report identifies all populated and unpopulated fields that lack data classification properties.  It provides a visual breakdown of these by population status, and includes field both utilization statistics and data classification properties for each offending field.

#### Data Dictionary Analysis (11 Reports)
Dive deep into your Salesforce metadata with this collection of reports focused on field documentation and properties. Uncover insights about description and help-text usage across custom fields, formulas, and data classification attributes for profiled objects.
> Salesforce administrators and data stewards can use these reports to pinpoint documentation gaps and description inconsistencies across multiple fields. This intelligence drives improvements in data quality, boosts user adoption, accelerates AI readiness, and contributes to a well-governed Salesforce environment.

![Cuneiform for Salesforce: Fields | Description & Help Text | Missing](img/reports/dictionary-missing-desc-helptext.gif)

> The `Fields | Descriptions & Help | Missing` report identifies all profiled fields that lack descriptions and help text. It provides a visual breakdown of populated and empty fields missing these field values that may need better descriptions or help text to enhance user understanding and data quality.

#### Default Value Analysis (5 Reports)
The Default Value Analysis category showcases a set of reports dedicated to examining the configuration and usage of default values across Salesforce fields. These reports delve into various aspects of default value implementation, including their presence in required fields, usage patterns, data type distributions, and fields with high default value adoption.
> Salesforce administrators and data quality specialists can leverage the insights in these reports to optimize field configuration, streamline data entry processes, and ensure default values align with business requirements. By scrutinizing default value usage patterns, organizations can improve data entry trustworthiness, enhance data consistency, and streamline business processes.

![Cuneiform for Salesforce: Fields | High Default Value Usage](img/reports/defaults-highusage.gif)

> The `Fields | High Default Value Usage` report identifies fields configured with default values that have high usage rates. It provides a visual breakdown of default value population percentages across different objects and fields and with our collection of field utilization statistics. This report is crucial to identify potential data quality issues or process inefficiencies where default values may be overused.

#### Duplicate Value Analysis (4 Reports)
Unveil the impact of duplicate values on your Salesforce data with this set of analysis reports. Identify fields with high percentages of duplicate values based on their overall and populated duplicate-density scores, and pinpoint fields with the highest propensity for duplicate values.
> Data quality teams can use these reports to accelerate deduplication efforts, inform which fields are used in match rules, and improve the reliability of deduplication initiatives. Dive deeper into duplicate value patterns by comparing duplicate-density scores against populated records and profiled records.  Use these insights to drive deduplication priorities.

![Cuneiform for Salesforce: Fields | With High Duplicate Frequency %](img/reports/duplicates-highfrequency.gif)

> The `Fields | With High Duplicate Frequency %` report identifies fields with a high percentage of duplicate values. It provides a visual breakdown of duplicate-density percentages across different objects and fields, and enables data quality teams to quickly pinpoint fields that may be contributing to data duplication issues.  Use our profiling statistics to inform field priorities and match rule design. 

#### Picklist Value Analysis (5 Reports)
Optimize your Salesforce picklist fields with this powerful set of analysis reports. Identify active and in-use picklist values, uncover inactive values that can be safely removed, and pinpoint non-picklist fields that may be candidates for conversion to streamline data entry and maintain consistency.
> Salesforce administrators and data managers can leverage these insights to refine picklist configurations, eliminate unused values, and improve data accuracy and consistency across Salesforce objects. By proactively managing picklist fields and values, teams can enhance the reliability of reporting and analysis processes.

![Cuneiform for Salesforce: Picklist Fields | Inactive Values in Use](img/reports/picklist-inactivevalues.gif)

> This `Picklist Fields | Inactive Values In-Use` report identifies picklist field values that are marked as inactive but are still being used in records.  It provides a visual breakdown of inactive picklist values across different objects and fields that helps Salesforce administrators and data quality teams identify discrepancies between picklist configurations and actual data usage.  

#### Identity Resolution Analysis (14 Reports)
Accelerate your Salesforce Data Cloud implementation with this insightful collection of Identity Resolution Analysis reports. These powerful tools enable you to identify the most suitable fields for identity resolution processes, a critical step in creating a unified customer view within Data Cloud.
> Salesforce professionals can leverage these reports to pinpoint fields that are primary contact point candidates for Data Cloud identity resolution.  Use the insights in these reports to inform matching rule design-decisions, streamline your data preparation efforts, and ensure accurate record matching within Data Cloud.

![Cuneiform for Salesforce: Resolution Fields | By Priority](img/reports/resolution-bypriority.gif)

> This `Resolution Fields | By Priority` report identifies and prioritizes fields suitable for identity resolution via Data Cloud based on their population rates and distinctness. It provides a visual breakdown of prioritization scores for fields like Email, Mobile, and Photo URL across different objects.  This report is invaluable for practitioners working on Customer 360 initiatives as it accelerates the identification of the most reliable fields for matching and merging contact records.

#### Low-Population Field Analysis (6 Reports)
Identify underutilized fields and optimize your Salesforce data model with this set of Low-Population Field Analysis reports. These reports provide valuable insights into fields with low population rates, enabling you to make informed decisions about data governance, field management, and system performance.
> Administrators and data architects can user these reports to pinpoint fields with population rates below specific thresholds (ex. such as 15%). By identifying low-population fields across various categories -- you can streamline your data model, drive data cleanup initiatives, identify field deprecation candidates, and ensure your Salesforce org maintains a lean and effective data structure.

![Cuneiform for Salesforce: Low Populated Fields | All](img/reports/lowpopulation-all.gif)

> The `Low Population Fields | All` report identifies fields with less than 15% population rate across different Salesforce objects. It provides a visual breakdown of low-populated fields by object and field type (custom vs. standard), along with field utilization statistics. This report enables practitioners to identify underutilized fields and focus on improving data completeness for critical fields.

#### Metadata Dependency Analysis (9 Reports)
Gain deep insights into your Salesforce metadata with this set of Metadata Dependency Analysis reports. These reports provide a comprehensive view of the complex relationships between custom fields and their associated metadata dependencies, empowering Salesforce professionals to make informed decisions about data management and system optimization.
> Administrators and developers can use these reports to identify custom fields with various types of metadata dependencies -- including ux, reporting, workflow dependencies. These reports provide valuable insights into fields with reporting, UX, or workflow dependencies, enabling teams to optimize their data model, business processes, and user experience.

![Cuneiform for Salesforce: Custom Fields | Empty | Total MDD](img/reports/customfields-empty-totalmdd.gif)

> This `Custom Fields | Empty | Total MDD` report identifies custom fields that are unpopulated but have metadata dependencies such as reporting, user interface, or workflow rules. It provides a visual breakdown of these empty fields by object accompanied by the number of dependencies for each field type. Use this report to identify potential technical debt, optimize user experience, and ensure that all custom fields serve a purpose.

#### Namespace Analysis (5 Reports)
This category offers a comprehensive set of reports designed to analyze and summarize field distribution, utilization, and object composition across different namespaces in your Salesforce org. These reports leverage the profiling capabilities of Cuneiform for CRM to provide detailed insights into field usage patterns for namespace-specific objects and fields.
> Salesforce administrators and architects can use these reports to gain a holistic view of the object / field / namespace distribution in their org, and make informed decisions about field management across namespaces. Teams can use these insights to streamline their data model, measure namespace package usage, and ensure efficient use of their Salesforce org's capacity.

![Cuneiform for Salesforce: Profiled Objects | By Namespace](img/reports/objectfields-bynamespace.gif)

> The `Profiled Objects | By Namespace` report provides an overview of profiled objects and fields grouped by their namespace. It offers a visual breakdown of the total number of fields per namespace accompanied by field utilization and profiling statistics. This report is useful in complex orgs with multiple packages or managed applications as it showcases the distribution of custom fields across multiple namespaces.

#### Object Reference Analysis (8 Reports)
Uncover the intricate web of relationships within your Salesforce org using this collection of reports. From field value distributions to empty reference fields, these analyses provide a clear picture of how objects are interconnected and where potential data gaps exist.
> Salesforce administrators and architects can use these insights to optimize data models, improve data quality, and enhance cross-object reporting capabilities. By understanding object relationships, teams can make informed decisions about data structure, consistency, and support more effective data governance and business processes.

![Cuneiform for Salesforce: Reference Fields | Empty vs. Populated](img/reports/reference-emptyvspopulated.gif)

> The `Reference Fields | Empty vs. Populated` report provides an analysis of reference fields across profiled Salesforce objects -- comparing their empty and populated statuses. It offers a visual breakdown of reference fields by object, distinguishing between empty and populated fields, along with key field utilization metrics and profiling statistics. This report helps practitioners improve overall data quality and maintain proper object relationships within the CRM.

#### Outlier Values Analysis (2 Reports)
Uncover exceptional data points in your Salesforce fields with this set of reports focused on identifying and quantifying outlier values. These analyses pinpoint field values that deviate significantly from the norm, appearing 10 times more frequently than average or exceeding typical population rates.
> Salesforce administrators and data quality specialists can leverage these reports to quickly spot field value anomalies, assess data integrity, and prioritize data cleansing efforts.  By identifying outliers, teams can improve data accuracy, enhance reporting trustworthiness, and optimize business processes reliant on clean, consistent data.

![Cuneiform for Salesforce: Field Value | Statistical Outliers](img/reports/fieldvalues-statisticaloutliers.gif)

> This `Field Values | Statistical Outliers` report identifies field values that occur 10x more frequently than the average of other field values based on their population rate. It provides a visual representation of these outlier values and their field utilization statistics across profiled Salesforce objects. Use this report to quickly spot anomalies potentially representing data entry errors, system issues, or unexpected patterns in business data that may require further investigation or cleanup.

#### Owner, Creator, and Modifier Analysis (6 Reports)
This set of reports offers valuable insights into user interactions with profiled Salesforce objects. By analyzing record ownership, creation, and modification patterns, these reports shed light on data stewardship and user engagement across your Salesforce org.
> Salesforce administrators and data quality teams can leverage these reports to identify key contributors, track data ownership trends, and optimize user permissions. This analysis aids in enhancing data governance strategies and pinpointing areas for targeted user training or process improvements.

![Cuneiform for Salesforce: Profiled Objects | By Record Owner](img/reports/profiledobjects-recordowner.gif)

> The `Profiled Objects | By Record Owner` report provides an analysis of record ownership distribution across profiled Salesforce objects. It offers a visual breakdown of the top record owners by object, showing the total number of records owned by each user or process.  Use this report to understand data ownership patterns, identify potential workload imbalances, and ensure proper data stewardship across the organization.

#### Profiling Segment Analysis (4 Reports)
These reports offer valuable insights into fields that warrant deeper examination for data profiling. These reports identify key fields and their associated values across objects, enabling a more granular understanding of your Salesforce data segments.
> Data architects and analysts can leverage these reports to pinpoint critical fields for segmentation, assess data quality within specific segments, and drive more targeted data governance strategies.  By utilizing these insights, teams can optimize their data profiling efforts and enhance the overall effectiveness of their CRM data management.

![Cuneiform for Salesforce: Profiled Fields | Segment Score](img/reports/segmentfields-segmentscore.gif)

> The `Profiling Segment Fields | Segment Score` report identifies and evaluates fields that are prime candidates for deeper data analysis based on utilization and composition. It provides a visual breakdown of segment scores across various fields and objects powered by field utilization statistics and insights.  Use this report to prioritize fields for in-depth analysis, data quality improvements, or segmentation strategies.

#### Record Type Usage (3 Reports)
This collection of reports examines the utilization of record types across Salesforce objects. By analyzing population rates and record counts, these reports provide a clear picture of how different record types are being used within your Salesforce org.
> Use these insights to optimize Salesforce object schemas, refine business processes across variations, and improve data quality for strategic Salesforce objects. Understanding record type usage patterns helps teams make informed decisions about simplifying complex business processes or identifying underutilized record types.  These efforts enhance CRM efficiency and user adoption.

![Cuneiform for Salesforce: Record Types | Populated Values %](img/reports/recordtypes-populatedvalues.gif)

> The `Record Types | Populated Values %` report provides a detailed breakdown of record type usage across Salesforce objects. It presents a visual comparison of different record types contrasting their population rate along with key profiling statistics and insights. Use this report to gain insights into how different record types are being used within your Salesforce org and which record types are underutilized.

#### Unpopulated Fields Analysis (7 Reports)
This suite of reports from Cuneiform for CRM zeroes in on fields with 0% population rates across various categories. From fields lacking governance properties to empty formula fields and abandoned fields without dependencies, these reports offer a comprehensive view of underutilized elements in your Salesforce org.
> Data architects and Salesforce administrators can harness these insights to streamline their org's data model, identify field deprecation candidates, and drive data governance outcomes.  By identifying fields ripe for retirement or requiring attention, teams can optimize storage, improve system performance, and ensure that every field in their CRM serves a clear purpose.

![Cuneiform for Salesforce: Empty Fields | Custom | Abandoned %](img/reports/customfields-empty-abandoned.gif)

> The `Empty Fields | Custom | Abandoned` report identifies custom fields that are completely unpopulated (0% population rate) and lack field descriptions, metadata dependencies, and data governance properties.  Use this report to identify unused custom fields that are deprecation candidates. By pinpointing custom fields that are unused and undocumented, practitioners can streamline their org's data model, improve end-user experience, and ensure that all custom fields serve a clear purpose.
 
For Salesforce administrators and business process owners, this report offers valuable insights into how record types are utilized within the org. By understanding which record types are most frequently used or underutilized, teams can streamline their data model, refine business processes, and ensure that the CRM structure aligns with actual business needs. This data-driven approach can lead to improved user adoption and more efficient use of Salesforce capabilities.

## [License](LICENSE.md)

The [reports in this repository are licensed](LICENSE.md) under the Creative Commons Attribution-NonCommercial 4.0 International License. You are free to use, share, remix, and adapt them, provided you give appropriate credit and do not use them for commercial purposes.

For more information, please refer to the [full license](https://creativecommons.org/licenses/by-nc/4.0/).