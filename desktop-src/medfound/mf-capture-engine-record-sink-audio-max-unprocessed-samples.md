---
description: Establece el número máximo de muestras sin procesar que se pueden almacenar en búfer para su procesamiento en la ruta de acceso de audio del receptor de registros.
ms.assetid: C959ED58-77EB-47EC-8D5D-BBFA9342295D
title: MF_CAPTURE_ENGINE_RECORD_SINK_AUDIO_MAX_UNPROCESSED_SAMPLES atributo (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 442e9b5eca3354e87b8e36b55a3c6cb92ec6f131
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360515"
---
# <a name="mf_capture_engine_record_sink_audio_max_unprocessed_samples-attribute"></a><span data-ttu-id="7bade-103">Modificador de registro del motor de captura de MF \_ atributo de \_ \_ \_ \_ muestras de audio máximo sin \_ \_ procesar \_</span><span class="sxs-lookup"><span data-stu-id="7bade-103">MF\_CAPTURE\_ENGINE\_RECORD\_SINK\_AUDIO\_MAX\_UNPROCESSED\_SAMPLES attribute</span></span>

<span data-ttu-id="7bade-104">Establece el número máximo de muestras sin procesar que se pueden almacenar en búfer para su procesamiento en la ruta de acceso de audio del receptor de registros.</span><span class="sxs-lookup"><span data-stu-id="7bade-104">Sets the maximum number of unprocessed samples that can be buffered for processing in the record sink audio path.</span></span>

## <a name="data-type"></a><span data-ttu-id="7bade-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="7bade-105">Data type</span></span>

<span data-ttu-id="7bade-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="7bade-106">**UINT64**</span></span>

## <a name="remarks"></a><span data-ttu-id="7bade-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7bade-107">Remarks</span></span>

<span data-ttu-id="7bade-108">Para configurar este atributo en el motor de captura, agréguelo al parámetro *pAttributes* cuando llame a [**IMFCaptureEngine:: Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize).</span><span class="sxs-lookup"><span data-stu-id="7bade-108">To configure this attribute on the capture engine, add it to the *pAttributes* parameter when you call [**IMFCaptureEngine::Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize).</span></span>

<span data-ttu-id="7bade-109">El valor máximo de este atributo es 100.</span><span class="sxs-lookup"><span data-stu-id="7bade-109">The maximum value for this attribute is 100.</span></span>

<span data-ttu-id="7bade-110">Una vez que el registro ha almacenado en búfer el número máximo de muestras sin procesar, especificadas por los \_ ejemplos de audio de receptor de registro del motor de captura MF Max sin \_ \_ \_ \_ \_ \_ procesar \_ , quita la velocidad de fotogramas mediante la eliminación de ejemplos.</span><span class="sxs-lookup"><span data-stu-id="7bade-110">Once the record has buffered the maximum number of unprocessed samples, specified by MF\_CAPTURE\_ENGINE\_RECORD\_SINK\_AUDIO\_MAX\_UNPROCESSED\_SAMPLES, it drops the frame rate by dropping samples.</span></span>

## <a name="requirements"></a><span data-ttu-id="7bade-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7bade-111">Requirements</span></span>



| <span data-ttu-id="7bade-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="7bade-112">Requirement</span></span> | <span data-ttu-id="7bade-113">Value</span><span class="sxs-lookup"><span data-stu-id="7bade-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="7bade-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7bade-114">Minimum supported client</span></span><br/> | <span data-ttu-id="7bade-115">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="7bade-115">Windows 8 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="7bade-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7bade-116">Minimum supported server</span></span><br/> | <span data-ttu-id="7bade-117">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="7bade-117">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="7bade-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7bade-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="7bade-119"><dt>Mfcaptureengine. h</dt></span><span class="sxs-lookup"><span data-stu-id="7bade-119"><dt>Mfcaptureengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7bade-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="7bade-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7bade-121">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="7bade-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="7bade-122">Atributos del motor de captura</span><span class="sxs-lookup"><span data-stu-id="7bade-122">Capture Engine Attributes</span></span>](capture-engine-attributes.md)
</dt> <dt>

[<span data-ttu-id="7bade-123">**IMFCaptureEngine:: Initialize**</span><span class="sxs-lookup"><span data-stu-id="7bade-123">**IMFCaptureEngine::Initialize**</span></span>](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 




