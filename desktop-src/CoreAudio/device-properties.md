---
description: Propiedades de dispositivos
ms.assetid: ad8753ba-ad20-4122-b0f2-eb165f98db67
title: Propiedades de dispositivo (API de audio Core)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14a868e4bb806bd49d934febed164bcd70fba39f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659312"
---
# <a name="device-properties-core-audio-apis"></a>Propiedades de dispositivo (API de audio Core)

Durante el proceso de enumeración de los [dispositivos de punto de conexión de audio](audio-endpoint-devices.md), una aplicación cliente puede consultar los objetos de punto de conexión para sus propiedades de dispositivo. Las propiedades del dispositivo se exponen en la implementación de la API de MMDevice de la interfaz **IPropertyStore** . Dada una referencia a la interfaz [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) de un objeto de punto de conexión, un cliente puede obtener una referencia al almacén de propiedades del objeto de extremo llamando al método [**IMMDevice:: OpenPropertyStore**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-openpropertystore) .

El objeto de almacén de propiedades expone una interfaz **IPropertyStore** . Los dos métodos principales de esta interfaz son **IPropertyStore:: GetValue**, que obtiene un valor de propiedad de dispositivo y **IPropertyStore:: SetValue**, que establece un valor de propiedad de dispositivo. Para obtener más información sobre **IPropertyStore**, consulte la documentación de Windows SDK.

La implementación de la API de MMDevice del almacén de propiedades es diferente del objeto de almacén de propiedades de Shell estándar. Para cambiar un valor de propiedad, la aplicación cliente debe llamar al método **IPropertyStore:: SetValue** . Durante esta llamada, los nuevos valores se establecen y se escriben en el registro. Por lo tanto, la aplicación no necesita llamar al método **IPropertyStore:: commit** después de la llamada a **SetValue** . El identificador del registro solo se cierra cuando el cliente libera el puntero de interfaz.

Normalmente, las aplicaciones cliente de terceros llaman al método **GetValue** , pero no al método **SetValue** . El administrador de puntos de conexión establece las propiedades básicas del dispositivo para los puntos de conexión. Endpoint Manager es el componente de Windows Vista responsable de detectar la presencia de dispositivos de punto de conexión de audio.

Cada \_ identificador de propiedad PKEY XXX de la lista siguiente es una constante de tipo **PROPERTYKEY** que se define en el archivo de encabezado Functiondiscoverykeys \_ devpkey. h. Todos los dispositivos de punto de conexión de audio tienen estas tres propiedades de dispositivo.



| Propiedad                                                                         | Descripción                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PKEY \_ DeviceInterface \_ FriendlyName**](pkey-deviceinterface-friendlyname.md) | El nombre descriptivo del adaptador de audio al que está conectado el dispositivo de extremo (por ejemplo, "adaptador de audio XYZ"). El miembro **VT** de **PROPVARIANT** se establece en VT \_ LPWStr y el miembro **pwszVal** apunta a una cadena de caracteres anchos terminada en null que contiene el nombre descriptivo. |
| [**\_DeviceDesc de dispositivo PKEY \_**](pkey-device-devicedesc.md)                       | La descripción del dispositivo de extremo (por ejemplo, "altavoces"). El miembro **VT** de **PROPVARIANT** se establece en VT \_ LPWStr y el miembro **pwszVal** apunta a una cadena de caracteres anchos terminada en null que contiene la descripción del dispositivo.                                       |
| [**PKEY el \_ dispositivo \_ FriendlyName**](pkey-device-friendlyname.md)                   | El nombre descriptivo del dispositivo de extremo (por ejemplo, "altavoces (adaptador de audio XYZ)"). El miembro **VT** de **PROPVARIANT** se establece en VT \_ LPWStr y el miembro **pwszVal** apunta a una cadena de caracteres anchos terminada en null que contiene el nombre descriptivo.                             |



 

Algunos dispositivos de punto de conexión de audio pueden tener propiedades adicionales que no aparecen en la lista anterior. Para obtener más información acerca de las propiedades adicionales, consulte [propiedades de punto de conexión de audio](audio-endpoint-properties.md). Para obtener más información acerca de **PROPERTYKEY**, consulte la documentación de Windows SDK.

En el ejemplo de código siguiente se imprimen los nombres para mostrar de todos los dispositivos de punto de conexión de representación de audio en el sistema:


