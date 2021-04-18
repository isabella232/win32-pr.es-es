---
description: Microsoft Media Foundation admite la captura de audio y vídeo.
ms.assetid: 8a9d96f8-1096-4b66-a2ec-8a95d754ea72
title: Captura de audio y vídeo en Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 506c14ee4ab94a27cfafbe18a97ffa8f05676f1f
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105697962"
---
# <a name="audiovideo-capture-in-media-foundation"></a><span data-ttu-id="7de24-103">Captura de audio y vídeo en Media Foundation</span><span class="sxs-lookup"><span data-stu-id="7de24-103">Audio/Video Capture in Media Foundation</span></span>

<span data-ttu-id="7de24-104">Microsoft Media Foundation admite la captura de audio y vídeo.</span><span class="sxs-lookup"><span data-stu-id="7de24-104">Microsoft Media Foundation supports audio and video capture.</span></span> <span data-ttu-id="7de24-105">Los dispositivos de captura de vídeo se admiten a través del controlador de la clase UVC y deben ser compatibles con UVC 1,1.</span><span class="sxs-lookup"><span data-stu-id="7de24-105">Video capture devices are supported through the UVC class driver and must be compatible with UVC 1.1.</span></span> <span data-ttu-id="7de24-106">Los dispositivos de captura de audio se admiten a través de la API de sesión de audio de Windows (WASAPI).</span><span class="sxs-lookup"><span data-stu-id="7de24-106">Audio capture devices are supported through Windows Audio Session API (WASAPI).</span></span>

<span data-ttu-id="7de24-107">Un dispositivo de captura se representa en Media Foundation mediante un objeto de origen multimedia, que expone la interfaz [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) .</span><span class="sxs-lookup"><span data-stu-id="7de24-107">A capture device is represented in Media Foundation by a media source object, which exposes the [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) interface.</span></span> <span data-ttu-id="7de24-108">En la mayoría de los casos, la aplicación no usará esta interfaz directamente, pero usará una API de nivel superior como el [lector de origen](source-reader.md) para controlar el dispositivo de captura.</span><span class="sxs-lookup"><span data-stu-id="7de24-108">In most cases, the application will not use this interface directly, but will use a higher-level API such as the [Source Reader](source-reader.md) to control the capture device.</span></span>

## <a name="enumerate-capture-devices"></a><span data-ttu-id="7de24-109">Enumerar dispositivos de captura</span><span class="sxs-lookup"><span data-stu-id="7de24-109">Enumerate Capture Devices</span></span>

<span data-ttu-id="7de24-110">Para enumerar los dispositivos de captura en el sistema, realice los pasos siguientes:</span><span class="sxs-lookup"><span data-stu-id="7de24-110">To enumerate the capture devices on the system, perform the following steps:</span></span>

1.  <span data-ttu-id="7de24-111">Llame a la función [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) para crear un almacén de atributos.</span><span class="sxs-lookup"><span data-stu-id="7de24-111">Call the [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) function to create an attribute store.</span></span>
2.  <span data-ttu-id="7de24-112">Establezca el atributo de [ \_ tipo de origen del \_ atributo \_ \_ MF DEVSOURCE](mf-devsource-attribute-source-type.md) en uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="7de24-112">Set the [MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE](mf-devsource-attribute-source-type.md) attribute to one of the following values:</span></span>

    | <span data-ttu-id="7de24-113">Value</span><span class="sxs-lookup"><span data-stu-id="7de24-113">Value</span></span>                                                    | <span data-ttu-id="7de24-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="7de24-114">Description</span></span>                      |
    |----------------------------------------------------------|----------------------------------|
    | <span data-ttu-id="7de24-115">**\_tipo de origen del atributo MF DEVSOURCE \_ \_ \_ \_ \_ GUID AUDCAP**</span><span class="sxs-lookup"><span data-stu-id="7de24-115">**MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_AUDCAP\_GUID**</span></span> | <span data-ttu-id="7de24-116">Enumerar los dispositivos de captura de audio.</span><span class="sxs-lookup"><span data-stu-id="7de24-116">Enumerate audio capture devices.</span></span> |
    | <span data-ttu-id="7de24-117">**\_tipo de origen de atributo MF DEVSOURCE de \_ \_ \_ \_ VIDCAP \_ GUID**</span><span class="sxs-lookup"><span data-stu-id="7de24-117">**MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_VIDCAP\_GUID**</span></span> | <span data-ttu-id="7de24-118">Enumerar los dispositivos de captura de vídeo.</span><span class="sxs-lookup"><span data-stu-id="7de24-118">Enumerate video capture devices.</span></span> |

    

     

