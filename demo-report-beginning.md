---
figureTitle: Рисунок
tableTitle: Таблица
tableEqns: true
titleDelim: "&nbsp;–"
link-citations: true
linkReferences: true
chapters: true
...

# [Список исполнителей]{custom-style="UnnumberedHeadingOneNoTOC"} {.unnumbered}


 -------------------------------------------    --------------------------------------------------------------------  ---------------------------
 [Студент]{custom-style="ContributorsTable"}    \_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_   Д. А. Зубарев  
 
 Студент                                        \_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_   Н. Е. Копылов
 
 Студент                                        \_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_   Н. А. Калиман

 Студент                                        \_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_   Н. А. Перминов

 Студент                                        \_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_   Е. А. Рудакова 

--------------------------------------------------------------------------------


<!-- # [Реферат]{custom-style="UnnumberedHeadingOneNoTOC"} {#referat .unnumbered}

Отчёт %NPAGES% с., %NFIGURES% рис., %NTABLES% табл., %NREFERENCES% источн., %NAPPENDICES% прил.

::: {custom-style="GostKeywords"}
Информационная система,
система учета проектов и задач работников,
бизнес-логика,
UML
:::
 
Целью построения данной работы является изучение основных элементов диаграммы последовательностей, создание диаграммы последовательностей, а также получение навыков по построению данного типа диаграмм. 

По результатам работы составлен данный отчёт, состоящий из введения, заключения
и %NCHAPTERS% глав.
 -->
<!-- Все вышеперечисленные числовые показатели проставлены скриптом постобработки,
т.е.\ не вручную. Изящно решена проблема согласования падежей числительных
и\ существительных: для количества страниц, рисунков, источников и приложений
соответствующие существительные даны в сокращённой форме; существующее написание
«глав» подойдёт к любому количеству от 2 до 20 включительно. -->

# [Содержание]{custom-style="UnnumberedHeadingOneNoTOC"} {.unnumbered}

%TOC%

<!-- # [Обозначения и сокращения]{custom-style="UnnumberedHeadingOneNoTOC"} {.unnumbered}

|    |     |    |
|:---|:---:|:---|
| [ИС]{custom-style="AbbreviationsTable"} | --- | Информационная система |
| ЛР | --- | Лабораторная работа |
| ПЗ | --- | Практическое занятие |
| ПрО | --- | Предметная область | -->
<!-- | Своя задача | --- | Задача, назначенная текущему сотруднику |
| Свой проект | --- | Проект, содержащий хотя бы одну задачу текущего сотрудника | -->
<!-- | [Время отклика]{custom-style="AbbreviationsTable"} | --- | время, необходимое для выполнения операций |
| Высокая производительность | --- | обеспечение работы системы с временем отклика, отвечающим требованиям производства |
| Одновременные запросы | --- | единовременная обработка запросов от нескольких пользователей |
| Масштабируемость | --- | это способность системы увеличивать свою производительность и способность обрабатывать больше задач или пользователей без серьезных проблем или ухудшения работы |
| Доступность информационной системы | --- | это способность этой системы быть доступной и работоспособной в любое время, когда пользователи в ней нуждаются |
| Интуитивно понятный интерфейс | --- | интерфейс, которым потенциальный пользователь может пользоваться без изучения документации |
| Восстановление системы | --- | процедура восстановления данных после сбоев или потери данных |
| Совместимость | --- | возможность работы системы с другими техническими средствами и программным обеспечением предприятия |
| Модель данных | --- | структура данных, включающая сущности и их атрибуты |
| Требования к хранению данных | --- | правила и стандарты хранения данных согласно классу информационной безопасности | -->
<!-- | Административным функциям | --- | просмотр списка всех задач, создание новой задачи, удаление и редактирование всех существующих задач | -->
<!-- | Действие "Войти" | --- | выполнить набор действий, необходимых для выполнения входа в систему | -->
 
