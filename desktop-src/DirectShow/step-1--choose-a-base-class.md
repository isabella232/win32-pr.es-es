---
description: Paso 1.
ms.assetid: 4b2d3add-0430-480b-ad5f-bb1aa19fef21
title: Paso 1. Elegir una clase base
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4679873e78e75b350335b5294db63579fd41f36
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911094"
---
# <a name="step-1-choose-a-base-class"></a><span data-ttu-id="4e6d5-104">Paso 1.</span><span class="sxs-lookup"><span data-stu-id="4e6d5-104">Step 1.</span></span> <span data-ttu-id="4e6d5-105">Elegir una clase base</span><span class="sxs-lookup"><span data-stu-id="4e6d5-105">Choose a Base Class</span></span>

<span data-ttu-id="4e6d5-106">Este es el paso 1 del tutorial de [escritura de filtros de transformación](writing-transform-filters.md).</span><span class="sxs-lookup"><span data-stu-id="4e6d5-106">This is step 1 of the tutorial [Writing Transform Filters](writing-transform-filters.md).</span></span>

<span data-ttu-id="4e6d5-107">Suponiendo que decida escribir un filtro y no un DMO, el primer paso es elegir la clase base que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="4e6d5-107">Assuming that you decide to write a filter and not a DMO, the first step is choosing which base class to use.</span></span> <span data-ttu-id="4e6d5-108">Las siguientes clases son adecuadas para los filtros de transformación:</span><span class="sxs-lookup"><span data-stu-id="4e6d5-108">The following classes are appropriate for transform filters:</span></span>

-   <span data-ttu-id="4e6d5-109">[**CTransformFilter**](ctransformfilter.md) está diseñado para filtros de transformación que utilizan búferes de entrada y salida independientes.</span><span class="sxs-lookup"><span data-stu-id="4e6d5-109">[**CTransformFilter**](ctransformfilter.md) is designed for transform filters that use separate input and output buffers.</span></span> <span data-ttu-id="4e6d5-110">Este tipo de filtro a veces se denomina filtro de copiar y transformar.</span><span class="sxs-lookup"><span data-stu-id="4e6d5-110">This kind of filter is sometimes called a copy-transform filter.</span></span> <span data-ttu-id="4e6d5-111">Cuando un filtro de copia y transformación recibe un ejemplo de entrada, escribe datos nuevos en un ejemplo de salida y entrega el ejemplo de salida al siguiente filtro.</span><span class="sxs-lookup"><span data-stu-id="4e6d5-111">When a copy-transform filter receives an input sample, it writes new data to an output sample and delivers the output sample to the next filter.</span></span>
-   <span data-ttu-id="4e6d5-112">[**CTransInPlaceFilter**](ctransinplacefilter.md) está diseñado para los filtros que modifican los datos en el búfer original, también denominados filtros de transacciones en contexto.</span><span class="sxs-lookup"><span data-stu-id="4e6d5-112">[**CTransInPlaceFilter**](ctransinplacefilter.md) is designed for filters that modify data in the original buffer, also called trans-in-place filters.</span></span> <span data-ttu-id="4e6d5-113">Cuando un filtro de transferencia en contexto recibe un ejemplo, cambia los datos dentro de ese ejemplo y entrega el mismo ejemplo de nivel inferior.</span><span class="sxs-lookup"><span data-stu-id="4e6d5-113">When a trans-in-place filter receives a sample, it changes the data inside that sample and delivers the same sample downstream.</span></span> <span data-ttu-id="4e6d5-114">El PIN de entrada y la salida del filtro siempre se conectan con tipos de medios coincidentes.</span><span class="sxs-lookup"><span data-stu-id="4e6d5-114">The filter's input pin and output pin always connect with matching media types.</span></span>
-   <span data-ttu-id="4e6d5-115">[**CVideoTransformFilter**](cvideotransformfilter.md) está diseñado principalmente para descodificadores de vídeo.</span><span class="sxs-lookup"><span data-stu-id="4e6d5-115">[**CVideoTransformFilter**](cvideotransformfilter.md) is designed primarily for video decoders.</span></span> <span data-ttu-id="4e6d5-116">Se deriva de **CTransformFilter**, pero incluye funcionalidad para quitar fotogramas si el representador de nivel inferior cae por detrás.</span><span class="sxs-lookup"><span data-stu-id="4e6d5-116">It derives from **CTransformFilter**, but includes functionality for dropping frames if the downstream renderer falls behind.</span></span>
-   <span data-ttu-id="4e6d5-117">[**CBaseFilter**](cbasefilter.md) es una clase de filtro genérico.</span><span class="sxs-lookup"><span data-stu-id="4e6d5-117">[**CBaseFilter**](cbasefilter.md) is a generic filter class.</span></span> <span data-ttu-id="4e6d5-118">Todas las demás clases de esta lista se derivan de **CBaseFilter**.</span><span class="sxs-lookup"><span data-stu-id="4e6d5-118">The other classes in this list all derive from **CBaseFilter**.</span></span> <span data-ttu-id="4e6d5-119">Si ninguno de ellos es adecuado, puede revertir a esta clase.</span><span class="sxs-lookup"><span data-stu-id="4e6d5-119">If none of them is suitable, you can fall back on this class.</span></span> <span data-ttu-id="4e6d5-120">Sin embargo, esta clase también requiere el mayor trabajo de su parte.</span><span class="sxs-lookup"><span data-stu-id="4e6d5-120">However, this class also requires the most work on your part.</span></span>
-   <span data-ttu-id="4e6d5-121">\[! Aún\]</span><span class="sxs-lookup"><span data-stu-id="4e6d5-121">\[!Important\]</span></span>  
    > <span data-ttu-id="4e6d5-122">Las transformaciones de vídeo en contexto pueden tener un impacto serio en el rendimiento de la representación.</span><span class="sxs-lookup"><span data-stu-id="4e6d5-122">In-place video transforms can have a serious impact on rendering performance.</span></span> <span data-ttu-id="4e6d5-123">Las transformaciones en contexto requieren operaciones de lectura-modificación-escritura en el búfer.</span><span class="sxs-lookup"><span data-stu-id="4e6d5-123">In-place transforms require read-modify-write operations on the buffer.</span></span> <span data-ttu-id="4e6d5-124">Si la memoria reside en una tarjeta gráfica, las operaciones de lectura son significativamente más lentas.</span><span class="sxs-lookup"><span data-stu-id="4e6d5-124">If the memory resides on a graphics card, read operations are significantly slower.</span></span> <span data-ttu-id="4e6d5-125">Además, incluso una transformación de copia puede producir operaciones de lectura imprevistas si no se implementa con cuidado.</span><span class="sxs-lookup"><span data-stu-id="4e6d5-125">Moreover, even a copy transform can cause unintended read operations if you do not implement it carefully.</span></span> <span data-ttu-id="4e6d5-126">Por lo tanto, siempre debe realizar pruebas de rendimiento si escribe una transformación de vídeo.</span><span class="sxs-lookup"><span data-stu-id="4e6d5-126">Therefore, you should always do performance testing if you write a video transform.</span></span>

     

