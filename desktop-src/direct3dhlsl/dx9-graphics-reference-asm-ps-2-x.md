---
title: ps_2_x
description: Un sombreador de píxeles programable se compone de un conjunto de instrucciones que operan en datos de píxeles. Registra datos de transferencia dentro y fuera de la ALU. Se puede aplicar un control adicional para modificar la instrucción, los resultados o los datos que se escriben.
ms.assetid: 06f657a9-6521-404e-b012-7c8e972e9d5c
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 13e5daf7c3a4b41e5b27b1c20f8b1f5f8355c325
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104997120"
---
# <a name="ps_2_x"></a><span data-ttu-id="c2f09-105">PS \_ 2 \_ x</span><span class="sxs-lookup"><span data-stu-id="c2f09-105">ps\_2\_x</span></span>

<span data-ttu-id="c2f09-106">Un sombreador de píxeles programable se compone de un conjunto de instrucciones que operan en datos de píxeles.</span><span class="sxs-lookup"><span data-stu-id="c2f09-106">A programmable pixel shader is made up of a set of instructions that operate on pixel data.</span></span> <span data-ttu-id="c2f09-107">Registra datos de transferencia dentro y fuera de la ALU.</span><span class="sxs-lookup"><span data-stu-id="c2f09-107">Registers transfer data in and out of the ALU.</span></span> <span data-ttu-id="c2f09-108">Se puede aplicar un control adicional para modificar la instrucción, los resultados o los datos que se escriben.</span><span class="sxs-lookup"><span data-stu-id="c2f09-108">Additional control can be applied to modify the instruction, the results, or what data gets written out.</span></span>

-   <span data-ttu-id="c2f09-109">[las \_ instrucciones de PS 2 \_ x](dx9-graphics-reference-asm-ps-instructions-ps-2-x.md) contienen una lista de las instrucciones disponibles.</span><span class="sxs-lookup"><span data-stu-id="c2f09-109">[ps\_2\_x Instructions](dx9-graphics-reference-asm-ps-instructions-ps-2-x.md) contains a list of the available instructions.</span></span>
-   <span data-ttu-id="c2f09-110">[en \_ registros de PS 2 \_ x](dx9-graphics-reference-asm-ps-registers-ps-2-x.md) se enumeran los distintos tipos de registros utilizados por el sombreador de vértices Alu.</span><span class="sxs-lookup"><span data-stu-id="c2f09-110">[ps\_2\_x Registers](dx9-graphics-reference-asm-ps-registers-ps-2-x.md) lists the different types of registers used by the vertex shader ALU.</span></span>
-   <span data-ttu-id="c2f09-111">[Modificadores](dx9-graphics-reference-asm-ps-registers-modifiers.md) Se utilizan para modificar la forma en que funciona una instrucción.</span><span class="sxs-lookup"><span data-stu-id="c2f09-111">[Modifiers](dx9-graphics-reference-asm-ps-registers-modifiers.md) Are used to modify the way an instruction works.</span></span>
-   <span data-ttu-id="c2f09-112">La [máscara de escritura del registro de destino](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md) determina los componentes del registro de destino que se van a escribir.</span><span class="sxs-lookup"><span data-stu-id="c2f09-112">[Destination Register Write Mask](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md) determines what components of the destination register get written.</span></span>
-   <span data-ttu-id="c2f09-113">Los [modificadores de registro de origen del sombreador de píxeles](dx9-graphics-reference-asm-ps-registers-modifiers-source.md) modifican los datos del registro de origen antes de que se ejecute la instrucción.</span><span class="sxs-lookup"><span data-stu-id="c2f09-113">[Pixel Shader Source Register Modifiers](dx9-graphics-reference-asm-ps-registers-modifiers-source.md) alter the source register data before the instruction runs.</span></span>
-   <span data-ttu-id="c2f09-114">[El registro de origen permutación](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md) proporciona control adicional sobre qué componentes de registro se leen, se copian o se escriben.</span><span class="sxs-lookup"><span data-stu-id="c2f09-114">[Source Register Swizzling](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md) gives additional control over which register components are read, copied, or written.</span></span>

## <a name="dynamic-flow-control"></a><span data-ttu-id="c2f09-115">Control de flujo dinámico</span><span class="sxs-lookup"><span data-stu-id="c2f09-115">Dynamic Flow Control</span></span>

