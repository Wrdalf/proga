# software-ingineering

Отчет по Теме #9 выполнил(а):

Бидаев Альфред Александрович
- ПИЭ-21-1



| Задание | Лаб_раб | Сам_раб |
| ------ | ------ |---|
| Задание 1 | + | + |
| Задание 2 | + | + |
| Задание 3 | + | + |
| Задание 4 | + | + |
| Задание 5 | + | + |


# Лабораторная работа # 1

### Создайте класс "Car" с атрибутами производитель и модель. Создайте объект этого класса. Напишите комментарии для кода, объясняющие его работу. Результатом выполнения задания будет листинг кода с комментариями.

```python
class Car:
    def __init__(self, make, model):
        self.make = make
        self.model = model
my_car = Car ("Toyota", "Corolla")
```
### Результат:

# Лабораторная работа # 2

### Дополните код из первого задания, добавив в него атрибуты и методы класса, заставьте машину "поехать". Напишите комментарии для кода, объясняющие его работу. Результатом выполнения задания будет листинг кода с комментариями и получившийся вывод в консоль.

```python
class Car:
    def __init__(self, make, model):
        self.make = make
        self.model = model

    def drive(self):
        print(f"Driving the {self.make} {self.model}")

my_car = Car ("Toyota", "Corolla")
my_car.drive()
```
### Результат:

![alt text](image.png)

# Лабораторная работа # 3

### Создайте новый класс "ElectricCar" с методом "charge" и атрибутом емкость батареи. Реализуйте его наследование от класса, созданного в первом задании. Заставьте машину поехать, а потом заряжаться. Напишите комментарии для кода, объясняющие его работу.
Результатом выполнения задания будет листинг кода с комментариями и получившийся вывод в консоль.

```python
# Определение класса ElectricCar, который является подклассом класса Car
class ElectricCar(Car):
    # Конструктор класса ElectricCar, принимающий марку, модель и емкость батареи
    def __init__(self, make, model, battery_capacity):
        # Вызов конструктора родительского класса с помощью super(),
        # чтобы инициализировать атрибуты марки и модели
        super().__init__(make, model)
        # Инициализация нового атрибута battery_capacity емкостью батареи
        self.battery_capacity = battery_capacity

    # Метод charge(), который выводит сообщение о зарядке электромобиля
    def charge(self):
        print(f"Charging the {self.make} {self.model} with {self.battery_capacity} kWh")

# Создание экземпляра класса ElectricCar с маркой Tesla, моделью Model S и емкостью батареи 75 кВт⋅ч
my_electric_car = ElectricCar("Tesla", "Model S", 75)

# Вызов метода drive() у экземпляра my_electric_car, унаследованного от родительского класса Car
my_electric_car.drive()

# Вызов метода charge() у экземпляра my_electric_car класса ElectricCar
my_electric_car.charge()

```
### Результат:


# Лабораторная работа # 4

### Реализуйте инкапсуляцию для класса, созданного в первом задании.
Создайте защищенный атрибут производителя и приватный атрибут модели. Вызовите защищенный атрибут и заставьте машину поехать.
Напишите комментарии для кода, объясняющие его работу.
Результатом выполнения задания будет листинг кода с комментариями и получившийся вывод в консоль.

```python
class Car:
    def __init__(self, make, model):
        self.make = make
        self.model = model

    def drive(self):
            print(f"Driving the {self.make} {self.model}")

my_car = Car ("Toyota", "Corolla")
print(my_car.make)
my_car.drive()
```
### Результат:

![alt text](image-1.png)

# Лабораторная работа # 5

### Реализуйте полиморфизм создав основной (общий) класс "Shape", а также еще два класса "Rectangle" и "Circle". Внутри последних двух классов реализуйте методы для подсчета площади фигуры. После этого создайте массив с фигурами, поместите туда круг и прямоугольник, затем при помощи цикла выведите их площади. Напишите комментарии для кода, объясняющие его работу. Результатом выполнения задания будет листинг кода с комментариями и получившийся вывод в консоль.

```python
class Shape:
    def area(self):
        pass

class Rectangle(Shape):
    def __init__(self, width, height):
        self.width = width
        self.height = height

    def area(self):
        return self.width * self. height
class Circle(Shape):
    def __init__ (self, radius) :
        self.radius = radius
    def area(self):
        return 3.14 * self. radius * self. radius
```
### Результат:

![alt text](image-2.png)