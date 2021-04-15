---
description: Describe una intersección de triángulo.
ms.assetid: b6f50fc0-2c8a-4efa-a144-bd0851f8b0ca
title: Estructura D3DXINTERSECTINFO (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXINTERSECTINFO
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 31a98e9a7095e81e962b2996dedb9bdf5871533d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707878"
---
# <a name="d3dxintersectinfo-structure"></a><span data-ttu-id="dc113-103">Estructura D3DXINTERSECTINFO</span><span class="sxs-lookup"><span data-stu-id="dc113-103">D3DXINTERSECTINFO structure</span></span>

<span data-ttu-id="dc113-104">Describe una intersección de triángulo.</span><span class="sxs-lookup"><span data-stu-id="dc113-104">Describes a ray-triangle intersection.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc113-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dc113-105">Syntax</span></span>


```C++
typedef struct D3DXINTERSECTINFO {
  DWORD FaceIndex;
  FLOAT U;
  FLOAT V;
  FLOAT Dist;
} D3DXINTERSECTINFO, *LPD3DXINTERSECTINFO;
```



## <a name="members"></a><span data-ttu-id="dc113-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="dc113-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="dc113-107">**FaceIndex**</span><span class="sxs-lookup"><span data-stu-id="dc113-107">**FaceIndex**</span></span>
</dt> <dd>

<span data-ttu-id="dc113-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dc113-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="dc113-109">Índice del triángulo que ha alcanzado el rayo.</span><span class="sxs-lookup"><span data-stu-id="dc113-109">Index of the triangle that hit the ray.</span></span>

</dd> <dt>

<span data-ttu-id="dc113-110">**U**</span><span class="sxs-lookup"><span data-stu-id="dc113-110">**U**</span></span>
</dt> <dd>

<span data-ttu-id="dc113-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dc113-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="dc113-112">Coordenada de Barycentric dentro del triángulo en el que se corta el rayo.</span><span class="sxs-lookup"><span data-stu-id="dc113-112">Barycentric coordinate within the triangle where the ray intersects.</span></span>

</dd> <dt>

<span data-ttu-id="dc113-113">**V**</span><span class="sxs-lookup"><span data-stu-id="dc113-113">**V**</span></span>
</dt> <dd>

<span data-ttu-id="dc113-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dc113-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="dc113-115">Coordenada de Barycentric dentro del triángulo en el que se corta el rayo.</span><span class="sxs-lookup"><span data-stu-id="dc113-115">Barycentric coordinate within the triangle where the ray intersects.</span></span>

</dd> <dt>

<span data-ttu-id="dc113-116">**Tribu**</span><span class="sxs-lookup"><span data-stu-id="dc113-116">**Dist**</span></span>
</dt> <dd>

<span data-ttu-id="dc113-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dc113-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="dc113-118">Distancia a lo largo del rayo en el que se produjo la intersección.</span><span class="sxs-lookup"><span data-stu-id="dc113-118">Distance along the ray where the intersection occurred.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dc113-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dc113-119">Remarks</span></span>

<span data-ttu-id="dc113-120">Las coordenadas Barycentric definen un punto dentro de un triángulo en cuanto a los vértices del triángulo.</span><span class="sxs-lookup"><span data-stu-id="dc113-120">Barycentric coordinates define a point inside a triangle in terms of the triangle's vertices.</span></span> <span data-ttu-id="dc113-121">Para obtener una descripción más detallada de las coordenadas de Barycentric, consulte Descripción de las [coordenadas del Barycentric de Wolfram](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span><span class="sxs-lookup"><span data-stu-id="dc113-121">For a more in-depth description of barycentric coordinates, see [Mathworld's Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span></span>

## <a name="requirements"></a><span data-ttu-id="dc113-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dc113-122">Requirements</span></span>



| <span data-ttu-id="dc113-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="dc113-123">Requirement</span></span> | <span data-ttu-id="dc113-124">Value</span><span class="sxs-lookup"><span data-stu-id="dc113-124">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="dc113-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="dc113-125">Header</span></span><br/> | <dl> <span data-ttu-id="dc113-126"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="dc113-126"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc113-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="dc113-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc113-128">Estructuras de D3DX</span><span class="sxs-lookup"><span data-stu-id="dc113-128">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
