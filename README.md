**HandsMen Threads - Salesforce CRM Automation Project**

---

### ✍️ Project Title:

**HandsMen Threads CRM Automation Using Salesforce**

---

### 🚧 Problem Statement:

HandsMen Threads, a fast-growing fashion retail company, faced major issues with decentralized customer management, untracked order histories, lack of automated alerts for stock, and no defined loyalty program. Manual processes for creating customer records, managing inventory, confirming orders, and assigning roles caused inefficiencies and delays.

---

### 📊 Objective:

To implement a fully automated and centralized CRM system in Salesforce for:

* Managing customer and order records
* Sending order confirmation emails
* Tracking inventory and sending low-stock alerts
* Assigning loyalty statuses based on purchases
* Managing users through profiles and permission sets
* Ensuring validations via Apex triggers
* Scheduling inventory restock via Apex batch jobs

---

### 💼 Modules Covered:

1. **Data Modeling**

   * Custom Objects: `HandsMen_Customer__c`, `HandsMen_Order__c`, `HandsMen_Product__c`, `Inventory__c`
   * Relationships: Lookup relationships (e.g., Order to Customer)

2. **User Management**

   * Created users: Niklaus (Sales), Kol (Inventory), Elijah & Rebekah (Marketing)
   * Profiles: Platform 1
   * Roles: Sales, Inventory Manager, Marketing Manager
   * Permission Set: `Permission_Platform_1`

3. **Automation via Flows**

   * Record-Triggered Flow: Order confirmation email when status = Confirmed
   * Record-Triggered Flow: Low Stock alert when quantity < 5
   * Scheduled Flow: Update Loyalty Status based on Total\_Purchases\_\_c

4. **Email Templates & Alerts**

   * `Order_Confirmation_Email` (HTML Template with Classic Letterhead)
   * `Low_Stock_Alert` email template
   * Email Alerts for both flows

5. **Apex Implementation**

   * `OrderTriggerHandler`: Validates Quantity based on Order Status
   * `OrderTrigger`: Calls the handler
   * `InventoryBatchJob`: Batch Apex + Schedulable to restock products with quantity < 10

6. **Testing & Deployment**

   * Trigger tested via record creation in Developer Console
   * Batch job scheduled via `System.schedule` in Execute Anonymous window
   * All flows and automation tested successfully

---

### 🔧 Highlights of Automation:

* Real-time order confirmation emails to customers
* Inventory stock monitoring with auto alerts
* Loyalty program classification (Gold, Silver, Bronze)
* Apex validations prevent incorrect order entries
* Daily scheduled restocking job
* Seamless role/profile-based access control

---

### 🌐 GitHub Repository:

https://github.com/Vinuthnavadikari/handsmen-salesforce-project

---

### 📹 Demo Video:

https://drive.google.com/file/d/1gjLiBxG4vfPF4suuQns0lV4FL0TJsJui/view?usp=sharing
---

### 🎓 Submitted by:

**Vinuthna Vadikari**

---

### ✅ Conclusion:

This Salesforce implementation enables HandsMen Threads to transform their customer relationship, order tracking, and inventory management into a seamless, automated system. By leveraging Flows, Apex, and core CRM features, the solution provides scalability, accuracy, and business efficiency.
