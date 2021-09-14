---
title: body (Elemento)
description: El elemento body contiene los elementos que definen el contenido de una lista de reproducción.
ms.assetid: 96d09635-c360-4a36-a56e-6cecbbd4ff30
keywords:
- Body Element Reproductor de Windows Media
topic_type:
- apiref
api_name:
- body Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: eb30885efe9e018bf8792b38facdc086c5473b3f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126889540"
---
# <a name="body-element"></a>body (Elemento)

El **elemento body** contiene los elementos que definen el contenido de una lista de reproducción.

``` syntax
<body>
</body>
```

## <a name="attributes"></a>Atributos

Este elemento no tiene atributos.

## <a name="parentchild-elements"></a>Elementos primarios y secundarios



| Hierarchy | Elementos                 |
|-----------|--------------------------|
| Parent    | [Smil](smil-element.md) |
| Elemento secundario     | [Seq](seq-element.md)   |



 

## <a name="remarks"></a>Observaciones

El contenido de una lista de reproducción se organiza dentro **de un elemento seq** que se encuentra dentro del **elemento body.** Normalmente hay un elemento **seq** que define un conjunto  estático de elementos multimedia y contiene elementos multimedia, o bien hay uno que define un conjunto dinámico de elementos multimedia y contiene un elemento **smartPlaylist.**

## <a name="examples"></a>Ejemplos


```XML
<body>
    <seq>
        <media></media>
        <media></media>
        <media></media>
    </seq>
</body>

<body>
    <seq>
        <smartPlaylist></smartPlaylist>
    </seq>
</body>
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media serie 9 o posterior.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**elemento media**](media-element.md)
</dt> <dt>

[**seq (Elemento)**](seq-element.md)
</dt> <dt>

[**Elemento smartPlaylist**](smartplaylist-element.md)
</dt> <dt>

[**smil (Elemento)**](smil-element.md)
</dt> <dt>

[**Windows Referencia de elementos de lista de reproducción multimedia**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





