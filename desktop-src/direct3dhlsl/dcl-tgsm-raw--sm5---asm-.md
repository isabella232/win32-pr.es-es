---
title: dcl_tgsm_raw (SM5-ASM)
description: Declare una referencia a una región del espacio de memoria compartido disponible para el grupo de subprocesos del sombreador de cálculo.
ms.assetid: 8EA6931C-5B13-431F-A886-04F8C73CD22D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd20d8a0d8d2309b9b895a5cb5439877bb10d31a
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "103785002"
---
# <a name="dcl_tgsm_raw-sm5---asm"></a><span data-ttu-id="65a0a-103">DCL \_ TGSM \_ raw (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="65a0a-103">dcl\_tgsm\_raw (sm5 - asm)</span></span>

<span data-ttu-id="65a0a-104">Declare una referencia a una región del espacio de memoria compartido disponible para el grupo de subprocesos del sombreador de cálculo.</span><span class="sxs-lookup"><span data-stu-id="65a0a-104">Declare a reference to a region of shared memory space available to the compute shader s thread group.</span></span>



| <span data-ttu-id="65a0a-105">\_TGSM \_ de DCL RAW g \# , byteCount</span><span class="sxs-lookup"><span data-stu-id="65a0a-105">dcl\_tgsm\_raw g\#, byteCount</span></span> |
|-------------------------------|



 



| <span data-ttu-id="65a0a-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="65a0a-106">Item</span></span>                                                                                                       | <span data-ttu-id="65a0a-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="65a0a-107">Description</span></span>                                                                             |
|------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="65a0a-108"><span id="g_"></span><span id="G_"></span>*i\#*</span><span class="sxs-lookup"><span data-stu-id="65a0a-108"><span id="g_"></span><span id="G_"></span>*g\#*</span></span><br/>                                                 | <span data-ttu-id="65a0a-109">\[en \] una referencia a un bloque de tamaño *byteCount* de memoria compartida sin tipo.</span><span class="sxs-lookup"><span data-stu-id="65a0a-109">\[in\] A reference to a block of size *byteCount* of untyped shared memory.</span></span> <br/> |
| <span data-ttu-id="65a0a-110"><span id="byteCount"></span><span id="bytecount"></span><span id="BYTECOUNT"></span>*byteCount*</span><span class="sxs-lookup"><span data-stu-id="65a0a-110"><span id="byteCount"></span><span id="bytecount"></span><span id="BYTECOUNT"></span>*byteCount*</span></span><br/> | <span data-ttu-id="65a0a-111">\[en \] debe ser un múltiplo de 4.</span><span class="sxs-lookup"><span data-stu-id="65a0a-111">\[in\] Must be a multiple of 4.</span></span> <br/>                                             |



 

## <a name="remarks"></a><span data-ttu-id="65a0a-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="65a0a-112">Remarks</span></span>

<span data-ttu-id="65a0a-113">El almacenamiento total de todos los g \# debe ser <= la cantidad de memoria compartida disponible por grupo de subprocesos, que es de 32 KB.</span><span class="sxs-lookup"><span data-stu-id="65a0a-113">The total storage for all g\# must be <= the amount of shared memory available per thread group, which is 32kB.</span></span>

<span data-ttu-id="65a0a-114">En un caso extremo, puede declarar 8192 g s en total \# , cada uno con un *byteCount* de 4.</span><span class="sxs-lookup"><span data-stu-id="65a0a-114">In an extreme case, you can declare 8192 total g\# s, each with a *byteCount* of 4.</span></span>

<span data-ttu-id="65a0a-115">En el extremo opuesto, puede declarar una sola g \# con un *byteCount* de 32768.</span><span class="sxs-lookup"><span data-stu-id="65a0a-115">In the opposite extreme, you can declare a single g\# with a *byteCount* of 32768.</span></span>

> [!Note]  
> <span data-ttu-id="65a0a-116">CS \_ 4 \_ 0 y CS \_ 4 \_ 1 admiten la [ \_ TGSM \_ de DCL](dcl-tgsm-structured--sm5---asm-.md), pero no la de **DCL \_ TGSM \_ raw**.</span><span class="sxs-lookup"><span data-stu-id="65a0a-116">cs\_4\_0 and cs\_4\_1 supports [dcl\_tgsm\_structured](dcl-tgsm-structured--sm5---asm-.md), but not **dcl\_tgsm\_raw**.</span></span>

 

<span data-ttu-id="65a0a-117">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="65a0a-117">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="65a0a-118">Vértice</span><span class="sxs-lookup"><span data-stu-id="65a0a-118">Vertex</span></span> | <span data-ttu-id="65a0a-119">Casco</span><span class="sxs-lookup"><span data-stu-id="65a0a-119">Hull</span></span> | <span data-ttu-id="65a0a-120">Dominio</span><span class="sxs-lookup"><span data-stu-id="65a0a-120">Domain</span></span> | <span data-ttu-id="65a0a-121">Geometría</span><span class="sxs-lookup"><span data-stu-id="65a0a-121">Geometry</span></span> | <span data-ttu-id="65a0a-122">Píxel</span><span class="sxs-lookup"><span data-stu-id="65a0a-122">Pixel</span></span> | <span data-ttu-id="65a0a-123">Compute</span><span class="sxs-lookup"><span data-stu-id="65a0a-123">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | <span data-ttu-id="65a0a-124">X</span><span class="sxs-lookup"><span data-stu-id="65a0a-124">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="65a0a-125">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="65a0a-125">Minimum Shader Model</span></span>

<span data-ttu-id="65a0a-126">Esta instrucción es compatible con los siguientes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="65a0a-126">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="65a0a-127">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="65a0a-127">Shader Model</span></span>                                              | <span data-ttu-id="65a0a-128">Compatible</span><span class="sxs-lookup"><span data-stu-id="65a0a-128">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="65a0a-129">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="65a0a-129">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="65a0a-130">sí</span><span class="sxs-lookup"><span data-stu-id="65a0a-130">yes</span></span>       |
| [<span data-ttu-id="65a0a-131">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="65a0a-131">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="65a0a-132">no</span><span class="sxs-lookup"><span data-stu-id="65a0a-132">no</span></span>        |
| [<span data-ttu-id="65a0a-133">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="65a0a-133">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="65a0a-134">no</span><span class="sxs-lookup"><span data-stu-id="65a0a-134">no</span></span>        |
| [<span data-ttu-id="65a0a-135">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="65a0a-135">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="65a0a-136">no</span><span class="sxs-lookup"><span data-stu-id="65a0a-136">no</span></span>        |
| [<span data-ttu-id="65a0a-137">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="65a0a-137">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="65a0a-138">no</span><span class="sxs-lookup"><span data-stu-id="65a0a-138">no</span></span>        |
| [<span data-ttu-id="65a0a-139">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="65a0a-139">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="65a0a-140">no</span><span class="sxs-lookup"><span data-stu-id="65a0a-140">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="65a0a-141">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="65a0a-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="65a0a-142">Ensamblador modelo de sombreador 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="65a0a-142">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





