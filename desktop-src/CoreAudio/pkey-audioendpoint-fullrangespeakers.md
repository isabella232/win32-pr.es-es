---
description: La \_ propiedad FullRangeSpeakers de AudioEndpoint de PKEY \_ especifica la máscara de configuración de canal para los altavoces de intervalo completo que están conectados al dispositivo de extremo de audio.
ms.assetid: c0a54b3d-84dc-4771-8891-167ce00e2218
title: PKEY_AudioEndpoint_FullRangeSpeakers (Mmdeviceapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0990d08e3d78eddf0fa6397e888b1e26c9f9a767
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153408"
---
# <a name="pkey_audioendpoint_fullrangespeakers"></a>PKEY \_ AudioEndpoint \_ FullRangeSpeakers

La **propiedad \_ \_ FullRangeSpeakers de AudioEndpoint de PKEY** especifica la máscara de configuración de canal para los altavoces de intervalo completo que están conectados al dispositivo de extremo de audio. La máscara indica la configuración física de los altavoces de alcance completo y especifica la asignación de canales a esos altavoces.

El miembro **VT** de la estructura **PROPVARIANT** se establece en VT \_ UI4.

El miembro **uintVal** de la estructura **PROPVARIANT** contiene una máscara de configuración de canal que se convierte al tipo **uint**.

Un altavoz completo puede reproducir sonidos en todo el intervalo, desde graves hasta agudos. Normalmente, los altavoces más grandes son de intervalo completo, pero los altavoces más pequeños son significativamente menos capaces de reproducir sonidos graves. En Windows Vista, el motor de audio usa esta propiedad para administrar los niveles de graves en el flujo de salida de audio que reproduce el dispositivo de punto de conexión de audio.

La máscara de configuración de canal para esta propiedad está en el mismo formato que la máscara de configuración de canal para la propiedad [**PKEY \_ AudioEndpoint \_ PhysicalSpeakers**](pkey-audioendpoint-physicalspeakers.md) . Para obtener más información acerca de las máscaras de configuración de canal, consulte lo siguiente:

-   La descripción de la \_ propiedad de configuración de canal de audio KSPROPERTY \_ \_ en la documentación de DDK de Windows.
-   Las notas del producto titulada "compatibilidad con controladores de audio para las configuraciones de altavoz de Home Theater" en el sitio Web [de tecnologías de dispositivos de audio para Windows](https://www.microsoft.com/whdc/device/audio/default.mspx) .

El sistema obtiene la máscara de configuración de canal para la \_ propiedad PKEY AudioEndpoint \_ FullRangeSpeakers del usuario. El usuario especifica esta información a través del panel de control multimedia de Windows Mmsys.cpl. Para obtener más información acerca de Mmsys.cpl, consulte la documentación de DDK de Windows.

La máscara de configuración de canal para la \_ propiedad PKEY AudioEndpoint \_ FullRangeSpeakers de un dispositivo de punto de conexión de audio es un subconjunto de la máscara de configuración de canal para la \_ propiedad PKEY AudioEndpoint \_ PhysicalSpeakers del mismo dispositivo.

Por ejemplo, si un dispositivo de punto de conexión de audio impulsa un conjunto de altavoces de sonido envolvente 5,1, la máscara de configuración de canal para la \_ propiedad PKEY AudioEndpoint \_ PHYSICALSPEAKERS es KSAUDIO \_ Speaker \_ 5POINT1. Esta máscara indica la presencia de los oradores frontal-izquierdo, frontal-derecho, frontal, lateral y derecho, y un subwoofer. Si los altavoces delantero-izquierdo y delantero derecho son lo suficientemente grandes como para producir sonidos graves, pero no son los oradores más pequeños del centro y el lado del centro, la máscara de configuración de canal para la \_ propiedad PKEY AudioEndpoint \_ FULLRANGESPEAKERS es KSAUDIO \_ Speaker \_ estéreo, que indica solo los hablantes frontal y derecho. Channel-Configuration masks KSAUDIO \_ Speaker \_ 5POINT1 y KSAUDIO \_ Speaker \_ estéreo se definen en el archivo de encabezado Ksmedia. h.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                     |
| Encabezado<br/>                   | <dl> <dt>Mmdeviceapi. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Propiedades de punto de conexión de audio**](audio-endpoint-properties.md)
</dt> <dt>

[Propiedades de audio principales](core-audio-properties.md)
</dt> <dt>

[**\_ \_ Propiedad PHYSICALSPEAKERS de PKEY AudioEndpoint**](pkey-audioendpoint-physicalspeakers.md)
</dt> </dl>

 

 




