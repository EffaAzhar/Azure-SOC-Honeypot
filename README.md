# Azure SOC and Honeypot Implementation

This project demonstrates the implementation of a basic Security Operations Center (SOC) and a honeypot environment within Microsoft Azure.

## Lab Breakdown

This repository is organized into sections corresponding to the parts of the lab:

* **part1-azure-setup/:** Notes on the initial Azure subscription setup.
* **part2-honeypot-vm/:** Details on creating the Windows 10 honeypot virtual machine and configuring its Network Security Group.
* **part3-log-inspection/:** Evidence of inspecting local security logs on the honeypot VM.
* **part4-log-forwarding-kql/:** Steps taken to set up the Log Analytics Workspace, Sentinel instance, configure the log connector, and initial KQL queries.
* **part5-log-enrichment-geoip/:** Implementation of the GeoIP watchlist and KQL query for enriching logs with location data.
* **part6-attack-map/:** The creation of a basic attack map in Sentinel Workbook.
* **screenshots/:** all relevant screenshots.

## Technologies Used

* **Microsoft Azure:**
    * Azure Virtual Machines
    * Microsoft Sentinel
    * Azure Monitor Logs
* **Scripting :** Kusto Query Language (KQL)


## Architecture

* Create a Resource Group and inside the resource group create Virtual Network.
* Create a Virtual Machine 'CORP-NET-EAST-2' and attach it to Virtual Network.
* Create Network Security Group and change the configuration so that VM is widely open to public internet.
* Create log Analytic Workspace and connect it to both Microsoft Sentinel(SIEM) and Virtual Machine.
This diagram illustrates the flow of logs from the Azure Virtual Machine (including the honeypot logs) into Azure Monitor Logs and subsequently into Microsoft Sentinel for analysis and alerting.

## Lab Objectives

The key objectives of this lab were to gain practical experience in:

* Creating and configuring Azure Virtual Machines for a honeypot.
* Managing Network Security Group rules for network access.
* Inspecting Windows Event Logs for security-related events.
* Setting up an Azure Log Analytics Workspace for centralized log storage.
* Deploying and connecting Microsoft Sentinel to the Log Analytics Workspace.
* Configuring log connectors to ingest Windows Security Events.
* Querying and analyzing logs using Kusto Query Language (KQL).
* Enriching logs with geographic location data using Sentinel Watchlists.
* Creating a basic attack map visualization in Sentinel Workbooks.
* Understanding the process of setting up a basic honeypot in Azure.
* Gaining experience with Azure Log Analytics Workspace as a central log repository.
* Learning how to deploy and connect Microsoft Sentinel to a Log Analytics Workspace.
* Practical application of configuring log connectors for ingesting security events.
* Developing skills in querying and analyzing logs using Kusto Query Language (KQL).
* Understanding the concept of log enrichment using Sentinel Watchlists to add valuable context (like geographic location).
* Basic introduction to creating visualizations like attack maps in Sentinel Workbooks.
  
This project was inspired by a YouTube tutorial [https://youtu.be/g5JL2RIbThM].

## Log Analysis and Detections

[Describe your approach to log analysis and provide examples of the detection rules you created in Sentinel. You can include snippets of your KQL queries or explanations of the logic behind them.]

For example, I created a Sentinel analytic rule to detect SSH brute-force attempts on the honeypot VM by analyzing the authentication logs. The KQL query for this rule is located in `code/sentinel-queries/ssh-brute-force.kql`.

[Include examples of interesting logs you analyzed and what they indicated.]

## Honeypot Activity

[Describe the activity you observed on your honeypot. What kind of attacks or probes did it attract? Include screenshots or summaries of the captured data (be mindful of any sensitive information).]

The honeypot captured several attempts to connect via SSH and various probes looking for common vulnerabilities. [Optional: Include a screenshot of your honeypot logs or a summary table].

## Author

[Your Name]
[Your GitHub Profile URL]
