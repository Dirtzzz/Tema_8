# Тема 8. Основы объектно-ориентированного программирования
Отчет по Теме #8 выполнил:
- Ильдейкин Антон Александрович
- ИНО ЗБ ПОАС-22-2

| Задание | Лаб_раб | Сам_раб |
| ------ | ------ | ------ |
| Задание 1 | - | + |
| Задание 2 | - | + |
| Задание 3 | - | + |
| Задание 4 | - | + |
| Задание 5 | - | + |
| Задание 6 | - | - |
| Задание 7 | - | - |
| Задание 8 | - | - |
| Задание 9 | - | - |
| Задание 10 | - | - |

Работу проверили:
- к.э.н., доцент Панов М.А.
## Самостоятельная работа №1
### Самостоятельно создайте класс и его объект. Они должны отличаться, от тех, что указаны в теоретическом материале (методичке) и лабораторных заданиях. Результатом выполнения задания будет листинг кода и получившийся вывод консоли.

```python
class product:
    def __init__(info, type, price, color):
        info.type = type
        info.price = price
        info.color = color

    def show_inf(info):
        print(f"Информация о товаре:\nТовар: {info.type}\nЦена: {info.price}\nЦвет: {info.color}")

    def gg (info):
        if info.color == "Черный":
            print(f"Черный {info.type}\n")
        elif info.color == "Белый":
            print(f"Белый {info.type}\n")
        elif info.color == "Серый":
            print(f"Серый {info.type}\n")

product1 = product('ноутбук', 300000, 'Белый')
product1.show_inf()
product1.gg()
product2 = product("ноутбук", 60000, "Черный")
product2.show_inf()
product2.gg()
product3 = product("ноутбук", 75000, "Серый")
product3.show_inf()
product3.gg()
```
### Результат:
![Меню](https://github.com/Dirtzzz/Tema_8/blob/main/8.1.png)
Вывод консоли:
![Меню](https://github.com/Dirtzzz/Tema_8/blob/main/8.1(1).png)

## Самостоятельная работа №2
### Самостоятельно создайте атрибуты и методы для ранее созданного класса. Они должны отличаться, от тех, что указаны в теоретическом материале (методичке) и лабораторных заданиях. Результатом выполнения задания будет листинг кода и получившийся вывод консоли.

```python
class Product:
    def __init__(info, type, price, color, stock):
        info.type = type
        info.price = price
        info.color = color
        info.stock = stock  # новый атрибут

    def show_inf(info):
        print(f"Информация о товаре:\nТовар: {info.type}\nЦена: {info.price}\nЦвет: {info.color}")

    def gg(info):
        if info.color == "Черный":
            print(f"Черный {info.type}\n")
        elif info.color == "Белый":
            print(f"Белый {info.type}\n")
        elif info.color == "Серый":
            print(f"Серый {info.type}\n")

    def check_stock(info):
        print(f"Количество товара на складе: {info.stock}")

product1 = Product('ноутбук', 300000, 'Белый', 10)
product1.show_inf()
product1.gg()
product1.check_stock()

product2 = Product("ноутбук", 60000, "Черный", 5)
product2.show_inf()
product2.gg()
product2.check_stock()

product3 = Product("ноутбук", 75000, "Серый", 15)
product3.show_inf()
product3.gg()
product3.check_stock()
```

### Результат:
![Меню](https://github.com/Dirtzzz/Tema_8/blob/main/8.2.png)
Вывод консоли:
![Меню](https://github.com/Dirtzzz/Tema_8/blob/main/8.2(1).png)

## Самостоятельная работа 3
### Самостоятельно реализуйте наследование, продолжая работать с ранее созданным классом. Оно должно отличаться, от того, что указано в теоретическом материале (методичке) и лабораторных заданиях. Результатом выполнения задания будет листинг кода и получившийся вывод консоли.

```python
class Product:
    def __init__(info, type, price, color, stock):
        info.type = type
        info.price = price
        info.color = color
        info.stock = stock

    def show_inf(info):
        print(f"Информация о товаре:\nТовар: {info.type}\nЦена: {info.price}\nЦвет: {info.color}")

    def gg(info):
        if info.color == "Черный":
            print(f"Черный {info.type}\n")
        elif info.color == "Белый":
            print(f"Белый {info.type}\n")
        elif info.color == "Серый":
            print(f"Серый {info.type}\n")

    def check_stock(info):
        print(f"Количество товара на складе: {info.stock}")

# новый класс, наследующийся от Product
class ElectronicProduct(Product):
    def __init__(info, type, price, color, stock, battery_life):
        super().__init__(type, price, color, stock)
        info.battery_life = battery_life

    def show_battery_life(info):
        print(f"Время работы от батареи: {info.battery_life} часов")

product1 = ElectronicProduct('ноутбук', 300000, 'Белый', 10, 15)
product1.show_inf()
product1.gg()
product1.check_stock()
product1.show_battery_life()
```

### Результат:
![Меню](https://github.com/Dirtzzz/Tema_8/blob/main/8.1(1).png)
Вывод консоли:
![Меню](https://github.com/Dirtzzz/Tema_8/blob/main/8.3.png)

## Самостоятельная работа 4
### Самостоятельно реализуйте инкапсуляцию, продолжая работать с ранее созданным классом. Она должна отличаться, от того, что указана в теоретическом материале (методичке) и лабораторных заданиях. Результатом выполнения задания будет листинг кода и получившийся вывод консоли.

```python
class product:
    def __init__(info, type, price, color):
        info._type = type
        info._price = price
        info._color = color

    def greet(info):
        return f"Это {info._type}, он стоит {info._price} и он {info._color} цвета."

product1 = product("Ноутбук MSI", "50000", "серого")

print(product1._type)
print(product1.greet())
```

### Результат:
![Меню](https://github.com/Dirtzzz/Tema_8/blob/main/8.4.png)

## Самостоятельная работа 5
### Самостоятельно реализуйте полиморфизм. Он должен отличаться, от того, что указан в теоретическом материале (методичке) и лабораторных заданиях. Результатом выполнения задания будет листинг кода и получившийся вывод консоли.

```python
class product:
    def __init__(info, type, price, color):
        info.type = type
        info.price = price
        info.color = color

    def show_inf(info):
        print(f"\nТовар: {info.type}\nЦена: {info.price}\nЦвет: {info.color}")

class phone(product):
    def __init__(info, type, price, color, OS):
        super().__init__(type, price, color)
        info.OS=OS
    def show_inf(info):
        print(f"\nТовар: {info.type}\nЦена: {info.price}\nЦвет: {info.color}\nОперационная система: {info.OS}")

class fridge(product):
    def __init__(info, type, price, color, display):
        super().__init__(type, price, color)
        info.display=display
    def show_inf(info):
        print(f"\nТовар: {info.type}\nЦена: {info.price}\nЦвет: {info.color}\nНаличие дисплея: {info.display}")


product1 = product('Ноутбук', 300000, 'белый')
product1.show_inf()
phone1 = phone("Телефон", 80000, "черный", "андроид")
phone1.show_inf()
fridge1 = fridge("Холодильник", 75000, "серый","есть")
fridge1.show_inf()
```

### Результат:
![Меню](https://github.com/Dirtzzz/Tema_8/blob/main/8.5.png)
Вывод консоли:
![Меню](https://github.com/Dirtzzz/Tema_8/blob/main/8.5(1)).png)
