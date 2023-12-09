# Урок 2: Основы CSS
### 1.1 Тема: Введение в CSS
🔗[Документация для работы с СSS ](https://doka.guide/css/)

Обзор
CSS (Cascading Style Sheets) является языком, который используется для описания внешнего вида и форматирования документа, написанного на языке разметки. В этом уроке мы рассмотрим основы CSS, включая синтаксис, как CSS связывается с HTML, и начнем изучать основные стили. </br>
#### Так что же такое CSS?</br>
Как и HTML, CSS на самом деле не является языком программирования. Это не язык разметки - это язык таблицы стилей. Это означает, что он позволяет применять стили выборочно к элементам в документах HTML. </br>
Как устроены таблицы стилей
CSS, как и любой язык, имеет свой синтаксис. В нем есть правила — значения, которые определяют внешний вид элементов. CSS-правило состоит из селектора, CSS-свойств и их значений:

Селекторы — это метки, которые помогают браузеру понять, к какой части HTML-кода нужно применить заданные параметры.
CSS-свойства — это определенные параметры оформления, например цвет элемента или текста (color) или цвет фона (background).
Значение — это просто значение, оно выражается текстом или числом, например черный (black).
<pre>селектор {
свойство: значение;
} 
 
p {
color: black
}
</pre>
CSS-правила в коде заключаются в фигурные скобки {…}. Перед открытием скобки обязательно нужно указать селектор, к которому относится это правило.

В примере селектором является `<p>`, и он выбирает все теги с именем `<p>`, color — это CSS-свойство а black — значение CSS-свойства. Связка «свойство: значение» называется блоком объявления стилей. Внутри него свойство отделяется от значения двоеточием, а один блок от другого отделяет точка с запятой.

Таблицы называются каскадными, потому что работают по принципу каскада — то есть правило, прописанное ниже, считается приоритетным. Например, если в нашем примере под значением фонового цвета мы пропишем еще одно значение color: red, то цвет текста будет красным, а не черным.

#### Цели Урока:
Понимание Роли CSS в Веб-Разработке:

Объяснение, как CSS улучшает визуальное представление веб-страниц.Различие между HTML и CSS 
#### Основы Синтаксиса CSS:

Понимание структуры правил CSS: селекторы, свойства и значения.
Различные типы селекторов: тег, класс, идентификатор.
#### Подключение стилей CSS
Чтобы использовать CSS совместно с HTML, можно выбрать один из способов:

1. Весь код, написанный на CSS, прописывается в отдельном внешнем файле с расширением .css. Его подключают к HTML-странице при помощи тега <link href> — это служебный тег, который на странице не будет видно:
```
<head>
<link href=”style.css” rel=”stylesheet”>
</head>
```

Атрибут rel со значением stylesheet указывает, что в документе применяются именно стили текста. Это важно, так как, кроме применения стилей, тег <link> используется еще во множестве разных значений.

2. Прописать стили CSS внутри конкретного тега с помощью атрибута style:
```
 <p style=»color: black; background: #eeeeee»> Добавление стиля с помощью атрибута style</p>
```
3. Внутренний CSS : При этом подходе стили размещаются внутри тега <style>, который, в свою очередь, находится в секции <head> HTML-документа:
```
<head>
  <style>
    p { color: blue; font-size: 14px; }
  </style>
</head>
```
#### Основные Свойства CSS:
1) Цвет и фон (`color, background-color`).</br>🔗[Описание тегa для работы с background ](https://doka.guide/css/background-color/)</br>🔗[Описание тегa для работы с color ](https://doka.guide/css/color/).
2) Шрифты (`font-family, font-size, font-weight`).
3) Текст (`text-align, line-height, text-decoration`).
4) margin: Внешний отступ вокруг элемента(`padding, border, width, height`).
5) Позиционирование и Отображение: (`position, display, z-index`)
6) Флексбокс и Грид: (`display: flex, display: grid`)
7) Анимации и Переходы: (`transition, animation, @keyframes`)
   
### Некоторые свойства: </br>
CSS-свойства влияющие на шрифт</br>
font-style стиль шрифта</br>
font-variant малые заглавные</br>
font-weight жирность шрифта</br>
font-size размер шрифта</br>
font-family шрифт элемента</br>

### CSS-свойства влияющие на цвет и фон:</br>
color: green;    цвет текста</br>
background-color: red;   фон</br>
CSS-свойства влияющие на границу(обводку)</br>
border: 1px solid red рамка</br>
border-radius: 50px; скругление рамки</br>

### CSS-свойства влияющие на текст:</br>
text-align: center;  поставит текст по центру </br>
text-indent: 20px; — отступ первой строки равен 20 пикселям, </br>
line-height задает расстояние между строками</br>
CSS-свойства влияющие на размеры объекта</br>
width: 100px; ширина</br>
height: 100px; высота</br>



### 🏆 Задание 1:
 1.1 Исследование различных веб-сайтов для анализа их стилей и попытка воссоздания некоторых элементов дизайна. </br>

 1.2 Работа с текстом  </br>
🔗[Ссылка на задание 1.2](https://greatcode.ru/lesson_2.1.html). </br>
1.3 У этого задания есть небольшое ТЗ: 
  1) В CSS файле в самом верху создайте селектор для тега body и напишите следующие стили - шрифт Arial, sans-serif, размер шрифта 16px, цвет текста #333, межстрочный отступ 1.5
  2) В CSS файле создайте селектор для класса title, и напишите следующие стили - размер шрифта 40px, цвет текста #f03333, межстрочный отступ 1.2, все буквы заглавные
  3) После заголовка создайте абзац и напишите там немного текста, можете использовать сайт-генератор случайного текста lipsum.com
  4) После абзаца создайте заголовок второго уровня, напишите текст "Заголовок второго уровня" и придайте ему класс subtitle
5) В CSS файле создайте селектор для класса subtitle, и напишите следующие стили - размер шрифта 30px, цвет текста #12ac11, межстрочный отступ 1.2, подчеркивание текста снизу
6) После заголовка создайте абзац и напишите там немного текста, можете использовать lorem или от себя
7) После абзаца создайте ненумерованный список с тремя пунктами
8) В каждом пункте напишите немного текста, на свой выбор
9) Задайте списку класс list
10) В CSS файле создайте селектор для класса list, и напишите следующие стили - размер шрифта 20px, цвет текста #444, все буквы наклонные, стиль маркеров списка - square </br>
### Итог: не смотри итоговое задание пока не сделаешь по ТЗ 
🚨🚨🚨🛑🛑🛑🛑🛑🛑🛑
🔗[Ссылка на задание 1.3](https://greatcode.ru/lesson_2.2.html). </br>
### ⭕❌⛔🚫Не открывать пока не закончишь задание по ТЗ и потом сравни результат

 1.4 🔗[Ссылка на задание 1.4](https://greatcode.ru/lesson_2.3.html)


