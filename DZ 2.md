# Инструкция по системе Контроля версий GIT

![image](image2.jpg)


## Ветвления в GIT

### В GIT множество полезных функций, одной из которых является **ветвление**. С помощью неё, мы как бы, путешествуем среди разных парраллельных вселенных, мы можем вносить в них изменения, проводить их слияние, удалять, переименовывать, возвращать назад во времени и снова менять там всё что захотим.
### Ветвление напоминает большое дерево с системой хаотично расположенных веток, но за этим скрыта чистая системность, комплексность и рациональность. Об этом мы с вами сегодня и поговорим.

Чтобы нам с вами посмотреть на "ветки дерева", нужно

*воспользоваться командой*:

    git branch
Эта команда позволяет нам посмотреть на существующие у нас ветки, сориентироваться по ним, узнать на какой мы находимся 
    
    *master
    fallin

После ввода команды "*" - "звездочкой" будет обозначена та ветка, на которой мы находимся.

====================================================
## Создание веток в GIT
Чтобы было много вариантов наших "вселенных", нам нужно создавать эти ветки, буквально, выращивать их. Чтобы это сделать, нам нужно 

*воспользоваться командой*:

    git branch "branch_name"
Мы должны обдуманно создавать их, название веток должно отражать их суть, их роль в нашем "дереве вселенных"
также мы не должны забывать, на какой мы ветке находимся в данный момент, в этом нам поможет упомянутая выше команда

    git branch
====================================================
## Удаление веток

Чтобы наши ветки не запутвались и не мешали нам, их нужно вовремя удалять, перед удалением нам нужно обязательно провериить целостность остальных веток и их зависимость от той, которую мы хотим удалить.

*с помощью команды*

     git branch

смотрим, на какой мы ветке, если мы оказались не на той ветке, нужно переключиться на другую ветку

*использовать команду*

    git checkout <branch_name>
далее еще раз проверяем на какой мы ветке, с помощью команды git branch и можно со спокойной душой удалять ненужную ветку.

затем уже, удостоверившись, что нам ничего не мешает, можем,  наконец, удалить ветку, при помощи

*команды*

    git branch -d <branch_name>
====================================================
## Иллюстрирование веток в терминале

Чтобы мы могли увидеть и подробнее разглядеть наши ветки, увидеть где они пересекаются, и при необходимости перейти к коммитам на этих ветках, нам нужна

*команда*

    git log --graph
Эта команда поможет отобразить нам весь наш путь коммитов и их веток в подробностях.

Если мы хотим увидеть более компактное отображение наших веток, откуда "берутся ноги" у одной, и в какую ветку она "врастает", следует прибегнуть к

*команде*

    git log --all --oneline --graph

====================================================
## Слияние веток и разрешение их конфликтов

Слияние веток - это процесс, за которым нужен глаз да глаз, ведь легко допустить ошибку в этом процессе, нам нужно правильно слиять ветки, мы можем сделать это неправильно и будет потом намного тяжелее все исправить. к счастью, функционал Git поможет разрешить все конфликты

Для того, чтобы скрестить наши ветки, нам необходимо узнать, на какой мы находимся в настоящее время, при помощи 

*команды*

      git branch
Мы должны помнить, что слияние будет происходить на ту ветку, на которой мы находимся , то есть, если мы на ветке master, мы добавим все наши изменения с другой ветки именно на ветку master.

Чтобы выполнить слияние, нам нужно воспользоваться 

*командой*

    git merge <branch_name>
Если же у нас, всё-таки после слияния произошел конфликт, мы можем его решить, в этом на поможет встроенный функционал Git, мы можем выбрать какие изменения мы хотим вносить, а какие нет, где
    
    current change
_Это данные из нашей ветки, в которую мы внедряем другую ветку_

     Incoming change
_Это изменения, которые пришли из другой ветки_

 у нас есть выбор, над каждым из этих обозначений будут предложены варианты решения, такие как:

 * Accept current change (Принять текущее изменение)
 * Accept incoming change (Принять входящие изменения)
 * Accept Both changes (Примите оба изменения)
 * Compare changes (Сравните изменения)

везде выбираем тот вариант, который мы считаем нужным и завершаем слияние.

====================================================

## Удаленные репозитории

Они нужны для....





    






