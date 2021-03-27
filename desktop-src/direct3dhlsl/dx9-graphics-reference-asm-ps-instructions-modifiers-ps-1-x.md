---
title: Modificadores para ps_1_X
description: Los modificadores de instrucción afectan al resultado de la instrucción antes de que se escriba en el registro de destino.
ms.assetid: 15b892da-b6fd-4bd5-8889-bc48035e7819
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bbc8a9b13f7ffc29cf84bc839409f29bea6c8c8b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903881"
---
# <a name="modifiers-for-ps_1_x"></a><span data-ttu-id="82256-103">Modificadores para PS \_ 1 \_ X</span><span class="sxs-lookup"><span data-stu-id="82256-103">Modifiers for ps\_1\_X</span></span>

<span data-ttu-id="82256-104">Los modificadores de instrucción afectan al resultado de la instrucción antes de que se escriba en el registro de destino.</span><span class="sxs-lookup"><span data-stu-id="82256-104">Instruction modifiers affect the result of the instruction before it is written into the destination register.</span></span> <span data-ttu-id="82256-105">Por ejemplo, úselos para multiplicar o dividir el resultado por un factor de dos, o para fijar el resultado entre cero y uno.</span><span class="sxs-lookup"><span data-stu-id="82256-105">For instance, use them to multiply or divide the result by a factor of two, or to clamp the result between zero and one.</span></span> <span data-ttu-id="82256-106">Los modificadores de instrucción se aplican después de que se ejecute la instrucción, pero antes de escribir el resultado en el registro de destino.</span><span class="sxs-lookup"><span data-stu-id="82256-106">Instruction modifiers are applied after the instruction runs but before writing the result to the destination register.</span></span>

<span data-ttu-id="82256-107">A continuación se muestra una lista de los modificadores.</span><span class="sxs-lookup"><span data-stu-id="82256-107">A list of the modifiers is shown below.</span></span>



