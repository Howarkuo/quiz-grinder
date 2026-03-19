# 🚀 Quiz Grinder

A lightweight, serverless web application for practicing multiple-choice questions. This tool runs entirely in your browser using **Vue.js** and **LocalStorage** to track your progress without the need for a backend.
![web view](web.png)

## 🛠 Credits
This application uses the **Quiz Grinder** engine developed by **Jeffrey Sun (Darkthread)**. 

* **Original Source:** [darkthread.github.io](https://github.com/darkthread/darkthread.github.io/tree/master/quiz-grinder)
* **Usage Instructions (Original):** [Darkthread Blog](https://blog.darkthread.net/blog/quiz-grinder/)

*Note: The UI and content have been translated into English for this specific implementation.*

---

## 🛠 Features

* **Progress Persistence:** Your current question index and "Incorrect Questions" list are saved automatically in your browser's `localStorage`.
* **Incorrect List:** Any question you get wrong is added to a dynamic list at the bottom for quick retries.



## 🚀 How to Run

You do not need a local server or complex environment setup. You can open it directly from your file system.

1.  **Clone or Download** this repository to your computer.
2.  **Ensure** your folder structure looks like this:
    ```plaintext
    quiz-grinder/
    ├── README.md
    ├── quiz-grinder.html      (The main application)
    └── organometalic.js       (The quiz data file)
    ```
3.  **Open the Quiz:**
    Copy the path below, replace `[PATH_TO_FOLDER]` with the actual location on your disk, and paste it into your browser's address bar:
    `file:///[PATH_TO_FOLDER]/quiz-grinder/quiz-grinder.html?organometalic`

## ⚙️ Technical Details

* **Framework:** Vue.js 3 (loaded via CDN).
* **Styling:** Vanilla CSS.
* **Data Format:** The quiz dynamically reads from a .js file defined in the URL query string (e.g., `?organometalic` loads `organometalic.js`).

## 🧪 Data Structure

To add a new quiz, create a `.js` file and ensure it follows this format:

```javascript
const questions = [
  {
    question: "What is the 18-electron rule?",
    options: ["Option A", "Option B", "Option C", "Option D"],
    answer: 0 // Index of the correct option
  }
];