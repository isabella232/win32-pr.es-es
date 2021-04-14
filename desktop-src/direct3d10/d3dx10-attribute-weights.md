---
description: Especifica los atributos de peso de la malla.
ms.assetid: 554bb8f2-9e92-4e9e-b500-c3cc47d57830
title: D3DX10_ATTRIBUTE_WEIGHTS estructura (D3DX10. h)
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
ms.openlocfilehash: 4f137c1ecc29c184c4dec3995fb0202741ce9f09
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362621"
---
# <a name="d3dx10_attribute_weights-structure"></a><span data-ttu-id="e59db-103">Estructura de pesos del \_ atributo D3DX10 \_</span><span class="sxs-lookup"><span data-stu-id="e59db-103">D3DX10\_ATTRIBUTE\_WEIGHTS structure</span></span>

<span data-ttu-id="e59db-104">Especifica los atributos de peso de la malla.</span><span class="sxs-lookup"><span data-stu-id="e59db-104">Specifies mesh weight attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="e59db-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e59db-105">Syntax</span></span>


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



## <a name="members"></a><span data-ttu-id="e59db-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="e59db-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="e59db-107">**Position**</span><span class="sxs-lookup"><span data-stu-id="e59db-107">**Position**</span></span>
</dt> <dd>

<span data-ttu-id="e59db-108">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e59db-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e59db-109">Ubicación.</span><span class="sxs-lookup"><span data-stu-id="e59db-109">Position.</span></span>

</dd> <dt>

<span data-ttu-id="e59db-110">**Límite**</span><span class="sxs-lookup"><span data-stu-id="e59db-110">**Boundary**</span></span>
</dt> <dd>

<span data-ttu-id="e59db-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e59db-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e59db-112">Peso de la mezcla.</span><span class="sxs-lookup"><span data-stu-id="e59db-112">Blend weight.</span></span>

</dd> <dt>

<span data-ttu-id="e59db-113">**Normal**</span><span class="sxs-lookup"><span data-stu-id="e59db-113">**Normal**</span></span>
</dt> <dd>

<span data-ttu-id="e59db-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e59db-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e59db-115">Normal.</span><span class="sxs-lookup"><span data-stu-id="e59db-115">Normal.</span></span>

</dd> <dt>

<span data-ttu-id="e59db-116">**Difusa**</span><span class="sxs-lookup"><span data-stu-id="e59db-116">**Diffuse**</span></span>
</dt> <dd>

<span data-ttu-id="e59db-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e59db-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e59db-118">Valor de iluminación difusa.</span><span class="sxs-lookup"><span data-stu-id="e59db-118">Diffuse lighting value.</span></span>

</dd> <dt>

<span data-ttu-id="e59db-119">**Especular**</span><span class="sxs-lookup"><span data-stu-id="e59db-119">**Specular**</span></span>
</dt> <dd>

<span data-ttu-id="e59db-120">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e59db-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e59db-121">Valor de iluminación especular.</span><span class="sxs-lookup"><span data-stu-id="e59db-121">Specular lighting value.</span></span>

</dd> <dt>

<span data-ttu-id="e59db-122">**Texcoord**</span><span class="sxs-lookup"><span data-stu-id="e59db-122">**Texcoord**</span></span>
</dt> <dd>

<span data-ttu-id="e59db-123">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e59db-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e59db-124">Ocho coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="e59db-124">Eight texture coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="e59db-125">**Tangente**</span><span class="sxs-lookup"><span data-stu-id="e59db-125">**Tangent**</span></span>
</dt> <dd>

<span data-ttu-id="e59db-126">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e59db-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e59db-127">Tangente.</span><span class="sxs-lookup"><span data-stu-id="e59db-127">Tangent.</span></span>

</dd> <dt>

<span data-ttu-id="e59db-128">**Binormalización**</span><span class="sxs-lookup"><span data-stu-id="e59db-128">**Binormal**</span></span>
</dt> <dd>

<span data-ttu-id="e59db-129">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e59db-129">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e59db-130">Binormal.</span><span class="sxs-lookup"><span data-stu-id="e59db-130">Binormal.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e59db-131">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e59db-131">Remarks</span></span>

<span data-ttu-id="e59db-132">En esta estructura se describe cómo una operación de simplificación considerará los datos de vértices al calcular los costos relativos entre los bordes contraídos.</span><span class="sxs-lookup"><span data-stu-id="e59db-132">This structure describes how a simplification operation will consider vertex data when calculating relative costs between collapsing edges.</span></span> <span data-ttu-id="e59db-133">Por ejemplo, si el campo normal es 0,0, la operación de simplificación omitirá el componente normal del vértice al calcular el error de la acción de contraer.</span><span class="sxs-lookup"><span data-stu-id="e59db-133">For example, if the Normal field is 0.0, the simplification operation will ignore the vertex normal component when calculating the error for the collapse.</span></span> <span data-ttu-id="e59db-134">Sin embargo, si el campo normal es 1,0, la operación de simplificación usará el componente normal de vértice.</span><span class="sxs-lookup"><span data-stu-id="e59db-134">However, if the Normal field is 1.0, the simplification operation will use the vertex normal component.</span></span> <span data-ttu-id="e59db-135">Si el campo normal es 2,0, duplique la cantidad de errores; Si el campo normal es 4,0, cuádruple el número de errores, etc.</span><span class="sxs-lookup"><span data-stu-id="e59db-135">If the Normal field is 2.0, double the amount of errors; if the Normal field is 4.0, then quadruple the number of errors, and so on.</span></span>

<span data-ttu-id="e59db-136">El \_ tipo de pesos del atributo LPD3DX \_ se define como un puntero a la \_ estructura de pesos del atributo D3DX \_ .</span><span class="sxs-lookup"><span data-stu-id="e59db-136">The LPD3DX\_ATTRIBUTE\_WEIGHTS type is defined as a pointer to the D3DX\_ATTRIBUTE\_WEIGHTS structure.</span></span>


```
    typedef D3DX_ATTRIBUTE_WEIGHTS* LPD3DX_ATTRIBUTE_WEIGHTS;
```



## <a name="requirements"></a><span data-ttu-id="e59db-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e59db-137">Requirements</span></span>



| <span data-ttu-id="e59db-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="e59db-138">Requirement</span></span> | <span data-ttu-id="e59db-139">Value</span><span class="sxs-lookup"><span data-stu-id="e59db-139">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="e59db-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e59db-140">Header</span></span><br/> | <dl> <span data-ttu-id="e59db-141"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="e59db-141"><dt>D3DX10.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e59db-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="e59db-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e59db-143">Estructuras de D3DX</span><span class="sxs-lookup"><span data-stu-id="e59db-143">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
