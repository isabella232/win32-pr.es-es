---
title: Modificadores de registro de origen del sombreador de píxeles
description: Use modificadores de registro de origen para cambiar el valor leído de un registro antes de que se ejecute una instrucción.
ms.assetid: b45d0919-7878-4184-ad4a-5623aae9d1f1
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a9dd4476dd7a1a885edb2e62a29b5127f5ff0a14
ms.sourcegitcommit: 7e4322a6ec1f964d5ad26e2e5e06cc8ce840030e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/01/2021
ms.locfileid: "113129682"
---
# <a name="pixel-shader-source-register-modifiers"></a><span data-ttu-id="d8b32-103">Modificadores de registro de origen del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="d8b32-103">Pixel Shader Source Register Modifiers</span></span>

<span data-ttu-id="d8b32-104">Use modificadores de registro de origen para cambiar el valor leído de un registro antes de que se ejecute una instrucción.</span><span class="sxs-lookup"><span data-stu-id="d8b32-104">Use source register modifiers to change the value read from a register before an instruction runs.</span></span> <span data-ttu-id="d8b32-105">El contenido de un registro de origen se deja sin cambios.</span><span class="sxs-lookup"><span data-stu-id="d8b32-105">The contents of a source register are left unchanged.</span></span> <span data-ttu-id="d8b32-106">Los modificadores son útiles para ajustar el intervalo de datos de registro como preparación para la instrucción.</span><span class="sxs-lookup"><span data-stu-id="d8b32-106">Modifiers are useful for adjusting the range of register data in preparation for the instruction.</span></span> <span data-ttu-id="d8b32-107">Un conjunto de modificadores denominado selectores copia o replica los datos de un único canal (r,g,b,a) en los demás canales.</span><span class="sxs-lookup"><span data-stu-id="d8b32-107">A set of modifiers called selectors copies or replicates the data from a single channel (r,g,b,a) into the other channels.</span></span>

## <a name="ps_1_1---ps_1_4"></a><span data-ttu-id="d8b32-108">ps \_ 1 \_ 1 - ps \_ 1 \_ 4</span><span class="sxs-lookup"><span data-stu-id="d8b32-108">ps\_1\_1 - ps\_1\_4</span></span>

<span data-ttu-id="d8b32-109">Esta tabla identifica las versiones que admiten cada modificador:</span><span class="sxs-lookup"><span data-stu-id="d8b32-109">This table identifies the versions that support each modifier:</span></span>



