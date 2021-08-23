---
description: Lo genera un receptor de flujo cuando completa la transición al estado detenido. La transición a detenido se produce cuando se llama al método IMFPresentationClock Stop en el reloj de presentación de receptores.
ms.assetid: 1a8c7faa-4d4a-4458-ad08-a760a15dc347
title: Evento MEStreamSinkStopped (Mfobjects.h)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d7bf6a39dca8f50fed8fdd1d0137405225624999fab42771e485174ba4f0afa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119715105"
---
# <a name="mestreamsinkstopped-event"></a>Evento MEStreamSinkStopped

Lo genera un receptor de flujo cuando completa la transición al estado detenido. La transición a detenido se produce cuando se llama al método [**IMFPresentationClock::Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-stop) en el reloj de presentación del receptor.

## <a name="event-values"></a>Valores de evento

Entre los valores posibles recuperados [**de IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) se incluyen los siguientes.



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

[Receptores de medios](media-sinks.md)
</dt> </dl>

 

 




