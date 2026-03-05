# LinkedIn Clone Microservices API Documentation
<img width="1431" height="821" alt="image" src="https://github.com/user-attachments/assets/15f98c61-615a-4990-939a-83c6fcede6aa" />


This documentation outlines the RESTful API endpoints available in the LinkedIn Clone microservices architecture. The endpoints are grouped logically by their domains.

---

## 🔐 Auth Service
Authentication and user registration endpoints.

| Method | Endpoint | Description |
| :--- | :--- | :--- |
| `POST` | `/auth/register` | Register a new user |
| `POST` | `/auth/login` | Authenticate a user and receive a token |

---

## 👤 User Service
Endpoints for managing user profiles, files, resumes, and networks.

### General User Operations
| Method | Endpoint | Description |
| :--- | :--- | :--- |
| `GET` | `/api/users` | Get a list of all users (Admin) |
| `GET` | `/api/users/{id}` | Get a specific user by ID |
| `PUT` | `/api/users` | Update current user details |
| `DELETE` | `/api/users/{id}` | Delete a specific user by ID (Admin) |
| `GET` | `/api/users/profile` | Get the profile of the current authenticated user |
| `GET` | `/api/users/profile/{id}` | Get the profile of a specific user by ID |
| `GET` | `/api/users/friends` | Get a list of friends/connections for the current user |

### User Files & Resumes
| Method | Endpoint | Description |
| :--- | :--- | :--- |
| `POST` | `/api/users/upload` | Upload a user file (e.g., avatar, cover) |
| `GET` | `/api/users/files` | Get all files for the current user |
| `GET` | `/api/users/files/{type}`| Get a specific user file by its type |
| `GET` | `/api/users/resumes` | Get all uploaded resumes for the current user |

### User Experiences
| Method | Endpoint | Description |
| :--- | :--- | :--- |
| `POST` | `/api/users/experiences` | Create a new experience for the current user |
| `GET` | `/api/users/experiences` | Get all experiences for the current user |
| `GET` | `/api/users/experiences/{id}`| Get a specific experience by its ID |
| `PUT` | `/api/users/experiences/{id}`| Update a specific experience |
| `DELETE` | `/api/users/experiences/{id}`| Delete a specific experience |

---

## 📝 Post Service
Endpoints for creating, managing, and interacting with posts.

### Posts
| Method | Endpoint | Description |
| :--- | :--- | :--- |
| `POST` | `/api/posts` | Create a new post |
| `POST` | `/api/posts/upload` | Upload a file/media attached to a specific post |
| `GET` | `/api/posts` | Get all posts (feed) |
| `GET` | `/api/posts/{id}` | Get a specific post by ID |
| `DELETE` | `/api/posts/{id}` | Delete a specific post |

### Post Comments
| Method | Endpoint | Description |
| :--- | :--- | :--- |
| `POST` | `/api/posts/comments` | Add a comment to a post |
| `GET` | `/api/posts/comments/{id}` | Get a specific comment by ID |
| `GET` | `/api/posts/comments/replies/{id}` | Get all replies to a specific comment |
| `GET` | `/api/posts/comments/post/{id}` | Get all comments for a specific post |
| `DELETE` | `/api/posts/comments/{id}` | Delete a specific comment |

### Post Likes
| Method | Endpoint | Description |
| :--- | :--- | :--- |
| `POST` | `/api/posts/likes` | Like or unlike a post |

---

## 🏢 Company & Job Service
Endpoints for managing companies, job postings, categories, and applications.

### Company Management
| Method | Endpoint | Description |
| :--- | :--- | :--- |
| `POST` | `/api/company` | Create a new company page |
| `POST` | `/api/company/upload` | Upload a company file (logo, banner) |
| `GET` | `/api/company` | Get all companies (Admin) |
| `GET` | `/api/company/{id}` | Get a specific company by ID |
| `GET` | `/api/company/detailed/{id}` | Get detailed data for a specific company |
| `PUT` | `/api/company/{id}` | Update company details |
| `DELETE` | `/api/company/{id}` | Delete a specific company |

### Company Locations
| Method | Endpoint | Description |
| :--- | :--- | :--- |
| `POST` | `/api/company/locations` | Add locations to a company |
| `PUT` | `/api/company/locations/{id}`| Update a specific company location |
| `DELETE` | `/api/company/locations/{id}`| Delete a specific company location |

### Job Management
| Method | Endpoint | Description |
| :--- | :--- | :--- |
| `POST` | `/api/jobs` | Create a new job posting |
| `GET` | `/api/jobs` | Get all job postings |
| `GET` | `/api/jobs/{id}` | Get a specific job posting by ID |
| `GET` | `/api/jobs/detailed/{id}` | Get detailed information for a specific job |
| `GET` | `/api/jobs/company/{id}` | Get all jobs posted by a specific company |
| `GET` | `/api/jobs/category/{id}` | Get all jobs under a specific category |
| `GET` | `/api/jobs/sorted/{sortType}`| Get jobs sorted by date (e.g., ascending/descending) |
| `PUT` | `/api/jobs/{id}` | Update a specific job posting |
| `DELETE` | `/api/jobs/{id}` | Delete a specific job posting |

### Applied Jobs
| Method | Endpoint | Description |
| :--- | :--- | :--- |
| `POST` | `/api/jobs/applied` | Apply for a job |
| `GET` | `/api/jobs/applied/{id}` | Get all applications for a specific job ID |

### Job Categories
| Method | Endpoint | Description |
| :--- | :--- | :--- |
| `POST` | `/api/category` | Create a new job category |
| `GET` | `/api/category` | Get all job categories |
| `GET` | `/api/category/{id}` | Get a specific category by ID |
| `PUT` | `/api/category/{id}` | Update a specific category (Admin) |
| `DELETE` | `/api/category/{id}` | Delete a specific category (Admin) |

---

## 💬 Chat Service
Endpoints for real-time messaging and chat management.

| Method | Endpoint | Description |
| :--- | :--- | :--- |
| `POST` | `/api/chats` | Create a new chat session |
| `GET` | `/api/chats` | Get all chats for the current user |
| `GET` | `/api/chats/{id}` | Get a specific chat by ID |
| `DELETE` | `/api/chats/{id}` | Delete a specific chat |
| `POST` | `/api/chats/messages` | Send a new message in a chat |
| `PUT` | `/api/chats/messages/{id}` | Update a specific message |
| `DELETE` | `/api/chats/messages/{id}` | Delete a specific message |

---

## 📁 File Service
Endpoints for standalone file uploading and batch management.

| Method | Endpoint | Description |
| :--- | :--- | :--- |
| `POST` | `/api/files` | Upload a file directly and return its URL |
| `POST` | `/api/files/batch-delete` | Batch delete multiple files |
| `DELETE` | `/api/files/{id}` | Delete a specific file by its ID |


<img width="1129" height="697" alt="image" src="https://github.com/user-attachments/assets/d909fb79-46af-45c1-95c0-53e4477f5c26" />

