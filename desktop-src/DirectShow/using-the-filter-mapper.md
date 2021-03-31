---
description: Usar el asignador de filtros
ms.assetid: 3f774350-4508-437f-98d1-cca91220f339
title: Usar el asignador de filtros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c2d7acf85a7b415fc161cd21e17d069b46c3f40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911070"
---
# <a name="using-the-filter-mapper"></a><span data-ttu-id="fe3d4-103">Usar el asignador de filtros</span><span class="sxs-lookup"><span data-stu-id="fe3d4-103">Using the Filter Mapper</span></span>

<span data-ttu-id="fe3d4-104">El [asignador de filtros](filter-mapper.md) es un objeto com que enumera los filtros de DirectShow en función de varios criterios de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="fe3d4-104">The [Filter Mapper](filter-mapper.md) is a COM object that enumerates DirectShow filters based on various search criteria.</span></span> <span data-ttu-id="fe3d4-105">El asignador de filtros puede ser menos eficaz que el enumerador de dispositivos del sistema, por lo que si necesita filtros de una categoría determinada, debe usar el enumerador de dispositivos del sistema.</span><span class="sxs-lookup"><span data-stu-id="fe3d4-105">The Filter Mapper can be less efficient than the System Device Enumerator, so if you need filters from a particular category, you should use the System Device Enumerator.</span></span> <span data-ttu-id="fe3d4-106">Pero si necesita buscar un filtro que admita una combinación determinada de tipos de medios, pero no se encuentra en una categoría de borrado, puede que tenga que usar el asignador de filtros.</span><span class="sxs-lookup"><span data-stu-id="fe3d4-106">But if you need to locate a filter that supports a certain combination of media types, but does not fall into a clear-cut category, you might need to use the Filter Mapper.</span></span> <span data-ttu-id="fe3d4-107">(Un ejemplo sería un filtro de representador o un filtro de descodificador).</span><span class="sxs-lookup"><span data-stu-id="fe3d4-107">(An example would be a renderer filter or a decoder filter.)</span></span>

<span data-ttu-id="fe3d4-108">El asignador de filtros expone la interfaz [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) .</span><span class="sxs-lookup"><span data-stu-id="fe3d4-108">The Filter Mapper exposes the [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) interface.</span></span> <span data-ttu-id="fe3d4-109">Para buscar un filtro, llame al método [**IFilterMapper2:: EnumMatchingFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters) .</span><span class="sxs-lookup"><span data-stu-id="fe3d4-109">To search for a filter, call the [**IFilterMapper2::EnumMatchingFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters) method.</span></span> <span data-ttu-id="fe3d4-110">Este método toma varios parámetros que definen los criterios de búsqueda y devuelve un enumerador para los filtros coincidentes.</span><span class="sxs-lookup"><span data-stu-id="fe3d4-110">This method takes several parameters that define the search criteria, and returns an enumerator for the matching filters.</span></span> <span data-ttu-id="fe3d4-111">El enumerador admite la interfaz [**IEnumMoniker**](/windows/win32/api/objidl/nn-objidl-ienummoniker) y proporciona un moniker único para cada filtro coincidente.</span><span class="sxs-lookup"><span data-stu-id="fe3d4-111">The enumerator supports the [**IEnumMoniker**](/windows/win32/api/objidl/nn-objidl-ienummoniker) interface, and supplies a unique moniker for each matching filter.</span></span>

<span data-ttu-id="fe3d4-112">En el ejemplo siguiente se enumeran los filtros que aceptan la entrada de vídeo digital (DV) y que tienen al menos un PIN de salida, de cualquier tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="fe3d4-112">The following example enumerates filters that accept digital video (DV) input and have at least one output pin, of any media type.</span></span> <span data-ttu-id="fe3d4-113">(El filtro de [descodificador de vídeo DV](dv-video-decoder-filter.md) coincide con estos criterios).</span><span class="sxs-lookup"><span data-stu-id="fe3d4-113">(The [DV Video Decoder](dv-video-decoder-filter.md) filter matches these criteria.)</span></span>


