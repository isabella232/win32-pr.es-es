---
description: Uso de la interfaz IKsControl para acceder a las propiedades de audio
ms.assetid: 72bf9164-96c6-4543-b858-19480b032fdb
title: Uso de la interfaz IKsControl para acceder a las propiedades de audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b763b874730981907d61ed7d4d2f46f4a9b053705b2747064c2505b9c5e90b14
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088234"
---
# <a name="using-the-ikscontrol-interface-to-access-audio-properties"></a>Uso de la interfaz IKsControl para acceder a las propiedades de audio

En raras ocasiones, es posible que una aplicación de audio especializada necesite usar la interfaz [**IKsControl**](/windows-hardware/drivers/ddi/ksproxy/nn-ksproxy-ikscontrol) para acceder a determinadas funcionalidades de hardware de un adaptador de audio que no están expuestas por [deviceTopology API](devicetopology-api.md) o [MMDevice API.](mmdevice-api.md) La **interfaz IKsControl** hace que las propiedades, los eventos y los métodos de los dispositivos de streaming de kernel (KS) estén disponibles para las aplicaciones en modo de usuario. El interés principal de las aplicaciones de audio son las propiedades KS. La **interfaz IKsControl** se puede usar junto con DeviceTopology API y MMDevice API para acceder a las propiedades KS de los adaptadores de audio.

La [**interfaz IKsControl**](/windows-hardware/drivers/ddi/ksproxy/nn-ksproxy-ikscontrol) está diseñada principalmente para su uso por proveedores de hardware que escriben aplicaciones de panel de control para administrar su hardware de audio. **IKsControl es** menos útil para aplicaciones de audio de uso general que no están asociadas a dispositivos de hardware concretos. El motivo es que los proveedores de hardware suelen implementar mecanismos propietarios para acceder a las propiedades de audio de sus dispositivos. A diferencia de DeviceTopology API, que oculta las características específicas del controlador de hardware y proporciona una interfaz relativamente uniforme para acceder a las propiedades de audio, las aplicaciones usan **IKsControl** para comunicarse directamente con los controladores. Para obtener más información **sobre IKsControl,** consulte la documentación Windows DDK.

Como se describe en Topologías de [dispositivo,](device-topologies.md)una subunidad de la topología de un dispositivo adaptador podría admitir una o varias de las interfaces de control específicas de la función que se muestran en la columna izquierda de la tabla siguiente. Cada entrada de la columna derecha de la tabla es la propiedad KS que corresponde a la interfaz de control de la izquierda. La interfaz de control proporciona un acceso cómodo a la propiedad . La mayoría de los controladores de audio usan propiedades KS para representar las funcionalidades de procesamiento específicas de la función de las subunidades (también denominadas nodos KS) en las topologías de sus adaptadores de audio. Para más información sobre las propiedades de KS y los nodos KS, consulte la documentación Windows DDK.



| Interfaz de control                                          | KS, propiedad                        |
|------------------------------------------------------------|------------------------------------|
| [**IAudioAutoGainControl**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioautogaincontrol)     | KSPROPERTY \_ AUDIO \_ AGC             |
| [**IAudioBass**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiobass)                           | KSPROPERTY \_ AUDIO \_ KCS            |
| [**IAudioChannelConfig**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiochannelconfig)         | CONFIGURACIÓN DEL CANAL DE AUDIO KSPROPERTY \_ \_ \_ |
| [**IAudioInputSelector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioinputselector)         | KSPROPERTY \_ AUDIO \_ MUX \_ SOURCE     |
| [**IAudioLoudness**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioloudness)                   | \_SONORIDAD DE AUDIO KSPROPERTY \_        |
| [**IAudioMidrange**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiomidrange)                   | KSPROPERTY \_ AUDIO \_ MID             |
| [**IAudioMute**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiomute)                           | KSPROPERTY \_ AUDIO \_ MUTE            |
| [**IAudioOutputSelector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiooutputselector)       | KSPROPERTY \_ AUDIO \_ DEMUX \_ DEST     |
| [**IAudioPeakMeter**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiopeakmeter)                 | KSPROPERTY \_ AUDIO \_ PEAKMETER       |
| [**IAudioTreble**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiotreble)                       | KSPROPERTY \_ AUDIO \_ TREBLE          |
| [**IAudioVolumeLevel**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiovolumelevel)             | KSPROPERTY \_ AUDIO \_ VOLUMELEVEL     |
| [**IDeviceSpecificProperty**](/windows/desktop/api/Devicetopology/nn-devicetopology-idevicespecificproperty) | KSPROPERTY \_ AUDIO \_ DEV \_ SPECIFIC   |



 

