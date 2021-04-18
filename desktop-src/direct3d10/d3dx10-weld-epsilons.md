---
description: Especifica los valores de tolerancia de cada componente de vértice cuando se comparan los vértices para determinar si son lo suficientemente similares como para ser soldados juntos.
ms.assetid: b28a17bd-5d5b-41b3-86d9-327f5497fc94
title: D3DX10_WELD_EPSILONS estructura (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_WELD_EPSILONS
api_type:
- HeaderDef
api_location:
- D3DX10.h
ms.openlocfilehash: c72f63e3ecef1fdb193fcaec9220f9768204d099
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718295"
---
# <a name="d3dx10_weld_epsilons-structure"></a><span data-ttu-id="52d97-103">D3DX10 de épsilon de soldadura de la \_ \_ estructura</span><span class="sxs-lookup"><span data-stu-id="52d97-103">D3DX10\_WELD\_EPSILONS structure</span></span>

<span data-ttu-id="52d97-104">Especifica los valores de tolerancia de cada componente de vértice cuando se comparan los vértices para determinar si son lo suficientemente similares como para ser soldados juntos.</span><span class="sxs-lookup"><span data-stu-id="52d97-104">Specifies tolerance values for each vertex component when comparing vertices to determine if they are similar enough to be welded together.</span></span>

## <a name="syntax"></a><span data-ttu-id="52d97-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="52d97-105">Syntax</span></span>


```C++
typedef struct D3DX10_WELD_EPSILONS {
  FLOAT Position;
  FLOAT BlendWeights;
  FLOAT Normal;
  FLOAT PSize;
  FLOAT Specular;
  FLOAT Diffuse;
  FLOAT Texcoord[8];
  FLOAT Tangent;
  FLOAT Binormal;
  FLOAT TessFactor;
} D3DX10_WELD_EPSILONS, *LPD3DX10_WELD_EPSILONS;
```



## <a name="members"></a><span data-ttu-id="52d97-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="52d97-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="52d97-107">**Position**</span><span class="sxs-lookup"><span data-stu-id="52d97-107">**Position**</span></span>
</dt> <dd>

<span data-ttu-id="52d97-108">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="52d97-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="52d97-109">Posición</span><span class="sxs-lookup"><span data-stu-id="52d97-109">Position</span></span>

</dd> <dt>

<span data-ttu-id="52d97-110">**BlendWeights**</span><span class="sxs-lookup"><span data-stu-id="52d97-110">**BlendWeights**</span></span>
</dt> <dd>

<span data-ttu-id="52d97-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="52d97-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="52d97-112">Peso de Blend</span><span class="sxs-lookup"><span data-stu-id="52d97-112">Blend weight</span></span>

</dd> <dt>

<span data-ttu-id="52d97-113">**Normal**</span><span class="sxs-lookup"><span data-stu-id="52d97-113">**Normal**</span></span>
</dt> <dd>

<span data-ttu-id="52d97-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="52d97-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="52d97-115">Normal</span><span class="sxs-lookup"><span data-stu-id="52d97-115">Normal</span></span>

</dd> <dt>

<span data-ttu-id="52d97-116">**PSize**</span><span class="sxs-lookup"><span data-stu-id="52d97-116">**PSize**</span></span>
</dt> <dd>

<span data-ttu-id="52d97-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="52d97-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="52d97-118">Valor de tamaño de punto</span><span class="sxs-lookup"><span data-stu-id="52d97-118">Point size value</span></span>

</dd> <dt>

<span data-ttu-id="52d97-119">**Especular**</span><span class="sxs-lookup"><span data-stu-id="52d97-119">**Specular**</span></span>
</dt> <dd>

<span data-ttu-id="52d97-120">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="52d97-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="52d97-121">Valor de iluminación especular</span><span class="sxs-lookup"><span data-stu-id="52d97-121">Specular lighting value</span></span>

</dd> <dt>

<span data-ttu-id="52d97-122">**Difusa**</span><span class="sxs-lookup"><span data-stu-id="52d97-122">**Diffuse**</span></span>
</dt> <dd>

<span data-ttu-id="52d97-123">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="52d97-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="52d97-124">Valor de iluminación difusa</span><span class="sxs-lookup"><span data-stu-id="52d97-124">Diffuse lighting value</span></span>

</dd> <dt>

<span data-ttu-id="52d97-125">**Texcoord**</span><span class="sxs-lookup"><span data-stu-id="52d97-125">**Texcoord**</span></span>
</dt> <dd>

<span data-ttu-id="52d97-126">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="52d97-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="52d97-127">Ocho coordenadas de textura</span><span class="sxs-lookup"><span data-stu-id="52d97-127">Eight texture coordinates</span></span>

</dd> <dt>

<span data-ttu-id="52d97-128">**Tangente**</span><span class="sxs-lookup"><span data-stu-id="52d97-128">**Tangent**</span></span>
</dt> <dd>

<span data-ttu-id="52d97-129">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="52d97-129">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="52d97-130">Tangente</span><span class="sxs-lookup"><span data-stu-id="52d97-130">Tangent</span></span>

</dd> <dt>

<span data-ttu-id="52d97-131">**Binormalización**</span><span class="sxs-lookup"><span data-stu-id="52d97-131">**Binormal**</span></span>
</dt> <dd>

<span data-ttu-id="52d97-132">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="52d97-132">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="52d97-133">Binormalización</span><span class="sxs-lookup"><span data-stu-id="52d97-133">Binormal</span></span>

</dd> <dt>

<span data-ttu-id="52d97-134">**TessFactor**</span><span class="sxs-lookup"><span data-stu-id="52d97-134">**TessFactor**</span></span>
</dt> <dd>

<span data-ttu-id="52d97-135">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="52d97-135">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="52d97-136">Factor de teselación</span><span class="sxs-lookup"><span data-stu-id="52d97-136">Tessellation factor</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="52d97-137">Observaciones</span><span class="sxs-lookup"><span data-stu-id="52d97-137">Remarks</span></span>

<span data-ttu-id="52d97-138">El tipo LPD3DXWeldEpsilons se define como un puntero a la estructura D3DXWeldEpsilons.</span><span class="sxs-lookup"><span data-stu-id="52d97-138">The LPD3DXWeldEpsilons type is defined as a pointer to the D3DXWeldEpsilons structure.</span></span>


```
typedef D3DX_WELD_EPSILONS *LPD3DX_WELD_EPSILONS;
```



## <a name="requirements"></a><span data-ttu-id="52d97-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="52d97-139">Requirements</span></span>



| <span data-ttu-id="52d97-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="52d97-140">Requirement</span></span> | <span data-ttu-id="52d97-141">Value</span><span class="sxs-lookup"><span data-stu-id="52d97-141">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="52d97-142">Encabezado</span><span class="sxs-lookup"><span data-stu-id="52d97-142">Header</span></span><br/> | <dl> <span data-ttu-id="52d97-143"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="52d97-143"><dt>D3DX10.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="52d97-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="52d97-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52d97-145">Estructuras de D3DX</span><span class="sxs-lookup"><span data-stu-id="52d97-145">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
