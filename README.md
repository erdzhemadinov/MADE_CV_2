# MADE_CV_2
The second task of CV MADE course.


Идея:

Решение состояло из нескольких этапов. 

Для начала выбросил из трейна странную разметку. 

Далее детектировался номер. Использовалась fasterrcnn_resnet50_fpn. Изначально пробовал сегментировать номера, но на выходе получались такие же сегментированные области, как и bounding box'ы, не отличавшиеся от них. 

Optimizer Adam. Использовался sheduler. Сеть обучалась три эпохи.

Первая часть основана на туториале. https://pytorch.org/tutorials/intermediate/torchvision_tutorial.html

Вторая часть извлекака номера из bounding box'ов. Основала на кернеле 9-ого семинара с некоторыми модификациями. 
Проверял номера на соотвествие паттерну автомобильного номера, если соответствовали, добавлял к выводу. Обучал сеть 8 эпох.

Прикрепил кернел на всякий случай.

Конечное решешение получалось брендом двух решений следующим образом. Если в первом решении у какого-либо изображения не было номера, оно добавлялось из второго (небольшая модификация первого кернела). 
