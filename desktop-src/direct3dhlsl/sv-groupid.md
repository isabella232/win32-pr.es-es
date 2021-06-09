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
ms.openlocfilehash: ab94cef0a9a33f23947e11b93a5487c65eee3890
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/09/2021
ms.locfileid: "111827044"
---
# <a name="sv_groupid"></a><span data-ttu-id="2678e-104">SV \_ GroupID</span><span class="sxs-lookup"><span data-stu-id="2678e-104">SV\_GroupID</span></span>

<span data-ttu-id="2678e-105">Índices en los que se ejecuta un sombreador de proceso para el grupo de subprocesos.</span><span class="sxs-lookup"><span data-stu-id="2678e-105">Indices for which thread group a compute shader is executing in.</span></span> <span data-ttu-id="2678e-106">Los índices son para todo el grupo y no para un subproceso individual.</span><span class="sxs-lookup"><span data-stu-id="2678e-106">The indices are to the whole group and not an individual thread.</span></span> <span data-ttu-id="2678e-107">Los valores posibles varían en el intervalo pasado como parámetros a [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch).</span><span class="sxs-lookup"><span data-stu-id="2678e-107">Possible values vary across the range passed as parameters to [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch).</span></span> <span data-ttu-id="2678e-108">Por ejemplo, llamar a Dispatch(2,1,1) da como resultado valores posibles de 0,0,0 y 1,0,0.</span><span class="sxs-lookup"><span data-stu-id="2678e-108">For example calling Dispatch(2,1,1) results in possible values of 0,0,0 and 1,0,0.</span></span>

<span data-ttu-id="2678e-109">Define el desplazamiento de grupo dentro de [**una llamada de**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch) dispatch, por dimensión de la llamada de distribución.</span><span class="sxs-lookup"><span data-stu-id="2678e-109">Defines the group offset within a [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch) call, per dimension of the dispatch call.</span></span>

## <a name="type"></a><span data-ttu-id="2678e-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="2678e-110">Type</span></span>



| <span data-ttu-id="2678e-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="2678e-111">Type</span></span>      |
|-------|
| <span data-ttu-id="2678e-112">uint3</span><span class="sxs-lookup"><span data-stu-id="2678e-112">uint3</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="2678e-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2678e-113">Remarks</span></span>

<span data-ttu-id="2678e-114">Este valor del sistema es opcional.</span><span class="sxs-lookup"><span data-stu-id="2678e-114">This system value is optional.</span></span>

<span data-ttu-id="2678e-115">En la ilustración siguiente se muestra la relación entre los parámetros pasados a [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch), Dispatch(5,3,2), los valores especificados en el atributo [numthreads,](sm5-attributes-numthreads.md) numthreads(10,8,3) y los valores que se pasarán al sombreador de proceso para los valores del sistema relacionados con subprocesos [(SV \_ GroupIndex](sv-groupindex.md),[SV \_ DispatchThreadID](sv-dispatchthreadid.md),[SV \_ GroupThreadID](sv-groupthreadid.md), SV \_ GroupID).</span><span class="sxs-lookup"><span data-stu-id="2678e-115">The following illustration shows the relationship between the parameters passed to [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch), Dispatch(5,3,2), the values specified in the [numthreads](sm5-attributes-numthreads.md) attribute, numthreads(10,8,3), and values that will passed to the compute shader for the thread-related system values ([SV\_GroupIndex](sv-groupindex.md),[SV\_DispatchThreadID](sv-dispatchthreadid.md),[SV\_GroupThreadID](sv-groupthreadid.md),SV\_GroupID).</span></span>

![ilustración de la relación entre distribución, grupos de subprocesos y subprocesos](images/threadgroupids.png)

<span data-ttu-id="2678e-117">Esta función se admite en los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="2678e-117">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="2678e-118">Vértice</span><span class="sxs-lookup"><span data-stu-id="2678e-118">Vertex</span></span> | <span data-ttu-id="2678e-119">Casco</span><span class="sxs-lookup"><span data-stu-id="2678e-119">Hull</span></span> | <span data-ttu-id="2678e-120">Dominio</span><span class="sxs-lookup"><span data-stu-id="2678e-120">Domain</span></span> | <span data-ttu-id="2678e-121">Geometría</span><span class="sxs-lookup"><span data-stu-id="2678e-121">Geometry</span></span> | <span data-ttu-id="2678e-122">Píxel</span><span class="sxs-lookup"><span data-stu-id="2678e-122">Pixel</span></span> | <span data-ttu-id="2678e-123">Compute</span><span class="sxs-lookup"><span data-stu-id="2678e-123">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | <span data-ttu-id="2678e-124">x</span><span class="sxs-lookup"><span data-stu-id="2678e-124">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="2678e-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="2678e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2678e-126">Semántica</span><span class="sxs-lookup"><span data-stu-id="2678e-126">Semantics</span></span>](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[<span data-ttu-id="2678e-127">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="2678e-127">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
