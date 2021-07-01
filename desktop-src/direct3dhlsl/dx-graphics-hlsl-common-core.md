---
title: Common-Shader Core
description: Common-Shader Core
ms.assetid: f3cf2969-83a4-461f-8177-d336536194ba
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 66c1f763c4771a8406acd2f3401445d1a29cde79
ms.sourcegitcommit: 7e4322a6ec1f964d5ad26e2e5e06cc8ce840030e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/01/2021
ms.locfileid: "113129722"
---
# <a name="common-shader-core"></a><span data-ttu-id="092a0-103">Common-Shader Core</span><span class="sxs-lookup"><span data-stu-id="092a0-103">Common-Shader Core</span></span>

<span data-ttu-id="092a0-104">En El modelo de sombreador 4, todas las fases del sombreador implementan la misma funcionalidad base mediante un núcleo de sombreador común.</span><span class="sxs-lookup"><span data-stu-id="092a0-104">In Shader Model 4, all shader stages implement the same base functionality using a common-shader core.</span></span> <span data-ttu-id="092a0-105">Además, cada una de las tres fases del sombreador (vértice, geometría y píxel) ofrece una funcionalidad única para cada fase, como la capacidad de generar nuevas primitivas a partir de la fase del sombreador de geometría o descartar un píxel específico en la fase del sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="092a0-105">In addition, each of the three shader stages (vertex, geometry, and pixel) offer functionality unique to each stage, such as the ability to generate new primitives from the geometry shader stage or to discard a specific pixel in the pixel shader stage.</span></span> <span data-ttu-id="092a0-106">En el diagrama siguiente se muestra cómo fluyen los datos a través de una fase del sombreador y la relación del núcleo de sombreador común con los recursos de memoria del sombreador.</span><span class="sxs-lookup"><span data-stu-id="092a0-106">The following diagram shows how data flows through a shader stage, and the relationship of the common-shader core with shader memory resources.</span></span>

![diagrama de flujo de datos en una fase de sombreador](images/d3d10-shader-unit.png)

