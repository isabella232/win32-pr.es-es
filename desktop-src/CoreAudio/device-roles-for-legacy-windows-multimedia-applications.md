---
description: Roles de dispositivo para aplicaciones multimedia heredadas de Windows
ms.assetid: 54dcaa0e-2652-406d-ba24-c8885924acc6
title: Roles de dispositivo para aplicaciones multimedia heredadas de Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44a4ad6728659e4c865aed773575268844fe330e
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105649325"
---
# <a name="device-roles-for-legacy-windows-multimedia-applications"></a><span data-ttu-id="e4763-103">Roles de dispositivo para aplicaciones multimedia heredadas de Windows</span><span class="sxs-lookup"><span data-stu-id="e4763-103">Device Roles for Legacy Windows Multimedia Applications</span></span>

> [!Note]  
> <span data-ttu-id="e4763-104">La API de MMDevice admite roles de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e4763-104">The MMDevice API supports device roles.</span></span> <span data-ttu-id="e4763-105">Sin embargo, la interfaz de usuario de Windows Vista no implementa la compatibilidad con esta característica.</span><span class="sxs-lookup"><span data-stu-id="e4763-105">However, the user interface in Windows Vista does not implement support for this feature.</span></span> <span data-ttu-id="e4763-106">La compatibilidad con la interfaz de usuario para los roles de dispositivo puede implementarse en una versión futura de Windows.</span><span class="sxs-lookup"><span data-stu-id="e4763-106">User interface support for device roles might be implemented in a future version of Windows.</span></span> <span data-ttu-id="e4763-107">Para obtener más información, consulte [roles de dispositivo en Windows Vista](device-roles-in-windows-vista.md).</span><span class="sxs-lookup"><span data-stu-id="e4763-107">For more information, see [Device Roles in Windows Vista](device-roles-in-windows-vista.md).</span></span>

 

<span data-ttu-id="e4763-108">Las funciones heredadas de **waveOutXxx** y **WaveInXxx** multimedia de Windows no proporcionan ningún medio para que una aplicación Seleccione el dispositivo de punto de [conexión de audio](audio-endpoint-devices.md) que el usuario ha asignado a un rol de [dispositivo](device-roles.md)determinado.</span><span class="sxs-lookup"><span data-stu-id="e4763-108">The legacy Windows multimedia **waveOutXxx** and **waveInXxx** functions provide no means for an application to select the [audio endpoint device](audio-endpoint-devices.md) that the user has assigned to a particular [device role](device-roles.md).</span></span> <span data-ttu-id="e4763-109">Sin embargo, en Windows Vista, las API de audio principales se pueden usar junto con una aplicación multimedia de Windows para habilitar la selección de dispositivos en función del rol del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e4763-109">However, in Windows Vista, the core audio APIs can be used in conjunction with a Windows multimedia application to enable device selection based on device role.</span></span> <span data-ttu-id="e4763-110">Por ejemplo, con la ayuda de la [API de MMDevice](mmdevice-api.md), una aplicación de **waveOutXxx** puede identificar el dispositivo de punto de conexión de audio que se asigna a un rol, identificar el dispositivo de salida de forma de onda correspondiente y llamar a la función **waveOutOpen** para abrir una instancia del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e4763-110">For example, with the help of the [MMDevice API](mmdevice-api.md), a **waveOutXxx** application can identify the audio endpoint device that is assigned to a role, identify the corresponding waveform output device, and call the **waveOutOpen** function to open an instance of the device.</span></span> <span data-ttu-id="e4763-111">Para obtener más información sobre **waveOutXxx** y **waveInXxx**, consulte la documentación de Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="e4763-111">For more information about **waveOutXxx** and **waveInXxx**, see the Windows SDK documentation.</span></span>

<span data-ttu-id="e4763-112">En el ejemplo de código siguiente se muestra cómo obtener el identificador de dispositivo de forma de onda para el dispositivo de punto de conexión de representación que se asigna a un rol de dispositivo determinado:</span><span class="sxs-lookup"><span data-stu-id="e4763-112">The following code example shows how to obtain the waveform device ID for the rendering endpoint device that is assigned to a particular device role:</span></span>


