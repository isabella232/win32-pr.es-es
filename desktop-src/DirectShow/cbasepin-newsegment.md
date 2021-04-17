---
description: 'El método NewSegment notifica al pin que los ejemplos de multimedia recibieron después de que esta llamada se agrupe como un segmento. Implementa el método IPin:: NewSegment.'
ms.assetid: e334d5a7-0398-496c-882c-bf73e6545867
title: Método CBasePin. NewSegment (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.NewSegment
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1f128ce8cb2fee5479efeddd5932d0392b92a6fc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660645"
---
# <a name="cbasepinnewsegment-method"></a>CBasePin. NewSegment, método

El `NewSegment` método notifica al pin que los ejemplos de multimedia recibieron después de que esta llamada se agrupe como un segmento. Implementa el método [**IPin:: NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) .

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

Posición del medio inicial del segmento, en unidades de 100-nanosegundos.

</dd> <dt>

*tStop* 
</dt> <dd>

Fin de la posición del medio del segmento, en unidades de 100-nanosegundos.

</dd> <dt>

*dRate* 
</dt> <dd>

Velocidad a la que se debe procesar este segmento, como porcentaje de la tasa original.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ correcto.

## <a name="remarks"></a>Observaciones

Este método establece las variables de miembro [**CBasePin:: m \_ tStart**](cbasepin-m-tstart.md), [**CBasePin:: m \_ tStop**](cbasepin-m-tstop.md)y [**CBasePin:: m \_ dRate**](cbasepin-m-drate.md) . En la clase derivada, Invalide este método para pasar la notificación de nivel inferior.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBasePin**](cbasepin.md)
</dt> </dl>

 

 




