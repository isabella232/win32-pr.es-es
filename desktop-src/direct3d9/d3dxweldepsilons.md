---
description: 'Estructura D3DXWELDEPSILONS: especifica los valores de tolerancia para cada componente de vértice al comparar los vértices para determinar si son lo suficientemente similares como para que se puedan unir.'
ms.assetid: 534903da-ff65-4629-9be9-66c9daed6ef5
title: Estructura D3DXWELDEPSILONS (D3dx9mesh.h)
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
ms.openlocfilehash: bb11e6f5481b1adf7cc1bac58edf40d4ac770e92
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115503"
---
# <a name="d3dxweldepsilons-structure"></a><span data-ttu-id="4f4e1-103">D3DXWELDEPSILONS (estructura)</span><span class="sxs-lookup"><span data-stu-id="4f4e1-103">D3DXWELDEPSILONS structure</span></span>

<span data-ttu-id="4f4e1-104">Especifica valores de tolerancia para cada componente de vértice al comparar vértices para determinar si son lo suficientemente similares como para que se puedan unir.</span><span class="sxs-lookup"><span data-stu-id="4f4e1-104">Specifies tolerance values for each vertex component when comparing vertices to determine if they are similar enough to be welded together.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f4e1-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4f4e1-105">Syntax</span></span>


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



## <a name="members"></a><span data-ttu-id="4f4e1-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="4f4e1-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="4f4e1-107">**Position**</span><span class="sxs-lookup"><span data-stu-id="4f4e1-107">**Position**</span></span>
</dt> <dd>

<span data-ttu-id="4f4e1-108">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4f4e1-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="4f4e1-109">Posición</span><span class="sxs-lookup"><span data-stu-id="4f4e1-109">Position</span></span>

</dd> <dt>

<span data-ttu-id="4f4e1-110">**BlendWeights**</span><span class="sxs-lookup"><span data-stu-id="4f4e1-110">**BlendWeights**</span></span>
</dt> <dd>

<span data-ttu-id="4f4e1-111">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4f4e1-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="4f4e1-112">Peso de blend</span><span class="sxs-lookup"><span data-stu-id="4f4e1-112">Blend weight</span></span>

</dd> <dt>

<span data-ttu-id="4f4e1-113">**Normal**</span><span class="sxs-lookup"><span data-stu-id="4f4e1-113">**Normal**</span></span>
</dt> <dd>

<span data-ttu-id="4f4e1-114">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4f4e1-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="4f4e1-115">Normal</span><span class="sxs-lookup"><span data-stu-id="4f4e1-115">Normal</span></span>

</dd> <dt>

<span data-ttu-id="4f4e1-116">**PSize**</span><span class="sxs-lookup"><span data-stu-id="4f4e1-116">**PSize**</span></span>
</dt> <dd>

<span data-ttu-id="4f4e1-117">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4f4e1-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="4f4e1-118">Valor de tamaño de punto</span><span class="sxs-lookup"><span data-stu-id="4f4e1-118">Point size value</span></span>

</dd> <dt>

<span data-ttu-id="4f4e1-119">**Especular**</span><span class="sxs-lookup"><span data-stu-id="4f4e1-119">**Specular**</span></span>
</dt> <dd>

<span data-ttu-id="4f4e1-120">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4f4e1-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="4f4e1-121">Valor de iluminación especular</span><span class="sxs-lookup"><span data-stu-id="4f4e1-121">Specular lighting value</span></span>

</dd> <dt>

<span data-ttu-id="4f4e1-122">**Difusa**</span><span class="sxs-lookup"><span data-stu-id="4f4e1-122">**Diffuse**</span></span>
</dt> <dd>

<span data-ttu-id="4f4e1-123">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4f4e1-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="4f4e1-124">Valor de iluminación difusa</span><span class="sxs-lookup"><span data-stu-id="4f4e1-124">Diffuse lighting value</span></span>

</dd> <dt>

<span data-ttu-id="4f4e1-125">**Texascoord**</span><span class="sxs-lookup"><span data-stu-id="4f4e1-125">**Texcoord**</span></span>
</dt> <dd>

<span data-ttu-id="4f4e1-126">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4f4e1-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="4f4e1-127">Ocho coordenadas de textura</span><span class="sxs-lookup"><span data-stu-id="4f4e1-127">Eight texture coordinates</span></span>

</dd> <dt>

<span data-ttu-id="4f4e1-128">**Tangente**</span><span class="sxs-lookup"><span data-stu-id="4f4e1-128">**Tangent**</span></span>
</dt> <dd>

<span data-ttu-id="4f4e1-129">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4f4e1-129">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="4f4e1-130">Tangente</span><span class="sxs-lookup"><span data-stu-id="4f4e1-130">Tangent</span></span>

</dd> <dt>

<span data-ttu-id="4f4e1-131">**Binormal**</span><span class="sxs-lookup"><span data-stu-id="4f4e1-131">**Binormal**</span></span>
</dt> <dd>

<span data-ttu-id="4f4e1-132">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4f4e1-132">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="4f4e1-133">Binormal</span><span class="sxs-lookup"><span data-stu-id="4f4e1-133">Binormal</span></span>

</dd> <dt>

<span data-ttu-id="4f4e1-134">**TessFactor**</span><span class="sxs-lookup"><span data-stu-id="4f4e1-134">**TessFactor**</span></span>
</dt> <dd>

<span data-ttu-id="4f4e1-135">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4f4e1-135">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="4f4e1-136">Factor de teselación</span><span class="sxs-lookup"><span data-stu-id="4f4e1-136">Tessellation factor</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4f4e1-137">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4f4e1-137">Remarks</span></span>

<span data-ttu-id="4f4e1-138">El tipo LPD3DXWELDEPSILONS se define como un puntero a la estructura **D3DXWELDEPSILONS.**</span><span class="sxs-lookup"><span data-stu-id="4f4e1-138">The LPD3DXWELDEPSILONS type is defined as a pointer to the **D3DXWELDEPSILONS** structure.</span></span>


```
typedef D3DXWELDEPSILONS *LPD3DXWELDEPSILONS;
```



## <a name="requirements"></a><span data-ttu-id="4f4e1-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4f4e1-139">Requirements</span></span>



| <span data-ttu-id="4f4e1-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="4f4e1-140">Requirement</span></span> | <span data-ttu-id="4f4e1-141">Value</span><span class="sxs-lookup"><span data-stu-id="4f4e1-141">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4f4e1-142">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4f4e1-142">Header</span></span><br/> | <dl> <span data-ttu-id="4f4e1-143"><dt>D3dx9mesh.h</dt></span><span class="sxs-lookup"><span data-stu-id="4f4e1-143"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f4e1-144">Consulte también</span><span class="sxs-lookup"><span data-stu-id="4f4e1-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f4e1-145">Estructuras D3DX</span><span class="sxs-lookup"><span data-stu-id="4f4e1-145">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[<span data-ttu-id="4f4e1-146">**D3DXWeldVertices**</span><span class="sxs-lookup"><span data-stu-id="4f4e1-146">**D3DXWeldVertices**</span></span>](d3dxweldvertices.md)
</dt> </dl>

 

 
