---
description: Paso 4.
ms.assetid: c2fd6d8b-b239-45e4-9c02-41edafa58762
title: Paso 4. Establecer propiedades de asignador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a32d5e3affba32b96dc93cb97e1886322bc6f2c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688226"
---
# <a name="step-4-set-allocator-properties"></a><span data-ttu-id="b8aaf-104">Paso 4.</span><span class="sxs-lookup"><span data-stu-id="b8aaf-104">Step 4.</span></span> <span data-ttu-id="b8aaf-105">Establecer propiedades de asignador</span><span class="sxs-lookup"><span data-stu-id="b8aaf-105">Set Allocator Properties</span></span>

<span data-ttu-id="b8aaf-106">Este es el paso 4 del tutorial de [escritura de filtros de transformación](writing-transform-filters.md).</span><span class="sxs-lookup"><span data-stu-id="b8aaf-106">This is step 4 of the tutorial [Writing Transform Filters](writing-transform-filters.md).</span></span>

> [!Note]  
> <span data-ttu-id="b8aaf-107">Este paso no es necesario para los filtros que derivan de **CTransInPlaceFilter**.</span><span class="sxs-lookup"><span data-stu-id="b8aaf-107">This step is not required for filters that derive from **CTransInPlaceFilter**.</span></span>

 

<span data-ttu-id="b8aaf-108">Una vez que dos clavijas coinciden con un tipo de medio, seleccionan un asignador para la conexión y negocian las propiedades del asignador, como el tamaño del búfer y el número de búferes.</span><span class="sxs-lookup"><span data-stu-id="b8aaf-108">After two pins agree on a media type, they select an allocator for the connection and negotiate allocator properties, such as the buffer size and the number of buffers.</span></span>

<span data-ttu-id="b8aaf-109">En la clase **CTransformFilter** , hay dos asignadores, uno para la conexión de PIN de nivel superior y otro para la conexión de PIN de bajada.</span><span class="sxs-lookup"><span data-stu-id="b8aaf-109">In the **CTransformFilter** class, there are two allocators, one for the upstream pin connection and one for the downstream pin connection.</span></span> <span data-ttu-id="b8aaf-110">El filtro de nivel superior selecciona el asignador de nivel superior y también elige las propiedades de asignador.</span><span class="sxs-lookup"><span data-stu-id="b8aaf-110">The upstream filter selects the upstream allocator and also chooses the allocator properties.</span></span> <span data-ttu-id="b8aaf-111">El PIN de entrada acepta lo que decida el filtro de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="b8aaf-111">The input pin accepts whatever the upstream filter decides.</span></span> <span data-ttu-id="b8aaf-112">Si necesita modificar este comportamiento, invalide el método [**CBaseInputPin:: NotifyAllocator**](cbaseinputpin-notifyallocator.md) .</span><span class="sxs-lookup"><span data-stu-id="b8aaf-112">If you need to modify this behavior, override the [**CBaseInputPin::NotifyAllocator**](cbaseinputpin-notifyallocator.md) method.</span></span>

<span data-ttu-id="b8aaf-113">El PIN de salida del filtro de transformación selecciona el asignador de nivel inferior.</span><span class="sxs-lookup"><span data-stu-id="b8aaf-113">The transform filter's output pin selects the downstream allocator.</span></span> <span data-ttu-id="b8aaf-114">Realiza los pasos siguientes:</span><span class="sxs-lookup"><span data-stu-id="b8aaf-114">It performs the following steps:</span></span>

