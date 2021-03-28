---
title: ENDLOOP (SM4-ASM)
description: Finaliza una instrucción de bucle.
ms.assetid: 0BEFADF4-036E-4FDA-9681-10965D6BA9FC
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 655fa6addd19a6ce9f6f6b20a2677ef43cb8b751
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104419878"
---
# <a name="endloop-sm4---asm"></a><span data-ttu-id="3a918-103">ENDLOOP (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="3a918-103">endloop (sm4 - asm)</span></span>

<span data-ttu-id="3a918-104">Finaliza una instrucción de bucle.</span><span class="sxs-lookup"><span data-stu-id="3a918-104">Ends a loop statement.</span></span>



| <span data-ttu-id="3a918-105">ENDLOOP</span><span class="sxs-lookup"><span data-stu-id="3a918-105">endloop</span></span> |
|---------|



 

## <a name="remarks"></a><span data-ttu-id="3a918-106">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3a918-106">Remarks</span></span>

<span data-ttu-id="3a918-107">En el ejemplo siguiente se muestra cómo utilizar esta instrucción.</span><span class="sxs-lookup"><span data-stu-id="3a918-107">The following example shows how to use this instruction.</span></span>

``` syntax
                loop
                    // example of termination condition
                    if_nz r0.x
                        break
                    endif
                    ...
                endloop
```

<span data-ttu-id="3a918-108">El formato de token contiene el desplazamiento de la instrucción de bucle correspondiente en el sombreador como una comodidad.</span><span class="sxs-lookup"><span data-stu-id="3a918-108">The token format contains the offset of the corresponding loop instruction in the Shader as a convenience.</span></span>

<span data-ttu-id="3a918-109">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="3a918-109">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="3a918-110">Sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="3a918-110">Vertex Shader</span></span> | <span data-ttu-id="3a918-111">Sombreador de geometría</span><span class="sxs-lookup"><span data-stu-id="3a918-111">Geometry Shader</span></span> | <span data-ttu-id="3a918-112">Sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="3a918-112">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="3a918-113">x</span><span class="sxs-lookup"><span data-stu-id="3a918-113">x</span></span>             | <span data-ttu-id="3a918-114">x</span><span class="sxs-lookup"><span data-stu-id="3a918-114">x</span></span>               | <span data-ttu-id="3a918-115">x</span><span class="sxs-lookup"><span data-stu-id="3a918-115">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="3a918-116">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="3a918-116">Minimum Shader Model</span></span>

<span data-ttu-id="3a918-117">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="3a918-117">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="3a918-118">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="3a918-118">Shader Model</span></span>                                              | <span data-ttu-id="3a918-119">Compatible</span><span class="sxs-lookup"><span data-stu-id="3a918-119">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="3a918-120">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="3a918-120">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="3a918-121">sí</span><span class="sxs-lookup"><span data-stu-id="3a918-121">yes</span></span>       |
| [<span data-ttu-id="3a918-122">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="3a918-122">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="3a918-123">sí</span><span class="sxs-lookup"><span data-stu-id="3a918-123">yes</span></span>       |
| [<span data-ttu-id="3a918-124">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="3a918-124">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="3a918-125">sí</span><span class="sxs-lookup"><span data-stu-id="3a918-125">yes</span></span>       |
| [<span data-ttu-id="3a918-126">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3a918-126">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="3a918-127">no</span><span class="sxs-lookup"><span data-stu-id="3a918-127">no</span></span>        |
| [<span data-ttu-id="3a918-128">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3a918-128">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="3a918-129">no</span><span class="sxs-lookup"><span data-stu-id="3a918-129">no</span></span>        |
| [<span data-ttu-id="3a918-130">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3a918-130">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="3a918-131">no</span><span class="sxs-lookup"><span data-stu-id="3a918-131">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="3a918-132">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3a918-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3a918-133">Ensamblado modelo de sombreador 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3a918-133">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




