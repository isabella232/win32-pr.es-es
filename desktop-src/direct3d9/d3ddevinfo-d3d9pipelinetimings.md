---
description: Porcentaje de tiempo de procesamiento de datos en la canalización.
ms.assetid: eb9dec27-2e45-4897-92af-8415c8fa08d4
title: D3DDEVINFO_D3D9PIPELINETIMINGS estructura (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVINFO_D3D9PIPELINETIMINGS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 627eec0ea93181b14c308ab229ed603412511a91
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105678783"
---
# <a name="d3ddevinfo_d3d9pipelinetimings-structure"></a><span data-ttu-id="9ced8-103">D3DDEVINFO \_ estructura D3D9PIPELINETIMINGS</span><span class="sxs-lookup"><span data-stu-id="9ced8-103">D3DDEVINFO\_D3D9PIPELINETIMINGS structure</span></span>

<span data-ttu-id="9ced8-104">Porcentaje de tiempo de procesamiento de datos en la canalización.</span><span class="sxs-lookup"><span data-stu-id="9ced8-104">Percent of time processing data in the pipeline.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ced8-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9ced8-105">Syntax</span></span>


```C++
typedef struct D3DDEVINFO_D3D9PIPELINETIMINGS {
  FLOAT VertexProcessingTimePercent;
  FLOAT PixelProcessingTimePercent;
  FLOAT OtherGPUProcessingTimePercent;
  FLOAT GPUIdleTimePercent;
} D3DDEVINFO_D3D9PIPELINETIMINGS, *LPD3DDEVINFO_D3D9PIPELINETIMINGS;
```



## <a name="members"></a><span data-ttu-id="9ced8-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="9ced8-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="9ced8-107">**VertexProcessingTimePercent**</span><span class="sxs-lookup"><span data-stu-id="9ced8-107">**VertexProcessingTimePercent**</span></span>
</dt> <dd>

<span data-ttu-id="9ced8-108">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9ced8-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9ced8-109">Porcentaje de tiempo invertido en ejecutar sombreadores de vértices.</span><span class="sxs-lookup"><span data-stu-id="9ced8-109">Percent of time spent running vertex shaders.</span></span>

</dd> <dt>

<span data-ttu-id="9ced8-110">**PixelProcessingTimePercent**</span><span class="sxs-lookup"><span data-stu-id="9ced8-110">**PixelProcessingTimePercent**</span></span>
</dt> <dd>

<span data-ttu-id="9ced8-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9ced8-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9ced8-112">Porcentaje de tiempo invertido en ejecutar sombreadores de píxeles.</span><span class="sxs-lookup"><span data-stu-id="9ced8-112">Percent of time spent running pixel shaders.</span></span>

</dd> <dt>

<span data-ttu-id="9ced8-113">**OtherGPUProcessingTimePercent**</span><span class="sxs-lookup"><span data-stu-id="9ced8-113">**OtherGPUProcessingTimePercent**</span></span>
</dt> <dd>

<span data-ttu-id="9ced8-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9ced8-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9ced8-115">Porcentaje de tiempo invertido en realizar otro procesamiento.</span><span class="sxs-lookup"><span data-stu-id="9ced8-115">Percent of time spent doing other processing.</span></span>

</dd> <dt>

<span data-ttu-id="9ced8-116">**GPUIdleTimePercent**</span><span class="sxs-lookup"><span data-stu-id="9ced8-116">**GPUIdleTimePercent**</span></span>
</dt> <dd>

<span data-ttu-id="9ced8-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9ced8-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9ced8-118">Porcentaje de tiempo que no procesa nada.</span><span class="sxs-lookup"><span data-stu-id="9ced8-118">Percent of time not processing anything.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9ced8-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9ced8-119">Remarks</span></span>

<span data-ttu-id="9ced8-120">Para obtener el mejor rendimiento, se recomienda una carga equilibrada.</span><span class="sxs-lookup"><span data-stu-id="9ced8-120">For best performance, a balanced load is recommended.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ced8-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9ced8-121">Requirements</span></span>



| <span data-ttu-id="9ced8-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="9ced8-122">Requirement</span></span> | <span data-ttu-id="9ced8-123">Value</span><span class="sxs-lookup"><span data-stu-id="9ced8-123">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9ced8-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9ced8-124">Header</span></span><br/> | <dl> <span data-ttu-id="9ced8-125"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="9ced8-125"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ced8-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="9ced8-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ced8-127">Estructuras de Direct3D</span><span class="sxs-lookup"><span data-stu-id="9ced8-127">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="9ced8-128">**GetData**</span><span class="sxs-lookup"><span data-stu-id="9ced8-128">**GetData**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata)
</dt> </dl>

 

 
