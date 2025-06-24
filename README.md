# JavaScript Practice – Conditionals & Strings

This project includes four beginner-friendly JavaScript tasks focusing on conditional logic, string manipulation, and switch-case statements. Each task demonstrates how to build simple utility functions and output meaningful messages.

---

## 📁 Project Structure


All JavaScript code is included inline or linked in a single HTML file.

---

## 🚀 How to Run

1. Clone or download the repository.  
2. Open `index.html` in your browser.  
3. Open the browser **Console** (F12 or right-click → Inspect → Console tab) to view function outputs.

---

## 📌 Tasks Overview

### ✅ Task 1 — `makeTransaction(quantity, pricePerDroid, customerCredits)`

Calculates the total price for a purchase and checks if the customer has enough credits. Returns either a confirmation message or an "Insufficient funds" warning.

```js
function makeTransaction(quantity, pricePerDroid, customerCredits) {
  const totalPrice = quantity * pricePerDroid;
  return totalPrice > customerCredits
    ? "Insufficient funds!"
    : `You ordered ${quantity} droids worth ${totalPrice} credits!`;
}
makeTransaction(5, 3000, 23000); // "You ordered 5 droids worth 15000 credits!"
makeTransaction(10, 5000, 8000); // "Insufficient funds!"

✅ Task 2 — formatMessage(message, maxLength)
Truncates a message if it exceeds the given maximum length and adds "..." to the end.

js
Копировать
Редактировать
function formatMessage(message, maxLength) {
  return message.length <= maxLength
    ? message
    : message.slice(0, maxLength) + "...";
}
Examples:

js
Копировать
Редактировать
formatMessage("Curabitur ligula sapien", 16); // "Curabitur ligula..."
formatMessage("Vestibulum facilisis purus nec", 30); // "Vestibulum facilisis purus nec"

✅ Task 3 — checkForSpam(message)
Checks if a message contains spam keywords like "spam" or "sale" (case-insensitive). Returns true if spam is detected.

js
Копировать
Редактировать
function checkForSpam(message) {
  const lower = message.toLowerCase();
  return lower.includes("spam") || lower.includes("sale");
}
Examples:

js
Копировать
Редактировать
checkForSpam("Get best sale offers now!"); // true
checkForSpam("JavaScript weekly newsletter"); // false


✅ Task 4 — getShippingCost(country)
Returns the shipping cost to a given country using a switch statement. If the country is not supported, returns a rejection message.

js
Копировать
Редактировать
function getShippingCost(country) {
  let price;
  switch (country) {
    case "China": price = 100; break;
    case "Chile": price = 250; break;
    case "Australia": price = 170; break;
    case "Jamaica": price = 120; break;
    default:
      return "Sorry, there is no delivery to your country";
  }
  return `Shipping to ${country} will cost ${price} credits`;
}
Examples:

js
Копировать
Редактировать
getShippingCost("Australia"); // "Shipping to Australia will cost 170 credits"
getShippingCost("Germany");   // "Sorry, there is no delivery to your country"
🧠 What You'll Practice
Conditional statements (if, else, ternary)

String methods (slice(), toLowerCase(), includes())

Switch-case branching

Writing reusable and testable utility functions
