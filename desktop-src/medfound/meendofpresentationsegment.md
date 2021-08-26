---
description: Lo genera el origen del secuenciador cuando se completa un segmento y va seguido de otro segmento. Cuando se completa el segmento final, el origen del secuenciador genera un evento MEEndOfPresentation.
ms.assetid: 1be13c9a-d454-4642-b26b-556f2461b705
title: Evento MEEndOfPresentationSegment (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b82f646ca76dbb6cc3cd8dc9e95dbaca2c55c504af261924918dbf790411e7d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013705"
---
# <a name="meendofpresentationsegment-event"></a>Evento MEEndOfPresentationSegment

Lo genera el origen del secuenciador cuando se completa un segmento y va seguido de otro segmento. Cuando se completa el segmento final, el origen del secuenciador genera un [evento MEEndOfPresentation.](meendofpresentation.md)

La sesión multimedia reenvía este evento a la aplicación.

## <a name="event-values"></a>Valores de evento

Los valores posibles recuperados [**de IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluyen lo siguiente.



| VARTYPE              | Descripción                           |
|----------------------|---------------------------------------|
| VT \_ EMPTY<br/> | Sin datos del evento.<br/> <br/> |



## <a name="attributes"></a>Atributos

Para este evento, se definen los atributos siguientes.



| Atributo                                                                                               | Descripción                                                                          |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [**TOPOLOGÍA \_ DE ORIGEN DE EVENTOS MF \_ \_ \_ CANCELADA**](mf-event-source-topology-canceled-attribute.md)<br/> | Especifica si el origen del secuenciador canceló este segmento.<br/> <br/> |



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

[Acerca del origen del secuenciador](about-the-sequencer-source.md)
</dt> <dt>

[Eventos de origen del secuenciador](sequencer-source-events.md)
</dt> </dl>

 

 




