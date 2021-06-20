---
description: Establezca las propiedades del asignador como parte de la escritura de un filtro de transformación. El pin de salida del filtro de transformación selecciona el asignador de nivel inferior.
ms.assetid: c2fd6d8b-b239-45e4-9c02-41edafa58762
title: Paso 4. Establecer propiedades de asignador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9ee7d9ecdc85b63ec6bd774a3a47e0e9399dcf3
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406828"
---
# <a name="step-4-set-allocator-properties"></a><span data-ttu-id="ca812-105">Paso 4.</span><span class="sxs-lookup"><span data-stu-id="ca812-105">Step 4.</span></span> <span data-ttu-id="ca812-106">Establecer propiedades de asignador</span><span class="sxs-lookup"><span data-stu-id="ca812-106">Set Allocator Properties</span></span>

<span data-ttu-id="ca812-107">Este es el paso 4 del tutorial Escribir [filtros de transformación](writing-transform-filters.md).</span><span class="sxs-lookup"><span data-stu-id="ca812-107">This is step 4 of the tutorial [Writing Transform Filters](writing-transform-filters.md).</span></span>

> [!Note]  
> <span data-ttu-id="ca812-108">Este paso no es necesario para los filtros que derivan de **CTransInPlaceFilter.**</span><span class="sxs-lookup"><span data-stu-id="ca812-108">This step is not required for filters that derive from **CTransInPlaceFilter**.</span></span>

 

<span data-ttu-id="ca812-109">Una vez que dos pines coinciden en un tipo de medio, seleccionan un asignador para la conexión y negocian las propiedades del asignador, como el tamaño del búfer y el número de búferes.</span><span class="sxs-lookup"><span data-stu-id="ca812-109">After two pins agree on a media type, they select an allocator for the connection and negotiate allocator properties, such as the buffer size and the number of buffers.</span></span>

<span data-ttu-id="ca812-110">En la **clase CTransformFilter,** hay dos asignadores, uno para la conexión de pin ascendente y otro para la conexión de pin de nivel inferior.</span><span class="sxs-lookup"><span data-stu-id="ca812-110">In the **CTransformFilter** class, there are two allocators, one for the upstream pin connection and one for the downstream pin connection.</span></span> <span data-ttu-id="ca812-111">El filtro ascendente selecciona el asignador ascendente y también elige las propiedades del asignador.</span><span class="sxs-lookup"><span data-stu-id="ca812-111">The upstream filter selects the upstream allocator and also chooses the allocator properties.</span></span> <span data-ttu-id="ca812-112">El pin de entrada acepta lo que decida el filtro ascendente.</span><span class="sxs-lookup"><span data-stu-id="ca812-112">The input pin accepts whatever the upstream filter decides.</span></span> <span data-ttu-id="ca812-113">Si necesita modificar este comportamiento, invalide el [**método CBaseInputPin::NotifyAllocator.**](cbaseinputpin-notifyallocator.md)</span><span class="sxs-lookup"><span data-stu-id="ca812-113">If you need to modify this behavior, override the [**CBaseInputPin::NotifyAllocator**](cbaseinputpin-notifyallocator.md) method.</span></span>

<span data-ttu-id="ca812-114">El pin de salida del filtro de transformación selecciona el asignador de nivel inferior.</span><span class="sxs-lookup"><span data-stu-id="ca812-114">The transform filter's output pin selects the downstream allocator.</span></span> <span data-ttu-id="ca812-115">Realiza los pasos siguientes:</span><span class="sxs-lookup"><span data-stu-id="ca812-115">It performs the following steps:</span></span>

1.  <span data-ttu-id="ca812-116">Si el filtro de nivel inferior puede proporcionar un asignador, el pin de salida usa ese.</span><span class="sxs-lookup"><span data-stu-id="ca812-116">If the downstream filter can provide an allocator, the output pin uses that one.</span></span> <span data-ttu-id="ca812-117">De lo contrario, la patilla de salida crea un nuevo asignador.</span><span class="sxs-lookup"><span data-stu-id="ca812-117">Otherwise, the output pin creates a new allocator.</span></span>
2.  <span data-ttu-id="ca812-118">El pin de salida obtiene los requisitos de asignador del filtro de bajada (si los hay) llamando a [**IMemInputPin::GetAllocatorRequirements**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocatorrequirements).</span><span class="sxs-lookup"><span data-stu-id="ca812-118">The output pin gets the downstream filter's allocator requirements (if any) by calling [**IMemInputPin::GetAllocatorRequirements**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocatorrequirements).</span></span>
3.  <span data-ttu-id="ca812-119">El pin de salida llama al método [**CTransformFilter::D ecideBufferSize**](ctransformfilter-decidebuffersize.md) del filtro de transformación, que es virtual puro.</span><span class="sxs-lookup"><span data-stu-id="ca812-119">The output pin calls the transform filter's [**CTransformFilter::DecideBufferSize**](ctransformfilter-decidebuffersize.md) method, which is pure virtual.</span></span> <span data-ttu-id="ca812-120">Los parámetros de este método son un puntero al asignador y una estructura [**ALLOCATOR \_ PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) con los requisitos del filtro de nivel inferior.</span><span class="sxs-lookup"><span data-stu-id="ca812-120">The parameters to this method are a pointer to the allocator and an [**ALLOCATOR\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) structure with the downstream filter's requirements.</span></span> <span data-ttu-id="ca812-121">Si el filtro de nivel inferior no tiene requisitos de asignador, la estructura se abate a cero.</span><span class="sxs-lookup"><span data-stu-id="ca812-121">If the downstream filter has no allocator requirements, the structure is zeroed out.</span></span>
4.  <span data-ttu-id="ca812-122">En el **método DecideBufferSize,** la clase derivada establece las propiedades del asignador llamando a [**IMemAllocator::SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-setproperties).</span><span class="sxs-lookup"><span data-stu-id="ca812-122">In the **DecideBufferSize** method, the derived class sets the allocator properties by calling [**IMemAllocator::SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-setproperties).</span></span>

