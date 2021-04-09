---
description: Describe una intersección de triángulo.
ms.assetid: 21658b74-6f1d-4a16-a8b3-0c7bb6edf899
title: D3DX10_INTERSECT_INFO estructura (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_INTERSECT_INFO
api_type:
- HeaderDef
api_location:
- D3DX10.h
ms.openlocfilehash: 87490e734299cba57952bb43d1ee4ffad8e014c8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821175"
---
# <a name="d3dx10_intersect_info-structure"></a><span data-ttu-id="827aa-103">D3DX10 \_ estructura de información de intersección \_</span><span class="sxs-lookup"><span data-stu-id="827aa-103">D3DX10\_INTERSECT\_INFO structure</span></span>

<span data-ttu-id="827aa-104">Describe una intersección de triángulo.</span><span class="sxs-lookup"><span data-stu-id="827aa-104">Describes a ray-triangle intersection.</span></span>

## <a name="syntax"></a><span data-ttu-id="827aa-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="827aa-105">Syntax</span></span>


```C++
typedef struct D3DX10_INTERSECT_INFO {
  UINT  FaceIndex;
  FLOAT U;
  FLOAT V;
  FLOAT Dist;
} D3DX10_INTERSECT_INFO, *LPD3DX10_INTERSECT_INFO;
```



## <a name="members"></a><span data-ttu-id="827aa-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="827aa-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="827aa-107">**FaceIndex**</span><span class="sxs-lookup"><span data-stu-id="827aa-107">**FaceIndex**</span></span>
</dt> <dd>

<span data-ttu-id="827aa-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="827aa-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="827aa-109">Índice del triángulo que ha alcanzado el rayo.</span><span class="sxs-lookup"><span data-stu-id="827aa-109">Index of the triangle that hit the ray.</span></span>

</dd> <dt>

<span data-ttu-id="827aa-110">**U**</span><span class="sxs-lookup"><span data-stu-id="827aa-110">**U**</span></span>
</dt> <dd>

<span data-ttu-id="827aa-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="827aa-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="827aa-112">Coordenada de Barycentric dentro del triángulo en el que se corta el rayo.</span><span class="sxs-lookup"><span data-stu-id="827aa-112">Barycentric coordinate within the triangle where the ray intersects.</span></span>

</dd> <dt>

<span data-ttu-id="827aa-113">**V**</span><span class="sxs-lookup"><span data-stu-id="827aa-113">**V**</span></span>
</dt> <dd>

<span data-ttu-id="827aa-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="827aa-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="827aa-115">Coordenada de Barycentric dentro del triángulo en el que se corta el rayo.</span><span class="sxs-lookup"><span data-stu-id="827aa-115">Barycentric coordinate within the triangle where the ray intersects.</span></span>

</dd> <dt>

<span data-ttu-id="827aa-116">**Tribu**</span><span class="sxs-lookup"><span data-stu-id="827aa-116">**Dist**</span></span>
</dt> <dd>

<span data-ttu-id="827aa-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="827aa-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="827aa-118">Distancia a lo largo del rayo en el que se produjo la intersección.</span><span class="sxs-lookup"><span data-stu-id="827aa-118">Distance along the ray where the intersection occurred.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="827aa-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="827aa-119">Remarks</span></span>

<span data-ttu-id="827aa-120">Las coordenadas Barycentric definen un punto dentro de un triángulo en cuanto a los vértices del triángulo.</span><span class="sxs-lookup"><span data-stu-id="827aa-120">Barycentric coordinates define a point inside a triangle in terms of the triangle's vertices.</span></span> <span data-ttu-id="827aa-121">Para obtener una descripción más detallada de las coordenadas de Barycentric, consulte Descripción de las [coordenadas del Barycentric de Wolfram](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span><span class="sxs-lookup"><span data-stu-id="827aa-121">For a more in-depth description of barycentric coordinates, see [Mathworld's Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span></span>

## <a name="requirements"></a><span data-ttu-id="827aa-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="827aa-122">Requirements</span></span>



| <span data-ttu-id="827aa-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="827aa-123">Requirement</span></span> | <span data-ttu-id="827aa-124">Value</span><span class="sxs-lookup"><span data-stu-id="827aa-124">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="827aa-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="827aa-125">Header</span></span><br/> | <dl> <span data-ttu-id="827aa-126"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="827aa-126"><dt>D3DX10.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="827aa-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="827aa-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="827aa-128">Estructuras de D3DX</span><span class="sxs-lookup"><span data-stu-id="827aa-128">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
