---
description: 'El método SetTime establece los tiempos de flujo en los que este ejemplo debe comenzar y finalizar. Este método implementa el método IMediaSample:: SetTime.'
ms.assetid: cab4907f-eb6f-4444-9b41-1f95a6ecffed
title: Método CMediaSample. SetTime (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.SetTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 935c4f3aa565b291e459d36e067805944b4fd6b2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105678888"
---
# <a name="cmediasamplesettime-method"></a>CMediaSample. SetTime, método

El `SetTime` método establece los tiempos de flujo en los que este ejemplo debe comenzar y finalizar. Este método implementa el método [**IMediaSample:: setTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-settime) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetTime(
   REFERENCE_TIME *pTimeStart,
   REFERENCE_TIME *pTimeEnd
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pTimeStart* 
</dt> <dd>

Puntero a la hora de flujo en la que comienza el ejemplo, en unidades de 100-nanosegundos o **null**.

</dd> <dt>

*pTimeEnd* 
</dt> <dd>

Puntero a la hora de flujo en la que finaliza el ejemplo, en unidades 100-nanosegundos, o **null**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ correcto.

## <a name="remarks"></a>Observaciones

Este método establece las variables de miembro de [**Inicio CMediaSample:: m \_ Start**](cmediasample-m-start.md) y [**CMediaSample:: m \_ End**](cmediasample-m-end.md) , que especifican las marcas de tiempo. También actualiza la variable miembro [**CMediaSample:: m \_ dwFlags**](cmediasample-m-dwflags.md) , que especifica si las marcas de tiempo son válidas.

Para obtener información acerca de las marcas de tiempo, consulte [hora y relojes en DirectShow](time-and-clocks-in-directshow.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CMediaSample**](cmediasample.md)
</dt> </dl>

 

 




