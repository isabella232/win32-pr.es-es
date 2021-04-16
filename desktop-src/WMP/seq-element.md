---
title: Seq (elemento)
description: El elemento SEQ contiene elementos que definen una lista de reproducción estática o elementos que definen una lista de reproducción inteligente.
ms.assetid: 849f7b38-25f2-4708-a83c-e651812a1a72
keywords:
- Elemento SEQ Windows Media Player
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649613"
---
# <a name="seq-element"></a>Seq (elemento)

El elemento **Seq** contiene elementos que definen una lista de reproducción estática o elementos que definen una lista de reproducción inteligente.

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
| Elemento secundario     | [medios](media-element.md), [smartPlaylist](smartplaylist-element.md) |



 

## <a name="remarks"></a>Observaciones

Cuando un elemento **Seq** solo contiene elementos **multimedia** que hacen referencia a elementos multimedia específicos, se considera que la lista de reproducción es estática. Cuando un elemento **Seq** contiene un elemento **smartPlaylist** , se considera que es una lista de reproducción "inteligente" dinámica.

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
| Versión<br/> | Windows Media Player 9 series o posterior.<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento BODY**](body-element.md)
</dt> <dt>

[**Elemento multimedia**](media-element.md)
</dt> <dt>

[**Elemento smartPlaylist**](smartplaylist-element.md)
</dt> <dt>

[**Referencia de elementos de lista de reproducción de Windows Media**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





