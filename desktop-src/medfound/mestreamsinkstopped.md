---
description: Generado por un receptor de flujo cuando completa la transición al estado detenido. La transición a Stopped se produce cuando se llama al método STOP IMFPresentationClock en el reloj de la presentación de receptores.
ms.assetid: 1a8c7faa-4d4a-4458-ad08-a760a15dc347
title: Evento MEStreamSinkStopped (Mfobjects. h)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e35313ab3d43c950184a82e403fa6ad0eb5b4ab4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104082970"
---
# <a name="mestreamsinkstopped-event"></a>Evento MEStreamSinkStopped

Generado por un receptor de flujo cuando completa la transición al estado detenido. La transición a Stopped se produce cuando se llama al método [**IMFPresentationClock:: Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-stop) en el reloj de presentación del receptor.

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

 

 




