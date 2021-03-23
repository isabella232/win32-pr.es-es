---
title: Enlace de recursos en HLSL
description: En este tema se describen algunas características específicas del uso del modelo de sombreador del lenguaje HLSL (High Level Shader Language) 5,1 con Direct3D 12.
ms.assetid: 3CD4BDAD-8AE3-4DE0-B3F8-9C9F9E83BBE9
ms.localizationpriority: high
ms.topic: article
ms.date: 08/27/2019
ms.openlocfilehash: 749fed319f9ffe840f2b06512e337efa28081e24
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104549142"
---
# <a name="resource-binding-in-hlsl"></a><span data-ttu-id="3829b-103">Enlace de recursos en HLSL</span><span class="sxs-lookup"><span data-stu-id="3829b-103">Resource binding in HLSL</span></span>

<span data-ttu-id="3829b-104">En este tema se describen algunas características específicas del uso del [modelo de sombreador](/windows/desktop/direct3dhlsl/shader-model-5-1) del lenguaje HLSL (High Level Shader Language) 5,1 con Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="3829b-104">This topic describes some specific features of using High Level Shader Language (HLSL) [Shader Model 5.1](/windows/desktop/direct3dhlsl/shader-model-5-1) with Direct3D 12.</span></span> <span data-ttu-id="3829b-105">Todo el hardware de Direct3D 12 admite el modelo de sombreador 5,1, por lo que la compatibilidad con este modelo no depende de cuál sea el nivel de características de hardware.</span><span class="sxs-lookup"><span data-stu-id="3829b-105">All Direct3D 12 hardware supports Shader Model 5.1, so support for this model does not depend on what the hardware feature level is.</span></span>

