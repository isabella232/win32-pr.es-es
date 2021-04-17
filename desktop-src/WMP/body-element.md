---
title: Elemento BODY
description: El elemento BODY contiene los elementos que definen el contenido de una lista de reproducción.
ms.assetid: 96d09635-c360-4a36-a56e-6cecbbd4ff30
keywords:
- Elemento de cuerpo Media Player de Windows
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700005"
---
# <a name="body-element"></a>Elemento BODY

El elemento **Body** contiene los elementos que definen el contenido de una lista de reproducción.

``` syntax
<body>
</body>
```

## <a name="attributes"></a>Atributos

Este elemento no tiene atributos.

## <a name="parentchild-elements"></a>Elementos primarios y secundarios



| Hierarchy | Elementos                 |
|-----------|--------------------------|
| Parent    | [gestual](smil-element.md) |
| Elemento secundario     | [Próx](seq-element.md)   |



 

## <a name="remarks"></a>Observaciones

El contenido de una lista de reproducción se organiza dentro de un elemento **Seq** incluido en el elemento **Body** . Normalmente, hay un elemento **Seq** que define un conjunto estático de elementos multimedia y contiene elementos **multimedia** , o bien uno que define un conjunto dinámico de elementos multimedia y contiene un elemento **smartPlaylist** .

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
| Versión<br/> | Windows Media Player 9 series o posterior.<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento multimedia**](media-element.md)
</dt> <dt>

[**Seq (elemento)**](seq-element.md)
</dt> <dt>

[**Elemento smartPlaylist**](smartplaylist-element.md)
</dt> <dt>

[**Elemento SMIL**](smil-element.md)
</dt> <dt>

[**Referencia de elementos de lista de reproducción de Windows Media**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