-   <span data-ttu-id="092a0-108">**Datos de entrada:** un sombreador de vértices recibe sus entradas de la fase del ensamblador de entrada; Los sombreadores de geometría y píxel reciben sus entradas de la fase anterior del sombreador.</span><span class="sxs-lookup"><span data-stu-id="092a0-108">**Input Data**: A vertex shader receives its inputs from the input assembler stage; geometry and pixel shaders receive their inputs from the previous shader stage.</span></span> <span data-ttu-id="092a0-109">Entre las entradas adicionales se [incluye la semántica de](dx-graphics-hlsl-semantics.md)valor del sistema, que se puede consumir mediante la primera unidad de la canalización a la que son aplicables.</span><span class="sxs-lookup"><span data-stu-id="092a0-109">Additional inputs include [system-value semantics](dx-graphics-hlsl-semantics.md), which are consumable by the first unit in the pipeline to which they are applicable.</span></span>
-   <span data-ttu-id="092a0-110">**Datos de salida:** los sombreadores generan resultados de salida que se pasarán a la fase posterior de la canalización.</span><span class="sxs-lookup"><span data-stu-id="092a0-110">**Output Data**: Shaders generate output results to be passed onto the subsequent stage in the pipeline.</span></span> <span data-ttu-id="092a0-111">Para un sombreador de geometría, la cantidad de salida de datos de una única invocación puede variar.</span><span class="sxs-lookup"><span data-stu-id="092a0-111">For a geometry shader, the amount of data output from a single invocation can vary.</span></span> <span data-ttu-id="092a0-112">Algunas salidas se interpretan mediante el núcleo común del sombreador (como la posición de los vértices y el índice render-target-array), mientras que otras están diseñadas para ser interpretadas por una aplicación.</span><span class="sxs-lookup"><span data-stu-id="092a0-112">Some outputs are interpreted by the common-shader core (such as vertex position and render-target-array index), others are designed to be interpreted by an application.</span></span>
-   <span data-ttu-id="092a0-113">**Código de sombreador:** los sombreadores pueden leer desde la memoria, realizar operaciones aritméticas de punto flotante vectorial y entero o operaciones de control de flujo.</span><span class="sxs-lookup"><span data-stu-id="092a0-113">**Shader Code**: Shaders can read from memory, perform vector floating point and integer arithmetic operations, or flow control operations.</span></span> <span data-ttu-id="092a0-114">No hay ningún límite en el número de instrucciones que se pueden implementar en un sombreador.</span><span class="sxs-lookup"><span data-stu-id="092a0-114">There is no limit to the number of statements that can be implemented in a shader.</span></span>
-   <span data-ttu-id="092a0-115">**Muestreadores:** los muestreadores definen cómo muestrear y filtrar texturas.</span><span class="sxs-lookup"><span data-stu-id="092a0-115">**Samplers**: Samplers define how to sample and filter textures.</span></span> <span data-ttu-id="092a0-116">Se pueden enlazar hasta 16 muestreadores a un sombreador simultáneamente.</span><span class="sxs-lookup"><span data-stu-id="092a0-116">As many as 16 samplers can be bound to a shader simultaneously.</span></span>
-   <span data-ttu-id="092a0-117">**Texturas:** las texturas se pueden filtrar mediante muestreadores o leerse por texel directamente con la [función intrínseca](dx-graphics-hlsl-to-load.md) de carga.</span><span class="sxs-lookup"><span data-stu-id="092a0-117">**Textures**: Textures can be filtered using samplers or read on a per-texel basis directly with the [load](dx-graphics-hlsl-to-load.md) intrinsic function.</span></span>
-   <span data-ttu-id="092a0-118">**Búferes:** los búferes nunca se filtran, pero se pueden leer de la memoria por elemento directamente con la [función intrínseca](dx-graphics-hlsl-to-load.md) de carga.</span><span class="sxs-lookup"><span data-stu-id="092a0-118">**Buffers**: Buffers are never filtered, but can be read from memory on a per-element basis directly with the [load](dx-graphics-hlsl-to-load.md) intrinsic function.</span></span> <span data-ttu-id="092a0-119">Se pueden enlazar hasta 128 recursos de textura y búfer (combinados) a un sombreador simultáneamente.</span><span class="sxs-lookup"><span data-stu-id="092a0-119">As many as 128 texture and buffer resources (combined) can be bound to a shader simultaneously.</span></span>
-   <span data-ttu-id="092a0-120">**Búferes constantes:** los búferes constantes están optimizados para las variables constantes del sombreador.</span><span class="sxs-lookup"><span data-stu-id="092a0-120">**Constant Buffers**: Constant buffers are optimized for shader constant-variables.</span></span> <span data-ttu-id="092a0-121">Se pueden enlazar hasta 16 búferes constantes a una fase del sombreador simultáneamente.</span><span class="sxs-lookup"><span data-stu-id="092a0-121">As many as 16 constant buffers can be bound to a shader stage simultaneously.</span></span> <span data-ttu-id="092a0-122">Están diseñados para una actualización más frecuente desde la CPU; por lo tanto, tienen restricciones de tamaño, diseño y acceso adicionales.</span><span class="sxs-lookup"><span data-stu-id="092a0-122">They are designed for more frequent update from the CPU; therefore, they have additional size, layout, and access restrictions.</span></span>


<span data-ttu-id="092a0-123">Diferencias entre Direct3D 9 y Direct3D 10:</span><span class="sxs-lookup"><span data-stu-id="092a0-123">Differences between Direct3D 9 and Direct3D 10:</span></span>

- <span data-ttu-id="092a0-124">En Direct3D 9, cada unidad de sombreador tenía un único archivo de registro constante pequeño para almacenar todas las variables de sombreador constantes.</span><span class="sxs-lookup"><span data-stu-id="092a0-124">In Direct3D 9, each shader unit had a single, small constant register file to store all constant shader variables.</span></span> <span data-ttu-id="092a0-125">La compatibilidad de todos los sombreadores con este espacio constante limitado requería el reciclaje frecuente de constantes por parte de la CPU.</span><span class="sxs-lookup"><span data-stu-id="092a0-125">Accommodating all shaders with this limited constant space required frequent recycling of constants by the CPU.</span></span>
- <span data-ttu-id="092a0-126">En Direct3D 10, las constantes se almacenan en búferes inmutables en memoria y se administran como cualquier otro recurso.</span><span class="sxs-lookup"><span data-stu-id="092a0-126">In Direct3D 10, constants are stored in immutable buffers in memory and are managed like any other resource.</span></span> <span data-ttu-id="092a0-127">No hay ningún límite en el número de búferes constantes que una aplicación puede crear.</span><span class="sxs-lookup"><span data-stu-id="092a0-127">There is no limit to the number of constant buffers an application can create.</span></span> <span data-ttu-id="092a0-128">Al organizar las constantes en búferes por frecuencia de actualización y uso, se puede reducir considerablemente la cantidad de ancho de banda necesario para actualizar las constantes para dar cabida a todos los sombreadores.</span><span class="sxs-lookup"><span data-stu-id="092a0-128">By organizing constants into buffers by frequency of update and usage, the amount of bandwidth required to update constants to accommodate all shaders can be significantly reduced.</span></span>



 

