# Python-RFM

Имеется 3 датасета:

- olist_orders_dataset.csv — таблица заказов
- olist_order_items_dataset.csv — товарные позиции, входящие в заказы
- olist_customers_datase.csv — таблица с уникальными идентификаторами пользователей

Необходимо построить RFM-сегментацию пользователей, чтобы качественно оценить аудиторию интернет-магазина.

- R - время от последней покупки пользователя до текущей даты
- F - суммарное количество покупок у пользователя за всё время
- M - сумма покупок за всё время

Для каждого RFM-сегмента нужно построить границы метрик recency, frequency и monetary для интерпретации этих кластеров.

Для решения задачи я использовал Python и платформу Jupyter.

Использованные библиотеки:

- pandas для анализа данных
- matplotlib.pyplot для визуализации данных.

# Решение

Готовое решение задачи с подробными описанием находится в файле "RFM-сегментация.ipynb".

Исходные датасеты лежат в файле "Датасеты.zip".

Наполнение датасетов:

olist_orders_dataset.csv —  таблица заказов
- order_id —  уникальный идентификатор заказа (номер чека)
- customer_id —  позаказный идентификатор пользователя
- order_status —  статус заказа
- order_purchase_timestamp —  время создания заказа
- order_approved_at —  время подтверждения оплаты заказа
- order_delivered_carrier_date —  время передачи заказа в логистическую службу
- order_delivered_customer_date —  время доставки заказа
- order_estimated_delivery_date —  обещанная дата доставки

olist_order_items_dataset.csv —  товарные позиции, входящие в заказы
- order_id —  уникальный идентификатор заказа (номер чека)
- order_item_id —  идентификатор товара внутри одного заказа
- product_id —  ид товара (аналог штрихкода)
- seller_id — ид производителя товара
- shipping_limit_date —  максимальная дата доставки продавцом для передачи заказа партнеру по логистике
- price —  цена за единицу товара
- freight_value —  вес товара

olist_customers_datase.csv — таблица с уникальными идентификаторами пользователей
- customer_id — позаказный идентификатор пользователя
- customer_unique_id —  уникальный идентификатор пользователя  (аналог номера паспорта)
- customer_zip_code_prefix —  почтовый индекс пользователя
- customer_city —  город доставки пользователя
- customer_state —  штат доставки пользователя
