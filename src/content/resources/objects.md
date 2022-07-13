---
title: Objects
description: Возвращает список идентификаторов всех доступных объектов.
---

## {frontmatter.title}

<p class="text-xl">{frontmatter.description}</p>

```
GET /collection/v1/objects
```

| Параметр       | Формат                                                                            | Описание                                                      |
| -------------- | --------------------------------------------------------------------------------- | ------------------------------------------------------------- |
| `metadataDate` | datetime, формат YYYY-MM-DD                                                       | Возвращает все объекты с обновленными данными после этой даты |
| `sourceIds`    | int, соответствующие идентификаторам источников, например, 1 или 3&#124;9&#124;12 | Возвращает все объекты из указанного источника                |

### Примеры

#### Request

```
GET /collection/v1/objects
```

#### Response

```json
{
    "total": 100,
    "objectsIds": {
        1,
        2,
        3,
        4,
        5,

        // Прочие результаты ...
    }
}
```

#### Request

```
GET /collection/v1/objects?sourceIds=1
```

#### Response

```json
{
    "total": 25, // Меньше, чем полное количество доступных объектов
    "objectsIds": {
        1,
        2,
        3,
        4,
        5,

        // Прочие результаты ...
    }
}
```

#### Request

```
GET /collection/v1/objects?sourceIds=1|2|3
```

#### Response

```json
{
    "total": 45, // Меньше, чем полное количество доступных объектов
    "objectsIds": {
        1,
        2,
        3,
        4,
        5,

        // Прочие результаты ...
    }
}
```

#### Request

```
GET /collection/v1/objects?metadataDate=2022-07-12
```

#### Response

```json
{
    "total": 45, // Меньше, чем полное количество доступных объектов
    "objectsIds": {
        1,
        2,
        3,
        4,
        5,

        // Прочие результаты ...
    }
}
```

#### Request

```
GET /collection/v1/objects?metadataDate=2022-07-12&sourceIds=1|2|3
```

#### Response

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
