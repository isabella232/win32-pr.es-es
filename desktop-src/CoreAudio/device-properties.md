---
description: Propiedades de dispositivos
ms.assetid: ad8753ba-ad20-4122-b0f2-eb165f98db67
title: Propiedades del dispositivo (API de audio básicas)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47e1a5068329ea2da794b68b777aa989a2e8b4a665df082982916942aa15b56e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118407023"
---
# <a name="device-properties-core-audio-apis"></a>Propiedades del dispositivo (API de audio básicas)

Durante el proceso de enumeración de dispositivos de punto de conexión de [audio,](audio-endpoint-devices.md)una aplicación cliente puede interrogar a los objetos de punto de conexión para sus propiedades de dispositivo. Las propiedades del dispositivo se exponen en la implementación de MMDevice API de la **interfaz IPropertyStore.** Dada una referencia a la [**interfaz IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) de un objeto de punto de conexión, un cliente puede obtener una referencia al almacén de propiedades del objeto de punto de conexión llamando al método [**IMMDevice::OpenPropertyStore.**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-openpropertystore)

El objeto de almacén de propiedades expone una **interfaz IPropertyStore.** Los dos métodos principales de esta interfaz son **IPropertyStore::GetValue**, que obtiene un valor de propiedad de dispositivo, y **IPropertyStore::SetValue**, que establece un valor de propiedad de dispositivo. Para más información sobre **IPropertyStore,** consulte la documentación Windows SDK.

La implementación de MMDevice API del almacén de propiedades es diferente del objeto de almacén de propiedades de shell estándar. Para cambiar un valor de propiedad, la aplicación cliente debe llamar al **método IPropertyStore::SetValue.** Durante esta llamada, los nuevos valores se establecen y escriben en el Registro. Por lo tanto, la aplicación no necesita llamar al método **IPropertyStore::Commit** después de la **llamada a SetValue.** El identificador del registro solo se cierra cuando el cliente libera el puntero de interfaz.

Normalmente, las aplicaciones cliente de terceros llaman al **método GetValue,** pero no **al método SetValue.** El administrador de puntos de conexión establece las propiedades básicas del dispositivo para los puntos de conexión. El administrador de puntos de conexión es el Windows vista que es responsable de detectar la presencia de dispositivos de punto de conexión de audio.

Cada identificador de propiedad PKEY Xxx de la lista siguiente es una constante de tipo PROPERTYKEY que se define en el archivo de encabezado \_ Functiondiscoverykeys  \_ devpkey.h. Todos los dispositivos de punto de conexión de audio tienen estas tres propiedades de dispositivo.



| Propiedad                                                                         | Descripción                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PKEY \_ DeviceInterface \_ FriendlyName**](pkey-deviceinterface-friendlyname.md) | Nombre descriptivo del adaptador de audio al que está conectado el dispositivo de punto de conexión (por ejemplo, "Adaptador de audio XYZ"). **PropVARIANT** member **vt** se establece en VT LPWSTR y el miembro \_ **pwszVal** apunta a una cadena de caracteres anchos terminada en NULL que contiene el nombre descriptivo. |
| [**Dispositivo \_ \_ PKEYDesc**](pkey-device-devicedesc.md)                       | La descripción del dispositivo del punto de conexión (por ejemplo, "Altavoces"). **PropVARIANT** member **vt** se establece en VT LPWSTR y el miembro \_ **pwszVal** apunta a una cadena de caracteres anchos terminada en NULL que contiene la descripción del dispositivo.                                       |
| [**PKEY \_ Device \_ FriendlyName**](pkey-device-friendlyname.md)                   | Nombre descriptivo del dispositivo del punto de conexión (por ejemplo, "Altavoces (adaptador de audio XYZ)"). **PropVARIANT** member **vt** se establece en VT LPWSTR y el miembro \_ **pwszVal** apunta a una cadena de caracteres anchos terminada en NULL que contiene el nombre descriptivo.                             |



 

Algunos dispositivos de punto de conexión de audio pueden tener propiedades adicionales que no aparecen en la lista anterior. Para obtener más información sobre las propiedades adicionales, vea [Propiedades de punto de conexión de audio.](audio-endpoint-properties.md) Para más información sobre **PROPERTYKEY,** consulte la documentación Windows SDK.

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



La macro FAILED del ejemplo de código anterior se define en el archivo de encabezado Winerror.h.

En el ejemplo de código anterior, el cuerpo del bucle **for** de la función PrintEndpointNames llama al método [**IMMDevice::GetId**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-getid) para obtener la cadena de identificador de punto de conexión para el dispositivo de punto de conexión de audio representado por la instancia de interfaz **IMMDevice.** [](endpoint-id-strings.md) La cadena identifica de forma única el dispositivo con respecto a todos los demás dispositivos de punto de conexión de audio del sistema. Un cliente puede usar la cadena de identificador de punto de conexión para crear una instancia del dispositivo de punto de conexión de audio más adelante o en un proceso diferente mediante una llamada al método [**IMMDeviceEnumerator::GetDevice.**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice) Los clientes deben tratar el contenido de la cadena de identificador de punto de conexión como opaco. Es decir, los clientes no deben intentar analizar el contenido de la cadena para obtener información sobre el dispositivo. El motivo es que el formato de cadena no está definido y podría cambiar de una implementación de MMDevice API a la siguiente.

Los nombres de dispositivo descriptivos y las cadenas de identificador de punto de conexión que obtiene la función PrintEndpointNames en el ejemplo de código anterior son idénticos a los nombres de dispositivo descriptivos y las cadenas de identificador de punto de conexión que proporciona Direct Sound durante la enumeración del dispositivo. Para obtener más información, vea [Eventos de audio para aplicaciones de audio heredadas.](audio-events-for-legacy-audio-applications.md)

En el ejemplo de código anterior, la función PrintEndpointNames llama a la función **CoCreateInstance** para crear un enumerador para los dispositivos de punto de conexión de audio del sistema. A menos que el programa de llamada llamara previamente a las funciones **CoInitialize** o **CoInitializeEx** para inicializar la biblioteca COM, se producirá un error en la llamada **a CoCreateInstance.** Para obtener más información sobre **CoCreateInstance,** **CoInitialize** y **CoInitializeEx,** consulte la documentación del SDK Windows.

Para obtener más información sobre las interfaces **IMMDeviceEnumerator,** **IMMDeviceCollection** e **IMMDevice,** vea [MMDevice API](mmdevice-api.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Dispositivos de punto de conexión de audio](audio-endpoint-devices.md)
</dt> </dl>

 

 



