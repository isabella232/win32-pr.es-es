---
title: MPSTATUS_INFO estructura (MpClient. h)
description: Información de estado para el administrador de protección contra malware de.
ms.assetid: 614F14EC-64CC-4E3F-8A89-42AA1E0DC95D
keywords:
- MPSTATUS_INFO estructura de las características heredadas del entorno de Windows
- Puntero de estructura de PMPSTATUS_INFO características de entorno heredado de Windows
topic_type:
- apiref
api_name:
- MPSTATUS_INFO
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efe31981f819d85d13457553beb1ce3c869b98bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801249"
---
# <a name="mpstatus_info-structure"></a><span data-ttu-id="d123f-105">Estructura de información de MPSTATUS \_</span><span class="sxs-lookup"><span data-stu-id="d123f-105">MPSTATUS\_INFO structure</span></span>

<span data-ttu-id="d123f-106">Información de estado para el administrador de protección contra malware de.</span><span class="sxs-lookup"><span data-stu-id="d123f-106">Status information for the malware protection manager.</span></span>

## <a name="syntax"></a><span data-ttu-id="d123f-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d123f-107">Syntax</span></span>


```C++
typedef struct tagMPSTATUS_INFO {
  DWORD               ProductStatus;
  MPSCAN_RESULT       LastQuickScan;
  MPSCAN_RESULT       LastFullScan;
  MPTHREAT_STATS      ThreatStats;
  MPTHREAT_STATS_DATA ThreatState[MP_THREAT_STAT_MAX_VALUE+1];
  MPCOMPONENT_STATUS  Component[MPCOMPONENT_MAXVALUE+1];
  ULARGE_INTEGER      ProductExpirationTime;
} MPSTATUS_INFO, *PMPSTATUS_INFO;
```



## <a name="members"></a><span data-ttu-id="d123f-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="d123f-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="d123f-109">**ProductStatus**</span><span class="sxs-lookup"><span data-stu-id="d123f-109">**ProductStatus**</span></span>
</dt> <dd>

<span data-ttu-id="d123f-110">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="d123f-110">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="d123f-111">Estado general del producto.</span><span class="sxs-lookup"><span data-stu-id="d123f-111">Overall product status.</span></span> <span data-ttu-id="d123f-112">Se trata de una combinación de marcas de bits de la [**\_ marca MPSTATUS**](mpstatus-flag.md).</span><span class="sxs-lookup"><span data-stu-id="d123f-112">This is a combination of bit flags from [**MPSTATUS\_FLAG**](mpstatus-flag.md).</span></span>

</dd> <dt>

<span data-ttu-id="d123f-113">**LastQuickScan**</span><span class="sxs-lookup"><span data-stu-id="d123f-113">**LastQuickScan**</span></span>
</dt> <dd>

