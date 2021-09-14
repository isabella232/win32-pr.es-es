---
description: 'Más información sobre: PKEY_AudioEndpoint_PhysicalSpeakers'
ms.assetid: 20049071-0a14-421e-8bc5-04af9c7117b0
title: PKEY_AudioEndpoint_PhysicalSpeakers (Mmdeviceapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6a627ec97dc329f50cc58a15d0df516f598af86
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127164909"
---
# <a name="pkey_audioendpoint_physicalspeakers"></a>PKEY \_ AudioEndpoint \_ PhysicalSpeakers

La **propiedad PKEY \_ AudioEndpoint \_ PhysicalSpeakers** especifica la máscara de configuración de canal para el dispositivo de punto de conexión de audio. La máscara indica la configuración física de un conjunto de oradores y especifica la asignación de canales a los hablantes. Para obtener más información sobre las máscaras de configuración de canal, vea lo siguiente:

1.  Descripción de la propiedad KSPROPERTY \_ AUDIO CHANNEL CONFIG en la documentación Windows \_ \_ DDK.
2.  Las white paper tituladas "Audio Driver Support for Home Speaker Configurations" (Compatibilidad del controlador de audio para configuraciones de altavoz de home Speaker) en el sitio web de [Audio Device Technologies for Windows.](https://www.microsoft.com/whdc/device/audio/default.mspx)

El **miembro vt** de la estructura **PROPVARIANT** se establece en VT \_ UI4.

El **miembro uintVal** de la **estructura PROPVARIANT** contiene una máscara de configuración de canal que se convierte al tipo **UINT**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                     |
| Encabezado<br/>                   | <dl> <dt>Mmdeviceapi.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Propiedades del punto de conexión de audio**](audio-endpoint-properties.md)
</dt> <dt>

[Propiedades de audio principal](core-audio-properties.md)
</dt> </dl>

 

 




