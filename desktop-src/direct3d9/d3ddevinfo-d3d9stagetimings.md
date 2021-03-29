---
description: Porcentaje de tiempo de procesamiento de datos de sombreador.
ms.assetid: 388bb943-c25f-4b50-b7e4-d6259f1186c2
title: D3DDEVINFO_D3D9STAGETIMINGS estructura (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVINFO_D3D9STAGETIMINGS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: cf8c9522decfcbb09a60aff0bee65ca05a0f5eeb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105678781"
---
# <a name="d3ddevinfo_d3d9stagetimings-structure"></a><span data-ttu-id="6d460-103">D3DDEVINFO \_ estructura D3D9STAGETIMINGS</span><span class="sxs-lookup"><span data-stu-id="6d460-103">D3DDEVINFO\_D3D9STAGETIMINGS structure</span></span>

<span data-ttu-id="6d460-104">Porcentaje de tiempo de procesamiento de datos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="6d460-104">Percent of time processing shader data.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d460-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6d460-105">Syntax</span></span>


```C++
typedef struct D3DDEVINFO_D3D9STAGETIMINGS {
  FLOAT MemoryProcessingPercent;
  FLOAT ComputationProcessingPercent;
} D3DDEVINFO_D3D9STAGETIMINGS, *LPD3DDEVINFO_D3D9STAGETIMINGS;
```



## <a name="members"></a><span data-ttu-id="6d460-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="6d460-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="6d460-107">**MemoryProcessingPercent**</span><span class="sxs-lookup"><span data-stu-id="6d460-107">**MemoryProcessingPercent**</span></span>
</dt> <dd>

<span data-ttu-id="6d460-108">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6d460-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="6d460-109">Porcentaje de tiempo en el sombreador empleado en el acceso a la memoria.</span><span class="sxs-lookup"><span data-stu-id="6d460-109">Percent of time in shader spent on memory accesses.</span></span>

</dd> <dt>

<span data-ttu-id="6d460-110">**ComputationProcessingPercent**</span><span class="sxs-lookup"><span data-stu-id="6d460-110">**ComputationProcessingPercent**</span></span>
</dt> <dd>

<span data-ttu-id="6d460-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6d460-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="6d460-112">Porcentaje de tiempo de procesamiento (movimiento de datos en registros o en operaciones matemáticas).</span><span class="sxs-lookup"><span data-stu-id="6d460-112">Percent of time processing (moving data around in registers or doing mathematical operations).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6d460-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6d460-113">Remarks</span></span>

<span data-ttu-id="6d460-114">Para obtener el mejor rendimiento, se recomienda una carga equilibrada.</span><span class="sxs-lookup"><span data-stu-id="6d460-114">For best performance, a balanced load is recommended.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d460-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6d460-115">Requirements</span></span>



| <span data-ttu-id="6d460-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="6d460-116">Requirement</span></span> | <span data-ttu-id="6d460-117">Value</span><span class="sxs-lookup"><span data-stu-id="6d460-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6d460-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6d460-118">Header</span></span><br/> | <dl> <span data-ttu-id="6d460-119"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="6d460-119"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6d460-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="6d460-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d460-121">Estructuras de Direct3D</span><span class="sxs-lookup"><span data-stu-id="6d460-121">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="6d460-122">**GetData**</span><span class="sxs-lookup"><span data-stu-id="6d460-122">**GetData**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata)
</dt> </dl>

 

 
