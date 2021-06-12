---
title: vs_2_x
description: Obtenga información vs_2_x, un sombreador de vértices programable, que se conste de un conjunto de instrucciones que funcionan con datos de vértices.
ms.assetid: 64b07597-1e16-4803-b991-e78eabc2c060
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3449ae4c1e1eb3b977916f6fb1d19303e9d21a4e
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2021
ms.locfileid: "112010719"
---
# <a name="vs_2_x"></a><span data-ttu-id="c4f61-103">vs \_ 2 \_ x</span><span class="sxs-lookup"><span data-stu-id="c4f61-103">vs\_2\_x</span></span>

<span data-ttu-id="c4f61-104">Un sombreador de vértices programable se forma de un conjunto de instrucciones que funcionan con datos de vértices.</span><span class="sxs-lookup"><span data-stu-id="c4f61-104">A programmable vertex shader is made up of a set of instructions that operate on vertex data.</span></span> <span data-ttu-id="c4f61-105">Registra la transferencia de datos dentro y fuera de la ALU.</span><span class="sxs-lookup"><span data-stu-id="c4f61-105">Registers transfer data in and out of the ALU.</span></span> <span data-ttu-id="c4f61-106">Se puede aplicar un control adicional para modificar la instrucción, los resultados o los datos que se escriben.</span><span class="sxs-lookup"><span data-stu-id="c4f61-106">Additional control can be applied to modify the instruction, the results, or what data gets written out.</span></span>

<span data-ttu-id="c4f61-107">La versión del sombreador de \_ vértices frente a 2 \_ x amplía el conjunto de características admitido por frente a \_ 2 \_ 0.</span><span class="sxs-lookup"><span data-stu-id="c4f61-107">Vertex shader version vs\_2\_x extends the feature set supported by vs\_2\_0.</span></span> <span data-ttu-id="c4f61-108">Cada característica adicional se representa mediante un límite correspondiente en la estructura [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9) dentro de [D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps).</span><span class="sxs-lookup"><span data-stu-id="c4f61-108">Each additional feature is represented by a corresponding cap in the [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9) structure within [D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps).</span></span> <span data-ttu-id="c4f61-109">Para usar cualquiera de las características mejoradas representadas por estos límites, la versión del sombreador de vértices debe especificarse como \_ 2 \_ x.</span><span class="sxs-lookup"><span data-stu-id="c4f61-109">To use any of the enhanced features represented by these caps, the vertex shader version must be specified as vs\_2\_x.</span></span>

-   <span data-ttu-id="c4f61-110">[Instrucciones: frente \_ a 2 \_ x](dx9-graphics-reference-asm-vs-instructions-vs-2-x.md) contiene una lista de las instrucciones disponibles.</span><span class="sxs-lookup"><span data-stu-id="c4f61-110">[Instructions - vs\_2\_x](dx9-graphics-reference-asm-vs-instructions-vs-2-x.md) contains a list of the available instructions.</span></span>
-   <span data-ttu-id="c4f61-111">[Registros: frente \_ a 2 \_ x,](dx9-graphics-reference-asm-vs-registers-vs-2-x.md) se enumeran los distintos tipos de registros que usa el sombreador de vértices ALU.</span><span class="sxs-lookup"><span data-stu-id="c4f61-111">[Registers - vs\_2\_x](dx9-graphics-reference-asm-vs-registers-vs-2-x.md) lists the different types of registers used by the vertex shader ALU.</span></span>
-   <span data-ttu-id="c4f61-112">[Los modificadores de registro del sombreador](dx9-graphics-reference-asm-vs-registers-modifiers.md) de vértices se usan para modificar el funcionamiento de una instrucción.</span><span class="sxs-lookup"><span data-stu-id="c4f61-112">[Vertex Shader Register Modifiers](dx9-graphics-reference-asm-vs-registers-modifiers.md) are used to modify the way an instruction works.</span></span>
-   <span data-ttu-id="c4f61-113">[Los modificadores de registro de origen del sombreador de vértices](dx9-graphics-reference-asm-vs-registers-modifiers-source.md) modifican los datos de registro de origen antes de que se ejecute la instrucción.</span><span class="sxs-lookup"><span data-stu-id="c4f61-113">[Vertex Shader Source Register Modifiers](dx9-graphics-reference-asm-vs-registers-modifiers-source.md) alter the source register data before the instruction runs.</span></span>
-   <span data-ttu-id="c4f61-114">[El swling del registro de origen](dx9-graphics-reference-asm-vs-registers-modifiers-source-swizzling.md) proporciona control adicional sobre qué componentes de registro se leen, copian o escriben.</span><span class="sxs-lookup"><span data-stu-id="c4f61-114">[Source Register Swizzling](dx9-graphics-reference-asm-vs-registers-modifiers-source-swizzling.md) gives additional control over which register components are read, copied, or written.</span></span>
-   <span data-ttu-id="c4f61-115">[El enmascaramiento del registro de](dx9-graphics-reference-asm-vs-registers-modifiers-masking.md) destino determina qué componentes del registro de destino se escriben.</span><span class="sxs-lookup"><span data-stu-id="c4f61-115">[Destination Register Masking](dx9-graphics-reference-asm-vs-registers-modifiers-masking.md) determines what components of the destination register get written.</span></span>

