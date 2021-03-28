---
title: vs_3_0
description: Un sombreador de vértices programable se compone de un conjunto de instrucciones que operan en los datos de vértices. Registra datos de transferencia dentro y fuera de la ALU. Se puede aplicar un control adicional para modificar la instrucción, los resultados o los datos que se escriben.
ms.assetid: 0f40f946-3525-4203-bfe2-1cd941d8e2ec
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 22a0e6e84aff34dcec44713dc4382e391ad05c2b
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/08/2020
ms.locfileid: "103904878"
---
# <a name="vs_3_0"></a><span data-ttu-id="36924-105">vs \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="36924-105">vs\_3\_0</span></span>

<span data-ttu-id="36924-106">Un sombreador de vértices programable se compone de un conjunto de instrucciones que operan en los datos de vértices.</span><span class="sxs-lookup"><span data-stu-id="36924-106">A programmable vertex shader is made up of a set of instructions that operate on vertex data.</span></span> <span data-ttu-id="36924-107">Registra datos de transferencia dentro y fuera de la ALU.</span><span class="sxs-lookup"><span data-stu-id="36924-107">Registers transfer data in and out of the ALU.</span></span> <span data-ttu-id="36924-108">Se puede aplicar un control adicional para modificar la instrucción, los resultados o los datos que se escriben.</span><span class="sxs-lookup"><span data-stu-id="36924-108">Additional control can be applied to modify the instruction, the results, or what data gets written out.</span></span>

<span data-ttu-id="36924-109">La versión del sombreador de vértices frente \_ \_ a 3 0 extiende el conjunto de características compatible con vs \_ 2 \_ x.</span><span class="sxs-lookup"><span data-stu-id="36924-109">Vertex shader version vs\_3\_0 extends the feature set supported by vs\_2\_x.</span></span> <span data-ttu-id="36924-110">Cada una de las características de vs \_ 2 \_ X que requiere que se establezca un límite, está disponible en vs \_ 3 \_ 0 sin necesidad del Cap.</span><span class="sxs-lookup"><span data-stu-id="36924-110">Each of the features in vs\_2\_X that requires a cap to be set, is available in vs\_3\_0 without requiring the cap.</span></span>

-   <span data-ttu-id="36924-111">[Instrucciones: vs \_ 3 \_ 0](dx9-graphics-reference-asm-vs-instructions-vs-3-0.md) contiene una lista de las instrucciones disponibles.</span><span class="sxs-lookup"><span data-stu-id="36924-111">[Instructions - vs\_3\_0](dx9-graphics-reference-asm-vs-instructions-vs-3-0.md) contains a list of the available instructions.</span></span>
-   <span data-ttu-id="36924-112">[Registros: vs \_ 3 \_ 0](dx9-graphics-reference-asm-vs-registers-vs-3-0.md) muestra los distintos tipos de registros utilizados por el sombreador de vértices Alu.</span><span class="sxs-lookup"><span data-stu-id="36924-112">[Registers - vs\_3\_0](dx9-graphics-reference-asm-vs-registers-vs-3-0.md) lists the different types of registers used by the vertex shader ALU.</span></span>
-   <span data-ttu-id="36924-113">Los [modificadores de registro del sombreador de vértices](dx9-graphics-reference-asm-vs-registers-modifiers.md) se utilizan para modificar la forma en que funciona una instrucción.</span><span class="sxs-lookup"><span data-stu-id="36924-113">[Vertex Shader Register Modifiers](dx9-graphics-reference-asm-vs-registers-modifiers.md) are used to modify the way an instruction works.</span></span>
-   <span data-ttu-id="36924-114">Los [modificadores de registro de origen del sombreador de vértices](dx9-graphics-reference-asm-vs-registers-modifiers-source.md) modifican los datos del registro de origen antes de que se ejecute la instrucción.</span><span class="sxs-lookup"><span data-stu-id="36924-114">[Vertex Shader Source Register Modifiers](dx9-graphics-reference-asm-vs-registers-modifiers-source.md) alter the source register data before the instruction runs.</span></span>
-   <span data-ttu-id="36924-115">[El registro de origen permutación](dx9-graphics-reference-asm-vs-registers-modifiers-source-swizzling.md) proporciona control adicional sobre qué componentes de registro se leen, se copian o se escriben.</span><span class="sxs-lookup"><span data-stu-id="36924-115">[Source Register Swizzling](dx9-graphics-reference-asm-vs-registers-modifiers-source-swizzling.md) gives additional control over which register components are read, copied, or written.</span></span>
-   <span data-ttu-id="36924-116">[El enmascaramiento del registro de destino](dx9-graphics-reference-asm-vs-registers-modifiers-masking.md) determina los componentes del registro de destino que se van a escribir.</span><span class="sxs-lookup"><span data-stu-id="36924-116">[Destination Register Masking](dx9-graphics-reference-asm-vs-registers-modifiers-masking.md) determines what components of the destination register get written.</span></span>

