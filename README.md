Indian States REST API

Live Backend URL:
👉 https://node-assignment-3-cmj0.onrender.com

This is a REST API built using Node.js and Express.js that manages data of 28 Indian states including population, literacy rate, GDP, and annual budget.

🚀 Tech Stack

Node.js

Express.js

In-Memory Database (Array)

Deployed on Render

📌 Base URL
https://node-assignment-3-cmj0.onrender.com
📖 API Routes Documentation
🔹 1. Get All State Names

GET /states

✅ Description:

Returns the list of all state names.

🔗 Example:
GET /states
📤 Response:
[
  "Andhra Pradesh",
  "Arunachal Pradesh",
  "Assam",
  ...
]
🔹 2. Get State By ID

GET /states/:id

✅ Description:

Returns complete data of a specific state by ID.

🔗 Example:
GET /states/5
📤 Response:
{
  "id": 5,
  "name": "Chhattisgarh",
  "population": 25545198,
  "literacyRate": 70.28,
  "annualBudget": 121500,
  "gdp": 4000000
}
🔹 3. Get State With Highest GDP

GET /states/highest-gdp

✅ Description:

Returns the state having the highest GDP.

🔗 Example:
GET /states/highest-gdp
📤 Response:
{
  "state": "Maharashtra",
  "highestGDP": 35000000
}
🔹 4. Add New State

POST /states

✅ Description:

Adds a new state.

📥 Body:
{
  "name": "New State",
  "population": 1000000,
  "GDP": 500000
}
📤 Response:
{
  "id": 29,
  "name": "New State",
  "population": 1000000,
  "GDP": 500000
}
🔹 5. Replace State Data (Full Update)

PUT /states/:id

📥 Body:
{
  "name": "Updated Name",
  "population": 2000000,
  "literacyRate": 80,
  "annualBudget": 50000,
  "gdp": 7000000
}
🔹 6. Update Annual Budget

PUT /states/:id/annualbudget

📥 Body:
{
  "annualBudget": 500000
}
🔹 7. Update Population

PUT /states/:id/population

📥 Body:
{
  "population": 50000000
}
🔹 8. Update Literacy Rate

PATCH /states/:id/literacyrate

📥 Body:
{
  "literacyRate": 85.5
}
🔹 9. Update GDP

PATCH /states/:id/gdp

📥 Body:
{
  "gdp": 45000000
}
🔹 10. Partial Update (Any Field)

PATCH /states/:id

📥 Body Example:
{
  "population": 99999999,
  "literacyRate": 90
}
🔹 11. Delete State By ID

DELETE /states/:id

🔗 Example:
DELETE /states/10
🔹 12. Delete State By Name

DELETE /states/name/:statename

🔗 Example:
DELETE /states/name/Goa
🔹 13. Delete States Below Literacy Rate

DELETE /states/low-literacy/:percentage

🔗 Example:
DELETE /states/low-literacy/60
✅ Description:

Deletes all states having literacy rate below given percentage.

⚠️ Notes

This project uses an in-memory array, so data resets every time the server restarts.

IDs are auto-generated based on array length.

No database is used in this project.

🏁 Run Locally
npm install
node index.js

Server runs on:

http://localhost:3000