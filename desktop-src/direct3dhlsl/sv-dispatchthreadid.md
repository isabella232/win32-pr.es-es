---
title: SV_DispatchThreadID
description: Índices para los que el subproceso combinado y el grupo de subprocesos se está ejecutando en un sombreador de proceso.
ms.assetid: bad697f6-26d9-47cd-93e5-127621a161e8
keywords:
- SV_DispatchThreadID HLSL
topic_type:
- apiref
api_name:
- SV_DispatchThreadID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e9653d98ebbfef6dd25bb137af3358a14d177f3e
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996522"
---
# <a name="sv_dispatchthreadid"></a><span data-ttu-id="3a1ce-104">SV \_ DispatchThreadID</span><span class="sxs-lookup"><span data-stu-id="3a1ce-104">SV\_DispatchThreadID</span></span>

<span data-ttu-id="3a1ce-105">Índices para los que el subproceso combinado y el grupo de subprocesos se está ejecutando en un sombreador de proceso.</span><span class="sxs-lookup"><span data-stu-id="3a1ce-105">Indices for which combined thread and thread group a compute shader is executing in.</span></span> <span data-ttu-id="3a1ce-106">SV \_ DispatchThreadID es la suma de SV \_ GroupID \* numthreads y GroupThreadID.</span><span class="sxs-lookup"><span data-stu-id="3a1ce-106">SV\_DispatchThreadID is the sum of SV\_GroupID \* numthreads and GroupThreadID.</span></span> <span data-ttu-id="3a1ce-107">Varía según el intervalo especificado en [**Dispatch y**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch) [numthreads](sm5-attributes-numthreads.md).</span><span class="sxs-lookup"><span data-stu-id="3a1ce-107">It varies across the range specified in [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch) and [numthreads](sm5-attributes-numthreads.md).</span></span> <span data-ttu-id="3a1ce-108">Por ejemplo, si se llama a Dispatch(2,2,2) en un sombreador de proceso con numthreads(3,3,3) SV DispatchThreadID tendrá un intervalo \_ de 0,.5 para cada dimensión.</span><span class="sxs-lookup"><span data-stu-id="3a1ce-108">For example if Dispatch(2,2,2) is called on a compute shader with numthreads(3,3,3) SV\_DispatchThreadID will have a range of 0..5 for each dimension.</span></span>

## <a name="type"></a><span data-ttu-id="3a1ce-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="3a1ce-109">Type</span></span>



|       |
|-------|
| <span data-ttu-id="3a1ce-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="3a1ce-110">Type</span></span>  |
| <span data-ttu-id="3a1ce-111">uint3</span><span class="sxs-lookup"><span data-stu-id="3a1ce-111">uint3</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="3a1ce-112">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3a1ce-112">Remarks</span></span>

<span data-ttu-id="3a1ce-113">Este valor del sistema es opcional.</span><span class="sxs-lookup"><span data-stu-id="3a1ce-113">This system value is optional.</span></span>

<span data-ttu-id="3a1ce-114">En la ilustración siguiente se muestra la relación entre los parámetros pasados a [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch), Dispatch(5,3,2), los valores especificados en el atributo [numthreads,](sm5-attributes-numthreads.md) numthreads(10,8,3) y los valores que se pasarán al sombreador de proceso para los valores del sistema relacionados con subprocesos ([SV \_ GroupIndex](sv-groupindex.md), SV \_ DispatchThreadID,[SV \_ GroupThreadID](sv-groupthreadid.md),[SV \_ GroupID](sv-groupid.md)).</span><span class="sxs-lookup"><span data-stu-id="3a1ce-114">The following illustration shows the relationship between the parameters passed to [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch), Dispatch(5,3,2), the values specified in the [numthreads](sm5-attributes-numthreads.md) attribute, numthreads(10,8,3), and values that will passed to the compute shader for the thread-related system values ([SV\_GroupIndex](sv-groupindex.md),SV\_DispatchThreadID,[SV\_GroupThreadID](sv-groupthreadid.md),[SV\_GroupID](sv-groupid.md)).</span></span>

![ilustración de la relación entre distribución, grupos de subprocesos y subprocesos](images/threadgroupids.png)

<span data-ttu-id="3a1ce-116">Esta función se admite en los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="3a1ce-116">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="3a1ce-117">Vértice</span><span class="sxs-lookup"><span data-stu-id="3a1ce-117">Vertex</span></span> | <span data-ttu-id="3a1ce-118">Casco</span><span class="sxs-lookup"><span data-stu-id="3a1ce-118">Hull</span></span> | <span data-ttu-id="3a1ce-119">Domain</span><span class="sxs-lookup"><span data-stu-id="3a1ce-119">Domain</span></span> | <span data-ttu-id="3a1ce-120">Geometría</span><span class="sxs-lookup"><span data-stu-id="3a1ce-120">Geometry</span></span> | <span data-ttu-id="3a1ce-121">Píxel</span><span class="sxs-lookup"><span data-stu-id="3a1ce-121">Pixel</span></span> | <span data-ttu-id="3a1ce-122">Proceso</span><span class="sxs-lookup"><span data-stu-id="3a1ce-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | <span data-ttu-id="3a1ce-123">x</span><span class="sxs-lookup"><span data-stu-id="3a1ce-123">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="3a1ce-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="3a1ce-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a1ce-125">Semántica</span><span class="sxs-lookup"><span data-stu-id="3a1ce-125">Semantics</span></span>](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[<span data-ttu-id="3a1ce-126">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="3a1ce-126">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
