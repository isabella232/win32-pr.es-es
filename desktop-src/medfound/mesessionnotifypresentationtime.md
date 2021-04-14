---
description: La inicia la sesión multimedia cuando se inicia una nueva presentación. Este evento indica cuándo se iniciará la presentación y el desplazamiento entre el tiempo de presentación y la hora de origen.
ms.assetid: 67c7d5f3-ffaf-4359-a59c-bb26b992b6cd
title: Evento MESessionNotifyPresentationTime (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7b0cd8811d98094ab58ddcf844ec73e1470d120
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105648265"
---
# <a name="mesessionnotifypresentationtime-event"></a>Evento MESessionNotifyPresentationTime

La inicia la sesión multimedia cuando se inicia una nueva presentación. Este evento indica cuándo se iniciará la presentación y el desplazamiento entre el tiempo de presentación y la hora de origen.

## <a name="event-values"></a>Valores de evento

Los valores posibles recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) son los siguientes.



| VARTYPE              | Descripción                           |
|----------------------|---------------------------------------|
| VT \_ vacío<br/> | Sin datos del evento.<br/> <br/> |



## <a name="attributes"></a>Atributos

Para este evento, se definen los atributos siguientes.



| Atributo                                                                                                                   | Descripción                                                                                                     |
|-----------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [**\_tiempo de \_ presentación de inicio de evento de MF \_ \_**](mf-event-start-presentation-time-attribute.md)<br/>                       | Hora de inicio de la presentación.<br/> <br/>                                                      |
| [**\_desplazamiento de \_ tiempo de presentación de evento MF \_ \_**](mf-event-presentation-time-offset-attribute.md)<br/>                     | Desplazamiento entre el tiempo de presentación y las marcas de tiempo del origen del medio.<br/> <br/>                 |
| [**\_ \_ \_ \_ tiempo de presentación de inicio \_ de evento MF en la \_ salida**](mf-event-start-presentation-time-at-output-attribute.md)<br/> | Tiempo de presentación cuando los receptores de medios van a representar el primer ejemplo de la nueva topología.<br/> <br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Mfobjects. h (incluye Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession)
</dt> <dt>

[Eventos de Media Foundation](media-foundation-events.md)
</dt> </dl>

 

 




