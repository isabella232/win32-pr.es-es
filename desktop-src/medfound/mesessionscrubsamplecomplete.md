---
description: Lo genera la sesión multimedia cuando completa una solicitud de limpieza.
ms.assetid: 1ae97022-3fb2-4c5e-9262-d5bdc2a62bee
title: Evento MESessionScrubSampleComplete (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b076c2f2978831cc30521fcf49d71c04620c4dee
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127257887"
---
# <a name="mesessionscrubsamplecomplete-event"></a>Evento MESessionScrubSampleComplete

Lo genera la sesión multimedia cuando completa una solicitud de limpieza.

La limpieza se produce cuando la velocidad de reproducción es cero y la aplicación llama [**a IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start). Este evento se genera después de que cada receptor de flujo haya completado la solicitud de limpieza.

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
| Encabezado<br/>                   | <dl> <dt>Mfobjects.h (incluir Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Media Foundation eventos](media-foundation-events.md)
</dt> <dt>

[MEStreamSinkScrubSampleComplete](mestreamsinkscrubsamplecomplete.md)
</dt> </dl>

 

 




