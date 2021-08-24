---
description: Lo genera un receptor de flujo cuando completa una solicitud de limpieza.
ms.assetid: 451c7e09-868e-4c05-b970-d222b97223f2
title: Evento MEStreamSinkScrubSampleComplete (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2ae6e0ea7a90db33fe21d39017ac99908ace86bb263e0ad6e2047f70e70f5de
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119715175"
---
# <a name="mestreamsinkscrubsamplecomplete-event"></a>Evento MEStreamSinkScrubSampleComplete

Lo genera un receptor de flujo cuando completa una solicitud de limpieza.

La limpieza se produce cuando la velocidad de reproducción es cero y el reloj de presentación se inicia con un tiempo de desplazamiento especificado. Si un receptor multimedia admite la limpieza, cada secuencia del receptor genera este evento cada vez que se llama al método [**IMFClockStateSink::OnClockStart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart) mientras la velocidad de reproducción es cero.

Si la secuencia representa los datos durante la limpieza, envía el evento en cuanto se representan los datos. Si la secuencia no representa datos, envía el evento inmediatamente después de llamar a [**OnClockStart.**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart)

## <a name="event-values"></a>Valores de evento

Los valores posibles recuperados [**de IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluyen lo siguiente.



| VARTYPE              | Descripción                           |
|----------------------|---------------------------------------|
| VT \_ EMPTY<br/> | Sin datos del evento.<br/> <br/> |



## <a name="attributes"></a>Atributos

Para este evento, se definen los atributos siguientes.



| Atributo                                                                              | Descripción                                                                                                                                                   |
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MF \_ EVENT \_ SCRUBSAMPLE \_ TIME**](mf-event-scrubsample-time-attribute.md)<br/> | Tiempo de presentación para el que se representaron los datos. Si el receptor de medios no representa los datos durante la limpieza, no establece este atributo.<br/> <br/> |



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
</dt> <dt>

[MESessionScrubSampleComplete](mesessionscrubsamplecomplete.md)
</dt> </dl>

 

 




