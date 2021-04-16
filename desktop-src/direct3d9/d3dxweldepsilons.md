---
description: Especifica los valores de tolerancia de cada componente de vértice cuando se comparan los vértices para determinar si son lo suficientemente similares como para ser soldados juntos.
ms.assetid: 534903da-ff65-4629-9be9-66c9daed6ef5
title: Estructura D3DXWELDEPSILONS (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXWELDEPSILONS
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 6b6673e16b153f53baf17967b7f33c4bcb40d518
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105649413"
---
# <a name="d3dxweldepsilons-structure"></a><span data-ttu-id="e328b-103">Estructura D3DXWELDEPSILONS</span><span class="sxs-lookup"><span data-stu-id="e328b-103">D3DXWELDEPSILONS structure</span></span>

<span data-ttu-id="e328b-104">Especifica los valores de tolerancia de cada componente de vértice cuando se comparan los vértices para determinar si son lo suficientemente similares como para ser soldados juntos.</span><span class="sxs-lookup"><span data-stu-id="e328b-104">Specifies tolerance values for each vertex component when comparing vertices to determine if they are similar enough to be welded together.</span></span>

## <a name="syntax"></a><span data-ttu-id="e328b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e328b-105">Syntax</span></span>


```C++
typedef struct _D3DXWELDEPSILONS {
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
} D3DXWELDEPSILONS, *LPD3DXWELDEPSILONS;
```



## <a name="members"></a><span data-ttu-id="e328b-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="e328b-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="e328b-107">**Position**</span><span class="sxs-lookup"><span data-stu-id="e328b-107">**Position**</span></span>
</dt> <dd>

<span data-ttu-id="e328b-108">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e328b-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e328b-109">Posición</span><span class="sxs-lookup"><span data-stu-id="e328b-109">Position</span></span>

</dd> <dt>

<span data-ttu-id="e328b-110">**BlendWeights**</span><span class="sxs-lookup"><span data-stu-id="e328b-110">**BlendWeights**</span></span>
</dt> <dd>

<span data-ttu-id="e328b-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e328b-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e328b-112">Peso de Blend</span><span class="sxs-lookup"><span data-stu-id="e328b-112">Blend weight</span></span>

</dd> <dt>

<span data-ttu-id="e328b-113">**Normal**</span><span class="sxs-lookup"><span data-stu-id="e328b-113">**Normal**</span></span>
</dt> <dd>

<span data-ttu-id="e328b-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e328b-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e328b-115">Normal</span><span class="sxs-lookup"><span data-stu-id="e328b-115">Normal</span></span>

</dd> <dt>

<span data-ttu-id="e328b-116">**PSize**</span><span class="sxs-lookup"><span data-stu-id="e328b-116">**PSize**</span></span>
</dt> <dd>

<span data-ttu-id="e328b-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e328b-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e328b-118">Valor de tamaño de punto</span><span class="sxs-lookup"><span data-stu-id="e328b-118">Point size value</span></span>

</dd> <dt>

<span data-ttu-id="e328b-119">**Especular**</span><span class="sxs-lookup"><span data-stu-id="e328b-119">**Specular**</span></span>
</dt> <dd>

<span data-ttu-id="e328b-120">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e328b-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e328b-121">Valor de iluminación especular</span><span class="sxs-lookup"><span data-stu-id="e328b-121">Specular lighting value</span></span>

</dd> <dt>

<span data-ttu-id="e328b-122">**Difusa**</span><span class="sxs-lookup"><span data-stu-id="e328b-122">**Diffuse**</span></span>
</dt> <dd>

<span data-ttu-id="e328b-123">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e328b-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e328b-124">Valor de iluminación difusa</span><span class="sxs-lookup"><span data-stu-id="e328b-124">Diffuse lighting value</span></span>

</dd> <dt>

<span data-ttu-id="e328b-125">**Texcoord**</span><span class="sxs-lookup"><span data-stu-id="e328b-125">**Texcoord**</span></span>
</dt> <dd>

<span data-ttu-id="e328b-126">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e328b-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e328b-127">Ocho coordenadas de textura</span><span class="sxs-lookup"><span data-stu-id="e328b-127">Eight texture coordinates</span></span>

</dd> <dt>

<span data-ttu-id="e328b-128">**Tangente**</span><span class="sxs-lookup"><span data-stu-id="e328b-128">**Tangent**</span></span>
</dt> <dd>

<span data-ttu-id="e328b-129">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e328b-129">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e328b-130">Tangente</span><span class="sxs-lookup"><span data-stu-id="e328b-130">Tangent</span></span>

</dd> <dt>

<span data-ttu-id="e328b-131">**Binormalización**</span><span class="sxs-lookup"><span data-stu-id="e328b-131">**Binormal**</span></span>
</dt> <dd>

<span data-ttu-id="e328b-132">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e328b-132">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e328b-133">Binormalización</span><span class="sxs-lookup"><span data-stu-id="e328b-133">Binormal</span></span>

</dd> <dt>

<span data-ttu-id="e328b-134">**TessFactor**</span><span class="sxs-lookup"><span data-stu-id="e328b-134">**TessFactor**</span></span>
</dt> <dd>

<span data-ttu-id="e328b-135">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e328b-135">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e328b-136">Factor de teselación</span><span class="sxs-lookup"><span data-stu-id="e328b-136">Tessellation factor</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e328b-137">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e328b-137">Remarks</span></span>

<span data-ttu-id="e328b-138">El tipo LPD3DXWELDEPSILONS se define como un puntero a la estructura **D3DXWELDEPSILONS** .</span><span class="sxs-lookup"><span data-stu-id="e328b-138">The LPD3DXWELDEPSILONS type is defined as a pointer to the **D3DXWELDEPSILONS** structure.</span></span>


```
typedef D3DXWELDEPSILONS *LPD3DXWELDEPSILONS;
```



## <a name="requirements"></a><span data-ttu-id="e328b-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e328b-139">Requirements</span></span>



| <span data-ttu-id="e328b-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="e328b-140">Requirement</span></span> | <span data-ttu-id="e328b-141">Value</span><span class="sxs-lookup"><span data-stu-id="e328b-141">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e328b-142">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e328b-142">Header</span></span><br/> | <dl> <span data-ttu-id="e328b-143"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="e328b-143"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e328b-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="e328b-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e328b-145">Estructuras de D3DX</span><span class="sxs-lookup"><span data-stu-id="e328b-145">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[<span data-ttu-id="e328b-146">**D3DXWeldVertices**</span><span class="sxs-lookup"><span data-stu-id="e328b-146">**D3DXWeldVertices**</span></span>](d3dxweldvertices.md)
</dt> </dl>

 

 
