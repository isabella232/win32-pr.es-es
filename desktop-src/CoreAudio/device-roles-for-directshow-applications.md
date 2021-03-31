---
description: Roles de dispositivo para aplicaciones de DirectShow
ms.assetid: 54f42bda-b4a0-465c-9ce6-9102d2908776
title: Roles de dispositivo para aplicaciones de DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df8b43ddd56870b65fc9ec1e3bb600e8e6b79528
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104495821"
---
# <a name="device-roles-for-directshow-applications"></a><span data-ttu-id="3c32a-103">Roles de dispositivo para aplicaciones de DirectShow</span><span class="sxs-lookup"><span data-stu-id="3c32a-103">Device Roles for DirectShow Applications</span></span>

> [!Note]  
> <span data-ttu-id="3c32a-104">La [API de MMDevice](mmdevice-api.md) admite roles de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3c32a-104">The [MMDevice API](mmdevice-api.md) supports device roles.</span></span> <span data-ttu-id="3c32a-105">Sin embargo, la interfaz de usuario de Windows Vista no implementa la compatibilidad con esta característica.</span><span class="sxs-lookup"><span data-stu-id="3c32a-105">However, the user interface in Windows Vista does not implement support for this feature.</span></span> <span data-ttu-id="3c32a-106">La compatibilidad con la interfaz de usuario para los roles de dispositivo puede implementarse en una versión futura de Windows.</span><span class="sxs-lookup"><span data-stu-id="3c32a-106">User interface support for device roles might be implemented in a future version of Windows.</span></span> <span data-ttu-id="3c32a-107">Para obtener más información, consulte [roles de dispositivo en Windows Vista](device-roles-in-windows-vista.md).</span><span class="sxs-lookup"><span data-stu-id="3c32a-107">For more information, see [Device Roles in Windows Vista](device-roles-in-windows-vista.md).</span></span>

 

<span data-ttu-id="3c32a-108">La API de DirectShow no proporciona un medio para que una aplicación Seleccione el [dispositivo de punto de conexión de audio](audio-endpoint-devices.md) que se asigna a un [rol de dispositivo](device-roles.md)determinado.</span><span class="sxs-lookup"><span data-stu-id="3c32a-108">The DirectShow API does not provide a means for an application to select the [audio endpoint device](audio-endpoint-devices.md) that is assigned to a particular [device role](device-roles.md).</span></span> <span data-ttu-id="3c32a-109">Sin embargo, en Windows Vista, las API de audio principales se pueden usar junto con una aplicación de DirectShow para habilitar la selección de dispositivos en función del rol del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3c32a-109">However, in Windows Vista, the core audio APIs can be used in conjunction with a DirectShow application to enable device selection based on device role.</span></span> <span data-ttu-id="3c32a-110">Con la ayuda de las API de audio principales, la aplicación puede:</span><span class="sxs-lookup"><span data-stu-id="3c32a-110">With the help of the core audio APIs, the application can:</span></span>

-   <span data-ttu-id="3c32a-111">Identifique el dispositivo de punto de conexión de audio que el usuario ha asignado a un rol de dispositivo determinado.</span><span class="sxs-lookup"><span data-stu-id="3c32a-111">Identify the audio endpoint device that the user has assigned to a particular device role.</span></span>
-   <span data-ttu-id="3c32a-112">Cree un filtro de representación de audio de DirectShow con una interfaz [**IBaseFilter**](/windows/desktop/api/strmif/nn-strmif-ibasefilter) que encapsule el dispositivo de punto de conexión de audio.</span><span class="sxs-lookup"><span data-stu-id="3c32a-112">Create a DirectShow audio rendering filter with an [**IBaseFilter**](/windows/desktop/api/strmif/nn-strmif-ibasefilter) interface that encapsulates the audio endpoint device.</span></span>
-   <span data-ttu-id="3c32a-113">Cree un gráfico de DirectShow que incorpore el filtro.</span><span class="sxs-lookup"><span data-stu-id="3c32a-113">Build a DirectShow graph that incorporates the filter.</span></span>

<span data-ttu-id="3c32a-114">Para obtener más información sobre DirectShow y [**IBaseFilter**](/windows/desktop/api/strmif/nn-strmif-ibasefilter), consulte la documentación de Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="3c32a-114">For more information about DirectShow and [**IBaseFilter**](/windows/desktop/api/strmif/nn-strmif-ibasefilter), see the Windows SDK documentation.</span></span>

<span data-ttu-id="3c32a-115">En el ejemplo de código siguiente se muestra cómo crear un filtro de representación de audio de DirectShow que encapsula el dispositivo de punto de conexión de representación que se asigna a un rol de dispositivo determinado:</span><span class="sxs-lookup"><span data-stu-id="3c32a-115">The following code example shows how to create a DirectShow audio rendering filter that encapsulates the rendering endpoint device that is assigned to a particular device role:</span></span>


