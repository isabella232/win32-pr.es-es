---
description: Los siguientes GUID definen las categorías para las transformaciones de Media Foundation (MFTs). Estas categorías se usan para registrar y enumerar MFTs.
ms.assetid: eca3ae3b-e40a-407d-986c-d0a85b891f52
title: MFT_CATEGORY (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb7bc74054ad9f201b1f2ca53b526826d34c510d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908648"
---
# <a name="mft_category"></a><span data-ttu-id="103dc-104">Categoría de MFT \_</span><span class="sxs-lookup"><span data-stu-id="103dc-104">MFT\_CATEGORY</span></span>

<span data-ttu-id="103dc-105">Los siguientes GUID definen las categorías para las transformaciones de Media Foundation (MFTs).</span><span class="sxs-lookup"><span data-stu-id="103dc-105">The following GUIDs define categories for Media Foundation transforms (MFTs).</span></span> <span data-ttu-id="103dc-106">Estas categorías se usan para registrar y enumerar MFTs.</span><span class="sxs-lookup"><span data-stu-id="103dc-106">These categories are used to register and enumerate MFTs.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="103dc-107">Constante</span><span class="sxs-lookup"><span data-stu-id="103dc-107">Constant</span></span></th>
<th style="text-align: left;"><span data-ttu-id="103dc-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="103dc-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="MFT_CATEGORY_AUDIO_DECODER"></span><span id="mft_category_audio_decoder"></span><dl> <span data-ttu-id="103dc-109"><dt><strong>MFT_CATEGORY_AUDIO_DECODER</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="103dc-109"><dt><strong>MFT_CATEGORY_AUDIO_DECODER</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="103dc-110">Descodificadores de audio.</span><span class="sxs-lookup"><span data-stu-id="103dc-110">Audio decoders.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="MFT_CATEGORY_AUDIO_EFFECT"></span><span id="mft_category_audio_effect"></span><dl> <span data-ttu-id="103dc-111"><dt><strong>MFT_CATEGORY_AUDIO_EFFECT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="103dc-111"><dt><strong>MFT_CATEGORY_AUDIO_EFFECT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="103dc-112">Efectos de audio.</span><span class="sxs-lookup"><span data-stu-id="103dc-112">Audio effects.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="MFT_CATEGORY_AUDIO_ENCODER"></span><span id="mft_category_audio_encoder"></span><dl> <span data-ttu-id="103dc-113"><dt><strong>MFT_CATEGORY_AUDIO_ENCODER</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="103dc-113"><dt><strong>MFT_CATEGORY_AUDIO_ENCODER</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="103dc-114">Codificadores de audio.</span><span class="sxs-lookup"><span data-stu-id="103dc-114">Audio encoders.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="MFT_CATEGORY_DEMULTIPLEXER"></span><span id="mft_category_demultiplexer"></span><dl> <span data-ttu-id="103dc-115"><dt><strong>MFT_CATEGORY_DEMULTIPLEXER</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="103dc-115"><dt><strong>MFT_CATEGORY_DEMULTIPLEXER</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="103dc-116">Demultiplexadores.</span><span class="sxs-lookup"><span data-stu-id="103dc-116">Demultiplexers.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="MFT_CATEGORY_MULTIPLEXER"></span><span id="mft_category_multiplexer"></span><dl> <span data-ttu-id="103dc-117"><dt><strong>MFT_CATEGORY_MULTIPLEXER</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="103dc-117"><dt><strong>MFT_CATEGORY_MULTIPLEXER</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="103dc-118">Multiplexores.</span><span class="sxs-lookup"><span data-stu-id="103dc-118">Multiplexers.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="103dc-119">En Windows Vista, la canalización de Media Foundation no admite MFTs con más de una entrada.</span><span class="sxs-lookup"><span data-stu-id="103dc-119">In Windows Vista, the Media Foundation pipeline does not support MFTs with more than one input.</span></span> <span data-ttu-id="103dc-120">Se admiten MFTs de varias entradas en Windows 7.</span><span class="sxs-lookup"><span data-stu-id="103dc-120">Multiple-input MFTs are supported in Windows 7.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="MFT_CATEGORY_OTHER"></span><span id="mft_category_other"></span><dl> <span data-ttu-id="103dc-121"><dt><strong>MFT_CATEGORY_OTHER</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="103dc-121"><dt><strong>MFT_CATEGORY_OTHER</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="103dc-122">MFTs varios.</span><span class="sxs-lookup"><span data-stu-id="103dc-122">Miscellaneous MFTs.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="MFT_CATEGORY_VIDEO_DECODER"></span><span id="mft_category_video_decoder"></span><dl> <span data-ttu-id="103dc-123"><dt><strong>MFT_CATEGORY_VIDEO_DECODER</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="103dc-123"><dt><strong>MFT_CATEGORY_VIDEO_DECODER</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="103dc-124">Descodificadores de vídeo.</span><span class="sxs-lookup"><span data-stu-id="103dc-124">Video decoders.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="MFT_CATEGORY_VIDEO_EFFECT"></span><span id="mft_category_video_effect"></span><dl> <span data-ttu-id="103dc-125"><dt><strong>MFT_CATEGORY_VIDEO_EFFECT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="103dc-125"><dt><strong>MFT_CATEGORY_VIDEO_EFFECT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="103dc-126">Efectos de vídeo.</span><span class="sxs-lookup"><span data-stu-id="103dc-126">Video effects.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="MFT_CATEGORY_VIDEO_RENDERER_EFFECT"></span><span id="mft_category_video_renderer_effect"></span><dl> <span data-ttu-id="103dc-127"><dt><strong>MFT_CATEGORY_VIDEO_RENDERER_EFFECT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="103dc-127"><dt><strong>MFT_CATEGORY_VIDEO_RENDERER_EFFECT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="103dc-128">Efectos del representador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="103dc-128">Video renderer effects.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="MFT_CATEGORY_VIDEO_ENCODER"></span><span id="mft_category_video_encoder"></span><dl> <span data-ttu-id="103dc-129"><dt><strong>MFT_CATEGORY_VIDEO_ENCODER</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="103dc-129"><dt><strong>MFT_CATEGORY_VIDEO_ENCODER</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="103dc-130">Codificadores de vídeo.</span><span class="sxs-lookup"><span data-stu-id="103dc-130">Video encoders.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="MFT_CATEGORY_VIDEO_PROCESSOR"></span><span id="mft_category_video_processor"></span><dl> <span data-ttu-id="103dc-131"><dt><strong>MFT_CATEGORY_VIDEO_PROCESSOR</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="103dc-131"><dt><strong>MFT_CATEGORY_VIDEO_PROCESSOR</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
<span data-ttu-id="103dc-132">Introducido en Windows 7.</span><span class="sxs-lookup"><span data-stu-id="103dc-132">Introduced in Windows 7.</span></span>
</blockquote>
<br/> <span data-ttu-id="103dc-133">Procesadores de vídeo.</span><span class="sxs-lookup"><span data-stu-id="103dc-133">Video processors.</span></span> <br/> <span data-ttu-id="103dc-134">Esta categoría está limitada a MFTs que realizan conversiones de formato en vídeo sin comprimir, incluidas las conversiones de espacio de color.</span><span class="sxs-lookup"><span data-stu-id="103dc-134">This category is limited to MFTs that perform format conversions on uncompressed video, including color-space conversions.</span></span> <span data-ttu-id="103dc-135">Para los efectos de vídeo que modifican la apariencia de la imagen (por ejemplo, un efecto de desenfoque o una transformación de color a escala de grises), use la categoría <strong>MFT_CATEGORY_VIDEO_EFFECT</strong> .</span><span class="sxs-lookup"><span data-stu-id="103dc-135">For video effects that modify the appearance of the image (such as a blur effect or a color-to-grayscale transform), use the <strong>MFT_CATEGORY_VIDEO_EFFECT</strong> category.</span></span><br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a><span data-ttu-id="103dc-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="103dc-136">Requirements</span></span>



| <span data-ttu-id="103dc-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="103dc-137">Requirement</span></span> | <span data-ttu-id="103dc-138">Value</span><span class="sxs-lookup"><span data-stu-id="103dc-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="103dc-139">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="103dc-139">Minimum supported client</span></span><br/> | <span data-ttu-id="103dc-140">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="103dc-140">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="103dc-141">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="103dc-141">Minimum supported server</span></span><br/> | <span data-ttu-id="103dc-142">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="103dc-142">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="103dc-143">Encabezado</span><span class="sxs-lookup"><span data-stu-id="103dc-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="103dc-144"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="103dc-144"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="103dc-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="103dc-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="103dc-146">Constantes de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="103dc-146">Media Foundation Constants</span></span>](media-foundation-constants.md)
</dt> <dt>

[<span data-ttu-id="103dc-147">Media Foundation transformaciones</span><span class="sxs-lookup"><span data-stu-id="103dc-147">Media Foundation Transforms</span></span>](media-foundation-transforms.md)
</dt> <dt>

[<span data-ttu-id="103dc-148">**MFTEnum**</span><span class="sxs-lookup"><span data-stu-id="103dc-148">**MFTEnum**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mftenum)
</dt> <dt>

[<span data-ttu-id="103dc-149">**MFTEnumEx**</span><span class="sxs-lookup"><span data-stu-id="103dc-149">**MFTEnumEx**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mftenumex)
</dt> <dt>

[<span data-ttu-id="103dc-150">**MFTRegister**</span><span class="sxs-lookup"><span data-stu-id="103dc-150">**MFTRegister**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mftregister)
</dt> </dl>

 

 




