---
title: smil (Elemento)
description: El elemento smil siempre es el elemento de nivel superior de un Windows lista de reproducción multimedia (WPL). Especifica que el archivo usa la sintaxis y la gramática de SMIL (lenguaje de integración multimedia sincronizada).
ms.assetid: bb14f1b8-53d0-47ff-9fd3-4620a1467985
keywords:
- smil Element Reproductor de Windows Media
topic_type:
- apiref
api_name:
- smil Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 15ed9c3d70b0af65019cd384bc68ab9c26f8d01673481b9ced3595730379bf1a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119763465"
---
# <a name="smil-element"></a>smil (Elemento)

El **elemento smil** siempre es el elemento de nivel superior de un archivo Windows lista de reproducción multimedia (WPL). Especifica que el archivo usa la sintaxis y la gramática de SMIL (lenguaje de integración multimedia sincronizada).

``` syntax
<smil>
</smil>
```

## <a name="attributes"></a>Atributos

Este elemento no tiene atributos.

## <a name="parentchild-elements"></a>Elementos primarios y secundarios



| Hierarchy | Elementos                                           |
|-----------|----------------------------------------------------|
| Parent    | Ninguno                                               |
| Elemento secundario     | [head](head-element.md), [body](body-element.md) |



 

## <a name="remarks"></a>Comentarios

Cada Windows lista de reproducción multimedia debe tener **el elemento smil** en su raíz.

## <a name="examples"></a>Ejemplos


```
<?wpl version = "1.0"?>
<smil>
    <head>
        <entity type="hellip"/>
    </head>

    <body>
        <entity type="hellip"/>
    </body>
</smil>
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media serie 9 o posterior.<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**body (Elemento)**](body-element.md)
</dt> <dt>

[**elemento head**](head-element.md)
</dt> <dt>

[**Windows Referencia de elementos de lista de reproducción multimedia**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