-   [<span data-ttu-id="3829b-106">Tipos de recursos y matrices</span><span class="sxs-lookup"><span data-stu-id="3829b-106">Resource types and arrays</span></span>](#resource-types-and-arrays)
-   [<span data-ttu-id="3829b-107">Matrices de descriptores y matrices de texturas</span><span class="sxs-lookup"><span data-stu-id="3829b-107">Descriptor arrays and texture arrays</span></span>](#descriptor-arrays-and-texture-arrays)
-   [<span data-ttu-id="3829b-108">Alias de recursos</span><span class="sxs-lookup"><span data-stu-id="3829b-108">Resource aliasing</span></span>](#resource-aliasing)
-   [<span data-ttu-id="3829b-109">Divergencia y derivados</span><span class="sxs-lookup"><span data-stu-id="3829b-109">Divergence and derivatives</span></span>](#divergence-and-derivatives)
-   [<span data-ttu-id="3829b-110">UAVs en sombreadores de píxeles</span><span class="sxs-lookup"><span data-stu-id="3829b-110">UAVs in pixel shaders</span></span>](#uavs-in-pixel-shaders)
-   [<span data-ttu-id="3829b-111">Búferes de constantes</span><span class="sxs-lookup"><span data-stu-id="3829b-111">Constant Buffers</span></span>](#constant-buffers)
-   [<span data-ttu-id="3829b-112">Cambios de código de bytes en SM 5.1</span><span class="sxs-lookup"><span data-stu-id="3829b-112">Bytecode changes in SM5.1</span></span>](#bytecode-changes-in-sm51)
-   [<span data-ttu-id="3829b-113">Declaraciones de ejemplo de HLSL</span><span class="sxs-lookup"><span data-stu-id="3829b-113">Example HLSL Declarations</span></span>](#example-hlsl-declarations)
-   [<span data-ttu-id="3829b-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3829b-114">Related topics</span></span>](#related-topics)

## <a name="resource-types-and-arrays"></a><span data-ttu-id="3829b-115">Tipos de recursos y matrices</span><span class="sxs-lookup"><span data-stu-id="3829b-115">Resource types and arrays</span></span>

<span data-ttu-id="3829b-116">La sintaxis de recursos del modelo de sombreador 5 (SM 5.0) usa la `register` palabra clave para retransmitir información importante sobre el recurso al compilador de HLSL.</span><span class="sxs-lookup"><span data-stu-id="3829b-116">Shader Model 5 (SM5.0) resource syntax uses the `register` keyword to relay important information about the resource to the HLSL compiler.</span></span> <span data-ttu-id="3829b-117">Por ejemplo, la instrucción siguiente declara una matriz de cuatro texturas enlazadas a las ranuras T3, T4, T5 y T6.</span><span class="sxs-lookup"><span data-stu-id="3829b-117">For example, the following statement declares an array of four textures bound at slots t3, t4, t5, and t6.</span></span> <span data-ttu-id="3829b-118">T3 es la única ranura de registro que aparece en la instrucción, simplemente siendo la primera en la matriz de cuatro.</span><span class="sxs-lookup"><span data-stu-id="3829b-118">t3 is the only register slot appearing in the statement, simply being the first in the array of four.</span></span>

``` syntax
Texture2D<float4> tex1[4] : register(t3)
```

<span data-ttu-id="3829b-119">La sintaxis de recursos del modelo de sombreador 5,1 (SM 5.1) en HLSL se basa en la sintaxis de recursos de registro existente para permitir una migración más sencilla.</span><span class="sxs-lookup"><span data-stu-id="3829b-119">Shader Model 5.1 (SM5.1) resource syntax in HLSL is based on existing register resource syntax, to allow easier porting.</span></span> <span data-ttu-id="3829b-120">Los recursos de Direct3D 12 en HLSL están enlazados a registros virtuales dentro de espacios de registro lógicos:</span><span class="sxs-lookup"><span data-stu-id="3829b-120">Direct3D 12 resources in HLSL are bound to virtual registers within logical register spaces:</span></span>

-   <span data-ttu-id="3829b-121">t: para vistas de recursos del sombreador (SRV)</span><span class="sxs-lookup"><span data-stu-id="3829b-121">t – for shader resource views (SRV)</span></span>
-   <span data-ttu-id="3829b-122">s: para muestreadores</span><span class="sxs-lookup"><span data-stu-id="3829b-122">s – for samplers</span></span>
-   <span data-ttu-id="3829b-123">u: para vistas de acceso desordenado (UAV)</span><span class="sxs-lookup"><span data-stu-id="3829b-123">u – for unordered access views (UAV)</span></span>
-   <span data-ttu-id="3829b-124">b: para las vistas de búfer de constantes (CBV)</span><span class="sxs-lookup"><span data-stu-id="3829b-124">b – for constant buffer views (CBV)</span></span>

<span data-ttu-id="3829b-125">La firma raíz que hace referencia al sombreador debe ser compatible con las ranuras de registro declaradas.</span><span class="sxs-lookup"><span data-stu-id="3829b-125">The root signature referencing the shader must be compatible with the declared register slots.</span></span> <span data-ttu-id="3829b-126">Por ejemplo, la siguiente parte de una firma raíz sería compatible con el uso de ranuras de textura T3 a través de T6, ya que describe una tabla de descriptores con ranuras de T0 a T98.</span><span class="sxs-lookup"><span data-stu-id="3829b-126">For example, the following portion of a root signature would be compatible with the use of texture slots t3 through t6, as it describes a descriptor table with slots t0 through t98.</span></span>

``` syntax
DescriptorTable( CBV(b1), SRV(t0,numDescriptors=99), CBV(b2) )
```

<span data-ttu-id="3829b-127">Una declaración de recursos puede ser una matriz escalar, 1D o multidimensional:</span><span class="sxs-lookup"><span data-stu-id="3829b-127">A resource declaration may be a scalar, a 1D array, or a multidimensional array:</span></span>

``` syntax
Texture2D<float4> tex1 : register(t3,  space0)
Texture2D<float4> tex2[4] : register(t10)
Texture2D<float4> tex3[7][5][3] : register(t20, space1)
```

<span data-ttu-id="3829b-128">SM 5.1 usa los mismos tipos de recursos y tipos de elemento que el SM 5.0.</span><span class="sxs-lookup"><span data-stu-id="3829b-128">SM5.1 uses the same resource types and element types as SM5.0 does.</span></span> <span data-ttu-id="3829b-129">Los límites de declaración de SM 5.1 son más flexibles y solo están restringidos por los límites de hardware y tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="3829b-129">SM5.1 declaration limits are more flexible, and constrained only by the runtime/hardware limits.</span></span> <span data-ttu-id="3829b-130">La `space` palabra clave especifica el espacio de registro lógico al que está enlazada la variable declarada.</span><span class="sxs-lookup"><span data-stu-id="3829b-130">The `space` keyword specifies to which logical register space the declared variable is bound.</span></span> <span data-ttu-id="3829b-131">Si `space` se omite la palabra clave, el índice de espacio predeterminado de 0 se asigna implícitamente al intervalo (por lo que el `tex2` intervalo anterior reside en `space0` ).</span><span class="sxs-lookup"><span data-stu-id="3829b-131">If the `space` keyword is omitted, then the default space index of 0 is implicitly assigned to the range (so the `tex2` range above resides in `space0`).</span></span> <span data-ttu-id="3829b-132">`register(t3,  space0)` nunca entrará en conflicto con `register(t3,  space1)` , ni con ninguna matriz en otro espacio que podría incluir T3.</span><span class="sxs-lookup"><span data-stu-id="3829b-132">`register(t3,  space0)` will never conflict with `register(t3,  space1)`, nor with any array in another space that might include t3.</span></span>

<span data-ttu-id="3829b-133">Un recurso de matriz puede tener un tamaño sin enlazar, que se declara especificando la primera dimensión que está vacía, o 0:</span><span class="sxs-lookup"><span data-stu-id="3829b-133">An array resource may have an unbounded size, which is declared by specifying the very first dimension to be empty, or 0:</span></span>

``` syntax
Texture2D<float4> tex1[] : register(t0)
```

<span data-ttu-id="3829b-134">La tabla del descriptor coincidente podría ser:</span><span class="sxs-lookup"><span data-stu-id="3829b-134">The matching descriptor table could be:</span></span>

``` syntax
DescriptorTable( CBV(b1), UAV(u0, numDescriptors = 4), SRV(t0, numDescriptors=unbounded)
```

<span data-ttu-id="3829b-135">Una matriz sin enlazar en HLSL coincide con un número fijo establecido con `numDescriptors` en la tabla de descriptores y un tamaño fijo en HLSL coincide con una declaración sin enlazar en la tabla de descriptores.</span><span class="sxs-lookup"><span data-stu-id="3829b-135">An unbounded array in HLSL does match a fixed number set with `numDescriptors` in the descriptor table, and a fixed size in the HLSL does match an unbounded declaration in the descriptor table.</span></span>

<span data-ttu-id="3829b-136">Se permiten matrices multidimensionales, incluido un tamaño sin enlazar.</span><span class="sxs-lookup"><span data-stu-id="3829b-136">Multi-dimensional arrays are allowed, including of an unbounded size.</span></span> <span data-ttu-id="3829b-137">Estas matrices multidimensionales se separan en el espacio de registro.</span><span class="sxs-lookup"><span data-stu-id="3829b-137">These multidimensional arrays are flattened out in register space.</span></span>

``` syntax
Texture2D<float4> tex2[3000][10] : register(t0, space0); // t0-t29999 in space0
Texture2D<float4> tex3[0][5][3] : register(t5, space1)
```

<span data-ttu-id="3829b-138">No se permiten los alias de los intervalos de recursos.</span><span class="sxs-lookup"><span data-stu-id="3829b-138">Aliasing of resource ranges is not allowed.</span></span> <span data-ttu-id="3829b-139">En otras palabras, para cada tipo de recurso (t, s, u, b), los intervalos de registro declarados no debe se superponen.</span><span class="sxs-lookup"><span data-stu-id="3829b-139">In other words, for each resource type (t, s, u, b), declared register ranges mustn't overlap.</span></span> <span data-ttu-id="3829b-140">Esto incluye también los intervalos sin enlazar.</span><span class="sxs-lookup"><span data-stu-id="3829b-140">That includes unbounded ranges, too.</span></span> <span data-ttu-id="3829b-141">Los rangos declarados en diferentes espacios de registro nunca se superponen.</span><span class="sxs-lookup"><span data-stu-id="3829b-141">Ranges declared in different register spaces never overlap.</span></span> <span data-ttu-id="3829b-142">Tenga en cuenta que el modo sin enlazar `tex2` (anterior) reside en `space0` , mientras que sin enlazar `tex3` reside en, de forma `space1` que no se superpongan.</span><span class="sxs-lookup"><span data-stu-id="3829b-142">Note that unbounded `tex2` (above) resides in `space0`, while unbounded `tex3` resides in `space1`, such that they don't overlap.</span></span>

<span data-ttu-id="3829b-143">El acceso a los recursos que se han declarado como matrices es tan sencillo como indexarlos.</span><span class="sxs-lookup"><span data-stu-id="3829b-143">Accessing resources that have been declared as arrays is as simple as indexing them.</span></span>

``` syntax
Texture2D<float4> tex1[400] : register(t3);
sampler samp[7] : register(s0);
tex1[myMaterialID].Sample(samp[samplerID], texCoords);
```

<span data-ttu-id="3829b-144">Existe una restricción predeterminada importante en el uso de los índices ( `myMaterialID` y `samplerID` en el código anterior) en que no se les permite variar dentro de una [onda](../direct3dhlsl/hlsl-shader-model-6-0-features-for-direct3d-12.md#terminology).</span><span class="sxs-lookup"><span data-stu-id="3829b-144">There's an important default restriction on the use of the indices (`myMaterialID` and `samplerID` in the code above) in that they're not allowed to vary within a [wave](../direct3dhlsl/hlsl-shader-model-6-0-features-for-direct3d-12.md#terminology).</span></span> <span data-ttu-id="3829b-145">Incluso cambiar el índice basado en la creación de instancias cuenta como variable.</span><span class="sxs-lookup"><span data-stu-id="3829b-145">Even changing the index based on instancing counts as varying.</span></span>

<span data-ttu-id="3829b-146">Si se requiere variar el índice, especifique el `NonUniformResourceIndex` calificador en el índice, por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="3829b-146">If varying the index is required then specify the `NonUniformResourceIndex` qualifier on the index, for example:</span></span>

``` syntax
tex1[NonUniformResourceIndex(myMaterialID)].Sample(samp[NonUniformResourceIndex(samplerID)], texCoords);
```

<span data-ttu-id="3829b-147">En el hardware, el uso de este calificador genera código adicional para aplicar la corrección (incluidos entre subprocesos), pero con un costo de rendimiento menor.</span><span class="sxs-lookup"><span data-stu-id="3829b-147">On some hardware the use of this qualifier generates additional code to enforce correctness (including across threads) but at a minor performance cost.</span></span> <span data-ttu-id="3829b-148">Si se cambia un índice sin este calificador y, dentro de un dibujo o una distribución, los resultados son indefinidos.</span><span class="sxs-lookup"><span data-stu-id="3829b-148">If an index is changed without this qualifier and within a draw/dispatch the results are undefined.</span></span>

## <a name="descriptor-arrays-and-texture-arrays"></a><span data-ttu-id="3829b-149">Matrices de descriptores y matrices de texturas</span><span class="sxs-lookup"><span data-stu-id="3829b-149">Descriptor arrays and texture arrays</span></span>

<span data-ttu-id="3829b-150">Las matrices de texturas están disponibles desde DirectX 10.</span><span class="sxs-lookup"><span data-stu-id="3829b-150">Texture arrays have been available since DirectX 10.</span></span> <span data-ttu-id="3829b-151">Las matrices de textura requieren un descriptor; sin embargo, todos los segmentos de la matriz deben compartir el mismo formato, el ancho, el alto y el número de MIP.</span><span class="sxs-lookup"><span data-stu-id="3829b-151">Texture arrays require one descriptor, however all the array slices must share the same format, width, height and mip count.</span></span> <span data-ttu-id="3829b-152">Además, la matriz debe ocupar un intervalo contiguo en el espacio de direcciones virtuales.</span><span class="sxs-lookup"><span data-stu-id="3829b-152">Also, the array must occupy a contiguous range in virtual address space.</span></span> <span data-ttu-id="3829b-153">En el código siguiente se muestra un ejemplo del acceso a una matriz de textura desde un sombreador.</span><span class="sxs-lookup"><span data-stu-id="3829b-153">The following code shows an example of accessing a texture array from a shader.</span></span>

``` syntax
float3 myCoord(1.0f,1.4f,2.2f); // 2.2f is array index (rounded to int)
color = myTex2DArray.Sample(mySampler, myCoord);
```

<span data-ttu-id="3829b-154">En una matriz de textura, el índice se puede variar libremente, sin necesidad de calificadores como `NonUniformResourceIndex` .</span><span class="sxs-lookup"><span data-stu-id="3829b-154">In a texture array, the index can be varied freely, without any need for qualifiers such as `NonUniformResourceIndex`.</span></span>

<span data-ttu-id="3829b-155">La matriz de descriptor equivalente sería:</span><span class="sxs-lookup"><span data-stu-id="3829b-155">The equivalent descriptor array would be:</span></span>

``` syntax
Texture2D<float4> myTex2DArray[] : register(t0); // t0+
float2 myCoord(1.0f, 1.4f);
color = myTex2D[2].Sample(mySampler,myCoord); // 2 is index
```

<span data-ttu-id="3829b-156">Tenga en cuenta que el uso poco práctico de un valor Float para el índice de matriz se reemplaza por `myTex2D[2]` .</span><span class="sxs-lookup"><span data-stu-id="3829b-156">Note the awkward use of a float for the array index is replaced with `myTex2D[2]`.</span></span> <span data-ttu-id="3829b-157">Además, las matrices de descriptor ofrecen más flexibilidad con las dimensiones.</span><span class="sxs-lookup"><span data-stu-id="3829b-157">Also descriptor arrays offer more flexibility with the dimensions.</span></span> <span data-ttu-id="3829b-158">El tipo, `Texture2D` es este ejemplo, no puede variar, pero el formato, el ancho, el alto y el número de MIP pueden variar con cada descriptor.</span><span class="sxs-lookup"><span data-stu-id="3829b-158">The type, `Texture2D` is this example, cannot vary, but the format, width, height, and mip count can all vary with each descriptor.</span></span>

<span data-ttu-id="3829b-159">Es legítimo tener una matriz de descriptores de matrices de texturas:</span><span class="sxs-lookup"><span data-stu-id="3829b-159">It is legitimate to have a descriptor array of texture arrays:</span></span>

``` syntax
Texture2DArray<float4> myTex2DArrayOfArrays[2] : register(t0);
```

<span data-ttu-id="3829b-160">No es legítimo declarar una matriz de estructuras, por ejemplo, no se admite cada estructura que contiene descriptores.</span><span class="sxs-lookup"><span data-stu-id="3829b-160">It is not legitimate to declare an array of structures, each structure containing descriptors, for example the following code is not supported.</span></span>

``` syntax
struct myStruct {
    Texture2D                    a; 
    Texture2D                    b;
    ConstantBuffer<myConstants>  c;
};
myStruct foo[10000] : register(....);
```

<span data-ttu-id="3829b-161">Esto habría permitido el diseño de memoria **abcabcabc...**, pero es una limitación de idioma y no se admite.</span><span class="sxs-lookup"><span data-stu-id="3829b-161">This would have allowed the memory layout **abcabcabc....**, but is a language limitation and is not supported.</span></span> <span data-ttu-id="3829b-162">Un método admitido para hacerlo sería el siguiente, aunque en este caso el diseño de memoria es **AAA... BBB... CCC..**..</span><span class="sxs-lookup"><span data-stu-id="3829b-162">One supported method of doing this would be as follows, though the memory layout in this case is **aaa...bbb...ccc...**.</span></span>

``` syntax
Texture2D                     a[10000] : register(t0);
Texture2D                     b[10000] : register(t10000);
ConstantBuffer<myConstants>   c[10000] : register(b0);
```

<span data-ttu-id="3829b-163">Para lograr el diseño de memoria **abcabcabc....** , use una tabla de descriptores sin usar la `myStruct` estructura.</span><span class="sxs-lookup"><span data-stu-id="3829b-163">To achieve the **abcabcabc....** memory layout, use a descriptor table without use of the `myStruct` structure.</span></span>

## <a name="resource-aliasing"></a><span data-ttu-id="3829b-164">Alias de recursos</span><span class="sxs-lookup"><span data-stu-id="3829b-164">Resource aliasing</span></span>

<span data-ttu-id="3829b-165">Los intervalos de recursos especificados en los sombreadores HLSL son intervalos lógicos.</span><span class="sxs-lookup"><span data-stu-id="3829b-165">The resource ranges specified in the HLSL shaders are logical ranges.</span></span> <span data-ttu-id="3829b-166">Se enlazan a intervalos de montón concretos en tiempo de ejecución a través del mecanismo de firma raíz.</span><span class="sxs-lookup"><span data-stu-id="3829b-166">They are be bound to concrete heap ranges at runtime via the root signature mechanism.</span></span> <span data-ttu-id="3829b-167">Normalmente, un intervalo lógico se asigna a un intervalo de montón que no se superpone con otros intervalos de montón.</span><span class="sxs-lookup"><span data-stu-id="3829b-167">Normally, a logical range maps to a heap range that does not overlap with other heap ranges.</span></span> <span data-ttu-id="3829b-168">Sin embargo, el mecanismo de firma raíz permite el alias (superponer) los intervalos de montones de tipos compatibles.</span><span class="sxs-lookup"><span data-stu-id="3829b-168">However, the root signature mechanism makes it possible to alias (overlap) heap ranges of compatible types.</span></span> <span data-ttu-id="3829b-169">Por ejemplo, `tex2` los `tex3` intervalos del ejemplo anterior pueden estar asignados al mismo intervalo de montones (o superpuestos), lo que tiene el efecto de aplicar alias a las texturas en el programa HLSL.</span><span class="sxs-lookup"><span data-stu-id="3829b-169">For example, `tex2` and `tex3` ranges from the above example may be mapped to the same (or overlapping) heap range, which has the effect of aliasing textures in the HLSL program.</span></span> <span data-ttu-id="3829b-170">Si se desea usar este tipo de alias, el sombreador se debe compilar con la \_ \_ opción de alias D3D10 de los recursos del sombreador \_ \_ para la [herramienta de compilador de efectos](/windows/desktop/direct3dtools/fxc) (FXC). *\_ \_*</span><span class="sxs-lookup"><span data-stu-id="3829b-170">If such aliasing is desired, the shader must be compiled with D3D10\_SHADER\_RESOURCES\_MAY\_ALIAS option, which is set by using the */res\_may\_alias* option for the [Effect-Compiler Tool](/windows/desktop/direct3dtools/fxc) (FXC).</span></span> <span data-ttu-id="3829b-171">La opción hace que el compilador genere código correcto mediante la prevención de ciertas optimizaciones de carga y almacenamiento bajo la suposición de que los recursos pueden tener alias.</span><span class="sxs-lookup"><span data-stu-id="3829b-171">The option makes the compiler produce correct code by preventing certain load/store optimizations under the assumption that resources may alias.</span></span>

## <a name="divergence-and-derivatives"></a><span data-ttu-id="3829b-172">Divergencia y derivados</span><span class="sxs-lookup"><span data-stu-id="3829b-172">Divergence and derivatives</span></span>

<span data-ttu-id="3829b-173">SM 5.1 no impone limitaciones en el índice de recursos; es decir, ` tex2[idx].Sample(…)` : el índ de índice puede ser una constante literal, una constante CBuffer o un valor interpolado.</span><span class="sxs-lookup"><span data-stu-id="3829b-173">SM5.1 does not impose limitations on the resource index; i.e.,` tex2[idx].Sample(…)` – the index idx can be a literal constant, a cbuffer constant, or an interpolated value.</span></span> <span data-ttu-id="3829b-174">Aunque el modelo de programación proporciona una gran flexibilidad, hay problemas que debe tener en cuenta:</span><span class="sxs-lookup"><span data-stu-id="3829b-174">While the programming model provides such great flexibility, there are issues to be aware of:</span></span>

-   <span data-ttu-id="3829b-175">Si el índice difiere en un cuádruple, el derivado calculado por hardware y las cantidades derivadas como LOD pueden ser indefinidos.</span><span class="sxs-lookup"><span data-stu-id="3829b-175">If index diverges across a quad, the hardware-computed derivative and derived quantities such as LOD may be undefined.</span></span> <span data-ttu-id="3829b-176">El compilador de HLSL realiza el mejor esfuerzo para emitir una advertencia en este caso, pero no impedirá que se compile un sombreador.</span><span class="sxs-lookup"><span data-stu-id="3829b-176">The HLSL compiler makes the best effort to issue a warning in this case, but will not prevent a shader from compiling.</span></span> <span data-ttu-id="3829b-177">Este comportamiento es similar al cálculo de derivados en un flujo de control divergente.</span><span class="sxs-lookup"><span data-stu-id="3829b-177">This behavior is similar to computing derivatives in divergent control flow.</span></span>
-   <span data-ttu-id="3829b-178">Si el índice de recursos es divergente, el rendimiento se reduce en comparación con el caso de un índice uniforme, ya que el hardware necesita realizar operaciones en varios recursos.</span><span class="sxs-lookup"><span data-stu-id="3829b-178">If the resource index is divergent, the performance is diminished compared to the case of a uniform index, because the hardware needs to perform operations on several resources.</span></span> <span data-ttu-id="3829b-179">Los índices de recursos que pueden ser divergentes se deben marcar con la `NonUniformResourceIndex` función en el código HLSL.</span><span class="sxs-lookup"><span data-stu-id="3829b-179">Resource indexes that may be divergent must be marked with the `NonUniformResourceIndex` function in HLSL code.</span></span> <span data-ttu-id="3829b-180">De lo contrario, los resultados son indefinidos.</span><span class="sxs-lookup"><span data-stu-id="3829b-180">Otherwise results are undefined.</span></span>

## <a name="uavs-in-pixel-shaders"></a><span data-ttu-id="3829b-181">UAVs en sombreadores de píxeles</span><span class="sxs-lookup"><span data-stu-id="3829b-181">UAVs in pixel shaders</span></span>

<span data-ttu-id="3829b-182">SM 5.1 no impone restricciones en los intervalos de UAV en los sombreadores de píxeles como era el caso del SM 5.0.</span><span class="sxs-lookup"><span data-stu-id="3829b-182">SM5.1 does not impose constraints on UAV ranges in pixel shaders as was the case for SM5.0.</span></span>

## <a name="constant-buffers"></a><span data-ttu-id="3829b-183">Búferes de constantes</span><span class="sxs-lookup"><span data-stu-id="3829b-183">Constant Buffers</span></span>

<span data-ttu-id="3829b-184">La sintaxis de búferes de constantes de SM 5.1 (CBuffer) ha cambiado desde SM 5.0 para que los desarrolladores puedan indexar búferes de constantes.</span><span class="sxs-lookup"><span data-stu-id="3829b-184">SM5.1 constant buffers (cbuffer) syntax has changed from SM5.0 to enable developers to index constant buffers.</span></span> <span data-ttu-id="3829b-185">Para habilitar los búferes de constantes indexables, SM 5.1 presenta la `ConstantBuffer` construcción "template":</span><span class="sxs-lookup"><span data-stu-id="3829b-185">To enable indexable constant buffers, SM5.1 introduces the `ConstantBuffer` “template” construct:</span></span>

``` syntax
struct Foo
{
    float4 a;
    int2 b;
};
ConstantBuffer<Foo> myCB1[2][3] : register(b2, space1);
ConstantBuffer<Foo> myCB2 : register(b0, space1);
```

<span data-ttu-id="3829b-186">El código anterior declara una variable de búfer `myCB1` de constantes de tipo `Foo` y tamaño 6, y una variable de búfer escalar constante `myCB2` .</span><span class="sxs-lookup"><span data-stu-id="3829b-186">The preceding code declares constant buffer variable `myCB1` of type `Foo` and size 6, and a scalar, constant buffer variable `myCB2`.</span></span> <span data-ttu-id="3829b-187">Ahora se puede indexar una variable de búfer de constantes en el sombreador como:</span><span class="sxs-lookup"><span data-stu-id="3829b-187">A constant buffer variable can now be indexed in the shader as:</span></span>

``` syntax
myCB1[i][j].a.xyzw
myCB2.b.yy
```

<span data-ttu-id="3829b-188">Los campos ' a ' y ' b ' no se convierten en variables globales, sino que deben tratarse como campos.</span><span class="sxs-lookup"><span data-stu-id="3829b-188">Fields ‘a’ and ‘b’ do not become global variables, but rather must be treated as fields.</span></span> <span data-ttu-id="3829b-189">Por compatibilidad con versiones anteriores, SM 5.1 admite el concepto de CBuffer anterior para cbuffers escalar.</span><span class="sxs-lookup"><span data-stu-id="3829b-189">For backward compatibility, SM5.1 supports the old cbuffer concept for scalar cbuffers.</span></span> <span data-ttu-id="3829b-190">La instrucción siguiente crea variables globales de solo lectura ' a ' y ' b ' como en SM 5.0.</span><span class="sxs-lookup"><span data-stu-id="3829b-190">The following statement makes ‘a’ and ‘b’ global, read-only variables as in SM5.0.</span></span> <span data-ttu-id="3829b-191">Sin embargo, este tipo de CBuffer de estilo antiguo no se puede indexar.</span><span class="sxs-lookup"><span data-stu-id="3829b-191">However, such an old-style cbuffer cannot be indexable.</span></span>

``` syntax
cbuffer : register(b1)
{
    float4 a;
    int2 b;
};
```

<span data-ttu-id="3829b-192">Actualmente, el compilador de sombreador admite la `ConstantBuffer` plantilla solo para estructuras definidas por el usuario.</span><span class="sxs-lookup"><span data-stu-id="3829b-192">Currently, the shader compiler supports the `ConstantBuffer` template for user-defined structures only.</span></span>

<span data-ttu-id="3829b-193">Por motivos de compatibilidad, el compilador de HLSL puede asignar automáticamente registros de recursos para los intervalos declarados en `space0` .</span><span class="sxs-lookup"><span data-stu-id="3829b-193">For compatibility reasons, the HLSL compiler may automatically assign resource registers for ranges declared in `space0`.</span></span> <span data-ttu-id="3829b-194">Si se omite ' Space ' en la cláusula Register, se usa el valor predeterminado `space0` .</span><span class="sxs-lookup"><span data-stu-id="3829b-194">If ‘space’ is omitted in the register clause, the default `space0` is used.</span></span> <span data-ttu-id="3829b-195">El compilador usa la heurística del primer orificio para asignar los registros.</span><span class="sxs-lookup"><span data-stu-id="3829b-195">The compiler uses the first-hole-fits heuristic to assign the registers.</span></span> <span data-ttu-id="3829b-196">La asignación se puede recuperar a través de la API de reflexión, que se ha ampliado para agregar el campo de *espacio* para el espacio, mientras que el campo *BindPoint* indica el límite inferior del intervalo del registro de recursos.</span><span class="sxs-lookup"><span data-stu-id="3829b-196">The assignment can be retrieved via the reflection API, which has been extended to add the *Space* field for space, while the *BindPoint* field indicates the lower bound of the resource register range.</span></span>

## <a name="bytecode-changes-in-sm51"></a><span data-ttu-id="3829b-197">Cambios de código de bytes en SM 5.1</span><span class="sxs-lookup"><span data-stu-id="3829b-197">Bytecode changes in SM5.1</span></span>

<span data-ttu-id="3829b-198">SM 5.1 cambia el modo en que se declaran y se hace referencia a los registros de recursos en las instrucciones.</span><span class="sxs-lookup"><span data-stu-id="3829b-198">SM5.1 changes how resource registers are declared and referenced in instructions.</span></span> <span data-ttu-id="3829b-199">La sintaxis implica declarar una "variable" de registro, de forma similar a como se hace para los registros de memoria compartida de Grupo:</span><span class="sxs-lookup"><span data-stu-id="3829b-199">The syntax involves declaring a register “variable”, similar to how it is done for group shared memory registers:</span></span>

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

<span data-ttu-id="3829b-200">Esto se desensamblará en:</span><span class="sxs-lookup"><span data-stu-id="3829b-200">This will disassemble to:</span></span>

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

<span data-ttu-id="3829b-201">Ahora cada intervalo de recursos del sombreador tiene un identificador (un nombre) que es único para el código de bytes del sombreador.</span><span class="sxs-lookup"><span data-stu-id="3829b-201">Each shader resource range now has an ID (a name) that is unique to the shader bytecode.</span></span> <span data-ttu-id="3829b-202">Por ejemplo, la matriz de texturas de Tex1 (T10) se convierte en ' t 1 ' en el código de bytes del sombreador.</span><span class="sxs-lookup"><span data-stu-id="3829b-202">For example, tex1 (t10) texture array becomes ‘T1’ in the shader bytecode.</span></span> <span data-ttu-id="3829b-203">Asignar identificadores únicos a cada intervalo de recursos permite dos cosas:</span><span class="sxs-lookup"><span data-stu-id="3829b-203">Giving unique IDs to each resource range allows two things:</span></span>

-   <span data-ttu-id="3829b-204">Identifique de forma inequívoca qué intervalo de recursos (consulte DCL \_ Resource \_ texture2d) se está indizando en una instrucción (vea la instrucción de ejemplo).</span><span class="sxs-lookup"><span data-stu-id="3829b-204">Unambiguously identify which resource range (see dcl\_resource\_texture2d) is being indexed in an instruction (see sample instruction).</span></span>
-   <span data-ttu-id="3829b-205">Asociar un conjunto de atributos a la declaración, por ejemplo, tipo de elemento, tamaño de intervalo, modo de operación de trama, etc.</span><span class="sxs-lookup"><span data-stu-id="3829b-205">Attaching a set of attributes to the declaration, e.g., element type, stride size, raster operation mode, etc.</span></span>

<span data-ttu-id="3829b-206">Tenga en cuenta que el identificador del intervalo no está relacionado con la declaración de límite inferior de HLSL.</span><span class="sxs-lookup"><span data-stu-id="3829b-206">Note that the ID of the range is not related to the HLSL lower bound declaration.</span></span>

<span data-ttu-id="3829b-207">El orden de los enlaces de recursos de reflexión (enumeración en la parte superior) y las instrucciones de declaración de sombreador (DCL \_ \* ) es el mismo para ayudar a identificar la correspondencia entre las variables de HLSL y los ID. de código de bytes.</span><span class="sxs-lookup"><span data-stu-id="3829b-207">The order of reflection resource bindings (listing at the top) and shader declaration instructions (dcl\_\*) is the same to aid in identifying the correspondence between HLSL variables and bytecode IDs.</span></span>

<span data-ttu-id="3829b-208">Cada instrucción de declaración en SM 5.1 usa un operando 3D para definir: ID. de intervalo, límites inferior y superior.</span><span class="sxs-lookup"><span data-stu-id="3829b-208">Each declaration instruction in SM5.1 uses a 3D operand to define: range ID, lower and upper bounds.</span></span> <span data-ttu-id="3829b-209">Se emite un token adicional para especificar el espacio de registro.</span><span class="sxs-lookup"><span data-stu-id="3829b-209">An additional token is emitted to specify the register space.</span></span> <span data-ttu-id="3829b-210">También se pueden emitir otros tokens para transmitir propiedades adicionales del intervalo; por ejemplo, CBuffer o la instrucción de declaración de búfer estructurado emite el tamaño de la CBuffer o la estructura.</span><span class="sxs-lookup"><span data-stu-id="3829b-210">Other tokens may be emitted as well to convey additional properties of the range, e.g., cbuffer or structured buffer declaration instruction emits the size of the cbuffer or structure.</span></span> <span data-ttu-id="3829b-211">Los detalles exactos de la codificación se pueden encontrar en d3d12TokenizedProgramFormat. h y **D3D10ShaderBinary:: CShaderCodeParser**.</span><span class="sxs-lookup"><span data-stu-id="3829b-211">The exact details of encoding can be found in d3d12TokenizedProgramFormat.h and **D3D10ShaderBinary::CShaderCodeParser**.</span></span>

<span data-ttu-id="3829b-212">Las instrucciones de SM 5.1 no emitirán información adicional del operando de recursos como parte de la instrucción (como en SM 5.0).</span><span class="sxs-lookup"><span data-stu-id="3829b-212">SM5.1 instructions will not emit additional resource operand information as part of the instruction (as in SM5.0).</span></span> <span data-ttu-id="3829b-213">Esta información está ahora en las instrucciones de declaración.</span><span class="sxs-lookup"><span data-stu-id="3829b-213">This information is now in the declaration instructions.</span></span> <span data-ttu-id="3829b-214">En SM 5.0, instrucciones que indexan los recursos de recursos necesarios para describirse en tokens de código de operación extendidos, ya que la indización ofuscaba la asociación con la declaración.</span><span class="sxs-lookup"><span data-stu-id="3829b-214">In SM5.0, instructions indexing resources required resource attributes to be described in extended opcode tokens, since indexing obfuscated the association to the declaration.</span></span> <span data-ttu-id="3829b-215">En SM 5.1, cada identificador (como ' t 1 ') está asociado de forma no ambigua a una única declaración que describe la información de recursos necesaria.</span><span class="sxs-lookup"><span data-stu-id="3829b-215">In SM5.1, each ID (such as ‘t1’) is unambiguously associated with a single declaration that describes the required resource information.</span></span> <span data-ttu-id="3829b-216">Por lo tanto, los tokens de código de operación extendidos usados en las instrucciones para describir la información de recursos ya no se emiten.</span><span class="sxs-lookup"><span data-stu-id="3829b-216">Therefore, the extended opcode tokens used on instructions to describe resource information are no longer emitted.</span></span>

<span data-ttu-id="3829b-217">En las instrucciones que no son de declaración, un operando de recursos para muestreadores, SRVs y UAVs es un operando 2D.</span><span class="sxs-lookup"><span data-stu-id="3829b-217">In non-declaration instructions, a resource operand for samplers, SRVs, and UAVs is a 2D operand.</span></span> <span data-ttu-id="3829b-218">El primer índice es una constante literal que especifica el identificador del intervalo.</span><span class="sxs-lookup"><span data-stu-id="3829b-218">The first index is a literal constant that specifies the range ID.</span></span> <span data-ttu-id="3829b-219">El segundo índice representa el valor de linealización del índice.</span><span class="sxs-lookup"><span data-stu-id="3829b-219">The second index represents the linearized value of the index.</span></span> <span data-ttu-id="3829b-220">El valor se calcula en relación con el principio del espacio de registro correspondiente (no con respecto al principio del intervalo lógico) para correlacionar mejor con la firma raíz y reducir la carga del compilador de controladores para ajustar el índice.</span><span class="sxs-lookup"><span data-stu-id="3829b-220">The value is computed relative to the beginning of the corresponding register space (not relative to the beginning of the logical range) to better correlate with the root signature and to reduce the driver compiler burden of adjusting the index.</span></span>

<span data-ttu-id="3829b-221">Un operando de recurso para CBVs es un operando 3D, que contiene: el identificador de literal del intervalo, el índice del búfer de constantes, el desplazamiento en la instancia concreta de búfer de constantes.</span><span class="sxs-lookup"><span data-stu-id="3829b-221">A resource operand for CBVs is a 3D operand, containing: literal ID of the range, index of the constant buffer, offset into the particular instance of constant buffer.</span></span>

## <a name="example-hlsl-declarations"></a><span data-ttu-id="3829b-222">Declaraciones de ejemplo de HLSL</span><span class="sxs-lookup"><span data-stu-id="3829b-222">Example HLSL Declarations</span></span>

<span data-ttu-id="3829b-223">No es necesario que los programas HLSL sepan nada sobre las firmas raíz.</span><span class="sxs-lookup"><span data-stu-id="3829b-223">HLSL programs do not need to know anything about root signatures.</span></span> <span data-ttu-id="3829b-224">Pueden asignar enlaces al espacio de enlace virtual "Register", t \# para SRVs, u \# para UAVs, b \# para CBVs, s \# para muestras o confiar en el compilador para seleccionar asignaciones (y consultar las asignaciones resultantes mediante la reflexión del sombreador posteriormente).</span><span class="sxs-lookup"><span data-stu-id="3829b-224">They can assign bindings to the virtual “register” binding space, t\# for SRVs, u\# for UAVs, b\# for CBVs, s\# for samplers, or rely on the compiler to pick assignments (and query the resulting mappings using shader reflection afterwards).</span></span> <span data-ttu-id="3829b-225">La firma raíz asigna las tablas de descriptores, los descriptores raíz y las constantes raíz a este espacio de registro virtual.</span><span class="sxs-lookup"><span data-stu-id="3829b-225">The root signature maps descriptor tables, root descriptors, and root constants to this virtual register space.</span></span>

<span data-ttu-id="3829b-226">A continuación se muestran algunas declaraciones de ejemplo que puede tener un sombreador HLSL.</span><span class="sxs-lookup"><span data-stu-id="3829b-226">The following are some example declarations an HLSL shader might have.</span></span> <span data-ttu-id="3829b-227">Tenga en cuenta que no hay ninguna referencia a las tablas de descriptores o firmas de raíz.</span><span class="sxs-lookup"><span data-stu-id="3829b-227">Note that there are no references to root signatures or descriptor tables.</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="3829b-228">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3829b-228">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3829b-229">Indexado dinámico mediante HLSL 5.1</span><span class="sxs-lookup"><span data-stu-id="3829b-229">Dynamic Indexing using HLSL 5.1</span></span>](dynamic-indexing-using-hlsl-5-1.md)
</dt> <dt>

[<span data-ttu-id="3829b-230">Efecto: herramienta de compilador</span><span class="sxs-lookup"><span data-stu-id="3829b-230">Effect-Compiler Tool</span></span>](/windows/desktop/direct3dtools/fxc)
</dt> <dt>

[<span data-ttu-id="3829b-231">Características del modelo de sombreador de HLSL 5,1 para Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="3829b-231">HLSL Shader Model 5.1 Features for Direct3D 12</span></span>](/windows/desktop/direct3dhlsl/hlsl-shader-model-5-1-features-for-direct3d-12)
</dt> <dt>

[<span data-ttu-id="3829b-232">Vistas ordenadas de rasterizador</span><span class="sxs-lookup"><span data-stu-id="3829b-232">Rasterizer Ordered Views</span></span>](rasterizer-order-views.md)
</dt> <dt>

[<span data-ttu-id="3829b-233">Enlace de recursos</span><span class="sxs-lookup"><span data-stu-id="3829b-233">Resource Binding</span></span>](resource-binding.md)
</dt> <dt>

[<span data-ttu-id="3829b-234">Firmas raíz</span><span class="sxs-lookup"><span data-stu-id="3829b-234">Root Signatures</span></span>](root-signatures.md)
</dt> <dt>

[<span data-ttu-id="3829b-235">Modelo de sombreador 5,1</span><span class="sxs-lookup"><span data-stu-id="3829b-235">Shader Model 5.1</span></span>](/windows/desktop/direct3dhlsl/shader-model-5-1)
</dt> <dt>

[<span data-ttu-id="3829b-236">Valor de referencia de estarcido del sombreador especificado</span><span class="sxs-lookup"><span data-stu-id="3829b-236">Shader Specified Stencil Reference Value</span></span>](shader-specified-stencil-reference-value.md)
</dt> <dt>

[<span data-ttu-id="3829b-237">Especificación de firmas de raíz en HLSL</span><span class="sxs-lookup"><span data-stu-id="3829b-237">Specifying Root Signatures in HLSL</span></span>](specifying-root-signatures-in-hlsl.md)
</dt> </dl>

 

 