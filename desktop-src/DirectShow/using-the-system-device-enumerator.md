---
description: Usar el enumerador de dispositivos del sistema
ms.assetid: 70db139c-2c5b-4574-bec3-dfe758b16715
title: Usar el enumerador de dispositivos del sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88f8f66cb64e9f7bb51d6b0716b9fa23cf531435
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104568640"
---
# <a name="using-the-system-device-enumerator"></a><span data-ttu-id="a8df1-103">Usar el enumerador de dispositivos del sistema</span><span class="sxs-lookup"><span data-stu-id="a8df1-103">Using the System Device Enumerator</span></span>

<span data-ttu-id="a8df1-104">El enumerador de dispositivos del sistema proporciona una manera uniforme de enumerar, por categoría, los filtros registrados en el sistema de un usuario.</span><span class="sxs-lookup"><span data-stu-id="a8df1-104">The System Device Enumerator provides a uniform way to enumerate, by category, the filters registered on a user's system.</span></span> <span data-ttu-id="a8df1-105">Además, distingue entre dispositivos de hardware individuales, aunque el mismo filtro los admita.</span><span class="sxs-lookup"><span data-stu-id="a8df1-105">Moreover, it differentiates between individual hardware devices, even if the same filter supports them.</span></span> <span data-ttu-id="a8df1-106">Esto es especialmente útil para los dispositivos que usan el Modelo de controlador de Windows (WDM) y el filtro KSProxy.</span><span class="sxs-lookup"><span data-stu-id="a8df1-106">This is particularly useful for devices that use the Windows Driver Model (WDM) and the KSProxy filter.</span></span> <span data-ttu-id="a8df1-107">Por ejemplo, el usuario puede tener varios dispositivos de captura de vídeo WDM, todos compatibles con el mismo filtro.</span><span class="sxs-lookup"><span data-stu-id="a8df1-107">For example, the user might have several WDM video capture devices, all supported by the same filter.</span></span> <span data-ttu-id="a8df1-108">El enumerador de dispositivos del sistema los trata como instancias de dispositivo independientes.</span><span class="sxs-lookup"><span data-stu-id="a8df1-108">The System Device Enumerator treats them as separate device instances.</span></span>

<span data-ttu-id="a8df1-109">El enumerador de dispositivos del sistema funciona mediante la creación de un enumerador para una categoría específica, como la captura de audio o la compresión de vídeo.</span><span class="sxs-lookup"><span data-stu-id="a8df1-109">The System Device Enumerator works by creating an enumerator for a specific category, such as audio capture or video compression.</span></span> <span data-ttu-id="a8df1-110">El enumerador de categoría devuelve un moniker único para cada dispositivo de la categoría.</span><span class="sxs-lookup"><span data-stu-id="a8df1-110">The category enumerator returns a unique moniker for each device in the category.</span></span> <span data-ttu-id="a8df1-111">El enumerador de categoría incluye automáticamente los dispositivos Plug and Play relevantes de la categoría.</span><span class="sxs-lookup"><span data-stu-id="a8df1-111">The category enumerator automatically includes any relevant Plug and Play devices in the category.</span></span> <span data-ttu-id="a8df1-112">Para obtener una lista de categorías, vea [filtrar categorías](filter-categories.md).</span><span class="sxs-lookup"><span data-stu-id="a8df1-112">For a list of categories, see [Filter Categories](filter-categories.md).</span></span>

<span data-ttu-id="a8df1-113">Para usar el enumerador de dispositivos del sistema, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="a8df1-113">To use the System Device Enumerator, do the following:</span></span>

