---
title: Máscara de escritura de registro de destino
description: Una máscara de escritura controla qué componentes de un registro de destino se escriben una vez completada una instrucción.
ms.assetid: 376a28c8-8a88-4807-a8ab-f59448d965e8
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 80f649770b84174dbb716967e9d941034c3966f5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994597"
---
# <a name="destination-register-write-mask"></a><span data-ttu-id="b3730-103">Máscara de escritura de registro de destino</span><span class="sxs-lookup"><span data-stu-id="b3730-103">Destination Register Write Mask</span></span>

<span data-ttu-id="b3730-104">Una máscara de escritura controla qué componentes de un registro de destino se escriben una vez completada una instrucción.</span><span class="sxs-lookup"><span data-stu-id="b3730-104">A write mask controls which components of a destination register are written after an instruction is completed.</span></span> <span data-ttu-id="b3730-105">Se permite una máscara de escritura de salida siempre que los componentes estén en el orden de. RGBA o. xyzw.</span><span class="sxs-lookup"><span data-stu-id="b3730-105">An output write mask is allowed as long as the components are in the order of .rgba or .xyzw.</span></span> <span data-ttu-id="b3730-106">Es decir,. RBA y. XW son máscaras válidas.</span><span class="sxs-lookup"><span data-stu-id="b3730-106">That is, .rba and .xw are valid masks.</span></span> <span data-ttu-id="b3730-107">Los registros de textura tienen un conjunto de reglas y los registros que no son de textura tienen otro conjunto de reglas.</span><span class="sxs-lookup"><span data-stu-id="b3730-107">Texture registers have one set of rules and non-texture registers have another set of rules.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3730-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b3730-108">Syntax</span></span>



| <span data-ttu-id="b3730-109">DST. writemask</span><span class="sxs-lookup"><span data-stu-id="b3730-109">dst.writemask</span></span> |
|---------------|



 

<span data-ttu-id="b3730-110">, donde</span><span class="sxs-lookup"><span data-stu-id="b3730-110">where</span></span>

-   <span data-ttu-id="b3730-111">DST es un registro de destino.</span><span class="sxs-lookup"><span data-stu-id="b3730-111">dst is a destination register.</span></span>
-   <span data-ttu-id="b3730-112">writemask es una secuencia de máscaras de cualquier conjunto: (x, y, z, w) o (rojo, verde, azul, alfa).</span><span class="sxs-lookup"><span data-stu-id="b3730-112">writemask is a sequence of masks from either set: (x,y,z,w) or (red, green, blue, alpha).</span></span>

## <a name="remarks"></a><span data-ttu-id="b3730-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b3730-113">Remarks</span></span>

<span data-ttu-id="b3730-114">Están disponibles las siguientes máscaras de escritura de destino.</span><span class="sxs-lookup"><span data-stu-id="b3730-114">The following destination write masks are available.</span></span>



