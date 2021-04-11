---
description: Señala un evento de un receptor de medios que representa los datos multimedia.
ms.assetid: bb7db7c9-c39f-4bf4-9412-42525c4f2ea3
title: Evento MERendererEvent (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c52e15bfbe97743e8af10a79cf3ef1d94626a877
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275972"
---
# <a name="merendererevent-event"></a>Evento MERendererEvent

Señala un evento de un receptor de medios que representa los datos multimedia.

El [representador de vídeo mejorado](enhanced-video-renderer.md) (EVR) envía este evento cuando recibe un evento de usuario del presentador de EVR.

## <a name="event-values"></a>Valores de evento

Los valores posibles recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) son los siguientes.



| VARTYPE           | Descripción                        |
|-------------------|------------------------------------|
| VT \_ I4<br/> | Código de evento.<br/> <br/> |



## <a name="remarks"></a>Observaciones

Si el presentador llama al método **IMediaEventSink:: Notify** de EVR con un código de evento en el usuario del intervalo de EC \_ o superior, el EVR envía este evento. Los datos del evento son el código de evento que se pasó al método **Notify** .

Los parámetros de evento originales (*EventParam1* y *EventParam2* en el método **IMediaEventSink:: Notify** ) se omiten, por lo que el presentador debe establecer estos valores en **null**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Mfobjects. h (incluye Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Eventos de Media Foundation](media-foundation-events.md)
</dt> </dl>

 

 




