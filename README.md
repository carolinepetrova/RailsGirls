# RailsGirls

## Конзола (Терминал)
Основни понятия и команди за създаване на файлове/директории и придвижване по файловото дърво

### Абсолютен / относителен път 
**Aбсолютен път** - този път, който започва от коренната директория, която се обозначава с / (МаcOS/Linux) или с буквата на диска и двоеточие за Windows (примерно C: D: ...)

**Относителен път** -  ОС счита, че пътя започва от текущата директория (тази в която се намираме в момента). Например ако имаме директорията home, в нея имаме директориите dir1 dir2 dir3 и сме в /home/dir1, за да преминем от dir1 в dir3 чрез `cd ../dir3`

### Директории 
- `.` - текуща директория
- `..` - родителска директория на текущата директория
- `~` - началната ни директория 
- `pwd` - показва абсолютния път на директорията, в която се намираме

### Придвижване из директориите
`cd [относителен/абсолютен път на директорията]`

Упражнете:
- `cd .`
- `cd ..`
- `cd ~`

### Показване на файловете в директория
`ls [опция]` 

Главни опции: 
- `ls -a` - показва скритите файлове
- `ls -l` - показва детайлна информация за всеки файл 
- `ls -h` - показва информацията във "Human Readable Format"

Moжем да ги комбинираме:
- `ls -al`
- `ls -lh`

Какво ще изведат тези две команди?

### Създаване на файл/директория
- `touch file.txt` - създава празен файл **file.txt** в текущата директория
- `tee file.txt` - създава празен файл **file.txt** в текущата директория и веднага след това ни дава да пишем в него 
- `mkdir dir1` - създава директория в текущата директория
- `mkdir [oтносителен или абсолютен път]/dir1` - създава директорията там, където сме и указали чрез относителен/абсолютен път

### Действия с файлове
- `cp [файл] [път до директория]` - копира файла в друга директория
- `cp [файл] [друго име на файл]` - прави копие на файла в текущата директория
- `mv [файл] [друго име на файл]` - преименува файла
- `mv [файл] [път до директория]` - премества файла в указаната директория

### Изтриване на файл/директория
- `rmdir [име на директория]` - изтрива директория ако е празна
- `rm [име на файл]` - изтрива файл
- `rm -r [директория]` - изтрива директория и всичкото съдържание в нея

## HTML 
### Структура на HTML документа
- `<html></html>` - създава HTML документа
- `<head></<head>` - тук се слагат таговете, чиято информация не се показва (например информация за самата страница)
- `<body></body>` - тук се слага всичко, което се изобразява на монитора

Пример: 
```html
<!--Чрез DOCTYPE уеб браузърът узнава как трябва да интерпретира страницата, като взима предвид версията на използвания език-->
<!DOCTYPE html> 
<html>
    <head>
        <!-- чрез <meta charset> се указва на какъв език е написан html документа -->
        <meta charset="UTF-8">
        <title>Заглавие на страницата</title>
    </head>
    <body>
        <h1>Това е моят сайт</h1>
    </body>
</html>
```
### Основни тагове
#### За текст
- `<h1></h1> ... <h6></h6>` - задават HTML заглавията. h1 е най-голямото, h6 е най-малкото (h* идва от heading)
- `<p></p>` - създава нов параграф (p идва от paragraph)
- `<span></span>` - използват се, за да oбрградят и форматират малки части от текст, снимки и тн
- `<div></div>` - използват се, за да обособят раздели в документ (div идва от divider)
- `<a></a>` - дефинира хиперлинк, използва се главно с атрибута си href: `<a href="URL">some text</a>` (a идва от anchor)
#### Списъци 
- `<ul></ul>` - създават неподреден лист (ul идва от unordered list)
- `<li></li>` - обособява всеки елемент на лист
#### Форми
- `<form></form>` - дефинира форма
- `<input type="TYPE" name=? value=?>` Дефинира поле за въвеждане на текст, където TYPE може да е: 
  - `type="checkbox"` или `type="radio"` - дефинираме отметка
  - `type="text"` - дефинираме поле, в което можем да въведем само едноредов текст
  - `type="email"` - поле, което приема само имейли
  - `type="password"` - поле за пароли
  - `type="date"` - поле за дата
