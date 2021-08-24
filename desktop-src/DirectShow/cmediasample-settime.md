---
description: El método SetTime establece los tiempos de secuencia en los que debe comenzar y finalizar este ejemplo. Este método implementa el método IMediaSample::SetTime.
ms.assetid: cab4907f-eb6f-4444-9b41-1f95a6ecffed
title: Método CMediaSample.SetTime (Amfilter.h)
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
ms.openlocfilehash: be9028db35cb6d74623bde77fac21e32793de436ea2f80d2f513687c15d1b64c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118156517"
---
# <a name="cmediasamplesettime-method"></a>Método CMediaSample.SetTime

El `SetTime` método establece las horas de transmisión en las que debe comenzar y finalizar este ejemplo. Este método implementa el [**método IMediaSample::SetTime.**](/windows/desktop/api/Strmif/nf-strmif-imediasample-settime)

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

Puntero al tiempo de secuencia en el que comienza el ejemplo, en unidades de 100 nanosegundos o **NULL.**

</dd> <dt>

*pTimeEnd* 
</dt> <dd>

Puntero al tiempo de secuencia en el que finaliza el ejemplo, en unidades de 100 nanosegundos, o **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK.

## <a name="remarks"></a>Comentarios

Este método establece las variables [**miembro CMediaSample::m \_ Start**](cmediasample-m-start.md) y [**CMediaSample::m \_ End,**](cmediasample-m-end.md) que especifican las marcas de tiempo. También actualiza la variable [**miembro CMediaSample::m \_ dwFlags,**](cmediasample-m-dwflags.md) que especifica si las marcas de tiempo son válidas.

Para obtener información sobre las marcas de tiempo, vea [Time and Clocks in DirectShow](time-and-clocks-in-directshow.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CMediaSample (clase)**](cmediasample.md)
</dt> </dl>

 

 




