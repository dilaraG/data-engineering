# data-engineering
Газизова Д.М., Туризм и гостиничный бизнес в Стамбуле

1. Домен: Туризм и гостиничный бизнес.
Бизнес-проблема: Оптимизация предложений по отелям и достопримечательностям для повышения клиентского опыта и увеличения числа бронирований.
Оптимизация предложений для туристов: анализ достопримечательностей, которые находятся рядом с отелями и как это влияет на выбор туристов.

2. Сбор данных (csrap_hotels_info.ipynb, scrap_geoposition.ipynb, scrap_hotels_info.ipynb):
   1) Скрапинг данных по отелям в Стамбуле с сайта Tripadvisor.ru - df = hotels_info
   2) Скрапинг координат по адресу из данных hotels_info с сайта https://nominatim.openstreetmap.org - df = hotels_info_coord
   3) Скрапинг данных по достопримечательностям Стамбула с сайта Tripadvisor.ru - df = dostoprim_info
   4) Скрапинг координат по адресу из данных dostoprim_info с сайта https://nominatim.openstreetmap.org - df = dostoprim_info_coord

3. Очистка, предобработка данных и анализ для выявления зависимостей - normilize_df.ipyn
   На основе анализа по графику можно заметить, что частота встречаемости отелей в городе не так популярна (по кол-ву отзывов)
   Популярны больше отели на побережье, хотя встречаемость их меньше
5. Хранение данных
   База данных Postgresql
   скрипт для создания бд - create_db.ipynb
7. Дашборды
   Построение в datalens.yandex.cloud
   Подключение бд -> Создание датасета -> Создание чартов на основе трех таблиц -> Создание дашборда из чартовы 
