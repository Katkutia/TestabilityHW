 # 3. 1 Домашнее задание к занятию «Testability. Введение в ООП»

## Цель задания

1. Написать свои сервисные классы.
2. Научиться писать многофайловую программу.

------

## Инструкция к заданию

1. Скачайте и установите профессиональный редактор кода [Intellij Idea Community Version](https://www.jetbrains.com/idea/download/).
1. Откройте IDEA и [создайте новый Java-проект](https://github.com/netology-code/javaqa-homeworks-video/blob/javaqa-55/QA_Java_Idea_Create.md). Под каждую задачу следует создавать отдельный проект, если обратное не сказано в условии.
2. Создайте пустой репозиторий на GitHub и свяжите его с папкой вашего проекта, а не с какой-либо другой.
3. Правильно настройте репозиторий в плане `.gitignore`. Проигнорируйте папки `.idea` и `out` и `.iml`-файл — их в репозитории быть не должно.
4. Выполните в IDEA требуемую задачу согласно условию.
5. Проверьте соблюдение [правил форматирования кода](https://github.com/netology-code/javaqa-homeworks-video/blob/javaqa-55/QA_Java_Idea_Format.md).
6. Закоммитьте и отправьте в репозиторий содержимое папки проекта.

------

## Материалы, которые пригодятся для выполнения задания

1. [Как создать Java-проект в IDEA?](https://github.com/netology-code/javaqa-homeworks-video/blob/javaqa-55/QA_Java_Idea_Create.md)
1. [Как отформатировать код в Java?](https://github.com/netology-code/javaqa-homeworks-video/blob/javaqa-55/QA_Java_Idea_Format.md)

------

## Задание 1 — обязательное

В этой задаче мы считаем, что пользователь вводит корректные значения входных данных.

Вы уже научились создавать классы и методы. Поэтому вам необходимо модернизировать [приложение для расчёта миль](https://github.com/netology-code/javaqa-homeworks-video/blob/javaqa-55/HW_PRIMITIVES.md). Напомним, мили начисляются как 1 миля за каждые 20 рублей в стоимости билета, дробные мили не допускаются. 

Теперь сама логика расчёта будет находиться в специально выделенном классе сервиса, а в `Main` мы будем лишь создавать объект этого сервиса и вызывать его метод, передавая аргументами все необходимые данные для расчёта. Получив от вызова метода рассчитанный результат, мы выведем его на экран.

Создайте класс `BonusMilesService`: `File -> New -> Java Class`, вводите название и нажимаете `Enter`.

Определите в нём метод `calculate`, который:
* принимает на вход один параметр: цену билета, типа `int`;
* анализируя значение переданного параметра, возвращает рассчитанное количество миль.

Разместите следующий код в классе `Main`:

```java
public class Main {
    public static void main(String[] args) {
        BonusMilesService service = new BonusMilesService();
        int price = 10_000;
        int miles = service.calculate(price); // должно получиться 500
        System.out.println(miles);
    }
}
```

Убедитесь, что выводимое в консоль значение соответствует логике расчёта бонуса. Проверьте на разных примерах.

------

## Правила приёма работы

Для каждой задачи прикреплена ссылка на публичный репозиторий GitHub с решением.


------

## Критерии оценки

1. В каждом репозитории размещено содержимое папки проекта IDEA. Корнем репозитория должна быть именно папка проекта — не папка `src`, не папка внутри которой лежит папка проекта. Таким образом, в корне репозитория должна лежать сразу папка `src`.
1. Есть файл `.gitignore`, игнорирующий ненужные файлы и папки, которые должны отсутствовать в репозитории. Если они присутствуют, их нужно оттуда удалить.
1. Программа соответствует всем требованиям из условия задачи.
1. Программа использует только те инструменты языка, которые мы проходили или которые прямо разрешены условием задачи.
1. Программа работает правильно на всех примерах из условия.
1. Программный код отформатирован и соответствует пройденным требованиям к качеству кода.
1. Программа спроектирована достаточно логично и правильно, не противоречит общепринятым в производстве практикам и традициям.
1. При наличии недочётов, в зависимости от их серьёзности и количества, работа может быть отправлена на доработку или принята — решение принимается на основе экспертной оценки работы.
