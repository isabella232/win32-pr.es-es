---
title: Switch (SM4-ASM)
description: Transfiere el control a un bloque de instrucciones distinto en el cuerpo del modificador en función del valor de un selector.
ms.assetid: ECAEECFD-B955-4356-B5C9-1D6A04C71D8F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: feed346b8aa33feecc13fe2a6ffad59c961b0173
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104077096"
---
# <a name="switch-sm4---asm"></a><span data-ttu-id="71d5b-103">Switch (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="71d5b-103">switch (sm4 - asm)</span></span>

<span data-ttu-id="71d5b-104">Transfiere el control a un bloque de instrucciones distinto en el cuerpo del modificador en función del valor de un selector.</span><span class="sxs-lookup"><span data-stu-id="71d5b-104">Transfers control to a different statement block within the switch body depending on the value of a selector.</span></span>



| <span data-ttu-id="71d5b-105">cambiar src0. \_ componente seleccionado</span><span class="sxs-lookup"><span data-stu-id="71d5b-105">switch src0.selected\_component</span></span> |
|---------------------------------|



 



| <span data-ttu-id="71d5b-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="71d5b-106">Item</span></span>                                                            | <span data-ttu-id="71d5b-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="71d5b-107">Description</span></span>                                              |
|-----------------------------------------------------------------|----------------------------------------------------------|
| <span data-ttu-id="71d5b-108"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="71d5b-108"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="71d5b-109">\[en \] el selector de la instrucción switch.</span><span class="sxs-lookup"><span data-stu-id="71d5b-109">\[in\] The selector for the switch statement.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="71d5b-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="71d5b-110">Remarks</span></span>

