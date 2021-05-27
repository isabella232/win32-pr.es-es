---
title: Enlace de recursos en HLSL
description: En este tema se describen algunas características específicas del uso del modelo de sombreador hlsl (lenguaje de sombreador de alto nivel) 5.1 con Direct3D 12.
ms.assetid: 3CD4BDAD-8AE3-4DE0-B3F8-9C9F9E83BBE9
ms.localizationpriority: high
ms.topic: article
ms.date: 08/27/2019
ms.openlocfilehash: 711ccdee71ff916445be68d03b84b7621aa04cf3
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/27/2021
ms.locfileid: "110550390"
---
# <a name="resource-binding-in-hlsl"></a><span data-ttu-id="b85f8-103">Enlace de recursos en HLSL</span><span class="sxs-lookup"><span data-stu-id="b85f8-103">Resource binding in HLSL</span></span>

<span data-ttu-id="b85f8-104">En este tema se describen algunas características específicas del uso del modelo de sombreador hlsl (lenguaje de sombreador de alto nivel) [5.1](/windows/desktop/direct3dhlsl/shader-model-5-1) con Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="b85f8-104">This topic describes some specific features of using High Level Shader Language (HLSL) [Shader Model 5.1](/windows/desktop/direct3dhlsl/shader-model-5-1) with Direct3D 12.</span></span> <span data-ttu-id="b85f8-105">Todo el hardware de Direct3D 12 admite el modelo de sombreador 5.1, por lo que la compatibilidad con este modelo no depende del nivel de característica de hardware.</span><span class="sxs-lookup"><span data-stu-id="b85f8-105">All Direct3D 12 hardware supports Shader Model 5.1, so support for this model does not depend on what the hardware feature level is.</span></span>

## <a name="resource-types-and-arrays"></a><span data-ttu-id="b85f8-106">Tipos de recursos y matrices</span><span class="sxs-lookup"><span data-stu-id="b85f8-106">Resource types and arrays</span></span>

<span data-ttu-id="b85f8-107">La sintaxis de recursos del modelo de sombreador 5 (SM5.0) usa la palabra clave para retransmitir información importante sobre el recurso `register` al compilador HLSL.</span><span class="sxs-lookup"><span data-stu-id="b85f8-107">Shader Model 5 (SM5.0) resource syntax uses the `register` keyword to relay important information about the resource to the HLSL compiler.</span></span> <span data-ttu-id="b85f8-108">Por ejemplo, la siguiente instrucción declara una matriz de cuatro texturas enlazadas en las ranuras t3, t4, t5 y t6.</span><span class="sxs-lookup"><span data-stu-id="b85f8-108">For example, the following statement declares an array of four textures bound at slots t3, t4, t5, and t6.</span></span> <span data-ttu-id="b85f8-109">t3 es la única ranura de registro que aparece en la instrucción , siendo simplemente la primera de la matriz de cuatro.</span><span class="sxs-lookup"><span data-stu-id="b85f8-109">t3 is the only register slot appearing in the statement, simply being the first in the array of four.</span></span>

``` syntax
Texture2D<float4> tex1[4] : register(t3)
```

<span data-ttu-id="b85f8-110">La sintaxis de recursos del Modelo de sombreador 5.1 (SM5.1) en HLSL se basa en la sintaxis de recursos de registro existente, para permitir una porción más sencilla.</span><span class="sxs-lookup"><span data-stu-id="b85f8-110">Shader Model 5.1 (SM5.1) resource syntax in HLSL is based on existing register resource syntax, to allow easier porting.</span></span> <span data-ttu-id="b85f8-111">Los recursos de Direct3D 12 en HLSL están enlazados a registros virtuales dentro de espacios de registro lógicos:</span><span class="sxs-lookup"><span data-stu-id="b85f8-111">Direct3D 12 resources in HLSL are bound to virtual registers within logical register spaces:</span></span>

-   <span data-ttu-id="b85f8-112">t: para vistas de recursos de sombreador (SRV)</span><span class="sxs-lookup"><span data-stu-id="b85f8-112">t – for shader resource views (SRV)</span></span>
-   <span data-ttu-id="b85f8-113">s: para muestreadores</span><span class="sxs-lookup"><span data-stu-id="b85f8-113">s – for samplers</span></span>
-   <span data-ttu-id="b85f8-114">u: para vistas de acceso no ordenado (UAV)</span><span class="sxs-lookup"><span data-stu-id="b85f8-114">u – for unordered access views (UAV)</span></span>
-   <span data-ttu-id="b85f8-115">b: para vistas de búfer constante (CBV)</span><span class="sxs-lookup"><span data-stu-id="b85f8-115">b – for constant buffer views (CBV)</span></span>

<span data-ttu-id="b85f8-116">La firma raíz que hace referencia al sombreador debe ser compatible con las ranuras de registro declaradas.</span><span class="sxs-lookup"><span data-stu-id="b85f8-116">The root signature referencing the shader must be compatible with the declared register slots.</span></span> <span data-ttu-id="b85f8-117">Por ejemplo, la siguiente parte de una firma raíz sería compatible con el uso de ranuras de textura t3 a t6, ya que describe una tabla de descriptores con ranuras de t0 a t98.</span><span class="sxs-lookup"><span data-stu-id="b85f8-117">For example, the following portion of a root signature would be compatible with the use of texture slots t3 through t6, as it describes a descriptor table with slots t0 through t98.</span></span>

``` syntax
DescriptorTable( CBV(b1), SRV(t0,numDescriptors=99), CBV(b2) )
```

<span data-ttu-id="b85f8-118">Una declaración de recursos puede ser escalar, matriz 1D o matriz multidimensional:</span><span class="sxs-lookup"><span data-stu-id="b85f8-118">A resource declaration may be a scalar, a 1D array, or a multidimensional array:</span></span>