<span data-ttu-id="ca812-123">Por lo general, la clase derivada seleccionará las propiedades del asignador en función del formato de salida, los requisitos del filtro de nivel inferior y los propios requisitos del filtro.</span><span class="sxs-lookup"><span data-stu-id="ca812-123">Generally, the derived class will select allocator properties based on the output format, the downstream filter's requirements, and the filter's own requirements.</span></span> <span data-ttu-id="ca812-124">Intente seleccionar las propiedades que son compatibles con la solicitud del filtro de nivel inferior.</span><span class="sxs-lookup"><span data-stu-id="ca812-124">Try to select properties that are compatible with the downstream filter's request.</span></span> <span data-ttu-id="ca812-125">De lo contrario, el filtro de nivel inferior podría rechazar la conexión.</span><span class="sxs-lookup"><span data-stu-id="ca812-125">Otherwise, the downstream filter might reject the connection.</span></span>

<span data-ttu-id="ca812-126">En el ejemplo siguiente, el codificador RLE establece los valores mínimos para el tamaño del búfer, la alineación del búfer y el recuento de búferes.</span><span class="sxs-lookup"><span data-stu-id="ca812-126">In the following example, the RLE encoder sets minimum values for the buffer size, buffer alignment, and buffer count.</span></span> <span data-ttu-id="ca812-127">Para el prefijo, usa cualquier valor que solicite el filtro de bajada.</span><span class="sxs-lookup"><span data-stu-id="ca812-127">For the prefix, it uses whatever value the downstream filter requested.</span></span> <span data-ttu-id="ca812-128">El prefijo suele ser de cero bytes, pero algunos filtros lo requieren.</span><span class="sxs-lookup"><span data-stu-id="ca812-128">The prefix is typically zero bytes, but some filters require it.</span></span> <span data-ttu-id="ca812-129">Por ejemplo, el [filtro AVI Mux](avi-mux-filter.md) usa el prefijo para escribir encabezados RIFF.</span><span class="sxs-lookup"><span data-stu-id="ca812-129">For example, the [AVI Mux](avi-mux-filter.md) filter uses the prefix to write RIFF headers.</span></span>


```C++
HRESULT CRleFilter::DecideBufferSize(
    IMemAllocator *pAlloc, ALLOCATOR_PROPERTIES *pProp)
{
    AM_MEDIA_TYPE mt;
    HRESULT hr = m_pOutput->ConnectionMediaType(&mt);
    if (FAILED(hr))
    {
        return hr;
    }

    ASSERT(mt.formattype == FORMAT_VideoInfo);
    BITMAPINFOHEADER *pbmi = HEADER(mt.pbFormat);
    pProp->cbBuffer = DIBSIZE(*pbmi) * 2; 
    if (pProp->cbAlign == 0)
    {
        pProp->cbAlign = 1;
    }
    if (pProp->cBuffers == 0)
    {
        pProp->cBuffers = 1;
    }
    // Release the format block.
    FreeMediaType(mt);

    // Set allocator properties.
    ALLOCATOR_PROPERTIES Actual;
    hr = pAlloc->SetProperties(pProp, &Actual);
    if (FAILED(hr)) 
    {
        return hr;
    }
    // Even when it succeeds, check the actual result.
    if (pProp->cbBuffer > Actual.cbBuffer) 
    {
        return E_FAIL;
    }
    return S_OK;
}
```



