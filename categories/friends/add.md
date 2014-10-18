---
layout: default
title: Метод Friends.Add
permalink: friends/add/
comments: true
---
# Метод Friends.Add
Одобряет или создает заявку на добавление в друзья.

## Синтаксис
```csharp
public AddFriendStatus Add(long userId, string text)
```

## Параметры
+ **userId** - идентификатор пользователя, которому необходимо отправить заявку, либо заявку от которого необходимо одобрить.
+ **text** - текст сопроводительного сообщения для заявки на добавление в друзья. Максимальная длина сообщения — 500 символов.

## Результат
После успешного выполнения возвращает одно из следующих значений:
1 — заявка на добавление данного пользователя в друзья отправлена;
2 — заявка на добавление в друзья от данного пользователя одобрена;
4 — повторная отправка заявки.
## Исключения

## Пример
```csharp
// TODO:
```