## <a name="integer-and-bitwise-support"></a><span data-ttu-id="092a0-129">Compatibilidad con enteros y bit a bit</span><span class="sxs-lookup"><span data-stu-id="092a0-129">Integer and Bitwise Support</span></span>

<span data-ttu-id="092a0-130">El núcleo común del sombreador proporciona un conjunto completo de operaciones bit a bit y enteros de 32 bits compatibles con IEEE.</span><span class="sxs-lookup"><span data-stu-id="092a0-130">The common shader core provides a full set of IEEE-compliant 32-bit integer and bitwise operations.</span></span> <span data-ttu-id="092a0-131">Estas operaciones permiten una nueva clase de algoritmos en ejemplos de hardware gráfico, como técnicas de compresión y empaquetado, FFT y control de flujo de programa de campo de bits.</span><span class="sxs-lookup"><span data-stu-id="092a0-131">These operations enable a new class of algorithms in graphics hardware examples include compression and packing techniques, FFTs, and bitfield program-flow control.</span></span>

<span data-ttu-id="092a0-132">Los tipos de datos **int** **y uint** de Direct3D 10 HLSL se asignan a enteros de 32 bits en hardware.</span><span class="sxs-lookup"><span data-stu-id="092a0-132">The **int** and **uint** data types in Direct3D 10 HLSL map to 32-bit integers in hardware.</span></span>



|                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="092a0-133">Diferencias entre Direct3D 9 y Direct3D 10:</span><span class="sxs-lookup"><span data-stu-id="092a0-133">Differences between Direct3D 9 and Direct3D 10:</span></span><br/> <span data-ttu-id="092a0-134">En Direct3D 9, las entradas de flujo marcadas como enteros en HLSL se interpretaron como de punto flotante.</span><span class="sxs-lookup"><span data-stu-id="092a0-134">In Direct3D 9 stream inputs marked as integer in HLSL were interpreted as floating-point.</span></span> <span data-ttu-id="092a0-135">En Direct3D 10, las entradas de secuencia marcadas como enteros se interpretan como un entero de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="092a0-135">In Direct3D 10, stream inputs marked as integer are interpreted as a 32- bit integer.</span></span><br/> <span data-ttu-id="092a0-136">Además, los valores booleanos ahora son todos los bits establecidos o todos los bits sin establecer.</span><span class="sxs-lookup"><span data-stu-id="092a0-136">In addition, boolean values are now all bits set or all bits unset.</span></span> <span data-ttu-id="092a0-137">Los datos convertidos a **bool** se interpretarán como true si el valor no es igual a 0,0f (se permite que los ceros positivos y negativos sean false) y false en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="092a0-137">Data converted to **bool** will be interpreted as true if the value is not equal to 0.0f (both positive and negative zero are allowed to be false) and false otherwise.</span></span><br/> |



 

## <a name="bitwise-operators"></a><span data-ttu-id="092a0-138">Operadores bit a bit</span><span class="sxs-lookup"><span data-stu-id="092a0-138">Bitwise operators</span></span>

<span data-ttu-id="092a0-139">El núcleo común del sombreador admite los siguientes operadores bit a bit:</span><span class="sxs-lookup"><span data-stu-id="092a0-139">The common shader core supports the following bitwise operators:</span></span>



