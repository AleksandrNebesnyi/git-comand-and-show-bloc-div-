git clone адрес репозитория - клонировать репозиторий на локальный компютер
git commit -m 'initial commit' комит изменений в локальный репозиторий
git push -u origin master - только первый раз отправка изменений в удаленный репозиторий
git push - все последующие разы отправка изменений в удаленный репозиторий


окат изменений
git pull - скачивается актуальная версия удаленного репозитория и все изменения применяются к локальному репозиторию
checkout - перейти в другую ветку
discard - не отправлять в репозиторий те изменения которые нам не нравятся
revert - откатить существующие комиты
hard reset -откатить целую пачку комитов


работа с ветками
merge - сначала подтягиваем в свою ветку из master все изменения
merge - потом тестируем и делаем слияние переходим (checkout) в master и применяем (merge) все изменения из нашей ветки


git commit -a -m 'commit all edited files' закомитить все измененные файлы безиспользования команды git add
git clone - скачивание репозитория 
git status - просмотр текущих изменений 
git add - добавить файл в локальный репозиторий 
git commit - коммит в локальный репозиторий 
git push - коммит в удаленный репозиторий


В консольном git можно указать настройки сетевого подключения. Прокси, порты, аутентификацию.
git config --global http.proxy http://proxyuser:proxypwd@proxy.server.com:8080 
(указываем ваши креденшлс, если есть, прокси-сервер и порт)


Работа с ветками
git branch -a  посмотреть в какой ветке мы находимся и показать все ветки ключ -а   all
git branch newbranch  - создать новую ветку с именем newbranch
git checkout newbranch - перейти в новую ветку
git push origin newbranch -  (сначала переключиться на мастер) отправить в удаленный репозиторий ветку newbranch
git branch -d newbranch - удалить ветку newbranch из локального репозитория 
git push origin --delete newbranch - удалить ветку newbranch в удаленном репозитории

Работа с версиями программы
1. Разработку лучше вести не в ветке master, 
   а в другой ветке, например, develop, новые функции программы ветвить от develop, 
   тестить и фиксить в develop, и только когда код отлажен до какой-то стабильной версии программы, 
   сливать изменения в master. 
2. При этом удобно добавить тэг с номером версии и изменениями что допилили в этой версии (release notes). 
3. По тэгу легко найти нужную версию в логе, 
   и можно по этому коммиту (вообще можно по любому коммиту) 
   воссоздать в отдельной ветке состояние программы в этой версии.
   
api/get-temperature-value
feature/select2-ibrary-added
fix/incorrect-users-sorting-fixed
т.е. принцип: "чем является доработка" / "что именно доработано".



Показ скрытого блока

HTML
<div class="container">
			<p
				>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Unde eligendi commodi ipsam animi numquam vitae,
				saepe voluptates quod praesentium quibusdam. Lorem, ipsum dolor sit amet consectetur adipisicing elit. Tempore
				inventore, id non ratione voluptatem architecto quae quam sequi hic! Voluptate, quas. Explicabo expedita modi
				vel omnis laudantium quasi repellendus error.
			</p>
			<input type="checkbox" id="read-more" hidden />
			<p class="extra-text"
				>Lorem ipsum dolor sit amet consectetur adipisicing elit. Quas sed nihil provident corporis cum numquam
				accusamus. Dignissimos, dolores vitae voluptate, quam, neque provident impedit suscipit molestiae facilis
				dolorum fugit deleniti.</p
			>
			<label for="read-more" class="read-more">Read <span class="more">more</span><span class="less">less</span></label>
		</div>
    
    
    CSS
    
    .read-more {
	border: 1px solid black;
	padding: 10px 30px;
	max-width: 200px;
}
.read-less {
	display: none;
}
p {
	margin: 20px 0;
}
.extra-text {
	display: none;
}
#read-more:checked ~ .extra-text {
	display: block;
}
.less {
	display: none;
}
#read-more:checked ~ .read-more .more {
	display: none;
}
#read-more:checked ~ .read-more .less {
	display: inline;
}
    
    
    


