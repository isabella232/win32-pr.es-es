---
description: 'Estructura D3DXATTRIBUTEWEIGHTS: especifica atributos de peso de malla.'
ms.assetid: 8901a0fe-e38a-4045-8e8d-584be2620cc3
title: Estructura D3DXATTRIBUTEWEIGHTS (D3dx9mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXATTRIBUTEWEIGHTS
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 7a833d2a58db0f434f836126926e461cd2ee3ea0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115973"
---
# <a name="d3dxattributeweights-structure"></a><span data-ttu-id="904d4-103">D3DXATTRIBUTEWEIGHTS (estructura)</span><span class="sxs-lookup"><span data-stu-id="904d4-103">D3DXATTRIBUTEWEIGHTS structure</span></span>

<span data-ttu-id="904d4-104">Especifica los atributos de peso de la malla.</span><span class="sxs-lookup"><span data-stu-id="904d4-104">Specifies mesh weight attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="904d4-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="904d4-105">Syntax</span></span>


```C++
typedef struct D3DXATTRIBUTEWEIGHTS {
  FLOAT Position;
  FLOAT Boundary;
  FLOAT Normal;
  FLOAT Diffuse;
  FLOAT Specular;
  FLOAT Texcoord[8];
  FLOAT Tangent;
  FLOAT Binormal;
} D3DXATTRIBUTEWEIGHTS, *LPD3DXATTRIBUTEWEIGHTS;
```



## <a name="members"></a><span data-ttu-id="904d4-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="904d4-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="904d4-107">**Position**</span><span class="sxs-lookup"><span data-stu-id="904d4-107">**Position**</span></span>
</dt> <dd>

<span data-ttu-id="904d4-108">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="904d4-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="904d4-109">Ubicación.</span><span class="sxs-lookup"><span data-stu-id="904d4-109">Position.</span></span>

</dd> <dt>

<span data-ttu-id="904d4-110">**Límite**</span><span class="sxs-lookup"><span data-stu-id="904d4-110">**Boundary**</span></span>
</dt> <dd>

<span data-ttu-id="904d4-111">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="904d4-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="904d4-112">Peso de mezcla.</span><span class="sxs-lookup"><span data-stu-id="904d4-112">Blend weight.</span></span>

</dd> <dt>

<span data-ttu-id="904d4-113">**Normal**</span><span class="sxs-lookup"><span data-stu-id="904d4-113">**Normal**</span></span>
</dt> <dd>

<span data-ttu-id="904d4-114">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="904d4-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="904d4-115">Normal.</span><span class="sxs-lookup"><span data-stu-id="904d4-115">Normal.</span></span>

</dd> <dt>

<span data-ttu-id="904d4-116">**Difusa**</span><span class="sxs-lookup"><span data-stu-id="904d4-116">**Diffuse**</span></span>
</dt> <dd>

<span data-ttu-id="904d4-117">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="904d4-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="904d4-118">Valor de iluminación difusa.</span><span class="sxs-lookup"><span data-stu-id="904d4-118">Diffuse lighting value.</span></span>

</dd> <dt>

<span data-ttu-id="904d4-119">**Especular**</span><span class="sxs-lookup"><span data-stu-id="904d4-119">**Specular**</span></span>
</dt> <dd>

<span data-ttu-id="904d4-120">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="904d4-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="904d4-121">Valor de iluminación especular.</span><span class="sxs-lookup"><span data-stu-id="904d4-121">Specular lighting value.</span></span>

</dd> <dt>

<span data-ttu-id="904d4-122">**Texascoord**</span><span class="sxs-lookup"><span data-stu-id="904d4-122">**Texcoord**</span></span>
</dt> <dd>

<span data-ttu-id="904d4-123">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="904d4-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="904d4-124">Ocho coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="904d4-124">Eight texture coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="904d4-125">**Tangente**</span><span class="sxs-lookup"><span data-stu-id="904d4-125">**Tangent**</span></span>
</dt> <dd>

<span data-ttu-id="904d4-126">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="904d4-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="904d4-127">Tangente.</span><span class="sxs-lookup"><span data-stu-id="904d4-127">Tangent.</span></span>

</dd> <dt>

<span data-ttu-id="904d4-128">**Binormal**</span><span class="sxs-lookup"><span data-stu-id="904d4-128">**Binormal**</span></span>
</dt> <dd>

<span data-ttu-id="904d4-129">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="904d4-129">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="904d4-130">Binormal.</span><span class="sxs-lookup"><span data-stu-id="904d4-130">Binormal.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="904d4-131">Comentarios</span><span class="sxs-lookup"><span data-stu-id="904d4-131">Remarks</span></span>

<span data-ttu-id="904d4-132">Esta estructura describe cómo una operación de simplificación tendrá en cuenta los datos de vértices al calcular los costos relativos entre los bordes contrayentes.</span><span class="sxs-lookup"><span data-stu-id="904d4-132">This structure describes how a simplification operation will consider vertex data when calculating relative costs between collapsing edges.</span></span> <span data-ttu-id="904d4-133">Por ejemplo, si el campo Normal es 0,0, la operación de simplificación omitirá el componente normal del vértice al calcular el error para el contrae.</span><span class="sxs-lookup"><span data-stu-id="904d4-133">For example, if the Normal field is 0.0, the simplification operation will ignore the vertex normal component when calculating the error for the collapse.</span></span> <span data-ttu-id="904d4-134">Sin embargo, si el campo Normal es 1.0, la operación de simplificación usará el componente normal del vértice.</span><span class="sxs-lookup"><span data-stu-id="904d4-134">However, if the Normal field is 1.0, the simplification operation will use the vertex normal component.</span></span> <span data-ttu-id="904d4-135">Si el campo Normal es 2.0, duplicó la cantidad de errores; si el campo Normal es 4.0, a continuación, el número de errores, y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="904d4-135">If the Normal field is 2.0, double the amount of errors; if the Normal field is 4.0, then quadruple the number of errors, and so on.</span></span>

<span data-ttu-id="904d4-136">El tipo LPD3DXATTRIBUTEWEIGHTS se define como un puntero a la **estructura D3DXATTRIBUTEWEIGHTS.**</span><span class="sxs-lookup"><span data-stu-id="904d4-136">The LPD3DXATTRIBUTEWEIGHTS type is defined as a pointer to the **D3DXATTRIBUTEWEIGHTS** structure.</span></span>


```
    
    typedef D3DXATTRIBUTEWEIGHTS* LPD3DXATTRIBUTEWEIGHTS;
```



## <a name="requirements"></a><span data-ttu-id="904d4-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="904d4-137">Requirements</span></span>



| <span data-ttu-id="904d4-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="904d4-138">Requirement</span></span> | <span data-ttu-id="904d4-139">Value</span><span class="sxs-lookup"><span data-stu-id="904d4-139">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="904d4-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="904d4-140">Header</span></span><br/> | <dl> <span data-ttu-id="904d4-141"><dt>D3dx9mesh.h</dt></span><span class="sxs-lookup"><span data-stu-id="904d4-141"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="904d4-142">Consulte también</span><span class="sxs-lookup"><span data-stu-id="904d4-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="904d4-143">Estructuras D3DX</span><span class="sxs-lookup"><span data-stu-id="904d4-143">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[<span data-ttu-id="904d4-144">**D3DXSimplifyMesh**</span><span class="sxs-lookup"><span data-stu-id="904d4-144">**D3DXSimplifyMesh**</span></span>](d3dxsimplifymesh.md)
</dt> </dl>

 

 
