## Activity File:  Interview Questions 

### Instructions

The work you did on this project cuts across a wide range of topics: network security logging and monitoring, offensive and defensive security.

When networking and talking to potential employers, you should know how to discuss the work you did on your project to address specific interview questions or to show your skills within a specific domain. This section will teach you how to do this.

First, you will choose a domain that you are interested in pursuing as a career. For this project, you will choose from among the following domains:

-  Network Security

- Logging & Monitoring

- Offensive Security

- Defensive Security: Incident Response Phases I & II

If you are unsure of which domain you would like to focus on, that's ok! You can either choose the one that you are the most comfortable discussing, or you can also complete the tasks in two or three domains.

For each domain, you will be provided a set of interview questions.  For each question, you will be prompted to think about specific aspects or tasks you completed in Project 2 that you can use to answer the question.

In this section, you will:

- Select one domain and one question.

- Write a one-page response that answers the question using specific examples from your work on Project . Your response should flow and read like a presentation while still keeping the general structure of the technical question response guidelines. 


A good response includes the following: 


- Restate the Problem

- Provide a Concrete Example Scenario

- Explain the Solution Requirements

- Explain the Solution Details

- Identify Advantages/Disadvantages of the Solution​

Including each of these components will ensure you provide the interviewer with proof of competency of subject matter and critical thinking. 

**Submission Guidelines​**: You will submit your one-page response. At the end of the project, you will have the opportunity to present your answer if you desire

---

### Common Interview Questions

Below you will find a list of questions, grouped by specific domains. Select one question to answer. 

For each question, feel free to use the provided prompts to structure each section of your response. 

### Domain: Defensive Security

#### Question 1: Intrusion Detection Systems

"What does an intrusion detection system (IDS) do and how does it do it?"

1.  Restate the Problem
    > Answer: An `IDS` or Intrusion Detection System is a passive device or software that monitors network traffic for malicious activity or policy violations. The device resides within the network architecture and reports to the `IDS Management` server. 
  
2.  In Project 2, which logging and monitoring systems were in place?
    > Answer: The logging and monitoring system used was an ELK stack; specifically, Kibana. I utilized Kibana to search, view, and visualize the data indexed in Elastisearch. 
        
3.  Explain the Solution Requirements

    -   What did Kibana do while you performed your engagement on Day 1?
      > Answer: For Day 1, Kibana logged information like such as: Nmap scans, the Hydra Brute Force Attack, and the PHP reverse shell. 
    -   What did you use Kibana for on Day 2?
      > Answer: For Day 2, I used Kibana for creating dashboards and visualizations to better interpret data and paint a clearer'big picture' of the data between the Kali machine and the Capstone machine. 
    -   How did Kibana capture the data that it did?
      > Answer: Kibana utilized Metricbeat, Filebeat, and Packetbeat to capture the data flow between the machines. 

4.  Explain the Solution Details

    -   Did Kibana collect logs from all machines on the network? If not, which machines did not send logs to Kibana?
      > Answer: Yes, On the dashboard I created you can see logs from all of the machines on the network. 
    -   How could Kibana be configured to capture some of the data that it did not collect?
      > Answer: I could implement various and install other packages outside of the 3 required for this project such as: Winlogbeat, Auditbeat, etc. 

    -   Which tools did you use to analyze the data: search, queries, dashboards, etc.?
      > Answer: Most of the information I analyzed was via searches, dashboards, and visualisations.
5.  Identify Advantages and Disadvantages of the Solution

    -   Should all machines on a network be subject to monitoring?
      > Answer: I believe that all machines should be subject to monitoring because it'll help with the security. If a machine is left without monitoring, that machine could be the culprit for exploitation. 
    -   How do you decide which metrics to monitor?
      > Answer:  I would decide which metrics to monitor based off the services and ports operating on a machine. For this specific project I monitored a web server via Port 80. This meant we needed Filebeat, Metricbeat, and Packetbeat to monitor basic information communicated to and from the web server. More beats could be installed to enhance understanding of the data. 

