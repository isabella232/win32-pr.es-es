---
description: 'D3DX10_MESHOPT enumeración: especifica el tipo de optimización de malla que se va a realizar.'
ms.assetid: 20d1da8c-8c3d-4045-9a37-d534a8682716
title: D3DX10_MESHOPT enumeración (D3DX10Mesh.h)
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
ms.openlocfilehash: 7b3085cf9970f2c1f6fe3748cc4db8f4fb2b2a78
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105453"
---
# <a name="d3dx10_meshopt-enumeration"></a><span data-ttu-id="bc80f-103">Enumeración D3DX10 \_ MESHOPT</span><span class="sxs-lookup"><span data-stu-id="bc80f-103">D3DX10\_MESHOPT enumeration</span></span>

<span data-ttu-id="bc80f-104">Especifica el tipo de optimización de malla que se va a realizar.</span><span class="sxs-lookup"><span data-stu-id="bc80f-104">Specifies the type of mesh optimization to be performed.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc80f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="bc80f-105">Syntax</span></span>


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



## <a name="constants"></a><span data-ttu-id="bc80f-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="bc80f-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="bc80f-107"><span id="D3DX10_MESHOPT_COMPACT"></span><span id="d3dx10_meshopt_compact"></span>**D3DX10 \_ MESHOPT \_ COMPACT**</span><span class="sxs-lookup"><span data-stu-id="bc80f-107"><span id="D3DX10_MESHOPT_COMPACT"></span><span id="d3dx10_meshopt_compact"></span>**D3DX10\_MESHOPT\_COMPACT**</span></span>
</dt> <dd>

<span data-ttu-id="bc80f-108">Reordena las caras para quitar los vértices y las caras que no se usan.</span><span class="sxs-lookup"><span data-stu-id="bc80f-108">Reorders faces to remove unused vertices and faces.</span></span>

</dd> <dt>

<span data-ttu-id="bc80f-109"><span id="D3DX10_MESHOPT_ATTR_SORT"></span><span id="d3dx10_meshopt_attr_sort"></span>**D3DX10 \_ MESHOPT \_ ATTR \_ SORT**</span><span class="sxs-lookup"><span data-stu-id="bc80f-109"><span id="D3DX10_MESHOPT_ATTR_SORT"></span><span id="d3dx10_meshopt_attr_sort"></span>**D3DX10\_MESHOPT\_ATTR\_SORT**</span></span>
</dt> <dd>

<span data-ttu-id="bc80f-110">Reordena las caras para optimizar para menos cambios de estado de agrupación de atributos y mejorar el rendimiento de DrawSubset.</span><span class="sxs-lookup"><span data-stu-id="bc80f-110">Reorders faces to optimize for fewer attribute bundle state changes and enhanced DrawSubset performance.</span></span>

</dd> <dt>

<span data-ttu-id="bc80f-111"><span id="D3DX10_MESHOPT_VERTEX_CACHE"></span><span id="d3dx10_meshopt_vertex_cache"></span>**CACHÉ DE VÉRTICES \_ DE MESHOPT D3DX10 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="bc80f-111"><span id="D3DX10_MESHOPT_VERTEX_CACHE"></span><span id="d3dx10_meshopt_vertex_cache"></span>**D3DX10\_MESHOPT\_VERTEX\_CACHE**</span></span>
</dt> <dd>

<span data-ttu-id="bc80f-112">Reordena las caras para aumentar la tasa de aciertos de caché de las cachés de vértices.</span><span class="sxs-lookup"><span data-stu-id="bc80f-112">Reorders faces to increase the cache hit rate of vertex caches.</span></span>

</dd> <dt>

<span data-ttu-id="bc80f-113"><span id="D3DX10_MESHOPT_STRIP_REORDER"></span><span id="d3dx10_meshopt_strip_reorder"></span>**REORDENACIÓN DE \_ BANDAS DE MESHOPT D3DX10 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="bc80f-113"><span id="D3DX10_MESHOPT_STRIP_REORDER"></span><span id="d3dx10_meshopt_strip_reorder"></span>**D3DX10\_MESHOPT\_STRIP\_REORDER**</span></span>
</dt> <dd>

<span data-ttu-id="bc80f-114">Reordena las caras para maximizar la longitud de los triángulos adyacentes.</span><span class="sxs-lookup"><span data-stu-id="bc80f-114">Reorders faces to maximize length of adjacent triangles.</span></span>

</dd> <dt>

