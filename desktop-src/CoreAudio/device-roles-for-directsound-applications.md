---
description: Roles de dispositivo para aplicaciones DirectSound
ms.assetid: 7d82d67f-aad8-4e5b-ac65-87d75774e613
title: Roles de dispositivo para aplicaciones DirectSound
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3829817f8b00c7288aceb8d0b6d418d5793ae580
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998068"
---
# <a name="device-roles-for-directsound-applications"></a><span data-ttu-id="32c90-103">Roles de dispositivo para aplicaciones DirectSound</span><span class="sxs-lookup"><span data-stu-id="32c90-103">Device Roles for DirectSound Applications</span></span>

> [!Note]  
> <span data-ttu-id="32c90-104">La [API de MMDevice](mmdevice-api.md) admite roles de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="32c90-104">The [MMDevice API](mmdevice-api.md) supports device roles.</span></span> <span data-ttu-id="32c90-105">Sin embargo, la interfaz de usuario de Windows Vista no implementa la compatibilidad con esta característica.</span><span class="sxs-lookup"><span data-stu-id="32c90-105">However, the user interface in Windows Vista does not implement support for this feature.</span></span> <span data-ttu-id="32c90-106">La compatibilidad con la interfaz de usuario para los roles de dispositivo puede implementarse en una versión futura de Windows.</span><span class="sxs-lookup"><span data-stu-id="32c90-106">User interface support for device roles might be implemented in a future version of Windows.</span></span> <span data-ttu-id="32c90-107">Para obtener más información, consulte [roles de dispositivo en Windows Vista](device-roles-in-windows-vista.md).</span><span class="sxs-lookup"><span data-stu-id="32c90-107">For more information, see [Device Roles in Windows Vista](device-roles-in-windows-vista.md).</span></span>

 

<span data-ttu-id="32c90-108">La API de DirectSound no proporciona un medio para que una aplicación Seleccione el [dispositivo de punto de conexión de audio](audio-endpoint-devices.md) que el usuario ha asignado a un [rol de dispositivo](device-roles.md)determinado.</span><span class="sxs-lookup"><span data-stu-id="32c90-108">The DirectSound API does not provide a means for an application to select the [audio endpoint device](audio-endpoint-devices.md) that the user has assigned to a particular [device role](device-roles.md).</span></span> <span data-ttu-id="32c90-109">Sin embargo, en Windows Vista, las API de audio principales se pueden usar junto con una aplicación DirectSound para habilitar la selección de dispositivos en función del rol del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="32c90-109">However, in Windows Vista, the core audio APIs can be used in conjunction with a DirectSound application to enable device selection based on device role.</span></span> <span data-ttu-id="32c90-110">Con la ayuda de las API de audio principales, la aplicación puede identificar el dispositivo de punto de conexión de audio que se asigna a un rol determinado, obtener el GUID del dispositivo de DirectSound para el dispositivo de punto de conexión y llamar a la función **DirectSoundCreate** o **DirectSoundCaptureCreate** para crear una instancia de la interfaz **IDirectSound** o **IDirectSoundCapture** que encapsula el dispositivo de extremo.</span><span class="sxs-lookup"><span data-stu-id="32c90-110">With the help of the core audio APIs, the application can identify the audio endpoint device that is assigned to a particular role, get the DirectSound device GUID for the endpoint device, and call the **DirectSoundCreate** or **DirectSoundCaptureCreate** function to create an **IDirectSound** or **IDirectSoundCapture** interface instance that encapsulates the endpoint device.</span></span> <span data-ttu-id="32c90-111">Para obtener más información acerca de DirectSound, consulte la documentación de Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="32c90-111">For more information about DirectSound, see the Windows SDK documentation.</span></span>

<span data-ttu-id="32c90-112">En el ejemplo de código siguiente se muestra cómo obtener el GUID del dispositivo DirectSound para el dispositivo de representación o captura que está asignado actualmente a un rol de dispositivo determinado:</span><span class="sxs-lookup"><span data-stu-id="32c90-112">The following code example shows how to obtain the DirectSound device GUID for the rendering or capture device that is currently assigned to a particular device role:</span></span>


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



