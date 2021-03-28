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
ms.openlocfilehash: e27ebe7d908c473890ac5b851eac3e0bc840c859
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903263"
---
# <a name="common-shader-core"></a><span data-ttu-id="e41a7-103">Common-Shader Core</span><span class="sxs-lookup"><span data-stu-id="e41a7-103">Common-Shader Core</span></span>

<span data-ttu-id="e41a7-104">En el modelo de sombreador 4, todas las fases del sombreador implementan la misma funcionalidad base mediante un núcleo común de sombreador.</span><span class="sxs-lookup"><span data-stu-id="e41a7-104">In Shader Model 4, all shader stages implement the same base functionality using a common-shader core.</span></span> <span data-ttu-id="e41a7-105">Además, cada una de las tres fases del sombreador (vértice, geometría y píxel) ofrecen una funcionalidad única para cada fase, como la capacidad de generar nuevos primitivos desde la fase del sombreador de geometría o para descartar un píxel específico en la fase del sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="e41a7-105">In addition, each of the three shader stages (vertex, geometry, and pixel) offer functionality unique to each stage, such as the ability to generate new primitives from the geometry shader stage or to discard a specific pixel in the pixel shader stage.</span></span> <span data-ttu-id="e41a7-106">En el diagrama siguiente se muestra cómo fluyen los datos a través de una fase del sombreador y la relación entre el núcleo común del sombreador y los recursos de la memoria del sombreador.</span><span class="sxs-lookup"><span data-stu-id="e41a7-106">The following diagram shows how data flows through a shader stage, and the relationship of the common-shader core with shader memory resources.</span></span>

![diagrama del flujo de datos en una fase del sombreador](images/d3d10-shader-unit.png)

-   <span data-ttu-id="e41a7-108">**Datos de entrada**: un sombreador de vértices recibe sus entradas de la etapa ensamblador de entrada; los sombreadores de píxeles y de geometría reciben sus entradas de la fase del sombreador anterior.</span><span class="sxs-lookup"><span data-stu-id="e41a7-108">**Input Data**: A vertex shader receives its inputs from the input assembler stage; geometry and pixel shaders receive their inputs from the previous shader stage.</span></span> <span data-ttu-id="e41a7-109">Entre las entradas adicionales se incluyen la [semántica de valores del sistema](dx-graphics-hlsl-semantics.md), que son consumibles por la primera unidad de la canalización a la que se aplican.</span><span class="sxs-lookup"><span data-stu-id="e41a7-109">Additional inputs include [system-value semantics](dx-graphics-hlsl-semantics.md), which are consumable by the first unit in the pipeline to which they are applicable.</span></span>
-   <span data-ttu-id="e41a7-110">**Datos de salida**: los sombreadores generan resultados de salida que se van a pasar a la fase siguiente de la canalización.</span><span class="sxs-lookup"><span data-stu-id="e41a7-110">**Output Data**: Shaders generate output results to be passed onto the subsequent stage in the pipeline.</span></span> <span data-ttu-id="e41a7-111">En el caso de un sombreador de geometría, la cantidad de datos de salida de una única invocación puede variar.</span><span class="sxs-lookup"><span data-stu-id="e41a7-111">For a geometry shader, the amount of data output from a single invocation can vary.</span></span> <span data-ttu-id="e41a7-112">Algunos resultados son interpretados por el núcleo del sombreador común (como la posición del vértice y el índice de representación-destino-matriz); otros están diseñados para ser interpretados por una aplicación.</span><span class="sxs-lookup"><span data-stu-id="e41a7-112">Some outputs are interpreted by the common-shader core (such as vertex position and render-target-array index), others are designed to be interpreted by an application.</span></span>
-   <span data-ttu-id="e41a7-113">**Código del sombreador**: los sombreadores pueden leer de la memoria, realizar operaciones aritméticas de punto flotante y de entero de Vector, o operaciones de control de flujo.</span><span class="sxs-lookup"><span data-stu-id="e41a7-113">**Shader Code**: Shaders can read from memory, perform vector floating point and integer arithmetic operations, or flow control operations.</span></span> <span data-ttu-id="e41a7-114">No hay ningún límite en el número de instrucciones que se pueden implementar en un sombreador.</span><span class="sxs-lookup"><span data-stu-id="e41a7-114">There is no limit to the number of statements that can be implemented in a shader.</span></span>
-   <span data-ttu-id="e41a7-115">**Muestreadores**: los muestreadores definen cómo se muestra y filtra las texturas.</span><span class="sxs-lookup"><span data-stu-id="e41a7-115">**Samplers**: Samplers define how to sample and filter textures.</span></span> <span data-ttu-id="e41a7-116">Hasta 16 muestras se pueden enlazar a un sombreador simultáneamente.</span><span class="sxs-lookup"><span data-stu-id="e41a7-116">As many as 16 samplers can be bound to a shader simultaneously.</span></span>
-   <span data-ttu-id="e41a7-117">**Texturas**: las texturas se pueden filtrar mediante muestreadores o leer por cada textura directamente con la función de [carga](dx-graphics-hlsl-to-load.md) intrínseca.</span><span class="sxs-lookup"><span data-stu-id="e41a7-117">**Textures**: Textures can be filtered using samplers or read on a per-texel basis directly with the [load](dx-graphics-hlsl-to-load.md) intrinsic function.</span></span>
-   <span data-ttu-id="e41a7-118">**Búferes**: los búferes nunca se filtran, pero se pueden leer de la memoria por elemento directamente con la función de [carga](dx-graphics-hlsl-to-load.md) intrínseca.</span><span class="sxs-lookup"><span data-stu-id="e41a7-118">**Buffers**: Buffers are never filtered, but can be read from memory on a per-element basis directly with the [load](dx-graphics-hlsl-to-load.md) intrinsic function.</span></span> <span data-ttu-id="e41a7-119">Como máximo 128, se pueden enlazar varios recursos de búfer y textura (combinados) a un sombreador simultáneamente.</span><span class="sxs-lookup"><span data-stu-id="e41a7-119">As many as 128 texture and buffer resources (combined) can be bound to a shader simultaneously.</span></span>
-   <span data-ttu-id="e41a7-120">**Búferes de constantes**: los búferes de constantes están optimizados para las variables de constantes de sombreador.</span><span class="sxs-lookup"><span data-stu-id="e41a7-120">**Constant Buffers**: Constant buffers are optimized for shader constant-variables.</span></span> <span data-ttu-id="e41a7-121">Hasta 16 búferes de constantes se pueden enlazar a una fase de sombreador simultáneamente.</span><span class="sxs-lookup"><span data-stu-id="e41a7-121">As many as 16 constant buffers can be bound to a shader stage simultaneously.</span></span> <span data-ttu-id="e41a7-122">Están diseñados para una actualización más frecuente de la CPU; por lo tanto, tienen restricciones de acceso, diseño y tamaño adicionales.</span><span class="sxs-lookup"><span data-stu-id="e41a7-122">They are designed for more frequent update from the CPU; therefore, they have additional size, layout, and access restrictions.</span></span>



