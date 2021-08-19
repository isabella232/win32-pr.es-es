---
description: Lo genera el representador de audio cuando una conexión en modo exclusivo adelanta la sesión de audio. El representador de audio ahora no es válido.
ms.assetid: f89acfe4-14a7-4051-a816-e5e0ba8db80a
title: Evento MEAudioSessionExclusiveModeOverride (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6344a5d073e9dc29777e6cb181c77bcae79da8602b830ade86646459e4d0bea
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120114225"
---
# <a name="meaudiosessionexclusivemodeoverride-event"></a>Evento MEAudioSessionExclusiveModeOverride

Lo genera el representador de audio cuando una conexión en modo exclusivo adelanta la sesión de audio. El representador de audio ahora no es válido.

La sesión multimedia reenvía este evento a la aplicación.

## <a name="event-values"></a>Valores de evento

Los valores posibles recuperados [**de IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluyen lo siguiente.



| VARTYPE                | Descripción                                                                               |
|------------------------|-------------------------------------------------------------------------------------------|
| VT \_ EMPTY<br/>   | Sin datos del evento.<br/> <br/>                                                     |
| VT \_ UNKNOWN<br/> | Puntero a la [**interfaz IMFAudioPolicy.**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy)<br/> <br/> |



## <a name="remarks"></a>Comentarios

El receptor de secuencias del representador de audio envía este evento. El evento se desencadena cuando el representador de audio recibe un evento [**IAudioSessionEvents::OnSessionDisconnected**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) de la sesión de audio con el motivo de desconexión igual a DisconnectReasonExclusiveModeOverride.

El [**puntero IMFAudioPolicy,**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) si se establece, no es útil, porque la secuencia de audio ya no es válida.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Mfobjects.h (incluir Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Media Foundation eventos](media-foundation-events.md)
</dt> <dt>

[Representador de audio de streaming](streaming-audio-renderer.md)
</dt> </dl>

 

 