<span data-ttu-id="c2f09-116">[**DynamicFlowControlDepth**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) representa la profundidad de anidamiento de las instrucciones de control de flujo dinámico: [si](if-bool---ps.md)es, si se ha [ \_ Compens](if-comp---ps.md), [si es \_ Pred](if-pred---ps.md), [break-PS](break---ps.md)y [break \_ COMP-PS](break-comp---ps.md).</span><span class="sxs-lookup"><span data-stu-id="c2f09-116">[**DynamicFlowControlDepth**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) represents the nesting depth of dynamic flow control instructions: [if](if-bool---ps.md), [if\_comp](if-comp---ps.md), [if\_pred](if-pred---ps.md), [break - ps](break---ps.md), and [break\_comp - ps](break-comp---ps.md).</span></span> <span data-ttu-id="c2f09-117">El valor es igual a la profundidad de anidamiento del bloque if \_ comp.</span><span class="sxs-lookup"><span data-stu-id="c2f09-117">The value is equal to the nesting depth of the if\_comp block.</span></span> <span data-ttu-id="c2f09-118">Si este extremo es cero, el dispositivo no admite las instrucciones de control de flujo dinámico.</span><span class="sxs-lookup"><span data-stu-id="c2f09-118">If this cap is zero, the device does not support dynamic flow control instructions.</span></span>

## <a name="number-of-temporary-registers"></a><span data-ttu-id="c2f09-119">Número de registros temporales</span><span class="sxs-lookup"><span data-stu-id="c2f09-119">Number of Temporary Registers</span></span>

<span data-ttu-id="c2f09-120">El número de registros temporales admitidos por el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c2f09-120">The number of temporary registers supported by the device.</span></span> <span data-ttu-id="c2f09-121">El intervalo está comprendido entre 12 y 32.</span><span class="sxs-lookup"><span data-stu-id="c2f09-121">The range is from 12 to 32.</span></span>

## <a name="static-flow-control-nesting-depth"></a><span data-ttu-id="c2f09-122">Profundidad de anidamiento de control de flujo estático</span><span class="sxs-lookup"><span data-stu-id="c2f09-122">Static Flow Control Nesting Depth</span></span>

<span data-ttu-id="c2f09-123">[**StaticFlowControlDepth**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) representa la profundidad de anidamiento de dos tipos de instrucciones de control de flujo estático: [Loop](loop---ps.md)  / [REP](rep---ps.md) y [Call](call---ps.md)  / [callnz](callnz-bool---ps.md).</span><span class="sxs-lookup"><span data-stu-id="c2f09-123">[**StaticFlowControlDepth**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) represents the nesting depth of two types of static flow control instructions: [loop](loop---ps.md) /[rep](rep---ps.md) And [call](call---ps.md) /[callnz](callnz-bool---ps.md).</span></span> <span data-ttu-id="c2f09-124">las instrucciones de bucle/REP se pueden anidar hasta **StaticFlowControlDepth** Deep.</span><span class="sxs-lookup"><span data-stu-id="c2f09-124">loop /rep instructions can be nested up to **StaticFlowControlDepth** deep.</span></span> <span data-ttu-id="c2f09-125">De forma independiente, las instrucciones Call/callnz se pueden anidar hasta **StaticFlowControlDepth** Deep.</span><span class="sxs-lookup"><span data-stu-id="c2f09-125">Independently, call /callnz instructions can be nested up to **StaticFlowControlDepth** deep.</span></span>

## <a name="number-of-instruction-slots"></a><span data-ttu-id="c2f09-126">Número de ranuras de instrucciones</span><span class="sxs-lookup"><span data-stu-id="c2f09-126">Number of Instruction Slots</span></span>

<span data-ttu-id="c2f09-127">El número de ranuras de instrucción puede oscilar entre 96 y un máximo de 512, y se especifica mediante [**MaxPixelShaderInstructionSlots**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0).</span><span class="sxs-lookup"><span data-stu-id="c2f09-127">The number of instruction slots can range from 96 to a maximum of 512, and is specified by the [**MaxPixelShaderInstructionSlots**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0).</span></span> <span data-ttu-id="c2f09-128">El número total de instrucciones que se pueden ejecutar está definido por **MaxPixelShaderInstructionsExecuted**.</span><span class="sxs-lookup"><span data-stu-id="c2f09-128">The total number of instructions that can run is defined by **MaxPixelShaderInstructionsExecuted**.</span></span> <span data-ttu-id="c2f09-129">Puede ser mayor que el número de ranuras de instrucciones debido a llamadas de bucle y subrutinas.</span><span class="sxs-lookup"><span data-stu-id="c2f09-129">This can be larger than the number of instruction slots due to looping and subroutine calls.</span></span>

## <a name="arbitrary-swizzle"></a><span data-ttu-id="c2f09-130">Swizzle arbitrario</span><span class="sxs-lookup"><span data-stu-id="c2f09-130">Arbitrary Swizzle</span></span>

