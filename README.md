# Building-a-Network-Attack-Monitoring-and-Detection-System-using-ELK-Stack
In the process of building a SIEM system using the ELK Stack, several crucial steps determine the system's success.

First, the most important step is deploying and configuring the main components, including Elasticsearch for data storage, Logstash for log processing, and Kibana for data display. Ensuring these services are stable and interconnected is fundamental to the entire system.

Next is the step of collecting logs from the system, using Filebeat to retrieve data from the /var/log/auth.log file on the Linux machine. This is a critical step because if logs are not sent correctly, the entire system will lack data for analysis.

Then, the Logstash pipeline needs to be configured to receive logs from Filebeat and forward them to Elasticsearch. Defining the input (port 5044) and output (index security-logs-*) helps to ensure that the stored data is organized and easily queried.

Another crucial step is attack simulation, using Kali Linux to perform SSH brute-force attacks. This step generates realistic data to test the system's detection capabilities.

Finally, the data analysis and visualization step in Kibana clearly demonstrates the value of the SIEM system. Users can search for events such as "Failed password," track the attacking IP address and the time the event occurred, thereby detecting unusual behavior.