## <a name="new-features"></a><span data-ttu-id="c4f61-116">Nuevas características</span><span class="sxs-lookup"><span data-stu-id="c4f61-116">New Features</span></span>

<span data-ttu-id="c4f61-117">Las nuevas características son las siguientes:</span><span class="sxs-lookup"><span data-stu-id="c4f61-117">New features are as follows:</span></span>

### <a name="dynamic-flow-control"></a><span data-ttu-id="c4f61-118">Control de flujo dinámico</span><span class="sxs-lookup"><span data-stu-id="c4f61-118">Dynamic Flow Control</span></span>

<span data-ttu-id="c4f61-119">Si [D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) > 0, se admiten las siguientes instrucciones de control de flujo dinámico:</span><span class="sxs-lookup"><span data-stu-id="c4f61-119">If [D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) > 0, then the following dynamic flow control instructions are supported:</span></span>

-   [<span data-ttu-id="c4f61-120">if \_ comp - vs</span><span class="sxs-lookup"><span data-stu-id="c4f61-120">if\_comp - vs</span></span>](if-comp---vs.md)
-   [<span data-ttu-id="c4f61-121">break- vs</span><span class="sxs-lookup"><span data-stu-id="c4f61-121">break - vs</span></span>](break---vs.md)
-   [<span data-ttu-id="c4f61-122">break \_ comp - vs</span><span class="sxs-lookup"><span data-stu-id="c4f61-122">break\_comp - vs</span></span>](break-comp---vs.md)

<span data-ttu-id="c4f61-123">Si [también se establece D3DVS20CAPS,](/windows/desktop/direct3d9/d3dvs20caps) se admiten las siguientes instrucciones de control de flujo adicionales:</span><span class="sxs-lookup"><span data-stu-id="c4f61-123">If [D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) is also set, the following additional flow control instructions are supported:</span></span>

-   [<span data-ttu-id="c4f61-124">setp \_ comp - vs</span><span class="sxs-lookup"><span data-stu-id="c4f61-124">setp\_comp - vs</span></span>](setp-comp---vs.md)
-   [<span data-ttu-id="c4f61-125">if pred - vs</span><span class="sxs-lookup"><span data-stu-id="c4f61-125">if pred - vs</span></span>](if-pred---vs.md)
-   [<span data-ttu-id="c4f61-126">callnz pred - vs</span><span class="sxs-lookup"><span data-stu-id="c4f61-126">callnz pred - vs</span></span>](callnz-pred---vs.md)
-   [<span data-ttu-id="c4f61-127">breakp: vs</span><span class="sxs-lookup"><span data-stu-id="c4f61-127">breakp - vs</span></span>](breakp---vs.md)

<span data-ttu-id="c4f61-128">El intervalo de valores para la profundidad del control de flujo dinámico es de 0 a [](dx9-graphics-reference-asm-vs-instructions-flow-control.md) 24 y es igual a la profundidad de anidamiento de las instrucciones de control de flujo dinámico (consulte Límites de anidamiento de controles de flujo para obtener más información).</span><span class="sxs-lookup"><span data-stu-id="c4f61-128">The range of values for dynamic flow control depth is 0 to 24 and is equal to the nesting depth of the dynamic flow control instructions (see [Flow Control Nesting Limits](dx9-graphics-reference-asm-vs-instructions-flow-control.md) for details).</span></span> <span data-ttu-id="c4f61-129">Si este límite es cero, el dispositivo no admite instrucciones de control de flujo dinámico.</span><span class="sxs-lookup"><span data-stu-id="c4f61-129">If this cap is zero, the device does not support dynamic flow control instructions.</span></span>

### <a name="number-of-temporary-registers"></a><span data-ttu-id="c4f61-130">Número de registros temporales</span><span class="sxs-lookup"><span data-stu-id="c4f61-130">Number of Temporary Registers</span></span>

<span data-ttu-id="c4f61-131">[D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) representa el número [de](dx9-graphics-reference-asm-vs-registers-temporary.md)registros temporales admitidos por el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c4f61-131">[D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) represents the number of [Temporary Register](dx9-graphics-reference-asm-vs-registers-temporary.md)s supported by the device.</span></span> <span data-ttu-id="c4f61-132">El intervalo de valores para este límite es de 12 a 32.</span><span class="sxs-lookup"><span data-stu-id="c4f61-132">The range of values for this cap is 12 to 32.</span></span>

### <a name="static-flow-control-nesting-depth"></a><span data-ttu-id="c4f61-133">Profundidad de anidamiento de controles de flujo estático</span><span class="sxs-lookup"><span data-stu-id="c4f61-133">Static Flow Control Nesting Depth</span></span>

