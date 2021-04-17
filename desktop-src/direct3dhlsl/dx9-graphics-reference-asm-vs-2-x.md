---
title: vs_2_x
description: Un sombreador de vértices programable se compone de un conjunto de instrucciones que operan en los datos de vértices. Registra datos de transferencia dentro y fuera de la ALU. Se puede aplicar un control adicional para modificar la instrucción, los resultados o los datos que se escriben.
ms.assetid: 64b07597-1e16-4803-b991-e78eabc2c060
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d09af016ca4fd399de0f2aeec1267343b9d11574
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104488039"
---
# <a name="vs_2_x"></a><span data-ttu-id="abafe-105">vs \_ 2 \_ x</span><span class="sxs-lookup"><span data-stu-id="abafe-105">vs\_2\_x</span></span>

<span data-ttu-id="abafe-106">Un sombreador de vértices programable se compone de un conjunto de instrucciones que operan en los datos de vértices.</span><span class="sxs-lookup"><span data-stu-id="abafe-106">A programmable vertex shader is made up of a set of instructions that operate on vertex data.</span></span> <span data-ttu-id="abafe-107">Registra datos de transferencia dentro y fuera de la ALU.</span><span class="sxs-lookup"><span data-stu-id="abafe-107">Registers transfer data in and out of the ALU.</span></span> <span data-ttu-id="abafe-108">Se puede aplicar un control adicional para modificar la instrucción, los resultados o los datos que se escriben.</span><span class="sxs-lookup"><span data-stu-id="abafe-108">Additional control can be applied to modify the instruction, the results, or what data gets written out.</span></span>

<span data-ttu-id="abafe-109">La versión del sombreador de vértices frente \_ \_ a 2 x amplía el conjunto de características compatible con vs \_ 2 \_ 0.</span><span class="sxs-lookup"><span data-stu-id="abafe-109">Vertex shader version vs\_2\_x extends the feature set supported by vs\_2\_0.</span></span> <span data-ttu-id="abafe-110">Cada característica adicional está representada por un límite correspondiente en la estructura [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9) dentro de [D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps).</span><span class="sxs-lookup"><span data-stu-id="abafe-110">Each additional feature is represented by a corresponding cap in the [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9) structure within [D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps).</span></span> <span data-ttu-id="abafe-111">Para usar cualquiera de las características mejoradas representadas por estos Cap, la versión del sombreador de vértices debe especificarse como vs \_ 2 \_ x.</span><span class="sxs-lookup"><span data-stu-id="abafe-111">To use any of the enhanced features represented by these caps, the vertex shader version must be specified as vs\_2\_x.</span></span>

-   <span data-ttu-id="abafe-112">[Instrucciones: vs \_ 2 \_ x](dx9-graphics-reference-asm-vs-instructions-vs-2-x.md) contiene una lista de las instrucciones disponibles.</span><span class="sxs-lookup"><span data-stu-id="abafe-112">[Instructions - vs\_2\_x](dx9-graphics-reference-asm-vs-instructions-vs-2-x.md) contains a list of the available instructions.</span></span>
-   <span data-ttu-id="abafe-113">[Registros: vs \_ 2 \_ x](dx9-graphics-reference-asm-vs-registers-vs-2-x.md) enumera los distintos tipos de registros utilizados por el sombreador de vértices Alu.</span><span class="sxs-lookup"><span data-stu-id="abafe-113">[Registers - vs\_2\_x](dx9-graphics-reference-asm-vs-registers-vs-2-x.md) lists the different types of registers used by the vertex shader ALU.</span></span>
-   <span data-ttu-id="abafe-114">Los [modificadores de registro del sombreador de vértices](dx9-graphics-reference-asm-vs-registers-modifiers.md) se utilizan para modificar la forma en que funciona una instrucción.</span><span class="sxs-lookup"><span data-stu-id="abafe-114">[Vertex Shader Register Modifiers](dx9-graphics-reference-asm-vs-registers-modifiers.md) are used to modify the way an instruction works.</span></span>
-   <span data-ttu-id="abafe-115">Los [modificadores de registro de origen del sombreador de vértices](dx9-graphics-reference-asm-vs-registers-modifiers-source.md) modifican los datos del registro de origen antes de que se ejecute la instrucción.</span><span class="sxs-lookup"><span data-stu-id="abafe-115">[Vertex Shader Source Register Modifiers](dx9-graphics-reference-asm-vs-registers-modifiers-source.md) alter the source register data before the instruction runs.</span></span>
-   <span data-ttu-id="abafe-116">[El registro de origen permutación](dx9-graphics-reference-asm-vs-registers-modifiers-source-swizzling.md) proporciona control adicional sobre qué componentes de registro se leen, se copian o se escriben.</span><span class="sxs-lookup"><span data-stu-id="abafe-116">[Source Register Swizzling](dx9-graphics-reference-asm-vs-registers-modifiers-source-swizzling.md) gives additional control over which register components are read, copied, or written.</span></span>
-   <span data-ttu-id="abafe-117">[El enmascaramiento del registro de destino](dx9-graphics-reference-asm-vs-registers-modifiers-masking.md) determina los componentes del registro de destino que se van a escribir.</span><span class="sxs-lookup"><span data-stu-id="abafe-117">[Destination Register Masking](dx9-graphics-reference-asm-vs-registers-modifiers-masking.md) determines what components of the destination register get written.</span></span>

