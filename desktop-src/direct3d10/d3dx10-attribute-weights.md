---
description: 'D3DX10_ATTRIBUTE_WEIGHTS estructura: especifica los atributos de peso de malla.'
ms.assetid: 554bb8f2-9e92-4e9e-b500-c3cc47d57830
title: D3DX10_ATTRIBUTE_WEIGHTS estructura (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_ATTRIBUTE_WEIGHTS
api_type:
- HeaderDef
api_location:
- D3DX10.h
ms.openlocfilehash: ab163149493ad73f892a251a691ad82544d7f382
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094362"
---
# <a name="d3dx10_attribute_weights-structure"></a><span data-ttu-id="3968f-103">Estructura D3DX10 \_ ATTRIBUTE \_ WEIGHTS</span><span class="sxs-lookup"><span data-stu-id="3968f-103">D3DX10\_ATTRIBUTE\_WEIGHTS structure</span></span>

<span data-ttu-id="3968f-104">Especifica los atributos de peso de malla.</span><span class="sxs-lookup"><span data-stu-id="3968f-104">Specifies mesh weight attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="3968f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3968f-105">Syntax</span></span>


```C++
typedef struct D3DX10_ATTRIBUTE_WEIGHTS {
  FLOAT Position;
  FLOAT Boundary;
  FLOAT Normal;
  FLOAT Diffuse;
  FLOAT Specular;
  FLOAT Texcoord[8];
  FLOAT Tangent;
  FLOAT Binormal;
} D3DX10_ATTRIBUTE_WEIGHTS, *LPD3DX10_ATTRIBUTE_WEIGHTS;
```



## <a name="members"></a><span data-ttu-id="3968f-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="3968f-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="3968f-107">**Position**</span><span class="sxs-lookup"><span data-stu-id="3968f-107">**Position**</span></span>
</dt> <dd>

<span data-ttu-id="3968f-108">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3968f-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="3968f-109">Ubicación.</span><span class="sxs-lookup"><span data-stu-id="3968f-109">Position.</span></span>

</dd> <dt>

<span data-ttu-id="3968f-110">**Límite**</span><span class="sxs-lookup"><span data-stu-id="3968f-110">**Boundary**</span></span>
</dt> <dd>

<span data-ttu-id="3968f-111">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3968f-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="3968f-112">Peso de mezcla.</span><span class="sxs-lookup"><span data-stu-id="3968f-112">Blend weight.</span></span>

</dd> <dt>

<span data-ttu-id="3968f-113">**Normal**</span><span class="sxs-lookup"><span data-stu-id="3968f-113">**Normal**</span></span>
</dt> <dd>

<span data-ttu-id="3968f-114">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3968f-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="3968f-115">Normal.</span><span class="sxs-lookup"><span data-stu-id="3968f-115">Normal.</span></span>

</dd> <dt>

<span data-ttu-id="3968f-116">**Difusa**</span><span class="sxs-lookup"><span data-stu-id="3968f-116">**Diffuse**</span></span>
</dt> <dd>

<span data-ttu-id="3968f-117">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3968f-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="3968f-118">Valor de iluminación difusa.</span><span class="sxs-lookup"><span data-stu-id="3968f-118">Diffuse lighting value.</span></span>

</dd> <dt>

<span data-ttu-id="3968f-119">**Especular**</span><span class="sxs-lookup"><span data-stu-id="3968f-119">**Specular**</span></span>
</dt> <dd>

<span data-ttu-id="3968f-120">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3968f-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="3968f-121">Valor de iluminación especular.</span><span class="sxs-lookup"><span data-stu-id="3968f-121">Specular lighting value.</span></span>

</dd> <dt>

<span data-ttu-id="3968f-122">**Texcoord**</span><span class="sxs-lookup"><span data-stu-id="3968f-122">**Texcoord**</span></span>
</dt> <dd>

<span data-ttu-id="3968f-123">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3968f-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="3968f-124">Ocho coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="3968f-124">Eight texture coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="3968f-125">**Tangente**</span><span class="sxs-lookup"><span data-stu-id="3968f-125">**Tangent**</span></span>
</dt> <dd>

<span data-ttu-id="3968f-126">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3968f-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="3968f-127">Tangente.</span><span class="sxs-lookup"><span data-stu-id="3968f-127">Tangent.</span></span>

</dd> <dt>

<span data-ttu-id="3968f-128">**Binormal**</span><span class="sxs-lookup"><span data-stu-id="3968f-128">**Binormal**</span></span>
</dt> <dd>

<span data-ttu-id="3968f-129">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3968f-129">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="3968f-130">Binormal.</span><span class="sxs-lookup"><span data-stu-id="3968f-130">Binormal.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3968f-131">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3968f-131">Remarks</span></span>

<span data-ttu-id="3968f-132">En esta estructura se describe cómo una operación de simplificación considerará los datos de vértices al calcular los costos relativos entre los bordes que se contrae.</span><span class="sxs-lookup"><span data-stu-id="3968f-132">This structure describes how a simplification operation will consider vertex data when calculating relative costs between collapsing edges.</span></span> <span data-ttu-id="3968f-133">Por ejemplo, si el campo Normal es 0,0, la operación de simplificación omitirá el componente normal del vértice al calcular el error para el contraer.</span><span class="sxs-lookup"><span data-stu-id="3968f-133">For example, if the Normal field is 0.0, the simplification operation will ignore the vertex normal component when calculating the error for the collapse.</span></span> <span data-ttu-id="3968f-134">Sin embargo, si el campo Normal es 1.0, la operación de simplificación usará el componente normal del vértice.</span><span class="sxs-lookup"><span data-stu-id="3968f-134">However, if the Normal field is 1.0, the simplification operation will use the vertex normal component.</span></span> <span data-ttu-id="3968f-135">Si el campo Normal es 2.0, duplica la cantidad de errores; si el campo Normal es 4.0, a continuación, se multiplica el número de errores, y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="3968f-135">If the Normal field is 2.0, double the amount of errors; if the Normal field is 4.0, then quadruple the number of errors, and so on.</span></span>

<span data-ttu-id="3968f-136">El tipo LPD3DX ATTRIBUTE WEIGHTS se define como un puntero a la estructura \_ \_ D3DX \_ ATTRIBUTE \_ WEIGHTS.</span><span class="sxs-lookup"><span data-stu-id="3968f-136">The LPD3DX\_ATTRIBUTE\_WEIGHTS type is defined as a pointer to the D3DX\_ATTRIBUTE\_WEIGHTS structure.</span></span>


```
    typedef D3DX_ATTRIBUTE_WEIGHTS* LPD3DX_ATTRIBUTE_WEIGHTS;
```



## <a name="requirements"></a><span data-ttu-id="3968f-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3968f-137">Requirements</span></span>



| <span data-ttu-id="3968f-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="3968f-138">Requirement</span></span> | <span data-ttu-id="3968f-139">Value</span><span class="sxs-lookup"><span data-stu-id="3968f-139">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="3968f-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3968f-140">Header</span></span><br/> | <dl> <span data-ttu-id="3968f-141"><dt>D3DX10.h</dt></span><span class="sxs-lookup"><span data-stu-id="3968f-141"><dt>D3DX10.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3968f-142">Consulte también</span><span class="sxs-lookup"><span data-stu-id="3968f-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3968f-143">Estructuras D3DX</span><span class="sxs-lookup"><span data-stu-id="3968f-143">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
