---
title: Constantes de WINBIO_BIR_PURPOSE (Winbio \_ Types. h)
description: Especifique el propósito para el que está previsto el registro de información biométrica (BIR) o para el que es adecuado.
ms.assetid: AAFD3203-4D3D-43B5-A833-1258E1E281D3
topic_type:
- apiref
api_name:
- WINBIO_NO_PURPOSE_AVAILABLE
- WINBIO_PURPOSE_VERIFY
- WINBIO_PURPOSE_IDENTIFY
- WINBIO_PURPOSE_ENROLL
- WINBIO_PURPOSE_ENROLL_FOR_VERIFICATION
- WINBIO_PURPOSE_ENROLL_FOR_IDENTIFICATION
- WINBIO_PURPOSE_AUDIT
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5a662a5ae045d3afc631f93cdf296508dabccf9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996448"
---
# <a name="winbio_bir_purpose-constants"></a><span data-ttu-id="c8ea4-103">\_Constantes WINBIO Bir \_ purpose</span><span class="sxs-lookup"><span data-stu-id="c8ea4-103">WINBIO\_BIR\_PURPOSE Constants</span></span>

<span data-ttu-id="c8ea4-104">El miembro **purpose** de la estructura de [**\_ \_ encabezado WINBIO Bir**](winbio-bir-header.md) usa las marcas siguientes para especificar el propósito para el que está previsto el registro de información biométrico (BIR) o para el que es adecuado.</span><span class="sxs-lookup"><span data-stu-id="c8ea4-104">The following flags are used by the **Purpose** member of the [**WINBIO\_BIR\_HEADER**](winbio-bir-header.md) structure to specify the purpose for which the biometric information record (BIR) is intended or for which it is suitable.</span></span>