```C++
//-----------------------------------------------------------
// Create a DirectShow audio rendering filter that
// encapsulates the audio endpoint device that is currently
// assigned to the specified device role.
//-----------------------------------------------------------
#define EXIT_ON_ERROR(hres)  \
              if (FAILED(hres)) { goto Exit; }
#define SAFE_RELEASE(punk)  \
              if ((punk) != NULL)  \
                { (punk)->Release(); (punk) = NULL; }

// This application's audio session GUID
const GUID guidAudioSessionId = {
    0xb13ff52e, 0xa5cf, 0x4fca,
    {0x9f, 0xc3, 0x42, 0x26, 0x5b, 0x0b, 0x14, 0xfb}
};

HRESULT CreateAudioRenderer(ERole role, IBaseFilter** ppAudioRenderer)
{
    HRESULT hr = S_OK;
    IMMDeviceEnumerator *pEnumerator = NULL;
    IMMDevice *pDevice = NULL;

    if (ppAudioRenderer == NULL)
    {
        return E_POINTER;
    }

    // Activate the IBaseFilter interface on the
    // audio renderer with the specified role.
    hr = CoCreateInstance(CLSID_MMDeviceEnumerator,
                          NULL, CLSCTX_INPROC_SERVER,
                          __uuidof(IMMDeviceEnumerator),
                          (void**)&pEnumerator);
    EXIT_ON_ERROR(hr)

    hr = pEnumerator->GetDefaultAudioEndpoint(eRender, role,
                                              &pDevice);
    EXIT_ON_ERROR(hr)

    DIRECTX_AUDIO_ACTIVATION_PARAMS  daap;
    daap.cbDirectXAudioActivationParams = sizeof(daap);
    daap.guidAudioSession = guidAudioSessionId;
    daap.dwAudioStreamFlags = AUDCLNT_STREAMFLAGS_CROSSPROCESS;

    PROPVARIANT  var;
    PropVariantInit(&var);

    var.vt = VT_BLOB;
    var.blob.cbSize = sizeof(daap);
    var.blob.pBlobData = (BYTE*)&daap;

    hr = pDevice->Activate(__uuidof(IBaseFilter),
                           CLSCTX_ALL, &var,
                           (void**)ppAudioRenderer);
    EXIT_ON_ERROR(hr)

Exit:
    SAFE_RELEASE(pEnumerator);
    SAFE_RELEASE(pDevice);
    return hr;
}
```



<span data-ttu-id="3c32a-116">En el ejemplo de código anterior, la función CreateAudioRenderer acepta un rol de dispositivo (eConsole, eMultimedia o eCommunications) como parámetro de entrada.</span><span class="sxs-lookup"><span data-stu-id="3c32a-116">In the preceding code example, the CreateAudioRenderer function accepts a device role (eConsole, eMultimedia, or eCommunications) as an input parameter.</span></span> <span data-ttu-id="3c32a-117">El segundo parámetro es un puntero a través del cual la función escribe la dirección de una instancia de la interfaz [**IBaseFilter**](/windows/desktop/api/strmif/nn-strmif-ibasefilter) .</span><span class="sxs-lookup"><span data-stu-id="3c32a-117">The second parameter is a pointer through which the function writes the address of an [**IBaseFilter**](/windows/desktop/api/strmif/nn-strmif-ibasefilter) interface instance.</span></span> <span data-ttu-id="3c32a-118">Además, en el ejemplo se muestra cómo usar el método [**IMMDevice:: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) para asignar la secuencia de audio de la instancia de **IBaseFilter** a una sesión de audio entre procesos con un GUID de sesión específico de la aplicación (especificado por la constante **guidAudioSessionId** ).</span><span class="sxs-lookup"><span data-stu-id="3c32a-118">In addition, the example shows how to use the [**IMMDevice::Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) method to assign the audio stream in the **IBaseFilter** instance to a cross-process audio session with an application-specific session GUID (specified by the **guidAudioSessionId** constant).</span></span> <span data-ttu-id="3c32a-119">El tercer parámetro de la llamada a **Activate** apunta a una estructura que contiene el GUID de sesión y el marcador de proceso cruzado.</span><span class="sxs-lookup"><span data-stu-id="3c32a-119">The third parameter in the **Activate** call points to a structure that contains the session GUID and cross-process flag.</span></span> <span data-ttu-id="3c32a-120">Si el usuario ejecuta varias instancias de la aplicación, las secuencias de audio de todas las instancias usan el mismo GUID de sesión y, por tanto, pertenecen a la misma sesión.</span><span class="sxs-lookup"><span data-stu-id="3c32a-120">If the user runs multiple instances of the application, then the audio streams from all the instances use the same session GUID and thus belong to the same session.</span></span>

<span data-ttu-id="3c32a-121">Como alternativa, el autor de la llamada puede especificar **null** como tercer parámetro en la llamada a [**Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) para asignar la secuencia a la sesión predeterminada como la sesión específica del proceso con el GUID NULL del valor GUID de sesión \_ .</span><span class="sxs-lookup"><span data-stu-id="3c32a-121">Alternatively, the caller can specify **NULL** as the third parameter in the [**Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) call to assign the stream to the default session as the process-specific session with session GUID value GUID\_NULL.</span></span> <span data-ttu-id="3c32a-122">Para obtener más información, vea **IMMDevice:: Activate**.</span><span class="sxs-lookup"><span data-stu-id="3c32a-122">For more information, see **IMMDevice::Activate**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3c32a-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3c32a-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3c32a-124">Interoperabilidad con las API de audio heredadas</span><span class="sxs-lookup"><span data-stu-id="3c32a-124">Interoperability with Legacy Audio APIs</span></span>](interoperability-with-legacy-audio-apis.md)
</dt> </dl>

 

 
