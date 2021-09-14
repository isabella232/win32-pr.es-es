---
description: El método DeliverNewSegment entrega una notificación de nuevo segmento al pin de entrada conectado.
ms.assetid: 304f0267-88e0-4642-98a2-68ce973bdeab
title: Método CBaseOutputPin.DeliverNewSegment (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.DeliverNewSegment
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3eb6d31a50095affdf38d44b69040304674ec6fe
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061373"
---
# <a name="cbaseoutputpindelivernewsegment-method"></a>Método CBaseOutputPin.DeliverNewSegment

El `DeliverNewSegment` método entrega una notificación de nuevo segmento al pin de entrada conectado.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT DeliverNewSegment(
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

Velocidad a la que se debe procesar este segmento, como porcentaje de la tasa original.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.** Los valores posibles incluyen los enumerados en la tabla siguiente.



| Código devuelto                                                                                           | Descripción                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                  | Correcto.<br/>              |
| <dl> <dt>**VFW \_ E \_ NO \_ CONECTADO**</dt> </dl> | El pin no está conectado.<br/> |



 

## <a name="remarks"></a>Observaciones

Este método llama al [**método IPin::NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) en el pin de entrada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CBaseOutputPin (clase)**](cbaseoutputpin.md)
</dt> </dl>

 

 




