---
title: Modificadores de registro de origen del sombreador de píxeles
description: Utilice modificadores de registro de origen para cambiar el valor leído de un registro antes de que se ejecute una instrucción.
ms.assetid: b45d0919-7878-4184-ad4a-5623aae9d1f1
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 12cfee533a71408a445d97a63bbd8b76b281236b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357757"
---
# <a name="pixel-shader-source-register-modifiers"></a><span data-ttu-id="e32ac-103">Modificadores de registro de origen del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="e32ac-103">Pixel Shader Source Register Modifiers</span></span>

<span data-ttu-id="e32ac-104">Utilice modificadores de registro de origen para cambiar el valor leído de un registro antes de que se ejecute una instrucción.</span><span class="sxs-lookup"><span data-stu-id="e32ac-104">Use source register modifiers to change the value read from a register before an instruction runs.</span></span> <span data-ttu-id="e32ac-105">El contenido de un registro de origen se deja sin cambios.</span><span class="sxs-lookup"><span data-stu-id="e32ac-105">The contents of a source register are left unchanged.</span></span> <span data-ttu-id="e32ac-106">Los modificadores son útiles para ajustar el intervalo de datos de registro como preparación para la instrucción.</span><span class="sxs-lookup"><span data-stu-id="e32ac-106">Modifiers are useful for adjusting the range of register data in preparation for the instruction.</span></span> <span data-ttu-id="e32ac-107">Un conjunto de modificadores denominados selectores copia o replica los datos de un canal único (r, g, b, a) en los otros canales.</span><span class="sxs-lookup"><span data-stu-id="e32ac-107">A set of modifiers called selectors copies or replicates the data from a single channel (r,g,b,a) into the other channels.</span></span>

## <a name="ps_1_1---ps_1_4"></a><span data-ttu-id="e32ac-108">PS \_ 1 \_ 1-PS \_ 1 \_ 4</span><span class="sxs-lookup"><span data-stu-id="e32ac-108">ps\_1\_1 - ps\_1\_4</span></span>

<span data-ttu-id="e32ac-109">En esta tabla se identifican las versiones que admiten cada modificador:</span><span class="sxs-lookup"><span data-stu-id="e32ac-109">This table identifies the versions that support each modifier:</span></span>



