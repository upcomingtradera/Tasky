## a skeleton project for a simple task management tool

### sections of the tool
    - **Task Creation**: Users should be able to create a new task with a title and perhaps a brief description.
    - **Task List**: Users should be able to view a list of all their tasks. Ideally, this list would update in real-time as tasks are added, modified, or removed.
    - **Task Modification**: Users should be able to update the details of a task after it's been created, such as changing its title or description.
    - **Task Completion**: Users should be able to mark a task as completed. Completed tasks might be moved to a separate list or crossed off in the main list.
    - **Task Deletion**: Users should be able to delete a task when it's no longer needed.



### Python skeleton
```python
class Task:
    def __init__(self, title, description):
        self.title = title
        self.description = description
        self.is_completed = False

    def mark_as_completed(self):
        self.is_completed = True

class TaskManager:
    def __init__(self):
        self.tasks = []

    def create_task(self, title, description):
        task = Task(title, description)
        self.tasks.append(task)

    def delete_task(self, task):
        self.tasks.remove(task)

    def get_all_tasks(self):
        return self.tasks

    def get_completed_tasks(self):
        return [task for task in self.tasks if task.is_completed]

    def get_incomplete_tasks(self):
        return [task for task in self.tasks if not task.is_completed]
```
