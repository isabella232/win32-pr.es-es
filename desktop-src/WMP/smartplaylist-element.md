---
title: Elemento smartPlaylist
description: El elemento smartPlaylist contiene la parte definida dinámicamente de una lista de reproducción.
ms.assetid: 05912849-7475-4eb9-a7bd-00f20b80b1cf
keywords:
- Elemento smartPlaylist Media Player Windows
topic_type:
- apiref
api_name:
- smartPlaylist Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 511294af2de4343cb7f63db4312d530aadf57da6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105709124"
---
# <a name="smartplaylist-element"></a>Elemento smartPlaylist

El elemento **smartPlaylist** contiene la parte definida dinámicamente de una lista de reproducción.

``` syntax
<smartPlaylist
    version = "number"
>
</smartPlaylist>
```

## <a name="attributes"></a>Atributos



| Término                                                                                                                                   | Descripción                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span id="version__required______________"></span><span id="VERSION__REQUIRED______________"></span>**versión** (obligatorio) <br/> | Número decimal que representa el número de versión del esquema de lista de reproducción inteligente. Establezca en 1.0.0.0.<br/> |



 

## <a name="parentchild-elements"></a>Elementos primarios y secundarios



| Hierarchy | Elementos                                                       |
|-----------|----------------------------------------------------------------|
| Parent    | [Próx](seq-element.md)                                         |
| Elemento secundario     | [querySet](queryset-element.md), [filtro](filter-element.md) |



 

## <a name="remarks"></a>Observaciones

Un elemento **smartPlaylist** normalmente contiene un elemento **querySet** y también puede contener un elemento **Filter** .

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



| Requisito | Value |
|--------------------|----------------------------------------------------|
| Versión<br/> | Windows Media Player 9 series o posterior.<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento argument**](argument-element.md)
</dt> <dt>

[**Elemento Filter**](filter-element.md)
</dt> <dt>

[**Elemento Fragment**](fragment-element.md)
</dt> <dt>

[**Elemento querySet**](queryset-element.md)
</dt> <dt>

[**Seq (elemento)**](seq-element.md)
</dt> <dt>

[**Referencia de elementos de lista de reproducción de Windows Media**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





