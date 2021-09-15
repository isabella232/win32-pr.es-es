---
title: Elemento PREVIEWDURATION
description: El elemento PREVIEWDURATION define la duración de reproducción de un clip en modo de vista previa.
ms.assetid: 428a4e3d-9c08-4b6c-acc7-b630aab37de3
keywords:
- Elemento PREVIEWDURATION Reproductor de Windows Media
topic_type:
- apiref
api_name:
- PREVIEWDURATION Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a944e86a4bd82bf57961d4d6b474c34afadba6b4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359447"
---
# <a name="previewduration-element"></a>Elemento PREVIEWDURATION

El **elemento PREVIEWDURATION** define la duración de reproducción de un clip en modo de vista previa.

``` syntax
<PREVIEWDURATION
   VALUE = "hh:mm:ss.fract"
/>
```

## <a name="attributes"></a>Atributos

**VALUE** (obligatorio)

Tiempo (en horas, minutos, segundos y centésimas de segundo) que el clip reproduce en modo de vista previa.

## <a name="parentchild-elements"></a>Elementos primarios y secundarios



| Hierarchy       | Elementos                    |
|-----------------|-----------------------------|
| Elementos primarios | **ASX**, **ENTRY**, **REF** |
| Elementos secundarios  | Ninguno                        |



 

## <a name="remarks"></a>Observaciones

Este elemento define el período de tiempo que un clip se reproduce en modo de vista previa. Si este elemento aparece dentro de **un elemento ENTRY** o un elemento **REF,** se aplica al clip definido por ese elemento. Si aparece dentro del ámbito de un **elemento ASX,** se aplica a cada clip del metarchivo. Un **elemento PREVIEWDURATION** de un elemento **REF** tiene prioridad sobre uno en un elemento **ENTRY** y tiene prioridad sobre un **elemento PREVIEWDURATION** en un **elemento ASX.** Si no se define ningún elemento **PREVIEWDURATION** para un clip, el tiempo de vista previa predeterminado es de 10 segundos.

Si hay un **elemento STARTTIME** o **STARTMARKER** para el clip, Reproductor de Windows Media el clip a partir del punto definido por uno de estos elementos; de lo contrario, se representa desde el principio del clip. El clip se detiene normalmente si es más corto que el tiempo definido por el **elemento PREVIEWDURATION.**

El **elemento DURATION** invalida un elemento **PREVIEWDURATION.**

## <a name="examples"></a>Ejemplos


```XML
<PREVIEWDURATION VALUE="0:30.0" />
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

 

 





