---
title: numthreads
description: Define el número de subprocesos que se van a ejecutar en un único grupo de subprocesos cuando se envía un sombreador de cálculo (consulte ID3D11DeviceContext Dispatch).
ms.assetid: ec6b751c-d81c-4221-ae80-166d2a3707fe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: abcca751b58bc88ba984ac5c2210a563591d592e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421350"
---
# <a name="numthreads"></a><span data-ttu-id="2eaa0-103">numthreads</span><span class="sxs-lookup"><span data-stu-id="2eaa0-103">numthreads</span></span>

<span data-ttu-id="2eaa0-104">Define el número de subprocesos que se van a ejecutar en un único grupo de subprocesos cuando se envía un sombreador de cálculo (vea [**ID3D11DeviceContext::D ispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch)).</span><span class="sxs-lookup"><span data-stu-id="2eaa0-104">Defines the number of threads to be executed in a single thread group when a compute shader is dispatched (see [**ID3D11DeviceContext::Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch)).</span></span>


```
numthreads(X, Y, Z)    
```



<span data-ttu-id="2eaa0-105">Los valores X, Y y Z indican el tamaño del grupo de subprocesos en una dirección determinada y el total de X \* y \* Z proporciona el número de subprocesos del grupo.</span><span class="sxs-lookup"><span data-stu-id="2eaa0-105">The X, Y and Z values indicate the size of the thread group in a particular direction and the total of X\*Y\*Z gives the number of threads in the group.</span></span> <span data-ttu-id="2eaa0-106">La capacidad de especificar el tamaño del grupo de subprocesos en tres dimensiones permite tener acceso a los subprocesos individuales de una manera que sea lógicamente estructuras de datos 2D y 3D.</span><span class="sxs-lookup"><span data-stu-id="2eaa0-106">The ability to specify the size of the thread group across three dimensions allows individual threads to be accessed in a manner that logically 2D and 3D data structures.</span></span>

<span data-ttu-id="2eaa0-107">Por ejemplo, si un sombreador de cálculo está realizando la adición de matriz 4x4, numthreads podría establecerse en numthreads (4, 4, 1) y la indexación de los subprocesos individuales coincidiría automáticamente con las entradas de la matriz.</span><span class="sxs-lookup"><span data-stu-id="2eaa0-107">For example, if a compute shader is doing 4x4 matrix addition then numthreads could be set to numthreads(4,4,1) and the indexing in the individual threads would automatically match the matrix entries.</span></span> <span data-ttu-id="2eaa0-108">El sombreador de cálculo también podría declarar un grupo de subprocesos con el mismo número de subprocesos (16) mediante numthreads (16, 1, 1), pero tendría que calcular la entrada de matriz actual en función del número de subproceso actual.</span><span class="sxs-lookup"><span data-stu-id="2eaa0-108">The compute shader could also declare a thread group with the same number of threads (16) using numthreads(16,1,1), however it would then have to calculate the current matrix entry based on the current thread number.</span></span>

<span data-ttu-id="2eaa0-109">Los valores de parámetro permitidos para **numthreads** dependen de la versión del sombreador de cálculo.</span><span class="sxs-lookup"><span data-stu-id="2eaa0-109">The allowable parameter values for **numthreads** depends on the compute shader version.</span></span>



