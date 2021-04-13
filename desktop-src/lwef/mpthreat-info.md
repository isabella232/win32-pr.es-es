---
title: MPTHREAT_INFO estructura (MpClient. h)
description: Contiene información sobre una amenaza.
ms.assetid: ED2A0BDB-0E7C-479D-ADA1-95B9A259F57E
keywords:
- MPTHREAT_INFO estructura de las características heredadas del entorno de Windows
- Puntero de estructura de PMPTHREAT_INFO características de entorno heredado de Windows
topic_type:
- apiref
api_name:
- MPTHREAT_INFO
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfa850a4293006a2f4b107a3f2579fdc14c1ea6e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492629"
---
# <a name="mpthreat_info-structure"></a><span data-ttu-id="0740f-105">Estructura de información de MPTHREAT \_</span><span class="sxs-lookup"><span data-stu-id="0740f-105">MPTHREAT\_INFO structure</span></span>

<span data-ttu-id="0740f-106">Contiene información sobre una amenaza.</span><span class="sxs-lookup"><span data-stu-id="0740f-106">Contains information about a threat.</span></span>

## <a name="syntax"></a><span data-ttu-id="0740f-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0740f-107">Syntax</span></span>


```C++
typedef struct tagMPTHREAT_INFO {
  MPTHREAT_ID           ThreatID;
  GUID                  DetectionID;
  MP_MIDL_STRING LPWSTR Name;
  MPTHREAT_TYPE         ThreatType;
  MPTHREAT_SEVERITY     ThreatCriticality;
  MPTHREAT_CATEGORY     ThreatCategory;
  DWORD                 ThreatShortDescriptionID;
  DWORD                 ThreatAdviseDescriptionID;
  MPTHREAT_STATUS       ThreatStatus;
  DWORD                 SuggestedActionCount;
  MPTHREAT_ACTION       SuggestedActionArray[MP_MAX_SUGGESTIONS];
  DWORD                 ResourceCount;
  PMPRESOURCE_INFO      *ResourceList[ResourceCount];
  ULARGE_INTEGER        ThreatStatusTime;
  HRESULT               ThreatStatusCode;
  MPTHREAT_DETECTION    ThreatDetection;
  GUID                  QuarantineGuid;
  MPEXECUTION_STATUS    ExecutionStatus;
  union {
    PMPTHREAT_INFOEX_UNUSED   pKnownBad;
    PMPTHREAT_INFOEX_BEHAVIOR pBehavior;
    PMPTHREAT_INFOEX_UNUSED   pUnknown;
    PMPTHREAT_INFOEX_UNUSED   pKnownGood;
    PMPTHREAT_INFOEX_NIS      pNis;
  } Data;
  MPDETECTION_STATE     State;
  MP_MIDL_STRING LPWSTR DetectionUser;
  MPSOURCE              DetectionSource;
  MP_MIDL_STRING LPWSTR ProcessName;
  MPDETECTION_ORIGIN    DetectionOrigin;
  DWORD                 reserved1;
  ULARGE_INTEGER        DetectionTime;
  MPEXECUTION_STATUS    PreExecutionStatus;
  ULARGE_INTEGER        RemediationTime;
  MPEXECUTION_STATUS    PostExecutionStatus;
  BOOL                  CriticalFailure;
  DWORD                 NonCriticalReason;
  MP_MIDL_STRING LPWSTR RemediationUser;
  DWORD                 RemediationResourceCount;
  PMPRESOURCE_INFO      RemediationResourceList[RemediationResourceCount];
  BOOL                  FailureResolved;
  MPRESOLVED_REASON     ResolvedReason;
  DWORD                 AdditionalActions;
  DWORD                 ResolvedActions;
  DWORD                 dwThreatStatusFlag;
} MPTHREAT_INFO, *PMPTHREAT_INFO;
```



## <a name="members"></a><span data-ttu-id="0740f-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="0740f-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="0740f-109">**ThreatID**</span><span class="sxs-lookup"><span data-stu-id="0740f-109">**ThreatID**</span></span>
</dt> <dd>

<span data-ttu-id="0740f-110">Tipo: **\_ ID. de MPTHREAT**</span><span class="sxs-lookup"><span data-stu-id="0740f-110">Type: **MPTHREAT\_ID**</span></span>

</dd> <dd>

<span data-ttu-id="0740f-111">Identificador de amenaza.</span><span class="sxs-lookup"><span data-stu-id="0740f-111">Threat identifier.</span></span> <span data-ttu-id="0740f-112">El bit superior se establece para identificar las amenazas relacionadas con el antivirus.</span><span class="sxs-lookup"><span data-stu-id="0740f-112">Upper bit is set to identify antivirus-related threats.</span></span>

</dd> <dt>

<span data-ttu-id="0740f-113">**DetectionID**</span><span class="sxs-lookup"><span data-stu-id="0740f-113">**DetectionID**</span></span>
</dt> <dd>

<span data-ttu-id="0740f-114">Tipo: **GUID**</span><span class="sxs-lookup"><span data-stu-id="0740f-114">Type: **GUID**</span></span>

</dd> <dd>

<span data-ttu-id="0740f-115">IDENTIFICADOR de detección.</span><span class="sxs-lookup"><span data-stu-id="0740f-115">Detection ID.</span></span>

</dd> <dt>

<span data-ttu-id="0740f-116">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="0740f-116">**Name**</span></span>
</dt> <dd>

<span data-ttu-id="0740f-117">Type: **MP \_ MIDL \_ String LPWStr**</span><span class="sxs-lookup"><span data-stu-id="0740f-117">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="0740f-118">Nombre de amenaza.</span><span class="sxs-lookup"><span data-stu-id="0740f-118">Threat name.</span></span>

