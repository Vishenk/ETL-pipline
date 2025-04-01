# Решаемые задачи: 
1. Построение физической модели данных на основе информации об источниках данных. 
2. Построение хранилища данных. 
3. Разработка процессов обновления распределенных данных при использовании Apache Spark.
## Описание входных и выходных данных
Источники содержатся в папке sources (их excel версии в папке sources_excel). Всего 3 источника, 2 из которых в формате SCD1 и обновляются один раз в конце месяца, 1 - в формате SCD2.  
Описание конечных таблиц представлено ER-диаграммой, процесс забора и очистки данных представлен BPMN-диаграммой.  

В папке support&results (их excel версии в папке support&results_excel) хранятся следующие файлы конечных таблиц:
1. client_attribute - информация обо всех атрибутах клиента, которые несут в себе бизнес-смысл (название, краткое описание, частота обновления источников, тип данных). 
2. sources - информация об источниках (название, краткое описание, частота обновления, колонка партиционирования). 
3. monthly_report - aтрибуты, которые обновляются раз в месяц. При этом формат представления вертикальный, а формат хранения SCD1. 
4. daily_report - aтрибуты, которые обновляются каждый день. При этом формат представления вертикальный, а формат хранения SCD2. 
5. updates- информация об обновлениях атриббутов клиента (атрибут, источник, дата обновления атрибута по источнику).
