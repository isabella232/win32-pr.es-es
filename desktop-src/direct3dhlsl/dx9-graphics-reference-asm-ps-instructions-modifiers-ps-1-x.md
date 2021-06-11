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
ms.openlocfilehash: 6c97196040a8f5f9888cb2fb354dcc18ca3743c7
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/10/2021
ms.locfileid: "111988730"
---
# <a name="modifiers-for-ps_1_x"></a><span data-ttu-id="71d68-104">Modificadores para ps \_ 1 \_ X</span><span class="sxs-lookup"><span data-stu-id="71d68-104">Modifiers for ps\_1\_X</span></span>

<span data-ttu-id="71d68-105">Los modificadores de instrucción afectan al resultado de la instrucción antes de que se escriba en el registro de destino.</span><span class="sxs-lookup"><span data-stu-id="71d68-105">Instruction modifiers affect the result of the instruction before it is written into the destination register.</span></span> <span data-ttu-id="71d68-106">Por ejemplo, úsenlos para multiplicar o dividir el resultado por un factor de dos, o para fijar el resultado entre cero y uno.</span><span class="sxs-lookup"><span data-stu-id="71d68-106">For instance, use them to multiply or divide the result by a factor of two, or to clamp the result between zero and one.</span></span> <span data-ttu-id="71d68-107">Los modificadores de instrucción se aplican después de que se ejecute la instrucción, pero antes de escribir el resultado en el registro de destino.</span><span class="sxs-lookup"><span data-stu-id="71d68-107">Instruction modifiers are applied after the instruction runs but before writing the result to the destination register.</span></span>

<span data-ttu-id="71d68-108">A continuación se muestra una lista de los modificadores.</span><span class="sxs-lookup"><span data-stu-id="71d68-108">A list of the modifiers is shown below.</span></span>



