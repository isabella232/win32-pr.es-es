---
description: Especifica el tipo de optimización de malla que se va a realizar.
ms.assetid: 32ef227a-b299-47c4-96b8-c0ea7bf549e1
title: Enumeración D3DXMESHOPT (D3dx9mesh. h)
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
ms.openlocfilehash: e7d4f9f4ae36cec74ea86fcb50a194ac66d0add7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698239"
---
# <a name="d3dxmeshopt-enumeration"></a><span data-ttu-id="aae0a-103">Enumeración D3DXMESHOPT</span><span class="sxs-lookup"><span data-stu-id="aae0a-103">D3DXMESHOPT enumeration</span></span>

<span data-ttu-id="aae0a-104">Especifica el tipo de optimización de malla que se va a realizar.</span><span class="sxs-lookup"><span data-stu-id="aae0a-104">Specifies the type of mesh optimization to be performed.</span></span>

## <a name="syntax"></a><span data-ttu-id="aae0a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="aae0a-105">Syntax</span></span>


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



## <a name="constants"></a><span data-ttu-id="aae0a-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="aae0a-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="aae0a-107"><span id="D3DXMESHOPT_COMPACT"></span><span id="d3dxmeshopt_compact"></span>**D3DXMESHOPT \_ Compact**</span><span class="sxs-lookup"><span data-stu-id="aae0a-107"><span id="D3DXMESHOPT_COMPACT"></span><span id="d3dxmeshopt_compact"></span>**D3DXMESHOPT\_COMPACT**</span></span>
</dt> <dd>

<span data-ttu-id="aae0a-108">Reordena las caras para quitar los vértices y caras sin usar.</span><span class="sxs-lookup"><span data-stu-id="aae0a-108">Reorders faces to remove unused vertices and faces.</span></span>

</dd> <dt>

<span data-ttu-id="aae0a-109"><span id="D3DXMESHOPT_ATTRSORT"></span><span id="d3dxmeshopt_attrsort"></span>**D3DXMESHOPT \_ ATTRSORT**</span><span class="sxs-lookup"><span data-stu-id="aae0a-109"><span id="D3DXMESHOPT_ATTRSORT"></span><span id="d3dxmeshopt_attrsort"></span>**D3DXMESHOPT\_ATTRSORT**</span></span>
</dt> <dd>

<span data-ttu-id="aae0a-110">Reordena las caras para optimizar menos cambios de estado de agrupación de atributos y ID3DXBaseMesh mejorado: el rendimiento de la [**:D rawsubset**](id3dxbasemesh--drawsubset.md) .</span><span class="sxs-lookup"><span data-stu-id="aae0a-110">Reorders faces to optimize for fewer attribute bundle state changes and enhanced [**ID3DXBaseMesh::DrawSubset**](id3dxbasemesh--drawsubset.md) performance.</span></span>

</dd> <dt>

<span data-ttu-id="aae0a-111"><span id="D3DXMESHOPT_VERTEXCACHE"></span><span id="d3dxmeshopt_vertexcache"></span>**D3DXMESHOPT \_ VERTEXCACHE**</span><span class="sxs-lookup"><span data-stu-id="aae0a-111"><span id="D3DXMESHOPT_VERTEXCACHE"></span><span id="d3dxmeshopt_vertexcache"></span>**D3DXMESHOPT\_VERTEXCACHE**</span></span>
</dt> <dd>

<span data-ttu-id="aae0a-112">Reordena las caras para aumentar la tasa de aciertos de caché de los vértices.</span><span class="sxs-lookup"><span data-stu-id="aae0a-112">Reorders faces to increase the cache hit rate of vertex caches.</span></span>

</dd> <dt>

<span data-ttu-id="aae0a-113"><span id="D3DXMESHOPT_STRIPREORDER"></span><span id="d3dxmeshopt_stripreorder"></span>**D3DXMESHOPT \_ STRIPREORDER**</span><span class="sxs-lookup"><span data-stu-id="aae0a-113"><span id="D3DXMESHOPT_STRIPREORDER"></span><span id="d3dxmeshopt_stripreorder"></span>**D3DXMESHOPT\_STRIPREORDER**</span></span>
</dt> <dd>

<span data-ttu-id="aae0a-114">Reordena las caras para maximizar la longitud de los triángulos adyacentes.</span><span class="sxs-lookup"><span data-stu-id="aae0a-114">Reorders faces to maximize length of adjacent triangles.</span></span>

