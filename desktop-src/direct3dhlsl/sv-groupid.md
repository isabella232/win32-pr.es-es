---
title: SV_GroupID
description: Índices en los que se ejecuta un sombreador de proceso para el grupo de subprocesos.
ms.assetid: 1b90ca74-a2b6-4a5f-aa4a-1ec879360593
keywords:
- SV_GroupID HLSL
topic_type:
- apiref
api_name:
- SV_GroupID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cf96e1db7dbb93c88ec741e309413dea3df2b01d
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997002"
---
# <a name="sv_groupid"></a><span data-ttu-id="44353-104">SV \_ GroupID</span><span class="sxs-lookup"><span data-stu-id="44353-104">SV\_GroupID</span></span>

<span data-ttu-id="44353-105">Índices en los que se ejecuta un sombreador de proceso para el grupo de subprocesos.</span><span class="sxs-lookup"><span data-stu-id="44353-105">Indices for which thread group a compute shader is executing in.</span></span> <span data-ttu-id="44353-106">Los índices son para todo el grupo y no para un subproceso individual.</span><span class="sxs-lookup"><span data-stu-id="44353-106">The indices are to the whole group and not an individual thread.</span></span> <span data-ttu-id="44353-107">Los valores posibles varían en el intervalo pasado como parámetros a [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch).</span><span class="sxs-lookup"><span data-stu-id="44353-107">Possible values vary across the range passed as parameters to [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch).</span></span> <span data-ttu-id="44353-108">Por ejemplo, llamar a Dispatch(2,1,1) da como resultado valores posibles de 0,0,0 y 1,0,0.</span><span class="sxs-lookup"><span data-stu-id="44353-108">For example calling Dispatch(2,1,1) results in possible values of 0,0,0 and 1,0,0.</span></span>

<span data-ttu-id="44353-109">Define el desplazamiento de grupo dentro de [**una llamada a Dispatch,**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch) por dimensión de la llamada de distribución.</span><span class="sxs-lookup"><span data-stu-id="44353-109">Defines the group offset within a [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch) call, per dimension of the dispatch call.</span></span>

## <a name="type"></a><span data-ttu-id="44353-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="44353-110">Type</span></span>



|       |
|-------|
| <span data-ttu-id="44353-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="44353-111">Type</span></span>  |
| <span data-ttu-id="44353-112">uint3</span><span class="sxs-lookup"><span data-stu-id="44353-112">uint3</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="44353-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="44353-113">Remarks</span></span>

<span data-ttu-id="44353-114">Este valor del sistema es opcional.</span><span class="sxs-lookup"><span data-stu-id="44353-114">This system value is optional.</span></span>

<span data-ttu-id="44353-115">En la ilustración siguiente se muestra la relación entre los parámetros pasados a [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch), Dispatch(5,3,2), los valores especificados en el atributo [numthreads,](sm5-attributes-numthreads.md) numthreads(10,8,3) y los valores que se pasarán al sombreador de proceso para los valores del sistema relacionados con subprocesos [(SV \_ GroupIndex](sv-groupindex.md),[SV \_ DispatchThreadID](sv-dispatchthreadid.md),[SV \_ GroupThreadID](sv-groupthreadid.md), SV \_ GroupID).</span><span class="sxs-lookup"><span data-stu-id="44353-115">The following illustration shows the relationship between the parameters passed to [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch), Dispatch(5,3,2), the values specified in the [numthreads](sm5-attributes-numthreads.md) attribute, numthreads(10,8,3), and values that will passed to the compute shader for the thread-related system values ([SV\_GroupIndex](sv-groupindex.md),[SV\_DispatchThreadID](sv-dispatchthreadid.md),[SV\_GroupThreadID](sv-groupthreadid.md),SV\_GroupID).</span></span>

![ilustración de la relación entre distribución, grupos de subprocesos y subprocesos](images/threadgroupids.png)

<span data-ttu-id="44353-117">Esta función se admite en los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="44353-117">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="44353-118">Vértice</span><span class="sxs-lookup"><span data-stu-id="44353-118">Vertex</span></span> | <span data-ttu-id="44353-119">Casco</span><span class="sxs-lookup"><span data-stu-id="44353-119">Hull</span></span> | <span data-ttu-id="44353-120">Domain</span><span class="sxs-lookup"><span data-stu-id="44353-120">Domain</span></span> | <span data-ttu-id="44353-121">Geometría</span><span class="sxs-lookup"><span data-stu-id="44353-121">Geometry</span></span> | <span data-ttu-id="44353-122">Píxel</span><span class="sxs-lookup"><span data-stu-id="44353-122">Pixel</span></span> | <span data-ttu-id="44353-123">Proceso</span><span class="sxs-lookup"><span data-stu-id="44353-123">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | <span data-ttu-id="44353-124">x</span><span class="sxs-lookup"><span data-stu-id="44353-124">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="44353-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="44353-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44353-126">Semántica</span><span class="sxs-lookup"><span data-stu-id="44353-126">Semantics</span></span>](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[<span data-ttu-id="44353-127">Shader Model 5</span><span class="sxs-lookup"><span data-stu-id="44353-127">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
