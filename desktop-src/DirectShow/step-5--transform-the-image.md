---
description: Paso 5.
ms.assetid: b7d878ab-523f-4b52-b98d-c9d4fa18ce8a
title: Paso 5. Transformar la imagen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 609acb626d00dbceea8b6f5bca6af012d8158b57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278286"
---
# <a name="step-5-transform-the-image"></a><span data-ttu-id="bbfb3-104">Paso 5.</span><span class="sxs-lookup"><span data-stu-id="bbfb3-104">Step 5.</span></span> <span data-ttu-id="bbfb3-105">Transformar la imagen</span><span class="sxs-lookup"><span data-stu-id="bbfb3-105">Transform the Image</span></span>

<span data-ttu-id="bbfb3-106">Este es el paso 5 del tutorial de [escritura de filtros de transformación](writing-transform-filters.md).</span><span class="sxs-lookup"><span data-stu-id="bbfb3-106">This is step 5 of the tutorial [Writing Transform Filters](writing-transform-filters.md).</span></span>

<span data-ttu-id="bbfb3-107">El filtro de nivel superior proporciona muestras de medios al filtro de transformación mediante una llamada al método [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) en el PIN de entrada del filtro de transformación.</span><span class="sxs-lookup"><span data-stu-id="bbfb3-107">The upstream filter delivers media samples to the transform filter by calling the [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) method on the transform filter's input pin.</span></span> <span data-ttu-id="bbfb3-108">Para procesar los datos, el filtro de transformación llama al método de **transformación** , que es virtual puro.</span><span class="sxs-lookup"><span data-stu-id="bbfb3-108">To process the data, the transform filter calls the **Transform** method, which is pure virtual.</span></span> <span data-ttu-id="bbfb3-109">Las clases **CTransformFilter** y **CTransInPlaceFilter** usan dos versiones diferentes de este método:</span><span class="sxs-lookup"><span data-stu-id="bbfb3-109">The **CTransformFilter** and **CTransInPlaceFilter** classes use two different versions of this method:</span></span>

-   <span data-ttu-id="bbfb3-110">[**CTransformFilter:: transform**](ctransformfilter-transform.md) toma un puntero al ejemplo de entrada y un puntero al ejemplo de salida.</span><span class="sxs-lookup"><span data-stu-id="bbfb3-110">[**CTransformFilter::Transform**](ctransformfilter-transform.md) takes a pointer to the input sample and a pointer to the output sample.</span></span> <span data-ttu-id="bbfb3-111">Antes de que el filtro llame al método, copia las propiedades de ejemplo del ejemplo de entrada en el ejemplo de salida, incluidas las marcas de tiempo.</span><span class="sxs-lookup"><span data-stu-id="bbfb3-111">Before the filter calls the method, it copies the sample properties from the input sample to the output sample, including the time stamps.</span></span>
-   <span data-ttu-id="bbfb3-112">[**CTransInPlaceFilter:: transform**](ctransinplacefilter-transform.md) toma un puntero al ejemplo de entrada.</span><span class="sxs-lookup"><span data-stu-id="bbfb3-112">[**CTransInPlaceFilter::Transform**](ctransinplacefilter-transform.md) takes a pointer to the input sample.</span></span> <span data-ttu-id="bbfb3-113">El filtro modifica los datos en su lugar.</span><span class="sxs-lookup"><span data-stu-id="bbfb3-113">The filter modifies the data in place.</span></span>

<span data-ttu-id="bbfb3-114">Si el método **Transform** devuelve S \_ OK, el filtro entrega el ejemplo de nivel inferior.</span><span class="sxs-lookup"><span data-stu-id="bbfb3-114">If the **Transform** method returns S\_OK, the filter delivers the sample downstream.</span></span> <span data-ttu-id="bbfb3-115">Para omitir un marco, devuelve S \_ false.</span><span class="sxs-lookup"><span data-stu-id="bbfb3-115">To skip a frame, return S\_FALSE.</span></span> <span data-ttu-id="bbfb3-116">Si se produce un error de streaming, devuelva un código de error.</span><span class="sxs-lookup"><span data-stu-id="bbfb3-116">If there is a streaming error, return a failure code.</span></span>

<span data-ttu-id="bbfb3-117">En el ejemplo siguiente se muestra cómo el codificador RLE podría implementar este método.</span><span class="sxs-lookup"><span data-stu-id="bbfb3-117">The following example shows how the RLE encoder might implement this method.</span></span> <span data-ttu-id="bbfb3-118">Su propia implementación podría diferir considerablemente en función de lo que hace el filtro.</span><span class="sxs-lookup"><span data-stu-id="bbfb3-118">Your own implementation might differ considerably, depending on what your filter does.</span></span>


