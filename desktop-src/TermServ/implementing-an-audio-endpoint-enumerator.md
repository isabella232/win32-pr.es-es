---
title: Implementación de un enumerador de punto de conexión de audio personalizado
description: A partir de Windows Server 2008 R2, puede implementar un enumerador de punto de conexión de audio remoto personalizado como parte de un proveedor de protocolo Escritorio remoto.
ms.assetid: 684bd62e-1e28-4330-a3c5-6bce684d652d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 435ab2a572169f20a7f8f9db194449be5361e409
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/08/2020
ms.locfileid: "105676519"
---
# <a name="implementing-a-custom-audio-endpoint-enumerator"></a>Implementación de un enumerador de punto de conexión de audio personalizado

A partir de Windows Server 2008 R2, puede implementar un enumerador de punto de conexión de audio remoto personalizado como parte de un proveedor de protocolo Escritorio remoto. Un proveedor de protocolo de Escritorio remoto puede utilizar un enumerador de punto de conexión de audio personalizado para recuperar una colección de puntos de conexión de audio que tienen un conjunto específico de funcionalidades.

**Para implementar un enumerador de punto de conexión de audio remoto personalizado**

1.  La solución de enumerador de punto de conexión personalizada debe implementar cuatro tipos principales de objetos: objetos de enumerador de dispositivos, objetos de colección de dispositivos, objetos de dispositivo y objetos de almacén de propiedades.

    

    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>Tipo de objeto</th>
    <th>Descripción</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td>Objeto de enumerador de dispositivo<br/></td>
    <td>Un objeto de enumerador de dispositivo proporciona la funcionalidad de enumerador de extremo. Expone métodos que devuelven un punto de conexión predeterminado y colecciones de extremos especificadas. Por ejemplo, en función de los criterios especificados, el enumerador puede devolver puntos de conexión de comunicación, puntos de conexión de reproducción o puntos de conexión de captura. El objeto de enumerador de dispositivos debe implementar la interfaz <a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator"><strong>IMMDeviceEnumerator</strong></a> .<br/></td>
    </tr>
    <tr class="even">
    <td>Objeto de colección de dispositivos<br/></td>
    <td>Un objeto de colección de dispositivos representa una colección de dispositivos de audio. Debe implementar la interfaz <a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdevicecollection"><strong>IMMDeviceCollection</strong></a> .<br/></td>
    </tr>
    <tr class="odd">
    <td>Objeto de dispositivo<br/></td>
    <td>Un objeto de dispositivo representa un dispositivo de audio determinado. Proporciona acceso al almacén de propiedades del dispositivo de audio y expone las interfaces de captura y reproducción de audio disponibles en el dispositivo. El objeto de dispositivo debe implementar las interfaces <a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdevice"><strong>IMMDevice</strong></a> y <a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immendpoint"><strong>IMMEndpoint</strong></a> .<br/></td>
    </tr>
    <tr class="even">
    <td>Objeto de almacén de propiedades<br/></td>
    <td>Un objeto de almacén de propiedades expone las propiedades asociadas a un dispositivo de audio. El sistema utiliza algunas de estas propiedades, pero las aplicaciones también pueden almacenar propiedades arbitrarias con el punto de conexión de audio.<br/> Todos los dispositivos de audio tienen las tres propiedades siguientes:<br/>
    <ul>
    <li><a href="/windows/desktop/CoreAudio/pkey-deviceinterface-friendlyname"><strong>PKEY_DeviceInterface_FriendlyName</strong></a></li>
    <li><a href="/windows/desktop/CoreAudio/pkey-device-devicedesc"><strong>PKEY_Device_DeviceDesc</strong></a></li>
    <li><a href="/windows/desktop/CoreAudio/pkey-device-friendlyname"><strong>PKEY_Device_FriendlyName</strong></a></li>
    </ul>
El objeto de almacén de propiedades debe implementar la interfaz <a href="/windows/win32/api/propsys/nn-propsys-ipropertystore">IPropertyStore</a> .<br/></td>
    </tr>
    </tbody>
    </table>

    

     

