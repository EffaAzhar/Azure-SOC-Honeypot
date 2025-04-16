# Azure SOC and Honeypot Implementation

[![License](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT) ## Overview

This project demonstrates the implementation of a basic Security Operations Center (SOC) and a honeypot environment within Microsoft Azure. The goal was to gain practical experience in:

* Deploying and configuring Azure Virtual Machines.
* Setting up a low-interaction honeypot.
* Integrating Azure logs with Microsoft Sentinel (Azure SIEM).
* Creating custom detection rules and alerts in Sentinel.
* Performing basic log analysis and threat hunting.

This project was inspired by a YouTube tutorial [Link to the YouTube video you followed].

## Technologies Used

* **Microsoft Azure:**
    * Azure Virtual Machines
    * Microsoft Sentinel
    * Azure Monitor Logs
    * [Mention any other Azure services you used]
* **Honeypot Software:** [Specify the honeypot software you used, e.g., Cowrie, Modern Honey Network (MHN)]
* **Scripting (Optional):** [Mention any scripting languages used, e.g., PowerShell, Python]

## Architecture

[Include a visual representation of your Azure architecture here. You can:
* Embed an image from your `screenshots/` folder: `![Azure Architecture](screenshots/architecture.png)`
* Use a tool like draw.io or Azure Diagram to create a diagram and save it as an image.]

This diagram illustrates the flow of logs from the Azure Virtual Machine (including the honeypot logs) into Azure Monitor Logs and subsequently into Microsoft Sentinel for analysis and alerting.

## Setup and Configuration

[Provide a high-level overview of the steps involved in setting up your project. You don't need to provide exact step-by-step instructions unless they are crucial and concise. Focus on the key components.]

1.  Deployed an Azure Virtual Machine to host the honeypot.
2.  Installed and configured [Honeypot Software Name] on the VM.
3.  Configured Azure Diagnostics to collect relevant logs from the VM and send them to Azure Monitor Logs.
4.  Onboarded the Azure subscription and the relevant log sources to Microsoft Sentinel.
5.  Created custom analytics rules in Sentinel to detect potential malicious activity based on honeypot logs and other Azure logs.
6.  [Mention any other significant configuration steps]

**For more detailed information on the setup of specific components, refer to the `documentation/` folder.**

## Log Analysis and Detections

[Describe your approach to log analysis and provide examples of the detection rules you created in Sentinel. You can include snippets of your KQL queries or explanations of the logic behind them.]

For example, I created a Sentinel analytic rule to detect SSH brute-force attempts on the honeypot VM by analyzing the authentication logs. The KQL query for this rule is located in `code/sentinel-queries/ssh-brute-force.kql`.

[Include examples of interesting logs you analyzed and what they indicated.]

## Honeypot Activity

[Describe the activity you observed on your honeypot. What kind of attacks or probes did it attract? Include screenshots or summaries of the captured data (be mindful of any sensitive information).]

The honeypot captured several attempts to connect via SSH and various probes looking for common vulnerabilities. [Optional: Include a screenshot of your honeypot logs or a summary table].

## Lessons Learned

[Share your key takeaways from this project. What did you learn about Azure security, SIEM, honeypots, and log analysis?]

* Understanding the importance of early threat detection using honeypots.
* Gaining practical experience with Microsoft Sentinel's capabilities for log ingestion, correlation, and alerting.
* Learning how to write effective KQL queries for security analysis.
* [Mention any challenges you faced and how you overcame them.]

## Next Steps (Optional)

[If you plan to expand on this project, mention your future goals.]

* Implement automated response playbooks in Sentinel.
* Integrate additional data sources into Sentinel.
* Deploy a more sophisticated, high-interaction honeypot.

## Author

[Your Name]
[Your GitHub Profile URL]
