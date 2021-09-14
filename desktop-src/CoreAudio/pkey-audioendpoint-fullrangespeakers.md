---
description: La propiedad PKEY \_ AudioEndpoint FullRangeSpeakers especifica la máscara de configuración de canal para los altavoces de intervalo completo que están conectados al dispositivo de punto de \_ conexión de audio.
ms.assetid: c0a54b3d-84dc-4771-8891-167ce00e2218
title: PKEY_AudioEndpoint_FullRangeSpeakers (Mmdeviceapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0990d08e3d78eddf0fa6397e888b1e26c9f9a767
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127164925"
---
# <a name="pkey_audioendpoint_fullrangespeakers"></a>PKEY \_ AudioEndpoint \_ FullRangeSpeakers

La **propiedad PKEY \_ AudioEndpoint \_ FullRangeSpeakers** especifica la máscara de configuración de canal para los altavoces de intervalo completo que están conectados al dispositivo de punto de conexión de audio. La máscara indica la configuración física de los altavoces de intervalo completo y especifica la asignación de canales a esos hablantes.

El **miembro vt** de la estructura **PROPVARIANT** se establece en VT \_ UI4.

El **miembro uintVal** de la **estructura PROPVARIANT** contiene una máscara de configuración de canal que se convierte al tipo **UINT**.

Un altavoz de rango completo es capaz de reproducir sonidos en todo el intervalo, desde los sonidos hasta los triples. Normalmente, los hablantes más grandes son de gama completa, pero los altavoces más pequeños son significativamente menos capaces de reproducir sonidos de sonido. En Windows Vista, el motor de audio usa esta propiedad para administrar los niveles de sonido en el flujo de salida de audio que reproduce el dispositivo de punto de conexión de audio.

La máscara de configuración de canal para esta propiedad tiene el mismo formato que la máscara de configuración de canal para la propiedad [**PKEY \_ AudioEndpoint \_ PhysicalSpeakers.**](pkey-audioendpoint-physicalspeakers.md) Para obtener más información sobre las máscaras de configuración de canal, vea lo siguiente:

-   La descripción de la propiedad KSPROPERTY \_ AUDIO CHANNEL CONFIG en la documentación Windows \_ \_ DDK.
-   Las white paper tituladas "Audio Driver Support for Home Speaker Configurations" (Compatibilidad del controlador de audio para configuraciones de altavoz de home speaker) en el sitio web audio [device technologies for Windows.com.](https://www.microsoft.com/whdc/device/audio/default.mspx)

El sistema obtiene la máscara de configuración de canal para la propiedad PKEY \_ AudioEndpoint \_ FullRangeSpeakers del usuario. El usuario escribe esta información a través del panel de control multimedia Windows, Mmsys.cpl. Para obtener más información sobre Mmsys.cpl, consulte la documentación Windows DDK.

La máscara de configuración de canal para la propiedad PKEY AudioEndpoint FullRangeSpeakers de un dispositivo de punto de conexión de audio es un subconjunto de la máscara de configuración de canal para la propiedad \_ \_ PKEY \_ AudioEndpoint PhysicalSpeakers del mismo \_ dispositivo.

Por ejemplo, si un dispositivo de punto de conexión de audio impulsa un conjunto de altavoces de sonido envolvente 5.1, la máscara de configuración de canal para la propiedad PKEY \_ AudioEndpoint \_ PhysicalSpeakers es KSAUDIO \_ SPEAKER \_ 5POINT1. Esta máscara indica la presencia de hablantes front-left, front-right, front-center, side-left y side-right, además de un pie. Si los altavoces front-left y front-right son lo suficientemente grandes como para producir sonidos de sonido de sonido, pero los altavoces laterales y frontales más pequeños no lo son, la máscara de configuración de canal para la propiedad \_ PKEY AudioEndpoint FullRangeSpeakers es KSAUDIO SPEAKER STEREO, que indica solo los altavoces \_ \_ front-left y \_ front-right. Las máscaras de configuración de canal KSAUDIO SPEAKER 5POINT1 y KSAUDIO SPEAKER STEREO se definen en el archivo de \_ \_ encabezado \_ \_ Ksmedia.h.

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
</dt> <dt>

[**Propiedad PKEY \_ AudioEndpoint \_ PhysicalSpeakers**](pkey-audioendpoint-physicalspeakers.md)
</dt> </dl>

 

 




