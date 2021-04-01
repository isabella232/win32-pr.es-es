---
title: MPTHREAT_STATS estructura (MpClient. h)
description: Estadísticas relacionadas con amenazas.
ms.assetid: 78B7E2A8-1BB4-4610-8E90-1F8ECBE740A8
keywords:
- MPTHREAT_STATS estructura de las características heredadas del entorno de Windows
- Puntero de estructura de PMPTHREAT_STATS características de entorno heredado de Windows
topic_type:
- apiref
api_name:
- MPTHREAT_STATS
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21a2eef7acde5fbeac2cf9951dfad3e6923ccea2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905208"
---
# <a name="mpthreat_stats-structure"></a><span data-ttu-id="70c82-105">MPTHREAT ( \_ estructura de estadísticas)</span><span class="sxs-lookup"><span data-stu-id="70c82-105">MPTHREAT\_STATS structure</span></span>

<span data-ttu-id="70c82-106">Estadísticas relacionadas con amenazas.</span><span class="sxs-lookup"><span data-stu-id="70c82-106">Threat-related statistics.</span></span>

## <a name="syntax"></a><span data-ttu-id="70c82-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="70c82-107">Syntax</span></span>


```C++
typedef struct tagMPTHREAT_STATS {
  UINT ThreatCount;
  UINT SuspiciousThreatCount;
  UINT Reserved[4];
} MPTHREAT_STATS, *PMPTHREAT_STATS;
```



## <a name="members"></a><span data-ttu-id="70c82-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="70c82-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="70c82-109">**ThreatCount**</span><span class="sxs-lookup"><span data-stu-id="70c82-109">**ThreatCount**</span></span>
</dt> <dd>

<span data-ttu-id="70c82-110">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="70c82-110">Type: **UINT**</span></span>

</dd> <dd>

<span data-ttu-id="70c82-111">Número de amenazas detectadas.</span><span class="sxs-lookup"><span data-stu-id="70c82-111">Number of threats detected.</span></span>

</dd> <dt>

<span data-ttu-id="70c82-112">**SuspiciousThreatCount**</span><span class="sxs-lookup"><span data-stu-id="70c82-112">**SuspiciousThreatCount**</span></span>
</dt> <dd>

<span data-ttu-id="70c82-113">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="70c82-113">Type: **UINT**</span></span>

</dd> <dd>

<span data-ttu-id="70c82-114">Número de amenazas detectadas con supervisión de comportamiento.</span><span class="sxs-lookup"><span data-stu-id="70c82-114">Number of threats detected with behavior monitoring.</span></span>

</dd> <dt>

<span data-ttu-id="70c82-115">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="70c82-115">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="70c82-116">Tipo: **uint \[ 4 \]**</span><span class="sxs-lookup"><span data-stu-id="70c82-116">Type: **UINT\[4\]**</span></span>

</dd> <dd>

<span data-ttu-id="70c82-117">Campos reservados para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="70c82-117">Fields reserved for future use.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="70c82-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="70c82-118">Requirements</span></span>



| <span data-ttu-id="70c82-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="70c82-119">Requirement</span></span> | <span data-ttu-id="70c82-120">Value</span><span class="sxs-lookup"><span data-stu-id="70c82-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="70c82-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="70c82-121">Minimum supported client</span></span><br/> | <span data-ttu-id="70c82-122">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="70c82-122">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="70c82-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="70c82-123">Minimum supported server</span></span><br/> | <span data-ttu-id="70c82-124">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="70c82-124">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="70c82-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="70c82-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="70c82-126"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="70c82-126"><dt>MpClient.h</dt></span></span> </dl> |



 

 





