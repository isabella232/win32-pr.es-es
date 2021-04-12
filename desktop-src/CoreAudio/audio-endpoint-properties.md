---
description: Propiedades de punto de conexión de audio
ms.assetid: db85ff3b-dbb1-4ed0-b663-21ca9eb66352
title: Propiedades de punto de conexión de audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d6ce4ed9b853c2b73b73de014f3a4c8a90072a9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104274980"
---
# <a name="audio-endpoint-properties"></a>Propiedades de punto de conexión de audio

El archivo de encabezado Mmdeviceapi. h define varias propiedades de los [dispositivos de punto de conexión de audio](audio-endpoint-devices.md) en Windows Vista y versiones posteriores. El servicio audio de Windows establece los valores de estas propiedades. Los clientes pueden leer estas propiedades, pero no deben establecerlas. Los valores de propiedad se almacenan como estructuras **PROPVARIANT** .

La forma recomendada de leer las propiedades de un dispositivo de entrada de audio es usar las API del espacio de nombres [**Windows. Devices. Enumeration**](/uwp/api/Windows.Devices.Enumeration) . Estas API son compatibles con las aplicaciones de la tienda Windows y las aplicaciones de escritorio. Para las aplicaciones de escritorio existentes que leen las propiedades del dispositivo mediante la interfaz [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) , consulte [propiedades del dispositivo](device-properties.md). **IMMDevice** no se admite para aplicaciones de la tienda Windows.

Para ver ejemplos de código que muestran cómo obtener acceso a las propiedades de un dispositivo de extremo de audio, consulte los temas siguientes:

-   [Eventos de dispositivo](device-events.md)
-   [Roles de dispositivo para aplicaciones DirectSound](device-roles-for-directsound-applications.md)

Para obtener información sobre **PROPVARIANT**, consulte la documentación de Windows SDK.

Las siguientes propiedades son específicas de los dispositivos de punto de conexión de audio.



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



 

Las API de audio principales admiten propiedades adicionales que no se aplican exclusivamente a los dispositivos de punto de conexión de audio. Para obtener más información acerca de estas propiedades adicionales, consulte [propiedades del dispositivo](device-properties.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Dispositivos de punto de conexión de audio](audio-endpoint-devices.md)
</dt> <dt>

[**Referencia de programación**](programming-reference.md)
</dt> </dl>

 

