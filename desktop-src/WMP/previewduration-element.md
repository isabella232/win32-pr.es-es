---
title: Elemento PREVIEWDURATION
description: El elemento PREVIEWDURATION define la cantidad de tiempo que se reproduce un clip en el modo de vista previa.
ms.assetid: 428a4e3d-9c08-4b6c-acc7-b630aab37de3
keywords:
- Elemento PREVIEWDURATION Media Player Windows
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708283"
---
# <a name="previewduration-element"></a>Elemento PREVIEWDURATION

El elemento **PREVIEWDURATION** define la cantidad de tiempo que se reproduce un clip en el modo de vista previa.

``` syntax
<PREVIEWDURATION
   VALUE = "hh:mm:ss.fract"
/>
```

## <a name="attributes"></a>Atributos

**Valor** (obligatorio)

Período de tiempo (en horas, minutos, segundos y centésimas de segundo) que el clip reproduce en el modo de vista previa.

## <a name="parentchild-elements"></a>Elementos primarios y secundarios



| Hierarchy       | Elementos                    |
|-----------------|-----------------------------|
| Elementos primarios | **ASX**, **entry**, **ref** |
| Elementos secundarios  | Ninguno                        |



 

## <a name="remarks"></a>Observaciones

Este elemento define el período de tiempo que un clip se reproduce en el modo de vista previa. Si este elemento aparece dentro de un elemento **entry** o **ref** , se aplica al clip definido por ese elemento. Si aparece dentro del ámbito de un elemento **ASX** , se aplica a todos los clips del metarchivo. Un elemento **PREVIEWDURATION** de un elemento **ref** tiene prioridad sobre uno en un **elemento** entry y tiene prioridad sobre un elemento **PREVIEWDURATION** en un elemento **ASX** . Si no se define ningún elemento **PREVIEWDURATION** para un clip, la hora de la vista previa predeterminada es de 10 segundos.

Si hay un elemento **STARTTIME** o **STARTMARKER** para el clip, Windows Media Player representa el clip comenzando en el punto definido por uno de estos elementos. en caso contrario, se representa desde el principio del clip. El clip se detiene normalmente si es menor que el tiempo definido por el elemento **PREVIEWDURATION** .

El elemento **Duration** invalida un elemento **PREVIEWDURATION** .

## <a name="examples"></a>Ejemplos


```XML
<PREVIEWDURATION VALUE="0:30.0" />
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

 

 





