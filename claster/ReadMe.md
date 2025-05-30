# Кластеризация изображений котиков

В этом проекте мы исследуем возможность кластеризации изображений котиков с использованием различных методов. Датасет состоит из изображений котиков размером 64x64 пикселя, и мы будем использовать методы понижения размерности и кластеризации, такие как PCA и KMeans.

## Описание данных
Данные содержат изображения котиков в формате PNG, расположенные в папке `cats`. Мы загружаем все изображения, преобразуем их в одномерные векторы и визуализируем несколько примеров.



## 1. Свойства метрики в пространстве котиков
Исследуем, существует ли проблема проклятия размерности в пространстве изображений котиков. Для этого выбираем случайные пары изображений, рассчитываем расстояния между ними и визуализируем KDE-оценку плотности нормированных расстояний.

Затем применяем PCA для различных чисел компонент (30, 100, 500) и анализируем изменения в распределении расстояний.



После применения PCA с различным числом компонент можно наблюдать, что с увеличением числа компонент дисперсия распределения расстояний уменьшается, что свидетельствует о снижении размерности пространства и возможной помощи в устранении проблемы проклятия размерности.

## 2. Кластеризация котиков по вектору изображения
Для начала кластеризуем изображения с помощью метода KMeans, преобразовав каждое изображение в одномерный вектор.



Затем проецируем изображения на 2D-плоскость с помощью PCA и визуализируем результаты кластеризации.



Визуализация позволяет увидеть, как изображения сгруппированы в кластеры, и получить представление о различиях между ними. Также мы выводим изображения, наиболее характерные для каждого кластера.

## 3. PCA + кластеризация
Для улучшения кластеризации перед применением KMeans применяем PCA с 100 компонентами, чтобы снизить размерность и улучшить качество кластеризации.


Визуализируем полученные кластеры на плоскости PCA и рисуем типичные изображения для каждого кластера.

## Выводы
Мы наблюдаем, что при кластеризации котиков выделяются несколько кластеров с различными особенностями: например, рыжие котики, белые котики, черные котики и т.д. Применение PCA помогает уменьшить размерность и улучшить результаты кластеризации, снижая влияние проблемы проклятия размерности.
