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
ms.openlocfilehash: 360a4b88c8c03d2f04ad55bc65eebf6be3797c92
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160278"
---
# <a name="camschedulegetevent-method"></a>Método CAMSchedule.GetEvent

El `GetEvent` método recupera un identificador de evento, que se usa para señalar un cambio en la siguiente hora de aviso.

## <a name="syntax"></a>Sintaxis


```C++
HANDLE GetEvent();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve un identificador a un evento.

## <a name="remarks"></a>Observaciones

Si la siguiente hora de aviso cambia en otras palabras, si se agrega una nueva solicitud de aviso al frente de la lista, el programador señala este evento. El reloj debe llamar al [**método CAMSchedule::Advise**](camschedule-advise.md) para determinar la siguiente hora de aviso.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Dsschedule.h (incluir Secuencias.h)</dt> </dl>                                                                                |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CLASE CAMSchedule**](camschedule.md)
</dt> </dl>

 

 