2.  El enumerador de punto de conexión personalizado debe implementarse en un archivo DLL que se pueda cargar en el sistema de audio y en otras aplicaciones. La DLL debe estar firmada para que los procesos seguros puedan cargarla. El archivo DLL debe implementar y exportar la función [**GetTSAudioEndpointEnumeratorForSession**](gettsaudioendpointenumeratorforsession.md) , que actúa como punto de entrada para el enumerador de punto de conexión personalizado.

El servicio Servicios de Escritorio remoto llama al método [**QueryProperty**](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-queryproperty) y establece el parámetro *QueryType* en la **consulta de WTS \_ \_ AUDIOENUM \_ dll** para recuperar el nombre del objeto de enumerador.

Los objetos de enumerador personalizados usan interfaces de tipo COM y un mecanismo de recuento de referencias COM, pero no son objetos COM verdaderos. El enumerador de punto de conexión personalizado debe tener la capacidad de trabajar con las interfaces de audio heredadas que usan las aplicaciones que no admiten COM. Por esta razón, el enumerador de punto de conexión personalizado no debe basarse en el mecanismo de administración del ciclo de vida de COM. Los consumidores del enumerador de punto de conexión de audio, como MMDevAPI.dll, cargan el archivo DLL del enumerador de punto de conexión personalizado cuando lo requieren las aplicaciones de usuario y no descargan el enumerador mientras el enumerador contiene una referencia a un objeto de enumerador de dispositivo, objeto de colección de dispositivos, objeto de dispositivo o objeto de almacén de propiedades. No obstante, no es posible que estos consumidores realicen un seguimiento de las referencias a otros tipos de objetos propiedad del enumerador de extremo personalizado. En consecuencia, se recomienda que el enumerador de punto de conexión personalizado no cree ningún objeto que durar más estos cuatro tipos de objetos.

## <a name="to-implement-a-custom-audio-endpoint"></a>Para implementar un punto de conexión de audio personalizado

Para implementar un enumerador de dispositivo de audio personalizado, debe implementar un punto de conexión de audio personalizado. La forma en que se vinculan los dispositivos de audio personalizados es mediante el uso de las dos instrucciones siguientes:

-   `IMMDevice::Activate(IAudioOutputEndpointRT)`
-   `IMMDevice::Activate(IAudioInputEndpointRT)`

No esperamos implementar la lista completa de interfaces [**IMMDevice:: Activate**](/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-immdevice-activate) en el enumerador de dispositivos de audio personalizado. En su lugar, debe implementar [**IAudioOutputEndpointRT**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudiooutputendpointrt) y [**IAudioInputEndpointRT**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioinputendpointrt). Opcionalmente, puede implementar algunos más, como [**IAudioEndpointVolume**](/windows/desktop/api/endpointvolume/nn-endpointvolume-iaudioendpointvolume). Para cualquier interfaz que no implemente, debe devolver **E \_ nointerface** (debe usar este código de error específico). A continuación, Windows revierte a una implementación estándar de la interfaz (por ejemplo, [**IAudioClient2**](/windows/desktop/api/audioclient/nn-audioclient-iaudioclient2)).

Para obtener documentación de referencia adicional sobre cómo implementar y registrar puntos de conexión de audio, vea [**IAudioInputEndpointRT**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioinputendpointrt). Para ver un diagrama que muestra cómo funciona WASAPI, consulte [componentes de audio de modo de usuario](/windows/desktop/CoreAudio/user-mode-audio-components). Tenga en cuenta que todo el audio de modo usuario es nuevo a partir de Windows Server 2008.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Creación de un proveedor de Protocolo de escritorio remoto](creating-a-custom-remote-protocol.md)
</dt> <dt>

[**GetTSAudioEndpointEnumeratorForSession**](gettsaudioendpointenumeratorforsession.md)
</dt> <dt>

[**IMMDevice**](/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdevice)
</dt> <dt>

[**IMMDeviceCollection**](/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdevicecollection)
</dt> <dt>

[**IMMDeviceEnumerator**](/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator)
</dt> <dt>

[**IMMEndpoint**](/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immendpoint)
</dt> <dt>

[IPropertyStore](/windows/win32/api/propsys/nn-propsys-ipropertystore)
</dt> </dl>