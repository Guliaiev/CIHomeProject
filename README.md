## Описание счетчиков покрытия JaCoCo/

1. _Instructions_ (покрытие C0) -
   Покрытие Instructions предоставляет информацию об объеме кода, 
   который был выполнен или пропущен.
2. _Branches_ (покрытие C1) - 
   Эта метрика подсчитывает общее количество
    ветвей в методе и определяет количество выполненных или пропущенных ветвей. Покрытие веток всегда доступно,
   даже при отсутствии отладочной информации в файлах классов. Если файлы классов были скомпилированы с отладочной информацией, точки принятия решения могут быть сопоставлены 
   с исходными строками и выделены соответствующим образом:

* Нет покрытия: нет ответвлений в линии (красный ромб)
* Частичное покрытие: выполнена только часть ветвей в линии (желтый ромб)
 * Полное покрытие: Все ответвления в линии выполнены (зеленый ромб)
3. _Line_ - Для всех файлов классов, которые были скомпилированы с отладочной информацией, можно рассчитать информацию о покрытии для отдельных строк. Исходная строка считается выполненной, если 
   была выполнена хотя бы одна инструкция, назначенная этой строке.
   В зависимости от форматирования исходного кода одна строка исходного кода может относиться к нескольким методам или нескольким классам. Следовательно, количество строк методов нельзя просто сложить, чтобы получить общее количество для содержащего класса. То же самое верно и для строк нескольких классов в одном исходном файле. JaCoCo рассчитывает покрытие строк для классов и исходного файла на основе фактически охваченных строк исходного кода.
4. _Cyclomatic Complexity_ - Вычисляет цикломатическую сложность для каждого неабстрактного метода и суммирует
   сложность для классов, пакетов и групп.Цикломатическая сложность - это минимальное количество путей, которые могут в (линейной) комбинации генерировать все возможные пути с помощью метода. Таким образом, значение сложности может служить индикатором количества примеров модульного тестирования,
   которые полностью охватывают определенную часть программного обеспечения. Показатели сложности всегда можно рассчитать, даже при отсутствии отладочной информации в файлах классов.
  + В проекте  выбран для покрытия тестов счётчик BRANCH, так как он  отображает покрытие всех сценариев тестов, соответственно даёт возможность визуально вычислить лишний/некорректный код и исправить его добившись нужного процента покрытия кода.
