---
description: El método GetEvent recupera un identificador de evento, que se usa para indicar un cambio en la hora del siguiente aviso.
ms.assetid: 2548a321-df65-4a5b-9e6a-8bbc031254c7
title: Método CAMSchedule. GetEvent (Dsschedule. h)
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660631"
---
# <a name="camschedulegetevent-method"></a>CAMSchedule. GetEvent, método

El `GetEvent` método recupera un identificador de evento, que se usa para indicar un cambio en la hora del siguiente aviso.

## <a name="syntax"></a>Sintaxis


```C++
HANDLE GetEvent();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve un identificador para un evento.

## <a name="remarks"></a>Observaciones

Si la hora del siguiente aviso cambia en otras palabras, si se agrega una nueva solicitud de notificación al principio de la lista, el programador indica este evento. El reloj debe llamar al método [**CAMSchedule:: Advise**](camschedule-advise.md) para determinar la hora del siguiente aviso.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Dsschedule. h (incluir streams. h)</dt> </dl>                                                                                |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CAMSchedule**](camschedule.md)
</dt> </dl>

 

 




