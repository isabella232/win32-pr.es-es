---
description: STRIDE Surface predeterminado, para un tipo de medio de vídeo sin comprimir. STRIDE es el número de bytes necesarios para pasar de una fila de píxeles a la siguiente.
ms.assetid: 71fda231-3497-49db-b82e-2fd79f6ade66
title: MF_MT_DEFAULT_STRIDE atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7b2b9633e14c8d414355ca41be29a9c6c2f8886
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275948"
---
# <a name="mf_mt_default_stride-attribute"></a><span data-ttu-id="0b77f-104">MF \_ MT \_ default \_ STRIDE (atributo)</span><span class="sxs-lookup"><span data-stu-id="0b77f-104">MF\_MT\_DEFAULT\_STRIDE attribute</span></span>

<span data-ttu-id="0b77f-105">STRIDE Surface predeterminado, para un tipo de medio de vídeo sin comprimir.</span><span class="sxs-lookup"><span data-stu-id="0b77f-105">Default surface stride, for an uncompressed video media type.</span></span> <span data-ttu-id="0b77f-106">STRIDE es el número de bytes necesarios para pasar de una fila de píxeles a la siguiente.</span><span class="sxs-lookup"><span data-stu-id="0b77f-106">Stride is the number of bytes needed to go from one row of pixels to the next.</span></span>

## <a name="data-type"></a><span data-ttu-id="0b77f-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="0b77f-107">Data type</span></span>

<span data-ttu-id="0b77f-108">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="0b77f-108">**UINT32**</span></span>

<span data-ttu-id="0b77f-109">Se trata como un valor **INT32** .</span><span class="sxs-lookup"><span data-stu-id="0b77f-109">Treat as a **INT32** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0b77f-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0b77f-110">Remarks</span></span>

<span data-ttu-id="0b77f-111">El valor del atributo se almacena como **UINT32**, pero debe convertirse en un valor entero con signo de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="0b77f-111">The attribute value is stored as a **UINT32**, but should be cast to a 32-bit signed integer value.</span></span> <span data-ttu-id="0b77f-112">STRIDE puede ser negativo.</span><span class="sxs-lookup"><span data-stu-id="0b77f-112">Stride can be negative.</span></span>

<span data-ttu-id="0b77f-113">STRIDE es positivo para las imágenes de arriba abajo y negativo para las imágenes ascendentes.</span><span class="sxs-lookup"><span data-stu-id="0b77f-113">Stride is positive for top-down images, and negative for bottom-up images.</span></span>

<span data-ttu-id="0b77f-114">Este atributo proporciona el intervalo para una representación *contigua* de la imagen en memoria; es decir, una representación sin bytes de relleno adicionales después de cada fila.</span><span class="sxs-lookup"><span data-stu-id="0b77f-114">This attribute gives the stride for a *contiguous* representation of the image in memory; that is, a representation with no additional padding bytes after each row.</span></span> <span data-ttu-id="0b77f-115">Si un búfer multimedia admite la interfaz [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) , use el método [**IMF2DBuffer:: Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d) para obtener el paso real de la superficie, que puede incluir bytes de relleno adicionales.</span><span class="sxs-lookup"><span data-stu-id="0b77f-115">If a media buffer supports the [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) interface, use the [**IMF2DBuffer::Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d) method to get the actual stride of the surface, which might include extra padding bytes.</span></span>

<span data-ttu-id="0b77f-116">Para obtener más información sobre el intervalo de superficie, consulte [STRIDE](image-stride.md)de la imagen.</span><span class="sxs-lookup"><span data-stu-id="0b77f-116">For more information about surface stride, see [Image Stride](image-stride.md).</span></span>

<span data-ttu-id="0b77f-117">Para obtener un ejemplo de cómo calcular el intervalo predeterminado, consulte [búferes de vídeo sin comprimir](uncompressed-video-buffers.md).</span><span class="sxs-lookup"><span data-stu-id="0b77f-117">For an example of how to calculate the default stride, see [Uncompressed Video Buffers](uncompressed-video-buffers.md).</span></span>

<span data-ttu-id="0b77f-118">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="0b77f-118">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b77f-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0b77f-119">Requirements</span></span>



| <span data-ttu-id="0b77f-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b77f-120">Requirement</span></span> | <span data-ttu-id="0b77f-121">Value</span><span class="sxs-lookup"><span data-stu-id="0b77f-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0b77f-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0b77f-122">Minimum supported client</span></span><br/> | <span data-ttu-id="0b77f-123">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="0b77f-123">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="0b77f-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0b77f-124">Minimum supported server</span></span><br/> | <span data-ttu-id="0b77f-125">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="0b77f-125">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="0b77f-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0b77f-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="0b77f-127"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="0b77f-127"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b77f-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="0b77f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b77f-129">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="0b77f-129">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="0b77f-130">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="0b77f-130">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="0b77f-131">**IMFAttributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="0b77f-131">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="0b77f-132">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="0b77f-132">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="0b77f-133">Atributos de tipo de medio</span><span class="sxs-lookup"><span data-stu-id="0b77f-133">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> <dt>

[<span data-ttu-id="0b77f-134">Intervalo de imagen</span><span class="sxs-lookup"><span data-stu-id="0b77f-134">Image Stride</span></span>](image-stride.md)
</dt> </dl>

 

 