| <span data-ttu-id="2eaa0-110">Sombreador de cálculo</span><span class="sxs-lookup"><span data-stu-id="2eaa0-110">Compute Shader</span></span> | <span data-ttu-id="2eaa0-111">Z como máximo</span><span class="sxs-lookup"><span data-stu-id="2eaa0-111">Maximum Z</span></span> | <span data-ttu-id="2eaa0-112">Número máximo de subprocesos (X \* Y \* Z)</span><span class="sxs-lookup"><span data-stu-id="2eaa0-112">Maximum Threads (X\*Y\*Z)</span></span> |
|----------------|-----------|---------------------------|
| <span data-ttu-id="2eaa0-113">CS \_ 4 \_ x</span><span class="sxs-lookup"><span data-stu-id="2eaa0-113">cs\_4\_x</span></span>       | <span data-ttu-id="2eaa0-114">1</span><span class="sxs-lookup"><span data-stu-id="2eaa0-114">1</span></span>         | <span data-ttu-id="2eaa0-115">768</span><span class="sxs-lookup"><span data-stu-id="2eaa0-115">768</span></span>                       |
| <span data-ttu-id="2eaa0-116">CS \_ 5 \_ 0</span><span class="sxs-lookup"><span data-stu-id="2eaa0-116">cs\_5\_0</span></span>       | <span data-ttu-id="2eaa0-117">64</span><span class="sxs-lookup"><span data-stu-id="2eaa0-117">64</span></span>        | <span data-ttu-id="2eaa0-118">1024</span><span class="sxs-lookup"><span data-stu-id="2eaa0-118">1024</span></span>                      |



 

<span data-ttu-id="2eaa0-119">En la ilustración siguiente se muestra la relación entre los parámetros pasados a [**ID3D11DeviceContext::D ispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch), dispatch (5, 3, 2), los valores especificados en el atributo numthreads, numthreads (10, 8, 3) y los valores que se pasarán al sombreador de cálculo para los valores del sistema relacionados con el subproceso ([VP \_ GroupIndex](sv-groupindex.md),[VP \_ DispatchThreadID](sv-dispatchthreadid.md),[VP \_ GroupThreadID](sv-groupthreadid.md),[VP \_ GroupID](sv-groupid.md))</span><span class="sxs-lookup"><span data-stu-id="2eaa0-119">The following illustration shows the relationship between the parameters passed to [**ID3D11DeviceContext::Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch), Dispatch(5,3,2), the values specified in the numthreads attribute, numthreads(10,8,3), and values that will passed to the compute shader for the thread related system values ([SV\_GroupIndex](sv-groupindex.md),[SV\_DispatchThreadID](sv-dispatchthreadid.md),[SV\_GroupThreadID](sv-groupthreadid.md),[SV\_GroupID](sv-groupid.md)).</span></span>

![Ilustración de la relación entre el envío, los grupos de subprocesos y los subprocesos](images/threadgroupids.png)

<span data-ttu-id="2eaa0-121">Este atributo es compatible con los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="2eaa0-121">This attribute is supported in the following types of shaders:</span></span>



| <span data-ttu-id="2eaa0-122">Vértice</span><span class="sxs-lookup"><span data-stu-id="2eaa0-122">Vertex</span></span> | <span data-ttu-id="2eaa0-123">Casco</span><span class="sxs-lookup"><span data-stu-id="2eaa0-123">Hull</span></span> | <span data-ttu-id="2eaa0-124">Dominio</span><span class="sxs-lookup"><span data-stu-id="2eaa0-124">Domain</span></span> | <span data-ttu-id="2eaa0-125">Geometría</span><span class="sxs-lookup"><span data-stu-id="2eaa0-125">Geometry</span></span> | <span data-ttu-id="2eaa0-126">Píxel</span><span class="sxs-lookup"><span data-stu-id="2eaa0-126">Pixel</span></span> | <span data-ttu-id="2eaa0-127">Compute</span><span class="sxs-lookup"><span data-stu-id="2eaa0-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | <span data-ttu-id="2eaa0-128">x</span><span class="sxs-lookup"><span data-stu-id="2eaa0-128">x</span></span>       |



 

## <a name="related-topics"></a><span data-ttu-id="2eaa0-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2eaa0-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2eaa0-130">Atributos del modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="2eaa0-130">Shader Model 5 Attributes</span></span>](d3d11-graphics-reference-sm5-attributes.md)
</dt> <dt>

[<span data-ttu-id="2eaa0-131">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="2eaa0-131">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 