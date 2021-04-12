---
title: SV_GroupThreadID
description: Índices para los que un subproceso individual dentro de un grupo de subprocesos se está ejecutando en un sombreador de cálculo.
ms.assetid: be944592-c4ea-43c9-88bc-98a9a190a437
keywords:
- SV_GroupThreadID HLSL
topic_type:
- apiref
api_name:
- SV_GroupThreadID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3d4d35766bdbdc2d69c98983a85f336ab784d24d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359351"
---
# <a name="sv_groupthreadid"></a><span data-ttu-id="daa57-104">VP \_ GroupThreadID</span><span class="sxs-lookup"><span data-stu-id="daa57-104">SV\_GroupThreadID</span></span>

<span data-ttu-id="daa57-105">Índices para los que un subproceso individual dentro de un grupo de subprocesos se está ejecutando en un sombreador de cálculo.</span><span class="sxs-lookup"><span data-stu-id="daa57-105">Indices for which an individual thread within a thread group a compute shader is executing in.</span></span> <span data-ttu-id="daa57-106">SV \_ GroupThreadID varía en el intervalo especificado para el sombreador de cálculo en el atributo [numthreads](sm5-attributes-numthreads.md) .</span><span class="sxs-lookup"><span data-stu-id="daa57-106">SV\_GroupThreadID varies across the range specified for the compute shader in the [numthreads](sm5-attributes-numthreads.md) attribute.</span></span> <span data-ttu-id="daa57-107">Por ejemplo, si se especifica numthreads (3, 2, 1), los valores posibles para el \_ valor de entrada VP GroupThreadID tienen este intervalo de valores (0-2, 0-1, 0).</span><span class="sxs-lookup"><span data-stu-id="daa57-107">For example if numthreads(3,2,1) was specified possible values for the SV\_GroupThreadID input value have this range of values (0-2,0-1,0).</span></span>

## <a name="type"></a><span data-ttu-id="daa57-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="daa57-108">Type</span></span>



|       |
|-------|
| <span data-ttu-id="daa57-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="daa57-109">Type</span></span>  |
| <span data-ttu-id="daa57-110">uint3</span><span class="sxs-lookup"><span data-stu-id="daa57-110">uint3</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="daa57-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="daa57-111">Remarks</span></span>

<span data-ttu-id="daa57-112">Este valor del sistema es opcional y siempre se encuentra dentro de los límites de los valores pasados al atributo [numthreads](sm5-attributes-numthreads.md) .</span><span class="sxs-lookup"><span data-stu-id="daa57-112">This system value is optional, and is always within the bounds of the values passed into the [numthreads](sm5-attributes-numthreads.md) attribute.</span></span>

<span data-ttu-id="daa57-113">En la ilustración siguiente se muestra la relación entre los parámetros que se pasan a [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch), dispatch (5, 3, 2), los valores especificados en el atributo [numthreads](sm5-attributes-numthreads.md) , numthreads (10, 8, 3) y los valores que se pasarán al sombreador de cálculo para los valores del sistema relacionados con el subproceso ([VP \_ GroupIndex](sv-groupindex.md),[VP \_ DispatchThreadID](sv-dispatchthreadid.md), VP \_ GroupThreadID,[VP \_ GroupID](sv-groupid.md)).</span><span class="sxs-lookup"><span data-stu-id="daa57-113">The following illustration shows the relationship between the parameters passed to [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch), Dispatch(5,3,2), the values specified in the [numthreads](sm5-attributes-numthreads.md) attribute, numthreads(10,8,3), and values that will passed to the compute shader for the thread-related system values ([SV\_GroupIndex](sv-groupindex.md),[SV\_DispatchThreadID](sv-dispatchthreadid.md),SV\_GroupThreadID,[SV\_GroupID](sv-groupid.md)).</span></span>

![Ilustración de la relación entre el envío, los grupos de subprocesos y los subprocesos](images/threadgroupids.png)

<span data-ttu-id="daa57-115">Esta función se admite en los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="daa57-115">This function is supported in the following types of shaders:</span></span>



|        |      |        |          |       |         |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="daa57-116">Vértice</span><span class="sxs-lookup"><span data-stu-id="daa57-116">Vertex</span></span> | <span data-ttu-id="daa57-117">Casco</span><span class="sxs-lookup"><span data-stu-id="daa57-117">Hull</span></span> | <span data-ttu-id="daa57-118">Dominio</span><span class="sxs-lookup"><span data-stu-id="daa57-118">Domain</span></span> | <span data-ttu-id="daa57-119">Geometría</span><span class="sxs-lookup"><span data-stu-id="daa57-119">Geometry</span></span> | <span data-ttu-id="daa57-120">Píxel</span><span class="sxs-lookup"><span data-stu-id="daa57-120">Pixel</span></span> | <span data-ttu-id="daa57-121">Compute</span><span class="sxs-lookup"><span data-stu-id="daa57-121">Compute</span></span> |
|        |      |        |          |       | <span data-ttu-id="daa57-122">x</span><span class="sxs-lookup"><span data-stu-id="daa57-122">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="daa57-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="daa57-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="daa57-124">Semántica</span><span class="sxs-lookup"><span data-stu-id="daa57-124">Semantics</span></span>](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[<span data-ttu-id="daa57-125">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="daa57-125">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 