|                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e41a7-123">Diferencias entre Direct3D 9 y Direct3D 10:</span><span class="sxs-lookup"><span data-stu-id="e41a7-123">Differences between Direct3D 9 and Direct3D 10:</span></span><br/> <span data-ttu-id="e41a7-124">En Direct3D 9, cada unidad de sombreador tenía un único archivo de registro constante pequeño para almacenar todas las variables de sombreador constantes.</span><span class="sxs-lookup"><span data-stu-id="e41a7-124">In Direct3D 9, each shader unit had a single, small constant register file to store all constant shader variables.</span></span> <span data-ttu-id="e41a7-125">Acomodar todos los sombreadores con este espacio constante limitado requería el reciclaje frecuente de constantes por la CPU.</span><span class="sxs-lookup"><span data-stu-id="e41a7-125">Accommodating all shaders with this limited constant space required frequent recycling of constants by the CPU.</span></span><br/> <span data-ttu-id="e41a7-126">En Direct3D 10, las constantes se almacenan en búferes inmutables en la memoria y se administran como cualquier otro recurso.</span><span class="sxs-lookup"><span data-stu-id="e41a7-126">In Direct3D 10, constants are stored in immutable buffers in memory and are managed like any other resource.</span></span> <span data-ttu-id="e41a7-127">No hay ningún límite en el número de búferes de constantes que puede crear una aplicación.</span><span class="sxs-lookup"><span data-stu-id="e41a7-127">There is no limit to the number of constant buffers an application can create.</span></span> <span data-ttu-id="e41a7-128">Mediante la organización de constantes en búferes por frecuencia de actualización y uso, la cantidad de ancho de banda necesaria para actualizar las constantes de forma que quepan todos los sombreadores se puede reducir considerablemente.</span><span class="sxs-lookup"><span data-stu-id="e41a7-128">By organizing constants into buffers by frequency of update and usage, the amount of bandwidth required to update constants to accommodate all shaders can be significantly reduced.</span></span><br/> |



 