| <span data-ttu-id="b3730-115">Versiones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="b3730-115">Pixel shader versions</span></span> | <span data-ttu-id="b3730-116">1\_1</span><span class="sxs-lookup"><span data-stu-id="b3730-116">1\_1</span></span> | <span data-ttu-id="b3730-117">1\_2</span><span class="sxs-lookup"><span data-stu-id="b3730-117">1\_2</span></span> | <span data-ttu-id="b3730-118">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="b3730-118">1\_3</span></span> | <span data-ttu-id="b3730-119">1\_4</span><span class="sxs-lookup"><span data-stu-id="b3730-119">1\_4</span></span> | <span data-ttu-id="b3730-120">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="b3730-120">2\_0</span></span> | <span data-ttu-id="b3730-121">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="b3730-121">2\_x</span></span> | <span data-ttu-id="b3730-122">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="b3730-122">2\_sw</span></span> | <span data-ttu-id="b3730-123">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="b3730-123">3\_0</span></span> | <span data-ttu-id="b3730-124">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="b3730-124">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="b3730-125">. xyzw (valor predeterminado)</span><span class="sxs-lookup"><span data-stu-id="b3730-125">.xyzw (default)</span></span>       | <span data-ttu-id="b3730-126">x</span><span class="sxs-lookup"><span data-stu-id="b3730-126">x</span></span>    | <span data-ttu-id="b3730-127">x</span><span class="sxs-lookup"><span data-stu-id="b3730-127">x</span></span>    | <span data-ttu-id="b3730-128">x</span><span class="sxs-lookup"><span data-stu-id="b3730-128">x</span></span>    | <span data-ttu-id="b3730-129">x</span><span class="sxs-lookup"><span data-stu-id="b3730-129">x</span></span>    | <span data-ttu-id="b3730-130">x</span><span class="sxs-lookup"><span data-stu-id="b3730-130">x</span></span>    | <span data-ttu-id="b3730-131">x</span><span class="sxs-lookup"><span data-stu-id="b3730-131">x</span></span>    | <span data-ttu-id="b3730-132">x</span><span class="sxs-lookup"><span data-stu-id="b3730-132">x</span></span>     | <span data-ttu-id="b3730-133">x</span><span class="sxs-lookup"><span data-stu-id="b3730-133">x</span></span>    | <span data-ttu-id="b3730-134">x</span><span class="sxs-lookup"><span data-stu-id="b3730-134">x</span></span>     |
| <span data-ttu-id="b3730-135">. XYZ</span><span class="sxs-lookup"><span data-stu-id="b3730-135">.xyz</span></span>                  | <span data-ttu-id="b3730-136">x</span><span class="sxs-lookup"><span data-stu-id="b3730-136">x</span></span>    | <span data-ttu-id="b3730-137">x</span><span class="sxs-lookup"><span data-stu-id="b3730-137">x</span></span>    | <span data-ttu-id="b3730-138">x</span><span class="sxs-lookup"><span data-stu-id="b3730-138">x</span></span>    | <span data-ttu-id="b3730-139">x</span><span class="sxs-lookup"><span data-stu-id="b3730-139">x</span></span>    | <span data-ttu-id="b3730-140">x</span><span class="sxs-lookup"><span data-stu-id="b3730-140">x</span></span>    | <span data-ttu-id="b3730-141">x</span><span class="sxs-lookup"><span data-stu-id="b3730-141">x</span></span>    | <span data-ttu-id="b3730-142">x</span><span class="sxs-lookup"><span data-stu-id="b3730-142">x</span></span>     | <span data-ttu-id="b3730-143">x</span><span class="sxs-lookup"><span data-stu-id="b3730-143">x</span></span>    | <span data-ttu-id="b3730-144">x</span><span class="sxs-lookup"><span data-stu-id="b3730-144">x</span></span>     |
| <span data-ttu-id="b3730-145">. w</span><span class="sxs-lookup"><span data-stu-id="b3730-145">.w</span></span>                    | <span data-ttu-id="b3730-146">x</span><span class="sxs-lookup"><span data-stu-id="b3730-146">x</span></span>    | <span data-ttu-id="b3730-147">x</span><span class="sxs-lookup"><span data-stu-id="b3730-147">x</span></span>    | <span data-ttu-id="b3730-148">x</span><span class="sxs-lookup"><span data-stu-id="b3730-148">x</span></span>    | <span data-ttu-id="b3730-149">x</span><span class="sxs-lookup"><span data-stu-id="b3730-149">x</span></span>    | <span data-ttu-id="b3730-150">x</span><span class="sxs-lookup"><span data-stu-id="b3730-150">x</span></span>    | <span data-ttu-id="b3730-151">x</span><span class="sxs-lookup"><span data-stu-id="b3730-151">x</span></span>    | <span data-ttu-id="b3730-152">x</span><span class="sxs-lookup"><span data-stu-id="b3730-152">x</span></span>     | <span data-ttu-id="b3730-153">x</span><span class="sxs-lookup"><span data-stu-id="b3730-153">x</span></span>    | <span data-ttu-id="b3730-154">x</span><span class="sxs-lookup"><span data-stu-id="b3730-154">x</span></span>     |
| <span data-ttu-id="b3730-155">máscara arbitraria</span><span class="sxs-lookup"><span data-stu-id="b3730-155">arbitrary mask</span></span>        |      |      |      | <span data-ttu-id="b3730-156">x</span><span class="sxs-lookup"><span data-stu-id="b3730-156">x</span></span>    | <span data-ttu-id="b3730-157">x</span><span class="sxs-lookup"><span data-stu-id="b3730-157">x</span></span>    | <span data-ttu-id="b3730-158">x</span><span class="sxs-lookup"><span data-stu-id="b3730-158">x</span></span>    | <span data-ttu-id="b3730-159">x</span><span class="sxs-lookup"><span data-stu-id="b3730-159">x</span></span>     | <span data-ttu-id="b3730-160">x</span><span class="sxs-lookup"><span data-stu-id="b3730-160">x</span></span>    | <span data-ttu-id="b3730-161">x</span><span class="sxs-lookup"><span data-stu-id="b3730-161">x</span></span>     |



 