<span data-ttu-id="c2f09-131">Si se establece [**D3DD3DPSHADERCAPS2 \_ 0 \_ ARBITRARYSWIZZLE**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) , se admite swizzle arbitrario.</span><span class="sxs-lookup"><span data-stu-id="c2f09-131">If [**D3DD3DPSHADERCAPS2\_0\_ARBITRARYSWIZZLE**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) is set, arbitrary swizzle is supported.</span></span> <span data-ttu-id="c2f09-132">Consulte [source Register permutación](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md).</span><span class="sxs-lookup"><span data-stu-id="c2f09-132">See [Source Register Swizzling](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md).</span></span>

## <a name="gradient-instructions"></a><span data-ttu-id="c2f09-133">Instrucciones de degradado</span><span class="sxs-lookup"><span data-stu-id="c2f09-133">Gradient Instructions</span></span>

<span data-ttu-id="c2f09-134">Si se establece [**D3DD3DPSHADERCAPS2 \_ 0 \_ GRADIENTINSTRUCTIONS**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) , se admiten las instrucciones de degradado.</span><span class="sxs-lookup"><span data-stu-id="c2f09-134">If [**D3DD3DPSHADERCAPS2\_0\_GRADIENTINSTRUCTIONS**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) is set, gradient instructions are supported.</span></span> <span data-ttu-id="c2f09-135">Consulte [DSX-PS](dsx---ps.md), [DSY-PS](dsy---ps.md)y [texldd-PS](texldd---ps.md).</span><span class="sxs-lookup"><span data-stu-id="c2f09-135">See [dsx - ps](dsx---ps.md), [dsy - ps](dsy---ps.md), and [texldd - ps](texldd---ps.md).</span></span>

## <a name="predication"></a><span data-ttu-id="c2f09-136">Predicación</span><span class="sxs-lookup"><span data-stu-id="c2f09-136">Predication</span></span>

<span data-ttu-id="c2f09-137">Si se establece [**D3DD3DPSHADERCAPS2 \_ 0 \_ PREDICATION**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) , se admite la instrucción PREDICATION.</span><span class="sxs-lookup"><span data-stu-id="c2f09-137">If [**D3DD3DPSHADERCAPS2\_0\_PREDICATION**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) is set, instruction predication is supported.</span></span> <span data-ttu-id="c2f09-138">Vea [registro de predicados](dx9-graphics-reference-asm-ps-registers-predicate.md).</span><span class="sxs-lookup"><span data-stu-id="c2f09-138">See [Predicate Register](dx9-graphics-reference-asm-ps-registers-predicate.md).</span></span>

## <a name="dependent-read-limit"></a><span data-ttu-id="c2f09-139">Límite de lectura dependiente</span><span class="sxs-lookup"><span data-stu-id="c2f09-139">Dependent Read Limit</span></span>

<span data-ttu-id="c2f09-140">Si se establece [**D3DD3DPSHADERCAPS2 \_ 0 \_ NODEPENDENTREADLIMIT**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) , no hay ningún límite de lectura dependiente.</span><span class="sxs-lookup"><span data-stu-id="c2f09-140">If [**D3DD3DPSHADERCAPS2\_0\_NODEPENDENTREADLIMIT**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) is set, there are no dependent read limits.</span></span>

## <a name="texture-instruction-limit"></a><span data-ttu-id="c2f09-141">Límite de instrucciones de textura</span><span class="sxs-lookup"><span data-stu-id="c2f09-141">Texture Instruction Limit</span></span>

<span data-ttu-id="c2f09-142">Si se establece [**D3DD3DPSHADERCAPS2 \_ 0 \_ NOTEXINSTRUCTIONLIMIT**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) , no hay ningún límite en las instrucciones de textura.</span><span class="sxs-lookup"><span data-stu-id="c2f09-142">If [**D3DD3DPSHADERCAPS2\_0\_NOTEXINSTRUCTIONLIMIT**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) is set, there is no limit on texture instructions.</span></span>

## <a name="sampler-count"></a><span data-ttu-id="c2f09-143">Recuento de muestras</span><span class="sxs-lookup"><span data-stu-id="c2f09-143">Sampler Count</span></span>

<span data-ttu-id="c2f09-144">El número de muestras de textura disponibles es 16.</span><span class="sxs-lookup"><span data-stu-id="c2f09-144">The number of texture samplers available is 16.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c2f09-145">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c2f09-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c2f09-146">Sombreadores de píxeles</span><span class="sxs-lookup"><span data-stu-id="c2f09-146">Pixel Shaders</span></span>](dx9-graphics-reference-asm-ps.md)
</dt> </dl>

 

 