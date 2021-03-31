---
description: Especifica si el motor de captura captura audio pero no vídeo.
ms.assetid: 0A905D55-CEE5-44FC-97A5-9474872D5724
title: MF_CAPTURE_ENGINE_USE_AUDIO_DEVICE_ONLY atributo (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f02e0b8f1002bcfff12f8a2bea93612456b6072
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001264"
---
# <a name="mf_capture_engine_use_audio_device_only-attribute"></a><span data-ttu-id="62028-103">El \_ motor de captura MF \_ usar el \_ \_ \_ atributo solo de dispositivo de audio \_</span><span class="sxs-lookup"><span data-stu-id="62028-103">MF\_CAPTURE\_ENGINE\_USE\_AUDIO\_DEVICE\_ONLY attribute</span></span>

<span data-ttu-id="62028-104">Especifica si el motor de captura captura audio pero no vídeo.</span><span class="sxs-lookup"><span data-stu-id="62028-104">Specifies whether the capture engine captures audio but not video.</span></span>

## <a name="data-type"></a><span data-ttu-id="62028-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="62028-105">Data type</span></span>

<span data-ttu-id="62028-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="62028-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="62028-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="62028-107">Remarks</span></span>

<span data-ttu-id="62028-108">Si este atributo es **true**, el motor de captura no selecciona ni usa un dispositivo de captura de vídeo.</span><span class="sxs-lookup"><span data-stu-id="62028-108">If this attribute is **TRUE**, the capture engine does not select or use a video capture device.</span></span> <span data-ttu-id="62028-109">Establezca este atributo en **true** si desea capturar audio sin vídeo.</span><span class="sxs-lookup"><span data-stu-id="62028-109">Set this attribute to **TRUE** if you want to capture audio without video.</span></span> <span data-ttu-id="62028-110">El valor predeterminado es **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="62028-110">The default value is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="62028-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="62028-111">Requirements</span></span>



| <span data-ttu-id="62028-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="62028-112">Requirement</span></span> | <span data-ttu-id="62028-113">Value</span><span class="sxs-lookup"><span data-stu-id="62028-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="62028-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="62028-114">Minimum supported client</span></span><br/> | <span data-ttu-id="62028-115">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="62028-115">Windows 8 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="62028-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="62028-116">Minimum supported server</span></span><br/> | <span data-ttu-id="62028-117">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="62028-117">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="62028-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="62028-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="62028-119"><dt>Mfcaptureengine. h</dt></span><span class="sxs-lookup"><span data-stu-id="62028-119"><dt>Mfcaptureengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62028-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="62028-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62028-121">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="62028-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="62028-122">Atributos del motor de captura</span><span class="sxs-lookup"><span data-stu-id="62028-122">Capture Engine Attributes</span></span>](capture-engine-attributes.md)
</dt> <dt>

[<span data-ttu-id="62028-123">**IMFCaptureEngine:: Initialize**</span><span class="sxs-lookup"><span data-stu-id="62028-123">**IMFCaptureEngine::Initialize**</span></span>](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 




