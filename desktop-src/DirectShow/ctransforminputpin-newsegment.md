---
description: El método NewSegment notifica al pin que los ejemplos de medios recibidos después de esta llamada se agrupan como un segmento. Este método implementa el método IPin::NewSegment.
ms.assetid: 8925b8b5-13dd-4127-82d8-96525bd4d6fc
title: Método CTransformInputPin.NewSegment (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.NewSegment
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 25c455fe5ec6ddf9157e991b70b468ace653daa9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127255440"
---
# <a name="ctransforminputpinnewsegment-method"></a>Método CTransformInputPin.NewSegment

El `NewSegment` método notifica al pin que los ejemplos de medios recibidos después de esta llamada se agrupan como un segmento. Este método implementa el [**método IPin::NewSegment.**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT NewSegment(
   REFERENCE_TIME tStart,
   REFERENCE_TIME tStop,
   double         dRate
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*tStart* 
</dt> <dd>

Hora de inicio del segmento.

</dd> <dt>

*tStop* 
</dt> <dd>

Hora de detenerse del segmento.

</dd> <dt>

*dRate* 
</dt> <dd>

Velocidad del segmento.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK u otro valor **HRESULT.**

## <a name="remarks"></a>Observaciones

Este método invalida el [**método CBasePin::NewSegment.**](cbasepin-newsegment.md) Llama al método [**CTransformFilter::NewSegment**](ctransformfilter-newsegment.md) del filtro para entregar la llamada de nivel inferior.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Transfrm.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



 

 




