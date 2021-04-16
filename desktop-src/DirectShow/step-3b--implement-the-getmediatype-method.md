---
description: Paso 3B.
ms.assetid: 0ec57083-b192-404a-938f-bc6bb1cf0ddb
title: Paso 3B. Implementar el método GetMediaType
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bab3ee41c6740fc2914f943784c0d51116f90428
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104547358"
---
# <a name="step-3b-implement-the-getmediatype-method"></a><span data-ttu-id="8b8d7-104">Paso 3B.</span><span class="sxs-lookup"><span data-stu-id="8b8d7-104">Step 3B.</span></span> <span data-ttu-id="8b8d7-105">Implementar el método GetMediaType</span><span class="sxs-lookup"><span data-stu-id="8b8d7-105">Implement the GetMediaType Method</span></span>

<span data-ttu-id="8b8d7-106">Este es el paso 3B del tutorial de [escritura de filtros de transformación](writing-transform-filters.md).</span><span class="sxs-lookup"><span data-stu-id="8b8d7-106">This is step 3B of the tutorial [Writing Transform Filters](writing-transform-filters.md).</span></span>

> [!Note]  
> <span data-ttu-id="8b8d7-107">Este paso no es necesario para los filtros que derivan de **CTransInPlaceFilter**.</span><span class="sxs-lookup"><span data-stu-id="8b8d7-107">This step is not required for filters that derive from **CTransInPlaceFilter**.</span></span>

 

<span data-ttu-id="8b8d7-108">El método [**CTransformFilter:: GetMediaType**](ctransformfilter-getmediatype.md) devuelve uno de los tipos de salida preferidos del filtro, al que se hace referencia en el número de índice.</span><span class="sxs-lookup"><span data-stu-id="8b8d7-108">The [**CTransformFilter::GetMediaType**](ctransformfilter-getmediatype.md) method returns one of the filter's preferred output types, referenced by index number.</span></span> <span data-ttu-id="8b8d7-109">Nunca se llama a este método a menos que el PIN de entrada del filtro ya esté conectado.</span><span class="sxs-lookup"><span data-stu-id="8b8d7-109">This method is never called unless the filter's input pin is already connected.</span></span> <span data-ttu-id="8b8d7-110">Por lo tanto, puede usar el tipo de medio de la conexión de nivel superior para determinar los tipos de salida preferidos.</span><span class="sxs-lookup"><span data-stu-id="8b8d7-110">Therefore, you can use the media type from the upstream connection to determine the preferred output types.</span></span>

<span data-ttu-id="8b8d7-111">Un codificador suele ofrecer un único tipo preferido que representa el formato de destino.</span><span class="sxs-lookup"><span data-stu-id="8b8d7-111">An encoder typically offers a single preferred type, representing the target format.</span></span> <span data-ttu-id="8b8d7-112">Los descodificadores generalmente admiten una variedad de formatos de salida y los ofrecen en orden de calidad o eficacia descendente.</span><span class="sxs-lookup"><span data-stu-id="8b8d7-112">Decoders generally support a range of output formats, and offer them in order of descending quality or efficiency.</span></span> <span data-ttu-id="8b8d7-113">Por ejemplo, la lista puede ser UYVY, Y211, RGB-24, RGB-565, RGB-555 y RGB-8, en ese orden.</span><span class="sxs-lookup"><span data-stu-id="8b8d7-113">For example, the list might be UYVY, Y211, RGB-24, RGB-565, RGB-555, and RGB-8, in that order.</span></span> <span data-ttu-id="8b8d7-114">Los filtros de efectos pueden requerir una coincidencia exacta entre el formato de salida y el formato de entrada.</span><span class="sxs-lookup"><span data-stu-id="8b8d7-114">Effect filters may require an exact match between the output format and the input format.</span></span>

<span data-ttu-id="8b8d7-115">En el ejemplo siguiente se devuelve un solo tipo de salida, que se construye modificando el tipo de entrada para especificar la compresión RLE8:</span><span class="sxs-lookup"><span data-stu-id="8b8d7-115">The following example returns a single output type, which is constructed by modifying the input type to specify RLE8 compression:</span></span>


