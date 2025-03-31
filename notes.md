Q1. Why i used max-width:470px and width:90% in class card?

🍕 Imagine a pizza box (your card)
width: 90% means "Make the box 90% of the table size" (the screen width).

max-width: 470px means "But don’t let it get bigger than 470px, even if the table is huge."

🔍 Why use both?
On big screens, max-width: 470px stops the box from becoming too large.

On small screens, width: 90% lets the box shrink so it fits nicely.

🚀 What happens if you remove one?
Remove width: 90% → On small screens, the box might stay too big and cause scrolling.

Remove max-width: 470px → On big screens, the box might stretch too wide and look bad.

✅ Best Practice
Using both together makes the design responsive—it looks good on all screen sizes! 🎯

---

Q2. Why we used response.json and not json.parse(response) to get the data ?
Great question! The key difference between `JSON.parse(response)` and `response.json()` is **how they handle data**. Let me explain it simply.

---

### **1️⃣ `response.json()` (✅ Correct Way)**

- `fetch()` returns a **Response object**.
- `.json()` is a **built-in method** of the Response object that **reads the response body** and **parses** it as JSON.

🔹 **Example (Correct Way)**

```js
async function checkWeather() {
  const response = await fetch(apiUrl + `&appid=${apiKey}`);
  const data = await response.json(); // ✅ Converts response body to JSON
  console.log(data);
}
```

**Why it works?**

- `response.json()` **reads the response body**.
- It **automatically converts** the JSON **text** into a JavaScript object.

---

### **2️⃣ `JSON.parse(response)` (❌ Wrong Way)**

- `JSON.parse()` expects a **string**, but `response` is a **Response object**.
- Since `response` is **not a string**, `JSON.parse(response)` **throws an error**.

🔹 **Example (Wrong Way)**

```js
var data = JSON.parse(response); // ❌ response is an object, not a string!
```

**Why it fails?**

- `JSON.parse()` **does NOT know how to handle a Response object**.
- It expects something like this:
  ```js
  var jsonString = '{"temp": 30, "city": "Bangalore"}';
  var data = JSON.parse(jsonString); // ✅ Works fine
  ```

---

### **🔑 Key Difference**

| Method            | What It Works On | What It Does                  |
| ----------------- | ---------------- | ----------------------------- |
| `response.json()` | Response object  | Reads body & converts to JSON |
| `JSON.parse()`    | JSON string      | Converts string to object     |

---

### **🚀 Best Practice**

**Always use `response.json()` when handling API responses.**  
If you already have a **JSON string**, then use `JSON.parse()`.

Let me know if you need more clarification! 😊
