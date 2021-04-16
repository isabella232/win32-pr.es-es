---
description: Generado por un receptor de flujo cuando completa una solicitud de limpieza.
ms.assetid: 451c7e09-868e-4c05-b970-d222b97223f2
title: Evento MEStreamSinkScrubSampleComplete (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81f29d478635d5a9ba7e7c5356c49ebd8da216f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678377"
---
# <a name="mestreamsinkscrubsamplecomplete-event"></a>Evento MEStreamSinkScrubSampleComplete

Generado por un receptor de flujo cuando completa una solicitud de limpieza.

La limpieza se produce cuando la velocidad de reproducción es cero y el reloj de la presentación se inicia con una hora de srubbing especificada. Si un receptor de medios admite la limpieza, cada secuencia del receptor genera este evento cada vez que se llama al método [**IMFClockStateSink:: OnClockStart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart) mientras que la velocidad de reproducción es cero.

Si el flujo representa datos durante la limpieza, envía el evento en cuanto se representan los datos. Si la secuencia no representa datos, envía el evento inmediatamente después de que se llame a [**OnClockStart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart) .

## <a name="event-values"></a>Valores de evento

Los valores posibles recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) son los siguientes.



| VARTYPE              | Descripción                           |
|----------------------|---------------------------------------|
| VT \_ vacío<br/> | Sin datos del evento.<br/> <br/> |



## <a name="attributes"></a>Atributos

Para este evento, se definen los atributos siguientes.



| Atributo                                                                              | Descripción                                                                                                                                                   |
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_hora de \_ SCRUBSAMPLE de eventos de MF \_**](mf-event-scrubsample-time-attribute.md)<br/> | Tiempo de presentación para el que se representan los datos. Si el receptor de medios no representa los datos durante la limpieza, no establece este atributo.<br/> <br/> |



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

[Receptores de medios](media-sinks.md)
</dt> <dt>

[MESessionScrubSampleComplete](mesessionscrubsamplecomplete.md)
</dt> </dl>

 

 




