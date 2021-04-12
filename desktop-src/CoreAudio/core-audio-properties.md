---
description: Esta referencia de programación para el SDK de audio básico incluye las siguientes propiedades.
ms.assetid: db7d68c3-5642-4238-a212-88d3479ce73d
title: Propiedades de audio principales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41528e66977f1f3b9282cf78ba76e4bae32c5bd6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538320"
---
# <a name="core-audio-properties"></a>Propiedades de audio principales

Esta referencia de programación para el SDK de audio básico incluye las siguientes propiedades.

## <a name="audio-endpoint-properties"></a>Propiedades de punto de conexión de audio

Core Audio SDK incluye varias propiedades de [dispositivos de punto de conexión de audio](audio-endpoint-devices.md). Para obtener más información, vea [propiedades del punto de conexión de audio](audio-endpoint-properties.md).

Las siguientes propiedades se definen en Mmdeviceapi. h en Windows Vista y versiones posteriores.



| Propiedad                                                                                                            | Descripción                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Asociación de PKEY \_ AudioEndpoint \_**](pkey-audioendpoint-association.md)                                          | Asocia una categoría de PIN de streaming de kernel (KS) a un dispositivo de punto de conexión de audio.                                                                                |
| [**PKEY \_ AudioEndpoint \_ ControlPanelPageProvider**](pkey-audioendpoint-controlpanelpageprovider.md)                | Especifica el CLSID del proveedor registrado de la extensión de propiedades de dispositivo para el dispositivo de punto de conexión de audio.                                              |
| [**PKEY \_ AudioEndpoint \_ deshabilitar \_ SysFx**](pkey-audioendpoint-disable-sysfx.md)                                     | Indica si los efectos del sistema están habilitados en la secuencia de modo compartido que fluye hacia o desde el dispositivo de punto de conexión de audio.                                       |
| [**PKEY \_ AudioEndpoint \_ FormFactor**](pkey-audioendpoint-formfactor.md)                                            | Indica los atributos físicos del dispositivo de extremo de audio.                                                                                               |
| [**PKEY \_ AudioEndpoint \_ FullRangeSpeakers**](pkey-audioendpoint-fullrangespeakers.md)                              | Especifica la máscara de configuración de canal para los altavoces de intervalo completo que están conectados al dispositivo de extremo de audio.                                         |
| [**GUID de PKEY \_ AudioEndpoint \_**](pkey-audioendpoint-guid.md)                                                        | Proporciona el identificador de dispositivo de DirectSound que corresponde al dispositivo de punto de conexión de audio.                                                                     |
| [**PKEY \_ AudioEndpoint \_ PhysicalSpeakers**](pkey-audioendpoint-physicalspeakers.md)                                | Define la configuración de los altavoces físicos para el dispositivo de punto de conexión de audio.                                                                                     |
| [**PKEY \_ Audioengine \_ DeviceFormat**](pkey-audioengine-deviceformat.md)                                            | Especifica el formato del dispositivo, que es el formato que usa el motor de audio para la secuencia de modo compartido que fluye hacia o desde el dispositivo de extremo de audio.       |
| [**PKEY \_ Audioengine \_ OEMFormat**](pkey-audioengine-oemformat.md)<br/>                                       | Especifica el formato predeterminado del dispositivo que se usa para representar o capturar un flujo. El OEM rellena los valores en un archivo. inf. <br/> |
| [**PKEY \_ AudioEndpoint \_ admite \_ el \_ modo EventDriven**](pkey-audioendpoint-supports-eventdriven-mode.md)<br/> | Indica si el extremo admite el modo basado en eventos. El OEM rellena los valores en un archivo. inf.<br/>                                |
| [**PKEY \_ AudioEndpoint \_ JackSubType**](pkey-audioendpoint-jacksubtype.md)<br/>                               | Contiene un GUID de categoría de salida para un dispositivo de punto de conexión de audio. <br/>                                                                                    |



 

## <a name="device-properties"></a>Propiedades de dispositivos

El SDK de audio Core incluye varias propiedades de dispositivo de [dispositivos de punto de conexión de audio](audio-endpoint-devices.md). Para obtener más información, consulte [propiedades del dispositivo](device-properties.md).

Las siguientes propiedades se definen en Functiondiscoverykeys \_ devpkey. h en Windows Vista y versiones posteriores.



| Propiedad                                                                         | Descripción                                                                                                                                                                                       |
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PKEY \_ DeviceInterface \_ FriendlyName**](pkey-deviceinterface-friendlyname.md) | El nombre descriptivo del adaptador de audio al que está conectado el dispositivo de extremo (por ejemplo, "adaptador de audio XYZ").                                                                               |
| [**\_DeviceDesc de dispositivo PKEY \_**](pkey-device-devicedesc.md)                       | La descripción del dispositivo de extremo (por ejemplo, "altavoces").                                                                                                                          |
| [**PKEY el \_ dispositivo \_ FriendlyName**](pkey-device-friendlyname.md)                   | El nombre descriptivo del dispositivo de extremo (por ejemplo, "altavoces (adaptador de audio XYZ)").                                                                                                           |
| **\_ContainerId del dispositivo PKEY \_**                                                    | Almacena el identificador del contenedor del dispositivo PnP que implementa el punto de conexión de audio. Para obtener más información sobre esta propiedad, vea "referencia de propiedades de dispositivo" en la documentación de Windows WDK. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de programación](programming-reference.md)
</dt> </dl>

 

 




