---
description: El método Advise envía todas las solicitudes que están programadas para una hora especificada o anterior.
ms.assetid: 09ea84b7-517a-4ea6-9e03-0d9cd8f72e1f
title: Método CAMSchedule. Advise (Dsschedule. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMSchedule.Advise
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 70880243cef294ebe747463cd11737027faf9277
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671116"
---
# <a name="camscheduleadvise-method"></a>CAMSchedule. Advise (método)

El `Advise` método envía todas las solicitudes que están programadas para una hora especificada o anterior.

## <a name="syntax"></a>Sintaxis


```C++
REFERENCE_TIME Advise(
  [ref] const REFERENCE_TIME &rtTime
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*rtTime* \[ CLI\]
</dt> <dd>

Valor que especifica el tiempo de referencia actual.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve la hora de referencia de la siguiente solicitud de notificación programada o el \_ tiempo máximo si no hay ninguna.

## <a name="remarks"></a>Observaciones

Cuando el reloj llama a este método, especifica el tiempo de referencia actual. Scheduler determina qué solicitudes de notificaciones han expirado, si hay alguna, y las envía. Si expira una solicitud de una captura, el programador la elimina. Si una solicitud periódica expira, Scheduler la vuelve a programar para el siguiente tiempo de notificación. El método devuelve la hora de la siguiente solicitud pendiente.

Para enviar una solicitud de notificación, el programador indica el evento o semáforo proporcionado en el parámetro *hNotify* del método [**CAMSchedule:: AddAdvisePacket**](camschedule-addadvisepacket.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Dsschedule. h (incluir streams. h)</dt> </dl>                                                                                |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CAMSchedule**](camschedule.md)
</dt> </dl>

 

 




