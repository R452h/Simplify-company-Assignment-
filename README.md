# AI Powered Digital Gold Investment Assistant

## Overview

This project simulates a simplified version of an AI-based investment assistant similar to the KuberAI workflow used in fintech platforms. The system interacts with users, identifies questions related to gold investment, and suggests investing in digital gold. If the user decides to proceed, the system processes the purchase and records the transaction.

The project demonstrates how conversational interaction can be connected with backend APIs to complete a financial transaction.

---

## Features

* Detects gold investment related queries.
* Provides a simple investment insight.
* Suggests digital gold purchase.
* Processes purchase requests through an API.
* Stores transaction data in a database.
* Provides API documentation for easy testing.

---

## Tech Stack

The project was built using the following technologies:

* Python
* FastAPI
* Uvicorn
* SQLite
* Google Colab
* ngrok

---

## System Workflow

1. The user asks a question about gold investment.
2. The Chat API receives the query.
3. The system checks if the message contains gold related keywords.
4. If the query is relevant, the system suggests buying digital gold.
5. The user proceeds with the purchase.
6. The Buy Gold API calculates the gold quantity based on the investment amount.
7. The purchase details are stored in the database.
8. A confirmation message is returned to the user.

---

## API Endpoints

### Chat API

**Endpoint**

```
POST /chat
```

**Example Request**

```json
{
 "message": "Should I invest in gold?"
}
```

**Example Response**

```json
{
 "answer": "Gold is considered a safe investment and protects against inflation.",
 "nudge": "You can invest in digital gold instantly through our platform."
}
```

---

### Buy Gold API

**Endpoint**

```
POST /buy-gold
```

**Example Request**

```json
{
 "user_name": "Sushant",
 "amount_in_inr": 5000
}
```

**Example Response**

```json
{
 "message": "Digital gold purchased successfully",
 "gold_grams": 0.833,
 "amount_paid": 5000
}
```

---

## Database

A SQLite database named **gold.db** is used to store transaction data.

### Table: gold_purchases

| Column      | Description            |
| ----------- | ---------------------- |
| id          | Unique transaction ID  |
| user_name   | Name of the user       |
| gold_amount | Gold purchased (grams) |
| price       | Amount invested        |
| date        | Transaction timestamp  |

---

## Running the Project

1. Install the required dependencies.

```
pip install fastapi uvicorn pyngrok nest_asyncio
```

2. Run the FastAPI server.

```
uvicorn main:app --reload
```

3. Start ngrok to expose the API.

```
ngrok http 8000
```

4. Open the API documentation.

```
http://localhost:8000/docs
```

or using the ngrok public URL.

---

## Future Improvements

Some possible improvements for this project include:

* Integrating a real AI model for better query understanding.
* Fetching real-time gold prices from an external API.
* Adding a user interface for chat interaction.
* Implementing authentication and transaction history features.

---

## Conclusion

This project demonstrates how an AI-like assistant can guide users from asking an investment question to completing a digital gold purchase through APIs. The implementation is simple but shows how conversational systems can be connected with backend services in financial applications.


## Screenshot 


<img width="1920" height="1080" alt="Screenshot (74)" src="https://github.com/user-attachments/assets/bffd3917-c140-4296-9a8d-9fdf253be5c3" />

<img width="1920" height="1080" alt="Screenshot (75)" src="https://github.com/user-attachments/assets/55a69142-0f1f-4875-b125-3d8a6eb754a5" />

<img width="1920" height="1080" alt="Screenshot (76)" src="https://github.com/user-attachments/assets/2691ad9f-c2aa-472b-b7ad-5ddafe648d13" />

<img width="1920" height="1080" alt="Screenshot (77)" src="https://github.com/user-attachments/assets/24c1e211-056b-450d-8d71-f6c0ca1f16d2" />






