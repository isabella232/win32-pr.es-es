---
description: Uso de la interfaz IKsControl para tener acceso a las propiedades de audio
ms.assetid: 72bf9164-96c6-4543-b858-19480b032fdb
title: Uso de la interfaz IKsControl para tener acceso a las propiedades de audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a67639a0e51334da80b7bff88293414a58bb204c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275010"
---
# <a name="using-the-ikscontrol-interface-to-access-audio-properties"></a>Uso de la interfaz IKsControl para tener acceso a las propiedades de audio

En raras ocasiones, es posible que una aplicación de audio especializada tenga que usar la interfaz [**IKsControl**](/windows-hardware/drivers/ddi/ksproxy/nn-ksproxy-ikscontrol) para tener acceso a determinadas funcionalidades de hardware de un adaptador de audio que no están expuestas por la [API DEVICETOPOLOGY](devicetopology-api.md) o la [API MMDevice](mmdevice-api.md). La interfaz **IKsControl** hace que las propiedades, los eventos y los métodos de los dispositivos de streaming de kernel (KS) estén disponibles para las aplicaciones de modo de usuario. El interés principal de las aplicaciones de audio son las propiedades de KS. La interfaz **IKsControl** se puede usar junto con la API DeviceTopology y la API MMDevice para tener acceso a las propiedades KS de los adaptadores de audio.

La interfaz [**IKsControl**](/windows-hardware/drivers/ddi/ksproxy/nn-ksproxy-ikscontrol) está pensada principalmente para su uso por parte de proveedores de hardware que escriben aplicaciones de panel de control para administrar su hardware de audio. **IKsControl** es menos útil para las aplicaciones de audio de uso general que no están vinculadas a dispositivos de hardware concretos. La razón es que los proveedores de hardware suelen implementar mecanismos de propiedad para tener acceso a las propiedades de audio de sus dispositivos. A diferencia de la API de DeviceTopology, que oculta las peculiaridades de los controladores específicos del hardware y proporciona una interfaz relativamente uniforme para el acceso a las propiedades de audio, las aplicaciones usan **IKsControl** para comunicarse directamente con los controladores. Para obtener más información sobre **IKsControl**, consulte la documentación de DDK de Windows.

Como se describe en [topologías de dispositivos](device-topologies.md), una subunidad en la topología de un dispositivo de adaptador podría admitir una o varias interfaces de control específicas de la función que se muestran en la columna izquierda de la tabla siguiente. Cada entrada de la columna derecha de la tabla es la propiedad KS que corresponde a la interfaz de control de la izquierda. La interfaz de control proporciona un acceso cómodo a la propiedad. La mayoría de los controladores de audio usan las propiedades KS para representar las capacidades de procesamiento específicas de la función de las subunidades (también denominadas nodos KS) en las topologías de sus adaptadores de audio. Para obtener más información acerca de las propiedades de KS y los nodos KS, consulte la documentación del DDK de Windows.



| Interfaz de control                                          | Propiedad KS                        |
|------------------------------------------------------------|------------------------------------|
| [**IAudioAutoGainControl**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioautogaincontrol)     | KSPROPERTY \_ audio \_ AGC             |
| [**IAudioBass**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiobass)                           | KSPROPERTY \_ audio \_ Bass            |
| [**IAudioChannelConfig**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiochannelconfig)         | \_configuración de \_ canal de audio de KSPROPERTY \_ |
| [**IAudioInputSelector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioinputselector)         | origen de KSPROPERTY \_ audio \_ MUX \_     |
| [**IAudioLoudness**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioloudness)                   | KSPROPERTY \_ audio \_ sonoridad        |
| [**IAudioMidrange**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiomidrange)                   | KSPROPERTY \_ audio \_ MID             |
| [**IAudioMute**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiomute)                           | \_ \_ Silenciar audio KSPROPERTY            |
| [**IAudioOutputSelector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiooutputselector)       | KSPROPERTY \_ audio \_ Demux \_ dest     |
| [**IAudioPeakMeter**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiopeakmeter)                 | \_PEAKMETER de audio KSPROPERTY \_       |
| [**IAudioTreble**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiotreble)                       | KSPROPERTY \_ audio \_ agudos          |
| [**IAudioVolumeLevel**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiovolumelevel)             | \_VOLUMELEVEL de audio KSPROPERTY \_     |
| [**IDeviceSpecificProperty**](/windows/desktop/api/Devicetopology/nn-devicetopology-idevicespecificproperty) | específico de KSPROPERTY \_ audio \_ dev \_   |



 

