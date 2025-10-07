👨‍💻 Author

Alves Gonzalez
JavaScript ES5 | Browser Automation | QA Engineering

# 🤖 todomvc-creator-bot

## 📋 Overview
`todomvc-creator-bot` is a **personal JavaScript ES5 automation project** I wrote to practice DOM scripting and browser automation.  
It automatically creates 100 todo items on the official [TodoMVC JavaScript ES5 app](https://todomvc.com/examples/javascript-es5/dist/).

The bot runs directly in the browser console, adding new todos every 500 milliseconds and naming them sequentially (`todo0`, `todo1`, `todo2`, ...).

---

## ⚙️ Features
- Automatically creates 100 todo items  
- Sequential naming (`todo0` → `todo99`)  
- Works directly in the browser console  
- 100% **vanilla JavaScript (ES5)**  
- Stops automatically after reaching the limit  

---

## 💻 Code
```js
let botTodoCount = 0;
let creatorBot = setInterval(function() {
    document.querySelector('input.new-todo').value = "todo" + botTodoCount;
    document.querySelector('input.new-todo').dispatchEvent(new Event('change', { bubbles: true }));

    botTodoCount++;
    if (botTodoCount >= 100) {
        clearInterval(creatorBot);
    }
}, 500);




🧪 How to Use

Open the TodoMVC JavaScript ES5 demo:
🔗 https://todomvc.com/examples/javascript-es5/dist/

Open Chrome DevTools → Console

Paste the script above and press Enter

Watch as the bot automatically creates todos in real time

🧰 Requirements

Works in any modern web browser

No dependencies or installation needed
