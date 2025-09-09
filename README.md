# 🚀 Flask App CI/CD with Docker & GitHub Actions

A simple Flask application that is **automatically built, tested, and pushed to Docker Hub** using **GitHub Actions**. This project demonstrates a lightweight CI/CD pipeline for containerized apps.

---

## 📂 Project Structure

```bash
.
├── app.py                # Main Flask application
├── test_app.py           # Unit tests for the app
├── Dockerfile            # Docker image build instructions
├── requirements.txt      # Python dependencies
├── .gitignore
├── README.md
└── .github/
    └── workflows/
        └── cicd.yml    # GitHub Actions workflow
```

---

## ⚙️ Tech Stack

* **Flask** – Lightweight Python web framework
* **Docker** – Containerizes the app
* **GitHub Actions** – Automates build, test, and Docker push

---

## 🔁 CI/CD Pipeline Overview

Every push to the `main` branch triggers the following steps:

1. ✅ **Checkout code**
2. 📦 **Install dependencies**
3. 🧪 **Run unit tests**
4. 🐳 **Build Docker image**
5. 🚀 **Push image to Docker Hub**

> The pipeline is defined in `.github/workflows/cicd.yml`.

---

## 🧪 Running Locally

### 1. Clone the repo

```bash
git clone https://github.com/amitkumar0128/flask_docker_cicd.git
cd flask_docker_cicd
```

### 2. Install dependencies

```bash
pip install -r requirements.txt
```

### 3. Run the app

```bash
python app.py
```

> App will be available at `http://localhost:5000`

---

## 🐳 Build & Run with Docker

### Build image:

```bash
docker build -t flask-docker-ci .
```

### Run container:

```bash
docker run -p 5000:5000 flask-docker-ci
```

---

## 🧪 Run Tests

```bash
python test_app.py
```

---

## 🐙 GitHub Actions Workflow

Update your Docker Hub credentials in GitHub:

1. Go to your repo → **Settings** → **Secrets and variables** → **Actions**
2. Add these secrets:

   * `DOCKER_USERNAME`
   * `DOCKER_PASSWORD`

> These will be used to authenticate and push the image to Docker Hub securely.

---

## 📦 Docker Hub Image

> 🐳 [docker.io/akj49/flask-app](https://hub.docker.com/repository/docker/akj49/flask-app/general)

---

## 📄 License

MIT License

---

## 🙋‍♂️ Author

**Amit Kumar**
🔗 [GitHub](https://github.com/amitkumar0128)
