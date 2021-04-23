---
description: Uso de DDO en DirectShow
ms.assetid: 47d75b9c-8b0d-4235-8ac1-02ae1502c0e7
title: Uso de DDO en DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdddc643d39798dc09807e9ecfa15c38a6e0c2cf
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908693"
---
# <a name="using-dmos-in-directshow"></a><span data-ttu-id="75ba9-103">Uso de DDO en DirectShow</span><span class="sxs-lookup"><span data-stu-id="75ba9-103">Using DMOs in DirectShow</span></span>

<span data-ttu-id="75ba9-104">Las aplicaciones basadas en DirectShow pueden usar DDO en un gráfico de filtros, a través del filtro [contenedor de DMO.](dmo-wrapper-filter.md)</span><span class="sxs-lookup"><span data-stu-id="75ba9-104">Applications based on DirectShow can use DMOs in a filter graph, through the [DMO Wrapper](dmo-wrapper-filter.md) filter.</span></span> <span data-ttu-id="75ba9-105">Este filtro agrega un DMO y controla todos los detalles del uso de DMO, como pasar datos a y desde el DMO, asignar objetos [**IMediaBuffer,**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediabuffer) etc.</span><span class="sxs-lookup"><span data-stu-id="75ba9-105">This filter aggregates a DMO and handles all the details of using the DMO, such as passing data to and from the DMO, allocating [**IMediaBuffer**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediabuffer) objects, and so forth.</span></span>

<span data-ttu-id="75ba9-106">Dado que el filtro agrega el DMO, la aplicación puede consultar el filtro para cualquier interfaz COM que exponga el DMO.</span><span class="sxs-lookup"><span data-stu-id="75ba9-106">Because the DMO is aggregated by the filter, the application can query the filter for any COM interfaces that the DMO exposes.</span></span> <span data-ttu-id="75ba9-107">Sin embargo, la aplicación debe permitir que el filtro controle todas las operaciones de streaming en el DMO.</span><span class="sxs-lookup"><span data-stu-id="75ba9-107">However, the application should let the filter handle all streaming operations on the DMO.</span></span> <span data-ttu-id="75ba9-108">Por ejemplo, no establezca tipos de medios, procese ningún búfer, vacíe el DMO, bloquee el DMO, habilite o deshabilite el control de calidad o establezca optimizaciones de vídeo.</span><span class="sxs-lookup"><span data-stu-id="75ba9-108">For example, do not set media types, process any buffers, flush the DMO, lock the DMO, enable or disable quality control, or set video optimizations.</span></span>

<span data-ttu-id="75ba9-109">Si conoce el identificador de clase (CLSID) de un DMO específico que desea usar, puede inicializar el filtro contenedor de DMO con ese DMO, como se muestra a continuación:</span><span class="sxs-lookup"><span data-stu-id="75ba9-109">If you know the class identifier (CLSID) of a specific DMO that you want to use, you can initialize the DMO Wrapper filter with that DMO, as follows:</span></span>

1.  <span data-ttu-id="75ba9-110">Llame **a CoCreateInstance** para crear el filtro contenedor de DMO.</span><span class="sxs-lookup"><span data-stu-id="75ba9-110">Call **CoCreateInstance** to create the DMO Wrapper filter.</span></span>
2.  <span data-ttu-id="75ba9-111">Consulte el filtro contenedor de DMO para la [**interfaz IDMOWrapperFilter.**](/previous-versions/windows/desktop/api/Dmodshow/nn-dmodshow-idmowrapperfilter)</span><span class="sxs-lookup"><span data-stu-id="75ba9-111">Query the DMO Wrapper filter for the [**IDMOWrapperFilter**](/previous-versions/windows/desktop/api/Dmodshow/nn-dmodshow-idmowrapperfilter) interface.</span></span>
3.  <span data-ttu-id="75ba9-112">Llame al [**método IDMOWrapperFilter::Init.**](/previous-versions/windows/desktop/api/Dmodshow/nf-dmodshow-idmowrapperfilter-init)</span><span class="sxs-lookup"><span data-stu-id="75ba9-112">Call the [**IDMOWrapperFilter::Init**](/previous-versions/windows/desktop/api/Dmodshow/nf-dmodshow-idmowrapperfilter-init) method.</span></span> <span data-ttu-id="75ba9-113">Especifique el CLSID del DMO y el GUID de la categoría de DMO.</span><span class="sxs-lookup"><span data-stu-id="75ba9-113">Specify the CLSID of the DMO and the GUID of the DMO's category.</span></span> <span data-ttu-id="75ba9-114">Para obtener una lista de categorías de DMO, vea [GUID de DMO](dmo-guids.md).</span><span class="sxs-lookup"><span data-stu-id="75ba9-114">For a list of DMO categories, see [DMO GUIDs](dmo-guids.md).</span></span>

