---
title: breakc (SM4-ASM)
description: Mueve condicionalmente el punto de ejecución a la instrucción después del siguiente ENDLOOP o endswitch.
ms.assetid: 5735EF88-1E8C-4142-8442-9328D78999A7
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 019a1c859f7d1e0ee6368f5b9984775ef9bfaba1
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104419943"
---
# <a name="breakc-sm4---asm"></a><span data-ttu-id="83971-103">breakc (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="83971-103">breakc (sm4 - asm)</span></span>

<span data-ttu-id="83971-104">Mueve condicionalmente el punto de ejecución a la instrucción después del siguiente [ENDLOOP](endloop--sm4---asm-.md) o [endswitch](endswitch--sm4---asm-.md).</span><span class="sxs-lookup"><span data-stu-id="83971-104">Conditionally moves the point of execution to the instruction after the next [endloop](endloop--sm4---asm-.md) or [endswitch](endswitch--sm4---asm-.md).</span></span>



| <span data-ttu-id="83971-105">breakc { \_ z </span><span class="sxs-lookup"><span data-stu-id="83971-105">breakc{\_z</span></span>\|<span data-ttu-id="83971-106">\_NZ} src0. Select ( \_ componente)</span><span class="sxs-lookup"><span data-stu-id="83971-106">\_nz} src0.select\_component</span></span> |
|------------------------------------------|



 



| <span data-ttu-id="83971-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="83971-107">Item</span></span>                                                            | <span data-ttu-id="83971-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="83971-108">Description</span></span>                                                     |
|-----------------------------------------------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="83971-109"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="83971-109"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="83971-110">\[en \] el componente en el que se va a probar la condición.</span><span class="sxs-lookup"><span data-stu-id="83971-110">\[in\] The component on which to test the condition.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="83971-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="83971-111">Remarks</span></span>

<span data-ttu-id="83971-112">El formato de token contiene el desplazamiento de la instrucción **ENDLOOP** correspondiente en el sombreador como una comodidad.</span><span class="sxs-lookup"><span data-stu-id="83971-112">The token format contains the offset of the corresponding **endloop** instruction in the Shader as a convenience.</span></span>

<span data-ttu-id="83971-113">En el ejemplo siguiente se muestra la instrucción **breakc** .</span><span class="sxs-lookup"><span data-stu-id="83971-113">The following example shows the **breakc** instruction.</span></span>


```
                loop
                    // example of termination condition
                    breakc_z  r0.x // break if all bits in r0.x are 0
                    breakc_nz r1.x // break if any bit in r1.x is nonzero
                    ...
                endloop

```



<span data-ttu-id="83971-114">Esta instrucción debe aparecer dentro de un **bucle** / **ENDLOOP** o **Switch** / **endswitch**.</span><span class="sxs-lookup"><span data-stu-id="83971-114">This instruction must appear within a **loop**/**endloop** or **switch**/**endswitch**.</span></span>

<span data-ttu-id="83971-115">El registro de 32 bits proporcionado por *src0* se prueba en un nivel de bits.</span><span class="sxs-lookup"><span data-stu-id="83971-115">The 32-bit register supplied by *src0* is tested at a bit level.</span></span> <span data-ttu-id="83971-116">Si algún bit es distinto de cero, **breakc \_ NZ** realizará la interrupción.</span><span class="sxs-lookup"><span data-stu-id="83971-116">If any bit is nonzero, **breakc\_nz** will perform the break.</span></span> <span data-ttu-id="83971-117">Si todos los bits son cero, **breakc \_ z** llevará a cabo la interrupción.</span><span class="sxs-lookup"><span data-stu-id="83971-117">If all bits are zero, **breakc\_z** will perform the break.</span></span>

<span data-ttu-id="83971-118">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="83971-118">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="83971-119">Sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="83971-119">Vertex Shader</span></span> | <span data-ttu-id="83971-120">Sombreador de geometría</span><span class="sxs-lookup"><span data-stu-id="83971-120">Geometry Shader</span></span> | <span data-ttu-id="83971-121">Sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="83971-121">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="83971-122">x</span><span class="sxs-lookup"><span data-stu-id="83971-122">x</span></span>             | <span data-ttu-id="83971-123">x</span><span class="sxs-lookup"><span data-stu-id="83971-123">x</span></span>               | <span data-ttu-id="83971-124">x</span><span class="sxs-lookup"><span data-stu-id="83971-124">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="83971-125">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="83971-125">Minimum Shader Model</span></span>

<span data-ttu-id="83971-126">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="83971-126">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="83971-127">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="83971-127">Shader Model</span></span>                                              | <span data-ttu-id="83971-128">Compatible</span><span class="sxs-lookup"><span data-stu-id="83971-128">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="83971-129">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="83971-129">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="83971-130">sí</span><span class="sxs-lookup"><span data-stu-id="83971-130">yes</span></span>       |
| [<span data-ttu-id="83971-131">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="83971-131">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="83971-132">sí</span><span class="sxs-lookup"><span data-stu-id="83971-132">yes</span></span>       |
| [<span data-ttu-id="83971-133">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="83971-133">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="83971-134">sí</span><span class="sxs-lookup"><span data-stu-id="83971-134">yes</span></span>       |
| [<span data-ttu-id="83971-135">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="83971-135">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="83971-136">no</span><span class="sxs-lookup"><span data-stu-id="83971-136">no</span></span>        |
| [<span data-ttu-id="83971-137">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="83971-137">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="83971-138">no</span><span class="sxs-lookup"><span data-stu-id="83971-138">no</span></span>        |
| [<span data-ttu-id="83971-139">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="83971-139">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="83971-140">no</span><span class="sxs-lookup"><span data-stu-id="83971-140">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="83971-141">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="83971-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="83971-142">Ensamblado modelo de sombreador 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="83971-142">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