1.  <span data-ttu-id="a8df1-114">Cree el enumerador de dispositivos del sistema llamando a **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="a8df1-114">Create the system device enumerator by calling **CoCreateInstance**.</span></span> <span data-ttu-id="a8df1-115">El identificador de clase (CLSID) es CLSID \_ SystemDeviceEnum.</span><span class="sxs-lookup"><span data-stu-id="a8df1-115">The class identifier (CLSID) is CLSID\_SystemDeviceEnum.</span></span>
2.  <span data-ttu-id="a8df1-116">Obtenga un enumerador de categoría mediante una llamada a [**ICreateDevEnum:: CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) con el CLSID de la categoría deseada.</span><span class="sxs-lookup"><span data-stu-id="a8df1-116">Obtain a category enumerator by calling [**ICreateDevEnum::CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) with the CLSID of the desired category.</span></span> <span data-ttu-id="a8df1-117">Este método devuelve un puntero de interfaz **IEnumMoniker** .</span><span class="sxs-lookup"><span data-stu-id="a8df1-117">This method returns an **IEnumMoniker** interface pointer.</span></span> <span data-ttu-id="a8df1-118">Si la categoría está vacía (o no existe), el método devuelve S \_ false en lugar de un código de error.</span><span class="sxs-lookup"><span data-stu-id="a8df1-118">If the category is empty (or does not exist), the method returns S\_FALSE rather than an error code.</span></span> <span data-ttu-id="a8df1-119">Si es así, el puntero de **IEnumMoniker** devuelto es **null** y al desreferenciarlo se producirá una excepción.</span><span class="sxs-lookup"><span data-stu-id="a8df1-119">If so, the returned **IEnumMoniker** pointer is **NULL** and dereferencing it will cause an exception.</span></span> <span data-ttu-id="a8df1-120">Por lo tanto, pruebe explícitamente \_ si es correcto cuando llame a **CreateClassEnumerator**, en lugar de llamar a la macro con **éxito** habitual.</span><span class="sxs-lookup"><span data-stu-id="a8df1-120">Therefore, explicitly test for S\_OK when you call **CreateClassEnumerator**, instead of calling the usual **SUCCEEDED** macro.</span></span>
3.  <span data-ttu-id="a8df1-121">Use el método **IEnumMoniker:: Next** para enumerar cada moniker.</span><span class="sxs-lookup"><span data-stu-id="a8df1-121">Use the **IEnumMoniker::Next** method to enumerate each moniker.</span></span> <span data-ttu-id="a8df1-122">Este método devuelve un puntero de interfaz **IMoniker** .</span><span class="sxs-lookup"><span data-stu-id="a8df1-122">This method returns an **IMoniker** interface pointer.</span></span> <span data-ttu-id="a8df1-123">Cuando el método **siguiente** alcanza el final de la enumeración, también devuelve s \_ false, de modo que se comprueba de nuevo si hay un valor \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="a8df1-123">When the **Next** method reaches the end of the enumeration, it also returns S\_FALSE, so again check for S\_OK.</span></span>
4.  <span data-ttu-id="a8df1-124">Para recuperar el nombre descriptivo del dispositivo (por ejemplo, para mostrarlo en la interfaz de usuario), llame al método **IMoniker:: BindToStorage** .</span><span class="sxs-lookup"><span data-stu-id="a8df1-124">To retrieve the friendly name of the device (for example, to display in the user interface), call the **IMoniker::BindToStorage** method.</span></span>
5.  <span data-ttu-id="a8df1-125">Para crear e inicializar el filtro de DirectShow que administra el dispositivo, llame a **IMoniker:: BindToObject** en el moniker.</span><span class="sxs-lookup"><span data-stu-id="a8df1-125">To create and initialize the DirectShow filter that manages the device, call **IMoniker::BindToObject** on the moniker.</span></span> <span data-ttu-id="a8df1-126">Llame a [**IFilterGraph:: addFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) para agregar el filtro al gráfico.</span><span class="sxs-lookup"><span data-stu-id="a8df1-126">Call [**IFilterGraph::AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) to add the filter to the graph.</span></span>

<span data-ttu-id="a8df1-127">En el siguiente diagrama se muestra este proceso.</span><span class="sxs-lookup"><span data-stu-id="a8df1-127">The following diagram illustrates this process.</span></span>

![enumerar dispositivos](images/sysdevenum.png)

<span data-ttu-id="a8df1-129">En el ejemplo siguiente se muestra cómo enumerar los compresores de vídeo instalados en el sistema del usuario.</span><span class="sxs-lookup"><span data-stu-id="a8df1-129">The following example shows how to enumerate the video compressors installed on the user's system.</span></span> <span data-ttu-id="a8df1-130">Por motivos de brevedad, en el ejemplo se realiza una comprobación de errores mínima.</span><span class="sxs-lookup"><span data-stu-id="a8df1-130">For brevity, the example performs minimal error checking.</span></span>