<span data-ttu-id="75ba9-115">El siguiente código muestra estos pasos:</span><span class="sxs-lookup"><span data-stu-id="75ba9-115">The following code shows these steps:</span></span>


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



<span data-ttu-id="75ba9-116">La [**función DMOEnum**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoenum) enumera las DDO en el Registro.</span><span class="sxs-lookup"><span data-stu-id="75ba9-116">The [**DMOEnum**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoenum) function enumerates DMOs in the registry.</span></span> <span data-ttu-id="75ba9-117">Esta función usa un conjunto diferente de GUID de categoría de los usados para los filtros de DirectShow.</span><span class="sxs-lookup"><span data-stu-id="75ba9-117">This function uses a different set of category GUIDs from the ones used for DirectShow filters.</span></span>

<span data-ttu-id="75ba9-118">**Uso del enumerador de dispositivos del sistema con DDO**</span><span class="sxs-lookup"><span data-stu-id="75ba9-118">**Using the System Device Enumerator with DMOs**</span></span>

<span data-ttu-id="75ba9-119">En lugar de crear un DMO directamente, puede usar el enumerador de dispositivos del sistema [,](system-device-enumerator.md)que puede enumerar cualquier categoría de DMO que sea compatible con el **método DMOEnum.**</span><span class="sxs-lookup"><span data-stu-id="75ba9-119">Instead of creating a DMO directly, you can use the [System Device Enumerator](system-device-enumerator.md), which can enumerate any DMO category that is supported by the **DMOEnum** method.</span></span> <span data-ttu-id="75ba9-120">El enumerador de dispositivos del sistema también incluye DDO cuando enumera determinadas categorías de filtro de DirectShow.</span><span class="sxs-lookup"><span data-stu-id="75ba9-120">The System Device Enumerator also includes DMOs when it enumerates certain DirectShow filter categories.</span></span> <span data-ttu-id="75ba9-121">En la tabla siguiente se muestra la asignación entre las categorías DMO y DirectShow.</span><span class="sxs-lookup"><span data-stu-id="75ba9-121">The following table shows the mapping between DMO categories and DirectShow categories.</span></span>



| <span data-ttu-id="75ba9-122">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="75ba9-122">Label</span></span> | <span data-ttu-id="75ba9-123">Value</span><span class="sxs-lookup"><span data-stu-id="75ba9-123">Value</span></span> |
|-----------------------------|--------------------------------|
| <span data-ttu-id="75ba9-124">Categoría DMO</span><span class="sxs-lookup"><span data-stu-id="75ba9-124">DMO Category</span></span>                | <span data-ttu-id="75ba9-125">Equivalente de DirectShow</span><span class="sxs-lookup"><span data-stu-id="75ba9-125">DirectShow Equivalent</span></span>          |
| <span data-ttu-id="75ba9-126">CODIFICADOR DE AUDIO DMOCATEGORY \_ \_</span><span class="sxs-lookup"><span data-stu-id="75ba9-126">DMOCATEGORY\_AUDIO\_ENCODER</span></span> | <span data-ttu-id="75ba9-127">CLSID \_ AudioCompressorCategory</span><span class="sxs-lookup"><span data-stu-id="75ba9-127">CLSID\_AudioCompressorCategory</span></span> |
| <span data-ttu-id="75ba9-128">DESCODIFICADOR DE AUDIO DMOCATEGORY \_ \_</span><span class="sxs-lookup"><span data-stu-id="75ba9-128">DMOCATEGORY\_AUDIO\_DECODER</span></span> | <span data-ttu-id="75ba9-129">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="75ba9-129">CLSID\_LegacyAmFilterCategory</span></span>  |
| <span data-ttu-id="75ba9-130">CODIFICADOR DE VÍDEO DMOCATEGORY \_ \_</span><span class="sxs-lookup"><span data-stu-id="75ba9-130">DMOCATEGORY\_VIDEO\_ENCODER</span></span> | <span data-ttu-id="75ba9-131">CLSID \_ VideoCompressorCategory</span><span class="sxs-lookup"><span data-stu-id="75ba9-131">CLSID\_VideoCompressorCategory</span></span> |
| <span data-ttu-id="75ba9-132">DESCODIFICADOR DE VÍDEO DMOCATEGORY \_ \_</span><span class="sxs-lookup"><span data-stu-id="75ba9-132">DMOCATEGORY\_VIDEO\_DECODER</span></span> | <span data-ttu-id="75ba9-133">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="75ba9-133">CLSID\_LegacyAmFilterCategory</span></span>  |



 

