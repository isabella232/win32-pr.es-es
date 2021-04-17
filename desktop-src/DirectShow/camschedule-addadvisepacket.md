---
description: El método AddAdvisePacket agrega una solicitud de notificación a la lista de solicitudes pendientes.
ms.assetid: 138d8404-7d28-47cc-91b4-4733a113ac7a
title: Método CAMSchedule. AddAdvisePacket (Dsschedule. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMSchedule.AddAdvisePacket
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5dd9586b09586c12f1a30f45b512336831372295
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671117"
---
# <a name="camscheduleaddadvisepacket-method"></a>CAMSchedule. AddAdvisePacket, método

El `AddAdvisePacket` método agrega una solicitud de notificación a la lista de solicitudes pendientes.

## <a name="syntax"></a>Sintaxis


```C++
DWORD_PTR AddAdvisePacket(
  [ref] const REFERENCE_TIME &time1,
  [ref] const REFERENCE_TIME &time2,
              HANDLE         hNotify,
              BOOL           bPeriodic
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*tiempo1* \[ CLI\]
</dt> <dd>

Hora solicitada para el aviso.

</dd> <dt>

*al tiempo2?* \[ CLI\]
</dt> <dd>

Para solicitudes de notificación periódicas, el tiempo entre notificaciones. Este parámetro se omite si *bPeriodic* es **false**.

</dd> <dt>

*hNotify* 
</dt> <dd>

Identificador de un semáforo si *bPeriodic* es **true** o identificador de un evento si *bPeriodic* es **false**.

</dd> <dt>

*bPeriodic* 
</dt> <dd>

Valor booleano que especifica si se debe agregar una notificación periódica o una notificación de una captura. Si es **true**, la notificación es periódica; el parámetro *al tiempo2?* especifica el tiempo entre notificaciones. Si **es false**, la notificación se produce una sola vez.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un identificador para la solicitud de notificación (la "cookie"). Si se produce un error en el método, el valor devuelto es cero.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Dsschedule. h (incluir streams. h)</dt> </dl>                                                                                |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CAMSchedule**](camschedule.md)
</dt> </dl>

 

 




