---
description: Propiedades del punto de conexión de audio
ms.assetid: db85ff3b-dbb1-4ed0-b663-21ca9eb66352
title: Propiedades del punto de conexión de audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf76ef70afaed98ed04ad2ee56e83c38c14ffde1bb6e4d43b557d25769afb2f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117828506"
---
# <a name="audio-endpoint-properties"></a>Propiedades del punto de conexión de audio

El archivo de encabezado Mmdeviceapi.h define varias propiedades de los dispositivos de punto de conexión de [audio](audio-endpoint-devices.md) Windows Vista y versiones posteriores. El Windows de audio establece los valores de estas propiedades. Los clientes pueden leer estas propiedades, pero no deben establecerlas. Los valores de propiedad se almacenan **como estructuras PROPVARIANT.**

La manera recomendada de leer las propiedades de un dispositivo de entrada de audio es usar las API del [**Windows. Espacio de nombres Devices.Enumeration.**](/uwp/api/Windows.Devices.Enumeration) Estas API son compatibles con las aplicaciones Windows store y las aplicaciones de escritorio. Para las aplicaciones de escritorio existentes que leen las propiedades del dispositivo mediante [**la interfaz IMMDevice,**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) consulte [Propiedades del dispositivo.](device-properties.md) **IMMDevice** no se admite para aplicaciones Windows Store.

Para ver ejemplos de código que muestran cómo acceder a las propiedades de un dispositivo de punto de conexión de audio, consulte los temas siguientes:

-   [Eventos de dispositivo](device-events.md)
-   [Roles de dispositivo para aplicaciones Direct Sound](device-roles-for-directsound-applications.md)

Para obtener información **sobre PROPVARIANT,** consulte la documentación Windows SDK.

Las siguientes propiedades son específicas de los dispositivos de punto de conexión de audio.



| Propiedad                                                                                                            | Descripción                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PKEY \_ AudioEndpoint \_ Association**](pkey-audioendpoint-association.md)                                          | Asocia una categoría de pin de kernel-streaming (KS) a un dispositivo de punto de conexión de audio.                                                                                |
| [**PKEY \_ AudioEndpoint \_ ControlPanelPageProvider**](pkey-audioendpoint-controlpanelpageprovider.md)                | Especifica el CLSID del proveedor registrado de la extensión device-properties para el dispositivo de punto de conexión de audio.                                              |
| [**PKEY \_ AudioEndpoint \_ Disable \_ SysFx**](pkey-audioendpoint-disable-sysfx.md)                                     | Indica si los efectos del sistema están habilitados en la secuencia en modo compartido que fluye hacia o desde el dispositivo de punto de conexión de audio.                                       |
| [**PKEY \_ AudioEndpoint \_ FormFactor**](pkey-audioendpoint-formfactor.md)                                            | Indica los atributos físicos del dispositivo de punto de conexión de audio.                                                                                               |
| [**PKEY \_ AudioEndpoint \_ FullRangeSpeakers**](pkey-audioendpoint-fullrangespeakers.md)                              | Especifica la máscara de configuración de canal para los altavoces de intervalo completo que están conectados al dispositivo de punto de conexión de audio.                                         |
| [**PKEY \_ AudioEndpoint \_ GUID**](pkey-audioendpoint-guid.md)                                                        | Proporciona el identificador de dispositivo Direct Sound que corresponde al dispositivo de punto de conexión de audio.                                                                     |
| [**PKEY \_ AudioEndpoint \_ PhysicalSpeakers**](pkey-audioendpoint-physicalspeakers.md)                                | Define la configuración del altavoz físico para el dispositivo de punto de conexión de audio.                                                                                     |
| [**PKEY \_ AudioEngine \_ DeviceFormat**](pkey-audioengine-deviceformat.md)                                            | Especifica el formato del dispositivo, que es el formato que usa el motor de audio para la secuencia en modo compartido que fluye hacia o desde el dispositivo de punto de conexión de audio.       |
| [**PKEY \_ AudioEngine \_ OEMFormat**](pkey-audioengine-oemformat.md)<br/>                                       | Especifica el formato predeterminado del dispositivo que se usa para representar o capturar una secuencia. El OEM rellena los valores en un archivo .inf. <br/> |
| [**PKEY \_ AudioEndpoint \_ admite el modo \_ EventDriven \_**](pkey-audioendpoint-supports-eventdriven-mode.md)<br/> | Indica si el punto de conexión admite el modo controlado por eventos. El OEM rellena los valores en un archivo .inf.<br/>                                |



 

Las API de audio principales admiten propiedades adicionales que no se aplican exclusivamente a los dispositivos de punto de conexión de audio. Para obtener más información sobre estas propiedades adicionales, vea [Propiedades del dispositivo.](device-properties.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Dispositivos de punto de conexión de audio](audio-endpoint-devices.md)
</dt> <dt>

[**Referencia de programación**](programming-reference.md)
</dt> </dl>

 

