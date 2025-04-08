# Deployment strategies | Comparison & Recommendation

![Deployment Strategies](https://github.com/user-attachments/assets/ad64fb50-17dd-42de-bacb-e80003c83be1)

| Author        | Created On   | Version | Last Updated By | Internal Reviewer | Reviewer L0    | Reviewer L1    | Reviewer L2    |
|---------------|--------------|---------|------------------|--------------------|----------------|----------------|----------------|
| Mohit Kumar   | 08-Apr-2025  | v1.0    | Mohit Kumar      | Harshit Singh     | Akshit Kapil   | Shashi Sharma  | Mahesh Kumar   |

---

## Table of Contents

1. [Introduction](#introduction)
2. [What is Deployment Strategies](#what-is-deployment-strategies)
3. [Deployment Strategy Types](#deployment-strategy-types)
4. [Comparison Table](#comparison-table)
5. [Conclusion and Recommendation](#conclusion-and-recommendation)
6. [Contact Information](#contact-information)
7. [References](#references)

---

## Introduction

Deployment strategies are ways to update software in a live (production) environment. Choosing the right strategy helps avoid system downtime, reduces risk, and keeps users happy.

This document explains some common deployment methods and helps you pick the best one based on availability, risk, cost, and automation needs.

---

## What are Deployment Strategies?

Deployment strategies are plans for how to release new software to users. They affect how smoothly the service runs during updates, how much it costs, how risky the update is, and how easy it is to go back if something goes wrong.

They are an important part of modern software development and delivery.


## Deployment Strategy Types

| Deployment Strategy     | Description                                                                 | Pros                                              | Cons                                                    |
|-------------------------|-----------------------------------------------------------------------------|---------------------------------------------------|---------------------------------------------------------|
| Recreate Deployment     | Completely shuts down the current version before deploying the new one.     | Simple and easy to execute                        | Causes downtime; risky if the new version fails        |
| Rolling Deployment      | Gradually replaces old version pods or instances with the new ones.         | Minimizes downtime; easy rollback                 | Slower rollout; requires monitoring during the process  |
| Blue-Green Deployment   | Maintains two identical environments (blue & green). New version goes to green; traffic is shifted once verified. | Zero downtime; immediate rollback                 | High infrastructure cost; needs good orchestration     |
| Canary Deployment       | Deploys the new version to a small subset of users initially. Gradually increases exposure. | Risk is controlled; real user feedback possible   | Requires metrics and monitoring; complex routing        |
| A/B Testing Deployment  | Different versions are served to different user segments to analyze performance or behavior. | Effective for experimentation and product decisions | Complex setup; needs traffic control and analysis     |

---

## Comparison Table

| **Criteria**              | **Recreate** | **Rolling** | **Blue-Green** | **Canary** | **A/B Testing** |
|---------------------------|--------------|-------------|----------------|------------|-----------------|
| **Downtime**              | High         | Low         | Zero           | Low        | Low             |
| **Failure Risk**          | High         | Medium      | Low            | Low        | Medium          |
| **Release Speed**         | Fast         | Moderate    | Moderate       | Controlled | Controlled      |
| **User Experience**       | Interrupted  | Smooth      | Seamless       | Smooth     | Controlled      |
| **Rollback Simplicity**   | Difficult    | Moderate    | Easy           | Easy       | Moderate        |
| **Infrastructure Cost**   | Low          | Medium      | High           | Medium     | High            |
| **Setup Complexity**      | Low          | Moderate    | High           | High       | High            |
| **Monitoring Required**   | Minimal      | Required    | Required       | Essential  | Essential       |
| **Automation Need**       | Minimal      | Medium      | High           | High       | High            |
| **Ideal For**             | Small apps   | Most cases  | Large-scale    | Production testing | Experimentation |

---

## Conclusion and Recommendation

###  **Recommended Strategy: Rolling Deployment**

Based on the comparison and project requirements, **Rolling Deployment** is the most balanced strategy offering:

-  **Low downtime** with gradual deployment.
-  **Simple rollback** as changes are incremental.
-  **Resource efficiency**, unlike Blue-Green which doubles resources.
-  **Great user experience** with uninterrupted service.
-  **Moderate complexity**, easier to adopt and automate.

> #### **Rolling Deployment** is a good balance of **easy setup**, **low risk**, and **low cost** — perfect for teams with limited resources but need high system uptime.
>
> ⚠️ **Note:** Always pick a deployment strategy based on your **product goals**, **team experience**, **how much downtime users can handle**, and **your infrastructure**.
---

---

## Contact Information

| Name         | Email Address               |
|--------------|-----------------------------|
| Mohit Kumar  | mohit.kumar@mygurukulam.co  |

---

## References

| Resource Link                                                                 | Description                              |
|-------------------------------------------------------------------------------|------------------------------------------|
| [SlideTeam: Deployment Strategies](https://www.slideteam.net/deployment-strategies-comparisons-deployment-strategy-ppt-icon.html) | Strategy comparison slide                |
| [DevOpsSchool](https://www.devopsschool.com/blog/list-of-popular-deployment-strategies/)     | Summary of popular deployment strategies |
| [BuildPiper - Guide to Canary Deployments](https://medium.com/buildpiper/a-detailed-guide-to-canary-deployments-5321a03682e1) | Canary deep dive                         |
| [Vertisystem - Blue-Green vs Canary](https://vertisystem.medium.com/in-depth-analysis-blue-green-deployment-vs-canary-deployment-in-software-delivery-1eecb00cd00c) | Deployment pattern comparison            |


---