| <span data-ttu-id="d8b32-110">Modificadores de registro de origen</span><span class="sxs-lookup"><span data-stu-id="d8b32-110">Source register modifiers</span></span>                                                                                    | <span data-ttu-id="d8b32-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d8b32-111">Syntax</span></span>         | <span data-ttu-id="d8b32-112">Versión 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="d8b32-112">Version 1\_1</span></span> | <span data-ttu-id="d8b32-113">Versión 1 \_ 2</span><span class="sxs-lookup"><span data-stu-id="d8b32-113">Version 1\_2</span></span>     | <span data-ttu-id="d8b32-114">Versión 1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="d8b32-114">Version 1\_3</span></span>     | <span data-ttu-id="d8b32-115">Versión 1 \_ 4</span><span class="sxs-lookup"><span data-stu-id="d8b32-115">Version 1\_4</span></span>     |
|--------------------------------------------------------------------------------------------------------------|----------------|---------|------|------|------|
| [<span data-ttu-id="d8b32-116">predisposición</span><span class="sxs-lookup"><span data-stu-id="d8b32-116">bias</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-bias.md)                                           | <span data-ttu-id="d8b32-117">registro \_ de sesgo</span><span class="sxs-lookup"><span data-stu-id="d8b32-117">register\_bias</span></span> | <span data-ttu-id="d8b32-118">X</span><span class="sxs-lookup"><span data-stu-id="d8b32-118">X</span></span>       | <span data-ttu-id="d8b32-119">X</span><span class="sxs-lookup"><span data-stu-id="d8b32-119">X</span></span>    | <span data-ttu-id="d8b32-120">X</span><span class="sxs-lookup"><span data-stu-id="d8b32-120">X</span></span>    | <span data-ttu-id="d8b32-121">X</span><span class="sxs-lookup"><span data-stu-id="d8b32-121">X</span></span>    |
| [<span data-ttu-id="d8b32-122">Invertir</span><span class="sxs-lookup"><span data-stu-id="d8b32-122">invert</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-invert.md)                                       | <span data-ttu-id="d8b32-123">1 : registro</span><span class="sxs-lookup"><span data-stu-id="d8b32-123">1 - register</span></span>   | <span data-ttu-id="d8b32-124">X</span><span class="sxs-lookup"><span data-stu-id="d8b32-124">X</span></span>       | <span data-ttu-id="d8b32-125">X</span><span class="sxs-lookup"><span data-stu-id="d8b32-125">X</span></span>    | <span data-ttu-id="d8b32-126">X</span><span class="sxs-lookup"><span data-stu-id="d8b32-126">X</span></span>    | <span data-ttu-id="d8b32-127">X</span><span class="sxs-lookup"><span data-stu-id="d8b32-127">X</span></span>    |
| [<span data-ttu-id="d8b32-128">Negar</span><span class="sxs-lookup"><span data-stu-id="d8b32-128">negate</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-negate.md)                                       | <span data-ttu-id="d8b32-129">\- Registro</span><span class="sxs-lookup"><span data-stu-id="d8b32-129">\- register</span></span>    | <span data-ttu-id="d8b32-130">X</span><span class="sxs-lookup"><span data-stu-id="d8b32-130">X</span></span>       | <span data-ttu-id="d8b32-131">X</span><span class="sxs-lookup"><span data-stu-id="d8b32-131">X</span></span>    | <span data-ttu-id="d8b32-132">X</span><span class="sxs-lookup"><span data-stu-id="d8b32-132">X</span></span>    | <span data-ttu-id="d8b32-133">X</span><span class="sxs-lookup"><span data-stu-id="d8b32-133">X</span></span>    |
| [<span data-ttu-id="d8b32-134">escala en 2</span><span class="sxs-lookup"><span data-stu-id="d8b32-134">scale by 2</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-scale-x2.md)                                 | <span data-ttu-id="d8b32-135">register \_ x2</span><span class="sxs-lookup"><span data-stu-id="d8b32-135">register\_x2</span></span>   |         |      |      | <span data-ttu-id="d8b32-136">X</span><span class="sxs-lookup"><span data-stu-id="d8b32-136">X</span></span>    |
| [<span data-ttu-id="d8b32-137">escalado firmado</span><span class="sxs-lookup"><span data-stu-id="d8b32-137">signed scaling</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-signed-scale.md)                         | <span data-ttu-id="d8b32-138">register \_ bx2</span><span class="sxs-lookup"><span data-stu-id="d8b32-138">register\_bx2</span></span>  | <span data-ttu-id="d8b32-139">X</span><span class="sxs-lookup"><span data-stu-id="d8b32-139">X</span></span>       | <span data-ttu-id="d8b32-140">X</span><span class="sxs-lookup"><span data-stu-id="d8b32-140">X</span></span>    | <span data-ttu-id="d8b32-141">X</span><span class="sxs-lookup"><span data-stu-id="d8b32-141">X</span></span>    | <span data-ttu-id="d8b32-142">X</span><span class="sxs-lookup"><span data-stu-id="d8b32-142">X</span></span>    |
| [<span data-ttu-id="d8b32-143">modificadores texld y texcrd</span><span class="sxs-lookup"><span data-stu-id="d8b32-143">texld and texcrd modifiers</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-ps-1-4.md)                   | <span data-ttu-id="d8b32-144">register \_ d\*</span><span class="sxs-lookup"><span data-stu-id="d8b32-144">register\_d\*</span></span>  | <span data-ttu-id="d8b32-145">X</span><span class="sxs-lookup"><span data-stu-id="d8b32-145">X</span></span>       | <span data-ttu-id="d8b32-146">X</span><span class="sxs-lookup"><span data-stu-id="d8b32-146">X</span></span>    | <span data-ttu-id="d8b32-147">X</span><span class="sxs-lookup"><span data-stu-id="d8b32-147">X</span></span>    | <span data-ttu-id="d8b32-148">X</span><span class="sxs-lookup"><span data-stu-id="d8b32-148">X</span></span>    |
| [<span data-ttu-id="d8b32-149">swling del registro de origen</span><span class="sxs-lookup"><span data-stu-id="d8b32-149">source register swizzling</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md) | <span data-ttu-id="d8b32-150">register.xyzw</span><span class="sxs-lookup"><span data-stu-id="d8b32-150">register.xyzw</span></span>  | <span data-ttu-id="d8b32-151">X</span><span class="sxs-lookup"><span data-stu-id="d8b32-151">X</span></span>       | <span data-ttu-id="d8b32-152">X</span><span class="sxs-lookup"><span data-stu-id="d8b32-152">X</span></span>    | <span data-ttu-id="d8b32-153">X</span><span class="sxs-lookup"><span data-stu-id="d8b32-153">X</span></span>    | <span data-ttu-id="d8b32-154">X</span><span class="sxs-lookup"><span data-stu-id="d8b32-154">X</span></span>    |



 

