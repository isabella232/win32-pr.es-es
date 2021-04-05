---
description: Especifica si el motor de captura captura vídeo pero no audio.
ms.assetid: B0B7A7F2-02F9-46A6-954F-D6E9C3B73A29
title: MF_CAPTURE_ENGINE_USE_VIDEO_DEVICE_ONLY atributo (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0b687bfa7ec2f30f296dd83997f3e64ac4198fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001510"
---
# <a name="mf_capture_engine_use_video_device_only-attribute"></a><span data-ttu-id="f4331-103">El \_ motor de captura MF \_ \_ usar \_ solo el atributo de dispositivo de vídeo \_ \_</span><span class="sxs-lookup"><span data-stu-id="f4331-103">MF\_CAPTURE\_ENGINE\_USE\_VIDEO\_DEVICE\_ONLY attribute</span></span>

<span data-ttu-id="f4331-104">Especifica si el motor de captura captura vídeo pero no audio.</span><span class="sxs-lookup"><span data-stu-id="f4331-104">Specifies whether the capture engine captures video but not audio.</span></span>

## <a name="data-type"></a><span data-ttu-id="f4331-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="f4331-105">Data type</span></span>

<span data-ttu-id="f4331-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="f4331-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="f4331-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f4331-107">Remarks</span></span>

<span data-ttu-id="f4331-108">Si este atributo es **true**, el motor de captura no selecciona ni usa un dispositivo de captura de audio.</span><span class="sxs-lookup"><span data-stu-id="f4331-108">If this attribute is **TRUE**, the capture engine does not select or use an audio capture device.</span></span> <span data-ttu-id="f4331-109">Establezca este atributo en **true** si desea capturar vídeo sin audio.</span><span class="sxs-lookup"><span data-stu-id="f4331-109">Set this attribute to **TRUE** if you want to capture video without audio.</span></span> <span data-ttu-id="f4331-110">El valor predeterminado es **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="f4331-110">The default value is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="f4331-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f4331-111">Requirements</span></span>



| <span data-ttu-id="f4331-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="f4331-112">Requirement</span></span> | <span data-ttu-id="f4331-113">Value</span><span class="sxs-lookup"><span data-stu-id="f4331-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4331-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f4331-114">Minimum supported client</span></span><br/> | <span data-ttu-id="f4331-115">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="f4331-115">Windows 8 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="f4331-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f4331-116">Minimum supported server</span></span><br/> | <span data-ttu-id="f4331-117">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="f4331-117">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="f4331-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f4331-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="f4331-119"><dt>Mfcaptureengine. h</dt></span><span class="sxs-lookup"><span data-stu-id="f4331-119"><dt>Mfcaptureengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4331-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="f4331-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4331-121">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f4331-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="f4331-122">Atributos del motor de captura</span><span class="sxs-lookup"><span data-stu-id="f4331-122">Capture Engine Attributes</span></span>](capture-engine-attributes.md)
</dt> <dt>

[<span data-ttu-id="f4331-123">**IMFCaptureEngine:: Initialize**</span><span class="sxs-lookup"><span data-stu-id="f4331-123">**IMFCaptureEngine::Initialize**</span></span>](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 