| <span data-ttu-id="c8ea4-105">Constante</span><span class="sxs-lookup"><span data-stu-id="c8ea4-105">Constant</span></span>                                                                                                                                                                                                                                          | <span data-ttu-id="c8ea4-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="c8ea4-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                 |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_NO_PURPOSE_AVAILABLE"></span><span id="winbio_no_purpose_available"></span><dl> <span data-ttu-id="c8ea4-107"><dt>**WINBIO \_ no hay ningún \_ propósito \_ disponible**</dt></span><span class="sxs-lookup"><span data-stu-id="c8ea4-107"><dt>**WINBIO\_NO\_PURPOSE\_AVAILABLE**</dt></span></span> </dl>                                         | <span data-ttu-id="c8ea4-108">No se especifica ningún propósito.</span><span class="sxs-lookup"><span data-stu-id="c8ea4-108">No purpose is specified.</span></span><br/>                                                                                                                                                                                                                                                                                                         |
| <span id="WINBIO_PURPOSE_VERIFY"></span><span id="winbio_purpose_verify"></span><dl> <span data-ttu-id="c8ea4-109"><dt>**\_comprobación de propósito de WINBIO \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c8ea4-109"><dt>**WINBIO\_PURPOSE\_VERIFY**</dt></span></span> </dl>                                                            | <span data-ttu-id="c8ea4-110">Comprobar la identidad de un usuario.</span><span class="sxs-lookup"><span data-stu-id="c8ea4-110">Verify the identity of a user.</span></span><br/>                                                                                                                                                                                                                                                                                                   |
| <span id="WINBIO_PURPOSE_IDENTIFY"></span><span id="winbio_purpose_identify"></span><dl> <span data-ttu-id="c8ea4-111"><dt>**\_identificación de propósito de WINBIO \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c8ea4-111"><dt>**WINBIO\_PURPOSE\_IDENTIFY**</dt></span></span> </dl>                                                      | <span data-ttu-id="c8ea4-112">Identifique a un usuario.</span><span class="sxs-lookup"><span data-stu-id="c8ea4-112">Identify a user.</span></span><br/>                                                                                                                                                                                                                                                                                                                 |
| <span id="WINBIO_PURPOSE_ENROLL"></span><span id="winbio_purpose_enroll"></span><dl> <span data-ttu-id="c8ea4-113"><dt>**\_inscripción de propósito de WINBIO \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c8ea4-113"><dt>**WINBIO\_PURPOSE\_ENROLL**</dt></span></span> </dl>                                                            | <span data-ttu-id="c8ea4-114">Inscribir a un usuario.</span><span class="sxs-lookup"><span data-stu-id="c8ea4-114">Enroll a user.</span></span><br/>                                                                                                                                                                                                                                                                                                                   |
| <span id="WINBIO_PURPOSE_ENROLL_FOR_VERIFICATION"></span><span id="winbio_purpose_enroll_for_verification"></span><dl> <span data-ttu-id="c8ea4-115"><dt>**WINBIO \_ propósito \_ inscribirse \_ para la \_ comprobación**</dt></span><span class="sxs-lookup"><span data-stu-id="c8ea4-115"><dt>**WINBIO\_PURPOSE\_ENROLL\_FOR\_VERIFICATION**</dt></span></span> </dl>       | <span data-ttu-id="c8ea4-116">Capture un ejemplo biométrico y determine si el ejemplo corresponde a la identidad de usuario especificada.</span><span class="sxs-lookup"><span data-stu-id="c8ea4-116">Capture a biometric sample and determine whether the sample corresponds to the specified user identity.</span></span><br/>                                                                                                                                                                                                                          |
| <span id="WINBIO_PURPOSE_ENROLL_FOR_IDENTIFICATION"></span><span id="winbio_purpose_enroll_for_identification"></span><dl> <span data-ttu-id="c8ea4-117"><dt>**WINBIO \_ propósito \_ inscribirse \_ para \_ identificación**</dt></span><span class="sxs-lookup"><span data-stu-id="c8ea4-117"><dt>**WINBIO\_PURPOSE\_ENROLL\_FOR\_IDENTIFICATION**</dt></span></span> </dl> | <span data-ttu-id="c8ea4-118">Capture un ejemplo biométrico y determine si coincide con una plantilla biométrica existente.</span><span class="sxs-lookup"><span data-stu-id="c8ea4-118">Capture a biometric sample and determine whether it matches an existing biometric template.</span></span><br/>                                                                                                                                                                                                                                      |
| <span id="WINBIO_PURPOSE_AUDIT"></span><span id="winbio_purpose_audit"></span><dl> <span data-ttu-id="c8ea4-119"><dt>**\_Auditoría de propósito de WINBIO \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c8ea4-119"><dt>**WINBIO\_PURPOSE\_AUDIT**</dt></span></span> </dl>                                                               | <span data-ttu-id="c8ea4-120">Información adicional que se puede usar para el registro o para la visualización.</span><span class="sxs-lookup"><span data-stu-id="c8ea4-120">Extra information that can be used for logging or for display.</span></span> <span data-ttu-id="c8ea4-121">Todas las funciones omiten este valor en la entrada.</span><span class="sxs-lookup"><span data-stu-id="c8ea4-121">This value is ignored on input by all functions.</span></span> <span data-ttu-id="c8ea4-122">En la salida, solo estará disponible si es compatible con la unidad biométrica y especifica **WINBIO \_ Data \_ Flag \_ raw** en el parámetro *Flags* de la función [**WinBioCaptureSample**](/windows/desktop/api/Winbio/nf-winbio-winbiocapturesample) .</span><span class="sxs-lookup"><span data-stu-id="c8ea4-122">On output, it will only be available if supported by the biometric unit and you specify **WINBIO\_DATA\_FLAG\_RAW** in the *Flags* parameter of the [**WinBioCaptureSample**](/windows/desktop/api/Winbio/nf-winbio-winbiocapturesample) function.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="c8ea4-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c8ea4-123">Requirements</span></span>



| <span data-ttu-id="c8ea4-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="c8ea4-124">Requirement</span></span> | <span data-ttu-id="c8ea4-125">Value</span><span class="sxs-lookup"><span data-stu-id="c8ea4-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8ea4-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c8ea4-126">Minimum supported client</span></span><br/> | <span data-ttu-id="c8ea4-127">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="c8ea4-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="c8ea4-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c8ea4-128">Minimum supported server</span></span><br/> | <span data-ttu-id="c8ea4-129">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="c8ea4-129">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="c8ea4-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c8ea4-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="c8ea4-131"><dt>Winbio \_ Types. h (incluye Winbio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c8ea4-131"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c8ea4-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="c8ea4-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8ea4-133">Constantes de aplicación cliente</span><span class="sxs-lookup"><span data-stu-id="c8ea4-133">Client Application Constants</span></span>](client-application-constants.md)
</dt> <dt>

[<span data-ttu-id="c8ea4-134">**WINBIO \_ \_ encabezado Bir**</span><span class="sxs-lookup"><span data-stu-id="c8ea4-134">**WINBIO\_BIR\_HEADER**</span></span>](winbio-bir-header.md)
</dt> </dl>

 

 