<!-- | [ГОСТ]{custom-style="AbbreviationsTable"} | --- | Государственный стандарт |
| ИПН\ ГПНД | --- | Институт прикладных наук о ГОСТах в области программной и научной документации |
| НИР | --- | Научно-исследовательская работа | -->

<!-- # [Введение]{custom-style="UnnumberedHeadingOne"} {.unnumbered}

В этом отчёте рассматривается информационная система "TaskMaster", созданная на основе описания представленного ниже.
На основе построенных ранее диаграммы прецедентов, диаграмм активностей, диаграммы понятий и описанию прецедентов, выполненных ранее при выполнении ЛР №1-2 и ПЗ №1-4 построим диаграммы последовательности. 

Далее представлено описание информационной системы в соответствии с предоставленной темой под номером 5 в [@temat].

ИС управления задачами предприятия. О каждой задаче известно: название задачи, дата запуска (может быть не задана, если задачи еще не запущена), дата остановки (дата остановки обязательно позже даты запуска и не может быть установлена, если дата запуска не задана), приоритет (целое число, влияет на порядок сортировки задач), имя сотрудника, название проекта, описание задачи. Администратор может просматривать списки задач, создавать новые задачи, удалять и редактировать существующие задачи. Сотрудник может видеть только свои задачи, может создавать задачи для себя и редактировать свои задачи. Сотрудник может запустить или остановить свою задачу. Сотрудник может работать над задачами из большого количества различных проектов.
 -->
<!-- Это пример научно-технического отчёта, оформленного по ГОСТу.
Он существует в двух формах: в виде текстового файла в формате Markdown
и в виде docx-файла (Word 2010+). Всё содержимое документа, кроме
титульной страницы, изначально создано в  Markdown и преобразуется в Word
автоматически, с использованием программ [Pandoc](http://pandoc.org)
и Powershell + COM-объектов Word.
Поставленная цель --- продемонстрировать возможность
создания в\ Markdown программной документации и научно-технических
отчётов для государственных заказчиков.

Далее описаны результаты опытов по созданию ГОСТ-френдли контента
в\ Markdown. Охвачены все основные элементы: простой текст, заголовки, нумерованные
и\ маркированные списки, таблицы, рисунки, формулы, вставки кода,
список литературы.

Простой текст включает также спецсимволы, такие как тире и неразрывные пробелы.
Используемый здесь способ их набора\ --- не единственный. В Markdown
поддерживаются юникодные символы и HTML-разметка.

Предполагается, что ищущий читатель найдёт в этом тексте образцы всего, что ему
потребуется для создания своего текста. Одни вещи делаются простым
и естественным путём (например, разбиение текста на абзацы пустой строкой);
другие требуют специальных приёмов и постобработки (например, этот раздел
«Введение» сделан ненумерованным с помощью
`{custom-style="UnnumberedHeadingOne"}` и\ соответствующей постобработки
в\ Powershell-скрипте). Не пугайтесь, писать на Powershell вам не потребуется
(если, конечно, вы не захотите чего-то особенного). Для создания своих
документов, оформление которых не выходит за установленные рамки, вам достаточно
работать с\ текстом в формате Markdown и\ ещё немного с шаблоном в\ Word,
в\ котором находится титульная страница и стили. -->

<!-- # [Введение]{custom-style="UnnumberedHeadingOne"} {.unnumbered} -->

<!-- Документ «Отчет о пилотном внедрении»  содержит результаты процесса внедрения, которые подтверждают, что разработанное решение соответствует спецификациям и требованиям заказчика. Фактически, успех пилотного внедрения показывает, насколько качественен текущий вариант решения. Как правило, успешное пилотное внедрение является следствием грамотного анализа, планирования и точному следованию проектной документации. В противном случае, мы можем получить отрицательные отзывы, которые потребуют принятия срочных мер. -->

<!-- В данном документе рассматривается внедрение продукта для стартап-компании ООО "ГЭТ Э БЛАНКЕТ",  -->

