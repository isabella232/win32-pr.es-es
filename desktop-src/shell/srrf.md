---
description: Marcas que restringen los datos que se van a establecer o devolver.
title: SRRF (shlwapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: c9dbffd1-3b3e-4a25-89ee-1666e2812a62
api_name:
- SRRF_RT_REG_NONE
- SRRF_RT_REG_SZ
- SRRF_RT_REG_EXPAND_SZ
- SRRF_RT_REG_BINARY
- SRRF_RT_REG_DWORD
- SRRF_RT_REG_MULTI_SZ
- SRRF_RT_REG_QWORD
- SRRF_RT_DWORD
- SRRF_RT_QWORD
- SRRF_RT_ANY
- SRRF_RM_ANY
- SRRF_RM_NORMAL
- SRRF_RM_SAFE
- SRRF_RM_SAFENETWORK
- SRRF_NOEXPAND
- SRRF_ZEROONFAILURE
- SRRF_NOVIRT
api_type:
- HeaderDef
api_location:
- Shlwapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 3ba36b64496413a54e6d8b8b96c16c265367d05c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104082806"
---
# <a name="srrf"></a><span data-ttu-id="d862b-103">SRRF</span><span class="sxs-lookup"><span data-stu-id="d862b-103">SRRF</span></span>

<span data-ttu-id="d862b-104">Marcas que restringen los datos que se van a establecer o devolver.</span><span class="sxs-lookup"><span data-stu-id="d862b-104">Flags that restrict the data to be set or returned.</span></span>



| <span data-ttu-id="d862b-105">Constante o valor</span><span class="sxs-lookup"><span data-stu-id="d862b-105">Constant/value</span></span>                                                                                                                                                                                                                                           | <span data-ttu-id="d862b-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="d862b-106">Description</span></span>                                                                                                                                                                                                            |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SRRF_RT_REG_NONE"></span><span id="srrf_rt_reg_none"></span><dl> <span data-ttu-id="d862b-107"><dt>**SRRF \_ RT \_ reg \_ ninguno**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="d862b-107"><dt>**SRRF\_RT\_REG\_NONE**</dt> <dt>0x00000001</dt></span></span> </dl>                 | <span data-ttu-id="d862b-108">Escriba REG \_ None.</span><span class="sxs-lookup"><span data-stu-id="d862b-108">Type REG\_NONE.</span></span><br/>                                                                                                                                                                                             |
| <span id="SRRF_RT_REG_SZ"></span><span id="srrf_rt_reg_sz"></span><dl> <span data-ttu-id="d862b-109"><dt>**SRRF \_ RT \_ reg \_ SZ**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="d862b-109"><dt>**SRRF\_RT\_REG\_SZ**</dt> <dt>0x00000002</dt></span></span> </dl>                       | <span data-ttu-id="d862b-110">Escriba REG \_ SZ.</span><span class="sxs-lookup"><span data-stu-id="d862b-110">Type REG\_SZ.</span></span> <span data-ttu-id="d862b-111">REG \_ Expand \_ Types se convierten automáticamente en REG \_ SZ a menos que \_ se especifique la marca SRRF NOEXPAND.</span><span class="sxs-lookup"><span data-stu-id="d862b-111">REG\_EXPAND\_SZ types are automatically converted to REG\_SZ unless the SRRF\_NOEXPAND flag is specified.</span></span><br/>                                                                                     |
| <span id="SRRF_RT_REG_EXPAND_SZ"></span><span id="srrf_rt_reg_expand_sz"></span><dl> <span data-ttu-id="d862b-112"><dt>**SRRF \_ RT \_ reg \_ expanda \_ SZ**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="d862b-112"><dt>**SRRF\_RT\_REG\_EXPAND\_SZ**</dt> <dt>0x00000004</dt></span></span> </dl> | <span data-ttu-id="d862b-113">Escriba REG \_ Expander \_ .</span><span class="sxs-lookup"><span data-stu-id="d862b-113">Type REG\_EXPAND\_SZ.</span></span> <span data-ttu-id="d862b-114">Si recupera un valor, también debe obtener la \_ marca SRRF NOEXPAND, o bien se produce un error en [**SHRegGetValue**](/windows/desktop/api/Shlwapi/nf-shlwapi-shreggetvaluea) con un \_ parámetro no válido \_ .</span><span class="sxs-lookup"><span data-stu-id="d862b-114">If retrieving a value, you must also get the SRRF\_NOEXPAND flag, or [**SHRegGetValue**](/windows/desktop/api/Shlwapi/nf-shlwapi-shreggetvaluea) fails with ERROR\_INVALID\_PARAMETER.</span></span><br/>                                     |
| <span id="SRRF_RT_REG_BINARY"></span><span id="srrf_rt_reg_binary"></span><dl> <span data-ttu-id="d862b-115"><dt>**SRRF \_ RT \_ reg \_ binario**</dt> <dt>0x00000008</dt></span><span class="sxs-lookup"><span data-stu-id="d862b-115"><dt>**SRRF\_RT\_REG\_BINARY**</dt> <dt>0x00000008</dt></span></span> </dl>           | <span data-ttu-id="d862b-116">Escriba REG \_ Binary.</span><span class="sxs-lookup"><span data-stu-id="d862b-116">Type REG\_BINARY.</span></span><br/>                                                                                                                                                                                           |
| <span id="SRRF_RT_REG_DWORD"></span><span id="srrf_rt_reg_dword"></span><dl> <span data-ttu-id="d862b-117"><dt>**SRRF \_ RT \_ reg \_ DWORD**</dt> <dt>0x00000010</dt></span><span class="sxs-lookup"><span data-stu-id="d862b-117"><dt>**SRRF\_RT\_REG\_DWORD**</dt> <dt>0x00000010</dt></span></span> </dl>              | <span data-ttu-id="d862b-118">Escriba REG \_ DWORD.</span><span class="sxs-lookup"><span data-stu-id="d862b-118">Type REG\_DWORD.</span></span><br/>                                                                                                                                                                                            |
| <span id="SRRF_RT_REG_MULTI_SZ"></span><span id="srrf_rt_reg_multi_sz"></span><dl> <span data-ttu-id="d862b-119"><dt>**SRRF \_ RT \_ reg \_ multi \_ SZ**</dt> <dt>0x00000020</dt></span><span class="sxs-lookup"><span data-stu-id="d862b-119"><dt>**SRRF\_RT\_REG\_MULTI\_SZ**</dt> <dt>0x00000020</dt></span></span> </dl>    | <span data-ttu-id="d862b-120">Escriba REG \_ multi \_ SZ.</span><span class="sxs-lookup"><span data-stu-id="d862b-120">Type REG\_MULTI\_SZ.</span></span><br/>                                                                                                                                                                                        |
| <span id="SRRF_RT_REG_QWORD"></span><span id="srrf_rt_reg_qword"></span><dl> <span data-ttu-id="d862b-121"><dt>**SRRF \_ RT \_ reg \_ QWord**</dt> <dt>0x00000040</dt></span><span class="sxs-lookup"><span data-stu-id="d862b-121"><dt>**SRRF\_RT\_REG\_QWORD**</dt> <dt>0x00000040</dt></span></span> </dl>              | <span data-ttu-id="d862b-122">Escriba REG \_ QWord.</span><span class="sxs-lookup"><span data-stu-id="d862b-122">Type REG\_QWORD.</span></span><br/>                                                                                                                                                                                            |
| <span id="SRRF_RT_DWORD"></span><span id="srrf_rt_dword"></span><dl> <span data-ttu-id="d862b-123"><dt>**SRRF \_ RT \_ DWORD**</dt> <dt>0x00000018</dt></span><span class="sxs-lookup"><span data-stu-id="d862b-123"><dt>**SRRF\_RT\_DWORD**</dt> <dt>0x00000018</dt></span></span> </dl>                           | <span data-ttu-id="d862b-124">REG \_ DWORD y 32 bits reg \_ Binary Types.</span><span class="sxs-lookup"><span data-stu-id="d862b-124">REG\_DWORD and 32-bit REG\_BINARY types.</span></span> <span data-ttu-id="d862b-125">Es equivalente a SRRF \_ RT \_ reg \_ Binary \| SRRF \_ RT \_ reg \_ DWORD.</span><span class="sxs-lookup"><span data-stu-id="d862b-125">This is equivalent to SRRF\_RT\_REG\_BINARY \| SRRF\_RT\_REG\_DWORD.</span></span> <span data-ttu-id="d862b-126">Si recupera un valor, si los datos binarios del valor son mayores de 32 bits, no se devuelve.</span><span class="sxs-lookup"><span data-stu-id="d862b-126">If retrieving a value, if the value's binary data is larger than 32 bits, it is not returned.</span></span><br/> |
| <span id="SRRF_RT_QWORD"></span><span id="srrf_rt_qword"></span><dl> <span data-ttu-id="d862b-127"><dt>**SRRF \_ 0x00000048 \_ QWord**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="d862b-127"><dt>**SRRF\_RT\_QWORD**</dt> <dt>0x00000048</dt></span></span> </dl>                           | <span data-ttu-id="d862b-128">\_Tipos binarios de reg QWord y 64 bits \_ .</span><span class="sxs-lookup"><span data-stu-id="d862b-128">REG\_QWORD and 64-bit REG\_BINARY types.</span></span> <span data-ttu-id="d862b-129">Esto es equivalente a SRRF \_ RT \_ reg \_ Binary \| SRRF \_ RT \_ reg \_ QWord.</span><span class="sxs-lookup"><span data-stu-id="d862b-129">This is equivalent to SRRF\_RT\_REG\_BINARY \| SRRF\_RT\_REG\_QWORD.</span></span> <span data-ttu-id="d862b-130">Si recupera un valor, si los datos binarios del valor son mayores de 64 bits, no se devuelve.</span><span class="sxs-lookup"><span data-stu-id="d862b-130">If retrieving a value, if the value's binary data is larger than 64 bits, it is not returned.</span></span><br/> |
| <span id="SRRF_RT_ANY"></span><span id="srrf_rt_any"></span><dl> <span data-ttu-id="d862b-131"><dt>**SRRF \_ RT \_ any**</dt> <dt>0x0000FFFF</dt></span><span class="sxs-lookup"><span data-stu-id="d862b-131"><dt>**SRRF\_RT\_ANY**</dt> <dt>0x0000FFFF</dt></span></span> </dl>                                 | <span data-ttu-id="d862b-132">Todos los tipos.</span><span class="sxs-lookup"><span data-stu-id="d862b-132">All types.</span></span> <span data-ttu-id="d862b-133">Establezca esta marca si no \_ se establece ningún otro valor RT de SRRF.</span><span class="sxs-lookup"><span data-stu-id="d862b-133">Set this flag if no other SRRF\_RT value is set.</span></span><br/>                                                                                                                                                 |
| <span id="SRRF_RM_ANY"></span><span id="srrf_rm_any"></span><dl> <span data-ttu-id="d862b-134"><dt>**SRRF \_ RM \_ cualquier**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="d862b-134"><dt>**SRRF\_RM\_ANY**</dt> <dt>0x00000000</dt></span></span> </dl>                                 | <span data-ttu-id="d862b-135">No hay ninguna restricción de modo.</span><span class="sxs-lookup"><span data-stu-id="d862b-135">No mode restriction.</span></span> <span data-ttu-id="d862b-136">Este es el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="d862b-136">This is the default value.</span></span><br/>                                                                                                                                                             |
| <span id="SRRF_RM_NORMAL"></span><span id="srrf_rm_normal"></span><dl> <span data-ttu-id="d862b-137"><dt>**SRRF \_ 0x00010000 de RM \_ normal**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="d862b-137"><dt>**SRRF\_RM\_NORMAL**</dt> <dt>0x00010000</dt></span></span> </dl>                        | <span data-ttu-id="d862b-138">Restrinja el modo de inicio del sistema a "arranque normal".</span><span class="sxs-lookup"><span data-stu-id="d862b-138">Restrict system startup mode to "normal boot".</span></span><br/>                                                                                                                                                              |
| <span id="SRRF_RM_SAFE"></span><span id="srrf_rm_safe"></span><dl> <span data-ttu-id="d862b-139"><dt>**SRRF \_ 0x00020000 \_ Safe de RM**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="d862b-139"><dt>**SRRF\_RM\_SAFE**</dt> <dt>0x00020000</dt></span></span> </dl>                              | <span data-ttu-id="d862b-140">Restrinja el modo de inicio del sistema a "modo seguro".</span><span class="sxs-lookup"><span data-stu-id="d862b-140">Restrict system startup mode to "safe mode".</span></span><br/>                                                                                                                                                                |
| <span id="SRRF_RM_SAFENETWORK"></span><span id="srrf_rm_safenetwork"></span><dl> <span data-ttu-id="d862b-141"><dt>**SRRF \_ RM \_ SAFENETWORK**</dt> <dt>0x00040000</dt></span><span class="sxs-lookup"><span data-stu-id="d862b-141"><dt>**SRRF\_RM\_SAFENETWORK**</dt> <dt>0x00040000</dt></span></span> </dl>         | <span data-ttu-id="d862b-142">Restrinja el modo de inicio del sistema a "modo seguro con funciones de red".</span><span class="sxs-lookup"><span data-stu-id="d862b-142">Restrict system startup mode to "safe mode with networking".</span></span><br/>                                                                                                                                                |
| <span id="SRRF_NOEXPAND"></span><span id="srrf_noexpand"></span><dl> <span data-ttu-id="d862b-143"><dt>**SRRF \_ NOEXPAND**</dt> <dt>0x10000000</dt></span><span class="sxs-lookup"><span data-stu-id="d862b-143"><dt>**SRRF\_NOEXPAND**</dt> <dt>0x10000000</dt></span></span> </dl>                            | <span data-ttu-id="d862b-144">No expanda automáticamente REG \_ Expand las \_ cadenas de entorno de.</span><span class="sxs-lookup"><span data-stu-id="d862b-144">Do not automatically expand REG\_EXPAND\_SZ environment strings.</span></span><br/>                                                                                                                                            |
| <span id="SRRF_ZEROONFAILURE"></span><span id="srrf_zeroonfailure"></span><dl> <span data-ttu-id="d862b-145"><dt>**SRRF \_ ZEROONFAILURE**</dt> <dt>0x20000000</dt></span><span class="sxs-lookup"><span data-stu-id="d862b-145"><dt>**SRRF\_ZEROONFAILURE**</dt> <dt>0x20000000</dt></span></span> </dl>             | <span data-ttu-id="d862b-146">Si recupera un valor, si *pvData* no es **null**, establezca el contenido del búfer *pvData* en ceros en caso de error.</span><span class="sxs-lookup"><span data-stu-id="d862b-146">If retrieving a value, if *pvData* is not **NULL**, set the contents of the *pvData* buffer to all zeros on failure.</span></span><br/>                                                                                        |
| <span id="SRRF_NOVIRT"></span><span id="srrf_novirt"></span><dl> <span data-ttu-id="d862b-147"><dt>**SRRF \_ NOVIRT**</dt> <dt>0x40000000</dt></span><span class="sxs-lookup"><span data-stu-id="d862b-147"><dt>**SRRF\_NOVIRT**</dt> <dt>0x40000000</dt></span></span> </dl>                                  | <span data-ttu-id="d862b-148">Al recuperar un valor, si la clave solicitada está virtualizada, se producirá un ERROR con el \_ archivo \_ no \_ encontrado.</span><span class="sxs-lookup"><span data-stu-id="d862b-148">When retrieving a value, if the requested key is virtualized, fail with ERROR\_FILE\_NOT\_FOUND.</span></span><br/>                                                                                                            |



## <a name="remarks"></a><span data-ttu-id="d862b-149">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d862b-149">Remarks</span></span>

<span data-ttu-id="d862b-150">Estos valores se definen en shlwapi. h.</span><span class="sxs-lookup"><span data-stu-id="d862b-150">These values are defined in Shlwapi.h.</span></span>

## <a name="requirements"></a><span data-ttu-id="d862b-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d862b-151">Requirements</span></span>



| <span data-ttu-id="d862b-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="d862b-152">Requirement</span></span> | <span data-ttu-id="d862b-153">Value</span><span class="sxs-lookup"><span data-stu-id="d862b-153">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d862b-154">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d862b-154">Minimum supported client</span></span><br/> | <span data-ttu-id="d862b-155">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="d862b-155">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="d862b-156">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d862b-156">Minimum supported server</span></span><br/> | <span data-ttu-id="d862b-157">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="d862b-157">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="d862b-158">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d862b-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="d862b-159"><dt>Shlwapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="d862b-159"><dt>Shlwapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d862b-160">Vea también</span><span class="sxs-lookup"><span data-stu-id="d862b-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d862b-161">**SHRegSetValue**</span><span class="sxs-lookup"><span data-stu-id="d862b-161">**SHRegSetValue**</span></span>](/windows/desktop/api/shlwapi/nf-shlwapi-shregsetvalue)
</dt> <dt>

[<span data-ttu-id="d862b-162">**SHRegGetValue**</span><span class="sxs-lookup"><span data-stu-id="d862b-162">**SHRegGetValue**</span></span>](/windows/desktop/api/Shlwapi/nf-shlwapi-shreggetvaluea)
</dt> </dl>

 

 




