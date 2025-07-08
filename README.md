# 🛠️ Jenkins Declarative Pipeline Project

This repository demonstrates a **Jenkins Declarative Pipeline** setup, using a multi-stage flow to simulate a typical software development lifecycle.

---

## 📁 Repository Structure

This repo contains several `.bat` files representing various CI/CD stages:

```
.
├── build.bat    # Simulates build process
├── deploy.bat   # Simulates deployment step
├── package.bat  # Simulates packaging
├── test.bat     # Simulates testing step
└── Jenkinsfile  # Defines the CI/CD pipeline
```

Each `.bat` file contains a simple `echo` command to verify pipeline execution.

---

## 🚀 Pipeline Overview

The Jenkinsfile includes the following stages:

- **Checkout** – Clones this GitHub repository
- **Build** – Executes `build.bat`
- **Test** – Executes `test.bat`
- **Package** – Executes `package.bat`
- **Deploy** – Executes `deploy.bat`

At the end of the pipeline, a post block runs regardless of outcome and provides messages for success, failure, or changes.

---

## 🔧 How to Run This Pipeline in Jenkins

1. **Create a new Pipeline project item** in Jenkins

    ![image](https://github.com/user-attachments/assets/268be7f4-2ccc-4b69-8650-9f1f1f4bbe81)

3. In the configuration, choose:

    - **Pipeline Script** or use **Pipeline script from SCM**
    - For SCM: Git
    - **Repository URL**: `https://github.com/deep0304/pipeline_test.git`
    - **Branch**: `main`
    - (Note: JenkinsFile has Pipeline Script inside)
      
![Screenshot 2025-07-09 002657](https://github.com/user-attachments/assets/e850e944-1b56-4976-bb72-ce46311a5cd0)

3. Save the configuration

---

## ▶️ Run and View Output

- Click **Build Now**
- The pipeline will clone the repo and run each stage
- Each stage simply executes an echo command in this example
- You can view detailed stage-by-stage output in the **Console Output**
- The **Pipeline Stage View** will also show visual progress of stages

   Console Output:

    ![Screenshot 2025-07-09 002807](https://github.com/user-attachments/assets/3b05a8d1-23ae-4385-bdc5-b7c65dd604ea)

  Pipeline Overview

  ![image](https://github.com/user-attachments/assets/f7ff3ea5-9734-4a2f-a03a-e9f0fec78431)


---

## ✅ Final Result

- Jenkins will evaluate if the pipeline succeeded or failed
- Based on the structure and execution result, the final build will be marked **Passed** or **Failed**
- You will see a check or cross icon indicating success or failure

This setup can be expanded later with real build/test/deploy logic or Docker integration.

![image](https://github.com/user-attachments/assets/e07e0eb1-f011-4d95-b59a-24ce34299ff5)

---

## 📌 Notes

- This is a Windows-based Jenkins setup (uses `bat` commands)
- You can convert to `sh` for Linux-based agents

---

📂 **GitHub Repo**: [https://github.com/deep0304/pipeline_test](https://github.com/deep0304/pipeline_test)
