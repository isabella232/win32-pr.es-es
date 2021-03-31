---
title: MPCALLBACK_DATA estructura (MpClient. h)
description: Datos pasados a la función de devolución de llamada.
ms.assetid: EA8E6C1E-F80B-4247-B073-C78D49A354CF
keywords:
- MPCALLBACK_DATA estructura de las características heredadas del entorno de Windows
- Puntero de estructura de PMPCALLBACK_DATA características de entorno heredado de Windows
topic_type:
- apiref
api_name:
- MPCALLBACK_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9741ca479eeb9770a3ae8c2aedbc51a8a2643033
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150237"
---
# <a name="mpcallback_data-structure"></a><span data-ttu-id="b8438-105">\_Estructura de datos MPCALLBACK</span><span class="sxs-lookup"><span data-stu-id="b8438-105">MPCALLBACK\_DATA structure</span></span>

<span data-ttu-id="b8438-106">Datos pasados a la función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="b8438-106">Data passed to the callback function.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8438-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b8438-107">Syntax</span></span>


```C++
typedef struct tagMPCALLBACK_DATA {
  MPNOTIFY        Notify;
  HRESULT         hResult;
  ULARGE_INTEGER  TimeStamp;
  MPCALLBACK_TYPE Type;
  union {
    PMPSTATUS_DATA         pStatusData;
    PMPSCAN_DATA           pScanData;
    PMPCLEAN_DATA          pCleanData;
    PMPCLEAN_PRECHECK_DATA pPrecheckData;
    PMPTHREAT_DATA         pThreatData;
    PMPSIGUPDATE_DATA      pSigUpdateData;
    PMPSAMPLE_DATA         pSampleData;
    PMPRESERVED_DATA       pReservedData;
    PMPCONFIGURATION_DATA  pConfigurationData;
    PMPFASTPATH_DATA       pFastPathData;
    PMPEXPIRATION_DATA     pExpirationData;
    PMPNIS_PRIVATE_DATA    pNISPrivateData;
    PMPHEALTH_DATA         pHealthData;
    PMPENDOFLIFE_DATA      pEndOfLifeData;
    PMPMALWARETOAST_DATA   pMalwareToastData;
  } Data;
} MPCALLBACK_DATA, *PMPCALLBACK_DATA;
```



## <a name="members"></a><span data-ttu-id="b8438-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="b8438-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="b8438-109">**Notificar**</span><span class="sxs-lookup"><span data-stu-id="b8438-109">**Notify**</span></span>
</dt> <dd>

