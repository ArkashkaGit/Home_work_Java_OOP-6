# Объектно-ориентированное программирование
## на основе языка JAVA
## Home work 6

![java](java.jpeg)


## ___Задача 1.___
___Чтобы разблокировать телефон, 
пользователь может выбрать один из способов:___
- Без пароля
- С пин-кодом (4-значное число)
- По отпечатку пальца (кодируется строкой)
- По распознаванию лица (кодируется строкой)

Программист написал класс Unlocker, 
в котором хранятся поля от всех способов сразу:
><i>class Unlocker {

>private int mode; // режим

>private int pin; // на случай пин-кода

>private String fingerprint; // на случай отпечатка пальца

>private String faceID; // на случай лица

>}</i>

Здесь нарушен принцип SRP: 
класс имеет несколько незаивисимых причин меняться.

Напишите решение, которое будет соответствовать SRP и OCP 
(мы хотим в будущем добавлять новые способы разблокировки).

## ___Задача 2.___
___Есть два самодельных класса коллекций:___

- ImmutableList<T> — коллекция, 
которая никогда ни при каких обстоятельствах не меняется. 
Методы:

><i>getSize ()

>get (int i)</i>

- MutableList<T> — коллекция, 
которая допускает изменения. 
Методы:
><i>getSize ()

>get (int i)

>set (int i, T newValue)

>add (T newValue)

>remove (T value)</i>

Реализуйте такую схему наследования между двумя этими классами, 
которая будет соответствовать принципу подстановки Лисков.