<span data-ttu-id="d8b32-155">Los modificadores de registro de origen solo se pueden usar en instrucciones aritméticas.</span><span class="sxs-lookup"><span data-stu-id="d8b32-155">Source register modifiers can be used only on arithmetic instructions.</span></span> <span data-ttu-id="d8b32-156">No se pueden usar en instrucciones de dirección de textura.</span><span class="sxs-lookup"><span data-stu-id="d8b32-156">They cannot be used on texture address instructions.</span></span> <span data-ttu-id="d8b32-157">La excepción a esto es el [modificador de escala por 2.](dx9-graphics-reference-asm-ps-registers-modifiers-scale-x2.md)</span><span class="sxs-lookup"><span data-stu-id="d8b32-157">The exception to this is the [scale by 2](dx9-graphics-reference-asm-ps-registers-modifiers-scale-x2.md) modifier.</span></span> <span data-ttu-id="d8b32-158">Para la versión \_ 1 1, se puede usar la escala con firma en el argumento de origen de cualquier instrucción \* texm.</span><span class="sxs-lookup"><span data-stu-id="d8b32-158">For version 1\_1, signed scale can be used on the source argument of any texm\* instruction.</span></span> <span data-ttu-id="d8b32-159">Para la versión 1 \_ 2 o 1 3, la escala con firma se puede usar en el argumento de origen \_ de cualquier instrucción de dirección de textura.</span><span class="sxs-lookup"><span data-stu-id="d8b32-159">For version 1\_2 or 1\_3, signed scale can be used on the source argument of any texture address instruction.</span></span>

<span data-ttu-id="d8b32-160">Algunas restricciones específicas del modificador:</span><span class="sxs-lookup"><span data-stu-id="d8b32-160">Some modifier specific restrictions:</span></span>

