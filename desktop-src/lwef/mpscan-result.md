---
title: MPSCAN_RESULT estructura (MpClient. h)
description: Los resultados de un examen.
ms.assetid: 9031A371-092A-4175-BE1D-90442A5BED2D
keywords:
- MPSCAN_RESULT estructura de las características heredadas del entorno de Windows
- Puntero de estructura de PMPSCAN_RESULT características de entorno heredado de Windows
topic_type:
- apiref
api_name:
- MPSCAN_RESULT
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7be60df7993732bafcd7c44ac2fb581c111aed6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104274552"
---
# <a name="mpscan_result-structure"></a><span data-ttu-id="e8b84-105">Estructura del resultado de MPSCAN \_</span><span class="sxs-lookup"><span data-stu-id="e8b84-105">MPSCAN\_RESULT structure</span></span>

<span data-ttu-id="e8b84-106">Los resultados de un examen.</span><span class="sxs-lookup"><span data-stu-id="e8b84-106">The results of a scan.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8b84-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e8b84-107">Syntax</span></span>


```C++
typedef struct tagMPSCAN_RESULT {
  MPSCAN_TYPE      ScanType;
  MPSOURCE         Source;
  GUID             ScanGuid;
  ULARGE_INTEGER   StartTime;
  ULARGE_INTEGER   EndTime;
  MPTHREAT_STATS   ThreatStats;
  MPRESOURCE_STATS ResourceStats;
  ULONGLONG        SignatureVersion;
} MPSCAN_RESULT, *PMPSCAN_RESULT;
```



## <a name="members"></a><span data-ttu-id="e8b84-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="e8b84-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="e8b84-109">**ScanType**</span><span class="sxs-lookup"><span data-stu-id="e8b84-109">**ScanType**</span></span>
</dt> <dd>

