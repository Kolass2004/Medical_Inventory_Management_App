# Medical Inventory Management (Salesforce)

A lightweight application built on the Salesforce Platform to track, manage, and audit medical supplies for clinics, hospitals, and pharmacies.

## Team Details
 Team ID : NM2025TMID06302  
    - Team Size : 4  
    - Team Leader : Kolass Rexon J  
    - Team member : Ramakrishnan M  
    - Team member : Manojkumar M  
    - Team member : Rahul B

## Core Features

* **Inventory Tracking:** Manage medical supplies, quantities, and locations using custom Salesforce objects.
* **Expiry Date Automation:** Utilizes Salesforce Flow to automatically flag items nearing their expiry date and send notifications.
* **Automated Re-ordering:** Record-triggered flows can create draft Purchase Orders or Tasks when stock levels fall below a defined threshold.
* **Audit Trail:** Leverages Field History Tracking and a custom `Audit_Log__c` object to maintain a clear, compliant record of all inventory changes.
* **Lightning-Powered UI:** A modern, responsive user interface built with **Lightning Web Components (LWC)** for managing inventory items, suppliers, and orders.

## Salesforce Components

This project is built using a modern, source-driven approach and includes:

* **Custom Objects:** `Inventory_Item__c`, `Supplier__c`, `Purchase_Order__c`, `Stock_Audit__c`
* **Lightning Web Components (LWC):** A component-based UI for managing inventory.
* **Salesforce Flow:** Automation for low-stock alerts and expiry notifications.
* **Apex:** Custom controllers for LWC and business logic for managing inventory transactions.
* **Permission Sets:** `Inventory_Manager` and `Clinic_Staff` profiles to ensure proper access control.
* **Reports & Dashboards:** Pre-built reports for "Low Stock" and "Expiring Soon" items.

---

## Quick Start (Installation)

This project is designed for deployment using the Salesforce CLI (SFDX).

**Prerequisites:**
* [Salesforce CLI](https://developer.salesforce.com/tools/sfdxcli)
* A Salesforce Dev Hub (or a Developer Edition org)

**Steps:**

1.  **Clone the repository:**
    ```bash
    git clone [YOUR_REPOSITORY_URL]
    cd medical-inventory-management-app
    ```

2.  **Authorize your Dev Hub (if not already done):**
    ```bash
    sf org login web -d -a MyDevHub
    ```

3.  **Create a new Scratch Org for testing:**
    ```bash
    sf org create scratch -f config/project-scratch-def.json -a MedInventoryScratch -d
    ```

4.  **Push the source code to the scratch org:**
    ```bash
    sf project deploy start
    ```

5.  **Assign the required Permission Set:**
    ```bash
    sf org assign permset -n Inventory_Manager
    ```

6.  **(Optional) Load sample data:**
    ```bash
    sf data tree import -p ./data/sample-data.json
    ```

7.  **Open your scratch org and the app:**
    ```bash
    sf org open
    ```
    > In the App Launcher, search for and select "Medical Inventory Management".

---

## Project Documentation & Artifacts

All project planning, design, and testing documents are located in the `/Documents` folder.

* [**Ideation Phase**](Documents/Ideation_Phase/README.md): Initial brainstorming, mockups, and concepts.
* [**Requirement Analysis**](Documents/Requirement_Analysis/README.md): User stories, functional, and non-functional requirements.
* [**Project Planning Phase**](Documents/Project_Planning_Phase/README.md): Timelines, milestones, and high-level strategy.
* [**Project Design Phase**](Documents/Project_Design_Phase/README.md): Data model (ERD), solution design, and technical architecture.
* [**Performance Testing**](Documents/Perfomance_Testing/README.md): Test plans, use cases, and performance benchmarks.
* [**Video Demo**](Video%20Demo/): A complete video walkthrough of the application.


