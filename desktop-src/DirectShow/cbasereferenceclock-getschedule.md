---
description: El método GetSchedule recupera un puntero al objeto de programación del reloj.
ms.assetid: ae509f16-d85f-4365-8cf2-c6585cbbdc3d
title: Método CBaseReferenceClock.GetSchedule (Refclock.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.GetSchedule
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6be5c4ed76573428967138682b478a54859e4ca97213f132ff805a0e83be0b50
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117822841"
---
# <a name="cbasereferenceclockgetschedule-method"></a>CBaseReferenceClock.GetSchedule (método)

El `GetSchedule` método recupera un puntero al objeto de programación del reloj.

## <a name="syntax"></a>Sintaxis


```C++
CAMSchedule* GetSchedule();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve la variable [**miembro CBaseReferenceClock::m \_ pSchedule.**](cbasereferenceclock-m-pschedule.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Refclock.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CBaseReferenceClock (clase)**](cbasereferenceclock.md)
</dt> </dl>

 

 




