---
description: Devuelve el identificador único del monitor asociado a esta salida de vídeo.
ms.assetid: d34d68ff-c513-483e-8619-4a9baa2a40ba
title: OPM_GET_OUTPUT_ID (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6146c07be3467e513b33f636bde78e699f3e0d6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705893"
---
# <a name="opm_get_output_id"></a><span data-ttu-id="2655f-103">\_obtener \_ \_ ID. de salida de OPM</span><span class="sxs-lookup"><span data-stu-id="2655f-103">OPM\_GET\_OUTPUT\_ID</span></span>

<span data-ttu-id="2655f-104">Devuelve el identificador único del monitor asociado a esta salida de vídeo.</span><span class="sxs-lookup"><span data-stu-id="2655f-104">Returns the unique identifier of the monitor associated with this video output.</span></span>



| <span data-ttu-id="2655f-105">Requisito</span><span class="sxs-lookup"><span data-stu-id="2655f-105">Requirement</span></span> | <span data-ttu-id="2655f-106">Value</span><span class="sxs-lookup"><span data-stu-id="2655f-106">Value</span></span> |
|--------------|------------------------------------------------------------------|
| <span data-ttu-id="2655f-107">GUID de solicitud</span><span class="sxs-lookup"><span data-stu-id="2655f-107">Request GUID</span></span> | <span data-ttu-id="2655f-108">\_obtener \_ \_ ID. de salida de OPM</span><span class="sxs-lookup"><span data-stu-id="2655f-108">OPM\_GET\_OUTPUT\_ID</span></span>                                             |
| <span data-ttu-id="2655f-109">Datos de entrada</span><span class="sxs-lookup"><span data-stu-id="2655f-109">Input data</span></span>   | <span data-ttu-id="2655f-110">None</span><span class="sxs-lookup"><span data-stu-id="2655f-110">None</span></span>                                                             |
| <span data-ttu-id="2655f-111">Devolver datos</span><span class="sxs-lookup"><span data-stu-id="2655f-111">Return data</span></span>  | <span data-ttu-id="2655f-112">Una estructura de [**\_ \_ \_ datos de ID. de salida OPM**](/windows/desktop/api/opmapi/ns-opmapi-opm_output_id_data)</span><span class="sxs-lookup"><span data-stu-id="2655f-112">An [**OPM\_OUTPUT\_ID\_DATA**](/windows/desktop/api/opmapi/ns-opmapi-opm_output_id_data) structure</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="2655f-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2655f-113">Remarks</span></span>

<span data-ttu-id="2655f-114">El controlador de vídeo asigna un identificador único a cada monitor.</span><span class="sxs-lookup"><span data-stu-id="2655f-114">The video driver assigns a unique identifier to each monitor.</span></span> <span data-ttu-id="2655f-115">Esta consulta devuelve el identificador del monitor que está asociado con el puntero de [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) actual.</span><span class="sxs-lookup"><span data-stu-id="2655f-115">This query returns the identifier for the monitor that is associated with the current [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) pointer.</span></span>

## <a name="requirements"></a><span data-ttu-id="2655f-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2655f-116">Requirements</span></span>



| <span data-ttu-id="2655f-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="2655f-117">Requirement</span></span> | <span data-ttu-id="2655f-118">Value</span><span class="sxs-lookup"><span data-stu-id="2655f-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="2655f-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2655f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="2655f-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="2655f-120">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="2655f-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2655f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="2655f-122">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="2655f-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="2655f-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2655f-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="2655f-124"><dt>Opmapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="2655f-124"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2655f-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="2655f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2655f-126">**IOPMVideoOutput:: GetInformation**</span><span class="sxs-lookup"><span data-stu-id="2655f-126">**IOPMVideoOutput::GetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> <dt>

[<span data-ttu-id="2655f-127">Solicitudes de estado de OPM</span><span class="sxs-lookup"><span data-stu-id="2655f-127">OPM Status Requests</span></span>](opm-status-requests.md)
</dt> </dl>

 

 




