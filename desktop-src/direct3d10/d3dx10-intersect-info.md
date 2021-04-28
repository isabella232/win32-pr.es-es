---
description: 'D3DX10_INTERSECT_INFO estructura: describe una intersección de triángulo de rayo.'
ms.assetid: 21658b74-6f1d-4a16-a8b3-0c7bb6edf899
title: D3DX10_INTERSECT_INFO estructura (D3DX10.h)
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
ms.openlocfilehash: 203daa48e766edd545bf232c4f8d94c4f17b5b2a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105463"
---
# <a name="d3dx10_intersect_info-structure"></a><span data-ttu-id="327b6-103">Estructura INFO de INTERSECT de D3DX10 \_ \_</span><span class="sxs-lookup"><span data-stu-id="327b6-103">D3DX10\_INTERSECT\_INFO structure</span></span>

<span data-ttu-id="327b6-104">Describe una intersección de triángulo de rayo.</span><span class="sxs-lookup"><span data-stu-id="327b6-104">Describes a ray-triangle intersection.</span></span>

## <a name="syntax"></a><span data-ttu-id="327b6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="327b6-105">Syntax</span></span>


```C++
typedef struct D3DX10_INTERSECT_INFO {
  UINT  FaceIndex;
  FLOAT U;
  FLOAT V;
  FLOAT Dist;
} D3DX10_INTERSECT_INFO, *LPD3DX10_INTERSECT_INFO;
```



## <a name="members"></a><span data-ttu-id="327b6-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="327b6-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="327b6-107">**FaceIndex**</span><span class="sxs-lookup"><span data-stu-id="327b6-107">**FaceIndex**</span></span>
</dt> <dd>

<span data-ttu-id="327b6-108">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="327b6-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="327b6-109">Índice del triángulo que alcanzó el rayo.</span><span class="sxs-lookup"><span data-stu-id="327b6-109">Index of the triangle that hit the ray.</span></span>

</dd> <dt>

<span data-ttu-id="327b6-110">**U**</span><span class="sxs-lookup"><span data-stu-id="327b6-110">**U**</span></span>
</dt> <dd>

<span data-ttu-id="327b6-111">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="327b6-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="327b6-112">Coordenada centrada en el triángulo en el que el rayo forma intersección.</span><span class="sxs-lookup"><span data-stu-id="327b6-112">Barycentric coordinate within the triangle where the ray intersects.</span></span>

</dd> <dt>

<span data-ttu-id="327b6-113">**V**</span><span class="sxs-lookup"><span data-stu-id="327b6-113">**V**</span></span>
</dt> <dd>

<span data-ttu-id="327b6-114">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="327b6-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="327b6-115">Coordenada centrada en el triángulo en el que el rayo forma intersección.</span><span class="sxs-lookup"><span data-stu-id="327b6-115">Barycentric coordinate within the triangle where the ray intersects.</span></span>

</dd> <dt>

<span data-ttu-id="327b6-116">**Dist**</span><span class="sxs-lookup"><span data-stu-id="327b6-116">**Dist**</span></span>
</dt> <dd>

<span data-ttu-id="327b6-117">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="327b6-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="327b6-118">Distancia a lo largo del rayo donde se produjo la intersección.</span><span class="sxs-lookup"><span data-stu-id="327b6-118">Distance along the ray where the intersection occurred.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="327b6-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="327b6-119">Remarks</span></span>

<span data-ttu-id="327b6-120">Las coordenadas barítricas definen un punto dentro de un triángulo en términos de los vértices del triángulo.</span><span class="sxs-lookup"><span data-stu-id="327b6-120">Barycentric coordinates define a point inside a triangle in terms of the triangle's vertices.</span></span> <span data-ttu-id="327b6-121">Para obtener una descripción más detallada de las coordenadas baricéntricas, vea [Mathworld's Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span><span class="sxs-lookup"><span data-stu-id="327b6-121">For a more in-depth description of barycentric coordinates, see [Mathworld's Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span></span>

## <a name="requirements"></a><span data-ttu-id="327b6-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="327b6-122">Requirements</span></span>



| <span data-ttu-id="327b6-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="327b6-123">Requirement</span></span> | <span data-ttu-id="327b6-124">Value</span><span class="sxs-lookup"><span data-stu-id="327b6-124">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="327b6-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="327b6-125">Header</span></span><br/> | <dl> <span data-ttu-id="327b6-126"><dt>D3DX10.h</dt></span><span class="sxs-lookup"><span data-stu-id="327b6-126"><dt>D3DX10.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="327b6-127">Consulte también</span><span class="sxs-lookup"><span data-stu-id="327b6-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="327b6-128">Estructuras D3DX</span><span class="sxs-lookup"><span data-stu-id="327b6-128">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
