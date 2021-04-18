---
title: Especificar destinos del compilador
description: Aquí se enumeran los destinos para varios perfiles que admiten las funciones D3DCompile y el compilador de HLSL.
ms.assetid: 594E1C14-C1D4-4207-91A1-28892CE6D821
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d68fc6c5a202ad537b02a20846d36526533240f3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421349"
---
# <a name="specifying-compiler-targets"></a><span data-ttu-id="a70b8-103">Especificar destinos del compilador</span><span class="sxs-lookup"><span data-stu-id="a70b8-103">Specifying Compiler Targets</span></span>

<span data-ttu-id="a70b8-104">Debe especificar el destino del sombreador (conjunto de características del sombreador) para compilar con cuando llame a la función [**D3DCompile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile), [**D3DCompile2**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile2)o [**D3DCompileFromFile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompilefromfile) .</span><span class="sxs-lookup"><span data-stu-id="a70b8-104">You need to specify the shader target — set of shader features — to compile against when you call the [**D3DCompile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile), [**D3DCompile2**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile2), or [**D3DCompileFromFile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompilefromfile) function.</span></span> <span data-ttu-id="a70b8-105">Aquí se enumeran los destinos para varios perfiles que admiten las funciones **D3DCompile \*** y el compilador de HLSL.</span><span class="sxs-lookup"><span data-stu-id="a70b8-105">Here we list the targets for various profiles that the **D3DCompile\*** functions and the HLSL compiler support.</span></span>

