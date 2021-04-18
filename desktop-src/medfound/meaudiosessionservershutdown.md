---
description: Generado por el procesador de audio cuando se apaga el sistema del servidor de audio de Windows. El representador de audio ahora no es válido.
ms.assetid: 8e80903c-d6ce-4fa2-87db-552c7fba3c6a
title: Evento MEAudioSessionServerShutdown (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d819d850df481477b2ea1a5052c18d140a41cdb0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105720405"
---
# <a name="meaudiosessionservershutdown-event"></a>Evento MEAudioSessionServerShutdown

Generado por el procesador de audio cuando se apaga el sistema del servidor de audio de Windows. El representador de audio ahora no es válido.

La sesión multimedia reenvía este evento a la aplicación.

## <a name="event-values"></a>Valores de evento

Los valores posibles recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) son los siguientes.



| VARTYPE                | Descripción                                                                               |
|------------------------|-------------------------------------------------------------------------------------------|
| VT \_ vacío<br/>   | Sin datos del evento.<br/> <br/>                                                     |
| VT \_ desconocido<br/> | Puntero a la interfaz [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) .<br/> <br/> |



## <a name="remarks"></a>Observaciones

El receptor de flujo del representador de audio envía este evento. El evento se desencadena cuando el representador de audio recibe un evento [**IAudioSessionEvents:: OnSessionDisconnected**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) de la sesión de audio con el motivo de la desconexión igual a **DisconnectReasonServerShutdown**.

El puntero [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) , si está establecido, no es útil porque la secuencia de audio ya no es válida.

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

 

 
