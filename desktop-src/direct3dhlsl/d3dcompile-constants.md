---
title: Constantes D3DCOMPILE (D3DCompiler. h)
description: Las constantes D3DCOMPILE especifican cómo el compilador compila el código HLSL.
ms.assetid: 039627DD-D6A4-4EA3-8E91-D2A20770E6FF
topic_type:
- apiref
api_name:
- D3DCOMPILE_DEBUG
- D3DCOMPILE_SKIP_VALIDATION
- D3DCOMPILE_SKIP_OPTIMIZATION
- D3DCOMPILE_PACK_MATRIX_ROW_MAJOR
- D3DCOMPILE_PACK_MATRIX_COLUMN_MAJOR
- D3DCOMPILE_PARTIAL_PRECISION
- D3DCOMPILE_FORCE_VS_SOFTWARE_NO_OPT
- D3DCOMPILE_FORCE_PS_SOFTWARE_NO_OPT
- D3DCOMPILE_NO_PRESHADER
- D3DCOMPILE_AVOID_FLOW_CONTROL
- D3DCOMPILE_PREFER_FLOW_CONTROL
- D3DCOMPILE_ENABLE_STRICTNESS
- D3DCOMPILE_ENABLE_BACKWARDS_COMPATIBILITY
- D3DCOMPILE_IEEE_STRICTNESS
- D3DCOMPILE_OPTIMIZATION_LEVEL0
- D3DCOMPILE_OPTIMIZATION_LEVEL1
- D3DCOMPILE_OPTIMIZATION_LEVEL2
- D3DCOMPILE_OPTIMIZATION_LEVEL3
- D3DCOMPILE_WARNINGS_ARE_ERRORS
- D3DCOMPILE_RESOURCES_MAY_ALIAS
- D3DCOMPILE_ENABLE_UNBOUNDED_DESCRIPTOR_TABLES
- D3DCOMPILE_ALL_RESOURCES_BOUND
api_location:
- D3DCompiler.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfd396eef06260ae879a3bb816d0bd89a078ea53
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280259"
---
# <a name="d3dcompile-constants"></a><span data-ttu-id="9415c-103">Constantes de D3DCOMPILE</span><span class="sxs-lookup"><span data-stu-id="9415c-103">D3DCOMPILE Constants</span></span>

<span data-ttu-id="9415c-104">Las constantes D3DCOMPILE especifican cómo el compilador compila el código HLSL.</span><span class="sxs-lookup"><span data-stu-id="9415c-104">The D3DCOMPILE constants specify how the compiler compiles the HLSL code.</span></span>

<dl> <dt>

<span data-ttu-id="9415c-105"><span id="D3DCOMPILE_DEBUG"></span><span id="d3dcompile_debug"></span>**Depuración de D3DCOMPILE \_**</span><span class="sxs-lookup"><span data-stu-id="9415c-105"><span id="D3DCOMPILE_DEBUG"></span><span id="d3dcompile_debug"></span>**D3DCOMPILE\_DEBUG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9415c-106">(1 << 0)</span><span class="sxs-lookup"><span data-stu-id="9415c-106">(1 << 0)</span></span>
</dt> <dt>



<span data-ttu-id="9415c-107">Indica al compilador que inserte información de archivo/línea/tipo/símbolo de depuración en el código de salida.</span><span class="sxs-lookup"><span data-stu-id="9415c-107">Directs the compiler to insert debug file/line/type/symbol information into the output code.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9415c-108"><span id="D3DCOMPILE_SKIP_VALIDATION"></span><span id="d3dcompile_skip_validation"></span>**D3DCOMPILE \_ omitir \_ validación**</span><span class="sxs-lookup"><span data-stu-id="9415c-108"><span id="D3DCOMPILE_SKIP_VALIDATION"></span><span id="d3dcompile_skip_validation"></span>**D3DCOMPILE\_SKIP\_VALIDATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9415c-109">(1 << 1)</span><span class="sxs-lookup"><span data-stu-id="9415c-109">(1 << 1)</span></span>
</dt> <dt>



