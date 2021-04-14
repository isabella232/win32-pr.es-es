---
description: Devuelve una descripción de la señal de vídeo que se transmite a través del conector.
ms.assetid: 8464470f-49db-4559-80b2-02cfc473e30e
title: OPM_GET_ACTUAL_OUTPUT_FORMAT (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12eeca9bcf8fde670447afe4268a86ffa31b6a94
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360483"
---
# <a name="opm_get_actual_output_format"></a><span data-ttu-id="220bc-103">\_formato de \_ \_ salida real \_ de OPM</span><span class="sxs-lookup"><span data-stu-id="220bc-103">OPM\_GET\_ACTUAL\_OUTPUT\_FORMAT</span></span>

<span data-ttu-id="220bc-104">Devuelve una descripción de la señal de vídeo que se transmite a través del conector.</span><span class="sxs-lookup"><span data-stu-id="220bc-104">Returns a description of the video signal that is being transmitted over the connector.</span></span>



| <span data-ttu-id="220bc-105">Requisito</span><span class="sxs-lookup"><span data-stu-id="220bc-105">Requirement</span></span> | <span data-ttu-id="220bc-106">Value</span><span class="sxs-lookup"><span data-stu-id="220bc-106">Value</span></span> |
|--------------|------------------------------------------------------------------------------|
| <span data-ttu-id="220bc-107">GUID de solicitud</span><span class="sxs-lookup"><span data-stu-id="220bc-107">Request GUID</span></span> | <span data-ttu-id="220bc-108">\_formato de \_ \_ salida real \_ de OPM</span><span class="sxs-lookup"><span data-stu-id="220bc-108">OPM\_GET\_ACTUAL\_OUTPUT\_FORMAT</span></span>                                             |
| <span data-ttu-id="220bc-109">Datos de entrada</span><span class="sxs-lookup"><span data-stu-id="220bc-109">Input data</span></span>   | <span data-ttu-id="220bc-110">None</span><span class="sxs-lookup"><span data-stu-id="220bc-110">None</span></span>                                                                         |
| <span data-ttu-id="220bc-111">Devolver datos</span><span class="sxs-lookup"><span data-stu-id="220bc-111">Return data</span></span>  | <span data-ttu-id="220bc-112">Una estructura de [**\_ \_ \_ formato de salida real de OPM**](/windows/desktop/api/opmapi/ns-opmapi-opm_actual_output_format)</span><span class="sxs-lookup"><span data-stu-id="220bc-112">An [**OPM\_ACTUAL\_OUTPUT\_FORMAT**](/windows/desktop/api/opmapi/ns-opmapi-opm_actual_output_format) structure</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="220bc-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="220bc-113">Remarks</span></span>

<span data-ttu-id="220bc-114">La señal de vídeo que se transmite a través del conector no tiene necesariamente el mismo formato que el modo de presentación del escritorio.</span><span class="sxs-lookup"><span data-stu-id="220bc-114">The video signal that is transmitted over the connector does not necessarily have the same format as the desktop display mode.</span></span> <span data-ttu-id="220bc-115">Por ejemplo, el modo de presentación del escritorio podría ser de 1024 x 768 píxeles a 85 Hz, mientras que el conector podría ser un conector de S-vídeo que transmite una señal de vídeo a 720 x 480 píxeles, 60/1.01 Hz entrelazada.</span><span class="sxs-lookup"><span data-stu-id="220bc-115">For example, the desktop display mode might be 1024 x 768 pixels at 85 Hz, while the connector might be an S-Video connector that transmits a video signal at 720 x 480 pixels, 60/1.01 Hz interlaced.</span></span> <span data-ttu-id="220bc-116">En ese caso, el controlador devolvería la resolución de la señal S-video, no la resolución del escritorio.</span><span class="sxs-lookup"><span data-stu-id="220bc-116">In that case, the driver would return the resolution of the S-Video signal, not the desktop resolution.</span></span>

<span data-ttu-id="220bc-117">Esta consulta es equivalente a la \_ consulta COPPQueryDisplayData de DXVA usada en el protocolo de protección de la salida certificada (COPP).</span><span class="sxs-lookup"><span data-stu-id="220bc-117">This query is equivalent to the DXVA\_COPPQueryDisplayData query used in Certified Output Protection Protocol (COPP).</span></span>

## <a name="requirements"></a><span data-ttu-id="220bc-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="220bc-118">Requirements</span></span>



| <span data-ttu-id="220bc-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="220bc-119">Requirement</span></span> | <span data-ttu-id="220bc-120">Value</span><span class="sxs-lookup"><span data-stu-id="220bc-120">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="220bc-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="220bc-121">Minimum supported client</span></span><br/> | <span data-ttu-id="220bc-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="220bc-122">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="220bc-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="220bc-123">Minimum supported server</span></span><br/> | <span data-ttu-id="220bc-124">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="220bc-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="220bc-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="220bc-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="220bc-126"><dt>Opmapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="220bc-126"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="220bc-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="220bc-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="220bc-128">**IOPMVideoOutput:: COPPCompatibleGetInformation**</span><span class="sxs-lookup"><span data-stu-id="220bc-128">**IOPMVideoOutput::COPPCompatibleGetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation)
</dt> <dt>

[<span data-ttu-id="220bc-129">**IOPMVideoOutput:: GetInformation**</span><span class="sxs-lookup"><span data-stu-id="220bc-129">**IOPMVideoOutput::GetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> <dt>

[<span data-ttu-id="220bc-130">Solicitudes de estado de OPM</span><span class="sxs-lookup"><span data-stu-id="220bc-130">OPM Status Requests</span></span>](opm-status-requests.md)
</dt> </dl>

 

 




