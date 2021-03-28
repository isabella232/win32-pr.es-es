---
title: emitThenCut (SM4-ASM)
description: Equivalente a un comando Emit seguido de un comando CUT. | emitThenCut (SM4-ASM)
ms.assetid: 80DE112A-790A-4DDF-A5BE-51F70BD7872C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb5b413ca11e22c7cfc17691fc0a39fe96bf7c0f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104362371"
---
# <a name="emitthencut-sm4---asm"></a><span data-ttu-id="56a22-104">emitThenCut (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="56a22-104">emitThenCut (sm4 - asm)</span></span>

<span data-ttu-id="56a22-105">Equivalente a un comando [Emit](emit--sm4---asm-.md) seguido de un comando [CUT](cut--sm4---asm-.md) .</span><span class="sxs-lookup"><span data-stu-id="56a22-105">Equivalent to an [emit](emit--sm4---asm-.md) command followed by a [cut](cut--sm4---asm-.md) command.</span></span>



| <span data-ttu-id="56a22-106">emitThenCut</span><span class="sxs-lookup"><span data-stu-id="56a22-106">emitThenCut</span></span> |
|-------------|



 

## <a name="remarks"></a><span data-ttu-id="56a22-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="56a22-107">Remarks</span></span>

<span data-ttu-id="56a22-108">Este comando es útil cuando se genera de forma consciente el último vértice de una topología.</span><span class="sxs-lookup"><span data-stu-id="56a22-108">This command is useful when knowingly outputting the last vertex in a topology.</span></span>

<span data-ttu-id="56a22-109">Si se han declarado secuencias, debe usar la [ \_ secuencia emitthencut](emitthencut-stream--sm5---asm-.md).</span><span class="sxs-lookup"><span data-stu-id="56a22-109">If streams have been declared, you must use [emitthencut\_stream](emitthencut-stream--sm5---asm-.md).</span></span>

<span data-ttu-id="56a22-110">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="56a22-110">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="56a22-111">Sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="56a22-111">Vertex Shader</span></span> | <span data-ttu-id="56a22-112">Sombreador de geometría</span><span class="sxs-lookup"><span data-stu-id="56a22-112">Geometry Shader</span></span> | <span data-ttu-id="56a22-113">Sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="56a22-113">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
|               | <span data-ttu-id="56a22-114">x</span><span class="sxs-lookup"><span data-stu-id="56a22-114">x</span></span>               |              |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="56a22-115">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="56a22-115">Minimum Shader Model</span></span>

<span data-ttu-id="56a22-116">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="56a22-116">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="56a22-117">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="56a22-117">Shader Model</span></span>                                              | <span data-ttu-id="56a22-118">Compatible</span><span class="sxs-lookup"><span data-stu-id="56a22-118">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="56a22-119">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="56a22-119">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="56a22-120">sí</span><span class="sxs-lookup"><span data-stu-id="56a22-120">yes</span></span>       |
| [<span data-ttu-id="56a22-121">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="56a22-121">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="56a22-122">sí</span><span class="sxs-lookup"><span data-stu-id="56a22-122">yes</span></span>       |
| [<span data-ttu-id="56a22-123">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="56a22-123">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="56a22-124">sí</span><span class="sxs-lookup"><span data-stu-id="56a22-124">yes</span></span>       |
| [<span data-ttu-id="56a22-125">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="56a22-125">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="56a22-126">no</span><span class="sxs-lookup"><span data-stu-id="56a22-126">no</span></span>        |
| [<span data-ttu-id="56a22-127">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="56a22-127">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="56a22-128">no</span><span class="sxs-lookup"><span data-stu-id="56a22-128">no</span></span>        |
| [<span data-ttu-id="56a22-129">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="56a22-129">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="56a22-130">no</span><span class="sxs-lookup"><span data-stu-id="56a22-130">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="56a22-131">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="56a22-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="56a22-132">Ensamblado modelo de sombreador 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="56a22-132">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




