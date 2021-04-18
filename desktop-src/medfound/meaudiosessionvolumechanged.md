---
description: Lo envía el representador de audio de transmisión por secuencias (SAR) cuando cambia el estado del volumen o el silenciador de la sesión de audio.
ms.assetid: 63c37bd2-0289-407a-92f1-169eb5d2e02e
title: Evento MEAudioSessionVolumeChanged (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 429edd8a26ed7f4ca1e764c7fbea1c6930c4871c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105720404"
---
# <a name="meaudiosessionvolumechanged-event"></a>Evento MEAudioSessionVolumeChanged

Lo envía el representador de audio de transmisión por secuencias (SAR) cuando cambia el estado del volumen o el silenciador de la sesión de audio.

La sesión multimedia reenvía este evento a la aplicación.

## <a name="event-values"></a>Valores de evento

Los valores posibles recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) son los siguientes.



| VARTYPE                | Descripción                                                                               |
|------------------------|-------------------------------------------------------------------------------------------|
| VT \_ vacío<br/>   | Sin datos del evento.<br/> <br/>                                                     |
| VT \_ desconocido<br/> | Puntero a la interfaz [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) .<br/> <br/> |



## <a name="remarks"></a>Observaciones

Este evento es desencadenado por el receptor de la secuencia de SAR. El evento se desencadena cuando el SAR recibe un evento [**IAudioSessionEvents:: OnSimpleVolumeChanged**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onsimplevolumechanged) de la sesión de audio. Para obtener el nuevo nivel de volumen y silenciar el estado, llame a [**IMFSimpleAudioVolume:: GetMasterVolume**](/windows/desktop/api/mfidl/nf-mfidl-imfsimpleaudiovolume-getmastervolume) y [**IMFSimpleAudioVolume:: GetMute**](/windows/desktop/api/mfidl/nf-mfidl-imfsimpleaudiovolume-getmute).

El SAR envía este evento si una acción externa cambia el volumen; por ejemplo, si el usuario cambia el volumen a través del programa de control de volumen del sistema (SndVol). El SAR no envía el evento si la aplicación cambia el volumen directamente en el SAR.

Además, el SAR no envía este evento cuando cambia el volumen del canal ([**IAudioSessionEvents:: OnChannelVolumeChanged**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onchannelvolumechanged)).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Mfobjects. h (incluye Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Eventos de Media Foundation](media-foundation-events.md)
</dt> <dt>

[Representador de audio de streaming](streaming-audio-renderer.md)
</dt> </dl>

 

 
