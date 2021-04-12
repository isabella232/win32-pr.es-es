---
description: Elección de un filtro de compresión
ms.assetid: 9a2c3c48-771e-44db-a042-3db0fd9a6c76
title: Elección de un filtro de compresión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a64ebebf41c35ed6aed9ab47d853c03ba720a31
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152666"
---
# <a name="choosing-a-compression-filter"></a><span data-ttu-id="239df-103">Elección de un filtro de compresión</span><span class="sxs-lookup"><span data-stu-id="239df-103">Choosing a Compression Filter</span></span>

<span data-ttu-id="239df-104">Varios tipos de componentes de software pueden realizar compresión de audio o vídeo, como:</span><span class="sxs-lookup"><span data-stu-id="239df-104">Several types of software components can perform video or audio compression, such as:</span></span>

-   <span data-ttu-id="239df-105">Filtros de DirectShow nativos</span><span class="sxs-lookup"><span data-stu-id="239df-105">Native DirectShow filters</span></span>
-   <span data-ttu-id="239df-106">Códecs del administrador de compresión de vídeo (VCM)</span><span class="sxs-lookup"><span data-stu-id="239df-106">Video Compression Manager (VCM) codecs</span></span>
-   <span data-ttu-id="239df-107">Códecs del administrador de compresión de audio (ACM)</span><span class="sxs-lookup"><span data-stu-id="239df-107">Audio Compression Manager (ACM) codecs</span></span>
-   <span data-ttu-id="239df-108">Objetos multimedia de DirectX (DMOs)</span><span class="sxs-lookup"><span data-stu-id="239df-108">DirectX Media Objects (DMOs)</span></span>

<span data-ttu-id="239df-109">En DirectShow, los códecs VCM están incluidos en el [filtro del compresor AVI](avi-compressor-filter.md)y los códecs ACM se incluyen en el [filtro contenedor ACM](acm-wrapper-filter.md).</span><span class="sxs-lookup"><span data-stu-id="239df-109">In DirectShow, VCM codecs are wrapped by the [AVI Compressor Filter](avi-compressor-filter.md), and ACM codecs are wrapped by the [ACM Wrapper Filter](acm-wrapper-filter.md).</span></span> <span data-ttu-id="239df-110">Los DMOs se ajustan mediante el [filtro de contenedor de DMO](dmo-wrapper-filter.md).</span><span class="sxs-lookup"><span data-stu-id="239df-110">DMOs are wrapped by the [DMO Wrapper Filter](dmo-wrapper-filter.md).</span></span> <span data-ttu-id="239df-111">El enumerador de dispositivos del sistema proporciona una manera coherente de enumerar y crear cualquiera de estos tipos de compresores, sin preocuparse por el modelo subyacente.</span><span class="sxs-lookup"><span data-stu-id="239df-111">The system device enumerator provides a consistent way to enumerate and create any of these compressor types, without worrying about the underlying model.</span></span>

<span data-ttu-id="239df-112">Para obtener más información sobre el enumerador de dispositivos del sistema, consulte [usar el enumerador de dispositivos del sistema](using-the-system-device-enumerator.md).</span><span class="sxs-lookup"><span data-stu-id="239df-112">For details about the system device enumerator, see [Using the System Device Enumerator](using-the-system-device-enumerator.md).</span></span> <span data-ttu-id="239df-113">En Resumen, todos los filtros de DirectShow se clasifican por categoría y cada categoría se identifica mediante un GUID.</span><span class="sxs-lookup"><span data-stu-id="239df-113">Briefly, all DirectShow filters are classified by category, and each category is identified by a GUID.</span></span> <span data-ttu-id="239df-114">En el caso de los compresores de vídeo, el GUID de categoría es CLSID \_ VideoCompressorCategory.</span><span class="sxs-lookup"><span data-stu-id="239df-114">For video compressors, the category GUID is CLSID\_VideoCompressorCategory.</span></span> <span data-ttu-id="239df-115">En el caso de los compresores de audio, es CLSID \_ AudioCompressorCategory.</span><span class="sxs-lookup"><span data-stu-id="239df-115">For audio compressors, it is CLSID\_AudioCompressorCategory.</span></span> <span data-ttu-id="239df-116">Para enumerar una categoría determinada, el enumerador de dispositivos del sistema crea un objeto de *enumerador* que admite la interfaz [**IEnumMoniker**](/windows/desktop/api/objidl/nn-objidl-ienummoniker) .</span><span class="sxs-lookup"><span data-stu-id="239df-116">To enumerate a particular category, the system device enumerator creates an *enumerator* object that supports the [**IEnumMoniker**](/windows/desktop/api/objidl/nn-objidl-ienummoniker) interface.</span></span> <span data-ttu-id="239df-117">La aplicación usa esta interfaz para recuperar monikers de dispositivo, donde cada moniker de dispositivo representa una instancia de un filtro de DirectShow.</span><span class="sxs-lookup"><span data-stu-id="239df-117">The application uses this interface to retrieve device monikers, where each device moniker represents an instance of a DirectShow filter.</span></span> <span data-ttu-id="239df-118">Puede utilizar el moniker para crear el filtro o para obtener el nombre descriptivo del dispositivo sin crear el filtro.</span><span class="sxs-lookup"><span data-stu-id="239df-118">You can use the moniker to create the filter, or to get the device's friendly name without creating the filter.</span></span>

