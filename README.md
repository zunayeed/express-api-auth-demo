# express-api-auth-demo

Express.js app exploring API authentication methods using Axios — No Auth, Basic Auth, API Key, and Bearer Token.

---

## 📖 About

This project demonstrates how to interact with a REST API using four different authentication methods. Built as a learning exercise using **Node.js**, **Express.js**, and **Axios**, it connects to the [Secrets API](https://secrets-api.appbrewery.com) to fetch data based on the auth type used.

---

## 🔐 Authentication Methods Covered

| Route | Endpoint | Auth Type |
|---|---|---|
| `/noAuth` | `/random` | No Authentication |
| `/basicAuth` | `/all?page=2` | Basic Auth (Username & Password) |
| `/apiKey` | `/filter` | API Key (Query Parameter) |
| `/bearerToken` | `/secrets/42` | Bearer Token (Authorization Header) |

---

## 🛠️ Tech Stack

- **Node.js**
- **Express.js**
- **Axios**
- **EJS** (Templating Engine)

---

## 🚀 Getting Started

### Prerequisites

Make sure you have **Node.js** installed on your machine.

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/express-api-auth-demo.git
   cd express-api-auth-demo
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Add your credentials in `index.js`:
   ```javascript
   const yourUsername = "your_username";
   const yourPassword = "your_password";
   const yourAPIKey = "your_api_key";
   const yourBearerToken = "your_bearer_token";
   ```
   > You can register and get your credentials at [secrets-api.appbrewery.com](https://secrets-api.appbrewery.com)

4. Start the server:
   ```bash
   node index.js
   ```

5. Open your browser and visit:
   ```
   http://localhost:3000
   ```

---

## 📁 Project Structure

```
express-api-auth-demo/
├── public/
├── views/
│   └── index.ejs
├── index.js
├── package.json
└── README.md
```

---

## 📌 Routes

- **`GET /`** — Home page
- **`GET /noAuth`** — Fetches a random secret with no authentication
- **`GET /basicAuth`** — Fetches all secrets from page 2 using Basic Auth
- **`GET /apiKey`** — Fetches secrets with embarrassment score ≥ 5 using an API Key
- **`GET /bearerToken`** — Fetches secret with ID 42 using a Bearer Token

---

## 📚 What I Learned

- How to make HTTP requests using **Axios**
- Difference between authentication methods (No Auth, Basic, API Key, Bearer Token)
- How to pass credentials via headers, query params, and auth config in Axios
- Rendering API responses in **EJS** templates

---

## 🙌 Acknowledgements

- (https://www.appbrewery.com/) for the Secrets API 
- [Axios Documentation](https://axios-http.com/docs/intro)
- [Express.js Documentation](https://expressjs.com/)

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).
