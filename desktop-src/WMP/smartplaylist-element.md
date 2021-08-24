---
title: elemento smartPlaylist
description: El elemento smartPlaylist contiene la parte definida dinámicamente de una lista de reproducción.
ms.assetid: 05912849-7475-4eb9-a7bd-00f20b80b1cf
keywords:
- Elemento smartPlaylist Reproductor de Windows Media
topic_type:
- apiref
api_name:
- smartPlaylist Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a21d685759e9e8b27c881ceaec6595535b3c4b799eb28ecd94dd96a3a571ec99
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119763475"
---
# <a name="smartplaylist-element"></a>elemento smartPlaylist

El **elemento smartPlaylist** contiene la parte definida dinámicamente de una lista de reproducción.

``` syntax
<smartPlaylist
    version = "number"
>
</smartPlaylist>
```

## <a name="attributes"></a>Atributos



| Término                                                                                                                                   | Descripción                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span id="version__required______________"></span><span id="VERSION__REQUIRED______________"></span>**version** (obligatorio) <br/> | Número decimal que representa el número de versión del esquema de lista de reproducción inteligente. Se establece en 1.0.0.0.<br/> |



 

## <a name="parentchild-elements"></a>Elementos primarios y secundarios



| Hierarchy | Elementos                                                       |
|-----------|----------------------------------------------------------------|
| Parent    | [Seq](seq-element.md)                                         |
| Elemento secundario     | [querySet](queryset-element.md), [filter](filter-element.md) |



 

## <a name="remarks"></a>Comentarios

Un **elemento smartPlaylist** normalmente contiene un **elemento querySet** y también puede contener un **elemento filter.**

## <a name="examples"></a>Ejemplos


```
<smartPlaylist version = "1.0.0.0">
    <querySet>
        <sourceFilter 
            type = "smartFilterObject"
            id = "12345678-1234-3333-abCD-123ABCdefGHI"
            name = "Music in my library">
                <fragment name = "Genre">
                    <argument name = "condition">Is</argument>
                    <argument name = "value">Rock</argument>
                </fragment>
                <fragment name = "Album Artist">
                    <argument name = "condition">Is Not</argument>
                    <argument name = "value">Brenda Diaz</argument>
                </fragment>
        </sourceFilter>
    </querySet>
    <filter>
    </filter>
</smartPlaylist>
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media serie 9 o posterior.<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**elemento argument**](argument-element.md)
</dt> <dt>

[**elemento filter**](filter-element.md)
</dt> <dt>

[**elemento fragment**](fragment-element.md)
</dt> <dt>

[**elemento querySet**](queryset-element.md)
</dt> <dt>

[**elemento seq**](seq-element.md)
</dt> <dt>

[**Windows Referencia de elementos de lista de reproducción multimedia**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