| <span data-ttu-id="e32ac-110">Modificadores de registro de origen</span><span class="sxs-lookup"><span data-stu-id="e32ac-110">Source register modifiers</span></span>                                                                                    | <span data-ttu-id="e32ac-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e32ac-111">Syntax</span></span>         | <span data-ttu-id="e32ac-112">Versión</span><span class="sxs-lookup"><span data-stu-id="e32ac-112">Version</span></span> |      |      |      |     |     |
|--------------------------------------------------------------------------------------------------------------|----------------|---------|------|------|------|-----|-----|
|                                                                                                              |                | <span data-ttu-id="e32ac-113">1\_1</span><span class="sxs-lookup"><span data-stu-id="e32ac-113">1\_1</span></span>    | <span data-ttu-id="e32ac-114">1\_2</span><span class="sxs-lookup"><span data-stu-id="e32ac-114">1\_2</span></span> | <span data-ttu-id="e32ac-115">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="e32ac-115">1\_3</span></span> | <span data-ttu-id="e32ac-116">1\_4</span><span class="sxs-lookup"><span data-stu-id="e32ac-116">1\_4</span></span> |     |     |
| [<span data-ttu-id="e32ac-117">parcial</span><span class="sxs-lookup"><span data-stu-id="e32ac-117">bias</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-bias.md)                                           | <span data-ttu-id="e32ac-118">\_desviar registro</span><span class="sxs-lookup"><span data-stu-id="e32ac-118">register\_bias</span></span> | <span data-ttu-id="e32ac-119">X</span><span class="sxs-lookup"><span data-stu-id="e32ac-119">X</span></span>       | <span data-ttu-id="e32ac-120">X</span><span class="sxs-lookup"><span data-stu-id="e32ac-120">X</span></span>    | <span data-ttu-id="e32ac-121">X</span><span class="sxs-lookup"><span data-stu-id="e32ac-121">X</span></span>    | <span data-ttu-id="e32ac-122">X</span><span class="sxs-lookup"><span data-stu-id="e32ac-122">X</span></span>    |     |     |
| [<span data-ttu-id="e32ac-123">triángulo</span><span class="sxs-lookup"><span data-stu-id="e32ac-123">invert</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-invert.md)                                       | <span data-ttu-id="e32ac-124">1-registro</span><span class="sxs-lookup"><span data-stu-id="e32ac-124">1 - register</span></span>   | <span data-ttu-id="e32ac-125">X</span><span class="sxs-lookup"><span data-stu-id="e32ac-125">X</span></span>       | <span data-ttu-id="e32ac-126">X</span><span class="sxs-lookup"><span data-stu-id="e32ac-126">X</span></span>    | <span data-ttu-id="e32ac-127">X</span><span class="sxs-lookup"><span data-stu-id="e32ac-127">X</span></span>    | <span data-ttu-id="e32ac-128">X</span><span class="sxs-lookup"><span data-stu-id="e32ac-128">X</span></span>    |     |     |
| [<span data-ttu-id="e32ac-129">negate</span><span class="sxs-lookup"><span data-stu-id="e32ac-129">negate</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-negate.md)                                       | <span data-ttu-id="e32ac-130">\- el</span><span class="sxs-lookup"><span data-stu-id="e32ac-130">\- register</span></span>    | <span data-ttu-id="e32ac-131">X</span><span class="sxs-lookup"><span data-stu-id="e32ac-131">X</span></span>       | <span data-ttu-id="e32ac-132">X</span><span class="sxs-lookup"><span data-stu-id="e32ac-132">X</span></span>    | <span data-ttu-id="e32ac-133">X</span><span class="sxs-lookup"><span data-stu-id="e32ac-133">X</span></span>    | <span data-ttu-id="e32ac-134">X</span><span class="sxs-lookup"><span data-stu-id="e32ac-134">X</span></span>    |     |     |
| [<span data-ttu-id="e32ac-135">escalar por 2</span><span class="sxs-lookup"><span data-stu-id="e32ac-135">scale by 2</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-scale-x2.md)                                 | <span data-ttu-id="e32ac-136">registrar \_ x2</span><span class="sxs-lookup"><span data-stu-id="e32ac-136">register\_x2</span></span>   |         |      |      | <span data-ttu-id="e32ac-137">X</span><span class="sxs-lookup"><span data-stu-id="e32ac-137">X</span></span>    |     |     |
| [<span data-ttu-id="e32ac-138">escalado con signo</span><span class="sxs-lookup"><span data-stu-id="e32ac-138">signed scaling</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-signed-scale.md)                         | <span data-ttu-id="e32ac-139">registrar \_ BX2</span><span class="sxs-lookup"><span data-stu-id="e32ac-139">register\_bx2</span></span>  | <span data-ttu-id="e32ac-140">X</span><span class="sxs-lookup"><span data-stu-id="e32ac-140">X</span></span>       | <span data-ttu-id="e32ac-141">X</span><span class="sxs-lookup"><span data-stu-id="e32ac-141">X</span></span>    | <span data-ttu-id="e32ac-142">X</span><span class="sxs-lookup"><span data-stu-id="e32ac-142">X</span></span>    | <span data-ttu-id="e32ac-143">X</span><span class="sxs-lookup"><span data-stu-id="e32ac-143">X</span></span>    |     |     |
| [<span data-ttu-id="e32ac-144">modificadores texld y texcrd</span><span class="sxs-lookup"><span data-stu-id="e32ac-144">texld and texcrd modifiers</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-ps-1-4.md)                   | <span data-ttu-id="e32ac-145">Registro \_ d\*</span><span class="sxs-lookup"><span data-stu-id="e32ac-145">register\_d\*</span></span>  | <span data-ttu-id="e32ac-146">X</span><span class="sxs-lookup"><span data-stu-id="e32ac-146">X</span></span>       | <span data-ttu-id="e32ac-147">X</span><span class="sxs-lookup"><span data-stu-id="e32ac-147">X</span></span>    | <span data-ttu-id="e32ac-148">X</span><span class="sxs-lookup"><span data-stu-id="e32ac-148">X</span></span>    | <span data-ttu-id="e32ac-149">X</span><span class="sxs-lookup"><span data-stu-id="e32ac-149">X</span></span>    |     |     |
| [<span data-ttu-id="e32ac-150">registro de origen permutación</span><span class="sxs-lookup"><span data-stu-id="e32ac-150">source register swizzling</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md) | <span data-ttu-id="e32ac-151">registro. xyzw</span><span class="sxs-lookup"><span data-stu-id="e32ac-151">register.xyzw</span></span>  | <span data-ttu-id="e32ac-152">X</span><span class="sxs-lookup"><span data-stu-id="e32ac-152">X</span></span>       | <span data-ttu-id="e32ac-153">X</span><span class="sxs-lookup"><span data-stu-id="e32ac-153">X</span></span>    | <span data-ttu-id="e32ac-154">X</span><span class="sxs-lookup"><span data-stu-id="e32ac-154">X</span></span>    | <span data-ttu-id="e32ac-155">X</span><span class="sxs-lookup"><span data-stu-id="e32ac-155">X</span></span>    |     |     |



 

