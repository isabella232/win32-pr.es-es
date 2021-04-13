---
description: Especifica el perfil de conformidad de dispositivos para la codificación de archivos de formato de transmisión avanzada (ASF).
ms.assetid: 9a6b6402-ff53-4399-8616-06b7768a8737
title: MF_TRANSCODE_ENCODINGPROFILE atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 020344cb2c2f6fc4a539c7cdbc8df0dc69d80d3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543235"
---
# <a name="mf_transcode_encodingprofile-attribute"></a><span data-ttu-id="0ee7b-103">\_Atributo ENCODINGPROFILE de TRANSCODE MF \_</span><span class="sxs-lookup"><span data-stu-id="0ee7b-103">MF\_TRANSCODE\_ENCODINGPROFILE attribute</span></span>

<span data-ttu-id="0ee7b-104">Especifica el perfil de conformidad de dispositivos para la codificación de archivos de formato de transmisión avanzada (ASF).</span><span class="sxs-lookup"><span data-stu-id="0ee7b-104">Specifies the device conformance profile for encoding Advanced Streaming Format (ASF) files.</span></span>

## <a name="data-type"></a><span data-ttu-id="0ee7b-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="0ee7b-105">Data type</span></span>

<span data-ttu-id="0ee7b-106">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="0ee7b-106">**LPWSTR**</span></span>

## <a name="getset"></a><span data-ttu-id="0ee7b-107">Obtener o establecer</span><span class="sxs-lookup"><span data-stu-id="0ee7b-107">Get/set</span></span>

<span data-ttu-id="0ee7b-108">Para obtener este atributo, llame a [**IMFAttributes:: GetAllocatedString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getallocatedstring).</span><span class="sxs-lookup"><span data-stu-id="0ee7b-108">To get this attribute, call [**IMFAttributes::GetAllocatedString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getallocatedstring).</span></span>