<span data-ttu-id="b3730-162">La máscara arbitraria permite combinar cualquier conjunto de canales para generar una máscara.</span><span class="sxs-lookup"><span data-stu-id="b3730-162">The arbitrary mask allows any set of channels to be combined to produce a mask.</span></span> <span data-ttu-id="b3730-163">Los canales deben aparecer en el orden r, g, b, a-por ejemplo, Register. RBA, que actualiza los canales rojo, azul y alfa del destino.</span><span class="sxs-lookup"><span data-stu-id="b3730-163">The channels must be listed in the order r, g, b, a - for example, register.rba, which updates the red, blue, and alpha channels of the destination.</span></span> <span data-ttu-id="b3730-164">La máscara arbitraria está disponible en la versión 1 \_ 4 o superior.</span><span class="sxs-lookup"><span data-stu-id="b3730-164">The arbitrary mask is available in version 1\_4 or higher.</span></span>

<span data-ttu-id="b3730-165">Si no se especifica ninguna máscara de escritura de destino, el valor predeterminado de la máscara de escritura de destino es el caso RGBA.</span><span class="sxs-lookup"><span data-stu-id="b3730-165">If no destination write mask is specified, the destination write mask defaults to the rgba case.</span></span> <span data-ttu-id="b3730-166">Es decir, se actualizan todos los canales del registro de destino.</span><span class="sxs-lookup"><span data-stu-id="b3730-166">In other words, all channels in the destination register are updated.</span></span>

<span data-ttu-id="b3730-167">En las versiones 1 \_ a 1 \_ 3, la instrucción aritmética [DP3-PS](dp3---ps.md) DP3 solo puede usar las máscaras de escritura de salida. RGB o. RGBA.</span><span class="sxs-lookup"><span data-stu-id="b3730-167">For versions 1\_0 to 1\_3, the [dp3 - ps](dp3---ps.md) dp3 arithmetic instruction can use only the .rgb or .rgba output write masks.</span></span>

<span data-ttu-id="b3730-168">Las máscaras de escritura del registro de destino solo se admiten para las operaciones aritméticas.</span><span class="sxs-lookup"><span data-stu-id="b3730-168">Destination register write masks are supported for arithmetic operations only.</span></span> <span data-ttu-id="b3730-169">No se pueden usar en instrucciones de direccionamiento de textura, con la excepción de las instrucciones de la versión 1 \_ , [texcrd-PS](texcrd---ps.md) y [texld-PS \_ 2 \_ y versiones up](texld---ps-2-0.md).</span><span class="sxs-lookup"><span data-stu-id="b3730-169">They cannot be used on texture addressing instructions, with the exception of the version 1\_4 instructions, [texcrd - ps](texcrd---ps.md) and [texld - ps\_2\_0 and up](texld---ps-2-0.md).</span></span>

<span data-ttu-id="b3730-170">El valor predeterminado es escribir los cuatro canales de color.</span><span class="sxs-lookup"><span data-stu-id="b3730-170">The default is to write all four color channels.</span></span>


```
// All four color channels can be written by explicitly listing them.
mul r0.rgba, t0, v0

// Or, the default mask can be used to write all four channels.
mul r0, t0, v0
```



<span data-ttu-id="b3730-171">También se hace referencia a la máscara de escritura alfa como máscara de escritura escalar, ya que utiliza la canalización escalar.</span><span class="sxs-lookup"><span data-stu-id="b3730-171">The alpha write mask is also referred to as the scalar write mask, because it uses the scalar pipeline.</span></span>


```
add r0.a, t1, v1
```



<span data-ttu-id="b3730-172">Por lo tanto, esta instrucción coloca eficazmente la suma del componente alfa de T1 y el componente alfa de V1 en R0. a.</span><span class="sxs-lookup"><span data-stu-id="b3730-172">So this instruction effectively puts the sum of the alpha component of t1 and the alpha component of v1 into r0.a.</span></span>

