# Fitness Studio CRM 🏋️‍♀️

A Salesforce-based CRM solution for Fitness Studios that streamlines membership management, class scheduling, trainer allocation, and payments while enhancing customer engagement and business growth.

This project was built **phase-wise** to cover the entire Salesforce ecosystem — from data modeling to automation, Apex programming, analytics, and deployment.

---

## 📑 Table of Contents
- Phase 1: Problem Statement & Goals
- Phase 2: Salesforce Setup
- Phase 3: Data Modeling & Relationships
- Phase 4: Process Automation (Admin)
- Phase 5: Apex Programming (Developer)
- Phase 6: Integration (API & External Systems)
- Phase 7: LWC & UI Enhancements
- Phase 8: Testing & Deployment
- Phase 9: Reporting, Dashboards & Security
- Phase 10: Final Presentation & Demo Day

---

## Phase 1: Problem Statement & Goals
### 🎯 Problem Statement
Fitness studios often struggle with:
- Manual handling of memberships and renewals
- Lack of proper class scheduling and trainer assignments
- Difficulty in tracking payments and attendance
- Limited customer engagement and feedback management

### ✅ Goals
- Centralize membership, trainer, and class management
- Automate payment reminders, renewals, and notifications
- Track attendance, class popularity, and trainer performance
- Provide actionable insights with dashboards & reports
- Enhance customer engagement with loyalty points and feedback

---

## Phase 2: Salesforce Setup
**Steps Followed:**
- Created a new Salesforce Developer Org.
- Configured Company Information:
  - Company Name: FitLife Studio
  - Currency: INR (₹)
  - Locale: English (India)
- Created Profiles & Roles:
  - Admin
  - Trainer
  - Front Desk Staff
  - Manager
- Enabled features:
  - Email Deliverability
  - Activities (Tasks/Events)
  - Reports & Dashboards

---

## Phase 3: Data Modeling & Relationships
**Custom Objects Created:**
- **Member__c** → Fields: Name, Email, Phone, Membership Type, Status
- **Trainer__c** → Fields: Name, Expertise, Availability, Experience
- **Class__c** → Fields: Name, Type, Schedule, Trainer Lookup, Capacity
- **Attendance__c** → Fields: Member Lookup, Class Lookup, Date, Status
- **Payment__c** → Fields: Member Lookup, Amount, Mode, Status, Due Date

**Relationships:**
- Member → Payment = 1:M
- Member → Attendance = 1:M
- Class → Trainer = M:1
- Class → Attendance = 1:M

---

## Phase 4: Process Automation (Admin)
**Automations Implemented:**
- **Validation Rules:**
  - Membership Start Date ≥ Today
  - Payment Amount > 0
- **Workflow Rules:**
  - Send welcome email when a new member is created
- **Approval Process:**
  - Memberships above ₹25,000 require Manager approval
- **Flow Builder:**
  - Auto-assign members to trainers based on class type
  - Send payment reminder 3 days before due date
  - Update membership status on payment completion

---

## Phase 5: Apex Programming (Developer)
**Key Implementations:**
- **Trigger:** Auto-update Membership Status after Payment
- **SOQL Queries:** Fetch most attended classes in last 3 months
- **Batch Apex:** Monthly attendance summary emailed to Manager
- **Queueable Apex:** Bulk import of members from campaigns
- **Scheduled Apex:** Daily payment due report sent to Admin
- **Future Methods:** Send WhatsApp/SMS for class reminders
- **Test Classes:** Achieved 85%+ coverage on triggers & classes

---

## Phase 6: Integration (API & External Systems)
**Integrations Implemented:**
- REST API → Fetch live fitness supplement prices & integrate with studio shop
- Third-Party Payment API → Capture online payment confirmations
- Email-to-Case → Convert member queries into Cases for support

---

## Phase 7: LWC & UI Enhancements
**UI Enhancements Implemented:**
- **LWC Component (a):** Class Schedule Calendar for members
- **LWC Component (b):** Trainer Availability Display on Trainer record page
- **LWC Component (c):** Member Dashboard → Membership status, loyalty points, payments

---

## Phase 8: Testing & Deployment
**Steps Taken:**
- Sandbox Testing: Validated automations, triggers, APIs
- Deployment via Change Sets: Migrated Sandbox → Production
- Post-Deployment Checks:
  - Verified Reports
  - Ensured security roles working correctly
  - Tested Flow executions

---

## Phase 9: Reporting, Dashboards & Security
**Reports Created:**
- Active vs Expired Memberships
- Trainer Performance by Class Attendance
- Payments Collected vs Pending
- Most Popular Classes

**Dashboards:**
- Studio Overview Dashboard
- Revenue Tracker
- Attendance Heatmap
- Member Retention Insights

**Security Settings:**
- OWD: Payments = Private, Classes = Role-based access
- Role Hierarchy: Manager > Trainer > Staff
- Audit Trail enabled for monitoring changes

---

## Phase 10: Final Presentation & Demo Day
**Pitch:**
Fitness Studio CRM automates operations, improves customer retention, and provides actionable insights to enhance studio performance.

**Demo Flow:**
1. Member Registration
2. Trainer Assignment
3. Class Scheduling
4. Attendance & Payment
5. Renewal & Reminder Notification
6. Dashboard Insights

**Handoff Docs:**
- Admin Setup Guide
- Trainer & Staff User Manual
- Customer Onboarding Guide

**Showcase:**
Presented as a **Fitness Studio CRM Project** highlighting Salesforce skills for real-world business automation.

---

## 👨‍💻 Built With
- Salesforce Lightning Platform
- Apex (Triggers, Batch, Queueable, Scheduled)
- LWC (Lightning Web Components)
- REST APIs for Integration
- Reports & Dashboards

---

## 📌 Author
**Rucha Deshpande**  
B.Tech Final Year | Computer Science Engineering  
Prof. Ram Meghe Institute of Technology and Research, Amravati
Mob: 7249714504

