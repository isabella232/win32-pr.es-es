---
title: ps_2_x
description: Obtenga información ps_2_x, un sombreador de píxeles programable, que se forma de un conjunto de instrucciones que funcionan con datos de píxeles.
ms.assetid: 06f657a9-6521-404e-b012-7c8e972e9d5c
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9efedc6011cb63b6465fd2d3ced4a7807c09f4da
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2021
ms.locfileid: "112010878"
---
# <a name="ps_2_x"></a><span data-ttu-id="a8374-103">ps \_ 2 \_ x</span><span class="sxs-lookup"><span data-stu-id="a8374-103">ps\_2\_x</span></span>

<span data-ttu-id="a8374-104">Un sombreador de píxeles programable se forma de un conjunto de instrucciones que funcionan con datos de píxeles.</span><span class="sxs-lookup"><span data-stu-id="a8374-104">A programmable pixel shader is made up of a set of instructions that operate on pixel data.</span></span> <span data-ttu-id="a8374-105">Registra la transferencia de datos dentro y fuera de la ALU.</span><span class="sxs-lookup"><span data-stu-id="a8374-105">Registers transfer data in and out of the ALU.</span></span> <span data-ttu-id="a8374-106">Se puede aplicar un control adicional para modificar la instrucción, los resultados o los datos que se escriben.</span><span class="sxs-lookup"><span data-stu-id="a8374-106">Additional control can be applied to modify the instruction, the results, or what data gets written out.</span></span>

-   <span data-ttu-id="a8374-107">[ps \_ 2 \_ x Instructions contiene](dx9-graphics-reference-asm-ps-instructions-ps-2-x.md) una lista de las instrucciones disponibles.</span><span class="sxs-lookup"><span data-stu-id="a8374-107">[ps\_2\_x Instructions](dx9-graphics-reference-asm-ps-instructions-ps-2-x.md) contains a list of the available instructions.</span></span>
-   <span data-ttu-id="a8374-108">[ps \_ 2 \_ x Registers muestra](dx9-graphics-reference-asm-ps-registers-ps-2-x.md) los distintos tipos de registros que usa el sombreador de vértices ALU.</span><span class="sxs-lookup"><span data-stu-id="a8374-108">[ps\_2\_x Registers](dx9-graphics-reference-asm-ps-registers-ps-2-x.md) lists the different types of registers used by the vertex shader ALU.</span></span>
-   <span data-ttu-id="a8374-109">[Modificadores](dx9-graphics-reference-asm-ps-registers-modifiers.md) Se usan para modificar el funcionamiento de una instrucción.</span><span class="sxs-lookup"><span data-stu-id="a8374-109">[Modifiers](dx9-graphics-reference-asm-ps-registers-modifiers.md) Are used to modify the way an instruction works.</span></span>
-   <span data-ttu-id="a8374-110">[La máscara de escritura del registro de destino](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md) determina qué componentes del registro de destino se escriben.</span><span class="sxs-lookup"><span data-stu-id="a8374-110">[Destination Register Write Mask](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md) determines what components of the destination register get written.</span></span>
-   <span data-ttu-id="a8374-111">[Los modificadores de registro de origen del sombreador de](dx9-graphics-reference-asm-ps-registers-modifiers-source.md) píxeles modifican los datos de registro de origen antes de que se ejecute la instrucción.</span><span class="sxs-lookup"><span data-stu-id="a8374-111">[Pixel Shader Source Register Modifiers](dx9-graphics-reference-asm-ps-registers-modifiers-source.md) alter the source register data before the instruction runs.</span></span>
-   <span data-ttu-id="a8374-112">[Source Register Swling proporciona](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md) control adicional sobre qué componentes de registro se leen, copian o escriben.</span><span class="sxs-lookup"><span data-stu-id="a8374-112">[Source Register Swizzling](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md) gives additional control over which register components are read, copied, or written.</span></span>

## <a name="dynamic-flow-control"></a><span data-ttu-id="a8374-113">Control dinámico de flujo</span><span class="sxs-lookup"><span data-stu-id="a8374-113">Dynamic Flow Control</span></span>