</dd> <dt>

<span data-ttu-id="0740f-119">**ThreatType**</span><span class="sxs-lookup"><span data-stu-id="0740f-119">**ThreatType**</span></span>
</dt> <dd>

<span data-ttu-id="0740f-120">Tipo: **[ **MPTHREAT \_ Type**](mpthreat-type.md)**</span><span class="sxs-lookup"><span data-stu-id="0740f-120">Type: **[**MPTHREAT\_TYPE**](mpthreat-type.md)**</span></span>

</dd> <dd>

<span data-ttu-id="0740f-121">Tipo de amenaza.</span><span class="sxs-lookup"><span data-stu-id="0740f-121">Threat type.</span></span> <span data-ttu-id="0740f-122">Se utiliza para diferenciar entre distintos tipos de amenazas, como los conocidos, los desconocidos o los conocidos.</span><span class="sxs-lookup"><span data-stu-id="0740f-122">Used to differentiate among different threat types such as known bad, unknown, or known good.</span></span> <span data-ttu-id="0740f-123">Consulte [**\_ tipo de MPTHREAT**](mpthreat-type.md).</span><span class="sxs-lookup"><span data-stu-id="0740f-123">See [**MPTHREAT\_TYPE**](mpthreat-type.md).</span></span>

</dd> <dt>

<span data-ttu-id="0740f-124">**ThreatCriticality**</span><span class="sxs-lookup"><span data-stu-id="0740f-124">**ThreatCriticality**</span></span>
</dt> <dd>

<span data-ttu-id="0740f-125">Tipo: **[ **\_ gravedad de MPTHREAT**](mpthreat-severity.md)**</span><span class="sxs-lookup"><span data-stu-id="0740f-125">Type: **[**MPTHREAT\_SEVERITY**](mpthreat-severity.md)**</span></span>

</dd> <dd>

<span data-ttu-id="0740f-126">Importancia de las amenazas.</span><span class="sxs-lookup"><span data-stu-id="0740f-126">Threat criticality.</span></span> <span data-ttu-id="0740f-127">Vea [**\_ gravedad de MPTHREAT**](mpthreat-severity.md).</span><span class="sxs-lookup"><span data-stu-id="0740f-127">See [**MPTHREAT\_SEVERITY**](mpthreat-severity.md).</span></span>

</dd> <dt>

<span data-ttu-id="0740f-128">**ThreatCategory**</span><span class="sxs-lookup"><span data-stu-id="0740f-128">**ThreatCategory**</span></span>
</dt> <dd>

<span data-ttu-id="0740f-129">Tipo: **[ **\_ categoría MPTHREAT**](mpthreat-category.md)**</span><span class="sxs-lookup"><span data-stu-id="0740f-129">Type: **[**MPTHREAT\_CATEGORY**](mpthreat-category.md)**</span></span>

</dd> <dd>

<span data-ttu-id="0740f-130">Categoría de amenazas, como un troyano o un registrador de virus.</span><span class="sxs-lookup"><span data-stu-id="0740f-130">Threat category, such as a trojan or a keylogger.</span></span> <span data-ttu-id="0740f-131">Vea [**la \_ categoría MPTHREAT**](mpthreat-category.md).</span><span class="sxs-lookup"><span data-stu-id="0740f-131">See [**MPTHREAT\_CATEGORY**](mpthreat-category.md).</span></span>

</dd> <dt>

<span data-ttu-id="0740f-132">**ThreatShortDescriptionID**</span><span class="sxs-lookup"><span data-stu-id="0740f-132">**ThreatShortDescriptionID**</span></span>
</dt> <dd>

<span data-ttu-id="0740f-133">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="0740f-133">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="0740f-134">IDENTIFICADOR de descripción breve de amenaza.</span><span class="sxs-lookup"><span data-stu-id="0740f-134">Threat short description ID.</span></span>

</dd> <dt>

<span data-ttu-id="0740f-135">**ThreatAdviseDescriptionID**</span><span class="sxs-lookup"><span data-stu-id="0740f-135">**ThreatAdviseDescriptionID**</span></span>
</dt> <dd>

<span data-ttu-id="0740f-136">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="0740f-136">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="0740f-137">IDENTIFICADOR de descripción de aviso de amenazas.</span><span class="sxs-lookup"><span data-stu-id="0740f-137">Threat advise description ID.</span></span>

</dd> <dt>

<span data-ttu-id="0740f-138">**ThreatStatus**</span><span class="sxs-lookup"><span data-stu-id="0740f-138">**ThreatStatus**</span></span>
</dt> <dd>

<span data-ttu-id="0740f-139">Tipo: **[ **\_ Estado de MPTHREAT**](mpthreat-status.md)**</span><span class="sxs-lookup"><span data-stu-id="0740f-139">Type: **[**MPTHREAT\_STATUS**](mpthreat-status.md)**</span></span>

</dd> <dd>

<span data-ttu-id="0740f-140">Estado de amenaza, como detectado, limpiado o en cuarentena.</span><span class="sxs-lookup"><span data-stu-id="0740f-140">Threat status such as detected, cleaned, or quarantined.</span></span> <span data-ttu-id="0740f-141">Consulte [**\_ Estado de MPTHREAT**](mpthreat-status.md).</span><span class="sxs-lookup"><span data-stu-id="0740f-141">See [**MPTHREAT\_STATUS**](mpthreat-status.md).</span></span>

</dd> <dt>

