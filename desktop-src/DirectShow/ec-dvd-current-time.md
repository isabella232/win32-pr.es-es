---
description: Indica el principio de cada unidad de objeto de vídeo (VOBU), un segmento de vídeo de 0,4 a 1,0 segundos de longitud.
ms.assetid: 1f2def2f-3a6b-458b-b564-09b6cf74543c
title: EC_DVD_CURRENT_TIME (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_CURRENT_TIME
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 0f1bb2f5f31efa881917ac71ea381cc0a82e8744
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653584"
---
# <a name="ec_dvd_current_time"></a>\_ \_ hora actual del DVD de EC \_

Indica el principio de cada unidad de objeto de vídeo (VOBU), un segmento de vídeo de 0,4 a 1,0 segundos de longitud.

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Valor **DWORD** que indica el código de tiempo de reproducción actual en un formato de horas, minutos, segundos y fotogramas (HH: mm: SS: FF) con código binario. Miembro de la estructura de [**\_ código de tiempo de DVD**](/windows/win32/api/strmif/ns-strmif-dvd_timecode) .

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Valor booleano (**bool**) que indica el código de tiempo. Cero (0) indica 25 fotogramas por segundo, mientras que 1 indica 30 fotogramas por segundo (no quitado). Un valor de 2 indica que no se puede determinar la hora de reproducción.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Solo las películas lineales simples señalan este evento.

Este evento se desencadena en el dominio de título.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Dvdevcode. h (incluir DShow. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Aplicaciones de DVD](dvd-applications.md)
</dt> <dt>

[Códigos de notificación de eventos de DVD](dvd-notification-codes.md)
</dt> <dt>

[Notificación de eventos en DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 




