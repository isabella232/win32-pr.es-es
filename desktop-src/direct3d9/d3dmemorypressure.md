---
description: Contiene datos de informes de presión de memoria.
ms.assetid: bdf65d35-281f-4795-a2c1-0d4e91bfa7bc
title: Estructura D3DMEMORYPRESSURE (D3d9types. h)
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
ms.openlocfilehash: 5917d1e61817f401106ae14aa5a0f98cd75b0d42
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718275"
---
# <a name="d3dmemorypressure-structure-d3d9typesh"></a><span data-ttu-id="f6556-103">Estructura D3DMEMORYPRESSURE (D3d9types. h)</span><span class="sxs-lookup"><span data-stu-id="f6556-103">D3DMEMORYPRESSURE structure (D3d9types.h)</span></span>

<span data-ttu-id="f6556-104">Contiene datos de informes de presión de memoria.</span><span class="sxs-lookup"><span data-stu-id="f6556-104">Contains data for memory pressure reporting.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6556-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f6556-105">Syntax</span></span>


```C++
typedef struct _D3DMEMORYPRESSURE {
  UINT64 BytesEvictedFromProcess;
  UINT64 SizeOfInefficientAllocation;
  DWORD  LevelOfEfficiency;
} D3DMEMORYPRESSURE;
```



## <a name="members"></a><span data-ttu-id="f6556-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="f6556-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="f6556-107">**BytesEvictedFromProcess**</span><span class="sxs-lookup"><span data-stu-id="f6556-107">**BytesEvictedFromProcess**</span></span>
</dt> <dd>

<span data-ttu-id="f6556-108">Tipo: **[ **UINT64**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f6556-108">Type: **[**UINT64**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f6556-109">Número de bytes expulsados por el proceso durante la ejecución de la consulta.</span><span class="sxs-lookup"><span data-stu-id="f6556-109">The number of bytes that were evicted by the process during the duration of the query.</span></span>

</dd> <dt>

<span data-ttu-id="f6556-110">**SizeOfInefficientAllocation**</span><span class="sxs-lookup"><span data-stu-id="f6556-110">**SizeOfInefficientAllocation**</span></span>
</dt> <dd>

<span data-ttu-id="f6556-111">Tipo: **[ **UINT64**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f6556-111">Type: **[**UINT64**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f6556-112">Número total de bytes colocados en segmentos de memoria no óptimos debido a un espacio inadecuado dentro de los segmentos de memoria preferidos.</span><span class="sxs-lookup"><span data-stu-id="f6556-112">The total number of bytes placed in nonoptimal memory segments, due to inadequate space within the preferred memory segments.</span></span>

</dd> <dt>

<span data-ttu-id="f6556-113">**LevelOfEfficiency**</span><span class="sxs-lookup"><span data-stu-id="f6556-113">**LevelOfEfficiency**</span></span>
</dt> <dd>

<span data-ttu-id="f6556-114">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f6556-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f6556-115">La eficiencia general de las asignaciones de memoria que se colocaron en memoria no óptima.</span><span class="sxs-lookup"><span data-stu-id="f6556-115">The overall efficiency of the memory allocations that were placed in nonoptimal memory.</span></span> <span data-ttu-id="f6556-116">El valor se expresa como un porcentaje.</span><span class="sxs-lookup"><span data-stu-id="f6556-116">The value is expressed as a percentage.</span></span> <span data-ttu-id="f6556-117">Por ejemplo, el valor 95 indica que las asignaciones colocadas en segmentos de memoria no preferidos son un 95% eficaz.</span><span class="sxs-lookup"><span data-stu-id="f6556-117">For example, the value 95 indicates that the allocations placed in nonpreferred memory segments are 95% efficient.</span></span> <span data-ttu-id="f6556-118">Este número no se debe considerar una medida exacta.</span><span class="sxs-lookup"><span data-stu-id="f6556-118">This number should not be considered an exact measurement.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f6556-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f6556-119">Requirements</span></span>



| <span data-ttu-id="f6556-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="f6556-120">Requirement</span></span> | <span data-ttu-id="f6556-121">Value</span><span class="sxs-lookup"><span data-stu-id="f6556-121">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f6556-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f6556-122">Header</span></span><br/> | <dl> <span data-ttu-id="f6556-123"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="f6556-123"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f6556-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="f6556-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6556-125">Estructuras de Direct3D</span><span class="sxs-lookup"><span data-stu-id="f6556-125">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
