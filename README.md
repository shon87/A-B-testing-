# A/B-testing: Расчет объемов выборки и оценка результатов

## План A/B теста:
* Планируем эксперимент 
* Собираем и готовим данные  
* Разведочный анализ
* Проверка гипотезы 
* Выводы

### Планируем эксперимент
Например, мы хотим увеличить конверсию в подписку предлагая разные условия пробного периода (триала). Вариант А - 30 дней, вариат B - 15 дней. <br />
Здесь нужно сформулировать нулевую гипотезу H0 и альтернативную H1 <br />
#### Нулевая гипотеза: 
Конверсия в подписку при разных условиях пробного периода НЕ отличаются. <br />
#### Альтернативная гипотеза: 
Конверсия в подписку при разных условиях пробного периода ЗНАЧИМО отличаются. <br />
**Пояснение:** 
*в нашем случае, мы хотим, чтобы верной оказалась нулевая гипотеза, ведь если продолжительности триала не влияет на коверсию, значит мы можем поставить меньший триал, а значит пользователи будут быстрее конвертироваться в платящих.*

Определяем уровень достоверности. Пусть будет 95%, это значит, что уровень значимости должен быть 0,05. <br />

Нам понадобится две группы <br />
А - контрольная <br />
В - тестовая <br />

Принадлежность группе - независимая переменная  <br />
Конверсия - зависимая переменная (то, на что мы хотим влиять) <br />

## Выбор размера выборки

От размера выборки зависит надежность и точность расчетов. По идее, чем больше, тем лучше. Но мы всегда находимся в условиях ограничений, в первую очередь временных. Поэтому нам важно определить минимальное количество людей в группе, необходимых для получения надежных результатов. 

Для определения размера выборок используется анализ мощности. <br />

#### Мощность зависит от нескольких факторов: 

* Мощность теста (1 - β) — это вероятность обнаружения статистической разницы между группами, когда разница действительно присутствует. Чаще всего мощность устанавливают равной 0,8.
* Уровень значимости альфа (α) — критическое значение. Чаще всего устанавливают 0,05 или 0,01. В нашем случае будет 0,05
* Ожидаемый эффект - разница между текущим коэффициентом конверсии и тем, которого мы хотели бы получить в результате изменений.

#### То есть нам нужно ответить на два вопроса:
* Какой коэффициент конверсии сейчас (12,5%)
* Какой ожидаемый эффект будет после внесения изменения. *Партнер считает, что произойдет ухудшение конврсии как минимум на 3%, мы же считаем, что никаких изменений не будет и верна H0.*