| <span data-ttu-id="71d68-109">Modificador</span><span class="sxs-lookup"><span data-stu-id="71d68-109">Modifier</span></span> | <span data-ttu-id="71d68-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="71d68-110">Description</span></span>                   | <span data-ttu-id="71d68-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="71d68-111">Syntax</span></span>           | <span data-ttu-id="71d68-112">Versión</span><span class="sxs-lookup"><span data-stu-id="71d68-112">Version</span></span> |      |      |      |
|----------|-------------------------------|------------------|---------|------|------|------|
|          |                               |                  | <span data-ttu-id="71d68-113">1\_1</span><span class="sxs-lookup"><span data-stu-id="71d68-113">1\_1</span></span>    | <span data-ttu-id="71d68-114">1\_2</span><span class="sxs-lookup"><span data-stu-id="71d68-114">1\_2</span></span> | <span data-ttu-id="71d68-115">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="71d68-115">1\_3</span></span> | <span data-ttu-id="71d68-116">1\_4</span><span class="sxs-lookup"><span data-stu-id="71d68-116">1\_4</span></span> |
| <span data-ttu-id="71d68-117">\_x2</span><span class="sxs-lookup"><span data-stu-id="71d68-117">\_x2</span></span>     | <span data-ttu-id="71d68-118">Multiplicar por 2</span><span class="sxs-lookup"><span data-stu-id="71d68-118">Multiply by 2</span></span>                 | <span data-ttu-id="71d68-119">instrucción \_ x2</span><span class="sxs-lookup"><span data-stu-id="71d68-119">instruction\_x2</span></span>  | <span data-ttu-id="71d68-120">X</span><span class="sxs-lookup"><span data-stu-id="71d68-120">X</span></span>       | <span data-ttu-id="71d68-121">X</span><span class="sxs-lookup"><span data-stu-id="71d68-121">X</span></span>    | <span data-ttu-id="71d68-122">X</span><span class="sxs-lookup"><span data-stu-id="71d68-122">X</span></span>    | <span data-ttu-id="71d68-123">X</span><span class="sxs-lookup"><span data-stu-id="71d68-123">X</span></span>    |
| <span data-ttu-id="71d68-124">\_x4</span><span class="sxs-lookup"><span data-stu-id="71d68-124">\_x4</span></span>     | <span data-ttu-id="71d68-125">Multiplicar por 4</span><span class="sxs-lookup"><span data-stu-id="71d68-125">Multiply by 4</span></span>                 | <span data-ttu-id="71d68-126">instrucción \_ x4</span><span class="sxs-lookup"><span data-stu-id="71d68-126">instruction\_x4</span></span>  | <span data-ttu-id="71d68-127">X</span><span class="sxs-lookup"><span data-stu-id="71d68-127">X</span></span>       | <span data-ttu-id="71d68-128">X</span><span class="sxs-lookup"><span data-stu-id="71d68-128">X</span></span>    | <span data-ttu-id="71d68-129">X</span><span class="sxs-lookup"><span data-stu-id="71d68-129">X</span></span>    | <span data-ttu-id="71d68-130">X</span><span class="sxs-lookup"><span data-stu-id="71d68-130">X</span></span>    |
| <span data-ttu-id="71d68-131">\_x8</span><span class="sxs-lookup"><span data-stu-id="71d68-131">\_x8</span></span>     | <span data-ttu-id="71d68-132">Multiplicar por 8</span><span class="sxs-lookup"><span data-stu-id="71d68-132">Multiply by 8</span></span>                 | <span data-ttu-id="71d68-133">instrucción \_ x8</span><span class="sxs-lookup"><span data-stu-id="71d68-133">instruction\_x8</span></span>  |         |      |      | <span data-ttu-id="71d68-134">X</span><span class="sxs-lookup"><span data-stu-id="71d68-134">X</span></span>    |
| <span data-ttu-id="71d68-135">\_d2</span><span class="sxs-lookup"><span data-stu-id="71d68-135">\_d2</span></span>     | <span data-ttu-id="71d68-136">Dividir entre 2</span><span class="sxs-lookup"><span data-stu-id="71d68-136">Divide by 2</span></span>                   | <span data-ttu-id="71d68-137">instrucción \_ d2</span><span class="sxs-lookup"><span data-stu-id="71d68-137">instruction\_d2</span></span>  | <span data-ttu-id="71d68-138">X</span><span class="sxs-lookup"><span data-stu-id="71d68-138">X</span></span>       | <span data-ttu-id="71d68-139">X</span><span class="sxs-lookup"><span data-stu-id="71d68-139">X</span></span>    | <span data-ttu-id="71d68-140">X</span><span class="sxs-lookup"><span data-stu-id="71d68-140">X</span></span>    | <span data-ttu-id="71d68-141">X</span><span class="sxs-lookup"><span data-stu-id="71d68-141">X</span></span>    |
| <span data-ttu-id="71d68-142">\_d4</span><span class="sxs-lookup"><span data-stu-id="71d68-142">\_d4</span></span>     | <span data-ttu-id="71d68-143">Dividir entre 4</span><span class="sxs-lookup"><span data-stu-id="71d68-143">Divide by 4</span></span>                   | <span data-ttu-id="71d68-144">instrucción \_ d4</span><span class="sxs-lookup"><span data-stu-id="71d68-144">instruction\_d4</span></span>  |         |      |      | <span data-ttu-id="71d68-145">X</span><span class="sxs-lookup"><span data-stu-id="71d68-145">X</span></span>    |
| <span data-ttu-id="71d68-146">\_d8</span><span class="sxs-lookup"><span data-stu-id="71d68-146">\_d8</span></span>     | <span data-ttu-id="71d68-147">Dividir entre 8</span><span class="sxs-lookup"><span data-stu-id="71d68-147">Divide by 8</span></span>                   | <span data-ttu-id="71d68-148">instrucción \_ d8</span><span class="sxs-lookup"><span data-stu-id="71d68-148">instruction\_d8</span></span>  |         |      |      | <span data-ttu-id="71d68-149">X</span><span class="sxs-lookup"><span data-stu-id="71d68-149">X</span></span>    |
| <span data-ttu-id="71d68-150">\_Sentado</span><span class="sxs-lookup"><span data-stu-id="71d68-150">\_sat</span></span>    | <span data-ttu-id="71d68-151">Saturación (fijación de 0 y 1)</span><span class="sxs-lookup"><span data-stu-id="71d68-151">Saturate (clamp from 0 and 1)</span></span> | <span data-ttu-id="71d68-152">instrucción \_ sat</span><span class="sxs-lookup"><span data-stu-id="71d68-152">instruction\_sat</span></span> | <span data-ttu-id="71d68-153">X</span><span class="sxs-lookup"><span data-stu-id="71d68-153">X</span></span>       | <span data-ttu-id="71d68-154">X</span><span class="sxs-lookup"><span data-stu-id="71d68-154">X</span></span>    | <span data-ttu-id="71d68-155">X</span><span class="sxs-lookup"><span data-stu-id="71d68-155">X</span></span>    | <span data-ttu-id="71d68-156">X</span><span class="sxs-lookup"><span data-stu-id="71d68-156">X</span></span>    |



 