<span data-ttu-id="4e6d5-127">Para el codificador RLE de ejemplo, la mejor opción es **CTransformFilter** o **CVideoTransformFilter**.</span><span class="sxs-lookup"><span data-stu-id="4e6d5-127">For the example RLE encoder, the best choice is either **CTransformFilter** or **CVideoTransformFilter**.</span></span> <span data-ttu-id="4e6d5-128">De hecho, las diferencias entre ellos son principalmente internas, por lo que es fácil convertir de uno a otro.</span><span class="sxs-lookup"><span data-stu-id="4e6d5-128">In fact, the differences between them are largely internal, so it is easy to convert from one to the other.</span></span> <span data-ttu-id="4e6d5-129">Dado que los tipos de medios deben ser diferentes en los dos PIN, la clase **CTransInPlaceFilter** no es adecuada para este filtro.</span><span class="sxs-lookup"><span data-stu-id="4e6d5-129">Because the media types must be different on the two pins, the **CTransInPlaceFilter** class is not appropriate for this filter.</span></span> <span data-ttu-id="4e6d5-130">En este ejemplo se usará **CTransformFilter**.</span><span class="sxs-lookup"><span data-stu-id="4e6d5-130">This example will use **CTransformFilter**.</span></span>

<span data-ttu-id="4e6d5-131">Siguiente: [paso 2. Declare la clase de filtro](step-2--declare-the-filter-class.md).</span><span class="sxs-lookup"><span data-stu-id="4e6d5-131">Next: [Step 2. Declare the Filter Class](step-2--declare-the-filter-class.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4e6d5-132">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4e6d5-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4e6d5-133">Escribir filtros de DirectShow</span><span class="sxs-lookup"><span data-stu-id="4e6d5-133">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 