```C++
//-----------------------------------------------------------
// This function gets the waveOut ID of the audio endpoint
// device that is currently assigned to the specified device
// role. The caller can use the waveOut ID to open the
// waveOut device that corresponds to the endpoint device.
//-----------------------------------------------------------
#define EXIT_ON_ERROR(hres)  \
              if (FAILED(hres)) { goto Exit; }
#define SAFE_RELEASE(punk)  \
              if ((punk) != NULL)  \
                { (punk)->Release(); (punk) = NULL; }

HRESULT GetWaveOutId(ERole role, int *pWaveOutId)
{
    HRESULT hr;
    IMMDeviceEnumerator *pEnumerator = NULL;
    IMMDevice *pDevice = NULL;
    WCHAR *pstrEndpointIdKey = NULL;
    WCHAR *pstrEndpointId = NULL;

    if (pWaveOutId == NULL)
    {
        return E_POINTER;
    }

    // Create an audio endpoint device enumerator.
    hr = CoCreateInstance(__uuidof(MMDeviceEnumerator),
                          NULL, CLSCTX_INPROC_SERVER,
                          __uuidof(IMMDeviceEnumerator),
                          (void**)&pEnumerator);
    EXIT_ON_ERROR(hr)

    // Get the audio endpoint device that the user has
    // assigned to the specified device role.
    hr = pEnumerator->GetDefaultAudioEndpoint(eRender, role,
                                              &pDevice);
    EXIT_ON_ERROR(hr)

    // Get the endpoint ID string of the audio endpoint device.
    hr = pDevice->GetId(&pstrEndpointIdKey);
    EXIT_ON_ERROR(hr)

    // Get the size of the endpoint ID string.
    size_t  cbEndpointIdKey;

    hr = StringCbLength(pstrEndpointIdKey,
                        STRSAFE_MAX_CCH * sizeof(WCHAR),
                        &cbEndpointIdKey);
    EXIT_ON_ERROR(hr)

    // Include terminating null in string size.
    cbEndpointIdKey += sizeof(WCHAR);

    // Allocate a buffer for a second string of the same size.
    pstrEndpointId = (WCHAR*)CoTaskMemAlloc(cbEndpointIdKey);
    if (pstrEndpointId == NULL)
    {
        EXIT_ON_ERROR(hr = E_OUTOFMEMORY)
    }

    // Each for-loop iteration below compares the endpoint ID
    // string of the audio endpoint device to the endpoint ID
    // string of an enumerated waveOut device. If the strings
    // match, then we've found the waveOut device that is
    // assigned to the specified device role.
    int waveOutId;
    int cWaveOutDevices = waveOutGetNumDevs();

    for (waveOutId = 0; waveOutId < cWaveOutDevices; waveOutId++)
    {
        MMRESULT mmr;
        size_t cbEndpointId;

        // Get the size (including the terminating null) of
        // the endpoint ID string of the waveOut device.
        mmr = waveOutMessage((HWAVEOUT)IntToPtr(waveOutId),
                             DRV_QUERYFUNCTIONINSTANCEIDSIZE,
                             (DWORD_PTR)&cbEndpointId, NULL);
        if (mmr != MMSYSERR_NOERROR ||
            cbEndpointIdKey != cbEndpointId)  // do sizes match?
        {
            continue;  // not a matching device
        }

        // Get the endpoint ID string for this waveOut device.
        mmr = waveOutMessage((HWAVEOUT)IntToPtr(waveOutId),
                             DRV_QUERYFUNCTIONINSTANCEID,
                             (DWORD_PTR)pstrEndpointId,
                             cbEndpointId);
        if (mmr != MMSYSERR_NOERROR)
        {
            continue;
        }

        // Check whether the endpoint ID string of this waveOut
        // device matches that of the audio endpoint device.
        if (lstrcmpi(pstrEndpointId, pstrEndpointIdKey) == 0)
        {
            *pWaveOutId = waveOutId;  // found match
            hr = S_OK;
            break;
        }
    }

    if (waveOutId == cWaveOutDevices)
    {
        // We reached the end of the for-loop above without
        // finding a waveOut device with a matching endpoint
        // ID string. This behavior is quite unexpected.
        hr = E_UNEXPECTED;
    }

Exit:
    SAFE_RELEASE(pEnumerator);
    SAFE_RELEASE(pDevice);
    CoTaskMemFree(pstrEndpointIdKey);  // NULL pointer okay
    CoTaskMemFree(pstrEndpointId);
    return hr;
}
```



