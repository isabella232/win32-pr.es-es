---
title: elemento head
description: El elemento principal contiene metadatos que se aplican a toda la lista de reproducción.
ms.assetid: 9554c84a-34af-4492-964a-4b262cd7c4a4
keywords:
- elemento head Reproductor de Windows Media
topic_type:
- apiref
api_name:
- head Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a865419a005927cd85ea6b03d4fabad2e2ac3ef15a840b3bd01209a4df00c075
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118339176"
---
# <a name="head-element"></a>elemento head

El **elemento principal** contiene metadatos que se aplican a toda la lista de reproducción.

``` syntax
<head>
</head>
```

## <a name="attributes"></a>Atributos

Este elemento no tiene atributos.

## <a name="parentchild-elements"></a>Elementos primarios y secundarios



| Hierarchy | Elementos                                                  |
|-----------|-----------------------------------------------------------|
| Parent    | [Smil](smil-element.md)                                  |
| Elemento secundario     | [title](title-element--wpl.md), [meta](meta-element.md) |



 

## <a name="remarks"></a>Comentarios

Normalmente, **el elemento principal** contiene un elemento **title** y uno o varios elementos **meta** que definen las características globales de la lista de reproducción.

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



| Requisito | Valor |
|--------------------|----------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media serie 9 o posterior.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**meta (Elemento)**](meta-element.md)
</dt> <dt>

[**elemento title (WPL)**](title-element--wpl.md)
</dt> <dt>

[**Windows Referencia de elementos de lista de reproducción multimedia**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





