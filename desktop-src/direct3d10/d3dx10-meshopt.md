---
description: Especifica el tipo de optimización de malla que se va a realizar.
ms.assetid: 20d1da8c-8c3d-4045-9a37-d534a8682716
title: Enumeración D3DX10_MESHOPT (D3DX10Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_MESHOPT
api_type:
- HeaderDef
api_location:
- D3DX10Mesh.h
ms.openlocfilehash: c8ccb13da1549b7e2eeeb67ebf7899c2187be363
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362711"
---
# <a name="d3dx10_meshopt-enumeration"></a><span data-ttu-id="06c40-103">\_Enumeración de D3DX10 MESHOPT</span><span class="sxs-lookup"><span data-stu-id="06c40-103">D3DX10\_MESHOPT enumeration</span></span>

<span data-ttu-id="06c40-104">Especifica el tipo de optimización de malla que se va a realizar.</span><span class="sxs-lookup"><span data-stu-id="06c40-104">Specifies the type of mesh optimization to be performed.</span></span>

## <a name="syntax"></a><span data-ttu-id="06c40-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="06c40-105">Syntax</span></span>


```C++
typedef enum D3DX10_MESHOPT { 
  D3DX10_MESHOPT_COMPACT             = 0x01000000,
  D3DX10_MESHOPT_ATTR_SORT           = 0x02000000,
  D3DX10_MESHOPT_VERTEX_CACHE        = 0x04000000,
  D3DX10_MESHOPT_STRIP_REORDER       = 0x08000000,
  D3DX10_MESHOPT_IGNORE_VERTS        = 0x10000000,
  D3DX10_MESHOPT_DO_NOT_SPLIT        = 0x20000000,
  D3DX10_MESHOPT_DEVICE_INDEPENDENT  = 0x00400000
} D3DX10_MESHOPT, *LPD3DX10_MESHOPT;
```



## <a name="constants"></a><span data-ttu-id="06c40-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="06c40-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="06c40-107"><span id="D3DX10_MESHOPT_COMPACT"></span><span id="d3dx10_meshopt_compact"></span>**D3DX10 \_ MESHOPT \_ Compact**</span><span class="sxs-lookup"><span data-stu-id="06c40-107"><span id="D3DX10_MESHOPT_COMPACT"></span><span id="d3dx10_meshopt_compact"></span>**D3DX10\_MESHOPT\_COMPACT**</span></span>
</dt> <dd>

<span data-ttu-id="06c40-108">Reordena las caras para quitar los vértices y caras sin usar.</span><span class="sxs-lookup"><span data-stu-id="06c40-108">Reorders faces to remove unused vertices and faces.</span></span>

</dd> <dt>

<span data-ttu-id="06c40-109"><span id="D3DX10_MESHOPT_ATTR_SORT"></span><span id="d3dx10_meshopt_attr_sort"></span>**D3DX10 \_ MESHOPT \_ ATTR \_ Sort**</span><span class="sxs-lookup"><span data-stu-id="06c40-109"><span id="D3DX10_MESHOPT_ATTR_SORT"></span><span id="d3dx10_meshopt_attr_sort"></span>**D3DX10\_MESHOPT\_ATTR\_SORT**</span></span>
</dt> <dd>

<span data-ttu-id="06c40-110">Reordena las caras para optimizar menos cambios de estado de agrupación de atributos y rendimiento de DrawSubset mejorado.</span><span class="sxs-lookup"><span data-stu-id="06c40-110">Reorders faces to optimize for fewer attribute bundle state changes and enhanced DrawSubset performance.</span></span>

</dd> <dt>

<span data-ttu-id="06c40-111"><span id="D3DX10_MESHOPT_VERTEX_CACHE"></span><span id="d3dx10_meshopt_vertex_cache"></span>**D3DX10 \_ MESHOPT \_ Vertex \_ Cache**</span><span class="sxs-lookup"><span data-stu-id="06c40-111"><span id="D3DX10_MESHOPT_VERTEX_CACHE"></span><span id="d3dx10_meshopt_vertex_cache"></span>**D3DX10\_MESHOPT\_VERTEX\_CACHE**</span></span>
</dt> <dd>

<span data-ttu-id="06c40-112">Reordena las caras para aumentar la tasa de aciertos de caché de los vértices.</span><span class="sxs-lookup"><span data-stu-id="06c40-112">Reorders faces to increase the cache hit rate of vertex caches.</span></span>

</dd> <dt>

<span data-ttu-id="06c40-113"><span id="D3DX10_MESHOPT_STRIP_REORDER"></span><span id="d3dx10_meshopt_strip_reorder"></span>**Reordenación de D3DX10 \_ MESHOPT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="06c40-113"><span id="D3DX10_MESHOPT_STRIP_REORDER"></span><span id="d3dx10_meshopt_strip_reorder"></span>**D3DX10\_MESHOPT\_STRIP\_REORDER**</span></span>
</dt> <dd>

<span data-ttu-id="06c40-114">Reordena las caras para maximizar la longitud de los triángulos adyacentes.</span><span class="sxs-lookup"><span data-stu-id="06c40-114">Reorders faces to maximize length of adjacent triangles.</span></span>

</dd> <dt>

<span data-ttu-id="06c40-115"><span id="D3DX10_MESHOPT_IGNORE_VERTS"></span><span id="d3dx10_meshopt_ignore_verts"></span>**D3DX10 \_ MESHOPT \_ Ignore \_ VERTS**</span><span class="sxs-lookup"><span data-stu-id="06c40-115"><span id="D3DX10_MESHOPT_IGNORE_VERTS"></span><span id="d3dx10_meshopt_ignore_verts"></span>**D3DX10\_MESHOPT\_IGNORE\_VERTS**</span></span>
</dt> <dd>

<span data-ttu-id="06c40-116">Optimizar solo las caras; no optimice los vértices.</span><span class="sxs-lookup"><span data-stu-id="06c40-116">Optimize the faces only; do not optimize the vertices.</span></span>

</dd> <dt>

<span data-ttu-id="06c40-117"><span id="D3DX10_MESHOPT_DO_NOT_SPLIT"></span><span id="d3dx10_meshopt_do_not_split"></span>**D3DX10 \_ MESHOPT \_ \_ no se \_ divide**</span><span class="sxs-lookup"><span data-stu-id="06c40-117"><span id="D3DX10_MESHOPT_DO_NOT_SPLIT"></span><span id="d3dx10_meshopt_do_not_split"></span>**D3DX10\_MESHOPT\_DO\_NOT\_SPLIT**</span></span>
</dt> <dd>

<span data-ttu-id="06c40-118">Mientras se ordena el atributo, no divida los vértices que se comparten entre los grupos de atributos.</span><span class="sxs-lookup"><span data-stu-id="06c40-118">While attribute sorting, do not split vertices that are shared between attribute groups.</span></span>

</dd> <dt>

<span data-ttu-id="06c40-119"><span id="D3DX10_MESHOPT_DEVICE_INDEPENDENT"></span><span id="d3dx10_meshopt_device_independent"></span>**\_Independiente del \_ dispositivo \_ MESHOPT de D3DX10**</span><span class="sxs-lookup"><span data-stu-id="06c40-119"><span id="D3DX10_MESHOPT_DEVICE_INDEPENDENT"></span><span id="d3dx10_meshopt_device_independent"></span>**D3DX10\_MESHOPT\_DEVICE\_INDEPENDENT**</span></span>
</dt> <dd>

<span data-ttu-id="06c40-120">Afecta al tamaño de la caché de vértices.</span><span class="sxs-lookup"><span data-stu-id="06c40-120">Affects the vertex cache size.</span></span> <span data-ttu-id="06c40-121">El uso de esta marca especifica un tamaño de caché de vértices predeterminado que funciona bien en el hardware heredado.</span><span class="sxs-lookup"><span data-stu-id="06c40-121">Using this flag specifies a default vertex cache size that works well on legacy hardware.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="06c40-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="06c40-122">Remarks</span></span>

<span data-ttu-id="06c40-123">Las \_ marcas de optimización D3DXMESHOPT STRIPREORDER y D3DXMESHOPT \_ VERTEXCACHE se excluyen mutuamente.</span><span class="sxs-lookup"><span data-stu-id="06c40-123">The D3DXMESHOPT\_STRIPREORDER and D3DXMESHOPT\_VERTEXCACHE optimization flags are mutually exclusive.</span></span>

<span data-ttu-id="06c40-124">La marca D3DXMESHOPT SHAREVB se ha \_ quitado de esta enumeración.</span><span class="sxs-lookup"><span data-stu-id="06c40-124">The D3DXMESHOPT\_SHAREVB flag has been removed from this enumeration.</span></span> <span data-ttu-id="06c40-125">\_ \_ En su lugar, use D3DXMESH VB Share, en D3DXMESH.</span><span class="sxs-lookup"><span data-stu-id="06c40-125">Use D3DXMESH\_VB\_SHARE instead, in D3DXMESH.</span></span>

## <a name="requirements"></a><span data-ttu-id="06c40-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="06c40-126">Requirements</span></span>



| <span data-ttu-id="06c40-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="06c40-127">Requirement</span></span> | <span data-ttu-id="06c40-128">Value</span><span class="sxs-lookup"><span data-stu-id="06c40-128">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="06c40-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="06c40-129">Header</span></span><br/> | <dl> <span data-ttu-id="06c40-130"><dt>D3DX10Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="06c40-130"><dt>D3DX10Mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06c40-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="06c40-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06c40-132">Enumeraciones de D3DX</span><span class="sxs-lookup"><span data-stu-id="06c40-132">D3DX Enumerations</span></span>](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 