```C++
IFilterMapper2 *pMapper = NULL;
IEnumMoniker *pEnum = NULL;

hr = CoCreateInstance(CLSID_FilterMapper2, 
    NULL, CLSCTX_INPROC, IID_IFilterMapper2, 
    (void **) &pMapper);

if (FAILED(hr))
{
    // Error handling omitted for clarity.
}

GUID arrayInTypes[2];
arrayInTypes[0] = MEDIATYPE_Video;
arrayInTypes[1] = MEDIASUBTYPE_dvsd;

hr = pMapper->EnumMatchingFilters(
        &pEnum,
        0,                  // Reserved.
        TRUE,               // Use exact match?
        MERIT_DO_NOT_USE+1, // Minimum merit.
        TRUE,               // At least one input pin?
        1,                  // Number of major type/subtype pairs for input.
        arrayInTypes,       // Array of major type/subtype pairs for input.
        NULL,               // Input medium.
        NULL,               // Input pin category.
        FALSE,              // Must be a renderer?
        TRUE,               // At least one output pin?
        0,                  // Number of major type/subtype pairs for output.
        NULL,               // Array of major type/subtype pairs for output.
        NULL,               // Output medium.
        NULL);              // Output pin category.

// Enumerate the monikers.
IMoniker *pMoniker;
ULONG cFetched;
while (pEnum->Next(1, &pMoniker, &cFetched) == S_OK)
{
    IPropertyBag *pPropBag = NULL;
    hr = pMoniker->BindToStorage(0, 0, IID_IPropertyBag, 
       (void **)&pPropBag);

    if (SUCCEEDED(hr))
    {
        // To retrieve the friendly name of the filter, do the following:
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
        hr = pMoniker->BindToObject(NULL, NULL, IID_IBaseFilter, (void**)&pFilter);
        // Now add the filter to the graph. Remember to release pFilter later.
    
        // Clean up.
        pPropBag->Release();
    }
    pMoniker->Release();
}

// Clean up.
pMapper->Release();
pEnum->Release();
```



<span data-ttu-id="fe3d4-114">El método [**EnumMatchingFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters) tiene un número bastante grande de parámetros, que se comentan en el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="fe3d4-114">The [**EnumMatchingFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters) method has a fairly large number of parameters, which are commented in the example.</span></span> <span data-ttu-id="fe3d4-115">Los más importantes para este ejemplo son:</span><span class="sxs-lookup"><span data-stu-id="fe3d4-115">The significant ones for this example include:</span></span>

-   <span data-ttu-id="fe3d4-116">Valor de mérito mínimo: el filtro debe tener un valor de mérito por encima del mérito \_ \_ no \_ utilizado.</span><span class="sxs-lookup"><span data-stu-id="fe3d4-116">Minimum merit value: The filter must have a merit value above MERIT\_DO\_NOT\_USE.</span></span>
-   <span data-ttu-id="fe3d4-117">Tipos de entrada: el llamador pasa una matriz que contiene pares de tipos y subtipos principales.</span><span class="sxs-lookup"><span data-stu-id="fe3d4-117">Input types: The caller passes an array containing pairs of major types and subtypes.</span></span> <span data-ttu-id="fe3d4-118">Solo coincidirán los filtros que admiten al menos uno de estos pares.</span><span class="sxs-lookup"><span data-stu-id="fe3d4-118">Only filters that support at least one of these pairs will match.</span></span>
-   <span data-ttu-id="fe3d4-119">Coincidencia exacta: un filtro puede registrar valores **null** para el tipo principal, el subtipo, la categoría de PIN o el medio.</span><span class="sxs-lookup"><span data-stu-id="fe3d4-119">Exact match: A filter can register **NULL** values for major type, subtype, pin category, or medium.</span></span> <span data-ttu-id="fe3d4-120">A menos que especifique la coincidencia exacta, un valor **null** actúa como carácter comodín, que coincide con cualquier valor que especifique.</span><span class="sxs-lookup"><span data-stu-id="fe3d4-120">Unless you specify exact matching, a **NULL** value acts as a wildcard, matching any value that you specify.</span></span> <span data-ttu-id="fe3d4-121">Con la coincidencia exacta, el filtro debe coincidir exactamente con los criterios.</span><span class="sxs-lookup"><span data-stu-id="fe3d4-121">With exact matching, the filter must exactly match your criteria.</span></span> <span data-ttu-id="fe3d4-122">Sin embargo, si se proporciona un parámetro **null** en los criterios de búsqueda, siempre actúa como un carácter comodín o "no tiene cuidado", que coincide con cualquier filtro.</span><span class="sxs-lookup"><span data-stu-id="fe3d4-122">However, if you give a **NULL** parameter in the search criteria, it always acts as a wildcard or "don't care" value, matching any filter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fe3d4-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="fe3d4-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fe3d4-124">Enumerar dispositivos y filtros</span><span class="sxs-lookup"><span data-stu-id="fe3d4-124">Enumerating Devices and Filters</span></span>](enumerating-devices-and-filters.md)
</dt> <dt>

[<span data-ttu-id="fe3d4-125">Conexión inteligente</span><span class="sxs-lookup"><span data-stu-id="fe3d4-125">Intelligent Connect</span></span>](intelligent-connect.md)
</dt> </dl>

 

 