<span data-ttu-id="b3730-173">La máscara de escritura de color se utiliza para controlar la escritura en los canales de color.</span><span class="sxs-lookup"><span data-stu-id="b3730-173">The color write mask is used to control writing to the color channels.</span></span>


```
// The color write mask is also referred to as the vector write mask, 
//   because it uses the vector pipeline.
mul r0.rgb, t0, v0
```



<span data-ttu-id="b3730-174">\_En el caso de la versión 4, las máscaras de escritura de destino se pueden usar en cualquier combinación siempre que las máscaras se ordenen como r, g, b, a.</span><span class="sxs-lookup"><span data-stu-id="b3730-174">For version 1\_4, destination write masks can be used in any combination as long as the masks are ordered r,g,b,a.</span></span>


```
// This example updates the red, blue, and alpha channels.
mov r0.rba, r1
```



<span data-ttu-id="b3730-175">Una instrucción de emisión conjunta permite que dos instrucciones potencialmente diferentes se emitan simultáneamente.</span><span class="sxs-lookup"><span data-stu-id="b3730-175">A co-issued instruction allows two potentially different instructions to be issued simultaneously.</span></span> <span data-ttu-id="b3730-176">Esto se consigue mediante la ejecución de las instrucciones de la canalización alfa y la canalización RGB.</span><span class="sxs-lookup"><span data-stu-id="b3730-176">This is accomplished by executing the instructions in the alpha pipeline and the RGB pipeline.</span></span>


```
  mul r0.rgb, t0, v0
+ add r1.a,   t1, c1
```



<span data-ttu-id="b3730-177">La ventaja de las instrucciones de emparejamiento de este modo es que permite realizar diferentes operaciones en el vector y en la canalización escalar en paralelo.</span><span class="sxs-lookup"><span data-stu-id="b3730-177">The advantage of pairing instructions this way is that it allows different operations to be performed in the vector and scalar pipeline in parallel.</span></span>

<span data-ttu-id="b3730-178">Estos registros de salida del sombreador de vértices están restringidos a las siguientes máscaras de escritura:</span><span class="sxs-lookup"><span data-stu-id="b3730-178">These vertex shader output registers are restricted to the following write masks:</span></span>



| <span data-ttu-id="b3730-179">Tipo de registro</span><span class="sxs-lookup"><span data-stu-id="b3730-179">Register Type</span></span> | <span data-ttu-id="b3730-180">Máscara de escritura necesaria</span><span class="sxs-lookup"><span data-stu-id="b3730-180">Required Write Mask</span></span>                                              |
|---------------|------------------------------------------------------------------|
| <span data-ttu-id="b3730-181">oFog</span><span class="sxs-lookup"><span data-stu-id="b3730-181">oFog</span></span>          | <span data-ttu-id="b3730-182">no se permite ninguna máscara de escritura explícita en este registro escalar</span><span class="sxs-lookup"><span data-stu-id="b3730-182">no explicit write mask is allowed on this scalar register</span></span>        |
| <span data-ttu-id="b3730-183">Aporta</span><span class="sxs-lookup"><span data-stu-id="b3730-183">oPts</span></span>          | <span data-ttu-id="b3730-184">no se permite ninguna máscara de escritura explícita en este registro escalar</span><span class="sxs-lookup"><span data-stu-id="b3730-184">no explicit write mask is allowed on this scalar register</span></span>        |
| <span data-ttu-id="b3730-185">oPos</span><span class="sxs-lookup"><span data-stu-id="b3730-185">oPos</span></span>          | <span data-ttu-id="b3730-186">. xyzw (que es el valor predeterminado)</span><span class="sxs-lookup"><span data-stu-id="b3730-186">.xyzw(which is the default)</span></span>                                      |
| <span data-ttu-id="b3730-187">OTR\#</span><span class="sxs-lookup"><span data-stu-id="b3730-187">oT\#</span></span>          | <span data-ttu-id="b3730-188">máscara combinada:. x \| . XY \| . XYZ \| . xyzw (que es el valor predeterminado)</span><span class="sxs-lookup"><span data-stu-id="b3730-188">combined mask: .x \| .xy \| .xyz \| .xyzw (which is the default)</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="b3730-189">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b3730-189">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b3730-190">Modificadores de registro del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="b3730-190">Pixel Shader Register Modifiers</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers.md)
</dt> </dl>

 

 