| <span data-ttu-id="092a0-140">Operador</span><span class="sxs-lookup"><span data-stu-id="092a0-140">Operator</span></span>  | <span data-ttu-id="092a0-141">Función</span><span class="sxs-lookup"><span data-stu-id="092a0-141">Function</span></span>          |
|-----------|-------------------|
| ~         | <span data-ttu-id="092a0-142">No lógico</span><span class="sxs-lookup"><span data-stu-id="092a0-142">Logical Not</span></span>       |
| <<  | <span data-ttu-id="092a0-143">Desplazamiento a la izquierda</span><span class="sxs-lookup"><span data-stu-id="092a0-143">Left Shift</span></span>        |
| >>  | <span data-ttu-id="092a0-144">Desplazamiento a la derecha</span><span class="sxs-lookup"><span data-stu-id="092a0-144">Right Shift</span></span>       |
| &         | <span data-ttu-id="092a0-145">Logical And</span><span class="sxs-lookup"><span data-stu-id="092a0-145">Logical And</span></span>       |
| \|        | <span data-ttu-id="092a0-146">Or lógico.</span><span class="sxs-lookup"><span data-stu-id="092a0-146">Logical Or</span></span>        |
| ^         | <span data-ttu-id="092a0-147">Xor lógico</span><span class="sxs-lookup"><span data-stu-id="092a0-147">Logical Xor</span></span>       |
| <<= | <span data-ttu-id="092a0-148">Desplazamiento a la izquierda Igual</span><span class="sxs-lookup"><span data-stu-id="092a0-148">Left shift Equal</span></span>  |
| >>= | <span data-ttu-id="092a0-149">Desplazamiento a la derecha igual</span><span class="sxs-lookup"><span data-stu-id="092a0-149">Right Shift Equal</span></span> |
| &=        | <span data-ttu-id="092a0-150">E igual</span><span class="sxs-lookup"><span data-stu-id="092a0-150">And Equal</span></span>         |
| \|=       | <span data-ttu-id="092a0-151">O igual</span><span class="sxs-lookup"><span data-stu-id="092a0-151">Or Equal</span></span>          |
| ^=        | <span data-ttu-id="092a0-152">Xor Equal</span><span class="sxs-lookup"><span data-stu-id="092a0-152">Xor Equal</span></span>         |



 

<span data-ttu-id="092a0-153">Los operadores bit a bit se definen para funcionar solo en tipos de datos **int** y **uint.**</span><span class="sxs-lookup"><span data-stu-id="092a0-153">Bitwise operators are defined to operate only on **int** and **uint** data types.</span></span> <span data-ttu-id="092a0-154">Si se intentan usar operadores bit a bit en tipos de datos **float** o **struct,** se producirá un error.</span><span class="sxs-lookup"><span data-stu-id="092a0-154">Attempting to use bitwise operators on **float** or **struct** data types will result in an error.</span></span> <span data-ttu-id="092a0-155">Los operadores bit a bit tienen la misma prioridad que C con respecto a otros operadores.</span><span class="sxs-lookup"><span data-stu-id="092a0-155">Bitwise operators follow the same precedence as C with regard to other operators.</span></span>

## <a name="binary-casts"></a><span data-ttu-id="092a0-156">Conversión binaria</span><span class="sxs-lookup"><span data-stu-id="092a0-156">Binary Casts</span></span>

<span data-ttu-id="092a0-157">La conversión entre un entero y un tipo de punto flotante convertirá el valor numérico siguiendo las reglas de truncamiento de C.</span><span class="sxs-lookup"><span data-stu-id="092a0-157">Casting between an integer and a floating-point type will convert the numeric value following C truncation rules.</span></span> <span data-ttu-id="092a0-158">Convertir un valor de **float** en **int** y volver a **float** es una conversión con pérdida que depende de la precisión del tipo de datos de destino.</span><span class="sxs-lookup"><span data-stu-id="092a0-158">Casting a value from a **float**, to an **int**, and back to a **float** is a lossy conversion dependent on the precision of the target data type.</span></span> <span data-ttu-id="092a0-159">Estas son algunas de las funciones de conversión: [**asfloat (DirectX HLSL)**](dx-graphics-hlsl-asfloat.md), [**asint (DirectX HLSL)**](dx-graphics-hlsl-asint.md), [**asuint (DirectX HLSL).**](dx-graphics-hlsl-asuint.md)</span><span class="sxs-lookup"><span data-stu-id="092a0-159">Here are some of the conversion functions: [**asfloat (DirectX HLSL)**](dx-graphics-hlsl-asfloat.md), [**asint (DirectX HLSL)**](dx-graphics-hlsl-asint.md), [**asuint (DirectX HLSL)**](dx-graphics-hlsl-asuint.md).</span></span>

<span data-ttu-id="092a0-160">Las conversión binarias también se pueden realizar mediante funciones intrínsecas HLSL.</span><span class="sxs-lookup"><span data-stu-id="092a0-160">Binary casts can also be performed using HLSL intrinsic functions.</span></span> <span data-ttu-id="092a0-161">Esto hace que el compilador reinterprete la representación de bits de un número en el tipo de datos de destino.</span><span class="sxs-lookup"><span data-stu-id="092a0-161">These cause the compiler to reinterpret the bit representation of a number into the target data type.</span></span>

## <a name="related-topics"></a><span data-ttu-id="092a0-162">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="092a0-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="092a0-163">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="092a0-163">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 





