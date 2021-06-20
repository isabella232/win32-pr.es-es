---
description: Elija una clase base como parte de la escritura de un filtro de transformación. Obtenga información sobre qué clases son adecuadas para los filtros de transformación.
ms.assetid: 4b2d3add-0430-480b-ad5f-bb1aa19fef21
title: Paso 1. Elegir una clase base
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1a2bbf704bb2247034bc2ba3a6f35812f46aaaa
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406468"
---
# <a name="step-1-choose-a-base-class"></a><span data-ttu-id="4db1a-105">Paso 1.</span><span class="sxs-lookup"><span data-stu-id="4db1a-105">Step 1.</span></span> <span data-ttu-id="4db1a-106">Elegir una clase base</span><span class="sxs-lookup"><span data-stu-id="4db1a-106">Choose a Base Class</span></span>

<span data-ttu-id="4db1a-107">Este es el paso 1 del tutorial Escribir [filtros de transformación](writing-transform-filters.md).</span><span class="sxs-lookup"><span data-stu-id="4db1a-107">This is step 1 of the tutorial [Writing Transform Filters](writing-transform-filters.md).</span></span>

<span data-ttu-id="4db1a-108">Suponiendo que decide escribir un filtro y no un DMO, el primer paso es elegir qué clase base usar.</span><span class="sxs-lookup"><span data-stu-id="4db1a-108">Assuming that you decide to write a filter and not a DMO, the first step is choosing which base class to use.</span></span> <span data-ttu-id="4db1a-109">Las clases siguientes son adecuadas para los filtros de transformación:</span><span class="sxs-lookup"><span data-stu-id="4db1a-109">The following classes are appropriate for transform filters:</span></span>

-   <span data-ttu-id="4db1a-110">[**CTransformFilter está**](ctransformfilter.md) diseñado para filtros de transformación que usan búferes de entrada y salida independientes.</span><span class="sxs-lookup"><span data-stu-id="4db1a-110">[**CTransformFilter**](ctransformfilter.md) is designed for transform filters that use separate input and output buffers.</span></span> <span data-ttu-id="4db1a-111">Este tipo de filtro a veces se denomina filtro de copia y transformación.</span><span class="sxs-lookup"><span data-stu-id="4db1a-111">This kind of filter is sometimes called a copy-transform filter.</span></span> <span data-ttu-id="4db1a-112">Cuando un filtro de copia y transformación recibe un ejemplo de entrada, escribe nuevos datos en un ejemplo de salida y entrega el ejemplo de salida al filtro siguiente.</span><span class="sxs-lookup"><span data-stu-id="4db1a-112">When a copy-transform filter receives an input sample, it writes new data to an output sample and delivers the output sample to the next filter.</span></span>
-   <span data-ttu-id="4db1a-113">[**CTransInPlaceFilter está**](ctransinplacefilter.md) diseñado para filtros que modifican datos en el búfer original, también denominados filtros trans-in-place.</span><span class="sxs-lookup"><span data-stu-id="4db1a-113">[**CTransInPlaceFilter**](ctransinplacefilter.md) is designed for filters that modify data in the original buffer, also called trans-in-place filters.</span></span> <span data-ttu-id="4db1a-114">Cuando un filtro trans-in-place recibe una muestra, cambia los datos dentro de esa muestra y entrega la misma muestra de bajada.</span><span class="sxs-lookup"><span data-stu-id="4db1a-114">When a trans-in-place filter receives a sample, it changes the data inside that sample and delivers the same sample downstream.</span></span> <span data-ttu-id="4db1a-115">El pin de entrada y el pin de salida del filtro siempre se conectan con los tipos de medios correspondientes.</span><span class="sxs-lookup"><span data-stu-id="4db1a-115">The filter's input pin and output pin always connect with matching media types.</span></span>
-   <span data-ttu-id="4db1a-116">[**CVideoTransformFilter está**](cvideotransformfilter.md) diseñado principalmente para descodificadores de vídeo.</span><span class="sxs-lookup"><span data-stu-id="4db1a-116">[**CVideoTransformFilter**](cvideotransformfilter.md) is designed primarily for video decoders.</span></span> <span data-ttu-id="4db1a-117">Deriva de **CTransformFilter,** pero incluye funcionalidad para quitar fotogramas si el representador de bajada se queda atrás.</span><span class="sxs-lookup"><span data-stu-id="4db1a-117">It derives from **CTransformFilter**, but includes functionality for dropping frames if the downstream renderer falls behind.</span></span>
-   <span data-ttu-id="4db1a-118">[**CBaseFilter es**](cbasefilter.md) una clase de filtro genérica.</span><span class="sxs-lookup"><span data-stu-id="4db1a-118">[**CBaseFilter**](cbasefilter.md) is a generic filter class.</span></span> <span data-ttu-id="4db1a-119">Todas las demás clases de esta lista se derivan **de CBaseFilter.**</span><span class="sxs-lookup"><span data-stu-id="4db1a-119">The other classes in this list all derive from **CBaseFilter**.</span></span> <span data-ttu-id="4db1a-120">Si ninguno de ellos es adecuado, puede volver a usar esta clase.</span><span class="sxs-lookup"><span data-stu-id="4db1a-120">If none of them is suitable, you can fall back on this class.</span></span> <span data-ttu-id="4db1a-121">Sin embargo, esta clase también requiere el mayor trabajo por su parte.</span><span class="sxs-lookup"><span data-stu-id="4db1a-121">However, this class also requires the most work on your part.</span></span>
-   <span data-ttu-id="4db1a-122">\[! Importante\]</span><span class="sxs-lookup"><span data-stu-id="4db1a-122">\[!Important\]</span></span>  
    > <span data-ttu-id="4db1a-123">Las transformaciones de vídeo en su lugar pueden tener un impacto grave en el rendimiento de la representación.</span><span class="sxs-lookup"><span data-stu-id="4db1a-123">In-place video transforms can have a serious impact on rendering performance.</span></span> <span data-ttu-id="4db1a-124">Las transformaciones locales requieren operaciones de lectura, modificación y escritura en el búfer.</span><span class="sxs-lookup"><span data-stu-id="4db1a-124">In-place transforms require read-modify-write operations on the buffer.</span></span> <span data-ttu-id="4db1a-125">Si la memoria reside en una tarjeta gráfica, las operaciones de lectura son significativamente más lentas.</span><span class="sxs-lookup"><span data-stu-id="4db1a-125">If the memory resides on a graphics card, read operations are significantly slower.</span></span> <span data-ttu-id="4db1a-126">Además, incluso una transformación de copia puede provocar operaciones de lectura no deseadas si no la implementa cuidadosamente.</span><span class="sxs-lookup"><span data-stu-id="4db1a-126">Moreover, even a copy transform can cause unintended read operations if you do not implement it carefully.</span></span> <span data-ttu-id="4db1a-127">Por lo tanto, siempre debe realizar pruebas de rendimiento si escribe una transformación de vídeo.</span><span class="sxs-lookup"><span data-stu-id="4db1a-127">Therefore, you should always do performance testing if you write a video transform.</span></span>

     

