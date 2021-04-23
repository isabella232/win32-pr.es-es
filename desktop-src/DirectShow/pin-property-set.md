---
description: Anclar conjunto de propiedades
ms.assetid: 0c01bd51-353d-4f48-b33c-796f740915e2
title: Anclar conjunto de propiedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e53955ba1f075094c4fb2f6324ed143ca54f72c2
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909623"
---
# <a name="pin-property-set"></a><span data-ttu-id="b89d1-103">Anclar conjunto de propiedades</span><span class="sxs-lookup"><span data-stu-id="b89d1-103">Pin Property Set</span></span>

<span data-ttu-id="b89d1-104">El conjunto de propiedades de pin devuelve la categoría de pin para un pin en un filtro.</span><span class="sxs-lookup"><span data-stu-id="b89d1-104">The pin property set returns the pin category for a pin on a filter.</span></span> <span data-ttu-id="b89d1-105">El filtro establece la categoría cuando crea el pin; la categoría indica qué tipo de datos entrega o recibe este pin.</span><span class="sxs-lookup"><span data-stu-id="b89d1-105">The category is set by the filter when it creates the pin; the category indicates what type of data the pin is delivered or receives by this pin.</span></span>



| <span data-ttu-id="b89d1-106">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="b89d1-106">Label</span></span> | <span data-ttu-id="b89d1-107">Value</span><span class="sxs-lookup"><span data-stu-id="b89d1-107">Value</span></span> |
|-------------------|----------------------|
| <span data-ttu-id="b89d1-108">GUID del conjunto de propiedades</span><span class="sxs-lookup"><span data-stu-id="b89d1-108">Property Set GUID</span></span> | <span data-ttu-id="b89d1-109">**Anclar AMPROPSETID \_**</span><span class="sxs-lookup"><span data-stu-id="b89d1-109">**AMPROPSETID\_Pin**</span></span> |



 



| <span data-ttu-id="b89d1-110">Id. de propiedad</span><span class="sxs-lookup"><span data-stu-id="b89d1-110">Property ID</span></span>                   | <span data-ttu-id="b89d1-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="b89d1-111">Description</span></span>                      |
|-------------------------------|----------------------------------|
| <span data-ttu-id="b89d1-112">**CATEGORÍA DE \_ PIN DE \_ AMPROPERTY**</span><span class="sxs-lookup"><span data-stu-id="b89d1-112">**AMPROPERTY\_PIN\_CATEGORY**</span></span> | <span data-ttu-id="b89d1-113">Especifica la categoría de un pin.</span><span class="sxs-lookup"><span data-stu-id="b89d1-113">Specifies the category of a pin.</span></span> |



 

<span data-ttu-id="b89d1-114">DirectShow define las siguientes categorías de pin en el archivo de encabezado Uuids.h.</span><span class="sxs-lookup"><span data-stu-id="b89d1-114">DirectShow defines the following pin categories in the Uuids.h header file.</span></span>



