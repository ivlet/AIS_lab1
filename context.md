# Контекст решения
<!-- Окружение системы (роли, участники, внешние системы) и связи системы с ним. Диаграмма контекста C4 и текстовое описание. 
-->
```plantuml
@startuml
!include https://raw.githubusercontent.com/plantuml-stdlib/C4-PlantUML/master/C4_Container.puml

Person(user, "Пользователь")
Person(admin, "Администратор")
Person(moder, "Модератор")

System(social_network_site, "Социальная сеть", "Веб-сайт для общения людей")



Rel(user, social_network_site, "Регистрация, просмотр информации на стене, отправка сообщений в чате, оставление комментариев на стене")
Rel(admin, social_network_site, "Назначение администраторов, назначение модераторов, модерация контента и пользователей")
Rel(moder, social_network_site, "Модерация контента и пользователей")


@enduml
```
## Назначение систем
|Система| Описание|
|-------|---------|
| Социальная сеть | Веб-интерфейс, обеспечивающий доступ к стенам пользователей, на которых размещены их сообщения. Бэкенд сервиса реализован в виде микросервисной архитектуры |

