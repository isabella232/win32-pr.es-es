---
description: El método NewSegment notifica al filtro que los ejemplos multimedia recibidos después de que esta llamada se agrupe como un segmento.
ms.assetid: 78ddaac7-9c1f-47b6-835d-dd16b1f5b01f
title: Método CTransformFilter. NewSegment (Transfrm. h)
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
ms.openlocfilehash: 0fd046288886d3e7619419dd591dd94310f56020
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661025"
---
# <a name="ctransformfilternewsegment-method"></a>CTransformFilter. NewSegment, método

El `NewSegment` método notifica al filtro que los ejemplos multimedia recibidos después de que esta llamada se agrupe como un segmento.

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

Hora de inicio del segmento, relativa al origen original.

</dd> <dt>

*tStop* 
</dt> <dd>

Hora de detención del segmento, relativa al origen original.

</dd> <dt>

*dRate* 
</dt> <dd>

Velocidad a la que se debe procesar el segmento.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ correcto.

## <a name="remarks"></a>Observaciones

El método [**CTransformInputPin:: NewSegment**](ctransforminputpin-newsegment.md) del PIN de entrada llama a este método. Este método entrega la `NewSegment` llamada al pin de entrada de nivel inferior.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Transfrm. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CTransformFilter**](ctransformfilter.md)
</dt> </dl>

 

 




