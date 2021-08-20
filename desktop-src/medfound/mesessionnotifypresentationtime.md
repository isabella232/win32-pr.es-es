---
description: Lo genera la sesión multimedia cuando se inicia una nueva presentación. Este evento indica cuándo se iniciará la presentación y el desplazamiento entre la hora de presentación y la hora de origen.
ms.assetid: 67c7d5f3-ffaf-4359-a59c-bb26b992b6cd
title: Evento MESessionNotifyPresentationTime (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d10c1b1e443bd2c6a56a926d5355de5606bf2f2e25618269f8d4ed735538d92f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118061769"
---
# <a name="mesessionnotifypresentationtime-event"></a>Evento MESessionNotifyPresentationTime

Lo genera la sesión multimedia cuando se inicia una nueva presentación. Este evento indica cuándo se iniciará la presentación y el desplazamiento entre la hora de presentación y la hora de origen.

## <a name="event-values"></a>Valores de evento

Los valores posibles recuperados [**de IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluyen lo siguiente.



| VARTYPE              | Descripción                           |
|----------------------|---------------------------------------|
| VT \_ EMPTY<br/> | Sin datos del evento.<br/> <br/> |



## <a name="attributes"></a>Atributos

Para este evento, se definen los atributos siguientes.



| Atributo                                                                                                                   | Descripción                                                                                                     |
|-----------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [**HORA DE \_ PRESENTACIÓN DEL \_ EVENTO \_ MF \_**](mf-event-start-presentation-time-attribute.md)<br/>                       | Hora de inicio de la presentación.<br/> <br/>                                                      |
| [**MF \_ EVENT \_ PRESENTATION \_ TIME \_ OFFSET**](mf-event-presentation-time-offset-attribute.md)<br/>                     | Desplazamiento entre el tiempo de presentación y las marcas de tiempo del origen del medio.<br/> <br/>                 |
| [**HORA DE PRESENTACIÓN DEL EVENTO MF \_ \_ EN LA \_ \_ \_ \_ SALIDA**](mf-event-start-presentation-time-at-output-attribute.md)<br/> | Hora de presentación en la que los receptores multimedia representarán el primer ejemplo de la nueva topología.<br/> <br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Mfobjects.h (incluir Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession)
</dt> <dt>

[Media Foundation eventos](media-foundation-events.md)
</dt> </dl>

 

 




