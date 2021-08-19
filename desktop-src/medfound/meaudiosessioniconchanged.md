---
description: Lo genera el representador de audio cuando cambia el icono de la sesión de audio.
ms.assetid: 72aae901-e5fe-481d-babb-459038abd629
title: Evento MEAudioSessionIconChanged (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ce466cf88b93c9cf806a2a6b70f76b084e8aa0b2c8fb2910a7391337a13b2f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118062464"
---
# <a name="meaudiosessioniconchanged-event"></a>Evento MEAudioSessionIconChanged

Lo genera el representador de audio cuando cambia el icono de la sesión de audio.

La sesión multimedia reenvía este evento a la aplicación.

## <a name="event-values"></a>Valores de evento

Los valores posibles recuperados [**de IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluyen lo siguiente.



| VARTYPE                | Descripción                                                                               |
|------------------------|-------------------------------------------------------------------------------------------|
| VT \_ EMPTY<br/>   | Sin datos del evento.<br/> <br/>                                                     |
| VT \_ UNKNOWN<br/> | Puntero a la [**interfaz DEAUDIOPolicy.**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy)<br/> <br/> |



## <a name="remarks"></a>Comentarios

El receptor de secuencias del representador de audio envía este evento. El evento se desencadena cuando el representador de audio recibe un evento [**IAudioSessionEvents::OnIconPathChanged**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-oniconpathchanged) de la sesión de audio.

Para obtener el nuevo icono, llame [**a ICONAudioPolicy::GetIconPath**](/windows/desktop/api/mfidl/nf-mfidl-imfaudiopolicy-geticonpath).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Mfobjects.h (incluir Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMFAudioPolicy::GetIconPath**](/windows/desktop/api/mfidl/nf-mfidl-imfaudiopolicy-geticonpath)
</dt> <dt>

[Media Foundation eventos](media-foundation-events.md)
</dt> <dt>

[Representador de audio de streaming](streaming-audio-renderer.md)
</dt> </dl>

 

 
