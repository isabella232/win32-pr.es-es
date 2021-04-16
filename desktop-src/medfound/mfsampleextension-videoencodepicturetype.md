---
description: Especifica el tipo de imagen que genera un codificador de vídeo.
ms.assetid: 18A47033-3EAC-46C3-94AB-6ED20732F63C
title: MFSampleExtension_VideoEncodePictureType atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bfe0df0e4f3163e7c8c0581c5c7c2a854555eec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687174"
---
# <a name="mfsampleextension_videoencodepicturetype-attribute"></a><span data-ttu-id="c3606-103">\_Atributo VideoEncodePictureType de MFSampleExtension</span><span class="sxs-lookup"><span data-stu-id="c3606-103">MFSampleExtension\_VideoEncodePictureType attribute</span></span>

<span data-ttu-id="c3606-104">Especifica el tipo de imagen que genera un codificador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="c3606-104">Specifies the type of picture that is output by a video encoder.</span></span>

## <a name="data-type"></a><span data-ttu-id="c3606-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="c3606-105">Data type</span></span>

<span data-ttu-id="c3606-106">**eAVEncH264PictureType \_ B** almacenado como **UINT32**</span><span class="sxs-lookup"><span data-stu-id="c3606-106">**eAVEncH264PictureType\_B** stored as **UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="c3606-107">Obtener o establecer</span><span class="sxs-lookup"><span data-stu-id="c3606-107">Get/set</span></span>

<span data-ttu-id="c3606-108">Para obtener este atributo, llame a [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="c3606-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="c3606-109">Para establecer este atributo, llame a [**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="c3606-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="c3606-110">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="c3606-110">Applies to</span></span>

[<span data-ttu-id="c3606-111">**IMFSample**</span><span class="sxs-lookup"><span data-stu-id="c3606-111">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a><span data-ttu-id="c3606-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c3606-112">Remarks</span></span>

<span data-ttu-id="c3606-113">El [**codificador de vídeo H. 264**](h-264-video-encoder.md) establece este atributo en los ejemplos de salida que genera.</span><span class="sxs-lookup"><span data-stu-id="c3606-113">The [**H.264 Video Encoder**](h-264-video-encoder.md) sets this attribute on the output samples that it generates.</span></span> <span data-ttu-id="c3606-114">El valor del atributo es un miembro de la enumeración [**eAVEncH264PictureType**](/windows/desktop/api/codecapi/ne-codecapi-eavench264picturetype) .</span><span class="sxs-lookup"><span data-stu-id="c3606-114">The value of the attribute is a member of the [**eAVEncH264PictureType**](/windows/desktop/api/codecapi/ne-codecapi-eavench264picturetype) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3606-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c3606-115">Requirements</span></span>



| <span data-ttu-id="c3606-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="c3606-116">Requirement</span></span> | <span data-ttu-id="c3606-117">Value</span><span class="sxs-lookup"><span data-stu-id="c3606-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c3606-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c3606-118">Minimum supported client</span></span><br/> | <span data-ttu-id="c3606-119">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="c3606-119">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="c3606-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c3606-120">Minimum supported server</span></span><br/> | <span data-ttu-id="c3606-121">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="c3606-121">None supported</span></span><br/>                                                          |
| <span data-ttu-id="c3606-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c3606-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="c3606-123"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="c3606-123"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c3606-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="c3606-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3606-125">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c3606-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="c3606-126">**Codificador de vídeo H. 264**</span><span class="sxs-lookup"><span data-stu-id="c3606-126">**H.264 Video Encoder**</span></span>](h-264-video-encoder.md)
</dt> <dt>

[<span data-ttu-id="c3606-127">Atributos de ejemplo</span><span class="sxs-lookup"><span data-stu-id="c3606-127">Sample Attributes</span></span>](sample-attributes.md)
</dt> <dt>

[<span data-ttu-id="c3606-128">Ejemplos de medios</span><span class="sxs-lookup"><span data-stu-id="c3606-128">Media Samples</span></span>](media-samples.md)
</dt> </dl>

 

 




