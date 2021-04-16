---
title: Elemento ABSTRACT
description: El elemento ABSTRACTo contiene texto que describe el elemento ASX, BANNER o ENTRY asociado.
ms.assetid: 7866fee8-1778-433a-be2f-9df0baa1c13e
keywords:
- Media Player de elementos ABSTRACTos de Windows
topic_type:
- apiref
api_name:
- ABSTRACT Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4e90b6f52b697242be23303ab3597dac549a6177
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699992"
---
# <a name="abstract-element"></a>Elemento ABSTRACT

El elemento **abstracto** contiene texto que describe el elemento **ASX**, **banner** o **entry** asociado.

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
| Parent    | **ASX**, **entrada**, **banner** |
| Elemento secundario     | None                           |



 

## <a name="remarks"></a>Observaciones

Si este elemento aparece dentro de un elemento **ASX** , el texto se muestra como información sobre herramientas cuando se mantiene el mouse sobre el título.

Si este elemento aparece dentro de un elemento de **entrada** , el texto se muestra como información sobre herramientas cuando se mantiene el mouse sobre el título del clip.

Si este elemento aparece dentro de un elemento **banner** , el texto se muestra como información sobre herramientas para el gráfico de banner.

Use solo un elemento **abstracto** por ámbito. Solo se utiliza el primer elemento **abstracto** dentro del ámbito de otro elemento cuando se procesa un archivo de metarchivo. Se omiten los elementos **abstractos** subsiguientes de ese ámbito.

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
| Versión<br/> | Windows Media Player versión 70 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Referencia de elementos de metarchivo de Windows Media**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Referencia de metarchivos de Windows Media**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





