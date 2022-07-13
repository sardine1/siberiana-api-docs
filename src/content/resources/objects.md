---
title: Объекты
description: Список всех доступных идентификаторов объектов
---

# {frontmatter.title}

{frontmatter.description}

```
GET /public/collection/v1/objects/[objectID]
```

| Параметр | Формат |             Описание             |
| :------: | :----: | :------------------------------: |
| objectId |  0-9   | Уникальный идентификатор объекта |

#### Примеры

##### Запрос

```
GET /public/collection/v1/objects
```

```json
{
    "total": 100,
    "objectsIDs": {
        1,
        2,
        3,
        4,
        5,

        // Прочие результаты ...
    }
}
```

##### Запрос

```
GET /public/collection/v1/objects?collectionIds=1
```

```json
{
    "total": 25, // Меньше, чем полное количество доступных объектов
    "objectsIDs": {
        1,
        2,
        3,
        4,
        5,

        // Прочие результаты ...
    }
}
```

##### Запрос

```
GET /public/collection/v1/objects?collectionIds=1|2|3
```

```json
{
    "total": 45, // Меньше, чем полное количество доступных объектов
    "objectsIDs": {
        1,
        2,
        3,
        4,
        5,

        // Прочие результаты ...
    }
}
```

##### Запрос

```
GET /public/collection/v1/objects?metadataDate=2022-07-12
```

```json
{
    "total": 45, // Меньше, чем полное количество доступных объектов
    "objectsIDs": {
        1,
        2,
        3,
        4,
        5,

        // Прочие результаты ...
    }
}
```

##### Запрос

```
GET /public/collection/v1/objects?metadataDate=2022-07-12&collectionIds=1|2|3
```

```json
{
    "total": 45, // Меньше, чем полное количество доступных объектов
    "objectsIDs": {
        1,
        2,
        3,
        4,
        5,

        // Прочие результаты ...
    }
}
```