## <a name="integer-and-bitwise-support"></a><span data-ttu-id="e41a7-129">Compatibilidad con enteros y bit a bit</span><span class="sxs-lookup"><span data-stu-id="e41a7-129">Integer and Bitwise Support</span></span>

<span data-ttu-id="e41a7-130">El núcleo de sombreador común proporciona un conjunto completo de operaciones bit a bit y de enteros de 32 bits compatibles con IEEE.</span><span class="sxs-lookup"><span data-stu-id="e41a7-130">The common shader core provides a full set of IEEE-compliant 32-bit integer and bitwise operations.</span></span> <span data-ttu-id="e41a7-131">Estas operaciones habilitan una nueva clase de algoritmos en los ejemplos de hardware de gráficos incluyen técnicas de compresión y empaquetado, FFTs y control de flujo de programa de bits de bits.</span><span class="sxs-lookup"><span data-stu-id="e41a7-131">These operations enable a new class of algorithms in graphics hardware examples include compression and packing techniques, FFTs, and bitfield program-flow control.</span></span>

<span data-ttu-id="e41a7-132">Los tipos de datos **int** y **uint** de Direct3D 10 HLSL se asignan a enteros de 32 bits en hardware.</span><span class="sxs-lookup"><span data-stu-id="e41a7-132">The **int** and **uint** data types in Direct3D 10 HLSL map to 32-bit integers in hardware.</span></span>



|                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e41a7-133">Diferencias entre Direct3D 9 y Direct3D 10:</span><span class="sxs-lookup"><span data-stu-id="e41a7-133">Differences between Direct3D 9 and Direct3D 10:</span></span><br/> <span data-ttu-id="e41a7-134">En Direct3D 9, las entradas de flujo marcadas como enteros en HLSL se interpretaban como punto flotante.</span><span class="sxs-lookup"><span data-stu-id="e41a7-134">In Direct3D 9 stream inputs marked as integer in HLSL were interpreted as floating-point.</span></span> <span data-ttu-id="e41a7-135">En Direct3D 10, las entradas de secuencia marcadas como Integer se interpretan como un entero de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="e41a7-135">In Direct3D 10, stream inputs marked as integer are interpreted as a 32- bit integer.</span></span><br/> <span data-ttu-id="e41a7-136">Además, los valores booleanos son ahora todos los bits establecidos o todos los bits no se establecen.</span><span class="sxs-lookup"><span data-stu-id="e41a7-136">In addition, boolean values are now all bits set or all bits unset.</span></span> <span data-ttu-id="e41a7-137">Los datos convertidos en **bool** se interpretarán como true si el valor no es igual a 0,0 f (los cero positivos y negativos pueden ser false) y false en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="e41a7-137">Data converted to **bool** will be interpreted as true if the value is not equal to 0.0f (both positive and negative zero are allowed to be false) and false otherwise.</span></span><br/> |



 

## <a name="bitwise-operators"></a><span data-ttu-id="e41a7-138">Operadores bit a bit</span><span class="sxs-lookup"><span data-stu-id="e41a7-138">Bitwise operators</span></span>

<span data-ttu-id="e41a7-139">Common Shader Core admite los siguientes operadores bit a bit:</span><span class="sxs-lookup"><span data-stu-id="e41a7-139">The common shader core supports the following bitwise operators:</span></span>



