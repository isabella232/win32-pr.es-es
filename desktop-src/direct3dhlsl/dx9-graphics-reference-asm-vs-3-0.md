---
title: vs_3_0
description: Obtenga información vs_3_0, un sombreador de vértices programable, que se forma de un conjunto de instrucciones que funcionan con datos de vértices.
ms.assetid: 0f40f946-3525-4203-bfe2-1cd941d8e2ec
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 310d64170280053c34766f214969f78d66560ea3
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2021
ms.locfileid: "112011078"
---
# <a name="vs_3_0"></a><span data-ttu-id="b4856-103">vs \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="b4856-103">vs\_3\_0</span></span>

<span data-ttu-id="b4856-104">Un sombreador de vértices programable se forma de un conjunto de instrucciones que funcionan con datos de vértices.</span><span class="sxs-lookup"><span data-stu-id="b4856-104">A programmable vertex shader is made up of a set of instructions that operate on vertex data.</span></span> <span data-ttu-id="b4856-105">Registra la transferencia de datos dentro y fuera de la ALU.</span><span class="sxs-lookup"><span data-stu-id="b4856-105">Registers transfer data in and out of the ALU.</span></span> <span data-ttu-id="b4856-106">Se puede aplicar un control adicional para modificar la instrucción, los resultados o los datos que se escriben.</span><span class="sxs-lookup"><span data-stu-id="b4856-106">Additional control can be applied to modify the instruction, the results, or what data gets written out.</span></span>

<span data-ttu-id="b4856-107">La versión del sombreador de \_ \_ vértices frente a 3 0 amplía el conjunto de características admitido por frente \_ a 2 \_ x.</span><span class="sxs-lookup"><span data-stu-id="b4856-107">Vertex shader version vs\_3\_0 extends the feature set supported by vs\_2\_x.</span></span> <span data-ttu-id="b4856-108">Cada una de las características de frente a 2 X que requiere que se establezca un límite, está disponible en frente \_ \_ a \_ 3 0 sin necesidad del \_ límite.</span><span class="sxs-lookup"><span data-stu-id="b4856-108">Each of the features in vs\_2\_X that requires a cap to be set, is available in vs\_3\_0 without requiring the cap.</span></span>

-   <span data-ttu-id="b4856-109">[Instrucciones: frente \_ a \_ 3 0](dx9-graphics-reference-asm-vs-instructions-vs-3-0.md) contiene una lista de las instrucciones disponibles.</span><span class="sxs-lookup"><span data-stu-id="b4856-109">[Instructions - vs\_3\_0](dx9-graphics-reference-asm-vs-instructions-vs-3-0.md) contains a list of the available instructions.</span></span>
-   <span data-ttu-id="b4856-110">[Registros: frente \_ a 3 \_ 0,](dx9-graphics-reference-asm-vs-registers-vs-3-0.md) se enumeran los distintos tipos de registros usados por el sombreador de vértices ALU.</span><span class="sxs-lookup"><span data-stu-id="b4856-110">[Registers - vs\_3\_0](dx9-graphics-reference-asm-vs-registers-vs-3-0.md) lists the different types of registers used by the vertex shader ALU.</span></span>
-   <span data-ttu-id="b4856-111">[Los modificadores de registro del sombreador](dx9-graphics-reference-asm-vs-registers-modifiers.md) de vértices se usan para modificar el funcionamiento de una instrucción.</span><span class="sxs-lookup"><span data-stu-id="b4856-111">[Vertex Shader Register Modifiers](dx9-graphics-reference-asm-vs-registers-modifiers.md) are used to modify the way an instruction works.</span></span>
-   <span data-ttu-id="b4856-112">[Los modificadores de registro de origen del sombreador de vértices](dx9-graphics-reference-asm-vs-registers-modifiers-source.md) modifican los datos de registro de origen antes de que se ejecute la instrucción.</span><span class="sxs-lookup"><span data-stu-id="b4856-112">[Vertex Shader Source Register Modifiers](dx9-graphics-reference-asm-vs-registers-modifiers-source.md) alter the source register data before the instruction runs.</span></span>
-   <span data-ttu-id="b4856-113">[Source Register Swling proporciona](dx9-graphics-reference-asm-vs-registers-modifiers-source-swizzling.md) control adicional sobre qué componentes de registro se leen, copian o escriben.</span><span class="sxs-lookup"><span data-stu-id="b4856-113">[Source Register Swizzling](dx9-graphics-reference-asm-vs-registers-modifiers-source-swizzling.md) gives additional control over which register components are read, copied, or written.</span></span>
-   <span data-ttu-id="b4856-114">[El enmascaramiento de registros de destino](dx9-graphics-reference-asm-vs-registers-modifiers-masking.md) determina qué componentes del registro de destino se escriben.</span><span class="sxs-lookup"><span data-stu-id="b4856-114">[Destination Register Masking](dx9-graphics-reference-asm-vs-registers-modifiers-masking.md) determines what components of the destination register get written.</span></span>