<span data-ttu-id="9415c-110">Indica al compilador que no valide el código generado con respecto a las capacidades y restricciones conocidas.</span><span class="sxs-lookup"><span data-stu-id="9415c-110">Directs the compiler not to validate the generated code against known capabilities and constraints.</span></span> <span data-ttu-id="9415c-111">Se recomienda usar esta constante solo con los sombreadores que se hayan compilado correctamente en el pasado.</span><span class="sxs-lookup"><span data-stu-id="9415c-111">We recommend that you use this constant only with shaders that have been successfully compiled in the past.</span></span> <span data-ttu-id="9415c-112">DirectX siempre valida los sombreadores antes de que los establezca en un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9415c-112">DirectX always validates shaders before it sets them to a device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9415c-113"><span id="D3DCOMPILE_SKIP_OPTIMIZATION"></span><span id="d3dcompile_skip_optimization"></span>**D3DCOMPILE \_ omitir \_ optimización**</span><span class="sxs-lookup"><span data-stu-id="9415c-113"><span id="D3DCOMPILE_SKIP_OPTIMIZATION"></span><span id="d3dcompile_skip_optimization"></span>**D3DCOMPILE\_SKIP\_OPTIMIZATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9415c-114">(1 << 2)</span><span class="sxs-lookup"><span data-stu-id="9415c-114">(1 << 2)</span></span>
</dt> <dt>



<span data-ttu-id="9415c-115">Indica al compilador que omita los pasos de optimización durante la generación de código.</span><span class="sxs-lookup"><span data-stu-id="9415c-115">Directs the compiler to skip optimization steps during code generation.</span></span> <span data-ttu-id="9415c-116">Se recomienda establecer esta constante solo con fines de depuración.</span><span class="sxs-lookup"><span data-stu-id="9415c-116">We recommend that you set this constant for debug purposes only.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9415c-117"><span id="D3DCOMPILE_PACK_MATRIX_ROW_MAJOR"></span><span id="d3dcompile_pack_matrix_row_major"></span>**\_ \_ \_ Fila \_ principal de la matriz de D3DCOMPILE Pack**</span><span class="sxs-lookup"><span data-stu-id="9415c-117"><span id="D3DCOMPILE_PACK_MATRIX_ROW_MAJOR"></span><span id="d3dcompile_pack_matrix_row_major"></span>**D3DCOMPILE\_PACK\_MATRIX\_ROW\_MAJOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9415c-118">(1 << 3)</span><span class="sxs-lookup"><span data-stu-id="9415c-118">(1 << 3)</span></span>
</dt> <dt>



<span data-ttu-id="9415c-119">Indica al compilador que empaquete las matrices en orden de fila principal en la entrada y la salida del sombreador.</span><span class="sxs-lookup"><span data-stu-id="9415c-119">Directs the compiler to pack matrices in row-major order on input and output from the shader.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9415c-120"><span id="D3DCOMPILE_PACK_MATRIX_COLUMN_MAJOR"></span><span id="d3dcompile_pack_matrix_column_major"></span>**Columna de matriz de D3DCOMPILE \_ Pack \_ \_ \_ principal**</span><span class="sxs-lookup"><span data-stu-id="9415c-120"><span id="D3DCOMPILE_PACK_MATRIX_COLUMN_MAJOR"></span><span id="d3dcompile_pack_matrix_column_major"></span>**D3DCOMPILE\_PACK\_MATRIX\_COLUMN\_MAJOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9415c-121">(1 << 4)</span><span class="sxs-lookup"><span data-stu-id="9415c-121">(1 << 4)</span></span>
</dt> <dt>



