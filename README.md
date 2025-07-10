🧵 HandsMen Threads Salesforce CRM Project Documentation
📖 Overview
HandsMen Threads, a progressive fashion organization, is implementing Salesforce CRM to modernize and automate its customer engagement, inventory tracking, and order fulfillment processes. This documentation outlines the entire Salesforce project architecture, including data modeling, automation, email communication, Apex development, and security implementation.

🎯 Project Goals
Centralize business data through a robust data model

Automate critical business processes like order confirmation, loyalty tracking, and stock management

Ensure data consistency and accuracy through validation and automation

Improve customer experience through timely communication and intelligent insights

🧵 Key Use Cases
Use Case	Description
Order Confirmation	Sends automatic emails to customers after order placement
Loyalty Management	Tracks customer spending and upgrades loyalty tiers dynamically
Stock Alerts	Notifies warehouse when product stock drops below 5 units
Bulk Order Processing	Runs scheduled job at midnight to process bulk orders and update inventory/financials

🧱 Salesforce Setup
🔐 Environment Configuration
Salesforce Developer Edition created

Authenticated with Salesforce CLI (SFDX)

Project initialized using Salesforce DX

🗂️ Data Model
📦 Custom Objects
Order__c

Product__c

Customer__c

Loyalty__c

🔑 Custom Fields
Stock_Level__c

Loyalty_Status__c

Total_Spent__c

Reward_Points__c

📋 Record Types & Layouts
Record Types to support order variations and loyalty levels

Custom Layouts for Sales and Warehouse teams

📊 Tabs & App
Tabs created for all major custom objects

Lightning App: HandsMen CRM with role-based accessibility

🔄 Automation Strategy
💡 Flows
Flow Type	Trigger	Action
Record-Triggered	On Order__c creation	Send email to customer
Record-Triggered	On Customer__c.Total_Spent__c update	Adjust loyalty tier
Record-Triggered	On Product__c.Stock_Level__c < 5	Notify warehouse
Scheduled Flow	Runs at 12:00 AM daily	Process bulk orders, update inventory & financials

✉️ Email Templates
Template Name	Purpose
Order Confirmation	Sent to customer after order placement
Loyalty Reward Notification	Informs customer about loyalty status change
Stock Alert Email	Sent to Warehouse Manager when stock is low

All templates use HTML format and are deployed with Flow actions or Apex.

💻 Apex Logic
🔧 Triggers
On Order__c → Maintain data relationship with Customer__c

On Customer__c.Total_Spent__c → Update Loyalty__c tier

📦 Classes
Class	Purpose
EmailUtility.cls	Sends dynamic emails via Apex
PurchaseLogicHandler.cls	Manages customer loyalty and purchase behavior tracking

🕓 Asynchronous Apex
🔁 Batch Apex
Batch Class: BulkOrderProcessorBatch

Purpose:

Update inventory and financial data

Handle nightly bulk orders

Scheduled Job: Executes every night at 12:00 AM

🔒 Security Model
Component	Description
Profiles	Sales_Rep, Warehouse_Manager
Roles	Defined for Sales, Inventory, Admin hierarchy
Permission Sets	Separate sets for Flow access, Reports, and App access
Users	Created and assigned with appropriate role/profile/permissions

🧠 Skills Applied
Skill	Application
Data Modeling	Built objects, relationships, fields, and record types
Lightning UI Design	Created modular pages using Lightning App Builder
Process Automation	Flows and Apex used to reduce manual work
Email Communication	Templated, automated email alerts and confirmations
Security	Configured fine-grained access with profiles and permission sets
Asynchronous Processing	Batch Apex to handle large data volumes efficiently

🗂️ Project Directory Structure
php
Copy
Edit
handsmen-threads-salesforce/
└── force-app/
    └── main/
        └── default/
            ├── objects/             # Custom Object Metadata
            ├── classes/             # Apex Classes (Business Logic, Utilities)
            ├── triggers/            # Apex Triggers (Order, Customer, Loyalty)
            ├── flows/               # Flow Definitions (RTFs, Scheduled)
            ├── layouts/             # Page Layouts for UIs
            ├── permissionsets/      # Permission Set Metadata
            └── flexipages/          # Lightning Pages for CRM App
├── sfdx-project.json                # Project Config File
└── README.md                        # Project Overview File
📅 Roadmap & Future Enhancements
 Integrate Payment Gateway for real-time transaction capture

 Add dashboards for Sales, Inventory, and Loyalty insights

 Launch Experience Cloud Portal for customer self-service

 Integrate third-party APIs for logistics and shipping

👥 Contributors
Lead Admin & Developer: Vadikari Vinuthna

Organization: HandsMen Threads

Contact: vinuthnavadikari2006@gmail.com

📄 License
This project is built for internal CRM enhancements and educational purposes. All trademarks and data models are the intellectual property of HandsMen Threads.
