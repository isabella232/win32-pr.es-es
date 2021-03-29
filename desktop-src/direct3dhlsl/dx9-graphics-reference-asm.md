---
title: Referencia del sombreador de ASM
description: Los sombreadores controlan la canalización programable de gráficos.
ms.assetid: 2c58815c-83b5-4ae8-a192-ba865b485bd6
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2941f4c32d03187ce08266bf1382cd1d94301ce0
ms.sourcegitcommit: 477b1efe7d9c2f91d5f2ac588a20edf348b1c734
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2019
ms.locfileid: "104983931"
---
# <a name="asm-shader-reference"></a><span data-ttu-id="58e65-103">Referencia del sombreador de ASM</span><span class="sxs-lookup"><span data-stu-id="58e65-103">Asm Shader Reference</span></span>

<span data-ttu-id="58e65-104">Los sombreadores controlan la canalización programable de gráficos.</span><span class="sxs-lookup"><span data-stu-id="58e65-104">Shaders drive the programmable graphics pipeline.</span></span>

## <a name="vertex-shader-reference"></a><span data-ttu-id="58e65-105">Referencia del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="58e65-105">Vertex Shader Reference</span></span>

-   [<span data-ttu-id="58e65-106">vs \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="58e65-106">vs\_1\_1</span></span>](dx9-graphics-reference-asm-vs-1-1.md)
-   [<span data-ttu-id="58e65-107">vs \_ 2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="58e65-107">vs\_2\_0</span></span>](dx9-graphics-reference-asm-vs-2-0.md)
-   [<span data-ttu-id="58e65-108">vs \_ 2 \_ x</span><span class="sxs-lookup"><span data-stu-id="58e65-108">vs\_2\_x</span></span>](dx9-graphics-reference-asm-vs-2-x.md)
-   [<span data-ttu-id="58e65-109">vs \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="58e65-109">vs\_3\_0</span></span>](dx9-graphics-reference-asm-vs-3-0.md)

<span data-ttu-id="58e65-110">Las [diferencias del sombreador de vértices](dx9-graphics-reference-asm-vs-differences.md) resumen las diferencias entre las versiones del sombreador de vértices.</span><span class="sxs-lookup"><span data-stu-id="58e65-110">[Vertex Shader Differences](dx9-graphics-reference-asm-vs-differences.md) summarizes the differences between vertex shader versions.</span></span>

## <a name="pixel-shader-reference"></a><span data-ttu-id="58e65-111">Referencia del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="58e65-111">Pixel Shader Reference</span></span>

-   [<span data-ttu-id="58e65-112">PS \_ 1 \_ , PS \_ 1 \_ 2, PS 1 \_ \_ 3, PS \_ 1 \_ 4</span><span class="sxs-lookup"><span data-stu-id="58e65-112">ps\_1\_1, ps\_1\_2, ps\_1\_3, ps\_1\_4</span></span>](dx9-graphics-reference-asm-ps-1-x.md)
-   [<span data-ttu-id="58e65-113">PS \_ 2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="58e65-113">ps\_2\_0</span></span>](dx9-graphics-reference-asm-ps-2-0.md)
-   [<span data-ttu-id="58e65-114">PS \_ 2 \_ x</span><span class="sxs-lookup"><span data-stu-id="58e65-114">ps\_2\_x</span></span>](dx9-graphics-reference-asm-ps-2-x.md)
-   [<span data-ttu-id="58e65-115">PS \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="58e65-115">ps\_3\_0</span></span>](dx9-graphics-reference-asm-ps-3-0.md)

<span data-ttu-id="58e65-116">Las [diferencias del sombreador de píxeles](dx9-graphics-reference-asm-ps-differences.md) resumen las diferencias entre las versiones del sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="58e65-116">[Pixel Shader Differences](dx9-graphics-reference-asm-ps-differences.md) summarizes the differences between pixel shader versions.</span></span>

## <a name="shader-model-4-and-5-reference"></a><span data-ttu-id="58e65-117">Referencia del modelo de sombreador 4 y 5</span><span class="sxs-lookup"><span data-stu-id="58e65-117">Shader Model 4 and 5 Reference</span></span>

