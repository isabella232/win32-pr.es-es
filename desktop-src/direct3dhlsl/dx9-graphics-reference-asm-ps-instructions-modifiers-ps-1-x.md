---
title: Modificadores para ps_1_X
description: Los modificadores de instrucción afectan al resultado de la instrucción antes de que se escriba en el registro de destino. Obtenga información sobre los modificadores para ps_1_X.
ms.assetid: 15b892da-b6fd-4bd5-8889-bc48035e7819
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b9291d818252c95bc11fae72bd3311ec733a45fa
ms.sourcegitcommit: 7e4322a6ec1f964d5ad26e2e5e06cc8ce840030e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/01/2021
ms.locfileid: "113129944"
---
# <a name="modifiers-for-ps_1_x"></a><span data-ttu-id="2fc38-104">Modificadores para ps \_ 1 \_ X</span><span class="sxs-lookup"><span data-stu-id="2fc38-104">Modifiers for ps\_1\_X</span></span>

<span data-ttu-id="2fc38-105">Los modificadores de instrucción afectan al resultado de la instrucción antes de que se escriba en el registro de destino.</span><span class="sxs-lookup"><span data-stu-id="2fc38-105">Instruction modifiers affect the result of the instruction before it is written into the destination register.</span></span> <span data-ttu-id="2fc38-106">Por ejemplo, úsenlos para multiplicar o dividir el resultado por un factor de dos, o para fijar el resultado entre cero y uno.</span><span class="sxs-lookup"><span data-stu-id="2fc38-106">For instance, use them to multiply or divide the result by a factor of two, or to clamp the result between zero and one.</span></span> <span data-ttu-id="2fc38-107">Los modificadores de instrucción se aplican después de que se ejecute la instrucción, pero antes de escribir el resultado en el registro de destino.</span><span class="sxs-lookup"><span data-stu-id="2fc38-107">Instruction modifiers are applied after the instruction runs but before writing the result to the destination register.</span></span>

<span data-ttu-id="2fc38-108">A continuación se muestra una lista de los modificadores.</span><span class="sxs-lookup"><span data-stu-id="2fc38-108">A list of the modifiers is shown below.</span></span>



