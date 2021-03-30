---
description: QueryAccept (ascendente)
ms.assetid: 3153e3a4-2227-4fdd-b2b0-218763013d2d
title: QueryAccept (ascendente)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7707c52d36c3d065c4a7277939f724aabdb73e46
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103806470"
---
# <a name="queryaccept-upstream"></a><span data-ttu-id="c05c7-103">QueryAccept (ascendente)</span><span class="sxs-lookup"><span data-stu-id="c05c7-103">QueryAccept (Upstream)</span></span>

<span data-ttu-id="c05c7-104">Este mecanismo permite a un PIN de entrada proponer un cambio de formato a su elemento del mismo nivel de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="c05c7-104">This mechanism enables an input pin to propose a format change to its upstream peer.</span></span> <span data-ttu-id="c05c7-105">El filtro de nivel inferior debe asociar un tipo de medio al ejemplo que el filtro ascendente obtendrá en la siguiente llamada a [**IMemAllocator:: getBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer).</span><span class="sxs-lookup"><span data-stu-id="c05c7-105">The downstream filter must attach a media type to the sample that the upstream filter will obtain in its next call to [**IMemAllocator::GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer).</span></span> <span data-ttu-id="c05c7-106">Para ello, sin embargo, el filtro de nivel inferior debe proporcionar un asignador personalizado para la conexión.</span><span class="sxs-lookup"><span data-stu-id="c05c7-106">In order to do this, however, the downstream filter must provide a custom allocator for the connection.</span></span> <span data-ttu-id="c05c7-107">Este asignador debe implementar un método privado que el filtro de nivel inferior pueda utilizar para establecer el tipo de medio en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="c05c7-107">This allocator must implement a private method that the downstream filter can use to set the media type on the next sample.</span></span>

<span data-ttu-id="c05c7-108">Tienen lugar los pasos siguientes:</span><span class="sxs-lookup"><span data-stu-id="c05c7-108">The following steps occur:</span></span>

1.  <span data-ttu-id="c05c7-109">El filtro de nivel inferior comprueba si la conexión del PIN utiliza el asignador personalizado del filtro.</span><span class="sxs-lookup"><span data-stu-id="c05c7-109">The downstream filter checks whether the pin connection uses the filter's custom allocator.</span></span> <span data-ttu-id="c05c7-110">Si el filtro de nivel superior posee el asignador, el filtro de nivel inferior no puede cambiar el formato.</span><span class="sxs-lookup"><span data-stu-id="c05c7-110">If the upstream filter owns the allocator, the downstream filter cannot change the format.</span></span>
2.  <span data-ttu-id="c05c7-111">El filtro de nivel inferior llama a [**IPin:: QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) en el PIN de salida ascendente (vea la ilustración, paso A).</span><span class="sxs-lookup"><span data-stu-id="c05c7-111">The downstream filter calls [**IPin::QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) on the upstream output pin (see illustration, step A).</span></span>
3.  <span data-ttu-id="c05c7-112">Si `QueryAccept` devuelve S \_ OK, el filtro de nivel inferior llama al método privado en su asignador para establecer el tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="c05c7-112">If `QueryAccept` returns S\_OK, the downstream filter calls the private method on its allocator in order to set the media type.</span></span> <span data-ttu-id="c05c7-113">Dentro de este método privado, el asignador llama a [**IMediaSample:: SetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setmediatype) en el siguiente ejemplo disponible (B).</span><span class="sxs-lookup"><span data-stu-id="c05c7-113">Within this private method, the allocator calls [**IMediaSample::SetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setmediatype) on the next available sample (B).</span></span>
4.  <span data-ttu-id="c05c7-114">El filtro de nivel superior llama a **getBuffer** para obtener un nuevo ejemplo (C) y [**IMediaSample:: GetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype) para obtener el tipo de medio (D).</span><span class="sxs-lookup"><span data-stu-id="c05c7-114">The upstream filter calls **GetBuffer** to get a new sample (C) and [**IMediaSample::GetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype) to get the media type (D).</span></span>
5.  <span data-ttu-id="c05c7-115">Cuando el filtro de nivel superior entrega el ejemplo, debe dejar el tipo de medio asociado a ese ejemplo.</span><span class="sxs-lookup"><span data-stu-id="c05c7-115">When the upstream filter delivers the sample, it should leave the media type attached to that sample.</span></span> <span data-ttu-id="c05c7-116">De este modo, el filtro de nivel inferior puede confirmar que el tipo de medio ha cambiado (E).</span><span class="sxs-lookup"><span data-stu-id="c05c7-116">That way, the downstream filter can confirm that the media type has changed (E).</span></span>