3.  <span data-ttu-id="7de24-119">Llame a la función [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources) .</span><span class="sxs-lookup"><span data-stu-id="7de24-119">Call the [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources) function.</span></span> <span data-ttu-id="7de24-120">Esta función asigna una matriz de punteros [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) .</span><span class="sxs-lookup"><span data-stu-id="7de24-120">This function allocates an array of [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointers.</span></span> <span data-ttu-id="7de24-121">Cada puntero representa un objeto de activación para un dispositivo del sistema.</span><span class="sxs-lookup"><span data-stu-id="7de24-121">Each pointer represents an activation object for one device on the system.</span></span>
4.  <span data-ttu-id="7de24-122">Llame al método [**IMFActivate:: ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) para crear una instancia del origen multimedia a partir de uno de los objetos de activación.</span><span class="sxs-lookup"><span data-stu-id="7de24-122">Call the [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) method to create an instance of the media source from one of the activation objects.</span></span>

<span data-ttu-id="7de24-123">En el ejemplo siguiente se crea un origen de medios para el primer dispositivo de captura de vídeo en la lista de enumeración:</span><span class="sxs-lookup"><span data-stu-id="7de24-123">The following example creates a media source for the first video capture device in the enumeration list:</span></span>


```C++
HRESULT CreateVideoCaptureDevice(IMFMediaSource **ppSource)
{
    *ppSource = NULL;

    UINT32 count = 0;

    IMFAttributes *pConfig = NULL;
    IMFActivate **ppDevices = NULL;

    // Create an attribute store to hold the search criteria.
    HRESULT hr = MFCreateAttributes(&pConfig, 1);

    // Request video capture devices.
    if (SUCCEEDED(hr))
    {
        hr = pConfig->SetGUID(
            MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE, 
            MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_GUID
            );
    }

    // Enumerate the devices,
    if (SUCCEEDED(hr))
    {
        hr = MFEnumDeviceSources(pConfig, &ppDevices, &count);
    }

    // Create a media source for the first device in the list.
    if (SUCCEEDED(hr))
    {
        if (count > 0)
        {
            hr = ppDevices[0]->ActivateObject(IID_PPV_ARGS(ppSource));
        }
        else
        {
            hr = MF_E_NOT_FOUND;
        }
    }

    for (DWORD i = 0; i < count; i++)
    {
        ppDevices[i]->Release();
    }
    CoTaskMemFree(ppDevices);
    return hr;
}
```



<span data-ttu-id="7de24-124">Puede consultar los objetos de activación para varios atributos, como los siguientes:</span><span class="sxs-lookup"><span data-stu-id="7de24-124">You can query the activation objects for various attributes, including the following:</span></span>

-   <span data-ttu-id="7de24-125">El atributo de [ \_ \_ \_ \_ nombre descriptivo del atributo MF DEVSOURCE](mf-devsource-attribute-friendly-name.md) contiene el nombre para mostrar del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7de24-125">The [MF\_DEVSOURCE\_ATTRIBUTE\_FRIENDLY\_NAME](mf-devsource-attribute-friendly-name.md) attribute contains the display name of the device.</span></span> <span data-ttu-id="7de24-126">El nombre para mostrar es adecuado para mostrar al usuario, pero podría no ser único.</span><span class="sxs-lookup"><span data-stu-id="7de24-126">The display name is suitable for showing to the user, but might not be unique.</span></span>
-   <span data-ttu-id="7de24-127">En el caso de los dispositivos de vídeo, el atributo de [ \_ tipo de origen del atributo MF DEVSOURCE de \_ \_ código fuente de atributo \_ \_ VIDCAP \_ \_ ](mf-devsource-attribute-source-type-vidcap-symbolic-link.md) contiene el vínculo simbólico al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7de24-127">For video devices, the [MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_VIDCAP\_SYMBOLIC\_LINK](mf-devsource-attribute-source-type-vidcap-symbolic-link.md) attribute contains the symbolic link to the device.</span></span> <span data-ttu-id="7de24-128">El vínculo simbólico identifica de forma única el dispositivo en el sistema, pero no es una cadena legible.</span><span class="sxs-lookup"><span data-stu-id="7de24-128">The symbolic link uniquely identifies the device on the system, but is not a readable string.</span></span>
-   <span data-ttu-id="7de24-129">En el caso de los dispositivos de audio, el atributo [MF \_ DEVSOURCE \_ tipo de origen de \_ \_ \_ \_ \_ identificador de extremo AUDCAP](mf-devsource-attribute-source-type-audcap-endpoint-id.md) contiene el ID. de punto de conexión de audio del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7de24-129">For audio devices, the [MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_AUDCAP\_ENDPOINT\_ID](mf-devsource-attribute-source-type-audcap-endpoint-id.md) attribute contains the audio endpoint ID of the device.</span></span> <span data-ttu-id="7de24-130">El identificador del punto de conexión de audio es similar a un vínculo simbólico.</span><span class="sxs-lookup"><span data-stu-id="7de24-130">The audio endpoint ID is similar to a symbolic link.</span></span> <span data-ttu-id="7de24-131">Identifica de forma única el dispositivo en el sistema, pero no es una cadena legible.</span><span class="sxs-lookup"><span data-stu-id="7de24-131">It uniquely identifies the device on the system, but is not a readable string.</span></span>

<span data-ttu-id="7de24-132">En el ejemplo siguiente se toma una matriz de punteros [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) y se imprime el nombre para mostrar de cada dispositivo en la ventana de depuración:</span><span class="sxs-lookup"><span data-stu-id="7de24-132">The following example takes an array of [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointers and prints the display name of each device to the debug window:</span></span>


```C++
void DebugShowDeviceNames(IMFActivate **ppDevices, UINT count)
{
    for (DWORD i = 0; i < count; i++)
    {
        HRESULT hr = S_OK;
        WCHAR *szFriendlyName = NULL;
    
        // Try to get the display name.
        UINT32 cchName;
        hr = ppDevices[i]->GetAllocatedString(
            MF_DEVSOURCE_ATTRIBUTE_FRIENDLY_NAME,
            &szFriendlyName, &cchName);

        if (SUCCEEDED(hr))
        {
            OutputDebugString(szFriendlyName);
            OutputDebugString(L"\n");
        }
        CoTaskMemFree(szFriendlyName);
    }
}
```



<span data-ttu-id="7de24-133">Si ya conoce el vínculo simbólico de un dispositivo de vídeo, hay otra manera de crear el origen de medios para el dispositivo:</span><span class="sxs-lookup"><span data-stu-id="7de24-133">If you already know the symbolic link for a video device, there is another way to create the media source for the device:</span></span>

1.  <span data-ttu-id="7de24-134">Llame a [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) para crear un almacén de atributos.</span><span class="sxs-lookup"><span data-stu-id="7de24-134">Call [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) to create an attribute store.</span></span>
2.  <span data-ttu-id="7de24-135">Establezca el atributo de [tipo de origen del \_ \_ atributo MF \_ \_ DEVSOURCE](mf-devsource-attribute-source-type.md) en el **tipo de origen de \_ atributo MF DEVSOURCE de \_ \_ \_ \_ VIDCAP \_ GUID**.</span><span class="sxs-lookup"><span data-stu-id="7de24-135">Set the [MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE](mf-devsource-attribute-source-type.md) attribute to **MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_VIDCAP\_GUID**.</span></span>
3.  <span data-ttu-id="7de24-136">Establezca el [tipo de origen del atributo MF DEVSOURCE atributo de \_ \_ \_ \_ \_ \_ \_ vínculo simbólico de VIDCAP](mf-devsource-attribute-source-type-vidcap-symbolic-link.md) en el vínculo simbólico.</span><span class="sxs-lookup"><span data-stu-id="7de24-136">Set the [MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_VIDCAP\_SYMBOLIC\_LINK](mf-devsource-attribute-source-type-vidcap-symbolic-link.md) attribute to the symbolic link.</span></span>
4.  <span data-ttu-id="7de24-137">Llame a la función [**MFCreateDeviceSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource) o [**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate) .</span><span class="sxs-lookup"><span data-stu-id="7de24-137">Call either the [**MFCreateDeviceSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource) or [**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate) function.</span></span> <span data-ttu-id="7de24-138">El primero devuelve un puntero [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) .</span><span class="sxs-lookup"><span data-stu-id="7de24-138">The former returns an [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) pointer.</span></span> <span data-ttu-id="7de24-139">El último devuelve un puntero [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) a un objeto de activación.</span><span class="sxs-lookup"><span data-stu-id="7de24-139">The latter returns an [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointer to an activation object.</span></span> <span data-ttu-id="7de24-140">Puede usar el objeto de activación para crear el origen.</span><span class="sxs-lookup"><span data-stu-id="7de24-140">You can use the activation object to create the source.</span></span> <span data-ttu-id="7de24-141">(Se pueden calcular las referencias de un objeto de activación en otro proceso, por lo que resulta útil si desea crear el origen en otro proceso.</span><span class="sxs-lookup"><span data-stu-id="7de24-141">(An activation object can be marshaled to another process, so it is useful if you want to create the source in another process.</span></span> <span data-ttu-id="7de24-142">Para obtener más información, vea [objetos de activación](activation-objects.md)).</span><span class="sxs-lookup"><span data-stu-id="7de24-142">For more information, see [Activation Objects](activation-objects.md).)</span></span>

<span data-ttu-id="7de24-143">En el ejemplo siguiente se toma el vínculo simbólico de un dispositivo de vídeo y se crea un origen de medios.</span><span class="sxs-lookup"><span data-stu-id="7de24-143">The following example takes the symbolic link of a video device and creates a media source.</span></span>


```C++
HRESULT CreateVideoCaptureDevice(PCWSTR *pszSymbolicLink, IMFMediaSource **ppSource)
{
    *ppSource = NULL;
    
    IMFAttributes *pAttributes = NULL;
    IMFMediaSource *pSource = NULL;

    HRESULT hr = MFCreateAttributes(&pAttributes, 2);

    // Set the device type to video.
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetGUID(
            MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE,
            MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_GUID
            );
    }


    // Set the symbolic link.
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetString(
            MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_SYMBOLIC_LINK,
            (LPCWSTR)pszSymbolicLink
            );            
    }

    if (SUCCEEDED(hr))
    {
        hr = MFCreateDeviceSource(pAttributes, ppSource);
    }

    SafeRelease(&pAttributes);
    return hr;    
}
```



<span data-ttu-id="7de24-144">Existe una manera equivalente de crear un dispositivo de audio a partir del identificador de punto de conexión de audio:</span><span class="sxs-lookup"><span data-stu-id="7de24-144">There is an equivalent way to create an audio device from the audio endpoint ID:</span></span>

1.  <span data-ttu-id="7de24-145">Llame a [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) para crear un almacén de atributos.</span><span class="sxs-lookup"><span data-stu-id="7de24-145">Call [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) to create an attribute store.</span></span>
2.  <span data-ttu-id="7de24-146">Establezca el atributo de [tipo de origen del \_ \_ atributo \_ \_ MF DEVSOURCE](mf-devsource-attribute-source-type.md) en el **tipo de origen de atributo MF \_ DEVSOURCE \_ \_ \_ \_ AUDCAP \_ GUID**.</span><span class="sxs-lookup"><span data-stu-id="7de24-146">Set the [MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE](mf-devsource-attribute-source-type.md) attribute to **MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_AUDCAP\_GUID**.</span></span>
3.  <span data-ttu-id="7de24-147">Establezca el atributo de ID. de [ \_ punto de \_ \_ \_ \_ \_ \_ conexión del tipo de origen del atributo MF DEVSOURCE](mf-devsource-attribute-source-type-audcap-endpoint-id.md) en el ID. de extremo.</span><span class="sxs-lookup"><span data-stu-id="7de24-147">Set the [MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_AUDCAP\_ENDPOINT\_ID](mf-devsource-attribute-source-type-audcap-endpoint-id.md) attribute to the endpoint ID.</span></span>
4.  <span data-ttu-id="7de24-148">Llame a la función [**MFCreateDeviceSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource) o [**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate) .</span><span class="sxs-lookup"><span data-stu-id="7de24-148">Call either the [**MFCreateDeviceSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource) or [**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate) function.</span></span>

<span data-ttu-id="7de24-149">En el ejemplo siguiente se toma un identificador de punto de conexión de audio y se crea un origen de medios.</span><span class="sxs-lookup"><span data-stu-id="7de24-149">The following example takes an audio endpoint ID and creates a media source.</span></span>


```C++
HRESULT CreateAudioCaptureDevice(PCWSTR *pszEndPointID, IMFMediaSource **ppSource)
{
    *ppSource = NULL;
    
    IMFAttributes *pAttributes = NULL;
    IMFMediaSource *pSource = NULL;

    HRESULT hr = MFCreateAttributes(&pAttributes, 2);

    // Set the device type to audio.
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetGUID(
            MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE,
            MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_AUDCAP_GUID
            );
    }

    // Set the endpoint ID.
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetString(
            MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_AUDCAP_ENDPOINT_ID,
            (LPCWSTR)pszEndPointID
            ); 
    }

    if (SUCCEEDED(hr))
    {
        hr = MFCreateDeviceSource(pAttributes, ppSource);
    }

    SafeRelease(&pAttributes);
    return hr;    
}
```



## <a name="use-a-capture-device"></a><span data-ttu-id="7de24-150">Uso de un dispositivo de captura</span><span class="sxs-lookup"><span data-stu-id="7de24-150">Use a capture device</span></span>

<span data-ttu-id="7de24-151">Después de crear el origen de medios para un dispositivo de captura, use el [lector de origen](source-reader.md) para obtener datos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7de24-151">After you create the media source for a capture device, use the [Source Reader](source-reader.md) to get data from the device.</span></span> <span data-ttu-id="7de24-152">El lector de origen proporciona ejemplos de medios que contienen los datos de audio de captura o fotogramas de vídeo.</span><span class="sxs-lookup"><span data-stu-id="7de24-152">The Source Reader delivers media samples that contain the capture audio data or video frames.</span></span> <span data-ttu-id="7de24-153">El paso siguiente depende del escenario de la aplicación:</span><span class="sxs-lookup"><span data-stu-id="7de24-153">The next step depends on your application scenario:</span></span>

-   <span data-ttu-id="7de24-154">Vista previa de vídeo: Use Microsoft Direct3D o Direct2D para mostrar el vídeo.</span><span class="sxs-lookup"><span data-stu-id="7de24-154">Video preview: Use Microsoft Direct3D or Direct2D to display the video.</span></span>
-   <span data-ttu-id="7de24-155">Captura de archivo: Use el [escritor de receptor](sink-writer.md) para codificar el archivo.</span><span class="sxs-lookup"><span data-stu-id="7de24-155">File capture: Use the [Sink Writer](sink-writer.md) to encode the file.</span></span>
-   <span data-ttu-id="7de24-156">Vista previa de audio: use [WASAPI](/windows/desktop/CoreAudio/wasapi).</span><span class="sxs-lookup"><span data-stu-id="7de24-156">Audio preview: Use [WASAPI](/windows/desktop/CoreAudio/wasapi).</span></span>

<span data-ttu-id="7de24-157">Si quiere combinar la captura de audio con la captura de vídeo, use el *origen multimedia agregado*.</span><span class="sxs-lookup"><span data-stu-id="7de24-157">If you want to combine audio capture with video capture, use the *aggregate media source*.</span></span> <span data-ttu-id="7de24-158">El origen multimedia agregado contiene una colección de orígenes multimedia y combina todos sus flujos en un solo objeto de origen multimedia.</span><span class="sxs-lookup"><span data-stu-id="7de24-158">The aggregate media source contains a collection of media sources and combines all of their streams into a single media source object.</span></span> <span data-ttu-id="7de24-159">Para crear una instancia del origen multimedia agregado, llame a la función [**MFCreateAggregateSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaggregatesource) .</span><span class="sxs-lookup"><span data-stu-id="7de24-159">To create an instance of the aggregate media source, call the [**MFCreateAggregateSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaggregatesource) function.</span></span>

## <a name="shut-down-the-capture-device"></a><span data-ttu-id="7de24-160">Apagar el dispositivo de captura</span><span class="sxs-lookup"><span data-stu-id="7de24-160">Shut down the capture device</span></span>

<span data-ttu-id="7de24-161">Cuando el dispositivo de captura ya no sea necesario, debe apagar el dispositivo mediante una llamada a [**Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) en el objeto [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) que obtuvo mediante una llamada a [**MFCreateDeviceSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource) o [**IMFActivate:: ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject).</span><span class="sxs-lookup"><span data-stu-id="7de24-161">When the capture device is no longer needed, you must shut down the device by calling [**Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) on the [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) object you obtained by calling [**MFCreateDeviceSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource) or [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject).</span></span> <span data-ttu-id="7de24-162">Si no se llama al **cierre** , pueden producirse vínculos de memoria porque el sistema puede mantener una referencia a los recursos de **IMFMediaSource** hasta que se llama al **cierre** .</span><span class="sxs-lookup"><span data-stu-id="7de24-162">Failure to call **Shutdown** can result in memory links because the system may keep a reference to **IMFMediaSource** resources until **Shutdown** is called.</span></span>


```C++
if (g_pSource)
{
    g_pSource->Shutdown();
    g_pSource->Release();
    g_pSource = NULL;
}
```



<span data-ttu-id="7de24-163">Si ha asignado una cadena que contiene el vínculo simbólico a un dispositivo de captura, también debe liberar este objeto.</span><span class="sxs-lookup"><span data-stu-id="7de24-163">If you allocated a string containing the symbolic link to a capture device, you should release this object as well.</span></span>


```C++
    CoTaskMemFree(g_pwszSymbolicLink);
    g_pwszSymbolicLink = NULL;

    g_cchSymbolicLink = 0;
```



## <a name="related-topics"></a><span data-ttu-id="7de24-164">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7de24-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7de24-165">Captura de audio y vídeo</span><span class="sxs-lookup"><span data-stu-id="7de24-165">Audio/Video Capture</span></span>](audio-video-capture.md)
</dt> </dl>

 

 