``` syntax
Texture2D<float4> tex1 : register(t3,  space0)
Texture2D<float4> tex2[4] : register(t10)
Texture2D<float4> tex3[7][5][3] : register(t20, space1)
```

<span data-ttu-id="b85f8-119">SM5.1 usa los mismos tipos de recursos y tipos de elemento que SM5.0.</span><span class="sxs-lookup"><span data-stu-id="b85f8-119">SM5.1 uses the same resource types and element types as SM5.0 does.</span></span> <span data-ttu-id="b85f8-120">Los límites de declaración SM5.1 son más flexibles y solo están restringidos por los límites de tiempo de ejecución o hardware.</span><span class="sxs-lookup"><span data-stu-id="b85f8-120">SM5.1 declaration limits are more flexible, and constrained only by the runtime/hardware limits.</span></span> <span data-ttu-id="b85f8-121">La `space` palabra clave especifica a qué espacio de registro lógico está enlazada la variable declarada.</span><span class="sxs-lookup"><span data-stu-id="b85f8-121">The `space` keyword specifies to which logical register space the declared variable is bound.</span></span> <span data-ttu-id="b85f8-122">Si se omite la palabra clave , el índice de espacio predeterminado de 0 se asigna implícitamente al intervalo (por lo que el intervalo anterior `space` `tex2` reside en `space0` ).</span><span class="sxs-lookup"><span data-stu-id="b85f8-122">If the `space` keyword is omitted, then the default space index of 0 is implicitly assigned to the range (so the `tex2` range above resides in `space0`).</span></span> <span data-ttu-id="b85f8-123">`register(t3,  space0)` nunca entra en conflicto con `register(t3,  space1)` , ni con ninguna matriz en otro espacio que pueda incluir t3.</span><span class="sxs-lookup"><span data-stu-id="b85f8-123">`register(t3,  space0)` will never conflict with `register(t3,  space1)`, nor with any array in another space that might include t3.</span></span>

<span data-ttu-id="b85f8-124">Un recurso de matriz puede tener un tamaño sin enlazar, que se declara especificando que la primera dimensión esté vacía, o 0:</span><span class="sxs-lookup"><span data-stu-id="b85f8-124">An array resource may have an unbounded size, which is declared by specifying the very first dimension to be empty, or 0:</span></span>

``` syntax
Texture2D<float4> tex1[] : register(t0)
```

<span data-ttu-id="b85f8-125">La tabla de descriptores correspondiente podría ser:</span><span class="sxs-lookup"><span data-stu-id="b85f8-125">The matching descriptor table could be:</span></span>

``` syntax
DescriptorTable( CBV(b1), UAV(u0, numDescriptors = 4), SRV(t0, numDescriptors=unbounded)
```

<span data-ttu-id="b85f8-126">Una matriz sin enlazar en HLSL coincide con un número fijo establecido con en la tabla de descriptores y un tamaño fijo en hlsl coincide con una declaración sin enlazar en la tabla `numDescriptors` de descriptores.</span><span class="sxs-lookup"><span data-stu-id="b85f8-126">An unbounded array in HLSL does match a fixed number set with `numDescriptors` in the descriptor table, and a fixed size in the HLSL does match an unbounded declaration in the descriptor table.</span></span>

<span data-ttu-id="b85f8-127">Se permiten matrices multidimensionales, incluidas las de un tamaño sin enlazar.</span><span class="sxs-lookup"><span data-stu-id="b85f8-127">Multi-dimensional arrays are allowed, including of an unbounded size.</span></span> <span data-ttu-id="b85f8-128">Estas matrices multidimensionales se aplana en el espacio de registro.</span><span class="sxs-lookup"><span data-stu-id="b85f8-128">These multidimensional arrays are flattened out in register space.</span></span>

``` syntax
Texture2D<float4> tex2[3000][10] : register(t0, space0); // t0-t29999 in space0
Texture2D<float4> tex3[0][5][3] : register(t5, space1)
```

<span data-ttu-id="b85f8-129">No se permite la asignación de alias de intervalos de recursos.</span><span class="sxs-lookup"><span data-stu-id="b85f8-129">Aliasing of resource ranges is not allowed.</span></span> <span data-ttu-id="b85f8-130">En otras palabras, para cada tipo de recurso (t, s, u, b), los intervalos de registro declarados no deben superponerse.</span><span class="sxs-lookup"><span data-stu-id="b85f8-130">In other words, for each resource type (t, s, u, b), declared register ranges mustn't overlap.</span></span> <span data-ttu-id="b85f8-131">Esto también incluye intervalos sin enlazar.</span><span class="sxs-lookup"><span data-stu-id="b85f8-131">That includes unbounded ranges, too.</span></span> <span data-ttu-id="b85f8-132">Los intervalos declarados en distintos espacios de registro nunca se superponen.</span><span class="sxs-lookup"><span data-stu-id="b85f8-132">Ranges declared in different register spaces never overlap.</span></span> <span data-ttu-id="b85f8-133">Tenga en cuenta que unbounded (arriba) reside en , mientras que unbounded reside en , de forma que no `tex2` `space0` se `tex3` `space1` superponen.</span><span class="sxs-lookup"><span data-stu-id="b85f8-133">Note that unbounded `tex2` (above) resides in `space0`, while unbounded `tex3` resides in `space1`, such that they don't overlap.</span></span>

<span data-ttu-id="b85f8-134">El acceso a los recursos que se han declarado como matrices es tan sencillo como indexarlos.</span><span class="sxs-lookup"><span data-stu-id="b85f8-134">Accessing resources that have been declared as arrays is as simple as indexing them.</span></span>

``` syntax
Texture2D<float4> tex1[400] : register(t3);
sampler samp[7] : register(s0);
tex1[myMaterialID].Sample(samp[samplerID], texCoords);
```