<span data-ttu-id="c05c7-117">Si el filtro de nivel superior acepta el cambio de formato, también debe poder volver al tipo de medio original, como se muestra en el diagrama siguiente.</span><span class="sxs-lookup"><span data-stu-id="c05c7-117">If the upstream filter accepts the format change, it must also be able to switch back to the original media type, as shown in the following diagram.</span></span>

![queryaccept (ascendente)](images/dynformat4.png)

<span data-ttu-id="c05c7-119">Los principales ejemplos de este tipo de cambio de formato implican los representadores de vídeo de DirectShow.</span><span class="sxs-lookup"><span data-stu-id="c05c7-119">The main examples of this kind of format change involve the DirectShow video renderers.</span></span>

-   <span data-ttu-id="c05c7-120">El filtro de [representador de vídeo](video-renderer-filter.md) original puede cambiar entre los tipos RGB y YUV durante el streaming.</span><span class="sxs-lookup"><span data-stu-id="c05c7-120">The original [Video Renderer](video-renderer-filter.md) filter can switch between RGB and YUV types during streaming.</span></span> <span data-ttu-id="c05c7-121">Cuando el filtro se conecta, requiere un formato RGB que coincida con la configuración de pantalla actual.</span><span class="sxs-lookup"><span data-stu-id="c05c7-121">When the filter connects, it requires an RGB format that matches the current display settings.</span></span> <span data-ttu-id="c05c7-122">Esto garantiza que puede revertirse en GDI si es necesario.</span><span class="sxs-lookup"><span data-stu-id="c05c7-122">This guarantees that it can fall back on GDI if it needs to.</span></span> <span data-ttu-id="c05c7-123">Una vez que se inicia el streaming, si DirectDraw está disponible, el representador de vídeo solicita un cambio de formato a un tipo YUV.</span><span class="sxs-lookup"><span data-stu-id="c05c7-123">After streaming begins, if DirectDraw is available, the Video Renderer requests a format change to a YUV type.</span></span> <span data-ttu-id="c05c7-124">Más adelante, podría volver a RGB si pierde la superficie DirectDraw por cualquier motivo.</span><span class="sxs-lookup"><span data-stu-id="c05c7-124">Later, it might switch back to RGB if it loses the DirectDraw surface for any reason.</span></span>
-   <span data-ttu-id="c05c7-125">El filtro de representador de mezcla de vídeo (VMR) más reciente se conectará con cualquier formato compatible con el hardware gráfico, incluidos los tipos YUV.</span><span class="sxs-lookup"><span data-stu-id="c05c7-125">The newer Video Mixing Renderer (VMR) filter will connect with any format that is supported by the graphics hardware, including YUV types.</span></span> <span data-ttu-id="c05c7-126">Sin embargo, el hardware gráfico podría cambiar el intervalo de la superficie de DirectDraw subyacente para optimizar el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="c05c7-126">However, the graphics hardware might change the stride of the underlying DirectDraw surface in order to optimize performance.</span></span> <span data-ttu-id="c05c7-127">El filtro VMR utiliza `QueryAccept` para notificar el nuevo STRIDE, que se especifica en el miembro **biwidth** de la estructura **BITMAPINFOHEADER** .</span><span class="sxs-lookup"><span data-stu-id="c05c7-127">The VMR filter uses `QueryAccept` to report the new stride, which is specified in the **biWidth** member of the **BITMAPINFOHEADER** structure.</span></span> <span data-ttu-id="c05c7-128">Los rectángulos de origen y de destino de la estructura **VIDEOINFOHEADER** o **VIDEOINFOHEADER2** identifican la región en la que se debe descodificar el vídeo.</span><span class="sxs-lookup"><span data-stu-id="c05c7-128">The source and target rectangles in the **VIDEOINFOHEADER** or **VIDEOINFOHEADER2** structure identify the region where the video should be decoded.</span></span>

