---
description: El método AdviseTime crea una solicitud de asesoramiento de un solo plano. Este método implementa el método IReferenceClock::AdviseTime.
ms.assetid: 4849a04d-35f2-4a24-bf5d-f20e541f5e99
title: Método CBaseReferenceClock.AdviseTime (Refclock.h)
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
ms.openlocfilehash: e50b864a63cdd021d82c0a2a73f4f9c3acb68d1afb1f6a2dcd8d8d575966a5fc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119502795"
---
# <a name="cbasereferenceclockadvisetime-method"></a>Método CBaseReferenceClock.AdviseTime

El `AdviseTime` método crea una solicitud de aviso de una sola toma. Este método implementa el [**método IReferenceClock::AdviseTime.**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-advisetime)

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

Tiempo de referencia base, en unidades de 100 nanosegundos.

</dd> <dt>

*streamTime* 
</dt> <dd>

Tiempo de desplazamiento de flujo, en unidades de 100 nanosegundos.

</dd> <dt>

*hEvent* 
</dt> <dd>

Controlar un evento creado por el autor de la llamada.

</dd> <dt>

*pdwAdviseToken* 
</dt> <dd>

Puntero a una variable que recibe un identificador para la solicitud de aviso.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los **valores HRESULT** que se muestran en la tabla siguiente.



| Código devuelto                                                                                   | Descripción                          |
|-----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Success<br/>                   |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Valores de hora no válidos<br/>       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Error<br/>                   |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl>     | **Argumento de** puntero NULL<br/> |



 

## <a name="remarks"></a>Comentarios

Este método crea una solicitud de aviso de un solo uso para el tiempo *de referencia baseTime*  +  *streamTime*. La suma debe ser mayor que cero y menor que MAX TIME, o bien \_ el método devuelve E \_ INVALIDARG. A la hora solicitada, el reloj señala el evento especificado en el *parámetro hEvent.*

Para cancelar la notificación antes de que se alcance la hora, llame al método [**CBaseReferenceClock::Unadvise**](cbasereferenceclock-unadvise.md) y pase el valor *pdwAdviseToken* devuelto por esta llamada. Una vez que se ha producido la notificación, el reloj la borra automáticamente, por lo que no es necesario llamar **a Unadvise**. Sin embargo, no es un error hacerlo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Refclock.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseReferenceClock (clase)**](cbasereferenceclock.md)
</dt> </dl>

 

 




