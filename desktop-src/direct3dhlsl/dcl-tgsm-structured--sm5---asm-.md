---
title: dcl_tgsm_structured (SM5-ASM)
description: Declare una referencia a una región del espacio de memoria compartido disponible para el grupo de subprocesos del sombreador de cálculo. La memoria se ve como una matriz de estructuras.
ms.assetid: C42CD506-58EB-4740-8403-3F9BF29F0CAE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a639d31c4449a0dfeb152c06b35cfb86c5cc30a
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104996888"
---
# <a name="dcl_tgsm_structured-sm5---asm"></a><span data-ttu-id="0bc52-104">DCL \_ TGSM \_ estructurado (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="0bc52-104">dcl\_tgsm\_structured (sm5 - asm)</span></span>

<span data-ttu-id="0bc52-105">Declare una referencia a una región del espacio de memoria compartido disponible para el grupo de subprocesos del sombreador de cálculo.</span><span class="sxs-lookup"><span data-stu-id="0bc52-105">Declare a reference to a region of shared memory space available to the compute shader s thread group.</span></span> <span data-ttu-id="0bc52-106">La memoria se ve como una matriz de estructuras.</span><span class="sxs-lookup"><span data-stu-id="0bc52-106">The memory is viewed as an array of structures.</span></span>



| <span data-ttu-id="0bc52-107">DCL \_ TGSM \_ estructurado g \# , structByteStride, structCount</span><span class="sxs-lookup"><span data-stu-id="0bc52-107">dcl\_tgsm\_structured g\#, structByteStride, structCount</span></span> |
|----------------------------------------------------------|



 



| <span data-ttu-id="0bc52-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="0bc52-108">Item</span></span>                                                                                                                                   | <span data-ttu-id="0bc52-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="0bc52-109">Description</span></span>                                                                                                   |
|----------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0bc52-110"><span id="g_"></span><span id="G_"></span>*i\#*</span><span class="sxs-lookup"><span data-stu-id="0bc52-110"><span id="g_"></span><span id="G_"></span>*g\#*</span></span><br/>                                                                             | <span data-ttu-id="0bc52-111">\[en \] una referencia a un bloque de memoria compartida de tamaño *structByteStride* \* *structCount* bytes.</span><span class="sxs-lookup"><span data-stu-id="0bc52-111">\[in\] A reference to a block of shared memory of size *structByteStride* \* *structCount* bytes.</span></span> <br/> |
| <span data-ttu-id="0bc52-112"><span id="structByteStride"></span><span id="structbytestride"></span><span id="STRUCTBYTESTRIDE"></span>*structByteStride*</span><span class="sxs-lookup"><span data-stu-id="0bc52-112"><span id="structByteStride"></span><span id="structbytestride"></span><span id="STRUCTBYTESTRIDE"></span>*structByteStride*</span></span><br/> | <span data-ttu-id="0bc52-113">\[en \] el intervalo de la estructura.</span><span class="sxs-lookup"><span data-stu-id="0bc52-113">\[in\] The structure stride.</span></span> <span data-ttu-id="0bc52-114">Este valor es un uint en bytes y debe ser un múltiplo de 4.</span><span class="sxs-lookup"><span data-stu-id="0bc52-114">This value is a uint in bytes and must be a multiple of 4.</span></span> <br/>           |
| <span data-ttu-id="0bc52-115"><span id="structCount"></span><span id="structcount"></span><span id="STRUCTCOUNT"></span>*structCount*</span><span class="sxs-lookup"><span data-stu-id="0bc52-115"><span id="structCount"></span><span id="structcount"></span><span id="STRUCTCOUNT"></span>*structCount*</span></span><br/>                     | <span data-ttu-id="0bc52-116">\[en \] el número de estructuras.</span><span class="sxs-lookup"><span data-stu-id="0bc52-116">\[in\] The number of structures.</span></span><br/>                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="0bc52-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0bc52-117">Remarks</span></span>

