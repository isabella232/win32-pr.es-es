---
description: Lo genera un origen multimedia cuando actualiza sus metadatos.
ms.assetid: 6818b0c9-9628-41e6-8dc6-dff26f4fcfd2
title: Evento MESourceMetadataChanged (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 644d04cd2913afcd2f91a6c4f91dd352456bd09f32d132f7976e4cf27df985f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118061654"
---
# <a name="mesourcemetadatachanged-event"></a>Evento MESourceMetadataChanged

Lo genera un origen multimedia cuando actualiza sus metadatos.

## <a name="event-values"></a>Valores de evento

Entre los valores posibles recuperados [**de IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) se incluyen los siguientes.



| VARTYPE              | Descripción                           |
|----------------------|---------------------------------------|
| VT \_ EMPTY<br/> | Sin datos del evento.<br/> <br/> |



## <a name="remarks"></a>Comentarios

Si el origen de medios no puede proporcionar todos los metadatos cuando se crea el origen por primera vez, debe generar este evento después de que los metadatos estén disponibles.

El origen multimedia debe crear un nuevo descriptor de presentación y copiar todos los atributos del descriptor de presentación (PD) en el objeto de evento. La aplicación puede usar el objeto de evento para enumerar los nuevos atributos de PD. En concreto, los valores de [MF \_ PD \_ DURATION](mf-pd-duration-attribute.md) y [MF PD TOTAL FILE \_ \_ \_ \_ SIZE](mf-pd-total-file-size-attribute.md) podrían ser desconocidos hasta que el archivo se descargue por completo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Mfobjects.h (incluir Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Media Foundation eventos](media-foundation-events.md)
</dt> <dt>

[Atributos del descriptor de presentación](presentation-descriptor-attributes.md)
</dt> </dl>

 

 




