---
description: La \_ \_ enumeración de marcas de búsqueda de DEXTERF Track \_ especifica las condiciones de límite en una búsqueda de un objeto en la escala de tiempo.
ms.assetid: 9a66ea17-5c2c-41fd-8a7b-c9918b10c8c9
title: Enumeración DEXTERF_TRACK_SEARCH_FLAGS (QEDIT. h)
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
ms.openlocfilehash: 09923d6be01bdf4a213db645a34b038dda15d86f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653821"
---
# <a name="dexterf_track_search_flags-enumeration"></a>\_ \_ Enumeración de marcas de búsqueda de DEXTERF Track \_

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

La `DEXTERF_TRACK_SEARCH_FLAGS` enumeración especifica las condiciones de límite en una búsqueda de un objeto en la escala de tiempo.

## <a name="syntax"></a>Sintaxis


```C++
typedef enum  { 
  DEXTERF_BOUNDING    = -1,
  DEXTERF_EXACTLY_AT  = 0,
  DEXTERF_FORWARDS    = 1
} DEXTERF_TRACK_SEARCH_FLAGS;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="DEXTERF_BOUNDING"></span><span id="dexterf_bounding"></span>**límite de DEXTERF \_**
</dt> <dd>

Buscar un objeto que abarque la hora especificada.

</dd> <dt>

<span id="DEXTERF_EXACTLY_AT"></span><span id="dexterf_exactly_at"></span>**DEXTERF \_ exactamente \_ en**
</dt> <dd>

Buscar un objeto que se inicia exactamente en el momento especificado.

</dd> <dt>

<span id="DEXTERF_FORWARDS"></span><span id="dexterf_forwards"></span>**reenvío de DEXTERF \_**
</dt> <dd>

Buscar un objeto que se inicia a la hora especificada o posterior.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Estas condiciones de límite se resumen en la tabla siguiente.



| Valor de enumeración    | Condición de límite                        |
|----------------------|-------------------------------------------|
| límite de DEXTERF \_    | Inicio <= hora de > TimeStop<br/> |
| DEXTERF \_ exactamente \_ en | Start = = hora                             |
| reenvío de DEXTERF \_    | Iniciar >= hora                          |



 

-   Inicio: hora de inicio del objeto recuperado.
-   Detener: hora de detención del objeto recuperado.
-   Hora: tiempo de búsqueda especificado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>QEDIT. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IAMTimelineTrack::GetSrcAtTime**](iamtimelinetrack-getsrcattime.md)
</dt> </dl>

 

 




