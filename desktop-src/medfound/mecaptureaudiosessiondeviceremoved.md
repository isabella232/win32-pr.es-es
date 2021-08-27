---
description: Enviado por un origen de captura de audio cuando se quita el dispositivo.
ms.assetid: A249D8B4-15A8-4AD3-8316-2886E5C37825
title: Evento MECaptureAudioSessionDeviceRemoved (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c1c3b0e9acbf627800f69ad8ba374edc4b6f075268e61d2c71618c07e8c95645
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120114205"
---
# <a name="mecaptureaudiosessiondeviceremoved-event"></a>Evento MECaptureAudioSessionDeviceRemoved

Enviado por un origen de captura de audio cuando se quita el dispositivo.

## <a name="event-values"></a>Valores de evento

Los valores posibles recuperados [**de IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluyen lo siguiente.



| VARTYPE               | Descripción                           |
|-----------------------|---------------------------------------|
| VT \_ EMPTY <br/> | Sin datos del evento.<br/> <br/> |



## <a name="remarks"></a>Comentarios

Este evento lo envía la secuencia multimedia del origen de captura de audio.

El origen de captura envía este evento cuando recibe un evento [**IAudioSessionEvents::OnSessionDisconnected**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) de la sesión de audio con el motivo de desconexión igual a **DisconnectReasonDeviceRemoval.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                                               |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Mfobjects.h (incluir Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Media Foundation eventos](media-foundation-events.md)
</dt> </dl>

 

 
