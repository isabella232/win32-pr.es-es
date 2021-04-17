---
description: Selección de un dispositivo de captura
ms.assetid: 8f92873d-569a-48af-a913-6d4cce65640f
title: Selección de un dispositivo de captura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b599728c6bd2d98b89285b6008923aa4fb2a3aef
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105686324"
---
# <a name="selecting-a-capture-device"></a><span data-ttu-id="b494b-103">Selección de un dispositivo de captura</span><span class="sxs-lookup"><span data-stu-id="b494b-103">Selecting a Capture Device</span></span>

<span data-ttu-id="b494b-104">Para seleccionar un dispositivo de captura de audio o vídeo, use el [enumerador de dispositivos del sistema](system-device-enumerator.md), que se describe en el tema [uso del enumerador de dispositivos del sistema](using-the-system-device-enumerator.md).</span><span class="sxs-lookup"><span data-stu-id="b494b-104">To select an audio or video capture device, use the [System Device Enumerator](system-device-enumerator.md), described in the topic [Using the System Device Enumerator](using-the-system-device-enumerator.md).</span></span> <span data-ttu-id="b494b-105">El enumerador de dispositivos de sistema devuelve una colección de monikers de dispositivo, seleccionados por categoría de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b494b-105">The System Device Enumerator returns a collection of device monikers, selected by device category.</span></span> <span data-ttu-id="b494b-106">Un *moniker* es un objeto com que contiene información sobre otro objeto.</span><span class="sxs-lookup"><span data-stu-id="b494b-106">A *moniker* is a COM object that contains information about another object.</span></span> <span data-ttu-id="b494b-107">Los monikers permiten a la aplicación obtener información sobre un objeto sin crear realmente el objeto.</span><span class="sxs-lookup"><span data-stu-id="b494b-107">Monikers enable the application to get information about an object without actually creating the object.</span></span> <span data-ttu-id="b494b-108">Posteriormente, la aplicación puede utilizar el moniker para crear el objeto.</span><span class="sxs-lookup"><span data-stu-id="b494b-108">Later, the application can use the moniker to create the object.</span></span> <span data-ttu-id="b494b-109">Para obtener más información acerca de los monikers, vea la documentación de [**IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker).</span><span class="sxs-lookup"><span data-stu-id="b494b-109">For more information about monikers, see the documentation for [**IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker).</span></span>

<span data-ttu-id="b494b-110">Para usar el enumerador de dispositivos del sistema, realice los pasos siguientes.</span><span class="sxs-lookup"><span data-stu-id="b494b-110">To use the System Device Enumerator, perform the following steps.</span></span>

