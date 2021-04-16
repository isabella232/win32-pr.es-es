---
description: El método GetPrivateTime recupera la hora real del reloj.
ms.assetid: ce9832cb-4b5a-49a1-9a69-d2fb90b3ed2e
title: Método CBaseReferenceClock. GetPrivateTime (Refclock. h)
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
ms.openlocfilehash: 387df10472e4913d33722492bf07601faf08e3ba
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671532"
---
# <a name="cbasereferenceclockgetprivatetime-method"></a>CBaseReferenceClock. GetPrivateTime, método

El `GetPrivateTime` método recupera la hora real del reloj.

## <a name="syntax"></a>Sintaxis


```C++
virtual REFERENCE_TIME GetPrivateTime();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve la hora actual del reloj, en unidades de 100-nanosegundos.

## <a name="remarks"></a>Observaciones

Este método devuelve el tiempo real indicado por el reloj. Los autores de llamadas externos usan el método [**CBaseReferenceClock:: getTime**](cbasereferenceclock-gettime.md) , que llama a este método. A diferencia del método **getTime** , el reloj interno puede retroceder. Si esto sucede, el método **getTime** continúa devolviendo la última vez que se informaba, hasta que el método se pone al día `GetPrivateTime` .

Este método devuelve la hora del sistema. Invalide este método si el reloj obtiene la hora de otro origen.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Refclock. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseReferenceClock**](cbasereferenceclock.md)
</dt> </dl>

 

 




