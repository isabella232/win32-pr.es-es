---
description: Especifica el tipo de contenedor de un archivo codificado.
ms.assetid: 97fd968a-6843-4695-aece-02f9acd618fd
title: MF_TRANSCODE_CONTAINERTYPE atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f86b8d5890a771200feda265c3878b6eb7030b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696635"
---
# <a name="mf_transcode_containertype-attribute"></a><span data-ttu-id="524e8-103">\_Atributo CONTAINERTYPE de TRANSCODE MF \_</span><span class="sxs-lookup"><span data-stu-id="524e8-103">MF\_TRANSCODE\_CONTAINERTYPE attribute</span></span>

<span data-ttu-id="524e8-104">Especifica el tipo de contenedor de un archivo codificado.</span><span class="sxs-lookup"><span data-stu-id="524e8-104">Specifies the container type of an encoded file.</span></span> <span data-ttu-id="524e8-105">Media Foundation admite los tipos de contenedor.</span><span class="sxs-lookup"><span data-stu-id="524e8-105">The container types are supported by Media Foundation.</span></span>

## <a name="data-type"></a><span data-ttu-id="524e8-106">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="524e8-106">Data type</span></span>

<span data-ttu-id="524e8-107">**GUID**</span><span class="sxs-lookup"><span data-stu-id="524e8-107">**GUID**</span></span>

<span data-ttu-id="524e8-108">En la tabla siguiente se describen los valores posibles para los tipos de contenedor proporcionados por Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="524e8-108">Possible values for the container types provided by Media Foundation are described in the following table.</span></span>