<span data-ttu-id="ca812-130">Es posible que el asignador no pueda coincidir exactamente con la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ca812-130">The allocator may not be able to match your request exactly.</span></span> <span data-ttu-id="ca812-131">Por lo tanto, **el método SetProperties** devuelve el resultado real en una estructura **ALLOCATOR \_ PROPERTIES** independiente (el *parámetro Real,* en el ejemplo anterior).</span><span class="sxs-lookup"><span data-stu-id="ca812-131">Therefore, the **SetProperties** method returns the actual result in a separate **ALLOCATOR\_PROPERTIES** structure (the *Actual* parameter, in the previous example).</span></span> <span data-ttu-id="ca812-132">Incluso cuando **SetProperties se** realiza correctamente, debe comprobar el resultado para asegurarse de que cumplen los requisitos mínimos del filtro.</span><span class="sxs-lookup"><span data-stu-id="ca812-132">Even when **SetProperties** succeeds, you should check the result to make sure they meet your filter's minimum requirements.</span></span>

<span data-ttu-id="ca812-133">**Asignadores personalizados**</span><span class="sxs-lookup"><span data-stu-id="ca812-133">**Custom Allocators**</span></span>

<span data-ttu-id="ca812-134">De forma predeterminada, todas las clases de filtro usan [**la clase CMemAllocator**](cmemallocator.md) para sus asignadores.</span><span class="sxs-lookup"><span data-stu-id="ca812-134">By default, all of the filter classes use the [**CMemAllocator**](cmemallocator.md) class for their allocators.</span></span> <span data-ttu-id="ca812-135">Esta clase asigna memoria desde el espacio de direcciones virtuales del proceso de cliente (mediante **VirtualAlloc**).</span><span class="sxs-lookup"><span data-stu-id="ca812-135">This class allocates memory from the virtual address space of the client process (using **VirtualAlloc**).</span></span> <span data-ttu-id="ca812-136">Si el filtro necesita usar algún otro tipo de memoria, como las superficies de DirectDraw, puede implementar un asignador personalizado.</span><span class="sxs-lookup"><span data-stu-id="ca812-136">If your filter needs to use some other kind of memory, such as DirectDraw surfaces, you can implement a custom allocator.</span></span> <span data-ttu-id="ca812-137">Puede usar la [**clase CBaseAllocator**](cbaseallocator.md) o escribir una clase de asignador completamente nueva.</span><span class="sxs-lookup"><span data-stu-id="ca812-137">You can use the [**CBaseAllocator**](cbaseallocator.md) class or write an entirely new allocator class.</span></span> <span data-ttu-id="ca812-138">Si el filtro tiene un asignador personalizado, invalide los métodos siguientes, en función de qué pin use el asignador:</span><span class="sxs-lookup"><span data-stu-id="ca812-138">If your filter has a custom allocator, override the following methods, depending on which pin uses the allocator:</span></span>

-   <span data-ttu-id="ca812-139">Pin de entrada: [**CBaseInputPin::GetAllocator**](cbaseinputpin-getallocator.md) y [**CBaseInputPin::NotifyAllocator**](cbaseinputpin-notifyallocator.md).</span><span class="sxs-lookup"><span data-stu-id="ca812-139">Input pin: [**CBaseInputPin::GetAllocator**](cbaseinputpin-getallocator.md) and [**CBaseInputPin::NotifyAllocator**](cbaseinputpin-notifyallocator.md).</span></span>
-   <span data-ttu-id="ca812-140">Pin de salida: [**CBaseOutputPin::D ecideAllocator**](cbaseoutputpin-decideallocator.md).</span><span class="sxs-lookup"><span data-stu-id="ca812-140">Output pin: [**CBaseOutputPin::DecideAllocator**](cbaseoutputpin-decideallocator.md).</span></span>

<span data-ttu-id="ca812-141">Si el otro filtro rechaza la conexión mediante el asignador personalizado, el filtro puede producir un error en la conexión o conectarse con el asignador del otro filtro.</span><span class="sxs-lookup"><span data-stu-id="ca812-141">If the other filter refuses to connect using your custom allocator, your filter can either fail the connection, or else connect with the other filter's allocator.</span></span> <span data-ttu-id="ca812-142">En el último caso, es posible que tenga que establecer una marca interna que indique el tipo de asignador.</span><span class="sxs-lookup"><span data-stu-id="ca812-142">In the latter case, you might need to set an internal flag indicating the type of allocator.</span></span> <span data-ttu-id="ca812-143">Para obtener un ejemplo de este enfoque, vea [**CDrawImage (clase).**](cdrawimage.md)</span><span class="sxs-lookup"><span data-stu-id="ca812-143">For an example of this approach, see [**CDrawImage Class**](cdrawimage.md).</span></span>

<span data-ttu-id="ca812-144">Siguiente: [Paso 5. Transforme la imagen](step-5--transform-the-image.md).</span><span class="sxs-lookup"><span data-stu-id="ca812-144">Next: [Step 5. Transform the Image](step-5--transform-the-image.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="ca812-145">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ca812-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ca812-146">Escribir filtros de DirectShow</span><span class="sxs-lookup"><span data-stu-id="ca812-146">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 