<span data-ttu-id="9415c-122">Indica al compilador que empaquete las matrices en el orden principal de la columna en la entrada y la salida del sombreador.</span><span class="sxs-lookup"><span data-stu-id="9415c-122">Directs the compiler to pack matrices in column-major order on input and output from the shader.</span></span> <span data-ttu-id="9415c-123">Este tipo de empaquetado suele ser más eficaz porque una serie de productos punto puede realizar la multiplicación de matrices vectoriales.</span><span class="sxs-lookup"><span data-stu-id="9415c-123">This type of packing is generally more efficient because a series of dot-products can then perform vector-matrix multiplication.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9415c-124"><span id="D3DCOMPILE_PARTIAL_PRECISION"></span><span id="d3dcompile_partial_precision"></span>**\_Precisión parcial de D3DCOMPILE \_**</span><span class="sxs-lookup"><span data-stu-id="9415c-124"><span id="D3DCOMPILE_PARTIAL_PRECISION"></span><span id="d3dcompile_partial_precision"></span>**D3DCOMPILE\_PARTIAL\_PRECISION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9415c-125">(1 << 5)</span><span class="sxs-lookup"><span data-stu-id="9415c-125">(1 << 5)</span></span>
</dt> <dt>



<span data-ttu-id="9415c-126">Indica al compilador que realice todos los cálculos con precisión parcial.</span><span class="sxs-lookup"><span data-stu-id="9415c-126">Directs the compiler to perform all computations with partial precision.</span></span> <span data-ttu-id="9415c-127">Si establece esta constante, el código compilado puede ejecutarse más rápido en el hardware.</span><span class="sxs-lookup"><span data-stu-id="9415c-127">If you set this constant, the compiled code might run faster on some hardware.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9415c-128"><span id="D3DCOMPILE_FORCE_VS_SOFTWARE_NO_OPT"></span><span id="d3dcompile_force_vs_software_no_opt"></span>**D3DCOMPILE \_ Force \_ vs \_ software \_ no \_ OPT**</span><span class="sxs-lookup"><span data-stu-id="9415c-128"><span id="D3DCOMPILE_FORCE_VS_SOFTWARE_NO_OPT"></span><span id="d3dcompile_force_vs_software_no_opt"></span>**D3DCOMPILE\_FORCE\_VS\_SOFTWARE\_NO\_OPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9415c-129">(1 << 6)</span><span class="sxs-lookup"><span data-stu-id="9415c-129">(1 << 6)</span></span>
</dt> <dt>



<span data-ttu-id="9415c-130">Indica al compilador que compile un sombreador de vértices para el siguiente perfil de sombreador más alto.</span><span class="sxs-lookup"><span data-stu-id="9415c-130">Directs the compiler to compile a vertex shader for the next highest shader profile.</span></span> <span data-ttu-id="9415c-131">Esta constante activa y desactiva la depuración.</span><span class="sxs-lookup"><span data-stu-id="9415c-131">This constant turns debugging on and optimizations off.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9415c-132"><span id="D3DCOMPILE_FORCE_PS_SOFTWARE_NO_OPT"></span><span id="d3dcompile_force_ps_software_no_opt"></span>**D3DCOMPILE \_ Force \_ PS \_ software \_ no \_ OPT**</span><span class="sxs-lookup"><span data-stu-id="9415c-132"><span id="D3DCOMPILE_FORCE_PS_SOFTWARE_NO_OPT"></span><span id="d3dcompile_force_ps_software_no_opt"></span>**D3DCOMPILE\_FORCE\_PS\_SOFTWARE\_NO\_OPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9415c-133">(1 << 7)</span><span class="sxs-lookup"><span data-stu-id="9415c-133">(1 << 7)</span></span>
</dt> <dt>



<span data-ttu-id="9415c-134">Indica al compilador que compile un sombreador de píxeles para el siguiente perfil del sombreador más alto.</span><span class="sxs-lookup"><span data-stu-id="9415c-134">Directs the compiler to compile a pixel shader for the next highest shader profile.</span></span> <span data-ttu-id="9415c-135">Esta constante también activa y desactiva la depuración.</span><span class="sxs-lookup"><span data-stu-id="9415c-135">This constant also turns debugging on and optimizations off.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9415c-136"><span id="D3DCOMPILE_NO_PRESHADER"></span><span id="d3dcompile_no_preshader"></span>**D3DCOMPILE \_ sin \_ sombreador**</span><span class="sxs-lookup"><span data-stu-id="9415c-136"><span id="D3DCOMPILE_NO_PRESHADER"></span><span id="d3dcompile_no_preshader"></span>**D3DCOMPILE\_NO\_PRESHADER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9415c-137">(1 << 8)</span><span class="sxs-lookup"><span data-stu-id="9415c-137">(1 << 8)</span></span>
</dt> <dt>



