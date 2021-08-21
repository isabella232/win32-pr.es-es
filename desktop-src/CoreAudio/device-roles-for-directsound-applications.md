---
description: Roles de dispositivo para aplicaciones DirectSound
ms.assetid: 7d82d67f-aad8-4e5b-ac65-87d75774e613
title: Roles de dispositivo para aplicaciones DirectSound
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3037b767d7ddfb96d892c789608f23523efed465535258c336496f3f23d82f19
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957334"
---
# <a name="device-roles-for-directsound-applications"></a>Roles de dispositivo para aplicaciones DirectSound

> [!Note]  
> MMDevice [API admite roles](mmdevice-api.md) de dispositivo. Sin embargo, la interfaz de usuario Windows Vista no implementa compatibilidad con esta característica. La compatibilidad de la interfaz de usuario con los roles de dispositivo podría implementarse en una versión futura de Windows. Para obtener más información, vea [Roles de dispositivo en Windows Vista](device-roles-in-windows-vista.md).

 

DirectSound API no proporciona un medio para que una aplicación seleccione el dispositivo de punto de conexión de [audio](audio-endpoint-devices.md) que el usuario ha asignado a un rol de [dispositivo determinado.](device-roles.md) Sin embargo, Windows Vista, las API de audio principales se pueden usar junto con una aplicación DirectSound para habilitar la selección de dispositivos en función del rol del dispositivo. Con la ayuda de las API de audio principales, la aplicación puede identificar el dispositivo de punto de conexión de audio asignado a un rol determinado, obtener el GUID del dispositivo DirectSound para el dispositivo de punto de conexión y llamar a la función **DirectSoundCreate** o **DirectSoundCaptureCreate** para crear una instancia de interfaz **IDirectSound** o **IDirectSoundCapture** que encapsula el dispositivo del punto de conexión. Para obtener más información sobre DirectSound, consulte la documentación Windows SDK.

En el ejemplo de código siguiente se muestra cómo obtener el GUID del dispositivo DirectSound para el dispositivo de representación o captura que está asignado actualmente a un rol de dispositivo determinado:


```C++
//-----------------------------------------------------------
// Get the DirectSound or DirectSoundCapture device GUID for
// an audio endpoint device. If flow = eRender, the function
// gets the DirectSound device GUID for the rendering device
// with the specified device role. If flow = eCapture, the
// function gets the DirectSoundCapture device GUID for the
// capture device with the specified device role.
//-----------------------------------------------------------
#define EXIT_ON_ERROR(hr)  \
              if (FAILED(hr)) { goto Exit; }
#define SAFE_RELEASE(punk)  \
              if ((punk) != NULL)  \
                { (punk)->Release(); (punk) = NULL; }

HRESULT GetDirectSoundGuid(EDataFlow flow, ERole role, GUID* pDevGuid)
{
    HRESULT hr = S_OK;
    IMMDeviceEnumerator *pEnumerator = NULL;
    IMMDevice *pDevice = NULL;
    IPropertyStore *pProps = NULL;

    PROPVARIANT var;
    PropVariantInit(&var);

    if (pDevGuid == NULL)
    {
        return E_POINTER;
    }

    // Get a device enumerator for the audio endpoint
    // devices in the system.
    hr = CoCreateInstance(__uuidof(MMDeviceEnumerator),
                          NULL, CLSCTX_INPROC_SERVER,
                          __uuidof(IMMDeviceEnumerator),
                          (void**)&pEnumerator);
    EXIT_ON_ERROR(hr)

    // Get the endpoint device with the specified dataflow
    // direction (eRender or eCapture) and device role.
    hr = pEnumerator->GetDefaultAudioEndpoint(flow, role,
                                              &pDevice);
    EXIT_ON_ERROR(hr)

    hr = pDevice->OpenPropertyStore(STGM_READ, &pProps);
    EXIT_ON_ERROR(hr)

    // Get the DirectSound or DirectSoundCapture device GUID
    // (in WCHAR string format) for the endpoint device.
    hr = pProps->GetValue(PKEY_AudioEndpoint_GUID, &var);
    EXIT_ON_ERROR(hr)

    // Convert the WCHAR string to a GUID structure.
    hr = CLSIDFromString(var.pwszVal, pDevGuid);
    EXIT_ON_ERROR(hr)

Exit:
    PropVariantClear(&var);
    SAFE_RELEASE(pEnumerator);
    SAFE_RELEASE(pDevice);
    SAFE_RELEASE(pProps);
    return hr;
}
```



