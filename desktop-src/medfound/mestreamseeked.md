---
description: 'Generado por un flujo multimedia después de una llamada a IMFMediaSource:: Start produce una búsqueda en la secuencia. Un flujo multimedia genera este evento cuando el origen del medio genera el evento MESourceSeeked.'
ms.assetid: df06df16-711d-4262-b049-fb29f25934de
title: Evento MEStreamSeeked (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7b66e2176b08c04b01fc487aac4b8218536b615
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275965"
---
# <a name="mestreamseeked-event"></a>Evento MEStreamSeeked

Generado por un flujo multimedia después de una llamada a [**IMFMediaSource:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) produce una búsqueda en la secuencia. Un flujo multimedia genera este evento cuando el origen del medio genera el evento [MESourceSeeked](mesourceseeked.md) .

## <a name="event-values"></a>Valores de evento

Los valores posibles recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) son los siguientes.



| VARTYPE           | Descripción                                                        |
|-------------------|--------------------------------------------------------------------|
| VT \_ i8<br/> | Nueva hora de inicio, en unidades de 100-nanosegundos.<br/> <br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Mfobjects. h (incluye Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Eventos de Media Foundation](media-foundation-events.md)
</dt> </dl>

 

 




