---
description: Lo genera un origen multimedia cuando actualiza sus metadatos.
ms.assetid: 6818b0c9-9628-41e6-8dc6-dff26f4fcfd2
title: Evento MESourceMetadataChanged (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b72463d145d7b4b4b14ac3c321f19a7f9a4c2178
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001266"
---
# <a name="mesourcemetadatachanged-event"></a>Evento MESourceMetadataChanged

Lo genera un origen multimedia cuando actualiza sus metadatos.

## <a name="event-values"></a>Valores de evento

Los valores posibles recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) son los siguientes.



| VARTYPE              | Descripción                           |
|----------------------|---------------------------------------|
| VT \_ vacío<br/> | Sin datos del evento.<br/> <br/> |



## <a name="remarks"></a>Observaciones

Si el origen multimedia no puede proporcionar todos los metadatos cuando el origen se crea por primera vez, debería producir este evento una vez que los metadatos estén disponibles.

El origen multimedia debe crear un nuevo descriptor de presentación y copiar todos los atributos del descriptor de presentación (PD) en el objeto de evento. La aplicación puede utilizar el objeto de evento para enumerar los nuevos atributos PD. En concreto, es posible que los valores de la [ \_ \_ duración de MF PD](mf-pd-duration-attribute.md) y el [ \_ \_ \_ \_ Tamaño total de archivo MF PD](mf-pd-total-file-size-attribute.md) sean desconocidos hasta que el archivo se descargue completamente.

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

[Atributos de descriptor de presentación](presentation-descriptor-attributes.md)
</dt> </dl>

 

 