<span data-ttu-id="75ba9-134">El enumerador de dispositivos del sistema devuelve una lista de objetos moniker.</span><span class="sxs-lookup"><span data-stu-id="75ba9-134">The System Device Enumerator returns a list of moniker objects.</span></span> <span data-ttu-id="75ba9-135">Si el moniker representa un DMO, el método **IMoniker::BindToObject** crea automáticamente el filtro contenedor DMO y lo inicializa con ese DMO.</span><span class="sxs-lookup"><span data-stu-id="75ba9-135">If the moniker represents a DMO, the **IMoniker::BindToObject** method automatically creates the DMO Wrapper filter and initializes it with that DMO.</span></span> <span data-ttu-id="75ba9-136">Por lo tanto, el hecho de que un DMO esté implicado es transparente para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="75ba9-136">Thus, the fact that a DMO is involved is transparent to the application.</span></span> <span data-ttu-id="75ba9-137">Para obtener más información sobre el uso del enumerador de dispositivos del sistema, vea [Usar el enumerador de dispositivos del sistema](using-the-system-device-enumerator.md).</span><span class="sxs-lookup"><span data-stu-id="75ba9-137">For more information on using the System Device Enumerator, see [Using the System Device Enumerator](using-the-system-device-enumerator.md).</span></span>

<span data-ttu-id="75ba9-138">**Limitaciones**</span><span class="sxs-lookup"><span data-stu-id="75ba9-138">**Limitations**</span></span>

<span data-ttu-id="75ba9-139">Existen algunas limitaciones al usar las DDO en DirectShow:</span><span class="sxs-lookup"><span data-stu-id="75ba9-139">There are some limitations when using DMOs in DirectShow:</span></span>

-   <span data-ttu-id="75ba9-140">El filtro contenedor DMO no admite DDO con cero entradas, varias entradas o cero salidas.</span><span class="sxs-lookup"><span data-stu-id="75ba9-140">The DMO Wrapper filter does not support DMOs with zero inputs, multiple inputs, or zero outputs.</span></span>
-   <span data-ttu-id="75ba9-141">Todas las conexiones ancladas en el filtro contenedor de DMO usan [**la interfaz IMemInputPin.**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)</span><span class="sxs-lookup"><span data-stu-id="75ba9-141">All pin connections on the DMO Wrapper Filter use the [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) interface.</span></span>
-   <span data-ttu-id="75ba9-142">DirectShow Editing Services no admite transiciones ni efectos basados en DMO.</span><span class="sxs-lookup"><span data-stu-id="75ba9-142">DirectShow Editing Services does not support DMO-based effects or transitions.</span></span>

## <a name="related-topics"></a><span data-ttu-id="75ba9-143">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="75ba9-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="75ba9-144">Uso de DDO</span><span class="sxs-lookup"><span data-stu-id="75ba9-144">Using DMOs</span></span>](using-dmos.md)
</dt> </dl>

 

 



