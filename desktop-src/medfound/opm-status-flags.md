---
description: En las marcas de la tabla siguiente se especifica el estado de una sesión de Output Protection Manager (OPM).
ms.assetid: d6d85fd4-e735-4610-93e0-bb2b1782f11b
title: Marcas de estado de OPM (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0cbf9d299d6d53a26a61d19372e56e42bd2cdf99
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543854"
---
# <a name="opm-status-flags"></a><span data-ttu-id="d2d0e-103">Marcas de estado de OPM</span><span class="sxs-lookup"><span data-stu-id="d2d0e-103">OPM Status Flags</span></span>

<span data-ttu-id="d2d0e-104">En las marcas de la tabla siguiente se especifica el estado de una sesión de Output Protection Manager (OPM).</span><span class="sxs-lookup"><span data-stu-id="d2d0e-104">The flags in the following table specify the status of an Output Protection Manager (OPM) session.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="d2d0e-105">Constante o valor</span><span class="sxs-lookup"><span data-stu-id="d2d0e-105">Constant/value</span></span></th>
<th style="text-align: left;"><span data-ttu-id="d2d0e-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="d2d0e-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="OPM_STATUS_NORMAL"></span><span id="opm_status_normal"></span><dl> <span data-ttu-id="d2d0e-107"><dt><strong>OPM_STATUS_NORMAL</strong></dt> <dt>0x00</dt> </span><span class="sxs-lookup"><span data-stu-id="d2d0e-107"><dt><strong>OPM_STATUS_NORMAL</strong></dt> <dt>0x00</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="d2d0e-108">Estado normal.</span><span class="sxs-lookup"><span data-stu-id="d2d0e-108">Normal status.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="OPM_STATUS_LINK_LOST"></span><span id="opm_status_link_lost"></span><dl> <span data-ttu-id="d2d0e-109"><dt><strong>OPM_STATUS_LINK_LOST</strong></dt> <dt>0x01</dt> </span><span class="sxs-lookup"><span data-stu-id="d2d0e-109"><dt><strong>OPM_STATUS_LINK_LOST</strong></dt> <dt>0x01</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="d2d0e-110">Se ha puesto en peligro la integridad de la conexión.</span><span class="sxs-lookup"><span data-stu-id="d2d0e-110">The integrity of the connection has been compromised.</span></span> <span data-ttu-id="d2d0e-111">Entre los ejemplos de eventos que hacen que el controlador establezca esta marca se incluyen:</span><span class="sxs-lookup"><span data-stu-id="d2d0e-111">Examples of events that cause the driver to set this flag include:</span></span><br/>
<ul>
<li><span data-ttu-id="d2d0e-112">El controlador ya no puede aplicar el nivel de protección actual.</span><span class="sxs-lookup"><span data-stu-id="d2d0e-112">The driver can no longer enforce the current protection level.</span></span></li>
<li><span data-ttu-id="d2d0e-113">El controlador ha detectado un error de integridad interno.</span><span class="sxs-lookup"><span data-stu-id="d2d0e-113">The driver detected an internal integrity error.</span></span></li>
<li><span data-ttu-id="d2d0e-114">Se desconectó el conector entre el equipo y el dispositivo de pantalla.</span><span class="sxs-lookup"><span data-stu-id="d2d0e-114">The connector between the computer and the display device was unplugged.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="OPM_STATUS_RENEGOTIATION_REQUIRED"></span><span id="opm_status_renegotiation_required"></span><dl> <span data-ttu-id="d2d0e-115"><dt><strong>OPM_STATUS_RENEGOTIATION_REQUIRED</strong></dt> <dt>0x02</dt> </span><span class="sxs-lookup"><span data-stu-id="d2d0e-115"><dt><strong>OPM_STATUS_RENEGOTIATION_REQUIRED</strong></dt> <dt>0x02</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="d2d0e-116">La configuración de la conexión ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="d2d0e-116">The connection configuration has changed.</span></span> <span data-ttu-id="d2d0e-117">Por ejemplo, el usuario ha cambiado el modo de presentación del escritorio.</span><span class="sxs-lookup"><span data-stu-id="d2d0e-117">For example, the user has changed the desktop display mode.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="OPM_STATUS_TAMPERING_DETECTED"></span><span id="opm_status_tampering_detected"></span><dl> <span data-ttu-id="d2d0e-118"><dt><strong>OPM_STATUS_TAMPERING_DETECTED</strong></dt> <dt>0x04</dt> </span><span class="sxs-lookup"><span data-stu-id="d2d0e-118"><dt><strong>OPM_STATUS_TAMPERING_DETECTED</strong></dt> <dt>0x04</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="d2d0e-119">El adaptador de gráficos o el controlador se han alterado.</span><span class="sxs-lookup"><span data-stu-id="d2d0e-119">The graphics adapter or the driver has been tampered with.</span></span><br/> <span data-ttu-id="d2d0e-120">Esta marca no se usa en el <em>modo de emulación de COPP</em>.</span><span class="sxs-lookup"><span data-stu-id="d2d0e-120">This flag is not used in <em>COPP emulation mode</em>.</span></span> <span data-ttu-id="d2d0e-121">En su lugar, la salida de vídeo establecerá la marca de OPM_STATUS_LINK_LOST si detecta alteraciones.</span><span class="sxs-lookup"><span data-stu-id="d2d0e-121">Instead, the video output will set the OPM_STATUS_LINK_LOST flag if it detects tampering.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="OPM_STATUS_REVOKED_HDCP_DEVICE_ATTACHED"></span><span id="opm_status_revoked_hdcp_device_attached"></span><dl> <span data-ttu-id="d2d0e-122"><dt><strong>OPM_STATUS_REVOKED_HDCP_DEVICE_ATTACHED</strong></dt> <dt>0x08</dt> </span><span class="sxs-lookup"><span data-stu-id="d2d0e-122"><dt><strong>OPM_STATUS_REVOKED_HDCP_DEVICE_ATTACHED</strong></dt> <dt>0x08</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="d2d0e-123">Un dispositivo High-Bandwidth Digital Content Protection (HDCP) revocado se adjunta a la salida de vídeo.</span><span class="sxs-lookup"><span data-stu-id="d2d0e-123">A revoked High-Bandwidth Digital Content Protection (HDCP) device is attached to the video output.</span></span><br/> <span data-ttu-id="d2d0e-124">Esta marca de estado se puede devolver desde una <a href="opm-get-virtual-protection-level.md">OPM_GET_VIRTUAL_PROTECTION_LEVEL</a> o <a href="opm-get-actual-protection-level.md">OPM_GET_ACTUAL_PROTECTION_LEVEL</a> consulta.</span><span class="sxs-lookup"><span data-stu-id="d2d0e-124">This status flag can be returned from an <a href="opm-get-virtual-protection-level.md">OPM_GET_VIRTUAL_PROTECTION_LEVEL</a> or <a href="opm-get-actual-protection-level.md">OPM_GET_ACTUAL_PROTECTION_LEVEL</a> query.</span></span> <br/> <span data-ttu-id="d2d0e-125">El dispositivo revocado puede estar conectado directamente a la salida de vídeo o indirectamente a través de un repetidor de HDCP.</span><span class="sxs-lookup"><span data-stu-id="d2d0e-125">The revoked device might be attached directly to the video output, or indirectly through an HDCP repeater.</span></span> <span data-ttu-id="d2d0e-126">Se necesita una salida de vídeo para detectar esta condición mientras se habilita HDCP, pero no.</span><span class="sxs-lookup"><span data-stu-id="d2d0e-126">A video output is required to detect this condition while HDCP is enabled, but not otherwise.</span></span><br/> <span data-ttu-id="d2d0e-127">Esta marca no se usa en el <em>modo de emulación de COPP</em>porque la salida de vídeo no detecta los dispositivos revocados en ese modo.</span><span class="sxs-lookup"><span data-stu-id="d2d0e-127">This flag is not used in <em>COPP emulation mode</em>, because the video output does not detect revoked devices in that mode.</span></span><br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="d2d0e-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d2d0e-128">Remarks</span></span>

<span data-ttu-id="d2d0e-129">Algunas de estas constantes son equivalentes a los valores de la enumeración **COPP \_ StatusFlags** usada en el protocolo de protección de la salida certificada (COPP).</span><span class="sxs-lookup"><span data-stu-id="d2d0e-129">Some of these constants are equivalent to values from the **COPP\_StatusFlags** enumeration used in Certified Output Protection Protocol (COPP).</span></span>

## <a name="requirements"></a><span data-ttu-id="d2d0e-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d2d0e-130">Requirements</span></span>



| <span data-ttu-id="d2d0e-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="d2d0e-131">Requirement</span></span> | <span data-ttu-id="d2d0e-132">Value</span><span class="sxs-lookup"><span data-stu-id="d2d0e-132">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="d2d0e-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d2d0e-133">Minimum supported client</span></span><br/> | <span data-ttu-id="d2d0e-134">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="d2d0e-134">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="d2d0e-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d2d0e-135">Minimum supported server</span></span><br/> | <span data-ttu-id="d2d0e-136">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="d2d0e-136">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="d2d0e-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d2d0e-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="d2d0e-138"><dt>Opmapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="d2d0e-138"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d2d0e-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="d2d0e-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2d0e-140">Enumeraciones de OPM</span><span class="sxs-lookup"><span data-stu-id="d2d0e-140">OPM Enumerations</span></span>](opm-enumerations.md)
</dt> </dl>

 

 




