# Google Form Clone - REST API

## 📌 Overview
This is a REST API backend for a **Google Form-like** application, allowing users to **create, manage, and submit online forms**.  
Built with **Node.js** and **Express.js**, it implements **JWT authentication** for security and follows RESTful principles.

## 🚀 Features
✅ **User Authentication** (Register, Login, JWT-based security)  
✅ **Form Management** (CRUD operations for forms)  
✅ **Question Handling** (CRUD operations for form questions)  
✅ **Answer Options** (CRUD operations for multiple-choice options)  
✅ **User Invitations** (Send & manage form invitations)  
✅ **Answer Submission** (Users can submit form responses)  
✅ **Response Analysis** (View submitted responses & summaries)  

---

## 🛠️ Tech Stack
- **Node.js** - JavaScript runtime for backend  
- **Express.js** - Lightweight web framework  
- **MongoDB / PostgreSQL** - Database storage for forms & responses  
- **JWT (JSON Web Token)** - Authentication & authorization  
- **Postman / Swagger** - API testing & documentation  

---

## 📌 API Endpoints
### 🔐 **Authentication**
| Method | Endpoint           | Description            |
|--------|--------------------|------------------------|
| POST   | `/register`        | Register new user     |
| POST   | `/login`           | User login            |
| POST   | `/refresh-token`   | Refresh auth token    |

### 📄 **Form Management**
| Method  | Endpoint                | Description                       |
|---------|-------------------------|-----------------------------------|
| GET     | `/forms`                 | Get all user-created forms       |
| POST    | `/forms`                 | Create a new form                |
| GET     | `/forms/:id`             | Get a specific form              |
| GET     | `/forms/:id/users`       | Show form to users               |
| PUT     | `/forms/:id`             | Update an existing form          |
| DELETE  | `/forms/:id`             | Delete a form                    |

### ❓ **Questions & Options**
| Method  | Endpoint                                         | Description                   |
|---------|-------------------------------------------------|-------------------------------|
| GET     | `/forms/:id/questions`                         | Get form questions           |
| POST    | `/forms/:id/questions`                         | Add a question               |
| PUT     | `/forms/:id/questions/:questionId`            | Update a question            |
| DELETE  | `/forms/:id/questions/:questionId`            | Delete a question            |
| POST    | `/forms/:id/questions/:questionId/options`     | Add options to a question    |
| PUT     | `/forms/:id/questions/:questionId/options/:optionId` | Update an option |
| DELETE  | `/forms/:id/questions/:questionId/options/:optionId` | Delete an option |

### 📩 **Invitations**
| Method  | Endpoint                | Description                     |
|---------|-------------------------|---------------------------------|
| GET     | `/forms/:id/invites`    | Get list of invited users      |
| POST    | `/forms/:id/invites`    | Invite users to fill the form  |
| DELETE  | `/forms/:id/invites`    | Remove an invitation           |

### ✏️ **Answer Submission**
| Method  | Endpoint                | Description                   |
|---------|-------------------------|-------------------------------|
| POST    | `/answers/:formId`      | Submit answers to a form     |

### 📊 **Response Management**
| Method  | Endpoint                      | Description                        |
|---------|------------------------------|------------------------------------|
| GET     | `/responses/:formId/list`     | Get submitted responses           |
| GET     | `/responses/:formId/summaries`| Get summary statistics            |

---

## 🔐 Security
- **JWT Authentication** is required for protected endpoints.
- Middleware `jwtAuth()` verifies tokens before granting access.

---

## 📖 How to Use
### 1️⃣ Clone the Repository
```bash
git clone https://github.com/your-username/your-repo-name.git
cd your-repo-name
