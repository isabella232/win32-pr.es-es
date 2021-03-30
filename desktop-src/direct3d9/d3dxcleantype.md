---
description: Define las operaciones que se deben realizar en los vértices como preparación para la limpieza de malla.
ms.assetid: f222acaa-fa82-4591-b7c2-b520cb648ed5
title: Enumeración D3DXCLEANTYPE (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCLEANTYPE
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: b38578d0f50521def552b8bd6608c2696b405d0f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280363"
---
# <a name="d3dxcleantype-enumeration"></a><span data-ttu-id="3d08f-103">Enumeración D3DXCLEANTYPE</span><span class="sxs-lookup"><span data-stu-id="3d08f-103">D3DXCLEANTYPE enumeration</span></span>

<span data-ttu-id="3d08f-104">Define las operaciones que se deben realizar en los vértices como preparación para la limpieza de malla.</span><span class="sxs-lookup"><span data-stu-id="3d08f-104">Defines operations to perform on vertices in preparation for mesh cleaning.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d08f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3d08f-105">Syntax</span></span>


```C++
typedef enum D3DXCLEANTYPE { 
  D3DXCLEAN_BACKFACING      = 1,
  D3DXCLEAN_BOWTIES         = 2,
  D3DXCLEAN_SKINNING        = D3DXCLEAN_BACKFACING,
  D3DXCLEAN_OPTIMIZATION    = D3DXCLEAN_BACKFACING,
  D3DXCLEAN_SIMPLIFICATION  = D3DXCLEAN_BACKFACING | D3DXCLEAN_BOWTIES
} D3DXCLEANTYPE, *LPD3DXCLEANTYPE;
```



## <a name="constants"></a><span data-ttu-id="3d08f-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="3d08f-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="3d08f-107"><span id="D3DXCLEAN_BACKFACING"></span><span id="d3dxclean_backfacing"></span>**D3DXCLEAN \_**</span><span class="sxs-lookup"><span data-stu-id="3d08f-107"><span id="D3DXCLEAN_BACKFACING"></span><span id="d3dxclean_backfacing"></span>**D3DXCLEAN\_BACKFACING**</span></span>
</dt> <dd>

<span data-ttu-id="3d08f-108">Mezclar triángulos que compartan los mismos índices de vértices pero que tengan caras normales que señalen a direcciones opuestas (triángulos hacia delante).</span><span class="sxs-lookup"><span data-stu-id="3d08f-108">Merge triangles that share the same vertex indices but have face normals pointing in opposite directions (back-facing triangles).</span></span> <span data-ttu-id="3d08f-109">A menos que los triángulos no se dividan agregando un vértice replicado, los datos de proximidad de la malla de los dos triángulos pueden entrar en conflicto.</span><span class="sxs-lookup"><span data-stu-id="3d08f-109">Unless the triangles are not split by adding a replicated vertex, mesh adjacency data from the two triangles may conflict.</span></span>

</dd> <dt>

<span data-ttu-id="3d08f-110"><span id="D3DXCLEAN_BOWTIES"></span><span id="d3dxclean_bowties"></span>**D3DXCLEAN \_ pajaritas**</span><span class="sxs-lookup"><span data-stu-id="3d08f-110"><span id="D3DXCLEAN_BOWTIES"></span><span id="d3dxclean_bowties"></span>**D3DXCLEAN\_BOWTIES**</span></span>
</dt> <dd>

<span data-ttu-id="3d08f-111">Si un vértice es el vértice de dos ventiladores de triángulo (una pajarita) y las operaciones de malla afectan a uno de los ventiladores, divida el vértice compartido en dos nuevos vértices.</span><span class="sxs-lookup"><span data-stu-id="3d08f-111">If a vertex is the apex of two triangle fans (a bowtie) and mesh operations will affect one of the fans, then split the shared vertex into two new vertices.</span></span> <span data-ttu-id="3d08f-112">Las Pajaritas pueden causar problemas en operaciones como la simplificación de malla que quitan vértices, ya que la eliminación de un vértice afecta a dos conjuntos distintos de triángulos.</span><span class="sxs-lookup"><span data-stu-id="3d08f-112">Bowties can cause problems for operations such as mesh simplification that remove vertices, because removing one vertex affects two distinct sets of triangles.</span></span>

</dd> <dt>

<span data-ttu-id="3d08f-113"><span id="D3DXCLEAN_SKINNING"></span><span id="d3dxclean_skinning"></span>**D3DXCLEAN de la \_ piel**</span><span class="sxs-lookup"><span data-stu-id="3d08f-113"><span id="D3DXCLEAN_SKINNING"></span><span id="d3dxclean_skinning"></span>**D3DXCLEAN\_SKINNING**</span></span>
</dt> <dd>

<span data-ttu-id="3d08f-114">Use esta marca para evitar bucles infinitos durante las operaciones de malla de configuración de la piel.</span><span class="sxs-lookup"><span data-stu-id="3d08f-114">Use this flag to prevent infinite loops during skinning setup mesh operations.</span></span>

</dd> <dt>

<span data-ttu-id="3d08f-115"><span id="D3DXCLEAN_OPTIMIZATION"></span><span id="d3dxclean_optimization"></span>**Optimización de D3DXCLEAN \_**</span><span class="sxs-lookup"><span data-stu-id="3d08f-115"><span id="D3DXCLEAN_OPTIMIZATION"></span><span id="d3dxclean_optimization"></span>**D3DXCLEAN\_OPTIMIZATION**</span></span>
</dt> <dd>

<span data-ttu-id="3d08f-116">Use esta marca para evitar bucles infinitos durante las operaciones de optimización de malla.</span><span class="sxs-lookup"><span data-stu-id="3d08f-116">Use this flag to prevent infinite loops during mesh optimization operations.</span></span>

</dd> <dt>

<span data-ttu-id="3d08f-117"><span id="D3DXCLEAN_SIMPLIFICATION"></span><span id="d3dxclean_simplification"></span>**\_Simplificación de D3DXCLEAN**</span><span class="sxs-lookup"><span data-stu-id="3d08f-117"><span id="D3DXCLEAN_SIMPLIFICATION"></span><span id="d3dxclean_simplification"></span>**D3DXCLEAN\_SIMPLIFICATION**</span></span>
</dt> <dd>

<span data-ttu-id="3d08f-118">Use esta marca para evitar bucles infinitos durante las operaciones de simplificación de malla.</span><span class="sxs-lookup"><span data-stu-id="3d08f-118">Use this flag to prevent infinite loops during mesh simplification operations.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3d08f-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3d08f-119">Requirements</span></span>



| <span data-ttu-id="3d08f-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="3d08f-120">Requirement</span></span> | <span data-ttu-id="3d08f-121">Value</span><span class="sxs-lookup"><span data-stu-id="3d08f-121">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3d08f-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3d08f-122">Header</span></span><br/> | <dl> <span data-ttu-id="3d08f-123"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="3d08f-123"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d08f-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="3d08f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d08f-125">Enumeraciones de D3DX</span><span class="sxs-lookup"><span data-stu-id="3d08f-125">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




