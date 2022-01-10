# Мой первый самостоятельный проект на React
(я даже не обратил внимания что я не пушил на гитхаб react код....)
# Что есть?
1)пока что я не нашел API-шки для аутентификации, поэтому аутентификация использует сервер, который бесплатно работает только с лока-хоста, поэтому аутентификация как бы есть, но ее нет
## Раздел с поиском фильмов (используется IMDb-API)
Закончил сегодня, когда пользователь открывает этот раздел, то на сервер отправляется запрос на 100 лучших фильмов, пока запрос обрабатывается показывается гифка с загрузкой, затем все фильмы отрисовываются. Название фильма и его картинка являются ссылками, нажав на ссылку, пользователя перебросит на страничку с полным описанием фильма. Сначала сделается запрос на сервер за описанием фильма, пока обрабатывается запрос показывается гифка с загрузкой, затем отрисовывается полное описание фильма

# Раздел с новостной лентой
Начал сегодня разработку этого раздела, пока что реализовал логику хедера новостной ленты, в нем будут группы на которые пользователь подписан, и кнопка подписаться/отписаться (состояние о подписке хранится в local storage). 

### Логика
Если в local storage у какого то значения стоит true(что означает что пользователь подписался на эту группу) то я делаю запрос на 100 картинок(что бы не дергать по многу раз сервер) из этой рубрики, затем я вывожу 2 картинки, и если пользователь нажал кнопку увидеть больше, то я расширяю массив с картинками, добавив в него еще 2 картинки,

(27.12.21) Добавил запросы на сервер за картинками собак и мемами, и объединил с логикой подписок, если пользователь подписан на какой либо раздел (аниме- скорее всего заменю потому что адекватных апишек так и не нашел, собаки и мемы) то у него в новостной ленте будут картинки только на которые он подписан, сделал так что бы отображалось всего 2 картинки, завтра добавлю кнопку "увидеть больше", стилизовать буду опять же в полслендюю очередь
(28.12.21) Добавил кнопки "увидеть больше", при их нажатии  добавляется еще 2 картинки из рубрики  

(27.12.21) Добавил запросы на сервер за картинками собак и мемами, и объединил с логикой подписок, если пользователь подписан на какой либо раздел (аниме- скорее всего заменю потому что адекватных апишек так и не нашел, собаки и мемы) то у него в новостной ленте будут картинки только на которые он подписан, сделал так что бы отображалось всего 2 картинки, завтра добавлю кнопку "увидеть больше", стилизовать буду опять же в полслендюю очередь  
(28.12.21) Добавил кнопки "увидеть больше", при их нажатии  добавляется еще 2 картинки из рубрики  
Сегодня было очень мало времени, поэтому я всего лишь добавил прелоадер, и поискал апишки для изображения котиков, но пока не нашел ничего хорошего...


## to-do-list
Начал разработку туду листа, начал разбираться с библиотекой react-final-form
Разобрался с базовыми принципами работы react-final-form, оказалось очень удобным инструментом, так же еще раз потренировался с local storage и более углубленно почитал про JSON  
Так же закончил с логикой туду листа, сделал добавление и удаление задач
стилизовать буду опять же в самом конце

## РАЗДЕЛ С СООБЩЕНИЯМИ
### начну уже завтра делать раздел с сообщениями при помощи сокетов(нужно будет еще с ними познакомиться)
Сегодня подключил socket.io для фронта и сервера ,разбирался как на node js сделать не сложный сервер, сверстал раздел с сообщенями(точнее вход в него, в последующем думаю как нибдуь связать его с регистрацией), сделал примитивный сервер, отправил на него post запрос, на фронте по мимо верстки сделал reducer для раздела с сообщениями
Сделал так что пользователи могут заходить в одну комнату, это можно понять по разделу "онлайн", в котором будут находиться пользователи из этой комнаты которые сейчас онлайн  
Пока что хранение пользователей происходит через Map, но когда я реализую чат полностью, я сделаю базу данных, в которой буду хранить сообщения  
Так же я решил сделать регистрацию через свой сервер, но это тоже после того как чат будет полностью рабочим
## Какие технологии используются
1)Redux  
2)thunk  
3)axios  
4)react-router-dom  
5)использовал хук useParams что бы достать id фильма из URL  
6)Для стилизации решил попробовать "styled-components" пока нравится, что не нужно бегать между файлами а сразу пишешь стили в js )  
7)использовал хуки useState и useEffect, (пока что только в разделе news, но планирую и дальше их использовать и отказаться от классовых компонент)

## Другое 
Стилизовать я пока не буду, потому что сейчас мне интереснее разбираться с логикой, а не с внешним видом.
