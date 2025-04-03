# n8n_Workflows


## 1. Inventory Agent

A simple `Inventory Agent` that retrieves or updates inventory data stored in a Google Sheet based on user input.

Nodes used: 

AI Agent, OpenAI Chat Model, Simple Memory, Get Inventory (Tools), Update Inventory (Tools)

![Inventory_Agent1](https://github.com/user-attachments/assets/90b42a1b-ac27-4438-8f64-88b8ed23c35b)

![Inventory_Agent2](https://github.com/user-attachments/assets/d12d8900-c4fb-433b-8cd5-33309f94f164)

---

## 2. Order Status via Email

A simple workflow that retrieves order data from a Google Sheet and automatically sends an email notification to the specified recipient, updating them on the order status.

Nodes used: 

Google Sheet (anyUpdate), OpenAI (to compose email), Gmail (send: message)

![image](https://github.com/user-attachments/assets/c13e6716-3e14-4902-b9f5-136de8da7dc6)

---

