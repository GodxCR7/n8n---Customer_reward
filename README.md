# Loyal Customer Reward Automation (n8n)

An automated **customer loyalty reward system** built using **n8n** that identifies repeat customers and sends personalized rewards based on their shopping behavior.

This workflow helps businesses **increase customer retention and engagement** by automatically rewarding loyal customers and re-engaging inactive ones.

---

# Overview

The workflow processes customer transaction data and triggers different reward messages depending on customer activity.

Rewards include:

- **Welcome Bonus** for first-time customers  
- **Cashback Reward** for loyal repeat customers  
- **Win-Back Offer** for inactive customers  

The system reads customer data from **Google Sheets**, evaluates conditions using **n8n logic nodes**, and automatically sends reward emails using **Gmail integration**.

---

# Workflow Logic

The automation follows this logic:

1. **Webhook Trigger**
   - Receives transaction data when a customer makes a purchase.

2. **Fetch Customer Data**
   - Retrieves customer information from **Google Sheets**.

3. **Evaluate Customer Behavior**
   - Checks the customer's visit count and last visit date.

4. **Reward Decision**
   - If visit count = 1 → **Welcome Bonus**
   - If visit count = 5 → **Loyalty Cashback Reward**
   - If last visit > 30 days → **Win-Back Offer**

5. **Send Reward Email**
   - Sends a personalized email with reward details.

---

# Features

- Event-driven automation using **webhooks**
- Customer segmentation using **conditional logic**
- Automated **loyalty reward distribution**
- Personalized reward email notifications
- Integration with **Google Sheets and Gmail**
- Fully automated workflow built with **n8n**

---

# Tech Stack

- **n8n** – Workflow automation platform  
- **Google Sheets** – Customer data storage  
- **Gmail API** – Sending reward emails  
- **Webhook** – Triggering workflow on transactions

---

# Example Rewards

| Condition | Reward |
|-----------|--------|
| First Visit | Welcome Bonus (50 points) |
| 5th Visit | 10% Cashback Reward |
| Inactive for 30+ Days | Win-Back Offer (20% discount) |

---

# Workflow Structure

Main nodes used in the workflow:

- Webhook Trigger
- Google Sheets Node
- IF Logic Nodes
- Set Nodes (Reward Generation)
- Gmail Node (Email Delivery)

---

# Use Case

This automation can be used by:

- Retail stores
- Small businesses
- E-commerce stores
- Customer loyalty programs

It helps businesses **reduce manual tracking of loyal customers and automate engagement campaigns.**

---

# How to Use

1. Install **n8n**
2. Import the `workflow.json` file
3. Connect your credentials:
   - Google Sheets
   - Gmail
4. Update your Google Sheet with customer data
5. Activate the workflow

---

# Future Improvements

- Add **SMS notifications**
- Integrate **CRM systems**
- Add **customer points tracking**
- Dashboard for loyalty analytics

---

# Author

**Pratik Nayak**  
MCA Student | Automation & AI Enthusiast  

Focused on building **automation systems that reduce manual work and improve operational efficiency.**
