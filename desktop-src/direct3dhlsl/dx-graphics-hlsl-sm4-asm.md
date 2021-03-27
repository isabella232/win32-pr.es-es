---
title: Ensamblado del modelo 4 del sombreador
description: Ensamblado del modelo 4 del sombreador
ms.assetid: 2896e195-b48b-4ce9-9421-f5fa40674b5e
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 20c7ff5d2a171228223d52db28d3bae6007068c5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075759"
---
# <a name="shader-model-4-assembly"></a><span data-ttu-id="c5b9c-103">Ensamblado del modelo 4 del sombreador</span><span class="sxs-lookup"><span data-stu-id="c5b9c-103">Shader Model 4 Assembly</span></span>

<span data-ttu-id="c5b9c-104">El modelo de sombreador 4 requiere la aplicación de sombreadores en HLSL.</span><span class="sxs-lookup"><span data-stu-id="c5b9c-104">Shader Model 4 requires you to program shaders in HLSL.</span></span> <span data-ttu-id="c5b9c-105">Sin embargo, el compilador del sombreador compila el código HLSL en el ensamblado que se ejecuta en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c5b9c-105">However, the shader compiler compiles the HLSL code into assembly that runs on the device.</span></span> <span data-ttu-id="c5b9c-106">Si usa PIX para Windows para depurar los sombreadores, puede elegir mostrar el código del sombreador en HLSL o en el ensamblado.</span><span class="sxs-lookup"><span data-stu-id="c5b9c-106">If you are using PIX for Windows to debug your shaders, you can choose to display shader code in either HLSL or assembly.</span></span> <span data-ttu-id="c5b9c-107">En esta sección se enumeran las instrucciones de ensamblado del modelo de sombreador 4 y 4,1 del modelo de sombreador que puede encontrarse al depurar un sombreador.</span><span class="sxs-lookup"><span data-stu-id="c5b9c-107">This section lists the Shader Model 4 and Shader Model 4.1 assembly instructions that you may encounter when debugging a shader.</span></span>

<dl>

