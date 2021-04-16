---
description: Devuelve el nivel de protección virtual para un mecanismo de protección especificado.
ms.assetid: 635d54de-2735-4390-8bac-ba63b9503909
title: OPM_GET_VIRTUAL_PROTECTION_LEVEL (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c7ac36abd0a043a74a18401205bbb5e661ac17d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696682"
---
# <a name="opm_get_virtual_protection_level"></a><span data-ttu-id="77d18-103">\_nivel de \_ \_ protección virtual \_ de OPM</span><span class="sxs-lookup"><span data-stu-id="77d18-103">OPM\_GET\_VIRTUAL\_PROTECTION\_LEVEL</span></span>

<span data-ttu-id="77d18-104">Devuelve el nivel de protección virtual para un mecanismo de protección especificado.</span><span class="sxs-lookup"><span data-stu-id="77d18-104">Returns the virtual protection level for a specified protection mechanism.</span></span>

<span data-ttu-id="77d18-105">El nivel de protección *virtual* es el nivel solicitado por la aplicación durante la sesión actual de Output Protection Manager (OPM).</span><span class="sxs-lookup"><span data-stu-id="77d18-105">The *virtual* protection level is the level requested by the application during the current Output Protection Manager (OPM) session.</span></span> <span data-ttu-id="77d18-106">El controlador puede aplicar un nivel superior, debido a eventos fuera de esta sesión OPM.</span><span class="sxs-lookup"><span data-stu-id="77d18-106">The driver might apply a higher level, due to events outside of this OPM session.</span></span> <span data-ttu-id="77d18-107">Para buscar el nivel de protección real que está en vigor, envíe la consulta de [**\_ nivel de \_ \_ protección \_ OPM real**](opm-get-actual-protection-level.md) .</span><span class="sxs-lookup"><span data-stu-id="77d18-107">To find the actual protection level that is in effect, send the [**OPM\_GET\_ACTUAL\_PROTECTION\_LEVEL**](opm-get-actual-protection-level.md) query.</span></span>



| <span data-ttu-id="77d18-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="77d18-108">Requirement</span></span> | <span data-ttu-id="77d18-109">Value</span><span class="sxs-lookup"><span data-stu-id="77d18-109">Value</span></span> |
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="77d18-110">GUID de solicitud</span><span class="sxs-lookup"><span data-stu-id="77d18-110">Request GUID</span></span> | <span data-ttu-id="77d18-111">\_nivel de \_ \_ protección virtual \_ de OPM</span><span class="sxs-lookup"><span data-stu-id="77d18-111">OPM\_GET\_VIRTUAL\_PROTECTION\_LEVEL</span></span>                                                                                                                                          |
| <span data-ttu-id="77d18-112">Datos de entrada</span><span class="sxs-lookup"><span data-stu-id="77d18-112">Input data</span></span>   | <span data-ttu-id="77d18-113">Mecanismo de protección que se va a consultar, especificado como un entero de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="77d18-113">The protection mechanism to query, specified as a 32-bit integer.</span></span> <span data-ttu-id="77d18-114">El valor se interpreta como un miembro de las [**marcas de tipo de protección OPM**](opm-protection-type-flags.md).</span><span class="sxs-lookup"><span data-stu-id="77d18-114">The value is interpreted as a member of the [**OPM Protection Type Flags**](opm-protection-type-flags.md).</span></span> |
| <span data-ttu-id="77d18-115">Devolver datos</span><span class="sxs-lookup"><span data-stu-id="77d18-115">Return data</span></span>  | <span data-ttu-id="77d18-116">Una estructura de [**\_ \_ información estándar de OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information)</span><span class="sxs-lookup"><span data-stu-id="77d18-116">An [**OPM\_STANDARD\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) structure</span></span>                                                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="77d18-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="77d18-117">Remarks</span></span>

<span data-ttu-id="77d18-118">El nivel de protección se devuelve en el miembro **ulInformation** de la estructura de [**\_ \_ información estándar de OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) .</span><span class="sxs-lookup"><span data-stu-id="77d18-118">The protection level is returned in the **ulInformation** member of the [**OPM\_STANDARD\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) structure.</span></span> <span data-ttu-id="77d18-119">El significado de este valor depende del mecanismo de protección que se consulta.</span><span class="sxs-lookup"><span data-stu-id="77d18-119">The meaning of this value depends on the protection mechanism that is queried.</span></span> <span data-ttu-id="77d18-120">Para cada mecanismo de protección, el valor de **ulInformation** es una marca de una enumeración diferente, como se muestra en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="77d18-120">For each protection mechanism, the value of **ulInformation** is a flag from a different enumeration, as shown in the following table.</span></span>



| <span data-ttu-id="77d18-121">Mecanismo de protección</span><span class="sxs-lookup"><span data-stu-id="77d18-121">Protection mechanism</span></span> | <span data-ttu-id="77d18-122">Enumeración</span><span class="sxs-lookup"><span data-stu-id="77d18-122">Enumeration</span></span>                                                       |
|----------------------|-------------------------------------------------------------------|
| <span data-ttu-id="77d18-123">ACP</span><span class="sxs-lookup"><span data-stu-id="77d18-123">ACP</span></span>                  | [<span data-ttu-id="77d18-124">**nivel de protección de OPM \_ ACP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="77d18-124">**OPM\_ACP\_PROTECTION\_LEVEL**</span></span>](/windows/desktop/api/opmapi/ne-opmapi-opm_acp_protection_level)   |
| <span data-ttu-id="77d18-125">CGMS-A</span><span class="sxs-lookup"><span data-stu-id="77d18-125">CGMS-A</span></span>               | [<span data-ttu-id="77d18-126">**Marcas de protección de CGMS-A**</span><span class="sxs-lookup"><span data-stu-id="77d18-126">**CGMS-A Protection Flags**</span></span>](cgms-a-protection-flags.md)        |
| <span data-ttu-id="77d18-127">DPCP</span><span class="sxs-lookup"><span data-stu-id="77d18-127">DPCP</span></span>                 | [<span data-ttu-id="77d18-128">**\_nivel de \_ protección de DPCP de OPM \_**</span><span class="sxs-lookup"><span data-stu-id="77d18-128">**OPM\_DPCP\_PROTECTION\_LEVEL**</span></span>](/windows/desktop/api/opmapi/ne-opmapi-opm_dpcp_protection_level) |
| <span data-ttu-id="77d18-129">HDCP</span><span class="sxs-lookup"><span data-stu-id="77d18-129">HDCP</span></span>                 | [<span data-ttu-id="77d18-130">**\_nivel de \_ protección de HDCP de OPM \_**</span><span class="sxs-lookup"><span data-stu-id="77d18-130">**OPM\_HDCP\_PROTECTION\_LEVEL**</span></span>](/windows/desktop/api/opmapi/ne-opmapi-opm_hdcp_protection_level) |



 

<span data-ttu-id="77d18-131">Esta consulta es equivalente a la \_ consulta COPPQueryLocalProtectionLevel de DXVA usada en el protocolo de protección de la salida certificada (COPP).</span><span class="sxs-lookup"><span data-stu-id="77d18-131">This query is equivalent to the DXVA\_COPPQueryLocalProtectionLevel query used in Certified Output Protection Protocol (COPP).</span></span>

## <a name="requirements"></a><span data-ttu-id="77d18-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="77d18-132">Requirements</span></span>



| <span data-ttu-id="77d18-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="77d18-133">Requirement</span></span> | <span data-ttu-id="77d18-134">Value</span><span class="sxs-lookup"><span data-stu-id="77d18-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="77d18-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="77d18-135">Minimum supported client</span></span><br/> | <span data-ttu-id="77d18-136">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="77d18-136">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="77d18-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="77d18-137">Minimum supported server</span></span><br/> | <span data-ttu-id="77d18-138">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="77d18-138">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="77d18-139">Encabezado</span><span class="sxs-lookup"><span data-stu-id="77d18-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="77d18-140"><dt>Opmapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="77d18-140"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="77d18-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="77d18-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77d18-142">**IOPMVideoOutput:: COPPCompatibleGetInformation**</span><span class="sxs-lookup"><span data-stu-id="77d18-142">**IOPMVideoOutput::COPPCompatibleGetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation)
</dt> <dt>

[<span data-ttu-id="77d18-143">**IOPMVideoOutput:: GetInformation**</span><span class="sxs-lookup"><span data-stu-id="77d18-143">**IOPMVideoOutput::GetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> <dt>

[<span data-ttu-id="77d18-144">Solicitudes de estado de OPM</span><span class="sxs-lookup"><span data-stu-id="77d18-144">OPM Status Requests</span></span>](opm-status-requests.md)
</dt> </dl>

 

 