<span data-ttu-id="32c90-113">En el ejemplo de código anterior, la función GetDirectSoundGuid acepta una dirección de flujo de datos (eRender o eCapture) y un rol de dispositivo (eConsole, eMultimedia o eCommunications) como parámetros de entrada.</span><span class="sxs-lookup"><span data-stu-id="32c90-113">In the preceding code example, the GetDirectSoundGuid function accepts a data-flow direction (eRender or eCapture) and a device role (eConsole, eMultimedia, or eCommunications) as input parameters.</span></span> <span data-ttu-id="32c90-114">El tercer parámetro es un puntero a través del cual la función escribe un GUID de dispositivo que la aplicación puede proporcionar como parámetro de entrada a la función **DirectSoundCreate** o **DirectSoundCaptureCreate** .</span><span class="sxs-lookup"><span data-stu-id="32c90-114">The third parameter is a pointer through which the function writes a device GUID that the application can supply as an input parameter to the **DirectSoundCreate** or **DirectSoundCaptureCreate** function.</span></span>

<span data-ttu-id="32c90-115">En el ejemplo de código anterior se obtiene el GUID del dispositivo DirectSound:</span><span class="sxs-lookup"><span data-stu-id="32c90-115">The preceding code example obtains the DirectSound device GUID by:</span></span>