| <span data-ttu-id="2fc38-109">Modificador</span><span class="sxs-lookup"><span data-stu-id="2fc38-109">Modifier</span></span> | <span data-ttu-id="2fc38-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="2fc38-110">Description</span></span>                   | <span data-ttu-id="2fc38-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2fc38-111">Syntax</span></span>           | <span data-ttu-id="2fc38-112">Versión 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="2fc38-112">Version 1\_1</span></span> | <span data-ttu-id="2fc38-113">Versión 1 \_ 2</span><span class="sxs-lookup"><span data-stu-id="2fc38-113">Version 1\_2</span></span>     |<span data-ttu-id="2fc38-114">Versión 1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="2fc38-114">Version  1\_3</span></span>    | <span data-ttu-id="2fc38-115">Versión 1 \_ 4</span><span class="sxs-lookup"><span data-stu-id="2fc38-115">Version 1\_4</span></span>    |
|----------|-------------------------------|------------------|---------|------|------|------|
| <span data-ttu-id="2fc38-116">\_x2</span><span class="sxs-lookup"><span data-stu-id="2fc38-116">\_x2</span></span>     | <span data-ttu-id="2fc38-117">Multiplicar por 2</span><span class="sxs-lookup"><span data-stu-id="2fc38-117">Multiply by 2</span></span>                 | <span data-ttu-id="2fc38-118">instrucción \_ x2</span><span class="sxs-lookup"><span data-stu-id="2fc38-118">instruction\_x2</span></span>  | <span data-ttu-id="2fc38-119">X</span><span class="sxs-lookup"><span data-stu-id="2fc38-119">X</span></span>       | <span data-ttu-id="2fc38-120">X</span><span class="sxs-lookup"><span data-stu-id="2fc38-120">X</span></span>    | <span data-ttu-id="2fc38-121">X</span><span class="sxs-lookup"><span data-stu-id="2fc38-121">X</span></span>    | <span data-ttu-id="2fc38-122">X</span><span class="sxs-lookup"><span data-stu-id="2fc38-122">X</span></span>    |
| <span data-ttu-id="2fc38-123">\_x4</span><span class="sxs-lookup"><span data-stu-id="2fc38-123">\_x4</span></span>     | <span data-ttu-id="2fc38-124">Multiplicar por 4</span><span class="sxs-lookup"><span data-stu-id="2fc38-124">Multiply by 4</span></span>                 | <span data-ttu-id="2fc38-125">instrucción \_ x4</span><span class="sxs-lookup"><span data-stu-id="2fc38-125">instruction\_x4</span></span>  | <span data-ttu-id="2fc38-126">X</span><span class="sxs-lookup"><span data-stu-id="2fc38-126">X</span></span>       | <span data-ttu-id="2fc38-127">X</span><span class="sxs-lookup"><span data-stu-id="2fc38-127">X</span></span>    | <span data-ttu-id="2fc38-128">X</span><span class="sxs-lookup"><span data-stu-id="2fc38-128">X</span></span>    | <span data-ttu-id="2fc38-129">X</span><span class="sxs-lookup"><span data-stu-id="2fc38-129">X</span></span>    |
| <span data-ttu-id="2fc38-130">\_x8</span><span class="sxs-lookup"><span data-stu-id="2fc38-130">\_x8</span></span>     | <span data-ttu-id="2fc38-131">Multiplicar por 8</span><span class="sxs-lookup"><span data-stu-id="2fc38-131">Multiply by 8</span></span>                 | <span data-ttu-id="2fc38-132">instrucción \_ x8</span><span class="sxs-lookup"><span data-stu-id="2fc38-132">instruction\_x8</span></span>  |         |      |      | <span data-ttu-id="2fc38-133">X</span><span class="sxs-lookup"><span data-stu-id="2fc38-133">X</span></span>    |
| <span data-ttu-id="2fc38-134">\_d2</span><span class="sxs-lookup"><span data-stu-id="2fc38-134">\_d2</span></span>     | <span data-ttu-id="2fc38-135">Dividir entre 2</span><span class="sxs-lookup"><span data-stu-id="2fc38-135">Divide by 2</span></span>                   | <span data-ttu-id="2fc38-136">instrucción \_ d2</span><span class="sxs-lookup"><span data-stu-id="2fc38-136">instruction\_d2</span></span>  | <span data-ttu-id="2fc38-137">X</span><span class="sxs-lookup"><span data-stu-id="2fc38-137">X</span></span>       | <span data-ttu-id="2fc38-138">X</span><span class="sxs-lookup"><span data-stu-id="2fc38-138">X</span></span>    | <span data-ttu-id="2fc38-139">X</span><span class="sxs-lookup"><span data-stu-id="2fc38-139">X</span></span>    | <span data-ttu-id="2fc38-140">X</span><span class="sxs-lookup"><span data-stu-id="2fc38-140">X</span></span>    |
| <span data-ttu-id="2fc38-141">\_d4</span><span class="sxs-lookup"><span data-stu-id="2fc38-141">\_d4</span></span>     | <span data-ttu-id="2fc38-142">Dividir entre 4</span><span class="sxs-lookup"><span data-stu-id="2fc38-142">Divide by 4</span></span>                   | <span data-ttu-id="2fc38-143">instrucción \_ d4</span><span class="sxs-lookup"><span data-stu-id="2fc38-143">instruction\_d4</span></span>  |         |      |      | <span data-ttu-id="2fc38-144">X</span><span class="sxs-lookup"><span data-stu-id="2fc38-144">X</span></span>    |
| <span data-ttu-id="2fc38-145">\_d8</span><span class="sxs-lookup"><span data-stu-id="2fc38-145">\_d8</span></span>     | <span data-ttu-id="2fc38-146">Dividir entre 8</span><span class="sxs-lookup"><span data-stu-id="2fc38-146">Divide by 8</span></span>                   | <span data-ttu-id="2fc38-147">instrucción \_ d8</span><span class="sxs-lookup"><span data-stu-id="2fc38-147">instruction\_d8</span></span>  |         |      |      | <span data-ttu-id="2fc38-148">X</span><span class="sxs-lookup"><span data-stu-id="2fc38-148">X</span></span>    |
| <span data-ttu-id="2fc38-149">\_Sentado</span><span class="sxs-lookup"><span data-stu-id="2fc38-149">\_sat</span></span>    | <span data-ttu-id="2fc38-150">Saturar (fijación de 0 y 1)</span><span class="sxs-lookup"><span data-stu-id="2fc38-150">Saturate (clamp from 0 and 1)</span></span> | <span data-ttu-id="2fc38-151">instrucción \_ sat</span><span class="sxs-lookup"><span data-stu-id="2fc38-151">instruction\_sat</span></span> | <span data-ttu-id="2fc38-152">X</span><span class="sxs-lookup"><span data-stu-id="2fc38-152">X</span></span>       | <span data-ttu-id="2fc38-153">X</span><span class="sxs-lookup"><span data-stu-id="2fc38-153">X</span></span>    | <span data-ttu-id="2fc38-154">X</span><span class="sxs-lookup"><span data-stu-id="2fc38-154">X</span></span>    | <span data-ttu-id="2fc38-155">X</span><span class="sxs-lookup"><span data-stu-id="2fc38-155">X</span></span>    |



 

