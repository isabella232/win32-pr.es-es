---
title: SV_GroupIndex
description: '\ 0034; aplanad \ 0034; Índice de un subproceso del sombreador de cálculo dentro de un grupo de subprocesos, que convierte el GroupThreadID VP multidimensional \_ en un valor 1D. SV \_ GroupIndex varía de 0 a (numthreadsX \ numthreadsY \ numThreadsZ) \ 8211; dimensional.'
ms.assetid: e793be10-7c83-478c-859a-4b0a2c537570
keywords:
- SV_GroupIndex HLSL
topic_type:
- apiref
api_name:
- SV_GroupIndex
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 952a94378a0570d5bb7bc4f08959074bc8a4da4d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792285"
---
# <a name="sv_groupindex"></a><span data-ttu-id="553f7-105">VP \_ GroupIndex</span><span class="sxs-lookup"><span data-stu-id="553f7-105">SV\_GroupIndex</span></span>

<span data-ttu-id="553f7-106">Índice "plano" de un subproceso del sombreador de cálculo dentro de un grupo de subprocesos, que convierte el valor de la VP multidimensional \_ GroupThreadID en un valor 1D.</span><span class="sxs-lookup"><span data-stu-id="553f7-106">The "flattened" index of a compute shader thread within a thread group, which turns the multi-dimensional SV\_GroupThreadID into a 1D value.</span></span> <span data-ttu-id="553f7-107">SV \_ GroupIndex varía de 0 a (numthreadsX \* numthreadsY \* numThreadsZ) – 1.</span><span class="sxs-lookup"><span data-stu-id="553f7-107">SV\_GroupIndex varies from 0 to (numthreadsX \* numthreadsY \* numThreadsZ) – 1.</span></span>

## <a name="type"></a><span data-ttu-id="553f7-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="553f7-108">Type</span></span>



| <span data-ttu-id="553f7-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="553f7-109">Type</span></span> |
|------|
| <span data-ttu-id="553f7-110">uint</span><span class="sxs-lookup"><span data-stu-id="553f7-110">uint</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="553f7-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="553f7-111">Remarks</span></span>


```
SV_GroupIndex = SV_GroupThreadID.z*dimx*dimy + 
                      SV_GroupThreadID.y*dimx + 
                      SV_GroupThreadID.x
```



<span data-ttu-id="553f7-112">donde dimx y dimy son las dimensiones especificadas en el atributo [numthreads](sm5-attributes-numthreads.md) para el punto de entrada.</span><span class="sxs-lookup"><span data-stu-id="553f7-112">where dimx and dimy are the dimensions specified in the [numthreads](sm5-attributes-numthreads.md) attribute for the entry point.</span></span>

<span data-ttu-id="553f7-113">Este valor del sistema es opcional.</span><span class="sxs-lookup"><span data-stu-id="553f7-113">This system value is optional.</span></span> <span data-ttu-id="553f7-114">Sin embargo, su uso garantiza que un subproceso solo escribe en su región de memoria asignada en la variable groupshared.</span><span class="sxs-lookup"><span data-stu-id="553f7-114">However, its use ensures that a thread only writes to its assigned region of memory in the groupshared variable.</span></span>

<span data-ttu-id="553f7-115">En la ilustración siguiente se muestra la relación entre los parámetros pasados a [**ID3D11DeviceContext::D ispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch), dispatch (5, 3, 2), los valores especificados en el atributo [numthreads](sm5-attributes-numthreads.md) , numthreads (10, 8, 3) y los valores que se pasarán al sombreador de cálculo para los valores del sistema relacionados con el subproceso (VP \_ GroupIndex,[VP \_ DispatchThreadID](sv-dispatchthreadid.md),[VP \_ GroupThreadID](sv-groupthreadid.md),[VP \_ GroupID](sv-groupid.md))</span><span class="sxs-lookup"><span data-stu-id="553f7-115">The following illustration shows the relationship between the parameters passed to [**ID3D11DeviceContext::Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch), Dispatch(5,3,2), the values specified in the [numthreads](sm5-attributes-numthreads.md) attribute, numthreads(10,8,3), and values that will passed to the compute shader for the thread-related system values (SV\_GroupIndex,[SV\_DispatchThreadID](sv-dispatchthreadid.md),[SV\_GroupThreadID](sv-groupthreadid.md),[SV\_GroupID](sv-groupid.md)).</span></span>

![Ilustración de la relación entre el envío, los grupos de subprocesos y los subprocesos](images/threadgroupids.png)

<span data-ttu-id="553f7-117">Esta función se admite en los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="553f7-117">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="553f7-118">Vértice</span><span class="sxs-lookup"><span data-stu-id="553f7-118">Vertex</span></span> | <span data-ttu-id="553f7-119">Casco</span><span class="sxs-lookup"><span data-stu-id="553f7-119">Hull</span></span> | <span data-ttu-id="553f7-120">Dominio</span><span class="sxs-lookup"><span data-stu-id="553f7-120">Domain</span></span> | <span data-ttu-id="553f7-121">Geometría</span><span class="sxs-lookup"><span data-stu-id="553f7-121">Geometry</span></span> | <span data-ttu-id="553f7-122">Píxel</span><span class="sxs-lookup"><span data-stu-id="553f7-122">Pixel</span></span> | <span data-ttu-id="553f7-123">Compute</span><span class="sxs-lookup"><span data-stu-id="553f7-123">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | <span data-ttu-id="553f7-124">x</span><span class="sxs-lookup"><span data-stu-id="553f7-124">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="553f7-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="553f7-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="553f7-126">Semántica</span><span class="sxs-lookup"><span data-stu-id="553f7-126">Semantics</span></span>](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[<span data-ttu-id="553f7-127">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="553f7-127">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 