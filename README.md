# SearchServer
# Учебный проект курса Яндекс Практикума "Разработчик С++"
Обеспечивает поиск документов по ключевым словам и ранжирование результатов по статистической мере TF-IDF. Поддерживает функциональность минус-слов и стоп-слов. Создание и обработка очереди запросов. Возможность работы в многопоточном режиме.

# Принцип работы
Создание экземпляра класса SearchServer. В конструктор передаётся строка с стоп-словами, разделенными пробелами. Вместо строки можно передавать произвольный контейнер (с последовательным доступом к элементам с возможностью использования в for-range цикле)

С помощью метода AddDocument добавляются документы для поиска. В метод передаётся id документа, статус, рейтинг, и сам документ в формате строки.

Метод FindTopDocuments возвращает вектор документов, согласно соответствию переданным ключевым словам. Результаты отсортированы по статистической мере TF-IDF. Возможна дополнительная фильтрация документов по id, статусу и рейтингу. Метод реализован как в однопоточной так и в многпоточной версии.

Класс RequestQueue реализует очередь запросов к поисковому серверу с сохранением результатов поиска.

# Сборка и установка
Сборка с помощью любого IDE либо сборка из командной строки

# Системные требования
Компилятор С++ с поддержкой стандарта C++17 или новее
