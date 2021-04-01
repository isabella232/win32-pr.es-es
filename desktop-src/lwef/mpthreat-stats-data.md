---
title: MPTHREAT_STATS_DATA estructura (MpClient. h)
description: Datos adicionales de estadísticas de amenazas.
ms.assetid: 8C01C746-8FD8-4311-908D-D1F4E3488480
keywords:
- MPTHREAT_STATS_DATA estructura de las características heredadas del entorno de Windows
- Puntero de estructura de PMPTHREAT_STATS_DATA características de entorno heredado de Windows
topic_type:
- apiref
api_name:
- MPTHREAT_STATS_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9525ddcfc580e9a82ffdb191d20e3748f7a1e16
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150233"
---
# <a name="mpthreat_stats_data-structure"></a><span data-ttu-id="97386-105">Estructura de datos de \_ estadísticas de MPTHREAT \_</span><span class="sxs-lookup"><span data-stu-id="97386-105">MPTHREAT\_STATS\_DATA structure</span></span>

<span data-ttu-id="97386-106">Datos adicionales de estadísticas de amenazas.</span><span class="sxs-lookup"><span data-stu-id="97386-106">Additional threat statistics data.</span></span>

## <a name="syntax"></a><span data-ttu-id="97386-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="97386-107">Syntax</span></span>


```C++
typedef struct tagMPTHREAT_STATS_DATA {
  DWORD dwThreatCount;
} MPTHREAT_STATS_DATA, *PMPTHREAT_STATS_DATA;
```



## <a name="members"></a><span data-ttu-id="97386-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="97386-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="97386-109">**dwThreatCount**</span><span class="sxs-lookup"><span data-stu-id="97386-109">**dwThreatCount**</span></span>
</dt> <dd>

<span data-ttu-id="97386-110">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="97386-110">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="97386-111">Número de amenazas.</span><span class="sxs-lookup"><span data-stu-id="97386-111">Number of threats.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="97386-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="97386-112">Requirements</span></span>



| <span data-ttu-id="97386-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="97386-113">Requirement</span></span> | <span data-ttu-id="97386-114">Value</span><span class="sxs-lookup"><span data-stu-id="97386-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="97386-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="97386-115">Minimum supported client</span></span><br/> | <span data-ttu-id="97386-116">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="97386-116">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="97386-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="97386-117">Minimum supported server</span></span><br/> | <span data-ttu-id="97386-118">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="97386-118">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="97386-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="97386-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="97386-120"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="97386-120"><dt>MpClient.h</dt></span></span> </dl> |



 

 





