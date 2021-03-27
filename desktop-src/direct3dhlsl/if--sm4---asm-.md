---
title: if (SM4-ASM)
description: Bifurcación basada en la lógica o en el resultado.
ms.assetid: 9F4CF9E0-4D9D-4300-B432-432C560F34BB
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 653c84be0d30a036bf93d852268e44bcca08bbcb
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104996849"
---
# <a name="if-sm4---asm"></a><span data-ttu-id="c2baf-103">if (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="c2baf-103">if (sm4 - asm)</span></span>

<span data-ttu-id="c2baf-104">Bifurcación basada en la lógica o en el resultado.</span><span class="sxs-lookup"><span data-stu-id="c2baf-104">Branch based on logical OR result.</span></span>



| <span data-ttu-id="c2baf-105">Si { \_ z </span><span class="sxs-lookup"><span data-stu-id="c2baf-105">if{\_z</span></span>\|<span data-ttu-id="c2baf-106">\_NZ} src0. Select ( \_ componente)</span><span class="sxs-lookup"><span data-stu-id="c2baf-106">\_nz} src0.select\_component</span></span> |
|--------------------------------------|



 



| <span data-ttu-id="c2baf-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="c2baf-107">Item</span></span>                                                            | <span data-ttu-id="c2baf-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="c2baf-108">Description</span></span>                                                              |
|-----------------------------------------------------------------|--------------------------------------------------------------------------|
| <span data-ttu-id="c2baf-109"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="c2baf-109"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="c2baf-110">\[en \] contiene el componente en el que se va a probar la condición.</span><span class="sxs-lookup"><span data-stu-id="c2baf-110">\[in\] Contains the component on which to test the condition.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c2baf-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c2baf-111">Remarks</span></span>

<span data-ttu-id="c2baf-112">El formato de token contiene el desplazamiento de la instrucción de endif correspondiente en el sombreador como una comodidad.</span><span class="sxs-lookup"><span data-stu-id="c2baf-112">The token format contains the offset of the corresponding endif instruction in the Shader as a convenience.</span></span>

<span data-ttu-id="c2baf-113">En el ejemplo siguiente se muestra cómo utilizar esta instrucción.</span><span class="sxs-lookup"><span data-stu-id="c2baf-113">The following example shows how to use this instruction.</span></span>

``` syntax
                if_z r0.x // if all bits in r0.x are zero
                   ...
                else // (optional)
                   ...
                endif
                if_nz r1.x // if any bit in r0.x is nonzero
                   ...
                else // (optional)
                   ...
                endif
```

### <a name="restrictions"></a><span data-ttu-id="c2baf-114">Restricciones</span><span class="sxs-lookup"><span data-stu-id="c2baf-114">Restrictions</span></span>

-   <span data-ttu-id="c2baf-115">Los operandos de origen (si 4 vectores de componente) deben utilizar un selector de componente único.</span><span class="sxs-lookup"><span data-stu-id="c2baf-115">The source operands (if 4 component vectors) must use a single component selector.</span></span>
-   <span data-ttu-id="c2baf-116">El registro de 32 bits proporcionado por *src0* se prueba en un nivel de bits.</span><span class="sxs-lookup"><span data-stu-id="c2baf-116">The 32-bit register supplied by *src0* is tested at a bit level.</span></span> <span data-ttu-id="c2baf-117">Si un bit es distinto de cero, **si \_ z** será true.</span><span class="sxs-lookup"><span data-stu-id="c2baf-117">If any bit is nonzero, **if\_z** will be true.</span></span> <span data-ttu-id="c2baf-118">Si todos los bits son cero, **si \_ NZ** será true.</span><span class="sxs-lookup"><span data-stu-id="c2baf-118">If all bits are zero, **if\_nz** will be true.</span></span>
-   <span data-ttu-id="c2baf-119">Los bloques de control de flujo pueden anidar hasta 64 de profundidad por subrutina (y Main).</span><span class="sxs-lookup"><span data-stu-id="c2baf-119">Flow control blocks can nest up to 64 deep per subroutine (and main).</span></span> <span data-ttu-id="c2baf-120">El compilador de HLSL no generará subrutinas que superen este límite.</span><span class="sxs-lookup"><span data-stu-id="c2baf-120">The HLSL compiler will not generate subroutines that exceed this limit.</span></span> <span data-ttu-id="c2baf-121">El comportamiento de las instrucciones de flujo de control más allá de 64 niveles de profundidad (por subrutina) es indefinido.</span><span class="sxs-lookup"><span data-stu-id="c2baf-121">Behavior of control flow instructions beyond 64 levels deep (per subroutine) is undefined.</span></span>

<span data-ttu-id="c2baf-122">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="c2baf-122">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="c2baf-123">Sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="c2baf-123">Vertex Shader</span></span> | <span data-ttu-id="c2baf-124">Sombreador de geometría</span><span class="sxs-lookup"><span data-stu-id="c2baf-124">Geometry Shader</span></span> | <span data-ttu-id="c2baf-125">Sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="c2baf-125">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="c2baf-126">x</span><span class="sxs-lookup"><span data-stu-id="c2baf-126">x</span></span>             | <span data-ttu-id="c2baf-127">x</span><span class="sxs-lookup"><span data-stu-id="c2baf-127">x</span></span>               | <span data-ttu-id="c2baf-128">x</span><span class="sxs-lookup"><span data-stu-id="c2baf-128">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="c2baf-129">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="c2baf-129">Minimum Shader Model</span></span>

<span data-ttu-id="c2baf-130">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="c2baf-130">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="c2baf-131">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="c2baf-131">Shader Model</span></span>                                              | <span data-ttu-id="c2baf-132">Compatible</span><span class="sxs-lookup"><span data-stu-id="c2baf-132">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="c2baf-133">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="c2baf-133">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="c2baf-134">sí</span><span class="sxs-lookup"><span data-stu-id="c2baf-134">yes</span></span>       |
| [<span data-ttu-id="c2baf-135">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="c2baf-135">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="c2baf-136">sí</span><span class="sxs-lookup"><span data-stu-id="c2baf-136">yes</span></span>       |
| [<span data-ttu-id="c2baf-137">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="c2baf-137">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="c2baf-138">sí</span><span class="sxs-lookup"><span data-stu-id="c2baf-138">yes</span></span>       |
| [<span data-ttu-id="c2baf-139">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c2baf-139">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="c2baf-140">no</span><span class="sxs-lookup"><span data-stu-id="c2baf-140">no</span></span>        |
| [<span data-ttu-id="c2baf-141">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c2baf-141">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="c2baf-142">no</span><span class="sxs-lookup"><span data-stu-id="c2baf-142">no</span></span>        |
| [<span data-ttu-id="c2baf-143">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c2baf-143">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="c2baf-144">no</span><span class="sxs-lookup"><span data-stu-id="c2baf-144">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="c2baf-145">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c2baf-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c2baf-146">Ensamblado modelo de sombreador 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c2baf-146">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





