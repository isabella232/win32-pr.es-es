---
description: Generado por el origen del secuenciador cuando se completa un segmento y va seguido de otro segmento. Cuando se completa el segmento final, el origen del secuenciador genera un evento MEEndOfPresentation.
ms.assetid: 1be13c9a-d454-4642-b26b-556f2461b705
title: Evento MEEndOfPresentationSegment (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d3608f51f3ff66e21261cc40d1f8cf690c92c4e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908476"
---
# <a name="meendofpresentationsegment-event"></a>Evento MEEndOfPresentationSegment

Generado por el origen del secuenciador cuando se completa un segmento y va seguido de otro segmento. Cuando se completa el segmento final, el origen del secuenciador genera un evento [MEEndOfPresentation](meendofpresentation.md) .

La sesión multimedia reenvía este evento a la aplicación.

## <a name="event-values"></a>Valores de evento

Los valores posibles recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) son los siguientes.



| VARTYPE              | Descripción                           |
|----------------------|---------------------------------------|
| VT \_ vacío<br/> | Sin datos del evento.<br/> <br/> |



## <a name="attributes"></a>Atributos

Para este evento, se definen los atributos siguientes.



| Atributo                                                                                               | Descripción                                                                          |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [**\_topología de origen de eventos MF \_ \_ \_ cancelada**](mf-event-source-topology-canceled-attribute.md)<br/> | Especifica si el origen del secuenciador canceló este segmento.<br/> <br/> |



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

[Acerca del origen del secuenciador](about-the-sequencer-source.md)
</dt> <dt>

[Eventos de origen de Sequencer](sequencer-source-events.md)
</dt> </dl>

 

 




