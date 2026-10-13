# Automated Python Application Deployment on AWS using Jenkins

## 📋 Table of Contents
1. [Introduction](#introduction)
2. [Architectural Diagram](#architectural-diagram)
3. [Input / Setup Configuration](#input--setup-configuration)
4. [Output / Execution](#output--execution)
5. [Conclusion](#conclusion)

---

## 🚀 1. Introduction
This project demonstrates a fully automated CI/CD pipeline for deploying a Python web application on Amazon Web Services (AWS) using Jenkins and Webhooks. Whenever code changes are pushed, Jenkins automatically triggers the build process and deploys the application onto an AWS EC2 instance. This approach eliminates manual intervention, reduces deployment errors, and ensures rapid and reliable software delivery.

---

## 📊 2. Architectural Diagram
Below is the architectural flow of the CI/CD pipeline running on AWS:

```text
[ Developer (Git Push) ] 
         │
         ▼
    [ GitHub Repository ]
         │
         ├──► (Webhook Trigger)
         ▼
  [ Jenkins Server ] (CI/CD Pipeline)
         │
         ▼
[ AWS EC2 Instance ] (Hosting Python App via Gunicorn on Port 5000)
         │
         ▼
[ End User Browser ] (Accessing deployed web page)
```

---

## 📥 3. Input / Setup Configuration
The input phase involves setting up the Python environment, configuring Jenkins, and running the application server command on the AWS EC2 instance.

### EC2 Terminal Command Input:
The following terminal input shows the execution of the Gunicorn server binding the application to port `5000` on the AWS EC2 instance (`ec2-user@ip-172-31-36-228`).

![EC2 Terminal Input](Screenshot_2026-10-10_182111.png)

---

## 🖥️ 4. Output / Execution
Once the Jenkins CI/CD pipeline triggers successfully via the webhook and the application starts running on the server, the web app becomes publicly accessible via the AWS EC2 public IP.

### Browser Output Screenshot:
The browser successfully renders the deployment message confirming that the Python application has been deployed via Jenkins with webhook integration.

![Browser Output](Screenshot_2026-10-10_181514.png)

---

## 📝 5. Conclusion
In this project, we successfully established a robust and automated CI/CD pipeline for a Python application using Jenkins and AWS EC2. By integrating webhooks, code updates are now pushed and deployed seamlessly without manual effort. This setup highlights the power of cloud infrastructure and automation tools in modern software development, ensuring high availability, scalability, and efficiency.