<span data-ttu-id="bc80f-115"><span id="D3DX10_MESHOPT_IGNORE_VERTS"></span><span id="d3dx10_meshopt_ignore_verts"></span>**D3DX10 \_ MESHOPT \_ OMITIR \_ VERTS**</span><span class="sxs-lookup"><span data-stu-id="bc80f-115"><span id="D3DX10_MESHOPT_IGNORE_VERTS"></span><span id="d3dx10_meshopt_ignore_verts"></span>**D3DX10\_MESHOPT\_IGNORE\_VERTS**</span></span>
</dt> <dd>

<span data-ttu-id="bc80f-116">Optimice solo las caras; no optimice los vértices.</span><span class="sxs-lookup"><span data-stu-id="bc80f-116">Optimize the faces only; do not optimize the vertices.</span></span>

</dd> <dt>

<span data-ttu-id="bc80f-117"><span id="D3DX10_MESHOPT_DO_NOT_SPLIT"></span><span id="d3dx10_meshopt_do_not_split"></span>**D3DX10 \_ MESHOPT \_ NO SE \_ \_ DIVIDE**</span><span class="sxs-lookup"><span data-stu-id="bc80f-117"><span id="D3DX10_MESHOPT_DO_NOT_SPLIT"></span><span id="d3dx10_meshopt_do_not_split"></span>**D3DX10\_MESHOPT\_DO\_NOT\_SPLIT**</span></span>
</dt> <dd>

<span data-ttu-id="bc80f-118">Durante la ordenación de atributos, no divida los vértices que se comparten entre grupos de atributos.</span><span class="sxs-lookup"><span data-stu-id="bc80f-118">While attribute sorting, do not split vertices that are shared between attribute groups.</span></span>

</dd> <dt>

<span data-ttu-id="bc80f-119"><span id="D3DX10_MESHOPT_DEVICE_INDEPENDENT"></span><span id="d3dx10_meshopt_device_independent"></span>**D3DX10 \_ MESHOPT \_ DEVICE \_ INDEPENDENT**</span><span class="sxs-lookup"><span data-stu-id="bc80f-119"><span id="D3DX10_MESHOPT_DEVICE_INDEPENDENT"></span><span id="d3dx10_meshopt_device_independent"></span>**D3DX10\_MESHOPT\_DEVICE\_INDEPENDENT**</span></span>
</dt> <dd>

<span data-ttu-id="bc80f-120">Afecta al tamaño de la caché de vértices.</span><span class="sxs-lookup"><span data-stu-id="bc80f-120">Affects the vertex cache size.</span></span> <span data-ttu-id="bc80f-121">El uso de esta marca especifica un tamaño de caché de vértices predeterminado que funciona bien en hardware heredado.</span><span class="sxs-lookup"><span data-stu-id="bc80f-121">Using this flag specifies a default vertex cache size that works well on legacy hardware.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bc80f-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="bc80f-122">Remarks</span></span>

<span data-ttu-id="bc80f-123">Las marcas de optimización D3DXMESHOPT \_ STRIPREORDER y D3DXMESHOPT \_ VERTEXCACHE son mutuamente excluyentes.</span><span class="sxs-lookup"><span data-stu-id="bc80f-123">The D3DXMESHOPT\_STRIPREORDER and D3DXMESHOPT\_VERTEXCACHE optimization flags are mutually exclusive.</span></span>

<span data-ttu-id="bc80f-124">La marca SHAREVB D3DXMESHOPT \_ se ha quitado de esta enumeración.</span><span class="sxs-lookup"><span data-stu-id="bc80f-124">The D3DXMESHOPT\_SHAREVB flag has been removed from this enumeration.</span></span> <span data-ttu-id="bc80f-125">Use D3DXMESH \_ VB SHARE en su \_ lugar, en D3DXMESH.</span><span class="sxs-lookup"><span data-stu-id="bc80f-125">Use D3DXMESH\_VB\_SHARE instead, in D3DXMESH.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc80f-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bc80f-126">Requirements</span></span>



| <span data-ttu-id="bc80f-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="bc80f-127">Requirement</span></span> | <span data-ttu-id="bc80f-128">Value</span><span class="sxs-lookup"><span data-stu-id="bc80f-128">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bc80f-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bc80f-129">Header</span></span><br/> | <dl> <span data-ttu-id="bc80f-130"><dt>D3DX10Mesh.h</dt></span><span class="sxs-lookup"><span data-stu-id="bc80f-130"><dt>D3DX10Mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bc80f-131">Consulte también</span><span class="sxs-lookup"><span data-stu-id="bc80f-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc80f-132">Enumeraciones D3DX</span><span class="sxs-lookup"><span data-stu-id="bc80f-132">D3DX Enumerations</span></span>](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 




