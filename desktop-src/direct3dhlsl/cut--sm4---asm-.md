---
title: cortar (SM4-ASM)
description: Instrucción del sombreador de geometría que completa la topología primitiva actual (si se ha emitido algún vértice) e inicia una nueva topología del tipo declarado por el sombreador de geometría.
ms.assetid: 9B28E33D-F518-4844-BE3F-BE61B5F08B4F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c462d2f4dc2e0c6b4076f577610c93794e890af
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104983823"
---
# <a name="cut-sm4---asm"></a><span data-ttu-id="0aed2-103">cortar (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="0aed2-103">cut (sm4 - asm)</span></span>

<span data-ttu-id="0aed2-104">Instrucción del sombreador de geometría que completa la topología primitiva actual (si se ha emitido algún vértice) e inicia una nueva topología del tipo declarado por el sombreador de geometría.</span><span class="sxs-lookup"><span data-stu-id="0aed2-104">Geometry Shader instruction that completes the current primitive topology (if any vertices have been emitted), and starts a new topology of the type declared by the Geometry Shader.</span></span>



| <span data-ttu-id="0aed2-105">cut</span><span class="sxs-lookup"><span data-stu-id="0aed2-105">cut</span></span> |
|-----|



 

## <a name="remarks"></a><span data-ttu-id="0aed2-106">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0aed2-106">Remarks</span></span>

<span data-ttu-id="0aed2-107">Cuando se ejecuta **CUT** , lo primero que ocurre es que se completa cualquier topología emitida previamente por la invocación del sombreador de geometría.</span><span class="sxs-lookup"><span data-stu-id="0aed2-107">When **cut** is executed, the first thing that happens is that any previously emitted topology by the Geometry Shader invocation is completed.</span></span> <span data-ttu-id="0aed2-108">Si no se emitieron suficientes vértices para la topología primitiva anterior, se descartan.</span><span class="sxs-lookup"><span data-stu-id="0aed2-108">If not enough vertices were emitted for the previous primitive topology, they are discarded.</span></span> <span data-ttu-id="0aed2-109">Dado que las únicas topologías de salida disponibles para el sombreador de geometría son PointList, linestrip y trianglestrip, nunca hay vértices sobrantes al **cortar**.</span><span class="sxs-lookup"><span data-stu-id="0aed2-109">Because the only available output topologies for the Geometry Shader are pointlist, linestrip, and trianglestrip, there are never any leftover vertices upon **cut**.</span></span>

<span data-ttu-id="0aed2-110">Una vez completada la topología anterior, si la hubiera, la instrucción **CUT** provoca que se inicie una nueva topología, utilizando la topología declarada como la salida del sombreador de geometría.</span><span class="sxs-lookup"><span data-stu-id="0aed2-110">After the previous topology, if any, is completed, **cut** causes a new topology to begin, using the topology declared as the Geometry Shader output.</span></span>

## <a name="restrictions"></a><span data-ttu-id="0aed2-111">Restricciones</span><span class="sxs-lookup"><span data-stu-id="0aed2-111">Restrictions</span></span>

-   <span data-ttu-id="0aed2-112">La instrucción **CUT** solo se aplica al sombreador de geometría.</span><span class="sxs-lookup"><span data-stu-id="0aed2-112">The **cut** instruction applies only to the Geometry Shader.</span></span>
-   <span data-ttu-id="0aed2-113">**CUT** puede aparecer cualquier número de veces en el sombreador de geometría, incluido en el control de flujo.</span><span class="sxs-lookup"><span data-stu-id="0aed2-113">**cut** can appear any number of times in the Geometry Shader, including within flow control.</span></span>
-   <span data-ttu-id="0aed2-114">Si el sombreador de geometría finaliza y se emiten los vértices, se completa la topología que se está compilando, como si se ejecutara un **corte** como última instrucción.</span><span class="sxs-lookup"><span data-stu-id="0aed2-114">If the Geometry Shader ends and vertices have been emitted, the topology they are building is completed, as if a **cut** was executed as the last instruction.</span></span>
-   <span data-ttu-id="0aed2-115">Si se han declarado secuencias, se debe usar [Cut \_ Stream](cut-stream---sm5---asm-.md) en lugar de **CUT**.</span><span class="sxs-lookup"><span data-stu-id="0aed2-115">If streams have been declared, then [cut\_stream](cut-stream---sm5---asm-.md) must be used instead of **cut**.</span></span>

<span data-ttu-id="0aed2-116">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="0aed2-116">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="0aed2-117">Sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="0aed2-117">Vertex Shader</span></span> | <span data-ttu-id="0aed2-118">Sombreador de geometría</span><span class="sxs-lookup"><span data-stu-id="0aed2-118">Geometry Shader</span></span> | <span data-ttu-id="0aed2-119">Sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="0aed2-119">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
|               | <span data-ttu-id="0aed2-120">x</span><span class="sxs-lookup"><span data-stu-id="0aed2-120">x</span></span>               |              |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="0aed2-121">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="0aed2-121">Minimum Shader Model</span></span>

<span data-ttu-id="0aed2-122">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="0aed2-122">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="0aed2-123">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="0aed2-123">Shader Model</span></span>                                              | <span data-ttu-id="0aed2-124">Compatible</span><span class="sxs-lookup"><span data-stu-id="0aed2-124">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="0aed2-125">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="0aed2-125">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="0aed2-126">sí</span><span class="sxs-lookup"><span data-stu-id="0aed2-126">yes</span></span>       |
| [<span data-ttu-id="0aed2-127">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="0aed2-127">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="0aed2-128">sí</span><span class="sxs-lookup"><span data-stu-id="0aed2-128">yes</span></span>       |
| [<span data-ttu-id="0aed2-129">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="0aed2-129">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="0aed2-130">sí</span><span class="sxs-lookup"><span data-stu-id="0aed2-130">yes</span></span>       |
| [<span data-ttu-id="0aed2-131">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0aed2-131">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="0aed2-132">no</span><span class="sxs-lookup"><span data-stu-id="0aed2-132">no</span></span>        |
| [<span data-ttu-id="0aed2-133">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0aed2-133">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="0aed2-134">no</span><span class="sxs-lookup"><span data-stu-id="0aed2-134">no</span></span>        |
| [<span data-ttu-id="0aed2-135">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0aed2-135">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="0aed2-136">no</span><span class="sxs-lookup"><span data-stu-id="0aed2-136">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="0aed2-137">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0aed2-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0aed2-138">Ensamblado modelo de sombreador 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0aed2-138">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




