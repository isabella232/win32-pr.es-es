---
description: Define la abertura geométrica para un tipo de medio de vídeo.
ms.assetid: a2489ba1-f322-4b63-a479-0d9879c30a8c
title: MF_MT_GEOMETRIC_APERTURE atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e194408dd8b6bf4a4dac717c7d41aaecbb06f306
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001500"
---
# <a name="mf_mt_geometric_aperture-attribute"></a><span data-ttu-id="a5756-103">\_Atributo de \_ \_ apertura geométrica de MF MT</span><span class="sxs-lookup"><span data-stu-id="a5756-103">MF\_MT\_GEOMETRIC\_APERTURE attribute</span></span>

<span data-ttu-id="a5756-104">Define la abertura geométrica para un tipo de medio de vídeo.</span><span class="sxs-lookup"><span data-stu-id="a5756-104">Defines the geometric aperture for a video media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="a5756-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="a5756-105">Data type</span></span>

<span data-ttu-id="a5756-106">Byte array</span><span class="sxs-lookup"><span data-stu-id="a5756-106">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="a5756-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a5756-107">Remarks</span></span>

<span data-ttu-id="a5756-108">El valor de este atributo es una estructura [**MFVideoArea**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoarea) .</span><span class="sxs-lookup"><span data-stu-id="a5756-108">The value of this attribute is an [**MFVideoArea**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoarea) structure.</span></span>

<span data-ttu-id="a5756-109">La relación de aspecto de la imagen se calcula con respecto a la abertura geométrica mediante la siguiente fórmula: relación de aspecto de la imagen = (ancho de abertura geométrica/alto de abertura geométrica) × relación de aspecto de píxeles.</span><span class="sxs-lookup"><span data-stu-id="a5756-109">The picture aspect ratio is calculated relative to the geometric aperture, using the following formula: Picture aspect ratio = (geometric aperture width / geometric aperture height) × pixel aspect ratio.</span></span>

<span data-ttu-id="a5756-110">Si no se establece este atributo, se supone que la abertura geométrica es todo el fotograma de vídeo.</span><span class="sxs-lookup"><span data-stu-id="a5756-110">If this attribute is not set, the geometric aperture is assumed to be the entire video frame.</span></span> <span data-ttu-id="a5756-111">Solo debe establecer este atributo cuando el tipo de medio describe un estándar de vídeo con un área activa definida.</span><span class="sxs-lookup"><span data-stu-id="a5756-111">You should set this attribute only when the media type describes a video standard with a defined active area.</span></span>

<span data-ttu-id="a5756-112">Por ejemplo, en la televisión NTSC, el fotograma de vídeo es 720 × 480 con un área activa de 704 × 480 y una relación de aspecto de 10:11 píxeles.</span><span class="sxs-lookup"><span data-stu-id="a5756-112">For example, in NTSC television the video frame is 720 × 480 with an active area of 704 × 480 and a 10:11 pixel aspect ratio.</span></span> <span data-ttu-id="a5756-113">La imagen resultante tiene una relación de aspecto de (704/480) × (10/11) = 4:3.</span><span class="sxs-lookup"><span data-stu-id="a5756-113">The resulting picture has an aspect ratio of (704/480) × (10/11) = 4:3.</span></span>

> [!Note]  
> <span data-ttu-id="a5756-114">El presentador predeterminado para el [representador de vídeo mejorado](enhanced-video-renderer.md) (EVR) muestra la abertura geométrica del vídeo, si se especifica.</span><span class="sxs-lookup"><span data-stu-id="a5756-114">The default presenter for the [Enhanced Video Renderer](enhanced-video-renderer.md) (EVR) shows the geometric aperture of the video, if specified.</span></span>

 

<span data-ttu-id="a5756-115">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="a5756-115">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="examples"></a><span data-ttu-id="a5756-116">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="a5756-116">Examples</span></span>


```
HRESULT SetGeometricAperture(
    IMFMediaType *pMediaType, 
    const MFVideoArea& area
    )
{
    return pMediaType->SetBlob(
        MF_MT_GEOMETRIC_APERTURE, 
        (UINT8*)&area, 
        sizeof(MFVideoArea)
        );
}
```



## <a name="requirements"></a><span data-ttu-id="a5756-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a5756-117">Requirements</span></span>



| <span data-ttu-id="a5756-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="a5756-118">Requirement</span></span> | <span data-ttu-id="a5756-119">Value</span><span class="sxs-lookup"><span data-stu-id="a5756-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a5756-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a5756-120">Minimum supported client</span></span><br/> | <span data-ttu-id="a5756-121">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="a5756-121">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="a5756-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a5756-122">Minimum supported server</span></span><br/> | <span data-ttu-id="a5756-123">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="a5756-123">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="a5756-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a5756-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="a5756-125"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="a5756-125"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a5756-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="a5756-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5756-127">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a5756-127">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="a5756-128">Atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a5756-128">Media Foundation Attributes</span></span>](media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="a5756-129">Relación de aspecto de la imagen</span><span class="sxs-lookup"><span data-stu-id="a5756-129">Picture Aspect Ratio</span></span>](picture-aspect-ratio.md)
</dt> <dt>

[<span data-ttu-id="a5756-130">Tipos de medios de vídeo</span><span class="sxs-lookup"><span data-stu-id="a5756-130">Video Media Types</span></span>](video-media-types.md)
</dt> <dt>

[<span data-ttu-id="a5756-131">**IMFAttributes:: GetBlob**</span><span class="sxs-lookup"><span data-stu-id="a5756-131">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="a5756-132">**IMFAttributes:: SetBlob**</span><span class="sxs-lookup"><span data-stu-id="a5756-132">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="a5756-133">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="a5756-133">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="a5756-134">**\_ \_ apertura mínima de \_ pantalla MF MT \_**</span><span class="sxs-lookup"><span data-stu-id="a5756-134">**MF\_MT\_MINIMUM\_DISPLAY\_APERTURE**</span></span>](mf-mt-minimum-display-aperture-attribute.md)
</dt> <dt>

[<span data-ttu-id="a5756-135">**\_apertura de \_ \_ análisis panorámico MF MT \_**</span><span class="sxs-lookup"><span data-stu-id="a5756-135">**MF\_MT\_PAN\_SCAN\_APERTURE**</span></span>](mf-mt-pan-scan-aperture-attribute.md)
</dt> </dl>

 

 