<span data-ttu-id="9415c-138">Indica al compilador que deshabilite los sombreadores.</span><span class="sxs-lookup"><span data-stu-id="9415c-138">Directs the compiler to disable Preshaders.</span></span> <span data-ttu-id="9415c-139">Si establece esta constante, el compilador no extrae la expresión estática para la evaluación.</span><span class="sxs-lookup"><span data-stu-id="9415c-139">If you set this constant, the compiler does not pull out static expression for evaluation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9415c-140"><span id="D3DCOMPILE_AVOID_FLOW_CONTROL"></span><span id="d3dcompile_avoid_flow_control"></span>**D3DCOMPILE \_ evitar \_ el \_ control de flujo**</span><span class="sxs-lookup"><span data-stu-id="9415c-140"><span id="D3DCOMPILE_AVOID_FLOW_CONTROL"></span><span id="d3dcompile_avoid_flow_control"></span>**D3DCOMPILE\_AVOID\_FLOW\_CONTROL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9415c-141">(1 << 9)</span><span class="sxs-lookup"><span data-stu-id="9415c-141">(1 << 9)</span></span>
</dt> <dt>



<span data-ttu-id="9415c-142">Indica al compilador que no use construcciones de control de flujo siempre que sea posible.</span><span class="sxs-lookup"><span data-stu-id="9415c-142">Directs the compiler to not use flow-control constructs where possible.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9415c-143"><span id="D3DCOMPILE_PREFER_FLOW_CONTROL"></span><span id="d3dcompile_prefer_flow_control"></span>**D3DCOMPILE \_ preferida ( \_ control de flujo) \_**</span><span class="sxs-lookup"><span data-stu-id="9415c-143"><span id="D3DCOMPILE_PREFER_FLOW_CONTROL"></span><span id="d3dcompile_prefer_flow_control"></span>**D3DCOMPILE\_PREFER\_FLOW\_CONTROL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9415c-144">(1 << 10)</span><span class="sxs-lookup"><span data-stu-id="9415c-144">(1 << 10)</span></span>
</dt> <dt>



<span data-ttu-id="9415c-145">Indica al compilador que use construcciones de control de flujo siempre que sea posible.</span><span class="sxs-lookup"><span data-stu-id="9415c-145">Directs the compiler to use flow-control constructs where possible.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9415c-146"><span id="D3DCOMPILE_ENABLE_STRICTNESS"></span><span id="d3dcompile_enable_strictness"></span>**D3DCOMPILE \_ Habilitar la \_ rigurosidad**</span><span class="sxs-lookup"><span data-stu-id="9415c-146"><span id="D3DCOMPILE_ENABLE_STRICTNESS"></span><span id="d3dcompile_enable_strictness"></span>**D3DCOMPILE\_ENABLE\_STRICTNESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9415c-147">(1 << 11)</span><span class="sxs-lookup"><span data-stu-id="9415c-147">(1 << 11)</span></span>
</dt> <dt>



<span data-ttu-id="9415c-148">Fuerza la compilación estricta, que podría no permitir la sintaxis heredada.</span><span class="sxs-lookup"><span data-stu-id="9415c-148">Forces strict compile, which might not allow for legacy syntax.</span></span>

<span data-ttu-id="9415c-149">De forma predeterminada, el compilador deshabilita la rigurosidad en la sintaxis desusada.</span><span class="sxs-lookup"><span data-stu-id="9415c-149">By default, the compiler disables strictness on deprecated syntax.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9415c-150"><span id="D3DCOMPILE_ENABLE_BACKWARDS_COMPATIBILITY"></span><span id="d3dcompile_enable_backwards_compatibility"></span>**D3DCOMPILE \_ habilitar \_ compatibilidad con versiones anteriores \_**</span><span class="sxs-lookup"><span data-stu-id="9415c-150"><span id="D3DCOMPILE_ENABLE_BACKWARDS_COMPATIBILITY"></span><span id="d3dcompile_enable_backwards_compatibility"></span>**D3DCOMPILE\_ENABLE\_BACKWARDS\_COMPATIBILITY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9415c-151">(1 << 12)</span><span class="sxs-lookup"><span data-stu-id="9415c-151">(1 << 12)</span></span>
</dt> <dt>