Las topologías de algunos adaptadores de audio pueden contener subunidades que tienen propiedades KS que no aparecen en la tabla anterior. Por ejemplo, suponga que una llamada al método [**IPart::GetSubType**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getsubtype) para una subunidad determinada recupera el valor GUID KSNODETYPE \_ TONE. Este GUID de subtipo indica que la subunidad admite una o varias de las siguientes propiedades de KS:

-   KSPROPERTY \_ AUDIO \_ KCS
-   KSPROPERTY \_ AUDIO \_ MID
-   KSPROPERTY \_ AUDIO \_ TREBLE
-   KSPROPERTY \_ AUDIO \_ BASS \_ BOOST

Se puede acceder a las tres primeras propiedades de esta lista a través de las interfaces de control que aparecen en la tabla anterior, pero la propiedad KSPROPERTY AUDIO BOOST DE AUDIO BOOST no tiene ninguna interfaz de control correspondiente en \_ \_ \_ DeviceTopology API. Sin embargo, una aplicación puede usar la [**interfaz IKsControl**](/windows-hardware/drivers/ddi/ksproxy/nn-ksproxy-ikscontrol) para acceder a esta propiedad, si la subunidad admite la propiedad .

Los pasos siguientes son necesarios para acceder a la propiedad KSPROPERTY \_ AUDIO BOOST de una subunidad de \_ \_ subtipo KSNODETYPE \_ TONE:

1.  Llame al [**método IConnector::GetDeviceIdConnectedTo**](/windows/desktop/api/Devicetopology/nf-devicetopology-iconnector-getdeviceidconnectedto) o [**IDeviceTopology::GetDeviceId**](/windows/desktop/api/Devicetopology/nf-devicetopology-idevicetopology-getdeviceid) para obtener la cadena de identificador de dispositivo que identifica el dispositivo del adaptador. Esta cadena es similar a una cadena [de identificador de](endpoint-id-strings.md)punto de conexión, salvo que identifica un dispositivo adaptador en lugar de un dispositivo de punto de conexión. Para obtener más información sobre la diferencia entre un dispositivo de adaptador y un dispositivo de punto de conexión, vea Dispositivos de [punto de conexión de audio.](audio-endpoint-devices.md)
2.  Obtenga la [**interfaz IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) del dispositivo adaptador mediante una llamada al método [**IMMDeviceEnumerator::GetDevice**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice) con la cadena de identificador de dispositivo. Esta **interfaz IMMDevice** es la misma que la interfaz descrita en **IMMDevice Interface**, pero representa un dispositivo adaptador en lugar de un dispositivo de punto de conexión.
3.  Obtenga la [**interfaz IKsControl**](/windows-hardware/drivers/ddi/ksproxy/nn-ksproxy-ikscontrol) en la subunidad llamando al método [**IMMDevice::Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) con el parámetro *iid* establecido en IKsControl de **REFIID.** \_ Tenga en cuenta que las interfaces admitidas por este **método Activate,** que es para un dispositivo adaptador, son diferentes de las interfaces admitidas por el método **Activate** para un dispositivo de punto de conexión. En concreto, el **método Activate** para un dispositivo de adaptador admite **IKsControl**.
4.  Llame al [**método IPart::GetLocalId**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getlocalid) para obtener el identificador local de la subunidad.
5.  Construya una solicitud de propiedad KS. El identificador de nodo KS necesario para la solicitud se encuentra en los 16 bits menos significativos del identificador local obtenido en el paso anterior.
6.  Envíe la solicitud de propiedad KS al controlador de audio mediante una llamada [**al método IKsControl::KsProperty.**](/windows-hardware/drivers/ddi/ksproxy/nf-ksproxy-ikscontrol-ksproperty) Para más información sobre este método, consulte la documentación Windows DDK.

En el ejemplo de código siguiente se recupera el valor de la propiedad KSPROPERTY AUDIO QR BOOST de una \_ \_ subunidad de \_ subtipo KSNODETYPE \_ TONE:


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

-   `pEnumerator` apunta a la [**interfaz IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) de un enumerador de punto de conexión de audio.
-   `pPart` apunta a la [**interfaz IPart**](/windows/desktop/api/Devicetopology/nn-devicetopology-ipart) de una subunidad que tiene un subtipo de KSNODETYPE \_ TONE.
-   `pbValue` apunta a una variable **BOOL** en la que la función escribe el valor de propiedad.

Un programa llama a GetBassBoost solo después de llamar a [**IPart::GetSubType**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getsubtype) y determina que el subtipo de la subunidad es KSNODETYPE \_ TONE. El valor de la propiedad **es TRUE** si está habilitado boost. Es **FALSE si está** deshabilitada la potenciación de los impulsos.

