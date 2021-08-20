---
description: Se genera cuando un origen multimedia se inicia sin buscar.
ms.assetid: a52d8ee1-cb46-487d-a744-fca6db7c2353
title: Evento MESourceStarted (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc4514e3d56b9a03cc66f635abf23cbeb36a992d7ed719499968c02c54f4f97d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117877364"
---
# <a name="mesourcestarted-event"></a>Evento MESourceStarted

Se genera cuando un origen multimedia se inicia sin buscar.

## <a name="event-values"></a>Valores de evento

Los valores posibles recuperados [**de IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluyen lo siguiente.



| VARTYPE              | Descripción                                                                                                    |
|----------------------|----------------------------------------------------------------------------------------------------------------|
| VT \_ EMPTY<br/> | Sin datos del evento. La hora de inicio era desde la posición actual.<br/> <br/>                            |
| VT \_ I8<br/>    | Hora de inicio, en unidades de 100 nanosegundos, con respecto a las marcas de tiempo de los ejemplos.<br/> <br/> |



## <a name="attributes"></a>Atributos

Para este evento, se definen los atributos siguientes.



| Atributo                                                                                     | Descripción                                                                                                                           |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [**INICIO \_ REAL DEL ORIGEN DEL EVENTO \_ \_ \_ MF**](mf-event-source-actual-start-attribute.md)<br/> | Hora de inicio. El origen de medios establece este atributo si se reinicia desde su posición actual.<br/> <br/>                     |
| [**MF \_ EVENT \_ SOURCE \_ FAKE \_ START**](mf-event-source-fake-start-attribute.md)<br/>     | Especifica si la topología de segmento actual está vacía. El origen del secuenciador establece este atributo.<br/> <br/>             |
| [**MF \_ EVENT \_ SOURCE \_ PROJECTSTART**](mf-event-source-projectstart-attribute.md)<br/>  | Hora de inicio de un segmento, con respecto al inicio de la presentación. El origen del secuenciador establece este atributo.<br/> <br/> |



## <a name="remarks"></a>Comentarios

Un origen multimedia genera este evento cuando se inicia desde un estado detenido o se inicia desde un estado en pausa en la misma posición del origen. El evento se genera si el [**método IMFMediaSource::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) devuelve S \_ OK.

Si el origen del medio comienza desde la posición actual y el estado anterior del origen se estaba ejecutando o en pausa, los datos del evento pueden estar vacíos (VT \_ EMPTY). Si los datos del evento son VT EMPTY, el origen de medios podría establecer el atributo \_ MF EVENT SOURCE ACTUAL [**\_ \_ \_ \_ START**](mf-event-source-actual-start-attribute.md) con la hora de inicio real.

Si el origen multimedia comienza desde una nueva posición o se ha detenido el estado anterior del origen, los datos del evento deben ser la hora de inicio (VT \_ I8).

Si el [**método Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) produce una búsqueda, el origen multimedia envía el [evento MESourceSeeked](mesourceseeked.md) en lugar de MESourceStarted.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Mfobjects.h (incluir Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Media Foundation eventos](media-foundation-events.md)
</dt> </dl>

 

 