```C++
// Create the System Device Enumerator.
HRESULT hr;
ICreateDevEnum *pSysDevEnum = NULL;
hr = CoCreateInstance(CLSID_SystemDeviceEnum, NULL, CLSCTX_INPROC_SERVER,
    IID_ICreateDevEnum, (void **)&pSysDevEnum);
if (FAILED(hr))
{
    return hr;
}

// Obtain a class enumerator for the video compressor category.
IEnumMoniker *pEnumCat = NULL;
hr = pSysDevEnum->CreateClassEnumerator(CLSID_VideoCompressorCategory, &pEnumCat, 0);

if (hr == S_OK) 
{
    // Enumerate the monikers.
    IMoniker *pMoniker = NULL;
    ULONG cFetched;
    while(pEnumCat->Next(1, &pMoniker, &cFetched) == S_OK)
    {
        IPropertyBag *pPropBag;
        hr = pMoniker->BindToStorage(0, 0, IID_IPropertyBag, 
            (void **)&pPropBag);
        if (SUCCEEDED(hr))
        {
            // To retrieve the filter's friendly name, do the following:
            VARIANT varName;
            VariantInit(&varName);
            hr = pPropBag->Read(L"FriendlyName", &varName, 0);
            if (SUCCEEDED(hr))
            {
                // Display the name in your UI somehow.
            }
            VariantClear(&varName);

            // To create an instance of the filter, do the following:
            IBaseFilter *pFilter;
            hr = pMoniker->BindToObject(NULL, NULL, IID_IBaseFilter,
                (void**)&pFilter);
            // Now add the filter to the graph. 
            //Remember to release pFilter later.
            pPropBag->Release();
        }
        pMoniker->Release();
    }
    pEnumCat->Release();
}
pSysDevEnum->Release();
```



<span data-ttu-id="a8df1-131">**Monikers de dispositivo**</span><span class="sxs-lookup"><span data-stu-id="a8df1-131">**Device Monikers**</span></span>

<span data-ttu-id="a8df1-132">En el caso de los monikers de dispositivo, puede pasar el moniker al método [**IFilterGraph2:: AddSourceFilterForMoniker**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph2-addsourcefilterformoniker) para crear un filtro de captura para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a8df1-132">For device monikers, you can pass the moniker to the [**IFilterGraph2::AddSourceFilterForMoniker**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph2-addsourcefilterformoniker) method to create a capture filter for the device.</span></span> <span data-ttu-id="a8df1-133">Para ver el código de ejemplo, consulte la documentación de ese método.</span><span class="sxs-lookup"><span data-stu-id="a8df1-133">For example code, see the documentation for that method.</span></span>

<span data-ttu-id="a8df1-134">El método **IMoniker:: getDisplayName** devuelve el nombre para mostrar del moniker.</span><span class="sxs-lookup"><span data-stu-id="a8df1-134">The **IMoniker::GetDisplayName** method returns the display name of the moniker.</span></span> <span data-ttu-id="a8df1-135">Aunque el nombre para mostrar se puede leer, normalmente no se muestra a un usuario final.</span><span class="sxs-lookup"><span data-stu-id="a8df1-135">Although the display name is readable, you would not typically display it to an end-user.</span></span> <span data-ttu-id="a8df1-136">En su lugar, obtenga el nombre descriptivo del contenedor de propiedades, como se ha descrito anteriormente.</span><span class="sxs-lookup"><span data-stu-id="a8df1-136">Get the friendly name from the property bag instead, as described previously.</span></span>

<span data-ttu-id="a8df1-137">El método **IMoniker::P arsedisplayname** o la función **MkParseDisplayName** se pueden usar para crear un moniker de dispositivo predeterminado para una categoría de filtro determinada.</span><span class="sxs-lookup"><span data-stu-id="a8df1-137">The **IMoniker::ParseDisplayName** method or the **MkParseDisplayName** function can be used to create a default device moniker for a given filter category.</span></span> <span data-ttu-id="a8df1-138">Use un nombre para mostrar con el formato `@device:*:{category-clsid}` , donde `category-clsid` es la representación de cadena del GUID de categoría.</span><span class="sxs-lookup"><span data-stu-id="a8df1-138">Use a display name with the form `@device:*:{category-clsid}`, where `category-clsid` is the string representation of the category GUID.</span></span> <span data-ttu-id="a8df1-139">El moniker predeterminado es el primer moniker devuelto por el enumerador de dispositivos de esa categoría.</span><span class="sxs-lookup"><span data-stu-id="a8df1-139">The default moniker is the first moniker returned by the device enumerator for that category.</span></span>

 

 



