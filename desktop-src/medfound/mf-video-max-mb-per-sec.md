---
description: Especifica, en IMFTransform, la velocidad de procesamiento máxima de adaptativo macrobloque, en macrobloques por segundo, que es compatible con el codificador de hardware.
ms.assetid: 1AA41DE3-C37C-41BA-9549-5F12373DDB3B
title: MF_VIDEO_MAX_MB_PER_SEC atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbee009b50daee074241c11750e9d25240cda153
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105720412"
---
# <a name="mf_video_max_mb_per_sec-attribute"></a><span data-ttu-id="f314c-103">\_Atributo MF \_ máx \_ \_ . MB por \_ segundo de vídeo</span><span class="sxs-lookup"><span data-stu-id="f314c-103">MF\_VIDEO\_MAX\_MB\_PER\_SEC attribute</span></span>

<span data-ttu-id="f314c-104">Especifica, en [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform), la velocidad de procesamiento máxima de adaptativo macrobloque, en macrobloques por segundo, que es compatible con el codificador de hardware.</span><span class="sxs-lookup"><span data-stu-id="f314c-104">Specifies, on [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform), the maximum macroblock processing rate, in macroblocks per second, that is supported by the hardware encoder.</span></span>

## <a name="data-type"></a><span data-ttu-id="f314c-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="f314c-105">Data type</span></span>

<span data-ttu-id="f314c-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="f314c-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="f314c-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f314c-107">Remarks</span></span>

<span data-ttu-id="f314c-108">Este atributo es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="f314c-108">This is a read-only attribute.</span></span>

<span data-ttu-id="f314c-109">**Codificadores H. 264/AVC:**</span><span class="sxs-lookup"><span data-stu-id="f314c-109">**H.264/AVC encoders:**</span></span>

<span data-ttu-id="f314c-110">Este atributo se ve afectado por las siguientes propiedades:</span><span class="sxs-lookup"><span data-stu-id="f314c-110">This attribute is affected by the following properties:</span></span>

-   <span data-ttu-id="f314c-111">[MF \_ \_ \_ Nivel de vídeo MT](mf-mt-video-level.md) (que es un alias de [ \_ nivel MF MT \_ MPEG2 \_ ](mf-mt-mpeg2-level-attribute.md))</span><span class="sxs-lookup"><span data-stu-id="f314c-111">[MF\_MT\_VIDEO\_LEVEL](mf-mt-video-level.md) (which is an alias of [MF\_MT\_MPEG2\_LEVEL](mf-mt-mpeg2-level-attribute.md))</span></span>
-   [<span data-ttu-id="f314c-112">CODECAPI \_ AVEncCommonQualityVsSpeed</span><span class="sxs-lookup"><span data-stu-id="f314c-112">CODECAPI\_AVEncCommonQualityVsSpeed</span></span>](../directshow/avenccommonqualityvsspeed-property.md)
-   [<span data-ttu-id="f314c-113">CODECAPI \_ AVEncMPVDefaultBPictureCount</span><span class="sxs-lookup"><span data-stu-id="f314c-113">CODECAPI\_AVEncMPVDefaultBPictureCount</span></span>](../directshow/avencmpvdefaultbpicturecount-property.md)

<span data-ttu-id="f314c-114">Si el atributo de [ \_ nivel de \_ vídeo \_ MF MT](mf-mt-video-level.md) está presente, el codificador debe devolver la velocidad de procesamiento de la velocidad de bits y la resolución más altas admitidas en el nivel especificado.</span><span class="sxs-lookup"><span data-stu-id="f314c-114">If the [MF\_MT\_VIDEO\_LEVEL](mf-mt-video-level.md) attribute is present, the encoder should return the processing rate for the highest bitrate and resolution supported at the specified level.</span></span> <span data-ttu-id="f314c-115">Si el \_ atributo de \_ nivel de vídeo MF MT \_ no está presente, debe usar un nivel predeterminado de 4.</span><span class="sxs-lookup"><span data-stu-id="f314c-115">If the MF\_MT\_VIDEO\_LEVEL attribute is not present then it should use a default level of 4.</span></span>

<span data-ttu-id="f314c-116">Si se ha establecido la propiedad [CODECAPI \_ AVEncCommonQualityVsSpeed](../directshow/avenccommonqualityvsspeed-property.md) ICodecAPI, el codificador debe devolver la velocidad de procesamiento correspondiente al valor establecido para esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="f314c-116">If the [CODECAPI\_AVEncCommonQualityVsSpeed](../directshow/avenccommonqualityvsspeed-property.md) ICodecAPI property has been set, the encoder should return the processing rate corresponding to the value set for this property.</span></span> <span data-ttu-id="f314c-117">Si el \_ atributo AVEncCommonQualityVsSpeed de CODECAPI no está presente, debe usar un valor predeterminado de 0, que debe ser el modo de procesamiento más rápido.</span><span class="sxs-lookup"><span data-stu-id="f314c-117">If the CODECAPI\_AVEncCommonQualityVsSpeed attribute is not present, then it should use a default value of 0 which should be the fastest processing mode.</span></span>

<span data-ttu-id="f314c-118">Si la propiedad ICodecAPI de [ \_ AVEncMPVDefaultBPictureCount de CODECAPI](../directshow/avencmpvdefaultbpicturecount-property.md) se ha establecido en un valor válido y admitido, el codificador debe devolver la velocidad de procesamiento correspondiente al valor establecido para esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="f314c-118">If the [CODECAPI\_AVEncMPVDefaultBPictureCount](../directshow/avencmpvdefaultbpicturecount-property.md) ICodecAPI property has been set to a valid and supported value, the encoder should return the processing rate corresponding the value set for this property.</span></span> <span data-ttu-id="f314c-119">Si el \_ atributo CODECAPI AVEncMPVDefaultBPictureCount no es Pres, entonces debe usar un valor predeterminado de 0 B fotogramas.</span><span class="sxs-lookup"><span data-stu-id="f314c-119">If the CODECAPI\_AVEncMPVDefaultBPictureCount attribute is not presen,t then it should use a default value of 0 B frames.</span></span>

<span data-ttu-id="f314c-120">Una aplicación solo debe usar los 28 bits inferiores.</span><span class="sxs-lookup"><span data-stu-id="f314c-120">Only the lower 28 bits should be used by an application.</span></span> <span data-ttu-id="f314c-121">Los 4bits superiores se reservan para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="f314c-121">The upper 4bits are reserved for future use.</span></span> <span data-ttu-id="f314c-122">Las aplicaciones deben omitir los 4 bits superiores y MFTs deben establecer los 4 bits superiores en 0.</span><span class="sxs-lookup"><span data-stu-id="f314c-122">Applications should ignore the upper 4 bits and MFTs should set the upper 4 bits to 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="f314c-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f314c-123">Requirements</span></span>



| <span data-ttu-id="f314c-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="f314c-124">Requirement</span></span> | <span data-ttu-id="f314c-125">Value</span><span class="sxs-lookup"><span data-stu-id="f314c-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f314c-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f314c-126">Minimum supported client</span></span><br/> | <span data-ttu-id="f314c-127">Aplicaciones \[ para UWP de Windows 8.1 Desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="f314c-127">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="f314c-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f314c-128">Minimum supported server</span></span><br/> | <span data-ttu-id="f314c-129">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="f314c-129">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="f314c-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f314c-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="f314c-131"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="f314c-131"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f314c-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="f314c-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f314c-133">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f314c-133">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