<span data-ttu-id="b85f8-135">Hay una restricción predeterminada importante en el uso de los índices ( y en el código anterior) en que no pueden variar dentro de `myMaterialID` `samplerID` una [ola](../direct3dhlsl/hlsl-shader-model-6-0-features-for-direct3d-12.md#terminology).</span><span class="sxs-lookup"><span data-stu-id="b85f8-135">There's an important default restriction on the use of the indices (`myMaterialID` and `samplerID` in the code above) in that they're not allowed to vary within a [wave](../direct3dhlsl/hlsl-shader-model-6-0-features-for-direct3d-12.md#terminology).</span></span> <span data-ttu-id="b85f8-136">Incluso el cambio del índice en función de los recuentos de creación de instancias varía.</span><span class="sxs-lookup"><span data-stu-id="b85f8-136">Even changing the index based on instancing counts as varying.</span></span>

<span data-ttu-id="b85f8-137">Si es necesario variar el índice, especifique el `NonUniformResourceIndex` calificador en el índice, por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="b85f8-137">If varying the index is required then specify the `NonUniformResourceIndex` qualifier on the index, for example:</span></span>

``` syntax
tex1[NonUniformResourceIndex(myMaterialID)].Sample(samp[NonUniformResourceIndex(samplerID)], texCoords);
```

<span data-ttu-id="b85f8-138">En algún hardware, el uso de este calificador genera código adicional para aplicar la corrección (incluidos los subprocesos), pero con un costo de rendimiento menor.</span><span class="sxs-lookup"><span data-stu-id="b85f8-138">On some hardware the use of this qualifier generates additional code to enforce correctness (including across threads) but at a minor performance cost.</span></span> <span data-ttu-id="b85f8-139">Si se cambia un índice sin este calificador y dentro de un draw/dispatch, los resultados no están definidos.</span><span class="sxs-lookup"><span data-stu-id="b85f8-139">If an index is changed without this qualifier and within a draw/dispatch the results are undefined.</span></span>

## <a name="descriptor-arrays-and-texture-arrays"></a><span data-ttu-id="b85f8-140">Matrices de descriptores y matrices de textura</span><span class="sxs-lookup"><span data-stu-id="b85f8-140">Descriptor arrays and texture arrays</span></span>

<span data-ttu-id="b85f8-141">Las matrices de texturas están disponibles desde DirectX 10.</span><span class="sxs-lookup"><span data-stu-id="b85f8-141">Texture arrays have been available since DirectX 10.</span></span> <span data-ttu-id="b85f8-142">Las matrices de textura requieren un descriptor, pero todos los segmentos de matriz deben compartir el mismo formato, ancho, alto y recuento de mip.</span><span class="sxs-lookup"><span data-stu-id="b85f8-142">Texture arrays require one descriptor, however all the array slices must share the same format, width, height and mip count.</span></span> <span data-ttu-id="b85f8-143">Además, la matriz debe ocupar un intervalo contiguo en el espacio de direcciones virtuales.</span><span class="sxs-lookup"><span data-stu-id="b85f8-143">Also, the array must occupy a contiguous range in virtual address space.</span></span> <span data-ttu-id="b85f8-144">En el código siguiente se muestra un ejemplo de acceso a una matriz de textura desde un sombreador.</span><span class="sxs-lookup"><span data-stu-id="b85f8-144">The following code shows an example of accessing a texture array from a shader.</span></span>

``` syntax
Texture2DArray<float4> myTex2DArray : register(t0); // t0
float3 myCoord(1.0f,1.4f,2.2f); // 2.2f is array index (rounded to int)
color = myTex2DArray.Sample(mySampler, myCoord);
```

<span data-ttu-id="b85f8-145">En una matriz de texturas, el índice puede variar libremente, sin necesidad de calificadores como `NonUniformResourceIndex` .</span><span class="sxs-lookup"><span data-stu-id="b85f8-145">In a texture array, the index can be varied freely, without any need for qualifiers such as `NonUniformResourceIndex`.</span></span>

<span data-ttu-id="b85f8-146">La matriz de descriptores equivalente sería:</span><span class="sxs-lookup"><span data-stu-id="b85f8-146">The equivalent descriptor array would be:</span></span>

``` syntax
Texture2D<float4> myArrayOfTex2D[] : register(t0); // t0+
float2 myCoord(1.0f, 1.4f);
color = myArrayOfTex2D[2].Sample(mySampler,myCoord); // 2 is index
```

<span data-ttu-id="b85f8-147">Tenga en cuenta que el uso extraño de un elemento float para el índice de la matriz se reemplaza por `myArrayOfTex2D[2]` .</span><span class="sxs-lookup"><span data-stu-id="b85f8-147">Note the awkward use of a float for the array index is replaced with `myArrayOfTex2D[2]`.</span></span> <span data-ttu-id="b85f8-148">Además, las matrices de descriptores ofrecen más flexibilidad con las dimensiones.</span><span class="sxs-lookup"><span data-stu-id="b85f8-148">Also descriptor arrays offer more flexibility with the dimensions.</span></span> <span data-ttu-id="b85f8-149">El tipo, en este ejemplo, no puede variar, pero el formato, el ancho, el alto y el recuento de mip pueden variar `Texture2D` con cada descriptor.</span><span class="sxs-lookup"><span data-stu-id="b85f8-149">The type, `Texture2D` is this example, cannot vary, but the format, width, height, and mip count can all vary with each descriptor.</span></span>

<span data-ttu-id="b85f8-150">Es legítimo tener una matriz de descriptores de matrices de textura:</span><span class="sxs-lookup"><span data-stu-id="b85f8-150">It is legitimate to have a descriptor array of texture arrays:</span></span>

``` syntax
Texture2DArray<float4> myArrayOfTex2DArrays[2] : register(t0);
```

<span data-ttu-id="b85f8-151">No es legítimo declarar una matriz de estructuras, cada estructura que contiene descriptores, por ejemplo, no se admite el código siguiente.</span><span class="sxs-lookup"><span data-stu-id="b85f8-151">It is not legitimate to declare an array of structures, each structure containing descriptors, for example the following code is not supported.</span></span>

``` syntax
struct myStruct {
    Texture2D                    a; 
    Texture2D                    b;
    ConstantBuffer<myConstants>  c;
};
myStruct foo[10000] : register(....);
```

<span data-ttu-id="b85f8-152">Esto habría permitido el diseño de memoria **abcabcabc...**, pero es una limitación del lenguaje y no se admite.</span><span class="sxs-lookup"><span data-stu-id="b85f8-152">This would have allowed the memory layout **abcabcabc....**, but is a language limitation and is not supported.</span></span> <span data-ttu-id="b85f8-153">Un método admitido para hacerlo sería el siguiente, aunque el diseño de memoria en este caso es **aaa... Bbb... y...**.</span><span class="sxs-lookup"><span data-stu-id="b85f8-153">One supported method of doing this would be as follows, though the memory layout in this case is **aaa...bbb...ccc...**.</span></span>

``` syntax
Texture2D                     a[10000] : register(t0);
Texture2D                     b[10000] : register(t10000);
ConstantBuffer<myConstants>   c[10000] : register(b0);
```

<span data-ttu-id="b85f8-154">Para lograr el diseño de memoria **abcabcabc...,** use una tabla de descriptores sin usar la `myStruct` estructura .</span><span class="sxs-lookup"><span data-stu-id="b85f8-154">To achieve the **abcabcabc....** memory layout, use a descriptor table without use of the `myStruct` structure.</span></span>

## <a name="resource-aliasing"></a><span data-ttu-id="b85f8-155">Alias de recursos</span><span class="sxs-lookup"><span data-stu-id="b85f8-155">Resource aliasing</span></span>

<span data-ttu-id="b85f8-156">Los intervalos de recursos especificados en los sombreadores HLSL son intervalos lógicos.</span><span class="sxs-lookup"><span data-stu-id="b85f8-156">The resource ranges specified in the HLSL shaders are logical ranges.</span></span> <span data-ttu-id="b85f8-157">Se enlazan a intervalos de montón concretos en tiempo de ejecución mediante el mecanismo de firma raíz.</span><span class="sxs-lookup"><span data-stu-id="b85f8-157">They are be bound to concrete heap ranges at runtime via the root signature mechanism.</span></span> <span data-ttu-id="b85f8-158">Normalmente, un intervalo lógico se asigna a un intervalo de montón que no se superpone con otros intervalos del montón.</span><span class="sxs-lookup"><span data-stu-id="b85f8-158">Normally, a logical range maps to a heap range that does not overlap with other heap ranges.</span></span> <span data-ttu-id="b85f8-159">Sin embargo, el mecanismo de firma raíz permite crear alias (superponerse) intervalos de montones de tipos compatibles.</span><span class="sxs-lookup"><span data-stu-id="b85f8-159">However, the root signature mechanism makes it possible to alias (overlap) heap ranges of compatible types.</span></span> <span data-ttu-id="b85f8-160">Por ejemplo, los intervalos y del ejemplo anterior se pueden asignar al mismo intervalo de montón (o superpuesto), lo que tiene el efecto de crear alias de texturas en el programa `tex2` `tex3` HLSL.</span><span class="sxs-lookup"><span data-stu-id="b85f8-160">For example, `tex2` and `tex3` ranges from the above example may be mapped to the same (or overlapping) heap range, which has the effect of aliasing textures in the HLSL program.</span></span> <span data-ttu-id="b85f8-161">Si se desea este tipo de alias, el sombreador debe compilarse con la opción DE ALIAS MAY SHADER RESOURCES (RECURSOS DE SOMBREADOR) D3D10, que se establece mediante la opción \_ \_ de alias \_ \_ */res \_ may \_ para* la herramienta [Effect-Compiler](../direct3dtools/fxc.md) Tool (FXC).</span><span class="sxs-lookup"><span data-stu-id="b85f8-161">If such aliasing is desired, the shader must be compiled with D3D10\_SHADER\_RESOURCES\_MAY\_ALIAS option, which is set by using the */res\_may\_alias* option for the [Effect-Compiler Tool](../direct3dtools/fxc.md) (FXC).</span></span> <span data-ttu-id="b85f8-162">La opción hace que el compilador produzca código correcto al impedir ciertas optimizaciones de carga y almacenamiento bajo la suposición de que los recursos pueden crear alias.</span><span class="sxs-lookup"><span data-stu-id="b85f8-162">The option makes the compiler produce correct code by preventing certain load/store optimizations under the assumption that resources may alias.</span></span>

## <a name="divergence-and-derivatives"></a><span data-ttu-id="b85f8-163">Diferencias y derivados</span><span class="sxs-lookup"><span data-stu-id="b85f8-163">Divergence and derivatives</span></span>

<span data-ttu-id="b85f8-164">SM5.1 no impone limitaciones en el índice de recursos; Es decir, el índice idx puede ser una constante literal, una ` tex2[idx].Sample(…)` constante cbuffer o un valor interpolado.</span><span class="sxs-lookup"><span data-stu-id="b85f8-164">SM5.1 does not impose limitations on the resource index; i.e.,` tex2[idx].Sample(…)` – the index idx can be a literal constant, a cbuffer constant, or an interpolated value.</span></span> <span data-ttu-id="b85f8-165">Aunque el modelo de programación proporciona una flexibilidad tan grande, hay problemas que debe tener en cuenta:</span><span class="sxs-lookup"><span data-stu-id="b85f8-165">While the programming model provides such great flexibility, there are issues to be aware of:</span></span>

-   <span data-ttu-id="b85f8-166">Si el índice difiere en un cuadrándice, es posible que las cantidades derivadas y derivadas calculadas por hardware, como LOD, no se definan.</span><span class="sxs-lookup"><span data-stu-id="b85f8-166">If index diverges across a quad, the hardware-computed derivative and derived quantities such as LOD may be undefined.</span></span> <span data-ttu-id="b85f8-167">El compilador HLSL hace todo lo posible para emitir una advertencia en este caso, pero no impedirá que se compila un sombreador.</span><span class="sxs-lookup"><span data-stu-id="b85f8-167">The HLSL compiler makes the best effort to issue a warning in this case, but will not prevent a shader from compiling.</span></span> <span data-ttu-id="b85f8-168">Este comportamiento es similar a la computación de derivados en un flujo de control divergente.</span><span class="sxs-lookup"><span data-stu-id="b85f8-168">This behavior is similar to computing derivatives in divergent control flow.</span></span>
-   <span data-ttu-id="b85f8-169">Si el índice de recursos es divergente, el rendimiento se reduce en comparación con el caso de un índice uniforme, ya que el hardware necesita realizar operaciones en varios recursos.</span><span class="sxs-lookup"><span data-stu-id="b85f8-169">If the resource index is divergent, the performance is diminished compared to the case of a uniform index, because the hardware needs to perform operations on several resources.</span></span> <span data-ttu-id="b85f8-170">Los índices de recursos que pueden ser divergentes deben marcarse con la `NonUniformResourceIndex` función en código HLSL.</span><span class="sxs-lookup"><span data-stu-id="b85f8-170">Resource indexes that may be divergent must be marked with the `NonUniformResourceIndex` function in HLSL code.</span></span> <span data-ttu-id="b85f8-171">De lo contrario, los resultados no están definidos.</span><span class="sxs-lookup"><span data-stu-id="b85f8-171">Otherwise results are undefined.</span></span>

## <a name="uavs-in-pixel-shaders"></a><span data-ttu-id="b85f8-172">UAV en sombreadores de píxeles</span><span class="sxs-lookup"><span data-stu-id="b85f8-172">UAVs in pixel shaders</span></span>

<span data-ttu-id="b85f8-173">SM5.1 no impone restricciones en los intervalos UAV en sombreadores de píxeles, como era el caso de SM5.0.</span><span class="sxs-lookup"><span data-stu-id="b85f8-173">SM5.1 does not impose constraints on UAV ranges in pixel shaders as was the case for SM5.0.</span></span>

## <a name="constant-buffers"></a><span data-ttu-id="b85f8-174">Búferes constantes</span><span class="sxs-lookup"><span data-stu-id="b85f8-174">Constant Buffers</span></span>

<span data-ttu-id="b85f8-175">La sintaxis de los búferes constantes (cbuffer) de SM5.1 ha cambiado de SM5.0 para permitir a los desarrolladores indexar búferes constantes.</span><span class="sxs-lookup"><span data-stu-id="b85f8-175">SM5.1 constant buffers (cbuffer) syntax has changed from SM5.0 to enable developers to index constant buffers.</span></span> <span data-ttu-id="b85f8-176">Para habilitar búferes constantes indexables, SM5.1 presenta la `ConstantBuffer` construcción "template":</span><span class="sxs-lookup"><span data-stu-id="b85f8-176">To enable indexable constant buffers, SM5.1 introduces the `ConstantBuffer` “template” construct:</span></span>

``` syntax
struct Foo
{
    float4 a;
    int2 b;
};
ConstantBuffer<Foo> myCB1[2][3] : register(b2, space1);
ConstantBuffer<Foo> myCB2 : register(b0, space1);
```

<span data-ttu-id="b85f8-177">El código anterior declara una variable de búfer constante de tipo y tamaño 6, y una variable de búfer `myCB1` `Foo` constante `myCB2` escalar.</span><span class="sxs-lookup"><span data-stu-id="b85f8-177">The preceding code declares constant buffer variable `myCB1` of type `Foo` and size 6, and a scalar, constant buffer variable `myCB2`.</span></span> <span data-ttu-id="b85f8-178">Ahora se puede indexar una variable de búfer constante en el sombreador como:</span><span class="sxs-lookup"><span data-stu-id="b85f8-178">A constant buffer variable can now be indexed in the shader as:</span></span>

``` syntax
myCB1[i][j].a.xyzw
myCB2.b.yy
```

<span data-ttu-id="b85f8-179">Los campos "a" y "b" no se convierten en variables globales, sino que deben tratarse como campos.</span><span class="sxs-lookup"><span data-stu-id="b85f8-179">Fields ‘a’ and ‘b’ do not become global variables, but rather must be treated as fields.</span></span> <span data-ttu-id="b85f8-180">Por compatibilidad con versiones anteriores, SM5.1 admite el concepto anterior de cbuffer para los búferes escalares.</span><span class="sxs-lookup"><span data-stu-id="b85f8-180">For backward compatibility, SM5.1 supports the old cbuffer concept for scalar cbuffers.</span></span> <span data-ttu-id="b85f8-181">La siguiente instrucción hace que las variables globales "a" y "b" de solo lectura, como en SM5.0.</span><span class="sxs-lookup"><span data-stu-id="b85f8-181">The following statement makes ‘a’ and ‘b’ global, read-only variables as in SM5.0.</span></span> <span data-ttu-id="b85f8-182">Sin embargo, este tipo de cbuffer de estilo antiguo no puede ser indexable.</span><span class="sxs-lookup"><span data-stu-id="b85f8-182">However, such an old-style cbuffer cannot be indexable.</span></span>

``` syntax
cbuffer : register(b1)
{
    float4 a;
    int2 b;
};
```

<span data-ttu-id="b85f8-183">Actualmente, el compilador del sombreador solo admite `ConstantBuffer` la plantilla para estructuras definidas por el usuario.</span><span class="sxs-lookup"><span data-stu-id="b85f8-183">Currently, the shader compiler supports the `ConstantBuffer` template for user-defined structures only.</span></span>

<span data-ttu-id="b85f8-184">Por motivos de compatibilidad, el compilador HLSL puede asignar automáticamente registros de recursos para los intervalos declarados en `space0` .</span><span class="sxs-lookup"><span data-stu-id="b85f8-184">For compatibility reasons, the HLSL compiler may automatically assign resource registers for ranges declared in `space0`.</span></span> <span data-ttu-id="b85f8-185">Si se omite "space" en la cláusula register, se usa el `space0` valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="b85f8-185">If ‘space’ is omitted in the register clause, the default `space0` is used.</span></span> <span data-ttu-id="b85f8-186">El compilador usa la heurística de primer ajuste para asignar los registros.</span><span class="sxs-lookup"><span data-stu-id="b85f8-186">The compiler uses the first-hole-fits heuristic to assign the registers.</span></span> <span data-ttu-id="b85f8-187">La asignación se puede recuperar a través de la API de reflexión, que se ha ampliado para agregar el campo *Espacio* para el espacio, mientras que el campo *BindPoint* indica el límite inferior del intervalo de registro de recursos.</span><span class="sxs-lookup"><span data-stu-id="b85f8-187">The assignment can be retrieved via the reflection API, which has been extended to add the *Space* field for space, while the *BindPoint* field indicates the lower bound of the resource register range.</span></span>

## <a name="bytecode-changes-in-sm51"></a><span data-ttu-id="b85f8-188">Cambios en el código de bytes en SM5.1</span><span class="sxs-lookup"><span data-stu-id="b85f8-188">Bytecode changes in SM5.1</span></span>

<span data-ttu-id="b85f8-189">SM5.1 cambia la forma en que se declaran los registros de recursos y se hace referencia a ellos en las instrucciones.</span><span class="sxs-lookup"><span data-stu-id="b85f8-189">SM5.1 changes how resource registers are declared and referenced in instructions.</span></span> <span data-ttu-id="b85f8-190">La sintaxis implica declarar una "variable" de registro, de forma similar a como se hace para los registros de memoria compartida de grupo:</span><span class="sxs-lookup"><span data-stu-id="b85f8-190">The syntax involves declaring a register “variable”, similar to how it is done for group shared memory registers:</span></span>

``` syntax
Texture2D<float4> tex0          : register(t5,  space0);
Texture2D<float4> tex1[][5][3]  : register(t10, space0);
Texture2D<float4> tex2[8]       : register(t0,  space1);
SamplerState samp0              : register(s5, space0);

float4 main(float4 coord : COORD) : SV_TARGET
{
    float4 r = coord;
    r += tex0.Sample(samp0, r.xy);
    r += tex2[r.x].Sample(samp0, r.xy);
    r += tex1[r.x][r.y][r.z].Sample(samp0, r.xy);
    return r;
}
```

<span data-ttu-id="b85f8-191">Esto se desensamblará para:</span><span class="sxs-lookup"><span data-stu-id="b85f8-191">This will disassemble to:</span></span>

``` syntax
// Resource Bindings:
//
// Name                                 Type  Format         Dim    ID   HLSL Bind     Count
// ------------------------------ ---------- ------- ----------- -----   --------- ---------
// samp0                             sampler      NA          NA     S0    a5            1
// tex0                              texture  float4          2d     T0    t5            1
// tex1[0][5][3]                     texture  float4          2d     T1   t10        unbounded
// tex2[8]                           texture  float4          2d     T2    t0.space1     8
//
//
//
// Input signature:
//
// Name                 Index   Mask Register SysValue  Format   Used
// -------------------- ----- ------ -------- -------- ------- ------
// COORD                    0   xyzw        0     NONE   float   xyzw
//
//
// Output signature:
//
// Name                 Index   Mask Register SysValue  Format   Used
// -------------------- ----- ------ -------- -------- ------- ------
// SV_TARGET                0   xyzw        0   TARGET   float   xyzw
//
ps_5_1
dcl_globalFlags refactoringAllowed
dcl_sampler s0[5:5], mode_default, space=0
dcl_resource_texture2d (float,float,float,float) t0[5:5], space=0
dcl_resource_texture2d (float,float,float,float) t1[10:*], space=0
dcl_resource_texture2d (float,float,float,float) t2[0:7], space=1
dcl_input_ps linear v0.xyzw
dcl_output o0.xyzw
dcl_temps 2
sample r0.xyzw, v0.xyxx, t0[0].xyzw, s0[5]
add r0.xyzw, r0.xyzw, v0.xyzw
ftou r1.x, r0.x
sample r1.xyzw, r0.xyxx, t2[r1.x + 0].xyzw, s0[5]
add r0.xyzw, r0.xyzw, r1.xyzw
ftou r1.xyz, r0.zyxz
imul null, r1.yz, r1.zzyz, l(0, 15, 3, 0)
iadd r1.y, r1.z, r1.y
iadd r1.x, r1.x, r1.y
sample r1.xyzw, r0.xyxx, t1[r1.x + 10].xyzw, s0[5]
add o0.xyzw, r0.xyzw, r1.xyzw
ret
// Approximately 12 instruction slots are used.
```

<span data-ttu-id="b85f8-192">Ahora, cada intervalo de recursos de sombreador tiene un identificador (un nombre) que es único para el código de bytes del sombreador.</span><span class="sxs-lookup"><span data-stu-id="b85f8-192">Each shader resource range now has an ID (a name) that is unique to the shader bytecode.</span></span> <span data-ttu-id="b85f8-193">Por ejemplo, la matriz de texturas texas1 (t10) se convierte en "T1" en el código de bytes del sombreador.</span><span class="sxs-lookup"><span data-stu-id="b85f8-193">For example, tex1 (t10) texture array becomes ‘T1’ in the shader bytecode.</span></span> <span data-ttu-id="b85f8-194">La asignación de identificadores únicos a cada intervalo de recursos permite dos cosas:</span><span class="sxs-lookup"><span data-stu-id="b85f8-194">Giving unique IDs to each resource range allows two things:</span></span>

-   <span data-ttu-id="b85f8-195">Identifique de forma inequívoca qué intervalo de recursos (consulte dcl resource texture2d) que se indexa en una instrucción \_ \_ (consulte la instrucción de ejemplo).</span><span class="sxs-lookup"><span data-stu-id="b85f8-195">Unambiguously identify which resource range (see dcl\_resource\_texture2d) is being indexed in an instruction (see sample instruction).</span></span>
-   <span data-ttu-id="b85f8-196">Adjuntar un conjunto de atributos a la declaración, por ejemplo, tipo de elemento, tamaño de paso, modo de operación de trama, etc.</span><span class="sxs-lookup"><span data-stu-id="b85f8-196">Attaching a set of attributes to the declaration, e.g., element type, stride size, raster operation mode, etc.</span></span>

<span data-ttu-id="b85f8-197">Tenga en cuenta que el identificador del intervalo no está relacionado con la declaración de límite inferior HLSL.</span><span class="sxs-lookup"><span data-stu-id="b85f8-197">Note that the ID of the range is not related to the HLSL lower bound declaration.</span></span>

<span data-ttu-id="b85f8-198">El orden de los enlaces de recursos de reflexión (lista en la parte superior) y las instrucciones de declaración de sombreador (dcl) es el mismo para ayudar a identificar la correspondencia entre variables HLSL e identificadores de código \_ \* de bytes.</span><span class="sxs-lookup"><span data-stu-id="b85f8-198">The order of reflection resource bindings (listing at the top) and shader declaration instructions (dcl\_\*) is the same to aid in identifying the correspondence between HLSL variables and bytecode IDs.</span></span>

<span data-ttu-id="b85f8-199">Cada instrucción de declaración de SM5.1 usa un operando 3D para definir: id. de intervalo, límites inferior y superior.</span><span class="sxs-lookup"><span data-stu-id="b85f8-199">Each declaration instruction in SM5.1 uses a 3D operand to define: range ID, lower and upper bounds.</span></span> <span data-ttu-id="b85f8-200">Se emite un token adicional para especificar el espacio de registro.</span><span class="sxs-lookup"><span data-stu-id="b85f8-200">An additional token is emitted to specify the register space.</span></span> <span data-ttu-id="b85f8-201">También se pueden emitir otros tokens para transmitir propiedades adicionales del intervalo, por ejemplo, la instrucción de declaración de búfer estructurado o de cbuffer emite el tamaño del búfer o la estructura.</span><span class="sxs-lookup"><span data-stu-id="b85f8-201">Other tokens may be emitted as well to convey additional properties of the range, e.g., cbuffer or structured buffer declaration instruction emits the size of the cbuffer or structure.</span></span> <span data-ttu-id="b85f8-202">Los detalles exactos de la codificación se pueden encontrar en d3d12TokenizedProgramFormat.h y **D3D10ShaderBinary::CShaderCodeParser**.</span><span class="sxs-lookup"><span data-stu-id="b85f8-202">The exact details of encoding can be found in d3d12TokenizedProgramFormat.h and **D3D10ShaderBinary::CShaderCodeParser**.</span></span>

<span data-ttu-id="b85f8-203">Las instrucciones SM5.1 no emitirán información adicional sobre operandos de recursos como parte de la instrucción (como en SM5.0).</span><span class="sxs-lookup"><span data-stu-id="b85f8-203">SM5.1 instructions will not emit additional resource operand information as part of the instruction (as in SM5.0).</span></span> <span data-ttu-id="b85f8-204">Esta información se encuentra ahora en las instrucciones de declaración.</span><span class="sxs-lookup"><span data-stu-id="b85f8-204">This information is now in the declaration instructions.</span></span> <span data-ttu-id="b85f8-205">En SM5.0, las instrucciones de indexación de recursos requerían que los atributos de recursos se describieron en tokens de código de operación extendidos, ya que la indexación ofuscaba la asociación a la declaración.</span><span class="sxs-lookup"><span data-stu-id="b85f8-205">In SM5.0, instructions indexing resources required resource attributes to be described in extended opcode tokens, since indexing obfuscated the association to the declaration.</span></span> <span data-ttu-id="b85f8-206">En SM5.1, cada identificador (como "t1") está asociado inequívocamente a una única declaración que describe la información de recursos necesaria.</span><span class="sxs-lookup"><span data-stu-id="b85f8-206">In SM5.1, each ID (such as ‘t1’) is unambiguously associated with a single declaration that describes the required resource information.</span></span> <span data-ttu-id="b85f8-207">Por lo tanto, ya no se emiten los tokens de código de operación extendidos que se usan en las instrucciones para describir la información de recursos.</span><span class="sxs-lookup"><span data-stu-id="b85f8-207">Therefore, the extended opcode tokens used on instructions to describe resource information are no longer emitted.</span></span>

<span data-ttu-id="b85f8-208">En las instrucciones que no son de declaración, un operando de recurso para muestreadores, SRV y UAV es un operando 2D.</span><span class="sxs-lookup"><span data-stu-id="b85f8-208">In non-declaration instructions, a resource operand for samplers, SRVs, and UAVs is a 2D operand.</span></span> <span data-ttu-id="b85f8-209">El primer índice es una constante literal que especifica el identificador de intervalo.</span><span class="sxs-lookup"><span data-stu-id="b85f8-209">The first index is a literal constant that specifies the range ID.</span></span> <span data-ttu-id="b85f8-210">El segundo índice representa el valor linealizado del índice.</span><span class="sxs-lookup"><span data-stu-id="b85f8-210">The second index represents the linearized value of the index.</span></span> <span data-ttu-id="b85f8-211">El valor se calcula con respecto al principio del espacio de registro correspondiente (no relativo al principio del intervalo lógico) para correlacionar mejor con la firma raíz y reducir la carga del compilador del controlador de ajustar el índice.</span><span class="sxs-lookup"><span data-stu-id="b85f8-211">The value is computed relative to the beginning of the corresponding register space (not relative to the beginning of the logical range) to better correlate with the root signature and to reduce the driver compiler burden of adjusting the index.</span></span>

<span data-ttu-id="b85f8-212">Un operando de recurso para CBV es un operando 3D que contiene: identificador literal del intervalo, índice del búfer constante, desplazamiento en la instancia concreta del búfer constante.</span><span class="sxs-lookup"><span data-stu-id="b85f8-212">A resource operand for CBVs is a 3D operand, containing: literal ID of the range, index of the constant buffer, offset into the particular instance of constant buffer.</span></span>

## <a name="example-hlsl-declarations"></a><span data-ttu-id="b85f8-213">Declaraciones HLSL de ejemplo</span><span class="sxs-lookup"><span data-stu-id="b85f8-213">Example HLSL Declarations</span></span>

<span data-ttu-id="b85f8-214">Los programas HLSL no necesitan saber nada sobre las firmas raíz.</span><span class="sxs-lookup"><span data-stu-id="b85f8-214">HLSL programs do not need to know anything about root signatures.</span></span> <span data-ttu-id="b85f8-215">Pueden asignar enlaces al espacio de enlace "registrar" virtual, t para SRV, u para UAV, b para CBV, s para muestreadores o confiar en el compilador para elegir asignaciones (y consultar las asignaciones resultantes mediante la reflexión del \# \# \# \# sombreador más adelante).</span><span class="sxs-lookup"><span data-stu-id="b85f8-215">They can assign bindings to the virtual “register” binding space, t\# for SRVs, u\# for UAVs, b\# for CBVs, s\# for samplers, or rely on the compiler to pick assignments (and query the resulting mappings using shader reflection afterwards).</span></span> <span data-ttu-id="b85f8-216">La firma raíz asigna tablas de descriptores, descriptores raíz y constantes raíz a este espacio de registro virtual.</span><span class="sxs-lookup"><span data-stu-id="b85f8-216">The root signature maps descriptor tables, root descriptors, and root constants to this virtual register space.</span></span>

<span data-ttu-id="b85f8-217">Las siguientes son algunas declaraciones de ejemplo que podría tener un sombreador HLSL.</span><span class="sxs-lookup"><span data-stu-id="b85f8-217">The following are some example declarations an HLSL shader might have.</span></span> <span data-ttu-id="b85f8-218">Tenga en cuenta que no hay referencias a las firmas raíz ni a las tablas de descriptores.</span><span class="sxs-lookup"><span data-stu-id="b85f8-218">Note that there are no references to root signatures or descriptor tables.</span></span>

``` syntax
Texture2D foo[5] : register(t2);
Buffer bar : register(t7);
RWBuffer dataLog : register(u1);

Sampler samp : register(s0);

struct Data
{
    UINT index;
    float4 color;
};
ConstantBuffer<Data> myData : register(b0);

Texture2D terrain[] : register(t8); // Unbounded array
Texture2D misc[] : register(t0,space1); // Another unbounded array 
                                        // space1 avoids overlap with above t#

struct MoreData
{
    float4x4 xform;
};
ConstantBuffer<MoreData> myMoreData : register(b1);

struct Stuff
{
    float2 factor;
    UINT drawID;
};
ConstantBuffer<Stuff> myStuff[][3][8]  : register(b2, space3)
```

## <a name="related-topics"></a><span data-ttu-id="b85f8-219">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b85f8-219">Related topics</span></span>

* [<span data-ttu-id="b85f8-220">Indexado dinámico mediante HLSL 5.1</span><span class="sxs-lookup"><span data-stu-id="b85f8-220">Dynamic Indexing using HLSL 5.1</span></span>](dynamic-indexing-using-hlsl-5-1.md)
* [<span data-ttu-id="b85f8-221">Herramienta Effect-Compiler</span><span class="sxs-lookup"><span data-stu-id="b85f8-221">Effect-Compiler Tool</span></span>](../direct3dtools/fxc.md)
* [<span data-ttu-id="b85f8-222">Características del modelo de sombreador HLSL 5.1 para Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="b85f8-222">HLSL Shader Model 5.1 Features for Direct3D 12</span></span>](../direct3dhlsl/hlsl-shader-model-5-1-features-for-direct3d-12.md)
* [<span data-ttu-id="b85f8-223">Vistas ordenadas por el rasterizador</span><span class="sxs-lookup"><span data-stu-id="b85f8-223">Rasterizer Ordered Views</span></span>](rasterizer-order-views.md)
* [<span data-ttu-id="b85f8-224">Enlace de recursos</span><span class="sxs-lookup"><span data-stu-id="b85f8-224">Resource Binding</span></span>](resource-binding.md)
* [<span data-ttu-id="b85f8-225">Firmas raíz</span><span class="sxs-lookup"><span data-stu-id="b85f8-225">Root Signatures</span></span>](root-signatures.md)
* [<span data-ttu-id="b85f8-226">Modelo de sombreador 5.1</span><span class="sxs-lookup"><span data-stu-id="b85f8-226">Shader Model 5.1</span></span>](../direct3dhlsl/shader-model-5-1.md)
* [<span data-ttu-id="b85f8-227">Valor de la referencia de galería de símbolos especificado por el sombreador</span><span class="sxs-lookup"><span data-stu-id="b85f8-227">Shader Specified Stencil Reference Value</span></span>](shader-specified-stencil-reference-value.md)
* [<span data-ttu-id="b85f8-228">Especificación de firmas de raíz en HLSL</span><span class="sxs-lookup"><span data-stu-id="b85f8-228">Specifying Root Signatures in HLSL</span></span>](specifying-root-signatures-in-hlsl.md)