<span data-ttu-id="4db1a-128">Para el codificador RLE de ejemplo, la mejor opción es **CTransformFilter** o **CVideoTransformFilter.**</span><span class="sxs-lookup"><span data-stu-id="4db1a-128">For the example RLE encoder, the best choice is either **CTransformFilter** or **CVideoTransformFilter**.</span></span> <span data-ttu-id="4db1a-129">De hecho, las diferencias entre ellas son en gran medida internas, por lo que es fácil convertir de una a otra.</span><span class="sxs-lookup"><span data-stu-id="4db1a-129">In fact, the differences between them are largely internal, so it is easy to convert from one to the other.</span></span> <span data-ttu-id="4db1a-130">Dado que los tipos de medios deben ser diferentes en los dos pines, la **clase CTransInPlaceFilter** no es adecuada para este filtro.</span><span class="sxs-lookup"><span data-stu-id="4db1a-130">Because the media types must be different on the two pins, the **CTransInPlaceFilter** class is not appropriate for this filter.</span></span> <span data-ttu-id="4db1a-131">En este ejemplo se **usará CTransformFilter**.</span><span class="sxs-lookup"><span data-stu-id="4db1a-131">This example will use **CTransformFilter**.</span></span>

<span data-ttu-id="4db1a-132">Siguiente: [Paso 2. Declare la clase Filter](step-2--declare-the-filter-class.md).</span><span class="sxs-lookup"><span data-stu-id="4db1a-132">Next: [Step 2. Declare the Filter Class](step-2--declare-the-filter-class.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4db1a-133">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4db1a-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4db1a-134">Escribir filtros de DirectShow</span><span class="sxs-lookup"><span data-stu-id="4db1a-134">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 



