---
description: El método Advise envía todas las solicitudes programadas para una hora especificada o anterior.
ms.assetid: 09ea84b7-517a-4ea6-9e03-0d9cd8f72e1f
title: Método CAMSchedule.Advise (Dsschedule.h)
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
ms.openlocfilehash: a0943479aaa7fe2e6d699bba147977a73f48fc31186fb64ea26a211e2ea31d8d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119757795"
---
# <a name="camscheduleadvise-method"></a>Método CAMSchedule.Advise

El `Advise` método envía todas las solicitudes programadas para una hora especificada o anterior.

## <a name="syntax"></a>Sintaxis


```C++
REFERENCE_TIME Advise(
  [ref] const REFERENCE_TIME &rtTime
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*rtTime* \[ Ref\]
</dt> <dd>

Valor que especifica la hora de referencia actual.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve la hora de referencia de la siguiente solicitud de aviso programada o MAX \_ TIME si no queda ninguna.

## <a name="remarks"></a>Comentarios

Cuando el reloj llama a este método, especifica la hora de referencia actual. El programador determina qué solicitudes de asesoramiento han expirado, si las hay, y las envía. Si expira una solicitud de una sola toma, el programador la elimina. Si expira una solicitud periódica, el programador la vuelve a programar para la próxima hora de aviso. El método devuelve la hora de la siguiente solicitud pendiente.

Para enviar una solicitud de aviso, el programador señala el evento o semáforo especificado en el *parámetro hNotify* del [**método CAMSchedule::AddAdvisePacket.**](camschedule-addadvisepacket.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Dsschedule.h (incluir Secuencias.h)</dt> </dl>                                                                                |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CLASE CAMSchedule**](camschedule.md)
</dt> </dl>

 

 