Es posible que las topologías de algunos adaptadores de audio contengan subunidades que tengan propiedades KS que no aparezcan en la tabla anterior. Por ejemplo, supongamos que una llamada al método [**IPart:: GetSubType**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getsubtype) para una subunidad determinada recupera el valor de GUID KSNODETYPE el \_ tono. Este GUID de subtipo indica que la subunidad admite una o varias de las siguientes propiedades de KS:

-   KSPROPERTY \_ audio \_ Bass
-   KSPROPERTY \_ audio \_ MID
-   KSPROPERTY \_ audio \_ agudos
-   \_aumento de \_ graves de audio de KSPROPERTY \_

Se puede tener acceso a las tres primeras propiedades de esta lista a través de las interfaces de control que aparecen en la tabla anterior, pero la \_ propiedad KSPROPERTY audio \_ Bass \_ Boost no tiene ninguna interfaz de control correspondiente en la API de DeviceTopology. Sin embargo, una aplicación puede usar la interfaz [**IKsControl**](/windows-hardware/drivers/ddi/ksproxy/nn-ksproxy-ikscontrol) para tener acceso a esta propiedad, si la subunidad admite la propiedad.

Los pasos siguientes son necesarios para tener acceso a \_ la \_ propiedad KSPROPERTY audio Bass \_ Boost de una subunidad de subtipo KSNODETYPE \_ Tone:

1.  Llame al método [**IConnector:: GetDeviceIdConnectedTo**](/windows/desktop/api/Devicetopology/nf-devicetopology-iconnector-getdeviceidconnectedto) o [**IDeviceTopology:: GetDeviceId**](/windows/desktop/api/Devicetopology/nf-devicetopology-idevicetopology-getdeviceid) para obtener la cadena de identificador de dispositivo que identifica el dispositivo de adaptador. Esta cadena es similar a una [cadena de identificador de punto de conexión](endpoint-id-strings.md), con la salvedad de que identifica un dispositivo de adaptador en lugar de un dispositivo de extremo. Para obtener más información acerca de la diferencia entre un dispositivo adaptador y un dispositivo de punto de conexión, consulte [dispositivos de punto de conexión de audio](audio-endpoint-devices.md).
2.  Obtenga la interfaz [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) del dispositivo adaptador llamando al método [**IMMDeviceEnumerator:: GetDevice**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice) con la cadena de identificador de dispositivo. Esta interfaz **IMMDevice** es la misma que la interfaz descrita en la **interfaz IMMDevice**, pero representa un dispositivo adaptador en lugar de un dispositivo de extremo.
3.  Obtenga la interfaz [**IKsControl**](/windows-hardware/drivers/ddi/ksproxy/nn-ksproxy-ikscontrol) en la subunidad llamando al método [**IMMDevice:: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) con el *IID* de parámetro establecido en **REFIID** IID \_ IKsControl. Tenga en cuenta que las interfaces admitidas por este método de **activación** , que es para un dispositivo de adaptador, son diferentes de las interfaces admitidas por el método **Activate** para un dispositivo de extremo. En concreto, el método **Activar** para un dispositivo adaptador es compatible con **IKsControl**.
4.  Llame al método [**IPart:: GetLocalId**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getlocalid) para obtener el identificador local de la subunidad.
5.  Construya una solicitud de propiedad KS. El ID. de nodo KS necesario para la solicitud se encuentra en los 16 bits menos significativos del ID. local obtenido en el paso anterior.
6.  Envíe la solicitud de la propiedad KS al controlador de audio llamando al método [**IKsControl:: KsProperty**](/windows-hardware/drivers/ddi/ksproxy/nf-ksproxy-ikscontrol-ksproperty) . Para obtener más información acerca de este método, consulte la documentación de DDK de Windows.

En el ejemplo de código siguiente se recupera el valor de \_ la \_ propiedad KSPROPERTY audio Bass \_ Boost de una subunidad de subtipo KSNODETYPE \_ Tone:


