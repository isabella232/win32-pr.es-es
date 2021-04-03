---
description: Establece el número máximo de muestras procesadas que se pueden almacenar en búfer en la ruta de acceso de vídeo del receptor de registros.
ms.assetid: 5AFA197E-5A7F-402E-A62B-4F624A5DD917
title: MF_CAPTURE_ENGINE_RECORD_SINK_VIDEO_MAX_PROCESSED_SAMPLES atributo (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70c3840f449cebb6579b2c1df5f330379ba30655
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810490"
---
# <a name="mf_capture_engine_record_sink_video_max_processed_samples-attribute"></a><span data-ttu-id="a2606-103">El atributo del receptor de registro del motor de captura MF muestra el \_ \_ \_ \_ \_ \_ \_ atributo Max Processed \_ Samples</span><span class="sxs-lookup"><span data-stu-id="a2606-103">MF\_CAPTURE\_ENGINE\_RECORD\_SINK\_VIDEO\_MAX\_PROCESSED\_SAMPLES attribute</span></span>

<span data-ttu-id="a2606-104">Establece el número máximo de muestras procesadas que se pueden almacenar en búfer en la ruta de acceso de vídeo del receptor de registros.</span><span class="sxs-lookup"><span data-stu-id="a2606-104">Sets the maximum number of processed samples that can be buffered in the record sink video path.</span></span>

## <a name="data-type"></a><span data-ttu-id="a2606-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="a2606-105">Data type</span></span>

<span data-ttu-id="a2606-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="a2606-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="a2606-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a2606-107">Remarks</span></span>

<span data-ttu-id="a2606-108">Para configurar este atributo en el motor de captura, agréguelo al parámetro *pAttributes* cuando llame a [**IMFCaptureEngine:: Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize).</span><span class="sxs-lookup"><span data-stu-id="a2606-108">To configure this attribute on the capture engine, add it to the *pAttributes* parameter when you call [**IMFCaptureEngine::Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize).</span></span>

<span data-ttu-id="a2606-109">El valor máximo de este atributo es 17.</span><span class="sxs-lookup"><span data-stu-id="a2606-109">The maximum value for this attribute is 17.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2606-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a2606-110">Requirements</span></span>



| <span data-ttu-id="a2606-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="a2606-111">Requirement</span></span> | <span data-ttu-id="a2606-112">Value</span><span class="sxs-lookup"><span data-stu-id="a2606-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2606-113">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a2606-113">Minimum supported client</span></span><br/> | <span data-ttu-id="a2606-114">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="a2606-114">Windows 8 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="a2606-115">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a2606-115">Minimum supported server</span></span><br/> | <span data-ttu-id="a2606-116">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="a2606-116">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="a2606-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a2606-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="a2606-118"><dt>Mfcaptureengine. h</dt></span><span class="sxs-lookup"><span data-stu-id="a2606-118"><dt>Mfcaptureengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2606-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="a2606-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2606-120">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a2606-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="a2606-121">Atributos del motor de captura</span><span class="sxs-lookup"><span data-stu-id="a2606-121">Capture Engine Attributes</span></span>](capture-engine-attributes.md)
</dt> <dt>

[<span data-ttu-id="a2606-122">**IMFCaptureEngine:: Initialize**</span><span class="sxs-lookup"><span data-stu-id="a2606-122">**IMFCaptureEngine::Initialize**</span></span>](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 




