# 🏦 Loan Qualification Checker

This JavaScript project checks if a user qualifies for different types of loans based on their **annual income** and **credit score**.

## 📌 Loan Types & Requirements

| Loan Type | Minimum Income | Minimum Credit Score |
|-----------|----------------|----------------------|
| Duplex    | $60,000        | 700                  |
| Condo     | $45,000        | 680                  |
| Car       | $30,000        | 650                  |

## 🧠 How It Works

The function `getLoanMessage(annualIncome, creditScore)` takes two inputs:

- `annualIncome`: User's yearly income
- `creditScore`: User's credit score

It returns a message based on what the user qualifies for:

- ✅ Duplex, Condo, and Car loan (if qualified for all)
- ✅ Condo and Car loan
- ✅ Car loan only
- ❌ No loan (if qualifications not met)

## 🧪 Example Usage

```js
const duplexLoanMsg = getLoanMessage(85000, 850);
console.log(duplexLoanMsg); 
// Output: "You qualify for a duplex, condo, and car loan."

const condoLoanMsg = getLoanMessage(65000, 690);
console.log(condoLoanMsg); 
// Output: "You qualify for a condo and car loan."

const carLoanMsg = getLoanMessage(45000, 660);
console.log(carLoanMsg); 
// Output: "You qualify for a car loan."

const noLoanMsg = getLoanMessage(25000, 550);
console.log(noLoanMsg); 
// Output: "You don't qualify for any loans."

📂 File Structure
bash
Copy
Edit
loan-qualification-checker/
│
├── index.js        # Contains the loan logic and test cases
└── README.md       # Project documentation