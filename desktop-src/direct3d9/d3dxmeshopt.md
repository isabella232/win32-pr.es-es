---
description: 'Enumeración D3DXMESHOPT: especifica el tipo de optimización de malla que se va a realizar.'
ms.assetid: 32ef227a-b299-47c4-96b8-c0ea7bf549e1
title: Enumeración D3DXMESHOPT (D3dx9mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _D3DXMESHOPT
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: db7c2a2411d1c846c7369fc1d925a8e5569df3b1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108114353"
---
# <a name="d3dxmeshopt-enumeration"></a><span data-ttu-id="fbe65-103">Enumeración D3DXMESHOPT</span><span class="sxs-lookup"><span data-stu-id="fbe65-103">D3DXMESHOPT enumeration</span></span>

<span data-ttu-id="fbe65-104">Especifica el tipo de optimización de malla que se va a realizar.</span><span class="sxs-lookup"><span data-stu-id="fbe65-104">Specifies the type of mesh optimization to be performed.</span></span>

## <a name="syntax"></a><span data-ttu-id="fbe65-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="fbe65-105">Syntax</span></span>


```C++
enum _D3DXMESHOPT {
  D3DXMESHOPT_COMPACT            = 0x01000000, 
  D3DXMESHOPT_ATTRSORT           = 0x02000000, 
  D3DXMESHOPT_VERTEXCACHE        = 0x04000000, 
  D3DXMESHOPT_STRIPREORDER       = 0x08000000, 
  D3DXMESHOPT_IGNOREVERTS        = 0x10000000, 
  D3DXMESHOPT_DONOTSPLIT         = 0x20000000, 
  D3DXMESHOPT_DEVICEINDEPENDENT  = 0x40000000 

};
```



## <a name="constants"></a><span data-ttu-id="fbe65-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="fbe65-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="fbe65-107"><span id="D3DXMESHOPT_COMPACT"></span><span id="d3dxmeshopt_compact"></span>**D3DXMESHOPT \_ COMPACT**</span><span class="sxs-lookup"><span data-stu-id="fbe65-107"><span id="D3DXMESHOPT_COMPACT"></span><span id="d3dxmeshopt_compact"></span>**D3DXMESHOPT\_COMPACT**</span></span>
</dt> <dd>

<span data-ttu-id="fbe65-108">Reordena las caras para quitar los vértices y las caras que no se usan.</span><span class="sxs-lookup"><span data-stu-id="fbe65-108">Reorders faces to remove unused vertices and faces.</span></span>

</dd> <dt>

<span data-ttu-id="fbe65-109"><span id="D3DXMESHOPT_ATTRSORT"></span><span id="d3dxmeshopt_attrsort"></span>**D3DXMESHOPT \_ ATTRSORT**</span><span class="sxs-lookup"><span data-stu-id="fbe65-109"><span id="D3DXMESHOPT_ATTRSORT"></span><span id="d3dxmeshopt_attrsort"></span>**D3DXMESHOPT\_ATTRSORT**</span></span>
</dt> <dd>

<span data-ttu-id="fbe65-110">Reordena las caras para optimizar para obtener menos cambios de estado de agrupación de atributos y un rendimiento [**mejorado de ID3DXBaseMesh::D rawSubset.**](id3dxbasemesh--drawsubset.md)</span><span class="sxs-lookup"><span data-stu-id="fbe65-110">Reorders faces to optimize for fewer attribute bundle state changes and enhanced [**ID3DXBaseMesh::DrawSubset**](id3dxbasemesh--drawsubset.md) performance.</span></span>

</dd> <dt>

<span data-ttu-id="fbe65-111"><span id="D3DXMESHOPT_VERTEXCACHE"></span><span id="d3dxmeshopt_vertexcache"></span>**D3DXMESHOPT \_ VERTEXCACHE**</span><span class="sxs-lookup"><span data-stu-id="fbe65-111"><span id="D3DXMESHOPT_VERTEXCACHE"></span><span id="d3dxmeshopt_vertexcache"></span>**D3DXMESHOPT\_VERTEXCACHE**</span></span>
</dt> <dd>

<span data-ttu-id="fbe65-112">Reordena las caras para aumentar la tasa de aciertos de caché de las cachés de vértices.</span><span class="sxs-lookup"><span data-stu-id="fbe65-112">Reorders faces to increase the cache hit rate of vertex caches.</span></span>

</dd> <dt>

<span data-ttu-id="fbe65-113"><span id="D3DXMESHOPT_STRIPREORDER"></span><span id="d3dxmeshopt_stripreorder"></span>**D3DXMESHOPT \_ STRIPREORDER**</span><span class="sxs-lookup"><span data-stu-id="fbe65-113"><span id="D3DXMESHOPT_STRIPREORDER"></span><span id="d3dxmeshopt_stripreorder"></span>**D3DXMESHOPT\_STRIPREORDER**</span></span>
</dt> <dd>

<span data-ttu-id="fbe65-114">Reordena las caras para maximizar la longitud de los triángulos adyacentes.</span><span class="sxs-lookup"><span data-stu-id="fbe65-114">Reorders faces to maximize length of adjacent triangles.</span></span>

</dd> <dt>

<span data-ttu-id="fbe65-115"><span id="D3DXMESHOPT_IGNOREVERTS"></span><span id="d3dxmeshopt_ignoreverts"></span>**D3DXMESHOPT \_ IGNOREVERTS**</span><span class="sxs-lookup"><span data-stu-id="fbe65-115"><span id="D3DXMESHOPT_IGNOREVERTS"></span><span id="d3dxmeshopt_ignoreverts"></span>**D3DXMESHOPT\_IGNOREVERTS**</span></span>
</dt> <dd>

<span data-ttu-id="fbe65-116">Optimice solo las caras; no optimice los vértices.</span><span class="sxs-lookup"><span data-stu-id="fbe65-116">Optimize the faces only; do not optimize the vertices.</span></span>

</dd> <dt>

<span data-ttu-id="fbe65-117"><span id="D3DXMESHOPT_DONOTSPLIT"></span><span id="d3dxmeshopt_donotsplit"></span>**D3DXMESHOPT \_ DONOTSPLIT**</span><span class="sxs-lookup"><span data-stu-id="fbe65-117"><span id="D3DXMESHOPT_DONOTSPLIT"></span><span id="d3dxmeshopt_donotsplit"></span>**D3DXMESHOPT\_DONOTSPLIT**</span></span>
</dt> <dd>

<span data-ttu-id="fbe65-118">Durante la ordenación de atributos, no divida los vértices que se comparten entre grupos de atributos.</span><span class="sxs-lookup"><span data-stu-id="fbe65-118">While attribute sorting, do not split vertices that are shared between attribute groups.</span></span>

</dd> <dt>

<span data-ttu-id="fbe65-119"><span id="D3DXMESHOPT_DEVICEINDEPENDENT"></span><span id="d3dxmeshopt_deviceindependent"></span>**D3DXMESHOPT \_ DEVICEINDEPENDENT**</span><span class="sxs-lookup"><span data-stu-id="fbe65-119"><span id="D3DXMESHOPT_DEVICEINDEPENDENT"></span><span id="d3dxmeshopt_deviceindependent"></span>**D3DXMESHOPT\_DEVICEINDEPENDENT**</span></span>
</dt> <dd>

<span data-ttu-id="fbe65-120">Afecta al tamaño de la caché de vértices.</span><span class="sxs-lookup"><span data-stu-id="fbe65-120">Affects the vertex cache size.</span></span> <span data-ttu-id="fbe65-121">El uso de esta marca especifica un tamaño de caché de vértices predeterminado que funciona bien en hardware heredado.</span><span class="sxs-lookup"><span data-stu-id="fbe65-121">Using this flag specifies a default vertex cache size that works well on legacy hardware.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fbe65-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="fbe65-122">Remarks</span></span>

<span data-ttu-id="fbe65-123">Las marcas de optimización D3DXMESHOPT \_ STRIPREORDER y D3DXMESHOPT \_ VERTEXCACHE son mutuamente excluyentes.</span><span class="sxs-lookup"><span data-stu-id="fbe65-123">The D3DXMESHOPT\_STRIPREORDER and D3DXMESHOPT\_VERTEXCACHE optimization flags are mutually exclusive.</span></span>

<span data-ttu-id="fbe65-124">La marca SHAREVB D3DXMESHOPT \_ se ha quitado de esta enumeración.</span><span class="sxs-lookup"><span data-stu-id="fbe65-124">The D3DXMESHOPT\_SHAREVB flag has been removed from this enumeration.</span></span> <span data-ttu-id="fbe65-125">Use D3DXMESH \_ VB SHARE en su \_ lugar, en [**D3DXMESH**](./d3dxmesh.md).</span><span class="sxs-lookup"><span data-stu-id="fbe65-125">Use D3DXMESH\_VB\_SHARE instead, in [**D3DXMESH**](./d3dxmesh.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fbe65-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fbe65-126">Requirements</span></span>



| <span data-ttu-id="fbe65-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="fbe65-127">Requirement</span></span> | <span data-ttu-id="fbe65-128">Value</span><span class="sxs-lookup"><span data-stu-id="fbe65-128">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fbe65-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fbe65-129">Header</span></span><br/> | <dl> <span data-ttu-id="fbe65-130"><dt>D3dx9mesh.h</dt></span><span class="sxs-lookup"><span data-stu-id="fbe65-130"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fbe65-131">Consulte también</span><span class="sxs-lookup"><span data-stu-id="fbe65-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fbe65-132">Enumeraciones D3DX</span><span class="sxs-lookup"><span data-stu-id="fbe65-132">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 