| <span data-ttu-id="524e8-109">Value</span><span class="sxs-lookup"><span data-stu-id="524e8-109">Value</span></span>                                                                                                                                                                                                                                                                 | <span data-ttu-id="524e8-110">Significado</span><span class="sxs-lookup"><span data-stu-id="524e8-110">Meaning</span></span>                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="MFTranscodeContainerType_ASF"></span><span id="mftranscodecontainertype_asf"></span><span id="MFTRANSCODECONTAINERTYPE_ASF"></span><dl> <span data-ttu-id="524e8-111"><dt>**MFTranscodeContainerType \_ ASF**</dt></span><span class="sxs-lookup"><span data-stu-id="524e8-111"><dt>**MFTranscodeContainerType\_ASF**</dt></span></span> </dl>             | <span data-ttu-id="524e8-112">Contenedor de archivos ASF.</span><span class="sxs-lookup"><span data-stu-id="524e8-112">ASF file container.</span></span><br/>                                                     |
| <span id="MFTranscodeContainerType_MPEG4"></span><span id="mftranscodecontainertype_mpeg4"></span><span id="MFTRANSCODECONTAINERTYPE_MPEG4"></span><dl> <span data-ttu-id="524e8-113"><dt>**MFTranscodeContainerType \_ MPEG4**</dt></span><span class="sxs-lookup"><span data-stu-id="524e8-113"><dt>**MFTranscodeContainerType\_MPEG4**</dt></span></span> </dl>     | <span data-ttu-id="524e8-114">Contenedor de archivos MP4.</span><span class="sxs-lookup"><span data-stu-id="524e8-114">MP4 file container.</span></span><br/>                                                     |
| <span id="MFTranscodeContainerType_MP3"></span><span id="mftranscodecontainertype_mp3"></span><span id="MFTRANSCODECONTAINERTYPE_MP3"></span><dl> <span data-ttu-id="524e8-115"><dt>**\_Mp3 MFTranscodeContainerType**</dt></span><span class="sxs-lookup"><span data-stu-id="524e8-115"><dt>**MFTranscodeContainerType\_MP3**</dt></span></span> </dl>             | <span data-ttu-id="524e8-116">Contenedor de archivos MP3.</span><span class="sxs-lookup"><span data-stu-id="524e8-116">MP3 file container.</span></span><br/>                                                     |
| <span id="MFTranscodeContainerType_3GP"></span><span id="mftranscodecontainertype_3gp"></span><span id="MFTRANSCODECONTAINERTYPE_3GP"></span><dl> <span data-ttu-id="524e8-117"><dt>**MFTranscodeContainerType \_ 3GP**</dt></span><span class="sxs-lookup"><span data-stu-id="524e8-117"><dt>**MFTranscodeContainerType\_3GP**</dt></span></span> </dl>             | <span data-ttu-id="524e8-118">archivo.</span><span class="sxs-lookup"><span data-stu-id="524e8-118">3GP file container.</span></span> <br/>                                                    |
| <span id="MFTranscodeContainerType_AC3"></span><span id="mftranscodecontainertype_ac3"></span><span id="MFTRANSCODECONTAINERTYPE_AC3"></span><dl> <span data-ttu-id="524e8-119"><dt>**MFTranscodeContainerType \_ AC3**</dt></span><span class="sxs-lookup"><span data-stu-id="524e8-119"><dt>**MFTranscodeContainerType\_AC3**</dt></span></span> </dl>             | <span data-ttu-id="524e8-120">Contenedor de archivos AC3.</span><span class="sxs-lookup"><span data-stu-id="524e8-120">AC3 file container.</span></span> <br/>                                                    |
| <span id="MFTranscodeContainerType_ADTS"></span><span id="mftranscodecontainertype_adts"></span><span id="MFTRANSCODECONTAINERTYPE_ADTS"></span><dl> <span data-ttu-id="524e8-121"><dt>**MFTranscodeContainerType \_ ADTS**</dt></span><span class="sxs-lookup"><span data-stu-id="524e8-121"><dt>**MFTranscodeContainerType\_ADTS**</dt></span></span> </dl>         | <span data-ttu-id="524e8-122">Contenedor de archivos ADTS.</span><span class="sxs-lookup"><span data-stu-id="524e8-122">ADTS file container.</span></span> <br/>                                                   |
| <span id="MFTranscodeContainerType_MPEG2"></span><span id="mftranscodecontainertype_mpeg2"></span><span id="MFTRANSCODECONTAINERTYPE_MPEG2"></span><dl> <span data-ttu-id="524e8-123"><dt>**MFTranscodeContainerType \_ MPEG2**</dt></span><span class="sxs-lookup"><span data-stu-id="524e8-123"><dt>**MFTranscodeContainerType\_MPEG2**</dt></span></span> </dl>     | <span data-ttu-id="524e8-124">Contenedor de archivos MPEG2.</span><span class="sxs-lookup"><span data-stu-id="524e8-124">MPEG2 file container.</span></span> <br/>                                                  |
| <span id="MFTranscodeContainerType_FMPEG4"></span><span id="mftranscodecontainertype_fmpeg4"></span><span id="MFTRANSCODECONTAINERTYPE_FMPEG4"></span><dl> <span data-ttu-id="524e8-125"><dt>**MFTranscodeContainerType \_ FMPEG4**</dt></span><span class="sxs-lookup"><span data-stu-id="524e8-125"><dt>**MFTranscodeContainerType\_FMPEG4**</dt></span></span> </dl> | <span data-ttu-id="524e8-126">Contenedor de archivos FMPEG4.</span><span class="sxs-lookup"><span data-stu-id="524e8-126">FMPEG4 file container.</span></span> <br/>                                                 |
| <span id="MFTranscodeContainerType_WAVE"></span><span id="mftranscodecontainertype_wave"></span><span id="MFTRANSCODECONTAINERTYPE_WAVE"></span><dl> <span data-ttu-id="524e8-127"><dt>**MFTranscodeContainerType \_ Wave**</dt></span><span class="sxs-lookup"><span data-stu-id="524e8-127"><dt>**MFTranscodeContainerType\_WAVE**</dt></span></span> </dl>         | <span data-ttu-id="524e8-128">Contenedor de archivos de onda.</span><span class="sxs-lookup"><span data-stu-id="524e8-128">WAVE file container.</span></span><br/> <span data-ttu-id="524e8-129">Se admite en Windows 8.1 y en versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="524e8-129">Supported in Windows 8.1 and and later.</span></span><br/> |
| <span id="MFTranscodeContainerType_AVI"></span><span id="mftranscodecontainertype_avi"></span><span id="MFTRANSCODECONTAINERTYPE_AVI"></span><dl> <span data-ttu-id="524e8-130"><dt>**\_AVI MFTranscodeContainerType**</dt></span><span class="sxs-lookup"><span data-stu-id="524e8-130"><dt>**MFTranscodeContainerType\_AVI**</dt></span></span> </dl>             | <span data-ttu-id="524e8-131">Contenedor de archivos AVI.</span><span class="sxs-lookup"><span data-stu-id="524e8-131">AVI file container.</span></span><br/> <span data-ttu-id="524e8-132">Se admite en Windows 8.1 y en versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="524e8-132">Supported in Windows 8.1 and and later.</span></span><br/>  |
| <span id="MFTranscodeContainerType_AMR"></span><span id="mftranscodecontainertype_amr"></span><span id="MFTRANSCODECONTAINERTYPE_AMR"></span><dl> <span data-ttu-id="524e8-133"><dt>**\_AMR MFTranscodeContainerType**</dt></span><span class="sxs-lookup"><span data-stu-id="524e8-133"><dt>**MFTranscodeContainerType\_AMR**</dt></span></span> </dl>             | <span data-ttu-id="524e8-134">Contenedor de archivos AMR.</span><span class="sxs-lookup"><span data-stu-id="524e8-134">AMR file container.</span></span> <br/>                                                    |



 

