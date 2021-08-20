---
description: Lo genera un receptor de flujo para solicitar un nuevo ejemplo multimedia de la canalización.
ms.assetid: 35020a15-942f-4dd0-9ca4-815affdacecf
title: Evento MEStreamSinkRequestSample (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de147486f54485ecb9f80b15394b1a2d48021c1f602ccd138cf6718ef7ec2c0b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118061330"
---
# <a name="mestreamsinkrequestsample-event"></a>Evento MEStreamSinkRequestSample

Lo genera un receptor de flujo para solicitar un nuevo ejemplo multimedia de la canalización. Para cada evento MEStreamSinkRequestSample, la canalización solicita datos del siguiente componente ascendente.

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

 

 