| <span data-ttu-id="b89d1-115">GUID de categoría</span><span class="sxs-lookup"><span data-stu-id="b89d1-115">Category GUID</span></span>                     | <span data-ttu-id="b89d1-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="b89d1-116">Description</span></span>                                                                                                                                                                                                                                                                                                             |
|-----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b89d1-117">**PIN \_ CATEGORY \_ ANALOGVIDEOIN**</span><span class="sxs-lookup"><span data-stu-id="b89d1-117">**PIN\_CATEGORY\_ANALOGVIDEOIN**</span></span>  | <span data-ttu-id="b89d1-118">Pin de entrada del filtro de captura que toma el análogo y lo digitaliza.</span><span class="sxs-lookup"><span data-stu-id="b89d1-118">Input pin of the capture filter that takes analog and digitizes it.</span></span>                                                                                                                                                                                                                                                     |
| <span data-ttu-id="b89d1-119">**CAPTURA DE \_ CATEGORÍA DE \_ PIN**</span><span class="sxs-lookup"><span data-stu-id="b89d1-119">**PIN\_CATEGORY\_CAPTURE**</span></span>        | <span data-ttu-id="b89d1-120">Pin de captura.</span><span class="sxs-lookup"><span data-stu-id="b89d1-120">Capture pin.</span></span>                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="b89d1-121">**PIN \_ CATEGORY \_ CC**</span><span class="sxs-lookup"><span data-stu-id="b89d1-121">**PIN\_CATEGORY\_CC**</span></span>             | <span data-ttu-id="b89d1-122">Anclar que proporciona datos de subtítulos de la línea 21.</span><span class="sxs-lookup"><span data-stu-id="b89d1-122">Pin providing closed captioning data from Line 21.</span></span>                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="b89d1-123">**PIN \_ CATEGORY \_ EDS**</span><span class="sxs-lookup"><span data-stu-id="b89d1-123">**PIN\_CATEGORY\_EDS**</span></span>            | <span data-ttu-id="b89d1-124">Anclar que proporciona Data Services extendidos (línea 21, incluso campos).</span><span class="sxs-lookup"><span data-stu-id="b89d1-124">Pin providing Extended Data Services (Line 21, even fields).</span></span>                                                                                                                                                                                                                                                            |
| <span data-ttu-id="b89d1-125">**PIN \_ \_ CATEGORYFILES**</span><span class="sxs-lookup"><span data-stu-id="b89d1-125">**PIN\_CATEGORY\_NABTS**</span></span>          | <span data-ttu-id="b89d1-126">Anclar que proporciona datos de North American Videotext Standard.</span><span class="sxs-lookup"><span data-stu-id="b89d1-126">Pin providing North American Videotext Standard data.</span></span>                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="b89d1-127">**PIN \_ CATEGORY \_ PREVIEW**</span><span class="sxs-lookup"><span data-stu-id="b89d1-127">**PIN\_CATEGORY\_PREVIEW**</span></span>        | <span data-ttu-id="b89d1-128">Pin de vista previa.</span><span class="sxs-lookup"><span data-stu-id="b89d1-128">Preview pin.</span></span>                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="b89d1-129">**CATEGORÍA \_ DE PIN \_ TODAVÍA**</span><span class="sxs-lookup"><span data-stu-id="b89d1-129">**PIN\_CATEGORY\_STILL**</span></span>          | <span data-ttu-id="b89d1-130">Anclar que proporciona una imagen fija.</span><span class="sxs-lookup"><span data-stu-id="b89d1-130">Pin that provides a still image.</span></span> <span data-ttu-id="b89d1-131">El pin de captura del filtro debe estar conectado antes de que se conecte el pin de imagen fija.</span><span class="sxs-lookup"><span data-stu-id="b89d1-131">The filter's capture pin must be connected before the still-image pin is connected.</span></span>                                                                                                                                                                                                    |
| <span data-ttu-id="b89d1-132">**PIN \_ CATEGORY \_ TELETEXT**</span><span class="sxs-lookup"><span data-stu-id="b89d1-132">**PIN\_CATEGORY\_TELETEXT**</span></span>       | <span data-ttu-id="b89d1-133">Anclar que proporciona teletexto (una variante de subtítulos).</span><span class="sxs-lookup"><span data-stu-id="b89d1-133">Pin providing teletext (a closed captioning variant).</span></span>                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="b89d1-134">**CÓDIGO \_ DE TIEMPO DE CATEGORÍA DE \_ PIN**</span><span class="sxs-lookup"><span data-stu-id="b89d1-134">**PIN\_CATEGORY\_TIMECODE**</span></span>       | <span data-ttu-id="b89d1-135">Anclar que proporciona datos de código de tiempo.</span><span class="sxs-lookup"><span data-stu-id="b89d1-135">Pin providing timecode data.</span></span>                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="b89d1-136">**CATEGORÍA \_ DE PIN \_ VBI**</span><span class="sxs-lookup"><span data-stu-id="b89d1-136">**PIN\_CATEGORY\_VBI**</span></span>            | <span data-ttu-id="b89d1-137">Anclar que proporciona datos de intervalo de espacios en blanco verticales.</span><span class="sxs-lookup"><span data-stu-id="b89d1-137">Pin providing vertical blanking interval data.</span></span>                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="b89d1-138">**PIN \_ CATEGORY \_ VIDEOPORT**</span><span class="sxs-lookup"><span data-stu-id="b89d1-138">**PIN\_CATEGORY\_VIDEOPORT**</span></span>      | <span data-ttu-id="b89d1-139">Pin de salida de vídeo que se va a conectar al pin de entrada cero en el [mezclador de superposición.](overlay-mixer-filter.md)</span><span class="sxs-lookup"><span data-stu-id="b89d1-139">Video output pin to be connected to input pin zero on the [Overlay Mixer](overlay-mixer-filter.md).</span></span>                                                                                                                                                                                                                    |
| <span data-ttu-id="b89d1-140">**PIN \_ CATEGORY \_ VIDEOPORT \_ VBI**</span><span class="sxs-lookup"><span data-stu-id="b89d1-140">**PIN\_CATEGORY\_VIDEOPORT\_VBI**</span></span> | <span data-ttu-id="b89d1-141">Anclar para conectarse al asignador de superficie de [VBI,](vbi-surface-allocator.md)el filtro de asignador de superficie de VBI necesario para asignar la memoria de vídeo correcta para cosas como superposiciones de subtítulos en escenarios donde se usa un puerto de vídeo.</span><span class="sxs-lookup"><span data-stu-id="b89d1-141">Pin to be connected to the [VBI Surface Allocator](vbi-surface-allocator.md), the VBI surface allocator filter that is needed to allocate the correct video memory for things like closed captioning overlays in scenarios where a video port is being used.</span></span> <span data-ttu-id="b89d1-142">Los escenarios PCI, IEEE 1394 y USB no usan este filtro.</span><span class="sxs-lookup"><span data-stu-id="b89d1-142">PCI, IEEE 1394, and USB scenarios do not use this filter.</span></span> |
| <span data-ttu-id="b89d1-143">**CAPTURA DE \_ CC DE VÍDEO PINNAME \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b89d1-143">**PINNAME\_VIDEO\_CC\_CAPTURE**</span></span>   | <span data-ttu-id="b89d1-144">Patilla de subtítulos de la licación de hardware</span><span class="sxs-lookup"><span data-stu-id="b89d1-144">Hardware slicing closed-captioning pin</span></span>                                                                                                                                                                                                                                                                                  |



 