</dd> <dt>

<span data-ttu-id="aae0a-115"><span id="D3DXMESHOPT_IGNOREVERTS"></span><span id="d3dxmeshopt_ignoreverts"></span>**D3DXMESHOPT \_ IGNOREVERTS**</span><span class="sxs-lookup"><span data-stu-id="aae0a-115"><span id="D3DXMESHOPT_IGNOREVERTS"></span><span id="d3dxmeshopt_ignoreverts"></span>**D3DXMESHOPT\_IGNOREVERTS**</span></span>
</dt> <dd>

<span data-ttu-id="aae0a-116">Optimizar solo las caras; no optimice los vértices.</span><span class="sxs-lookup"><span data-stu-id="aae0a-116">Optimize the faces only; do not optimize the vertices.</span></span>

</dd> <dt>

<span data-ttu-id="aae0a-117"><span id="D3DXMESHOPT_DONOTSPLIT"></span><span id="d3dxmeshopt_donotsplit"></span>**D3DXMESHOPT \_ DONOTSPLIT**</span><span class="sxs-lookup"><span data-stu-id="aae0a-117"><span id="D3DXMESHOPT_DONOTSPLIT"></span><span id="d3dxmeshopt_donotsplit"></span>**D3DXMESHOPT\_DONOTSPLIT**</span></span>
</dt> <dd>

<span data-ttu-id="aae0a-118">Mientras se ordena el atributo, no divida los vértices que se comparten entre los grupos de atributos.</span><span class="sxs-lookup"><span data-stu-id="aae0a-118">While attribute sorting, do not split vertices that are shared between attribute groups.</span></span>

</dd> <dt>

<span data-ttu-id="aae0a-119"><span id="D3DXMESHOPT_DEVICEINDEPENDENT"></span><span id="d3dxmeshopt_deviceindependent"></span>**D3DXMESHOPT \_ DEVICEINDEPENDENT**</span><span class="sxs-lookup"><span data-stu-id="aae0a-119"><span id="D3DXMESHOPT_DEVICEINDEPENDENT"></span><span id="d3dxmeshopt_deviceindependent"></span>**D3DXMESHOPT\_DEVICEINDEPENDENT**</span></span>
</dt> <dd>

<span data-ttu-id="aae0a-120">Afecta al tamaño de la caché de vértices.</span><span class="sxs-lookup"><span data-stu-id="aae0a-120">Affects the vertex cache size.</span></span> <span data-ttu-id="aae0a-121">El uso de esta marca especifica un tamaño de caché de vértices predeterminado que funciona bien en el hardware heredado.</span><span class="sxs-lookup"><span data-stu-id="aae0a-121">Using this flag specifies a default vertex cache size that works well on legacy hardware.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="aae0a-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="aae0a-122">Remarks</span></span>

<span data-ttu-id="aae0a-123">Las \_ marcas de optimización D3DXMESHOPT STRIPREORDER y D3DXMESHOPT \_ VERTEXCACHE se excluyen mutuamente.</span><span class="sxs-lookup"><span data-stu-id="aae0a-123">The D3DXMESHOPT\_STRIPREORDER and D3DXMESHOPT\_VERTEXCACHE optimization flags are mutually exclusive.</span></span>

<span data-ttu-id="aae0a-124">La marca D3DXMESHOPT SHAREVB se ha \_ quitado de esta enumeración.</span><span class="sxs-lookup"><span data-stu-id="aae0a-124">The D3DXMESHOPT\_SHAREVB flag has been removed from this enumeration.</span></span> <span data-ttu-id="aae0a-125">\_ \_ En su lugar, use D3DXMESH VB Share, en [**D3DXMESH**](./d3dxmesh.md).</span><span class="sxs-lookup"><span data-stu-id="aae0a-125">Use D3DXMESH\_VB\_SHARE instead, in [**D3DXMESH**](./d3dxmesh.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="aae0a-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aae0a-126">Requirements</span></span>



| <span data-ttu-id="aae0a-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="aae0a-127">Requirement</span></span> | <span data-ttu-id="aae0a-128">Value</span><span class="sxs-lookup"><span data-stu-id="aae0a-128">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="aae0a-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="aae0a-129">Header</span></span><br/> | <dl> <span data-ttu-id="aae0a-130"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="aae0a-130"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aae0a-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="aae0a-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aae0a-132">Enumeraciones de D3DX</span><span class="sxs-lookup"><span data-stu-id="aae0a-132">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 
