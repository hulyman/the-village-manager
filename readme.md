Первое задание.
a. (Если человек знаком со флешем). Есть анимация во флеше (test_anim.fla). Нужно перевести ее в анимацию Unity.
б. (Если человек не знаком со флешем). Есть набор ресурсов для анимации (Timer.png, Timer.png.meta). Необходимо сделать анимацию по аналогии с предоставленным test_anim.swf.
Описание анимации:
TimerSunMoon движется справа налево под статической маской (TimerMask).
Поверх него лежит TimerSunLight (статический), показываемой под маской (TimerLightMask), которая движется справа налево (синхронно с TimerSunMoon).
Анимация должна быть зацикленная (солнце-луна-солнце-луна-...).

Второе задание.
Придумать подход и написать классы которые позволяли ли бы реализовать производственную цепочку.

Допустим в игре есть 4 вида зданий:

Добывающее предприятие

Перерабатывающее предприятие

Склад

Ратуша


Добывающее предприятие 

Добывает N1 единиц ресурса A за промежуток времени T1.

После цикла производства Добывающее предприятие отправляет ресурс A на склад, если есть такая возможность (хотя бы один склад работает и на этом складе есть место). Если отправить на склад невозможно - добыча новых ресурсов прекращается в ожидании пока текущие ресурсы не будут переправлены на склад.

Добывающее предприятие потребляет (на зарплату рабочим) L1 единиц золота из Ратуши за промежуток времени T2, даже если простаивает из-за невозможности передать ресурсы на склад. Если золото своевременно не получено - производство ставится на паузу до тех пор, пока не будет получено золото.

Имеет цену строительства C1.


Перерабатывающее предприятие потребляет N2 единиц ресурса A с любого из складов и производит N3 единиц ресурса B за промежуток времени T3.

Цикл производства не может быть запущен до тех пор, пока предприятие не получит необходимое количество необходимого ресурса с любого из складов.

После цикла производства Перерабатывающее предприятие продает произведенный ресурс B по цене L2 за единицу (ресурс изымается из игры а золото добавляется в ратушу).

Перерабатывающее предприятие потребляет (на зарплату рабочим) L3 единиц золота из Ратуши за промежуток времени T4, даже если простаивает из-за отсутствия нужного ресурса на складе. Если золото не получено - переработка ставится на паузу до тех пор, пока не будет получено золото.

Имеет цену строительства C2.


Склад может содержать M единиц любых ресурсов. 

Склад  потребляет (на зарплату рабочим) L4 единиц золота из Ратуши за промежуток времени T5. Если золото не получено - склад перестает принимать и передавать ресурсы.

Имеет цену строительства C3.


Ратуша хранит в себе золото и отправляет золото в том количестве в котором нужно каждому из предприятий. Так же золото может быть использовано на строительство новых предприятий и складов. Ратуша может быть только одна.


Следует предусмотреть:

Данные всех показателей всех зданий должны получаться из текстового файла с конфигурацией. 

Предложите структуру и набор необходимых параметров благодаря которым в дальнейшем гейм-дизайнер сможет без участия программиста заводить новые здания, ресурсы и производственные цепочки.

Вас не должна беспокоить визуальная реализация, только техническая. Игра может представлять собой набор серых кубов в пространстве или кнопок на Canvas
