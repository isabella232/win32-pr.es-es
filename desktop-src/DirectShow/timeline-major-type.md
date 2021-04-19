---
description: La \_ \_ enumeración de tipo principal de la escala de tiempo especifica el tipo principal de un objeto.
ms.assetid: 1a5fde83-2a0a-4bcf-bffe-340a9d914885
title: Enumeración TIMELINE_MAJOR_TYPE (QEDIT. h)
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690097"
---
# <a name="timeline_major_type-enumeration"></a>\_Enumeración de tipo principal de escala de tiempo \_

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

La `TIMELINE_MAJOR_TYPE` enumeración especifica el tipo principal de un objeto.

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

<span id="TIMELINE_MAJOR_TYPE_COMPOSITE"></span><span id="timeline_major_type_composite"></span>**tipo principal de escala de tiempo \_ \_ \_ compuesto**
</dt> <dd>

Objeto compuesto. Contiene una o más pistas.

</dd> <dt>

<span id="TIMELINE_MAJOR_TYPE_TRACK"></span><span id="timeline_major_type_track"></span>**\_pista de \_ tipo \_ principal de escala de tiempo**
</dt> <dd>

Objeto Track. Contiene uno o más orígenes.

</dd> <dt>

<span id="TIMELINE_MAJOR_TYPE_SOURCE"></span><span id="timeline_major_type_source"></span>**\_origen de \_ tipo \_ principal de la escala de tiempo**
</dt> <dd>

Objeto de origen. Contiene una referencia a un origen de multimedia.

</dd> <dt>

<span id="TIMELINE_MAJOR_TYPE_TRANSITION"></span><span id="timeline_major_type_transition"></span>**\_transición de \_ tipo \_ principal de escala de tiempo**
</dt> <dd>

Objeto de transición. Define una transición entre compuestos, pistas o orígenes.

</dd> <dt>

<span id="TIMELINE_MAJOR_TYPE_EFFECT"></span><span id="timeline_major_type_effect"></span>**\_efecto de \_ tipo \_ principal de la escala de tiempo**
</dt> <dd>

Objeto de efecto. Define un efecto de entrada única que se va a aplicar a un objeto compuesto, de seguimiento o de origen.

</dd> <dt>

<span id="TIMELINE_MAJOR_TYPE_GROUP"></span><span id="timeline_major_type_group"></span>**Grupo de tipo de escala de tiempo \_ principal \_ \_**
</dt> <dd>

Objeto de grupo. Contiene una o más pistas de un tipo determinado.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>QEDIT. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IAMTimeline**](iamtimeline.md)
</dt> <dt>

[**IAMTimelineComp::GetCountOfType**](iamtimelinecomp-getcountoftype.md)
</dt> <dt>

[**IAMTimelineObj::GetTimelineType**](iamtimelineobj-gettimelinetype.md)
</dt> </dl>

 

 




