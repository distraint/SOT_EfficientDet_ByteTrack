# Single Object Tracking with EfficientDet and BYTETracker

## Описание

Этот проект представляет собой систему трекинга автомобиля в видеопотоке с использованием нейросетевой архитектуры EfficientDet для обнаружения объекта и алгоритма BYTETracker для его отслеживания. Тестирование системы было выполнено с использованием двух видео в разном разрешении, а также следующих моделей нейросети: tf_efficientdet_lite1, tf_efficientdet_lite2, tf_efficientdet_lite3 и tf_efficientdet_lite3x.

## Основные этапы работы трекера

1. **Инициализация**:
   - Создание экземпляра модели EfficientDet и загрузка предварительно обученных весов.
   - Инициализация трекера BYTETracker.

3. **Преобразование изображения**:
   - Изменение размера и дополнение изображения для соответствия требованиям модели.

4. **Детектирование**:
   - Обработка изображения с помощью модели EfficientDet для получения bounding box'ов и оценок вероятностей объектов.
   - Фильтрация оценок детекций по порогу уверенности и выбор одной с максимальной оценкой.

5. **Отслеживание**:
   - Обновление трекера с новой детекцией.

6. **Визуализация**:
   - Отображение на оригинальном изображении идентификатора трека и рамки  вокруг отслеживаемого объекта.

7. **Анализ результатов**:
   - Подсчет и вывод средней оценки детекций, FPS, количества треков (для проверки единственности) и суммарной длины треков в кадрах.

## Демонстрация результатов

Видео red_car_360x640.mp4, модель tf_efficientdet_lite3x:
</br></br>[![Watch the video](https://img.youtube.com/vi/wf9_lemPlVo/hqdefault.jpg)](https://www.youtube.com/watch?v=wf9_lemPlVo)

Видео black_car_360x640.mp4, модель tf_efficientdet_lite3x:
</br></br>[![Watch the video](https://img.youtube.com/vi/wHlWy0dvyQo/hqdefault.jpg)](https://www.youtube.com/watch?v=wHlWy0dvyQo)

## Ссылка на Colab
   https://colab.research.google.com/drive/1XYXmMWLpd3IO2rtd9iF7n2eO4DxiUyTr#scrollTo=Lt-44kHrH1yO
   
## Использованные источники
-   https://blog.roboflow.com/top-object-tracking-software/
-   https://www.hitechbpo.com/blog/top-object-detection-models.php
-   https://vc.ru/dev/656805-top-5-metodov-trekinga-obektov?ysclid=lysmi6hk4w673224911
-   https://habr.com/ru/articles/503766/
-   https://github.com/ifzhang/ByteTrack
      -   https://arxiv.org/pdf/2110.06864
-   https://github.com/rwightman/efficientdet-pytorch
      -   https://arxiv.org/pdf/1911.09070
-   https://medium.com/tech-blogs-by-nest-digital/object-tracking-object-detection-tracking-using-bytetrack-0aafe924d292
-   https://www.ikomia.ai/blog/bytetrack-multi-object-tracking#:~:text=At%20its%20core%2C%20ByteTrack%20transcends%20traditional%20tracking%20methods,handling%20scenarios%20that%20would%20confound%20conventional%20tracking%20systems
-   https://blog.roboflow.com/yolov3-versus-efficientdet-for-state-of-the-art-object-detection/
-   https://medium.com/suitable-ryans-thoughts/yolov8-vs-efficientdet-a-deep-dive-into-the-future-of-real-time-object-detection-code-at-bottom-86513de2f69d