<span data-ttu-id="9415c-152">Indica al compilador que permita a los sombreadores más antiguos compilar en 5 \_ 0 destinos.</span><span class="sxs-lookup"><span data-stu-id="9415c-152">Directs the compiler to enable older shaders to compile to 5\_0 targets.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9415c-153"><span id="D3DCOMPILE_IEEE_STRICTNESS"></span><span id="d3dcompile_ieee_strictness"></span>**\_Restricción IEEE \_ D3DCOMPILE**</span><span class="sxs-lookup"><span data-stu-id="9415c-153"><span id="D3DCOMPILE_IEEE_STRICTNESS"></span><span id="d3dcompile_ieee_strictness"></span>**D3DCOMPILE\_IEEE\_STRICTNESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9415c-154">(1 << 13)</span><span class="sxs-lookup"><span data-stu-id="9415c-154">(1 << 13)</span></span>
</dt> <dt>



<span data-ttu-id="9415c-155">Fuerza la compilación IEEE STRICT.</span><span class="sxs-lookup"><span data-stu-id="9415c-155">Forces the IEEE strict compile.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9415c-156"><span id="D3DCOMPILE_OPTIMIZATION_LEVEL0"></span><span id="d3dcompile_optimization_level0"></span>**D3DCOMPILE \_ optimización de \_ LEVEL0**</span><span class="sxs-lookup"><span data-stu-id="9415c-156"><span id="D3DCOMPILE_OPTIMIZATION_LEVEL0"></span><span id="d3dcompile_optimization_level0"></span>**D3DCOMPILE\_OPTIMIZATION\_LEVEL0**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9415c-157">(1 << 14)</span><span class="sxs-lookup"><span data-stu-id="9415c-157">(1 << 14)</span></span>
</dt> <dt>



<span data-ttu-id="9415c-158">Indica al compilador que use el nivel de optimización más bajo.</span><span class="sxs-lookup"><span data-stu-id="9415c-158">Directs the compiler to use the lowest optimization level.</span></span> <span data-ttu-id="9415c-159">Si establece esta constante, el compilador puede generar código más lento, pero genera el código más rápidamente.</span><span class="sxs-lookup"><span data-stu-id="9415c-159">If you set this constant, the compiler might produce slower code but produces the code more quickly.</span></span> <span data-ttu-id="9415c-160">Establezca esta constante cuando desarrolle el sombreador de forma iterativa.</span><span class="sxs-lookup"><span data-stu-id="9415c-160">Set this constant when you develop the shader iteratively.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9415c-161"><span id="D3DCOMPILE_OPTIMIZATION_LEVEL1"></span><span id="d3dcompile_optimization_level1"></span>**D3DCOMPILE \_ optimización de \_ Level1**</span><span class="sxs-lookup"><span data-stu-id="9415c-161"><span id="D3DCOMPILE_OPTIMIZATION_LEVEL1"></span><span id="d3dcompile_optimization_level1"></span>**D3DCOMPILE\_OPTIMIZATION\_LEVEL1**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9415c-162">0</span><span class="sxs-lookup"><span data-stu-id="9415c-162">0</span></span>
</dt> <dt>



<span data-ttu-id="9415c-163">Indica al compilador que use el segundo nivel de optimización más bajo.</span><span class="sxs-lookup"><span data-stu-id="9415c-163">Directs the compiler to use the second lowest optimization level.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9415c-164"><span id="D3DCOMPILE_OPTIMIZATION_LEVEL2"></span><span id="d3dcompile_optimization_level2"></span>**D3DCOMPILE \_ optimización de \_ LEVEL2**</span><span class="sxs-lookup"><span data-stu-id="9415c-164"><span id="D3DCOMPILE_OPTIMIZATION_LEVEL2"></span><span id="d3dcompile_optimization_level2"></span>**D3DCOMPILE\_OPTIMIZATION\_LEVEL2**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9415c-165">((1 << 14) \| (1 << 15))</span><span class="sxs-lookup"><span data-stu-id="9415c-165">((1 << 14) \| (1 << 15))</span></span>
</dt> <dt>