<span data-ttu-id="e8b84-110">Tipo: **[ **MPSCAN \_ Type**](mpscan-type.md)**</span><span class="sxs-lookup"><span data-stu-id="e8b84-110">Type: **[**MPSCAN\_TYPE**](mpscan-type.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e8b84-111">Tipo de examen.</span><span class="sxs-lookup"><span data-stu-id="e8b84-111">Scan type.</span></span> <span data-ttu-id="e8b84-112">Consulte [**\_ tipo de MPSCAN**](mpscan-type.md).</span><span class="sxs-lookup"><span data-stu-id="e8b84-112">See [**MPSCAN\_TYPE**](mpscan-type.md).</span></span>

</dd> <dt>

<span data-ttu-id="e8b84-113">**Origen**</span><span class="sxs-lookup"><span data-stu-id="e8b84-113">**Source**</span></span>
</dt> <dd>

<span data-ttu-id="e8b84-114">Tipo: **[ **MPSOURCE**](mpsource.md)**</span><span class="sxs-lookup"><span data-stu-id="e8b84-114">Type: **[**MPSOURCE**](mpsource.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e8b84-115">Origen de la exploración, como usuario o sistema iniciado.</span><span class="sxs-lookup"><span data-stu-id="e8b84-115">Scan source, such as user or system initiated.</span></span> <span data-ttu-id="e8b84-116">Vea [**MPSOURCE**](mpsource.md).</span><span class="sxs-lookup"><span data-stu-id="e8b84-116">See [**MPSOURCE**](mpsource.md).</span></span>

</dd> <dt>

<span data-ttu-id="e8b84-117">**ScanGuid**</span><span class="sxs-lookup"><span data-stu-id="e8b84-117">**ScanGuid**</span></span>
</dt> <dd>

<span data-ttu-id="e8b84-118">Tipo: **GUID**</span><span class="sxs-lookup"><span data-stu-id="e8b84-118">Type: **GUID**</span></span>

</dd> <dd>

<span data-ttu-id="e8b84-119">Identificador de examen.</span><span class="sxs-lookup"><span data-stu-id="e8b84-119">Scan identifier.</span></span>

</dd> <dt>

<span data-ttu-id="e8b84-120">**StartTime**</span><span class="sxs-lookup"><span data-stu-id="e8b84-120">**StartTime**</span></span>
</dt> <dd>

<span data-ttu-id="e8b84-121">Tipo: **ULARGE \_ Integer**</span><span class="sxs-lookup"><span data-stu-id="e8b84-121">Type: **ULARGE\_INTEGER**</span></span>

</dd> <dd>

<span data-ttu-id="e8b84-122">Hora de inicio del examen.</span><span class="sxs-lookup"><span data-stu-id="e8b84-122">Scan start time.</span></span>

</dd> <dt>

<span data-ttu-id="e8b84-123">**EndTime**</span><span class="sxs-lookup"><span data-stu-id="e8b84-123">**EndTime**</span></span>
</dt> <dd>

<span data-ttu-id="e8b84-124">Tipo: **ULARGE \_ Integer**</span><span class="sxs-lookup"><span data-stu-id="e8b84-124">Type: **ULARGE\_INTEGER**</span></span>

</dd> <dd>

<span data-ttu-id="e8b84-125">Hora de finalización del examen.</span><span class="sxs-lookup"><span data-stu-id="e8b84-125">Scan end time.</span></span>

</dd> <dt>

<span data-ttu-id="e8b84-126">**ThreatStats**</span><span class="sxs-lookup"><span data-stu-id="e8b84-126">**ThreatStats**</span></span>
</dt> <dd>

<span data-ttu-id="e8b84-127">Tipo: **[ **\_ estadísticas de MPTHREAT**](mpthreat-stats.md)**</span><span class="sxs-lookup"><span data-stu-id="e8b84-127">Type: **[**MPTHREAT\_STATS**](mpthreat-stats.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e8b84-128">Estadísticas relacionadas con amenazas.</span><span class="sxs-lookup"><span data-stu-id="e8b84-128">Threat-related statistics.</span></span> <span data-ttu-id="e8b84-129">Consulte [**\_ estadísticas de MPTHREAT**](mpthreat-stats.md).</span><span class="sxs-lookup"><span data-stu-id="e8b84-129">See [**MPTHREAT\_STATS**](mpthreat-stats.md).</span></span>

</dd> <dt>

<span data-ttu-id="e8b84-130">**ResourceStats**</span><span class="sxs-lookup"><span data-stu-id="e8b84-130">**ResourceStats**</span></span>
</dt> <dd>

<span data-ttu-id="e8b84-131">Tipo: **[ **\_ estadísticas de MPRESOURCE**](mpresource-stats.md)**</span><span class="sxs-lookup"><span data-stu-id="e8b84-131">Type: **[**MPRESOURCE\_STATS**](mpresource-stats.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e8b84-132">Estadísticas relacionadas con recursos.</span><span class="sxs-lookup"><span data-stu-id="e8b84-132">Resource-related statistics.</span></span> <span data-ttu-id="e8b84-133">Consulte [**\_ estadísticas de MPRESOURCE**](mpresource-stats.md).</span><span class="sxs-lookup"><span data-stu-id="e8b84-133">See [**MPRESOURCE\_STATS**](mpresource-stats.md).</span></span>

</dd> <dt>

<span data-ttu-id="e8b84-134">**SignatureVersion**</span><span class="sxs-lookup"><span data-stu-id="e8b84-134">**SignatureVersion**</span></span>
</dt> <dd>

<span data-ttu-id="e8b84-135">Tipo: **ULONGLONG**</span><span class="sxs-lookup"><span data-stu-id="e8b84-135">Type: **ULONGLONG**</span></span>

</dd> <dd>

<span data-ttu-id="e8b84-136">Versión de la firma utilizada para el examen.</span><span class="sxs-lookup"><span data-stu-id="e8b84-136">Version of signature used for scan.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e8b84-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e8b84-137">Requirements</span></span>



| <span data-ttu-id="e8b84-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="e8b84-138">Requirement</span></span> | <span data-ttu-id="e8b84-139">Value</span><span class="sxs-lookup"><span data-stu-id="e8b84-139">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e8b84-140">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e8b84-140">Minimum supported client</span></span><br/> | <span data-ttu-id="e8b84-141">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="e8b84-141">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="e8b84-142">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e8b84-142">Minimum supported server</span></span><br/> | <span data-ttu-id="e8b84-143">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="e8b84-143">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e8b84-144">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e8b84-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="e8b84-145"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="e8b84-145"><dt>MpClient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e8b84-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="e8b84-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8b84-147">**estadísticas de MPRESOURCE \_**</span><span class="sxs-lookup"><span data-stu-id="e8b84-147">**MPRESOURCE\_STATS**</span></span>](mpresource-stats.md)
</dt> <dt>

[<span data-ttu-id="e8b84-148">**\_tipo MPSCAN**</span><span class="sxs-lookup"><span data-stu-id="e8b84-148">**MPSCAN\_TYPE**</span></span>](mpscan-type.md)
</dt> <dt>

[<span data-ttu-id="e8b84-149">**MPSOURCE**</span><span class="sxs-lookup"><span data-stu-id="e8b84-149">**MPSOURCE**</span></span>](mpsource.md)
</dt> <dt>

[<span data-ttu-id="e8b84-150">**estadísticas de MPTHREAT \_**</span><span class="sxs-lookup"><span data-stu-id="e8b84-150">**MPTHREAT\_STATS**</span></span>](mpthreat-stats.md)
</dt> </dl>

 

 





