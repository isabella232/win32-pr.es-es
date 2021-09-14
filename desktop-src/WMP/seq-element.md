---
title: seq (Elemento)
description: El elemento seq contiene elementos que definen una lista de reproducción estática o elementos que definen una lista de reproducción inteligente.
ms.assetid: 849f7b38-25f2-4708-a83c-e651812a1a72
keywords:
- seq Element Reproductor de Windows Media
topic_type:
- apiref
api_name:
- seq Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b08b3f4dfa448e48f3a9d2472c6ddb46a4d4dfaf
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070859"
---
# <a name="seq-element"></a>seq (Elemento)

El **elemento seq** contiene elementos que definen una lista de reproducción estática o elementos que definen una lista de reproducción inteligente.

``` syntax
<seq>
</seq>
```

## <a name="attributes"></a>Atributos

Este elemento no tiene atributos.

## <a name="parentchild-elements"></a>Elementos primarios y secundarios



| Hierarchy | Elementos                                                               |
|-----------|------------------------------------------------------------------------|
| Parent    | [body](body-element.md)                                               |
| Elemento secundario     | [media](media-element.md), [smartPlaylist](smartplaylist-element.md) |



 

## <a name="remarks"></a>Observaciones

Cuando un **elemento seq** solo **contiene** elementos multimedia que hacen referencia a elementos multimedia específicos, la lista de reproducción se considera estática. Cuando un **elemento seq** contiene un **elemento smartPlaylist,** se considera una lista de reproducción dinámica "inteligente".

## <a name="examples"></a>Ejemplos


```
<seq>
    <media></media>
    <media></media>
</seq>

<seq>
    <smartPlaylist></smartPlaylist>
</seq>
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media serie 9 o posterior.<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**body (Elemento)**](body-element.md)
</dt> <dt>

[**elemento media**](media-element.md)
</dt> <dt>

[**Elemento smartPlaylist**](smartplaylist-element.md)
</dt> <dt>

[**Windows Referencia de elementos de lista de reproducción multimedia**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





