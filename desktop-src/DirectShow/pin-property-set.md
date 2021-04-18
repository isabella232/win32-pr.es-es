---
description: Conjunto de propiedades de PIN
ms.assetid: 0c01bd51-353d-4f48-b33c-796f740915e2
title: Conjunto de propiedades de PIN
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bc2d3ed55d7fed70d37a92427d1288ed58aef65
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104422840"
---
# <a name="pin-property-set"></a><span data-ttu-id="2f7cf-103">Conjunto de propiedades de PIN</span><span class="sxs-lookup"><span data-stu-id="2f7cf-103">Pin Property Set</span></span>

<span data-ttu-id="2f7cf-104">El conjunto de propiedades PIN devuelve la categoría PIN de un PIN en un filtro.</span><span class="sxs-lookup"><span data-stu-id="2f7cf-104">The pin property set returns the pin category for a pin on a filter.</span></span> <span data-ttu-id="2f7cf-105">La categoría se establece mediante el filtro cuando crea el PIN; la categoría indica el tipo de datos que el PIN envía o recibe.</span><span class="sxs-lookup"><span data-stu-id="2f7cf-105">The category is set by the filter when it creates the pin; the category indicates what type of data the pin is delivered or receives by this pin.</span></span>



|                   |                      |
|-------------------|----------------------|
| <span data-ttu-id="2f7cf-106">GUID del conjunto de propiedades</span><span class="sxs-lookup"><span data-stu-id="2f7cf-106">Property Set GUID</span></span> | <span data-ttu-id="2f7cf-107">**AMPROPSETID \_ PIN**</span><span class="sxs-lookup"><span data-stu-id="2f7cf-107">**AMPROPSETID\_Pin**</span></span> |



 



| <span data-ttu-id="2f7cf-108">Id. de propiedad</span><span class="sxs-lookup"><span data-stu-id="2f7cf-108">Property ID</span></span>                   | <span data-ttu-id="2f7cf-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="2f7cf-109">Description</span></span>                      |
|-------------------------------|----------------------------------|
| <span data-ttu-id="2f7cf-110">**\_categoría AMPROPERTY PIN \_**</span><span class="sxs-lookup"><span data-stu-id="2f7cf-110">**AMPROPERTY\_PIN\_CATEGORY**</span></span> | <span data-ttu-id="2f7cf-111">Especifica la categoría de un PIN.</span><span class="sxs-lookup"><span data-stu-id="2f7cf-111">Specifies the category of a pin.</span></span> |



 

<span data-ttu-id="2f7cf-112">DirectShow define las siguientes categorías de PIN en el archivo de encabezado UUID. h.</span><span class="sxs-lookup"><span data-stu-id="2f7cf-112">DirectShow defines the following pin categories in the Uuids.h header file.</span></span>



