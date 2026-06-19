Simple REST API

A clean, simple REST API built with Node.js and Express.

Setup

bashnpm install
npm run dev     # development (auto-reload)
npm start       # production

Server starts at http://localhost:3000


API Endpoints

Health Check

MethodEndpointDescriptionGET/Check if API is running

Items (/api/items)

MethodEndpointDescriptionGET/api/itemsGet all itemsGET/api/items/:idGet a single itemPOST/api/itemsCreate a new itemPUT/api/items/:idUpdate an itemDELETE/api/items/:idDelete an item


Examples

Create an item

bashcurl -X POST http://localhost:3000/api/items \
  -H "Content-Type: application/json" \
  -d '{"name": "Orange", "description": "A citrus fruit"}'

Get all items

bashcurl http://localhost:3000/api/items

Update an item

bashcurl -X PUT http://localhost:3000/api/items/1 \
  -H "Content-Type: application/json" \
  -d '{"name": "Green Apple"}'

Delete an item

bashcurl -X DELETE http://localhost:3000/api/items/1


Project Structure

src/
├── index.js                  # App entry point
├── routes/
│   └── items.js              # Route definitions
├── controllers/
│   └── itemsController.js    # Business logic
└── middleware/
    └── errorHandler.js       # Error handling

Next Steps


Add a database (MongoDB, PostgreSQL, SQLite)
Add authentication (JWT)
Add input validation (Joi, Zod)
Add tests (Jest, Supertest)
