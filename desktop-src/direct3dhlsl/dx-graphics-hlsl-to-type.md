---
title: Objeto Texture
description: En Direct3D 10, los ejemplos y las texturas se especifican de forma independiente. el muestreo de textura se implementa mediante el uso de un objeto de textura con plantilla. Este objeto de textura con plantilla tiene un formato específico, devuelve un tipo específico e implementa varios métodos.
ms.assetid: e8cb483a-d831-4942-b6fe-61dd5edb1813
keywords:
- HLSL de objeto de textura
topic_type:
- apiref
api_name:
- Texture Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b075ddc1f659923efd03d9fe9d21ee3238e656e9
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/10/2021
ms.locfileid: "104280217"
---
# <a name="texture-object"></a><span data-ttu-id="60764-105">Objeto Texture</span><span class="sxs-lookup"><span data-stu-id="60764-105">Texture Object</span></span>

<span data-ttu-id="60764-106">En Direct3D 10, los ejemplos y las texturas se especifican de forma independiente. el muestreo de textura se implementa mediante el uso de un objeto de textura con plantilla.</span><span class="sxs-lookup"><span data-stu-id="60764-106">In Direct3D 10, you specify the samplers and textures independently; texture sampling is implemented by using a templated-texture object.</span></span> <span data-ttu-id="60764-107">Este objeto de textura con plantilla tiene un formato específico, devuelve un tipo específico e implementa varios métodos.</span><span class="sxs-lookup"><span data-stu-id="60764-107">This templated-texture object has a specific format, returns a specific type, and implements several methods.</span></span>




|                                                                                                                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="60764-108">Diferencias entre Direct3D9 y Direct3D10: en Direct3D 9, los muestreadores se enlazan a texturas específicas; en Direct3D 10, las texturas y los muestreadores son objetos independientes.</span><span class="sxs-lookup"><span data-stu-id="60764-108">Differences between Direct3D9 and Direct3D10: In Direct3D 9, samplers are bound to specific textures; in Direct3D 10, textures and samplers are independent objects.</span></span> <span data-ttu-id="60764-109">Cada objeto de textura con plantilla implementa métodos de muestreo de textura que toman la textura y la muestra como parámetros de entrada.</span><span class="sxs-lookup"><span data-stu-id="60764-109">Each templated-texture object implements texture sampling methods that take both the texture and the sampler as input parameters.</span></span><br/> |



 

<span data-ttu-id="60764-110">Esta es la sintaxis para crear todos los objetos de textura (excepto los objetos multimuestreados).</span><span class="sxs-lookup"><span data-stu-id="60764-110">Here is the syntax for creating all texture objects (except multisampled objects).</span></span>



| <span data-ttu-id="60764-111">Nombre del \[ < *tipo* de Object1 > \] ;</span><span class="sxs-lookup"><span data-stu-id="60764-111">Object1 \[<*Type*>\] *Name*;</span></span> |
|------------------------------------|



 

<span data-ttu-id="60764-112">Los objetos multimuestreados (Texture2DMS y Texture2DMSArray) requieren que el tamaño de la textura se indique explícitamente y se exprese como el número de muestras.</span><span class="sxs-lookup"><span data-stu-id="60764-112">Multisampled objects (Texture2DMS and Texture2DMSArray) require the texture size to be explicitly stated and expressed as the number of samples.</span></span>