| <span data-ttu-id="2f7cf-113">GUID de categoría</span><span class="sxs-lookup"><span data-stu-id="2f7cf-113">Category GUID</span></span>                     | <span data-ttu-id="2f7cf-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="2f7cf-114">Description</span></span>                                                                                                                                                                                                                                                                                                             |
|-----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f7cf-115">**PIN \_ categoría \_ ANALOGVIDEOIN**</span><span class="sxs-lookup"><span data-stu-id="2f7cf-115">**PIN\_CATEGORY\_ANALOGVIDEOIN**</span></span>  | <span data-ttu-id="2f7cf-116">PIN de entrada del filtro de captura que toma el analógico y lo digitaliza.</span><span class="sxs-lookup"><span data-stu-id="2f7cf-116">Input pin of the capture filter that takes analog and digitizes it.</span></span>                                                                                                                                                                                                                                                     |
| <span data-ttu-id="2f7cf-117">**\_captura de categoría de PIN \_**</span><span class="sxs-lookup"><span data-stu-id="2f7cf-117">**PIN\_CATEGORY\_CAPTURE**</span></span>        | <span data-ttu-id="2f7cf-118">PIN de captura.</span><span class="sxs-lookup"><span data-stu-id="2f7cf-118">Capture pin.</span></span>                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="2f7cf-119">**Categoría de PIN \_ \_ CC**</span><span class="sxs-lookup"><span data-stu-id="2f7cf-119">**PIN\_CATEGORY\_CC**</span></span>             | <span data-ttu-id="2f7cf-120">PIN que proporciona datos de subtítulos (CC) de la línea 21.</span><span class="sxs-lookup"><span data-stu-id="2f7cf-120">Pin providing closed captioning data from Line 21.</span></span>                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="2f7cf-121">**Categoría de PIN \_ \_ EDS**</span><span class="sxs-lookup"><span data-stu-id="2f7cf-121">**PIN\_CATEGORY\_EDS**</span></span>            | <span data-ttu-id="2f7cf-122">PIN que proporciona Data Services extendida (línea 21, pares campos).</span><span class="sxs-lookup"><span data-stu-id="2f7cf-122">Pin providing Extended Data Services (Line 21, even fields).</span></span>                                                                                                                                                                                                                                                            |
| <span data-ttu-id="2f7cf-123">**PIN \_ categoría \_ NABTS**</span><span class="sxs-lookup"><span data-stu-id="2f7cf-123">**PIN\_CATEGORY\_NABTS**</span></span>          | <span data-ttu-id="2f7cf-124">PIN que proporciona datos estándar de videotexto de Norteamérica.</span><span class="sxs-lookup"><span data-stu-id="2f7cf-124">Pin providing North American Videotext Standard data.</span></span>                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="2f7cf-125">**\_vista previa de categoría de PIN \_**</span><span class="sxs-lookup"><span data-stu-id="2f7cf-125">**PIN\_CATEGORY\_PREVIEW**</span></span>        | <span data-ttu-id="2f7cf-126">PIN de vista previa.</span><span class="sxs-lookup"><span data-stu-id="2f7cf-126">Preview pin.</span></span>                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="2f7cf-127">**Categoría de PIN \_ \_ todavía**</span><span class="sxs-lookup"><span data-stu-id="2f7cf-127">**PIN\_CATEGORY\_STILL**</span></span>          | <span data-ttu-id="2f7cf-128">PIN que proporciona una imagen fija.</span><span class="sxs-lookup"><span data-stu-id="2f7cf-128">Pin that provides a still image.</span></span> <span data-ttu-id="2f7cf-129">El PIN de captura del filtro debe estar conectado antes de que se conecte el PIN de imagen fija.</span><span class="sxs-lookup"><span data-stu-id="2f7cf-129">The filter's capture pin must be connected before the still-image pin is connected.</span></span>                                                                                                                                                                                                    |
| <span data-ttu-id="2f7cf-130">**\_teletexto de categoría de PIN \_**</span><span class="sxs-lookup"><span data-stu-id="2f7cf-130">**PIN\_CATEGORY\_TELETEXT**</span></span>       | <span data-ttu-id="2f7cf-131">PIN que proporciona teletexto (una variante de subtítulos).</span><span class="sxs-lookup"><span data-stu-id="2f7cf-131">Pin providing teletext (a closed captioning variant).</span></span>                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="2f7cf-132">**código de tiempo de \_ categoría de PIN \_**</span><span class="sxs-lookup"><span data-stu-id="2f7cf-132">**PIN\_CATEGORY\_TIMECODE**</span></span>       | <span data-ttu-id="2f7cf-133">PIN que proporciona datos de código de tiempo.</span><span class="sxs-lookup"><span data-stu-id="2f7cf-133">Pin providing timecode data.</span></span>                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="2f7cf-134">**PIN \_ categoría \_ VBI**</span><span class="sxs-lookup"><span data-stu-id="2f7cf-134">**PIN\_CATEGORY\_VBI**</span></span>            | <span data-ttu-id="2f7cf-135">PIN que proporciona datos de intervalo de espacio en blanco vertical.</span><span class="sxs-lookup"><span data-stu-id="2f7cf-135">Pin providing vertical blanking interval data.</span></span>                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="2f7cf-136">**videopuerto de categoría de PIN \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2f7cf-136">**PIN\_CATEGORY\_VIDEOPORT**</span></span>      | <span data-ttu-id="2f7cf-137">PIN de salida de vídeo que se va a conectar a la clavija de entrada cero en el [mezclador de superposición](overlay-mixer-filter.md).</span><span class="sxs-lookup"><span data-stu-id="2f7cf-137">Video output pin to be connected to input pin zero on the [Overlay Mixer](overlay-mixer-filter.md).</span></span>                                                                                                                                                                                                                    |
| <span data-ttu-id="2f7cf-138">**Categoría de PIN de \_ \_ videopuerto \_ VBI**</span><span class="sxs-lookup"><span data-stu-id="2f7cf-138">**PIN\_CATEGORY\_VIDEOPORT\_VBI**</span></span> | <span data-ttu-id="2f7cf-139">PIN que se va a conectar al [asignador de superficie de VBI](vbi-surface-allocator.md), el filtro de asignador de superficie de VBI necesario para asignar la memoria de vídeo correcta para elementos como superposiciones de subtítulos (CC) en escenarios en los que se usa un puerto de vídeo.</span><span class="sxs-lookup"><span data-stu-id="2f7cf-139">Pin to be connected to the [VBI Surface Allocator](vbi-surface-allocator.md), the VBI surface allocator filter that is needed to allocate the correct video memory for things like closed captioning overlays in scenarios where a video port is being used.</span></span> <span data-ttu-id="2f7cf-140">Los escenarios PCI, IEEE 1394 y USB no usan este filtro.</span><span class="sxs-lookup"><span data-stu-id="2f7cf-140">PCI, IEEE 1394, and USB scenarios do not use this filter.</span></span> |
| <span data-ttu-id="2f7cf-141">**\_captura de \_ CC de vídeo PINNAME \_**</span><span class="sxs-lookup"><span data-stu-id="2f7cf-141">**PINNAME\_VIDEO\_CC\_CAPTURE**</span></span>   | <span data-ttu-id="2f7cf-142">División de hardware cerrado: PIN de subtítulos</span><span class="sxs-lookup"><span data-stu-id="2f7cf-142">Hardware slicing closed-captioning pin</span></span>                                                                                                                                                                                                                                                                                  |



 

