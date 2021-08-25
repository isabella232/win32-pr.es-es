---
title: ELEMENTO DURATION
description: El elemento DURATION define el período de tiempo durante el Reproductor de Windows Media representará la entrada de lista de reproducción asociada.
ms.assetid: fe5c242e-08c9-44f0-a6fc-3f0fa432ba38
keywords:
- Elemento DURATION Reproductor de Windows Media
topic_type:
- apiref
api_name:
- DURATION Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5b06b497a6d31b03c4cbec23748f6995a1382fb806ad18fabaa542ed8ff33e4f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119863355"
---
# <a name="duration-element"></a>ELEMENTO DURATION

El **elemento DURATION** define el período de tiempo durante el Reproductor de Windows Media representará la entrada de lista de reproducción asociada.

``` syntax
<DURATION
    VALUE = "hh:mm:ss.fract"
/>
```

## <a name="attributes"></a>Atributos

**VALUE** (obligatorio)

El tiempo, en horas, minutos, segundos y centésimas de segundo, que representa una entrada Reproductor de Windows Media. El valor predeterminado es la longitud completa de la entrada. Si la entrada es un archivo gráfico, se debe especificar un valor de duración.

## <a name="parentchild-elements"></a>Elementos primarios y secundarios



| Hierarchy       | Elementos           |
|-----------------|--------------------|
| Elementos primarios | **ENTRY**, **REF** |
| Elementos secundarios  | Ninguno               |



 

## <a name="remarks"></a>Observaciones

Este elemento define el período de tiempo durante el que se va a representar una secuencia. Si el **atributo VALUE** supera la longitud de la secuencia de contenido, la secuencia finaliza en su punto final normal.

Este elemento puede aparecer dentro de un **elemento REF** o dentro de un **elemento ENTRY.** Sin embargo, **un elemento DURATION** definido dentro de un  **elemento REF** invalida uno que aparece dentro del elemento PRIMARIO ENTRY del **elemento REF.**

El **elemento DURATION** invalida un elemento **PREVIEWDURATION.**

## <a name="examples"></a>Ejemplos


```XML
<DURATION VALUE="00:00:30" />   <!-- 30 seconds -->
<DURATION VALUE="1:01.5" />     <!-- 61.5 seconds -->

```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Windows Referencia de elementos de metarchivo multimedia**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Referencia de metarchivo multimedia**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