<span data-ttu-id="e4763-113">En el ejemplo de código anterior, la función GetWaveOutId acepta un rol de dispositivo (eConsole, eMultimedia o eCommunications) como parámetro de entrada.</span><span class="sxs-lookup"><span data-stu-id="e4763-113">In the preceding code example, the GetWaveOutId function accepts a device role (eConsole, eMultimedia, or eCommunications) as an input parameter.</span></span> <span data-ttu-id="e4763-114">El segundo parámetro es un puntero a través del cual la función escribe el identificador de dispositivo de forma de onda para el dispositivo de salida de forma de onda asignado al rol especificado.</span><span class="sxs-lookup"><span data-stu-id="e4763-114">The second parameter is a pointer through which the function writes the waveform device ID for the waveform output device that is assigned to the specified role.</span></span> <span data-ttu-id="e4763-115">A continuación, la aplicación puede llamar a **waveOutOpen** con este identificador para abrir el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e4763-115">The application can then call **waveOutOpen** with this ID to open the device.</span></span>

<span data-ttu-id="e4763-116">El bucle principal del ejemplo de código anterior contiene dos llamadas a la función **waveOutMessage** .</span><span class="sxs-lookup"><span data-stu-id="e4763-116">The main loop in the preceding code example contains two calls to the **waveOutMessage** function.</span></span> <span data-ttu-id="e4763-117">La primera llamada envía un \_ mensaje DRV QUERYFUNCTIONINSTANCEIDSIZE para recuperar el tamaño, en bytes, de la [cadena de identificador de punto de conexión](endpoint-id-strings.md) del dispositivo de forma de onda que se identifica mediante el parámetro *waveOutId* .</span><span class="sxs-lookup"><span data-stu-id="e4763-117">The first call sends a DRV\_QUERYFUNCTIONINSTANCEIDSIZE message to retrieve the size, in bytes, of the [endpoint ID string](endpoint-id-strings.md) of the waveform device that is identified by the *waveOutId* parameter.</span></span> <span data-ttu-id="e4763-118">(La cadena de ID. de punto de conexión identifica el dispositivo de punto de conexión de audio que subyace a la abstracción de dispositivo de onda). El tamaño indicado por esta llamada incluye el espacio para el carácter nulo de terminación al final de la cadena.</span><span class="sxs-lookup"><span data-stu-id="e4763-118">(The endpoint ID string identifies the audio endpoint device that underlies the waveform device abstraction.) The size reported by this call includes the space for the terminating null character at the end of the string.</span></span> <span data-ttu-id="e4763-119">El programa puede utilizar la información de tamaño para asignar un búfer lo suficientemente grande como para contener la cadena de identificador de extremo completa.</span><span class="sxs-lookup"><span data-stu-id="e4763-119">The program can use the size information to allocate a buffer that is large enough to contain the entire endpoint ID string.</span></span>

<span data-ttu-id="e4763-120">La segunda llamada a **waveOutMessage** envía un \_ mensaje DRV QUERYFUNCTIONINSTANCEID para recuperar la cadena de identificador de dispositivo del dispositivo de salida de onda.</span><span class="sxs-lookup"><span data-stu-id="e4763-120">The second call to **waveOutMessage** sends a DRV\_QUERYFUNCTIONINSTANCEID message to retrieve the device ID string of the waveform output device.</span></span> <span data-ttu-id="e4763-121">En el código de ejemplo se compara esta cadena con la cadena de identificador de dispositivo del dispositivo de punto de conexión de audio con el rol de dispositivo especificado.</span><span class="sxs-lookup"><span data-stu-id="e4763-121">The example code compares this string to the device ID string of the audio endpoint device with the specified device role.</span></span> <span data-ttu-id="e4763-122">Si las cadenas coinciden, la función escribe el identificador de dispositivo de forma de onda en la ubicación a la que apunta el parámetro *pWaveOutId*.</span><span class="sxs-lookup"><span data-stu-id="e4763-122">If the strings match, then the function writes the waveform device ID to the location pointed to by parameter *pWaveOutId*.</span></span> <span data-ttu-id="e4763-123">El autor de la llamada puede usar este identificador para abrir el dispositivo de salida de onda que tiene el rol de dispositivo especificado.</span><span class="sxs-lookup"><span data-stu-id="e4763-123">The caller can use this ID to open the waveform output device that has the specified device role.</span></span>

