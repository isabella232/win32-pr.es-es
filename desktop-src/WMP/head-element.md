---
title: Elemento de encabezado
description: El elemento de encabezado contiene metadatos que se aplican a toda la lista de reproducción.
ms.assetid: 9554c84a-34af-4492-964a-4b262cd7c4a4
keywords:
- Elemento de encabezado de Windows Media Player
topic_type:
- apiref
api_name:
- head Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8708a8a683f7457e6568df3a897c71253ad76c02
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699760"
---
# <a name="head-element"></a>Elemento de encabezado

El elemento de **encabezado** contiene metadatos que se aplican a toda la lista de reproducción.

``` syntax
<head>
</head>
```

## <a name="attributes"></a>Atributos

Este elemento no tiene atributos.

## <a name="parentchild-elements"></a>Elementos primarios y secundarios



| Hierarchy | Elementos                                                  |
|-----------|-----------------------------------------------------------|
| Parent    | [gestual](smil-element.md)                                  |
| Elemento secundario     | [título](title-element--wpl.md), [meta](meta-element.md) |



 

## <a name="remarks"></a>Observaciones

Normalmente, el elemento de **encabezado** contiene un elemento de **título** y uno o varios elementos **meta** que definen las características globales de la lista de reproducción.

## <a name="examples"></a>Ejemplos


```
<head>
    <title>Party Playlist</title>
    <meta name = "Author" CONTENT = "Frank Lee"/>
    <meta name = "Category" CONTENT = "Party Music"/>
    <meta name = "Genre" CONTENT = "Pop"/>
    <meta name = "UserName1" CONTENT = "Frank001"/>
    <meta name = "UserRating1" CONTENT = "82"/>
</head>
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------|
| Versión<br/> | Windows Media Player 9 series o posterior.<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento meta**](meta-element.md)
</dt> <dt>

[**Elemento title (WPL)**](title-element--wpl.md)
</dt> <dt>

[**Referencia de elementos de lista de reproducción de Windows Media**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





