---
description: 'Más información sobre: PKEY_AudioEndpoint_PhysicalSpeakers'
ms.assetid: 20049071-0a14-421e-8bc5-04af9c7117b0
title: PKEY_AudioEndpoint_PhysicalSpeakers (Mmdeviceapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 358623626274a0ab3a0898e9e912e4f5f990c14d00dd6f6ef57bb4050297403f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118406421"
---
# <a name="pkey_audioendpoint_physicalspeakers"></a>PKEY \_ AudioEndpoint \_ PhysicalSpeakers

La **propiedad PKEY \_ AudioEndpoint \_ PhysicalSpeakers** especifica la máscara de configuración de canal para el dispositivo de punto de conexión de audio. La máscara indica la configuración física de un conjunto de hablantes y especifica la asignación de canales a los hablantes. Para obtener más información sobre las máscaras de configuración de canal, vea lo siguiente:

1.  La descripción de la propiedad KSPROPERTY \_ AUDIO CHANNEL CONFIG en la documentación Windows \_ \_ DDK.
2.  Las white paper tituladas "Audio Driver Support for Home Speaker Configurations" (Compatibilidad del controlador de audio para configuraciones de altavoz de home speaker) en audio [device technologies for Windows](https://www.microsoft.com/whdc/device/audio/default.mspx) website (Tecnologías de dispositivos de audio para Windows sitio web).

El **miembro vt** de la estructura **PROPVARIANT** se establece en VT \_ UI4.

El **miembro uintVal** de la **estructura PROPVARIANT** contiene una máscara de configuración de canal que se convierte al tipo **UINT**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Mmdeviceapi.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Propiedades del punto de conexión de audio**](audio-endpoint-properties.md)
</dt> <dt>

[Propiedades de audio principal](core-audio-properties.md)
</dt> </dl>

 

 




