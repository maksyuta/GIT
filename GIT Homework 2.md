1. На локальном репозитории сделать ветки для:
- Postman
- Jmeter
- CheckLists
- Bag Reports
- SQL
- Charles
- Mobile testing
```bash
git branch Postman
git branch Jmeter
git branch Checklists
git branch Bug Reports
git branch SQL
git branch Charles
git branch Mobile_testing
```

2. Запушить все ветки на внешний репозиторий
```bash
git push -u origin all
```
3. В ветке Bag Reports сделать текстовый документ со структурой баг репорта
```bash
git checkout Bug_Reports
touch bug_report.txt
vim bug_report.txt
Press button "i"

 1 - ID - Уникальный идентификационный номер
 2 - Environment - Окружение 
 3 - Module - Компонент/модуль/юнит, в котором обнаружен дефект
 4 - Project - Название проекта
 5 - Build - Версия сборки
 6 - Summary/Title - Что? Где? Когда?
 7 - STR - Шаги воспроизведения
 8 - Actual Result - Фактический результат
 9 - Expected Result - Ожидаемый результат
 10 - Severity - Критичность бага по степени влияния на продукт
 11 - Priority - Критичность бага по степени влияния на бизнес
 12 - Status - Статус бага в жизненном цикле бага
 13 - Author - Тот, кто нашёл баг
 14 - Assigned to - Назначен
 15 - Attachments - Логи/скриншоты/видео
 
 Esc
 :wq
```
4. Запушить структуру багрепорта на внешний репозиторий
```bash
git add bug_report.txt
git commit -m bug_report.txt
git push
```
5. Вмержить ветку Bag Reports в Main
```bash
git checkout main
git merge Bug_Reports
```
6. Запушить main на внешний репозиторий.
```bash
git push
```
7. В ветке CheckLists набросать структуру чек листа.
```bash
git checkout CheckLists
touch checklist.txt
vim checklist.txt
Press button "i"

Check list ID
Check list summary
Status
Tester
Test date
Comment

Esc
:wq
```
8. Запушить структуру на внешний репозиторий
```bash
git add checklist.txt
git commit -m "add new filt checklist.txt"
git push
```
9. На внешнем репозитории сделать Pull Request ветки CheckLists в main
```
1. Нажать кнопку "Compare & pull request"
2. Нажать "create pull request"
3. После проверки нажать "Merge pull request"
4. Нажать "Confirm merge"
5. После слияния веток должно быть указано Pull request successfull merged and closed.
```
10. Синхронизировать Внешнюю и Локальную ветки Main
```bash
git checkout main
git pull
```
