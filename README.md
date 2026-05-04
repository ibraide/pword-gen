# 🔐 Random Password Generator

A simple yet powerful **Random Password Generator** built with **vanilla JavaScript**, HTML, and CSS.
It generates strong, unique passwords instantly — and lets you copy them to your clipboard with a single click.
The app also includes a **light/dark theme toggle** for a more personalized experience.

---

## 🌟 Features

✅ **Generates two secure passwords** at once, each 15 characters long.
✅ **Includes uppercase, lowercase, numbers, and symbols** for stronger passwords.
✅ **Instant copy-to-clipboard** functionality — just click a password to copy it.
✅ **Light/Dark mode toggle** to switch between themes.
✅ Clean, responsive, and intuitive UI.

---

## 🧠 How It Works

1. **Character Pool:**
   The app stores all possible characters (A-Z, a-z, 0-9, symbols) in an array.

2. **Password Generation:**
   When you click **“Generate Passwords”**, the app randomly selects 15 characters from the array and builds two separate passwords.

   ```javascript
   function generateRandomPassword() {
     let passwordOne = "";
     let passwordTwo = "";
     for (let i = 0; i < passwordLength; i++) {
       passwordOne += getRandomCharacter();
       passwordTwo += getRandomCharacter();
     }
     txtOne.textContent = passwordOne;
     txtTwo.textContent = passwordTwo;
   }
   ```

3. **Copy to Clipboard:**
   Clicking on a generated password copies it to your clipboard using the `navigator.clipboard` API:

   ```javascript
   navigator.clipboard.writeText(text)
     .then(() => alert("Password copied to clipboard!"));
   ```

4. **Theme Toggle:**
   The light/dark theme is handled using `classList.toggle()` on the body element:

   ```javascript
   lightBtn.addEventListener("click", function() {
     document.body.classList.toggle("colored");
     lightBtn.textContent = document.body.classList.contains("colored")
       ? "Change to dark theme"
       : "Change to light theme";
   });
   ```

---

## 🛠️ Technologies Used

* **HTML5** — for structure
* **CSS3** — for styling and themes
* **JavaScript (ES6)** — for logic, DOM manipulation, and clipboard functionality

---

## 🚀 Getting Started

### 1️⃣ Clone the repository

```bash
git clone https://github.com/yourusername/random-password-generator.git
cd random-password-generator
```

### 2️⃣ Open the project

Open `index.html` directly in your web browser — no build tools required.

### 3️⃣ Generate passwords

Click the **“Generate Passwords”** button and copy your favorite password with a single click!

---

## 💡 Future Improvements

* Add **password length selector** (user-defined length).
* Include **checkbox filters** for uppercase, numbers, or special characters.
* Add **strength indicator** for generated passwords.
* Store recent passwords locally for reuse.

---

## 📸 Preview

> *(Optional — add a screenshot or GIF of your app here)*

---

## 👩‍💻 Author

**Ibi-ilate Braide**
📧 ibi-ilatebraide@outlook.com
🌐 https://github.com/ibraide

