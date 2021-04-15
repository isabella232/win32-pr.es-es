---
description: 'Más información acerca de: OPM_GET_ACP_AND_CGMSA_SIGNALING'
ms.assetid: d477fe3e-4498-450b-93b7-ce74ae9ed005
title: OPM_GET_ACP_AND_CGMSA_SIGNALING (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bf6294c3f1d90ac8a2292c65b3c1b8558e69220
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715531"
---
# <a name="opm_get_acp_and_cgmsa_signaling"></a><span data-ttu-id="b2687-103">la \_ \_ \_ señalización de OPM y \_ CGMSA de \_ OPM</span><span class="sxs-lookup"><span data-stu-id="b2687-103">OPM\_GET\_ACP\_AND\_CGMSA\_SIGNALING</span></span>

<span data-ttu-id="b2687-104">Devuelve la siguiente información sobre una salida de vídeo:</span><span class="sxs-lookup"><span data-stu-id="b2687-104">Returns the following information about a video output:</span></span>

-   <span data-ttu-id="b2687-105">Una lista de los estándares de protección de televisión que admite el controlador.</span><span class="sxs-lookup"><span data-stu-id="b2687-105">A list of television protection standards supported by the driver.</span></span>
-   <span data-ttu-id="b2687-106">Estándar que está activo actualmente.</span><span class="sxs-lookup"><span data-stu-id="b2687-106">The standard that is currently active.</span></span>
-   <span data-ttu-id="b2687-107">La relación de aspecto actual u otros datos de señalización.</span><span class="sxs-lookup"><span data-stu-id="b2687-107">The current aspect ratio or other signaling data.</span></span>



| <span data-ttu-id="b2687-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="b2687-108">Requirement</span></span> | <span data-ttu-id="b2687-109">Value</span><span class="sxs-lookup"><span data-stu-id="b2687-109">Value</span></span> |
|--------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="b2687-110">GUID de solicitud</span><span class="sxs-lookup"><span data-stu-id="b2687-110">Request GUID</span></span> | <span data-ttu-id="b2687-111">la \_ \_ \_ señalización de OPM y \_ CGMSA de \_ OPM</span><span class="sxs-lookup"><span data-stu-id="b2687-111">OPM\_GET\_ACP\_AND\_CGMSA\_SIGNALING</span></span>                                                |
| <span data-ttu-id="b2687-112">Datos de entrada</span><span class="sxs-lookup"><span data-stu-id="b2687-112">Input data</span></span>   | <span data-ttu-id="b2687-113">None</span><span class="sxs-lookup"><span data-stu-id="b2687-113">None</span></span>                                                                                |
| <span data-ttu-id="b2687-114">Devolver datos</span><span class="sxs-lookup"><span data-stu-id="b2687-114">Return data</span></span>  | <span data-ttu-id="b2687-115">Una [**estructura \_ \_ de \_ \_ señalización de CGMSA y ACP de OPM**](/windows/desktop/api/opmapi/ns-opmapi-opm_acp_and_cgmsa_signaling)</span><span class="sxs-lookup"><span data-stu-id="b2687-115">An [**OPM\_ACP\_AND\_CGMSA\_SIGNALING**](/windows/desktop/api/opmapi/ns-opmapi-opm_acp_and_cgmsa_signaling) structure</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="b2687-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b2687-116">Remarks</span></span>

<span data-ttu-id="b2687-117">Esta consulta es equivalente a la \_ consulta COPPQuerySignaling de DXVA usada en el protocolo de protección de la salida certificada (COPP).</span><span class="sxs-lookup"><span data-stu-id="b2687-117">This query is equivalent to the DXVA\_COPPQuerySignaling query used in Certified Output Protection Protocol (COPP).</span></span>

## <a name="requirements"></a><span data-ttu-id="b2687-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b2687-118">Requirements</span></span>



| <span data-ttu-id="b2687-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="b2687-119">Requirement</span></span> | <span data-ttu-id="b2687-120">Value</span><span class="sxs-lookup"><span data-stu-id="b2687-120">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="b2687-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b2687-121">Minimum supported client</span></span><br/> | <span data-ttu-id="b2687-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="b2687-122">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="b2687-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b2687-123">Minimum supported server</span></span><br/> | <span data-ttu-id="b2687-124">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="b2687-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="b2687-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b2687-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="b2687-126"><dt>Opmapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="b2687-126"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2687-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="b2687-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2687-128">**IOPMVideoOutput:: COPPCompatibleGetInformation**</span><span class="sxs-lookup"><span data-stu-id="b2687-128">**IOPMVideoOutput::COPPCompatibleGetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation)
</dt> <dt>

[<span data-ttu-id="b2687-129">**IOPMVideoOutput:: GetInformation**</span><span class="sxs-lookup"><span data-stu-id="b2687-129">**IOPMVideoOutput::GetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> <dt>

[<span data-ttu-id="b2687-130">Solicitudes de estado de OPM</span><span class="sxs-lookup"><span data-stu-id="b2687-130">OPM Status Requests</span></span>](opm-status-requests.md)
</dt> </dl>

 

 