<span data-ttu-id="b8438-110">Tipo: **[ **MPNOTIFY**](mpnotify.md)**</span><span class="sxs-lookup"><span data-stu-id="b8438-110">Type: **[**MPNOTIFY**](mpnotify.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b8438-111">Notificación de cambio a informe.</span><span class="sxs-lookup"><span data-stu-id="b8438-111">Change notification to report.</span></span>

</dd> <dt>

<span data-ttu-id="b8438-112">**Valor**</span><span class="sxs-lookup"><span data-stu-id="b8438-112">**hResult**</span></span>
</dt> <dd>

<span data-ttu-id="b8438-113">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="b8438-113">Type: **HRESULT**</span></span>

</dd> <dd>

<span data-ttu-id="b8438-114">Código de error, en caso de un error interno.</span><span class="sxs-lookup"><span data-stu-id="b8438-114">Error code, in case of an internal failure.</span></span>

</dd> <dt>

<span data-ttu-id="b8438-115">**Indicaciones**</span><span class="sxs-lookup"><span data-stu-id="b8438-115">**TimeStamp**</span></span>
</dt> <dd>

<span data-ttu-id="b8438-116">Tipo: **ULARGE \_ Integer**</span><span class="sxs-lookup"><span data-stu-id="b8438-116">Type: **ULARGE\_INTEGER**</span></span>

</dd> <dd>

<span data-ttu-id="b8438-117">Marca de tiempo actual.</span><span class="sxs-lookup"><span data-stu-id="b8438-117">Current timestamp.</span></span>

</dd> <dt>

<span data-ttu-id="b8438-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="b8438-118">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="b8438-119">Tipo: **[ **MPCALLBACK \_ Type**](mpcallback-type.md)**</span><span class="sxs-lookup"><span data-stu-id="b8438-119">Type: **[**MPCALLBACK\_TYPE**](mpcallback-type.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b8438-120">Tipo de datos Especial de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="b8438-120">Callback special data type.</span></span>

</dd> <dt>

<span data-ttu-id="b8438-121">**Data**</span><span class="sxs-lookup"><span data-stu-id="b8438-121">**Data**</span></span>
</dt> <dd>

<span data-ttu-id="b8438-122">Datos especiales de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="b8438-122">Callback special data.</span></span> <span data-ttu-id="b8438-123">El puntero a la estructura adecuada depende del valor de **tipo**.</span><span class="sxs-lookup"><span data-stu-id="b8438-123">The pointer to the appropriate structure depends on the value of **Type**.</span></span>

<dl> <dt>

<span data-ttu-id="b8438-124">**pStatusData**</span><span class="sxs-lookup"><span data-stu-id="b8438-124">**pStatusData**</span></span>
</dt> <dd>

<span data-ttu-id="b8438-125">Tipo: **PMPSTATUS \_ Data**</span><span class="sxs-lookup"><span data-stu-id="b8438-125">Type: **PMPSTATUS\_DATA**</span></span>

</dd> <dd>

<span data-ttu-id="b8438-126">Cuando **Escriba**  ==  **MPCALLBACK \_ status**.</span><span class="sxs-lookup"><span data-stu-id="b8438-126">When **Type** == **MPCALLBACK\_STATUS**.</span></span> <span data-ttu-id="b8438-127">Vea [**MPSTATUS \_ Data**](mpstatus-data.md).</span><span class="sxs-lookup"><span data-stu-id="b8438-127">See [**MPSTATUS\_DATA**](mpstatus-data.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8438-128">**pScanData**</span><span class="sxs-lookup"><span data-stu-id="b8438-128">**pScanData**</span></span>
</dt> <dd>

<span data-ttu-id="b8438-129">Tipo: **PMPSCAN \_ Data**</span><span class="sxs-lookup"><span data-stu-id="b8438-129">Type: **PMPSCAN\_DATA**</span></span>

</dd> <dd>

<span data-ttu-id="b8438-130">Cuando **Escriba**  ==  **MPCALLBACK \_ scan**.</span><span class="sxs-lookup"><span data-stu-id="b8438-130">When **Type** == **MPCALLBACK\_SCAN**.</span></span> <span data-ttu-id="b8438-131">Vea [**MPSCAN \_ Data**](mpscan-data.md).</span><span class="sxs-lookup"><span data-stu-id="b8438-131">See [**MPSCAN\_DATA**](mpscan-data.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8438-132">**pCleanData**</span><span class="sxs-lookup"><span data-stu-id="b8438-132">**pCleanData**</span></span>
</dt> <dd>

<span data-ttu-id="b8438-133">Tipo: **PMPCLEAN \_ Data**</span><span class="sxs-lookup"><span data-stu-id="b8438-133">Type: **PMPCLEAN\_DATA**</span></span>

</dd> <dd>

<span data-ttu-id="b8438-134">Cuando **Escriba**  ==  **MPCALLBACK \_ Clean**.</span><span class="sxs-lookup"><span data-stu-id="b8438-134">When **Type** == **MPCALLBACK\_CLEAN**.</span></span> <span data-ttu-id="b8438-135">Vea [**MPCLEAN \_ Data**](mpclean-data.md).</span><span class="sxs-lookup"><span data-stu-id="b8438-135">See [**MPCLEAN\_DATA**](mpclean-data.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8438-136">**pPrecheckData**</span><span class="sxs-lookup"><span data-stu-id="b8438-136">**pPrecheckData**</span></span>
</dt> <dd>

<span data-ttu-id="b8438-137">Tipo: **PMPCLEAN \_ comprobar \_ datos**</span><span class="sxs-lookup"><span data-stu-id="b8438-137">Type: **PMPCLEAN\_PRECHECK\_DATA**</span></span>

</dd> <dd>

<span data-ttu-id="b8438-138">Cuando **Escriba**  ==  **MPCALLBACK \_ precheck**.</span><span class="sxs-lookup"><span data-stu-id="b8438-138">When **Type** == **MPCALLBACK\_PRECHECK**.</span></span> <span data-ttu-id="b8438-139">Vea [**MPCLEAN \_ precheck \_ Data**](mpclean-precheck-data.md).</span><span class="sxs-lookup"><span data-stu-id="b8438-139">See [**MPCLEAN\_PRECHECK\_DATA**](mpclean-precheck-data.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8438-140">**pThreatData**</span><span class="sxs-lookup"><span data-stu-id="b8438-140">**pThreatData**</span></span>
</dt> <dd>

<span data-ttu-id="b8438-141">Tipo: **PMPTHREAT \_ Data**</span><span class="sxs-lookup"><span data-stu-id="b8438-141">Type: **PMPTHREAT\_DATA**</span></span>

</dd> <dd>

<span data-ttu-id="b8438-142">Cuando **Escriba**  ==  **MPCALLBACK \_ amenaza**.</span><span class="sxs-lookup"><span data-stu-id="b8438-142">When **Type** == **MPCALLBACK\_THREAT**.</span></span> <span data-ttu-id="b8438-143">Vea [**MPTHREAT \_ Data**](mpthreat-data.md).</span><span class="sxs-lookup"><span data-stu-id="b8438-143">See [**MPTHREAT\_DATA**](mpthreat-data.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8438-144">**pSigUpdateData**</span><span class="sxs-lookup"><span data-stu-id="b8438-144">**pSigUpdateData**</span></span>
</dt> <dd>

<span data-ttu-id="b8438-145">Tipo: **PMPSIGUPDATE \_ Data**</span><span class="sxs-lookup"><span data-stu-id="b8438-145">Type: **PMPSIGUPDATE\_DATA**</span></span>

</dd> <dd>

<span data-ttu-id="b8438-146">Cuando **Escriba**  ==  **MPCALLBACK \_ SIGUPDATE**.</span><span class="sxs-lookup"><span data-stu-id="b8438-146">When **Type** == **MPCALLBACK\_SIGUPDATE**.</span></span> <span data-ttu-id="b8438-147">Vea [**MPSIGUPDATE \_ Data**](mpsigupdate-data.md).</span><span class="sxs-lookup"><span data-stu-id="b8438-147">See [**MPSIGUPDATE\_DATA**](mpsigupdate-data.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8438-148">**pSampleData**</span><span class="sxs-lookup"><span data-stu-id="b8438-148">**pSampleData**</span></span>
</dt> <dd>

<span data-ttu-id="b8438-149">Tipo: **PMPSAMPLE \_ Data**</span><span class="sxs-lookup"><span data-stu-id="b8438-149">Type: **PMPSAMPLE\_DATA**</span></span>

</dd> <dd>

<span data-ttu-id="b8438-150">Cuando **Escriba**  ==  **\_ ejemplo de MPCALLBACK**.</span><span class="sxs-lookup"><span data-stu-id="b8438-150">When **Type** == **MPCALLBACK\_SAMPLE**.</span></span> <span data-ttu-id="b8438-151">Vea [**MPSAMPLE \_ Data**](mpsample-data.md).</span><span class="sxs-lookup"><span data-stu-id="b8438-151">See [**MPSAMPLE\_DATA**](mpsample-data.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8438-152">**pReservedData**</span><span class="sxs-lookup"><span data-stu-id="b8438-152">**pReservedData**</span></span>
</dt> <dd>

<span data-ttu-id="b8438-153">Tipo: **PMPRESERVED \_ Data**</span><span class="sxs-lookup"><span data-stu-id="b8438-153">Type: **PMPRESERVED\_DATA**</span></span>

</dd> <dd>

<span data-ttu-id="b8438-154">Cuando el **tipo**  ==  **MPCALLBACK está \_ reservado**.</span><span class="sxs-lookup"><span data-stu-id="b8438-154">When **Type** == **MPCALLBACK\_RESERVED**.</span></span> <span data-ttu-id="b8438-155">Vea [**MPRESERVED \_ Data**](mpreserved-data.md).</span><span class="sxs-lookup"><span data-stu-id="b8438-155">See [**MPRESERVED\_DATA**](mpreserved-data.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8438-156">**pConfigurationData**</span><span class="sxs-lookup"><span data-stu-id="b8438-156">**pConfigurationData**</span></span>
</dt> <dd>

<span data-ttu-id="b8438-157">Tipo: **PMPCONFIGURATION \_ Data**</span><span class="sxs-lookup"><span data-stu-id="b8438-157">Type: **PMPCONFIGURATION\_DATA**</span></span>

</dd> <dd>

<span data-ttu-id="b8438-158">Cuando **Escriba**  ==  **\_ \_ notificación de configuración de MPCALLBACK**.</span><span class="sxs-lookup"><span data-stu-id="b8438-158">When **Type** == **MPCALLBACK\_CONFIGURATION\_NOTIFICATION**.</span></span> <span data-ttu-id="b8438-159">Vea [**MPCONFIGURATION \_ Data**](mpconfiguration-data.md).</span><span class="sxs-lookup"><span data-stu-id="b8438-159">See [**MPCONFIGURATION\_DATA**](mpconfiguration-data.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8438-160">**pFastPathData**</span><span class="sxs-lookup"><span data-stu-id="b8438-160">**pFastPathData**</span></span>
</dt> <dd>

<span data-ttu-id="b8438-161">Tipo: **PMPFASTPATH \_ Data**</span><span class="sxs-lookup"><span data-stu-id="b8438-161">Type: **PMPFASTPATH\_DATA**</span></span>

</dd> <dd>

<span data-ttu-id="b8438-162">Cuando **Escriba**  ==  **MPCALLBACK \_ FASTPATH**.</span><span class="sxs-lookup"><span data-stu-id="b8438-162">When **Type** == **MPCALLBACK\_FASTPATH**.</span></span> <span data-ttu-id="b8438-163">Vea [**MPFASTPATH \_ Data**](mpfastpath-data.md).</span><span class="sxs-lookup"><span data-stu-id="b8438-163">See [**MPFASTPATH\_DATA**](mpfastpath-data.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8438-164">**pExpirationData**</span><span class="sxs-lookup"><span data-stu-id="b8438-164">**pExpirationData**</span></span>
</dt> <dd>

<span data-ttu-id="b8438-165">Tipo: **PMPEXPIRATION \_ Data**</span><span class="sxs-lookup"><span data-stu-id="b8438-165">Type: **PMPEXPIRATION\_DATA**</span></span>

</dd> <dd>

<span data-ttu-id="b8438-166">Cuando **Escriba**  ==  **\_ \_ expiración del producto MPCALLBACK**.</span><span class="sxs-lookup"><span data-stu-id="b8438-166">When **Type** == **MPCALLBACK\_PRODUCT\_EXPIRATION**.</span></span> <span data-ttu-id="b8438-167">Vea [**MPEXPIRATION \_ Data**](mpexpiration-data.md).</span><span class="sxs-lookup"><span data-stu-id="b8438-167">See [**MPEXPIRATION\_DATA**](mpexpiration-data.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8438-168">**pNISPrivateData**</span><span class="sxs-lookup"><span data-stu-id="b8438-168">**pNISPrivateData**</span></span>
</dt> <dd>

<span data-ttu-id="b8438-169">Tipo: **PMPNIS \_ \_ datos privados**</span><span class="sxs-lookup"><span data-stu-id="b8438-169">Type: **PMPNIS\_PRIVATE\_DATA**</span></span>

</dd> <dd>

<span data-ttu-id="b8438-170">Cuando **Escriba**  ==  **MPCALLBACK \_ NIS \_ Private**.</span><span class="sxs-lookup"><span data-stu-id="b8438-170">When **Type** == **MPCALLBACK\_NIS\_PRIVATE**.</span></span> <span data-ttu-id="b8438-171">Vea [**MPNIS \_ Private \_ Data**](mpnis-private-data.md).</span><span class="sxs-lookup"><span data-stu-id="b8438-171">See [**MPNIS\_PRIVATE\_DATA**](mpnis-private-data.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8438-172">**pHealthData**</span><span class="sxs-lookup"><span data-stu-id="b8438-172">**pHealthData**</span></span>
</dt> <dd>

<span data-ttu-id="b8438-173">Tipo: **PMPHEALTH \_ Data**</span><span class="sxs-lookup"><span data-stu-id="b8438-173">Type: **PMPHEALTH\_DATA**</span></span>

</dd> <dd>

<span data-ttu-id="b8438-174">Cuando **Escriba**  ==  **MPCALLBACK \_ Health**.</span><span class="sxs-lookup"><span data-stu-id="b8438-174">When **Type** == **MPCALLBACK\_HEALTH**.</span></span> <span data-ttu-id="b8438-175">Vea [**MPHEALTH \_ Data**](mphealth-data.md).</span><span class="sxs-lookup"><span data-stu-id="b8438-175">See [**MPHEALTH\_DATA**](mphealth-data.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8438-176">**pEndOfLifeData**</span><span class="sxs-lookup"><span data-stu-id="b8438-176">**pEndOfLifeData**</span></span>
</dt> <dd>

<span data-ttu-id="b8438-177">Tipo: **PMPENDOFLIFE \_ Data**</span><span class="sxs-lookup"><span data-stu-id="b8438-177">Type: **PMPENDOFLIFE\_DATA**</span></span>

</dd> <dd>

<span data-ttu-id="b8438-178">Cuando **Escriba**  ==  **MPCALLBACK \_ ENDOFLIFE**.</span><span class="sxs-lookup"><span data-stu-id="b8438-178">When **Type** == **MPCALLBACK\_ENDOFLIFE**.</span></span> <span data-ttu-id="b8438-179">Vea [**MPENDOFLIFE \_ Data**](mpendoflife-data.md).</span><span class="sxs-lookup"><span data-stu-id="b8438-179">See [**MPENDOFLIFE\_DATA**](mpendoflife-data.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8438-180">**pMalwareToastData**</span><span class="sxs-lookup"><span data-stu-id="b8438-180">**pMalwareToastData**</span></span>
</dt> <dd>

<span data-ttu-id="b8438-181">Tipo: **PMPMALWARETOAST \_ Data**</span><span class="sxs-lookup"><span data-stu-id="b8438-181">Type: **PMPMALWARETOAST\_DATA**</span></span>

</dd> <dd>

<span data-ttu-id="b8438-182">Cuando **Escriba**  ==  **MPCALLBACK \_ MALWARETOAST**.</span><span class="sxs-lookup"><span data-stu-id="b8438-182">When **Type** == **MPCALLBACK\_MALWARETOAST**.</span></span> <span data-ttu-id="b8438-183">Vea [**MPMALWARETOAST \_ Data**](mpmalwaretoast-data.md).</span><span class="sxs-lookup"><span data-stu-id="b8438-183">See [**MPMALWARETOAST\_DATA**](mpmalwaretoast-data.md).</span></span>

</dd> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b8438-184">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b8438-184">Requirements</span></span>



| <span data-ttu-id="b8438-185">Requisito</span><span class="sxs-lookup"><span data-stu-id="b8438-185">Requirement</span></span> | <span data-ttu-id="b8438-186">Value</span><span class="sxs-lookup"><span data-stu-id="b8438-186">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b8438-187">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b8438-187">Minimum supported client</span></span><br/> | <span data-ttu-id="b8438-188">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="b8438-188">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="b8438-189">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b8438-189">Minimum supported server</span></span><br/> | <span data-ttu-id="b8438-190">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="b8438-190">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b8438-191">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b8438-191">Header</span></span><br/>                   | <dl> <span data-ttu-id="b8438-192"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="b8438-192"><dt>MpClient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8438-193">Vea también</span><span class="sxs-lookup"><span data-stu-id="b8438-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8438-194">**\_tipo MPCALLBACK**</span><span class="sxs-lookup"><span data-stu-id="b8438-194">**MPCALLBACK\_TYPE**</span></span>](mpcallback-type.md)
</dt> <dt>

[<span data-ttu-id="b8438-195">**datos de MPCLEAN \_**</span><span class="sxs-lookup"><span data-stu-id="b8438-195">**MPCLEAN\_DATA**</span></span>](mpclean-data.md)
</dt> <dt>

[<span data-ttu-id="b8438-196">**MPCLEAN \_ comprobar \_ datos**</span><span class="sxs-lookup"><span data-stu-id="b8438-196">**MPCLEAN\_PRECHECK\_DATA**</span></span>](mpclean-precheck-data.md)
</dt> <dt>

[<span data-ttu-id="b8438-197">**datos de MPCONFIGURATION \_**</span><span class="sxs-lookup"><span data-stu-id="b8438-197">**MPCONFIGURATION\_DATA**</span></span>](mpconfiguration-data.md)
</dt> <dt>

[<span data-ttu-id="b8438-198">**datos de MPENDOFLIFE \_**</span><span class="sxs-lookup"><span data-stu-id="b8438-198">**MPENDOFLIFE\_DATA**</span></span>](mpendoflife-data.md)
</dt> <dt>

[<span data-ttu-id="b8438-199">**datos de MPEXPIRATION \_**</span><span class="sxs-lookup"><span data-stu-id="b8438-199">**MPEXPIRATION\_DATA**</span></span>](mpexpiration-data.md)
</dt> <dt>

[<span data-ttu-id="b8438-200">**datos de MPFASTPATH \_**</span><span class="sxs-lookup"><span data-stu-id="b8438-200">**MPFASTPATH\_DATA**</span></span>](mpfastpath-data.md)
</dt> <dt>

[<span data-ttu-id="b8438-201">**datos de MPHEALTH \_**</span><span class="sxs-lookup"><span data-stu-id="b8438-201">**MPHEALTH\_DATA**</span></span>](mphealth-data.md)
</dt> <dt>

[<span data-ttu-id="b8438-202">**datos de MPMALWARETOAST \_**</span><span class="sxs-lookup"><span data-stu-id="b8438-202">**MPMALWARETOAST\_DATA**</span></span>](mpmalwaretoast-data.md)
</dt> <dt>

[<span data-ttu-id="b8438-203">**MPNIS \_ \_ datos privados**</span><span class="sxs-lookup"><span data-stu-id="b8438-203">**MPNIS\_PRIVATE\_DATA**</span></span>](mpnis-private-data.md)
</dt> <dt>

[<span data-ttu-id="b8438-204">**MPNOTIFY**</span><span class="sxs-lookup"><span data-stu-id="b8438-204">**MPNOTIFY**</span></span>](mpnotify.md)
</dt> <dt>

[<span data-ttu-id="b8438-205">**datos de MPRESERVED \_**</span><span class="sxs-lookup"><span data-stu-id="b8438-205">**MPRESERVED\_DATA**</span></span>](mpreserved-data.md)
</dt> <dt>

[<span data-ttu-id="b8438-206">**datos de MPSAMPLE \_**</span><span class="sxs-lookup"><span data-stu-id="b8438-206">**MPSAMPLE\_DATA**</span></span>](mpsample-data.md)
</dt> <dt>

[<span data-ttu-id="b8438-207">**datos de MPSCAN \_**</span><span class="sxs-lookup"><span data-stu-id="b8438-207">**MPSCAN\_DATA**</span></span>](mpscan-data.md)
</dt> <dt>

[<span data-ttu-id="b8438-208">**datos de MPSIGUPDATE \_**</span><span class="sxs-lookup"><span data-stu-id="b8438-208">**MPSIGUPDATE\_DATA**</span></span>](mpsigupdate-data.md)
</dt> <dt>

[<span data-ttu-id="b8438-209">**datos de MPSTATUS \_**</span><span class="sxs-lookup"><span data-stu-id="b8438-209">**MPSTATUS\_DATA**</span></span>](mpstatus-data.md)
</dt> <dt>

[<span data-ttu-id="b8438-210">**datos de MPTHREAT \_**</span><span class="sxs-lookup"><span data-stu-id="b8438-210">**MPTHREAT\_DATA**</span></span>](mpthreat-data.md)
</dt> </dl>

 

 





