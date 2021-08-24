---
description: El método NewSegment notifica al pin que los ejemplos multimedia recibidos después de esta llamada se agrupan como un segmento. Este método implementa el método IPin::NewSegment.
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
ms.openlocfilehash: c522755fe898717f0c06af9698be07ab2ebca491666982d6ff62756ef48ae08f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119907425"
---
# <a name="ctransforminputpinnewsegment-method"></a>Método CTransformInputPin.NewSegment

El `NewSegment` método notifica al pin que los ejemplos multimedia recibidos después de esta llamada se agrupan como un segmento. Este método implementa el [**método IPin::NewSegment.**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment)

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

Tiempo de detenerse del segmento.

</dd> <dt>

*dRate* 
</dt> <dd>

Velocidad del segmento.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK u otro valor **HRESULT.**

## <a name="remarks"></a>Comentarios

Este método invalida el [**método CBasePin::NewSegment.**](cbasepin-newsegment.md) Llama al método [**CTransformFilter::NewSegment**](ctransformfilter-newsegment.md) del filtro para entregar la llamada de nivel inferior.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Transfrm.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



 

 




