---
title: MPSCAN_DATA estructura (MpClient. h)
description: Examinar los datos pasados a la devolución de llamada.
ms.assetid: 6C9AAF1E-7566-43EE-A100-5112E9B8878C
keywords:
- MPSCAN_DATA estructura de las características heredadas del entorno de Windows
- Puntero de estructura de PMPSCAN_DATA características de entorno heredado de Windows
topic_type:
- apiref
api_name:
- MPSCAN_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e78508313f102e2baad19cf359a5c3a7c172db0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493060"
---
# <a name="mpscan_data-structure"></a><span data-ttu-id="8aca8-105">\_Estructura de datos MPSCAN</span><span class="sxs-lookup"><span data-stu-id="8aca8-105">MPSCAN\_DATA structure</span></span>

<span data-ttu-id="8aca8-106">Examinar los datos pasados a la devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="8aca8-106">Scan data passed to the callback.</span></span>

<span data-ttu-id="8aca8-107">Esta estructura contiene estadísticas acumuladas de recursos y amenazas.</span><span class="sxs-lookup"><span data-stu-id="8aca8-107">This structure contains cumulative threat and resource statistics.</span></span> <span data-ttu-id="8aca8-108">Estos campos de STAT siempre son válidos.</span><span class="sxs-lookup"><span data-stu-id="8aca8-108">These stat fields are always valid.</span></span>

## <a name="syntax"></a><span data-ttu-id="8aca8-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8aca8-109">Syntax</span></span>


```C++
typedef struct tagMPSCAN_DATA {
  MPSCAN_TYPE      ScanType;
  PMPRESOURCE_INFO ResourceInfo;
  MPRESOURCE_STATS ResourceStats;
  MPTHREAT_STATS   ThreatStats;
} MPSCAN_DATA, *PMPSCAN_DATA;
```



## <a name="members"></a><span data-ttu-id="8aca8-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="8aca8-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="8aca8-111">**ScanType**</span><span class="sxs-lookup"><span data-stu-id="8aca8-111">**ScanType**</span></span>
</dt> <dd>

<span data-ttu-id="8aca8-112">Tipo: **[ **MPSCAN \_ Type**](mpscan-type.md)**</span><span class="sxs-lookup"><span data-stu-id="8aca8-112">Type: **[**MPSCAN\_TYPE**](mpscan-type.md)**</span></span>

</dd> <dd>

<span data-ttu-id="8aca8-113">Tipo de examen.</span><span class="sxs-lookup"><span data-stu-id="8aca8-113">Scan type.</span></span>

</dd> <dt>

<span data-ttu-id="8aca8-114">**ResourceInfo**</span><span class="sxs-lookup"><span data-stu-id="8aca8-114">**ResourceInfo**</span></span>
</dt> <dd>

<span data-ttu-id="8aca8-115">Tipo: **PMPRESOURCE \_ info**</span><span class="sxs-lookup"><span data-stu-id="8aca8-115">Type: **PMPRESOURCE\_INFO**</span></span>

</dd> <dd>

<span data-ttu-id="8aca8-116">Información de recursos.</span><span class="sxs-lookup"><span data-stu-id="8aca8-116">Resource information.</span></span> <span data-ttu-id="8aca8-117">Vea [**\_ información de MPRESOURCE**](mpresource-info.md).</span><span class="sxs-lookup"><span data-stu-id="8aca8-117">See [**MPRESOURCE\_INFO**](mpresource-info.md).</span></span>

</dd> <dt>

<span data-ttu-id="8aca8-118">**ResourceStats**</span><span class="sxs-lookup"><span data-stu-id="8aca8-118">**ResourceStats**</span></span>
</dt> <dd>

<span data-ttu-id="8aca8-119">Tipo: **[ **\_ estadísticas de MPRESOURCE**](mpresource-stats.md)**</span><span class="sxs-lookup"><span data-stu-id="8aca8-119">Type: **[**MPRESOURCE\_STATS**](mpresource-stats.md)**</span></span>

</dd> <dd>

<span data-ttu-id="8aca8-120">Estadísticas acumulativas relacionadas con recursos.</span><span class="sxs-lookup"><span data-stu-id="8aca8-120">Resource-related cumulative statistics.</span></span>

</dd> <dt>

<span data-ttu-id="8aca8-121">**ThreatStats**</span><span class="sxs-lookup"><span data-stu-id="8aca8-121">**ThreatStats**</span></span>
</dt> <dd>

<span data-ttu-id="8aca8-122">Tipo: **[ **\_ estadísticas de MPTHREAT**](mpthreat-stats.md)**</span><span class="sxs-lookup"><span data-stu-id="8aca8-122">Type: **[**MPTHREAT\_STATS**](mpthreat-stats.md)**</span></span>

</dd> <dd>

<span data-ttu-id="8aca8-123">Estadísticas de amenazas con finalizaciones de análisis correctas.</span><span class="sxs-lookup"><span data-stu-id="8aca8-123">Threat statistics with successful scan completions.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8aca8-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8aca8-124">Requirements</span></span>



| <span data-ttu-id="8aca8-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="8aca8-125">Requirement</span></span> | <span data-ttu-id="8aca8-126">Value</span><span class="sxs-lookup"><span data-stu-id="8aca8-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8aca8-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8aca8-127">Minimum supported client</span></span><br/> | <span data-ttu-id="8aca8-128">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="8aca8-128">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="8aca8-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8aca8-129">Minimum supported server</span></span><br/> | <span data-ttu-id="8aca8-130">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="8aca8-130">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8aca8-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8aca8-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="8aca8-132"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="8aca8-132"><dt>MpClient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8aca8-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="8aca8-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8aca8-134">**información de MPRESOURCE \_**</span><span class="sxs-lookup"><span data-stu-id="8aca8-134">**MPRESOURCE\_INFO**</span></span>](mpresource-info.md)
</dt> <dt>

[<span data-ttu-id="8aca8-135">**estadísticas de MPRESOURCE \_**</span><span class="sxs-lookup"><span data-stu-id="8aca8-135">**MPRESOURCE\_STATS**</span></span>](mpresource-stats.md)
</dt> <dt>

[<span data-ttu-id="8aca8-136">**\_tipo MPSCAN**</span><span class="sxs-lookup"><span data-stu-id="8aca8-136">**MPSCAN\_TYPE**</span></span>](mpscan-type.md)
</dt> <dt>

[<span data-ttu-id="8aca8-137">**estadísticas de MPTHREAT \_**</span><span class="sxs-lookup"><span data-stu-id="8aca8-137">**MPTHREAT\_STATS**</span></span>](mpthreat-stats.md)
</dt> </dl>

 

 