## <a name="new-features"></a><span data-ttu-id="36924-117">Nuevas características</span><span class="sxs-lookup"><span data-stu-id="36924-117">New Features</span></span>

<span data-ttu-id="36924-118">\_ \_ En las secciones siguientes se enumeran las nuevas características de la versión de sombreador de vértices frente a 3 0.</span><span class="sxs-lookup"><span data-stu-id="36924-118">New features of vertex shader version vs\_3\_0 are listed in the following sections.</span></span>

### <a name="indexing-registers"></a><span data-ttu-id="36924-119">Registros de indexación</span><span class="sxs-lookup"><span data-stu-id="36924-119">Indexing Registers</span></span>

<span data-ttu-id="36924-120">En los modelos de sombreador anteriores, solo se podría indexar el Banco de registro de constantes.</span><span class="sxs-lookup"><span data-stu-id="36924-120">In the earlier shader models, only the constant register bank could be indexed.</span></span> <span data-ttu-id="36924-121">En este modelo, se pueden indexar los siguientes bancos de registro mediante el registro de contador de bucle (aL):</span><span class="sxs-lookup"><span data-stu-id="36924-121">In this model, the following register banks can be indexed, using the loop counter register (aL):</span></span>

-   <span data-ttu-id="36924-122">Registro de entrada (v \# )</span><span class="sxs-lookup"><span data-stu-id="36924-122">Input register (v\#)</span></span>
-   <span data-ttu-id="36924-123">Registro de salida (o \# )</span><span class="sxs-lookup"><span data-stu-id="36924-123">Output register (o\#)</span></span>

### <a name="vertex-textures"></a><span data-ttu-id="36924-124">Texturas de vértices</span><span class="sxs-lookup"><span data-stu-id="36924-124">Vertex Textures</span></span>

<span data-ttu-id="36924-125">Este modelo de sombreador admite la búsqueda de texturas en el sombreador de vértices mediante texldl.</span><span class="sxs-lookup"><span data-stu-id="36924-125">This shader model supports texture lookup in the vertex shader using texldl.</span></span> <span data-ttu-id="36924-126">El motor de vértices tiene cuatro fases de muestra de textura (distintas de la muestra de mapa de desplazamiento y los muestreadores de textura en el motor de píxeles) que se pueden usar para muestrear las texturas establecidas en esas fases.</span><span class="sxs-lookup"><span data-stu-id="36924-126">The vertex engine has four texture sampler stages (distinct from the displacement map sampler and the texture samplers in the pixel engine) that can be used to sample textures set at those stages.</span></span> <span data-ttu-id="36924-127">Vea [texturas de vértices en vs \_ 3 \_ 0 (DirectX HLSL)](/windows/desktop/direct3d9/vertex-textures-in-vs-3-0).</span><span class="sxs-lookup"><span data-stu-id="36924-127">See [Vertex Textures in vs\_3\_0 (DirectX HLSL)](/windows/desktop/direct3d9/vertex-textures-in-vs-3-0).</span></span>

### <a name="vertex-stream-frequency"></a><span data-ttu-id="36924-128">Frecuencia de flujo de vértices</span><span class="sxs-lookup"><span data-stu-id="36924-128">Vertex Stream Frequency</span></span>

<span data-ttu-id="36924-129">Esta característica permite inicializar un subconjunto de los registros de entrada a una velocidad distinta de una vez por cada vértice.</span><span class="sxs-lookup"><span data-stu-id="36924-129">This feature allows a subset of the input registers to be initialized at a rate different from once per vertex.</span></span> <span data-ttu-id="36924-130">Vea [dibujar geometría no indizada](/windows/desktop/direct3d9/efficiently-drawing-multiple-instances-of-geometry).</span><span class="sxs-lookup"><span data-stu-id="36924-130">See [Drawing Non-Indexed Geometry](/windows/desktop/direct3d9/efficiently-drawing-multiple-instances-of-geometry).</span></span>

### <a name="shader-output"></a><span data-ttu-id="36924-131">Salida del sombreador</span><span class="sxs-lookup"><span data-stu-id="36924-131">Shader Output</span></span>

<span data-ttu-id="36924-132">Similar a vs \_ 2 \_ 0, la salida del sombreador puede variar con el control de flujo estático.</span><span class="sxs-lookup"><span data-stu-id="36924-132">Similar to vs\_2\_0, the output of the shader can vary with static flow control.</span></span> <span data-ttu-id="36924-133">Tenga cuidado con la bifurcación dinámica, ya que esto puede hacer que las salidas del sombreador varíen según el vértice.</span><span class="sxs-lookup"><span data-stu-id="36924-133">Be careful with dynamic branching as this can cause shader outputs to vary per vertex.</span></span> <span data-ttu-id="36924-134">Esto producirá resultados imprevisibles en hardware diferente.</span><span class="sxs-lookup"><span data-stu-id="36924-134">This will produce unpredictable results on different hardware.</span></span>

### <a name="dynamic-flow-control"></a><span data-ttu-id="36924-135">Control de flujo dinámico</span><span class="sxs-lookup"><span data-stu-id="36924-135">Dynamic flow control</span></span>

<span data-ttu-id="36924-136">Se admiten todas las instrucciones de control de flujo dinámico.</span><span class="sxs-lookup"><span data-stu-id="36924-136">All dynamic flow control instructions are supported.</span></span> <span data-ttu-id="36924-137">El valor de profundidad de anidamiento máximo permitido es 24.</span><span class="sxs-lookup"><span data-stu-id="36924-137">The maximum nesting depth value allowed is 24.</span></span> <span data-ttu-id="36924-138">(Vea [límites de anidamiento de control de flujo](dx9-graphics-reference-asm-vs-instructions-flow-control.md) para más información).</span><span class="sxs-lookup"><span data-stu-id="36924-138">(See [Flow Control Nesting Limits](dx9-graphics-reference-asm-vs-instructions-flow-control.md) for details.)</span></span>

### <a name="temporary-registers"></a><span data-ttu-id="36924-139">Registros temporales</span><span class="sxs-lookup"><span data-stu-id="36924-139">Temporary Registers</span></span>

<span data-ttu-id="36924-140">Se admite un total de 32 registros temporales (r \# ).</span><span class="sxs-lookup"><span data-stu-id="36924-140">A total of 32 temporary registers (r\#) is supported.</span></span>

### <a name="static-flow-control"></a><span data-ttu-id="36924-141">Control de flujo estático</span><span class="sxs-lookup"><span data-stu-id="36924-141">Static Flow Control</span></span>

<span data-ttu-id="36924-142">La profundidad de anidamiento máxima para el [bucle-vs](loop---vs.md) / [REP-vs](rep---vs.md) es 4.</span><span class="sxs-lookup"><span data-stu-id="36924-142">The maximum nesting depth for [loop - vs](loop---vs.md)/[rep - vs](rep---vs.md) is 4.</span></span> <span data-ttu-id="36924-143">La profundidad de anidamiento máxima para [Call-vs](call---vs.md) / [callnz bool-vs](callnz-bool---vs.md) / [callnz Pred-vs](callnz-pred---vs.md) es 4.</span><span class="sxs-lookup"><span data-stu-id="36924-143">The maximum nesting depth for [call - vs](call---vs.md)/[callnz bool - vs](callnz-bool---vs.md)/[callnz pred - vs](callnz-pred---vs.md) is 4.</span></span> <span data-ttu-id="36924-144">Para [Si bool-vs](if-bool---vs.md), el valor de profundidad de anidamiento máximo permitido es 24.</span><span class="sxs-lookup"><span data-stu-id="36924-144">For [if bool - vs](if-bool---vs.md), the maximum nesting depth value allowed is 24.</span></span> <span data-ttu-id="36924-145">(Vea [límites de anidamiento de control de flujo](dx9-graphics-reference-asm-vs-instructions-flow-control.md) para más información).</span><span class="sxs-lookup"><span data-stu-id="36924-145">(See [Flow Control Nesting Limits](dx9-graphics-reference-asm-vs-instructions-flow-control.md) for details.)</span></span>

### <a name="predication"></a><span data-ttu-id="36924-146">Predicación</span><span class="sxs-lookup"><span data-stu-id="36924-146">Predication</span></span>

<span data-ttu-id="36924-147">Se admite la instrucción predication.</span><span class="sxs-lookup"><span data-stu-id="36924-147">Instruction predication is supported.</span></span> <span data-ttu-id="36924-148">Use [SETP \_ COMP-vs](setp-comp---vs.md) para establecer el registro de predicado.</span><span class="sxs-lookup"><span data-stu-id="36924-148">Use [setp\_comp - vs](setp-comp---vs.md) to set the predicate register.</span></span>

### <a name="instruction-count"></a><span data-ttu-id="36924-149">Recuento de instrucciones</span><span class="sxs-lookup"><span data-stu-id="36924-149">Instruction Count</span></span>

<span data-ttu-id="36924-150">Cada sombreador de vértices se permite desde 512 hasta el número de ranuras de MaxVertexShader30InstructionSlots en [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9).</span><span class="sxs-lookup"><span data-stu-id="36924-150">Each vertex shader is allowed anywhere from 512 up to the number of slots in MaxVertexShader30InstructionSlots in [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9).</span></span> <span data-ttu-id="36924-151">El número de instrucciones que se ejecutan puede ser mucho mayor debido a la compatibilidad con bucles o representantes; sin embargo, esto está limitado por MaxVShaderInstructionsExecuted en D3DCAPS9, que debe ser al menos 0xFFFF.</span><span class="sxs-lookup"><span data-stu-id="36924-151">The number of instructions run can be much higher because of the loop/rep support; however, this is capped by MaxVShaderInstructionsExecuted in D3DCAPS9 which should be at least 0xFFFF.</span></span>

### <a name="device-caps"></a><span data-ttu-id="36924-152">Cap del dispositivo</span><span class="sxs-lookup"><span data-stu-id="36924-152">Device Caps</span></span>

<span data-ttu-id="36924-153">Si se admite el sombreador de vértices 3 \_ 0, se admiten los siguientes límites en el hardware (como mínimo):</span><span class="sxs-lookup"><span data-stu-id="36924-153">If Vertex Shader 3\_0 is supported, the following caps are supported in hardware (at a minimum):</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="36924-154">Punto</span><span class="sxs-lookup"><span data-stu-id="36924-154">Cap</span></span></th>
<th><span data-ttu-id="36924-155">Capacidad</span><span class="sxs-lookup"><span data-stu-id="36924-155">Capability</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="36924-156">Límites del sombreador</span><span class="sxs-lookup"><span data-stu-id="36924-156">Shader caps</span></span></td>
<td><ul>
<li><span data-ttu-id="36924-157">DynamicFlowControlDepth es 24</span><span class="sxs-lookup"><span data-stu-id="36924-157">DynamicFlowControlDepth is 24</span></span></li>
<li><span data-ttu-id="36924-158">NumTemps es 32</span><span class="sxs-lookup"><span data-stu-id="36924-158">NumTemps is 32</span></span></li>
<li><span data-ttu-id="36924-159">StaticFlowControlDepth es 4</span><span class="sxs-lookup"><span data-stu-id="36924-159">StaticFlowControlDepth is 4</span></span></li>
<li><span data-ttu-id="36924-160">Se admite Predication.</span><span class="sxs-lookup"><span data-stu-id="36924-160">Predication is supported.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="36924-161">GuardBandLeft, GuardBandTop, GuardBandRight, GuardBandBottom</span><span class="sxs-lookup"><span data-stu-id="36924-161">GuardBandLeft, GuardBandTop, GuardBandRight, GuardBandBottom</span></span></td>
<td><span data-ttu-id="36924-162">8 K</span><span class="sxs-lookup"><span data-stu-id="36924-162">8K</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="36924-163">VertexShaderVersion</span><span class="sxs-lookup"><span data-stu-id="36924-163">VertexShaderVersion</span></span></td>
<td><span data-ttu-id="36924-164">3_0</span><span class="sxs-lookup"><span data-stu-id="36924-164">3_0</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="36924-165">MaxVertexShaderConst</span><span class="sxs-lookup"><span data-stu-id="36924-165">MaxVertexShaderConst</span></span></td>
<td><span data-ttu-id="36924-166">256</span><span class="sxs-lookup"><span data-stu-id="36924-166">256</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="36924-167">MaxVertexShader30InstructionSlots</span><span class="sxs-lookup"><span data-stu-id="36924-167">MaxVertexShader30InstructionSlots</span></span></td>
<td><span data-ttu-id="36924-168">512</span><span class="sxs-lookup"><span data-stu-id="36924-168">512</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="36924-169">Compatibilidad con niebla</span><span class="sxs-lookup"><span data-stu-id="36924-169">Fog support</span></span></td>
<td><span data-ttu-id="36924-170">D3DPRASTERCAPS_FOGVERTEX</span><span class="sxs-lookup"><span data-stu-id="36924-170">D3DPRASTERCAPS_FOGVERTEX</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="36924-171">VertexTextureFilterCaps</span><span class="sxs-lookup"><span data-stu-id="36924-171">VertexTextureFilterCaps</span></span></td>
<td><ul>
<li><span data-ttu-id="36924-172"><a href="/windows/desktop/direct3d9/d3dptfiltercaps">D3DPTFILTERCAPS_MINFPOINT</a></span><span class="sxs-lookup"><span data-stu-id="36924-172"><a href="/windows/desktop/direct3d9/d3dptfiltercaps">D3DPTFILTERCAPS_MINFPOINT</a></span></span></li>
<li><span data-ttu-id="36924-173"><a href="/windows/desktop/direct3d9/d3dptfiltercaps">D3DPTFILTERCAPS_MAGFPOINT</a></span><span class="sxs-lookup"><span data-stu-id="36924-173"><a href="/windows/desktop/direct3d9/d3dptfiltercaps">D3DPTFILTERCAPS_MAGFPOINT</a></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="36924-174"><a href="/windows/desktop/direct3d9/d3ddevcaps2">D3DDEVCAPS2_VERTEXELEMENTSCANSHARESTREAMOFFSET</a></span><span class="sxs-lookup"><span data-stu-id="36924-174"><a href="/windows/desktop/direct3d9/d3ddevcaps2">D3DDEVCAPS2_VERTEXELEMENTSCANSHARESTREAMOFFSET</a></span></span></td>
<td><span data-ttu-id="36924-175">Los elementos de vértice en una declaración de vértice pueden compartir el mismo desplazamiento de flujo.</span><span class="sxs-lookup"><span data-stu-id="36924-175">Vertex elements in a vertex declaration can share the same stream offset.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="36924-176">Formatos de vértices</span><span class="sxs-lookup"><span data-stu-id="36924-176">Vertex formats</span></span></td>
<td><ul>
<li><span data-ttu-id="36924-177">D3DDECLTYPE_UBYTE4</span><span class="sxs-lookup"><span data-stu-id="36924-177">D3DDECLTYPE_UBYTE4</span></span></li>
<li><span data-ttu-id="36924-178">D3DDECLTYPE_UBYTE4N</span><span class="sxs-lookup"><span data-stu-id="36924-178">D3DDECLTYPE_UBYTE4N</span></span></li>
<li><span data-ttu-id="36924-179">D3DDECLTYPE_SHORT2N</span><span class="sxs-lookup"><span data-stu-id="36924-179">D3DDECLTYPE_SHORT2N</span></span></li>
<li><span data-ttu-id="36924-180">D3DDECLTYPE_SHORT4N</span><span class="sxs-lookup"><span data-stu-id="36924-180">D3DDECLTYPE_SHORT4N</span></span></li>
<li><span data-ttu-id="36924-181">D3DDECLTYPE_FLOAT16_2</span><span class="sxs-lookup"><span data-stu-id="36924-181">D3DDECLTYPE_FLOAT16_2</span></span></li>
<li><span data-ttu-id="36924-182">D3DDECLTYPE_FLOAT16_4</span><span class="sxs-lookup"><span data-stu-id="36924-182">D3DDECLTYPE_FLOAT16_4</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="36924-183">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="36924-183">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="36924-184">Sombreadores de vértices</span><span class="sxs-lookup"><span data-stu-id="36924-184">Vertex Shaders</span></span>](dx9-graphics-reference-asm-vs.md)
</dt> </dl>

 

 