<span data-ttu-id="e32ac-156">Los modificadores de registro de origen solo se pueden usar en Instrucciones aritméticas.</span><span class="sxs-lookup"><span data-stu-id="e32ac-156">Source register modifiers can be used only on arithmetic instructions.</span></span> <span data-ttu-id="e32ac-157">No se pueden usar en instrucciones de dirección de textura.</span><span class="sxs-lookup"><span data-stu-id="e32ac-157">They cannot be used on texture address instructions.</span></span> <span data-ttu-id="e32ac-158">La excepción es el modificador [Scale by 2](dx9-graphics-reference-asm-ps-registers-modifiers-scale-x2.md) .</span><span class="sxs-lookup"><span data-stu-id="e32ac-158">The exception to this is the [scale by 2](dx9-graphics-reference-asm-ps-registers-modifiers-scale-x2.md) modifier.</span></span> <span data-ttu-id="e32ac-159">En el caso de la versión 1 \_ , se puede usar la escala con signo en el argumento de origen de cualquier \* instrucción texm.</span><span class="sxs-lookup"><span data-stu-id="e32ac-159">For version 1\_1, signed scale can be used on the source argument of any texm\* instruction.</span></span> <span data-ttu-id="e32ac-160">En el caso de la versión 1 \_ 2 o 1 \_ 3, la escala firmada se puede utilizar en el argumento de origen de cualquier instrucción de dirección de textura.</span><span class="sxs-lookup"><span data-stu-id="e32ac-160">For version 1\_2 or 1\_3, signed scale can be used on the source argument of any texture address instruction.</span></span>

<span data-ttu-id="e32ac-161">Algunas restricciones específicas del modificador:</span><span class="sxs-lookup"><span data-stu-id="e32ac-161">Some modifier specific restrictions:</span></span>

-   <span data-ttu-id="e32ac-162">Niega puede combinarse con el modificador Bias, escalado con signo o scalex2.</span><span class="sxs-lookup"><span data-stu-id="e32ac-162">Negate can be combined with either the bias, signed scaling, or scalex2 modifier.</span></span> <span data-ttu-id="e32ac-163">Cuando se combina, la ejecución de la negación es la última.</span><span class="sxs-lookup"><span data-stu-id="e32ac-163">When combined, negate is run last.</span></span>
-   <span data-ttu-id="e32ac-164">La inversión no se puede combinar con ningún otro modificador.</span><span class="sxs-lookup"><span data-stu-id="e32ac-164">Invert cannot be combined with any other modifier.</span></span>
-   <span data-ttu-id="e32ac-165">Invert, Negate, Bias, escala firmada y scalex2 se pueden combinar con cualquiera de los selectores.</span><span class="sxs-lookup"><span data-stu-id="e32ac-165">Invert, negate, bias, signed scaling, and scalex2 can be combined with any of the selectors.</span></span>
-   <span data-ttu-id="e32ac-166">Los modificadores de registro de origen no se deben usar en registros constantes porque producirán resultados no definidos.</span><span class="sxs-lookup"><span data-stu-id="e32ac-166">Source register modifiers should not be used on constant registers because they will cause undefined results.</span></span> <span data-ttu-id="e32ac-167">En el caso de la versión \_ 4, no se permiten modificadores en constantes y se producirá un error en la validación.</span><span class="sxs-lookup"><span data-stu-id="e32ac-167">For version 1\_4, modifiers on constants are not allowed and will fail validation.</span></span>

## <a name="ps_2_0-and-above"></a><span data-ttu-id="e32ac-168">PS \_ 2 \_ 0 y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="e32ac-168">ps\_2\_0 and Above</span></span>

<span data-ttu-id="e32ac-169">En el caso de la versión PS \_ 2 \_ 0 y versiones más arriba, se ha simplificado el número de modificadores.</span><span class="sxs-lookup"><span data-stu-id="e32ac-169">For version ps\_2\_0 and up, the number of modifiers has been simplified.</span></span>

### <a name="negate"></a><span data-ttu-id="e32ac-170">Negate</span><span class="sxs-lookup"><span data-stu-id="e32ac-170">Negate</span></span>

<span data-ttu-id="e32ac-171">Niega el contenido del registro de origen.</span><span class="sxs-lookup"><span data-stu-id="e32ac-171">Negate the contents of the source register.</span></span>



| <span data-ttu-id="e32ac-172">Modificador de componente</span><span class="sxs-lookup"><span data-stu-id="e32ac-172">Component modifier</span></span> | <span data-ttu-id="e32ac-173">Descripción</span><span class="sxs-lookup"><span data-stu-id="e32ac-173">Description</span></span>     |
|--------------------|-----------------|
| <span data-ttu-id="e32ac-174">\- c</span><span class="sxs-lookup"><span data-stu-id="e32ac-174">\- r</span></span>               | <span data-ttu-id="e32ac-175">Negación de origen</span><span class="sxs-lookup"><span data-stu-id="e32ac-175">Source negation</span></span> |



 

