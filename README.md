# Переводчик с английского на русский язык.
# $\textcolor{blue}{Постановка\ задачи}$
## Создание нейросети для перевода с английского на русский язык, с использованием языка Pytorch
# $\textcolor{blue}{Цель}$
## Упростить ежедневные задачи при работе с англоязычным текстом.
# $\textcolor{blue}{Задачи}$
## Получение базы с сайта
## Небольшой прасинг базы 
## Параметризация базы (токенизация, тензоры)
## Создание нейросети на основе Transformer (Attention all you need)
## Обучение нейросети
## Проверка нейросети
# $\textcolor{blue}{Обучающая\ база}$
## База взята с сайта http://www.manythings.org/anki
![alt text](https://github.com/Denis799/project_translator/blob/master/images/10.jpg?raw=true)
# $\textcolor{blue}{Этапы\ обработки\ базы}$
## Небольшой парсинг базы – это чистка базы, для получения пары слов или пары предложений англ. – русс.
## Токенизация текста  для разделения предложений на слова.
## Преобразование слов в индексы.
## Преобразование индексов в тензоры
# $\textcolor{blue}{Очистка\ и\ токенизация}$
### Так выглядит pandas таблица после получения базы
![alt text](https://github.com/Denis799/project_translator/blob/master/images/13.jpg?raw=true)
### Очистка
![alt text](https://github.com/Denis799/project_translator/blob/master/images/14.jpg?raw=true)
### Токенизация
![alt text](https://github.com/Denis799/project_translator/blob/master/images/15.jpg?raw=true)
# $\textcolor{blue}{Инструменты}$
## Для очистки базы использовалась библиотека pandas путем слайсинга, так же используется библиотека регулярных выражений “re”, что бы убрать лишние символы
![alt text](https://github.com/Denis799/project_translator/blob/master/images/16.jpg?raw=true)
## С помощью инструмента “get_tokenizer”, тот что импортируем из библиотеки “torchtext.data.utils”, мы разбиваем предложения на слова. Данный инструмент разбивает не только на слова, но и на знаки препинания
![alt text](https://github.com/Denis799/project_translator/blob/master/images/17.jpg?raw=true)
## Библиотека spacy в совокупности с “en_core_web_sm”(для анг.) и “ru_core_news_sm”(для русс.) дает нам возможность правильного чтения предложений на двух языках при их разбивки на слова.
## Инструмент “build_vocab_from_iterator”, тот что импортируется из библиотеки “torchtext.vocab”, превращает слова в индексы
![alt text](https://github.com/Denis799/project_translator/blob/master/images/18.jpg?raw=true)
## Библиотека “torch” позволяет нам преобразовать полученные индексы в тензоры, которые мы будем подавать в нейросеть
![alt text](https://github.com/Denis799/project_translator/blob/master/images/19.jpg?raw=true)
# $\textcolor{blue}{Графики\ подготовленной\ базы}$
![alt text](https://github.com/Denis799/project_translator/blob/master/images/20.jpg?raw=true)
![alt text](https://github.com/Denis799/project_translator/blob/master/images/43.jpg?raw=true)
![alt text](https://github.com/Denis799/project_translator/blob/master/images/44.jpg?raw=true)
# $\textcolor{blue}{Метрики,\ Loss,\ функции оценки}$
![alt text](https://github.com/Denis799/project_translator/blob/master/images/45.jpg?raw=true)
# $\textcolor{blue}{Оценка\ точности\ модели}$
![alt text](https://github.com/Denis799/project_translator/blob/master/images/46.jpg?raw=true)
# $\textcolor{blue}{Демонстрация\ этапов\ распознавания}$
![alt text](https://github.com/Denis799/project_translator/blob/master/images/47.jpg?raw=true)
![alt text](https://github.com/Denis799/project_translator/blob/master/images/48.jpg?raw=true)