## <a name="new-features"></a><span data-ttu-id="abafe-118">Nuevas características</span><span class="sxs-lookup"><span data-stu-id="abafe-118">New Features</span></span>

<span data-ttu-id="abafe-119">Las nuevas características son las siguientes:</span><span class="sxs-lookup"><span data-stu-id="abafe-119">New features are as follows:</span></span>

### <a name="dynamic-flow-control"></a><span data-ttu-id="abafe-120">Control de flujo dinámico</span><span class="sxs-lookup"><span data-stu-id="abafe-120">Dynamic Flow Control</span></span>

<span data-ttu-id="abafe-121">Si [D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) > 0, se admiten las siguientes instrucciones de control de flujo dinámico:</span><span class="sxs-lookup"><span data-stu-id="abafe-121">If [D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) > 0, then the following dynamic flow control instructions are supported:</span></span>

-   [<span data-ttu-id="abafe-122">If \_ COMP-vs</span><span class="sxs-lookup"><span data-stu-id="abafe-122">if\_comp - vs</span></span>](if-comp---vs.md)
-   [<span data-ttu-id="abafe-123">Inter-vs</span><span class="sxs-lookup"><span data-stu-id="abafe-123">break - vs</span></span>](break---vs.md)
-   [<span data-ttu-id="abafe-124">Break \_ COMP-vs</span><span class="sxs-lookup"><span data-stu-id="abafe-124">break\_comp - vs</span></span>](break-comp---vs.md)

<span data-ttu-id="abafe-125">Si también se establece [D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) , se admiten las siguientes instrucciones de control de flujo adicionales:</span><span class="sxs-lookup"><span data-stu-id="abafe-125">If [D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) is also set, the following additional flow control instructions are supported:</span></span>

-   [<span data-ttu-id="abafe-126">\_COMP SETP-vs</span><span class="sxs-lookup"><span data-stu-id="abafe-126">setp\_comp - vs</span></span>](setp-comp---vs.md)
-   [<span data-ttu-id="abafe-127">Si Pred-vs</span><span class="sxs-lookup"><span data-stu-id="abafe-127">if pred - vs</span></span>](if-pred---vs.md)
-   [<span data-ttu-id="abafe-128">callnz Pred-vs</span><span class="sxs-lookup"><span data-stu-id="abafe-128">callnz pred - vs</span></span>](callnz-pred---vs.md)
-   [<span data-ttu-id="abafe-129">breakp-vs</span><span class="sxs-lookup"><span data-stu-id="abafe-129">breakp - vs</span></span>](breakp---vs.md)

<span data-ttu-id="abafe-130">El intervalo de valores para la profundidad de control de flujo dinámico es de 0 a 24 y es igual a la profundidad de anidamiento de las instrucciones de control de flujo dinámico (vea [límites de anidamiento de control de flujo](dx9-graphics-reference-asm-vs-instructions-flow-control.md) para obtener más detalles).</span><span class="sxs-lookup"><span data-stu-id="abafe-130">The range of values for dynamic flow control depth is 0 to 24 and is equal to the nesting depth of the dynamic flow control instructions (see [Flow Control Nesting Limits](dx9-graphics-reference-asm-vs-instructions-flow-control.md) for details).</span></span> <span data-ttu-id="abafe-131">Si este extremo es cero, el dispositivo no admite las instrucciones de control de flujo dinámico.</span><span class="sxs-lookup"><span data-stu-id="abafe-131">If this cap is zero, the device does not support dynamic flow control instructions.</span></span>

### <a name="number-of-temporary-registers"></a><span data-ttu-id="abafe-132">Número de registros temporales</span><span class="sxs-lookup"><span data-stu-id="abafe-132">Number of Temporary Registers</span></span>

<span data-ttu-id="abafe-133">[D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) representa el número de [registros temporales](dx9-graphics-reference-asm-vs-registers-temporary.md)admitidos por el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="abafe-133">[D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) represents the number of [Temporary Register](dx9-graphics-reference-asm-vs-registers-temporary.md)s supported by the device.</span></span> <span data-ttu-id="abafe-134">El intervalo de valores para este Cap es de 12 a 32.</span><span class="sxs-lookup"><span data-stu-id="abafe-134">The range of values for this cap is 12 to 32.</span></span>