-   <span data-ttu-id="71d68-157">El modificador de multiplicación multiplica los datos de registro por una potencia de dos después de leerse.</span><span class="sxs-lookup"><span data-stu-id="71d68-157">The multiply modifier multiplies the register data by a power of two after it is read.</span></span> <span data-ttu-id="71d68-158">Esto es lo mismo que un desplazamiento a la izquierda.</span><span class="sxs-lookup"><span data-stu-id="71d68-158">This is the same as a shift left.</span></span>
-   <span data-ttu-id="71d68-159">El modificador de división divide los datos de registro por una potencia de dos después de leerlos.</span><span class="sxs-lookup"><span data-stu-id="71d68-159">The divide modifier divides the register data by a power of two after it is read.</span></span> <span data-ttu-id="71d68-160">Esto es lo mismo que un desplazamiento a la derecha.</span><span class="sxs-lookup"><span data-stu-id="71d68-160">This is the same as a shift right.</span></span>
-   <span data-ttu-id="71d68-161">El modificador saturate fija el intervalo de valores de registro de cero a uno.</span><span class="sxs-lookup"><span data-stu-id="71d68-161">The saturate modifier clamps the range of register values from zero to one.</span></span>

<span data-ttu-id="71d68-162">Los modificadores de instrucción se pueden usar en instrucciones aritméticas.</span><span class="sxs-lookup"><span data-stu-id="71d68-162">Instruction modifiers can be used on arithmetic instructions.</span></span> <span data-ttu-id="71d68-163">No se pueden usar en instrucciones de dirección de textura.</span><span class="sxs-lookup"><span data-stu-id="71d68-163">They may not be used on texture address instructions.</span></span>

<span data-ttu-id="71d68-164">Multiplicación del modificador</span><span class="sxs-lookup"><span data-stu-id="71d68-164">Multiply modifier</span></span>

<span data-ttu-id="71d68-165">En este ejemplo se carga el registro de destino (dest) con la suma de los dos colores de los operandos de origen (src0 y src1) y se multiplica el resultado por dos.</span><span class="sxs-lookup"><span data-stu-id="71d68-165">This example loads the destination register (dest) with the sum of the two colors in the source operands (src0 and src1) and multiplies the result by two.</span></span>


```
add_x2 dest, src0, src1
```



<span data-ttu-id="71d68-166">En este ejemplo se combinan dos modificadores de instrucción.</span><span class="sxs-lookup"><span data-stu-id="71d68-166">This example combines two instruction modifiers.</span></span> <span data-ttu-id="71d68-167">En primer lugar, se agregan dos colores en los operandos de origen (src0 y src1).</span><span class="sxs-lookup"><span data-stu-id="71d68-167">First, two colors in the source operands (src0 and src1) are added.</span></span> <span data-ttu-id="71d68-168">A continuación, el resultado se multiplica por dos y se fija entre 0,0 y 1,0 para cada componente.</span><span class="sxs-lookup"><span data-stu-id="71d68-168">The result is then multiplied by two, and clamped between 0.0 to 1.0 for each component.</span></span> <span data-ttu-id="71d68-169">El resultado se guarda en el registro de destino.</span><span class="sxs-lookup"><span data-stu-id="71d68-169">The result is saved in the destination register.</span></span>


```
add_x2_sat dest, src0, src1
```



<span data-ttu-id="71d68-170">Modificador de división</span><span class="sxs-lookup"><span data-stu-id="71d68-170">Divide modifier</span></span>