```C++
HRESULT CRleFilter::Transform(IMediaSample *pSource, IMediaSample *pDest)
{
    // Get pointers to the underlying buffers.
    BYTE *pBufferIn, *pBufferOut;
    hr = pSource->GetPointer(&pBufferIn);
    if (FAILED(hr))
    {
        return hr;
    }
    hr = pDest->GetPointer(&pBufferOut);
    if (FAILED(hr))
    {
        return hr;
    }
    // Process the data.
    DWORD cbDest = EncodeFrame(pBufferIn, pBufferOut);
    KASSERT((long)cbDest <= pDest->GetSize());

    pDest->SetActualDataLength(cbDest);
    pDest->SetSyncPoint(TRUE);
    return S_OK;
}
```



<span data-ttu-id="bbfb3-119">En este ejemplo se da por supuesto que EncodeFrame es un método privado que implementa la codificación RLE.</span><span class="sxs-lookup"><span data-stu-id="bbfb3-119">This example assumes that EncodeFrame is a private method that implements the RLE encoding.</span></span> <span data-ttu-id="bbfb3-120">El algoritmo de codificación en sí no se describe aquí. para obtener más información, vea el tema "compresión de mapa de bits" en la documentación de Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="bbfb3-120">The encoding algorithm itself is not described here; for details, see the topic "Bitmap Compression" in the Platform SDK documentation.</span></span>

<span data-ttu-id="bbfb3-121">En primer lugar, el ejemplo llama a [**IMediaSample:: GetPointer**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getpointer) para recuperar las direcciones de los búferes subyacentes.</span><span class="sxs-lookup"><span data-stu-id="bbfb3-121">First, the example calls [**IMediaSample::GetPointer**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getpointer) to retrieve the addresses of the underlying buffers.</span></span> <span data-ttu-id="bbfb3-122">Los pasa al método privado EncoderFrame.</span><span class="sxs-lookup"><span data-stu-id="bbfb3-122">It passes these to the private EncoderFrame method.</span></span> <span data-ttu-id="bbfb3-123">A continuación, llama a [**IMediaSample:: SetActualDataLength**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setactualdatalength) para especificar la longitud de los datos codificados.</span><span class="sxs-lookup"><span data-stu-id="bbfb3-123">Then it calls [**IMediaSample::SetActualDataLength**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setactualdatalength) to specify the length of the encoded data.</span></span> <span data-ttu-id="bbfb3-124">El filtro de nivel inferior necesita esta información para que pueda administrar el búfer correctamente.</span><span class="sxs-lookup"><span data-stu-id="bbfb3-124">The downstream filter needs this information so that it can manage the buffer properly.</span></span> <span data-ttu-id="bbfb3-125">Por último, el método llama a [**IMediaSample:: SetSyncPoint**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setsyncpoint) para establecer la marca de fotograma clave en **true**.</span><span class="sxs-lookup"><span data-stu-id="bbfb3-125">Finally, the method calls [**IMediaSample::SetSyncPoint**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setsyncpoint) to set the key frame flag to **TRUE**.</span></span> <span data-ttu-id="bbfb3-126">La codificación de longitud de ejecución no usa ningún fotograma Delta, por lo que cada fotograma es un fotograma clave.</span><span class="sxs-lookup"><span data-stu-id="bbfb3-126">Run-length encoding does not use any delta frames, so every frame is a key frame.</span></span> <span data-ttu-id="bbfb3-127">En el caso de los fotogramas Delta, establezca el valor en **false**.</span><span class="sxs-lookup"><span data-stu-id="bbfb3-127">For delta frames, set the value to **FALSE**.</span></span>

<span data-ttu-id="bbfb3-128">Otros problemas que debe tener en cuenta son:</span><span class="sxs-lookup"><span data-stu-id="bbfb3-128">Other issues that you must consider include:</span></span>