Al principio de la función GetBassBoost, la llamada al método [**IPart::GetTopologyObject**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-gettopologyobject) obtiene la interfaz [**IDeviceTopology**](/windows/desktop/api/Devicetopology/nn-devicetopology-idevicetopology) del dispositivo adaptador que contiene la subunidad KSNODETYPE \_ TONE. La [**llamada al método IDeviceTopology::GetDeviceId**](/windows/desktop/api/Devicetopology/nf-devicetopology-idevicetopology-getdeviceid) recupera la cadena de identificador de dispositivo que identifica el dispositivo adaptador. La llamada al método [**IMMDeviceEnumerator::GetDevice**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice) toma la cadena de identificador de dispositivo como parámetro de entrada y recupera la [**interfaz IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) del dispositivo adaptador. A continuación, la llamada al método [**IMMDevice::Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) recupera la [**interfaz IKsControl**](/windows-hardware/drivers/ddi/ksproxy/nn-ksproxy-ikscontrol) de la subunidad. Para más información sobre la **interfaz IKsControl,** consulte la documentación Windows DDK.

A continuación, el ejemplo de código anterior crea una [**estructura KSNODEPROPERTY \_ AUDIO \_ CHANNEL**](/windows-hardware/drivers/ddi/ksmedia/ns-ksmedia-ksnodeproperty_audio_channel) que describe la propiedad boost. En el ejemplo de código se pasa un puntero a la estructura al método [**IKsControl::KsProperty,**](/windows-hardware/drivers/ddi/ksproxy/nf-ksproxy-ikscontrol-ksproperty) que usa la información de la estructura para recuperar el valor de propiedad. Para obtener más información sobre la estructura **KSNODEPROPERTY \_ AUDIO \_ CHANNEL** y el método **IKsControl::KsProperty,** consulte la documentación Windows DDK.

Normalmente, el hardware de audio asigna un estado de potenciación de sonido independiente a cada canal de una secuencia de audio. En principio, se puede habilitar el aumento de frecuencias para algunos canales y deshabilitarse para otros. La [**estructura KSNODEPROPERTY \_ AUDIO \_ CHANNEL**](/windows-hardware/drivers/ddi/ksmedia/ns-ksmedia-ksnodeproperty_audio_channel) contiene un **miembro Channel** que especifica el número de canal. Si una secuencia contiene *N* canales, los canales se numeran de 0 a *N—* 1. En el ejemplo de código anterior se obtiene el valor de la propiedad boost para el canal 0 únicamente. Esta implementación supone implícitamente que las propiedades de aumento de frecuencia para todos los canales se establecen uniformemente en el mismo estado. Por lo tanto, la lectura de la propiedad boost para el canal 0 es suficiente para determinar el valor de la propiedad boost para la secuencia. Para ser coherentes con esta suposición, una función correspondiente para establecer la propiedad de aumento de velocidad establecería todos los canales en el mismo valor de propiedad de aumento de precio. Se trata de convenciones razonables, pero no todos los proveedores de hardware las siguen necesariamente. Por ejemplo, un proveedor podría proporcionar una aplicación de panel de control que permita la potenciación de las baterías solo para los canales que impulsan altavoces de gama completa. (Un altavoz de gama completa es capaz de reproducir sonidos en todo el intervalo, desde sonidos hasta triples). En ese caso, es posible que el valor de propiedad recuperado por el ejemplo de código anterior no represente con precisión el estado de potenciación de la secuencia.

Los clientes que usan las interfaces de control enumeradas en la tabla anterior pueden llamar al método [**IPart::RegisterControlChangeCallback**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-registercontrolchangecallback) para registrarse para recibir notificaciones cuando cambia el valor de un parámetro de control. Tenga en cuenta [**que la interfaz IKsControl**](/windows-hardware/drivers/ddi/ksproxy/nn-ksproxy-ikscontrol) no proporciona un medio similar para que los clientes se registren para recibir notificaciones cuando cambia un valor de propiedad. Si **IKsControl admite** notificaciones de cambio de propiedad, podría informar a una aplicación cuando otra aplicación cambió un valor de propiedad. Sin embargo, a diferencia de los controles más usados que se supervisan a través de notificaciones [**IPart,**](/windows/desktop/api/Devicetopology/nn-devicetopology-ipart) las propiedades administradas por **IKsControl** están diseñadas principalmente para que las usen los proveedores de hardware y es probable que solo las aplicaciones del panel de control escritas por los proveedores cambien esas propiedades. Si una aplicación debe detectar los cambios de propiedad realizados por otra aplicación, puede detectar los cambios sondeando periódicamente el valor de propiedad a través **de IKsControl**.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Guía de programación](programming-guide.md)
</dt> </dl>

 

 
