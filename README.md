# О работе

Использовуя Pandas очистил данные от дубликатов, аномалий и пропусков, преобразовал типы данных и добавил новые категориальные признаки. Эта часть была проверена автоматически. На основании сводных таблиц провел анализ того как различные факторы влияют на воврат кредита

Технологии: Python, Pandas

# Вывод в конце работы

## Данные для анализа и их предобработка

Анализ был проведен на данных о 21525 заемщиков кредитов. Был удален 71 дупликат.

### Были решены следующие проблемы во входных данных:

1. Отрицательные значения в столбце days_employed сделаны положительными.
2. Для каждого из типов дохода пропуски в столбцах total_income и days_emloyed были заполнены медианными значениями этой группы
3. Удалены строки с аномальным количеством детей (20, -1)

### Изменения в данных

1. Добавлен стоблец с категорией уровня дохода total_income_category и столбец с категорией цели кредита purpose_category

### Рекомендации по сбору данных

1. Наладить автоматизированную систему так, чтобы в данных не возникало отрицательных чисел
2. Добавить в опрос пользователя обязательный пункт "Цель кредита"
3. Записывать все качественный описания пользователя в нижнем регистре (образование не Высшее, а высшее)

### 3.5 Возможные причины появления пропусков в исходных данных.

Пропуски есть лишь в столбцах days_employed и total_income

Это может быть по тому, что:

1. Люди могут не хотеть раскрывать свое место работы и свой доход
2. Люди не могут подвердить свое место работы и доход
3. Произошла техническая ошибка

## Итоги анализа

### Есть ли зависимость между количеством детей и возвратом кредита в срок?

Сделать вывод о том, как часто кредит всрок возвращают люди с 4 и 5-ю детьми невозможно из-за недостатка данных.  
Заемщики без детей в среднем на 1-2 процента чаще возвращают кредит всрок, что может быть связано с отсутствием расходов на детей.  
Люди с 1 ребенком или 2 детьми не возвращают кредит практически одинаково часто (9.3% случаев). Лица с 3-мя детьми детьми не возвращают кредит чуть чаще (8.5% случаев).

### 3.2 Есть ли зависимость между семейным положением и возвратом кредита в срок?

Люди в статусе вдовца / вдовы наиболее успешно возвращают кредиты, что может быть связано с полученным наследством или с тем, что они брали кредит на похороны. Часто, такие кредиты компесируются родственниками. _(невозврат в 6.6% случаев)_  
Люди в в браке _(невозврат в 7.6% случаев)_ и в разводе _(невозврат в 7% случаев)_ возвращают кредиты на 2% лучше чем люди не замужем _(невозврат в 9.7% случаев)_ или в гражданском браке _(невозврат в 9.5% случаев)_, и на 1% хуже чем люди потерявшие супругу / супруга _(невозврат в 6.6% случаев)_.

### 3.3 Есть ли зависимость между уровнем дохода и возвратом кредита в срок?

Данных по категории А и Е слишком мало для точных выводов. Наиболее успешно кредиты возвращают люди с доходом 30001–50000, что может быть связано с маленькими сумамаи кредита _(случаев невозврата 6%)_  
Для категорий B и C можем заметить, что с ростом дохода уменьшается количество возвратов всрок _(Для D 91.5%, а для B 93%)_

### 3.4 Как разные цели кредита влияют на его возврат в срок?

Кредиты, взятые на недвижимость, возвращают чаще всего _(невозврат в 7.2% случаях)_, на 0.7 % реже возвращают кредиты на свадьбу. Кредиты на автомобиль и образование возвращают на 2% реже чем кредиты на недвижимость _(невозврат в 9.3% случаях)_.

# ТЗ

## Описание проекта

Заказчик — кредитный отдел банка. Нужно разобраться, влияет ли семейное положение и количество детей клиента на факт погашения кредита в срок. Входные данные — статистика о платёжеспособности клиентов.

Результаты исследования будут учтены при построении модели **кредитного скоринга** — специальной системы, которая оценивает способность потенциального заёмщика вернуть кредит банку.

## Описание данных

- `children` — количество детей в семье
- `days_employed` — общий трудовой стаж в днях
- `dob_years` — возраст клиента в годах
- `education` — уровень образования клиента
- `education_id` — идентификатор уровня образования
- `family_status` — семейное положение
- `family_status_id` — идентификатор семейного положения
- `gender` — пол клиента
- `income_type` — тип занятости
- `debt` — имел ли задолженность по возврату кредитов
- `total_income` — ежемесячный доход
- `purpose` — цель получения кредита

## Что важно учесть

На что нужно обратить внимание:

- Как вы описываете найденные в данных проблемы?
- Какие методы замены типов данных, обработки пропусков и дубликатов применяете?
- Категоризируете ли данные?
- Соблюдаете ли структуру проекта и поддерживаете аккуратность кода?
- Какие выводы делаете?
- Оставляете ли комментарии к шагам?

Держите под рукой шпаргалки и конспекты прошлых уроков.

Успехов!

# Технические комментарии
- Версия с опциональной критикой без правок
- Diamond