| <span data-ttu-id="60764-113">Objeto2 \[ < *Type, samples* > \] *Name*;</span><span class="sxs-lookup"><span data-stu-id="60764-113">Object2 \[<*Type, Samples*>\] *Name*;</span></span> |
|---------------------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="60764-114">Parámetros</span><span class="sxs-lookup"><span data-stu-id="60764-114">Parameters</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="60764-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="60764-115">Item</span></span></th>
<th><span data-ttu-id="60764-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="60764-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="60764-117"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Objeto</em></span><span class="sxs-lookup"><span data-stu-id="60764-117"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Object</em></span></span><br/></td>
<td><span data-ttu-id="60764-118">Objeto de textura.</span><span class="sxs-lookup"><span data-stu-id="60764-118">A texture object.</span></span> <span data-ttu-id="60764-119">Debe ser uno de los tipos siguientes.</span><span class="sxs-lookup"><span data-stu-id="60764-119">Must be one of the following types.</span></span> <br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="60764-120">Tipo de Object1</span><span class="sxs-lookup"><span data-stu-id="60764-120">Object1 Type</span></span></th>
<th><span data-ttu-id="60764-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="60764-121">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="60764-122">Buffer</span><span class="sxs-lookup"><span data-stu-id="60764-122">Buffer</span></span></td>
<td><span data-ttu-id="60764-123">Buffer</span><span class="sxs-lookup"><span data-stu-id="60764-123">Buffer</span></span> </td>
</tr>
<tr class="even">
<td><span data-ttu-id="60764-124">Texture1D</span><span class="sxs-lookup"><span data-stu-id="60764-124">Texture1D</span></span></td>
<td><span data-ttu-id="60764-125">textura 1D</span><span class="sxs-lookup"><span data-stu-id="60764-125">1D texture</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="60764-126">Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="60764-126">Texture1DArray</span></span></td>
<td><span data-ttu-id="60764-127">Matriz de texturas 1D</span><span class="sxs-lookup"><span data-stu-id="60764-127">Array of 1D textures</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="60764-128">Texture2D</span><span class="sxs-lookup"><span data-stu-id="60764-128">Texture2D</span></span></td>
<td><span data-ttu-id="60764-129">textura 2D</span><span class="sxs-lookup"><span data-stu-id="60764-129">2D texture</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="60764-130">Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="60764-130">Texture2DArray</span></span></td>
<td><span data-ttu-id="60764-131">Matriz de texturas 2D</span><span class="sxs-lookup"><span data-stu-id="60764-131">Array of 2D textures</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="60764-132">Texture3D</span><span class="sxs-lookup"><span data-stu-id="60764-132">Texture3D</span></span></td>
<td><span data-ttu-id="60764-133">textura 3D</span><span class="sxs-lookup"><span data-stu-id="60764-133">3D texture</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="60764-134">TextureCube</span><span class="sxs-lookup"><span data-stu-id="60764-134">TextureCube</span></span></td>
<td><span data-ttu-id="60764-135">Textura del cubo</span><span class="sxs-lookup"><span data-stu-id="60764-135">Cube texture</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="60764-136">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="60764-136">TextureCubeArray</span></span>  </td>
<td><span data-ttu-id="60764-137">Matriz de texturas de cubo</span><span class="sxs-lookup"><span data-stu-id="60764-137">Array of cube textures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="60764-138">Tipo objeto2</span><span class="sxs-lookup"><span data-stu-id="60764-138">Object2 Type</span></span></td>
<td><span data-ttu-id="60764-139">Descripción</span><span class="sxs-lookup"><span data-stu-id="60764-139">Description</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="60764-140">Texture2DMS</span><span class="sxs-lookup"><span data-stu-id="60764-140">Texture2DMS</span></span></td>
<td><span data-ttu-id="60764-141">textura multimuestreada 2D</span><span class="sxs-lookup"><span data-stu-id="60764-141">2D multisampled texture</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="60764-142">Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="60764-142">Texture2DMSArray</span></span></td>
<td><span data-ttu-id="60764-143">Matriz de texturas multimuestreadas en 2D</span><span class="sxs-lookup"><span data-stu-id="60764-143">Array of 2D multisampled textures</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<ol>
<li><span data-ttu-id="60764-144">El tipo de búfer admite la mayoría de los métodos de objeto Texture excepto Getdimensions (.</span><span class="sxs-lookup"><span data-stu-id="60764-144">The Buffer type supports most texture object methods except GetDimensions.</span></span></li>
<li><span data-ttu-id="60764-145">TextureCubeArray está disponible en el modelo de sombreador 4,1 o superior.</span><span class="sxs-lookup"><span data-stu-id="60764-145">TextureCubeArray is available in shader model 4.1 or higher.</span></span></li>
<li><span data-ttu-id="60764-146">El modelo de sombreador 4,1 está disponible en Direct3D 10,1 o superior.</span><span class="sxs-lookup"><span data-stu-id="60764-146">Shader model 4.1 is available in Direct3D 10.1 or higher.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="60764-147"><span id="Type"></span><span id="type"></span><span id="TYPE"></span><em>Automáticamente</em></span><span class="sxs-lookup"><span data-stu-id="60764-147"><span id="Type"></span><span id="type"></span><span id="TYPE"></span><em>Type</em></span></span></p></td>
<td><p><span data-ttu-id="60764-148">Opcional.</span><span class="sxs-lookup"><span data-stu-id="60764-148">Optional.</span></span> <span data-ttu-id="60764-149">Cualquier tipo HLSL <a href="dx-graphics-hlsl-scalar.md">escalar</a> o <a href="dx-graphics-hlsl-vector.md"><strong>tipo HLSL vectorial</strong></a>, rodeado de corchetes angulares.</span><span class="sxs-lookup"><span data-stu-id="60764-149">Any <a href="dx-graphics-hlsl-scalar.md">scalar HLSL type</a> or <a href="dx-graphics-hlsl-vector.md"><strong>vector HLSL type</strong></a>, surrounded by angle brackets.</span></span> <span data-ttu-id="60764-150">El tipo predeterminado es <strong>FLOAT4</strong>.</span><span class="sxs-lookup"><span data-stu-id="60764-150">The default type is <strong>float4</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="60764-151"><span id="Name"></span><span id="name"></span><span id="NAME"></span><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="60764-151"><span id="Name"></span><span id="name"></span><span id="NAME"></span><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="60764-152">Cadena ASCII que especifica el nombre del objeto de textura.</span><span class="sxs-lookup"><span data-stu-id="60764-152">An ASCII string that specifies the texture object name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="60764-153"><span id="Samples"></span><span id="samples"></span><span id="SAMPLES"></span><em>Assembl</em></span><span class="sxs-lookup"><span data-stu-id="60764-153"><span id="Samples"></span><span id="samples"></span><span id="SAMPLES"></span><em>Samples</em></span></span></p></td>
<td><p><span data-ttu-id="60764-154">El número de muestras (oscila entre 1 y 128).</span><span class="sxs-lookup"><span data-stu-id="60764-154">The number of samples (ranges between 1 and 128).</span></span></p></td>
</tr>
</tbody>
</table>



 

## <a name="example-1"></a><span data-ttu-id="60764-155">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="60764-155">Example 1</span></span>

<span data-ttu-id="60764-156">Este es un ejemplo de cómo declarar un objeto Texture.</span><span class="sxs-lookup"><span data-stu-id="60764-156">Here is an example of declaring a texture object.</span></span>


```
Texture2D <float4> MyTex;

Texture2DMS <float4, 128> MyMSTex;
```



## <a name="texture-object-methods"></a><span data-ttu-id="60764-157">Métodos de objeto Texture</span><span class="sxs-lookup"><span data-stu-id="60764-157">Texture Object Methods</span></span>

<span data-ttu-id="60764-158">Cada objeto Texture implementa determinados métodos; Esta es la tabla en la que se enumeran todos los métodos.</span><span class="sxs-lookup"><span data-stu-id="60764-158">Each texture object implements certain methods; here's the table that lists all of the methods.</span></span> <span data-ttu-id="60764-159">Vea la página de referencia de cada método para ver qué objetos pueden usar ese método.</span><span class="sxs-lookup"><span data-stu-id="60764-159">See the reference page for each method to see what objects can use that method.</span></span>



| <span data-ttu-id="60764-160">Texture (método)</span><span class="sxs-lookup"><span data-stu-id="60764-160">Texture Method</span></span>                                                                     | <span data-ttu-id="60764-161">Descripción</span><span class="sxs-lookup"><span data-stu-id="60764-161">Description</span></span>                                                                                                       | <span data-ttu-id="60764-162">vs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="60764-162">vs\_4\_0</span></span> | <span data-ttu-id="60764-163">vs \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="60764-163">vs\_4\_1</span></span>  | <span data-ttu-id="60764-164">PS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="60764-164">ps\_4\_0</span></span> | <span data-ttu-id="60764-165">PS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="60764-165">ps\_4\_1</span></span>  | <span data-ttu-id="60764-166">GS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="60764-166">gs\_4\_0</span></span> | <span data-ttu-id="60764-167">GS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="60764-167">gs\_4\_1</span></span>  |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|----------|-----------|----------|-----------|----------|-----------|
| [<span data-ttu-id="60764-168">CalculateLevelOfDetail</span><span class="sxs-lookup"><span data-stu-id="60764-168">CalculateLevelOfDetail</span></span>](dx-graphics-hlsl-to-calculate-lod.md)                    | <span data-ttu-id="60764-169">Calcule el LOD y devuelva un resultado de compresión.</span><span class="sxs-lookup"><span data-stu-id="60764-169">Calculate the LOD, return a clamped result.</span></span>                                                                       |          |           |          | <span data-ttu-id="60764-170">x</span><span class="sxs-lookup"><span data-stu-id="60764-170">x</span></span>         |          |           |
| [<span data-ttu-id="60764-171">CalculateLevelOfDetailUnclamped</span><span class="sxs-lookup"><span data-stu-id="60764-171">CalculateLevelOfDetailUnclamped</span></span>](dx-graphics-hlsl-to-calculate-lod-unclamped.md) | <span data-ttu-id="60764-172">Calcule el LOD y devuelva un resultado desgarrado.</span><span class="sxs-lookup"><span data-stu-id="60764-172">Calculate the LOD, return an unclamped result.</span></span>                                                                    |          |           |          | <span data-ttu-id="60764-173">x</span><span class="sxs-lookup"><span data-stu-id="60764-173">x</span></span>         |          |           |
| [<span data-ttu-id="60764-174">Recopilar</span><span class="sxs-lookup"><span data-stu-id="60764-174">Gather</span></span>](dx-graphics-hlsl-to-gather.md)                                           | <span data-ttu-id="60764-175">Obtiene los cuatro ejemplos (solo componente rojo) que se utilizarían para la interpolación bilineal al realizar el muestreo de una textura.</span><span class="sxs-lookup"><span data-stu-id="60764-175">Gets the four samples (red component only) that would be used for bilinear interpolation when sampling a texture.</span></span> |          | <span data-ttu-id="60764-176">x</span><span class="sxs-lookup"><span data-stu-id="60764-176">x</span></span>         |          | <span data-ttu-id="60764-177">x</span><span class="sxs-lookup"><span data-stu-id="60764-177">x</span></span>         |          | <span data-ttu-id="60764-178">x</span><span class="sxs-lookup"><span data-stu-id="60764-178">x</span></span>         |
| [<span data-ttu-id="60764-179">GetDimensions</span><span class="sxs-lookup"><span data-stu-id="60764-179">GetDimensions</span></span>](dx-graphics-hlsl-to-getdimensions.md)                             | <span data-ttu-id="60764-180">Obtiene la dimensión de textura para un nivel de mipmap especificado.</span><span class="sxs-lookup"><span data-stu-id="60764-180">Get the texture dimension for a specified mipmap level.</span></span>                                                           | <span data-ttu-id="60764-181">x</span><span class="sxs-lookup"><span data-stu-id="60764-181">x</span></span>        | <span data-ttu-id="60764-182">x</span><span class="sxs-lookup"><span data-stu-id="60764-182">x</span></span>         | <span data-ttu-id="60764-183">x</span><span class="sxs-lookup"><span data-stu-id="60764-183">x</span></span>        | <span data-ttu-id="60764-184">x</span><span class="sxs-lookup"><span data-stu-id="60764-184">x</span></span>         | <span data-ttu-id="60764-185">x</span><span class="sxs-lookup"><span data-stu-id="60764-185">x</span></span>        | <span data-ttu-id="60764-186">x</span><span class="sxs-lookup"><span data-stu-id="60764-186">x</span></span>         |
| [<span data-ttu-id="60764-187">Getdimensions ((Multimuestra)</span><span class="sxs-lookup"><span data-stu-id="60764-187">GetDimensions (MultiSample)</span></span>](dx-graphics-hlsl-to-getdimensions.md)               | <span data-ttu-id="60764-188">Obtiene la dimensión de textura para un nivel de mipmap especificado.</span><span class="sxs-lookup"><span data-stu-id="60764-188">Get the texture dimension for a specified mipmap level.</span></span>                                                           |          | <span data-ttu-id="60764-189">x</span><span class="sxs-lookup"><span data-stu-id="60764-189">x</span></span>         |          | <span data-ttu-id="60764-190">x</span><span class="sxs-lookup"><span data-stu-id="60764-190">x</span></span>         |          | <span data-ttu-id="60764-191">x</span><span class="sxs-lookup"><span data-stu-id="60764-191">x</span></span>         |
| [<span data-ttu-id="60764-192">GetSamplePosition</span><span class="sxs-lookup"><span data-stu-id="60764-192">GetSamplePosition</span></span>](dx-graphics-hlsl-to-get-sample-position.md)                   | <span data-ttu-id="60764-193">Obtiene la posición del ejemplo especificado.</span><span class="sxs-lookup"><span data-stu-id="60764-193">Get the position of the specified sample.</span></span>                                                                         |          | <span data-ttu-id="60764-194">x</span><span class="sxs-lookup"><span data-stu-id="60764-194">x</span></span>         |          | <span data-ttu-id="60764-195">x</span><span class="sxs-lookup"><span data-stu-id="60764-195">x</span></span>         |          | <span data-ttu-id="60764-196">x</span><span class="sxs-lookup"><span data-stu-id="60764-196">x</span></span>         |
| [<span data-ttu-id="60764-197">Cargar</span><span class="sxs-lookup"><span data-stu-id="60764-197">Load</span></span>](dx-graphics-hlsl-to-load.md)                                               | <span data-ttu-id="60764-198">Cargar datos sin ningún filtrado o muestreo.</span><span class="sxs-lookup"><span data-stu-id="60764-198">Load data without any filtering or sampling.</span></span>                                                                      | <span data-ttu-id="60764-199">x</span><span class="sxs-lookup"><span data-stu-id="60764-199">x</span></span>        | <span data-ttu-id="60764-200">x</span><span class="sxs-lookup"><span data-stu-id="60764-200">x</span></span>         | <span data-ttu-id="60764-201">x</span><span class="sxs-lookup"><span data-stu-id="60764-201">x</span></span>        | <span data-ttu-id="60764-202">x</span><span class="sxs-lookup"><span data-stu-id="60764-202">x</span></span>         | <span data-ttu-id="60764-203">x</span><span class="sxs-lookup"><span data-stu-id="60764-203">x</span></span>        | <span data-ttu-id="60764-204">x</span><span class="sxs-lookup"><span data-stu-id="60764-204">x</span></span>         |
| [<span data-ttu-id="60764-205">Load (Multimuestra)</span><span class="sxs-lookup"><span data-stu-id="60764-205">Load (Multisample)</span></span>](dx-graphics-hlsl-to-load.md)                                 | <span data-ttu-id="60764-206">Cargar datos sin ningún filtrado o muestreo.</span><span class="sxs-lookup"><span data-stu-id="60764-206">Load data without any filtering or sampling.</span></span>                                                                      |          | <span data-ttu-id="60764-207">x</span><span class="sxs-lookup"><span data-stu-id="60764-207">x</span></span>         | <span data-ttu-id="60764-208">x</span><span class="sxs-lookup"><span data-stu-id="60764-208">x</span></span>        | <span data-ttu-id="60764-209">x</span><span class="sxs-lookup"><span data-stu-id="60764-209">x</span></span>         |          | <span data-ttu-id="60764-210">x</span><span class="sxs-lookup"><span data-stu-id="60764-210">x</span></span>         |
| [<span data-ttu-id="60764-211">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="60764-211">Sample</span></span>](dx-graphics-hlsl-to-sample.md)                                           | <span data-ttu-id="60764-212">Muestra una textura.</span><span class="sxs-lookup"><span data-stu-id="60764-212">Sample a texture.</span></span>                                                                                                 |          |           | <span data-ttu-id="60764-213">x</span><span class="sxs-lookup"><span data-stu-id="60764-213">x</span></span>        | <span data-ttu-id="60764-214">x</span><span class="sxs-lookup"><span data-stu-id="60764-214">x</span></span>         |          |           |
| [<span data-ttu-id="60764-215">SampleBias</span><span class="sxs-lookup"><span data-stu-id="60764-215">SampleBias</span></span>](dx-graphics-hlsl-to-samplebias.md)                                   | <span data-ttu-id="60764-216">Muestra una textura, después de aplicar el valor de diferencia al nivel de mipmap.</span><span class="sxs-lookup"><span data-stu-id="60764-216">Sample a texture, after applying the bias value to the mipmap level.</span></span>                                              |          |           | <span data-ttu-id="60764-217">x</span><span class="sxs-lookup"><span data-stu-id="60764-217">x</span></span>        | <span data-ttu-id="60764-218">x</span><span class="sxs-lookup"><span data-stu-id="60764-218">x</span></span>         |          |           |
| [<span data-ttu-id="60764-219">SampleCmp</span><span class="sxs-lookup"><span data-stu-id="60764-219">SampleCmp</span></span>](dx-graphics-hlsl-to-samplecmp.md)                                     | <span data-ttu-id="60764-220">Muestre una textura con un valor de comparación para rechazar ejemplos.</span><span class="sxs-lookup"><span data-stu-id="60764-220">Sample a texture, using a comparison value to reject samples.</span></span>                                                     |          |           | <span data-ttu-id="60764-221">x</span><span class="sxs-lookup"><span data-stu-id="60764-221">x</span></span>        | <span data-ttu-id="60764-222">x</span><span class="sxs-lookup"><span data-stu-id="60764-222">x</span></span>         |          |           |
| [<span data-ttu-id="60764-223">SampleCmpLevelZero</span><span class="sxs-lookup"><span data-stu-id="60764-223">SampleCmpLevelZero</span></span>](dx-graphics-hlsl-to-samplecmplevelzero.md)                   | <span data-ttu-id="60764-224">Muestra una textura (solo el nivel de mipmap 0), utilizando un valor de comparación para rechazar muestras.</span><span class="sxs-lookup"><span data-stu-id="60764-224">Sample a texture (mipmap level 0 only), using a comparison value to reject samples.</span></span>                               | <span data-ttu-id="60764-225">x</span><span class="sxs-lookup"><span data-stu-id="60764-225">x</span></span>        | <span data-ttu-id="60764-226">x</span><span class="sxs-lookup"><span data-stu-id="60764-226">x</span></span>         | <span data-ttu-id="60764-227">x</span><span class="sxs-lookup"><span data-stu-id="60764-227">x</span></span>        | <span data-ttu-id="60764-228">x</span><span class="sxs-lookup"><span data-stu-id="60764-228">x</span></span>         | <span data-ttu-id="60764-229">x</span><span class="sxs-lookup"><span data-stu-id="60764-229">x</span></span>        | <span data-ttu-id="60764-230">x</span><span class="sxs-lookup"><span data-stu-id="60764-230">x</span></span>         |
| [<span data-ttu-id="60764-231">SampleGrad</span><span class="sxs-lookup"><span data-stu-id="60764-231">SampleGrad</span></span>](dx-graphics-hlsl-to-samplegrad.md)                                   | <span data-ttu-id="60764-232">Muestra una textura con un degradado para influir en la forma en que se calcula la ubicación de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="60764-232">Sample a texture using a gradient to influence the way the sample location is calculated.</span></span>                         | <span data-ttu-id="60764-233">x</span><span class="sxs-lookup"><span data-stu-id="60764-233">x</span></span>        | <span data-ttu-id="60764-234">x</span><span class="sxs-lookup"><span data-stu-id="60764-234">x</span></span>         | <span data-ttu-id="60764-235">x</span><span class="sxs-lookup"><span data-stu-id="60764-235">x</span></span>        | <span data-ttu-id="60764-236">x</span><span class="sxs-lookup"><span data-stu-id="60764-236">x</span></span>         | <span data-ttu-id="60764-237">x</span><span class="sxs-lookup"><span data-stu-id="60764-237">x</span></span>        | <span data-ttu-id="60764-238">x</span><span class="sxs-lookup"><span data-stu-id="60764-238">x</span></span>         |
| [<span data-ttu-id="60764-239">SampleLevel</span><span class="sxs-lookup"><span data-stu-id="60764-239">SampleLevel</span></span>](dx-graphics-hlsl-to-samplelevel.md)                                 | <span data-ttu-id="60764-240">Muestra una textura en el nivel de mipmap especificado.</span><span class="sxs-lookup"><span data-stu-id="60764-240">Sample a texture on the specified mipmap level.</span></span>                                                                   | <span data-ttu-id="60764-241">x</span><span class="sxs-lookup"><span data-stu-id="60764-241">x</span></span>        | <span data-ttu-id="60764-242">x</span><span class="sxs-lookup"><span data-stu-id="60764-242">x</span></span>         | <span data-ttu-id="60764-243">x</span><span class="sxs-lookup"><span data-stu-id="60764-243">x</span></span>        | <span data-ttu-id="60764-244">x</span><span class="sxs-lookup"><span data-stu-id="60764-244">x</span></span>         | <span data-ttu-id="60764-245">x</span><span class="sxs-lookup"><span data-stu-id="60764-245">x</span></span>        | <span data-ttu-id="60764-246">x</span><span class="sxs-lookup"><span data-stu-id="60764-246">x</span></span>         |



 

### <a name="return-type"></a><span data-ttu-id="60764-247">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="60764-247">Return Type</span></span>

<span data-ttu-id="60764-248">El tipo de valor devuelto de un método de objeto Texture es FLOAT4, a menos que se especifique lo contrario, con la excepción de los objetos de textura con suavizado de contorno múltiple que siempre necesitan el tipo y el recuento de muestras especificado.</span><span class="sxs-lookup"><span data-stu-id="60764-248">The return type of a texture object method is float4 unless specified otherwise, with the exception of the multisampled anti-aliased texture objects that always need the type and sample count specified.</span></span> <span data-ttu-id="60764-249">El tipo de valor devuelto es el mismo que el tipo de recurso de textura ([**\_ formato de DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)).</span><span class="sxs-lookup"><span data-stu-id="60764-249">The return type is the same as the texture resource type ([**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)).</span></span> <span data-ttu-id="60764-250">En otras palabras, puede ser cualquiera de los siguientes tipos.</span><span class="sxs-lookup"><span data-stu-id="60764-250">In other words, it can be any of the following types.</span></span>



| <span data-ttu-id="60764-251">Tipo</span><span class="sxs-lookup"><span data-stu-id="60764-251">Type</span></span>                       | <span data-ttu-id="60764-252">Description</span><span class="sxs-lookup"><span data-stu-id="60764-252">Description</span></span>                                                                                                                                                             |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="60764-253">FLOAT</span><span class="sxs-lookup"><span data-stu-id="60764-253">float</span></span>                      | <span data-ttu-id="60764-254">32 bits Float (vea [reglas de punto flotante](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-float-rules) para conocer las diferencias de IEEE float)</span><span class="sxs-lookup"><span data-stu-id="60764-254">32-bit float (see [Floating-Point Rules](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-float-rules) for differences from IEEE float)</span></span>                            |
| <span data-ttu-id="60764-255">int</span><span class="sxs-lookup"><span data-stu-id="60764-255">int</span></span>                        | <span data-ttu-id="60764-256">Entero de 32 bits con signo</span><span class="sxs-lookup"><span data-stu-id="60764-256">32-bit signed integer</span></span>                                                                                                                                                   |
| <span data-ttu-id="60764-257">unsigned int</span><span class="sxs-lookup"><span data-stu-id="60764-257">unsigned int</span></span>               | <span data-ttu-id="60764-258">Entero de 32 bits sin signo</span><span class="sxs-lookup"><span data-stu-id="60764-258">32-bit unsigned integer</span></span>                                                                                                                                                 |
| <span data-ttu-id="60764-259">snorm</span><span class="sxs-lookup"><span data-stu-id="60764-259">snorm</span></span>                      | <span data-ttu-id="60764-260">32 bits Float en el intervalo comprendido entre 1 y 1, ambos inclusive (vea [reglas de punto flotante](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-float-rules) para conocer las diferencias de IEEE float)</span><span class="sxs-lookup"><span data-stu-id="60764-260">32-bit float in range -1 to 1 inclusive (see [Floating-Point Rules](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-float-rules) for differences from IEEE float)</span></span> |
| <span data-ttu-id="60764-261">unorm</span><span class="sxs-lookup"><span data-stu-id="60764-261">unorm</span></span>                      | <span data-ttu-id="60764-262">32 bits Float en el intervalo de 0 a 1, ambos inclusive (vea [reglas de punto flotante](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-float-rules) para conocer las diferencias de IEEE float)</span><span class="sxs-lookup"><span data-stu-id="60764-262">32-bit float in range 0 to 1 inclusive (see [Floating-Point Rules](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-float-rules) for differences from IEEE float)</span></span>  |
| <span data-ttu-id="60764-263">cualquier tipo de textura o struct</span><span class="sxs-lookup"><span data-stu-id="60764-263">any texture type or struct</span></span> | <span data-ttu-id="60764-264">El número de componentes devueltos debe estar entre 1 y 3, ambos inclusive.</span><span class="sxs-lookup"><span data-stu-id="60764-264">The number of components returned must be between 1 and 3 inclusive.</span></span>                                                                                                    |



 

<span data-ttu-id="60764-265">Además, el tipo de valor devuelto puede ser cualquier tipo de textura, incluida una estructura, pero debe ser inferior a 4 componentes, como un tipo float1, que devuelve un componente.</span><span class="sxs-lookup"><span data-stu-id="60764-265">In addition, the return type can be any texture type including a structure but, it must be less than 4 components such as a float1 type which returns one component.</span></span>

## <a name="default-values-for-missing-components-in-a-texture"></a><span data-ttu-id="60764-266">Valores predeterminados para los componentes que faltan en una textura</span><span class="sxs-lookup"><span data-stu-id="60764-266">Default Values for Missing Components in a Texture</span></span>

<span data-ttu-id="60764-267">El valor predeterminado para los componentes que faltan en un tipo de recurso de textura es cero para cualquier componente excepto el componente alfa (A); el valor predeterminado para el que falta un es uno.</span><span class="sxs-lookup"><span data-stu-id="60764-267">The default value for missing components in a texture resource type is zero for any component except the alpha component (A); the default value for the missing A is one.</span></span> <span data-ttu-id="60764-268">La forma en que este aparece en el sombreador depende del tipo de recurso de textura.</span><span class="sxs-lookup"><span data-stu-id="60764-268">The way that this one appears to the shader depends on the texture resource type.</span></span> <span data-ttu-id="60764-269">Adopta la forma del primer componente con tipo que está realmente presente en el tipo de recurso de textura (a partir de la izquierda en el orden RGBA).</span><span class="sxs-lookup"><span data-stu-id="60764-269">It takes the form of the first typed component that is actually present in the texture resource type (starting from the left in RGBA order).</span></span> <span data-ttu-id="60764-270">Si este formulario es UNORM o FLOAT, el valor predeterminado para el que falta es 1,0 f.</span><span class="sxs-lookup"><span data-stu-id="60764-270">If this form is UNORM or FLOAT, the default value for the missing A is 1.0f.</span></span> <span data-ttu-id="60764-271">Si el formulario es SINT o UINT, el valor predeterminado para el que falta es 0x1.</span><span class="sxs-lookup"><span data-stu-id="60764-271">If the form is SINT or UINT, the default value for the missing A is 0x1.</span></span>

<span data-ttu-id="60764-272">Por ejemplo, cuando un sombreador lee el tipo de recurso de textura [**\_ \_ \_ \_ \_ sin tipo de formato DXGI R24 UNORM X8**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) , los valores predeterminados para G y B son cero y el valor predeterminado para es 1,0 f; cuando un sombreador lee el tipo de recurso [**\_ \_ R16G16 \_ uint de formato DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) , el valor predeterminado de B es cero y el valor predeterminado de un es 0x00000001; cuando un sombreador lee el tipo de recurso de textura [**\_ formato DXGI \_ R16 \_ San**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) , los valores predeterminados para G y B son cero y el valor predeterminado para es 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="60764-272">For example, when a shader reads the [**DXGI\_FORMAT\_R24\_UNORM\_X8\_TYPELESS**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) texture resource type, the default values for G and B are zero and the default value for A is 1.0f; when a shader reads the [**DXGI\_FORMAT\_R16G16\_UINT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) texture resource type, the default value for B is zero and the default value for A is 0x00000001; when a shader reads the [**DXGI\_FORMAT\_R16\_SINT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) texture resource type, the default values for G and B are zero and the default value for A is 0x00000001.</span></span>

## <a name="example-2"></a><span data-ttu-id="60764-273">Ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="60764-273">Example 2</span></span>

<span data-ttu-id="60764-274">Este es un ejemplo de muestreo de textura mediante un método de textura.</span><span class="sxs-lookup"><span data-stu-id="60764-274">Here is an example of texture sampling using a texture method.</span></span>


```
sampler MySamp;
Texture2D <float4> MyTex;
 
float4 main( float2 TexCoords[2] : TEXCOORD ) : SV_Target
{
    return MyTex.Sample( MySamp, TexCoords[0] ));
}
```



## <a name="minimum-shader-model"></a><span data-ttu-id="60764-275">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="60764-275">Minimum Shader Model</span></span>

<span data-ttu-id="60764-276">Este objeto es compatible con los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="60764-276">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="60764-277">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="60764-277">Shader Model</span></span>                                                        | <span data-ttu-id="60764-278">Compatible</span><span class="sxs-lookup"><span data-stu-id="60764-278">Supported</span></span> |
|---------------------------------------------------------------------|-----------|
| <span data-ttu-id="60764-279">Modelos de sombreador [modelo 4](dx-graphics-hlsl-sm4.md) y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="60764-279">[Shader Model 4](dx-graphics-hlsl-sm4.md) and higher shader models</span></span> | <span data-ttu-id="60764-280">sí</span><span class="sxs-lookup"><span data-stu-id="60764-280">yes</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="60764-281">Vea también</span><span class="sxs-lookup"><span data-stu-id="60764-281">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60764-282">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="60764-282">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

