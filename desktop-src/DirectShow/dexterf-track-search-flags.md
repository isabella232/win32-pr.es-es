---
description: La enumeración DE MARCADORES DE BÚSQUEDA DE TRACK DE LA MARCA DE TRACKF especifica las condiciones de límite en \_ una búsqueda de un objeto en la escala de \_ \_ tiempo.
ms.assetid: 9a66ea17-5c2c-41fd-8a7b-c9918b10c8c9
title: DEXTERF_TRACK_SEARCH_FLAGS enumeración (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DEXTERF_TRACK_SEARCH_FLAGS
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: 55d7c70dffbf57ae4d9788a10dfea02911a998e21ab5ea8e3d9ad7fffcf91624
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952944"
---
# <a name="dexterf_track_search_flags-enumeration"></a>ENUMERACIÓN DE MARCADORES DE BÚSQUEDA DE TRACK DE LA MARCA DE TRACKF \_ \_ \_

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

La `DEXTERF_TRACK_SEARCH_FLAGS` enumeración especifica las condiciones de límite en una búsqueda de un objeto en la escala de tiempo.

## <a name="syntax"></a>Syntax


```C++
typedef enum  { 
  DEXTERF_BOUNDING    = -1,
  DEXTERF_EXACTLY_AT  = 0,
  DEXTERF_FORWARDS    = 1
} DEXTERF_TRACK_SEARCH_FLAGS;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="DEXTERF_BOUNDING"></span><span id="dexterf_bounding"></span>**LÍMITE \_ DE LAF DE DESFAS**
</dt> <dd>

Busque un objeto que abarque el tiempo especificado.

</dd> <dt>

<span id="DEXTERF_EXACTLY_AT"></span><span id="dexterf_exactly_at"></span>**EXACTLY \_ AT DE \_ LAF**
</dt> <dd>

Busque un objeto que se inicie exactamente en el momento especificado.

</dd> <dt>

<span id="DEXTERF_FORWARDS"></span><span id="dexterf_forwards"></span>**\_REENVIADORES DE REENVIADORES DE DESFAS**
</dt> <dd>

Busque un objeto que se inicie en el momento especificado o posterior.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Estas condiciones de límite se resumen en la tabla siguiente.



| Valor de enumeración    | Condición de límite                        |
|----------------------|-------------------------------------------|
| LÍMITE \_ DE LAF DE DESFAS    | Start <= TimeStop > Time<br/> |
| EXACTLY \_ AT DE \_ LAF | Start == Time                             |
| \_REENVIADORES DE REENVIADORES DE DESFAS    | Start >= Time                          |



 

-   Inicio: hora de inicio del objeto recuperado.
-   Stop: tiempo de detenerse del objeto recuperado.
-   Hora: tiempo de búsqueda especificado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Qedit.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IAMTimelineTrack::GetSrcAtTime**](iamtimelinetrack-getsrcattime.md)
</dt> </dl>

 

 




