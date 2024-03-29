# `Типы и характеристики физических сетей Ethernet`


### Цель задания

1. Выбрать верные патч-корды  под конкретные передатчики.
2. Применить алгоритмы диагностики инцидентов на физических линиях связи.

### Задание 1. 

Cкоммутировать между собой 10Gbit\s порты коммутаторов SW_1 и SW_2.

- Коммутаторы расположены в соседних стойках, расстояние по прямой между ними 1 метр.
- В порты установлены SFP+ SR  MM 850nm

Вопрос: какой патч-корд выбрать, чтобы выполнить задачу?
Укажите все характеристики патч-корда: тип, длину, форму коннекторов, класс и вид ОВ.

*Приведите ответ в свободной форме.*

---
# Ответ:

- `Тип` - Дуплексный многомодовый ОВ пачкорд;
- `Длина` - C учётом оккуратной прокладки, может потребоваться от 5 до 10 метров;
-`форму коннекторов` - Для SFP+ SR  MM 850nm потребуется дуплексный LC коннектор;
- `класса` - `OM3` с сердечником 50/125 (оранжевые патч-корды применять в системах со скоростями 1 Gbit\s, на 10–15 метров можно и в 10Gbit\s);
- `вид ОВ`- Многомодовое волокно.
### Задание 2

При коммутации медных FastEthernet портов коммутаторов линк согласуется только в 10Mbit\s. Длина линии немного больше 100 метров. 

Почему скорость не поднимается выше 10Mbit\s? Что нужно изменить, чтобы линки поднялись на 100Mbit\s? 

*Приведите ответ в свободной форме.*

---
# Ответ
Могу предположить, что так сильно упасть скорость при указанной длине не может, скорее это связано с повреждением пачкорда или его неправильно обжали.
Что нужно сделать: 
1. Проверить тип кабеля и его качество, возможно, используется Cat5, данный кабель может передавать 100Mbit\s, но при очень малой длине, если это так, то стоит заменить на CAT5e или вовсе на CAT6, если все ок, пункт ниже. 
2. Если дело не в качестве кабеля, то требуется проверить целостность линии, посмотреть с помощью тестера на оборудовании или ручным, нет ли обрыва жилы, если есть по переобжать, если не помогло, то осмотреть визуально укладку, заменить пачкорд по необходимости. 
3. Для идеального решения проблемы, следует заменить пачкорд, сократив его длину хотя бы до 90 метров,  например установив `repeater`-повторитель, тем самым мы сохраним сигнал на требуемом уровне.  