<span data-ttu-id="c05c7-129">**Nota de implementación**</span><span class="sxs-lookup"><span data-stu-id="c05c7-129">**Implementation Note**</span></span>

<span data-ttu-id="c05c7-130">Es poco probable que escriba un filtro que necesite solicitar cambios en el formato ascendente, ya que se trata principalmente de una característica de los representadores de vídeo.</span><span class="sxs-lookup"><span data-stu-id="c05c7-130">It is unlikely that you will write a filter that needs to request upstream format changes, since this is mainly a feature of video renderers.</span></span> <span data-ttu-id="c05c7-131">Sin embargo, si escribe un filtro de transformación de vídeo o un descodificador de vídeo, el filtro debe responder correctamente a las solicitudes del representador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="c05c7-131">However, if you write a video transform filter or a video decoder, your filter must respond correctly to requests from the video renderer.</span></span>

<span data-ttu-id="c05c7-132">Un filtro de transacciones que se encuentra entre el representador de vídeo y el descodificador debe pasar todas las `QueryAccept` llamadas de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="c05c7-132">A trans-in-place filter that sits between the video renderer and the decoder should pass all `QueryAccept` calls upstream.</span></span> <span data-ttu-id="c05c7-133">Almacene la nueva información de formato cuando llegue.</span><span class="sxs-lookup"><span data-stu-id="c05c7-133">Store the new format information when it arrives.</span></span>

<span data-ttu-id="c05c7-134">Un filtro de copia y transformación (es decir, un filtro que no es trans-in situ) debe implementar uno de los siguientes comportamientos:</span><span class="sxs-lookup"><span data-stu-id="c05c7-134">A copy-transform filter (that is, a non-trans-in-place filter) should implement one of the following behaviors:</span></span>

-   <span data-ttu-id="c05c7-135">Los cambios de formato de paso ascendente y almacenan la nueva información de formato cuando llega.</span><span class="sxs-lookup"><span data-stu-id="c05c7-135">Pass format changes upstream and store the new format information when it arrives.</span></span> <span data-ttu-id="c05c7-136">El filtro debe utilizar un asignador personalizado para que pueda adjuntar el formato al ejemplo de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="c05c7-136">Your filter must use a custom allocator so that it can attach the format to the upstream sample.</span></span>
-   <span data-ttu-id="c05c7-137">Realice la conversión de formato dentro del filtro.</span><span class="sxs-lookup"><span data-stu-id="c05c7-137">Perform the format conversion inside the filter.</span></span> <span data-ttu-id="c05c7-138">Esto es probablemente más fácil que pasar el cambio de formato de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="c05c7-138">This is probably easier than passing the format change upstream.</span></span> <span data-ttu-id="c05c7-139">Sin embargo, puede ser menos eficaz que dejar que el filtro del descodificador se descodifique en el formato correcto.</span><span class="sxs-lookup"><span data-stu-id="c05c7-139">However, it might be less efficient than letting the decoder filter decode into the correct format.</span></span>
-   <span data-ttu-id="c05c7-140">Como último recurso, simplemente rechace el cambio de formato.</span><span class="sxs-lookup"><span data-stu-id="c05c7-140">As a last resort, simply reject the format change.</span></span> <span data-ttu-id="c05c7-141">(Para obtener más información, consulte el código fuente para el método [**CTransInPlaceOutputPin:: CheckMediaType**](ctransinplaceoutputpin-checkmediatype.md) en la biblioteca de clases base de DirectShow). Sin embargo, el rechazo de un cambio de formato puede reducir el rendimiento, ya que impide que el representador de vídeo use el formato más eficaz.</span><span class="sxs-lookup"><span data-stu-id="c05c7-141">(For more information, refer to the source code for the [**CTransInPlaceOutputPin::CheckMediaType**](ctransinplaceoutputpin-checkmediatype.md) method in the DirectShow base class library.) Rejecting a format change can reduce performance, however, because it prevents the video renderer from using the most efficient format.</span></span>

