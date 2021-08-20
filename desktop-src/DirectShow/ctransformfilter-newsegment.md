---
description: El método NewSegment notifica al filtro que los ejemplos de medios recibidos después de esta llamada se agrupan como un segmento.
ms.assetid: 78ddaac7-9c1f-47b6-835d-dd16b1f5b01f
title: Método CTransformFilter.NewSegment (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.NewSegment
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a2cb83c376b012ae3474f87b0f8d26c7fb5560812c1d8ddcbb3ea62293797bb9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953554"
---
# <a name="ctransformfilternewsegment-method"></a>Método CTransformFilter.NewSegment

El `NewSegment` método notifica al filtro que los ejemplos de medios recibidos después de esta llamada se agrupan como un segmento.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT NewSegment(
   REFERENCE_TIME tStart,
   REFERENCE_TIME tStop,
   double         dRate
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*tStart* 
</dt> <dd>

Hora de inicio del segmento, con respecto al origen original.

</dd> <dt>

*tStop* 
</dt> <dd>

Hora de detenerse del segmento, en relación con el origen original.

</dd> <dt>

*dRate* 
</dt> <dd>

Velocidad a la que se debe procesar el segmento.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK.

## <a name="remarks"></a>Comentarios

El método [**CTransformInputPin::NewSegment**](ctransforminputpin-newsegment.md) del pin de entrada llama a este método. Este método entrega la `NewSegment` llamada a la patilla de entrada de bajada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Transfrm.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CTransformFilter (clase)**](ctransformfilter.md)
</dt> </dl>

 

 




