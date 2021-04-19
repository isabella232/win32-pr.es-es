---
description: Enviado por un origen de captura de audio cuando cambia el volumen.
ms.assetid: 4A525D5F-9226-4277-BDB7-174BF65FE320
title: Evento MECaptureAudioSessionVolumeChanged (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5a391c55e8fcebaef0f620430b12f7cdcc67364
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105720417"
---
# <a name="mecaptureaudiosessionvolumechanged-event"></a>Evento MECaptureAudioSessionVolumeChanged

Enviado por un origen de captura de audio cuando cambia el volumen.

## <a name="event-values"></a>Valores de evento

Los valores posibles recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) son los siguientes.



| VARTYPE               | Descripción                           |
|-----------------------|---------------------------------------|
| VT \_ vacío <br/> | Sin datos del evento.<br/> <br/> |



## <a name="remarks"></a>Observaciones

Este evento lo envía el flujo multimedia del origen de captura de audio.

El origen de captura de audio envía este evento si una acción externa cambia el volumen; por ejemplo, si el usuario cambia el volumen a través del panel de control. El origen de captura no envía el evento si la aplicación cambia el volumen directamente en el origen.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                                               |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Mfobjects. h (incluye Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Eventos de Media Foundation](media-foundation-events.md)
</dt> </dl>

 

 