<span data-ttu-id="c05c7-142">En el siguiente pseudocódigo se muestra cómo podría implementar un filtro de copia y transformación (derivado de **CTransformFilter**) que puede cambiar entre los tipos de salida YUV y RGB.</span><span class="sxs-lookup"><span data-stu-id="c05c7-142">The following pseudo-code shows how you might implement a copy-transform filter (derived from **CTransformFilter**) that can switch between YUV and RGB output types.</span></span> <span data-ttu-id="c05c7-143">En este ejemplo se da por supuesto que el filtro realiza la conversión en sí mismo, en lugar de pasar el cambio de formato de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="c05c7-143">This example assumes that the filter does the conversion itself, rather than passing the format change upstream.</span></span>


```C++
HRESULT CMyTransform::CheckInputType(const CMediaType *pmt)
{
    if (pmt is a YUV type that you support) {
        return S_OK;
    }
    else {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }
}

HRESULT CMyTransform::CheckTransform(
    const CMediaType *mtIn, const CMediaType *mtOut)
{
    if (mtOut is a YUV or RGB type that you support)
    {
        if ((mtIn has the same video dimensions as mtOut) &&
            (you support the mtIn-to-mtOut transform))
        {
            return S_OK;
        }
    }
    // otherwise
    return VFW_E_TYPE_NOT_ACCEPTED;
}

// GetMediaType: Return a preferred output type.
HRESULT CMyTransform::GetMediaType(int iPosition, CMediaType *pMediaType)
{
    if (iPosition < 0) {
        return E_INVALIDARG;
    }
    switch (iPosition)
    {
    case 0:
        Copy the input type (YUV) to pMediaType
        return S_OK;
    case 1:
        Construct an RGB type that matches the input type.
        return S_OK;
    default:
        return VFW_S_NO_MORE_ITEMS;
    }
}

// SetMediaType: Override from CTransformFilter. 
HRESULT CMyTransform::SetMediaType(
    PIN_DIRECTION direction, const CMediaType *pmt)
{
    // Capture this information...
    if (direction == PINDIR_OUTPUT)
    {
       m_bYuv = (pmt->subtype == MEDIASUBTYPE_UYVY);
    }
    return S_OK;
}

HRESULT CMyTransform::Transform(
    IMediaSample *pSource, IMediaSample *pDest)
{
    // Look for format changes from downstream.
    CMediaType *pMT = NULL;
    HRESULT hr = pDest->GetMediaType((AM_MEDIA_TYPE**)&pMT);
    if (hr == S_OK)
    {
        hr = m_pOutput->CheckMediaType(pMT);
        if(FAILED(hr))
        {
            DeleteMediaType(pMT);
            return E_FAIL;
        }
        // Notify our own output pin about the new type.
        m_pOutput->SetMediaType(pMT);
        DeleteMediaType(pMT);
    }
    // Process the buffers
    if (m_bYuv) {
        return ProcessFrameYUV(pSource, pDest);
    }
    else {
        return ProcessFrameRGB(pSource, pDest);
    }
}
```



 

 