```C++
HRESULT CRleFilter::GetMediaType(int iPosition, CMediaType *pMediaType)
{
    ASSERT(m_pInput->IsConnected());
    if (iPosition < 0)
    {
        return E_INVALIDARG;
    }
    if (iPosition == 0)
    {
        HRESULT hr = m_pInput->ConnectionMediaType(pMediaType);
        if (FAILED(hr))
        {
            return hr;
        }
        FOURCCMap fccMap = FCC('MRLE'); 
        pMediaType->subtype = static_cast<GUID>(fccMap);
        pMediaType->SetVariableSize();
        pMediaType->SetTemporalCompression(FALSE);

        ASSERT(pMediaType->formattype == FORMAT_VideoInfo);
        VIDEOINFOHEADER *pVih =
            reinterpret_cast<VIDEOINFOHEADER*>(pMediaType->pbFormat);
        pVih->bmiHeader.biCompression = BI_RLE8;
        pVih->bmiHeader.biSizeImage = DIBSIZE(pVih->bmiHeader); 
        return S_OK;
    }
    // else
    return VFW_S_NO_MORE_ITEMS;
}
```



<span data-ttu-id="8b8d7-116">En este ejemplo, el método llama a [**IPin:: ConnectionMediaType**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectionmediatype) para obtener el tipo de entrada del PIN de entrada.</span><span class="sxs-lookup"><span data-stu-id="8b8d7-116">In this example, the method calls [**IPin::ConnectionMediaType**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectionmediatype) to get the input type from the input pin.</span></span> <span data-ttu-id="8b8d7-117">Después, cambia algunos de los campos para indicar el formato de compresión, como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8b8d7-117">Then it changes some of the fields to indicate the compression format, as follows:</span></span>

-   <span data-ttu-id="8b8d7-118">Asigna un nuevo GUID de subtipo, que se construye a partir del código FOURCC ' MRLE ', mediante la clase [**FOURCCMap**](fourccmap.md) .</span><span class="sxs-lookup"><span data-stu-id="8b8d7-118">It assigns a new subtype GUID, which is constructed from the FOURCC code 'MRLE', using the [**FOURCCMap**](fourccmap.md) class.</span></span>
-   <span data-ttu-id="8b8d7-119">Llama al método [**CMediaType:: SetVariableSize**](cmediatype-setvariablesize.md) , que establece la marca **bFixedSizeSamples** en **false** y el miembro **lSampleSize** en cero, lo que indica ejemplos de tamaño variable.</span><span class="sxs-lookup"><span data-stu-id="8b8d7-119">It calls the [**CMediaType::SetVariableSize**](cmediatype-setvariablesize.md) method, which sets the **bFixedSizeSamples** flag to **FALSE** and the **lSampleSize** member to zero, indicating variable-sized samples.</span></span>
-   <span data-ttu-id="8b8d7-120">Llama al método [**CMediaType:: SetTemporalCompression**](cmediatype-settemporalcompression.md) con el valor **false**, lo que indica que cada fotograma es un fotograma clave.</span><span class="sxs-lookup"><span data-stu-id="8b8d7-120">It calls the [**CMediaType::SetTemporalCompression**](cmediatype-settemporalcompression.md) method with the value **FALSE**, indicating that every frame is a key frame.</span></span> <span data-ttu-id="8b8d7-121">(Este campo es meramente informativo, por lo que puede omitirlo sin ningún riesgo).</span><span class="sxs-lookup"><span data-stu-id="8b8d7-121">(This field is informational only, so you could safely ignore it.)</span></span>
-   <span data-ttu-id="8b8d7-122">Establece el campo **bicompression** en RLE8 de BI \_ .</span><span class="sxs-lookup"><span data-stu-id="8b8d7-122">It sets the **biCompression** field to BI\_RLE8.</span></span>
-   <span data-ttu-id="8b8d7-123">Establece el campo **biSizeImage** en el tamaño de la imagen.</span><span class="sxs-lookup"><span data-stu-id="8b8d7-123">It sets the **biSizeImage** field to the image size.</span></span>

<span data-ttu-id="8b8d7-124">Siguiente: [paso 3C. implemente el método CheckTransform](step-3c--implement-the-checktransform-method.md).</span><span class="sxs-lookup"><span data-stu-id="8b8d7-124">Next: [Step 3C. Implement the CheckTransform Method](step-3c--implement-the-checktransform-method.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="8b8d7-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8b8d7-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8b8d7-126">Escribir filtros de DirectShow</span><span class="sxs-lookup"><span data-stu-id="8b8d7-126">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 



