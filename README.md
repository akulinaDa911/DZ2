# DZ2
child's homework
class Homework:
    def __init__(self, subject, task_done, grade=None):
        self.subject = subject
        self.task_done = task_done
        self.grade = grade

    def check_homework(self):
        if not self.task_done:
            return f"Домашнее задание по {self.subject} не выполнено."
        elif self.grade is None:
            return f"Домашнее задание по {self.subject} выполнено, но оценка не поставлена."
        else:
            return f"Домашнее задание по {self.subject} выполнено. Оценка: {self.grade}"

def check_all_homeworks(homeworks):
    for homework in homeworks:
        print(homework.check_homework())

# Пример использования
homeworks = [
    Homework(subject="Математика", task_done=True, grade=5),
    Homework(subject="Русский язык", task_done=False),
    Homework(subject="Физика", task_done=True, grade=4),
    Homework(subject="История", task_done=True, grade=None),
]

check_all_homeworks(homeworks)
