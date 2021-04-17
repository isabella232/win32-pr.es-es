---
title: Elemento DURATION
description: El elemento DURATION define el período de tiempo durante el cual Windows Media Player representará la entrada de lista de reproducción asociada.
ms.assetid: fe5c242e-08c9-44f0-a6fc-3f0fa432ba38
keywords:
- Elemento DURATION de Windows Media Player
topic_type:
- apiref
api_name:
- DURATION Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c0446fd207ce04ab08d4c7bd2e055ef8d11a5a36
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700119"
---
# <a name="duration-element"></a>Elemento DURATION

El elemento **Duration** define el período de tiempo durante el cual Windows Media Player representará la entrada de lista de reproducción asociada.

``` syntax
<DURATION
    VALUE = "hh:mm:ss.fract"
/>
```

## <a name="attributes"></a>Atributos

**Valor** (obligatorio)

La cantidad de tiempo, en horas, minutos, segundos y centésimas de segundo, que representa una entrada de Windows Media Player. El valor predeterminado es la longitud total de la entrada. Si la entrada es un archivo gráfico, debe especificarse un valor de duración.

## <a name="parentchild-elements"></a>Elementos primarios y secundarios



| Hierarchy       | Elementos           |
|-----------------|--------------------|
| Elementos primarios | **entrada**, **ref** |
| Elementos secundarios  | Ninguno               |



 

## <a name="remarks"></a>Observaciones

Este elemento define el período de tiempo que se va a representar una secuencia. Si el atributo de **valor** supera la longitud de la secuencia de contenido, la secuencia finaliza en su punto final normal.

Este elemento puede aparecer dentro de un elemento **ref** o dentro de un elemento **entry** . Sin embargo, un elemento **Duration** definido dentro de un elemento **ref** reemplaza a uno que aparece dentro del elemento de **entrada** primario del elemento **ref** .

El elemento **Duration** invalida un elemento **PREVIEWDURATION** .

## <a name="examples"></a>Ejemplos


```XML
<DURATION VALUE="00:00:30" />   <!-- 30 seconds -->
<DURATION VALUE="1:01.5" />     <!-- 61.5 seconds -->

```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Referencia de elementos de metarchivo de Windows Media**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Referencia de metarchivos de Windows Media**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