-   <span data-ttu-id="d8b32-161">Negate se puede combinar con el sesgo, el escalado con firma o el modificador scalex2.</span><span class="sxs-lookup"><span data-stu-id="d8b32-161">Negate can be combined with either the bias, signed scaling, or scalex2 modifier.</span></span> <span data-ttu-id="d8b32-162">Cuando se combina, negate se ejecuta en último lugar.</span><span class="sxs-lookup"><span data-stu-id="d8b32-162">When combined, negate is run last.</span></span>
-   <span data-ttu-id="d8b32-163">La inversión no se puede combinar con ningún otro modificador.</span><span class="sxs-lookup"><span data-stu-id="d8b32-163">Invert cannot be combined with any other modifier.</span></span>
-   <span data-ttu-id="d8b32-164">Invert, negate, bias, signed scaling y scalex2 se pueden combinar con cualquiera de los selectores.</span><span class="sxs-lookup"><span data-stu-id="d8b32-164">Invert, negate, bias, signed scaling, and scalex2 can be combined with any of the selectors.</span></span>
-   <span data-ttu-id="d8b32-165">Los modificadores de registro de origen no deben usarse en registros constantes porque provocarán resultados no definidos.</span><span class="sxs-lookup"><span data-stu-id="d8b32-165">Source register modifiers should not be used on constant registers because they will cause undefined results.</span></span> <span data-ttu-id="d8b32-166">Para la versión 1 4, no se permiten modificadores en constantes \_ y se producirá un error en la validación.</span><span class="sxs-lookup"><span data-stu-id="d8b32-166">For version 1\_4, modifiers on constants are not allowed and will fail validation.</span></span>

## <a name="ps_2_0-and-above"></a><span data-ttu-id="d8b32-167">ps \_ 2 \_ 0 y superiores</span><span class="sxs-lookup"><span data-stu-id="d8b32-167">ps\_2\_0 and Above</span></span>

<span data-ttu-id="d8b32-168">Para la versión ps 2 0 y versiones arriba, se ha simplificado el número \_ \_ de modificadores.</span><span class="sxs-lookup"><span data-stu-id="d8b32-168">For version ps\_2\_0 and up, the number of modifiers has been simplified.</span></span>

### <a name="negate"></a><span data-ttu-id="d8b32-169">Negate</span><span class="sxs-lookup"><span data-stu-id="d8b32-169">Negate</span></span>

<span data-ttu-id="d8b32-170">Niega el contenido del registro de origen.</span><span class="sxs-lookup"><span data-stu-id="d8b32-170">Negate the contents of the source register.</span></span>



| <span data-ttu-id="d8b32-171">Modificador de componente</span><span class="sxs-lookup"><span data-stu-id="d8b32-171">Component modifier</span></span> | <span data-ttu-id="d8b32-172">Descripción</span><span class="sxs-lookup"><span data-stu-id="d8b32-172">Description</span></span>     |
|--------------------|-----------------|
| <span data-ttu-id="d8b32-173">\- R</span><span class="sxs-lookup"><span data-stu-id="d8b32-173">\- r</span></span>               | <span data-ttu-id="d8b32-174">Negación de origen</span><span class="sxs-lookup"><span data-stu-id="d8b32-174">Source negation</span></span> |



 

<span data-ttu-id="d8b32-175">El modificador negate no se puede usar en el segundo registro de origen de estas instrucciones: [m3x2 - ps](m3x2---ps.md), [m3x3 - ps](m3x3---ps.md), [m3x4 - ps](m3x4---ps.md), [m4x3 - ps](m4x3---ps.md)y [m4x4 - ps](m4x4---ps.md).</span><span class="sxs-lookup"><span data-stu-id="d8b32-175">The negate modifier cannot be used on second source register of these instructions: [m3x2 - ps](m3x2---ps.md), [m3x3 - ps](m3x3---ps.md), [m3x4 - ps](m3x4---ps.md), [m4x3 - ps](m4x3---ps.md), and [m4x4 - ps](m4x4---ps.md).</span></span>



