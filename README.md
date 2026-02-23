# DevSecOps Pipeline: Zomato Clone Deployment 🚀🛡️

![DevSecOps](https://miro.medium.com/v2/resize:fit:1400/format:webp/1*X_hm5iF0NRjbOZHB6RQIFA.jpeg)

This project demonstrates a high-level **DevSecOps Pipeline** implementation. It focuses on integrating security at every stage of the CI/CD lifecycle, ensuring that the application is not only built and deployed automatically but also scanned for vulnerabilities.

---

## 📋 Project Overview
The goal of this project is to implement a "Shift Left" security approach by integrating scanning tools directly into the Jenkins pipeline:
1. **Source Control:** GitHub (Zomato Clone Code).
2. **Static Analysis:** SonarQube for Code Quality & SAST.
3. **Dependency Scanning:** OWASP Dependency Check for vulnerable libraries.
4. **Vulnerability Scanning:** Trivy for File System and Docker Image security.
5. **Deployment:** Automated containerized deployment on AWS.

---

## 🛠️ Tech Stack & Tools
| Category | Technology |
| :--- | :--- |
| **Cloud Provider** | AWS (EC2 T2-Large, Security Groups) |
| **Automation Server** | Jenkins (Declarative Pipeline) |
| **Code Quality / SAST** | SonarQube |
| **Security (SCA)** | OWASP Dependency Check |
| **Security (Scanning)** | Trivy |
| **Containerization** | Docker |
| **Build Tool** | Node.js (NPM) |

---

## 🏗️ System Architecture & Pipeline Stages
The pipeline is structured into 10 automated stages:
* **Clean & Checkout:** Prepares the environment and pulls the latest source code.
* **SonarQube Analysis:** Scans code for bugs and security "smells" with a Quality Gate.
* **Security Scanning (SCA):** OWASP checks for vulnerabilities in the Node.js dependencies.
* **Trivy FS Scan:** Scans the repository files for sensitive data or vulnerabilities.
* **Docker Automation:** Builds the image, tags it, and pushes it to Docker Hub.
* **Image Security:** Trivy scans the final Docker image before deployment.
* **Deployment:** Automatically runs the container on port `3000`.

---

## 🚀 Key Features Implemented
* **Declarative Pipeline:** Used Jenkinsfile for "Pipeline as Code" best practices.
* **Security Integration:** Multi-layer security (SAST, SCA, and Image Scanning).
* **Quality Gates:** Configured Jenkins to fail the build if SonarQube quality standards are not met.
* **Automated Cleanup:** Optimized AWS resources by ensuring clean workspaces.

---

## 📝 Quick Execution Guide
1. **AWS Setup:** Launch an Ubuntu 22.04 instance (T2-Large for RAM requirements).
2. **Installation:** Install Jenkins, Docker, and Trivy using the provided scripts.
3. **SonarQube:** Deploy SonarQube using Docker:
   ```bash
   docker run -d --name sonar -p 9000:9000 sonarqube:lts-community

---
## 🏁 Conclusion
* This project proves that security doesn't have to be a manual bottleneck. By using Jenkins, Docker, and scanning tools like Trivy, we can achieve a secure, automated, and reliable deployment lifecycle.

---

## 🛠️ Author & Community   
I’d love to hear your feedback! Feel free to share your thoughts.  

📧 **Connect with me:**

- **GitHub**: [M0hamedAmgad](https://github.com/NotHarshhaa)    
- **LinkedIn**: [Mohamed Amgad Elgamal](https://www.linkedin.com/in/mohamed-amgad-elgamal)  

---