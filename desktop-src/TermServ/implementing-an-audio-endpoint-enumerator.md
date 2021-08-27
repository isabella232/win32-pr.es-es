---
title: Implementar un enumerador de extremo de audio personalizado
description: A partir Windows Server 2008 R2, puede implementar un enumerador de punto de conexión de audio remoto personalizado como parte de un proveedor Escritorio remoto protocolo.
ms.assetid: 684bd62e-1e28-4330-a3c5-6bce684d652d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ae135d19e13e3b78fddbdd58bccd476b7e5ee7a
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122478861"
---
# <a name="implementing-a-custom-audio-endpoint-enumerator"></a>Implementar un enumerador de extremo de audio personalizado

A partir Windows Server 2008 R2, puede implementar un enumerador de punto de conexión de audio remoto personalizado como parte de un proveedor Escritorio remoto protocolo. Un Escritorio remoto de protocolos puede usar un enumerador de punto de conexión de audio personalizado para recuperar una colección de puntos de conexión de audio que tienen un conjunto específico de funcionalidades.

**Para implementar un enumerador de punto de conexión de audio remoto personalizado**

1.  La solución de enumerador de puntos de conexión personalizada debe implementar cuatro tipos principales de objetos: objetos enumerador de dispositivos, objetos de colección de dispositivos, objetos de dispositivo y objetos de almacén de propiedades.

    

    
| Tipo de objeto | Descripción | 
|-------------|-------------|
| Objeto enumerador de dispositivos<br /> | Un objeto enumerador de dispositivos proporciona la funcionalidad de enumerador de punto de conexión. Expone métodos que devuelven un punto de conexión predeterminado y colecciones especificadas de puntos de conexión. Por ejemplo, según los criterios especificados, el enumerador puede devolver puntos de conexión de comunicación, puntos de conexión de reproducción o capturar puntos de conexión. El objeto enumerador de dispositivos debe implementar la <a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator"><strong>interfaz IMMDeviceEnumerator.</strong></a><br /> | 
| Objeto de recopilación de dispositivos<br /> | Un objeto de recopilación de dispositivos representa una colección de dispositivos de audio. Debe implementar la <a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdevicecollection"><strong>interfaz IMMDeviceCollection.</strong></a><br /> | 
| Objeto de dispositivo<br /> | Un objeto de dispositivo representa un dispositivo de audio determinado. Proporciona acceso al almacén de propiedades del dispositivo de audio y expone las interfaces de reproducción y captura de audio disponibles en el dispositivo. El objeto de dispositivo debe implementar las <a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdevice"><strong>interfaces IMMDevice</strong></a> <a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immendpoint"><strong>e IMMEndpoint.</strong></a><br /> | 
| Objeto de almacén de propiedades<br /> | Un objeto de almacén de propiedades expone las propiedades asociadas a un dispositivo de audio. Algunas de estas propiedades las usa el sistema, pero las aplicaciones también pueden almacenar propiedades arbitrarias con el punto de conexión de audio.<br /> Todos los dispositivos de audio tienen las tres propiedades siguientes:<br /><ul><li><a href="/windows/desktop/CoreAudio/pkey-deviceinterface-friendlyname"><strong>PKEY_DeviceInterface_FriendlyName</strong></a></li><li><a href="/windows/desktop/CoreAudio/pkey-device-devicedesc"><strong>PKEY_Device_DeviceDesc</strong></a></li><li><a href="/windows/desktop/CoreAudio/pkey-device-friendlyname"><strong>PKEY_Device_FriendlyName</strong></a></li></ul>    El objeto de almacén de propiedades debe implementar la <a href="/windows/win32/api/propsys/nn-propsys-ipropertystore">interfaz IPropertyStore.</a><br /> | 


    

     

2.  El enumerador de extremo personalizado debe implementarse en un archivo DLL que se pueda cargar en el sistema de audio y en otras aplicaciones. El archivo DLL debe estar firmado para que los procesos seguros puedan cargarlo. El archivo DLL debe implementar y exportar la función [**GetTSAudioEndpointEnumeratorForSession,**](gettsaudioendpointenumeratorforsession.md) que actúa como punto de entrada al enumerador de punto de conexión personalizado.

El Servicios de Escritorio remoto llama al [**método QueryProperty**](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-queryproperty) y establece el parámetro *QueryType* en **WTS QUERY \_ \_ AUDIOENUM \_ DLL** para recuperar el nombre del objeto enumerador.

Los objetos de enumerador personalizados usan interfaces de tipo COM y un mecanismo de recuento de referencias de tipo COM, pero no son objetos COM verdaderos. El enumerador de punto de conexión personalizado debe tener la capacidad de trabajar con interfaces de audio heredadas usadas por aplicaciones que no admiten COM. Por esta razón, el enumerador de punto de conexión personalizado no debe basarse en el mecanismo de administración del ciclo de vida de COM. Los consumidores del enumerador de puntos de conexión de audio, como MMDevAPI.dll, cargan el archivo DLL del enumerador de extremo personalizado cuando lo requieran las aplicaciones de usuario y no descargarán el enumerador mientras el enumerador contiene una referencia a un objeto enumerador de dispositivo, un objeto de recopilación de dispositivos, un objeto de dispositivo o un objeto de almacén de propiedades. Sin embargo, no es posible que estos consumidores realicen un seguimiento de las referencias a otros tipos de objetos que pertenecen al enumerador de extremo personalizado. En consecuencia, se recomienda que el enumerador de punto de conexión personalizado no cree ningún objeto que pueda sobrevivir a estos cuatro tipos de objetos.

## <a name="to-implement-a-custom-audio-endpoint"></a>Para implementar un punto de conexión de audio personalizado

Para implementar un enumerador de dispositivo de audio personalizado, debe implementar un punto de conexión de audio personalizado. La manera en que se vinculan los dispositivos de audio personalizados es mediante las dos instrucciones siguientes:

-   `IMMDevice::Activate(IAudioOutputEndpointRT)`
-   `IMMDevice::Activate(IAudioInputEndpointRT)`

No esperamos que implemente la lista completa de interfaces [**IMMDevice::Activate**](/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-immdevice-activate) en el enumerador de dispositivo de audio personalizado. En su lugar, debe implementar [**IAudioOutputEndpointRT**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudiooutputendpointrt) [**e IAudioInputEndpointRT**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioinputendpointrt). Opcionalmente, puede implementar algunos más, como [**IAudioEndpointVolume.**](/windows/desktop/api/endpointvolume/nn-endpointvolume-iaudioendpointvolume) Para cualquier interfaz que no implemente, debe devolver **E \_ NOINTERFACE** (debe usar este código de error específico). Windows a una implementación estándar de la interfaz (por ejemplo, [**IAudioClient2).**](/windows/desktop/api/audioclient/nn-audioclient-iaudioclient2)

Para obtener documentación de referencia adicional sobre cómo implementar y registrar puntos de conexión de audio, vea [**IAudioInputEndpointRT**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioinputendpointrt). Para obtener un diagrama que muestra cómo funciona WASAPI, vea [Componentes de audio en modo de usuario](/windows/desktop/CoreAudio/user-mode-audio-components). Tenga en cuenta que todo el audio en modo de usuario es nuevo a partir Windows Server 2008.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Creación de un Protocolo de escritorio remoto proveedor](creating-a-custom-remote-protocol.md)
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
