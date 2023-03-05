# Исследование JVM через VisualVM
### 1) Вывод консоли после завершения программы. Пронумерован для сопоставления на графиках VisualVM
![](/console.JPG)
### 2) График Metaspace с размеченными на таймлайне номерами строк, которые вывела консоль
![](/metaspace.JPG)
### 3) График Heap с размеченными на таймлайне номерами строк, которые вывела консоль
![](/heap.JPG)
### 4) График Classes с размеченными на таймлайне номерами строк, которые вывела консоль
![](/classes.JPG)
### Выводы: 
исследование JVM через VisualVM подтвердило, что при загрузке классов увеличивается 
используемая память Metaspace, также была замечена загрузка служебных классов.
При загрузке объектов расходуется память в куче, которая при включении сборщика мусора 
частично освобождается. Также замечена синхронность всех графиков, так как загрузка классов 
и объектов сразу отражается в соответствующих областях памяти Metaspace и Heap.