<span data-ttu-id="71d68-171">En este ejemplo se carga el registro de destino (dest) con la suma de los dos colores de los operandos de origen (src0 y src1) y se divide el resultado entre dos.</span><span class="sxs-lookup"><span data-stu-id="71d68-171">This example loads the destination register (dest) with the sum of the two colors in the source operands (src0 and src1) and divides the result by two.</span></span>


```
add_d2 dest, src0, src1
```



<span data-ttu-id="71d68-172">Modificador Saturate</span><span class="sxs-lookup"><span data-stu-id="71d68-172">Saturate modifier</span></span>

<span data-ttu-id="71d68-173">Para las instrucciones aritméticas, el modificador de saturación fija el resultado de esta instrucción en el intervalo de 0,0 a 1,0 para cada componente.</span><span class="sxs-lookup"><span data-stu-id="71d68-173">For arithmetic instructions, the saturation modifier clamps the result of this instruction into the range 0.0 to 1.0 for each component.</span></span> <span data-ttu-id="71d68-174">En el ejemplo siguiente se muestra cómo usar este modificador de instrucción.</span><span class="sxs-lookup"><span data-stu-id="71d68-174">The following example shows how to use this instruction modifier.</span></span>


```
dp3_sat r0, t0_bx2, v0_bx2    ; t0 is bump, v0 is light direction
```



<span data-ttu-id="71d68-175">Esta operación se produce después de cualquier modificador de instrucción de multiplicación o división.</span><span class="sxs-lookup"><span data-stu-id="71d68-175">This operation occurs after any multiply or divide instruction modifier.</span></span> <span data-ttu-id="71d68-176">\_sat se usa con mayor frecuencia para fijar los resultados del producto de punto.</span><span class="sxs-lookup"><span data-stu-id="71d68-176">\_sat is most often used to clamp dot product results.</span></span> <span data-ttu-id="71d68-177">Sin embargo, también permite la emulación coherente de métodos multipass donde el búfer de fotogramas siempre está en el intervalo de 0 a 1, y de la sintaxis multitexture de DirectX 6 y 7.0, en la que se define la saturación para que se produzca en cada fase.</span><span class="sxs-lookup"><span data-stu-id="71d68-177">However, it also enables consistent emulation of multipass methods where the frame buffer is always in the range 0 to 1, and of DirectX 6 and 7.0 multitexture syntax, in which saturation is defined to occur at every stage.</span></span>

<span data-ttu-id="71d68-178">En este ejemplo se carga el registro de destino (dest) con la suma de los dos colores de los operandos de origen (src0 y src1) y se fija el resultado en el intervalo de 0,0 a 1,0 para cada componente.</span><span class="sxs-lookup"><span data-stu-id="71d68-178">This example loads the destination register (dest) with the sum of the two colors in the source operands (src0 and src1), and clamps the result into the range 0.0 to 1.0 for each component.</span></span>


```
add_sat dest, src0, src1
```



<span data-ttu-id="71d68-179">En este ejemplo se combinan dos modificadores de instrucción.</span><span class="sxs-lookup"><span data-stu-id="71d68-179">This example combines two instruction modifiers.</span></span> <span data-ttu-id="71d68-180">En primer lugar, se agregan dos colores en los operandos de origen (src0 y src1).</span><span class="sxs-lookup"><span data-stu-id="71d68-180">First, two colors in the source operands (src0 and src1) are added.</span></span> <span data-ttu-id="71d68-181">El resultado se multiplica por dos y se fija entre 0,0 y 1,0 para cada componente.</span><span class="sxs-lookup"><span data-stu-id="71d68-181">The result is multiplied by two and clamped between 0.0 to 1.0 for each component.</span></span> <span data-ttu-id="71d68-182">El resultado se guarda en el registro de destino.</span><span class="sxs-lookup"><span data-stu-id="71d68-182">The result is saved in the destination register.</span></span>


```
add_x2_sat dest, src0, src1
```



## <a name="related-topics"></a><span data-ttu-id="71d68-183">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="71d68-183">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="71d68-184">Instrucciones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="71d68-184">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