<span data-ttu-id="239df-119">Para enumerar los compresores de audio o vídeo disponibles en el sistema del usuario, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="239df-119">To enumerate the video or audio compressors available on the user's system, do the following:</span></span>

1.  <span data-ttu-id="239df-120">Llame a [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) para crear el enumerador de dispositivos del sistema, que tiene un identificador de clase de CLSID \_ SystemDeviceEnum.</span><span class="sxs-lookup"><span data-stu-id="239df-120">Call [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) to create the system device enumerator, which has a class ID of CLSID\_SystemDeviceEnum.</span></span>
2.  <span data-ttu-id="239df-121">Llame a [**ICreateDevEnum:: CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) con el GUID de la categoría de filtro.</span><span class="sxs-lookup"><span data-stu-id="239df-121">Call [**ICreateDevEnum::CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) with the filter category GUID.</span></span> <span data-ttu-id="239df-122">El método devuelve un puntero de interfaz **IEnumMoniker** .</span><span class="sxs-lookup"><span data-stu-id="239df-122">The method returns an **IEnumMoniker** interface pointer.</span></span>
3.  <span data-ttu-id="239df-123">Use el método IEnumMoniker:: Next para enumerar los monikers de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="239df-123">Use the IEnumMoniker::Next method to enumerate the device monikers.</span></span> <span data-ttu-id="239df-124">Este método devuelve una interfaz [**IMoniker**](/windows/desktop/api/objidl/nn-objidl-imoniker) , que representa el moniker.</span><span class="sxs-lookup"><span data-stu-id="239df-124">This method returns an [**IMoniker**](/windows/desktop/api/objidl/nn-objidl-imoniker) interface, which represents the moniker.</span></span>

<span data-ttu-id="239df-125">Para obtener el nombre descriptivo de un moniker, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="239df-125">To get the friendly name from a moniker, do the following:</span></span>

1.  <span data-ttu-id="239df-126">Llame al método **IMoniker:: BindToStorage** .</span><span class="sxs-lookup"><span data-stu-id="239df-126">Call the **IMoniker::BindToStorage** method.</span></span> <span data-ttu-id="239df-127">Este método devuelve un puntero a la interfaz **IPropertyBag** .</span><span class="sxs-lookup"><span data-stu-id="239df-127">This method returns an **IPropertyBag** interface pointer.</span></span>
2.  <span data-ttu-id="239df-128">Use el método **IPropertyBag:: Read** para leer la propiedad **FriendlyName** .</span><span class="sxs-lookup"><span data-stu-id="239df-128">Use the **IPropertyBag::Read** method to read the **FriendlyName** property.</span></span>

<span data-ttu-id="239df-129">Normalmente, una aplicación mostraría una lista de compresores, de modo que el usuario pudiera elegir uno.</span><span class="sxs-lookup"><span data-stu-id="239df-129">Typically, an application would display a list of compressors, so that the user could choose one.</span></span> <span data-ttu-id="239df-130">Por ejemplo, el siguiente código rellena un cuadro de lista con los nombres de los compresores de vídeo disponibles.</span><span class="sxs-lookup"><span data-stu-id="239df-130">For example, the following code populates a list box with the names of the available video compressors.</span></span>


