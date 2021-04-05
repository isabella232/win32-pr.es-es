---
description: 'Se genera cuando el método IMFMediaSession:: Start se completa de forma asincrónica.'
ms.assetid: 28ed32f0-9b23-4da1-9587-15f490da7bf9
title: Evento MESessionStarted (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9510fb5f5dda3d14b916ed40dcba4ca05800b52b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082354"
---
# <a name="mesessionstarted-event"></a>Evento MESessionStarted

Se genera cuando el método [**IMFMediaSession:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) se completa de forma asincrónica.

## <a name="event-values"></a>Valores de evento

Los valores posibles recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) son los siguientes.



| VARTYPE              | Descripción                           |
|----------------------|---------------------------------------|
| VT \_ vacío<br/> | Sin datos del evento.<br/> <br/> |



## <a name="attributes"></a>Atributos

Para este evento, se definen los atributos siguientes.



| Atributo                                                                                               | Descripción                                                                                     |
|---------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [**\_desplazamiento de \_ tiempo de presentación de evento MF \_ \_**](mf-event-presentation-time-offset-attribute.md)<br/> | Desplazamiento entre el tiempo de presentación y las marcas de tiempo del origen del medio.<br/> <br/> |



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

 

 




