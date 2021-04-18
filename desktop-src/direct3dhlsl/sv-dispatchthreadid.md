---
title: SV_DispatchThreadID
description: Índices para los que se está ejecutando un sombreador de cálculo en el subproceso y el grupo de subprocesos combinados.
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
ms.openlocfilehash: d55fcf7e291c561ecb51dd32dfac135c563974c7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104567863"
---
# <a name="sv_dispatchthreadid"></a><span data-ttu-id="13202-104">VP \_ DispatchThreadID</span><span class="sxs-lookup"><span data-stu-id="13202-104">SV\_DispatchThreadID</span></span>

<span data-ttu-id="13202-105">Índices para los que se está ejecutando un sombreador de cálculo en el subproceso y el grupo de subprocesos combinados.</span><span class="sxs-lookup"><span data-stu-id="13202-105">Indices for which combined thread and thread group a compute shader is executing in.</span></span> <span data-ttu-id="13202-106">VP \_ DispatchThreadID es la suma de SV \_ GroupID \* numthreads y GroupThreadID.</span><span class="sxs-lookup"><span data-stu-id="13202-106">SV\_DispatchThreadID is the sum of SV\_GroupID \* numthreads and GroupThreadID.</span></span> <span data-ttu-id="13202-107">Varía en el intervalo especificado en [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch) y [numthreads](sm5-attributes-numthreads.md).</span><span class="sxs-lookup"><span data-stu-id="13202-107">It varies across the range specified in [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch) and [numthreads](sm5-attributes-numthreads.md).</span></span> <span data-ttu-id="13202-108">Por ejemplo, si se llama a dispatch (2, 2, 2) en un sombreador de cálculo con numthreads (3, 3, 3) SV \_ DispatchThreadID tendrá un intervalo de 0.. 5 para cada dimensión.</span><span class="sxs-lookup"><span data-stu-id="13202-108">For example if Dispatch(2,2,2) is called on a compute shader with numthreads(3,3,3) SV\_DispatchThreadID will have a range of 0..5 for each dimension.</span></span>

## <a name="type"></a><span data-ttu-id="13202-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="13202-109">Type</span></span>



|       |
|-------|
| <span data-ttu-id="13202-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="13202-110">Type</span></span>  |
| <span data-ttu-id="13202-111">uint3</span><span class="sxs-lookup"><span data-stu-id="13202-111">uint3</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="13202-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="13202-112">Remarks</span></span>

<span data-ttu-id="13202-113">Este valor del sistema es opcional.</span><span class="sxs-lookup"><span data-stu-id="13202-113">This system value is optional.</span></span>

<span data-ttu-id="13202-114">En la ilustración siguiente se muestra la relación entre los parámetros que se pasan a [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch), dispatch (5, 3, 2), los valores especificados en el atributo [numthreads](sm5-attributes-numthreads.md) , numthreads (10, 8, 3) y los valores que se pasarán al sombreador de cálculo para los valores del sistema relacionados con el subproceso ([VP \_ GroupIndex](sv-groupindex.md), VP \_ DispatchThreadID,[VP \_ GroupThreadID](sv-groupthreadid.md),[VP \_ GroupID](sv-groupid.md)).</span><span class="sxs-lookup"><span data-stu-id="13202-114">The following illustration shows the relationship between the parameters passed to [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch), Dispatch(5,3,2), the values specified in the [numthreads](sm5-attributes-numthreads.md) attribute, numthreads(10,8,3), and values that will passed to the compute shader for the thread-related system values ([SV\_GroupIndex](sv-groupindex.md),SV\_DispatchThreadID,[SV\_GroupThreadID](sv-groupthreadid.md),[SV\_GroupID](sv-groupid.md)).</span></span>

![Ilustración de la relación entre el envío, los grupos de subprocesos y los subprocesos](images/threadgroupids.png)

<span data-ttu-id="13202-116">Esta función se admite en los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="13202-116">This function is supported in the following types of shaders:</span></span>



|        |      |        |          |       |         |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="13202-117">Vértice</span><span class="sxs-lookup"><span data-stu-id="13202-117">Vertex</span></span> | <span data-ttu-id="13202-118">Casco</span><span class="sxs-lookup"><span data-stu-id="13202-118">Hull</span></span> | <span data-ttu-id="13202-119">Dominio</span><span class="sxs-lookup"><span data-stu-id="13202-119">Domain</span></span> | <span data-ttu-id="13202-120">Geometría</span><span class="sxs-lookup"><span data-stu-id="13202-120">Geometry</span></span> | <span data-ttu-id="13202-121">Píxel</span><span class="sxs-lookup"><span data-stu-id="13202-121">Pixel</span></span> | <span data-ttu-id="13202-122">Compute</span><span class="sxs-lookup"><span data-stu-id="13202-122">Compute</span></span> |
|        |      |        |          |       | <span data-ttu-id="13202-123">x</span><span class="sxs-lookup"><span data-stu-id="13202-123">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="13202-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="13202-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13202-125">Semántica</span><span class="sxs-lookup"><span data-stu-id="13202-125">Semantics</span></span>](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[<span data-ttu-id="13202-126">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="13202-126">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 