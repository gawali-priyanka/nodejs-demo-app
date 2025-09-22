# Node.js CI/CD Pipeline with GitHub Actions and Docker
## TASK 1
---


This project demonstrates a CI/CD pipeline to automatically build, test, push, and deploy a Dockerized Node.js application using: <br>

1) Node.js – simple HTTP server <br>
2) GitHub Actions – CI/CD automation <br>
3) Docker & DockerHub – containerization and image registry <br>
4) Amazon EC2 – deployment <br> 

---

## Folder Structure

nodejs-demo-app/ <br>
├── .github/ <br>
│   └── workflows/ <br>
│       └── main.yml <br>
├── screenshots/ <br>
│   ├── github-actions-success.png <br>
│   ├── browser-response.png <br>
│   ├── dockerhub-image.png <br>
│   └── curl-response.png <br> 
├── Dockerfile <br>
├── index.js <br>
├── README.md <br>
└── package.json <br>

## CI/CD Pipeline Flow 

1) Push code to the main branch. <br>
2) GitHub Actions builds the Docker image and pushes it to DockerHub. <br> 
3) EC2 instance pulls the image and deploys the app using Docker. <br>

## Screenshots

GitHub Actions Workflow – Success
Shows a successful CI/CD run triggered by a push to the main branch.
![Screenshot](screenshot/Github-action.png) 

---


App Output – Browser
Confirms the app is running successfully on port 3000.
![Screenshot](screenshot/browser-responce.png)

---

App Output – Curl
Confirms the app is running successfully on EC2 at port 3000.
![Screenshot](screenshot/curl-responce.png)

---

DockerHub – Image Pushed
Docker image is available on DockerHub after CI/CD completion.
![Screenshot](screenshot/dockerhub.png)

---

## Live on EC2

**Access via**: `http://<your-ec2-public-ip>:3000`
