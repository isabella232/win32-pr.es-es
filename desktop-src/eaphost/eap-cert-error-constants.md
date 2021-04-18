---
title: '\_Constantes de error de certificado EAP (Eaphosterror. h)'
description: Defina los errores relacionados con los certificados comunes a todas las tecnologías de API de EAPHost.
ms.assetid: 12f626e1-520a-4aba-954b-769c3062a38c
topic_type:
- apiref
api_name:
- _EAP_CERT_FIRST
- _EAP_CERT_LAST
- _EAP_CERT_NOT_FOUND
- _EAP_CERT_INVALID
- _EAP_CERT_EXPIRED
- _EAP_CERT_REVOKED
- _EAP_CERT_OTHER_ERROR
- _EAP_CERT_REJECTED
- _EAP_CERT_NAME_REQUIRED
- _EAP_GENERAL_FIRST
- _EAP_GENERAL_LAST
api_location:
- eaphosterror.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0543636f36d823b5557ad2f5a5f7cb000d93259a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104533903"
---
# <a name="eap_cert-error-constants"></a><span data-ttu-id="60277-103">\_Constantes de error de certificado EAP</span><span class="sxs-lookup"><span data-stu-id="60277-103">EAP\_CERT Error Constants</span></span>

<span data-ttu-id="60277-104">Estas constantes definen errores relacionados con los certificados comunes a todas las tecnologías de API de EAPHost.</span><span class="sxs-lookup"><span data-stu-id="60277-104">These constants define certificate-related errors common to all EAPHost API technologies.</span></span>

<dl> <dt>

<span data-ttu-id="60277-105"><span id="_EAP_CERT_FIRST"></span><span id="_eap_cert_first"></span>**\_\_certificado EAP \_ primero**</span><span class="sxs-lookup"><span data-stu-id="60277-105"><span id="_EAP_CERT_FIRST"></span><span id="_eap_cert_first"></span>**\_EAP\_CERT\_FIRST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60277-106">0x0</span><span class="sxs-lookup"><span data-stu-id="60277-106">0x0</span></span>
</dt> <dt>



<span data-ttu-id="60277-107">Define el límite de los informes de errores; en **\_ \_ \_ último** lugar, se producirá un error de certificado entre el certificado **\_ EAP \_ \_** y el certificado EAP.</span><span class="sxs-lookup"><span data-stu-id="60277-107">Defines the boundary of error reports; any certificate error will occur between **\_EAP\_CERT\_FIRST** and **\_EAP\_CERT\_LAST**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="60277-108"><span id="_EAP_CERT_LAST"></span><span id="_eap_cert_last"></span>**\_\_último certificado \_ EAP**</span><span class="sxs-lookup"><span data-stu-id="60277-108"><span id="_EAP_CERT_LAST"></span><span id="_eap_cert_last"></span>**\_EAP\_CERT\_LAST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60277-109">0xF</span><span class="sxs-lookup"><span data-stu-id="60277-109">0xF</span></span>
</dt> <dt>



<span data-ttu-id="60277-110">Define el límite de los informes de errores; en **\_ \_ \_ último** lugar, se producirá un error de certificado entre el certificado **\_ EAP \_ \_** y el certificado EAP.</span><span class="sxs-lookup"><span data-stu-id="60277-110">Defines the boundary of error reports; any certificate error will occur between **\_EAP\_CERT\_FIRST** and **\_EAP\_CERT\_LAST**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="60277-111"><span id="_EAP_CERT_NOT_FOUND"></span><span id="_eap_cert_not_found"></span>**\_\_ \_ no \_ se encontró el certificado EAP**</span><span class="sxs-lookup"><span data-stu-id="60277-111"><span id="_EAP_CERT_NOT_FOUND"></span><span id="_eap_cert_not_found"></span>**\_EAP\_CERT\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60277-112">0x1</span><span class="sxs-lookup"><span data-stu-id="60277-112">0x1</span></span>
</dt> <dt>



<span data-ttu-id="60277-113">No se encontró ningún certificado de usuario.</span><span class="sxs-lookup"><span data-stu-id="60277-113">No user certificate was found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="60277-114"><span id="_EAP_CERT_INVALID"></span><span id="_eap_cert_invalid"></span>**\_\_certificado EAP \_ no válido**</span><span class="sxs-lookup"><span data-stu-id="60277-114"><span id="_EAP_CERT_INVALID"></span><span id="_eap_cert_invalid"></span>**\_EAP\_CERT\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60277-115">0x2</span><span class="sxs-lookup"><span data-stu-id="60277-115">0x2</span></span>
</dt> <dt>



<span data-ttu-id="60277-116">El certificado de usuario no es válido.</span><span class="sxs-lookup"><span data-stu-id="60277-116">The user certificate is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="60277-117"><span id="_EAP_CERT_EXPIRED"></span><span id="_eap_cert_expired"></span>**\_\_certificado EAP \_ expirado**</span><span class="sxs-lookup"><span data-stu-id="60277-117"><span id="_EAP_CERT_EXPIRED"></span><span id="_eap_cert_expired"></span>**\_EAP\_CERT\_EXPIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60277-118">0x3</span><span class="sxs-lookup"><span data-stu-id="60277-118">0x3</span></span>
</dt> <dt>