-   <span data-ttu-id="bbfb3-129">Marcas de tiempo.</span><span class="sxs-lookup"><span data-stu-id="bbfb3-129">Time stamps.</span></span> <span data-ttu-id="bbfb3-130">La clase **CTransformFilter** marca las marcas de tiempo en el ejemplo de salida antes de llamar al método **Transform** .</span><span class="sxs-lookup"><span data-stu-id="bbfb3-130">The **CTransformFilter** class timestamps the output sample before calling the **Transform** method.</span></span> <span data-ttu-id="bbfb3-131">Copia los valores de la marca de tiempo de la muestra de entrada, sin modificarlos.</span><span class="sxs-lookup"><span data-stu-id="bbfb3-131">It copies the time stamp values from the input sample, without modifying them.</span></span> <span data-ttu-id="bbfb3-132">Si el filtro debe cambiar las marcas de tiempo, llame a [**IMediaSample:: setTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-settime) en el ejemplo de salida.</span><span class="sxs-lookup"><span data-stu-id="bbfb3-132">If your filter needs to change the time stamps, call [**IMediaSample::SetTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-settime) on the output sample.</span></span>
-   <span data-ttu-id="bbfb3-133">Cambios de formato.</span><span class="sxs-lookup"><span data-stu-id="bbfb3-133">Format changes.</span></span> <span data-ttu-id="bbfb3-134">El filtro de nivel superior puede cambiar el formato de la secuencia intermedia adjuntando un tipo de medio al ejemplo.</span><span class="sxs-lookup"><span data-stu-id="bbfb3-134">The upstream filter can change formats mid-stream by attaching a media type to the sample.</span></span> <span data-ttu-id="bbfb3-135">Antes de hacerlo, llama a [**IPin:: QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) en el PIN de entrada del filtro.</span><span class="sxs-lookup"><span data-stu-id="bbfb3-135">Before doing so, it calls [**IPin::QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) on your filter's input pin.</span></span> <span data-ttu-id="bbfb3-136">En la clase **CTransformFilter** , esto da como resultado una llamada a **CheckInputType** seguida de **CheckTransform**.</span><span class="sxs-lookup"><span data-stu-id="bbfb3-136">In the **CTransformFilter** class, this results in a call to **CheckInputType** followed by **CheckTransform**.</span></span> <span data-ttu-id="bbfb3-137">El filtro de nivel inferior también puede cambiar los tipos de medios mediante el mismo mecanismo.</span><span class="sxs-lookup"><span data-stu-id="bbfb3-137">The downstream filter can also change media types, using the same mechanism.</span></span> <span data-ttu-id="bbfb3-138">En su propio filtro, hay dos aspectos que se deben tener en cuenta:</span><span class="sxs-lookup"><span data-stu-id="bbfb3-138">In your own filter, there are two things to watch for:</span></span>

    -   <span data-ttu-id="bbfb3-139">Asegúrese de que **QueryAccept** no devuelva la aceptación falsa.</span><span class="sxs-lookup"><span data-stu-id="bbfb3-139">Make sure that **QueryAccept** does not return false acceptances.</span></span>
    -   <span data-ttu-id="bbfb3-140">Si el filtro acepta cambios de formato, compruébelos en el método de **transformación** mediante una llamada a [**IMediaSample:: GetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype).</span><span class="sxs-lookup"><span data-stu-id="bbfb3-140">If your filter does accept format changes, check for them inside the **Transform** method by calling [**IMediaSample::GetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype).</span></span> <span data-ttu-id="bbfb3-141">Si el método devuelve S \_ correcto, el filtro debe responder al cambio de formato.</span><span class="sxs-lookup"><span data-stu-id="bbfb3-141">If that method returns S\_OK, your filter must respond to the format change.</span></span>

    <span data-ttu-id="bbfb3-142">Para obtener más información, consulte [Dynamic Format Changes](dynamic-format-changes.md).</span><span class="sxs-lookup"><span data-stu-id="bbfb3-142">For more information, see [Dynamic Format Changes](dynamic-format-changes.md).</span></span>

-   <span data-ttu-id="bbfb3-143">Subprocesos.</span><span class="sxs-lookup"><span data-stu-id="bbfb3-143">Threads.</span></span> <span data-ttu-id="bbfb3-144">En **CTransformFilter** y **CTransInPlaceFilter**, el filtro de transformación entrega los ejemplos de salida sincrónicamente dentro del método **Receive** .</span><span class="sxs-lookup"><span data-stu-id="bbfb3-144">In both **CTransformFilter** and **CTransInPlaceFilter**, the transform filter delivers output samples synchronously inside the **Receive** method.</span></span> <span data-ttu-id="bbfb3-145">El filtro no crea ningún subproceso de trabajo para procesar los datos.</span><span class="sxs-lookup"><span data-stu-id="bbfb3-145">The filter does not create any worker threads to process the data.</span></span> <span data-ttu-id="bbfb3-146">Normalmente, no hay ningún motivo para que un filtro de transformación cree subprocesos de trabajo.</span><span class="sxs-lookup"><span data-stu-id="bbfb3-146">Typically, there is no reason for a transform filter to create worker threads.</span></span>

<span data-ttu-id="bbfb3-147">Siguiente: [paso 6. Agregar compatibilidad para COM](step-6--add-support-for-com.md).</span><span class="sxs-lookup"><span data-stu-id="bbfb3-147">Next: [Step 6. Add Support for COM](step-6--add-support-for-com.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="bbfb3-148">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="bbfb3-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bbfb3-149">Escribir filtros de DirectShow</span><span class="sxs-lookup"><span data-stu-id="bbfb3-149">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 



