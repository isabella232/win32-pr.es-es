---
description: Establece el número máximo de muestras procesadas que se pueden almacenar en búfer en la ruta de acceso de audio del receptor de registros.
ms.assetid: 216886DB-B206-4944-925A-C2106331F1CB
title: MF_CAPTURE_ENGINE_RECORD_SINK_AUDIO_MAX_PROCESSED_SAMPLES atributo (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19d1ce4d649c75106545eb2ff39d4f3ea742e6a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542566"
---
# <a name="mf_capture_engine_record_sink_audio_max_processed_samples-attribute"></a><span data-ttu-id="5f87e-103">Modificador de registro del motor de captura de MF \_ atributo de \_ muestreo de número de \_ \_ \_ \_ \_ muestras procesadas \_</span><span class="sxs-lookup"><span data-stu-id="5f87e-103">MF\_CAPTURE\_ENGINE\_RECORD\_SINK\_AUDIO\_MAX\_PROCESSED\_SAMPLES attribute</span></span>

<span data-ttu-id="5f87e-104">Establece el número máximo de muestras procesadas que se pueden almacenar en búfer en la ruta de acceso de audio del receptor de registros.</span><span class="sxs-lookup"><span data-stu-id="5f87e-104">Sets the maximum number of processed samples that can be buffered in the record sink audio path.</span></span>

## <a name="data-type"></a><span data-ttu-id="5f87e-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="5f87e-105">Data type</span></span>

<span data-ttu-id="5f87e-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="5f87e-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="5f87e-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5f87e-107">Remarks</span></span>

<span data-ttu-id="5f87e-108">Para configurar este atributo en el motor de captura, agréguelo al parámetro *pAttributes* cuando llame a [**IMFCaptureEngine:: Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize).</span><span class="sxs-lookup"><span data-stu-id="5f87e-108">To configure this attribute on the capture engine, add it to the *pAttributes* parameter when you call [**IMFCaptureEngine::Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize).</span></span>

<span data-ttu-id="5f87e-109">El valor máximo de este atributo es 100.</span><span class="sxs-lookup"><span data-stu-id="5f87e-109">The maximum value for this attribute is 100.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f87e-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5f87e-110">Requirements</span></span>



| <span data-ttu-id="5f87e-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="5f87e-111">Requirement</span></span> | <span data-ttu-id="5f87e-112">Value</span><span class="sxs-lookup"><span data-stu-id="5f87e-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f87e-113">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5f87e-113">Minimum supported client</span></span><br/> | <span data-ttu-id="5f87e-114">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="5f87e-114">Windows 8 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="5f87e-115">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5f87e-115">Minimum supported server</span></span><br/> | <span data-ttu-id="5f87e-116">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="5f87e-116">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="5f87e-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5f87e-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="5f87e-118"><dt>Mfcaptureengine. h</dt></span><span class="sxs-lookup"><span data-stu-id="5f87e-118"><dt>Mfcaptureengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f87e-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="5f87e-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f87e-120">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5f87e-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="5f87e-121">Atributos del motor de captura</span><span class="sxs-lookup"><span data-stu-id="5f87e-121">Capture Engine Attributes</span></span>](capture-engine-attributes.md)
</dt> <dt>

[<span data-ttu-id="5f87e-122">**IMFCaptureEngine:: Initialize**</span><span class="sxs-lookup"><span data-stu-id="5f87e-122">**IMFCaptureEngine::Initialize**</span></span>](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 




