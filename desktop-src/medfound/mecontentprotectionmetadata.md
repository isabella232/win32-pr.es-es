---
description: Media Stream usa este evento para enviar metadatos específicos del sistema de protección al descodificador.
ms.assetid: 249446CA-AEF7-41A1-98EB-0B9392AE4AD8
title: Evento MEContentProtectionMetadata (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1dd72289a900b9c9b96fe9a64d427dab13110d66
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127579944"
---
# <a name="mecontentprotectionmetadata-event"></a>Evento MEContentProtectionMetadata

Media Stream usa este evento para enviar metadatos específicos del sistema de protección al descodificador.

## <a name="event-values"></a>Valores de evento

Los valores posibles recuperados [**de IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluyen lo siguiente.



| VARTYPE              | Descripción                           |
|----------------------|---------------------------------------|
| VT \_ EMPTY<br/> | Sin datos del evento.<br/> <br/> |



## <a name="attributes"></a>Atributos

Para este evento, se definen los atributos siguientes.



| Atributo                                                                                              | Descripción                                                                                         |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [MF \_ EVENT \_ STREAM \_ METADATA \_ KEYDATA](mf-event-stream-metadata-keydata.md)<br/>                | Es un atributo opcional. Datos específicos del sistema de protección.<br/> <br/>              |
| [\_KEYIDS DE CONTENIDO DE \_ \_ \_ METADATOS DE \_ MF EVENT STREAM](mf-event-stream-metadata-content-keyids.md)<br/> | Los IDs de clave de contenido a los que está asociado el evento.<br/> <br/>                          |
| [MF \_ EVENT \_ STREAM \_ METADATA \_ SYSTEMID](mf-event-stream-metadata-systemid.md)<br/>              | Es un atributo opcional. Identificador del sistema para el que están previstos los datos de clave.<br/> <br/> |



## <a name="remarks"></a>Observaciones

Este evento se usa, por ejemplo, para comunicar el evento de rotación de claves. En este caso, se debe enviar lo antes posible para dar al descodificador tiempo para prepararse antes de que comiencen a llegar los ejemplos cifrados con el nuevo identificador de clave.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8.1 solo aplicaciones de escritorio\]<br/>                                                             |
| Servidor mínimo compatible<br/> | Windows Server 2012 Solo aplicaciones \[ de escritorio R2\]<br/>                                                  |
| Encabezado<br/>                   | <dl> <dt>Mfobjects.h (incluir Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Media Foundation eventos](media-foundation-events.md)
</dt> </dl>

 

 