| <span data-ttu-id="e41a7-140">Operador</span><span class="sxs-lookup"><span data-stu-id="e41a7-140">Operator</span></span>  | <span data-ttu-id="e41a7-141">Función</span><span class="sxs-lookup"><span data-stu-id="e41a7-141">Function</span></span>          |
|-----------|-------------------|
| ~         | <span data-ttu-id="e41a7-142">Not lógico</span><span class="sxs-lookup"><span data-stu-id="e41a7-142">Logical Not</span></span>       |
| <<  | <span data-ttu-id="e41a7-143">Desplazamiento a la izquierda</span><span class="sxs-lookup"><span data-stu-id="e41a7-143">Left Shift</span></span>        |
| >>  | <span data-ttu-id="e41a7-144">Desplazamiento a la derecha</span><span class="sxs-lookup"><span data-stu-id="e41a7-144">Right Shift</span></span>       |
| &         | <span data-ttu-id="e41a7-145">Logical And</span><span class="sxs-lookup"><span data-stu-id="e41a7-145">Logical And</span></span>       |
| \|        | <span data-ttu-id="e41a7-146">Or lógico.</span><span class="sxs-lookup"><span data-stu-id="e41a7-146">Logical Or</span></span>        |
| ^         | <span data-ttu-id="e41a7-147">XOR lógico</span><span class="sxs-lookup"><span data-stu-id="e41a7-147">Logical Xor</span></span>       |
| <<= | <span data-ttu-id="e41a7-148">Igual a la izquierda</span><span class="sxs-lookup"><span data-stu-id="e41a7-148">Left shift Equal</span></span>  |
| >>= | <span data-ttu-id="e41a7-149">Desplazamiento a la derecha</span><span class="sxs-lookup"><span data-stu-id="e41a7-149">Right Shift Equal</span></span> |
| &=        | <span data-ttu-id="e41a7-150">Y igual</span><span class="sxs-lookup"><span data-stu-id="e41a7-150">And Equal</span></span>         |
| \|=       | <span data-ttu-id="e41a7-151">O igual</span><span class="sxs-lookup"><span data-stu-id="e41a7-151">Or Equal</span></span>          |
| ^=        | <span data-ttu-id="e41a7-152">XOR igual</span><span class="sxs-lookup"><span data-stu-id="e41a7-152">Xor Equal</span></span>         |



 

<span data-ttu-id="e41a7-153">Los operadores bit a bit se definen para funcionar solo en los tipos de datos **int** y **uint** .</span><span class="sxs-lookup"><span data-stu-id="e41a7-153">Bitwise operators are defined to operate only on **int** and **uint** data types.</span></span> <span data-ttu-id="e41a7-154">Si se intenta usar operadores bit a bit en tipos de datos **float** o **struct** , se producirá un error.</span><span class="sxs-lookup"><span data-stu-id="e41a7-154">Attempting to use bitwise operators on **float** or **struct** data types will result in an error.</span></span> <span data-ttu-id="e41a7-155">Los operadores bit a bit siguen la misma precedencia que C con respecto a otros operadores.</span><span class="sxs-lookup"><span data-stu-id="e41a7-155">Bitwise operators follow the same precedence as C with regard to other operators.</span></span>

## <a name="binary-casts"></a><span data-ttu-id="e41a7-156">Conversiones binarias</span><span class="sxs-lookup"><span data-stu-id="e41a7-156">Binary Casts</span></span>

<span data-ttu-id="e41a7-157">La conversión entre un entero y un tipo de punto flotante convertirá el valor numérico después de las reglas de truncamiento de C.</span><span class="sxs-lookup"><span data-stu-id="e41a7-157">Casting between an integer and a floating-point type will convert the numeric value following C truncation rules.</span></span> <span data-ttu-id="e41a7-158">Convertir un valor de **float** a **int** y volver a un valor **float** es una conversión de pérdida que depende de la precisión del tipo de datos de destino.</span><span class="sxs-lookup"><span data-stu-id="e41a7-158">Casting a value from a **float**, to an **int**, and back to a **float** is a lossy conversion dependent on the precision of the target data type.</span></span> <span data-ttu-id="e41a7-159">Estas son algunas de las funciones de conversión: [**asfloat (DirectX HLSL)**](dx-graphics-hlsl-asfloat.md), [**Asint (DirectX HLSL)**](dx-graphics-hlsl-asint.md), [**asuint (DirectX HLSL)**](dx-graphics-hlsl-asuint.md).</span><span class="sxs-lookup"><span data-stu-id="e41a7-159">Here are some of the conversion functions: [**asfloat (DirectX HLSL)**](dx-graphics-hlsl-asfloat.md), [**asint (DirectX HLSL)**](dx-graphics-hlsl-asint.md), [**asuint (DirectX HLSL)**](dx-graphics-hlsl-asuint.md).</span></span>

<span data-ttu-id="e41a7-160">Las conversiones binarias también se pueden realizar mediante las funciones intrínsecas de HLSL.</span><span class="sxs-lookup"><span data-stu-id="e41a7-160">Binary casts can also be performed using HLSL intrinsic functions.</span></span> <span data-ttu-id="e41a7-161">Esto hace que el compilador reinterprete la representación de bits de un número en el tipo de datos de destino.</span><span class="sxs-lookup"><span data-stu-id="e41a7-161">These cause the compiler to reinterpret the bit representation of a number into the target data type.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e41a7-162">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e41a7-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e41a7-163">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="e41a7-163">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 





