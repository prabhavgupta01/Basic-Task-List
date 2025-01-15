# Basic-Task-List
# Task Management App Documentation

## Overview
This is a simple command-line Task Management Application implemented in Python. It allows users to manage a list of tasks by adding, removing, listing, and recommending tasks based on priority. The application uses a CSV file to persist task data between sessions.

---

## Features
1. **Add Tasks:** Add new tasks with a description and priority (Low, Medium, or High).
2. **Remove Tasks:** Remove a task by its description.
3. **List Tasks:** View all the tasks with their descriptions and priorities.
4. **Recommend Tasks:** Suggest a high-priority task to focus on.
5. **Persistent Storage:** Tasks are saved to a `tasks.csv` file and loaded automatically when the app starts.

---

## Prerequisites
- Python 3.x
- Pandas library

To install Pandas, use:
```bash
pip install pandas
```

---

## Code Description

### 1. **Imports**
```python
import pandas as pd
import random
```
- `pandas`: Handles data storage and manipulation.
- `random`: Selects a random high-priority task for recommendations.

### 2. **Global Variables**
- `tasks`: A DataFrame that stores task descriptions and priorities.
- Tasks are loaded from `tasks.csv` if available, otherwise initialized as an empty DataFrame.

### 3. **Functions**

#### `save_tasks()`
Saves the `tasks` DataFrame to `tasks.csv`.

#### `add_task(description, priority)`
Adds a new task to the `tasks` DataFrame and saves it.

#### `remove_task(description)`
Removes a task by its description from the `tasks` DataFrame and saves the changes.

#### `list_tasks()`
Displays all tasks. If no tasks are available, it prints a message.

#### `recommend_task()`
Recommends a random high-priority task if available.

### 4. **Main Menu**
A loop that provides options to:
- Add a task
- Remove a task
- List all tasks
- Recommend a task
- Exit the application

---

## Usage

1. Clone the repository:
```bash
git clone https://github.com/your-username/task-management-app.git
```

2. Navigate to the project directory:
```bash
cd task-management-app
```

3. Run the script:
```bash
python task_management.py
```

4. Follow the prompts to manage your tasks.

---

## File Structure
```
task-management-app/
│
├── task_management.py   # Main Python script
├── tasks.csv            # CSV file for storing tasks (auto-generated)
└── README.md            # Documentation
```

---

## Sample Output
```
Task Management App
1. Add Task
2. Remove Task
3. List Tasks
4. Recommend Task
5. Exit
Select an option: 1
Enter task description: Complete project report
Enter task priority (Low/Medium/High): High
Task added successfully.

Task Management App
1. Add Task
2. Remove Task
3. List Tasks
4. Recommend Task
5. Exit
Select an option: 4
Recommended task: Complete project report - Priority: High
```

---

## Contributing
1. Fork the repository.
2. Create a new branch:
   ```bash
   git checkout -b feature-branch
   ```
3. Commit your changes:
   ```bash
   git commit -m "Description of changes"
   ```
4. Push to the branch:
   ```bash
   git push origin feature-branch
   ```
5. Open a pull request.

---

## License
This project is licensed under the MIT License.

Feel free to use and modify the code! Contributions are welcome.