| <span data-ttu-id="d8b32-176">Versiones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="d8b32-176">Pixel shader versions</span></span> | <span data-ttu-id="d8b32-177">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="d8b32-177">2\_0</span></span> | <span data-ttu-id="d8b32-178">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="d8b32-178">2\_x</span></span> | <span data-ttu-id="d8b32-179">2 \_ sw</span><span class="sxs-lookup"><span data-stu-id="d8b32-179">2\_sw</span></span> | <span data-ttu-id="d8b32-180">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="d8b32-180">3\_0</span></span> | <span data-ttu-id="d8b32-181">3 \_ sw</span><span class="sxs-lookup"><span data-stu-id="d8b32-181">3\_sw</span></span> |
|-----------------------|------|------|-------|------|-------|
| \-                    | <span data-ttu-id="d8b32-182">x</span><span class="sxs-lookup"><span data-stu-id="d8b32-182">x</span></span>    | <span data-ttu-id="d8b32-183">x</span><span class="sxs-lookup"><span data-stu-id="d8b32-183">x</span></span>    | <span data-ttu-id="d8b32-184">x</span><span class="sxs-lookup"><span data-stu-id="d8b32-184">x</span></span>     | <span data-ttu-id="d8b32-185">x</span><span class="sxs-lookup"><span data-stu-id="d8b32-185">x</span></span>    | <span data-ttu-id="d8b32-186">x</span><span class="sxs-lookup"><span data-stu-id="d8b32-186">x</span></span>     |



 

### <a name="absolute-value"></a><span data-ttu-id="d8b32-187">Valor absoluto</span><span class="sxs-lookup"><span data-stu-id="d8b32-187">Absolute Value</span></span>

<span data-ttu-id="d8b32-188">Tome el valor absoluto del registro.</span><span class="sxs-lookup"><span data-stu-id="d8b32-188">Take the absolute value of the register.</span></span>



| <span data-ttu-id="d8b32-189">Versiones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="d8b32-189">Pixel shader versions</span></span> | <span data-ttu-id="d8b32-190">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="d8b32-190">2\_0</span></span> | <span data-ttu-id="d8b32-191">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="d8b32-191">2\_x</span></span> | <span data-ttu-id="d8b32-192">2 \_ sw</span><span class="sxs-lookup"><span data-stu-id="d8b32-192">2\_sw</span></span> | <span data-ttu-id="d8b32-193">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="d8b32-193">3\_0</span></span> | <span data-ttu-id="d8b32-194">3 \_ sw</span><span class="sxs-lookup"><span data-stu-id="d8b32-194">3\_sw</span></span> |
|-----------------------|------|------|-------|------|-------|
| <span data-ttu-id="d8b32-195">abs</span><span class="sxs-lookup"><span data-stu-id="d8b32-195">abs</span></span>                   |      |      |       | <span data-ttu-id="d8b32-196">x</span><span class="sxs-lookup"><span data-stu-id="d8b32-196">x</span></span>    | <span data-ttu-id="d8b32-197">x</span><span class="sxs-lookup"><span data-stu-id="d8b32-197">x</span></span>     |



 

<span data-ttu-id="d8b32-198">Si algún sombreador de la versión 3 lee de uno o varios registros float constantes \# (c), debe cumplirse una de las siguientes condiciones.</span><span class="sxs-lookup"><span data-stu-id="d8b32-198">If any version 3 shader reads from one or more constant float registers (c\#), one of the following must be true.</span></span>

-   <span data-ttu-id="d8b32-199">Todos los registros de punto flotante constantes deben usar el modificador abs.</span><span class="sxs-lookup"><span data-stu-id="d8b32-199">All of the constant floating-point registers must use the abs modifier.</span></span>
-   <span data-ttu-id="d8b32-200">Ninguno de los registros de punto flotante constantes puede usar el modificador abs.</span><span class="sxs-lookup"><span data-stu-id="d8b32-200">None of the constant floating-point registers can use the abs modifier.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d8b32-201">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d8b32-201">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d8b32-202">Modificadores de registro del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="d8b32-202">Pixel Shader Register Modifiers</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers.md)
</dt> </dl>

 

 




