---
description: 'Método CBaseFilter.StreamTime: el método StreamTime recupera el tiempo de transmisión actual.'
ms.assetid: 88a2939d-fb51-49fd-af71-21c99511de43
title: Método CBaseFilter.StreamTime (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.StreamTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f3334ac273a733c3f0591b76af7e76460997a199
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108120073"
---
# <a name="cbasefilterstreamtime-method"></a>Método CBaseFilter.StreamTime

El **método StreamTime** recupera el tiempo de secuencia actual.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT StreamTime(
  [ref] CRefTime &rtStream
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*rtStream* \[ Ref\]
</dt> <dd>

Referencia a un [**objeto CRefTime**](creftime.md) que recibe el tiempo de secuencia actual.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.** Los valores posibles incluyen los enumerados en la tabla siguiente.



| Código devuelto                                                                                      | Descripción                                 |
|--------------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>             | Correcto.<br/>                         |
| <dl> <dt>**VFW \_ E \_ NO \_ CLOCK**</dt> </dl> | No hay ningún reloj de referencia disponible.<br/> |



 

## <a name="remarks"></a>Comentarios

La hora de la secuencia se define como la hora de referencia actual (según lo indicado por el reloj de referencia) menos la hora de inicio (especificada por [**CBaseFilter::m \_ tStart**](cbasefilter-m-tstart.md)). La marca de tiempo de *un ejemplo multimedia* especifica el tiempo de secuencia en el que se debe representar. Si aún no se ha representado un ejemplo con una marca de tiempo inferior a la hora de transmisión actual, es tarde.

Este método obtiene el tiempo de secuencia llamando a [**IReferenceClock::GetTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) para obtener la hora de referencia actual y restando la hora de inicio inicial.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Streams.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Hora y relojes en DirectShow](time-and-clocks-in-directshow.md)
</dt> <dt>

[**CBaseFilter (clase)**](cbasefilter.md)
</dt> </dl>

 

 