<span data-ttu-id="71d5b-111">Una construcción **Switch** / [endswitch](endswitch--sm4---asm-.md) se comporta exactamente como una construcción de **modificador** en el lenguaje C, con la siguiente excepción: para las [](case--sm4---asm-.md) / instrucciones [predeterminadas](default--sm4---asm-.md) de D3D11 case que pasen al siguiente **caso** / **predeterminado** sin [interrupción](break--sm4---asm-.md) no puede tener código en ellas.</span><span class="sxs-lookup"><span data-stu-id="71d5b-111">A **switch**/[endswitch](endswitch--sm4---asm-.md) construct behaves exactly as a **switch** construct in the C language, with the following exception: for D3D11 [case](case--sm4---asm-.md)/[default](default--sm4---asm-.md) statements that fall through to the next **case**/**default** without a [break](break--sm4---asm-.md) cannot have any code in them.</span></span> <span data-ttu-id="71d5b-112">Se permite que varias instrucciones **Case** , como **default**, aparezcan secuencialmente, compartiendo el mismo bloque de código.</span><span class="sxs-lookup"><span data-stu-id="71d5b-112">It is permitted for multiple **case** statements, including **default**, to appear sequentially, sharing the same code block.</span></span>

<span data-ttu-id="71d5b-113">La condición debe ser un componente de registro de 32 bits o una cantidad inmediata.</span><span class="sxs-lookup"><span data-stu-id="71d5b-113">The condition must be a 32-bit register component or immediate quantity.</span></span> <span data-ttu-id="71d5b-114">La comparación de igualdad es bit a bit (entero).</span><span class="sxs-lookup"><span data-stu-id="71d5b-114">The equality comparison is bitwise (integer).</span></span>

<span data-ttu-id="71d5b-115">Como con cualquier instrucción del sombreador en el D3D11, el hardware puede o no implementar directamente la construcción **Switch** .</span><span class="sxs-lookup"><span data-stu-id="71d5b-115">As with any Shader instruction in the D3D11, hardware may or may not implement the **switch** construct directly.</span></span>

<span data-ttu-id="71d5b-116">Las instrucciones **Switch** pueden estar anidadas.</span><span class="sxs-lookup"><span data-stu-id="71d5b-116">**Switch** statements can be nested.</span></span> <span data-ttu-id="71d5b-117">Cada bloque **Switch** cuenta como 1 nivel en el límite de profundidad de anidamiento del control de flujo de 64 por subrutina y principal, independientemente del número de instrucciones **Case** .</span><span class="sxs-lookup"><span data-stu-id="71d5b-117">Each **switch** block counts as 1 level against the flow control nesting depth limit of 64 per subroutine and main, independent of the number of **case** statements.</span></span> <span data-ttu-id="71d5b-118">El compilador de HLSL no generará subrutinas que superen este límite.</span><span class="sxs-lookup"><span data-stu-id="71d5b-118">The HLSL compiler will not generate subroutines that exceed this limit.</span></span> <span data-ttu-id="71d5b-119">El comportamiento de las instrucciones de flujo de control más allá de 64 niveles de profundidad por subrutina es indefinido.</span><span class="sxs-lookup"><span data-stu-id="71d5b-119">Behavior of control flow instructions beyond 64 levels deep per subroutine is undefined.</span></span>

<span data-ttu-id="71d5b-120">En el ejemplo siguiente se muestra cómo utilizar esta instrucción.</span><span class="sxs-lookup"><span data-stu-id="71d5b-120">The following example shows how to use this instruction.</span></span>

``` syntax
                ...
                switch r0.x
                default: // falling through
                case 3
                    switch r1.x
                    case 4
                        ...
                        break
                    case 5
                        ...
                        break
                    endswitch
                    break
                case 0
                    break
                endswitch
```

<span data-ttu-id="71d5b-121">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="71d5b-121">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="71d5b-122">Sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="71d5b-122">Vertex Shader</span></span> | <span data-ttu-id="71d5b-123">Sombreador de geometría</span><span class="sxs-lookup"><span data-stu-id="71d5b-123">Geometry Shader</span></span> | <span data-ttu-id="71d5b-124">Sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="71d5b-124">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="71d5b-125">x</span><span class="sxs-lookup"><span data-stu-id="71d5b-125">x</span></span>             | <span data-ttu-id="71d5b-126">x</span><span class="sxs-lookup"><span data-stu-id="71d5b-126">x</span></span>               | <span data-ttu-id="71d5b-127">x</span><span class="sxs-lookup"><span data-stu-id="71d5b-127">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="71d5b-128">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="71d5b-128">Minimum Shader Model</span></span>

<span data-ttu-id="71d5b-129">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="71d5b-129">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="71d5b-130">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="71d5b-130">Shader Model</span></span>                                              | <span data-ttu-id="71d5b-131">Compatible</span><span class="sxs-lookup"><span data-stu-id="71d5b-131">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="71d5b-132">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="71d5b-132">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="71d5b-133">sí</span><span class="sxs-lookup"><span data-stu-id="71d5b-133">yes</span></span>       |
| [<span data-ttu-id="71d5b-134">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="71d5b-134">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="71d5b-135">sí</span><span class="sxs-lookup"><span data-stu-id="71d5b-135">yes</span></span>       |
| [<span data-ttu-id="71d5b-136">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="71d5b-136">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="71d5b-137">sí</span><span class="sxs-lookup"><span data-stu-id="71d5b-137">yes</span></span>       |
| [<span data-ttu-id="71d5b-138">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="71d5b-138">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="71d5b-139">no</span><span class="sxs-lookup"><span data-stu-id="71d5b-139">no</span></span>        |
| [<span data-ttu-id="71d5b-140">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="71d5b-140">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="71d5b-141">no</span><span class="sxs-lookup"><span data-stu-id="71d5b-141">no</span></span>        |
| [<span data-ttu-id="71d5b-142">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="71d5b-142">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="71d5b-143">no</span><span class="sxs-lookup"><span data-stu-id="71d5b-143">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="71d5b-144">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="71d5b-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="71d5b-145">Ensamblado modelo de sombreador 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="71d5b-145">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





