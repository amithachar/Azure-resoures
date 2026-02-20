# Azure-resoures
Azure resoures creation and app interlock applications.

-----------------------------------------------------------------------------------------------------------------------------------------
# Task 1 — Build an Order Processing Pipeline (Event-Driven)
-----------------------------------------------------------------------------------------------------------------------------------------

-----------------------------------------------------------------------------------------------------------------------------------------

# Step 1 — Create Azure Resources

You’ll need:

• Resource Group
• Storage Account
• Service Bus Namespace
• Service Bus Queue (orders-queue)
• Azure SQL or Cosmos DB
• Azure Function App
• Application Insights

Why Storage Account?

Azure Functions require it for:

Trigger state management

Scaling metadata

Logging checkpoints

Even serverless has infrastructure bones.

# Create Namespace 

<img width="1094" height="842" alt="image" src="https://github.com/user-attachments/assets/8dd30fc8-988f-4dda-9594-a3cd14d49736" />

<img width="1059" height="482" alt="image" src="https://github.com/user-attachments/assets/853beb19-4e69-479f-b855-b145e4c3e1e9" />

<img width="1094" height="541" alt="image" src="https://github.com/user-attachments/assets/cf593338-ecb3-41f1-aec4-6620a92dd037" />

<img width="1044" height="589" alt="image" src="https://github.com/user-attachments/assets/6c412ebe-aa09-4268-bf30-63048bd5e52a" />

-----------------------------------------------------------------------------------------------------------------------------------------

# Step 2 — Create Service Bus Queue

Create:

Queue name: orders-queue
Enable:

Dead-lettering

Duplicate detection (optional)

Lock duration ~30 seconds

Service Bus works on at-least-once delivery.
Meaning: your function might process a message more than once.

So your code must be idempotent (safe if executed twice).

That’s a real engineering concept. Tattoo it mentally.

# Create Bus Queue with following config

<img width="1889" height="865" alt="image" src="https://github.com/user-attachments/assets/773b2500-f97f-4dc7-8454-9873990a96f6" />


<img width="1888" height="837" alt="image" src="https://github.com/user-attachments/assets/cd5de254-acd1-4570-bb18-de61efcaf559" />

-----------------------------------------------------------------------------------------------------------------------------------------
# Step 3 — Create the Azure Function App

<img width="1233" height="842" alt="image" src="https://github.com/user-attachments/assets/2eeeafab-5c2e-4a48-88a0-57090c53c90c" />

<img width="1173" height="829" alt="image" src="https://github.com/user-attachments/assets/2804c839-94b9-4abd-bf11-a4abb1200794" />

<img width="1218" height="827" alt="image" src="https://github.com/user-attachments/assets/eb1e6fc3-c25d-427b-8d89-ea254f09bab0" />

<img width="1169" height="821" alt="image" src="https://github.com/user-attachments/assets/747d5aeb-6fdb-42b4-822c-2ffb9c82d090" />

<img width="1162" height="817" alt="image" src="https://github.com/user-attachments/assets/23495178-efe2-4b09-b3fc-266ff16267f0" />

<img width="1149" height="805" alt="image" src="https://github.com/user-attachments/assets/8e454c3b-e65a-41d3-b52f-c9bcdba86123" />