1.  <span data-ttu-id="b8aaf-115">Si el filtro de nivel inferior puede proporcionar un asignador, el PIN de salida utiliza ese.</span><span class="sxs-lookup"><span data-stu-id="b8aaf-115">If the downstream filter can provide an allocator, the output pin uses that one.</span></span> <span data-ttu-id="b8aaf-116">De lo contrario, el PIN de salida crea un nuevo asignador.</span><span class="sxs-lookup"><span data-stu-id="b8aaf-116">Otherwise, the output pin creates a new allocator.</span></span>
2.  <span data-ttu-id="b8aaf-117">El PIN de salida obtiene los requisitos de asignador del filtro de nivel inferior (si existen) mediante una llamada a [**IMemInputPin:: GetAllocatorRequirements**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocatorrequirements).</span><span class="sxs-lookup"><span data-stu-id="b8aaf-117">The output pin gets the downstream filter's allocator requirements (if any) by calling [**IMemInputPin::GetAllocatorRequirements**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocatorrequirements).</span></span>
3.  <span data-ttu-id="b8aaf-118">El PIN de salida llama al método [**CTransformFilter::D ecidebuffersize**](ctransformfilter-decidebuffersize.md) del filtro de transformación, que es virtual puro.</span><span class="sxs-lookup"><span data-stu-id="b8aaf-118">The output pin calls the transform filter's [**CTransformFilter::DecideBufferSize**](ctransformfilter-decidebuffersize.md) method, which is pure virtual.</span></span> <span data-ttu-id="b8aaf-119">Los parámetros de este método son un puntero al asignador y una estructura de [**\_ propiedades de asignador**](/windows/win32/api/strmif/ns-strmif-allocator_properties) con los requisitos del filtro de nivel inferior.</span><span class="sxs-lookup"><span data-stu-id="b8aaf-119">The parameters to this method are a pointer to the allocator and an [**ALLOCATOR\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) structure with the downstream filter's requirements.</span></span> <span data-ttu-id="b8aaf-120">Si el filtro de nivel inferior no tiene ningún requisito de asignador, la estructura se pone a cero.</span><span class="sxs-lookup"><span data-stu-id="b8aaf-120">If the downstream filter has no allocator requirements, the structure is zeroed out.</span></span>
4.  <span data-ttu-id="b8aaf-121">En el método **DecideBufferSize** , la clase derivada establece las propiedades de asignador llamando a [**IMemAllocator:: SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-setproperties).</span><span class="sxs-lookup"><span data-stu-id="b8aaf-121">In the **DecideBufferSize** method, the derived class sets the allocator properties by calling [**IMemAllocator::SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-setproperties).</span></span>

<span data-ttu-id="b8aaf-122">Por lo general, la clase derivada seleccionará las propiedades de asignador basadas en el formato de salida, los requisitos del filtro de nivel inferior y los propios requisitos del filtro.</span><span class="sxs-lookup"><span data-stu-id="b8aaf-122">Generally, the derived class will select allocator properties based on the output format, the downstream filter's requirements, and the filter's own requirements.</span></span> <span data-ttu-id="b8aaf-123">Intente seleccionar propiedades que sean compatibles con la solicitud del filtro de nivel inferior.</span><span class="sxs-lookup"><span data-stu-id="b8aaf-123">Try to select properties that are compatible with the downstream filter's request.</span></span> <span data-ttu-id="b8aaf-124">De lo contrario, el filtro de nivel inferior podría rechazar la conexión.</span><span class="sxs-lookup"><span data-stu-id="b8aaf-124">Otherwise, the downstream filter might reject the connection.</span></span>

<span data-ttu-id="b8aaf-125">En el ejemplo siguiente, el codificador RLE establece los valores mínimos para el tamaño de búfer, la alineación del búfer y el recuento de búferes.</span><span class="sxs-lookup"><span data-stu-id="b8aaf-125">In the following example, the RLE encoder sets minimum values for the buffer size, buffer alignment, and buffer count.</span></span> <span data-ttu-id="b8aaf-126">Para el prefijo, utiliza el valor que solicitó el filtro de nivel inferior.</span><span class="sxs-lookup"><span data-stu-id="b8aaf-126">For the prefix, it uses whatever value the downstream filter requested.</span></span> <span data-ttu-id="b8aaf-127">Normalmente, el prefijo es de cero bytes, pero algunos filtros lo requieren.</span><span class="sxs-lookup"><span data-stu-id="b8aaf-127">The prefix is typically zero bytes, but some filters require it.</span></span> <span data-ttu-id="b8aaf-128">Por ejemplo, el filtro de [AVI MUX](avi-mux-filter.md) usa el prefijo para escribir encabezados riff.</span><span class="sxs-lookup"><span data-stu-id="b8aaf-128">For example, the [AVI Mux](avi-mux-filter.md) filter uses the prefix to write RIFF headers.</span></span>


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



<span data-ttu-id="b8aaf-129">Es posible que el asignador no pueda coincidir exactamente con la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b8aaf-129">The allocator may not be able to match your request exactly.</span></span> <span data-ttu-id="b8aaf-130">Por lo tanto, el método **SetProperties** devuelve el resultado real en una estructura de **\_ propiedades de asignador** independiente (el parámetro *real* , en el ejemplo anterior).</span><span class="sxs-lookup"><span data-stu-id="b8aaf-130">Therefore, the **SetProperties** method returns the actual result in a separate **ALLOCATOR\_PROPERTIES** structure (the *Actual* parameter, in the previous example).</span></span> <span data-ttu-id="b8aaf-131">Incluso cuando **SetProperties** se realiza correctamente, debe comprobar el resultado para asegurarse de que cumplen los requisitos mínimos del filtro.</span><span class="sxs-lookup"><span data-stu-id="b8aaf-131">Even when **SetProperties** succeeds, you should check the result to make sure they meet your filter's minimum requirements.</span></span>

