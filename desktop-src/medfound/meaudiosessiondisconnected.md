---
description: Lo genera el representador de audio cuando la sesión de audio se desconecta de una sesión Terminal Windows Services (WTS). El representador de audio ahora no es válido.
ms.assetid: 08f9844c-f3b1-4d60-990e-9131f3312f6b
title: Evento MEAudioSessionDisconnected (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b345d755c07bf823f6d1ca60c80e3620cb0242b8451a0b7227d5dab38902f8f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118062707"
---
# <a name="meaudiosessiondisconnected-event"></a>Evento MEAudioSessionDisconnected

Lo genera el representador de audio cuando la sesión de audio se desconecta de una sesión Terminal Windows Services (WTS). El representador de audio ahora no es válido.

La sesión multimedia reenvía este evento a la aplicación.

## <a name="event-values"></a>Valores de evento

Los valores posibles recuperados [**de IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluyen lo siguiente.



| VARTYPE                | Descripción                                                                               |
|------------------------|-------------------------------------------------------------------------------------------|
| VT \_ EMPTY<br/>   | Sin datos del evento.<br/> <br/>                                                     |
| VT \_ UNKNOWN<br/> | Puntero a la [**interfaz DEAUDIOPolicy.**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy)<br/> <br/> |



## <a name="remarks"></a>Comentarios

El receptor de secuencias del representador de audio envía este evento. El evento se desencadena cuando el representador de audio recibe un evento [**IAudioSessionEvents::OnSessionDisconnected**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) de la sesión de audio con el motivo de desconexión igual a DisconnectReasonSessionDisconnected.

Si se establece, no resulta útil el puntero [**DEAUDIOPolicy,**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) ya que la secuencia de audio ya no es válida.

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

 

 