<span data-ttu-id="c4f61-134">[D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) representa la profundidad de anidamiento de dos tipos de instrucciones de control de flujo estático: [loop - vs](loop---vs.md)rep - vs y call - vs callnz bool - vs if bool - vs . loop - vs/rep - vs instructions se pueden anidar hasta / [](rep---vs.md) [](call---vs.md) / [](callnz-bool---vs.md) / [](if-bool---vs.md)D3DVS20CAPS deep.</span><span class="sxs-lookup"><span data-stu-id="c4f61-134">[D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) represents the nesting depth of two types of static flow control instructions: [loop - vs](loop---vs.md)/[rep - vs](rep---vs.md) and [call - vs](call---vs.md)/[callnz bool - vs](callnz-bool---vs.md)/[if bool - vs](if-bool---vs.md). loop - vs/rep - vs instructions can be nested up to D3DVS20CAPS deep.</span></span> <span data-ttu-id="c4f61-135">De forma independiente, las instrucciones call - vs/callnz bool - vs se pueden anidar hasta D3DVS20CAPS deep.</span><span class="sxs-lookup"><span data-stu-id="c4f61-135">Independently, call - vs/callnz bool - vs instructions can be nested up to D3DVS20CAPS deep.</span></span> <span data-ttu-id="c4f61-136">Si también se establece D3DVS20CAPS, entonces [callnz pred - vs](callnz-pred---vs.md) se cuenta para la profundidad de anidamiento de la llamada - vs/callnz bool - vs/if bool - vs (vea [Límites](dx9-graphics-reference-asm-vs-instructions-flow-control.md) de anidamiento de control de flujo para obtener más información).</span><span class="sxs-lookup"><span data-stu-id="c4f61-136">If D3DVS20CAPS is also set, then [callnz pred - vs](callnz-pred---vs.md) is counted toward the nesting depth of call - vs/callnz bool - vs/if bool - vs (see [Flow Control Nesting Limits](dx9-graphics-reference-asm-vs-instructions-flow-control.md) for details).</span></span>

### <a name="predication"></a><span data-ttu-id="c4f61-137">Predicación</span><span class="sxs-lookup"><span data-stu-id="c4f61-137">Predication</span></span>

<span data-ttu-id="c4f61-138">Si [se establece D3DVS20CAPS,](/windows/desktop/direct3d9/d3dvs20caps) el dispositivo admite el [predicado setp comp - \_ vs](setp-comp---vs.md) y de instrucción.</span><span class="sxs-lookup"><span data-stu-id="c4f61-138">If [D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) is set, the device supports [setp\_comp - vs](setp-comp---vs.md) and instruction predication.</span></span> <span data-ttu-id="c4f61-139">Si D3DVS20CAPS también es mayor que 0, se admiten las siguientes instrucciones de control de flujo dinámico adicionales:</span><span class="sxs-lookup"><span data-stu-id="c4f61-139">If D3DVS20CAPS is also greater than 0, then the following additional dynamic flow control instructions are supported:</span></span>

-   [<span data-ttu-id="c4f61-140">if pred - vs</span><span class="sxs-lookup"><span data-stu-id="c4f61-140">if pred - vs</span></span>](if-pred---vs.md)
-   [<span data-ttu-id="c4f61-141">callnz pred - vs</span><span class="sxs-lookup"><span data-stu-id="c4f61-141">callnz pred - vs</span></span>](callnz-pred---vs.md)
-   [<span data-ttu-id="c4f61-142">breakp: vs</span><span class="sxs-lookup"><span data-stu-id="c4f61-142">breakp - vs</span></span>](breakp---vs.md)

### <a name="instruction-count"></a><span data-ttu-id="c4f61-143">Recuento de instrucciones</span><span class="sxs-lookup"><span data-stu-id="c4f61-143">Instruction Count</span></span>

<span data-ttu-id="c4f61-144">Cada sombreador de vértices puede tener hasta 256 instrucciones almacenadas.</span><span class="sxs-lookup"><span data-stu-id="c4f61-144">Each vertex shader can have up to 256 instructions stored.</span></span> <span data-ttu-id="c4f61-145">El número de instrucciones ejecutadas puede ser mucho mayor (debido a la compatibilidad con bucles o representantes) y está limitado por [**D3DCAPS9,**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9)que debe ser al menos 0xFFFF.</span><span class="sxs-lookup"><span data-stu-id="c4f61-145">The number of instructions run can be much higher (because of the loop/rep support), and is capped by [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9), which should be at least 0xFFFF.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c4f61-146">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c4f61-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c4f61-147">Sombreadores de vértices</span><span class="sxs-lookup"><span data-stu-id="c4f61-147">Vertex Shaders</span></span>](dx9-graphics-reference-asm-vs.md)
</dt> </dl>

 

 