<span data-ttu-id="b8aaf-132">**Asignadores personalizados**</span><span class="sxs-lookup"><span data-stu-id="b8aaf-132">**Custom Allocators**</span></span>

<span data-ttu-id="b8aaf-133">De forma predeterminada, todas las clases de filtro usan la clase [**CMemAllocator**](cmemallocator.md) para sus asignadores.</span><span class="sxs-lookup"><span data-stu-id="b8aaf-133">By default, all of the filter classes use the [**CMemAllocator**](cmemallocator.md) class for their allocators.</span></span> <span data-ttu-id="b8aaf-134">Esta clase asigna memoria del espacio de direcciones virtuales del proceso del cliente (mediante **VirtualAlloc**).</span><span class="sxs-lookup"><span data-stu-id="b8aaf-134">This class allocates memory from the virtual address space of the client process (using **VirtualAlloc**).</span></span> <span data-ttu-id="b8aaf-135">Si el filtro necesita usar algún otro tipo de memoria, como superficies de DirectDraw, puede implementar un asignador personalizado.</span><span class="sxs-lookup"><span data-stu-id="b8aaf-135">If your filter needs to use some other kind of memory, such as DirectDraw surfaces, you can implement a custom allocator.</span></span> <span data-ttu-id="b8aaf-136">Puede usar la clase [**CBaseAllocator**](cbaseallocator.md) o escribir una clase de asignador completamente nueva.</span><span class="sxs-lookup"><span data-stu-id="b8aaf-136">You can use the [**CBaseAllocator**](cbaseallocator.md) class or write an entirely new allocator class.</span></span> <span data-ttu-id="b8aaf-137">Si el filtro tiene un asignador personalizado, invalide los métodos siguientes, en función del PIN que use el asignador:</span><span class="sxs-lookup"><span data-stu-id="b8aaf-137">If your filter has a custom allocator, override the following methods, depending on which pin uses the allocator:</span></span>

-   <span data-ttu-id="b8aaf-138">PIN de entrada: [**CBaseInputPin:: GetAllocator**](cbaseinputpin-getallocator.md) y [**CBaseInputPin:: NotifyAllocator**](cbaseinputpin-notifyallocator.md).</span><span class="sxs-lookup"><span data-stu-id="b8aaf-138">Input pin: [**CBaseInputPin::GetAllocator**](cbaseinputpin-getallocator.md) and [**CBaseInputPin::NotifyAllocator**](cbaseinputpin-notifyallocator.md).</span></span>
-   <span data-ttu-id="b8aaf-139">PIN de salida: [**CBaseOutputPin::D ecideallocator**](cbaseoutputpin-decideallocator.md).</span><span class="sxs-lookup"><span data-stu-id="b8aaf-139">Output pin: [**CBaseOutputPin::DecideAllocator**](cbaseoutputpin-decideallocator.md).</span></span>

<span data-ttu-id="b8aaf-140">Si el otro filtro se niega a conectar con el asignador personalizado, el filtro puede producir un error en la conexión o conectarse al otro asignador del filtro.</span><span class="sxs-lookup"><span data-stu-id="b8aaf-140">If the other filter refuses to connect using your custom allocator, your filter can either fail the connection, or else connect with the other filter's allocator.</span></span> <span data-ttu-id="b8aaf-141">En el último caso, es posible que tenga que establecer una marca interna que indique el tipo de asignador.</span><span class="sxs-lookup"><span data-stu-id="b8aaf-141">In the latter case, you might need to set an internal flag indicating the type of allocator.</span></span> <span data-ttu-id="b8aaf-142">Para obtener un ejemplo de este enfoque, consulte [**clase CDrawImage**](cdrawimage.md).</span><span class="sxs-lookup"><span data-stu-id="b8aaf-142">For an example of this approach, see [**CDrawImage Class**](cdrawimage.md).</span></span>

<span data-ttu-id="b8aaf-143">Siguiente: [paso 5. Transformar la imagen](step-5--transform-the-image.md).</span><span class="sxs-lookup"><span data-stu-id="b8aaf-143">Next: [Step 5. Transform the Image](step-5--transform-the-image.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b8aaf-144">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b8aaf-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b8aaf-145">Escribir filtros de DirectShow</span><span class="sxs-lookup"><span data-stu-id="b8aaf-145">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 