[<span data-ttu-id="c5b9c-108">Modificadores de instrucciones</span><span class="sxs-lookup"><span data-stu-id="c5b9c-108">Instruction Modifiers</span></span>](instruction-modifiers.md)  
[<span data-ttu-id="c5b9c-109">add</span><span class="sxs-lookup"><span data-stu-id="c5b9c-109">add</span></span>](add--sm4---asm-.md)  
[<span data-ttu-id="c5b9c-110">and</span><span class="sxs-lookup"><span data-stu-id="c5b9c-110">and</span></span>](and--sm4---asm-.md)  
[<span data-ttu-id="c5b9c-111">break</span><span class="sxs-lookup"><span data-stu-id="c5b9c-111">break</span></span>](break--sm4---asm-.md)  
[<span data-ttu-id="c5b9c-112">breakc</span><span class="sxs-lookup"><span data-stu-id="c5b9c-112">breakc</span></span>](breakc--sm4---asm-.md)  
[<span data-ttu-id="c5b9c-113">call</span><span class="sxs-lookup"><span data-stu-id="c5b9c-113">call</span></span>](call--sm4---asm-.md)  
[<span data-ttu-id="c5b9c-114">callc</span><span class="sxs-lookup"><span data-stu-id="c5b9c-114">callc</span></span>](callc--sm4---asm-.md)  
[<span data-ttu-id="c5b9c-115">case</span><span class="sxs-lookup"><span data-stu-id="c5b9c-115">case</span></span>](case--sm4---asm-.md)  
[<span data-ttu-id="c5b9c-116">continue</span><span class="sxs-lookup"><span data-stu-id="c5b9c-116">continue</span></span>](continue--sm4---asm-.md)  
[<span data-ttu-id="c5b9c-117">continuec</span><span class="sxs-lookup"><span data-stu-id="c5b9c-117">continuec</span></span>](continuec--sm4---asm-.md)  
[<span data-ttu-id="c5b9c-118">límite</span><span class="sxs-lookup"><span data-stu-id="c5b9c-118">cut</span></span>](cut--sm4---asm-.md)  
[<span data-ttu-id="c5b9c-119">constantBuffer de DCL \_</span><span class="sxs-lookup"><span data-stu-id="c5b9c-119">dcl\_constantBuffer</span></span>](dcl-constantbuffer.md)  
[<span data-ttu-id="c5b9c-120">DCL \_ indicadores_globales</span><span class="sxs-lookup"><span data-stu-id="c5b9c-120">dcl\_globalFlags</span></span>](dcl-globalflags.md)  
[<span data-ttu-id="c5b9c-121">immediateConstantBuffer de DCL \_</span><span class="sxs-lookup"><span data-stu-id="c5b9c-121">dcl\_immediateConstantBuffer</span></span>](dcl-immediateconstantbuffer.md)  
[<span data-ttu-id="c5b9c-122">indexableTemp de DCL \_</span><span class="sxs-lookup"><span data-stu-id="c5b9c-122">dcl\_indexableTemp</span></span>](dcl-indexabletemp.md)  
[<span data-ttu-id="c5b9c-123">indexRange de DCL \_</span><span class="sxs-lookup"><span data-stu-id="c5b9c-123">dcl\_indexRange</span></span>](dcl-indexrange.md)  
[<span data-ttu-id="c5b9c-124">entrada de DCL \_</span><span class="sxs-lookup"><span data-stu-id="c5b9c-124">dcl\_input</span></span>](dcl-input.md)  
[<span data-ttu-id="c5b9c-125">\_SV de entrada de DCL \_</span><span class="sxs-lookup"><span data-stu-id="c5b9c-125">dcl\_input\_sv</span></span>](dcl-input-sv.md)  
[<span data-ttu-id="c5b9c-126">vPrim de entrada de DCL \_</span><span class="sxs-lookup"><span data-stu-id="c5b9c-126">dcl\_input vPrim</span></span>](dcl-input-vprim.md)  
[<span data-ttu-id="c5b9c-127">maxOutputVertexCount de DCL \_</span><span class="sxs-lookup"><span data-stu-id="c5b9c-127">dcl\_maxOutputVertexCount</span></span>](dcl-maxoutputvertexcount.md)  
[<span data-ttu-id="c5b9c-128">salida de DCL \_</span><span class="sxs-lookup"><span data-stu-id="c5b9c-128">dcl\_output</span></span>](dcl-output.md)  
[<span data-ttu-id="c5b9c-129">\_oDepth de salida de DCL \_</span><span class="sxs-lookup"><span data-stu-id="c5b9c-129">dcl\_output\_oDepth</span></span>](dcl-output-odepth.md)  
[<span data-ttu-id="c5b9c-130">\_SGV de salida de DCL \_</span><span class="sxs-lookup"><span data-stu-id="c5b9c-130">dcl\_output\_sgv</span></span>](dcl-output-sgv.md)  
[<span data-ttu-id="c5b9c-131">\_SIV de salida de DCL \_</span><span class="sxs-lookup"><span data-stu-id="c5b9c-131">dcl\_output\_siv</span></span>](dcl-output-siv.md)  
[<span data-ttu-id="c5b9c-132">outputTopology de DCL \_</span><span class="sxs-lookup"><span data-stu-id="c5b9c-132">dcl\_outputTopology</span></span>](dcl-outputtopology.md)  
[<span data-ttu-id="c5b9c-133">\_recurso DCL</span><span class="sxs-lookup"><span data-stu-id="c5b9c-133">dcl\_resource</span></span>](dcl-resource.md)  
[<span data-ttu-id="c5b9c-134">muestra de DCL \_</span><span class="sxs-lookup"><span data-stu-id="c5b9c-134">dcl\_sampler</span></span>](dcl-sampler.md)  
[<span data-ttu-id="c5b9c-135">Temps de DCL \_</span><span class="sxs-lookup"><span data-stu-id="c5b9c-135">dcl\_temps</span></span>](dcl-temps.md)  
[<span data-ttu-id="c5b9c-136">default</span><span class="sxs-lookup"><span data-stu-id="c5b9c-136">default</span></span>](default--sm4---asm-.md)  
[<span data-ttu-id="c5b9c-137">derivar \_ RTX</span><span class="sxs-lookup"><span data-stu-id="c5b9c-137">deriv\_rtx</span></span>](deriv-rtx--sm4---asm-.md)  
[<span data-ttu-id="c5b9c-138">derivar \_ propiedad</span><span class="sxs-lookup"><span data-stu-id="c5b9c-138">deriv\_rty</span></span>](deriv-rty--sm4---asm-.md)  
[<span data-ttu-id="c5b9c-139">omiti</span><span class="sxs-lookup"><span data-stu-id="c5b9c-139">discard</span></span>](discard--sm4---asm-.md)  
[<span data-ttu-id="c5b9c-140">div</span><span class="sxs-lookup"><span data-stu-id="c5b9c-140">div</span></span>](div--sm4---asm-.md)  
[<span data-ttu-id="c5b9c-141">dp2</span><span class="sxs-lookup"><span data-stu-id="c5b9c-141">dp2</span></span>](dp2--sm4---asm-.md)  
[<span data-ttu-id="c5b9c-142">dp3</span><span class="sxs-lookup"><span data-stu-id="c5b9c-142">dp3</span></span>](dp3--sm4---asm-.md)  
[<span data-ttu-id="c5b9c-143">dp4</span><span class="sxs-lookup"><span data-stu-id="c5b9c-143">dp4</span></span>](dp4--sm4---asm-.md)  
[<span data-ttu-id="c5b9c-144">else</span><span class="sxs-lookup"><span data-stu-id="c5b9c-144">else</span></span>](else--sm4---asm-.md)  
[<span data-ttu-id="c5b9c-145">reflexión</span><span class="sxs-lookup"><span data-stu-id="c5b9c-145">emit</span></span>](emit--sm4---asm-.md)  
[<span data-ttu-id="c5b9c-146">emitThenCut</span><span class="sxs-lookup"><span data-stu-id="c5b9c-146">emitThenCut</span></span>](emitthencut--sm4---asm-.md)  
[<span data-ttu-id="c5b9c-147">endif</span><span class="sxs-lookup"><span data-stu-id="c5b9c-147">endif</span></span>](endif--sm4---asm-.md)  
[<span data-ttu-id="c5b9c-148">ENDLOOP</span><span class="sxs-lookup"><span data-stu-id="c5b9c-148">endloop</span></span>](endloop--sm4---asm-.md)  
[<span data-ttu-id="c5b9c-149">endswitch</span><span class="sxs-lookup"><span data-stu-id="c5b9c-149">endswitch</span></span>](endswitch--sm4---asm-.md)  
[<span data-ttu-id="c5b9c-150">eq</span><span class="sxs-lookup"><span data-stu-id="c5b9c-150">eq</span></span>](eq--sm4---asm-.md)  
[<span data-ttu-id="c5b9c-151">exp</span><span class="sxs-lookup"><span data-stu-id="c5b9c-151">exp</span></span>](exp--sm4---asm-.md)  
[<span data-ttu-id="c5b9c-152">frc</span><span class="sxs-lookup"><span data-stu-id="c5b9c-152">frc</span></span>](frc--sm4---asm-.md)  
[<span data-ttu-id="c5b9c-153">ftoi</span><span class="sxs-lookup"><span data-stu-id="c5b9c-153">ftoi</span></span>](ftoi--sm4---asm-.md)  
[<span data-ttu-id="c5b9c-154">ftou</span><span class="sxs-lookup"><span data-stu-id="c5b9c-154">ftou</span></span>](ftou--sm4---asm-.md)  
[<span data-ttu-id="c5b9c-155">ge</span><span class="sxs-lookup"><span data-stu-id="c5b9c-155">ge</span></span>](ge--sm4---asm-.md)  
[<span data-ttu-id="c5b9c-156">iadd</span><span class="sxs-lookup"><span data-stu-id="c5b9c-156">iadd</span></span>](iadd--sm4---asm-.md)  
[<span data-ttu-id="c5b9c-157">ibfe</span><span class="sxs-lookup"><span data-stu-id="c5b9c-157">ibfe</span></span>](dne--sm5---asm-.md)  
[<span data-ttu-id="c5b9c-158">ieq</span><span class="sxs-lookup"><span data-stu-id="c5b9c-158">ieq</span></span>](ieq--sm4---asm-.md)  
[<span data-ttu-id="c5b9c-159">if</span><span class="sxs-lookup"><span data-stu-id="c5b9c-159">if</span></span>](if--sm4---asm-.md)  
[<span data-ttu-id="c5b9c-160">ige</span><span class="sxs-lookup"><span data-stu-id="c5b9c-160">ige</span></span>](ige--sm4---asm-.md)  
[<span data-ttu-id="c5b9c-161">ILT</span><span class="sxs-lookup"><span data-stu-id="c5b9c-161">ilt</span></span>](ilt--sm4---asm-.md)  
[<span data-ttu-id="c5b9c-162">imad</span><span class="sxs-lookup"><span data-stu-id="c5b9c-162">imad</span></span>](imad--sm4---asm-.md)  
[<span data-ttu-id="c5b9c-163">imin</span><span class="sxs-lookup"><span data-stu-id="c5b9c-163">imin</span></span>](imin--sm4---asm-.md)  
[<span data-ttu-id="c5b9c-164">imul</span><span class="sxs-lookup"><span data-stu-id="c5b9c-164">imul</span></span>](imul--sm4---asm-.md)  
[<span data-ttu-id="c5b9c-165">Nea</span><span class="sxs-lookup"><span data-stu-id="c5b9c-165">ine</span></span>](ine--sm4---asm-.md)  
[<span data-ttu-id="c5b9c-166">ineg</span><span class="sxs-lookup"><span data-stu-id="c5b9c-166">ineg</span></span>](ineg--sm4---asm-.md)  
[<span data-ttu-id="c5b9c-167">ishl</span><span class="sxs-lookup"><span data-stu-id="c5b9c-167">ishl</span></span>](ishl--sm4---asm-.md)  
[<span data-ttu-id="c5b9c-168">ishr</span><span class="sxs-lookup"><span data-stu-id="c5b9c-168">ishr</span></span>](ishr--sm4---asm-.md)  
[<span data-ttu-id="c5b9c-169">itof</span><span class="sxs-lookup"><span data-stu-id="c5b9c-169">itof</span></span>](itof--sm4---asm-.md)  
[<span data-ttu-id="c5b9c-170">label</span><span class="sxs-lookup"><span data-stu-id="c5b9c-170">label</span></span>](label--sm4---asm-.md)  
<span data-ttu-id="c5b9c-171">[!](ld--sm4---asm-.md)</span><span class="sxs-lookup"><span data-stu-id="c5b9c-171">[ld](ld--sm4---asm-.md)</span></span>  
[<span data-ttu-id="c5b9c-172">inicia</span><span class="sxs-lookup"><span data-stu-id="c5b9c-172">log</span></span>](log--sm4---asm-.md)  
[<span data-ttu-id="c5b9c-173">bucle</span><span class="sxs-lookup"><span data-stu-id="c5b9c-173">loop</span></span>](loop--sm4---asm-.md)  
[<span data-ttu-id="c5b9c-174">lt</span><span class="sxs-lookup"><span data-stu-id="c5b9c-174">lt</span></span>](lt--sm4---asm-.md)  
[<span data-ttu-id="c5b9c-175">Mad</span><span class="sxs-lookup"><span data-stu-id="c5b9c-175">mad</span></span>](mad--sm4---asm-.md)  
[<span data-ttu-id="c5b9c-176">max</span><span class="sxs-lookup"><span data-stu-id="c5b9c-176">max</span></span>](max--sm4---asm-.md)  
[<span data-ttu-id="c5b9c-177">min</span><span class="sxs-lookup"><span data-stu-id="c5b9c-177">min</span></span>](min--sm4---asm-.md)  
[<span data-ttu-id="c5b9c-178">MOV</span><span class="sxs-lookup"><span data-stu-id="c5b9c-178">mov</span></span>](mov--sm4---asm-.md)  
[<span data-ttu-id="c5b9c-179">movc</span><span class="sxs-lookup"><span data-stu-id="c5b9c-179">movc</span></span>](movc--sm4---asm-.md)  
[<span data-ttu-id="c5b9c-180">mul</span><span class="sxs-lookup"><span data-stu-id="c5b9c-180">mul</span></span>](mul--sm4---asm-.md)  
[<span data-ttu-id="c5b9c-181">ne</span><span class="sxs-lookup"><span data-stu-id="c5b9c-181">ne</span></span>](ne--sm4---asm-.md)  
[<span data-ttu-id="c5b9c-182">instrucción</span><span class="sxs-lookup"><span data-stu-id="c5b9c-182">nop</span></span>](nop--sm4---asm-.md)  
[<span data-ttu-id="c5b9c-183">not</span><span class="sxs-lookup"><span data-stu-id="c5b9c-183">not</span></span>](not--sm4---asm-.md)  
[<span data-ttu-id="c5b9c-184">or</span><span class="sxs-lookup"><span data-stu-id="c5b9c-184">or</span></span>](or--sm4---asm-.md)  
[<span data-ttu-id="c5b9c-185">resinfo</span><span class="sxs-lookup"><span data-stu-id="c5b9c-185">resinfo</span></span>](resinfo--sm4---asm-.md)  
[<span data-ttu-id="c5b9c-186">direcc</span><span class="sxs-lookup"><span data-stu-id="c5b9c-186">ret</span></span>](ret--sm4---asm-.md)  
[<span data-ttu-id="c5b9c-187">retc</span><span class="sxs-lookup"><span data-stu-id="c5b9c-187">retc</span></span>](retc--sm4---asm-.md)  
[<span data-ttu-id="c5b9c-188">Round \_ ne</span><span class="sxs-lookup"><span data-stu-id="c5b9c-188">round\_ne</span></span>](round-ne--sm4---asm-.md)  
[<span data-ttu-id="c5b9c-189">no redondeo \_ ni</span><span class="sxs-lookup"><span data-stu-id="c5b9c-189">round\_ni</span></span>](round-ni--sm4---asm-.md)  
[<span data-ttu-id="c5b9c-190">redondear \_ PI</span><span class="sxs-lookup"><span data-stu-id="c5b9c-190">round\_pi</span></span>](round-pi--sm4---asm-.md)  
[<span data-ttu-id="c5b9c-191">Round \_ z</span><span class="sxs-lookup"><span data-stu-id="c5b9c-191">round\_z</span></span>](round-z--sm4---asm-.md)  
[<span data-ttu-id="c5b9c-192">rsq</span><span class="sxs-lookup"><span data-stu-id="c5b9c-192">rsq</span></span>](rsq--sm4---asm-.md)  
[<span data-ttu-id="c5b9c-193">AdventureWorks</span><span class="sxs-lookup"><span data-stu-id="c5b9c-193">sample</span></span>](sample--sm4---asm-.md)  
[<span data-ttu-id="c5b9c-194">ejemplo \_ b</span><span class="sxs-lookup"><span data-stu-id="c5b9c-194">sample\_b</span></span>](sample-b--sm4---asm-.md)  
[<span data-ttu-id="c5b9c-195">ejemplo \_ c</span><span class="sxs-lookup"><span data-stu-id="c5b9c-195">sample\_c</span></span>](sample-c--sm4---asm-.md)  
[<span data-ttu-id="c5b9c-196">ejemplo de \_ c \_ LZ</span><span class="sxs-lookup"><span data-stu-id="c5b9c-196">sample\_c\_lz</span></span>](sample-c-lz--sm4---asm-.md)  
[<span data-ttu-id="c5b9c-197">ejemplo \_ d</span><span class="sxs-lookup"><span data-stu-id="c5b9c-197">sample\_d</span></span>](sample-d--sm4---asm-.md)  
[<span data-ttu-id="c5b9c-198">ejemplo \_ l</span><span class="sxs-lookup"><span data-stu-id="c5b9c-198">sample\_l</span></span>](sample-l--sm4---asm-.md)  
[<span data-ttu-id="c5b9c-199">sincos (</span><span class="sxs-lookup"><span data-stu-id="c5b9c-199">sincos</span></span>](sincos--sm4---asm-.md)  
[<span data-ttu-id="c5b9c-200">sqrt</span><span class="sxs-lookup"><span data-stu-id="c5b9c-200">sqrt</span></span>](sqrt--sm4---asm-.md)  
[<span data-ttu-id="c5b9c-201">switch</span><span class="sxs-lookup"><span data-stu-id="c5b9c-201">switch</span></span>](switch--sm4---asm-.md)  
[<span data-ttu-id="c5b9c-202">UDIV</span><span class="sxs-lookup"><span data-stu-id="c5b9c-202">udiv</span></span>](udiv--sm4---asm-.md)  
[<span data-ttu-id="c5b9c-203">uge</span><span class="sxs-lookup"><span data-stu-id="c5b9c-203">uge</span></span>](uge--sm4---asm-.md)  
[<span data-ttu-id="c5b9c-204">ULT</span><span class="sxs-lookup"><span data-stu-id="c5b9c-204">ult</span></span>](ult--sm4---asm-.md)  
[<span data-ttu-id="c5b9c-205">umad</span><span class="sxs-lookup"><span data-stu-id="c5b9c-205">umad</span></span>](umad--sm4---asm-.md)  
[<span data-ttu-id="c5b9c-206">escáner</span><span class="sxs-lookup"><span data-stu-id="c5b9c-206">umax</span></span>](umax--sm4---asm-.md)  
[<span data-ttu-id="c5b9c-207">umin</span><span class="sxs-lookup"><span data-stu-id="c5b9c-207">umin</span></span>](umin--sm4---asm-.md)  
[<span data-ttu-id="c5b9c-208">umul</span><span class="sxs-lookup"><span data-stu-id="c5b9c-208">umul</span></span>](umul--sm4---asm-.md)  
[<span data-ttu-id="c5b9c-209">ushr</span><span class="sxs-lookup"><span data-stu-id="c5b9c-209">ushr</span></span>](ushr--sm4---asm-.md)  
[<span data-ttu-id="c5b9c-210">utof</span><span class="sxs-lookup"><span data-stu-id="c5b9c-210">utof</span></span>](utof--sm4---asm-.md)  
[<span data-ttu-id="c5b9c-211">xor</span><span class="sxs-lookup"><span data-stu-id="c5b9c-211">xor</span></span>](xor--sm4---asm-.md)  
</dl>

## <a name="shader-model-41-assembly"></a><span data-ttu-id="c5b9c-212">Ensamblado modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="c5b9c-212">Shader Model 4.1 Assembly</span></span>

<span data-ttu-id="c5b9c-213">El modelo de sombreador 4,1 es compatible con todas las instrucciones del modelo de sombreador 4,0 y las siguientes instrucciones adicionales:</span><span class="sxs-lookup"><span data-stu-id="c5b9c-213">Shader Model 4.1 supports all of the Shader Model 4.0 instructions and the following additional instructions:</span></span>

<dl>

[<span data-ttu-id="c5b9c-214">gather4</span><span class="sxs-lookup"><span data-stu-id="c5b9c-214">gather4</span></span>](gather4--sm4-1---asm-.md)  
[<span data-ttu-id="c5b9c-215">ld2dms</span><span class="sxs-lookup"><span data-stu-id="c5b9c-215">ld2dms</span></span>](ld2dms--sm4-1---asm-.md)  
[<span data-ttu-id="c5b9c-216">LOD</span><span class="sxs-lookup"><span data-stu-id="c5b9c-216">lod</span></span>](lod--sm4-1---asm-.md)  
[<span data-ttu-id="c5b9c-217">sampleinfo</span><span class="sxs-lookup"><span data-stu-id="c5b9c-217">sampleinfo</span></span>](sampleinfo--sm4-1---asm-.md)  
[<span data-ttu-id="c5b9c-218">samplepos</span><span class="sxs-lookup"><span data-stu-id="c5b9c-218">samplepos</span></span>](samplepos--sm4-1---asm-.md)  
</dl>

## <a name="related-topics"></a><span data-ttu-id="c5b9c-219">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c5b9c-219">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c5b9c-220">Referencia del sombreador de ASM</span><span class="sxs-lookup"><span data-stu-id="c5b9c-220">Asm Shader Reference</span></span>](dx9-graphics-reference-asm.md)
</dt> <dt>

[<span data-ttu-id="c5b9c-221">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="c5b9c-221">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 




