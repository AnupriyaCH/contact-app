# 🟢 Q1 – Promo Code Generator

### 📖 Problem
Our national retail client has a 200-store branch network.  
They want to run a promotion where customers enter their **email + unique code** into our website.  

Requirements:
- Each store issues up to 10,000 customer codes/day  
- The promo code must:
  - Be **≤ 9 characters**
  - Encode:
    - Store ID
    - Date
    - Transaction number (1..10,000 per day)
  - Be human-friendly (easy to type, hard to cheat)  

---

### 💻 Implementation
We use **Base36 encoding** to keep codes short.  

- **Generate Code**: `(storeId + date + transactionId) → promoCode`  
- **Decode Code**: `promoCode → storeId, date, transactionId`  

---

### 📂 Files
- `promo-code/index.html` → simple UI to test  
- `promo-code/script.js` → generator + decoder  

---

### ▶️ Run Instructions
1. Open the `promo-code/` folder in VS Code  
2. Open `index.html` in your browser (no server needed)  
3. Enter:
   - Store ID  
   - Date (YYYYMMDD)  
   - Transaction Number  
4. Click **Generate** → you get a promo code  
5. Paste a promo code and click **Decode** → details are revealed  

---
