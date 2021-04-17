---
description: En las marcas de la tabla siguiente se especifican los mecanismos de protección de salida para el administrador de protección de salida (OPM).
ms.assetid: 484dfea9-301d-4b2b-b5d1-d785ebaa8c8f
title: Marcas de tipo de protección OPM (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1cc8b30a18f5c7bf68fb01775751aa56e1e619f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715522"
---
# <a name="opm-protection-type-flags"></a><span data-ttu-id="7819a-103">Marcas de tipo de protección OPM</span><span class="sxs-lookup"><span data-stu-id="7819a-103">OPM Protection Type Flags</span></span>

<span data-ttu-id="7819a-104">En las marcas de la tabla siguiente se especifican los mecanismos de protección de salida para el administrador de protección de salida (OPM).</span><span class="sxs-lookup"><span data-stu-id="7819a-104">The flags in the following table specify output protection mechanisms for Output Protection Manager (OPM).</span></span>



| <span data-ttu-id="7819a-105">Constante o valor</span><span class="sxs-lookup"><span data-stu-id="7819a-105">Constant/value</span></span>                                                                                                                                                                                                                                                                                                     | <span data-ttu-id="7819a-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="7819a-106">Description</span></span>                                                                                                                                                                                                                 |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OPM_PROTECTION_TYPE_OTHER"></span><span id="opm_protection_type_other"></span><dl> <span data-ttu-id="7819a-107"><dt>**OPM \_ Tipo de protección \_ \_ otro**</dt> <dt>0x80000000</dt></span><span class="sxs-lookup"><span data-stu-id="7819a-107"><dt>**OPM\_PROTECTION\_TYPE\_OTHER**</dt> <dt>0x80000000</dt></span></span> </dl>                                                | <span data-ttu-id="7819a-108">Mecanismo de protección desconocido.</span><span class="sxs-lookup"><span data-stu-id="7819a-108">Unknown protection mechanism.</span></span><br/>                                                                                                                                                                                    |
| <span id="OPM_PROTECTION_TYPE_NONE"></span><span id="opm_protection_type_none"></span><dl> <span data-ttu-id="7819a-109"><dt>**OPM \_ Tipo de protección \_ \_ ninguno**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="7819a-109"><dt>**OPM\_PROTECTION\_TYPE\_NONE**</dt> <dt>0x00000000</dt></span></span> </dl>                                                   | <span data-ttu-id="7819a-110">Sin mecanismos de protección.</span><span class="sxs-lookup"><span data-stu-id="7819a-110">No protection mechanisms.</span></span><br/>                                                                                                                                                                                        |
| <span id="OPM_PROTECTION_TYPE_COPP_COMPATIBLE_HDCP"></span><span id="opm_protection_type_copp_compatible_hdcp"></span><dl> <span data-ttu-id="7819a-111"><dt>**OPM \_ Tipo de protección de \_ \_ \_ \_ HDCP compatible con COPP**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="7819a-111"><dt>**OPM\_PROTECTION\_TYPE\_COPP\_COMPATIBLE\_HDCP**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="7819a-112">High-Bandwidth Digital Content Protection (HDCP).</span><span class="sxs-lookup"><span data-stu-id="7819a-112">High-Bandwidth Digital Content Protection (HDCP).</span></span> <span data-ttu-id="7819a-113">Esta marca se usa al emular el protocolo de protección de la salida (COPP).</span><span class="sxs-lookup"><span data-stu-id="7819a-113">This flag is used when emulating Certified Output Protection Protocol (COPP).</span></span> <span data-ttu-id="7819a-114">Para obtener más información, vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="7819a-114">For more information, see Remarks.</span></span> <span data-ttu-id="7819a-115">Esta marca no se admite para la semántica de OPM.</span><span class="sxs-lookup"><span data-stu-id="7819a-115">This flag is not supported for OPM semantics.</span></span><br/> |
| <span id="OPM_PROTECTION_TYPE_ACP"></span><span id="opm_protection_type_acp"></span><dl> <span data-ttu-id="7819a-116"><dt>**OPM \_ Tipo de protección \_ \_ ACP**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="7819a-116"><dt>**OPM\_PROTECTION\_TYPE\_ACP**</dt> <dt>0x00000002</dt></span></span> </dl>                                                      | <span data-ttu-id="7819a-117">Protección de copia analógica (ACP).</span><span class="sxs-lookup"><span data-stu-id="7819a-117">Analog Copy Protection (ACP).</span></span><br/>                                                                                                                                                                                    |
| <span id="OPM_PROTECTION_TYPE_CGMSA"></span><span id="opm_protection_type_cgmsa"></span><dl> <span data-ttu-id="7819a-118"><dt>**OPM \_ Tipo de protección \_ \_ CGMSA**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="7819a-118"><dt>**OPM\_PROTECTION\_TYPE\_CGMSA**</dt> <dt>0x00000004</dt></span></span> </dl>                                                | <span data-ttu-id="7819a-119">Sistema de administración de generación de copias: analógico (CGMS-A).</span><span class="sxs-lookup"><span data-stu-id="7819a-119">Copy Generation Management System—Analog (CGMS-A).</span></span><br/>                                                                                                                                                               |
| <span id="OPM_PROTECTION_TYPE_HDCP"></span><span id="opm_protection_type_hdcp"></span><dl> <span data-ttu-id="7819a-120"><dt>**OPM \_ Tipo de protección \_ \_ HDCP**</dt> <dt>0x00000008</dt></span><span class="sxs-lookup"><span data-stu-id="7819a-120"><dt>**OPM\_PROTECTION\_TYPE\_HDCP**</dt> <dt>0x00000008</dt></span></span> </dl>                                                   | <span data-ttu-id="7819a-121">HDCP.</span><span class="sxs-lookup"><span data-stu-id="7819a-121">HDCP.</span></span> <span data-ttu-id="7819a-122">Esta marca se usa cuando el objeto OPM tiene semántica de OPM.</span><span class="sxs-lookup"><span data-stu-id="7819a-122">This flag is used when the OPM object has OPM semantics.</span></span> <span data-ttu-id="7819a-123">No se admite para la semántica de COPP.</span><span class="sxs-lookup"><span data-stu-id="7819a-123">It is not supported for COPP semantics.</span></span><br/>                                                                                                           |
| <span id="OPM_PROTECTION_TYPE_DPCP"></span><span id="opm_protection_type_dpcp"></span><dl> <span data-ttu-id="7819a-124"><dt>**OPM \_ Tipo de protección \_ \_ DPCP**</dt> <dt>0x00000010</dt></span><span class="sxs-lookup"><span data-stu-id="7819a-124"><dt>**OPM\_PROTECTION\_TYPE\_DPCP**</dt> <dt>0x00000010</dt></span></span> </dl>                                                   | <span data-ttu-id="7819a-125">Content Protection de DisplayPort (DPCP).</span><span class="sxs-lookup"><span data-stu-id="7819a-125">DisplayPort Content Protection (DPCP).</span></span><br/>                                                                                                                                                                           |



## <a name="remarks"></a><span data-ttu-id="7819a-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7819a-126">Remarks</span></span>

<span data-ttu-id="7819a-127">Estas marcas se usan en los siguientes comandos de OPM y solicitudes de estado.</span><span class="sxs-lookup"><span data-stu-id="7819a-127">These flags are used in the following OPM commands and status requests.</span></span>

-   [<span data-ttu-id="7819a-128">\_nivel de \_ protección de conjunto de OPM \_</span><span class="sxs-lookup"><span data-stu-id="7819a-128">OPM\_SET\_PROTECTION\_LEVEL</span></span>](opm-set-protection-level.md)
-   [<span data-ttu-id="7819a-129">\_nivel de \_ \_ protección virtual \_ de OPM</span><span class="sxs-lookup"><span data-stu-id="7819a-129">OPM\_GET\_VIRTUAL\_PROTECTION\_LEVEL</span></span>](opm-get-virtual-protection-level.md)
-   [<span data-ttu-id="7819a-130">\_obtener \_ nivel de \_ protección \_ real de OPM</span><span class="sxs-lookup"><span data-stu-id="7819a-130">OPM\_GET\_ACTUAL\_PROTECTION\_LEVEL</span></span>](opm-get-actual-protection-level.md)

### <a name="hdcp"></a><span data-ttu-id="7819a-131">HDCP</span><span class="sxs-lookup"><span data-stu-id="7819a-131">HDCP</span></span>

<span data-ttu-id="7819a-132">Las dos marcas siguientes están definidas para HDCP.</span><span class="sxs-lookup"><span data-stu-id="7819a-132">The following two flags are defined for HDCP.</span></span>



| <span data-ttu-id="7819a-133">Value</span><span class="sxs-lookup"><span data-stu-id="7819a-133">Value</span></span>                                         | <span data-ttu-id="7819a-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="7819a-134">Description</span></span>                                                                                                                                                                    |
|-----------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7819a-135">\_tipo de protección OPM \_ \_ HDCP</span><span class="sxs-lookup"><span data-stu-id="7819a-135">OPM\_PROTECTION\_TYPE\_HDCP</span></span>                   | <span data-ttu-id="7819a-136">Use esta marca si se ha creado el puntero [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) con semántica de OPM.</span><span class="sxs-lookup"><span data-stu-id="7819a-136">Use this flag if the [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) pointer was created with OPM semantics.</span></span>                                                                        |
| <span data-ttu-id="7819a-137">tipo de protección OPM, \_ \_ \_ \_ HDCP compatible con COPP \_</span><span class="sxs-lookup"><span data-stu-id="7819a-137">OPM\_PROTECTION\_TYPE\_COPP\_COMPATIBLE\_HDCP</span></span> | <span data-ttu-id="7819a-138">Use esta marca si el puntero [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) se creó con la semántica de COPP.</span><span class="sxs-lookup"><span data-stu-id="7819a-138">Use this flag if the [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) pointer was created with COPP semantics.</span></span> <span data-ttu-id="7819a-139">Esta marca corresponde a la \_ marca de \_ HDCP PROTECTIONTYPE de COPP en COPP.</span><span class="sxs-lookup"><span data-stu-id="7819a-139">This flag corresponds to the COPP\_ProtectionType\_HDCP flag in COPP.</span></span> |



 

<span data-ttu-id="7819a-140">Ambos modos (semántica de OPM y semántica de COPP) admiten las siguientes operaciones para HDCP:</span><span class="sxs-lookup"><span data-stu-id="7819a-140">Both modes (OPM semantics and COPP semantics) support the following operations for HDCP:</span></span>

-   <span data-ttu-id="7819a-141">Habilite o deshabilite HDCP mediante el comando de [nivel de protección de set de OPM \_ \_ \_ ](opm-set-protection-level.md) .</span><span class="sxs-lookup"><span data-stu-id="7819a-141">Enable or disable HDCP by using the [OPM\_SET\_PROTECTION\_LEVEL](opm-set-protection-level.md) command.</span></span>
-   <span data-ttu-id="7819a-142">Consulte si se ha habilitado HDCP mediante la solicitud de estado de nivel de [ \_ \_ \_ protección \_ virtual de OPM](opm-get-virtual-protection-level.md) o [OPM obtener estado de \_ \_ \_ protección \_ real](opm-get-actual-protection-level.md) .</span><span class="sxs-lookup"><span data-stu-id="7819a-142">Query whether HDCP is enabled by using the [OPM\_GET\_VIRTUAL\_PROTECTION\_LEVEL](opm-get-virtual-protection-level.md) or [OPM\_GET\_ACTUAL\_PROTECTION\_LEVEL](opm-get-actual-protection-level.md) status request.</span></span>

<span data-ttu-id="7819a-143">La semántica de OPM también admite lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="7819a-143">OPM semantics also support the following:</span></span>

-   <span data-ttu-id="7819a-144">Repetidores de HDCP.</span><span class="sxs-lookup"><span data-stu-id="7819a-144">HDCP repeaters.</span></span> <span data-ttu-id="7819a-145">Un *repetidor de HDCP* es un dispositivo HDCP que puede recibir contenido de HDCP y también volver a cifrar y transmitir el mismo contenido.</span><span class="sxs-lookup"><span data-stu-id="7819a-145">An *HDCP repeater* is an HDCP device that can receive HDCP content and also re-encrypt and transmit the same content.</span></span>
-   <span data-ttu-id="7819a-146">Revocación de HDCP.</span><span class="sxs-lookup"><span data-stu-id="7819a-146">HDCP revocation.</span></span> <span data-ttu-id="7819a-147">Si un dispositivo HDCP revocado está conectado a la salida de vídeo OPM, la salida de vídeo no transmitirá el vídeo.</span><span class="sxs-lookup"><span data-stu-id="7819a-147">If a revoked HDCP device is attached to the OPM video output, the video output will not transmit the video.</span></span> <span data-ttu-id="7819a-148">La aplicación no necesita analizar los mensajes de renovación del sistema HDCP (SRMs) o determinar si se ha revocado el dispositivo de salida.</span><span class="sxs-lookup"><span data-stu-id="7819a-148">The application does not need to parse HDCP system renewability messages (SRMs) or determine whether the output device has been revoked.</span></span> <span data-ttu-id="7819a-149">Para obtener más información, consulte el comando [**OPM \_ set \_ HDCP \_ SRM**](opm-set-hdcp-srm.md) .</span><span class="sxs-lookup"><span data-stu-id="7819a-149">For more information, see the [**OPM\_SET\_HDCP\_SRM**](opm-set-hdcp-srm.md) command.</span></span>

<span data-ttu-id="7819a-150">Cuando se usan semánticas de COPP, la interfaz [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) no admite repetidores de HDCP.</span><span class="sxs-lookup"><span data-stu-id="7819a-150">When COPP semantics are used, the [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) interface does not support HDCP repeaters.</span></span> <span data-ttu-id="7819a-151">Además, no controla la revocación de HDCP.</span><span class="sxs-lookup"><span data-stu-id="7819a-151">Also, it does not handle HDCP revocation.</span></span> <span data-ttu-id="7819a-152">En su lugar, la aplicación debe analizar el SRM para determinar si se ha revocado un dispositivo HDCP.</span><span class="sxs-lookup"><span data-stu-id="7819a-152">Instead, the application must parse the SRM to determine whether an HDCP device has been revoked.</span></span>

## <a name="requirements"></a><span data-ttu-id="7819a-153">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7819a-153">Requirements</span></span>



| <span data-ttu-id="7819a-154">Requisito</span><span class="sxs-lookup"><span data-stu-id="7819a-154">Requirement</span></span> | <span data-ttu-id="7819a-155">Value</span><span class="sxs-lookup"><span data-stu-id="7819a-155">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="7819a-156">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7819a-156">Minimum supported client</span></span><br/> | <span data-ttu-id="7819a-157">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="7819a-157">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="7819a-158">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7819a-158">Minimum supported server</span></span><br/> | <span data-ttu-id="7819a-159">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="7819a-159">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="7819a-160">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7819a-160">Header</span></span><br/>                   | <dl> <span data-ttu-id="7819a-161"><dt>Opmapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="7819a-161"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7819a-162">Vea también</span><span class="sxs-lookup"><span data-stu-id="7819a-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7819a-163">Enumeraciones de OPM</span><span class="sxs-lookup"><span data-stu-id="7819a-163">OPM Enumerations</span></span>](opm-enumerations.md)
</dt> </dl>

 

 




