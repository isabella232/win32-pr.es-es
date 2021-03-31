---
title: Enumeración MPTHREAT_DETECTION (MpClient. h)
description: Posibles tipos conocidos de detección de amenazas defectuosas.
ms.assetid: 14FCA9BD-A9A1-488B-B8E8-88DE0DF18F27
keywords:
- MPTHREAT_DETECTION enumeración características de entorno heredado de Windows
- PMPTHREAT_DETECTION el puntero de enumeración características de entorno heredado de Windows
topic_type:
- apiref
api_name:
- MPTHREAT_DETECTION
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86edc0e1ca4ee130f2a2a4a678447771f1ae40ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801904"
---
# <a name="mpthreat_detection-enumeration"></a><span data-ttu-id="44ffb-105">\_Enumeración de detección MPTHREAT</span><span class="sxs-lookup"><span data-stu-id="44ffb-105">MPTHREAT\_DETECTION enumeration</span></span>

<span data-ttu-id="44ffb-106">Posibles tipos conocidos de detección de amenazas defectuosas.</span><span class="sxs-lookup"><span data-stu-id="44ffb-106">Possible known bad threat detection types.</span></span>

## <a name="syntax"></a><span data-ttu-id="44ffb-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="44ffb-107">Syntax</span></span>


```C++
typedef enum tagMPTHREAT_DETECTION { 
  MP_THREAT_DETECTION_CONCRETE    = 0,
  MP_THREAT_DETECTION_HEURISTIC   = 1,
  MP_THREAT_DETECTION_GENERIC     = 2,
  MP_THREAT_DETECTION_SUSPICIOUS  = 4,
  MP_THREAT_DETECTION_FASTPATH    = 8
} MPTHREAT_DETECTION, *PMPTHREAT_DETECTION;
```



## <a name="constants"></a><span data-ttu-id="44ffb-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="44ffb-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="44ffb-109"><span id="MP_THREAT_DETECTION_CONCRETE"></span><span id="mp_threat_detection_concrete"></span>**\_específico de \_ detección de amenazas de MP \_**</span><span class="sxs-lookup"><span data-stu-id="44ffb-109"><span id="MP_THREAT_DETECTION_CONCRETE"></span><span id="mp_threat_detection_concrete"></span>**MP\_THREAT\_DETECTION\_CONCRETE**</span></span>
</dt> <dd>

<span data-ttu-id="44ffb-110">Se detectó una amenaza a través de firmas concretas.</span><span class="sxs-lookup"><span data-stu-id="44ffb-110">Threat was detected via concrete signatures.</span></span>

</dd> <dt>

<span data-ttu-id="44ffb-111"><span id="MP_THREAT_DETECTION_HEURISTIC"></span><span id="mp_threat_detection_heuristic"></span>**\_heurística de \_ detección de amenazas MP \_**</span><span class="sxs-lookup"><span data-stu-id="44ffb-111"><span id="MP_THREAT_DETECTION_HEURISTIC"></span><span id="mp_threat_detection_heuristic"></span>**MP\_THREAT\_DETECTION\_HEURISTIC**</span></span>
</dt> <dd>

<span data-ttu-id="44ffb-112">Se detectó una amenaza a través de la heurística.</span><span class="sxs-lookup"><span data-stu-id="44ffb-112">Threat was detected via heuristic.</span></span>

</dd> <dt>

<span data-ttu-id="44ffb-113"><span id="MP_THREAT_DETECTION_GENERIC"></span><span id="mp_threat_detection_generic"></span>**\_ \_ Generic detección de amenazas de MP \_**</span><span class="sxs-lookup"><span data-stu-id="44ffb-113"><span id="MP_THREAT_DETECTION_GENERIC"></span><span id="mp_threat_detection_generic"></span>**MP\_THREAT\_DETECTION\_GENERIC**</span></span>
</dt> <dd>

<span data-ttu-id="44ffb-114">Se detectó una amenaza mediante firmas genéricas.</span><span class="sxs-lookup"><span data-stu-id="44ffb-114">Threat was detected via generic signatures.</span></span>

</dd> <dt>

<span data-ttu-id="44ffb-115"><span id="MP_THREAT_DETECTION_SUSPICIOUS"></span><span id="mp_threat_detection_suspicious"></span>**detección de amenazas de MP \_ \_ \_ sospechosa**</span><span class="sxs-lookup"><span data-stu-id="44ffb-115"><span id="MP_THREAT_DETECTION_SUSPICIOUS"></span><span id="mp_threat_detection_suspicious"></span>**MP\_THREAT\_DETECTION\_SUSPICIOUS**</span></span>
</dt> <dd>

<span data-ttu-id="44ffb-116">Se detectó una amenaza a través de la supervisión del comportamiento.</span><span class="sxs-lookup"><span data-stu-id="44ffb-116">Threat was detected via behavior monitoring.</span></span>

</dd> <dt>

<span data-ttu-id="44ffb-117"><span id="MP_THREAT_DETECTION_FASTPATH"></span><span id="mp_threat_detection_fastpath"></span>**detección de amenazas de MP \_ \_ \_ FASTPATH**</span><span class="sxs-lookup"><span data-stu-id="44ffb-117"><span id="MP_THREAT_DETECTION_FASTPATH"></span><span id="mp_threat_detection_fastpath"></span>**MP\_THREAT\_DETECTION\_FASTPATH**</span></span>
</dt> <dd>

<span data-ttu-id="44ffb-118">Se detectó una amenaza a través de FastPATH.</span><span class="sxs-lookup"><span data-stu-id="44ffb-118">Threat was detected via fastpath.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="44ffb-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="44ffb-119">Requirements</span></span>



| <span data-ttu-id="44ffb-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="44ffb-120">Requirement</span></span> | <span data-ttu-id="44ffb-121">Value</span><span class="sxs-lookup"><span data-stu-id="44ffb-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="44ffb-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="44ffb-122">Minimum supported client</span></span><br/> | <span data-ttu-id="44ffb-123">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="44ffb-123">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="44ffb-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="44ffb-124">Minimum supported server</span></span><br/> | <span data-ttu-id="44ffb-125">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="44ffb-125">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="44ffb-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="44ffb-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="44ffb-127"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="44ffb-127"><dt>MpClient.h</dt></span></span> </dl> |



 

 