1.  <span data-ttu-id="b494b-111">Llame a [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para crear una instancia del enumerador de dispositivos del sistema.</span><span class="sxs-lookup"><span data-stu-id="b494b-111">Call [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to create an instance of the System Device Enumerator.</span></span>
2.  <span data-ttu-id="b494b-112">Llame a [**ICreateDevEnum:: CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) y especifique la categoría de dispositivo como un GUID.</span><span class="sxs-lookup"><span data-stu-id="b494b-112">Call [**ICreateDevEnum::CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) and specify the device category as a GUID.</span></span> <span data-ttu-id="b494b-113">En el caso de los dispositivos de captura, las siguientes categorías son relevantes.</span><span class="sxs-lookup"><span data-stu-id="b494b-113">For capture devices, the following categories are relevant.</span></span> 

    | <span data-ttu-id="b494b-114">GUID de categoría</span><span class="sxs-lookup"><span data-stu-id="b494b-114">Category GUID</span></span>                       | <span data-ttu-id="b494b-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="b494b-115">Description</span></span>           |
    |-------------------------------------|-----------------------|
    | <span data-ttu-id="b494b-116">**CLSID \_ AudioInputDeviceCategory**</span><span class="sxs-lookup"><span data-stu-id="b494b-116">**CLSID\_AudioInputDeviceCategory**</span></span> | <span data-ttu-id="b494b-117">Dispositivos de captura de audio</span><span class="sxs-lookup"><span data-stu-id="b494b-117">Audio capture devices</span></span> |
    | <span data-ttu-id="b494b-118">**CLSID \_ VideoInputDeviceCategory**</span><span class="sxs-lookup"><span data-stu-id="b494b-118">**CLSID\_VideoInputDeviceCategory**</span></span> | <span data-ttu-id="b494b-119">Dispositivos de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="b494b-119">Video capture devices</span></span> |

    

     

    <span data-ttu-id="b494b-120">Si una cámara de vídeo tiene un micrófono integrado, aparece en ambas categorías.</span><span class="sxs-lookup"><span data-stu-id="b494b-120">If a video camera has an integrated microphone, it appears in both categories.</span></span> <span data-ttu-id="b494b-121">Sin embargo, la cámara y el micrófono se tratan como dispositivos independientes por el sistema, para la enumeración, la creación de dispositivos y el streaming de datos.</span><span class="sxs-lookup"><span data-stu-id="b494b-121">However, the camera and microphone are treated as separate devices by the system, for purposes of enumeration, device creation, and data streaming.</span></span>

3.  <span data-ttu-id="b494b-122">El método [**CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) devuelve un puntero a la interfaz [**IEnumMoniker**](/windows/win32/api/objidl/nn-objidl-ienummoniker) .</span><span class="sxs-lookup"><span data-stu-id="b494b-122">The [**CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) method returns a pointer to the [**IEnumMoniker**](/windows/win32/api/objidl/nn-objidl-ienummoniker) interface.</span></span> <span data-ttu-id="b494b-123">Para enumerar los monikers, llame a [**IEnumMoniker:: Next**](/windows/win32/api/objidl/nf-objidl-ienummoniker-next).</span><span class="sxs-lookup"><span data-stu-id="b494b-123">To enumerate the monikers, call [**IEnumMoniker::Next**](/windows/win32/api/objidl/nf-objidl-ienummoniker-next).</span></span>

<span data-ttu-id="b494b-124">En el código siguiente se crea un enumerador para una categoría de dispositivo especificada.</span><span class="sxs-lookup"><span data-stu-id="b494b-124">The following code creates an enumerator for a specified device category.</span></span>


```C++
#include <windows.h>
#include <dshow.h>

#pragma comment(lib, "strmiids")

HRESULT EnumerateDevices(REFGUID category, IEnumMoniker **ppEnum)
{
    // Create the System Device Enumerator.
    ICreateDevEnum *pDevEnum;
    HRESULT hr = CoCreateInstance(CLSID_SystemDeviceEnum, NULL,  
        CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pDevEnum));

    if (SUCCEEDED(hr))
    {
        // Create an enumerator for the category.
        hr = pDevEnum->CreateClassEnumerator(category, ppEnum, 0);
        if (hr == S_FALSE)
        {
            hr = VFW_E_NOT_FOUND;  // The category is empty. Treat as an error.
        }
        pDevEnum->Release();
    }
    return hr;
}
```



<span data-ttu-id="b494b-125">La interfaz [**IEnumMoniker**](/windows/win32/api/objidl/nn-objidl-ienummoniker) enumera una lista de interfaces [**IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker) , cada una de las cuales representa un moniker de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b494b-125">The [**IEnumMoniker**](/windows/win32/api/objidl/nn-objidl-ienummoniker) interface enumerates a list of [**IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker) interfaces, each of which represents a device moniker.</span></span> <span data-ttu-id="b494b-126">La aplicación puede leer propiedades del moniker o utilizar el moniker para crear un filtro de captura de DirectShow para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b494b-126">The application can read properties from the moniker, or use the moniker to create a DirectShow capture filter for the device.</span></span> <span data-ttu-id="b494b-127">Las propiedades de moniker se devuelven como valores **Variant** .</span><span class="sxs-lookup"><span data-stu-id="b494b-127">Moniker properties are returned as **VARIANT** values.</span></span> <span data-ttu-id="b494b-128">Los monikers de dispositivo admiten las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="b494b-128">The following properties are supported by device monikers.</span></span>



| <span data-ttu-id="b494b-129">Propiedad</span><span class="sxs-lookup"><span data-stu-id="b494b-129">Property</span></span>       | <span data-ttu-id="b494b-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="b494b-130">Description</span></span>                                                               | <span data-ttu-id="b494b-131">Tipo de VARIANTE</span><span class="sxs-lookup"><span data-stu-id="b494b-131">VARIANT Type</span></span> |
|----------------|---------------------------------------------------------------------------|--------------|
| <span data-ttu-id="b494b-132">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="b494b-132">"FriendlyName"</span></span> | <span data-ttu-id="b494b-133">Nombre del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b494b-133">The name of the device.</span></span>                                                   | <span data-ttu-id="b494b-134">**VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="b494b-134">**VT\_BSTR**</span></span> |
| <span data-ttu-id="b494b-135">Denominación</span><span class="sxs-lookup"><span data-stu-id="b494b-135">"Description"</span></span>  | <span data-ttu-id="b494b-136">Una descripción del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b494b-136">A description of the device.</span></span>                                              | <span data-ttu-id="b494b-137">**VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="b494b-137">**VT\_BSTR**</span></span> |
| <span data-ttu-id="b494b-138">DevicePath</span><span class="sxs-lookup"><span data-stu-id="b494b-138">"DevicePath"</span></span>   | <span data-ttu-id="b494b-139">Cadena única que identifica el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b494b-139">A unique string that identifies the device.</span></span> <span data-ttu-id="b494b-140">(Solo dispositivos de captura de vídeo).</span><span class="sxs-lookup"><span data-stu-id="b494b-140">(Video capture devices only.)</span></span> | <span data-ttu-id="b494b-141">**VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="b494b-141">**VT\_BSTR**</span></span> |
| <span data-ttu-id="b494b-142">"WaveInID"</span><span class="sxs-lookup"><span data-stu-id="b494b-142">"WaveInID"</span></span>     | <span data-ttu-id="b494b-143">Identificador de un dispositivo de captura de audio.</span><span class="sxs-lookup"><span data-stu-id="b494b-143">The identifier for an audio capture device.</span></span> <span data-ttu-id="b494b-144">(Solo dispositivos de captura de audio).</span><span class="sxs-lookup"><span data-stu-id="b494b-144">(Audio capture devices only.)</span></span> | <span data-ttu-id="b494b-145">**VT \_ I4**</span><span class="sxs-lookup"><span data-stu-id="b494b-145">**VT\_I4**</span></span>   |



 

<span data-ttu-id="b494b-146">Las propiedades "FriendlyName" y "Description" son adecuadas para mostrar en una interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="b494b-146">The "FriendlyName" and "Description" properties are suitable for displaying in a UI.</span></span>

-   <span data-ttu-id="b494b-147">La propiedad "FriendlyName" está disponible para todos los dispositivos.</span><span class="sxs-lookup"><span data-stu-id="b494b-147">The "FriendlyName" property is available for every device.</span></span> <span data-ttu-id="b494b-148">Contiene un nombre legible para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b494b-148">It contains a human-readable name for the device.</span></span>
-   <span data-ttu-id="b494b-149">La propiedad "Description" solo está disponible para los dispositivos DV y D-VHS/MPEG camcorder.</span><span class="sxs-lookup"><span data-stu-id="b494b-149">The "Description" property is available only for DV and D-VHS/MPEG camcorder devices.</span></span> <span data-ttu-id="b494b-150">Para obtener más información, consulte [controlador MSDV](msdv-driver.md) y [controlador MSTape](mstape-driver.md).</span><span class="sxs-lookup"><span data-stu-id="b494b-150">For more information, see [MSDV Driver](msdv-driver.md) and [MSTape Driver](mstape-driver.md).</span></span> <span data-ttu-id="b494b-151">Si está disponible, contiene una descripción del dispositivo que es más específica que la propiedad "FriendlyName".</span><span class="sxs-lookup"><span data-stu-id="b494b-151">If available, it contains a description of the device which is more specific than the "FriendlyName" property.</span></span> <span data-ttu-id="b494b-152">Normalmente incluye el nombre del proveedor.</span><span class="sxs-lookup"><span data-stu-id="b494b-152">Typically it includes the vendor name.</span></span>
-   <span data-ttu-id="b494b-153">La propiedad "DevicePath" no es una cadena legible para el usuario, pero se garantiza que sea única para cada dispositivo de captura de vídeo en el sistema.</span><span class="sxs-lookup"><span data-stu-id="b494b-153">The "DevicePath" property is not a human-readable string, but is guaranteed to be unique for each video capture device on the system.</span></span> <span data-ttu-id="b494b-154">Puede usar esta propiedad para distinguir entre dos o más instancias del mismo modelo de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b494b-154">You can use this property to distinguish between two or more instances of the same model of device.</span></span>
-   <span data-ttu-id="b494b-155">Si la propiedad "WaveInID" está presente, significa que el filtro de captura de DirectShow usa internamente las API de audio de forma de [onda](../multimedia/waveform-audio.md) para comunicarse con el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b494b-155">If the "WaveInID" property is present, it means the DirectShow capture filter uses the [Waveform Audio](../multimedia/waveform-audio.md) APIs internally to communicate with the device.</span></span> <span data-ttu-id="b494b-156">El valor de la propiedad "WaveInID" corresponde al identificador usado por las funciones \**Wave \** _, como [_ *waveInOpen* \*](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen).</span><span class="sxs-lookup"><span data-stu-id="b494b-156">The value of the "WaveInID" property corresponds to the identifier used by the \**waveIn\** _ functions, such as [_ *waveInOpen*\*](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen).</span></span>

<span data-ttu-id="b494b-157">Para leer las propiedades del moniker, realice los pasos siguientes.</span><span class="sxs-lookup"><span data-stu-id="b494b-157">To read properties from the moniker, perform the following steps.</span></span>

1.  <span data-ttu-id="b494b-158">Llame a [**IMoniker:: BindToStorage**](/windows/win32/api/objidl/nf-objidl-imoniker-bindtostorage) para obtener un puntero a la interfaz [**IPropertyBag**](../com/ipropertybag-and-ipersistpropertybag.md) .</span><span class="sxs-lookup"><span data-stu-id="b494b-158">Call [**IMoniker::BindToStorage**](/windows/win32/api/objidl/nf-objidl-imoniker-bindtostorage) to get a pointer to the [**IPropertyBag**](../com/ipropertybag-and-ipersistpropertybag.md) interface.</span></span>
2.  <span data-ttu-id="b494b-159">Llame a **IPropertyBag:: Read** para leer la propiedad.</span><span class="sxs-lookup"><span data-stu-id="b494b-159">Call **IPropertyBag::Read** to read the property.</span></span>

<span data-ttu-id="b494b-160">En el ejemplo de código siguiente se muestra cómo enumerar una lista de monikers de dispositivo y obtener las propiedades.</span><span class="sxs-lookup"><span data-stu-id="b494b-160">The following code example shows how to enumerate a list of device monikers and get the properties.</span></span>


```C++
void DisplayDeviceInformation(IEnumMoniker *pEnum)
{
    IMoniker *pMoniker = NULL;

    while (pEnum->Next(1, &pMoniker, NULL) == S_OK)
    {
        IPropertyBag *pPropBag;
        HRESULT hr = pMoniker->BindToStorage(0, 0, IID_PPV_ARGS(&pPropBag));
        if (FAILED(hr))
        {
            pMoniker->Release();
            continue;  
        } 

        VARIANT var;
        VariantInit(&var);

        // Get description or friendly name.
        hr = pPropBag->Read(L"Description", &var, 0);
        if (FAILED(hr))
        {
            hr = pPropBag->Read(L"FriendlyName", &var, 0);
        }
        if (SUCCEEDED(hr))
        {
            printf("%S\n", var.bstrVal);
            VariantClear(&var); 
        }

        hr = pPropBag->Write(L"FriendlyName", &var);

        // WaveInID applies only to audio capture devices.
        hr = pPropBag->Read(L"WaveInID", &var, 0);
        if (SUCCEEDED(hr))
        {
            printf("WaveIn ID: %d\n", var.lVal);
            VariantClear(&var); 
        }

        hr = pPropBag->Read(L"DevicePath", &var, 0);
        if (SUCCEEDED(hr))
        {
            // The device path is not intended for display.
            printf("Device path: %S\n", var.bstrVal);
            VariantClear(&var); 
        }

        pPropBag->Release();
        pMoniker->Release();
    }
}

void main()
{
    HRESULT hr = CoInitializeEx(NULL, COINIT_MULTITHREADED);
    if (SUCCEEDED(hr))
    {
        IEnumMoniker *pEnum;

        hr = EnumerateDevices(CLSID_VideoInputDeviceCategory, &pEnum);
        if (SUCCEEDED(hr))
        {
            DisplayDeviceInformation(pEnum);
            pEnum->Release();
        }
        hr = EnumerateDevices(CLSID_AudioInputDeviceCategory, &pEnum);
        if (SUCCEEDED(hr))
        {
            DisplayDeviceInformation(pEnum);
            pEnum->Release();
        }
        CoUninitialize();
    }
}
```



<span data-ttu-id="b494b-161">Para crear un filtro de captura de DirectShow para el dispositivo, llame al método [**IMoniker:: BindToObject**](/windows/win32/api/objidl/nf-objidl-imoniker-bindtoobject) para obtener un puntero [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) .</span><span class="sxs-lookup"><span data-stu-id="b494b-161">To create a DirectShow capture filter for the device, call the [**IMoniker::BindToObject**](/windows/win32/api/objidl/nf-objidl-imoniker-bindtoobject) method to get an [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) pointer.</span></span> <span data-ttu-id="b494b-162">A continuación, llame a [**IFilterGraph:: addFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) para agregar el filtro al gráfico de filtro:</span><span class="sxs-lookup"><span data-stu-id="b494b-162">Then call [**IFilterGraph::AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) to add the filter to the filter graph:</span></span>


```C++
IBaseFilter *pCap = NULL;
hr = pMoniker->BindToObject(0, 0, IID_IBaseFilter, (void**)&pCap);
if (SUCCEEDED(hr))
{
    hr = m_pGraph->AddFilter(pCap, L"Capture Filter");
}
```



## <a name="related-topics"></a><span data-ttu-id="b494b-163">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b494b-163">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b494b-164">Captura de audio</span><span class="sxs-lookup"><span data-stu-id="b494b-164">Audio Capture</span></span>](audio-capture.md)
</dt> <dt>

[<span data-ttu-id="b494b-165">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="b494b-165">Video Capture</span></span>](video-capture.md)
</dt> </dl>

 

 