<span data-ttu-id="60277-119">El certificado de usuario ha expirado.</span><span class="sxs-lookup"><span data-stu-id="60277-119">The user certificate has expired.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="60277-120"><span id="_EAP_CERT_REVOKED"></span><span id="_eap_cert_revoked"></span>**\_\_certificado EAP \_ revocado**</span><span class="sxs-lookup"><span data-stu-id="60277-120"><span id="_EAP_CERT_REVOKED"></span><span id="_eap_cert_revoked"></span>**\_EAP\_CERT\_REVOKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60277-121">0x4</span><span class="sxs-lookup"><span data-stu-id="60277-121">0x4</span></span>
</dt> <dt>



<span data-ttu-id="60277-122">Se revocó el certificado de usuario.</span><span class="sxs-lookup"><span data-stu-id="60277-122">The user certificate was revoked.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="60277-123"><span id="_EAP_CERT_OTHER_ERROR"></span><span id="_eap_cert_other_error"></span>**\_\_error de \_ otro \_ certificado EAP**</span><span class="sxs-lookup"><span data-stu-id="60277-123"><span id="_EAP_CERT_OTHER_ERROR"></span><span id="_eap_cert_other_error"></span>**\_EAP\_CERT\_OTHER\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60277-124">0X5</span><span class="sxs-lookup"><span data-stu-id="60277-124">0x5</span></span>
</dt> <dt>



<span data-ttu-id="60277-125">Error desconocido relacionado con el certificado.</span><span class="sxs-lookup"><span data-stu-id="60277-125">There is an unknown certificate related error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="60277-126"><span id="_EAP_CERT_REJECTED"></span><span id="_eap_cert_rejected"></span>**\_\_certificado EAP \_ rechazado**</span><span class="sxs-lookup"><span data-stu-id="60277-126"><span id="_EAP_CERT_REJECTED"></span><span id="_eap_cert_rejected"></span>**\_EAP\_CERT\_REJECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60277-127">0x6</span><span class="sxs-lookup"><span data-stu-id="60277-127">0x6</span></span>
</dt> <dt>



<span data-ttu-id="60277-128">Se rechazó el certificado de usuario.</span><span class="sxs-lookup"><span data-stu-id="60277-128">The user certificate was rejected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="60277-129"><span id="_EAP_CERT_NAME_REQUIRED"></span><span id="_eap_cert_name_required"></span>**\_se \_ \_ requiere el nombre de certificado EAP \_**</span><span class="sxs-lookup"><span data-stu-id="60277-129"><span id="_EAP_CERT_NAME_REQUIRED"></span><span id="_eap_cert_name_required"></span>**\_EAP\_CERT\_NAME\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60277-130">0X7</span><span class="sxs-lookup"><span data-stu-id="60277-130">0x7</span></span>
</dt> <dt>



<span data-ttu-id="60277-131">El certificado de usuario requiere un nombre.</span><span class="sxs-lookup"><span data-stu-id="60277-131">The user certificate requires a name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="60277-132"><span id="_EAP_GENERAL_FIRST"></span><span id="_eap_general_first"></span>**\_EAP \_ General \_ primero**</span><span class="sxs-lookup"><span data-stu-id="60277-132"><span id="_EAP_GENERAL_FIRST"></span><span id="_eap_general_first"></span>**\_EAP\_GENERAL\_FIRST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60277-133">0x10</span><span class="sxs-lookup"><span data-stu-id="60277-133">0x10</span></span>
</dt> <dt>



<span data-ttu-id="60277-134">Define el límite de los informes de errores; cualquier error de EAP general se producirá entre **\_ EAP \_ General \_ primero** y **\_ EAP \_ General en \_ último** lugar.</span><span class="sxs-lookup"><span data-stu-id="60277-134">Defines the boundary of error reports; any general EAP error will occur between **\_EAP\_GENERAL\_FIRST** and **\_EAP\_GENERAL\_LAST**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="60277-135"><span id="_EAP_GENERAL_LAST"></span><span id="_eap_general_last"></span>**\_\_último EAP general \_**</span><span class="sxs-lookup"><span data-stu-id="60277-135"><span id="_EAP_GENERAL_LAST"></span><span id="_eap_general_last"></span>**\_EAP\_GENERAL\_LAST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60277-136">0x3F</span><span class="sxs-lookup"><span data-stu-id="60277-136">0x3F</span></span>
</dt> <dt>



<span data-ttu-id="60277-137">Define el límite de los informes de errores; cualquier error de EAP general se producirá entre **\_ EAP \_ General \_ primero** y **\_ EAP \_ General en \_ último** lugar.</span><span class="sxs-lookup"><span data-stu-id="60277-137">Defines the boundary of error reports; any general EAP error will occur between **\_EAP\_GENERAL\_FIRST** and **\_EAP\_GENERAL\_LAST**.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="60277-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="60277-138">Requirements</span></span>



| <span data-ttu-id="60277-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="60277-139">Requirement</span></span> | <span data-ttu-id="60277-140">Value</span><span class="sxs-lookup"><span data-stu-id="60277-140">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="60277-141">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="60277-141">Minimum supported client</span></span><br/> | <span data-ttu-id="60277-142">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="60277-142">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="60277-143">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="60277-143">Minimum supported server</span></span><br/> | <span data-ttu-id="60277-144">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="60277-144">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="60277-145">Encabezado</span><span class="sxs-lookup"><span data-stu-id="60277-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="60277-146"><dt>Eaphosterror. h</dt></span><span class="sxs-lookup"><span data-stu-id="60277-146"><dt>Eaphosterror.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60277-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="60277-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60277-148">Constantes de EAPHost comunes</span><span class="sxs-lookup"><span data-stu-id="60277-148">Common EAPHost Constants</span></span>](common-eap-host-error-constants.md)
</dt> </dl>

 

 





