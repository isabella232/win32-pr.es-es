---
description: Se genera cuando un origen multimedia comienza sin búsquedas.
ms.assetid: a52d8ee1-cb46-487d-a744-fca6db7c2353
title: Evento MESourceStarted (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c17ba7898a8bf33df4a3508afee9b7c0c9bc81c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544374"
---
# <a name="mesourcestarted-event"></a>Evento MESourceStarted

Se genera cuando un origen multimedia comienza sin búsquedas.

## <a name="event-values"></a>Valores de evento

Los valores posibles recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) son los siguientes.



| VARTYPE              | Descripción                                                                                                    |
|----------------------|----------------------------------------------------------------------------------------------------------------|
| VT \_ vacío<br/> | Sin datos del evento. La hora de inicio era desde la posición actual.<br/> <br/>                            |
| VT \_ i8<br/>    | La hora de inicio, en unidades de 100-nanosegundos, con respecto a las marcas de tiempo de los ejemplos.<br/> <br/> |



## <a name="attributes"></a>Atributos

Para este evento, se definen los atributos siguientes.



| Atributo                                                                                     | Descripción                                                                                                                           |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [**\_ \_ Inicio real del origen de eventos MF \_ \_**](mf-event-source-actual-start-attribute.md)<br/> | Hora de inicio. El origen de medios establece este atributo si se reinicia desde su posición actual.<br/> <br/>                     |
| [**\_ \_ Inicio falso de origen de evento MF \_ \_**](mf-event-source-fake-start-attribute.md)<br/>     | Especifica si la topología de segmento actual está vacía. El origen del secuenciador establece este atributo.<br/> <br/>             |
| [**\_origen de evento MF \_ \_ PROJECTSTART**](mf-event-source-projectstart-attribute.md)<br/>  | Hora de inicio de un segmento, con respecto al inicio de la presentación. El origen del secuenciador establece este atributo.<br/> <br/> |



## <a name="remarks"></a>Observaciones

Un origen multimedia genera este evento cuando se inicia desde un estado detenido o se inicia a partir de un estado de pausa en la misma posición del origen. El evento se desencadena si el método [**IMFMediaSource:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) devuelve S \_ correcto.

Si el origen multimedia se inicia desde la posición actual y el estado anterior del origen se estaba ejecutando o en pausa, los datos del evento pueden estar vacíos (VT \_ vacío). Si los datos de evento están \_ vacíos en VT, el origen de medios podría establecer el atributo de [**\_ \_ \_ \_ Inicio real del origen de eventos MF**](mf-event-source-actual-start-attribute.md) con la hora de inicio real.

Si el origen multimedia se inicia desde una nueva posición o se detuvo el estado anterior del origen, los datos del evento deben ser la hora de inicio (VT \_ i8).

Si el método [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) produce una búsqueda, el origen multimedia envía el evento [MESourceSeeked](mesourceseeked.md) en lugar de MESourceStarted.

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

 

 