-   <span data-ttu-id="2fc38-156">El modificador de multiplicación multiplica los datos de registro por una potencia de dos después de leerse.</span><span class="sxs-lookup"><span data-stu-id="2fc38-156">The multiply modifier multiplies the register data by a power of two after it is read.</span></span> <span data-ttu-id="2fc38-157">Esto es lo mismo que un desplazamiento a la izquierda.</span><span class="sxs-lookup"><span data-stu-id="2fc38-157">This is the same as a shift left.</span></span>
-   <span data-ttu-id="2fc38-158">El modificador de división divide los datos de registro por una potencia de dos después de leerlos.</span><span class="sxs-lookup"><span data-stu-id="2fc38-158">The divide modifier divides the register data by a power of two after it is read.</span></span> <span data-ttu-id="2fc38-159">Esto es lo mismo que un desplazamiento a la derecha.</span><span class="sxs-lookup"><span data-stu-id="2fc38-159">This is the same as a shift right.</span></span>
-   <span data-ttu-id="2fc38-160">El modificador saturate fija el intervalo de valores de registro de cero a uno.</span><span class="sxs-lookup"><span data-stu-id="2fc38-160">The saturate modifier clamps the range of register values from zero to one.</span></span>

<span data-ttu-id="2fc38-161">Los modificadores de instrucción se pueden usar en instrucciones aritméticas.</span><span class="sxs-lookup"><span data-stu-id="2fc38-161">Instruction modifiers can be used on arithmetic instructions.</span></span> <span data-ttu-id="2fc38-162">No se pueden usar en instrucciones de dirección de textura.</span><span class="sxs-lookup"><span data-stu-id="2fc38-162">They may not be used on texture address instructions.</span></span>

<span data-ttu-id="2fc38-163">Multiplicación del modificador</span><span class="sxs-lookup"><span data-stu-id="2fc38-163">Multiply modifier</span></span>

<span data-ttu-id="2fc38-164">Este ejemplo carga el registro de destino (dest) con la suma de los dos colores de los operandos de origen (src0 y src1) y multiplica el resultado por dos.</span><span class="sxs-lookup"><span data-stu-id="2fc38-164">This example loads the destination register (dest) with the sum of the two colors in the source operands (src0 and src1) and multiplies the result by two.</span></span>


```
add_x2 dest, src0, src1
```



<span data-ttu-id="2fc38-165">En este ejemplo se combinan dos modificadores de instrucción.</span><span class="sxs-lookup"><span data-stu-id="2fc38-165">This example combines two instruction modifiers.</span></span> <span data-ttu-id="2fc38-166">En primer lugar, se agregan dos colores en los operandos de origen (src0 y src1).</span><span class="sxs-lookup"><span data-stu-id="2fc38-166">First, two colors in the source operands (src0 and src1) are added.</span></span> <span data-ttu-id="2fc38-167">A continuación, el resultado se multiplica por dos y se fija entre 0,0 y 1,0 para cada componente.</span><span class="sxs-lookup"><span data-stu-id="2fc38-167">The result is then multiplied by two, and clamped between 0.0 to 1.0 for each component.</span></span> <span data-ttu-id="2fc38-168">El resultado se guarda en el registro de destino.</span><span class="sxs-lookup"><span data-stu-id="2fc38-168">The result is saved in the destination register.</span></span>


```
add_x2_sat dest, src0, src1
```



