---
description: Paso 3A.
ms.assetid: 774fcb12-8928-4667-8ef6-dce86717cc29
title: Paso 3A. Implementar el método CheckInputType
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5eb6ff440838d7a4b65b586e5dba963ff254eef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678271"
---
# <a name="step-3a-implement-the-checkinputtype-method"></a><span data-ttu-id="6bc01-104">Paso 3A.</span><span class="sxs-lookup"><span data-stu-id="6bc01-104">Step 3A.</span></span> <span data-ttu-id="6bc01-105">Implementar el método CheckInputType</span><span class="sxs-lookup"><span data-stu-id="6bc01-105">Implement the CheckInputType Method</span></span>

<span data-ttu-id="6bc01-106">Este es el paso 3A del tutorial de [escritura de filtros de transformación](writing-transform-filters.md).</span><span class="sxs-lookup"><span data-stu-id="6bc01-106">This is step 3A of the tutorial [Writing Transform Filters](writing-transform-filters.md).</span></span>

<span data-ttu-id="6bc01-107">Se llama al método [**CTransformFilter:: CheckInputType**](ctransformfilter-checkinputtype.md) cuando el filtro de nivel superior propone un tipo de medio al filtro de transformación.</span><span class="sxs-lookup"><span data-stu-id="6bc01-107">The [**CTransformFilter::CheckInputType**](ctransformfilter-checkinputtype.md) method is called when the upstream filter proposes a media type to the transform filter.</span></span> <span data-ttu-id="6bc01-108">Este método toma un puntero a un objeto [**CMediaType**](cmediatype.md) , que es un contenedor fino para la estructura de [**\_ \_ tipo de medio am**](/windows/win32/api/strmif/ns-strmif-am_media_type) .</span><span class="sxs-lookup"><span data-stu-id="6bc01-108">This method takes a pointer to a [**CMediaType**](cmediatype.md) object, which is a thin wrapper for the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span> <span data-ttu-id="6bc01-109">En este método, debe examinar todos los campos pertinentes de la estructura de **\_ \_ tipo de medio am** , incluidos los campos del bloque de formato.</span><span class="sxs-lookup"><span data-stu-id="6bc01-109">In this method, you should examine every relevant field of the **AM\_MEDIA\_TYPE** structure, including the fields in the format block.</span></span> <span data-ttu-id="6bc01-110">Puede usar los métodos de descriptor de acceso definidos en **CMediaType** o hacer referencia a los miembros de la estructura directamente.</span><span class="sxs-lookup"><span data-stu-id="6bc01-110">You can use the accessor methods defined in **CMediaType**, or reference the structure members directly.</span></span> <span data-ttu-id="6bc01-111">Si un campo no es válido, devuelve el \_ tipo VFW E \_ \_ no \_ aceptado.</span><span class="sxs-lookup"><span data-stu-id="6bc01-111">If any field is not valid, return VFW\_E\_TYPE\_NOT\_ACCEPTED.</span></span> <span data-ttu-id="6bc01-112">Si el tipo de medio completo es válido, devuelva S \_ correctos.</span><span class="sxs-lookup"><span data-stu-id="6bc01-112">If the entire media type is valid, return S\_OK.</span></span>

<span data-ttu-id="6bc01-113">Por ejemplo, en el filtro del codificador RLE, el tipo de entrada debe ser vídeo RGB sin comprimir de 8 bits o de 4 bits.</span><span class="sxs-lookup"><span data-stu-id="6bc01-113">For example, in the RLE encoder filter, the input type must be 8-bit or 4-bit uncompressed RGB video.</span></span> <span data-ttu-id="6bc01-114">No hay ninguna razón para admitir otros formatos de entrada, como RGB de 16 o 24 bits, ya que el filtro tendría que convertirlos a una profundidad de bits más baja y DirectShow ya proporciona un filtro de [convertidor de espacio de colores](color-space-converter-filter.md) para ese propósito.</span><span class="sxs-lookup"><span data-stu-id="6bc01-114">There is no reason to support other input formats, such as 16- or 24-bit RGB, because the filter would have to convert them to a lower bit depth, and DirectShow already provides a [Color Space Converter](color-space-converter-filter.md) filter for that purpose.</span></span> <span data-ttu-id="6bc01-115">En el ejemplo siguiente se da por supuesto que el codificador admite vídeo de 8 bits, pero no vídeo de 4 bits:</span><span class="sxs-lookup"><span data-stu-id="6bc01-115">The following example assumes that the encoder supports 8-bit video but not 4-bit video:</span></span>