<span data-ttu-id="0740f-142">**SuggestedActionCount**</span><span class="sxs-lookup"><span data-stu-id="0740f-142">**SuggestedActionCount**</span></span>
</dt> <dd>

<span data-ttu-id="0740f-143">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="0740f-143">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="0740f-144">Recuento de acciones sugeridas en **SuggestedActionArray**.</span><span class="sxs-lookup"><span data-stu-id="0740f-144">Count of suggested actions in **SuggestedActionArray**.</span></span>

</dd> <dt>

<span data-ttu-id="0740f-145">**SuggestedActionArray**</span><span class="sxs-lookup"><span data-stu-id="0740f-145">**SuggestedActionArray**</span></span>
</dt> <dd>

<span data-ttu-id="0740f-146">Tipo: **[**MPTHREAT de \_ acción**](mpthreat-action.md)máxima del módulo de administración de acciones \[ \_ \_\]**</span><span class="sxs-lookup"><span data-stu-id="0740f-146">Type: **[**MPTHREAT\_ACTION**](mpthreat-action.md)\[MP\_MAX\_SUGGESTIONS\]**</span></span>

</dd> <dd>

<span data-ttu-id="0740f-147">Matriz de acciones sugeridas.</span><span class="sxs-lookup"><span data-stu-id="0740f-147">Array of suggested actions.</span></span> <span data-ttu-id="0740f-148">Consulte [**la \_ acción MPTHREAT**](mpthreat-action.md).</span><span class="sxs-lookup"><span data-stu-id="0740f-148">See [**MPTHREAT\_ACTION**](mpthreat-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="0740f-149">**ResourceCount**</span><span class="sxs-lookup"><span data-stu-id="0740f-149">**ResourceCount**</span></span>
</dt> <dd>

<span data-ttu-id="0740f-150">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="0740f-150">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="0740f-151">Recuento de recursos en **ResourceList**.</span><span class="sxs-lookup"><span data-stu-id="0740f-151">Count of resources in **ResourceList**.</span></span>

</dd> <dt>

<span data-ttu-id="0740f-152">**ResourceList**</span><span class="sxs-lookup"><span data-stu-id="0740f-152">**ResourceList**</span></span>
</dt> <dd>

<span data-ttu-id="0740f-153">Tipo: \**PMPRESOURCE \_ info \** _</span><span class="sxs-lookup"><span data-stu-id="0740f-153">Type: \**PMPRESOURCE\_INFO\** _</span></span>

</dd> <dd>

<span data-ttu-id="0740f-154">Lista de recursos identificados con la amenaza.</span><span class="sxs-lookup"><span data-stu-id="0740f-154">List of resources identified with the threat.</span></span> <span data-ttu-id="0740f-155">Vea [_ *MPRESOURCE \_ info* \*](mpresource-info.md).</span><span class="sxs-lookup"><span data-stu-id="0740f-155">See [_ *MPRESOURCE\_INFO*\*](mpresource-info.md).</span></span>

</dd> <dt>

<span data-ttu-id="0740f-156">**ThreatStatusTime**</span><span class="sxs-lookup"><span data-stu-id="0740f-156">**ThreatStatusTime**</span></span>
</dt> <dd>

<span data-ttu-id="0740f-157">Tipo: **ULARGE \_ Integer**</span><span class="sxs-lookup"><span data-stu-id="0740f-157">Type: **ULARGE\_INTEGER**</span></span>

</dd> <dd>

<span data-ttu-id="0740f-158">Hora en que se modificó por última vez el estado de la amenaza.</span><span class="sxs-lookup"><span data-stu-id="0740f-158">Time when threat status last changed.</span></span>

</dd> <dt>

<span data-ttu-id="0740f-159">**ThreatStatusCode**</span><span class="sxs-lookup"><span data-stu-id="0740f-159">**ThreatStatusCode**</span></span>
</dt> <dd>

<span data-ttu-id="0740f-160">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="0740f-160">Type: **HRESULT**</span></span>

</dd> <dd>

<span data-ttu-id="0740f-161">Código de estado asociado al estado de amenaza.</span><span class="sxs-lookup"><span data-stu-id="0740f-161">Status code associated with the threat status.</span></span>

</dd> <dt>

<span data-ttu-id="0740f-162">**ThreatDetection**</span><span class="sxs-lookup"><span data-stu-id="0740f-162">**ThreatDetection**</span></span>
</dt> <dd>

<span data-ttu-id="0740f-163">Tipo: **[ **\_ detección de MPTHREAT**](mpthreat-detection.md)**</span><span class="sxs-lookup"><span data-stu-id="0740f-163">Type: **[**MPTHREAT\_DETECTION**](mpthreat-detection.md)**</span></span>

</dd> <dd>

<span data-ttu-id="0740f-164">Tipo de detección de amenazas, como concreto, sospechoso o genérico.</span><span class="sxs-lookup"><span data-stu-id="0740f-164">Threat detection type, such as concrete, suspicious, or generic.</span></span> <span data-ttu-id="0740f-165">Consulte [**\_ detección de MPTHREAT**](mpthreat-detection.md).</span><span class="sxs-lookup"><span data-stu-id="0740f-165">See [**MPTHREAT\_DETECTION**](mpthreat-detection.md).</span></span>

</dd> <dt>

<span data-ttu-id="0740f-166">**QuarantineGuid**</span><span class="sxs-lookup"><span data-stu-id="0740f-166">**QuarantineGuid**</span></span>
</dt> <dd>

<span data-ttu-id="0740f-167">Tipo: **GUID**</span><span class="sxs-lookup"><span data-stu-id="0740f-167">Type: **GUID**</span></span>

</dd> <dd>

<span data-ttu-id="0740f-168">GUID de cuarentena.</span><span class="sxs-lookup"><span data-stu-id="0740f-168">Quarantine guid.</span></span>

</dd> <dt>

<span data-ttu-id="0740f-169">**ExecutionStatus**</span><span class="sxs-lookup"><span data-stu-id="0740f-169">**ExecutionStatus**</span></span>
</dt> <dd>

<span data-ttu-id="0740f-170">Tipo: **[ **\_ Estado de MPEXECUTION**](mpexecution-status.md)**</span><span class="sxs-lookup"><span data-stu-id="0740f-170">Type: **[**MPEXECUTION\_STATUS**](mpexecution-status.md)**</span></span>

</dd> <dd>

<span data-ttu-id="0740f-171">Estado de ejecución de la amenaza, como desconocido, bloqueado o activo.</span><span class="sxs-lookup"><span data-stu-id="0740f-171">Execution status of the threat, such as not known, blocked, or active.</span></span> <span data-ttu-id="0740f-172">Consulte [**\_ Estado de MPEXECUTION**](mpexecution-status.md).</span><span class="sxs-lookup"><span data-stu-id="0740f-172">See [**MPEXECUTION\_STATUS**](mpexecution-status.md).</span></span>

</dd> <dt>

<span data-ttu-id="0740f-173">**Data**</span><span class="sxs-lookup"><span data-stu-id="0740f-173">**Data**</span></span>
</dt> <dd>

<span data-ttu-id="0740f-174">Información adicional.</span><span class="sxs-lookup"><span data-stu-id="0740f-174">Extra information.</span></span> <span data-ttu-id="0740f-175">El puntero a la estructura adecuada depende del valor de **ThreatType**.</span><span class="sxs-lookup"><span data-stu-id="0740f-175">The pointer to the appropriate structure depends on the value of **ThreatType**.</span></span>

<dl> <dt>

<span data-ttu-id="0740f-176">**pKnownBad**</span><span class="sxs-lookup"><span data-stu-id="0740f-176">**pKnownBad**</span></span>
</dt> <dd>

<span data-ttu-id="0740f-177">Tipo: **PMPTHREAT \_ INFOEX \_ no usado**</span><span class="sxs-lookup"><span data-stu-id="0740f-177">Type: **PMPTHREAT\_INFOEX\_UNUSED**</span></span>

</dd> <dd>

<span data-ttu-id="0740f-178">When **ThreatType**  ==  **MPTHREAT \_ Type \_ KNOWNBAD**.</span><span class="sxs-lookup"><span data-stu-id="0740f-178">When **ThreatType** == **MPTHREAT\_TYPE\_KNOWNBAD**.</span></span> <span data-ttu-id="0740f-179">Consulte [**MPTHREAT \_ INFOEX \_ Unused**](mpthreat-infoex-unused.md).</span><span class="sxs-lookup"><span data-stu-id="0740f-179">See [**MPTHREAT\_INFOEX\_UNUSED**](mpthreat-infoex-unused.md).</span></span>

</dd> <dt>

<span data-ttu-id="0740f-180">**pBehavior**</span><span class="sxs-lookup"><span data-stu-id="0740f-180">**pBehavior**</span></span>
</dt> <dd>

<span data-ttu-id="0740f-181">Tipo: **PMPTHREAT \_ INFOEX \_ Behavior**</span><span class="sxs-lookup"><span data-stu-id="0740f-181">Type: **PMPTHREAT\_INFOEX\_BEHAVIOR**</span></span>

</dd> <dd>

<span data-ttu-id="0740f-182">Cuando el comportamiento de tipo de **ThreatType**  ==  **MPTHREAT \_ \_**.</span><span class="sxs-lookup"><span data-stu-id="0740f-182">When **ThreatType** == **MPTHREAT\_TYPE\_BEHAVIOR**.</span></span> <span data-ttu-id="0740f-183">Consulte [**MPTHREAT \_ INFOEX \_ Behavior**](mpthreat-infoex-behavior.md).</span><span class="sxs-lookup"><span data-stu-id="0740f-183">See [**MPTHREAT\_INFOEX\_BEHAVIOR**](mpthreat-infoex-behavior.md).</span></span>

</dd> <dt>

<span data-ttu-id="0740f-184">**pUnknown**</span><span class="sxs-lookup"><span data-stu-id="0740f-184">**pUnknown**</span></span>
</dt> <dd>

<span data-ttu-id="0740f-185">Tipo: **PMPTHREAT \_ INFOEX \_ no usado**</span><span class="sxs-lookup"><span data-stu-id="0740f-185">Type: **PMPTHREAT\_INFOEX\_UNUSED**</span></span>

</dd> <dd>

<span data-ttu-id="0740f-186">Cuando **ThreatType**  ==  **MPTHREAT \_ Type \_ Unknown**.</span><span class="sxs-lookup"><span data-stu-id="0740f-186">When **ThreatType** == **MPTHREAT\_TYPE\_UNKNOWN**.</span></span> <span data-ttu-id="0740f-187">Consulte [**MPTHREAT \_ INFOEX \_ Unused**](mpthreat-infoex-unused.md).</span><span class="sxs-lookup"><span data-stu-id="0740f-187">See [**MPTHREAT\_INFOEX\_UNUSED**](mpthreat-infoex-unused.md).</span></span>

</dd> <dt>

<span data-ttu-id="0740f-188">**pKnownGood**</span><span class="sxs-lookup"><span data-stu-id="0740f-188">**pKnownGood**</span></span>
</dt> <dd>

<span data-ttu-id="0740f-189">Tipo: **PMPTHREAT \_ INFOEX \_ no usado**</span><span class="sxs-lookup"><span data-stu-id="0740f-189">Type: **PMPTHREAT\_INFOEX\_UNUSED**</span></span>

</dd> <dd>

<span data-ttu-id="0740f-190">When **ThreatType** = = MPTHREAT \_ Type \_ KNOWNGOOD.</span><span class="sxs-lookup"><span data-stu-id="0740f-190">When **ThreatType** == MPTHREAT\_TYPE\_KNOWNGOOD.</span></span> <span data-ttu-id="0740f-191">Consulte [**MPTHREAT \_ INFOEX \_ Unused**](mpthreat-infoex-unused.md).</span><span class="sxs-lookup"><span data-stu-id="0740f-191">See [**MPTHREAT\_INFOEX\_UNUSED**](mpthreat-infoex-unused.md).</span></span>

</dd> <dt>

<span data-ttu-id="0740f-192">**pNis**</span><span class="sxs-lookup"><span data-stu-id="0740f-192">**pNis**</span></span>
</dt> <dd>

<span data-ttu-id="0740f-193">Tipo: **PMPTHREAT \_ INFOEX \_ NIS**</span><span class="sxs-lookup"><span data-stu-id="0740f-193">Type: **PMPTHREAT\_INFOEX\_NIS**</span></span>

</dd> <dd>

<span data-ttu-id="0740f-194">Cuando **ThreatType**  ==  **MPTHREAT \_ Type \_ NIS**.</span><span class="sxs-lookup"><span data-stu-id="0740f-194">When **ThreatType** == **MPTHREAT\_TYPE\_NIS**.</span></span> <span data-ttu-id="0740f-195">Consulte [**MPTHREAT \_ INFOEX \_ NIS**](mpthreat-infoex-nis.md).</span><span class="sxs-lookup"><span data-stu-id="0740f-195">See [**MPTHREAT\_INFOEX\_NIS**](mpthreat-infoex-nis.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="0740f-196">**State**</span><span class="sxs-lookup"><span data-stu-id="0740f-196">**State**</span></span>
</dt> <dd>

<span data-ttu-id="0740f-197">Tipo: **[ **\_ Estado de MPDETECTION**](mpdetection-state.md)**</span><span class="sxs-lookup"><span data-stu-id="0740f-197">Type: **[**MPDETECTION\_STATE**](mpdetection-state.md)**</span></span>

</dd> <dd>

<span data-ttu-id="0740f-198">Estado actual de la detección.</span><span class="sxs-lookup"><span data-stu-id="0740f-198">The current state of the detection.</span></span> <span data-ttu-id="0740f-199">Consulte [**\_ Estado de MPDETECTION**](mpdetection-state.md).</span><span class="sxs-lookup"><span data-stu-id="0740f-199">See [**MPDETECTION\_STATE**](mpdetection-state.md).</span></span>

</dd> <dt>

<span data-ttu-id="0740f-200">**DetectionUser**</span><span class="sxs-lookup"><span data-stu-id="0740f-200">**DetectionUser**</span></span>
</dt> <dd>

<span data-ttu-id="0740f-201">Type: **MP \_ MIDL \_ String LPWStr**</span><span class="sxs-lookup"><span data-stu-id="0740f-201">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="0740f-202">Usuario asociado a la detección, con el formato "dominio/usuario".</span><span class="sxs-lookup"><span data-stu-id="0740f-202">The user associated with the detection, in the format "domain/user".</span></span>

</dd> <dt>

<span data-ttu-id="0740f-203">**DetectionSource**</span><span class="sxs-lookup"><span data-stu-id="0740f-203">**DetectionSource**</span></span>
</dt> <dd>

<span data-ttu-id="0740f-204">Tipo: **[ **MPSOURCE**](mpsource.md)**</span><span class="sxs-lookup"><span data-stu-id="0740f-204">Type: **[**MPSOURCE**](mpsource.md)**</span></span>

</dd> <dd>

<span data-ttu-id="0740f-205">Origen de la detección.</span><span class="sxs-lookup"><span data-stu-id="0740f-205">The source of the detection.</span></span> <span data-ttu-id="0740f-206">Vea [**MPSOURCE**](mpsource.md).</span><span class="sxs-lookup"><span data-stu-id="0740f-206">See [**MPSOURCE**](mpsource.md).</span></span>

</dd> <dt>

<span data-ttu-id="0740f-207">**ProcessName**</span><span class="sxs-lookup"><span data-stu-id="0740f-207">**ProcessName**</span></span>
</dt> <dd>

<span data-ttu-id="0740f-208">Type: **MP \_ MIDL \_ String LPWStr**</span><span class="sxs-lookup"><span data-stu-id="0740f-208">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="0740f-209">Nombre del proceso asociado a la detección.</span><span class="sxs-lookup"><span data-stu-id="0740f-209">Process name associated with the detection.</span></span>

</dd> <dt>

<span data-ttu-id="0740f-210">**DetectionOrigin**</span><span class="sxs-lookup"><span data-stu-id="0740f-210">**DetectionOrigin**</span></span>
</dt> <dd>

<span data-ttu-id="0740f-211">Tipo: **[ **MPDETECTION \_ Origin**](mpdetection-origin.md)**</span><span class="sxs-lookup"><span data-stu-id="0740f-211">Type: **[**MPDETECTION\_ORIGIN**](mpdetection-origin.md)**</span></span>

</dd> <dd>

<span data-ttu-id="0740f-212">El origen de la detección, como local o de red.</span><span class="sxs-lookup"><span data-stu-id="0740f-212">The origin of the detection, such as local or network.</span></span> <span data-ttu-id="0740f-213">Vea [**MPDETECTION \_ Origin**](mpdetection-origin.md).</span><span class="sxs-lookup"><span data-stu-id="0740f-213">See [**MPDETECTION\_ORIGIN**](mpdetection-origin.md).</span></span>

</dd> <dt>

<span data-ttu-id="0740f-214">**reserved1**</span><span class="sxs-lookup"><span data-stu-id="0740f-214">**reserved1**</span></span>
</dt> <dd>

<span data-ttu-id="0740f-215">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="0740f-215">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="0740f-216">Metadatos reservados sobre la detección.</span><span class="sxs-lookup"><span data-stu-id="0740f-216">Reserved metadata about the detection.</span></span>

</dd> <dt>

<span data-ttu-id="0740f-217">**DetectionTime**</span><span class="sxs-lookup"><span data-stu-id="0740f-217">**DetectionTime**</span></span>
</dt> <dd>

<span data-ttu-id="0740f-218">Tipo: **ULARGE \_ Integer**</span><span class="sxs-lookup"><span data-stu-id="0740f-218">Type: **ULARGE\_INTEGER**</span></span>

</dd> <dd>

<span data-ttu-id="0740f-219">Hora de la detección inicial.</span><span class="sxs-lookup"><span data-stu-id="0740f-219">The time of the initial detection.</span></span>

</dd> <dt>

<span data-ttu-id="0740f-220">**PreExecutionStatus**</span><span class="sxs-lookup"><span data-stu-id="0740f-220">**PreExecutionStatus**</span></span>
</dt> <dd>

<span data-ttu-id="0740f-221">Tipo: **[ **\_ Estado de MPEXECUTION**](mpexecution-status.md)**</span><span class="sxs-lookup"><span data-stu-id="0740f-221">Type: **[**MPEXECUTION\_STATUS**](mpexecution-status.md)**</span></span>

</dd> <dd>

<span data-ttu-id="0740f-222">Estado de ejecución justo antes de la corrección.</span><span class="sxs-lookup"><span data-stu-id="0740f-222">Execution status right before remediation.</span></span> <span data-ttu-id="0740f-223">Consulte [**\_ Estado de MPEXECUTION**](mpexecution-status.md).</span><span class="sxs-lookup"><span data-stu-id="0740f-223">See [**MPEXECUTION\_STATUS**](mpexecution-status.md).</span></span>

</dd> <dt>

<span data-ttu-id="0740f-224">**RemediationTime**</span><span class="sxs-lookup"><span data-stu-id="0740f-224">**RemediationTime**</span></span>
</dt> <dd>

<span data-ttu-id="0740f-225">Tipo: **ULARGE \_ Integer**</span><span class="sxs-lookup"><span data-stu-id="0740f-225">Type: **ULARGE\_INTEGER**</span></span>

</dd> <dd>

<span data-ttu-id="0740f-226">La corrección de tiempo que se ha producido.</span><span class="sxs-lookup"><span data-stu-id="0740f-226">The time remediation occured.</span></span>

</dd> <dt>

<span data-ttu-id="0740f-227">**PostExecutionStatus**</span><span class="sxs-lookup"><span data-stu-id="0740f-227">**PostExecutionStatus**</span></span>
</dt> <dd>

<span data-ttu-id="0740f-228">Tipo: **[ **\_ Estado de MPEXECUTION**](mpexecution-status.md)**</span><span class="sxs-lookup"><span data-stu-id="0740f-228">Type: **[**MPEXECUTION\_STATUS**](mpexecution-status.md)**</span></span>

</dd> <dd>

<span data-ttu-id="0740f-229">Estado de ejecución después de la corrección.</span><span class="sxs-lookup"><span data-stu-id="0740f-229">Execution status after remediation.</span></span> <span data-ttu-id="0740f-230">Consulte [**\_ Estado de MPEXECUTION**](mpexecution-status.md).</span><span class="sxs-lookup"><span data-stu-id="0740f-230">See [**MPEXECUTION\_STATUS**](mpexecution-status.md).</span></span>

</dd> <dt>

<span data-ttu-id="0740f-231">**CriticalFailure**</span><span class="sxs-lookup"><span data-stu-id="0740f-231">**CriticalFailure**</span></span>
</dt> <dd>

<span data-ttu-id="0740f-232">Tipo: **bool**</span><span class="sxs-lookup"><span data-stu-id="0740f-232">Type: **BOOL**</span></span>

</dd> <dd>

<span data-ttu-id="0740f-233">True si el error de corrección era crítico.</span><span class="sxs-lookup"><span data-stu-id="0740f-233">True if the remediation failure was critical.</span></span>

</dd> <dt>

<span data-ttu-id="0740f-234">**NonCriticalReason**</span><span class="sxs-lookup"><span data-stu-id="0740f-234">**NonCriticalReason**</span></span>
</dt> <dd>

<span data-ttu-id="0740f-235">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="0740f-235">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="0740f-236">Razón por la que el error de corrección no es crítico.</span><span class="sxs-lookup"><span data-stu-id="0740f-236">The reason the remediation failure is not critical.</span></span> <span data-ttu-id="0740f-237">No se garantiza que se admita en el futuro.</span><span class="sxs-lookup"><span data-stu-id="0740f-237">This is not guaranteed to be supported in the future.</span></span>

</dd> <dt>

<span data-ttu-id="0740f-238">**RemediationUser**</span><span class="sxs-lookup"><span data-stu-id="0740f-238">**RemediationUser**</span></span>
</dt> <dd>

<span data-ttu-id="0740f-239">Type: **MP \_ MIDL \_ String LPWStr**</span><span class="sxs-lookup"><span data-stu-id="0740f-239">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="0740f-240">Usuario que solicitó la corrección, con el formato "dominio/usuario".</span><span class="sxs-lookup"><span data-stu-id="0740f-240">User that requested the remediation, in the format "domain/user".</span></span>

</dd> <dt>

<span data-ttu-id="0740f-241">**RemediationResourceCount**</span><span class="sxs-lookup"><span data-stu-id="0740f-241">**RemediationResourceCount**</span></span>
</dt> <dd>

<span data-ttu-id="0740f-242">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="0740f-242">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="0740f-243">Recuento de recursos en **RemediationResourceList**.</span><span class="sxs-lookup"><span data-stu-id="0740f-243">Count of resources in **RemediationResourceList**.</span></span>

</dd> <dt>

<span data-ttu-id="0740f-244">**RemediationResourceList**</span><span class="sxs-lookup"><span data-stu-id="0740f-244">**RemediationResourceList**</span></span>
</dt> <dd>

<span data-ttu-id="0740f-245">Tipo: **PMPRESOURCE \_ info \[ RemediationResourceCount \]**</span><span class="sxs-lookup"><span data-stu-id="0740f-245">Type: **PMPRESOURCE\_INFO\[RemediationResourceCount\]**</span></span>

</dd> <dd>

<span data-ttu-id="0740f-246">Lista de recursos con errores durante la corrección.</span><span class="sxs-lookup"><span data-stu-id="0740f-246">List of resources that failed during remediation.</span></span> <span data-ttu-id="0740f-247">Vea [**\_ información de MPRESOURCE**](mpresource-info.md).</span><span class="sxs-lookup"><span data-stu-id="0740f-247">See [**MPRESOURCE\_INFO**](mpresource-info.md).</span></span>

</dd> <dt>

<span data-ttu-id="0740f-248">**FailureResolved**</span><span class="sxs-lookup"><span data-stu-id="0740f-248">**FailureResolved**</span></span>
</dt> <dd>

<span data-ttu-id="0740f-249">Tipo: **bool**</span><span class="sxs-lookup"><span data-stu-id="0740f-249">Type: **BOOL**</span></span>

</dd> <dd>

<span data-ttu-id="0740f-250">True si se ha resuelto el error de corrección.</span><span class="sxs-lookup"><span data-stu-id="0740f-250">True if remediation failure been resolved.</span></span> <span data-ttu-id="0740f-251">Esto moverá el cubo a completa o a una acción adicional.</span><span class="sxs-lookup"><span data-stu-id="0740f-251">This will move the bucket to either complete or an additional action.</span></span>

</dd> <dt>

<span data-ttu-id="0740f-252">**ResolvedReason**</span><span class="sxs-lookup"><span data-stu-id="0740f-252">**ResolvedReason**</span></span>
</dt> <dd>

<span data-ttu-id="0740f-253">Tipo: **[ **MPRESOLVED \_ Reason**](mpresolved-reason.md)**</span><span class="sxs-lookup"><span data-stu-id="0740f-253">Type: **[**MPRESOLVED\_REASON**](mpresolved-reason.md)**</span></span>

</dd> <dd>

<span data-ttu-id="0740f-254">Motivo de la resolución de un error de corrección.</span><span class="sxs-lookup"><span data-stu-id="0740f-254">Reason for remediation failure being resolved.</span></span> <span data-ttu-id="0740f-255">Este es el motivo por el que la detección se ha pasado de no se pudo realizar una acción adicional o ha finalizado.</span><span class="sxs-lookup"><span data-stu-id="0740f-255">This is the reason the detection moved from failed to additional action or finished.</span></span> <span data-ttu-id="0740f-256">Consulte [**MPRESOLVED \_ Reason**](mpresolved-reason.md).</span><span class="sxs-lookup"><span data-stu-id="0740f-256">See [**MPRESOLVED\_REASON**](mpresolved-reason.md).</span></span>

</dd> <dt>

<span data-ttu-id="0740f-257">**AdditionalActions**</span><span class="sxs-lookup"><span data-stu-id="0740f-257">**AdditionalActions**</span></span>
</dt> <dd>

<span data-ttu-id="0740f-258">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="0740f-258">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="0740f-259">Se requieren acciones adicionales.</span><span class="sxs-lookup"><span data-stu-id="0740f-259">Are additional actions required.</span></span>

</dd> <dt>

<span data-ttu-id="0740f-260">**ResolvedActions**</span><span class="sxs-lookup"><span data-stu-id="0740f-260">**ResolvedActions**</span></span>
</dt> <dd>

<span data-ttu-id="0740f-261">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="0740f-261">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="0740f-262">Acciones adicionales que se han realizado.</span><span class="sxs-lookup"><span data-stu-id="0740f-262">Any additional actions that have been performed.</span></span>

</dd> <dt>

<span data-ttu-id="0740f-263">**dwThreatStatusFlag**</span><span class="sxs-lookup"><span data-stu-id="0740f-263">**dwThreatStatusFlag**</span></span>
</dt> <dd>

<span data-ttu-id="0740f-264">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="0740f-264">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="0740f-265">Información adicional sobre la detección de amenazas.</span><span class="sxs-lookup"><span data-stu-id="0740f-265">Additonal information about the threat detection.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0740f-266">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0740f-266">Requirements</span></span>



| <span data-ttu-id="0740f-267">Requisito</span><span class="sxs-lookup"><span data-stu-id="0740f-267">Requirement</span></span> | <span data-ttu-id="0740f-268">Value</span><span class="sxs-lookup"><span data-stu-id="0740f-268">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0740f-269">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0740f-269">Minimum supported client</span></span><br/> | <span data-ttu-id="0740f-270">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="0740f-270">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="0740f-271">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0740f-271">Minimum supported server</span></span><br/> | <span data-ttu-id="0740f-272">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="0740f-272">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0740f-273">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0740f-273">Header</span></span><br/>                   | <dl> <span data-ttu-id="0740f-274"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="0740f-274"><dt>MpClient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0740f-275">Vea también</span><span class="sxs-lookup"><span data-stu-id="0740f-275">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0740f-276">**MpFreeMemory**</span><span class="sxs-lookup"><span data-stu-id="0740f-276">**MpFreeMemory**</span></span>](mpfreememory.md)
</dt> <dt>

[<span data-ttu-id="0740f-277">**MpThreatEnumerate**</span><span class="sxs-lookup"><span data-stu-id="0740f-277">**MpThreatEnumerate**</span></span>](mpthreatenumerate.md)
</dt> <dt>

[<span data-ttu-id="0740f-278">**MpThreatQuery**</span><span class="sxs-lookup"><span data-stu-id="0740f-278">**MpThreatQuery**</span></span>](mpthreatquery.md)
</dt> <dt>

[<span data-ttu-id="0740f-279">**origen de MPDETECTION \_**</span><span class="sxs-lookup"><span data-stu-id="0740f-279">**MPDETECTION\_ORIGIN**</span></span>](mpdetection-origin.md)
</dt> <dt>

[<span data-ttu-id="0740f-280">**Estado de MPDETECTION \_**</span><span class="sxs-lookup"><span data-stu-id="0740f-280">**MPDETECTION\_STATE**</span></span>](mpdetection-state.md)
</dt> <dt>

[<span data-ttu-id="0740f-281">**Estado de MPEXECUTION \_**</span><span class="sxs-lookup"><span data-stu-id="0740f-281">**MPEXECUTION\_STATUS**</span></span>](mpexecution-status.md)
</dt> <dt>

[<span data-ttu-id="0740f-282">**motivo de MPRESOLVED \_**</span><span class="sxs-lookup"><span data-stu-id="0740f-282">**MPRESOLVED\_REASON**</span></span>](mpresolved-reason.md)
</dt> <dt>

[<span data-ttu-id="0740f-283">**información de MPRESOURCE \_**</span><span class="sxs-lookup"><span data-stu-id="0740f-283">**MPRESOURCE\_INFO**</span></span>](mpresource-info.md)
</dt> <dt>

[<span data-ttu-id="0740f-284">**MPSOURCE**</span><span class="sxs-lookup"><span data-stu-id="0740f-284">**MPSOURCE**</span></span>](mpsource.md)
</dt> <dt>

[<span data-ttu-id="0740f-285">**\_acción MPTHREAT**</span><span class="sxs-lookup"><span data-stu-id="0740f-285">**MPTHREAT\_ACTION**</span></span>](mpthreat-action.md)
</dt> <dt>

[<span data-ttu-id="0740f-286">**\_categoría MPTHREAT**</span><span class="sxs-lookup"><span data-stu-id="0740f-286">**MPTHREAT\_CATEGORY**</span></span>](mpthreat-category.md)
</dt> <dt>

[<span data-ttu-id="0740f-287">**detección de MPTHREAT \_**</span><span class="sxs-lookup"><span data-stu-id="0740f-287">**MPTHREAT\_DETECTION**</span></span>](mpthreat-detection.md)
</dt> <dt>

[<span data-ttu-id="0740f-288">**\_comportamiento de INFOEX de MPTHREAT \_**</span><span class="sxs-lookup"><span data-stu-id="0740f-288">**MPTHREAT\_INFOEX\_BEHAVIOR**</span></span>](mpthreat-infoex-behavior.md)
</dt> <dt>

[<span data-ttu-id="0740f-289">**MPTHREAT \_ INFOEX \_ NIS**</span><span class="sxs-lookup"><span data-stu-id="0740f-289">**MPTHREAT\_INFOEX\_NIS**</span></span>](mpthreat-infoex-nis.md)
</dt> <dt>

[<span data-ttu-id="0740f-290">**MPTHREAT \_ INFOEX \_ no usado**</span><span class="sxs-lookup"><span data-stu-id="0740f-290">**MPTHREAT\_INFOEX\_UNUSED**</span></span>](mpthreat-infoex-unused.md)
</dt> <dt>

[<span data-ttu-id="0740f-291">**gravedad de MPTHREAT \_**</span><span class="sxs-lookup"><span data-stu-id="0740f-291">**MPTHREAT\_SEVERITY**</span></span>](mpthreat-severity.md)
</dt> <dt>

[<span data-ttu-id="0740f-292">**Estado de MPTHREAT \_**</span><span class="sxs-lookup"><span data-stu-id="0740f-292">**MPTHREAT\_STATUS**</span></span>](mpthreat-status.md)
</dt> <dt>

[<span data-ttu-id="0740f-293">**\_tipo MPTHREAT**</span><span class="sxs-lookup"><span data-stu-id="0740f-293">**MPTHREAT\_TYPE**</span></span>](mpthreat-type.md)
</dt> </dl>

 

 