-   <span data-ttu-id="32c90-116">Creación de una instancia de la interfaz [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) que representa el dispositivo de punto de conexión de audio que tiene la dirección de flujo de datos y el rol de dispositivo especificados.</span><span class="sxs-lookup"><span data-stu-id="32c90-116">Creating an [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) interface instance that represents the audio endpoint device that has the specified data-flow direction and device role.</span></span>
-   <span data-ttu-id="32c90-117">Abrir el almacén de propiedades del dispositivo de extremo de audio.</span><span class="sxs-lookup"><span data-stu-id="32c90-117">Opening the property store of the audio endpoint device.</span></span>
-   <span data-ttu-id="32c90-118">Obtener la [**propiedad \_ \_ GUID de PKEY AudioEndpoint**](pkey-audioendpoint-guid.md) del almacén de propiedades.</span><span class="sxs-lookup"><span data-stu-id="32c90-118">Getting the [**PKEY\_AudioEndpoint\_GUID**](pkey-audioendpoint-guid.md) property from the property store.</span></span> <span data-ttu-id="32c90-119">El valor de propiedad es una representación de cadena del GUID del dispositivo DirectSound para el dispositivo de extremo de audio.</span><span class="sxs-lookup"><span data-stu-id="32c90-119">The property value is a string representation of the DirectSound device GUID for the audio endpoint device.</span></span>
-   <span data-ttu-id="32c90-120">Llamar a la función [**CLSIDFromString**](https://www.bing.com/search?q=**CLSIDFromString**) para convertir la representación de cadena del GUID del dispositivo en una estructura GUID.</span><span class="sxs-lookup"><span data-stu-id="32c90-120">Calling the [**CLSIDFromString**](https://www.bing.com/search?q=**CLSIDFromString**) function to convert the string representation of the device GUID to a GUID structure.</span></span> <span data-ttu-id="32c90-121">Para obtener más información sobre **CLSIDFromString**, consulte la documentación de Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="32c90-121">For more information about **CLSIDFromString**, see the Windows SDK documentation.</span></span>

<span data-ttu-id="32c90-122">Después de obtener un GUID de dispositivo de la función GetDirectSoundGuid, la aplicación puede llamar a **DirectSoundCreate** o **DIRECTSOUNDCAPTURECREATE** con este GUID para crear el dispositivo de representación o captura de DirectSound que encapsula el dispositivo de punto de conexión de audio.</span><span class="sxs-lookup"><span data-stu-id="32c90-122">After obtaining a device GUID from the GetDirectSoundGuid function, the application can call **DirectSoundCreate** or **DirectSoundCaptureCreate** with this GUID to create the DirectSound rendering or capture device that encapsulates the audio endpoint device.</span></span> <span data-ttu-id="32c90-123">Cuando DirectSound crea un dispositivo de esta manera, siempre asigna la secuencia de audio del dispositivo a la sesión predeterminada, la sesión de audio específica del proceso identificada por el GUID del valor GUID de la sesión \_ .</span><span class="sxs-lookup"><span data-stu-id="32c90-123">When DirectSound creates a device in this way, it always assigns the device's audio stream to the default session—the process-specific audio session that is identified by the session GUID value GUID\_NULL.</span></span>

<span data-ttu-id="32c90-124">Si la aplicación requiere DirectSound para asignar la secuencia a una sesión de audio entre procesos o a una sesión con un GUID de sesión que no sea **null** , debe llamar al método [**IMMDevice:: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) para crear un objeto **IDirectSound** o **IDirectSoundCapture** en lugar de utilizar la técnica que se muestra en el ejemplo de código anterior.</span><span class="sxs-lookup"><span data-stu-id="32c90-124">If the application requires DirectSound to assign the stream to a cross-process audio session or to a session with a non-**NULL** session GUID, it should call the [**IMMDevice::Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) method to create an **IDirectSound** or **IDirectSoundCapture** object instead of using the technique shown in the preceding code example.</span></span> <span data-ttu-id="32c90-125">Para obtener un ejemplo de código que muestra cómo usar el método **Activate** para especificar una sesión de audio entre procesos o un GUID de sesión que no **es null** para un flujo, vea [roles de dispositivo para aplicaciones de DirectShow](device-roles-for-directshow-applications.md).</span><span class="sxs-lookup"><span data-stu-id="32c90-125">For a code example that shows how to use the **Activate** method to specify a cross-process audio session or a non-**NULL** session GUID for a stream, see [Device Roles for DirectShow Applications](device-roles-for-directshow-applications.md).</span></span> <span data-ttu-id="32c90-126">En el ejemplo de código de esta sección se muestra cómo crear un filtro de DirectShow, pero, con modificaciones menores, el código se puede adaptar para crear un dispositivo de DirectSound.</span><span class="sxs-lookup"><span data-stu-id="32c90-126">The code example in that section shows how to create a DirectShow filter, but, with minor modifications, the code can be adapted to create a DirectSound device.</span></span>

<span data-ttu-id="32c90-127">La función GetDirectSoundGuid del ejemplo de código anterior llama a la función [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) para crear un enumerador para los dispositivos de punto de conexión de audio en el sistema.</span><span class="sxs-lookup"><span data-stu-id="32c90-127">The GetDirectSoundGuid function in the preceding code example calls the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) function to create an enumerator for the audio endpoint devices in the system.</span></span> <span data-ttu-id="32c90-128">A menos que el programa de llamada previamente haya llamado a la función [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) o [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) para inicializar la biblioteca com, se producirá un error en la llamada a **CoCreateInstance** .</span><span class="sxs-lookup"><span data-stu-id="32c90-128">Unless the calling program previously called either the [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) or [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) function to initialize the COM library, the **CoCreateInstance** call will fail.</span></span> <span data-ttu-id="32c90-129">Para obtener más información sobre **CoCreateInstance**, **CoInitialize** y **CoInitializeEx**, vea la documentación de Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="32c90-129">For more information about **CoCreateInstance**, **CoInitialize**, and **CoInitializeEx**, see the Windows SDK documentation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="32c90-130">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="32c90-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="32c90-131">Interoperabilidad con las API de audio heredadas</span><span class="sxs-lookup"><span data-stu-id="32c90-131">Interoperability with Legacy Audio APIs</span></span>](interoperability-with-legacy-audio-apis.md)
</dt> </dl>

 

 