```C++
//-----------------------------------------------------------
// This function enumerates all active (plugged in) audio
// rendering endpoint devices. It prints the friendly name
// and endpoint ID string of each endpoint device.
//-----------------------------------------------------------
#define EXIT_ON_ERROR(hres)  \
              if (FAILED(hres)) { goto Exit; }
#define SAFE_RELEASE(punk)  \
              if ((punk) != NULL)  \
                { (punk)->Release(); (punk) = NULL; }

const CLSID CLSID_MMDeviceEnumerator = __uuidof(MMDeviceEnumerator);
const IID IID_IMMDeviceEnumerator = __uuidof(IMMDeviceEnumerator);

void PrintEndpointNames()
{
    HRESULT hr = S_OK;
    IMMDeviceEnumerator *pEnumerator = NULL;
    IMMDeviceCollection *pCollection = NULL;
    IMMDevice *pEndpoint = NULL;
    IPropertyStore *pProps = NULL;
    LPWSTR pwszID = NULL;

    hr = CoCreateInstance(
           CLSID_MMDeviceEnumerator, NULL,
           CLSCTX_ALL, IID_IMMDeviceEnumerator,
           (void**)&pEnumerator);
    EXIT_ON_ERROR(hr)

    hr = pEnumerator->EnumAudioEndpoints(
                        eRender, DEVICE_STATE_ACTIVE,
                        &pCollection);
    EXIT_ON_ERROR(hr)

    UINT  count;
    hr = pCollection->GetCount(&count);
    EXIT_ON_ERROR(hr)

    if (count == 0)
    {
        printf("No endpoints found.\n");
    }

    // Each loop prints the name of an endpoint device.
    for (ULONG i = 0; i < count; i++)
    {
        // Get pointer to endpoint number i.
        hr = pCollection->Item(i, &pEndpoint);
        EXIT_ON_ERROR(hr)

        // Get the endpoint ID string.
        hr = pEndpoint->GetId(&pwszID);
        EXIT_ON_ERROR(hr)
        
        hr = pEndpoint->OpenPropertyStore(
                          STGM_READ, &pProps);
        EXIT_ON_ERROR(hr)

        PROPVARIANT varName;
        // Initialize container for property value.
        PropVariantInit(&varName);

        // Get the endpoint's friendly-name property.
        hr = pProps->GetValue(
                       PKEY_Device_FriendlyName, &varName);
        EXIT_ON_ERROR(hr)

        // Print endpoint friendly name and endpoint ID.
        printf("Endpoint %d: \"%S\" (%S)\n",
               i, varName.pwszVal, pwszID);

        CoTaskMemFree(pwszID);
        pwszID = NULL;
        PropVariantClear(&varName);
        SAFE_RELEASE(pProps)
        SAFE_RELEASE(pEndpoint)
    }
    SAFE_RELEASE(pEnumerator)
    SAFE_RELEASE(pCollection)
    return;

Exit:
    printf("Error!\n");
    CoTaskMemFree(pwszID);
    SAFE_RELEASE(pEnumerator)
    SAFE_RELEASE(pCollection)
    SAFE_RELEASE(pEndpoint)
    SAFE_RELEASE(pProps)
}
```



La macro FAILed en el ejemplo de código anterior se define en el archivo de encabezado Winerror. h.

En el ejemplo de código anterior, el cuerpo del bucle **for** de la función PrintEndpointNames llama al método [**IMMDevice:: getId**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-getid) para obtener la [cadena de identificador de punto de conexión](endpoint-id-strings.md) para el dispositivo de punto de conexión de audio representado por la instancia de la interfaz **IMMDevice** . La cadena identifica de forma única el dispositivo con respecto a todos los demás dispositivos de punto de conexión de audio del sistema. Un cliente puede usar la cadena de identificador de punto de conexión para crear una instancia del dispositivo de punto de conexión de audio más adelante o en un proceso diferente llamando al método [**IMMDeviceEnumerator:: GetDevice**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice) . Los clientes deben tratar el contenido de la cadena de ID. de punto de conexión como opaco. Es decir, los clientes no deben intentar analizar el contenido de la cadena para obtener información sobre el dispositivo. La razón es que el formato de la cadena no está definido y puede cambiar de una implementación de la API de MMDevice al siguiente.

Los nombres descriptivos de los dispositivos y las cadenas de ID. de punto de conexión obtenidos por la función PrintEndpointNames en el ejemplo de código anterior son idénticos a los nombres descriptivos de los dispositivos y las cadenas de identificador de punto de conexión que proporciona DirectSound durante la enumeración de dispositivos. Para obtener más información, consulte [eventos de audio para aplicaciones de audio heredadas](audio-events-for-legacy-audio-applications.md).

En el ejemplo de código anterior, la función PrintEndpointNames llama a la función **CoCreateInstance** para crear un enumerador para los dispositivos de punto de conexión de audio en el sistema. A menos que el programa de llamada previamente haya llamado a la función **CoInitialize** o **CoInitializeEx** para inicializar la biblioteca com, se producirá un error en la llamada a **CoCreateInstance** . Para obtener más información sobre **CoCreateInstance**, **CoInitialize** y **CoInitializeEx**, vea la documentación de Windows SDK.

Para obtener más información sobre las interfaces **IMMDeviceEnumerator**, **IMMDeviceCollection** y **IMMDevice** , vea [API de MMDevice](mmdevice-api.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Dispositivos de punto de conexión de audio](audio-endpoint-devices.md)
</dt> </dl>

 

 



