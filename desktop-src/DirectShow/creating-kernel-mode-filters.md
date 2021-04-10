---
description: Crear filtros de Kernel-Mode
ms.assetid: cbc86a5d-c53a-44a0-aa81-5c41527a8f67
title: Crear filtros de Kernel-Mode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c915a08312e33f0e35245325fd8bce7e55e486c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152634"
---
# <a name="creating-kernel-mode-filters"></a><span data-ttu-id="61657-103">Crear filtros de Kernel-Mode</span><span class="sxs-lookup"><span data-stu-id="61657-103">Creating Kernel-Mode Filters</span></span>

<span data-ttu-id="61657-104">Determinados filtros de modo kernel no se pueden crear a través de **CoCreateInstance** y, por tanto, no tienen CLSID.</span><span class="sxs-lookup"><span data-stu-id="61657-104">Certain kernel-mode filters cannot be created through **CoCreateInstance**, and thus do not have CLSIDs.</span></span> <span data-ttu-id="61657-105">Estos filtros incluyen el [convertidor Tee/Sink-to-Sink](tee-sink-to-sink-converter.md), el filtro del [descodificador de CC](cc-decoder-filter.md) y el filtro de [códec elemento WST](wst-codec-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="61657-105">These filters include the [Tee/Sink-to-Sink Converter](tee-sink-to-sink-converter.md), the [CC Decoder](cc-decoder-filter.md) filter, and the [WST Codec](wst-codec-filter.md) filter.</span></span> <span data-ttu-id="61657-106">Para crear uno de estos filtros, use el objeto de [enumerador de dispositivos del sistema](system-device-enumerator.md) y busque por el nombre del filtro.</span><span class="sxs-lookup"><span data-stu-id="61657-106">To create one of these filters, use the [System Device Enumerator](system-device-enumerator.md) object and search by the filter's name.</span></span>

1.  <span data-ttu-id="61657-107">Cree el enumerador de dispositivos del sistema.</span><span class="sxs-lookup"><span data-stu-id="61657-107">Create the System Device Enumerator.</span></span>
2.  <span data-ttu-id="61657-108">Llame al método [**ICreateDevEnum:: CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) con el CLSID de la categoría de filtro para ese filtro.</span><span class="sxs-lookup"><span data-stu-id="61657-108">Call the [**ICreateDevEnum::CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) method with the CLSID of the filter category for that filter.</span></span> <span data-ttu-id="61657-109">Este método crea un enumerador para la categoría de filtro.</span><span class="sxs-lookup"><span data-stu-id="61657-109">This method creates an enumerator for the filter category.</span></span> <span data-ttu-id="61657-110">(Un *enumerador* es simplemente un objeto que devuelve una lista de otros objetos, utilizando una interfaz com definida). El enumerador devuelve punteros **IMoniker** , que representan los filtros de esa categoría.</span><span class="sxs-lookup"><span data-stu-id="61657-110">(An *enumerator* is simply an object that returns a list of other objects, using a defined COM interface.) The enumerator returns **IMoniker** pointers, which represent the filters in that category.</span></span>
3.  <span data-ttu-id="61657-111">Para cada moniker, llame a **IMoniker:: BindToStorage** para obtener una interfaz **IPropertyBag** .</span><span class="sxs-lookup"><span data-stu-id="61657-111">For each moniker, call **IMoniker::BindToStorage** to get an **IPropertyBag** interface.</span></span>
4.  <span data-ttu-id="61657-112">Llame a **IPropertyBag:: Read** para obtener el nombre del filtro.</span><span class="sxs-lookup"><span data-stu-id="61657-112">Call **IPropertyBag::Read** to get the name of the filter.</span></span>
5.  <span data-ttu-id="61657-113">Si el nombre coincide, llame a **IMoniker:: BindToObject** para crear el filtro.</span><span class="sxs-lookup"><span data-stu-id="61657-113">If the name matches, call **IMoniker::BindToObject** to create the filter.</span></span>

<span data-ttu-id="61657-114">En el código siguiente se muestra una función que realiza estos pasos:</span><span class="sxs-lookup"><span data-stu-id="61657-114">The following code shows a function that performs these steps:</span></span>


```C++
HRESULT CreateKernelFilter(
    const GUID &guidCategory,  // Filter category.
    LPCOLESTR szName,          // The name of the filter.
    IBaseFilter **ppFilter     // Receives a pointer to the filter.
)
{
    HRESULT hr;
    ICreateDevEnum *pDevEnum = NULL;
    IEnumMoniker *pEnum = NULL;
    if (!szName || !ppFilter) 
    {
        return E_POINTER;
    }

    // Create the system device enumerator.
    hr = CoCreateInstance(CLSID_SystemDeviceEnum, NULL, CLSCTX_INPROC,
        IID_ICreateDevEnum, (void**)&pDevEnum);
    if (FAILED(hr))
    {
        return hr;
    }

    // Create a class enumerator for the specified category.
    hr = pDevEnum->CreateClassEnumerator(guidCategory, &pEnum, 0);
    pDevEnum->Release();
    if (hr != S_OK) // S_FALSE means the category is empty.
    {
        return E_FAIL;
    }

    // Enumerate devices within this category.
    bool bFound = false;
    IMoniker *pMoniker;
    while (!bFound && (S_OK == pEnum->Next(1, &pMoniker, 0)))
    {
        IPropertyBag *pBag = NULL;
        hr = pMoniker->BindToStorage(0, 0, IID_IPropertyBag, (void **)&pBag);
        if (FAILED(hr))
        {
            pMoniker->Release();
            continue; // Maybe the next one will work.
        }
        // Check the friendly name.
        VARIANT var;
        VariantInit(&var);
        hr = pBag->Read(L"FriendlyName", &var, NULL);
        if (SUCCEEDED(hr) && (lstrcmpiW(var.bstrVal, szName) == 0))
        {
            // This is the right filter.
            hr = pMoniker->BindToObject(0, 0, IID_IBaseFilter,
                (void**)ppFilter);
            bFound = true;
        }
        VariantClear(&var);
        pBag->Release();
        pMoniker->Release();
    }
    pEnum->Release();
    return (bFound ? hr : E_FAIL);
}
```



<span data-ttu-id="61657-115">En el ejemplo de código siguiente se usa esta función para crear el filtro del descodificador de CC y agregarlo al gráfico de filtros:</span><span class="sxs-lookup"><span data-stu-id="61657-115">The following code example uses this function to create the CC Decoder filter and add it to the filter graph:</span></span>


```C++
IBaseFilter *pCC = NULL;
hr = CreateKernelFilter(AM_KSCATEGORY_VBICODEC, 
    OLESTR("CC Decoder"), &pCC);
if (SUCCEEDED(hr))
{
    hr = pGraph->AddFilter(pCC, L"CC Decoder");
    pCC->Release();
}
```



## <a name="related-topics"></a><span data-ttu-id="61657-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="61657-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="61657-117">Temas de captura avanzada</span><span class="sxs-lookup"><span data-stu-id="61657-117">Advanced Capture Topics</span></span>](advanced-capture-topics.md)
</dt> <dt>

[<span data-ttu-id="61657-118">Usar el enumerador de dispositivos del sistema</span><span class="sxs-lookup"><span data-stu-id="61657-118">Using the System Device Enumerator</span></span>](using-the-system-device-enumerator.md)
</dt> </dl>

 

 



