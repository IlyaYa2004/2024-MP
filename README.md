# 2024-MP
Практика по курсам "Методы программирования" и "Программная инженерия" РФФ ННГУ

[Презентация по курсу (обновляемая)](https://docs.google.com/presentation/d/1wmYjy5QDoYECEHi7NAAINPulU9pLsaIi-aLaUppspps/edit?usp=sharing)

Для работы необходим python 3.9 и выше. Библиотеки: numpy, pandas, matplotlib, tensorflow, Pillow, scipy.signal. Редактор любой. Из неплохих: IDLE (родной, идёт вместе с установщиком), Visual Studio Code, notepad++, PyCharm, vim (для любителей сначала страдать, потом наслаждаться).

Работа с блокнотами онлайн, с возможностью подключения удалённых мощностей гугла (GPU, TPU): https://colab.research.google.com/

Таблица, где я буду отмечать сданные работы: [2023-Методы программирования](https://docs.google.com/spreadsheets/d/1ZWUKtqh-tL6q9-Yp9E7JzbmENkRBfSRvh4vgdkGI640/edit?usp=sharing)
Сервер в Дискорд, где буду дублировать: https://discord.gg/MzPkCYf4Dh (получить роль в канале "Основной") Мой контакт: nsmorozov@rf.unn.ru

Внутри папки группы создать папку имени себя (фамилия и имя). В своей папке можете делать все что угодно, в чужие не залезать, в корневую тоже. Я буду ориентироваться на файлы, где в названии будет номер лабораторной.

## Крайний срок приема работ 27.05.2024 до 11:00

## [1] Работа со структурами данных
	
Исходные данные:

- свои ФИО, число, месяц, год рождения в виде кортежа;
- предметы в школьном аттестате (не меньше 14), как словарь из названия и оценки (можно мокать);
- имена (только) ближайших (до двоюродных включительно) родственников в списке и их год рождения через пробел (в одной строке);
- имя, которое вы бы дали своей домашней пушистой киве (строка).

Действия:

1) вывести среднюю оценку в аттестате;
2) вывести уникальные имена среди своих родственников (включая свое);
3) общая длина всех названий предметов;
4) уникальные буквы в названиях предметов;
5) имя вашей домашней пушистой кивы в бинарном виде;
6) отсортированный по алфавиту (в обратном порядке) список родственников;
7) количество дней от вашей даты рождения до текущей даты (должна быть всегда актуальной);
8) FIFO очередь, в которую можно добавлять предметы по вводимому с клавиатуры индексу (до команды остановки), после введения - вывести все;
9) по введеному индексу, поменять имя в отсортированном списке родственников на имя ацтекского правителя (смотреть по списку всех на странице https://en.wikipedia.org/wiki/List_of_rulers_of_Tenochtitlan) под номером, получаемым из вашей даты рождения: number = (day + month**2 + year) % 21 + 1;
10) создать связный список, например, как словарь, где ключ - имя родственника, а значение (ссылка на следующий элемент) - индекс следующего имени по исходному списку, упорядоченному по их (родственников) годам рождения), исходный список при этом должен остаться неизменным;
11) написать функцию-генератор, свой вариант определяется как number = len("ФИО") * len (family_names) % 4:

	0. аликвотной последовательности; 
	1. последовательности Сильвестра; 
	2. числа трибоначчи; 
	3. числа Леонардо. 

## [2] Алгоритмы сортировки

### Исходные данные:

- список целых чисел от 0 до 999999;
- список из 99999 случайных вещественных чисел в диапазоне [-1, 1];
- 42000 разных точки комплексной плоскости, лежащие внутри окружности радиуса r = birth_day / birth_month (можно случайных, можно равномерно распределённых), сортировать по модулю числа;
- отрывок из книги (любой, на свой выбор) не менее 10000 слов, разбитый в список по словам.

### Действия:

Реализовать для каждого из исходных списков один из представленных алгоритмов сортировки (подробнее почитать о них [тут](https://habr.com/en/post/335920/)). Выбор тех четырех алгоритмов, которые будут использованы конкретно у вас: 

>>import random

>>random.sample(range(1, 18), 4) # вернет список из 4 случайных значений в заданном диапазоне

1. shaker sort, сортировка перемешиванием;
2. bubble sort, сортировка пузырьком;
3. comp sort, сортировка расческой;
4. insertion sort, сортировка вставкой;
5. Shellsort, сортировка Шелла;
6. tree sort, сортировка деревом;
7. Gnome sort, гномья сортировка;
8. selection sort, сортировка выбором;
9. Heapsort, пирамидальная сортировка;
10. Quicksort, быстрая сортировка;
11. Merge sort, сортировка слиянием;
12. Counting sort, сортировка подсчетом;
13. Bucket sort, блочная (карманная) сортировка;
14. Radix sort, поразрядная сортировка;
15. least significant digit;
16. most significant digit;
17. bitonic sort, битонная сортировка;
18. timsort, гибридная сортировка.

## [3] Алгоритмы поиска пути и структурное программирование

### Исходные данные:

- файл с текстовым представлением лабиринта;
- координаты аватара (если задали в стене, то переместить в любую соседнюю свободную);
- координаты ключа от выхода (если задали в стене, то переместить в любую соседнюю свободную);
- координаты выхода (на одной из внешних границ);
- правила нахождения пути до ключа и до выхода.

### Действия

1. В папке *_3* запустить скрипт gen_lab_origin.py, подождать его работу несколько минут;
2. Полученный файл maze-for-u.txt *переместить* в свою папку;
3. Найти любой маршрут от начальной координаты аватара до ключа, используя (выбрать или все, или по номеру сезона, в который вы родились, начиная с зимы):

	a. алгоритм Дейкстры;
	b. поиск в ширину;
	c. поиск в глубину;
	d. жадный алгоритм.
	
4. Используя А* со следующими параметрами (вес g(x), вес h(x), максимальная длина хранимого списка возможных шагов), найти оптимальный путь до ближайшего выхода;
5. Сохранить в файл 'maze-for-me-done.txt', в котором точка ключа будет указана как '*', а сам маршрут построен точками к ключу и запятыми от него к выходу.


## [4] Моделирование, сопрограммы и объектно-ориентированное программирование

### Исходные данные

### Действия
