---
title: Elemento ABSTRACT
description: El elemento ABSTRACT contiene texto que describe el elemento ASX, BANNER o ENTRY asociado.
ms.assetid: 7866fee8-1778-433a-be2f-9df0baa1c13e
keywords:
- Resumen del elemento ABSTRACT Reproductor de Windows Media
topic_type:
- apiref
api_name:
- ABSTRACT Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 153759dbe4bef47693cba13549b58215e4992686eab81cdcb4dadb33aa30279f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119903055"
---
# <a name="abstract-element"></a>Elemento ABSTRACT

El **elemento ABSTRACT** contiene texto que describe el elemento **ASX,** **BANNER** o **ENTRY** asociado.

``` syntax
<ABSTRACT>
   text string
</ABSTRACT>
      
```

## <a name="attributes"></a>Atributos

Este elemento no tiene atributos.

## <a name="parentchild-elements"></a>Elementos primarios y secundarios



| Hierarchy | Elementos                       |
|-----------|--------------------------------|
| Parent    | **ASX**, **ENTRY**, **BANNER** |
| Elemento secundario     | Ninguno                           |



 

## <a name="remarks"></a>Observaciones

Si este elemento aparece dentro de un **elemento ASX,** el texto se muestra como información sobre herramientas cuando el mouse se mantiene sobre el título de presentación.

Si este elemento aparece dentro de un **elemento ENTRY,** el texto se muestra como información sobre herramientas cuando el mouse mantiene el mouse sobre el título del clip.

Si este elemento aparece dentro de un **elemento BANNER,** el texto se muestra como información sobre herramientas para el gráfico de banner.

Use solo un **elemento ABSTRACT** por ámbito. Solo se usa **el primer** elemento ABSTRACT dentro del ámbito de otro elemento cuando se procesa un archivo de metarchivo. Se **omiten los** elementos ABSTRACT posteriores de ese ámbito.

## <a name="examples"></a>Ejemplos


```XML
<ASX VERSION="3.0">
    <TITLE>The Title of the Show<TITLE>
    <ABSTRACT>
        Brief description of the show. 
    </ABSTRACT>

<ENTRY>    
    <REF HREF="YourMediaFilename.asf" />
    <TITLE>The Title of the Track</TITLE>
    <ABSTRACT>
        Brief description of the track.
    </ABSTRACT>
</ENTRY>
</ASX>
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 70 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Windows Referencia de elementos de metarchivo multimedia**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Referencia de metarchivo multimedia**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