-   [<span data-ttu-id="a70b8-106">Niveles de características de Direct3D 11,0 y 11,1</span><span class="sxs-lookup"><span data-stu-id="a70b8-106">Direct3D 11.0 and 11.1 feature levels</span></span>](#direct3d-110-and-111-feature-levels)
-   [<span data-ttu-id="a70b8-107">Nivel de características de Direct3D 10,1</span><span class="sxs-lookup"><span data-stu-id="a70b8-107">Direct3D 10.1 feature level</span></span>](#direct3d-101-feature-level)
-   [<span data-ttu-id="a70b8-108">Nivel de características de Direct3D 10,0</span><span class="sxs-lookup"><span data-stu-id="a70b8-108">Direct3D 10.0 feature level</span></span>](#direct3d-100-feature-level)
-   [<span data-ttu-id="a70b8-109">Niveles de características de Direct3D 9,1, 9,2 y 9,3</span><span class="sxs-lookup"><span data-stu-id="a70b8-109">Direct3D 9.1, 9.2, and 9.3 feature levels</span></span>](#direct3d-91-92-and-93-feature-levels)
-   [<span data-ttu-id="a70b8-110">Modelo de sombreador de Direct3D 9 heredado 3,0</span><span class="sxs-lookup"><span data-stu-id="a70b8-110">Legacy Direct3D 9 Shader Model 3.0</span></span>](#legacy-direct3d-9-shader-model-30)
-   [<span data-ttu-id="a70b8-111">Modelo de sombreador de Direct3D 9 heredado 2,0</span><span class="sxs-lookup"><span data-stu-id="a70b8-111">Legacy Direct3D 9 Shader Model 2.0</span></span>](#legacy-direct3d-9-shader-model-20)
-   [<span data-ttu-id="a70b8-112">Modelo 1. x del sombreador de Direct3D 9 heredado</span><span class="sxs-lookup"><span data-stu-id="a70b8-112">Legacy Direct3D 9 Shader Model 1.x</span></span>](#legacy-direct3d-9-shader-model-1x)
-   [<span data-ttu-id="a70b8-113">Efectos heredados</span><span class="sxs-lookup"><span data-stu-id="a70b8-113">Legacy Effects</span></span>](#legacy-effects)
-   [<span data-ttu-id="a70b8-114">Notas</span><span class="sxs-lookup"><span data-stu-id="a70b8-114">Notes</span></span>](#notes)
-   [<span data-ttu-id="a70b8-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a70b8-115">Related topics</span></span>](#related-topics)

## <a name="direct3d-110-and-111-feature-levels"></a><span data-ttu-id="a70b8-116">Niveles de características de Direct3D 11,0 y 11,1</span><span class="sxs-lookup"><span data-stu-id="a70b8-116">Direct3D 11.0 and 11.1 feature levels</span></span>

<span data-ttu-id="a70b8-117">Estos son los destinos del sombreador que admiten [los niveles de características](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) de Direct3D 11,0 y 11,1.</span><span class="sxs-lookup"><span data-stu-id="a70b8-117">Here are the shader targets that Direct3D 11.0 and 11.1 [feature levels](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) support.</span></span>



| <span data-ttu-id="a70b8-118">Destino</span><span class="sxs-lookup"><span data-stu-id="a70b8-118">Target</span></span>   | <span data-ttu-id="a70b8-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="a70b8-119">Description</span></span>                                                                                                              |
|----------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a70b8-120">CS \_ 5 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a70b8-120">cs\_5\_0</span></span> | <span data-ttu-id="a70b8-121">DirectCompute 5,0 ([sombreador de cálculo](/windows/desktop/direct3d11/direct3d-11-advanced-stages-compute-shader))</span><span class="sxs-lookup"><span data-stu-id="a70b8-121">DirectCompute 5.0 ([compute shader](/windows/desktop/direct3d11/direct3d-11-advanced-stages-compute-shader))</span></span>                              |
| <span data-ttu-id="a70b8-122">DS \_ 5 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a70b8-122">ds\_5\_0</span></span> | [<span data-ttu-id="a70b8-123">Sombreador de dominios</span><span class="sxs-lookup"><span data-stu-id="a70b8-123">Domain shader</span></span>](/windows/desktop/direct3d11/direct3d-11-advanced-stages-tessellation)             |
| <span data-ttu-id="a70b8-124">GS \_ 5 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a70b8-124">gs\_5\_0</span></span> | <span data-ttu-id="a70b8-125">[Sombreador de geometría](/previous-versions//bb205146(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a70b8-125">[Geometry shader](/previous-versions//bb205146(v=vs.85))</span></span> |
| <span data-ttu-id="a70b8-126">HS \_ 5 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a70b8-126">hs\_5\_0</span></span> | [<span data-ttu-id="a70b8-127">Sombreador de casco</span><span class="sxs-lookup"><span data-stu-id="a70b8-127">Hull shader</span></span>](/windows/desktop/direct3d11/direct3d-11-advanced-stages-tessellation)                   |
| <span data-ttu-id="a70b8-128">PS \_ 5 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a70b8-128">ps\_5\_0</span></span> | <span data-ttu-id="a70b8-129">[Sombreador de píxeles](/previous-versions//bb205146(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a70b8-129">[Pixel shader](/previous-versions//bb205146(v=vs.85))</span></span>          |
| <span data-ttu-id="a70b8-130">vs \_ 5 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a70b8-130">vs\_5\_0</span></span> | <span data-ttu-id="a70b8-131">[Sombreador de vértices](/previous-versions//bb205146(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a70b8-131">[Vertex shader](/previous-versions//bb205146(v=vs.85))</span></span>       |



 

## <a name="direct3d-101-feature-level"></a><span data-ttu-id="a70b8-132">Nivel de características de Direct3D 10,1</span><span class="sxs-lookup"><span data-stu-id="a70b8-132">Direct3D 10.1 feature level</span></span>

<span data-ttu-id="a70b8-133">Estos son los destinos del sombreador que admite el [nivel de características](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) de Direct3D 10,1.</span><span class="sxs-lookup"><span data-stu-id="a70b8-133">Here are the shader targets that the Direct3D 10.1 [feature level](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) supports.</span></span>



| <span data-ttu-id="a70b8-134">Destino</span><span class="sxs-lookup"><span data-stu-id="a70b8-134">Target</span></span>   | <span data-ttu-id="a70b8-135">Descripción</span><span class="sxs-lookup"><span data-stu-id="a70b8-135">Description</span></span>                                                                                                              |
|----------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a70b8-136">CS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="a70b8-136">cs\_4\_1</span></span> | <span data-ttu-id="a70b8-137">DirectCompute 4,1 ([sombreador de cálculo](/windows/desktop/direct3d11/direct3d-11-advanced-stages-compute-shader)) ¹</span><span class="sxs-lookup"><span data-stu-id="a70b8-137">DirectCompute 4.1 ([compute shader](/windows/desktop/direct3d11/direct3d-11-advanced-stages-compute-shader))¹</span></span>                             |
| <span data-ttu-id="a70b8-138">GS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="a70b8-138">gs\_4\_1</span></span> | <span data-ttu-id="a70b8-139">[Sombreador de geometría](/previous-versions//bb205146(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a70b8-139">[Geometry shader](/previous-versions//bb205146(v=vs.85))</span></span> |
| <span data-ttu-id="a70b8-140">PS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="a70b8-140">ps\_4\_1</span></span> | <span data-ttu-id="a70b8-141">[Sombreador de píxeles](/previous-versions//bb205146(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a70b8-141">[Pixel shader](/previous-versions//bb205146(v=vs.85))</span></span>          |
| <span data-ttu-id="a70b8-142">vs \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="a70b8-142">vs\_4\_1</span></span> | <span data-ttu-id="a70b8-143">[Sombreador de vértices](/previous-versions//bb205146(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a70b8-143">[Vertex shader](/previous-versions//bb205146(v=vs.85))</span></span>       |



 

## <a name="direct3d-100-feature-level"></a><span data-ttu-id="a70b8-144">Nivel de características de Direct3D 10,0</span><span class="sxs-lookup"><span data-stu-id="a70b8-144">Direct3D 10.0 feature level</span></span>

<span data-ttu-id="a70b8-145">Estos son los destinos del sombreador que admite el [nivel de características](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) de Direct3D 10,0.</span><span class="sxs-lookup"><span data-stu-id="a70b8-145">Here are the shader targets that the Direct3D 10.0 [feature level](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) supports.</span></span>



| <span data-ttu-id="a70b8-146">Destino</span><span class="sxs-lookup"><span data-stu-id="a70b8-146">Target</span></span>   | <span data-ttu-id="a70b8-147">Descripción</span><span class="sxs-lookup"><span data-stu-id="a70b8-147">Description</span></span>                                                                                                              |
|----------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a70b8-148">CS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a70b8-148">cs\_4\_0</span></span> | <span data-ttu-id="a70b8-149">DirectCompute 4,0 ([sombreador de cálculo](/windows/desktop/direct3d11/direct3d-11-advanced-stages-compute-shader)) ¹</span><span class="sxs-lookup"><span data-stu-id="a70b8-149">DirectCompute 4.0 ([compute shader](/windows/desktop/direct3d11/direct3d-11-advanced-stages-compute-shader))¹</span></span>                             |
| <span data-ttu-id="a70b8-150">GS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a70b8-150">gs\_4\_0</span></span> | <span data-ttu-id="a70b8-151">[Sombreador de geometría](/previous-versions//bb205146(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a70b8-151">[Geometry shader](/previous-versions//bb205146(v=vs.85))</span></span> |
| <span data-ttu-id="a70b8-152">PS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a70b8-152">ps\_4\_0</span></span> | <span data-ttu-id="a70b8-153">[Sombreador de píxeles](/previous-versions//bb205146(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a70b8-153">[Pixel shader](/previous-versions//bb205146(v=vs.85))</span></span>          |
| <span data-ttu-id="a70b8-154">vs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a70b8-154">vs\_4\_0</span></span> | <span data-ttu-id="a70b8-155">[Sombreador de vértices](/previous-versions//bb205146(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a70b8-155">[Vertex shader](/previous-versions//bb205146(v=vs.85))</span></span>       |



 

## <a name="direct3d-91-92-and-93-feature-levels"></a><span data-ttu-id="a70b8-156">Niveles de características de Direct3D 9,1, 9,2 y 9,3</span><span class="sxs-lookup"><span data-stu-id="a70b8-156">Direct3D 9.1, 9.2, and 9.3 feature levels</span></span>

<span data-ttu-id="a70b8-157">Estos son los destinos del sombreador que admiten [los niveles de características](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) de Direct3D 9,1, 9,2 y 9,3.</span><span class="sxs-lookup"><span data-stu-id="a70b8-157">Here are the shader targets that Direct3D 9.1, 9.2 and 9.3 [feature levels](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) support.</span></span>

> [!Note]  
> <span data-ttu-id="a70b8-158">Cuando se usan los \* \_ \_ perfiles del \_ \_ \_ sombreador HLSL de 4 0 nivel 9 x, se usan implícitamente los perfiles del [modelo de sombreador 2. x](dx-graphics-hlsl-sm2.md) para admitir el hardware compatible con Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="a70b8-158">When you use the \*\_4\_0\_level\_9\_x HLSL shader profiles, you implicitly use of the [Shader Model 2.x](dx-graphics-hlsl-sm2.md) profiles to support Direct3D 9 capable hardware.</span></span> <span data-ttu-id="a70b8-159">Los perfiles del modelo de sombreador 2. x admiten un comportamiento de control de flujo más limitado que los perfiles del [modelo de sombreador 4. x](dx-graphics-hlsl-sm4.md) y posteriores.</span><span class="sxs-lookup"><span data-stu-id="a70b8-159">Shader Model 2.x profiles support more limited flow control behavior than the [Shader Model 4.x](dx-graphics-hlsl-sm4.md) and later profiles.</span></span>

 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a70b8-160">Destino</span><span class="sxs-lookup"><span data-stu-id="a70b8-160">Target</span></span></th>
<th><span data-ttu-id="a70b8-161">Descripción</span><span class="sxs-lookup"><span data-stu-id="a70b8-161">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a70b8-162">ps_4_0_level_9_1</span><span class="sxs-lookup"><span data-stu-id="a70b8-162">ps_4_0_level_9_1</span></span></td>
<td><span data-ttu-id="a70b8-163">[Sombreador de píxeles](/previous-versions//bb205146(v=vs.85)) para 9,1 y 9,2 (límites similares a ps_2_0)</span><span class="sxs-lookup"><span data-stu-id="a70b8-163">[Pixel shader](/previous-versions//bb205146(v=vs.85)) for 9.1 and 9.2 (similar limits to ps_2_0)</span></span>
<ul>
<li><span data-ttu-id="a70b8-164">64 instrucciones de textura aritmética y 32</span><span class="sxs-lookup"><span data-stu-id="a70b8-164">64 arithmetic and 32 texture instructions</span></span></li>
<li><span data-ttu-id="a70b8-165">12 registros temporales</span><span class="sxs-lookup"><span data-stu-id="a70b8-165">12 temporary registers</span></span></li>
<li><span data-ttu-id="a70b8-166">4 niveles de lecturas dependientes</span><span class="sxs-lookup"><span data-stu-id="a70b8-166">4 levels of dependent reads</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a70b8-167">ps_4_0_level_9_3</span><span class="sxs-lookup"><span data-stu-id="a70b8-167">ps_4_0_level_9_3</span></span></td>
<td><span data-ttu-id="a70b8-168"><a href="/previous-versions//bb205146(v=vs.85)">Sombreador de píxeles</a> para 9,3 (límites similares a ps_2_x ² con características adicionales del sombreador)</span><span class="sxs-lookup"><span data-stu-id="a70b8-168"><a href="/previous-versions//bb205146(v=vs.85)">Pixel shader</a> for 9.3 (similar limits to ps_2_x² with additional shader features)</span></span>
<ul>
<li><span data-ttu-id="a70b8-169">512 instrucciones</span><span class="sxs-lookup"><span data-stu-id="a70b8-169">512 instructions</span></span></li>
<li><span data-ttu-id="a70b8-170">32 registros temporales</span><span class="sxs-lookup"><span data-stu-id="a70b8-170">32 temporary registers</span></span></li>
<li><span data-ttu-id="a70b8-171">Control de flujo estático (profundidad máxima de 4)</span><span class="sxs-lookup"><span data-stu-id="a70b8-171">Static flow control (max depth of 4)</span></span></li>
<li><span data-ttu-id="a70b8-172">Control de flujo dinámico (profundidad máxima de 24)</span><span class="sxs-lookup"><span data-stu-id="a70b8-172">Dynamic flow control (max depth of 24)</span></span></li>
<li><span data-ttu-id="a70b8-173">D3DPS20CAPS_ARBITRARYSWIZZLE</span><span class="sxs-lookup"><span data-stu-id="a70b8-173">D3DPS20CAPS_ARBITRARYSWIZZLE</span></span></li>
<li><span data-ttu-id="a70b8-174">D3DPS20CAPS_GRADIENTINSTRUCTIONS</span><span class="sxs-lookup"><span data-stu-id="a70b8-174">D3DPS20CAPS_GRADIENTINSTRUCTIONS</span></span></li>
<li><span data-ttu-id="a70b8-175">D3DPS20CAPS_PREDICATION</span><span class="sxs-lookup"><span data-stu-id="a70b8-175">D3DPS20CAPS_PREDICATION</span></span></li>
<li><span data-ttu-id="a70b8-176">D3DPS20CAPS_NODEPENDENTREADLIMIT</span><span class="sxs-lookup"><span data-stu-id="a70b8-176">D3DPS20CAPS_NODEPENDENTREADLIMIT</span></span></li>
<li><span data-ttu-id="a70b8-177">D3DPS20CAPS_NOTEXINSTRUCTIONLIMIT</span><span class="sxs-lookup"><span data-stu-id="a70b8-177">D3DPS20CAPS_NOTEXINSTRUCTIONLIMIT</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a70b8-178">vs_4_0_level_9_1</span><span class="sxs-lookup"><span data-stu-id="a70b8-178">vs_4_0_level_9_1</span></span></td>
<td><span data-ttu-id="a70b8-179"><a href="/previous-versions//bb205146(v=vs.85)">Sombreador de vértices</a> para 9,1 y 9,2 (similar a vs_2_0)</span><span class="sxs-lookup"><span data-stu-id="a70b8-179"><a href="/previous-versions//bb205146(v=vs.85)">Vertex shader</a> for 9.1 and 9.2 (similar to vs_2_0)</span></span>
<ul>
<li><span data-ttu-id="a70b8-180">256 instrucciones</span><span class="sxs-lookup"><span data-stu-id="a70b8-180">256 instructions</span></span></li>
<li><span data-ttu-id="a70b8-181">12 registros temporales</span><span class="sxs-lookup"><span data-stu-id="a70b8-181">12 temporary registers</span></span></li>
<li><span data-ttu-id="a70b8-182">Control de flujo estático (profundidad máxima de 1)</span><span class="sxs-lookup"><span data-stu-id="a70b8-182">Static flow control (max depth of 1)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a70b8-183">vs_4_0_level_9_3</span><span class="sxs-lookup"><span data-stu-id="a70b8-183">vs_4_0_level_9_3</span></span></td>
<td><span data-ttu-id="a70b8-184"><a href="/previous-versions//bb205146(v=vs.85)">Sombreador de vértices</a> para 9,3 (similar a vs_2_a ² con características adicionales del sombreador y creación de instancias)</span><span class="sxs-lookup"><span data-stu-id="a70b8-184"><a href="/previous-versions//bb205146(v=vs.85)">Vertex shader</a> for 9.3 (similar to vs_2_a² with additional shader features and instancing)</span></span>
<ul>
<li><span data-ttu-id="a70b8-185">256 instrucciones</span><span class="sxs-lookup"><span data-stu-id="a70b8-185">256 instructions</span></span></li>
<li><span data-ttu-id="a70b8-186">32 registros temporales</span><span class="sxs-lookup"><span data-stu-id="a70b8-186">32 temporary registers</span></span></li>
<li><span data-ttu-id="a70b8-187">Control de flujo estático (profundidad máxima de 4)</span><span class="sxs-lookup"><span data-stu-id="a70b8-187">Static flow control (max depth of 4)</span></span></li>
<li><span data-ttu-id="a70b8-188">D3DVS20CAPS_PREDICATION</span><span class="sxs-lookup"><span data-stu-id="a70b8-188">D3DVS20CAPS_PREDICATION</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="legacy-direct3d-9-shader-model-30"></a><span data-ttu-id="a70b8-189">Modelo de sombreador de Direct3D 9 heredado 3,0</span><span class="sxs-lookup"><span data-stu-id="a70b8-189">Legacy Direct3D 9 Shader Model 3.0</span></span>

<span data-ttu-id="a70b8-190">Estos son los destinos del sombreador para el modelo de sombreador de Direct3D 9 heredado 3,0 ³.</span><span class="sxs-lookup"><span data-stu-id="a70b8-190">Here are the shader targets for legacy Direct3D 9 shader model 3.0³.</span></span>



| <span data-ttu-id="a70b8-191">Destino</span><span class="sxs-lookup"><span data-stu-id="a70b8-191">Target</span></span>    | <span data-ttu-id="a70b8-192">Descripción</span><span class="sxs-lookup"><span data-stu-id="a70b8-192">Description</span></span>                                                                                                                       |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a70b8-193">PS \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a70b8-193">ps\_3\_0</span></span>  | <span data-ttu-id="a70b8-194">[Sombreador de píxeles](/previous-versions//bb205146(v=vs.85)) 3,0</span><span class="sxs-lookup"><span data-stu-id="a70b8-194">[Pixel shader](/previous-versions//bb205146(v=vs.85)) 3.0</span></span>               |
| <span data-ttu-id="a70b8-195">PS \_ 3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="a70b8-195">ps\_3\_sw</span></span> | <span data-ttu-id="a70b8-196">[Sombreador de píxeles](/previous-versions//bb205146(v=vs.85)) 3,0 (software)</span><span class="sxs-lookup"><span data-stu-id="a70b8-196">[Pixel shader](/previous-versions//bb205146(v=vs.85)) 3.0 (software)</span></span>    |
| <span data-ttu-id="a70b8-197">vs \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a70b8-197">vs\_3\_0</span></span>  | <span data-ttu-id="a70b8-198">[Sombreador de vértices](/previous-versions//bb205146(v=vs.85)) 3,0</span><span class="sxs-lookup"><span data-stu-id="a70b8-198">[Vertex shader](/previous-versions//bb205146(v=vs.85)) 3.0</span></span>            |
| <span data-ttu-id="a70b8-199">vs \_ 3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="a70b8-199">vs\_3\_sw</span></span> | <span data-ttu-id="a70b8-200">[Sombreador de vértices](/previous-versions//bb205146(v=vs.85)) 3,0 (software)</span><span class="sxs-lookup"><span data-stu-id="a70b8-200">[Vertex shader](/previous-versions//bb205146(v=vs.85)) 3.0 (software)</span></span> |



 

## <a name="legacy-direct3d-9-shader-model-20"></a><span data-ttu-id="a70b8-201">Modelo de sombreador de Direct3D 9 heredado 2,0</span><span class="sxs-lookup"><span data-stu-id="a70b8-201">Legacy Direct3D 9 Shader Model 2.0</span></span>

<span data-ttu-id="a70b8-202">Estos son los destinos del sombreador para el modelo de sombreador de Direct3D 9 heredado 2,0 ³.</span><span class="sxs-lookup"><span data-stu-id="a70b8-202">Here are the shader targets for legacy Direct3D 9 shader model 2.0³.</span></span>



| <span data-ttu-id="a70b8-203">Destino</span><span class="sxs-lookup"><span data-stu-id="a70b8-203">Target</span></span>    | <span data-ttu-id="a70b8-204">Descripción</span><span class="sxs-lookup"><span data-stu-id="a70b8-204">Description</span></span>                                                                                                                     |
|-----------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a70b8-205">PS \_ 2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a70b8-205">ps\_2\_0</span></span>  | <span data-ttu-id="a70b8-206">[Sombreador de píxeles](/previous-versions//bb205146(v=vs.85)) 2,0</span><span class="sxs-lookup"><span data-stu-id="a70b8-206">[Pixel shader](/previous-versions//bb205146(v=vs.85)) 2.0</span></span>             |
| <span data-ttu-id="a70b8-207">PS \_ 2 \_ a</span><span class="sxs-lookup"><span data-stu-id="a70b8-207">ps\_2\_a</span></span>  | <span data-ttu-id="a70b8-208">[Sombreador de píxeles](/previous-versions//bb205146(v=vs.85)) 2A</span><span class="sxs-lookup"><span data-stu-id="a70b8-208">[Pixel shader](/previous-versions//bb205146(v=vs.85)) 2a</span></span>              |
| <span data-ttu-id="a70b8-209">PS \_ 2 \_ b</span><span class="sxs-lookup"><span data-stu-id="a70b8-209">ps\_2\_b</span></span>  | <span data-ttu-id="a70b8-210">[Sombreador de píxeles](/previous-versions//bb205146(v=vs.85)) 2B</span><span class="sxs-lookup"><span data-stu-id="a70b8-210">[Pixel shader](/previous-versions//bb205146(v=vs.85)) 2b</span></span>              |
| <span data-ttu-id="a70b8-211">PS \_ 2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="a70b8-211">ps\_2\_sw</span></span> | <span data-ttu-id="a70b8-212">Software del [sombreador de píxeles](/previous-versions//bb205146(v=vs.85)) 2,0</span><span class="sxs-lookup"><span data-stu-id="a70b8-212">[Pixel shader](/previous-versions//bb205146(v=vs.85)) 2.0 software</span></span>    |
| <span data-ttu-id="a70b8-213">vs \_ 2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a70b8-213">vs\_2\_0</span></span>  | <span data-ttu-id="a70b8-214">[Sombreador de vértices](/previous-versions//bb205146(v=vs.85)) 2,0</span><span class="sxs-lookup"><span data-stu-id="a70b8-214">[Vertex shader](/previous-versions//bb205146(v=vs.85)) 2.0</span></span>          |
| <span data-ttu-id="a70b8-215">vs \_ 2 \_ a</span><span class="sxs-lookup"><span data-stu-id="a70b8-215">vs\_2\_a</span></span>  | <span data-ttu-id="a70b8-216">[Sombreador de vértices](/previous-versions//bb205146(v=vs.85)) 2A</span><span class="sxs-lookup"><span data-stu-id="a70b8-216">[Vertex shader](/previous-versions//bb205146(v=vs.85)) 2a</span></span>           |
| <span data-ttu-id="a70b8-217">vs \_ 2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="a70b8-217">vs\_2\_sw</span></span> | <span data-ttu-id="a70b8-218">Software del [sombreador de vértices](/previous-versions//bb205146(v=vs.85)) 2,0</span><span class="sxs-lookup"><span data-stu-id="a70b8-218">[Vertex shader](/previous-versions//bb205146(v=vs.85)) 2.0 software</span></span> |



 

## <a name="legacy-direct3d-9-shader-model-1x"></a><span data-ttu-id="a70b8-219">Modelo 1. x del sombreador de Direct3D 9 heredado</span><span class="sxs-lookup"><span data-stu-id="a70b8-219">Legacy Direct3D 9 Shader Model 1.x</span></span>

<span data-ttu-id="a70b8-220">Estos son los destinos del sombreador para el modelo de sombreador de Direct3D 9 heredado 1. x ⁴.</span><span class="sxs-lookup"><span data-stu-id="a70b8-220">Here are the shader targets for legacy Direct3D 9 shader model 1.x⁴.</span></span>



| <span data-ttu-id="a70b8-221">Destino</span><span class="sxs-lookup"><span data-stu-id="a70b8-221">Target</span></span>   | <span data-ttu-id="a70b8-222">Descripción</span><span class="sxs-lookup"><span data-stu-id="a70b8-222">Description</span></span>                                                                                                                                                                       |
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a70b8-223">TX \_ 1 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a70b8-223">tx\_1\_0</span></span> | <span data-ttu-id="a70b8-224">Perfil de sombreador de textura que hereda D3DX9 ⁵ Functions [**D3DXCreateTextureShader**](/windows/desktop/direct3d9/d3dxcreatetextureshader) y [**D3DXFillTextureTX**](/windows/desktop/direct3d9/d3dxfilltexturetx) use</span><span class="sxs-lookup"><span data-stu-id="a70b8-224">Texture shader profile that legacy D3DX9⁵ functions [**D3DXCreateTextureShader**](/windows/desktop/direct3d9/d3dxcreatetextureshader) and [**D3DXFillTextureTX**](/windows/desktop/direct3d9/d3dxfilltexturetx) use</span></span> |
| <span data-ttu-id="a70b8-225">vs \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="a70b8-225">vs\_1\_1</span></span> | <span data-ttu-id="a70b8-226">[Sombreador de vértices](/previous-versions//bb205146(v=vs.85)) 1,1</span><span class="sxs-lookup"><span data-stu-id="a70b8-226">[Vertex shader](/previous-versions//bb205146(v=vs.85)) 1.1</span></span>                                                            |



 

## <a name="legacy-effects"></a><span data-ttu-id="a70b8-227">Efectos heredados</span><span class="sxs-lookup"><span data-stu-id="a70b8-227">Legacy Effects</span></span>

<span data-ttu-id="a70b8-228">Estos son los objetivos de efecto de los efectos heredados.</span><span class="sxs-lookup"><span data-stu-id="a70b8-228">Here are the effect targets for legacy effects.</span></span>



| <span data-ttu-id="a70b8-229">Destino</span><span class="sxs-lookup"><span data-stu-id="a70b8-229">Target</span></span>   | <span data-ttu-id="a70b8-230">Descripción</span><span class="sxs-lookup"><span data-stu-id="a70b8-230">Description</span></span>                               |
|----------|-------------------------------------------|
| <span data-ttu-id="a70b8-231">FX \_ 2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a70b8-231">fx\_2\_0</span></span> | <span data-ttu-id="a70b8-232">Effects (FX) para Direct3D 9 en D3DX9 ⁵</span><span class="sxs-lookup"><span data-stu-id="a70b8-232">Effects (FX) for Direct3D 9 in D3DX9⁵</span></span>     |
| <span data-ttu-id="a70b8-233">FX \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a70b8-233">fx\_4\_0</span></span> | <span data-ttu-id="a70b8-234">Effects (FX) para Direct3D 10,0 en D3DX10 ⁵</span><span class="sxs-lookup"><span data-stu-id="a70b8-234">Effects (FX) for Direct3D 10.0 in D3DX10⁵</span></span> |
| <span data-ttu-id="a70b8-235">FX \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="a70b8-235">fx\_4\_1</span></span> | <span data-ttu-id="a70b8-236">Effects (FX) para Direct3D 10,1 en D3DX10 ⁵</span><span class="sxs-lookup"><span data-stu-id="a70b8-236">Effects (FX) for Direct3D 10.1 in D3DX10⁵</span></span> |
| <span data-ttu-id="a70b8-237">FX \_ 5 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a70b8-237">fx\_5\_0</span></span> | <span data-ttu-id="a70b8-238">Effects (FX) para Direct3D 11 ⁵</span><span class="sxs-lookup"><span data-stu-id="a70b8-238">Effects (FX) for Direct3D 11⁵</span></span>             |



 

## <a name="notes"></a><span data-ttu-id="a70b8-239">Notas</span><span class="sxs-lookup"><span data-stu-id="a70b8-239">Notes</span></span>

<span data-ttu-id="a70b8-240">A continuación se muestran algunas notas a las que se hace referencia en las secciones anteriores:</span><span class="sxs-lookup"><span data-stu-id="a70b8-240">Here are some notes that the preceding sections refer to:</span></span>

1.  <span data-ttu-id="a70b8-241">los dispositivos de [nivel de característica](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 10,0 y 10,1 pueden admitir opcionalmente DirectCompute.</span><span class="sxs-lookup"><span data-stu-id="a70b8-241">[feature level](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 10.0 and 10.1 devices can optionally support DirectCompute.</span></span> <span data-ttu-id="a70b8-242">Para comprobar la compatibilidad, use [**ID3D11Device:: CheckFeatureSupport**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-checkfeaturesupport) con [**\_ \_ \_ \_ \_ las opciones de hardware D3D10 X de la característica D3D11**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_feature).</span><span class="sxs-lookup"><span data-stu-id="a70b8-242">To verify support, use [**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-checkfeaturesupport) with [**D3D11\_FEATURE\_D3D10\_X\_HARDWARE\_OPTIONS**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_feature).</span></span>
2.  <span data-ttu-id="a70b8-243">el [nivel de características](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9,3 requiere de forma eficaz hardware que cumpla los requisitos del modelo de [sombreador de Direct3D 9 heredado 3,0](#legacy-direct3d-9-shader-model-30), pero este nivel de característica no hace uso de los destinos vs \_ 3 \_ 0 o PS \_ 3 \_ 0.</span><span class="sxs-lookup"><span data-stu-id="a70b8-243">[feature level](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9.3 effectively requires hardware that complies with the requirements for [legacy Direct3D 9 shader model 3.0](#legacy-direct3d-9-shader-model-30), but this feature level does not make use of vs\_3\_0 or ps\_3\_0 targets.</span></span>
3.  <span data-ttu-id="a70b8-244">Use solo modelos de sombreador de Direct3D 9 heredados con la API de Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="a70b8-244">Only use legacy Direct3D 9 shader models with the Direct3D 9 API.</span></span> <span data-ttu-id="a70b8-245">En su lugar, use los perfiles 9. x con la API Direct3D 10. x y 11. x.</span><span class="sxs-lookup"><span data-stu-id="a70b8-245">Instead, use the 9.x profiles with the Direct3D 10.x and 11.x API.</span></span>
4.  <span data-ttu-id="a70b8-246">Las funciones **D3DCompile \*** del sombreador de HLSL actuales no admiten los sombreadores de píxeles de 1. x heredados.</span><span class="sxs-lookup"><span data-stu-id="a70b8-246">The current HLSL shader **D3DCompile\*** functions don't support legacy 1.x pixel shaders.</span></span> <span data-ttu-id="a70b8-247">La última versión de HLSL para admitir estos destinos se D3DX9 en la versión de octubre de 2006 del SDK de DirectX.</span><span class="sxs-lookup"><span data-stu-id="a70b8-247">The last version of HLSL to support these targets was D3DX9 in the October 2006 release of the DirectX SDK.</span></span>
5.  <span data-ttu-id="a70b8-248">Todas las versiones de D3DX y el SDK de DirectX están en desuso.</span><span class="sxs-lookup"><span data-stu-id="a70b8-248">All versions of D3DX and the DirectX SDK are deprecated.</span></span> <span data-ttu-id="a70b8-249">Para obtener más información, vea [¿Dónde está el SDK de DirectX?](/windows/desktop/directx-sdk--august-2009-).</span><span class="sxs-lookup"><span data-stu-id="a70b8-249">For more info, see [Where is the DirectX SDK?](/windows/desktop/directx-sdk--august-2009-).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a70b8-250">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a70b8-250">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a70b8-251">Guía de programación para HLSL</span><span class="sxs-lookup"><span data-stu-id="a70b8-251">Programming Guide for HLSL</span></span>](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

 