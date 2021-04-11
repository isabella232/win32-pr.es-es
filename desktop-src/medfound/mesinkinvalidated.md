---
description: Se genera cuando un receptor de medios deja de ser válido.
ms.assetid: fa75926e-7cef-44da-9efe-f2f86fd4fd45
title: Evento MESinkInvalidated (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46807a45e907999b34190f9678bd3dc0051680ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275584"
---
# <a name="mesinkinvalidated-event"></a>Evento MESinkInvalidated

Se genera cuando un receptor de medios deja de ser válido.

## <a name="event-values"></a>Valores de evento

Los valores posibles recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) son los siguientes.



| VARTYPE              | Descripción                           |
|----------------------|---------------------------------------|
| VT \_ vacío<br/> | Sin datos del evento.<br/> <br/> |



## <a name="attributes"></a>Atributos

Para este evento, se definen los atributos siguientes.



| Atributo                                                                    | Descripción                                                              |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [**\_nodo de \_ salida de evento MF \_**](mf-event-output-node-attribute.md)<br/> | Identifica el nodo de la topología para este receptor de medios.<br/> <br/> |



## <a name="remarks"></a>Observaciones

La sesión multimedia genera este evento si recibe alguno de los siguientes eventos del receptor de medios:

-   [MEAudioSessionDeviceRemoved](meaudiosessiondeviceremoved.md)

-   [MEAudioSessionDisconnected](meaudiosessiondisconnected.md)

-   [MEAudioSessionExclusiveModeOverride](meaudiosessionexclusivemodeoverride.md)

-   [MEAudioSessionFormatChanged](meaudiosessionformatchanged.md)

-   [MEAudioSessionServerShutdown](meaudiosessionservershutdown.md)

Un receptor de medios también puede generar este evento, en cuyo caso la sesión multimedia establece el atributo de [**\_ nodo de \_ salida \_ de evento MF**](mf-event-output-node-attribute.md) en el evento y reenvía el evento a la aplicación.

Si la aplicación recibe este evento, debe volver a crear el receptor de medios y poner en cola la topología de nuevo.

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

 

 




