---
title: Elemento SMIL
description: El elemento SMIL siempre es el elemento de nivel superior de un archivo de lista de reproducción de Windows Media (WPL). Especifica que el archivo usa la gramática y la sintaxis de SMIL (lenguaje de integración multimedia sincronizado).
ms.assetid: bb14f1b8-53d0-47ff-9fd3-4620a1467985
keywords:
- Media Player de ventanas de elemento SMIL
topic_type:
- apiref
api_name:
- smil Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 78ec8900139cfbd5982228c59010674bbc14765e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661121"
---
# <a name="smil-element"></a>Elemento SMIL

El elemento **SMIL** siempre es el elemento de nivel superior de un archivo de lista de reproducción de Windows Media (Wpl). Especifica que el archivo usa la gramática y la sintaxis de SMIL (lenguaje de integración multimedia sincronizado).

``` syntax
<smil>
</smil>
```

## <a name="attributes"></a>Atributos

Este elemento no tiene atributos.

## <a name="parentchild-elements"></a>Elementos primarios y secundarios



| Hierarchy | Elementos                                           |
|-----------|----------------------------------------------------|
| Parent    | None                                               |
| Elemento secundario     | [encabezado](head-element.md), [cuerpo](body-element.md) |



 

## <a name="remarks"></a>Observaciones

Cada lista de reproducción de Windows Media debe tener el elemento **SMIL** en su raíz.

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
| Versión<br/> | Windows Media Player 9 series o posterior.<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento BODY**](body-element.md)
</dt> <dt>

[**Elemento de encabezado**](head-element.md)
</dt> <dt>

[**Referencia de elementos de lista de reproducción de Windows Media**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