<span data-ttu-id="9415c-166">Indica al compilador que use el segundo nivel de optimización más alto.</span><span class="sxs-lookup"><span data-stu-id="9415c-166">Directs the compiler to use the second highest optimization level.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9415c-167"><span id="D3DCOMPILE_OPTIMIZATION_LEVEL3"></span><span id="d3dcompile_optimization_level3"></span>**D3DCOMPILE \_ optimización de \_ level3**</span><span class="sxs-lookup"><span data-stu-id="9415c-167"><span id="D3DCOMPILE_OPTIMIZATION_LEVEL3"></span><span id="d3dcompile_optimization_level3"></span>**D3DCOMPILE\_OPTIMIZATION\_LEVEL3**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9415c-168">(1 << 15)</span><span class="sxs-lookup"><span data-stu-id="9415c-168">(1 << 15)</span></span>
</dt> <dt>



<span data-ttu-id="9415c-169">Indica al compilador que use el nivel de optimización más alto.</span><span class="sxs-lookup"><span data-stu-id="9415c-169">Directs the compiler to use the highest optimization level.</span></span> <span data-ttu-id="9415c-170">Si establece esta constante, el compilador genera el mejor código posible, pero podría tardar mucho más tiempo en hacerlo.</span><span class="sxs-lookup"><span data-stu-id="9415c-170">If you set this constant, the compiler produces the best possible code but might take significantly longer to do so.</span></span> <span data-ttu-id="9415c-171">Establezca esta constante para las compilaciones finales de una aplicación cuando el rendimiento sea el factor más importante.</span><span class="sxs-lookup"><span data-stu-id="9415c-171">Set this constant for final builds of an application when performance is the most important factor.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9415c-172"><span id="D3DCOMPILE_WARNINGS_ARE_ERRORS"></span><span id="d3dcompile_warnings_are_errors"></span>**Las \_ advertencias de D3DCOMPILE \_ son \_ errores**</span><span class="sxs-lookup"><span data-stu-id="9415c-172"><span id="D3DCOMPILE_WARNINGS_ARE_ERRORS"></span><span id="d3dcompile_warnings_are_errors"></span>**D3DCOMPILE\_WARNINGS\_ARE\_ERRORS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9415c-173">(1 << 18)</span><span class="sxs-lookup"><span data-stu-id="9415c-173">(1 << 18)</span></span>
</dt> <dt>



<span data-ttu-id="9415c-174">Indica al compilador que trate todas las advertencias como errores al compilar el código del sombreador.</span><span class="sxs-lookup"><span data-stu-id="9415c-174">Directs the compiler to treat all warnings as errors when it compiles the shader code.</span></span> <span data-ttu-id="9415c-175">Se recomienda usar esta constante para el nuevo código de sombreador, de modo que pueda resolver todas las advertencias y reducir el número de defectos de código difíciles de encontrar.</span><span class="sxs-lookup"><span data-stu-id="9415c-175">We recommend that you use this constant for new shader code, so that you can resolve all warnings and lower the number of hard-to-find code defects.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9415c-176"><span id="D3DCOMPILE_RESOURCES_MAY_ALIAS"></span><span id="d3dcompile_resources_may_alias"></span>**\_Los recursos de D3DCOMPILE \_ pueden tener \_ alias**</span><span class="sxs-lookup"><span data-stu-id="9415c-176"><span id="D3DCOMPILE_RESOURCES_MAY_ALIAS"></span><span id="d3dcompile_resources_may_alias"></span>**D3DCOMPILE\_RESOURCES\_MAY\_ALIAS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9415c-177">(1 << 19)</span><span class="sxs-lookup"><span data-stu-id="9415c-177">(1 << 19)</span></span>
</dt> <dt>