<span data-ttu-id="58e65-118">Las secciones del ensamblado del modelo de [sombreador 4](dx-graphics-hlsl-sm4-asm.md) y del [modelo de sombreador modelo 5](shader-model-5-assembly--directx-hlsl-.md) describen las instrucciones que admiten el modelo de sombreador 4 y 5.</span><span class="sxs-lookup"><span data-stu-id="58e65-118">The [Shader Model 4 Assembly](dx-graphics-hlsl-sm4-asm.md) and [Shader Model 5 Assembly](shader-model-5-assembly--directx-hlsl-.md) sections describe the instructions that shader model 4 and 5 support.</span></span>

## <a name="behavior-of-constant-registers-in-assembly-shaders"></a><span data-ttu-id="58e65-119">Comportamiento de registros constantes en sombreadores de ensamblados</span><span class="sxs-lookup"><span data-stu-id="58e65-119">Behavior of Constant Registers in Assembly Shaders</span></span>

<span data-ttu-id="58e65-120">Hay dos maneras de establecer registros constantes en un sombreador de ensamblado:</span><span class="sxs-lookup"><span data-stu-id="58e65-120">There are two ways to set constant registers in an assembly shader:</span></span>

-   <span data-ttu-id="58e65-121">Declare una constante de sombreador en el código de ensamblado mediante una de las instrucciones de Def \* .</span><span class="sxs-lookup"><span data-stu-id="58e65-121">Declare a shader constant in assembly code using one of the def\* instructions.</span></span>
-   <span data-ttu-id="58e65-122">Use uno de los métodos set de la \* \* \* API de ShaderConstant \* .</span><span class="sxs-lookup"><span data-stu-id="58e65-122">Use one of the Set\*\*\*ShaderConstant\* API methods.</span></span>

### <a name="direct3d-9-shader-constants"></a><span data-ttu-id="58e65-123">Constantes de sombreador de Direct3D 9</span><span class="sxs-lookup"><span data-stu-id="58e65-123">Direct3D 9 Shader Constants</span></span>

<span data-ttu-id="58e65-124">En Direct3D 9, la duración de las constantes definidas en un sombreador determinado se limita solo a la ejecución de ese sombreador (y no es reemplazable).</span><span class="sxs-lookup"><span data-stu-id="58e65-124">In Direct3D 9 the lifetime of defined constants in a given shader is confined to the execution of that shader only (and is non-overridable).</span></span> <span data-ttu-id="58e65-125">Las constantes definidas en Direct3D 9 no tienen efectos secundarios fuera del sombreador.</span><span class="sxs-lookup"><span data-stu-id="58e65-125">Defined constants in Direct3D 9 have no side effects outside of the shader.</span></span>

<span data-ttu-id="58e65-126">Este es un ejemplo de uso de Direct3D 9:</span><span class="sxs-lookup"><span data-stu-id="58e65-126">Here's an example using Direct3D 9:</span></span>


```
Given: 
    Create shader1 which references c4 and defines it with the def instruction

Scenario 1:
    Call Set***Shader shader1
    Call Set***ShaderConstant* to set c4
    Call Draw
    Result: The shader will see the def'd value in c4

    
Given: 
    Scenario 1 has just completed
    Create shader2 (which references c4 but does not use the def instruction
      to define it) 

Scenario 2: 
    Call Set***Shader shader2
    Call Draw
    Result: The shader will see the value last set in c4 by 
     Set***ShaderConstant* in scenario 1. This is because shader 2 
     didn't def c4.
```



<span data-ttu-id="58e65-127">En Direct3D 9, al llamar a get \* \* \* ShaderConstant \* solo se recuperarán los valores constantes establecidos mediante set \* \* \* ShaderConstant \* .</span><span class="sxs-lookup"><span data-stu-id="58e65-127">In Direct3D 9, calling Get\*\*\*ShaderConstant\* will only retrieve constant values set via Set\*\*\*ShaderConstant\*.</span></span>

### <a name="direct3d-8-shader-constants"></a><span data-ttu-id="58e65-128">Constantes de sombreador de Direct3D 8</span><span class="sxs-lookup"><span data-stu-id="58e65-128">Direct3D 8 Shader Constants</span></span>

<span data-ttu-id="58e65-129">Este comportamiento es diferente en Direct3D 8. x.</span><span class="sxs-lookup"><span data-stu-id="58e65-129">This behavior is different in Direct3D 8.x.</span></span>


```
Given:
    Create shader1 which references c4 and defines it with the def instruction

Scenario 1 (repeated with Direct3D 8):
    Call Set***Shader with shader1
    Call Set***ShaderConstant to set c4
    Call Draw
    Result: The shader will see the value in c4 from Set***ShaderConstant
```



