
# Deploying Helm Charts using GitHub Pages  

## References

[Video](https://youtu.be/x4IF7yyWw9g)

## 📌 Overview  
This repository demonstrates how to **publish a Helm Chart on GitHub Pages** and turn it into a **self-hosted Helm Chart repository** using **GitHub Actions**. This allows you to store, manage, and deploy Helm Charts easily across multiple Kubernetes projects.  

## 🎯 What You'll Learn  
✅ How to create and customize a **Helm Chart**  
✅ How to **automate Helm Chart publishing** with **GitHub Actions**  
✅ How to **use the published Helm Chart** in Kubernetes deployments  



---

## 🚀 Publishing the Helm Chart  

This repository is configured to automatically **publish Helm Charts to GitHub Pages** using GitHub Actions.

### **Prerequisites**  
Before publishing, ensure:  
✅ Your **GitHub repository** has a `charts/` directory containing Helm Charts  
✅ You have a **GitHub Pages branch (`gh-pages`)** to store the published charts  
✅ Your repository settings allow GitHub Pages from the `gh-pages` branch  

### 🔄 **Publishing Steps**  
GitHub Actions will trigger automatically when:  
1. A **push is made to the `main` branch**  
2. A **manual workflow dispatch is triggered**  

To manually trigger the workflow:  
1. Go to **GitHub → Actions**  
2. Select **Publish Helm Chart Workflow**  
3. Click **Run Workflow**  

do
Once the workflow completes, your Helm Chart will be available via **GitHub Pages**.

---

## 📥 Using the Published Helm Chart  

### **Step 1: Add the Helm Repository**
To use the published Helm Chart in your Kubernetes projects, add the Helm repository:

```bash
helm repo add myrepo https://<your-github-username>.github.io/<your-repo-name>/
helm repo update
```





