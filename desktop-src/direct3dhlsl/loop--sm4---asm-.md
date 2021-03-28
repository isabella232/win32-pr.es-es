---
title: bucle (SM4-ASM)
description: Especifica un bucle que recorre en iteración hasta que se encuentra una instrucción de salto.
ms.assetid: 0BEFADF4-036E-4FDA-9681-10965D6BA9FC
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 243bdf3b370d3505d787451162c22340acef3a45
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104996920"
---
# <a name="loop-sm4---asm"></a><span data-ttu-id="cb38b-103">bucle (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="cb38b-103">loop (sm4 - asm)</span></span>

<span data-ttu-id="cb38b-104">Especifica un bucle que recorre en iteración hasta que se encuentra una instrucción de salto.</span><span class="sxs-lookup"><span data-stu-id="cb38b-104">Specifies a loop which iterates until a break instruction is encountered.</span></span>



| <span data-ttu-id="cb38b-105">bucle</span><span class="sxs-lookup"><span data-stu-id="cb38b-105">loop</span></span> |
|------|



 

## <a name="remarks"></a><span data-ttu-id="cb38b-106">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cb38b-106">Remarks</span></span>

<span data-ttu-id="cb38b-107">**Loop** puede iterar indefinidamente, aunque se puede forzar la finalización de la ejecución general del sombreador después de que se ejecute un número indefinido de instrucciones.</span><span class="sxs-lookup"><span data-stu-id="cb38b-107">**loop** can iterate indefinitely, although overall execution of the Shader may be forced to terminate after some number of instructions are executed.</span></span>

<span data-ttu-id="cb38b-108">Los bloques de control de flujo pueden anidar hasta 64 de profundidad por subrutina y principal.</span><span class="sxs-lookup"><span data-stu-id="cb38b-108">Flow control blocks can nest up to 64 deep per subroutine and main.</span></span> <span data-ttu-id="cb38b-109">El compilador de HLSL no generará subrutinas que superen este límite.</span><span class="sxs-lookup"><span data-stu-id="cb38b-109">The HLSL compiler will not generate subroutines that exceed this limit.</span></span> <span data-ttu-id="cb38b-110">El comportamiento de las instrucciones de flujo de control más allá de 64 niveles de profundidad por subrutina es indefinido.</span><span class="sxs-lookup"><span data-stu-id="cb38b-110">Behavior of control flow instructions beyond 64 levels deep per subroutine is undefined.</span></span>

<span data-ttu-id="cb38b-111">El formato de token contiene el desplazamiento de la instrucción [ENDLOOP](endloop--sm4---asm-.md) correspondiente en el sombreador como una comodidad.</span><span class="sxs-lookup"><span data-stu-id="cb38b-111">The token format contains the offset of the corresponding [endloop](endloop--sm4---asm-.md) instruction in the Shader as a convenience.</span></span>

<span data-ttu-id="cb38b-112">En el ejemplo siguiente se muestra cómo usar la instrucción de bucle.</span><span class="sxs-lookup"><span data-stu-id="cb38b-112">The following example shows how to use the loop instruction.</span></span>

``` syntax
                loop
                    // example of termination condition
                    if_nz r0.x
                        break
                    endif
                    ...
                endloop
```

<span data-ttu-id="cb38b-113">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="cb38b-113">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="cb38b-114">Sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="cb38b-114">Vertex Shader</span></span> | <span data-ttu-id="cb38b-115">Sombreador de geometría</span><span class="sxs-lookup"><span data-stu-id="cb38b-115">Geometry Shader</span></span> | <span data-ttu-id="cb38b-116">Sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="cb38b-116">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="cb38b-117">x</span><span class="sxs-lookup"><span data-stu-id="cb38b-117">x</span></span>             | <span data-ttu-id="cb38b-118">x</span><span class="sxs-lookup"><span data-stu-id="cb38b-118">x</span></span>               | <span data-ttu-id="cb38b-119">x</span><span class="sxs-lookup"><span data-stu-id="cb38b-119">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="cb38b-120">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="cb38b-120">Minimum Shader Model</span></span>

<span data-ttu-id="cb38b-121">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="cb38b-121">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="cb38b-122">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="cb38b-122">Shader Model</span></span>                                              | <span data-ttu-id="cb38b-123">Compatible</span><span class="sxs-lookup"><span data-stu-id="cb38b-123">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="cb38b-124">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="cb38b-124">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="cb38b-125">sí</span><span class="sxs-lookup"><span data-stu-id="cb38b-125">yes</span></span>       |
| [<span data-ttu-id="cb38b-126">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="cb38b-126">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="cb38b-127">sí</span><span class="sxs-lookup"><span data-stu-id="cb38b-127">yes</span></span>       |
| [<span data-ttu-id="cb38b-128">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="cb38b-128">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="cb38b-129">sí</span><span class="sxs-lookup"><span data-stu-id="cb38b-129">yes</span></span>       |
| [<span data-ttu-id="cb38b-130">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="cb38b-130">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="cb38b-131">no</span><span class="sxs-lookup"><span data-stu-id="cb38b-131">no</span></span>        |
| [<span data-ttu-id="cb38b-132">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="cb38b-132">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="cb38b-133">no</span><span class="sxs-lookup"><span data-stu-id="cb38b-133">no</span></span>        |
| [<span data-ttu-id="cb38b-134">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="cb38b-134">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="cb38b-135">no</span><span class="sxs-lookup"><span data-stu-id="cb38b-135">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="cb38b-136">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="cb38b-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cb38b-137">Ensamblado modelo de sombreador 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="cb38b-137">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