| <span data-ttu-id="82256-108">Modificador</span><span class="sxs-lookup"><span data-stu-id="82256-108">Modifier</span></span> | <span data-ttu-id="82256-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="82256-109">Description</span></span>                   | <span data-ttu-id="82256-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="82256-110">Syntax</span></span>           | <span data-ttu-id="82256-111">Versión</span><span class="sxs-lookup"><span data-stu-id="82256-111">Version</span></span> |      |      |      |
|----------|-------------------------------|------------------|---------|------|------|------|
|          |                               |                  | <span data-ttu-id="82256-112">1\_1</span><span class="sxs-lookup"><span data-stu-id="82256-112">1\_1</span></span>    | <span data-ttu-id="82256-113">1\_2</span><span class="sxs-lookup"><span data-stu-id="82256-113">1\_2</span></span> | <span data-ttu-id="82256-114">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="82256-114">1\_3</span></span> | <span data-ttu-id="82256-115">1\_4</span><span class="sxs-lookup"><span data-stu-id="82256-115">1\_4</span></span> |
| <span data-ttu-id="82256-116">\_RCA</span><span class="sxs-lookup"><span data-stu-id="82256-116">\_x2</span></span>     | <span data-ttu-id="82256-117">Multiplicar por 2</span><span class="sxs-lookup"><span data-stu-id="82256-117">Multiply by 2</span></span>                 | <span data-ttu-id="82256-118">instrucción \_ x2</span><span class="sxs-lookup"><span data-stu-id="82256-118">instruction\_x2</span></span>  | <span data-ttu-id="82256-119">X</span><span class="sxs-lookup"><span data-stu-id="82256-119">X</span></span>       | <span data-ttu-id="82256-120">X</span><span class="sxs-lookup"><span data-stu-id="82256-120">X</span></span>    | <span data-ttu-id="82256-121">X</span><span class="sxs-lookup"><span data-stu-id="82256-121">X</span></span>    | <span data-ttu-id="82256-122">X</span><span class="sxs-lookup"><span data-stu-id="82256-122">X</span></span>    |
| <span data-ttu-id="82256-123">\_x4</span><span class="sxs-lookup"><span data-stu-id="82256-123">\_x4</span></span>     | <span data-ttu-id="82256-124">Multiplicar por 4</span><span class="sxs-lookup"><span data-stu-id="82256-124">Multiply by 4</span></span>                 | <span data-ttu-id="82256-125">instrucción \_ x4</span><span class="sxs-lookup"><span data-stu-id="82256-125">instruction\_x4</span></span>  | <span data-ttu-id="82256-126">X</span><span class="sxs-lookup"><span data-stu-id="82256-126">X</span></span>       | <span data-ttu-id="82256-127">X</span><span class="sxs-lookup"><span data-stu-id="82256-127">X</span></span>    | <span data-ttu-id="82256-128">X</span><span class="sxs-lookup"><span data-stu-id="82256-128">X</span></span>    | <span data-ttu-id="82256-129">X</span><span class="sxs-lookup"><span data-stu-id="82256-129">X</span></span>    |
| <span data-ttu-id="82256-130">\_canal</span><span class="sxs-lookup"><span data-stu-id="82256-130">\_x8</span></span>     | <span data-ttu-id="82256-131">Multiplicar por 8</span><span class="sxs-lookup"><span data-stu-id="82256-131">Multiply by 8</span></span>                 | <span data-ttu-id="82256-132">instrucción \_ x8</span><span class="sxs-lookup"><span data-stu-id="82256-132">instruction\_x8</span></span>  |         |      |      | <span data-ttu-id="82256-133">X</span><span class="sxs-lookup"><span data-stu-id="82256-133">X</span></span>    |
| <span data-ttu-id="82256-134">\_D2</span><span class="sxs-lookup"><span data-stu-id="82256-134">\_d2</span></span>     | <span data-ttu-id="82256-135">Dividir por 2</span><span class="sxs-lookup"><span data-stu-id="82256-135">Divide by 2</span></span>                   | <span data-ttu-id="82256-136">instrucción \_ D2</span><span class="sxs-lookup"><span data-stu-id="82256-136">instruction\_d2</span></span>  | <span data-ttu-id="82256-137">X</span><span class="sxs-lookup"><span data-stu-id="82256-137">X</span></span>       | <span data-ttu-id="82256-138">X</span><span class="sxs-lookup"><span data-stu-id="82256-138">X</span></span>    | <span data-ttu-id="82256-139">X</span><span class="sxs-lookup"><span data-stu-id="82256-139">X</span></span>    | <span data-ttu-id="82256-140">X</span><span class="sxs-lookup"><span data-stu-id="82256-140">X</span></span>    |
| <span data-ttu-id="82256-141">\_D4</span><span class="sxs-lookup"><span data-stu-id="82256-141">\_d4</span></span>     | <span data-ttu-id="82256-142">Dividir por 4</span><span class="sxs-lookup"><span data-stu-id="82256-142">Divide by 4</span></span>                   | <span data-ttu-id="82256-143">instrucción \_ D4</span><span class="sxs-lookup"><span data-stu-id="82256-143">instruction\_d4</span></span>  |         |      |      | <span data-ttu-id="82256-144">X</span><span class="sxs-lookup"><span data-stu-id="82256-144">X</span></span>    |
| <span data-ttu-id="82256-145">\_D8</span><span class="sxs-lookup"><span data-stu-id="82256-145">\_d8</span></span>     | <span data-ttu-id="82256-146">Dividir por 8</span><span class="sxs-lookup"><span data-stu-id="82256-146">Divide by 8</span></span>                   | <span data-ttu-id="82256-147">instrucción \_ D8</span><span class="sxs-lookup"><span data-stu-id="82256-147">instruction\_d8</span></span>  |         |      |      | <span data-ttu-id="82256-148">X</span><span class="sxs-lookup"><span data-stu-id="82256-148">X</span></span>    |
| <span data-ttu-id="82256-149">\_sábado</span><span class="sxs-lookup"><span data-stu-id="82256-149">\_sat</span></span>    | <span data-ttu-id="82256-150">Saturación (Clamp de 0 y 1)</span><span class="sxs-lookup"><span data-stu-id="82256-150">Saturate (clamp from 0 and 1)</span></span> | <span data-ttu-id="82256-151">instrucción \_ SAT</span><span class="sxs-lookup"><span data-stu-id="82256-151">instruction\_sat</span></span> | <span data-ttu-id="82256-152">X</span><span class="sxs-lookup"><span data-stu-id="82256-152">X</span></span>       | <span data-ttu-id="82256-153">X</span><span class="sxs-lookup"><span data-stu-id="82256-153">X</span></span>    | <span data-ttu-id="82256-154">X</span><span class="sxs-lookup"><span data-stu-id="82256-154">X</span></span>    | <span data-ttu-id="82256-155">X</span><span class="sxs-lookup"><span data-stu-id="82256-155">X</span></span>    |



 