<span data-ttu-id="a8374-114">[**DynamicFlowControlDepth**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) representa la profundidad de anidamiento de instrucciones de control de flujo [dinámico:](if-bool---ps.md)si , si [ \_ comp](if-comp---ps.md), si [ \_ pred](if-pred---ps.md), [break - ps](break---ps.md)y break comp - [ \_ ps](break-comp---ps.md).</span><span class="sxs-lookup"><span data-stu-id="a8374-114">[**DynamicFlowControlDepth**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) represents the nesting depth of dynamic flow control instructions: [if](if-bool---ps.md), [if\_comp](if-comp---ps.md), [if\_pred](if-pred---ps.md), [break - ps](break---ps.md), and [break\_comp - ps](break-comp---ps.md).</span></span> <span data-ttu-id="a8374-115">El valor es igual a la profundidad de anidamiento del bloque if \_ comp.</span><span class="sxs-lookup"><span data-stu-id="a8374-115">The value is equal to the nesting depth of the if\_comp block.</span></span> <span data-ttu-id="a8374-116">Si este límite es cero, el dispositivo no admite instrucciones de control de flujo dinámico.</span><span class="sxs-lookup"><span data-stu-id="a8374-116">If this cap is zero, the device does not support dynamic flow control instructions.</span></span>

## <a name="number-of-temporary-registers"></a><span data-ttu-id="a8374-117">Número de registros temporales</span><span class="sxs-lookup"><span data-stu-id="a8374-117">Number of Temporary Registers</span></span>

<span data-ttu-id="a8374-118">Número de registros temporales admitidos por el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a8374-118">The number of temporary registers supported by the device.</span></span> <span data-ttu-id="a8374-119">El intervalo es de 12 a 32.</span><span class="sxs-lookup"><span data-stu-id="a8374-119">The range is from 12 to 32.</span></span>

## <a name="static-flow-control-nesting-depth"></a><span data-ttu-id="a8374-120">Profundidad de anidamiento del control de flujo estático</span><span class="sxs-lookup"><span data-stu-id="a8374-120">Static Flow Control Nesting Depth</span></span>

<span data-ttu-id="a8374-121">[**StaticFlowControlDepth representa**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) la profundidad de anidamiento de dos tipos de instrucciones de control de flujo estático: [loop](loop---ps.md)  / [rep](rep---ps.md) y [call](call---ps.md)  / [callnz](callnz-bool---ps.md).</span><span class="sxs-lookup"><span data-stu-id="a8374-121">[**StaticFlowControlDepth**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) represents the nesting depth of two types of static flow control instructions: [loop](loop---ps.md) /[rep](rep---ps.md) And [call](call---ps.md) /[callnz](callnz-bool---ps.md).</span></span> <span data-ttu-id="a8374-122">Las instrucciones de loop /rep se pueden anidar hasta **StaticFlowControlDepth** deep.</span><span class="sxs-lookup"><span data-stu-id="a8374-122">loop /rep instructions can be nested up to **StaticFlowControlDepth** deep.</span></span> <span data-ttu-id="a8374-123">De forma independiente, las instrucciones /callnz se pueden anidar hasta **staticflowControlDepth** en profundidad.</span><span class="sxs-lookup"><span data-stu-id="a8374-123">Independently, call /callnz instructions can be nested up to **StaticFlowControlDepth** deep.</span></span>

## <a name="number-of-instruction-slots"></a><span data-ttu-id="a8374-124">Número de ranuras de instrucción</span><span class="sxs-lookup"><span data-stu-id="a8374-124">Number of Instruction Slots</span></span>

<span data-ttu-id="a8374-125">El número de ranuras de instrucción puede oscilar entre 96 y un máximo de 512, y se especifica mediante [**MaxPixelShaderInstructionSlots**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0).</span><span class="sxs-lookup"><span data-stu-id="a8374-125">The number of instruction slots can range from 96 to a maximum of 512, and is specified by the [**MaxPixelShaderInstructionSlots**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0).</span></span> <span data-ttu-id="a8374-126">**MaxPixelShaderInstructionsExecuted** define el número total de instrucciones que se pueden ejecutar.</span><span class="sxs-lookup"><span data-stu-id="a8374-126">The total number of instructions that can run is defined by **MaxPixelShaderInstructionsExecuted**.</span></span> <span data-ttu-id="a8374-127">Esto puede ser mayor que el número de ranuras de instrucción debido a bucles y llamadas de subrutina.</span><span class="sxs-lookup"><span data-stu-id="a8374-127">This can be larger than the number of instruction slots due to looping and subroutine calls.</span></span>

## <a name="arbitrary-swizzle"></a><span data-ttu-id="a8374-128">Swzzle arbitrario</span><span class="sxs-lookup"><span data-stu-id="a8374-128">Arbitrary Swizzle</span></span>

