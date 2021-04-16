---
description: Lo genera un origen multimedia cuando finaliza una presentación. Este evento indica que se han completado todas las secuencias de la presentación. La sesión multimedia reenvía este evento a la aplicación.
ms.assetid: 259b00ae-a91b-461b-a12f-f7291ecc04ff
title: Evento MEEndOfPresentation (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5e3a904725908d83afd54bbd64012420075037a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652543"
---
# <a name="meendofpresentation-event"></a>Evento MEEndOfPresentation

Lo genera un origen multimedia cuando finaliza una presentación. Este evento indica que se han completado todas las secuencias de la presentación. La sesión multimedia reenvía este evento a la aplicación.

## <a name="event-values"></a>Valores de evento

Los valores posibles recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) son los siguientes.



| VARTYPE              | Descripción                           |
|----------------------|---------------------------------------|
| VT \_ vacío<br/> | Sin datos del evento.<br/> <br/> |



## <a name="attributes"></a>Atributos

Para este evento, se definen los atributos siguientes.



| Atributo                                                                                               | Descripción                                                                               |
|---------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [**\_topología de origen de eventos MF \_ \_ \_ cancelada**](mf-event-source-topology-canceled-attribute.md)<br/> | Especifica si el origen del secuenciador canceló esta presentación.<br/> <br/> |



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

 

 




