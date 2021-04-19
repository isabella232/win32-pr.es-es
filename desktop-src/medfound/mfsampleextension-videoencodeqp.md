---
description: Especifica el parámetro de cuantificación (QP) que se usó para codificar un ejemplo de vídeo.
ms.assetid: F7C4FEFC-FEE7-4614-BC90-4F9D5D878F49
title: MFSampleExtension_VideoEncodeQP atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 721f5df00ff24b307daed2ccbcbf61a04b129db2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715795"
---
# <a name="mfsampleextension_videoencodeqp-attribute"></a><span data-ttu-id="b1796-103">\_Atributo VideoEncodeQP de MFSampleExtension</span><span class="sxs-lookup"><span data-stu-id="b1796-103">MFSampleExtension\_VideoEncodeQP attribute</span></span>

<span data-ttu-id="b1796-104">Especifica el parámetro de cuantificación (QP) que se usó para codificar un ejemplo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="b1796-104">Specifies the quantization parameter (QP) that was used to encode a video sample.</span></span>

## <a name="data-type"></a><span data-ttu-id="b1796-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="b1796-105">Data type</span></span>

<span data-ttu-id="b1796-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="b1796-106">**UINT64**</span></span>

## <a name="getset"></a><span data-ttu-id="b1796-107">Obtener o establecer</span><span class="sxs-lookup"><span data-stu-id="b1796-107">Get/set</span></span>

<span data-ttu-id="b1796-108">Para obtener este atributo, llame a [**IMFAttributes:: GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).</span><span class="sxs-lookup"><span data-stu-id="b1796-108">To get this attribute, call [**IMFAttributes::GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).</span></span>

<span data-ttu-id="b1796-109">Para establecer este atributo, llame a [**IMFAttributes:: SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64).</span><span class="sxs-lookup"><span data-stu-id="b1796-109">To set this attribute, call [**IMFAttributes::SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64).</span></span>

## <a name="applies-to"></a><span data-ttu-id="b1796-110">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="b1796-110">Applies to</span></span>

[<span data-ttu-id="b1796-111">**IMFSample**</span><span class="sxs-lookup"><span data-stu-id="b1796-111">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a><span data-ttu-id="b1796-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b1796-112">Remarks</span></span>

<span data-ttu-id="b1796-113">El [**codificador de vídeo H. 264**](h-264-video-encoder.md) establece este atributo en los ejemplos de salida que genera.</span><span class="sxs-lookup"><span data-stu-id="b1796-113">The [**H.264 Video Encoder**](h-264-video-encoder.md) sets this attribute on the output samples that it generates.</span></span>

## <a name="requirements"></a><span data-ttu-id="b1796-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b1796-114">Requirements</span></span>



| <span data-ttu-id="b1796-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="b1796-115">Requirement</span></span> | <span data-ttu-id="b1796-116">Value</span><span class="sxs-lookup"><span data-stu-id="b1796-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b1796-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b1796-117">Minimum supported client</span></span><br/> | <span data-ttu-id="b1796-118">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="b1796-118">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="b1796-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b1796-119">Minimum supported server</span></span><br/> | <span data-ttu-id="b1796-120">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="b1796-120">None supported</span></span><br/>                                                          |
| <span data-ttu-id="b1796-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b1796-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="b1796-122"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="b1796-122"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b1796-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="b1796-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1796-124">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b1796-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="b1796-125">**Codificador de vídeo H. 264**</span><span class="sxs-lookup"><span data-stu-id="b1796-125">**H.264 Video Encoder**</span></span>](h-264-video-encoder.md)
</dt> <dt>

[<span data-ttu-id="b1796-126">Atributos de ejemplo</span><span class="sxs-lookup"><span data-stu-id="b1796-126">Sample Attributes</span></span>](sample-attributes.md)
</dt> <dt>

[<span data-ttu-id="b1796-127">Ejemplos de medios</span><span class="sxs-lookup"><span data-stu-id="b1796-127">Media Samples</span></span>](media-samples.md)
</dt> </dl>

 

 




