---
description: Enviado por un origen de captura de audio cuando otro programa abre el dispositivo de audio en modo exclusivo.
ms.assetid: E9CC8507-38AB-4049-8DAC-767EC0ECE270
title: Evento MECaptureAudioSessionExclusiveModeOverride (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2051e6073b06f62823b95c80d7d4cfaf21de2f3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127579965"
---
# <a name="mecaptureaudiosessionexclusivemodeoverride-event"></a>Evento MECaptureAudioSessionExclusiveModeOverride

Enviado por un origen de captura de audio cuando otro programa abre el dispositivo de audio en modo exclusivo.

## <a name="event-values"></a>Valores de evento

Los valores posibles recuperados [**de IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluyen lo siguiente.



| VARTYPE               | Descripción                           |
|-----------------------|---------------------------------------|
| VT \_ EMPTY <br/> | Sin datos del evento.<br/> <br/> |



## <a name="remarks"></a>Observaciones

Este evento lo envía la secuencia multimedia del origen de captura de audio.

El origen de captura envía este evento cuando recibe un evento [**IAudioSessionEvents::OnSessionDisconnected**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) de la sesión de audio con el motivo de desconexión igual a **DisconnectReasonExclusiveModeOverride**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                                               |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Mfobjects.h (incluir Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Media Foundation eventos](media-foundation-events.md)
</dt> </dl>

 

 