## <a name="getset"></a><span data-ttu-id="524e8-135">Obtener o establecer</span><span class="sxs-lookup"><span data-stu-id="524e8-135">Get/set</span></span>

<span data-ttu-id="524e8-136">Para obtener este atributo, llame a [**IMFAttributes:: GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid).</span><span class="sxs-lookup"><span data-stu-id="524e8-136">To get this attribute, call [**IMFAttributes::GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid).</span></span>

<span data-ttu-id="524e8-137">Para establecer este atributo, llame a [**IMFAttributes:: SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid).</span><span class="sxs-lookup"><span data-stu-id="524e8-137">To set this attribute, call [**IMFAttributes::SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid).</span></span>

## <a name="remarks"></a><span data-ttu-id="524e8-138">Observaciones</span><span class="sxs-lookup"><span data-stu-id="524e8-138">Remarks</span></span>

<span data-ttu-id="524e8-139">Este atributo se usa con la característica de transcodificación rápida y el objeto de escritor del receptor.</span><span class="sxs-lookup"><span data-stu-id="524e8-139">This attribute is used with both the Fast Transcode feature and the sink writer object.</span></span>

<span data-ttu-id="524e8-140">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="524e8-140">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

### <a name="fast-transcode"></a><span data-ttu-id="524e8-141">Transcodificación rápida</span><span class="sxs-lookup"><span data-stu-id="524e8-141">Fast Transcode</span></span>

<span data-ttu-id="524e8-142">La aplicación debe establecer el atributo de contenedor en el perfil de transcodificación antes de compilar la topología de transcodificación.</span><span class="sxs-lookup"><span data-stu-id="524e8-142">The application must set the container attribute on the transcode profile before building the transcode topology.</span></span> <span data-ttu-id="524e8-143">El generador de topología analiza este atributo y carga el receptor de medios adecuado en la canalización.</span><span class="sxs-lookup"><span data-stu-id="524e8-143">The topology builder analyses this attribute and loads the appropriate media sink in the pipeline.</span></span> <span data-ttu-id="524e8-144">Para obtener más información, vea los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="524e8-144">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="524e8-145">**IMFTranscodeProfile::GetContainerAttributes**</span><span class="sxs-lookup"><span data-stu-id="524e8-145">**IMFTranscodeProfile::GetContainerAttributes**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-getcontainerattributes)
-   [<span data-ttu-id="524e8-146">**IMFTranscodeProfile::SetContainerAttributes**</span><span class="sxs-lookup"><span data-stu-id="524e8-146">**IMFTranscodeProfile::SetContainerAttributes**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes)

### <a name="sink-writer"></a><span data-ttu-id="524e8-147">Escritor de receptor</span><span class="sxs-lookup"><span data-stu-id="524e8-147">Sink Writer</span></span>

<span data-ttu-id="524e8-148">Este atributo se puede usar para configurar el tipo de contenedor de archivos para el escritor del receptor.</span><span class="sxs-lookup"><span data-stu-id="524e8-148">This attribute can be used to configure the file-container type for the sink writer.</span></span> <span data-ttu-id="524e8-149">Para obtener más información, vea [atributos del escritor de receptor](sink-writer-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="524e8-149">For more information, see [Sink Writer Attributes](sink-writer-attributes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="524e8-150">Requisitos</span><span class="sxs-lookup"><span data-stu-id="524e8-150">Requirements</span></span>



| <span data-ttu-id="524e8-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="524e8-151">Requirement</span></span> | <span data-ttu-id="524e8-152">Value</span><span class="sxs-lookup"><span data-stu-id="524e8-152">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="524e8-153">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="524e8-153">Minimum supported client</span></span><br/> | <span data-ttu-id="524e8-154">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="524e8-154">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="524e8-155">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="524e8-155">Minimum supported server</span></span><br/> | <span data-ttu-id="524e8-156">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="524e8-156">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="524e8-157">Encabezado</span><span class="sxs-lookup"><span data-stu-id="524e8-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="524e8-158"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="524e8-158"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="524e8-159">Vea también</span><span class="sxs-lookup"><span data-stu-id="524e8-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="524e8-160">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="524e8-160">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="524e8-161">API de transcodificación</span><span class="sxs-lookup"><span data-stu-id="524e8-161">Transcode API</span></span>](transcode-api.md)
</dt> </dl>

 

 




