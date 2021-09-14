---
description: Esta referencia de programación para core Audio SDK incluye las siguientes propiedades.
ms.assetid: db7d68c3-5642-4238-a212-88d3479ce73d
title: Propiedades de audio principal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41528e66977f1f3b9282cf78ba76e4bae32c5bd6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127165082"
---
# <a name="core-audio-properties"></a>Propiedades de audio principal

Esta referencia de programación para core Audio SDK incluye las siguientes propiedades.

## <a name="audio-endpoint-properties"></a>Propiedades del punto de conexión de audio

Core Audio SDK incluye varias propiedades de dispositivos de [punto de conexión de audio.](audio-endpoint-devices.md) Para obtener más información, vea [Propiedades del punto de conexión de audio](audio-endpoint-properties.md).

Las siguientes propiedades se definen en Mmdeviceapi.h en Windows Vista y versiones posteriores.



| Propiedad                                                                                                            | Descripción                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PKEY \_ AudioEndpoint \_ Association**](pkey-audioendpoint-association.md)                                          | Asocia una categoría de pin de kernel-streaming (KS) a un dispositivo de punto de conexión de audio.                                                                                |
| [**PKEY \_ AudioEndpoint \_ ControlPanelPageProvider**](pkey-audioendpoint-controlpanelpageprovider.md)                | Especifica el CLSID del proveedor registrado de la extensión device-properties para el dispositivo de punto de conexión de audio.                                              |
| [**PKEY \_ AudioEndpoint \_ Deshabilitar \_ SysFx**](pkey-audioendpoint-disable-sysfx.md)                                     | Indica si los efectos del sistema están habilitados en la secuencia en modo compartido que fluye hacia o desde el dispositivo de punto de conexión de audio.                                       |
| [**PKEY \_ AudioEndpoint \_ FormFactor**](pkey-audioendpoint-formfactor.md)                                            | Indica los atributos físicos del dispositivo de punto de conexión de audio.                                                                                               |
| [**PKEY \_ AudioEndpoint \_ FullRangeSpeakers**](pkey-audioendpoint-fullrangespeakers.md)                              | Especifica la máscara de configuración de canal para los altavoces de intervalo completo que están conectados al dispositivo de punto de conexión de audio.                                         |
| [**PKEY \_ AudioEndpoint \_ GUID**](pkey-audioendpoint-guid.md)                                                        | Proporciona el identificador de dispositivo DirectSound que corresponde al dispositivo de punto de conexión de audio.                                                                     |
| [**PKEY \_ AudioEndpoint \_ PhysicalSpeakers**](pkey-audioendpoint-physicalspeakers.md)                                | Define la configuración del altavoz físico para el dispositivo de punto de conexión de audio.                                                                                     |
| [**PKEY \_ AudioEngine \_ DeviceFormat**](pkey-audioengine-deviceformat.md)                                            | Especifica el formato del dispositivo, que es el formato que usa el motor de audio para la secuencia en modo compartido que fluye hacia o desde el dispositivo del punto de conexión de audio.       |
| [**PKEY \_ AudioEngine \_ OEMFormat**](pkey-audioengine-oemformat.md)<br/>                                       | Especifica el formato predeterminado del dispositivo que se usa para representar o capturar una secuencia. El OEM rellena los valores en un archivo .inf. <br/> |
| [**PKEY \_ AudioEndpoint \_ admite el modo \_ EventDriven \_**](pkey-audioendpoint-supports-eventdriven-mode.md)<br/> | Indica si el punto de conexión admite el modo controlado por eventos. El OEM rellena los valores en un archivo .inf.<br/>                                |
| [**PKEY \_ AudioEndpoint \_ JackSubType**](pkey-audioendpoint-jacksubtype.md)<br/>                               | Contiene un GUID de categoría de salida para un dispositivo de punto de conexión de audio. <br/>                                                                                    |



 

## <a name="device-properties"></a>Propiedades de dispositivos

Core Audio SDK incluye varias propiedades de dispositivo de dispositivos de [punto de conexión de audio.](audio-endpoint-devices.md) Para obtener más información, vea [Propiedades del dispositivo.](device-properties.md)

Las siguientes propiedades se definen en Functiondiscoverykeys \_ devpkey.h en Windows Vista y versiones posteriores.



| Propiedad                                                                         | Descripción                                                                                                                                                                                       |
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PKEY \_ DeviceInterface \_ FriendlyName**](pkey-deviceinterface-friendlyname.md) | Nombre descriptivo del adaptador de audio al que está conectado el dispositivo de punto de conexión (por ejemplo, "Adaptador de audio XYZ").                                                                               |
| [**Dispositivo de dispositivo \_ \_ PKEYDesc**](pkey-device-devicedesc.md)                       | Descripción del dispositivo del punto de conexión (por ejemplo, "Speakers").                                                                                                                          |
| [**PKEY \_ Device \_ FriendlyName**](pkey-device-friendlyname.md)                   | Nombre descriptivo del dispositivo del punto de conexión (por ejemplo, "Altavoces (adaptador de audio XYZ)").                                                                                                           |
| **PKEY \_ Device \_ ContainerId**                                                    | Almacena el identificador de contenedor del dispositivo PnP que implementa el punto de conexión de audio. Para obtener más información sobre esta propiedad, vea "Device Property Reference" (Referencia de propiedades de dispositivo) en la documentación Windows WDK. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de programación](programming-reference.md)
</dt> </dl>

 

 




