---
description: Especifique los niveles de protección para el sistema de administración de generación de copias&\# 8212; Analógico (CGMS-A).
ms.assetid: 739e2f9e-b8f1-4ee1-8706-9a069773a3de
title: Marcas de protección de CGMS-A (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3329ae13741490f2783d548baeead65ba59bc5ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423575"
---
# <a name="cgms-a-protection-flags"></a><span data-ttu-id="bd761-103">Marcas de protección de CGMS-A</span><span class="sxs-lookup"><span data-stu-id="bd761-103">CGMS-A Protection Flags</span></span>

<span data-ttu-id="bd761-104">En las constantes de la tabla siguiente se especifican los niveles de protección para el sistema de administración de la generación de copias analógica (CGMS-A).</span><span class="sxs-lookup"><span data-stu-id="bd761-104">The constants in the following table specify the protection levels for Copy Generation Management System Analog (CGMS-A).</span></span>



| <span data-ttu-id="bd761-105">Constante o valor</span><span class="sxs-lookup"><span data-stu-id="bd761-105">Constant/value</span></span>                                                                                                                                                                                                                                                                                                 | <span data-ttu-id="bd761-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="bd761-106">Description</span></span>                                                                                                                       |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------|
| <span id="OPM_CGMSA_OFF"></span><span id="opm_cgmsa_off"></span><dl> <span data-ttu-id="bd761-107"><dt>**OPM \_ CGMSA \_**</dt> de <dt>0x00</dt></span><span class="sxs-lookup"><span data-stu-id="bd761-107"><dt>**OPM\_CGMSA\_OFF**</dt> <dt>0x00</dt></span></span> </dl>                                                                                       | <span data-ttu-id="bd761-108">CGMS-A está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="bd761-108">CGMS-A is disabled.</span></span> <br/>                                                                                                   |
| <span id="OPM_CGMSA_COPY_FREELY"></span><span id="opm_cgmsa_copy_freely"></span><dl> <span data-ttu-id="bd761-109"><dt>**OPM \_ Copia de CGMSA con la \_ \_ libertad**</dt> <dt>0x01</dt></span><span class="sxs-lookup"><span data-stu-id="bd761-109"><dt>**OPM\_CGMSA\_COPY\_FREELY**</dt> <dt>0x01</dt></span></span> </dl>                                                              | <span data-ttu-id="bd761-110">El nivel de protección se copia libremente.</span><span class="sxs-lookup"><span data-stu-id="bd761-110">The protection level is Copy Freely.</span></span><br/>                                                                                   |
| <span id="OPM_CGMSA_COPY_NO_MORE"></span><span id="opm_cgmsa_copy_no_more"></span><dl> <span data-ttu-id="bd761-111"><dt>**OPM \_ CGMSA \_ copiar \_ no \_ más**</dt> <dt>0x02</dt></span><span class="sxs-lookup"><span data-stu-id="bd761-111"><dt>**OPM\_CGMSA\_COPY\_NO\_MORE**</dt> <dt>0x02</dt></span></span> </dl>                                                          | <span data-ttu-id="bd761-112">El nivel de protección es la copia no más.</span><span class="sxs-lookup"><span data-stu-id="bd761-112">The protection level is Copy No More.</span></span> <br/>                                                                                 |
| <span id="OPM_CGMSA_COPY_ONE_GENERATION"></span><span id="opm_cgmsa_copy_one_generation"></span><dl> <span data-ttu-id="bd761-113"><dt>**OPM \_ CGMSA \_ copiar \_ una \_ generación**</dt> <dt>0x03</dt></span><span class="sxs-lookup"><span data-stu-id="bd761-113"><dt>**OPM\_CGMSA\_COPY\_ONE\_GENERATION**</dt> <dt>0x03</dt></span></span> </dl>                                     | <span data-ttu-id="bd761-114">El nivel de protección es copiar una generación.</span><span class="sxs-lookup"><span data-stu-id="bd761-114">The protection level is Copy One Generation.</span></span> <br/>                                                                          |
| <span id="OPM_CGMSA_COPY_NEVER"></span><span id="opm_cgmsa_copy_never"></span><dl> <span data-ttu-id="bd761-115"><dt>**OPM \_ CGMSA \_ Copy \_ nunca**</dt> <dt>0x04</dt></span><span class="sxs-lookup"><span data-stu-id="bd761-115"><dt>**OPM\_CGMSA\_COPY\_NEVER**</dt> <dt>0x04</dt></span></span> </dl>                                                                 | <span data-ttu-id="bd761-116">El nivel de protección es copiar nunca.</span><span class="sxs-lookup"><span data-stu-id="bd761-116">The protection level is Copy Never.</span></span><br/>                                                                                    |
| <span id="OPM_CGMSA_REDISTRIBUTION_CONTROL_REQUIRED"></span><span id="opm_cgmsa_redistribution_control_required"></span><dl> <span data-ttu-id="bd761-117"><dt>**OPM \_ Se \_ requiere el \_ control \_ de redistribución de CGMSA**</dt> <dt>0x08</dt></span><span class="sxs-lookup"><span data-stu-id="bd761-117"><dt>**OPM\_CGMSA\_REDISTRIBUTION\_CONTROL\_REQUIRED**</dt> <dt>0x08</dt></span></span> </dl> | <span data-ttu-id="bd761-118">Es necesario el control de redistribución (también denominado *marca de difusión*).</span><span class="sxs-lookup"><span data-stu-id="bd761-118">Redistribution control (also called the *broadcast flag*) is required.</span></span> <span data-ttu-id="bd761-119">Esta marca se puede combinar con las demás marcas.</span><span class="sxs-lookup"><span data-stu-id="bd761-119">This flag can be combined with the other flags.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="bd761-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bd761-120">Remarks</span></span>

<span data-ttu-id="bd761-121">Estas marcas son equivalentes a las constantes de enumeración de **\_ nivel de \_ protección \_ de COPP CGMSA** usadas en el protocolo de protección de la salida certificada (COPP).</span><span class="sxs-lookup"><span data-stu-id="bd761-121">These flags are equivalent to the **COPP\_CGMSA\_Protection\_Level** enumeration constants used in the Certified Output Protection Protocol (COPP).</span></span>

## <a name="requirements"></a><span data-ttu-id="bd761-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bd761-122">Requirements</span></span>



| <span data-ttu-id="bd761-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="bd761-123">Requirement</span></span> | <span data-ttu-id="bd761-124">Value</span><span class="sxs-lookup"><span data-stu-id="bd761-124">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="bd761-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bd761-125">Minimum supported client</span></span><br/> | <span data-ttu-id="bd761-126">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="bd761-126">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="bd761-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bd761-127">Minimum supported server</span></span><br/> | <span data-ttu-id="bd761-128">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="bd761-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="bd761-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bd761-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="bd761-130"><dt>Opmapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="bd761-130"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bd761-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="bd761-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd761-132">Constantes de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="bd761-132">Media Foundation Constants</span></span>](media-foundation-constants.md)
</dt> </dl>

 

 