<span data-ttu-id="0ee7b-109">Para establecer este atributo, llame a [**IMFAttributes:: setString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span><span class="sxs-lookup"><span data-stu-id="0ee7b-109">To set this attribute, call [**IMFAttributes::SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span></span>

## <a name="remarks"></a><span data-ttu-id="0ee7b-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0ee7b-110">Remarks</span></span>

<span data-ttu-id="0ee7b-111">Use este atributo al transcodificar en un dispositivo que admita Windows Media.</span><span class="sxs-lookup"><span data-stu-id="0ee7b-111">Use this attribute when transcoding to a device that supports Windows Media.</span></span> <span data-ttu-id="0ee7b-112">Si se establece este atributo, el codificador usará el perfil de conformidad del dispositivo, o plantilla, para los códecs de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="0ee7b-112">If this attribute is set, the encoder will use the device conformance profile, or template, for Windows Media codecs.</span></span> <span data-ttu-id="0ee7b-113">Establezca el atributo en el perfil de transcodificación antes de compilar la topología de transcodificación.</span><span class="sxs-lookup"><span data-stu-id="0ee7b-113">Set the attribute on the transcode profile before building the transcode topology.</span></span>

<span data-ttu-id="0ee7b-114">El valor de este atributo puede ser cualquiera de las cadenas de plantilla de cumplimiento enumeradas en los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="0ee7b-114">The value of this attribute can be any of the conformance template strings listed in the following topics:</span></span>

-   [<span data-ttu-id="0ee7b-115">Plantillas de cumplimiento de dispositivos de audio</span><span class="sxs-lookup"><span data-stu-id="0ee7b-115">Audio Device Conformance Templates</span></span>](../wmformat/audio-device-conformance-templates.md)
-   [<span data-ttu-id="0ee7b-116">Plantillas de cumplimiento de dispositivos de vídeo</span><span class="sxs-lookup"><span data-stu-id="0ee7b-116">Video Device Conformance Templates</span></span>](../wmformat/video-device-conformance-templates.md)

<span data-ttu-id="0ee7b-117">En el caso de la codificación Windows Media Video, el generador de topología usa este atributo para establecer la propiedad [**\_ DECODERCOMPLEXITYREQUESTED de MFPKEY**](mfpkey-decodercomplexityrequestedproperty.md) en el codificador.</span><span class="sxs-lookup"><span data-stu-id="0ee7b-117">For Windows Media Video encoding, the topology builder uses this attribute to set the [**MFPKEY\_DECODERCOMPLEXITYREQUESTED**](mfpkey-decodercomplexityrequestedproperty.md) property on the encoder.</span></span> <span data-ttu-id="0ee7b-118">El codificador intentará usar la plantilla especificada para codificar el contenido.</span><span class="sxs-lookup"><span data-stu-id="0ee7b-118">The encoder will attempt to use the specified template to encode the content.</span></span> <span data-ttu-id="0ee7b-119">Para obtener la plantilla real, recorra los nodos de la topología de transcodificación para obtener un puntero al nodo del codificador.</span><span class="sxs-lookup"><span data-stu-id="0ee7b-119">To get the actual template, traverse the nodes of the transcode topology to get a pointer to the encoder node.</span></span> <span data-ttu-id="0ee7b-120">A continuación, obtenga el valor de la propiedad [**MFPKEY \_ DECODERCOMPLEXITYPROFILE**](mfpkey-decodercomplexityprofileproperty.md) del codificador.</span><span class="sxs-lookup"><span data-stu-id="0ee7b-120">Then get the value of the [**MFPKEY\_DECODERCOMPLEXITYPROFILE**](mfpkey-decodercomplexityprofileproperty.md) property from the encoder.</span></span>

<span data-ttu-id="0ee7b-121">El generador de topología también usa el valor de este atributo para establecer la propiedad "DeviceConformanceTemplate" en el receptor multimedia ASF.</span><span class="sxs-lookup"><span data-stu-id="0ee7b-121">The topology builder also uses the value of this attribute to set the "DeviceConformanceTemplate" property on the ASF media sink.</span></span>

<span data-ttu-id="0ee7b-122">Si se establece este atributo, el objeto de metadatos del archivo ASF siempre se genera con independencia del valor especificado por la aplicación del atributo [MF \_ Transcode \_ SKIP omitir \_ \_ transferencia de metadatos](mf-transcode-skip-metadata-transfer.md) .</span><span class="sxs-lookup"><span data-stu-id="0ee7b-122">If this attribute is set, the metadata object of the ASF file is always generated irrespective of the application-specified value of the [MF\_TRANSCODE\_SKIP\_METADATA\_TRANSFER](mf-transcode-skip-metadata-transfer.md) attribute.</span></span>

<span data-ttu-id="0ee7b-123">Los valores típicos de este atributo incluyen los siguientes:</span><span class="sxs-lookup"><span data-stu-id="0ee7b-123">Typical values for this attribute include the following:</span></span>



| <span data-ttu-id="0ee7b-124">Value</span><span class="sxs-lookup"><span data-stu-id="0ee7b-124">Value</span></span>   | <span data-ttu-id="0ee7b-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="0ee7b-125">Description</span></span>                      |
|---------|----------------------------------|
| <span data-ttu-id="0ee7b-126">AISLAMIENTO</span><span class="sxs-lookup"><span data-stu-id="0ee7b-126">"AP"</span></span>    | <span data-ttu-id="0ee7b-127">Vídeo de perfil avanzado</span><span class="sxs-lookup"><span data-stu-id="0ee7b-127">Advanced profile video</span></span>           |
| <span data-ttu-id="0ee7b-128">MP</span><span class="sxs-lookup"><span data-stu-id="0ee7b-128">"MP"</span></span>    | <span data-ttu-id="0ee7b-129">Vídeo de perfil principal</span><span class="sxs-lookup"><span data-stu-id="0ee7b-129">Main profile video</span></span>               |
| <span data-ttu-id="0ee7b-130">DAÑADO</span><span class="sxs-lookup"><span data-stu-id="0ee7b-130">"SP"</span></span>    | <span data-ttu-id="0ee7b-131">Vídeo de perfil sencillo</span><span class="sxs-lookup"><span data-stu-id="0ee7b-131">Simple profile video</span></span>             |
| <span data-ttu-id="0ee7b-132">"MP@LL"</span><span class="sxs-lookup"><span data-stu-id="0ee7b-132">"MP@LL"</span></span> | <span data-ttu-id="0ee7b-133">Perfil principal, vídeo de nivel medio</span><span class="sxs-lookup"><span data-stu-id="0ee7b-133">Main profile, medium level video</span></span> |
| <span data-ttu-id="0ee7b-134">L2</span><span class="sxs-lookup"><span data-stu-id="0ee7b-134">"L2"</span></span>    | <span data-ttu-id="0ee7b-135">Perfil de audio, <= 160 Kbps</span><span class="sxs-lookup"><span data-stu-id="0ee7b-135">Audio profile, <= 160 Kbps</span></span>    |



 

<span data-ttu-id="0ee7b-136">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="0ee7b-136">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ee7b-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0ee7b-137">Requirements</span></span>



| <span data-ttu-id="0ee7b-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="0ee7b-138">Requirement</span></span> | <span data-ttu-id="0ee7b-139">Value</span><span class="sxs-lookup"><span data-stu-id="0ee7b-139">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0ee7b-140">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0ee7b-140">Minimum supported client</span></span><br/> | <span data-ttu-id="0ee7b-141">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="0ee7b-141">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="0ee7b-142">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0ee7b-142">Minimum supported server</span></span><br/> | <span data-ttu-id="0ee7b-143">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="0ee7b-143">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="0ee7b-144">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0ee7b-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="0ee7b-145"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0ee7b-145"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ee7b-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="0ee7b-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ee7b-147">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="0ee7b-147">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="0ee7b-148">API de transcodificación</span><span class="sxs-lookup"><span data-stu-id="0ee7b-148">Transcode API</span></span>](transcode-api.md)
</dt> <dt>

[<span data-ttu-id="0ee7b-149">**IMFTranscodeProfile::GetAudioAttributes**</span><span class="sxs-lookup"><span data-stu-id="0ee7b-149">**IMFTranscodeProfile::GetAudioAttributes**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-getaudioattributes)
</dt> <dt>

[<span data-ttu-id="0ee7b-150">**IMFTranscodeProfile::SetAudioAttributes**</span><span class="sxs-lookup"><span data-stu-id="0ee7b-150">**IMFTranscodeProfile::SetAudioAttributes**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setaudioattributes)
</dt> <dt>

[<span data-ttu-id="0ee7b-151">**IMFTranscodeProfile::SetVideoAttributes**</span><span class="sxs-lookup"><span data-stu-id="0ee7b-151">**IMFTranscodeProfile::SetVideoAttributes**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-getvideoattributes)
</dt> <dt>

[<span data-ttu-id="0ee7b-152">**IMFTranscodeProfile::GetVideoAttributes**</span><span class="sxs-lookup"><span data-stu-id="0ee7b-152">**IMFTranscodeProfile::GetVideoAttributes**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setvideoattributes)
</dt> </dl>

 

 
