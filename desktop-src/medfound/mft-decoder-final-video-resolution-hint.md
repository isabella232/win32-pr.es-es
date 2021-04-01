---
description: Especifica la resolución de salida final de la imagen descodificada, después del procesamiento de vídeo.
ms.assetid: 067867D8-155C-4406-BE07-720016B2AEBC
title: MFT_DECODER_FINAL_VIDEO_RESOLUTION_HINT atributo (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7bbc0f01ef2a1d7062c6ab58c528b015383fc68
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275842"
---
# <a name="mft_decoder_final_video_resolution_hint-attribute"></a><span data-ttu-id="79dc5-103">Atributo de sugerencia de \_ \_ resolución de vídeo final del \_ descodificador de MFT \_ \_</span><span class="sxs-lookup"><span data-stu-id="79dc5-103">MFT\_DECODER\_FINAL\_VIDEO\_RESOLUTION\_HINT attribute</span></span>

<span data-ttu-id="79dc5-104">Especifica la resolución de salida final de la imagen descodificada, después del procesamiento de vídeo.</span><span class="sxs-lookup"><span data-stu-id="79dc5-104">Specifies the final output resolution of the decoded image, after video processing.</span></span>

## <a name="data-type"></a><span data-ttu-id="79dc5-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="79dc5-105">Data type</span></span>

<span data-ttu-id="79dc5-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="79dc5-106">**UINT64**</span></span>

## <a name="remarks"></a><span data-ttu-id="79dc5-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="79dc5-107">Remarks</span></span>

<span data-ttu-id="79dc5-108">Algunos descodificadores de vídeo admiten este atributo.</span><span class="sxs-lookup"><span data-stu-id="79dc5-108">This attribute is supported by some video decoders.</span></span> <span data-ttu-id="79dc5-109">Una aplicación puede establecer este atributo para indicar el ancho y el alto de la imagen después del procesamiento de vídeo.</span><span class="sxs-lookup"><span data-stu-id="79dc5-109">An application can set this attribute to indicate the width and height of the image after video processing.</span></span> <span data-ttu-id="79dc5-110">El descodificador puede utilizar esta información para optimizar el proceso de descodificación, especialmente si el tamaño de la imagen final es mucho menor que el tamaño de la imagen nativa.</span><span class="sxs-lookup"><span data-stu-id="79dc5-110">The decoder can use this information to optimize the decoding process, especially if the final image size is much smaller than the native image size.</span></span> <span data-ttu-id="79dc5-111">Por ejemplo, el descodificador podría omitir un filtro fuera de bucle.</span><span class="sxs-lookup"><span data-stu-id="79dc5-111">For example, the decoder might skip an out-of-loop filter.</span></span>

<span data-ttu-id="79dc5-112">Los 32 bits superiores contienen el ancho y los bits inferiores 32 contienen el alto.</span><span class="sxs-lookup"><span data-stu-id="79dc5-112">The upper 32 bits contain the width and the lower 32 bits contain the height.</span></span>

<span data-ttu-id="79dc5-113">Para establecer este atributo:</span><span class="sxs-lookup"><span data-stu-id="79dc5-113">To set this attribute:</span></span>

1.  <span data-ttu-id="79dc5-114">Llame a [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) en el descodificador para obtener un puntero [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="79dc5-114">Call [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) on the decoder to get an [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) pointer.</span></span>
2.  <span data-ttu-id="79dc5-115">Llame a [**MFSetAttributeSize**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributesize) para agregar el atributo.</span><span class="sxs-lookup"><span data-stu-id="79dc5-115">Call [**MFSetAttributeSize**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributesize) to add the attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="79dc5-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="79dc5-116">Requirements</span></span>



| <span data-ttu-id="79dc5-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="79dc5-117">Requirement</span></span> | <span data-ttu-id="79dc5-118">Value</span><span class="sxs-lookup"><span data-stu-id="79dc5-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="79dc5-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="79dc5-119">Minimum supported client</span></span><br/> | <span data-ttu-id="79dc5-120">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="79dc5-120">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="79dc5-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="79dc5-121">Minimum supported server</span></span><br/> | <span data-ttu-id="79dc5-122">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="79dc5-122">None supported</span></span><br/>                                                                |
| <span data-ttu-id="79dc5-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="79dc5-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="79dc5-124"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="79dc5-124"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="79dc5-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="79dc5-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79dc5-126">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="79dc5-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="79dc5-127">Atributos de transformación</span><span class="sxs-lookup"><span data-stu-id="79dc5-127">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 




