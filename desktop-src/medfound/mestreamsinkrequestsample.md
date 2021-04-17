---
description: Generado por un receptor de flujo para solicitar un nuevo ejemplo multimedia de la canalización.
ms.assetid: 35020a15-942f-4dd0-9ca4-815affdacecf
title: Evento MEStreamSinkRequestSample (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1c5afbfa9f0cfe4b320b451e699612a4729c23a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677594"
---
# <a name="mestreamsinkrequestsample-event"></a>Evento MEStreamSinkRequestSample

Generado por un receptor de flujo para solicitar un nuevo ejemplo multimedia de la canalización. Para cada evento MEStreamSinkRequestSample, la canalización solicita datos del siguiente componente de nivel superior.

## <a name="event-values"></a>Valores de evento

Los valores posibles recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) son los siguientes.



| VARTYPE              | Descripción                           |
|----------------------|---------------------------------------|
| VT \_ vacío<br/> | Sin datos del evento.<br/> <br/> |



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
</dt> </dl>

 

 