<span data-ttu-id="2f7cf-143">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="2f7cf-143">This property is read-only.</span></span>

### <a name="example-code"></a><span data-ttu-id="2f7cf-144">Código de ejemplo</span><span class="sxs-lookup"><span data-stu-id="2f7cf-144">Example Code</span></span>

<span data-ttu-id="2f7cf-145">En el código siguiente se muestra cómo comprobar si un PIN admite este conjunto de propiedades y, en ese caso, cómo obtener la categoría de PIN:</span><span class="sxs-lookup"><span data-stu-id="2f7cf-145">The following code shows how to check whether a pin supports this property set, and if so, how to obtain the pin category:</span></span>


```C++
HRESULT GetPinCategory(IPin *pPin, GUID *pPinCategory)
{
    IKsPropertySet *pKs = NULL;

    HRESULT hr = pPin->QueryInterface(IID_PPV_ARGS(&pKs));
    if (FAILED(hr))
    {
        return hr;
    }

    // Try to retrieve the pin category.
    DWORD cbReturned = 0;
    hr = pKs->Get(AMPROPSETID_Pin, AMPROPERTY_PIN_CATEGORY, NULL, 0, 
        pPinCategory, sizeof(GUID), &cbReturned);
    
    // If this succeeded, pPinCategory now contains the category GUID.

    SafeRelease(&pKs);
    return hr;
}
```



> [!Note]  
> <span data-ttu-id="2f7cf-146">En este ejemplo se usa la función [SafeRelease](../medfound/saferelease.md) para liberar punteros de interfaz.</span><span class="sxs-lookup"><span data-stu-id="2f7cf-146">This example uses the [SafeRelease](../medfound/saferelease.md) function to release interface pointers.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="2f7cf-147">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2f7cf-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2f7cf-148">Requisitos de PIN para los filtros de captura</span><span class="sxs-lookup"><span data-stu-id="2f7cf-148">Pin Requirements for Capture Filters</span></span>](pin-requirements-for-capture-filters.md)
</dt> <dt>

[<span data-ttu-id="2f7cf-149">Conjuntos de propiedades</span><span class="sxs-lookup"><span data-stu-id="2f7cf-149">Property Sets</span></span>](property-sets.md)
</dt> <dt>

[<span data-ttu-id="2f7cf-150">Trabajar con categorías de PIN</span><span class="sxs-lookup"><span data-stu-id="2f7cf-150">Working with Pin Categories</span></span>](working-with-pin-categories.md)
</dt> </dl>

 

 
