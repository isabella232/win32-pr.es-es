---
description: Esta estructura contiene datos para los informes de presión de memoria.
ms.assetid: 42cf0922-53cc-48b9-8359-b88583ef5f1c
title: Estructura D3DMEMORYPRESSURE (D3d9types. h) para Microsoft Media Foundation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DMEMORYPRESSURE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 7400c4822b61a84ab288f0424cfa84e825e69dc9
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/02/2021
ms.locfileid: "106188030"
---
# <a name="d3dmemorypressure-structure-d3d9typesh-for-microsoft-media-foundation"></a><span data-ttu-id="69db2-103">Estructura D3DMEMORYPRESSURE (D3d9types. h) para Microsoft Media Foundation</span><span class="sxs-lookup"><span data-stu-id="69db2-103">D3DMEMORYPRESSURE structure (D3d9types.h) for Microsoft Media Foundation</span></span>

<span data-ttu-id="69db2-104">Contiene datos de informes de presión de memoria.</span><span class="sxs-lookup"><span data-stu-id="69db2-104">Contains data for memory pressure reporting.</span></span>

## <a name="syntax"></a><span data-ttu-id="69db2-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="69db2-105">Syntax</span></span>


```C++
typedef struct _D3DMEMORYPRESSURE {
  UINT64 BytesEvictedFromProcess;
  UINT64 SizeOfInefficientAllocation;
  DWORD  LevelOfEfficiency;
} D3DMEMORYPRESSURE;
```



## <a name="members"></a><span data-ttu-id="69db2-106">Members</span><span class="sxs-lookup"><span data-stu-id="69db2-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="69db2-107">**BytesEvictedFromProcess**</span><span class="sxs-lookup"><span data-stu-id="69db2-107">**BytesEvictedFromProcess**</span></span>
</dt> <dd>

<span data-ttu-id="69db2-108">Número de bytes expulsados por el proceso durante la ejecución de la consulta.</span><span class="sxs-lookup"><span data-stu-id="69db2-108">The number of bytes that were evicted by the process during the duration of the query.</span></span>

</dd> <dt>

<span data-ttu-id="69db2-109">**SizeOfInefficientAllocation**</span><span class="sxs-lookup"><span data-stu-id="69db2-109">**SizeOfInefficientAllocation**</span></span>
</dt> <dd>

<span data-ttu-id="69db2-110">Número total de bytes colocados en segmentos de memoria no óptimos debido a un espacio inadecuado dentro de los segmentos de memoria preferidos.</span><span class="sxs-lookup"><span data-stu-id="69db2-110">The total number of bytes placed in nonoptimal memory segments, due to inadequate space within the preferred memory segments.</span></span>

</dd> <dt>

<span data-ttu-id="69db2-111">**LevelOfEfficiency**</span><span class="sxs-lookup"><span data-stu-id="69db2-111">**LevelOfEfficiency**</span></span>
</dt> <dd>

<span data-ttu-id="69db2-112">La eficiencia general de las asignaciones de memoria que se colocaron en memoria no óptima.</span><span class="sxs-lookup"><span data-stu-id="69db2-112">The overall efficiency of the memory allocations that were placed in nonoptimal memory.</span></span> <span data-ttu-id="69db2-113">El valor se expresa como un porcentaje.</span><span class="sxs-lookup"><span data-stu-id="69db2-113">The value is expressed as a percentage.</span></span> <span data-ttu-id="69db2-114">Por ejemplo, el valor 95 indica que las asignaciones colocadas en segmentos de memoria no preferidos son un 95% eficaz.</span><span class="sxs-lookup"><span data-stu-id="69db2-114">For example, the value 95 indicates that the allocations placed in nonpreferred memory segments are 95% efficient.</span></span> <span data-ttu-id="69db2-115">Este número no se debe considerar una medida exacta.</span><span class="sxs-lookup"><span data-stu-id="69db2-115">This number should not be considered an exact measurement.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="69db2-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="69db2-116">Requirements</span></span>



| <span data-ttu-id="69db2-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="69db2-117">Requirement</span></span> | <span data-ttu-id="69db2-118">Value</span><span class="sxs-lookup"><span data-stu-id="69db2-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="69db2-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="69db2-119">Minimum supported client</span></span> | <span data-ttu-id="69db2-120">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="69db2-120">Windows 7 \[desktop apps only\]</span></span>                                                              |
| <span data-ttu-id="69db2-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="69db2-121">Minimum supported server</span></span> | <span data-ttu-id="69db2-122">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="69db2-122">Windows Server 2008 R2 \[desktop apps only\]</span></span>                                                 |
| <span data-ttu-id="69db2-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="69db2-123">Header</span></span>                  | <span data-ttu-id="69db2-124">D3d9types. h (incluye d3d9. h)</span><span class="sxs-lookup"><span data-stu-id="69db2-124">D3d9types.h (include D3d9.h)</span></span> |



## <a name="see-also"></a><span data-ttu-id="69db2-125">Consulte también</span><span class="sxs-lookup"><span data-stu-id="69db2-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69db2-126">Estructuras de vídeo de Direct3D</span><span class="sxs-lookup"><span data-stu-id="69db2-126">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="69db2-127">Informes de presión de memoria</span><span class="sxs-lookup"><span data-stu-id="69db2-127">Memory Pressure Reporting</span></span>](memory-pressure-reporting.md)
</dt> </dl>

 

 