<span data-ttu-id="e4763-124">Windows Vista admite los \_ mensajes DRV QUERYFUNCTIONINSTANCEIDSIZE y DRV \_ QUERYFUNCTIONINSTANCEID.</span><span class="sxs-lookup"><span data-stu-id="e4763-124">Windows Vista supports the DRV\_QUERYFUNCTIONINSTANCEIDSIZE and DRV\_QUERYFUNCTIONINSTANCEID messages.</span></span> <span data-ttu-id="e4763-125">No se admiten en versiones anteriores de Windows, incluidas Windows Server 2003, Windows XP y Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="e4763-125">They are not supported in earlier versions of Windows, including Windows Server 2003, Windows XP, and Windows 2000.</span></span>

<span data-ttu-id="e4763-126">La función en el ejemplo de código anterior obtiene el identificador de dispositivo de la onda de onda para un dispositivo de representación, pero, con algunas modificaciones, se puede adaptar para obtener el identificador de dispositivo de la onda de un dispositivo de captura.</span><span class="sxs-lookup"><span data-stu-id="e4763-126">The function in the preceding code example obtains the waveform device ID for a rendering device, but, with a few modifications, it can be adapted to obtain the waveform device ID for a capture device.</span></span> <span data-ttu-id="e4763-127">A continuación, la aplicación puede llamar a **waveInOpen** con este identificador para abrir el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e4763-127">The application can then call **waveInOpen** with this ID to open the device.</span></span> <span data-ttu-id="e4763-128">Para cambiar el ejemplo de código anterior para obtener el identificador de dispositivo de forma de onda para el dispositivo de extremo de captura de audio que se asigna a un rol determinado, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="e4763-128">To change the preceding code example to get the waveform device ID for the audio-capture endpoint device that is assigned to a particular role, do the following:</span></span>

-   <span data-ttu-id="e4763-129">Reemplace todas las llamadas a la función **waveOutXxx** en el ejemplo anterior por las llamadas de función **waveInXxx** correspondientes.</span><span class="sxs-lookup"><span data-stu-id="e4763-129">Replace all of the **waveOutXxx** function calls in the preceding example with the corresponding **waveInXxx** function calls.</span></span>
-   <span data-ttu-id="e4763-130">Cambie el tipo de identificador HWAVEOUT a HWAVEIN.</span><span class="sxs-lookup"><span data-stu-id="e4763-130">Change handle type HWAVEOUT to HWAVEIN.</span></span>
-   <span data-ttu-id="e4763-131">Reemplace la constante de enumeración [**ERole**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole) ERender por eCapture.</span><span class="sxs-lookup"><span data-stu-id="e4763-131">Replace [**ERole**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole) enumeration constant eRender with eCapture.</span></span>

<span data-ttu-id="e4763-132">En Windows Vista, las funciones **waveOutOpen** y **waveInOpen** siempre asignan las secuencias de audio que crean a la sesión predeterminada, la sesión específica del proceso que se identifica mediante el GUID NULL del valor GUID de la sesión \_ .</span><span class="sxs-lookup"><span data-stu-id="e4763-132">In Windows Vista, the **waveOutOpen** and **waveInOpen** functions always assign the audio streams that they create to the default session—the process-specific session that is identified by the session GUID value GUID\_NULL.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e4763-133">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e4763-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e4763-134">Interoperabilidad con las API de audio heredadas</span><span class="sxs-lookup"><span data-stu-id="e4763-134">Interoperability with Legacy Audio APIs</span></span>](interoperability-with-legacy-audio-apis.md)
</dt> </dl>

 

 