#### Question 2: HIDS vs NIDS

"What is the difference between a HIDS and a NIDS? When would Blue Team operatives use one over the other?"

1.  Restate the Problem
  > Answer: `HIDS` are Host-based Intrusion Detection Systems, and `NIDS` are Network-based Intrusion Detection Systems. HIDS are considered to be the last line of defense because they target things at the host level. Where as NIDS operate at a much higher level and can protect various other things like print-servers, routers, and VPN concentrators. 


2.  Provide a Concrete Example Scenario

    -   In Project 2, which logging and monitoring systems were in place?
      > Answer: For this project Kibana was a NIDS. Data was sent from the Capstone Machine to the ELK server running Kibana. After installing the 3 beat packages mentioned above, I was able to gather information about which machines were communicating, and what was happening within those communications. 


1.  Identify Advantages and Disadvantages of the Solution

    -   Can a network have both HIDS and NIDS?
      > Answer: In short, Yes. A network should employ HIDS to monitor the individual laptops or computers. There should also be NIDS to monitor the network as a whole.  
      
    -   When is it appropriate to use a HIDS?
      > Answer: An appropriate time to use a HIDS is when you want to remove a laptop from the network and take it to the field. If an employee plugs in a compromised USB drive the HIDS can quarantine the malicious file(s). 
    
    -   When is it appropriate to use a NIDS?
      > Answer: It is always appropriate to use a NIDS. It is ideal to have these running to be able to monitor traffic flowing across the network. 
     
#### Question 3: Dashboards

Why are dashboards so important for log analysis?

1.  Restate the Problem
  > Answer: Dashboards are important because it is often difficult to vizualize large sums of data. For example, during my Nmap scan of the Capstone machine, there were 127,119 hits. The dashboard can help me see and understand: when these hits happened, and there frequency over specific periods of time; who was conducting the scan; and what they were searching for. If I were to simply pull up a log without a dashboard I would have a difficult time parsing through 127,119 hits. 

2.  Explain the Solution Requirements

    -   What kinds of data did you look for during your analysis?
      > Answer: I would look for data such as: user_agent, HTTP response codes, source_ip, destination_ip, etc. 
      
    -   Which tools did you use to analyze the data -- search, queries, dashboards, etc.?
      > Answer: I used Filebeat, Metricbeat, and Packetbeat to analyze the data and create the dashboard.

    -   Relative to the other tools, how much did you use dashboards and why?
      > Answer: I used the dashboard initially to get an understanding of what transpired on the network. Then I began my searches to dig deeper into the indexed data. 
      
1.  Explain the Solution Details

    -   Which dashboards did you use? Give at least three specific examples, including:
    > Answer 1: First I used the http transactions dashboard. This dashboard helped paint a picture of when the Nmap scan occured. I could see counts of HTTP traffic going to the Capstone machine which is telling of a port scan. 
    > 
    > Answer 2: The next dashboard, and my personal favorite, was the dashboard for the Hydra Brute Force Attack. This dashboard showed how fast Hydra was working to work against cracking Ashton's password. The highest frequency I observed was 31 counts/millisecond, which is obviously inhuman and a clear example of a malicious attack. 
    > 
    > Answer 3: Finally, the dashboard showing network traffic between hosts was interesting. Obviously the traffic between the ELK server and the Capstone machine would have the most data in this instance because the attacks were relatively minor and no significant files were traveling between the Kali and Capstone machines. However the next two hosts talking the most were indeed the Kali and Capstone machine. 


1.  Identify Advantages/Disadvantages of the Solution

    -   Suppose you couldn't use dashboards. Which tools would you use instead?
      > Answer: If I was unable to use the dashboard I would next use the search functions. I would need to make sure to study the data and figure out how to manipulate the data within the search to get the same visual effects. Using things like `top`, `sort by`, and `user_agent.original` were vital for the success of this project. 

---

© 2020 Trilogy Education Services, a 2U, Inc. brand. All Rights Reserved.  
