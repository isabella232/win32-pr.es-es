---
description: Usar DMOs en DirectShow
ms.assetid: 47d75b9c-8b0d-4235-8ac1-02ae1502c0e7
title: Usar DMOs en DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c90513649756a49067e523390292d4b44e1eac2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104156732"
---
# <a name="using-dmos-in-directshow"></a><span data-ttu-id="3412b-103">Usar DMOs en DirectShow</span><span class="sxs-lookup"><span data-stu-id="3412b-103">Using DMOs in DirectShow</span></span>

<span data-ttu-id="3412b-104">Las aplicaciones basadas en DirectShow pueden usar DMOs en un gráfico de filtros, a través del filtro de [contenedor de DMO](dmo-wrapper-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="3412b-104">Applications based on DirectShow can use DMOs in a filter graph, through the [DMO Wrapper](dmo-wrapper-filter.md) filter.</span></span> <span data-ttu-id="3412b-105">Este filtro agrega un DMO y controla todos los detalles del uso de DMO, como pasar datos hacia y desde DMO, asignando objetos [**IMediaBuffer**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediabuffer) , etc.</span><span class="sxs-lookup"><span data-stu-id="3412b-105">This filter aggregates a DMO and handles all the details of using the DMO, such as passing data to and from the DMO, allocating [**IMediaBuffer**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediabuffer) objects, and so forth.</span></span>

<span data-ttu-id="3412b-106">Como el filtro agrega DMO, la aplicación puede consultar el filtro para las interfaces COM que expone el DMO.</span><span class="sxs-lookup"><span data-stu-id="3412b-106">Because the DMO is aggregated by the filter, the application can query the filter for any COM interfaces that the DMO exposes.</span></span> <span data-ttu-id="3412b-107">Sin embargo, la aplicación debe permitir que el filtro controle todas las operaciones de streaming en DMO.</span><span class="sxs-lookup"><span data-stu-id="3412b-107">However, the application should let the filter handle all streaming operations on the DMO.</span></span> <span data-ttu-id="3412b-108">Por ejemplo, no establezca tipos de medios, procese ningún búfer, vacíe el DMO, bloquee el DMO, habilite o deshabilite el control de calidad o establezca optimizaciones de vídeo.</span><span class="sxs-lookup"><span data-stu-id="3412b-108">For example, do not set media types, process any buffers, flush the DMO, lock the DMO, enable or disable quality control, or set video optimizations.</span></span>

<span data-ttu-id="3412b-109">Si conoce el identificador de clase (CLSID) de un DMO específico que desea usar, puede inicializar el filtro de contenedor de DMO con ese DMO, como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="3412b-109">If you know the class identifier (CLSID) of a specific DMO that you want to use, you can initialize the DMO Wrapper filter with that DMO, as follows:</span></span>

1.  <span data-ttu-id="3412b-110">Llame a **CoCreateInstance** para crear el filtro de contenedor de DMO.</span><span class="sxs-lookup"><span data-stu-id="3412b-110">Call **CoCreateInstance** to create the DMO Wrapper filter.</span></span>
2.  <span data-ttu-id="3412b-111">Consulte el filtro de contenedor de DMO para la interfaz [**IDMOWrapperFilter**](/previous-versions/windows/desktop/api/Dmodshow/nn-dmodshow-idmowrapperfilter) .</span><span class="sxs-lookup"><span data-stu-id="3412b-111">Query the DMO Wrapper filter for the [**IDMOWrapperFilter**](/previous-versions/windows/desktop/api/Dmodshow/nn-dmodshow-idmowrapperfilter) interface.</span></span>
3.  <span data-ttu-id="3412b-112">Llame al método [**IDMOWrapperFilter:: init**](/previous-versions/windows/desktop/api/Dmodshow/nf-dmodshow-idmowrapperfilter-init) .</span><span class="sxs-lookup"><span data-stu-id="3412b-112">Call the [**IDMOWrapperFilter::Init**](/previous-versions/windows/desktop/api/Dmodshow/nf-dmodshow-idmowrapperfilter-init) method.</span></span> <span data-ttu-id="3412b-113">Especifique el CLSID de DMO y el GUID de la categoría de DMO.</span><span class="sxs-lookup"><span data-stu-id="3412b-113">Specify the CLSID of the DMO and the GUID of the DMO's category.</span></span> <span data-ttu-id="3412b-114">Para obtener una lista de las categorías de DMO, consulte los [GUID de DMO](dmo-guids.md).</span><span class="sxs-lookup"><span data-stu-id="3412b-114">For a list of DMO categories, see [DMO GUIDs](dmo-guids.md).</span></span>

<span data-ttu-id="3412b-115">El siguiente código muestra estos pasos:</span><span class="sxs-lookup"><span data-stu-id="3412b-115">The following code shows these steps:</span></span>


```C++
// Create the DMO Wrapper filter.
IBaseFilter *pFilter;
HRESULT hr = CoCreateInstance(CLSID_DMOWrapperFilter, NULL, 
    CLSCTX_INPROC_SERVER, IID_IBaseFilter, 
    reinterpret_cast<void**>(&pFilter));

if (SUCCEEDED(hr)) 
{
    // Query for IDMOWrapperFilter.
    IDMOWrapperFilter *pDmoWrapper;
    hr = pFilter->QueryInterface(IID_IDMOWrapperFilter, 
        reinterpret_cast<void**>(&pDmoWrapper));

    if (SUCCEEDED(hr)) 
    {     
        // Initialize the filter.
        hr = pDmoWrapper->Init(CLSID_MyDMO, DMOCATEGORY_VIDEO_EFFECT); 
        pDmoWrapper->Release();

        if (SUCCEEDED(hr)) 
        {
            // Add the filter to the graph.
            hr = pGraph->AddFilter(pFilter, L"My DMO");
        }
    }
    pFilter->Release();
}
```



<span data-ttu-id="3412b-116">La función [**DMOEnum**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoenum) enumera DMOs en el registro.</span><span class="sxs-lookup"><span data-stu-id="3412b-116">The [**DMOEnum**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoenum) function enumerates DMOs in the registry.</span></span> <span data-ttu-id="3412b-117">Esta función utiliza un conjunto diferente de GUID de categoría de los que se usan para los filtros de DirectShow.</span><span class="sxs-lookup"><span data-stu-id="3412b-117">This function uses a different set of category GUIDs from the ones used for DirectShow filters.</span></span>

<span data-ttu-id="3412b-118">**Usar el enumerador de dispositivos del sistema con DMOs**</span><span class="sxs-lookup"><span data-stu-id="3412b-118">**Using the System Device Enumerator with DMOs**</span></span>

<span data-ttu-id="3412b-119">En lugar de crear directamente un DMO, puede usar el [enumerador de dispositivos del sistema](system-device-enumerator.md), que puede enumerar cualquier categoría de DMO compatible con el método **DMOEnum** .</span><span class="sxs-lookup"><span data-stu-id="3412b-119">Instead of creating a DMO directly, you can use the [System Device Enumerator](system-device-enumerator.md), which can enumerate any DMO category that is supported by the **DMOEnum** method.</span></span> <span data-ttu-id="3412b-120">El enumerador de dispositivos del sistema también incluye DMOs cuando enumera determinadas categorías de filtros de DirectShow.</span><span class="sxs-lookup"><span data-stu-id="3412b-120">The System Device Enumerator also includes DMOs when it enumerates certain DirectShow filter categories.</span></span> <span data-ttu-id="3412b-121">En la tabla siguiente se muestra la asignación entre categorías de DMO y categorías de DirectShow.</span><span class="sxs-lookup"><span data-stu-id="3412b-121">The following table shows the mapping between DMO categories and DirectShow categories.</span></span>



|                             |                                |
|-----------------------------|--------------------------------|
| <span data-ttu-id="3412b-122">Categoría de DMO</span><span class="sxs-lookup"><span data-stu-id="3412b-122">DMO Category</span></span>                | <span data-ttu-id="3412b-123">Equivalente de DirectShow</span><span class="sxs-lookup"><span data-stu-id="3412b-123">DirectShow Equivalent</span></span>          |
| <span data-ttu-id="3412b-124">\_codificador de audio DMOCATEGORY \_</span><span class="sxs-lookup"><span data-stu-id="3412b-124">DMOCATEGORY\_AUDIO\_ENCODER</span></span> | <span data-ttu-id="3412b-125">CLSID \_ AudioCompressorCategory</span><span class="sxs-lookup"><span data-stu-id="3412b-125">CLSID\_AudioCompressorCategory</span></span> |
| <span data-ttu-id="3412b-126">descodificador de audio de DMOCATEGORY \_ \_</span><span class="sxs-lookup"><span data-stu-id="3412b-126">DMOCATEGORY\_AUDIO\_DECODER</span></span> | <span data-ttu-id="3412b-127">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="3412b-127">CLSID\_LegacyAmFilterCategory</span></span>  |
| <span data-ttu-id="3412b-128">\_codificador de vídeo de DMOCATEGORY \_</span><span class="sxs-lookup"><span data-stu-id="3412b-128">DMOCATEGORY\_VIDEO\_ENCODER</span></span> | <span data-ttu-id="3412b-129">CLSID \_ VideoCompressorCategory</span><span class="sxs-lookup"><span data-stu-id="3412b-129">CLSID\_VideoCompressorCategory</span></span> |
| <span data-ttu-id="3412b-130">descodificador de vídeo de DMOCATEGORY \_ \_</span><span class="sxs-lookup"><span data-stu-id="3412b-130">DMOCATEGORY\_VIDEO\_DECODER</span></span> | <span data-ttu-id="3412b-131">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="3412b-131">CLSID\_LegacyAmFilterCategory</span></span>  |



 

<span data-ttu-id="3412b-132">El enumerador de dispositivos del sistema devuelve una lista de objetos moniker.</span><span class="sxs-lookup"><span data-stu-id="3412b-132">The System Device Enumerator returns a list of moniker objects.</span></span> <span data-ttu-id="3412b-133">Si el moniker representa un DMO, el método **IMoniker:: BindToObject** crea automáticamente el filtro de contenedor de DMO y lo inicializa con dicho DMO.</span><span class="sxs-lookup"><span data-stu-id="3412b-133">If the moniker represents a DMO, the **IMoniker::BindToObject** method automatically creates the DMO Wrapper filter and initializes it with that DMO.</span></span> <span data-ttu-id="3412b-134">Por lo tanto, el hecho de que un DMO esté implicado es transparente para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="3412b-134">Thus, the fact that a DMO is involved is transparent to the application.</span></span> <span data-ttu-id="3412b-135">Para obtener más información acerca del uso del enumerador de dispositivos del sistema, consulte [usar el enumerador de dispositivos del sistema](using-the-system-device-enumerator.md).</span><span class="sxs-lookup"><span data-stu-id="3412b-135">For more information on using the System Device Enumerator, see [Using the System Device Enumerator](using-the-system-device-enumerator.md).</span></span>

<span data-ttu-id="3412b-136">**Limitaciones**</span><span class="sxs-lookup"><span data-stu-id="3412b-136">**Limitations**</span></span>

<span data-ttu-id="3412b-137">Hay algunas limitaciones al usar DMOs en DirectShow:</span><span class="sxs-lookup"><span data-stu-id="3412b-137">There are some limitations when using DMOs in DirectShow:</span></span>

-   <span data-ttu-id="3412b-138">El filtro de contenedor de DMO no admite DMOs con cero entradas, entradas múltiples o salidas cero.</span><span class="sxs-lookup"><span data-stu-id="3412b-138">The DMO Wrapper filter does not support DMOs with zero inputs, multiple inputs, or zero outputs.</span></span>
-   <span data-ttu-id="3412b-139">Todas las conexiones de PIN en el filtro de contenedor de DMO usan la interfaz [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) .</span><span class="sxs-lookup"><span data-stu-id="3412b-139">All pin connections on the DMO Wrapper Filter use the [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) interface.</span></span>
-   <span data-ttu-id="3412b-140">Los servicios de edición de DirectShow no admiten efectos ni transiciones basados en DMO.</span><span class="sxs-lookup"><span data-stu-id="3412b-140">DirectShow Editing Services does not support DMO-based effects or transitions.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3412b-141">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3412b-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3412b-142">Usar DMOs</span><span class="sxs-lookup"><span data-stu-id="3412b-142">Using DMOs</span></span>](using-dmos.md)
</dt> </dl>

 

 



