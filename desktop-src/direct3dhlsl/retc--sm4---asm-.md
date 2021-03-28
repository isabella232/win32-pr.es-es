---
title: RETC (SM4-ASM)
description: Devolución condicional.
ms.assetid: D936099D-4A75-4AE2-9FE3-70ED213DF4D9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e394bc6b947d91fafb09dbfdc075b0c60be2cf8
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104983882"
---
# <a name="retc-sm4---asm"></a><span data-ttu-id="5849b-103">RETC (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="5849b-103">retc (sm4 - asm)</span></span>

<span data-ttu-id="5849b-104">Devolución condicional.</span><span class="sxs-lookup"><span data-stu-id="5849b-104">Conditional return.</span></span>



| <span data-ttu-id="5849b-105">RETC { \_ z </span><span class="sxs-lookup"><span data-stu-id="5849b-105">retc{\_z</span></span>\|<span data-ttu-id="5849b-106">\_NZ} src0. Select ( \_ componente)</span><span class="sxs-lookup"><span data-stu-id="5849b-106">\_nz} src0.select\_component</span></span> |
|----------------------------------------|



 



| <span data-ttu-id="5849b-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="5849b-107">Item</span></span>                                                            | <span data-ttu-id="5849b-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="5849b-108">Description</span></span>                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="5849b-109"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="5849b-109"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="5849b-110">\[en \] el registro en el que se va a probar la condición.</span><span class="sxs-lookup"><span data-stu-id="5849b-110">\[in\] The register to test the condition against.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="5849b-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5849b-111">Remarks</span></span>

<span data-ttu-id="5849b-112">Si se encuentra dentro de una subrutina, esta instrucción devuelve condicionalmente a la instrucción después de la llamada.</span><span class="sxs-lookup"><span data-stu-id="5849b-112">If within a subroutine, this instruction conditionally returns to the instruction after the call.</span></span> <span data-ttu-id="5849b-113">Si no está dentro de una subrutina, esta instrucción finaliza la ejecución del programa.</span><span class="sxs-lookup"><span data-stu-id="5849b-113">If not inside a subroutine, this instruction terminates program execution.</span></span>

<span data-ttu-id="5849b-114">En el ejemplo siguiente se muestra cómo utilizar esta instrucción.</span><span class="sxs-lookup"><span data-stu-id="5849b-114">The following example shows how to use this instruction.</span></span>

``` syntax
           ...
           call l3
           ...
           ret
           label l3
               ...
               retc_nz r0.x  // If any bit in r0.x is nonzero, then return
               retc_z  r1.x  // If all bits in r0.x are zero, then return.
               ...
           ret
```

### <a name="restrictions"></a><span data-ttu-id="5849b-115">Restricciones</span><span class="sxs-lookup"><span data-stu-id="5849b-115">Restrictions</span></span>

-   <span data-ttu-id="5849b-116">**RETC** puede aparecer en cualquier parte de un programa, en cualquier número de veces.</span><span class="sxs-lookup"><span data-stu-id="5849b-116">**retc** can appear anywhere in a program, any number of times.</span></span>
-   <span data-ttu-id="5849b-117">La última instrucción de un programa o subrutina principal no puede ser **RETC \_ z** ni **RETC \_ NZ**.</span><span class="sxs-lookup"><span data-stu-id="5849b-117">The last instruction in a main program or subroutine cannot be a **retc\_z** or **retc\_nz**.</span></span> <span data-ttu-id="5849b-118">En su lugar, se puede usar el [RET](ret--sm4---asm-.md) incondicional.</span><span class="sxs-lookup"><span data-stu-id="5849b-118">Instead, the unconditional [ret](ret--sm4---asm-.md) can be used.</span></span>
-   <span data-ttu-id="5849b-119">El registro de 32 bits proporcionado por *src0* se prueba en un nivel de bits.</span><span class="sxs-lookup"><span data-stu-id="5849b-119">The 32-bit register supplied by *src0* is tested at a bit level.</span></span> <span data-ttu-id="5849b-120">Si un bit es distinto de cero, **RET \_ NZ** devolverá.</span><span class="sxs-lookup"><span data-stu-id="5849b-120">If any bit is nonzero, **ret\_nz** will return.</span></span> <span data-ttu-id="5849b-121">Si todos los bits son cero, **RETC \_ z** devolverá.</span><span class="sxs-lookup"><span data-stu-id="5849b-121">If all bits are zero, **retc\_z** will return.</span></span>

<span data-ttu-id="5849b-122">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="5849b-122">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="5849b-123">Sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="5849b-123">Vertex Shader</span></span> | <span data-ttu-id="5849b-124">Sombreador de geometría</span><span class="sxs-lookup"><span data-stu-id="5849b-124">Geometry Shader</span></span> | <span data-ttu-id="5849b-125">Sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="5849b-125">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="5849b-126">x</span><span class="sxs-lookup"><span data-stu-id="5849b-126">x</span></span>             | <span data-ttu-id="5849b-127">x</span><span class="sxs-lookup"><span data-stu-id="5849b-127">x</span></span>               | <span data-ttu-id="5849b-128">x</span><span class="sxs-lookup"><span data-stu-id="5849b-128">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="5849b-129">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="5849b-129">Minimum Shader Model</span></span>

<span data-ttu-id="5849b-130">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="5849b-130">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="5849b-131">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="5849b-131">Shader Model</span></span>                                              | <span data-ttu-id="5849b-132">Compatible</span><span class="sxs-lookup"><span data-stu-id="5849b-132">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="5849b-133">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="5849b-133">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="5849b-134">sí</span><span class="sxs-lookup"><span data-stu-id="5849b-134">yes</span></span>       |
| [<span data-ttu-id="5849b-135">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="5849b-135">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="5849b-136">sí</span><span class="sxs-lookup"><span data-stu-id="5849b-136">yes</span></span>       |
| [<span data-ttu-id="5849b-137">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="5849b-137">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="5849b-138">sí</span><span class="sxs-lookup"><span data-stu-id="5849b-138">yes</span></span>       |
| [<span data-ttu-id="5849b-139">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5849b-139">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="5849b-140">no</span><span class="sxs-lookup"><span data-stu-id="5849b-140">no</span></span>        |
| [<span data-ttu-id="5849b-141">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5849b-141">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="5849b-142">no</span><span class="sxs-lookup"><span data-stu-id="5849b-142">no</span></span>        |
| [<span data-ttu-id="5849b-143">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5849b-143">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="5849b-144">no</span><span class="sxs-lookup"><span data-stu-id="5849b-144">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="5849b-145">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5849b-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5849b-146">Ensamblado modelo de sombreador 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5849b-146">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





