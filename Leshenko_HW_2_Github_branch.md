1. На локальном репозитории сделать ветки для:
- Postman - `git branch Postman`
- Jmeter - `git branch Jmeter`
- CheckLists - `git branch CheckLists`
- Bug Reports - `git branch Bug_Reports`
- SQL - `git branch SQL`
- Charles - `git branch Charles`
- Mobile testing - `git branch Mobile_testing`

2. Запушить все ветки на внешний репозиторий - `git push --all`
3. В ветке Bug Reports сделать текстовый документ со структурой баг репорта - 
`git checkout Bug_Reports ; cat > bug_report_1.txt`
    - Summary:[9] button it always is disable on panel of calculator however digits 9 can enter from keyboard
    - Descriprion: When calculator is run button always is disable on panel of calculator however digits 9 can enter from keyboard. It is unfriendly behavior for users
    - Actual result: [9] button is disable
    - Expected result: [9] button is enable
    - Reproduced on: Win 7
    - Reproducibility: always
    - For more details see attachment: `https://yadi.sk/i/4IBhTrDF3VxXhR`
    - Steps to reproduce:    
	    - 1: Run calc.exe
	    - 2: Click [9] button
    - Severity: minor
    - Priority: low
`Enter` `CTRL+D`

5. Запушить структуру багрепорта на внешний репозиторий - `git add . ; git commit -m "add bug_report_1.txt" ; git push --set-upstream origin Bag_Reports`
6. Вмержить ветку Bug Reports в Main - `git checkout main ; git merge Bug_Reports`
7. Запушить main на внешний репозиторий - `git add . ; git commit -m "merge Bug report to master" ; git push`

9. В ветке CheckLists набросать структуру чек листа - 
`git checkout CheckLists ; cat > cheklist_website.txt`
	+ ID
	+ Title
	+ Precondition
	+ Module
	+ Steps_to_reproduce
	+ Expected_result
	+ Status
`Enter` `CTRL+D`

10. Запушить структуру на внешний репозиторий - ` git add . ; git commit -m "add checklist.txt" ; git push --set-upstream origin CheckLists`
11. На внешнем репозитории сделать Pull Request ветки CheckLists в main - Перейти на веб версию github в нужный репозиторий, изменить ветку на Checklists, нажать `Pull Request`
12. Синхронизировать Внешнюю и Локальную ветки Main - `git checkout main ; git pull`