- `<textarea name=? cols="x" rows="y"></textarea>` - дефинира многоредово поле за текст, cols задава широчината му, а rows височината
#### Други
- `<img src="URL" />` - добавяне на изображение
- `<br>` - преминаване на нов ред
- `<hr>` - добавя линия 

Тези тагове са примери за така наречените тагове синглетони. Те нямат нужда да бъдат затваряни, за да са валидни.

#### Упражнение
Направете страница за вас `aboutme.html`, включваща вашите имена, къде учите, с какво се занимавате. Включете ваша снимка. Изброите вашите хобита. Може да включите линкове към социалните ви мрежи. Направете форма за контакт с вас.

## Ruby
Ruby е интерпретируем, обектно-ориентиран език за програмиране. 

## Компилатор vs Интерпретатор
**Компилаторът** превежда кода от програмен език на машинен код и така програмата се изпълнява директно от микропроцесора. Самата компилация се извършва задължително преди нейното изпълнение и по време на компилация се откриват синтактичните грешки.

**Интерпретаторът** е "програма за изпълняване на програми". Той изпълнява командите на програмата една след друга. Поради липса на предварителна компилация, при интерпретируемите езици грешките се откриват по време на изпълнение.

Файловете с Ruby код са с разширение `.rb`

Ruby файловете се изпълняват с командата `ruby name_of_file.rb`

## Работа с данни 
Преди това: 
`irb` - интерактивна конзола, където можем да пишем Ruby код. 
### Числа
Цели числа (Integers) и числа с плаваща запетая (floats)
**Събиране на целочислени числа**
```Ruby
> 1 + 2
=> 3
```
**Събиране на целочислено число с число с плаваща запетая**
```Ruby
> 1.0 + 2
=> 3.0
> 1 + 2.0
=> 3.0
```
**Упражнение**

От какъв тип ще са данните, получени след следните аритметични операции:
- `5 / 2`
- `5 / 2.0`

### Списъци
Имаме следният списък 

`fruits = ["apple", "orange", "pear", "melon"]`

**Достъпване на елемент**
```Ruby
puts fruits[0] # apple
puts fruits[1] # orange
puts fruits[2] # pear
fruits[3] = "watermelon" # променяме melon на watermelon
```
**Търсене в списък**
```Ruby
fruits.include? "apple" # true
puts fruits.include? "banana" # false
```
**Други функции**
Нека имаме следния списък 

`vegetables = ["potatoes", "carrots", "broccoli", "cucumber", "potatoes"]`
- `vegetables.uniq # ["potatoes", "carrots", "broccoli", "cucumber"]` маха дублиращите елементи
- `vegetables.sort # ["broccoli", "carrots", "cucumber", "potatoes", "potatoes"]` сортира списъка

### Речници
Може да правите аналогия с тълковен речник. Елементите на речниците представляват съответствие между ключ и стойност, като ключът се използва за търсене. 

Нека имаме следният речник `dictionary = { "one" => "eins", "two" => "zwei", "three" => "drei" }`

**Достъпване на елемент**
```Ruby
puts dictionary["one"] # eins
```
**Добавяне на елемент**
В квадратните скоби пишем ключа, който искаме да вмъкнем, а след = стойността
```Ruby
 dictionary["zero"] = "null"
 puts dictionary["zero"]
 ```
 **Променяне на елемент**
 ```Ruby
dictionary["zero"] = "uno"
puts dictionary["zero"] #uno
```

Речниците могат да използват всякакви типове данни за ключове и стойности

**Действия с речници**
- `dictionary.keys # one, two, tree, zero` - извежда имената на ключовете
- `dictionary.length # 4` - извежда броя на елементите в речника
- ` { "one" => "eins" }.merge({ "two" => "zwei" })` - слива два речника
