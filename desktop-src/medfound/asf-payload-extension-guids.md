---
description: Los siguientes GUID definen las extensiones de carga para las secuencias de formato ASF (Advanced Systems Format).
ms.assetid: db973b41-1e5c-4bc8-921d-5e9312eb21cb
title: GUID de la extensión de carga ASF (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb7dbd27212c8f4812360ba22f89a717659307f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539651"
---
# <a name="asf-payload-extension-guids"></a><span data-ttu-id="12606-103">GUID de extensión de carga ASF</span><span class="sxs-lookup"><span data-stu-id="12606-103">ASF Payload Extension GUIDs</span></span>

<span data-ttu-id="12606-104">Los siguientes GUID definen las extensiones de carga para las secuencias de formato ASF (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="12606-104">The following GUIDs define payload extensions for Advanced Systems Format (ASF) streams.</span></span>



| <span data-ttu-id="12606-105">Constante</span><span class="sxs-lookup"><span data-stu-id="12606-105">Constant</span></span>                                                                                                                                                                                                                                                                                      | <span data-ttu-id="12606-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="12606-106">Description</span></span>                                                                                                                                                                      |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MFASFSampleExtension_SampleDuration"></span><span id="mfasfsampleextension_sampleduration"></span><span id="MFASFSAMPLEEXTENSION_SAMPLEDURATION"></span><dl> <span data-ttu-id="12606-107"><dt>**MFASFSampleExtension \_ SampleDuration**</dt></span><span class="sxs-lookup"><span data-stu-id="12606-107"><dt>**MFASFSampleExtension\_SampleDuration**</dt></span></span> </dl>         | <span data-ttu-id="12606-108">Los datos indican la duración, en milisegundos, del ejemplo contenido en el objeto de búfer.</span><span class="sxs-lookup"><span data-stu-id="12606-108">The data indicates the duration, in milliseconds, of the sample contained in the buffer object.</span></span><br/>                                                                       |
| <span id="MFASFSampleExtension_OutputCleanPoint"></span><span id="mfasfsampleextension_outputcleanpoint"></span><span id="MFASFSAMPLEEXTENSION_OUTPUTCLEANPOINT"></span><dl> <span data-ttu-id="12606-109"><dt>**MFASFSampleExtension \_ OutputCleanPoint**</dt></span><span class="sxs-lookup"><span data-stu-id="12606-109"><dt>**MFASFSampleExtension\_OutputCleanPoint**</dt></span></span> </dl> | <span data-ttu-id="12606-110">Los datos indican si el ejemplo es un fotograma clave.</span><span class="sxs-lookup"><span data-stu-id="12606-110">The data indicates whether the sample is a key frame.</span></span> <span data-ttu-id="12606-111">Un valor de cero indica que el ejemplo no es un fotograma clave.</span><span class="sxs-lookup"><span data-stu-id="12606-111">A value of zero indicates that the sample is not a key frame.</span></span> <span data-ttu-id="12606-112">Un valor distinto de cero indica que se trata de un fotograma clave.</span><span class="sxs-lookup"><span data-stu-id="12606-112">A nonzero value indicates that it is a key frame.</span></span><br/> |
| <span id="MFASFSampleExtension_SMPTE"></span><span id="mfasfsampleextension_smpte"></span><span id="MFASFSAMPLEEXTENSION_SMPTE"></span><dl> <span data-ttu-id="12606-113"><dt>**MFASFSampleExtension \_ SMPTE**</dt></span><span class="sxs-lookup"><span data-stu-id="12606-113"><dt>**MFASFSampleExtension\_SMPTE**</dt></span></span> </dl>                                             | <span data-ttu-id="12606-114">Los datos son un código de tiempo SMPTE.</span><span class="sxs-lookup"><span data-stu-id="12606-114">The data is a SMPTE time code.</span></span><br/>                                                                                                                                        |
| <span id="MFASFSampleExtension_FileName"></span><span id="mfasfsampleextension_filename"></span><span id="MFASFSAMPLEEXTENSION_FILENAME"></span><dl> <span data-ttu-id="12606-115"><dt>**\_Nombre de archivo MFASFSampleExtension**</dt></span><span class="sxs-lookup"><span data-stu-id="12606-115"><dt>**MFASFSampleExtension\_FileName**</dt></span></span> </dl>                                 | <span data-ttu-id="12606-116">Los datos de la extensión de ejemplo especifican el nombre del archivo del que se tomó el contenido de la muestra.</span><span class="sxs-lookup"><span data-stu-id="12606-116">The data in the sample extension specifies the name of the file from which the content in the sample was taken.</span></span><br/>                                                       |
| <span id="MFASFSampleExtension_ContentType"></span><span id="mfasfsampleextension_contenttype"></span><span id="MFASFSAMPLEEXTENSION_CONTENTTYPE"></span><dl> <span data-ttu-id="12606-117"><dt>**\_ContentType MFASFSampleExtension**</dt></span><span class="sxs-lookup"><span data-stu-id="12606-117"><dt>**MFASFSampleExtension\_ContentType**</dt></span></span> </dl>                     | <span data-ttu-id="12606-118">Los datos identifican el tipo de contenido que contiene el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="12606-118">The data identifies the type of content that the sample contains.</span></span><br/>                                                                                                     |
| <span id="MFASFSampleExtension_PixelAspectRatio"></span><span id="mfasfsampleextension_pixelaspectratio"></span><span id="MFASFSAMPLEEXTENSION_PIXELASPECTRATIO"></span><dl> <span data-ttu-id="12606-119"><dt>**MFASFSampleExtension \_ PixelAspectRatio**</dt></span><span class="sxs-lookup"><span data-stu-id="12606-119"><dt>**MFASFSampleExtension\_PixelAspectRatio**</dt></span></span> </dl> | <span data-ttu-id="12606-120">Los datos indican la relación de aspecto de píxeles del contenido en el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="12606-120">The data indicates the pixel aspect ratio of the content in the sample.</span></span><br/>                                                                                               |



## <a name="requirements"></a><span data-ttu-id="12606-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="12606-121">Requirements</span></span>



| <span data-ttu-id="12606-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="12606-122">Requirement</span></span> | <span data-ttu-id="12606-123">Value</span><span class="sxs-lookup"><span data-stu-id="12606-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="12606-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="12606-124">Minimum supported client</span></span><br/> | <span data-ttu-id="12606-125">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="12606-125">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="12606-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="12606-126">Minimum supported server</span></span><br/> | <span data-ttu-id="12606-127">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="12606-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="12606-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="12606-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="12606-129"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="12606-129"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12606-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="12606-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12606-131">**IMFASFStreamConfig::AddPayloadExtension**</span><span class="sxs-lookup"><span data-stu-id="12606-131">**IMFASFStreamConfig::AddPayloadExtension**</span></span>](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-addpayloadextension)
</dt> <dt>

[<span data-ttu-id="12606-132">**IMFASFStreamConfig::GetPayloadExtension**</span><span class="sxs-lookup"><span data-stu-id="12606-132">**IMFASFStreamConfig::GetPayloadExtension**</span></span>](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getpayloadextension)
</dt> <dt>

[<span data-ttu-id="12606-133">Constantes de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="12606-133">Media Foundation Constants</span></span>](media-foundation-constants.md)
</dt> </dl>

 

 