```C++
HRESULT CRleFilter::CheckInputType(const CMediaType *mtIn)
{
    if ((mtIn->majortype != MEDIATYPE_Video) ||
        (mtIn->subtype != MEDIASUBTYPE_RGB8) ||
        (mtIn->formattype != FORMAT_VideoInfo) || 
        (mtIn->cbFormat < sizeof(VIDEOINFOHEADER)))
    {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }

    VIDEOINFOHEADER *pVih = 
        reinterpret_cast<VIDEOINFOHEADER*>(mtIn->pbFormat);
    if ((pVih->bmiHeader.biBitCount != 8) ||
        (pVih->bmiHeader.biCompression != BI_RGB))
    {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }

    // Check the palette table.
    if (pVih->bmiHeader.biClrUsed > PALETTE_ENTRIES(pVih))
    {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }
    DWORD cbPalette = pVih->bmiHeader.biClrUsed * sizeof(RGBQUAD);
    if (mtIn->cbFormat < sizeof(VIDEOINFOHEADER) + cbPalette)
    {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }

    // Everything is good.
    return S_OK;
}
```



<span data-ttu-id="6bc01-116">En este ejemplo, el método comprueba primero el tipo y el subtipo principales.</span><span class="sxs-lookup"><span data-stu-id="6bc01-116">In this example, the method first checks the major type and subtype.</span></span> <span data-ttu-id="6bc01-117">A continuación, comprueba el tipo de formato para asegurarse de que el bloque de formato es una estructura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) .</span><span class="sxs-lookup"><span data-stu-id="6bc01-117">Then it checks the format type, to make sure the format block is a [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure.</span></span> <span data-ttu-id="6bc01-118">El filtro también podría admitir [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2), pero en este caso no sería ninguna ventaja real.</span><span class="sxs-lookup"><span data-stu-id="6bc01-118">The filter could also support [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2), but in this case there would be no real benefit.</span></span> <span data-ttu-id="6bc01-119">La estructura **VIDEOINFOHEADER2** agrega compatibilidad con el entrelazado y los píxeles no cuadrados, que es probable que no sean relevantes en el vídeo de 8 bits.</span><span class="sxs-lookup"><span data-stu-id="6bc01-119">The **VIDEOINFOHEADER2** structure adds support for interlacing and non-square pixels, which are not likely to be relevant in 8-bit video.</span></span>

<span data-ttu-id="6bc01-120">Si el tipo de formato es correcto, en el ejemplo se comprueban los miembros **biBitCount** y **bicompression** de la estructura **VIDEOINFOHEADER** para comprobar que el formato es RGB sin comprimir de 8 bits.</span><span class="sxs-lookup"><span data-stu-id="6bc01-120">If the format type is correct, the example checks the **biBitCount** and **biCompression** members of the **VIDEOINFOHEADER** structure, to verify that the format is 8-bit uncompressed RGB.</span></span> <span data-ttu-id="6bc01-121">Como se muestra en este ejemplo, debe forzar el</span><span class="sxs-lookup"><span data-stu-id="6bc01-121">As this example shows, you must coerce the</span></span>


```C++
pbFormat
```



<span data-ttu-id="6bc01-122">puntero a la estructura correcta, en función del tipo de formato.</span><span class="sxs-lookup"><span data-stu-id="6bc01-122">pointer to the correct structure, based on the format type.</span></span> <span data-ttu-id="6bc01-123">Compruebe siempre el GUID de tipo de formato (**formatType**) y el tamaño del bloque de formato (**cbFormat**) antes de convertir el puntero.</span><span class="sxs-lookup"><span data-stu-id="6bc01-123">Always check the format type GUID (**formattype**) and the size of the format block (**cbFormat**) before casting the pointer.</span></span>

<span data-ttu-id="6bc01-124">En el ejemplo también se comprueba que el número de entradas de la paleta es compatible con la profundidad de bits y que el bloque de formato es lo suficientemente grande como para contener las entradas de la paleta.</span><span class="sxs-lookup"><span data-stu-id="6bc01-124">The example also verifies that the number of palette entries is compatible with the bit depth and the format block is large enough to hold the palette entries.</span></span> <span data-ttu-id="6bc01-125">Si toda esta información es correcta, el método devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="6bc01-125">If all of this information is correct, the method returns S\_OK.</span></span>

<span data-ttu-id="6bc01-126">Siguiente: [paso 3B. implemente el método GetMediaType](step-3b--implement-the-getmediatype-method.md).</span><span class="sxs-lookup"><span data-stu-id="6bc01-126">Next: [Step 3B. Implement the GetMediaType Method](step-3b--implement-the-getmediatype-method.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="6bc01-127">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6bc01-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6bc01-128">Escribir filtros de DirectShow</span><span class="sxs-lookup"><span data-stu-id="6bc01-128">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 



