---
description: Se genera mediante los receptores de flujo del representador de vídeo mejorado (EVR) si cambia el dispositivo de vídeo.
ms.assetid: 5b663d6b-5df8-4321-a6a5-a21b9810065a
title: Evento MEStreamSinkDeviceChanged (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb760a45125ae7434ff2a58d43f087d2ec3c030cb29351ea4d2113ca8fe10c0a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120061015"
---
# <a name="mestreamsinkdevicechanged-event"></a>Evento MEStreamSinkDeviceChanged

Se genera mediante los receptores de flujo del representador de vídeo mejorado (EVR) si cambia el dispositivo de vídeo. Por ejemplo, la EVR genera este evento cuando recibe un evento [**\_ EC DISPLAY \_ CHANGED.**](../directshow/ec-display-changed.md)

La Media Foundation de datos responde a este evento al volver a enviar todas las solicitudes de ejemplo que no se pudieron hacer mientras el dispositivo cambiaba.

## <a name="event-values"></a>Valores de evento

Los valores posibles recuperados [**de IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluyen lo siguiente.



| VARTYPE              | Descripción                           |
|----------------------|---------------------------------------|
| VT \_ EMPTY<br/> | Sin datos del evento.<br/> <br/> |



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

[Receptores multimedia](media-sinks.md)
</dt> </dl>

 

 
