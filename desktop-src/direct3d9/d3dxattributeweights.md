---
description: Especifica los atributos de peso de la malla.
ms.assetid: 8901a0fe-e38a-4045-8e8d-584be2620cc3
title: Estructura D3DXATTRIBUTEWEIGHTS (D3dx9mesh. h)
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
ms.openlocfilehash: 49725e410fb700c7ecb93fd56a8db367d7f982a0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105721469"
---
# <a name="d3dxattributeweights-structure"></a><span data-ttu-id="d7f0d-103">Estructura D3DXATTRIBUTEWEIGHTS</span><span class="sxs-lookup"><span data-stu-id="d7f0d-103">D3DXATTRIBUTEWEIGHTS structure</span></span>

<span data-ttu-id="d7f0d-104">Especifica los atributos de peso de la malla.</span><span class="sxs-lookup"><span data-stu-id="d7f0d-104">Specifies mesh weight attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7f0d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d7f0d-105">Syntax</span></span>


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



## <a name="members"></a><span data-ttu-id="d7f0d-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="d7f0d-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="d7f0d-107">**Position**</span><span class="sxs-lookup"><span data-stu-id="d7f0d-107">**Position**</span></span>
</dt> <dd>

<span data-ttu-id="d7f0d-108">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d7f0d-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d7f0d-109">Ubicación.</span><span class="sxs-lookup"><span data-stu-id="d7f0d-109">Position.</span></span>

</dd> <dt>

<span data-ttu-id="d7f0d-110">**Límite**</span><span class="sxs-lookup"><span data-stu-id="d7f0d-110">**Boundary**</span></span>
</dt> <dd>

<span data-ttu-id="d7f0d-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d7f0d-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d7f0d-112">Peso de la mezcla.</span><span class="sxs-lookup"><span data-stu-id="d7f0d-112">Blend weight.</span></span>

</dd> <dt>

<span data-ttu-id="d7f0d-113">**Normal**</span><span class="sxs-lookup"><span data-stu-id="d7f0d-113">**Normal**</span></span>
</dt> <dd>

<span data-ttu-id="d7f0d-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d7f0d-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d7f0d-115">Normal.</span><span class="sxs-lookup"><span data-stu-id="d7f0d-115">Normal.</span></span>

</dd> <dt>

<span data-ttu-id="d7f0d-116">**Difusa**</span><span class="sxs-lookup"><span data-stu-id="d7f0d-116">**Diffuse**</span></span>
</dt> <dd>

<span data-ttu-id="d7f0d-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d7f0d-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d7f0d-118">Valor de iluminación difusa.</span><span class="sxs-lookup"><span data-stu-id="d7f0d-118">Diffuse lighting value.</span></span>

</dd> <dt>

<span data-ttu-id="d7f0d-119">**Especular**</span><span class="sxs-lookup"><span data-stu-id="d7f0d-119">**Specular**</span></span>
</dt> <dd>

<span data-ttu-id="d7f0d-120">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d7f0d-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d7f0d-121">Valor de iluminación especular.</span><span class="sxs-lookup"><span data-stu-id="d7f0d-121">Specular lighting value.</span></span>

</dd> <dt>

<span data-ttu-id="d7f0d-122">**Texcoord**</span><span class="sxs-lookup"><span data-stu-id="d7f0d-122">**Texcoord**</span></span>
</dt> <dd>

<span data-ttu-id="d7f0d-123">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d7f0d-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d7f0d-124">Ocho coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="d7f0d-124">Eight texture coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="d7f0d-125">**Tangente**</span><span class="sxs-lookup"><span data-stu-id="d7f0d-125">**Tangent**</span></span>
</dt> <dd>

<span data-ttu-id="d7f0d-126">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d7f0d-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d7f0d-127">Tangente.</span><span class="sxs-lookup"><span data-stu-id="d7f0d-127">Tangent.</span></span>

</dd> <dt>

<span data-ttu-id="d7f0d-128">**Binormalización**</span><span class="sxs-lookup"><span data-stu-id="d7f0d-128">**Binormal**</span></span>
</dt> <dd>

<span data-ttu-id="d7f0d-129">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d7f0d-129">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d7f0d-130">Binormal.</span><span class="sxs-lookup"><span data-stu-id="d7f0d-130">Binormal.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d7f0d-131">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d7f0d-131">Remarks</span></span>

<span data-ttu-id="d7f0d-132">En esta estructura se describe cómo una operación de simplificación considerará los datos de vértices al calcular los costos relativos entre los bordes contraídos.</span><span class="sxs-lookup"><span data-stu-id="d7f0d-132">This structure describes how a simplification operation will consider vertex data when calculating relative costs between collapsing edges.</span></span> <span data-ttu-id="d7f0d-133">Por ejemplo, si el campo normal es 0,0, la operación de simplificación omitirá el componente normal del vértice al calcular el error de la acción de contraer.</span><span class="sxs-lookup"><span data-stu-id="d7f0d-133">For example, if the Normal field is 0.0, the simplification operation will ignore the vertex normal component when calculating the error for the collapse.</span></span> <span data-ttu-id="d7f0d-134">Sin embargo, si el campo normal es 1,0, la operación de simplificación usará el componente normal de vértice.</span><span class="sxs-lookup"><span data-stu-id="d7f0d-134">However, if the Normal field is 1.0, the simplification operation will use the vertex normal component.</span></span> <span data-ttu-id="d7f0d-135">Si el campo normal es 2,0, duplique la cantidad de errores; Si el campo normal es 4,0, cuádruple el número de errores, etc.</span><span class="sxs-lookup"><span data-stu-id="d7f0d-135">If the Normal field is 2.0, double the amount of errors; if the Normal field is 4.0, then quadruple the number of errors, and so on.</span></span>

<span data-ttu-id="d7f0d-136">El tipo LPD3DXATTRIBUTEWEIGHTS se define como un puntero a la estructura **D3DXATTRIBUTEWEIGHTS** .</span><span class="sxs-lookup"><span data-stu-id="d7f0d-136">The LPD3DXATTRIBUTEWEIGHTS type is defined as a pointer to the **D3DXATTRIBUTEWEIGHTS** structure.</span></span>


```
    
    typedef D3DXATTRIBUTEWEIGHTS* LPD3DXATTRIBUTEWEIGHTS;
```



## <a name="requirements"></a><span data-ttu-id="d7f0d-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d7f0d-137">Requirements</span></span>



| <span data-ttu-id="d7f0d-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="d7f0d-138">Requirement</span></span> | <span data-ttu-id="d7f0d-139">Value</span><span class="sxs-lookup"><span data-stu-id="d7f0d-139">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d7f0d-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d7f0d-140">Header</span></span><br/> | <dl> <span data-ttu-id="d7f0d-141"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="d7f0d-141"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7f0d-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="d7f0d-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7f0d-143">Estructuras de D3DX</span><span class="sxs-lookup"><span data-stu-id="d7f0d-143">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[<span data-ttu-id="d7f0d-144">**D3DXSimplifyMesh**</span><span class="sxs-lookup"><span data-stu-id="d7f0d-144">**D3DXSimplifyMesh**</span></span>](d3dxsimplifymesh.md)
</dt> </dl>

 

 
