---
description: El método GetEvent recupera un identificador de evento, que se usa para señalar un cambio en la próxima hora de aviso.
ms.assetid: 2548a321-df65-4a5b-9e6a-8bbc031254c7
title: Método CAMSchedule.GetEvent (Dsschedule.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMSchedule.GetEvent
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9e5126fde495c9553975daaf2db9e82de4ab4530a4629d217eba51818e20d1f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119689085"
---
# <a name="camschedulegetevent-method"></a>Método CAMSchedule.GetEvent

El `GetEvent` método recupera un identificador de evento, que se usa para señalar un cambio en la próxima hora de aviso.

## <a name="syntax"></a>Sintaxis


```C++
HANDLE GetEvent();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve un identificador a un evento.

## <a name="remarks"></a>Comentarios

Si la hora del aviso siguiente cambia en otras palabras, si se agrega una nueva solicitud de aviso al frente de la lista, el programador señala este evento. El reloj debe llamar al [**método CAMSchedule::Advise**](camschedule-advise.md) para determinar la siguiente hora de aviso.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Dsschedule.h (incluir Secuencias.h)</dt> </dl>                                                                                |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CLASE CAMSchedule**](camschedule.md)
</dt> </dl>

 

 




