<<<<<<< HEAD
# DemoBlaze E-Commerce: Full QA Automation & CI/CD Pipeline

![Playwright](https://img.shields.io/badge/Test%20Framework-Playwright-2E8555?style=for-the-badge&logo=playwright)
![Cucumber](https://img.shields.io/badge/BDD-Cucumber-36AD7F?style=for-the-badge&logo=cucumber)
![Jenkins](https://img.shields.io/badge/CI/CD-Jenkins-D24939?style=for-the-badge&logo=jenkins)
![Docker](https://img.shields.io/badge/Container-Docker-2496ED?style=for-the-badge&logo=docker)

This repository holds a comprehensive, end-to-end QA testing project for the [DemoBlaze e-commerce website](https://www.demoblaze.com/index.html).

It is designed to showcase the complete QA lifecycle, from initial planning and manual test case design to a fully automated, "no-hands" CI/CD pipeline.

## 1. Project Objective

This project simulates a real-world QA process. The goal is to build a robust and reliable testing suite that:

* **Maps Critical Flows:** Identifies and documents key user journeys (User auth, Add to Cart, Purchase).
* **Embraces BDD:** Uses Gherkin (Cucumber.js) to create test scenarios that are readable by both technical and non-technical stakeholders.
* **Automates UI & API:** Implements automation for both the UI (Playwright) and the underlying APIs (Playwright `request`).
* **Integrates Continuously:** Uses a Jenkins pipeline, containerized via Docker, to run all tests automatically.
* **Provides Feedback:** Is configured for daily regression runs (every 24h) and sends test execution reports via email.

## 2. Test Documentation & Planning

Before automation, a "Docs as Code" approach was used to map critical flows and define manual test cases.

<!-- * [**`docs/Exploratory_Testing_Findings.md`**](./docs/Exploratory_Testing_Findings.md) (Link to the future exploratory doc)
* [**`docs/TC_01_User_Authentication.md`**](./docs/TC_01_User_Authentication.md) (Link to the future Login test cases)
* [**`docs/TC_02_Product_Flow.md`**](./docs/TC_02_Product_Flow.md) (Link to the future Add to cart test cases)
* [**`docs/TC_03_Checkout_Process.md`**](./docs/TC_03_Checkout_Process.md) (Link to the future Purchase test cases) -->

## 3. Technology Stack

| Area | Tool / Technology | Purpose |
| :--- | :--- | :--- |
| **Automation** | **Playwright** | E2E test execution and API testing (`request`). |
| **BDD** | **Cucumber.js** | Gherkin syntax parsing and step definition execution. |
| **Language** | **Javascript** | For scripting automation logic and step definitions. |
| **CI/CD** | **Jenkins** | Orchestrating the entire build, test, and report pipeline. |
| **Containerization** | **Docker** | To run a clean, isolated Jenkins instance and its build agents. |
| **Reporting** | **Cucumber-HTML-Reporter** | Generating user-friendly HTML reports from test runs. |
| **Notifications** | **Jenkins Email Ext** | Sending reports to stakeholders after scheduled runs. |

## 4. Tested Scenarios (BDD)

This suite covers the following Gherkin-defined user flows:

<!-- * **Authentication**
    * `Scenario: User can sign up successfully`
    * `Scenario: User can log in with valid credentials`
    * `Scenario: User cannot log in with an invalid password`
* **Product & Cart**
    * `Scenario: User can browse product categories`
    * `Scenario: User can add a product to the cart`
    * `Scenario: User can view the cart and delete items`
* **Checkout**
    * `Scenario: User can successfully complete a purchase` -->


## 5. CI/CD Pipeline (Jenkins + Docker)

The entire process is automated via the `Jenkinsfile` in this repository.

![CI/CD Pipeline Diagram](link da img) 

The pipeline executes the following stages:

1.  **Checkout SCM:** Clones the latest code from this GitHub repository.
2.  **Install Dependencies:** Runs `npm install` inside a Node.js container to get all dependencies.
3.  **Install Browsers:** Runs `npx playwright install`.
4.  **Run Automation Suite:** Executes all Cucumber.js (`.feature`) tests.
5.  **Generate & Archive Report:** Collects test artifacts and generates the final HTML report.
6.  **Send Notification:** (If triggered by the 24h timer) sends the report to a specified email list.

## 6. How to Run This Project Locally

### Prerequisites

* [Node.js](https://nodejs.org/en/) (v18+)
* [Git](https://git-scm.com/)

### 1. Clone the Repository
<!-- ```bash
git clone [https://github.com/SEU-USUARIO/SEU-REPOSITORIO.git](https://github.com/SEU-USUARIO/SEU-REPOSITORIO.git)
cd SEU-REPOSITORIO -->
=======
# Product Store - Testing Process
Test automation and exploratory testing project for [Product Store](https://www.demoblaze.com), a demo e-commerce website designed for practicing QA and automation testing.
>>>>>>> 3c2be653492bc843a52cd5cea97657bf72c7d5f3
