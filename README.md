# 🧠 Stable-FAST-API

A lightweight, modular API for generating images using Stable Diffusion via Hugging Face's Diffusers library. Built with FastAPI, this project is designed for speed, scalability, and secure access.

---

## 📌 Overview

Stable-FAST-API allows users to generate AI-powered images through a RESTful interface. It supports token-based authentication, customizable prompts, and easy deployment on platforms like Render or Railway.

---

## 🚀 Features

- ⚡ **FastAPI** backend for high-performance image generation
- 🔐 **Token-based authentication** via `authtoken.py`
- 🧨 **Stable Diffusion** integration using Hugging Face's `diffusers`
- 🧱 **Modular architecture** for easy extension and maintenance
- 📄 **Interactive Swagger docs** at `/docs`

---

## 🛠️ Tech Stack

| Layer        | Tools & Libraries                          |
|--------------|--------------------------------------------|
| Backend      | FastAPI, Uvicorn                           |
| AI/ML        | Diffusers, Transformers, Torch             |
| Auth         | Custom token-based system (`authtoken.py`) |
| Image Utils  | PIL (Python Imaging Library)               |
| Deployment   | Render, Railway, Vercel (optional)         |

---

## 📁 File Structure

```
Stable-FAST-API/
├── api.py            # FastAPI app with image generation routes
├── authtoken.py      # Token-based authentication logic
├── README.md         # Project documentation
```

---

## 📦 Installation

```bash
git clone https://github.com/Guna-Asher/Stable-FAST-API.git
cd Stable-FAST-API
pip install -r requirements.txt
```

---

## ▶️ Usage

Start the API locally:

```bash
uvicorn api:app --reload
```

Access Swagger UI at: [http://localhost:8000/docs](http://localhost:8000/docs)

---

## 🔒 Authentication

Include your token in the request header:

```http
Authorization: Bearer <your_token>
```

Tokens are managed in `authtoken.py`. You can customize this for database-backed or OAuth-based systems.

---

## 🧪 Example Request

```bash
curl -X POST "http://localhost:8000/generate" \
     -H "Authorization: Bearer your_token" \
     -H "Content-Type: application/json" \
     -d '{"prompt": "a futuristic cityscape at sunset"}'
```

---

## 📌 TODO

- [ ] Add support for prompt strength, seed, and negative prompts
- [ ] Integrate logging and error handling
- [ ] Add rate limiting and user roles
- [ ] Deploy to Render or Railway with environment variables

---

## 📫 Contact

Built with ❤️ by **Guna R**  
📍 MCA Student | Ethical AI Advocate | Full-Stack Developer  
🔗 [GitHub](https://github.com/Guna-Asher) • [LinkedIn](https://www.linkedin.com/in/guna-asher)

---

> “Technology should empower, not exclude.” – This project reflects my commitment to accessible and ethical AI.

```
