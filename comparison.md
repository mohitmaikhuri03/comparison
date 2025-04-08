# Deployment Strategies Comparison

![image](https://github.com/user-attachments/assets/ad64fb50-17dd-42de-bacb-e80003c83be1)



| Author        | Created On   | Version | Last Updated By | Internal Reviewer | Reviewer L0    | Reviewer L1    | Reviewer L2    |
|---------------|--------------|---------|------------------|--------------------|----------------|----------------|----------------|
| Mohit Kumar   | 08-Apr-2025  | v1.0    | Mohit Kumar      |Harshit Singh| Akshit Kapil   | Shashi Sharma  | Mahesh Kumar   |

---

## Table of Contents

1. [Introduction](#introduction)
2. [What is Deployment Strategies](#what-is-deployment-strategies)
3. [Deployment Strategy Types](#deployment-strategy-types)
4. [ Comparison Table ](#comparison-table)
5. [Conclusion and Recommendation](#conclusion-and-recommendation)
6. [Contact Information](#contact-information)
7. [References](#references)

---

## Introduction

This document provides a comprehensive understanding of the various deployment strategies used in software development and DevOps pipelines. The primary objective is to help teams choose the most suitable strategy that balances availability, performance, risk, and cost.

---

## What is Deployment Strategies

Deployment strategies refer to the approach used to release a new version of an application or service into a production environment. These strategies play a critical role in minimizing downtime, ensuring system reliability, and improving the user experience.

---

## Deployment Strategy Types

**1. Recreate Deployment**  
- Stops the current running version completely before deploying the new version. It is straightforward but causes downtime.

**2. Rolling Deployment**  
- Gradually replaces instances of the old version with new ones, ensuring that at least part of the system remains available during the process.

**3. Blue-Green Deployment**  
- Two identical environments (blue and green) exist. The new version is deployed to the green environment, and once verified, traffic is switched from blue to green.

**4. Canary Deployment**  
- The new version is initially released to a small subset of users. Based on the results, the rollout continues gradually.

**5. A/B Testing Deployment**  
- Multiple versions are deployed simultaneously to different user groups to measure performance, engagement, or other metrics.

---

## Comparison Table

| Criteria                  | Recreate     | Rolling      | Blue-Green    | Canary        | A/B Testing   |
|---------------------------|--------------|--------------|----------------|---------------|----------------|
| Downtime                  | High         | Low          | Zero           | Low           | Low            |
| Failure Risk              | High         | Medium       | Low            | Low           | Medium         |
| Speed/Frequency           | Low          | High         | Moderate       | High          | Moderate       |
| User Experience Impact    | High         | Minimal      | Minimal        | Minimal       | Controlled      |
| Resource Usage            | Low          | Medium       | High           | Medium        | High           |
| Complexity                | Low          | Moderate     | Low            | High          | High           |
| Skill Level Required      | Basic        | Moderate     | Advanced       | Advanced      | Advanced       |
| Cost                      | Low          | Medium       | High           | Medium        | High           |
| Automation Needs          | Minimal      | Moderate     | Extensive      | Extensive     | Extensive      |

---

## Conclusion and Recommendation

**Recommended Strategy: Rolling Deployment**

Rolling Deployment is the most suitable strategy for this project because:

- It offers minimal downtime and low risk during deployment.
- Rollbacks are simpler since only a portion of the environment is updated at a time.
- It is resource-efficient as it doesn't require duplicate environments.
- The user experience is not significantly affected during deployment.
- It provides a balance between complexity, risk, and automation.

This strategy is ideal for teams that want safe and continuous delivery without overcomplicating infrastructure or increasing costs.

---

## Contact Information

| Name         | Email Address                  |
|--------------|--------------------------------|
| Mohit Kumar  | mohit.kumar@mygurukulam.co     |

---

## References

| Resource Link                                                                 | Description                              |
|-------------------------------------------------------------------------------|------------------------------------------|
| https://www.slideteam.net/deployment-strategies-comparisons-deployment-strategy-ppt-icon.html | Strategy comparison slide                |
| https://www.devopsschool.com/blog/list-of-popular-deployment-strategies/     | Summary of popular deployment strategies |
| https://medium.com/buildpiper/a-detailed-guide-to-canary-deployments-5321a03682e1 | Guide to Canary Deployments              |
| https://vertisystem.medium.com/in-depth-analysis-blue-green-deployment-vs-canary-deployment-in-software-delivery-1eecb00cd00c | Blue-Green vs Canary analysis            |
| https://ibrahimhkoyuncu.medium.com/mastering-progressive-delivery-implementing-canary-releases-a-b-testing-and-custom-metrics-with-373a21918c9e | Progressive delivery and A/B testing     |

---

Note: Choose your deployment strategy based on business needs, infrastructure capability, and team maturity.
