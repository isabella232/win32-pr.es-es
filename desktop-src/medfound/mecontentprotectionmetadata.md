---
description: El flujo multimedia usa este evento para enviar metadatos específicos del sistema de protección al descodificador.
ms.assetid: 249446CA-AEF7-41A1-98EB-0B9392AE4AD8
title: Evento MEContentProtectionMetadata (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1dd72289a900b9c9b96fe9a64d427dab13110d66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908255"
---
# <a name="mecontentprotectionmetadata-event"></a>Evento MEContentProtectionMetadata

El flujo multimedia usa este evento para enviar metadatos específicos del sistema de protección al descodificador.

## <a name="event-values"></a>Valores de evento

Los valores posibles recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) son los siguientes.



| VARTYPE              | Descripción                           |
|----------------------|---------------------------------------|
| VT \_ vacío<br/> | Sin datos del evento.<br/> <br/> |



## <a name="attributes"></a>Atributos

Para este evento, se definen los atributos siguientes.



| Atributo                                                                                              | Descripción                                                                                         |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [\_KEYDATA de \_ \_ metadatos del flujo de eventos MF \_](mf-event-stream-metadata-keydata.md)<br/>                | Es un atributo opcional. Datos específicos del sistema de protección.<br/> <br/>              |
| [\_contenido de \_ metadatos del flujo de eventos MF \_ \_ \_ KEYIDS](mf-event-stream-metadata-content-keyids.md)<br/> | Los identificadores de clave de contenido a los que está asociado el evento.<br/> <br/>                          |
| [\_SYSTEMID de \_ \_ metadatos del flujo de eventos MF \_](mf-event-stream-metadata-systemid.md)<br/>              | Es un atributo opcional. IDENTIFICADOR del sistema para el que se van a usar los datos de la clave.<br/> <br/> |



## <a name="remarks"></a>Observaciones

Este evento se utiliza, por ejemplo, para el evento de rotación de claves de comunicación. En este caso, se debe enviar tan pronto como sea posible para dar tiempo al descodificador a la preparación antes de que lleguen los ejemplos cifrados con el nuevo ID. de clave.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio Windows 8.1\]<br/>                                                             |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]<br/>                                                  |
| Encabezado<br/>                   | <dl> <dt>Mfobjects. h (incluye Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Eventos de Media Foundation](media-foundation-events.md)
</dt> </dl>

 

 




