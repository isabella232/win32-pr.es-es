---
description: El método NewSegment notifica al pin que los ejemplos de medios recibidos después de esta llamada se agrupan como un segmento. Implementa el método IPin::NewSegment.
ms.assetid: e334d5a7-0398-496c-882c-bf73e6545867
title: Método CBasePin.NewSegment (Amfilter.h)
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
ms.openlocfilehash: ed3ffc9cc0656509b29a6c32baeaf7311437a79e8402fbae0727cf9f93a30abe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119384555"
---
# <a name="cbasepinnewsegment-method"></a>Método CBasePin.NewSegment

El `NewSegment` método notifica al pin que los ejemplos de medios recibidos después de esta llamada se agrupan como un segmento. Implementa el [**método IPin::NewSegment.**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment)

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

Posición del medio inicial del segmento, en unidades de 100 nanosegundos.

</dd> <dt>

*tStop* 
</dt> <dd>

Posición del medio final del segmento, en unidades de 100 nanosegundos.

</dd> <dt>

*dRate* 
</dt> <dd>

Velocidad a la que se debe procesar este segmento, como porcentaje de la velocidad original.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK.

## <a name="remarks"></a>Comentarios

Este método establece las variables [**miembro CBasePin::m \_ tStart**](cbasepin-m-tstart.md), [**CBasePin::m \_ tStop**](cbasepin-m-tstop.md)y [**CBasePin::m \_ dRate.**](cbasepin-m-drate.md) En la clase derivada, invalide este método para pasar la notificación de nivel inferior.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CBasePin (clase)**](cbasepin.md)
</dt> </dl>

 

 




