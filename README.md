# TNSkills-servicenow-IT-procurement-automation
TNSkills Team Project servicenow-IT-procurement-automation
# Streamlining IT Procurement: Automating Standard Laptop Procurement

## Naan Mudhalvan - ServiceNow Project

This project was developed as part of the *Naan Mudhalvan ServiceNow training program*. The project focuses on automating the IT procurement process for standard laptops using the *ServiceNow platform*. The solution uses Service Catalog, Flow Designer, approvals, catalog tasks, and assignment groups to create a simple end-to-end automated procurement workflow.

---

## 📌 Project Overview

In a typical organization, requesting and procuring IT hardware such as laptops can involve multiple manual steps, including:
- Submitting a hardware request
- Getting approval
- Creating procurement tasks
- Assigning tasks to the appropriate team
- Tracking the request

This project demonstrates how these steps can be streamlined using *ServiceNow automation*. The workflow allows an employee to request a standard laptop through the Service Catalog. After the request is submitted and approved, ServiceNow automatically creates the required catalog task and assigns it to the appropriate *Hardware* assignment group.

---

## 🎯 Objectives

The main objectives of this project are:
- Create a Standard Laptop Service Catalog item
- Allow users to place laptop requests through the Service Catalog
- Implement an approval process
- Automate catalog task creation after approval
- Automatically assign the task to the Hardware assignment group
- Update task information through Flow Designer
- Reduce manual intervention in the IT procurement process
- Demonstrate an end-to-end automated ServiceNow workflow

---

## 🛠️ Technologies & Skills

- *ServiceNow*
- *Service Catalog*
- *Flow Designer*
- *Service Catalog Items*
- *Catalog Tasks*
- *Approvals*
- *Assignment Groups*
- *Workflow Automation*
- *IT Service Management (ITSM)*

---

## 🔄 Project Workflow

The automated procurement workflow is illustrated below:

![ServiceNow Procurement Workflow]

<img width="1024" height="559" alt="WhatsApp Image 2026-10-12 at 7 35 12 PM" src="https://github.com/user-attachments/assets/3339bb7b-2585-4486-a58c-648f0628a9f6" />


---

## ⚡ Key Features Implemented

- **Dynamic Service Catalog Item:** Built a user-friendly form allowing employees to specify their laptop model, department, and business justification.
- **Automated Approval Routing:** Configured conditional logic to automatically trigger manager and financial approvals based on the request type.
- **Flow Designer Integration:** Replaced legacy workflows with a modern Flow Designer trigger that reacts instantly upon approval status updates.
- **Automated Task Assignment:** Programmatically generates a **Catalog Task** and routes it straight to the **Hardware Procurement Group** without manual queue sorting.

---

## 💻 Step-by-Step Implementation Guide

If you want to recreate or understand how this workflow was built in ServiceNow, follow these configuration steps:

1. **Create the Service Catalog Item:**
   - Navigate to **Service Catalog > Maintain Items**.
   - Create a new item named **Standard Laptop** and add relevant variables (e.g., Business Justification, Preferred Model).
2. **Configure Flow Designer:**
   - Go to **Flow Designer > Designer** and create a new Flow named `Laptop Procurement Workflow`.
   - Set the Trigger to **Service Catalog** (fires when an order is placed).
3. **Add Approval Action:**
   - Add an **Ask for Approval** action to route the request to the employee's manager or approval group.
4. **Automate Task Creation:**
   - Add a **Create Catalog Task** action linked to the flow.
   - Configure the template to set the **Assignment Group** to `Hardware` and assign short descriptions automatically.

---

## 🧪 How to Test the Workflow

1. Navigate to the **Service Catalog** in your ServiceNow developer instance.
2. Search for and open the **Standard Laptop** catalog item.
3. Fill out the required variables and click **Order Now**.
4. Check the generated Request (REQ) and Requested Item (RITM) stages.
5. Verify that the approval triggers correctly and that once approved, the **Catalog Task** is automatically created and assigned to the **Hardware** group.