<span data-ttu-id="e32ac-176">No se puede usar el modificador Negate en el segundo registro de código fuente de estas instrucciones: [m3x2-PS](m3x2---ps.md), [M3x3-PS](m3x3---ps.md), [M3x4-PS](m3x4---ps.md), [m4x3-PS](m4x3---ps.md)y [M4x4-PS](m4x4---ps.md).</span><span class="sxs-lookup"><span data-stu-id="e32ac-176">The negate modifier cannot be used on second source register of these instructions: [m3x2 - ps](m3x2---ps.md), [m3x3 - ps](m3x3---ps.md), [m3x4 - ps](m3x4---ps.md), [m4x3 - ps](m4x3---ps.md), and [m4x4 - ps](m4x4---ps.md).</span></span>



| <span data-ttu-id="e32ac-177">Versiones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="e32ac-177">Pixel shader versions</span></span> | <span data-ttu-id="e32ac-178">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="e32ac-178">2\_0</span></span> | <span data-ttu-id="e32ac-179">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="e32ac-179">2\_x</span></span> | <span data-ttu-id="e32ac-180">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="e32ac-180">2\_sw</span></span> | <span data-ttu-id="e32ac-181">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="e32ac-181">3\_0</span></span> | <span data-ttu-id="e32ac-182">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="e32ac-182">3\_sw</span></span> |
|-----------------------|------|------|-------|------|-------|
| \-                    | <span data-ttu-id="e32ac-183">x</span><span class="sxs-lookup"><span data-stu-id="e32ac-183">x</span></span>    | <span data-ttu-id="e32ac-184">x</span><span class="sxs-lookup"><span data-stu-id="e32ac-184">x</span></span>    | <span data-ttu-id="e32ac-185">x</span><span class="sxs-lookup"><span data-stu-id="e32ac-185">x</span></span>     | <span data-ttu-id="e32ac-186">x</span><span class="sxs-lookup"><span data-stu-id="e32ac-186">x</span></span>    | <span data-ttu-id="e32ac-187">x</span><span class="sxs-lookup"><span data-stu-id="e32ac-187">x</span></span>     |



 

### <a name="absolute-value"></a><span data-ttu-id="e32ac-188">Valor absoluto</span><span class="sxs-lookup"><span data-stu-id="e32ac-188">Absolute Value</span></span>

<span data-ttu-id="e32ac-189">Tome el valor absoluto del registro.</span><span class="sxs-lookup"><span data-stu-id="e32ac-189">Take the absolute value of the register.</span></span>



| <span data-ttu-id="e32ac-190">Versiones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="e32ac-190">Pixel shader versions</span></span> | <span data-ttu-id="e32ac-191">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="e32ac-191">2\_0</span></span> | <span data-ttu-id="e32ac-192">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="e32ac-192">2\_x</span></span> | <span data-ttu-id="e32ac-193">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="e32ac-193">2\_sw</span></span> | <span data-ttu-id="e32ac-194">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="e32ac-194">3\_0</span></span> | <span data-ttu-id="e32ac-195">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="e32ac-195">3\_sw</span></span> |
|-----------------------|------|------|-------|------|-------|
| <span data-ttu-id="e32ac-196">abs</span><span class="sxs-lookup"><span data-stu-id="e32ac-196">abs</span></span>                   |      |      |       | <span data-ttu-id="e32ac-197">x</span><span class="sxs-lookup"><span data-stu-id="e32ac-197">x</span></span>    | <span data-ttu-id="e32ac-198">x</span><span class="sxs-lookup"><span data-stu-id="e32ac-198">x</span></span>     |



 

<span data-ttu-id="e32ac-199">Si cualquier sombreador de la versión 3 Lee de uno o más registros Float constantes (c \# ), debe cumplirse una de las siguientes condiciones.</span><span class="sxs-lookup"><span data-stu-id="e32ac-199">If any version 3 shader reads from one or more constant float registers (c\#), one of the following must be true.</span></span>

-   <span data-ttu-id="e32ac-200">Todos los registros de punto flotante constantes deben usar el modificador ABS.</span><span class="sxs-lookup"><span data-stu-id="e32ac-200">All of the constant floating-point registers must use the abs modifier.</span></span>
-   <span data-ttu-id="e32ac-201">Ninguno de los registros de punto flotante constantes puede usar el modificador ABS.</span><span class="sxs-lookup"><span data-stu-id="e32ac-201">None of the constant floating-point registers can use the abs modifier.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e32ac-202">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e32ac-202">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e32ac-203">Modificadores de registro del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="e32ac-203">Pixel Shader Register Modifiers</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers.md)
</dt> </dl>

 

 




