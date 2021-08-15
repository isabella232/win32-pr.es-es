---
description: Enviado por el representador de audio de streaming (SAR) cuando cambia el volumen o el estado de exclusión de la sesión de audio.
ms.assetid: 63c37bd2-0289-407a-92f1-169eb5d2e02e
title: Evento MEAudioSessionVolumeChanged (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 721de9751cac284cb25d390d948f0f686447c04eaa613c1fecd4bf3503bce76d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119465405"
---
# <a name="meaudiosessionvolumechanged-event"></a>Evento MEAudioSessionVolumeChanged

Enviado por el representador de audio de streaming (SAR) cuando cambia el volumen o el estado de exclusión de la sesión de audio.

La sesión multimedia reenvía este evento a la aplicación.

## <a name="event-values"></a>Valores de evento

Los valores posibles recuperados [**de IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluyen lo siguiente.



| VARTYPE                | Descripción                                                                               |
|------------------------|-------------------------------------------------------------------------------------------|
| VT \_ EMPTY<br/>   | Sin datos del evento.<br/> <br/>                                                     |
| VT \_ UNKNOWN<br/> | Puntero a la [**interfaz DEAUDIOPolicy.**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy)<br/> <br/> |



## <a name="remarks"></a>Observaciones

El receptor de flujo de la SAR genera este evento. El evento se desencadena cuando el SAR recibe un evento [**IAudioSessionEvents::OnSimpleVolumeChanged**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onsimplevolumechanged) de la sesión de audio. Para obtener el nuevo nivel de volumen y el estado de exclusión mutua, llame a [**IMFSimpleAudioVolume::GetMasterVolume**](/windows/desktop/api/mfidl/nf-mfidl-imfsimpleaudiovolume-getmastervolume) y [**ASESIMPLEAudioVolume::GetMute**](/windows/desktop/api/mfidl/nf-mfidl-imfsimpleaudiovolume-getmute).

La RAE envía este evento si una acción externa cambia el volumen, por ejemplo, si el usuario cambia el volumen a través del programa de control de volúmenes del sistema (SndVol). La RAE no envía el evento si la aplicación cambia el volumen directamente en la SAR.

Además, la SAR no envía este evento cuando cambia el volumen del canal ([**IAudioSessionEvents::OnChannelVolumeChanged**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onchannelvolumechanged)).

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

 

 