```C++
//-----------------------------------------------------------
// This function calls the IKsControl::Property method to get
// the value of the KSPROPERTY_AUDIO_BASS_BOOST property of
// a subunit. Parameter pPart should point to a part that is
// a subunit with a subtype GUID value of KSNODETYPE_TONE.
//-----------------------------------------------------------
#define PARTID_MASK 0x0000ffff
#define EXIT_ON_ERROR(hres)  \
              if (FAILED(hres)) { goto Exit; }
#define SAFE_RELEASE(punk)  \
              if ((punk) != NULL)  \
                { (punk)->Release(); (punk) = NULL; }

const IID IID_IKsControl = __uuidof(IKsControl);

HRESULT GetBassBoost(IMMDeviceEnumerator *pEnumerator,
                     IPart *pPart, BOOL *pbValue)
{
    HRESULT hr;
    IDeviceTopology *pTopology = NULL;
    IMMDevice *pPnpDevice = NULL;
    IKsControl *pKsControl = NULL;
    LPWSTR pwszDeviceId = NULL;

    if (pEnumerator == NULL || pPart == NULL || pbValue == NULL)
    {
        return E_INVALIDARG;
    }

    // Get the topology object for the adapter device that contains
    // the subunit represented by the IPart interface.
    hr = pPart->GetTopologyObject(&pTopology);
    EXIT_ON_ERROR(hr)

    // Get the device ID string that identifies the adapter device.
    hr = pTopology->GetDeviceId(&pwszDeviceId);
    EXIT_ON_ERROR(hr)

    // Get the IMMDevice interface of the adapter device object.
    hr = pEnumerator->GetDevice(pwszDeviceId, &pPnpDevice);
    EXIT_ON_ERROR(hr)

    // Activate an IKsControl interface on the adapter device object.
    hr = pPnpDevice->Activate(IID_IKsControl, CLSCTX_ALL, NULL, (void**)&pKsControl);
    EXIT_ON_ERROR(hr)

    // Get the local ID of the subunit (contains the KS node ID).
    UINT localId = 0;
    hr = pPart->GetLocalId(&localId);
    EXIT_ON_ERROR(hr)

    KSNODEPROPERTY_AUDIO_CHANNEL ksprop;
    ZeroMemory(&ksprop, sizeof(ksprop));
    ksprop.NodeProperty.Property.Set = KSPROPSETID_Audio;
    ksprop.NodeProperty.Property.Id = KSPROPERTY_AUDIO_BASS_BOOST;
    ksprop.NodeProperty.Property.Flags = KSPROPERTY_TYPE_GET | KSPROPERTY_TYPE_TOPOLOGY;
    ksprop.NodeProperty.NodeId = localId & PARTID_MASK;
    ksprop.Channel = 0;

    // Send the property request.to the device driver.
    BOOL bValue = FALSE;
    ULONG valueSize;
    hr = pKsControl->KsProperty(
                         &ksprop.NodeProperty.Property, sizeof(ksprop),
                         &bValue, sizeof(bValue), &valueSize);
    EXIT_ON_ERROR(hr)

    *pbValue = bValue;

Exit:
    SAFE_RELEASE(pTopology)
    SAFE_RELEASE(pPnpDevice)
    SAFE_RELEASE(pKsControl)
    CoTaskMemFree(pwszDeviceId);
    return hr;
}

```



En el ejemplo de código anterior, la función GetBassBoost toma los tres parámetros siguientes:

-   `pEnumerator` apunta a la interfaz [**IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) de un enumerador de punto de conexión de audio.
-   `pPart` apunta a la interfaz [**IPart**](/windows/desktop/api/Devicetopology/nn-devicetopology-ipart) de una subunidad que tiene un subtipo de \_ tono KSNODETYPE.
-   `pbValue` apunta a una variable **bool** en la que la función escribe el valor de propiedad.

Un programa llama a GetBassBoost solo después de llamar a [**IPart:: GetSubType**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getsubtype) y determina que el subtipo de la subunidad es el tono de KSNODETYPE \_ . El valor de la propiedad es **true** si se habilita el aumento de graves. Es **false** si se deshabilita el aumento de graves.

