---
description: 'El método AdviseTime crea una solicitud de notificación de una captura. Este método implementa el método IReferenceClock:: AdviseTime.'
ms.assetid: 4849a04d-35f2-4a24-bf5d-f20e541f5e99
title: Método CBaseReferenceClock. AdviseTime (Refclock. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.AdviseTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 326fc5e0939803ab66e0466fbf32351387977019
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660941"
---
# <a name="cbasereferenceclockadvisetime-method"></a>CBaseReferenceClock. AdviseTime, método

El `AdviseTime` método crea una solicitud de notificación de una captura. Este método implementa el método [**IReferenceClock:: AdviseTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-advisetime) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT AdviseTime(
   REFERENCE_TIME baseTime,
   REFERENCE_TIME streamTime,
   HEVENT         hEvent,
   DWORD_PTR      *pdwAdviseToken
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*baseTime* 
</dt> <dd>

Tiempo de referencia base, en unidades de 100-nanosegundos.

</dd> <dt>

*streamTime* 
</dt> <dd>

Tiempo de desplazamiento de flujo, en unidades de 100-nanosegundos.

</dd> <dt>

*hEvent* 
</dt> <dd>

Identificador de un evento creado por el autor de la llamada.

</dd> <dt>

*pdwAdviseToken* 
</dt> <dd>

Puntero a una variable que recibe un identificador para la solicitud de notificación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los valores **HRESULT** que se muestran en la tabla siguiente.



| Código devuelto                                                                                   | Descripción                          |
|-----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>          | Correcto<br/>                   |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Valores de hora no válidos<br/>       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Error<br/>                   |
| <dl> <dt>**\_puntero E**</dt> </dl>     | Argumento de puntero **nulo**<br/> |



 

## <a name="remarks"></a>Observaciones

Este método crea una solicitud de notificación de una captura para el tiempo de referencia *baseTime*  +  *streamTime*. La suma debe ser mayor que cero y menor que \_ el tiempo máximo, o el método devuelve E \_ INVALIDARG. En el momento solicitado, el reloj señala el evento especificado en el parámetro *hEvent* .

Para cancelar la notificación antes de que se alcance el tiempo, llame al método [**CBaseReferenceClock:: Unadvise**](cbasereferenceclock-unadvise.md) y pase el valor de *pdwAdviseToken* devuelto desde esta llamada. Una vez que se ha producido la notificación, el reloj la borra automáticamente, por lo que no es necesario llamar a **unvise**. Sin embargo, no es un error hacerlo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Refclock. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseReferenceClock**](cbasereferenceclock.md)
</dt> </dl>

 

 