<span data-ttu-id="58e65-130">En Direct3D 8. x Set \* \* \* ShaderConstant surte efecto inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="58e65-130">In Direct3D 8.x Set\*\*\*ShaderConstant takes effect immediately.</span></span> <span data-ttu-id="58e65-131">Considere el escenario siguiente:</span><span class="sxs-lookup"><span data-stu-id="58e65-131">Consider this scenario:</span></span>


```
Given:
    Create shader1 which references c4 and defines it with the def instruction
    
Scenario 3:
    Call Set***Shader with shader1
    Call Draw
    Result: The shader will see the def'd value in c4

Given:
    Scenario 3 has just completed
    Create shader2 (which references c4 but does not use the def instruction 
      to define it)     
    
Scenario 4 :    
    Call Set***Shader with shader2
    Call Draw
    Result: The shader will see the def'd value in c4 (set by def in shader 1)
```



<span data-ttu-id="58e65-132">El resultado no deseado es que el orden en el que se establecen los sombreadores podría afectar al comportamiento observado de los sombreadores individuales.</span><span class="sxs-lookup"><span data-stu-id="58e65-132">The undesirable result is that the order in which the shaders are set could affect the observed behavior of individual shaders.</span></span>

## <a name="shader-driver-model-requirements"></a><span data-ttu-id="58e65-133">Requisitos del modelo del controlador del sombreador</span><span class="sxs-lookup"><span data-stu-id="58e65-133">Shader Driver Model Requirements</span></span>

<span data-ttu-id="58e65-134">Las interfaces de Direct3D 9 están restringidas a los controladores de la interfaz de controlador de dispositivo (DDI) que son DirectX 7 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="58e65-134">Direct3D 9 interfaces are restricted to device driver interface (DDI) drivers that are DirectX 7-level and above.</span></span> <span data-ttu-id="58e65-135">Para comprobar el nivel de DDI, ejecute la [herramienta de diagnóstico de DirectX](https://msdn.microsoft.com/library/Ee416792(v=VS.85).aspx) y examine el archivo de texto guardado.</span><span class="sxs-lookup"><span data-stu-id="58e65-135">To check the DDI level, run the [DirectX Diagnostic Tool](https://msdn.microsoft.com/library/Ee416792(v=VS.85).aspx) and examine the saved text file.</span></span>

<span data-ttu-id="58e65-136">Como referencia, las interfaces de Direct3D 8 solo funcionan en los controladores DDI que son DirectX de nivel 6 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="58e65-136">For reference, Direct3D 8 interfaces work only on DDI drivers that are DirectX 6-level and above.</span></span>

## <a name="shader-binary-format"></a><span data-ttu-id="58e65-137">Formato binario del sombreador</span><span class="sxs-lookup"><span data-stu-id="58e65-137">Shader Binary Format</span></span>

<span data-ttu-id="58e65-138">El diseño bit a bit de la secuencia de instrucciones del sombreador se define en D3d9types. h.</span><span class="sxs-lookup"><span data-stu-id="58e65-138">The bitwise layout of the shader instruction stream is defined in D3d9types.h.</span></span> <span data-ttu-id="58e65-139">Si quiere diseñar sus propias herramientas de construcción o compilador de sombreador y desea obtener más información sobre el flujo de tokens del sombreador, consulte el kit de desarrollo de controladores (DDK) de Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="58e65-139">If you want to design your own shader compiler or construction tools and you want more information about the shader token stream, refer to the Direct3D 9 Driver Development Kit (DDK).</span></span>

## <a name="c-like-shader-language"></a><span data-ttu-id="58e65-140">Lenguaje de sombreador de tipo C</span><span class="sxs-lookup"><span data-stu-id="58e65-140">C-like Shader Language</span></span>

<span data-ttu-id="58e65-141">Consulte [referencia de HLSL](dx-graphics-hlsl-reference.md) para experimentar un lenguaje de sombreador similar a C.</span><span class="sxs-lookup"><span data-stu-id="58e65-141">See [HLSL Reference](dx-graphics-hlsl-reference.md) to experience a C-like shader language.</span></span>

## <a name="related-topics"></a><span data-ttu-id="58e65-142">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="58e65-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="58e65-143">Referencia de HLSL</span><span class="sxs-lookup"><span data-stu-id="58e65-143">Reference for HLSL</span></span>](dx-graphics-hlsl-reference.md)
</dt> </dl>

 

 




