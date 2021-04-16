---
description: Mida el rendimiento de la tasa de aciertos de caché para las texturas y los vértices indizados.
ms.assetid: 70bc4e93-0a34-485b-bdcc-028c24b52f62
title: D3DDEVINFO_D3D9CACHEUTILIZATION estructura (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVINFO_D3D9CACHEUTILIZATION
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 94f77549d0ea2a9c59d7de8367a6133085cc2771
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104547846"
---
# <a name="d3ddevinfo_d3d9cacheutilization-structure"></a><span data-ttu-id="ba1c1-103">D3DDEVINFO \_ estructura D3D9CACHEUTILIZATION</span><span class="sxs-lookup"><span data-stu-id="ba1c1-103">D3DDEVINFO\_D3D9CACHEUTILIZATION structure</span></span>

<span data-ttu-id="ba1c1-104">Mida el rendimiento de la tasa de aciertos de caché para las texturas y los vértices indizados.</span><span class="sxs-lookup"><span data-stu-id="ba1c1-104">Measure the cache hit rate performance for textures and indexed vertices.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba1c1-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ba1c1-105">Syntax</span></span>


```C++
typedef struct D3DDEVINFO_D3D9CACHEUTILIZATION {
  FLOAT TextureCacheHitRate;
  FLOAT PostTransformVertexCacheHitRate;
} D3DDEVINFO_D3D9CACHEUTILIZATION, *LPD3DDEVINFO_D3D9CACHEUTILIZATION;
```



## <a name="members"></a><span data-ttu-id="ba1c1-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="ba1c1-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="ba1c1-107">**TextureCacheHitRate**</span><span class="sxs-lookup"><span data-stu-id="ba1c1-107">**TextureCacheHitRate**</span></span>
</dt> <dd>

<span data-ttu-id="ba1c1-108">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ba1c1-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ba1c1-109">La tasa de aciertos para buscar una textura en la memoria caché de textura.</span><span class="sxs-lookup"><span data-stu-id="ba1c1-109">The hit rate for finding a texture in the texture cache.</span></span> <span data-ttu-id="ba1c1-110">Se supone que hay una caché de textura.</span><span class="sxs-lookup"><span data-stu-id="ba1c1-110">This assumes there is a texture cache.</span></span> <span data-ttu-id="ba1c1-111">Aumentar el sesgo de nivel de detalle para usar la textura más detallada, usar muchas texturas grandes o generar un patrón de acceso de textura casi aleatorio en texturas grandes con código de sombreador personalizado puede afectar drásticamente a la tasa de aciertos de la caché de textura.</span><span class="sxs-lookup"><span data-stu-id="ba1c1-111">Increasing the level-of-detail bias to use the most detailed texture, using many large textures, or producing a near random texture access pattern on large textures with custom shader code can dramatically affect the texture cache hit rate.</span></span>

</dd> <dt>

<span data-ttu-id="ba1c1-112">**PostTransformVertexCacheHitRate**</span><span class="sxs-lookup"><span data-stu-id="ba1c1-112">**PostTransformVertexCacheHitRate**</span></span>
</dt> <dd>

<span data-ttu-id="ba1c1-113">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ba1c1-113">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ba1c1-114">La tasa de aciertos para buscar vértices transformados en la memoria caché de vértices.</span><span class="sxs-lookup"><span data-stu-id="ba1c1-114">The hit rate for finding transformed vertices in the vertex cache.</span></span> <span data-ttu-id="ba1c1-115">La GPU está diseñada para transformar vértices indexados y puede almacenarlos en una caché de vértices.</span><span class="sxs-lookup"><span data-stu-id="ba1c1-115">The GPU is designed to transform indexed vertices and may store them in a vertex cache.</span></span> <span data-ttu-id="ba1c1-116">Si usa mallas, [**D3DXOptimizeFaces**](d3dxoptimizefaces.md) o [**D3DXOptimizeVertices**](d3dxoptimizevertices.md) pueden dar lugar a un mejor uso de la memoria caché de vértices.</span><span class="sxs-lookup"><span data-stu-id="ba1c1-116">If you are using meshes, [**D3DXOptimizeFaces**](d3dxoptimizefaces.md) or [**D3DXOptimizeVertices**](d3dxoptimizevertices.md) may result in better vertex cache utilization.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ba1c1-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ba1c1-117">Remarks</span></span>

<span data-ttu-id="ba1c1-118">Una caché eficaz suele estar más cerca de una tasa de aciertos del 90 por ciento, y una caché ineficaz suele estar más cerca de una tasa de aciertos de 10% (aunque un porcentaje bajo no es necesariamente un problema).</span><span class="sxs-lookup"><span data-stu-id="ba1c1-118">An efficient cache is typically closer to a 90 percent hit rate, and an inefficient cache is typically closer to a 10 percent hit rate (although a low percentage is not necessarily a problem).</span></span>

## <a name="requirements"></a><span data-ttu-id="ba1c1-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ba1c1-119">Requirements</span></span>



| <span data-ttu-id="ba1c1-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="ba1c1-120">Requirement</span></span> | <span data-ttu-id="ba1c1-121">Value</span><span class="sxs-lookup"><span data-stu-id="ba1c1-121">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ba1c1-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ba1c1-122">Header</span></span><br/> | <dl> <span data-ttu-id="ba1c1-123"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="ba1c1-123"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ba1c1-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="ba1c1-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba1c1-125">Estructuras de Direct3D</span><span class="sxs-lookup"><span data-stu-id="ba1c1-125">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="ba1c1-126">**GetData**</span><span class="sxs-lookup"><span data-stu-id="ba1c1-126">**GetData**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata)
</dt> </dl>

 

 