```C++
void OnInitDialog(HWND hDlg)
{
    HRESULT hr;
    ICreateDevEnum *pSysDevEnum = NULL;
    IEnumMoniker *pEnum = NULL;
    IMoniker *pMoniker = NULL;

    hr = CoCreateInstance(CLSID_SystemDeviceEnum, NULL, 
        CLSCTX_INPROC_SERVER, IID_ICreateDevEnum, 
        (void**)&pSysDevEnum);
    if (FAILED(hr))
    {
        // Handle the error.
    }    

    hr = pSysDevEnum->CreateClassEnumerator(
             CLSID_VideoCompressorCategory, &pEnum, 0);
    if (hr == S_OK)  // S_FALSE means nothing in this category.
    {
        while (S_OK == pEnum->Next(1, &pMoniker, NULL))
        {
            IPropertyBag *pPropBag = NULL;
            pMoniker->BindToStorage(0, 0, IID_IPropertyBag, 
                (void **)&pPropBag);
            VARIANT var;
            VariantInit(&var);
            hr = pPropBag->Read(L"FriendlyName", &var, 0);
            if (SUCCEEDED(hr))
            {
                LRESULT iSel = AddString(GetDlgItem(hDlg, 
                    IDC_CODEC_LIST), var.bstrVal);
            }   
            VariantClear(&var); 
            pPropBag->Release();
            pMoniker->Release();
        }
    }

    SendDlgItemMessage(hDlg, IDC_CODEC_LIST, 
                       LB_SETCURSEL, 0, 0);
    pSysDevEnum->Release();
    pEnum->Release();
}
```



<span data-ttu-id="239df-131">Para crear una instancia de filtro a partir del moniker, llame al método **IMoniker:: BindToObject** .</span><span class="sxs-lookup"><span data-stu-id="239df-131">To create a filter instance from the moniker, call the **IMoniker::BindToObject** method.</span></span> <span data-ttu-id="239df-132">El método devuelve un puntero [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) .</span><span class="sxs-lookup"><span data-stu-id="239df-132">The method returns an [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) pointer.</span></span>


```C++
IBaseFilter *pFilter = NULL;
hr = pMoniker->BindToObject(NULL, NULL, IID_IBaseFilter, 
                                       (void**)&pFilter);
if (SUCCEEDED(hr))
{
    // Use the filter. 
    // Remember to release the IBaseFilter interface.
}
```



<span data-ttu-id="239df-133">En el caso de los códecs VCM, cada moniker representa un códec determinado, aunque todos los códecs están encapsulados con el mismo filtro de compresión AVI.</span><span class="sxs-lookup"><span data-stu-id="239df-133">For VCM codecs, each moniker represents one particular codec, even though all of the codecs are wrapped by the same AVI Compression filter.</span></span> <span data-ttu-id="239df-134">La llamada a **BindToObject** crea una instancia de este filtro, inicializada para ese códec.</span><span class="sxs-lookup"><span data-stu-id="239df-134">Calling **BindToObject** creates an instance of this filter, initialized for that codec.</span></span> <span data-ttu-id="239df-135">Por esta razón, no se puede llamar a **CoCreateInstance** directamente en el filtro de compresión AVI.</span><span class="sxs-lookup"><span data-stu-id="239df-135">For this reason, you cannot call **CoCreateInstance** directly on the AVI Compression filter.</span></span> <span data-ttu-id="239df-136">Debe pasar por el enumerador de dispositivos del sistema.</span><span class="sxs-lookup"><span data-stu-id="239df-136">You must go through the system device enumerator.</span></span>

## <a name="related-topics"></a><span data-ttu-id="239df-137">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="239df-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="239df-138">Volver a comprimir un archivo AVI</span><span class="sxs-lookup"><span data-stu-id="239df-138">Recompressing an AVI File</span></span>](recompressing-an-avi-file.md)
</dt> </dl>

 

 
