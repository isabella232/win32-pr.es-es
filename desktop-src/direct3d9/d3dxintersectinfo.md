---
description: 'Estructura D3DXINTERSECTINFO: describe una intersección de triángulo de rayo.'
ms.assetid: b6f50fc0-2c8a-4efa-a144-bd0851f8b0ca
title: Estructura D3DXINTERSECTINFO (D3dx9mesh.h)
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
ms.openlocfilehash: f4a63c7f4a479bfbe9dcb49f485ce0acb8db6486
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098293"
---
# <a name="d3dxintersectinfo-structure"></a><span data-ttu-id="0bbbb-103">D3DXINTERSECTINFO (estructura)</span><span class="sxs-lookup"><span data-stu-id="0bbbb-103">D3DXINTERSECTINFO structure</span></span>

<span data-ttu-id="0bbbb-104">Describe una intersección de triángulo de rayo.</span><span class="sxs-lookup"><span data-stu-id="0bbbb-104">Describes a ray-triangle intersection.</span></span>

## <a name="syntax"></a><span data-ttu-id="0bbbb-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0bbbb-105">Syntax</span></span>


```C++
typedef struct D3DXINTERSECTINFO {
  DWORD FaceIndex;
  FLOAT U;
  FLOAT V;
  FLOAT Dist;
} D3DXINTERSECTINFO, *LPD3DXINTERSECTINFO;
```



## <a name="members"></a><span data-ttu-id="0bbbb-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="0bbbb-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="0bbbb-107">**FaceIndex**</span><span class="sxs-lookup"><span data-stu-id="0bbbb-107">**FaceIndex**</span></span>
</dt> <dd>

<span data-ttu-id="0bbbb-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0bbbb-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="0bbbb-109">Índice del triángulo que alcanzó el rayo.</span><span class="sxs-lookup"><span data-stu-id="0bbbb-109">Index of the triangle that hit the ray.</span></span>

</dd> <dt>

<span data-ttu-id="0bbbb-110">**U**</span><span class="sxs-lookup"><span data-stu-id="0bbbb-110">**U**</span></span>
</dt> <dd>

<span data-ttu-id="0bbbb-111">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0bbbb-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="0bbbb-112">Coordenada centrada en barras dentro del triángulo donde el rayo forma intersección.</span><span class="sxs-lookup"><span data-stu-id="0bbbb-112">Barycentric coordinate within the triangle where the ray intersects.</span></span>

</dd> <dt>

<span data-ttu-id="0bbbb-113">**V**</span><span class="sxs-lookup"><span data-stu-id="0bbbb-113">**V**</span></span>
</dt> <dd>

<span data-ttu-id="0bbbb-114">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0bbbb-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="0bbbb-115">Coordenada centrada en barras dentro del triángulo donde el rayo forma intersección.</span><span class="sxs-lookup"><span data-stu-id="0bbbb-115">Barycentric coordinate within the triangle where the ray intersects.</span></span>

</dd> <dt>

<span data-ttu-id="0bbbb-116">**Dist**</span><span class="sxs-lookup"><span data-stu-id="0bbbb-116">**Dist**</span></span>
</dt> <dd>

<span data-ttu-id="0bbbb-117">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0bbbb-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="0bbbb-118">Distancia a lo largo del rayo donde se produjo la intersección.</span><span class="sxs-lookup"><span data-stu-id="0bbbb-118">Distance along the ray where the intersection occurred.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0bbbb-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0bbbb-119">Remarks</span></span>

<span data-ttu-id="0bbbb-120">Las coordenadas centradas en barras definen un punto dentro de un triángulo en términos de los vértices del triángulo.</span><span class="sxs-lookup"><span data-stu-id="0bbbb-120">Barycentric coordinates define a point inside a triangle in terms of the triangle's vertices.</span></span> <span data-ttu-id="0bbbb-121">Para obtener una descripción más detallada de las coordenadas centradas en barras, vea [Mathworld's Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span><span class="sxs-lookup"><span data-stu-id="0bbbb-121">For a more in-depth description of barycentric coordinates, see [Mathworld's Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span></span>

## <a name="requirements"></a><span data-ttu-id="0bbbb-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0bbbb-122">Requirements</span></span>



| <span data-ttu-id="0bbbb-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="0bbbb-123">Requirement</span></span> | <span data-ttu-id="0bbbb-124">Value</span><span class="sxs-lookup"><span data-stu-id="0bbbb-124">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0bbbb-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0bbbb-125">Header</span></span><br/> | <dl> <span data-ttu-id="0bbbb-126"><dt>D3dx9mesh.h</dt></span><span class="sxs-lookup"><span data-stu-id="0bbbb-126"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0bbbb-127">Consulte también</span><span class="sxs-lookup"><span data-stu-id="0bbbb-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0bbbb-128">Estructuras D3DX</span><span class="sxs-lookup"><span data-stu-id="0bbbb-128">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
