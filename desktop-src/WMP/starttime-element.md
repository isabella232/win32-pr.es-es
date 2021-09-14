---
title: Elemento STARTTIME
description: El elemento STARTTIME define un índice de tiempo a partir del Reproductor de Windows Media comenzará a representar la secuencia.
ms.assetid: 9b0199c8-5c95-4b4e-a943-e3bd037bf0bc
keywords:
- Elemento STARTTIME Reproductor de Windows Media
topic_type:
- apiref
api_name:
- STARTTIME Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8a882da6c07ec76a94c8e214fe1da11c71680b0c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127241731"
---
# <a name="starttime-element"></a>Elemento STARTTIME

El **elemento STARTTIME** define un índice de tiempo a partir del Reproductor de Windows Media comenzará a representar la secuencia.

``` syntax
<STARTTIME
   VALUE = "hh:mm:ss.fract"
/>
```

## <a name="attributes"></a>Atributos

**VALUE** (obligatorio)

Índice de tiempo (en horas, minutos, segundos y centésimas de segundo) desde el que Reproductor de Windows Media comienza a reproducir una secuencia definida en el elemento asociado.

## <a name="parentchild-elements"></a>Elementos primarios y secundarios



| Hierarchy       | Elementos           |
|-----------------|--------------------|
| Elementos primarios | **ENTRY**, **REF** |
| Elementos secundarios  | Ninguno               |



 

## <a name="remarks"></a>Observaciones

Este elemento define un índice de tiempo en el contenido donde Reproductor de Windows Media va a empezar a representar la secuencia. Este elemento solo se puede usar con contenido almacenado a petición que se ha indexado.

## <a name="examples"></a>Ejemplos


```XML
<STARTTIME VALUE="1:30.0" />
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

 

 





