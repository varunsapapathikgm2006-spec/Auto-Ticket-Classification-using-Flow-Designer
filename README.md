
Auto Ticket Classification – ServiceNow
Overview

Auto Ticket Classification is a ServiceNow project that automatically classifies incoming support tickets based on their description and other ticket information.

The goal is to reduce manual effort by automatically identifying the appropriate category, subcategory, priority, and assignment group for a ticket.

Objectives

Automatically classify incoming incidents.

Reduce manual ticket-routing effort.

Improve ticket assignment accuracy.

Standardize incident categorization.

Speed up the incident resolution process.

Platform

Platform: ServiceNow

Environment: ServiceNow Developer Instance (PDI)

Application: Incident Management

Tables: incident, along with supporting configuration/data tables

Key Features
1. Automatic Classification

When an incident is created, the system analyzes information such as:

Short description

Description

Caller information

Existing ticket attributes

Based on the available information, the ticket can be classified into categories such as:

Hardware

Software

Network

Access

Email

2. Automatic Assignment

After classification, the system can automatically determine the appropriate assignment group.

Example:

Ticket:
"Unable to connect to company Wi-Fi"

Category:
Network

Assignment Group:
Network Support

3. Priority Determination

The system can also determine incident priority based on predefined rules.

Example:

Impact: High
Urgency: High

Priority: Critical

Implementation

The project can be implemented using ServiceNow features such as:

Business Rules

Client Scripts

Script Includes

Flow Designer

Decision Tables

Assignment Rules

Data Lookup Rules

REST APIs (optional)

Predictive Intelligence / Machine Learning (optional)

Basic Workflow
New Incident
     |
     v
Read Ticket Details
     |
     v
Analyze Description
     |
     v
Determine Category
     |
     v
Determine Assignment Group
     |
     v
Determine Priority
     |
     v
Update Incident
     |
     v
Ticket Ready for Support Team

Example
Input
Short Description:
Laptop is not connecting to Wi-Fi

Description:
I am unable to connect my company laptop to the office Wi-Fi.

Automated Output
Category: Network
Subcategory: Wi-Fi
Assignment Group: Network Support
Priority: 3 - Moderate

Testing

The following test cases can be used:

Test Case	Expected Classification
Password reset request	Access
Laptop not working	Hardware
Application not opening	Software
Cannot connect to Wi-Fi	Network
Email not receiving messages	Email
Project Structure
Auto-Ticket-Classification/
│
├── README.md
├── Business Rules/
├── Script Includes/
├── Client Scripts/
├── Flow Designer/
├── Assignment Rules/
└── Test Cases/

Future Enhancements

Integrate AI/ML-based ticket classification.

Use historical incidents as training data.

Automatically identify duplicate incidents.

Suggest knowledge articles.

Predict incident priority.

Automatically recommend resolution steps.

Provide classification confidence scores.

Conclusion

The Auto Ticket Classification project demonstrates how ServiceNow can automate incident categorization and routing. It can be extended from simple rule-based classification to an AI/ML-based solution as more historical ticket data becomes available.