<span data-ttu-id="b89d1-145">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="b89d1-145">This property is read-only.</span></span>

### <a name="example-code"></a><span data-ttu-id="b89d1-146">Código de ejemplo</span><span class="sxs-lookup"><span data-stu-id="b89d1-146">Example Code</span></span>

<span data-ttu-id="b89d1-147">El código siguiente muestra cómo comprobar si un pin admite este conjunto de propiedades y, si es así, cómo obtener la categoría pin:</span><span class="sxs-lookup"><span data-stu-id="b89d1-147">The following code shows how to check whether a pin supports this property set, and if so, how to obtain the pin category:</span></span>


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
> <span data-ttu-id="b89d1-148">En este ejemplo se usa [la función SafeRelease para](../medfound/saferelease.md) liberar punteros de interfaz.</span><span class="sxs-lookup"><span data-stu-id="b89d1-148">This example uses the [SafeRelease](../medfound/saferelease.md) function to release interface pointers.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="b89d1-149">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b89d1-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b89d1-150">Requisitos de anclar para filtros de captura</span><span class="sxs-lookup"><span data-stu-id="b89d1-150">Pin Requirements for Capture Filters</span></span>](pin-requirements-for-capture-filters.md)
</dt> <dt>

[<span data-ttu-id="b89d1-151">Conjuntos de propiedades</span><span class="sxs-lookup"><span data-stu-id="b89d1-151">Property Sets</span></span>](property-sets.md)
</dt> <dt>

[<span data-ttu-id="b89d1-152">Trabajar con categorías de pin</span><span class="sxs-lookup"><span data-stu-id="b89d1-152">Working with Pin Categories</span></span>](working-with-pin-categories.md)
</dt> </dl>

 

 