En el ejemplo de código anterior, la función GetDirectSoundGuid acepta una dirección de flujo de datos (eRender o eCapture) y un rol de dispositivo (eConsole, eMultimedia o eCommunications) como parámetros de entrada. El tercer parámetro es un puntero a través del cual la función escribe un GUID de dispositivo que la aplicación puede proporcionar como parámetro de entrada a la función **DirectSoundCreate** o **DirectSoundCaptureCreate.**

En el ejemplo de código anterior se obtiene el GUID del dispositivo DirectSound mediante:

-   Creación de una [**instancia de interfaz IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) que representa el dispositivo de punto de conexión de audio que tiene la dirección de flujo de datos y el rol de dispositivo especificados.
-   Abrir el almacén de propiedades del dispositivo de punto de conexión de audio.
-   Obtención de [**la \_ propiedad \_ PKEY AudioEndpoint GUID**](pkey-audioendpoint-guid.md) del almacén de propiedades. El valor de propiedad es una representación de cadena del GUID del dispositivo DirectSound para el dispositivo de punto de conexión de audio.
-   Llamar a [**la función CLSIDFromString para**](https://www.bing.com/search?q=**CLSIDFromString**) convertir la representación de cadena del GUID del dispositivo en una estructura GUID. Para obtener más información sobre **CLSIDFromString,** consulte la documentación Windows SDK.

Después de obtener un GUID de dispositivo de la función GetDirectSoundGuid, la aplicación puede llamar a **DirectSoundCreate** o **DirectSoundCaptureCreate** con este GUID para crear el dispositivo de representación o captura de DirectSound que encapsula el dispositivo de punto de conexión de audio. Cuando DirectSound crea un dispositivo de esta manera, siempre asigna la secuencia de audio del dispositivo a la sesión predeterminada, la sesión de audio específica del proceso que se identifica mediante el VALOR GUID de la sesión \_ GUID NULL.

Si la aplicación requiere que DirectSound asigne la secuencia a una sesión de audio entre procesos o a una sesión con un GUID de sesión que no sea NULL, debe llamar al método [**IMMDevice::Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) para crear un objeto **IDirectSound** o **IDirectSoundCapture** en lugar de usar la técnica que se muestra en el ejemplo de código anterior. Para obtener un ejemplo de código que muestra cómo usar el método **Activate** para especificar una sesión de audio entre procesos o un GUID de sesión que no sea NULL para una secuencia, vea Roles de dispositivo [para DirectShow Aplicaciones](device-roles-for-directshow-applications.md). El ejemplo de código de esa sección muestra cómo crear un filtro DirectShow, pero, con modificaciones menores, el código se puede adaptar para crear un dispositivo DirectSound.

La función GetDirectSoundGuid del ejemplo de código anterior llama a la función [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) para crear un enumerador para los dispositivos de punto de conexión de audio del sistema. A menos que el programa de llamada llamara previamente a la función [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) o [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) para inicializar la biblioteca COM, se producirá un error en la llamada **a CoCreateInstance.** Para obtener más información sobre **CoCreateInstance,** **CoInitialize** y **CoInitializeEx,** consulte la documentación Windows SDK.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Interoperabilidad con las API de audio heredadas](interoperability-with-legacy-audio-apis.md)
</dt> </dl>

 

 
