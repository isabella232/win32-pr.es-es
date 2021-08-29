---
description: El método GetPrivateTime recupera la hora real del reloj.
ms.assetid: ce9832cb-4b5a-49a1-9a69-d2fb90b3ed2e
title: Método CBaseReferenceClock.GetPrivateTime (Refclock.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.GetPrivateTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c8381f6e6e868fc6a57a65cf3bf124d90c035c854176265b2f9991356874e0ef
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120076505"
---
# <a name="cbasereferenceclockgetprivatetime-method"></a>Método CBaseReferenceClock.GetPrivateTime

El `GetPrivateTime` método recupera la hora real del reloj.

## <a name="syntax"></a>Sintaxis


```C++
virtual REFERENCE_TIME GetPrivateTime();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve la hora del reloj actual, en unidades de 100 nanosegundos.

## <a name="remarks"></a>Comentarios

Este método devuelve el tiempo real notificado por el reloj. Los llamadores externos usan [**el método CBaseReferenceClock::GetTime,**](cbasereferenceclock-gettime.md) que llama a este método. A diferencia **del método GetTime,** el reloj interno puede retroceder. Si esto sucede, el **método GetTime** sigue devolviendo la última vez que se informó, hasta que `GetPrivateTime` el método se activa.

Este método devuelve la hora del sistema. Invalide este método si el reloj obtiene la hora de otro origen.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Refclock.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseReferenceClock (clase)**](cbasereferenceclock.md)
</dt> </dl>

 

 