### <a name="static-flow-control-nesting-depth"></a><span data-ttu-id="abafe-135">Profundidad de anidamiento de control de flujo estático</span><span class="sxs-lookup"><span data-stu-id="abafe-135">Static Flow Control Nesting Depth</span></span>

<span data-ttu-id="abafe-136">[D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) representa la profundidad de anidamiento de dos tipos de instrucciones de control de flujo estático: [Loop-vs](loop---vs.md) / [REP-vs](rep---vs.md) y [Call-vs](call---vs.md) / [callnz bool-vs](callnz-bool---vs.md) / [Si bool-vs](if-bool---vs.md). Loop-vs/REP-vs las instrucciones se pueden anidar hasta D3DVS20CAPS Deep.</span><span class="sxs-lookup"><span data-stu-id="abafe-136">[D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) represents the nesting depth of two types of static flow control instructions: [loop - vs](loop---vs.md)/[rep - vs](rep---vs.md) and [call - vs](call---vs.md)/[callnz bool - vs](callnz-bool---vs.md)/[if bool - vs](if-bool---vs.md). loop - vs/rep - vs instructions can be nested up to D3DVS20CAPS deep.</span></span> <span data-ttu-id="abafe-137">De forma independiente, Call-vs/callnz bool-las instrucciones de vs se pueden anidar hasta D3DVS20CAPS Deep.</span><span class="sxs-lookup"><span data-stu-id="abafe-137">Independently, call - vs/callnz bool - vs instructions can be nested up to D3DVS20CAPS deep.</span></span> <span data-ttu-id="abafe-138">Si también se establece D3DVS20CAPS, [callnz Pred-vs](callnz-pred---vs.md) se cuenta para la profundidad de anidamiento de Call-vs/callnz bool-vs/if bool-vs (vea [límites de anidamiento del control de flujo](dx9-graphics-reference-asm-vs-instructions-flow-control.md) para obtener detalles).</span><span class="sxs-lookup"><span data-stu-id="abafe-138">If D3DVS20CAPS is also set, then [callnz pred - vs](callnz-pred---vs.md) is counted toward the nesting depth of call - vs/callnz bool - vs/if bool - vs (see [Flow Control Nesting Limits](dx9-graphics-reference-asm-vs-instructions-flow-control.md) for details).</span></span>

### <a name="predication"></a><span data-ttu-id="abafe-139">Predicación</span><span class="sxs-lookup"><span data-stu-id="abafe-139">Predication</span></span>

<span data-ttu-id="abafe-140">Si se establece [D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) , el dispositivo admite [SETP \_ COMP-vs](setp-comp---vs.md) e instruction predication.</span><span class="sxs-lookup"><span data-stu-id="abafe-140">If [D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) is set, the device supports [setp\_comp - vs](setp-comp---vs.md) and instruction predication.</span></span> <span data-ttu-id="abafe-141">Si D3DVS20CAPS también es mayor que 0, se admiten las siguientes instrucciones de control de flujo dinámico adicionales:</span><span class="sxs-lookup"><span data-stu-id="abafe-141">If D3DVS20CAPS is also greater than 0, then the following additional dynamic flow control instructions are supported:</span></span>

-   [<span data-ttu-id="abafe-142">Si Pred-vs</span><span class="sxs-lookup"><span data-stu-id="abafe-142">if pred - vs</span></span>](if-pred---vs.md)
-   [<span data-ttu-id="abafe-143">callnz Pred-vs</span><span class="sxs-lookup"><span data-stu-id="abafe-143">callnz pred - vs</span></span>](callnz-pred---vs.md)
-   [<span data-ttu-id="abafe-144">breakp-vs</span><span class="sxs-lookup"><span data-stu-id="abafe-144">breakp - vs</span></span>](breakp---vs.md)

### <a name="instruction-count"></a><span data-ttu-id="abafe-145">Recuento de instrucciones</span><span class="sxs-lookup"><span data-stu-id="abafe-145">Instruction Count</span></span>

<span data-ttu-id="abafe-146">Cada sombreador de vértices puede tener hasta 256 instrucciones almacenadas.</span><span class="sxs-lookup"><span data-stu-id="abafe-146">Each vertex shader can have up to 256 instructions stored.</span></span> <span data-ttu-id="abafe-147">El número de instrucciones que se ejecutan puede ser mucho mayor (debido al soporte de bucle o representación) y está limitado por [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9), que debe ser al menos 0xFFFF.</span><span class="sxs-lookup"><span data-stu-id="abafe-147">The number of instructions run can be much higher (because of the loop/rep support), and is capped by [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9), which should be at least 0xFFFF.</span></span>

## <a name="related-topics"></a><span data-ttu-id="abafe-148">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="abafe-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="abafe-149">Sombreadores de vértices</span><span class="sxs-lookup"><span data-stu-id="abafe-149">Vertex Shaders</span></span>](dx9-graphics-reference-asm-vs.md)
</dt> </dl>

 

 