-   <span data-ttu-id="82256-156">El modificador Multiply multiplica los datos de registro por una potencia de dos después de leerlos.</span><span class="sxs-lookup"><span data-stu-id="82256-156">The multiply modifier multiplies the register data by a power of two after it is read.</span></span> <span data-ttu-id="82256-157">Es lo mismo que un desplazamiento a la izquierda.</span><span class="sxs-lookup"><span data-stu-id="82256-157">This is the same as a shift left.</span></span>
-   <span data-ttu-id="82256-158">El modificador de división divide los datos de registro por una potencia de dos después de leerlos.</span><span class="sxs-lookup"><span data-stu-id="82256-158">The divide modifier divides the register data by a power of two after it is read.</span></span> <span data-ttu-id="82256-159">Es lo mismo que un desplazamiento a la derecha.</span><span class="sxs-lookup"><span data-stu-id="82256-159">This is the same as a shift right.</span></span>
-   <span data-ttu-id="82256-160">El modificador satura el intervalo de valores de registro de cero a uno.</span><span class="sxs-lookup"><span data-stu-id="82256-160">The saturate modifier clamps the range of register values from zero to one.</span></span>

<span data-ttu-id="82256-161">Los modificadores de instrucción se pueden utilizar en Instrucciones aritméticas.</span><span class="sxs-lookup"><span data-stu-id="82256-161">Instruction modifiers can be used on arithmetic instructions.</span></span> <span data-ttu-id="82256-162">No se pueden usar en instrucciones de dirección de textura.</span><span class="sxs-lookup"><span data-stu-id="82256-162">They may not be used on texture address instructions.</span></span>

<span data-ttu-id="82256-163">Multiply (modificador)</span><span class="sxs-lookup"><span data-stu-id="82256-163">Multiply modifier</span></span>

<span data-ttu-id="82256-164">En este ejemplo se carga el registro de destino (DEST) con la suma de los dos colores de los operandos de origen (src0 y SRC1) y se multiplica el resultado por dos.</span><span class="sxs-lookup"><span data-stu-id="82256-164">This example loads the destination register (dest) with the sum of the two colors in the source operands (src0 and src1) and multiplies the result by two.</span></span>


```
add_x2 dest, src0, src1
```



<span data-ttu-id="82256-165">En este ejemplo se combinan dos modificadores de instrucción.</span><span class="sxs-lookup"><span data-stu-id="82256-165">This example combines two instruction modifiers.</span></span> <span data-ttu-id="82256-166">En primer lugar, se agregan dos colores en los operandos de origen (src0 y SRC1).</span><span class="sxs-lookup"><span data-stu-id="82256-166">First, two colors in the source operands (src0 and src1) are added.</span></span> <span data-ttu-id="82256-167">El resultado se multiplica por dos y se fija entre 0,0 y 1,0 para cada componente.</span><span class="sxs-lookup"><span data-stu-id="82256-167">The result is then multiplied by two, and clamped between 0.0 to 1.0 for each component.</span></span> <span data-ttu-id="82256-168">El resultado se guarda en el registro de destino.</span><span class="sxs-lookup"><span data-stu-id="82256-168">The result is saved in the destination register.</span></span>


```
add_x2_sat dest, src0, src1
```



<span data-ttu-id="82256-169">Divide (modificador)</span><span class="sxs-lookup"><span data-stu-id="82256-169">Divide modifier</span></span>

