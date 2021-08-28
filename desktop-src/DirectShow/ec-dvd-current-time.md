---
description: Señala el principio de cada unidad de objeto de vídeo (VOBU), un segmento de vídeo de entre 0,4 y 1,0 segundos de longitud.
ms.assetid: 1f2def2f-3a6b-458b-b564-09b6cf74543c
title: EC_DVD_CURRENT_TIME (Dvdevcode.h)
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
ms.openlocfilehash: f72f49fde761418417b198787ef1b67d654f114f57fcd29bd7aa7edfae4b1e00
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119998005"
---
# <a name="ec_dvd_current_time"></a>HORA \_ ACTUAL DEL DVD DE \_ \_ EC

Señala el principio de cada unidad de objeto de vídeo (VOBU), un segmento de vídeo de entre 0,4 y 1,0 segundos de longitud.

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

**Valor DWORD** que indica el código de tiempo de reproducción actual en un formato binario codificado decimal (BCD) horas, minutos, segundos, fotogramas (HH:MM:SS:FF). Miembro de la [**estructura \_ TIMECODE de DVD.**](/windows/win32/api/strmif/ns-strmif-dvd_timecode)

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Valor **booleano (BOOL)** que indica el código de tiempo. Cero (0) indica 25 fotogramas por segundo, mientras que 1 indica 30 fotogramas por segundo (sin límite). Un valor de 2 indica que no se puede determinar el tiempo de reproducción.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Solo las películas lineales simples señalan este evento.

Este evento se genera en el dominio de título.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Dvdevcode.h (incluir Dshow.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Aplicaciones de DVD](dvd-applications.md)
</dt> <dt>

[Códigos de notificación de eventos de DVD](dvd-notification-codes.md)
</dt> <dt>

[Notificación de eventos en DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 