## <a name="new-features"></a><span data-ttu-id="b4856-115">Nuevas características</span><span class="sxs-lookup"><span data-stu-id="b4856-115">New Features</span></span>

<span data-ttu-id="b4856-116">Las nuevas características de la versión del sombreador de vértices frente \_ a \_ 3 0 se enumeran en las secciones siguientes.</span><span class="sxs-lookup"><span data-stu-id="b4856-116">New features of vertex shader version vs\_3\_0 are listed in the following sections.</span></span>

### <a name="indexing-registers"></a><span data-ttu-id="b4856-117">Indexación de registros</span><span class="sxs-lookup"><span data-stu-id="b4856-117">Indexing Registers</span></span>

<span data-ttu-id="b4856-118">En los modelos de sombreador anteriores, solo se podía indexar el banco de registros constante.</span><span class="sxs-lookup"><span data-stu-id="b4856-118">In the earlier shader models, only the constant register bank could be indexed.</span></span> <span data-ttu-id="b4856-119">En este modelo, se pueden indexar los siguientes bancos de registro mediante el registro de contador de bucles (aL):</span><span class="sxs-lookup"><span data-stu-id="b4856-119">In this model, the following register banks can be indexed, using the loop counter register (aL):</span></span>

-   <span data-ttu-id="b4856-120">Registro de entrada (v \# )</span><span class="sxs-lookup"><span data-stu-id="b4856-120">Input register (v\#)</span></span>
-   <span data-ttu-id="b4856-121">Registro de salida (o \# )</span><span class="sxs-lookup"><span data-stu-id="b4856-121">Output register (o\#)</span></span>

### <a name="vertex-textures"></a><span data-ttu-id="b4856-122">Texturas de vértice</span><span class="sxs-lookup"><span data-stu-id="b4856-122">Vertex Textures</span></span>

<span data-ttu-id="b4856-123">Este modelo de sombreador admite la búsqueda de textura en el sombreador de vértices mediante texldl.</span><span class="sxs-lookup"><span data-stu-id="b4856-123">This shader model supports texture lookup in the vertex shader using texldl.</span></span> <span data-ttu-id="b4856-124">El motor de vértices tiene cuatro fases del muestreador de textura (distintas del muestreador del mapa de desplazamiento y los muestreadores de textura en el motor de píxeles) que se pueden usar para muestrear texturas establecidas en esas fases.</span><span class="sxs-lookup"><span data-stu-id="b4856-124">The vertex engine has four texture sampler stages (distinct from the displacement map sampler and the texture samplers in the pixel engine) that can be used to sample textures set at those stages.</span></span> <span data-ttu-id="b4856-125">Vea [Texturas de vértice en vs \_ 3 \_ 0 (DirectX HLSL).](/windows/desktop/direct3d9/vertex-textures-in-vs-3-0)</span><span class="sxs-lookup"><span data-stu-id="b4856-125">See [Vertex Textures in vs\_3\_0 (DirectX HLSL)](/windows/desktop/direct3d9/vertex-textures-in-vs-3-0).</span></span>

### <a name="vertex-stream-frequency"></a><span data-ttu-id="b4856-126">Frecuencia de flujo de vértices</span><span class="sxs-lookup"><span data-stu-id="b4856-126">Vertex Stream Frequency</span></span>

<span data-ttu-id="b4856-127">Esta característica permite inicializar un subconjunto de los registros de entrada a una velocidad diferente de una vez por vértice.</span><span class="sxs-lookup"><span data-stu-id="b4856-127">This feature allows a subset of the input registers to be initialized at a rate different from once per vertex.</span></span> <span data-ttu-id="b4856-128">Vea [Dibujar geometría no indizada.](/windows/desktop/direct3d9/efficiently-drawing-multiple-instances-of-geometry)</span><span class="sxs-lookup"><span data-stu-id="b4856-128">See [Drawing Non-Indexed Geometry](/windows/desktop/direct3d9/efficiently-drawing-multiple-instances-of-geometry).</span></span>

### <a name="shader-output"></a><span data-ttu-id="b4856-129">Salida del sombreador</span><span class="sxs-lookup"><span data-stu-id="b4856-129">Shader Output</span></span>

<span data-ttu-id="b4856-130">De forma similar a \_ 2 \_ 0, la salida del sombreador puede variar con el control de flujo estático.</span><span class="sxs-lookup"><span data-stu-id="b4856-130">Similar to vs\_2\_0, the output of the shader can vary with static flow control.</span></span> <span data-ttu-id="b4856-131">Tenga cuidado con la bifurcación dinámica, ya que esto puede hacer que las salidas del sombreador varían por vértice.</span><span class="sxs-lookup"><span data-stu-id="b4856-131">Be careful with dynamic branching as this can cause shader outputs to vary per vertex.</span></span> <span data-ttu-id="b4856-132">Esto producirá resultados impredecibles en hardware diferente.</span><span class="sxs-lookup"><span data-stu-id="b4856-132">This will produce unpredictable results on different hardware.</span></span>

### <a name="dynamic-flow-control"></a><span data-ttu-id="b4856-133">Control de flujo dinámico</span><span class="sxs-lookup"><span data-stu-id="b4856-133">Dynamic flow control</span></span>

<span data-ttu-id="b4856-134">Se admiten todas las instrucciones de control de flujo dinámico.</span><span class="sxs-lookup"><span data-stu-id="b4856-134">All dynamic flow control instructions are supported.</span></span> <span data-ttu-id="b4856-135">El valor máximo de profundidad de anidamiento permitido es 24.</span><span class="sxs-lookup"><span data-stu-id="b4856-135">The maximum nesting depth value allowed is 24.</span></span> <span data-ttu-id="b4856-136">(Consulte [Límites de anidamiento de controles de flujo](dx9-graphics-reference-asm-vs-instructions-flow-control.md) para obtener más información).</span><span class="sxs-lookup"><span data-stu-id="b4856-136">(See [Flow Control Nesting Limits](dx9-graphics-reference-asm-vs-instructions-flow-control.md) for details.)</span></span>

### <a name="temporary-registers"></a><span data-ttu-id="b4856-137">Registros temporales</span><span class="sxs-lookup"><span data-stu-id="b4856-137">Temporary Registers</span></span>

<span data-ttu-id="b4856-138">Se admite un total de 32 registros temporales \# (r).</span><span class="sxs-lookup"><span data-stu-id="b4856-138">A total of 32 temporary registers (r\#) is supported.</span></span>

### <a name="static-flow-control"></a><span data-ttu-id="b4856-139">Control de flujo estático</span><span class="sxs-lookup"><span data-stu-id="b4856-139">Static Flow Control</span></span>

<span data-ttu-id="b4856-140">La profundidad de anidamiento máxima del [bucle (frente](loop---vs.md) / [a rep) frente](rep---vs.md) a 4.</span><span class="sxs-lookup"><span data-stu-id="b4856-140">The maximum nesting depth for [loop - vs](loop---vs.md)/[rep - vs](rep---vs.md) is 4.</span></span> <span data-ttu-id="b4856-141">La profundidad de anidamiento máxima para [la llamada ( vs](call---vs.md) / [callnz bool - vs](callnz-bool---vs.md) / [callnz pred ) vs](callnz-pred---vs.md) es 4.</span><span class="sxs-lookup"><span data-stu-id="b4856-141">The maximum nesting depth for [call - vs](call---vs.md)/[callnz bool - vs](callnz-bool---vs.md)/[callnz pred - vs](callnz-pred---vs.md) is 4.</span></span> <span data-ttu-id="b4856-142">Para [if bool - vs](if-bool---vs.md), el valor máximo de profundidad de anidamiento permitido es 24.</span><span class="sxs-lookup"><span data-stu-id="b4856-142">For [if bool - vs](if-bool---vs.md), the maximum nesting depth value allowed is 24.</span></span> <span data-ttu-id="b4856-143">(Consulte [Límites de anidamiento de controles de flujo](dx9-graphics-reference-asm-vs-instructions-flow-control.md) para obtener más información).</span><span class="sxs-lookup"><span data-stu-id="b4856-143">(See [Flow Control Nesting Limits](dx9-graphics-reference-asm-vs-instructions-flow-control.md) for details.)</span></span>

### <a name="predication"></a><span data-ttu-id="b4856-144">Predicación</span><span class="sxs-lookup"><span data-stu-id="b4856-144">Predication</span></span>

<span data-ttu-id="b4856-145">Se admite el predicado de instrucciones.</span><span class="sxs-lookup"><span data-stu-id="b4856-145">Instruction predication is supported.</span></span> <span data-ttu-id="b4856-146">Use [setp \_ comp - vs para](setp-comp---vs.md) establecer el registro de predicado.</span><span class="sxs-lookup"><span data-stu-id="b4856-146">Use [setp\_comp - vs](setp-comp---vs.md) to set the predicate register.</span></span>

### <a name="instruction-count"></a><span data-ttu-id="b4856-147">Recuento de instrucciones</span><span class="sxs-lookup"><span data-stu-id="b4856-147">Instruction Count</span></span>

<span data-ttu-id="b4856-148">Cada sombreador de vértices se permite desde 512 hasta el número de ranuras de MaxVertexShader30InstructionSlots en [**D3DCAPS9.**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9)</span><span class="sxs-lookup"><span data-stu-id="b4856-148">Each vertex shader is allowed anywhere from 512 up to the number of slots in MaxVertexShader30InstructionSlots in [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9).</span></span> <span data-ttu-id="b4856-149">El número de instrucciones que se ejecutan puede ser mucho mayor debido a la compatibilidad con bucles o representantes. sin embargo, maxVShaderInstructionsExecuted en D3DCAPS9, que debe ser al menos 0xFFFF.</span><span class="sxs-lookup"><span data-stu-id="b4856-149">The number of instructions run can be much higher because of the loop/rep support; however, this is capped by MaxVShaderInstructionsExecuted in D3DCAPS9 which should be at least 0xFFFF.</span></span>

### <a name="device-caps"></a><span data-ttu-id="b4856-150">Límites de dispositivo</span><span class="sxs-lookup"><span data-stu-id="b4856-150">Device Caps</span></span>

<span data-ttu-id="b4856-151">Si se admite Sombreador de vértices 3 0, se admiten los siguientes límites en \_ el hardware (como mínimo):</span><span class="sxs-lookup"><span data-stu-id="b4856-151">If Vertex Shader 3\_0 is supported, the following caps are supported in hardware (at a minimum):</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b4856-152">Tapa</span><span class="sxs-lookup"><span data-stu-id="b4856-152">Cap</span></span></th>
<th><span data-ttu-id="b4856-153">Capacidad</span><span class="sxs-lookup"><span data-stu-id="b4856-153">Capability</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b4856-154">Límites de sombreador</span><span class="sxs-lookup"><span data-stu-id="b4856-154">Shader caps</span></span></td>
<td><ul>
<li><span data-ttu-id="b4856-155">DynamicFlowControlDepth es 24</span><span class="sxs-lookup"><span data-stu-id="b4856-155">DynamicFlowControlDepth is 24</span></span></li>
<li><span data-ttu-id="b4856-156">NumTemps es 32</span><span class="sxs-lookup"><span data-stu-id="b4856-156">NumTemps is 32</span></span></li>
<li><span data-ttu-id="b4856-157">StaticFlowControlDepth es 4</span><span class="sxs-lookup"><span data-stu-id="b4856-157">StaticFlowControlDepth is 4</span></span></li>
<li><span data-ttu-id="b4856-158">Se admite la predicado.</span><span class="sxs-lookup"><span data-stu-id="b4856-158">Predication is supported.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b4856-159">GuardBandLeft, GuardBandTop, GuardBandRight, GuardBandBottom</span><span class="sxs-lookup"><span data-stu-id="b4856-159">GuardBandLeft, GuardBandTop, GuardBandRight, GuardBandBottom</span></span></td>
<td><span data-ttu-id="b4856-160">8 K</span><span class="sxs-lookup"><span data-stu-id="b4856-160">8K</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b4856-161">VertexShaderVersion</span><span class="sxs-lookup"><span data-stu-id="b4856-161">VertexShaderVersion</span></span></td>
<td><span data-ttu-id="b4856-162">3_0</span><span class="sxs-lookup"><span data-stu-id="b4856-162">3_0</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b4856-163">MaxVertexShaderConst</span><span class="sxs-lookup"><span data-stu-id="b4856-163">MaxVertexShaderConst</span></span></td>
<td><span data-ttu-id="b4856-164">256</span><span class="sxs-lookup"><span data-stu-id="b4856-164">256</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b4856-165">MaxVertexShader30InstructionSlots</span><span class="sxs-lookup"><span data-stu-id="b4856-165">MaxVertexShader30InstructionSlots</span></span></td>
<td><span data-ttu-id="b4856-166">512</span><span class="sxs-lookup"><span data-stu-id="b4856-166">512</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b4856-167">Compatibilidad con la nube</span><span class="sxs-lookup"><span data-stu-id="b4856-167">Fog support</span></span></td>
<td><span data-ttu-id="b4856-168">D3DPRASTERCAPS_FOGVERTEX</span><span class="sxs-lookup"><span data-stu-id="b4856-168">D3DPRASTERCAPS_FOGVERTEX</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b4856-169">VertexTextureFilterCaps</span><span class="sxs-lookup"><span data-stu-id="b4856-169">VertexTextureFilterCaps</span></span></td>
<td><ul>
<li><span data-ttu-id="b4856-170"><a href="/windows/desktop/direct3d9/d3dptfiltercaps">D3DPTFILTERCAPS_MINFPOINT</a></span><span class="sxs-lookup"><span data-stu-id="b4856-170"><a href="/windows/desktop/direct3d9/d3dptfiltercaps">D3DPTFILTERCAPS_MINFPOINT</a></span></span></li>
<li><span data-ttu-id="b4856-171"><a href="/windows/desktop/direct3d9/d3dptfiltercaps">D3DPTFILTERCAPS_MAGFPOINT</a></span><span class="sxs-lookup"><span data-stu-id="b4856-171"><a href="/windows/desktop/direct3d9/d3dptfiltercaps">D3DPTFILTERCAPS_MAGFPOINT</a></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b4856-172"><a href="/windows/desktop/direct3d9/d3ddevcaps2">D3DDEVCAPS2_VERTEXELEMENTSCANSHARESTREAMOFFSET</a></span><span class="sxs-lookup"><span data-stu-id="b4856-172"><a href="/windows/desktop/direct3d9/d3ddevcaps2">D3DDEVCAPS2_VERTEXELEMENTSCANSHARESTREAMOFFSET</a></span></span></td>
<td><span data-ttu-id="b4856-173">Los elementos de vértice de una declaración de vértice pueden compartir el mismo desplazamiento de flujo.</span><span class="sxs-lookup"><span data-stu-id="b4856-173">Vertex elements in a vertex declaration can share the same stream offset.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b4856-174">Formatos de vértice</span><span class="sxs-lookup"><span data-stu-id="b4856-174">Vertex formats</span></span></td>
<td><ul>
<li><span data-ttu-id="b4856-175">D3DDECLTYPE_UBYTE4</span><span class="sxs-lookup"><span data-stu-id="b4856-175">D3DDECLTYPE_UBYTE4</span></span></li>
<li><span data-ttu-id="b4856-176">D3DDECLTYPE_UBYTE4N</span><span class="sxs-lookup"><span data-stu-id="b4856-176">D3DDECLTYPE_UBYTE4N</span></span></li>
<li><span data-ttu-id="b4856-177">D3DDECLTYPE_SHORT2N</span><span class="sxs-lookup"><span data-stu-id="b4856-177">D3DDECLTYPE_SHORT2N</span></span></li>
<li><span data-ttu-id="b4856-178">D3DDECLTYPE_SHORT4N</span><span class="sxs-lookup"><span data-stu-id="b4856-178">D3DDECLTYPE_SHORT4N</span></span></li>
<li><span data-ttu-id="b4856-179">D3DDECLTYPE_FLOAT16_2</span><span class="sxs-lookup"><span data-stu-id="b4856-179">D3DDECLTYPE_FLOAT16_2</span></span></li>
<li><span data-ttu-id="b4856-180">D3DDECLTYPE_FLOAT16_4</span><span class="sxs-lookup"><span data-stu-id="b4856-180">D3DDECLTYPE_FLOAT16_4</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="b4856-181">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b4856-181">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b4856-182">Sombreadores de vértices</span><span class="sxs-lookup"><span data-stu-id="b4856-182">Vertex Shaders</span></span>](dx9-graphics-reference-asm-vs.md)
</dt> </dl>

 

 