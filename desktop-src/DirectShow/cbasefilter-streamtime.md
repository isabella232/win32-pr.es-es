---
description: El método StreamTime recupera la hora de la secuencia actual.
ms.assetid: 88a2939d-fb51-49fd-af71-21c99511de43
title: Método CBaseFilter. StreamTime (Amfilter. h)
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
ms.openlocfilehash: f4370758eb4ab15a9e53a5157550ee2129783c7f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661099"
---
# <a name="cbasefilterstreamtime-method"></a>CBaseFilter. StreamTime, método

El método **StreamTime** recupera la hora de la secuencia actual.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT StreamTime(
  [ref] CRefTime &rtStream
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*rtStream* \[ CLI\]
</dt> <dd>

Referencia a un objeto [**CRefTime**](creftime.md) que recibe la hora de la secuencia actual.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** . Entre los valores posibles se incluyen los que aparecen en la tabla siguiente.



| Código devuelto                                                                                      | Descripción                                 |
|--------------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>             | Correcto.<br/>                         |
| <dl> <dt>**VFW \_ E \_ sin \_ reloj**</dt> </dl> | No hay ningún reloj de referencia disponible.<br/> |



 

## <a name="remarks"></a>Observaciones

La hora de la secuencia se define como la hora de referencia actual (indicada por el reloj de referencia) menos la hora de inicio (especificada por [**CBaseFilter:: m \_ tStart**](cbasefilter-m-tstart.md)). La *marca de tiempo* de un ejemplo multimedia especifica el tiempo de flujo en el que se debe representar. Si aún no se ha representado una muestra con una marca de tiempo menor que la hora actual de la secuencia, se retrasa.

Este método obtiene el tiempo de flujo llamando a [**IReferenceClock:: getTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) para obtener el tiempo de referencia actual y restar la hora de inicio inicial.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Hora y relojes en DirectShow](time-and-clocks-in-directshow.md)
</dt> <dt>

[**Clase CBaseFilter**](cbasefilter.md)
</dt> </dl>

 

 