<span data-ttu-id="82256-170">En este ejemplo se carga el registro de destino (DEST) con la suma de los dos colores de los operandos de origen (src0 y SRC1) y se divide el resultado entre dos.</span><span class="sxs-lookup"><span data-stu-id="82256-170">This example loads the destination register (dest) with the sum of the two colors in the source operands (src0 and src1) and divides the result by two.</span></span>


```
add_d2 dest, src0, src1
```



<span data-ttu-id="82256-171">Modificador de saturación</span><span class="sxs-lookup"><span data-stu-id="82256-171">Saturate modifier</span></span>

<span data-ttu-id="82256-172">En el caso de las instrucciones aritméticas, el modificador de saturación fija el resultado de esta instrucción en el intervalo de 0,0 a 1,0 para cada componente.</span><span class="sxs-lookup"><span data-stu-id="82256-172">For arithmetic instructions, the saturation modifier clamps the result of this instruction into the range 0.0 to 1.0 for each component.</span></span> <span data-ttu-id="82256-173">En el ejemplo siguiente se muestra cómo usar este modificador de instrucciones.</span><span class="sxs-lookup"><span data-stu-id="82256-173">The following example shows how to use this instruction modifier.</span></span>


```
dp3_sat r0, t0_bx2, v0_bx2    ; t0 is bump, v0 is light direction
```



<span data-ttu-id="82256-174">Esta operación se produce después de cualquier modificador de instrucción Multiply o de división.</span><span class="sxs-lookup"><span data-stu-id="82256-174">This operation occurs after any multiply or divide instruction modifier.</span></span> <span data-ttu-id="82256-175">\_SAT se usa con más frecuencia para Clamp los resultados de los productos de punto.</span><span class="sxs-lookup"><span data-stu-id="82256-175">\_sat is most often used to clamp dot product results.</span></span> <span data-ttu-id="82256-176">Sin embargo, también permite la emulación coherente de los métodos de Multipass en los que el búfer de fotogramas siempre está en el intervalo comprendido entre 0 y 1, y con la sintaxis multitexture de DirectX 6 y 7,0, en la que se define la saturación para que se produzca en cada fase.</span><span class="sxs-lookup"><span data-stu-id="82256-176">However, it also enables consistent emulation of multipass methods where the frame buffer is always in the range 0 to 1, and of DirectX 6 and 7.0 multitexture syntax, in which saturation is defined to occur at every stage.</span></span>

<span data-ttu-id="82256-177">En este ejemplo se carga el registro de destino (DEST) con la suma de los dos colores de los operandos de origen (src0 y SRC1) y se divide el resultado en el intervalo de 0,0 a 1,0 para cada componente.</span><span class="sxs-lookup"><span data-stu-id="82256-177">This example loads the destination register (dest) with the sum of the two colors in the source operands (src0 and src1), and clamps the result into the range 0.0 to 1.0 for each component.</span></span>


```
add_sat dest, src0, src1
```



<span data-ttu-id="82256-178">En este ejemplo se combinan dos modificadores de instrucción.</span><span class="sxs-lookup"><span data-stu-id="82256-178">This example combines two instruction modifiers.</span></span> <span data-ttu-id="82256-179">En primer lugar, se agregan dos colores en los operandos de origen (src0 y SRC1).</span><span class="sxs-lookup"><span data-stu-id="82256-179">First, two colors in the source operands (src0 and src1) are added.</span></span> <span data-ttu-id="82256-180">El resultado se multiplica por dos y se fija entre 0,0 y 1,0 para cada componente.</span><span class="sxs-lookup"><span data-stu-id="82256-180">The result is multiplied by two and clamped between 0.0 to 1.0 for each component.</span></span> <span data-ttu-id="82256-181">El resultado se guarda en el registro de destino.</span><span class="sxs-lookup"><span data-stu-id="82256-181">The result is saved in the destination register.</span></span>


```
add_x2_sat dest, src0, src1
```



## <a name="related-topics"></a><span data-ttu-id="82256-182">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="82256-182">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="82256-183">Instrucciones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="82256-183">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




