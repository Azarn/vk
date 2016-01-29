---
layout: default
title: Метод Auth.Restore
permalink: auth/restore/
comments: true
---
# Метод Auth.Restore
Позволяет восстановить доступ к аккаунту, используя код, полученный через SMS. 
Данный метод доступен только приложениям, имеющим доступ к Прямой авторизации.

Страница документации ВКонтакте [auth.restore](https://vk.com/dev/auth.restore).
## Синтаксис
``` csharp
public string Restore(string phone)
```

## Параметры
+ **phone** - Номер телефона пользователя. строка, обязательный параметр

## Результат
В случае успеха метод возвращает объект содержащий следующие поля: 
success – 1; 
sid – параметр необходимый для получения доступа по коду. 
Для завершения восстановления доступа необходимо обратиться по адресу: https://oauth.vk.com/token?grant_type=restore_code&amp;client_id={Идентификатор приложения}&amp;client_secret={Секретный_ключ}&amp;username={Номер телефона}&amp;scope={Список прав доступа}&amp;sid={Параметр, получаемый в данном методе}&amp;code={Код полученный через SMS} 
Список параметров: 
grant_type – необходимо передать значение: restore_code; 
client_id – Идентификатор приложения; 
client_secret – Секретный ключ; 
username – Номер телефона по которому был восстановлен пароль; 
scope – список прав доступа, разделенных через запятую; 
sid – идентификатор сессии, полученный в результате выполнения этого метода; 
code – код, полученный через SMS. 
В результате авторизации через restore_code OAuth вернет данные аналогичные обычной авторизации, с дополнительным параметром change_password_hash необходимым для метода account.changePassword.

## Пример
``` csharp
// Пример кода
```

## Версия Вконтакте API v.5.44
Дата обновления: 28.01.2016 14:06:14