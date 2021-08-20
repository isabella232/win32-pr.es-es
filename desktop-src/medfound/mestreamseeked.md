---
description: La generación por una secuencia de medios después de una llamada a IMFMediaSource::Start provoca una búsqueda en la secuencia. Una secuencia multimedia genera este evento cuando el origen multimedia genera el evento MESourceSeeked.
ms.assetid: df06df16-711d-4262-b049-fb29f25934de
title: Evento MEStreamSeeked (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b03e58b11785a7b807f6793ff2ba6b2a4afa5f912d21e626938d7b3c725242f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118061341"
---
# <a name="mestreamseeked-event"></a>Evento MEStreamSeeked

La generación por una secuencia de medios después de una llamada a [**IMFMediaSource::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) provoca una búsqueda en la secuencia. Una secuencia multimedia genera este evento cuando el origen multimedia genera el [evento MESourceSeeked.](mesourceseeked.md)

## <a name="event-values"></a>Valores de evento

Los valores posibles recuperados [**de IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluyen lo siguiente.



| VARTYPE           | Descripción                                                        |
|-------------------|--------------------------------------------------------------------|
| VT \_ I8<br/> | Nueva hora de inicio, en unidades de 100 nanosegundos.<br/> <br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Mfobjects.h (incluir Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Media Foundation eventos](media-foundation-events.md)
</dt> </dl>

 

 




