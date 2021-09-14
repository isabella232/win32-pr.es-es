---
description: La \_ enumeración TIMELINE MAJOR \_ TYPE especifica el tipo principal de un objeto .
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
ms.openlocfilehash: 25c3e829aa73d1da78c110ffd148fb0ebaaebdd9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126891657"
---
# <a name="timeline_major_type-enumeration"></a>TIMELINE \_ MAJOR \_ TYPE (enumeración)

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

La `TIMELINE_MAJOR_TYPE` enumeración especifica el tipo principal de un objeto .

## <a name="syntax"></a>Sintaxis


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

<span id="TIMELINE_MAJOR_TYPE_TRACK"></span><span id="timeline_major_type_track"></span>**PISTA DE \_ TIPO PRINCIPAL DE ESCALA DE \_ \_ TIEMPO**
</dt> <dd>

Realizar un seguimiento del objeto. Contiene uno o varios orígenes.

</dd> <dt>

<span id="TIMELINE_MAJOR_TYPE_SOURCE"></span><span id="timeline_major_type_source"></span>**ORIGEN DE \_ TIPO PRINCIPAL DE ESCALA DE \_ \_ TIEMPO**
</dt> <dd>

Objeto de origen. Contiene una referencia a un origen multimedia.

</dd> <dt>

<span id="TIMELINE_MAJOR_TYPE_TRANSITION"></span><span id="timeline_major_type_transition"></span>**TRANSICIÓN \_ DE TIPO PRINCIPAL DE ESCALA DE \_ \_ TIEMPO**
</dt> <dd>

Objeto de transición. Define una transición entre compuestos, pistas o orígenes.

</dd> <dt>

<span id="TIMELINE_MAJOR_TYPE_EFFECT"></span><span id="timeline_major_type_effect"></span>**EFECTO DE \_ TIPO PRINCIPAL DE ESCALA DE \_ \_ TIEMPO**
</dt> <dd>

Objeto de efecto. Define un efecto de entrada única que se va a aplicar a un objeto compuesto, de seguimiento o de origen.

</dd> <dt>

<span id="TIMELINE_MAJOR_TYPE_GROUP"></span><span id="timeline_major_type_group"></span>**GRUPO \_ DE TIPOS PRINCIPAL DE ESCALA DE \_ \_ TIEMPO**
</dt> <dd>

Objeto de grupo. Contiene una o varias pistas de un tipo determinado.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Qedit.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IAMTimeline**](iamtimeline.md)
</dt> <dt>

[**IAMTimelineComp::GetCountOfType**](iamtimelinecomp-getcountoftype.md)
</dt> <dt>

[**IAMTimelineObj::GetTimelineType**](iamtimelineobj-gettimelinetype.md)
</dt> </dl>

 

 




