---
description: Devuelve el nivel de protección global para un mecanismo de protección especificado.
ms.assetid: 3dd4f6f0-2305-4470-bbd4-7737fa2d8eae
title: OPM_GET_ACTUAL_PROTECTION_LEVEL (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 960d704fd44ca779f128795b26603698bb0ad622
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082293"
---
# <a name="opm_get_actual_protection_level"></a><span data-ttu-id="9e99b-103">\_obtener \_ nivel de \_ protección \_ real de OPM</span><span class="sxs-lookup"><span data-stu-id="9e99b-103">OPM\_GET\_ACTUAL\_PROTECTION\_LEVEL</span></span>

<span data-ttu-id="9e99b-104">Devuelve el nivel de protección global para un mecanismo de protección especificado.</span><span class="sxs-lookup"><span data-stu-id="9e99b-104">Returns the global protection level for a specified protection mechanism.</span></span>



| <span data-ttu-id="9e99b-105">Requisito</span><span class="sxs-lookup"><span data-stu-id="9e99b-105">Requirement</span></span> | <span data-ttu-id="9e99b-106">Value</span><span class="sxs-lookup"><span data-stu-id="9e99b-106">Value</span></span> |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e99b-107">GUID de solicitud</span><span class="sxs-lookup"><span data-stu-id="9e99b-107">Request GUID</span></span> | <span data-ttu-id="9e99b-108">\_obtener \_ nivel de \_ protección \_ real de OPM</span><span class="sxs-lookup"><span data-stu-id="9e99b-108">OPM\_GET\_ACTUAL\_PROTECTION\_LEVEL</span></span>                                                                                                                                       |
| <span data-ttu-id="9e99b-109">Datos de entrada</span><span class="sxs-lookup"><span data-stu-id="9e99b-109">Input data</span></span>   | <span data-ttu-id="9e99b-110">Mecanismo de protección que se va a consultar, especificado como un entero de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="9e99b-110">The protection mechanism to query, specified as a 32-bit integer.</span></span> <span data-ttu-id="9e99b-111">El valor se interpreta como un miembro de las [marcas de tipo de protección OPM](opm-protection-type-flags.md).</span><span class="sxs-lookup"><span data-stu-id="9e99b-111">The value is interpreted as a member of the [OPM Protection Type Flags](opm-protection-type-flags.md).</span></span> |
| <span data-ttu-id="9e99b-112">Devolver datos</span><span class="sxs-lookup"><span data-stu-id="9e99b-112">Return data</span></span>  | <span data-ttu-id="9e99b-113">Una estructura de [**\_ \_ información estándar de OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information)</span><span class="sxs-lookup"><span data-stu-id="9e99b-113">An [**OPM\_STANDARD\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) structure</span></span>                                                                                               |



 

## <a name="remarks"></a><span data-ttu-id="9e99b-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9e99b-114">Remarks</span></span>

<span data-ttu-id="9e99b-115">El nivel de protección global es el nivel de protección que se está aplicando actualmente en el conector, independientemente de cómo se haya indicado al controlador de gráficos que aplique la protección.</span><span class="sxs-lookup"><span data-stu-id="9e99b-115">The global protection level is the protection level that is currently being applied on the connector, regardless of how the graphics driver was instructed to apply the protection.</span></span> <span data-ttu-id="9e99b-116">Por ejemplo, una aplicación puede establecer el nivel de protección ACP llamando a la función **ChangeDisplaySettingsEx** .</span><span class="sxs-lookup"><span data-stu-id="9e99b-116">For example, an application can set the ACP protection level by calling the **ChangeDisplaySettingsEx** function.</span></span> <span data-ttu-id="9e99b-117">En ese caso, el nivel de protección global reflejaría esta configuración, aunque no se solicitó a través de Output Protection Manager (OPM).</span><span class="sxs-lookup"><span data-stu-id="9e99b-117">In that case, the global protection level would reflect this setting, even though it was not requested through Output Protection Manager (OPM).</span></span>

<span data-ttu-id="9e99b-118">El nivel de protección se devuelve en el miembro **ulInformation** de la estructura de [**\_ \_ información estándar de OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) .</span><span class="sxs-lookup"><span data-stu-id="9e99b-118">The protection level is returned in the **ulInformation** member of the [**OPM\_STANDARD\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) structure.</span></span> <span data-ttu-id="9e99b-119">El significado de este valor depende del mecanismo de protección que se consulta.</span><span class="sxs-lookup"><span data-stu-id="9e99b-119">The meaning of this value depends on the protection mechanism that is queried.</span></span> <span data-ttu-id="9e99b-120">Para cada mecanismo de protección, el valor de **ulInformation** es una marca de una enumeración diferente, como se muestra en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="9e99b-120">For each protection mechanism, the value of **ulInformation** is a flag from a different enumeration, as shown in the following table.</span></span>



| <span data-ttu-id="9e99b-121">Mecanismo de protección</span><span class="sxs-lookup"><span data-stu-id="9e99b-121">Protection mechanism</span></span> | <span data-ttu-id="9e99b-122">Enumeración</span><span class="sxs-lookup"><span data-stu-id="9e99b-122">Enumeration</span></span>                                                       |
|----------------------|-------------------------------------------------------------------|
| <span data-ttu-id="9e99b-123">ACP</span><span class="sxs-lookup"><span data-stu-id="9e99b-123">ACP</span></span>                  | [<span data-ttu-id="9e99b-124">**nivel de protección de OPM \_ ACP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="9e99b-124">**OPM\_ACP\_PROTECTION\_LEVEL**</span></span>](/windows/desktop/api/opmapi/ne-opmapi-opm_acp_protection_level)   |
| <span data-ttu-id="9e99b-125">CGMS-A</span><span class="sxs-lookup"><span data-stu-id="9e99b-125">CGMS-A</span></span>               | [<span data-ttu-id="9e99b-126">Marcas de protección de CGMS-A</span><span class="sxs-lookup"><span data-stu-id="9e99b-126">CGMS-A Protection Flags</span></span>](cgms-a-protection-flags.md)            |
| <span data-ttu-id="9e99b-127">DPCP</span><span class="sxs-lookup"><span data-stu-id="9e99b-127">DPCP</span></span>                 | [<span data-ttu-id="9e99b-128">**\_nivel de \_ protección de DPCP de OPM \_**</span><span class="sxs-lookup"><span data-stu-id="9e99b-128">**OPM\_DPCP\_PROTECTION\_LEVEL**</span></span>](/windows/desktop/api/opmapi/ne-opmapi-opm_dpcp_protection_level) |
| <span data-ttu-id="9e99b-129">HDCP</span><span class="sxs-lookup"><span data-stu-id="9e99b-129">HDCP</span></span>                 | [<span data-ttu-id="9e99b-130">**\_nivel de \_ protección de HDCP de OPM \_**</span><span class="sxs-lookup"><span data-stu-id="9e99b-130">**OPM\_HDCP\_PROTECTION\_LEVEL**</span></span>](/windows/desktop/api/opmapi/ne-opmapi-opm_hdcp_protection_level) |



 

<span data-ttu-id="9e99b-131">Esta consulta es equivalente a la \_ consulta COPPQueryGlobalProtectionLevel de DXVA usada en el protocolo de protección de la salida certificada (COPP).</span><span class="sxs-lookup"><span data-stu-id="9e99b-131">This query is equivalent to the DXVA\_COPPQueryGlobalProtectionLevel query used in Certified Output Protection Protocol (COPP).</span></span>

## <a name="requirements"></a><span data-ttu-id="9e99b-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9e99b-132">Requirements</span></span>



| <span data-ttu-id="9e99b-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="9e99b-133">Requirement</span></span> | <span data-ttu-id="9e99b-134">Value</span><span class="sxs-lookup"><span data-stu-id="9e99b-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="9e99b-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9e99b-135">Minimum supported client</span></span><br/> | <span data-ttu-id="9e99b-136">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="9e99b-136">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="9e99b-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9e99b-137">Minimum supported server</span></span><br/> | <span data-ttu-id="9e99b-138">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="9e99b-138">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="9e99b-139">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9e99b-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="9e99b-140"><dt>Opmapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="9e99b-140"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9e99b-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="9e99b-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e99b-142">**IOPMVideoOutput:: COPPCompatibleGetInformation**</span><span class="sxs-lookup"><span data-stu-id="9e99b-142">**IOPMVideoOutput::COPPCompatibleGetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation)
</dt> <dt>

[<span data-ttu-id="9e99b-143">**IOPMVideoOutput:: GetInformation**</span><span class="sxs-lookup"><span data-stu-id="9e99b-143">**IOPMVideoOutput::GetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> <dt>

[<span data-ttu-id="9e99b-144">Solicitudes de estado de OPM</span><span class="sxs-lookup"><span data-stu-id="9e99b-144">OPM Status Requests</span></span>](opm-status-requests.md)
</dt> </dl>

 

 




