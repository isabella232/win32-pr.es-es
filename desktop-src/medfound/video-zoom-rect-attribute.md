---
description: Especifica el rectángulo de origen para el mezclador de vídeo del representador de vídeo mejorado (EVR). El rectángulo de origen es la parte del fotograma de vídeo que el mezclador blits a la superficie de destino.
ms.assetid: 4364ff87-816e-4b64-b5e9-c53dd6c9bb33
title: VIDEO_ZOOM_RECT atributo (EVR. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dda4efca5beab844baf3b3f53074d6b3012e8621
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666774"
---
# <a name="video_zoom_rect-attribute"></a><span data-ttu-id="4e428-104">\_Atributo Rect zoom de vídeo \_</span><span class="sxs-lookup"><span data-stu-id="4e428-104">VIDEO\_ZOOM\_RECT attribute</span></span>

<span data-ttu-id="4e428-105">Especifica el rectángulo de origen para el mezclador de vídeo del [representador de vídeo mejorado](enhanced-video-renderer.md) (EVR).</span><span class="sxs-lookup"><span data-stu-id="4e428-105">Specifies the source rectangle for video mixer of the [Enhanced Video Renderer](enhanced-video-renderer.md) (EVR).</span></span> <span data-ttu-id="4e428-106">El rectángulo de origen es la parte del fotograma de vídeo que el mezclador blits a la superficie de destino.</span><span class="sxs-lookup"><span data-stu-id="4e428-106">The source rectangle is the portion of the video frame that the mixer blits to the destination surface.</span></span>

## <a name="data-type"></a><span data-ttu-id="4e428-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="4e428-107">Data type</span></span>

<span data-ttu-id="4e428-108">Byte array</span><span class="sxs-lookup"><span data-stu-id="4e428-108">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="4e428-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4e428-109">Remarks</span></span>

<span data-ttu-id="4e428-110">El valor de este atributo es una estructura [**MFVideoNormalizedRect**](/windows/desktop/api/evr/ns-evr-mfvideonormalizedrect) .</span><span class="sxs-lookup"><span data-stu-id="4e428-110">The value of this attribute is an [**MFVideoNormalizedRect**](/windows/desktop/api/evr/ns-evr-mfvideonormalizedrect) structure.</span></span>

<span data-ttu-id="4e428-111">El rectángulo de origen se define en relación con un sistema de coordenadas normalizado, en el que todo el fotograma de vídeo ocupa un rectángulo con las coordenadas {0, 0, 1, 1}.</span><span class="sxs-lookup"><span data-stu-id="4e428-111">The source rectangle is defined relative to a normalized coordinate system, in which the entire video frame occupies a rectangle with coordinates {0, 0, 1, 1}.</span></span> <span data-ttu-id="4e428-112">El rectángulo de origen debe caber dentro del fotograma de vídeo. las coordenadas del rectángulo de origen tienen un intervalo de (0... 1).</span><span class="sxs-lookup"><span data-stu-id="4e428-112">The source rectangle must fit within the video frame; the coordinates of the source rectangle have a range of (0...1).</span></span>

<span data-ttu-id="4e428-113">El presentador estándar de EVR establece este atributo en el mezclador.</span><span class="sxs-lookup"><span data-stu-id="4e428-113">The standard EVR presenter sets this attribute on the mixer.</span></span> <span data-ttu-id="4e428-114">Para establecer el atributo, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="4e428-114">To set the attribute, do the following:</span></span>

1.  <span data-ttu-id="4e428-115">Llame a [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) en el mezclador para obtener el almacén de atributos del mezclador.</span><span class="sxs-lookup"><span data-stu-id="4e428-115">Call [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) on the mixer, to get the mixer's attribute store.</span></span>
2.  <span data-ttu-id="4e428-116">Llame a [**IMFAttributes:: SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob) para establecer el atributo de **zoom de \_ zoom \_ de vídeo** en el mezclador.</span><span class="sxs-lookup"><span data-stu-id="4e428-116">Call [**IMFAttributes::SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob) to set the **VIDEO\_ZOOM\_RECT** attribute on the mixer.</span></span> <span data-ttu-id="4e428-117">El valor es una estructura [**MFVideoNormalizedRect**](/windows/desktop/api/evr/ns-evr-mfvideonormalizedrect) .</span><span class="sxs-lookup"><span data-stu-id="4e428-117">The value is an [**MFVideoNormalizedRect**](/windows/desktop/api/evr/ns-evr-mfvideonormalizedrect) structure.</span></span>

<span data-ttu-id="4e428-118">En un presentador EVR personalizado, puede usar este atributo para implementar el método [**IMFVideoDisplayControl:: SetVideoPosition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition) .</span><span class="sxs-lookup"><span data-stu-id="4e428-118">In a custom EVR presenter, you can use this attribute to implement the [**IMFVideoDisplayControl::SetVideoPosition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition) method.</span></span> <span data-ttu-id="4e428-119">Para obtener más información, vea [rectángulos de origen y de destino](how-to-write-an-evr-presenter.md).</span><span class="sxs-lookup"><span data-stu-id="4e428-119">For more information, see [Source and Destination Rectangles](how-to-write-an-evr-presenter.md).</span></span>

<span data-ttu-id="4e428-120">La constante GUID para este atributo se exporta desde strmiids. lib.</span><span class="sxs-lookup"><span data-stu-id="4e428-120">The GUID constant for this attribute is exported from strmiids.lib.</span></span>

## <a name="examples"></a><span data-ttu-id="4e428-121">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="4e428-121">Examples</span></span>

<span data-ttu-id="4e428-122">En el ejemplo siguiente se establece el rectángulo de origen en el mezclador.</span><span class="sxs-lookup"><span data-stu-id="4e428-122">The following example sets the source rectangle on the mixer.</span></span>


```C++
HRESULT SetMixerSourceRect(IMFTransform *pMixer, const MFVideoNormalizedRect& nrcSource)
{
    if (pMixer == NULL)
    {
        return E_POINTER;
    }

    IMFAttributes *pAttributes = NULL;

    HRESULT hr = pMixer->GetAttributes(&pAttributes);
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetBlob(VIDEO_ZOOM_RECT, (const UINT8*)&nrcSource, sizeof(nrcSource));
        pAttributes->Release();
    }
    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="4e428-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4e428-123">Requirements</span></span>



| <span data-ttu-id="4e428-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="4e428-124">Requirement</span></span> | <span data-ttu-id="4e428-125">Value</span><span class="sxs-lookup"><span data-stu-id="4e428-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="4e428-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4e428-126">Minimum supported client</span></span><br/> | <span data-ttu-id="4e428-127">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="4e428-127">Windows Vista \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="4e428-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4e428-128">Minimum supported server</span></span><br/> | <span data-ttu-id="4e428-129">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="4e428-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="4e428-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4e428-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="4e428-131"><dt>EVR. h</dt></span><span class="sxs-lookup"><span data-stu-id="4e428-131"><dt>Evr.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e428-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="4e428-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e428-133">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="4e428-133">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="4e428-134">Atributos de representador de vídeo mejorados</span><span class="sxs-lookup"><span data-stu-id="4e428-134">Enhanced Video Renderer Attributes</span></span>](enhanced-video-renderer-attributes.md)
</dt> <dt>

[<span data-ttu-id="4e428-135">Cómo escribir un presentador de EVR</span><span class="sxs-lookup"><span data-stu-id="4e428-135">How to Write an EVR Presenter</span></span>](how-to-write-an-evr-presenter.md)
</dt> <dt>

[<span data-ttu-id="4e428-136">**IMFAttributes:: GetBlob**</span><span class="sxs-lookup"><span data-stu-id="4e428-136">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="4e428-137">**IMFAttributes:: SetBlob**</span><span class="sxs-lookup"><span data-stu-id="4e428-137">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> </dl>

 

 