<span data-ttu-id="2fc38-169">Modificador de división</span><span class="sxs-lookup"><span data-stu-id="2fc38-169">Divide modifier</span></span>

<span data-ttu-id="2fc38-170">En este ejemplo se carga el registro de destino (dest) con la suma de los dos colores de los operandos de origen (src0 y src1) y se divide el resultado entre dos.</span><span class="sxs-lookup"><span data-stu-id="2fc38-170">This example loads the destination register (dest) with the sum of the two colors in the source operands (src0 and src1) and divides the result by two.</span></span>


```
add_d2 dest, src0, src1
```



<span data-ttu-id="2fc38-171">Modificador Saturate</span><span class="sxs-lookup"><span data-stu-id="2fc38-171">Saturate modifier</span></span>

<span data-ttu-id="2fc38-172">Para las instrucciones aritméticas, el modificador de saturación fija el resultado de esta instrucción en el intervalo de 0,0 a 1,0 para cada componente.</span><span class="sxs-lookup"><span data-stu-id="2fc38-172">For arithmetic instructions, the saturation modifier clamps the result of this instruction into the range 0.0 to 1.0 for each component.</span></span> <span data-ttu-id="2fc38-173">En el ejemplo siguiente se muestra cómo usar este modificador de instrucción.</span><span class="sxs-lookup"><span data-stu-id="2fc38-173">The following example shows how to use this instruction modifier.</span></span>


```
dp3_sat r0, t0_bx2, v0_bx2    ; t0 is bump, v0 is light direction
```



<span data-ttu-id="2fc38-174">Esta operación se produce después de cualquier modificador de instrucción de multiplicación o división.</span><span class="sxs-lookup"><span data-stu-id="2fc38-174">This operation occurs after any multiply or divide instruction modifier.</span></span> <span data-ttu-id="2fc38-175">\_sat se usa con mayor frecuencia para fijar los resultados del producto de punto.</span><span class="sxs-lookup"><span data-stu-id="2fc38-175">\_sat is most often used to clamp dot product results.</span></span> <span data-ttu-id="2fc38-176">Sin embargo, también permite la emulación coherente de métodos multipass donde el búfer de fotogramas siempre está en el intervalo de 0 a 1, y de la sintaxis multitexture de DirectX 6 y 7.0, en la que se define la saturación para que se produzca en cada fase.</span><span class="sxs-lookup"><span data-stu-id="2fc38-176">However, it also enables consistent emulation of multipass methods where the frame buffer is always in the range 0 to 1, and of DirectX 6 and 7.0 multitexture syntax, in which saturation is defined to occur at every stage.</span></span>

<span data-ttu-id="2fc38-177">En este ejemplo se carga el registro de destino (dest) con la suma de los dos colores de los operandos de origen (src0 y src1) y se fija el resultado en el intervalo de 0,0 a 1,0 para cada componente.</span><span class="sxs-lookup"><span data-stu-id="2fc38-177">This example loads the destination register (dest) with the sum of the two colors in the source operands (src0 and src1), and clamps the result into the range 0.0 to 1.0 for each component.</span></span>


```
add_sat dest, src0, src1
```



<span data-ttu-id="2fc38-178">En este ejemplo se combinan dos modificadores de instrucción.</span><span class="sxs-lookup"><span data-stu-id="2fc38-178">This example combines two instruction modifiers.</span></span> <span data-ttu-id="2fc38-179">En primer lugar, se agregan dos colores en los operandos de origen (src0 y src1).</span><span class="sxs-lookup"><span data-stu-id="2fc38-179">First, two colors in the source operands (src0 and src1) are added.</span></span> <span data-ttu-id="2fc38-180">El resultado se multiplica por dos y se fija entre 0,0 y 1,0 para cada componente.</span><span class="sxs-lookup"><span data-stu-id="2fc38-180">The result is multiplied by two and clamped between 0.0 to 1.0 for each component.</span></span> <span data-ttu-id="2fc38-181">El resultado se guarda en el registro de destino.</span><span class="sxs-lookup"><span data-stu-id="2fc38-181">The result is saved in the destination register.</span></span>


```
add_x2_sat dest, src0, src1
```



## <a name="related-topics"></a><span data-ttu-id="2fc38-182">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2fc38-182">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2fc38-183">Instrucciones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="2fc38-183">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