<span data-ttu-id="0bc52-118">El almacenamiento total de todos los g \# debe ser <= la cantidad de memoria compartida disponible por grupo de subprocesos, que es de 32 KB o escalares de 8192 32 bits.</span><span class="sxs-lookup"><span data-stu-id="0bc52-118">The total storage for all g\# must be <= the amount of shared memory available per thread group, which is 32kB, or 8192 32-bit scalars.</span></span>

<span data-ttu-id="0bc52-119">En un caso extremo, puede declarar 8192 g s totales \# , si cada una tiene un *structByteStride* de 4 y un *structCount* de 1.</span><span class="sxs-lookup"><span data-stu-id="0bc52-119">In an extreme case, you can declare 8192 total g\# s, if each has a *structByteStride* of 4 and a *structCount* of 1.</span></span>

<span data-ttu-id="0bc52-120">En el extremo opuesto, puede declarar una sola g \# con un paso de estructura de 32 KB y un recuento de estructura de 1.</span><span class="sxs-lookup"><span data-stu-id="0bc52-120">In the opposite extreme, you can declare a single g\# with a structure stride of 32kB and a structure count of 1.</span></span>

<span data-ttu-id="0bc52-121">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="0bc52-121">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="0bc52-122">Vértice</span><span class="sxs-lookup"><span data-stu-id="0bc52-122">Vertex</span></span> | <span data-ttu-id="0bc52-123">Casco</span><span class="sxs-lookup"><span data-stu-id="0bc52-123">Hull</span></span> | <span data-ttu-id="0bc52-124">Dominio</span><span class="sxs-lookup"><span data-stu-id="0bc52-124">Domain</span></span> | <span data-ttu-id="0bc52-125">Geometría</span><span class="sxs-lookup"><span data-stu-id="0bc52-125">Geometry</span></span> | <span data-ttu-id="0bc52-126">Píxel</span><span class="sxs-lookup"><span data-stu-id="0bc52-126">Pixel</span></span> | <span data-ttu-id="0bc52-127">Compute</span><span class="sxs-lookup"><span data-stu-id="0bc52-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | <span data-ttu-id="0bc52-128">X</span><span class="sxs-lookup"><span data-stu-id="0bc52-128">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="0bc52-129">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="0bc52-129">Minimum Shader Model</span></span>

<span data-ttu-id="0bc52-130">Esta instrucción es compatible con los siguientes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="0bc52-130">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="0bc52-131">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="0bc52-131">Shader Model</span></span>                                              | <span data-ttu-id="0bc52-132">Compatible</span><span class="sxs-lookup"><span data-stu-id="0bc52-132">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="0bc52-133">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="0bc52-133">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="0bc52-134">sí</span><span class="sxs-lookup"><span data-stu-id="0bc52-134">yes</span></span>       |
| [<span data-ttu-id="0bc52-135">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="0bc52-135">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="0bc52-136">no</span><span class="sxs-lookup"><span data-stu-id="0bc52-136">no</span></span>        |
| [<span data-ttu-id="0bc52-137">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="0bc52-137">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="0bc52-138">no</span><span class="sxs-lookup"><span data-stu-id="0bc52-138">no</span></span>        |
| [<span data-ttu-id="0bc52-139">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0bc52-139">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="0bc52-140">no</span><span class="sxs-lookup"><span data-stu-id="0bc52-140">no</span></span>        |
| [<span data-ttu-id="0bc52-141">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0bc52-141">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="0bc52-142">no</span><span class="sxs-lookup"><span data-stu-id="0bc52-142">no</span></span>        |
| [<span data-ttu-id="0bc52-143">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0bc52-143">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="0bc52-144">no</span><span class="sxs-lookup"><span data-stu-id="0bc52-144">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="0bc52-145">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0bc52-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0bc52-146">Ensamblador modelo de sombreador 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0bc52-146">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





