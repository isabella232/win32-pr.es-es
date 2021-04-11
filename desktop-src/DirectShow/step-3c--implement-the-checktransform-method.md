---
description: Paso 3C.
ms.assetid: e780df46-bf47-4334-b788-05ad8179f051
title: Paso 3C. Implementar el método CheckTransform
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78148701fc54e73a6970d45fde95d70f4cf0df3a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278825"
---
# <a name="step-3c-implement-the-checktransform-method"></a><span data-ttu-id="1ff78-104">Paso 3C.</span><span class="sxs-lookup"><span data-stu-id="1ff78-104">Step 3C.</span></span> <span data-ttu-id="1ff78-105">Implementar el método CheckTransform</span><span class="sxs-lookup"><span data-stu-id="1ff78-105">Implement the CheckTransform Method</span></span>

<span data-ttu-id="1ff78-106">Este es el paso 3C del tutorial [Writing Transform filters](writing-transform-filters.md).</span><span class="sxs-lookup"><span data-stu-id="1ff78-106">This is step 3C of the tutorial [Writing Transform Filters](writing-transform-filters.md).</span></span>

> [!Note]  
> <span data-ttu-id="1ff78-107">Este paso no es necesario para los filtros que derivan de **CTransInPlaceFilter**.</span><span class="sxs-lookup"><span data-stu-id="1ff78-107">This step is not required for filters that derive from **CTransInPlaceFilter**.</span></span>

 

<span data-ttu-id="1ff78-108">El método [**CTransformFilter:: CheckTransform**](ctransformfilter-checktransform.md) comprueba si un tipo de resultado propuesto es compatible con el tipo de entrada actual.</span><span class="sxs-lookup"><span data-stu-id="1ff78-108">The [**CTransformFilter::CheckTransform**](ctransformfilter-checktransform.md) method checks if a proposed output type is compatible with the current input type.</span></span> <span data-ttu-id="1ff78-109">También se llama al método si el PIN de entrada se vuelve a conectar después de que se conecte el PIN de salida.</span><span class="sxs-lookup"><span data-stu-id="1ff78-109">The method is also called if the input pin reconnects after the output pin connects.</span></span>

<span data-ttu-id="1ff78-110">En el ejemplo siguiente se comprueba si el formato es RLE8 video; las dimensiones de la imagen coinciden con el formato de entrada; y las entradas de la paleta son las mismas.</span><span class="sxs-lookup"><span data-stu-id="1ff78-110">The following example verifies whether the format is RLE8 video; the image dimensions match the input format; and the palette entries are the same.</span></span> <span data-ttu-id="1ff78-111">También rechaza los rectángulos de origen y de destino que no coinciden con el tamaño de la imagen.</span><span class="sxs-lookup"><span data-stu-id="1ff78-111">It also rejects source and target rectangles that do not match the image size.</span></span>


```C++
HRESULT CRleFilter::CheckTransform(
    const CMediaType *mtIn, const CMediaType *mtOut)
{
    // Check the major type.
    if (mtOut->majortype != MEDIATYPE_Video)
    {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }

    // Check the subtype and format type.
    FOURCCMap fccMap = FCC('MRLE'); 
    if (mtOut->subtype != static_cast<GUID>(fccMap))
    {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }
    if ((mtOut->formattype != FORMAT_VideoInfo) || 
        (mtOut->cbFormat < sizeof(VIDEOINFOHEADER)))
    {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }

    // Compare the bitmap information against the input type.
    ASSERT(mtIn->formattype == FORMAT_VideoInfo);
    BITMAPINFOHEADER *pBmiOut = HEADER(mtOut->pbFormat);
    BITMAPINFOHEADER *pBmiIn = HEADER(mtIn->pbFormat);
    if ((pBmiOut->biPlanes != 1) ||
        (pBmiOut->biBitCount != 8) ||
        (pBmiOut->biCompression != BI_RLE8) ||
        (pBmiOut->biWidth != pBmiIn->biWidth) ||
        (pBmiOut->biHeight != pBmiIn->biHeight))
    {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }

    // Compare source and target rectangles.
    RECT rcImg;
    SetRect(&rcImg, 0, 0, pBmiIn->biWidth, pBmiIn->biHeight);
    RECT *prcSrc = &((VIDEOINFOHEADER*)(mtIn->pbFormat))->rcSource;
    RECT *prcTarget = &((VIDEOINFOHEADER*)(mtOut->pbFormat))->rcTarget;
    if (!IsRectEmpty(prcSrc) && !EqualRect(prcSrc, &rcImg))
    {
        return VFW_E_INVALIDMEDIATYPE;
    }
    if (!IsRectEmpty(prcTarget) && !EqualRect(prcTarget, &rcImg))
    {
        return VFW_E_INVALIDMEDIATYPE;
    }

    // Check the palette table.
    if (pBmiOut->biClrUsed != pBmiIn->biClrUsed)
    {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }
    DWORD cbPalette = pBmiOut->biClrUsed * sizeof(RGBQUAD);
    if (mtOut->cbFormat < sizeof(VIDEOINFOHEADER) + cbPalette)
    {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }
    if (0 != memcmp(pBmiOut + 1, pBmiIn + 1, cbPalette))
    {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }

    // Everything is good.
    return S_OK;
}
```



<span data-ttu-id="1ff78-112">**Anclar reconexiones**</span><span class="sxs-lookup"><span data-stu-id="1ff78-112">**Pin Reconnections**</span></span>

<span data-ttu-id="1ff78-113">Las aplicaciones pueden desconectarse y volver a conectarse.</span><span class="sxs-lookup"><span data-stu-id="1ff78-113">Applications can disconnect and reconnect pins.</span></span> <span data-ttu-id="1ff78-114">Supongamos que una aplicación conecta ambos PIN, desconecta el PIN de entrada y, a continuación, vuelve a conectar el PIN de entrada con un nuevo tamaño de imagen.</span><span class="sxs-lookup"><span data-stu-id="1ff78-114">Suppose an application connects both pins, disconnects the input pin, and then reconnects the input pin using a new image size.</span></span> <span data-ttu-id="1ff78-115">En ese caso, **CheckTransform** produce un error porque las dimensiones de la imagen ya no coinciden.</span><span class="sxs-lookup"><span data-stu-id="1ff78-115">In that case, **CheckTransform** fails because the dimensions of the image no longer match.</span></span> <span data-ttu-id="1ff78-116">Este comportamiento es razonable, aunque el filtro también podría intentar volver a conectar el PIN de salida con un nuevo tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="1ff78-116">This behavior is reasonable, although the filter could also try reconnecting the output pin with a new media type.</span></span>

<span data-ttu-id="1ff78-117">Siguiente: [paso 4. Establecer propiedades de asignador](step-4--set-allocator-properties.md).</span><span class="sxs-lookup"><span data-stu-id="1ff78-117">Next: [Step 4. Set Allocator Properties](step-4--set-allocator-properties.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="1ff78-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1ff78-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1ff78-119">Volver a conectar PIN</span><span class="sxs-lookup"><span data-stu-id="1ff78-119">Reconnecting Pins</span></span>](reconnecting-pins.md)
</dt> <dt>

[<span data-ttu-id="1ff78-120">Rectángulos de origen y de destino en representadores de vídeo</span><span class="sxs-lookup"><span data-stu-id="1ff78-120">Source and Target Rectangles in Video Renderers</span></span>](source-and-target-rectangles-in-video-renderers.md)
</dt> <dt>

[<span data-ttu-id="1ff78-121">Escribir filtros de DirectShow</span><span class="sxs-lookup"><span data-stu-id="1ff78-121">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 



