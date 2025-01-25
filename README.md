# To-Do List App

A simple and intuitive To-Do List application that allows users to add, mark, and delete tasks. The app uses local storage to persist tasks even after refreshing the page. This project is ideal for beginners to learn and practice HTML, CSS, and JavaScript.

---

## 🌟 Features

- **Add Tasks:** Quickly add tasks to the list.
- **Mark as Completed:** Toggle tasks as completed or incomplete.
- **Delete Tasks:** Remove tasks from the list.
- **Local Storage Integration:** Tasks are saved in the browser's local storage to retain data after page reload.
- **Responsive Design:** User-friendly layout and intuitive UI.

---

## 🛠️ Technologies Used

- **HTML5**: For the structure of the app.
- **CSS3**: For styling the app with a modern look.
- **JavaScript**: For dynamic functionality and interactivity.

---

## 📂 Folder Structure

```
├── index.html       # The main HTML file
├── style.css        # The CSS file for styling
├── script.js        # The JavaScript file for functionality
├── images/          # Folder containing icons (unchecked and checked images)
```

---

## 🚀 How to Use

1. Clone the repository or download the project files.
   ```bash
   git clone <repository-url>
   ```

2. Open the `index.html` file in any modern browser.

3. Start adding your tasks by typing into the input box and clicking the **Add** button or pressing `Enter`.

4. Mark tasks as completed by clicking on them.

5. Delete tasks by clicking the **×** icon next to the task.

---

✨ Demo
Live Demo <!-- Add your deployed link here -->

---

## 📸 Screenshots

### Main Interface

![Main Interface](images/todo-screenshot.png)

### Adding Tasks

![Adding Tasks](images/add-task-screenshot.png)

### Marking Tasks as Completed

![Marking Tasks](images/mark-task-screenshot.png)

---

## 🧑‍💻 Code Highlights

### Adding Tasks
```javascript
function addTask() {
    if (inputBox.value === '') {
        alert("You must write something!");
        inputBox.value = ""; // Clear the input
    } else {
        let li = document.createElement("li");
        li.innerText = inputBox.value;
        listContainer.appendChild(li);

        let span = document.createElement("span");
        span.innerText = "\u00d7";
        li.appendChild(span);
    }
    inputBox.value = "";
    saveData();
}
```

### Saving and Showing Tasks from Local Storage
```javascript
function saveData() {
    localStorage.setItem("data", listContainer.innerHTML);
}

function showTask() {
    const savedData = localStorage.getItem("data");
    listContainer.innerHTML = savedData ? savedData : "";
}
showTask();
```

---

## 🤔 Future Enhancements

- Add an **Edit Task** feature to modify existing tasks.
- Implement **filters** to view all, completed, or pending tasks.
- Include a **dark mode** toggle for better user experience.

---

## 🏆 Acknowledgments

This project is created as part of a learning journey in web development. Special thanks to all the resources and tutorials that inspired this project.

---

## 📜 License

This project is licensed under the MIT License. Feel free to use and modify it as you like.

---

🌟 Don't forget to give this project a ⭐ if you liked it!

---

**Developed with ❤️ by Pranav Thorat**

