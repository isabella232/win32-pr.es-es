---
description: 'D3DX10_WELD_EPSILONS estructura: especifica los valores de tolerancia para cada componente de vértice al comparar los vértices para determinar si son lo suficientemente similares como para que se puedan unir.'
ms.assetid: b28a17bd-5d5b-41b3-86d9-327f5497fc94
title: D3DX10_WELD_EPSILONS estructura (D3DX10.h)
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
ms.openlocfilehash: 720a10dbe4b22b69910d88d3c03cea9ded768f1b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105433"
---
# <a name="d3dx10_weld_epsilons-structure"></a><span data-ttu-id="c862d-103">Estructura D3DX10 \_ HISTOGRAM \_ EPSILONS</span><span class="sxs-lookup"><span data-stu-id="c862d-103">D3DX10\_WELD\_EPSILONS structure</span></span>

<span data-ttu-id="c862d-104">Especifica valores de tolerancia para cada componente de vértice al comparar vértices para determinar si son lo suficientemente similares como para que se puedan unir.</span><span class="sxs-lookup"><span data-stu-id="c862d-104">Specifies tolerance values for each vertex component when comparing vertices to determine if they are similar enough to be welded together.</span></span>

## <a name="syntax"></a><span data-ttu-id="c862d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c862d-105">Syntax</span></span>


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



## <a name="members"></a><span data-ttu-id="c862d-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="c862d-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="c862d-107">**Position**</span><span class="sxs-lookup"><span data-stu-id="c862d-107">**Position**</span></span>
</dt> <dd>

<span data-ttu-id="c862d-108">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c862d-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c862d-109">Posición</span><span class="sxs-lookup"><span data-stu-id="c862d-109">Position</span></span>

</dd> <dt>

<span data-ttu-id="c862d-110">**BlendWeights**</span><span class="sxs-lookup"><span data-stu-id="c862d-110">**BlendWeights**</span></span>
</dt> <dd>

<span data-ttu-id="c862d-111">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c862d-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c862d-112">Peso de blend</span><span class="sxs-lookup"><span data-stu-id="c862d-112">Blend weight</span></span>

</dd> <dt>

<span data-ttu-id="c862d-113">**Normal**</span><span class="sxs-lookup"><span data-stu-id="c862d-113">**Normal**</span></span>
</dt> <dd>

<span data-ttu-id="c862d-114">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c862d-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c862d-115">Normal</span><span class="sxs-lookup"><span data-stu-id="c862d-115">Normal</span></span>

</dd> <dt>

<span data-ttu-id="c862d-116">**PSize**</span><span class="sxs-lookup"><span data-stu-id="c862d-116">**PSize**</span></span>
</dt> <dd>

<span data-ttu-id="c862d-117">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c862d-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c862d-118">Valor de tamaño de punto</span><span class="sxs-lookup"><span data-stu-id="c862d-118">Point size value</span></span>

</dd> <dt>

<span data-ttu-id="c862d-119">**Especular**</span><span class="sxs-lookup"><span data-stu-id="c862d-119">**Specular**</span></span>
</dt> <dd>

<span data-ttu-id="c862d-120">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c862d-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c862d-121">Valor de iluminación especular</span><span class="sxs-lookup"><span data-stu-id="c862d-121">Specular lighting value</span></span>

</dd> <dt>

<span data-ttu-id="c862d-122">**Difusa**</span><span class="sxs-lookup"><span data-stu-id="c862d-122">**Diffuse**</span></span>
</dt> <dd>

<span data-ttu-id="c862d-123">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c862d-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c862d-124">Valor de iluminación difusa</span><span class="sxs-lookup"><span data-stu-id="c862d-124">Diffuse lighting value</span></span>

</dd> <dt>

<span data-ttu-id="c862d-125">**Texcoord**</span><span class="sxs-lookup"><span data-stu-id="c862d-125">**Texcoord**</span></span>
</dt> <dd>

<span data-ttu-id="c862d-126">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c862d-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c862d-127">Ocho coordenadas de textura</span><span class="sxs-lookup"><span data-stu-id="c862d-127">Eight texture coordinates</span></span>

</dd> <dt>

<span data-ttu-id="c862d-128">**Tangente**</span><span class="sxs-lookup"><span data-stu-id="c862d-128">**Tangent**</span></span>
</dt> <dd>

<span data-ttu-id="c862d-129">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c862d-129">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c862d-130">Tangente</span><span class="sxs-lookup"><span data-stu-id="c862d-130">Tangent</span></span>

</dd> <dt>

<span data-ttu-id="c862d-131">**Binormal**</span><span class="sxs-lookup"><span data-stu-id="c862d-131">**Binormal**</span></span>
</dt> <dd>

<span data-ttu-id="c862d-132">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c862d-132">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c862d-133">Binormal</span><span class="sxs-lookup"><span data-stu-id="c862d-133">Binormal</span></span>

</dd> <dt>

<span data-ttu-id="c862d-134">**TessFactor**</span><span class="sxs-lookup"><span data-stu-id="c862d-134">**TessFactor**</span></span>
</dt> <dd>

<span data-ttu-id="c862d-135">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c862d-135">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c862d-136">Factor de teselación</span><span class="sxs-lookup"><span data-stu-id="c862d-136">Tessellation factor</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c862d-137">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c862d-137">Remarks</span></span>

<span data-ttu-id="c862d-138">El tipo LPD3DXWeldEpsilons se define como un puntero a la estructura D3DXWeldEpsilons.</span><span class="sxs-lookup"><span data-stu-id="c862d-138">The LPD3DXWeldEpsilons type is defined as a pointer to the D3DXWeldEpsilons structure.</span></span>


```
typedef D3DX_WELD_EPSILONS *LPD3DX_WELD_EPSILONS;
```



## <a name="requirements"></a><span data-ttu-id="c862d-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c862d-139">Requirements</span></span>



| <span data-ttu-id="c862d-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="c862d-140">Requirement</span></span> | <span data-ttu-id="c862d-141">Value</span><span class="sxs-lookup"><span data-stu-id="c862d-141">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="c862d-142">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c862d-142">Header</span></span><br/> | <dl> <span data-ttu-id="c862d-143"><dt>D3DX10.h</dt></span><span class="sxs-lookup"><span data-stu-id="c862d-143"><dt>D3DX10.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c862d-144">Consulte también</span><span class="sxs-lookup"><span data-stu-id="c862d-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c862d-145">Estructuras D3DX</span><span class="sxs-lookup"><span data-stu-id="c862d-145">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