<span data-ttu-id="9415c-178">Indica al compilador que asuma que las vistas de acceso desordenados (UAVs) y las vistas de recursos del sombreador (SRVs) pueden tener alias para CS \_ 5 \_ 0.</span><span class="sxs-lookup"><span data-stu-id="9415c-178">Directs the compiler to assume that unordered access views (UAVs) and shader resource views (SRVs) may alias for cs\_5\_0.</span></span>

> [!Note]  
> <span data-ttu-id="9415c-179">Esta constante del compilador es nueva empezando por el \_47.dll D3dcompiler.</span><span class="sxs-lookup"><span data-stu-id="9415c-179">This compiler constant is new starting with the D3dcompiler\_47.dll.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="9415c-180"><span id="D3DCOMPILE_ENABLE_UNBOUNDED_DESCRIPTOR_TABLES"></span><span id="d3dcompile_enable_unbounded_descriptor_tables"></span>**D3DCOMPILE \_ habilitar \_ \_ tablas de DESCRIPTOres sin enlazar \_**</span><span class="sxs-lookup"><span data-stu-id="9415c-180"><span id="D3DCOMPILE_ENABLE_UNBOUNDED_DESCRIPTOR_TABLES"></span><span id="d3dcompile_enable_unbounded_descriptor_tables"></span>**D3DCOMPILE\_ENABLE\_UNBOUNDED\_DESCRIPTOR\_TABLES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9415c-181">(1 << 20)</span><span class="sxs-lookup"><span data-stu-id="9415c-181">(1 << 20)</span></span>
</dt> <dt>



<span data-ttu-id="9415c-182">Indica al compilador que habilite las tablas de descriptores sin enlazar.</span><span class="sxs-lookup"><span data-stu-id="9415c-182">Directs the compiler to enable unbounded descriptor tables.</span></span>

> [!Note]  
> <span data-ttu-id="9415c-183">Esta constante del compilador es nueva empezando por el \_47.dll D3dcompiler.</span><span class="sxs-lookup"><span data-stu-id="9415c-183">This compiler constant is new starting with the D3dcompiler\_47.dll.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="9415c-184"><span id="D3DCOMPILE_ALL_RESOURCES_BOUND"></span><span id="d3dcompile_all_resources_bound"></span>**D3DCOMPILE \_ todos \_ los recursos \_ enlazados**</span><span class="sxs-lookup"><span data-stu-id="9415c-184"><span id="D3DCOMPILE_ALL_RESOURCES_BOUND"></span><span id="d3dcompile_all_resources_bound"></span>**D3DCOMPILE\_ALL\_RESOURCES\_BOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9415c-185">(1 << 21)</span><span class="sxs-lookup"><span data-stu-id="9415c-185">(1 << 21)</span></span>
</dt> <dt>



<span data-ttu-id="9415c-186">Dirige el compilador para asegurarse de que todos los recursos están enlazados.</span><span class="sxs-lookup"><span data-stu-id="9415c-186">Directs the compiler to ensure all resources are bound.</span></span>

> [!Note]  
> <span data-ttu-id="9415c-187">Esta constante del compilador es nueva empezando por el \_47.dll D3dcompiler.</span><span class="sxs-lookup"><span data-stu-id="9415c-187">This compiler constant is new starting with the D3dcompiler\_47.dll.</span></span>

 


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9415c-188">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9415c-188">Requirements</span></span>



| <span data-ttu-id="9415c-189">Requisito</span><span class="sxs-lookup"><span data-stu-id="9415c-189">Requirement</span></span> | <span data-ttu-id="9415c-190">Value</span><span class="sxs-lookup"><span data-stu-id="9415c-190">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="9415c-191">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9415c-191">Header</span></span><br/> | <dl> <span data-ttu-id="9415c-192"><dt>D3DCompiler. h</dt></span><span class="sxs-lookup"><span data-stu-id="9415c-192"><dt>D3DCompiler.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9415c-193">Vea también</span><span class="sxs-lookup"><span data-stu-id="9415c-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9415c-194">Constantes de D3DCompiler</span><span class="sxs-lookup"><span data-stu-id="9415c-194">D3DCompiler Constants</span></span>](dx-graphics-d3dcompiler-reference-constants.md)
</dt> </dl>

 

 