<span data-ttu-id="d123f-114">Tipo: **[ **\_ resultado de MPSCAN**](mpscan-result.md)**</span><span class="sxs-lookup"><span data-stu-id="d123f-114">Type: **[**MPSCAN\_RESULT**](mpscan-result.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d123f-115">Resultados del último examen por parte del administrador de protección contra malware de.</span><span class="sxs-lookup"><span data-stu-id="d123f-115">Results of the last scan by the malware protection manager.</span></span> <span data-ttu-id="d123f-116">Vea [**el \_ resultado de MPSCAN**](mpscan-result.md).</span><span class="sxs-lookup"><span data-stu-id="d123f-116">See [**MPSCAN\_RESULT**](mpscan-result.md).</span></span>

</dd> <dt>

<span data-ttu-id="d123f-117">**LastFullScan**</span><span class="sxs-lookup"><span data-stu-id="d123f-117">**LastFullScan**</span></span>
</dt> <dd>

<span data-ttu-id="d123f-118">Tipo: **[ **\_ resultado de MPSCAN**](mpscan-result.md)**</span><span class="sxs-lookup"><span data-stu-id="d123f-118">Type: **[**MPSCAN\_RESULT**](mpscan-result.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d123f-119">Resultados del último examen completo por parte del administrador de protección contra malware.</span><span class="sxs-lookup"><span data-stu-id="d123f-119">Results of the last full scan by the malware protection manager.</span></span> <span data-ttu-id="d123f-120">Vea [**el \_ resultado de MPSCAN**](mpscan-result.md).</span><span class="sxs-lookup"><span data-stu-id="d123f-120">See [**MPSCAN\_RESULT**](mpscan-result.md).</span></span>

</dd> <dt>

<span data-ttu-id="d123f-121">**ThreatStats**</span><span class="sxs-lookup"><span data-stu-id="d123f-121">**ThreatStats**</span></span>
</dt> <dd>

<span data-ttu-id="d123f-122">Tipo: **[ **\_ estadísticas de MPTHREAT**](mpthreat-stats.md)**</span><span class="sxs-lookup"><span data-stu-id="d123f-122">Type: **[**MPTHREAT\_STATS**](mpthreat-stats.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d123f-123">Estadísticas de amenazas activas.</span><span class="sxs-lookup"><span data-stu-id="d123f-123">Active threat statistics.</span></span> <span data-ttu-id="d123f-124">Consulte [**\_ estadísticas de MPTHREAT**](mpthreat-stats.md).</span><span class="sxs-lookup"><span data-stu-id="d123f-124">See [**MPTHREAT\_STATS**](mpthreat-stats.md).</span></span>

</dd> <dt>

<span data-ttu-id="d123f-125">**ThreatState**</span><span class="sxs-lookup"><span data-stu-id="d123f-125">**ThreatState**</span></span>
</dt> <dd>

<span data-ttu-id="d123f-126">Type: **[**MPTHREAT \_ stats \_ Data**](mpthreat-stats-data.md) \[ MP \_ Threat \_ STAT \_ Max \_ Value + 1\]**</span><span class="sxs-lookup"><span data-stu-id="d123f-126">Type: **[**MPTHREAT\_STATS\_DATA**](mpthreat-stats-data.md)\[MP\_THREAT\_STAT\_MAX\_VALUE+1\]**</span></span>

</dd> <dd>

<span data-ttu-id="d123f-127">Datos adicionales de estadísticas de amenazas, como el número de amenazas.</span><span class="sxs-lookup"><span data-stu-id="d123f-127">Additional threat statistics data, such as the number of threats.</span></span> <span data-ttu-id="d123f-128">Consulte [**\_ \_ datos de estadísticas de MPTHREAT**](mpthreat-stats-data.md).</span><span class="sxs-lookup"><span data-stu-id="d123f-128">See [**MPTHREAT\_STATS\_DATA**](mpthreat-stats-data.md).</span></span>

</dd> <dt>

<span data-ttu-id="d123f-129">**Componente**</span><span class="sxs-lookup"><span data-stu-id="d123f-129">**Component**</span></span>
</dt> <dd>

<span data-ttu-id="d123f-130">Tipo: **[**MPCOMPONENT \_ status**](mpcomponent-status.md) \[ MPCOMPONENT \_ MAXVALUE + 1\]**</span><span class="sxs-lookup"><span data-stu-id="d123f-130">Type: **[**MPCOMPONENT\_STATUS**](mpcomponent-status.md)\[MPCOMPONENT\_MAXVALUE+1\]**</span></span>

</dd> <dd>

<span data-ttu-id="d123f-131">Una matriz de Estados para varios componentes.</span><span class="sxs-lookup"><span data-stu-id="d123f-131">An array of statuses for multiple components.</span></span> <span data-ttu-id="d123f-132">Use un valor de la enumeración [**MPCOMPONENT \_ ID**](mpcomponent-id.md) como un índice en la matriz.</span><span class="sxs-lookup"><span data-stu-id="d123f-132">Use a value from the [**MPCOMPONENT\_ID**](mpcomponent-id.md) enumeration as an index into the array.</span></span>

</dd> <dt>

<span data-ttu-id="d123f-133">**ProductExpirationTime**</span><span class="sxs-lookup"><span data-stu-id="d123f-133">**ProductExpirationTime**</span></span>
</dt> <dd>

<span data-ttu-id="d123f-134">Tipo: **ULARGE \_ Integer**</span><span class="sxs-lookup"><span data-stu-id="d123f-134">Type: **ULARGE\_INTEGER**</span></span>

</dd> <dd>

<span data-ttu-id="d123f-135">Marca de tiempo de expiración del producto en UNC.</span><span class="sxs-lookup"><span data-stu-id="d123f-135">Product expiration timestamp in UNC.</span></span> <span data-ttu-id="d123f-136">Esto solo es válido si se ha establecido el estado de expiración.</span><span class="sxs-lookup"><span data-stu-id="d123f-136">This is valid only if the expiration status is set.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d123f-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d123f-137">Requirements</span></span>



| <span data-ttu-id="d123f-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="d123f-138">Requirement</span></span> | <span data-ttu-id="d123f-139">Value</span><span class="sxs-lookup"><span data-stu-id="d123f-139">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d123f-140">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d123f-140">Minimum supported client</span></span><br/> | <span data-ttu-id="d123f-141">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="d123f-141">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="d123f-142">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d123f-142">Minimum supported server</span></span><br/> | <span data-ttu-id="d123f-143">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="d123f-143">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d123f-144">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d123f-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="d123f-145"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="d123f-145"><dt>MpClient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d123f-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="d123f-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d123f-147">**identificador de MPCOMPONENT \_**</span><span class="sxs-lookup"><span data-stu-id="d123f-147">**MPCOMPONENT\_ID**</span></span>](mpcomponent-id.md)
</dt> <dt>

[<span data-ttu-id="d123f-148">**Estado de MPCOMPONENT \_**</span><span class="sxs-lookup"><span data-stu-id="d123f-148">**MPCOMPONENT\_STATUS**</span></span>](mpcomponent-status.md)
</dt> <dt>

[<span data-ttu-id="d123f-149">**resultado de MPSCAN \_**</span><span class="sxs-lookup"><span data-stu-id="d123f-149">**MPSCAN\_RESULT**</span></span>](mpscan-result.md)
</dt> <dt>

[<span data-ttu-id="d123f-150">**\_marca MPSTATUS**</span><span class="sxs-lookup"><span data-stu-id="d123f-150">**MPSTATUS\_FLAG**</span></span>](mpstatus-flag.md)
</dt> <dt>

[<span data-ttu-id="d123f-151">**estadísticas de MPTHREAT \_**</span><span class="sxs-lookup"><span data-stu-id="d123f-151">**MPTHREAT\_STATS**</span></span>](mpthreat-stats.md)
</dt> <dt>

[<span data-ttu-id="d123f-152">**datos de estadísticas de MPTHREAT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d123f-152">**MPTHREAT\_STATS\_DATA**</span></span>](mpthreat-stats-data.md)
</dt> </dl>

 

 