Al principio de la función GetBassBoost, la llamada al método [**IPart:: GetTopologyObject**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-gettopologyobject) obtiene la interfaz [**IDeviceTopology**](/windows/desktop/api/Devicetopology/nn-devicetopology-idevicetopology) del dispositivo adaptador que contiene la \_ subunidad de tono KSNODETYPE. La llamada al método [**IDeviceTopology:: GetDeviceId**](/windows/desktop/api/Devicetopology/nf-devicetopology-idevicetopology-getdeviceid) recupera la cadena de identificador de dispositivo que identifica el dispositivo de adaptador. La llamada al método [**IMMDeviceEnumerator:: GetDevice**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice) toma la cadena de identificador de dispositivo como parámetro de entrada y recupera la interfaz [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) del dispositivo adaptador. A continuación, la llamada al método [**IMMDevice:: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) recupera la interfaz [**IKsControl**](/windows-hardware/drivers/ddi/ksproxy/nn-ksproxy-ikscontrol) de la subunidad. Para obtener más información acerca de la interfaz **IKsControl** , consulte la documentación de DDK de Windows.

A continuación, en el ejemplo de código anterior se crea una estructura de [**\_ \_ canal de audio KSNODEPROPERTY**](/windows-hardware/drivers/ddi/ksmedia/ns-ksmedia-ksnodeproperty_audio_channel) que describe la propiedad graves-Boost. En el ejemplo de código se pasa un puntero a la estructura al método [**IKsControl:: KsProperty**](/windows-hardware/drivers/ddi/ksproxy/nf-ksproxy-ikscontrol-ksproperty) , que usa la información de la estructura para recuperar el valor de propiedad. Para obtener más información sobre la estructura de **\_ \_ canal de audio KSNODEPROPERTY** y el método **IKsControl:: KsProperty** , consulte la documentación de DDK de Windows.

Normalmente, el hardware de audio asigna un estado de graves-Boost independiente a cada canal de una secuencia de audio. En principio, el aumento de graves se puede habilitar para algunos canales y deshabilitarse para otros. La estructura de [**\_ \_ canal de audio KSNODEPROPERTY**](/windows-hardware/drivers/ddi/ksmedia/ns-ksmedia-ksnodeproperty_audio_channel) contiene un miembro de **canal** que especifica el número de canal. Si una secuencia contiene *N* canales, los canales se numeran de 0 a *N*-1. En el ejemplo de código anterior se obtiene el valor de la propiedad Bass-Boost solo para el canal 0. Esta implementación presupone implícitamente que las propiedades de graves-Boost para todos los canales se establecen de forma uniforme en el mismo estado. Por lo tanto, la lectura de la propiedad graves-Boost para el canal 0 es suficiente para determinar el valor de la propiedad graves-Boost para la secuencia. Para ser coherente con esta suposición, una función correspondiente para establecer la propiedad de graves-Boost establecería todos los canales en el mismo valor de la propiedad Bass-Boost. Se trata de convenciones razonables, pero no todos los proveedores de hardware las siguen necesariamente. Por ejemplo, un proveedor puede proporcionar una aplicación del panel de control que habilita el aumento de graves solo para los canales que impulsan a los hablantes de intervalos completos. (Un altavoz completo puede reproducir sonidos en todo el intervalo, desde graves hasta agudos). En ese caso, el valor de propiedad recuperado por el ejemplo de código anterior podría no representar con precisión el estado de graves-Boost de la secuencia.

Los clientes que usan las interfaces de control enumeradas en la tabla anterior pueden llamar al método [**IPart:: RegisterControlChangeCallback**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-registercontrolchangecallback) para registrarse para recibir notificaciones cuando cambia el valor de un parámetro de control. Tenga en cuenta que la interfaz [**IKsControl**](/windows-hardware/drivers/ddi/ksproxy/nn-ksproxy-ikscontrol) no proporciona un medio similar para que los clientes se registren para las notificaciones cuando cambia el valor de una propiedad. Si **IKsControl** admitía notificaciones de cambio de propiedad, podría informar a una aplicación cuando otra aplicación cambiara un valor de propiedad. Sin embargo, a diferencia de los controles que se usan con más frecuencia y que se supervisan a través de notificaciones de [**IPart**](/windows/desktop/api/Devicetopology/nn-devicetopology-ipart) , las propiedades administradas por **IKsControl** están pensadas principalmente para su uso por parte de los proveedores de hardware, y es probable que estas propiedades solo las cambien las aplicaciones del panel de control escritas por los proveedores. Si una aplicación debe detectar los cambios de propiedades realizados por otra aplicación, puede detectar los cambios sondeando periódicamente el valor de la propiedad a través de **IKsControl**.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Guía de programación](programming-guide.md)
</dt> </dl>

 

 
