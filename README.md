# ИСБД Лаба 1

Ну лаба и лаба.

ПИиКТ 3 курс ИСБД (Информационные системы и базы данных)
Вариант: 309553

## Описание предметной области, по которой должна быть построена доменная модель:
```
Сквозь иллюминатор Флойд ясно видел стелющуюся перед ними отчетливо обозначенную дорогу: 
десятки машин, прошедшие по ней, оставили в хрупкой породе лунной поверхности плотно 
укатанные колеи. Вдоль дороги через определенные промежутки были установлены высокие 
тонкие вехи с яркими лампами. На трехсоткилометровом маршруте от базы Клавий до ЛМА-1
заблудиться было невозможно, хотя кругом стояла еще глубокая ночь и до рассвета 
оставалось несколько часов. 
```

## Моё описание 
```
Есть дорога. На неё можно посмотреть. Машины ездят по ней и оставляют колеи.
Колеи бывают плотно укатанные. Вдоль дороги установлены высокие вехи с лампами.
Лампы бывают яркие. Есть базы: база Клавий. Есть аномалии: ЛМА-1(кратер). 
Маршрут от базы Клавий до ЛМА-1 - 300 км.
```

## Понимание задачи
Придумай свой OSM и чтобы работало.

## Список сущностей
### Стержневые
- Точка = (x, y)
- Место = точка, название, тип
- Дорога = список точек, дата появления
- Машина = марка, модель, 4 колеса

### Характеристики
- Колея = дорога, начало колеи, конец колеи, дата появления
- Колесо = размер, изготовитель
- Ремонт дороги = дорога, начало участка, конец участка, дата ремонта
- Положение машины = индентификатор машины и точка
- Тип места = кратер (аномалия) или база.

### Ассоциации
- Маршрут = список точек, начальное место, конечное место