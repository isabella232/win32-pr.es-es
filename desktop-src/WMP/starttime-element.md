---
title: STARTTIME (elemento)
description: El elemento STARTTIME define un índice de tiempo desde el que Windows Media Player comenzará a representar la secuencia.
ms.assetid: 9b0199c8-5c95-4b4e-a943-e3bd037bf0bc
keywords:
- Elemento STARTTIME Media Player Windows
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699468"
---
# <a name="starttime-element"></a>STARTTIME (elemento)

El elemento **STARTTIME** define un índice de tiempo desde el que Windows Media Player comenzará a representar la secuencia.

``` syntax
<STARTTIME
   VALUE = "hh:mm:ss.fract"
/>
```

## <a name="attributes"></a>Atributos

**Valor** (obligatorio)

El índice de tiempo (en horas, minutos, segundos y centésimas de segundo) desde el que Windows Media Player comienza a reproducir un flujo definido en el elemento asociado.

## <a name="parentchild-elements"></a>Elementos primarios y secundarios



| Hierarchy       | Elementos           |
|-----------------|--------------------|
| Elementos primarios | **entrada**, **ref** |
| Elementos secundarios  | Ninguno               |



 

## <a name="remarks"></a>Observaciones

Este elemento define un índice de tiempo en el contenido donde Windows Media Player va a comenzar a representar la secuencia. Este elemento solo se puede usar con contenido almacenado a petición que se ha indexado.

## <a name="examples"></a>Ejemplos


```XML
<STARTTIME VALUE="1:30.0" />
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

 

 