<span data-ttu-id="a8374-129">Si [**se establece D3DD3DPSHADERCAPS2 \_ 0 \_ ARBITRARYSWAPILE,**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) se admite el swzzle arbitrario.</span><span class="sxs-lookup"><span data-stu-id="a8374-129">If [**D3DD3DPSHADERCAPS2\_0\_ARBITRARYSWIZZLE**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) is set, arbitrary swizzle is supported.</span></span> <span data-ttu-id="a8374-130">Consulte [Source Register Swlingling](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md).</span><span class="sxs-lookup"><span data-stu-id="a8374-130">See [Source Register Swizzling](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md).</span></span>

## <a name="gradient-instructions"></a><span data-ttu-id="a8374-131">Instrucciones de degradado</span><span class="sxs-lookup"><span data-stu-id="a8374-131">Gradient Instructions</span></span>

<span data-ttu-id="a8374-132">Si [**se establece D3DD3DPSHADERCAPS2 \_ 0 \_ GRADIENTINSTRUCTIONS,**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) se admiten instrucciones de degradado.</span><span class="sxs-lookup"><span data-stu-id="a8374-132">If [**D3DD3DPSHADERCAPS2\_0\_GRADIENTINSTRUCTIONS**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) is set, gradient instructions are supported.</span></span> <span data-ttu-id="a8374-133">Vea [dsx - ps](dsx---ps.md), [dsy - ps](dsy---ps.md)y [texldd - ps](texldd---ps.md).</span><span class="sxs-lookup"><span data-stu-id="a8374-133">See [dsx - ps](dsx---ps.md), [dsy - ps](dsy---ps.md), and [texldd - ps](texldd---ps.md).</span></span>

## <a name="predication"></a><span data-ttu-id="a8374-134">Predicación</span><span class="sxs-lookup"><span data-stu-id="a8374-134">Predication</span></span>

<span data-ttu-id="a8374-135">Si [**se establece D3DD3DPSHADERCAPS2 \_ 0 \_ PREDICATION,**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) se admite el predicado de instrucciones.</span><span class="sxs-lookup"><span data-stu-id="a8374-135">If [**D3DD3DPSHADERCAPS2\_0\_PREDICATION**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) is set, instruction predication is supported.</span></span> <span data-ttu-id="a8374-136">Vea [Predicate Register](dx9-graphics-reference-asm-ps-registers-predicate.md).</span><span class="sxs-lookup"><span data-stu-id="a8374-136">See [Predicate Register](dx9-graphics-reference-asm-ps-registers-predicate.md).</span></span>

## <a name="dependent-read-limit"></a><span data-ttu-id="a8374-137">Límite de lectura dependiente</span><span class="sxs-lookup"><span data-stu-id="a8374-137">Dependent Read Limit</span></span>

<span data-ttu-id="a8374-138">Si [**se establece D3DD3DPSHADERCAPS2 \_ 0 \_ NODEPENDENTREADLIMIT,**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) no hay límites de lectura dependientes.</span><span class="sxs-lookup"><span data-stu-id="a8374-138">If [**D3DD3DPSHADERCAPS2\_0\_NODEPENDENTREADLIMIT**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) is set, there are no dependent read limits.</span></span>

## <a name="texture-instruction-limit"></a><span data-ttu-id="a8374-139">Límite de instrucciones de textura</span><span class="sxs-lookup"><span data-stu-id="a8374-139">Texture Instruction Limit</span></span>

<span data-ttu-id="a8374-140">Si [**D3DD3DPSHADERCAPS2 \_ 0 \_ NOTESTRUCTIONLIMIT**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) está establecido, no hay ningún límite en las instrucciones de textura.</span><span class="sxs-lookup"><span data-stu-id="a8374-140">If [**D3DD3DPSHADERCAPS2\_0\_NOTEXINSTRUCTIONLIMIT**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) is set, there is no limit on texture instructions.</span></span>

## <a name="sampler-count"></a><span data-ttu-id="a8374-141">Sampler Count</span><span class="sxs-lookup"><span data-stu-id="a8374-141">Sampler Count</span></span>

<span data-ttu-id="a8374-142">El número de muestreadores de textura disponibles es 16.</span><span class="sxs-lookup"><span data-stu-id="a8374-142">The number of texture samplers available is 16.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a8374-143">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a8374-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a8374-144">Sombreadores de píxeles</span><span class="sxs-lookup"><span data-stu-id="a8374-144">Pixel Shaders</span></span>](dx9-graphics-reference-asm-ps.md)
</dt> </dl>

 

 