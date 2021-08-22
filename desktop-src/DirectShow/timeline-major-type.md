---
description: La \_ enumeración TIMELINE MAJOR TYPE especifica el tipo principal de un \_ objeto.
ms.assetid: 1a5fde83-2a0a-4bcf-bffe-340a9d914885
title: TIMELINE_MAJOR_TYPE enumeración (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TIMELINE_MAJOR_TYPE
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: b18088a9d01b263c80a4ff941a6b7720043da708eaeaebf4f79a2084d1ed258f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119501725"
---
# <a name="timeline_major_type-enumeration"></a>Timeline \_ MAJOR \_ TYPE (enumeración)

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

La `TIMELINE_MAJOR_TYPE` enumeración especifica el tipo principal de un objeto .

## <a name="syntax"></a>Syntax


```C++
typedef enum  { 
  TIMELINE_MAJOR_TYPE_COMPOSITE   = 1,
  TIMELINE_MAJOR_TYPE_TRACK       = 2,
  TIMELINE_MAJOR_TYPE_SOURCE      = 4,
  TIMELINE_MAJOR_TYPE_TRANSITION  = 8,
  TIMELINE_MAJOR_TYPE_EFFECT      = 16,
  TIMELINE_MAJOR_TYPE_GROUP       = 128
} TIMELINE_MAJOR_TYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="TIMELINE_MAJOR_TYPE_COMPOSITE"></span><span id="timeline_major_type_composite"></span>**TIMELINE \_ MAJOR \_ TYPE \_ COMPOSITE**
</dt> <dd>

Objeto compuesto. Contiene una o varias pistas.

</dd> <dt>

<span id="TIMELINE_MAJOR_TYPE_TRACK"></span><span id="timeline_major_type_track"></span>**SEGUIMIENTO DE \_ TIPO PRINCIPAL DE ESCALA DE \_ \_ TIEMPO**
</dt> <dd>

Objeto de seguimiento. Contiene uno o varios orígenes.

</dd> <dt>

<span id="TIMELINE_MAJOR_TYPE_SOURCE"></span><span id="timeline_major_type_source"></span>**ORIGEN \_ DE TIPO PRINCIPAL DE ESCALA DE \_ \_ TIEMPO**
</dt> <dd>

Objeto de origen. Contiene una referencia a un origen multimedia.

</dd> <dt>

<span id="TIMELINE_MAJOR_TYPE_TRANSITION"></span><span id="timeline_major_type_transition"></span>**TRANSICIÓN \_ DE TIPO PRINCIPAL DE ESCALA DE \_ \_ TIEMPO**
</dt> <dd>

Objeto de transición. Define una transición entre compuestos, pistas u orígenes.

</dd> <dt>

<span id="TIMELINE_MAJOR_TYPE_EFFECT"></span><span id="timeline_major_type_effect"></span>**EFECTO DE \_ TIPO PRINCIPAL DE ESCALA DE \_ \_ TIEMPO**
</dt> <dd>

Objeto de efecto. Define un efecto de entrada única que se va a aplicar a un objeto compuesto, de seguimiento u de origen.

</dd> <dt>

<span id="TIMELINE_MAJOR_TYPE_GROUP"></span><span id="timeline_major_type_group"></span>**GRUPO \_ DE TIPOS PRINCIPALES DE ESCALA DE \_ \_ TIEMPO**
</dt> <dd>

Objeto de grupo. Contiene una o varias pistas de un tipo determinado.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Qedit.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IAMTimeline**](iamtimeline.md)
</dt> <dt>

[**IAMTimelineComp::GetCountOfType**](iamtimelinecomp-getcountoftype.md)
</dt> <dt>

[**IAMTimelineObj::GetTimelineType**](iamtimelineobj-gettimelinetype.md)
</dt> </dl>

 

 




