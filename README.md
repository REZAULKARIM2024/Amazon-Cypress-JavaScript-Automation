# 🛒 Amazon E-Commerce Test Automation

![Cypress](https://img.shields.io/badge/Cypress-15.16.0-04C38E?style=for-the-badge&logo=cypress&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-ES6+-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![Cucumber](https://img.shields.io/badge/Cucumber-BDD-23D96C?style=for-the-badge&logo=cucumber&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-blue?style=for-the-badge)
![Tests](https://img.shields.io/badge/Tests-39%20Passing-brightgreen?style=for-the-badge)

End-to-end test automation suite for Amazon.com built with **Cypress**, **JavaScript**, and **Cucumber BDD**. Covers authentication, shopping workflows, checkout, account management, returns, Prime membership, and more.

---

## 📋 Table of Contents

- [Features](#-features)
- [Tech Stack](#-tech-stack)
- [Project Structure](#-project-structure)
- [Test Coverage](#-test-coverage)
- [Prerequisites](#-prerequisites)
- [Installation](#-installation)
- [Running Tests](#-running-tests)
- [Reports](#-reports)
- [Author](#-author)

---

## ✨ Features

- ✅ BDD-style tests written in plain English (Gherkin)
- ✅ 39 test cases across 3 feature files
- ✅ 100% pass rate
- ✅ HTML & JSON test reports (Mochawesome + Cucumber)
- ✅ Cross-browser support (Chrome, Firefox, Edge)
- ✅ Headless CI/CD ready
- ✅ Reusable custom Cypress commands
- ✅ Fixture-based test data management

---

## 🛠 Tech Stack

| Tool | Version | Purpose |
|------|---------|---------|
| [Cypress](https://www.cypress.io/) | 15.16.0 | Test framework |
| [JavaScript](https://developer.mozilla.org/en-US/docs/Web/JavaScript) | ES6+ | Language |
| [@badeball/cypress-cucumber-preprocessor](https://github.com/badeball/cypress-cucumber-preprocessor) | 24.0.1 | BDD / Gherkin support |
| [Mochawesome](https://github.com/adamgruber/mochawesome) | 7.1.3 | HTML test reports |
| [multiple-cucumber-html-reporter](https://github.com/WasiqB/multiple-cucumber-html-reporter) | 3.10.0 | Cucumber HTML reports |
| [esbuild](https://esbuild.github.io/) | 0.21.5 | Fast bundler |
| [ESLint](https://eslint.org/) | 8.57.1 | Code linting |
| [Prettier](https://prettier.io/) | 3.2.0 | Code formatting |

---

## 📁 Project Structure

```
AmazonCypressJavaScriptAutomation/
│
├── cypress/
│   ├── features/                          # BDD Feature files (Gherkin)
│   │   ├── 01-authentication.feature      # Login, Register, Logout
│   │   ├── 02-shopping.feature            # Search, Cart, Checkout
│   │   └── 03-account-management.feature  # Returns, Prime, History
│   │
│   ├── support/
│   │   ├── e2e.js                         # Global hooks & custom commands
│   │   └── step_definitions/
│   │       ├── auth.js                    # Authentication steps
│   │       ├── shopping.js                # Shopping & cart steps
│   │       └── checkout-account.js        # Checkout & account steps
│   │
│   ├── fixtures/
│   │   ├── testData.json                  # Test users, credentials
│   │   └── selectors.json                 # CSS selectors
│   │
│   ├── results/                           # Generated test reports
│   ├── screenshots/                       # Failure screenshots
│   └── videos/                            # Test recordings
│
├── cypress.config.js                      # Cypress configuration
├── package.json                           # Dependencies & scripts
├── .env                                   # Environment variables
└── .env.example                           # Environment template
```

---

## 🧪 Test Coverage

### Feature 1 — User Authentication (`01-authentication.feature`)
| TC | Test Case | Status |
|----|-----------|--------|
| TC-001 | New user registration with valid data | ✅ Pass |
| TC-001 | Registration with invalid email format | ✅ Pass |
| TC-001 | Registration with weak password | ✅ Pass |
| TC-002 | Login with valid credentials | ✅ Pass |
| TC-002 | Login with incorrect password | ✅ Pass |
| TC-002 | Login with non-existent email | ✅ Pass |
| TC-003 | Logout from account | ✅ Pass |
| TC-003 | Session expires after logout | ✅ Pass |
| TC-002 | Remember me functionality | ✅ Pass |
| TC-002 | Two-factor authentication setup | ✅ Pass |

### Feature 2 — Shopping Workflows (`02-shopping.feature`)
| TC | Test Case | Status |
|----|-----------|--------|
| TC-004 | Search product by keyword | ✅ Pass |
| TC-004 | Search with filters | ✅ Pass |
| TC-004 | Sort search results | ✅ Pass |
| TC-005 | Add single product to cart | ✅ Pass |
| TC-005 | Add multiple items to cart | ✅ Pass |
| TC-005 | Add out-of-stock product to cart | ✅ Pass |
| TC-006 | Remove product from cart | ✅ Pass |
| TC-006 | Update cart quantity | ✅ Pass |
| TC-006 | Clear entire cart | ✅ Pass |
| TC-007 | Complete checkout process | ✅ Pass |
| TC-007 | Checkout with new address | ✅ Pass |
| TC-007 | Apply coupon code at checkout | ✅ Pass |
| TC-007 | Checkout with different payment methods | ✅ Pass |

### Feature 3 — Account Management (`03-account-management.feature`)
| TC | Test Case | Status |
|----|-----------|--------|
| TC-008 | Initiate product return | ✅ Pass |
| TC-008 | Track return status | ✅ Pass |
| TC-009 | Join Prime membership | ✅ Pass |
| TC-009 | Prime membership features | ✅ Pass |
| TC-009 | Cancel Prime membership | ✅ Pass |
| TC-010 | View browsing history | ✅ Pass |
| TC-010 | Filter browsing history by date | ✅ Pass |
| TC-011 | View purchase history | ✅ Pass |
| TC-011 | Filter orders by date range | ✅ Pass |
| TC-011 | Download invoice | ✅ Pass |
| TC-012 | View Amazon Visa card benefits | ✅ Pass |
| TC-012 | Apply for Amazon Visa card | ✅ Pass |
| TC-012 | Manage Amazon card account | ✅ Pass |
| TC-013 | Enroll in Amazon Associates program | ✅ Pass |
| TC-013 | Generate affiliate links | ✅ Pass |
| TC-013 | Track affiliate earnings | ✅ Pass |

**Total: 39 tests — 39 ✅ Pass — 0 ❌ Fail**

---

## 📦 Prerequisites

- [Node.js](https://nodejs.org/) v18.0.0 or higher
- [npm](https://www.npmjs.com/) v8.0.0 or higher
- Google Chrome (recommended)

---

## 🚀 Installation

**1. Clone the repository**
```bash
git clone https://github.com/REZAULKARIM2024/Amazon-Cypress-JavaScript-Automation.git
cd Amazon-Cypress-JavaScript-Automation
```

**2. Install dependencies**
```bash
npm install
```

**3. Install Cypress binary**
```bash
npx cypress install
```

**4. Set up environment variables**
```bash
cp .env.example .env
```
Edit `.env` and set:
```
AMAZON_URL=https://www.amazon.com
```

---

## ▶️ Running Tests

### Open Cypress UI (interactive)
```bash
npm run open
```

### Run all tests (headless)
```bash
npm test
```

### Run specific feature
```bash
npm run test:auth        # Authentication tests
npm run test:shopping    # Shopping tests
npm run test:account     # Account management tests
```

### Run in specific browser
```bash
npm run test:chrome
npm run test:firefox
npm run test:edge
```

### Run with report generation
```bash
npm run test:report
```

---

## 📊 Reports

After running `npm run test:report`, reports are generated in `cypress/results/`:

| Report | File | Description |
|--------|------|-------------|
| Mochawesome HTML | `cypress/results/report.html` | Visual HTML report with charts |
| Mochawesome JSON | `cypress/results/report.json` | Raw JSON data |
| Cucumber HTML | `cypress/results/cucumber-report.html` | BDD-style report |
| Cucumber JSON | `cypress/results/cucumber-json/cucumber-report.json` | Cucumber JSON data |

Open the HTML report in your browser:
```bash
start cypress/results/report.html        # Windows
open cypress/results/report.html         # Mac/Linux
```

---

## 👤 Author

**Rezaul Karim**  
Software Developer & QA Automation Engineer  
GitHub: [@REZAULKARIM2024](https://github.com/REZAULKARIM2024)

---

## 📄 License

This project is licensed under the [MIT License](LICENSE).

---
