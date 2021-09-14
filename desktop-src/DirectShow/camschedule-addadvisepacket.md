---
description: El método AddAdvisePacket agrega una solicitud de aviso a la lista de solicitudes pendientes.
ms.assetid: 138d8404-7d28-47cc-91b4-4733a113ac7a
title: Método CAMSchedule.AddAdvisePacket (Dsschedule.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070171"
---
# <a name="camscheduleaddadvisepacket-method"></a>Método CAMSchedule.AddAdvisePacket

El `AddAdvisePacket` método agrega una solicitud de aviso a la lista de solicitudes pendientes.

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

*time1* \[ Ref\]
</dt> <dd>

Hora solicitada para el aviso.

</dd> <dt>

*time2* \[ Ref\]
</dt> <dd>

Para las solicitudes de asesoramiento periódicas, el tiempo entre notificaciones. Este parámetro se omite si *bPeriodic* es **FALSE.**

</dd> <dt>

*hNotify* 
</dt> <dd>

Controlar a un semáforo si *bPeriodic* es **TRUE** o controlar un evento si *bPeriodic* es **FALSE.**

</dd> <dt>

*bPeriódico* 
</dt> <dd>

Valor booleano que especifica si se va a agregar una notificación periódica o una notificación de una sola toma. Si **es TRUE,** la notificación es periódica; El *parámetro time2* especifica el tiempo entre notificaciones. Si **es FALSE,** la notificación se produce solo una vez.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un identificador para la solicitud de asesoramiento (la "cookie"). Si se produce un error en el método , el valor devuelto es cero.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Dsschedule.h (incluir Secuencias.h)</dt> </dl>                                                                                |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CLASE CAMSchedule**](camschedule.md)
</dt> </dl>

 

 




