---
title: Objeto Texture
description: En Direct3D 10, se especifican los muestreadores y las texturas de forma independiente. el muestreo de textura se implementa mediante un objeto templated-texture. Este objeto templated-texture tiene un formato específico, devuelve un tipo específico e implementa varios métodos.
ms.assetid: e8cb483a-d831-4942-b6fe-61dd5edb1813
keywords:
- Objeto de textura HLSL
topic_type:
- apiref
api_name:
- Texture Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d1881ba4a88e97e978e2646c92d276bb9763ffd
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/09/2021
ms.locfileid: "111825775"
---
# <a name="texture-object"></a><span data-ttu-id="a7bfa-105">Objeto Texture</span><span class="sxs-lookup"><span data-stu-id="a7bfa-105">Texture Object</span></span>

<span data-ttu-id="a7bfa-106">En Direct3D 10, se especifican los muestreadores y las texturas de forma independiente. el muestreo de textura se implementa mediante un objeto templated-texture.</span><span class="sxs-lookup"><span data-stu-id="a7bfa-106">In Direct3D 10, you specify the samplers and textures independently; texture sampling is implemented by using a templated-texture object.</span></span> <span data-ttu-id="a7bfa-107">Este objeto templated-texture tiene un formato específico, devuelve un tipo específico e implementa varios métodos.</span><span class="sxs-lookup"><span data-stu-id="a7bfa-107">This templated-texture object has a specific format, returns a specific type, and implements several methods.</span></span>

<span data-ttu-id="a7bfa-108">Diferencias entre Direct3D9 y Direct3D10:</span><span class="sxs-lookup"><span data-stu-id="a7bfa-108">Differences between Direct3D9 and Direct3D10:</span></span>

- <span data-ttu-id="a7bfa-109">En Direct3D 9, los muestreadores se enlazan a texturas específicas.</span><span class="sxs-lookup"><span data-stu-id="a7bfa-109">In Direct3D 9, samplers are bound to specific textures.</span></span>
- <span data-ttu-id="a7bfa-110">En Direct3D 10, las texturas y los muestreadores son objetos independientes.</span><span class="sxs-lookup"><span data-stu-id="a7bfa-110">In Direct3D 10, textures and samplers are independent objects.</span></span> <span data-ttu-id="a7bfa-111">Cada objeto templated-texture implementa métodos de muestreo de textura que toman la textura y el muestreador como parámetros de entrada.</span><span class="sxs-lookup"><span data-stu-id="a7bfa-111">Each templated-texture object implements texture sampling methods that take both the texture and the sampler as input parameters.</span></span>



 

<span data-ttu-id="a7bfa-112">Esta es la sintaxis para crear todos los objetos de textura (excepto los objetos multimuestreo).</span><span class="sxs-lookup"><span data-stu-id="a7bfa-112">Here is the syntax for creating all texture objects (except multisampled objects).</span></span>



| <span data-ttu-id="a7bfa-113">Object1 \[ < *Nombre de* > \] *tipo*;</span><span class="sxs-lookup"><span data-stu-id="a7bfa-113">Object1 \[<*Type*>\] *Name*;</span></span> |
|------------------------------------|



 

<span data-ttu-id="a7bfa-114">Los objetos multimuestreo (Texture2DMS y Texture2DMSArray) requieren que el tamaño de la textura se especifique explícitamente y se exprese como el número de muestras.</span><span class="sxs-lookup"><span data-stu-id="a7bfa-114">Multisampled objects (Texture2DMS and Texture2DMSArray) require the texture size to be explicitly stated and expressed as the number of samples.</span></span>



| <span data-ttu-id="a7bfa-115">Object2 \[ < *Type, Samples* > \] *Name*;</span><span class="sxs-lookup"><span data-stu-id="a7bfa-115">Object2 \[<*Type, Samples*>\] *Name*;</span></span> |
|---------------------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="a7bfa-116">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a7bfa-116">Parameters</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a7bfa-117">Elemento</span><span class="sxs-lookup"><span data-stu-id="a7bfa-117">Item</span></span></th>
<th><span data-ttu-id="a7bfa-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="a7bfa-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a7bfa-119"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Objeto</em></span><span class="sxs-lookup"><span data-stu-id="a7bfa-119"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Object</em></span></span><br/></td>
<td><span data-ttu-id="a7bfa-120">Objeto de textura.</span><span class="sxs-lookup"><span data-stu-id="a7bfa-120">A texture object.</span></span> <span data-ttu-id="a7bfa-121">Debe ser uno de los tipos siguientes.</span><span class="sxs-lookup"><span data-stu-id="a7bfa-121">Must be one of the following types.</span></span> <br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="a7bfa-122">Tipo Object1</span><span class="sxs-lookup"><span data-stu-id="a7bfa-122">Object1 Type</span></span></th>
<th><span data-ttu-id="a7bfa-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="a7bfa-123">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a7bfa-124">Buffer</span><span class="sxs-lookup"><span data-stu-id="a7bfa-124">Buffer</span></span></td>
<td><span data-ttu-id="a7bfa-125">Buffer</span><span class="sxs-lookup"><span data-stu-id="a7bfa-125">Buffer</span></span> </td>
</tr>
<tr class="even">
<td><span data-ttu-id="a7bfa-126">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a7bfa-126">Texture1D</span></span></td>
<td><span data-ttu-id="a7bfa-127">Textura 1D</span><span class="sxs-lookup"><span data-stu-id="a7bfa-127">1D texture</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a7bfa-128">Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="a7bfa-128">Texture1DArray</span></span></td>
<td><span data-ttu-id="a7bfa-129">Matriz de texturas 1D</span><span class="sxs-lookup"><span data-stu-id="a7bfa-129">Array of 1D textures</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a7bfa-130">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a7bfa-130">Texture2D</span></span></td>
<td><span data-ttu-id="a7bfa-131">Textura 2D</span><span class="sxs-lookup"><span data-stu-id="a7bfa-131">2D texture</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a7bfa-132">Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="a7bfa-132">Texture2DArray</span></span></td>
<td><span data-ttu-id="a7bfa-133">Matriz de texturas 2D</span><span class="sxs-lookup"><span data-stu-id="a7bfa-133">Array of 2D textures</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a7bfa-134">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a7bfa-134">Texture3D</span></span></td>
<td><span data-ttu-id="a7bfa-135">Textura 3D</span><span class="sxs-lookup"><span data-stu-id="a7bfa-135">3D texture</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a7bfa-136">TextureCube</span><span class="sxs-lookup"><span data-stu-id="a7bfa-136">TextureCube</span></span></td>
<td><span data-ttu-id="a7bfa-137">Textura del cubo</span><span class="sxs-lookup"><span data-stu-id="a7bfa-137">Cube texture</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a7bfa-138">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="a7bfa-138">TextureCubeArray</span></span>  </td>
<td><span data-ttu-id="a7bfa-139">Matriz de texturas de cubo</span><span class="sxs-lookup"><span data-stu-id="a7bfa-139">Array of cube textures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a7bfa-140">Tipo Object2</span><span class="sxs-lookup"><span data-stu-id="a7bfa-140">Object2 Type</span></span></td>
<td><span data-ttu-id="a7bfa-141">Descripción</span><span class="sxs-lookup"><span data-stu-id="a7bfa-141">Description</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a7bfa-142">Texture2DMS</span><span class="sxs-lookup"><span data-stu-id="a7bfa-142">Texture2DMS</span></span></td>
<td><span data-ttu-id="a7bfa-143">Textura multimuestreo 2D</span><span class="sxs-lookup"><span data-stu-id="a7bfa-143">2D multisampled texture</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a7bfa-144">Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="a7bfa-144">Texture2DMSArray</span></span></td>
<td><span data-ttu-id="a7bfa-145">Matriz de texturas multimuestreo 2D</span><span class="sxs-lookup"><span data-stu-id="a7bfa-145">Array of 2D multisampled textures</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<ol>
<li><span data-ttu-id="a7bfa-146">El tipo Buffer admite la mayoría de los métodos de objeto de textura, excepto GetDimensions.</span><span class="sxs-lookup"><span data-stu-id="a7bfa-146">The Buffer type supports most texture object methods except GetDimensions.</span></span></li>
<li><span data-ttu-id="a7bfa-147">TextureCubeArray está disponible en el modelo de sombreador 4.1 o superior.</span><span class="sxs-lookup"><span data-stu-id="a7bfa-147">TextureCubeArray is available in shader model 4.1 or higher.</span></span></li>
<li><span data-ttu-id="a7bfa-148">El modelo de sombreador 4.1 está disponible en Direct3D 10.1 o posterior.</span><span class="sxs-lookup"><span data-stu-id="a7bfa-148">Shader model 4.1 is available in Direct3D 10.1 or higher.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a7bfa-149"><span id="Type"></span><span id="type"></span><span id="TYPE"></span><em>Tipo</em></span><span class="sxs-lookup"><span data-stu-id="a7bfa-149"><span id="Type"></span><span id="type"></span><span id="TYPE"></span><em>Type</em></span></span></p></td>
<td><p><span data-ttu-id="a7bfa-150">Opcional.</span><span class="sxs-lookup"><span data-stu-id="a7bfa-150">Optional.</span></span> <span data-ttu-id="a7bfa-151">Cualquier <a href="dx-graphics-hlsl-scalar.md">tipo HLSL escalar o</a> tipo <a href="dx-graphics-hlsl-vector.md"><strong>HLSL vectorial,</strong></a>entre corchetes angulares.</span><span class="sxs-lookup"><span data-stu-id="a7bfa-151">Any <a href="dx-graphics-hlsl-scalar.md">scalar HLSL type</a> or <a href="dx-graphics-hlsl-vector.md"><strong>vector HLSL type</strong></a>, surrounded by angle brackets.</span></span> <span data-ttu-id="a7bfa-152">El tipo predeterminado es <strong>float4.</strong></span><span class="sxs-lookup"><span data-stu-id="a7bfa-152">The default type is <strong>float4</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a7bfa-153"><span id="Name"></span><span id="name"></span><span id="NAME"></span><em>Nombre</em></span><span class="sxs-lookup"><span data-stu-id="a7bfa-153"><span id="Name"></span><span id="name"></span><span id="NAME"></span><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="a7bfa-154">Cadena ASCII que especifica el nombre del objeto de textura.</span><span class="sxs-lookup"><span data-stu-id="a7bfa-154">An ASCII string that specifies the texture object name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a7bfa-155"><span id="Samples"></span><span id="samples"></span><span id="SAMPLES"></span><em>Muestras</em></span><span class="sxs-lookup"><span data-stu-id="a7bfa-155"><span id="Samples"></span><span id="samples"></span><span id="SAMPLES"></span><em>Samples</em></span></span></p></td>
<td><p><span data-ttu-id="a7bfa-156">Número de muestras (intervalos entre 1 y 128).</span><span class="sxs-lookup"><span data-stu-id="a7bfa-156">The number of samples (ranges between 1 and 128).</span></span></p></td>
</tr>
</tbody>
</table>



 

## <a name="example-1"></a><span data-ttu-id="a7bfa-157">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="a7bfa-157">Example 1</span></span>

<span data-ttu-id="a7bfa-158">Este es un ejemplo de declaración de un objeto de textura.</span><span class="sxs-lookup"><span data-stu-id="a7bfa-158">Here is an example of declaring a texture object.</span></span>


```
Texture2D <float4> MyTex;

Texture2DMS <float4, 128> MyMSTex;
```



## <a name="texture-object-methods"></a><span data-ttu-id="a7bfa-159">Métodos de objeto texture</span><span class="sxs-lookup"><span data-stu-id="a7bfa-159">Texture Object Methods</span></span>

<span data-ttu-id="a7bfa-160">Cada objeto de textura implementa determinados métodos; esta es la tabla que enumera todos los métodos.</span><span class="sxs-lookup"><span data-stu-id="a7bfa-160">Each texture object implements certain methods; here's the table that lists all of the methods.</span></span> <span data-ttu-id="a7bfa-161">Consulte la página de referencia de cada método para ver qué objetos pueden usar ese método.</span><span class="sxs-lookup"><span data-stu-id="a7bfa-161">See the reference page for each method to see what objects can use that method.</span></span>



| <span data-ttu-id="a7bfa-162">Método texture</span><span class="sxs-lookup"><span data-stu-id="a7bfa-162">Texture Method</span></span>                                                                     | <span data-ttu-id="a7bfa-163">Descripción</span><span class="sxs-lookup"><span data-stu-id="a7bfa-163">Description</span></span>                                                                                                       | <span data-ttu-id="a7bfa-164">vs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a7bfa-164">vs\_4\_0</span></span> | <span data-ttu-id="a7bfa-165">vs \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="a7bfa-165">vs\_4\_1</span></span>  | <span data-ttu-id="a7bfa-166">ps \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a7bfa-166">ps\_4\_0</span></span> | <span data-ttu-id="a7bfa-167">ps \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="a7bfa-167">ps\_4\_1</span></span>  | <span data-ttu-id="a7bfa-168">gs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a7bfa-168">gs\_4\_0</span></span> | <span data-ttu-id="a7bfa-169">gs \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="a7bfa-169">gs\_4\_1</span></span>  |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|----------|-----------|----------|-----------|----------|-----------|
| [<span data-ttu-id="a7bfa-170">CalculateLevelOfDetail</span><span class="sxs-lookup"><span data-stu-id="a7bfa-170">CalculateLevelOfDetail</span></span>](dx-graphics-hlsl-to-calculate-lod.md)                    | <span data-ttu-id="a7bfa-171">Calcule el LOD y devuelva un resultado de fijación.</span><span class="sxs-lookup"><span data-stu-id="a7bfa-171">Calculate the LOD, return a clamped result.</span></span>                                                                       |          |           |          | <span data-ttu-id="a7bfa-172">x</span><span class="sxs-lookup"><span data-stu-id="a7bfa-172">x</span></span>         |          |           |
| [<span data-ttu-id="a7bfa-173">CalculateLevelOfDetailUnclamped</span><span class="sxs-lookup"><span data-stu-id="a7bfa-173">CalculateLevelOfDetailUnclamped</span></span>](dx-graphics-hlsl-to-calculate-lod-unclamped.md) | <span data-ttu-id="a7bfa-174">Calcule el LOD y devuelva un resultado no reclamado.</span><span class="sxs-lookup"><span data-stu-id="a7bfa-174">Calculate the LOD, return an unclamped result.</span></span>                                                                    |          |           |          | <span data-ttu-id="a7bfa-175">x</span><span class="sxs-lookup"><span data-stu-id="a7bfa-175">x</span></span>         |          |           |
| [<span data-ttu-id="a7bfa-176">Reunir</span><span class="sxs-lookup"><span data-stu-id="a7bfa-176">Gather</span></span>](dx-graphics-hlsl-to-gather.md)                                           | <span data-ttu-id="a7bfa-177">Obtiene las cuatro muestras (solo componente rojo) que se usarían para la interpolación bilineal al muestrear una textura.</span><span class="sxs-lookup"><span data-stu-id="a7bfa-177">Gets the four samples (red component only) that would be used for bilinear interpolation when sampling a texture.</span></span> |          | <span data-ttu-id="a7bfa-178">x</span><span class="sxs-lookup"><span data-stu-id="a7bfa-178">x</span></span>         |          | <span data-ttu-id="a7bfa-179">x</span><span class="sxs-lookup"><span data-stu-id="a7bfa-179">x</span></span>         |          | <span data-ttu-id="a7bfa-180">x</span><span class="sxs-lookup"><span data-stu-id="a7bfa-180">x</span></span>         |
| [<span data-ttu-id="a7bfa-181">GetDimensions</span><span class="sxs-lookup"><span data-stu-id="a7bfa-181">GetDimensions</span></span>](dx-graphics-hlsl-to-getdimensions.md)                             | <span data-ttu-id="a7bfa-182">Obtiene la dimensión de textura para un nivel de mapa mip especificado.</span><span class="sxs-lookup"><span data-stu-id="a7bfa-182">Get the texture dimension for a specified mipmap level.</span></span>                                                           | <span data-ttu-id="a7bfa-183">x</span><span class="sxs-lookup"><span data-stu-id="a7bfa-183">x</span></span>        | <span data-ttu-id="a7bfa-184">x</span><span class="sxs-lookup"><span data-stu-id="a7bfa-184">x</span></span>         | <span data-ttu-id="a7bfa-185">x</span><span class="sxs-lookup"><span data-stu-id="a7bfa-185">x</span></span>        | <span data-ttu-id="a7bfa-186">x</span><span class="sxs-lookup"><span data-stu-id="a7bfa-186">x</span></span>         | <span data-ttu-id="a7bfa-187">x</span><span class="sxs-lookup"><span data-stu-id="a7bfa-187">x</span></span>        | <span data-ttu-id="a7bfa-188">x</span><span class="sxs-lookup"><span data-stu-id="a7bfa-188">x</span></span>         |
| [<span data-ttu-id="a7bfa-189">GetDimensions (MultiSample)</span><span class="sxs-lookup"><span data-stu-id="a7bfa-189">GetDimensions (MultiSample)</span></span>](dx-graphics-hlsl-to-getdimensions.md)               | <span data-ttu-id="a7bfa-190">Obtiene la dimensión de textura para un nivel de mapa mip especificado.</span><span class="sxs-lookup"><span data-stu-id="a7bfa-190">Get the texture dimension for a specified mipmap level.</span></span>                                                           |          | <span data-ttu-id="a7bfa-191">x</span><span class="sxs-lookup"><span data-stu-id="a7bfa-191">x</span></span>         |          | <span data-ttu-id="a7bfa-192">x</span><span class="sxs-lookup"><span data-stu-id="a7bfa-192">x</span></span>         |          | <span data-ttu-id="a7bfa-193">x</span><span class="sxs-lookup"><span data-stu-id="a7bfa-193">x</span></span>         |
| [<span data-ttu-id="a7bfa-194">GetSamplePosition</span><span class="sxs-lookup"><span data-stu-id="a7bfa-194">GetSamplePosition</span></span>](dx-graphics-hlsl-to-get-sample-position.md)                   | <span data-ttu-id="a7bfa-195">Obtiene la posición del ejemplo especificado.</span><span class="sxs-lookup"><span data-stu-id="a7bfa-195">Get the position of the specified sample.</span></span>                                                                         |          | <span data-ttu-id="a7bfa-196">x</span><span class="sxs-lookup"><span data-stu-id="a7bfa-196">x</span></span>         |          | <span data-ttu-id="a7bfa-197">x</span><span class="sxs-lookup"><span data-stu-id="a7bfa-197">x</span></span>         |          | <span data-ttu-id="a7bfa-198">x</span><span class="sxs-lookup"><span data-stu-id="a7bfa-198">x</span></span>         |
| [<span data-ttu-id="a7bfa-199">Cargar</span><span class="sxs-lookup"><span data-stu-id="a7bfa-199">Load</span></span>](dx-graphics-hlsl-to-load.md)                                               | <span data-ttu-id="a7bfa-200">Cargar datos sin ningún filtrado ni muestreo.</span><span class="sxs-lookup"><span data-stu-id="a7bfa-200">Load data without any filtering or sampling.</span></span>                                                                      | <span data-ttu-id="a7bfa-201">x</span><span class="sxs-lookup"><span data-stu-id="a7bfa-201">x</span></span>        | <span data-ttu-id="a7bfa-202">x</span><span class="sxs-lookup"><span data-stu-id="a7bfa-202">x</span></span>         | <span data-ttu-id="a7bfa-203">x</span><span class="sxs-lookup"><span data-stu-id="a7bfa-203">x</span></span>        | <span data-ttu-id="a7bfa-204">x</span><span class="sxs-lookup"><span data-stu-id="a7bfa-204">x</span></span>         | <span data-ttu-id="a7bfa-205">x</span><span class="sxs-lookup"><span data-stu-id="a7bfa-205">x</span></span>        | <span data-ttu-id="a7bfa-206">x</span><span class="sxs-lookup"><span data-stu-id="a7bfa-206">x</span></span>         |
| [<span data-ttu-id="a7bfa-207">Carga (multimuestreo)</span><span class="sxs-lookup"><span data-stu-id="a7bfa-207">Load (Multisample)</span></span>](dx-graphics-hlsl-to-load.md)                                 | <span data-ttu-id="a7bfa-208">Cargar datos sin ningún filtrado ni muestreo.</span><span class="sxs-lookup"><span data-stu-id="a7bfa-208">Load data without any filtering or sampling.</span></span>                                                                      |          | <span data-ttu-id="a7bfa-209">x</span><span class="sxs-lookup"><span data-stu-id="a7bfa-209">x</span></span>         | <span data-ttu-id="a7bfa-210">x</span><span class="sxs-lookup"><span data-stu-id="a7bfa-210">x</span></span>        | <span data-ttu-id="a7bfa-211">x</span><span class="sxs-lookup"><span data-stu-id="a7bfa-211">x</span></span>         |          | <span data-ttu-id="a7bfa-212">x</span><span class="sxs-lookup"><span data-stu-id="a7bfa-212">x</span></span>         |
| [<span data-ttu-id="a7bfa-213">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a7bfa-213">Sample</span></span>](dx-graphics-hlsl-to-sample.md)                                           | <span data-ttu-id="a7bfa-214">Muestrear una textura.</span><span class="sxs-lookup"><span data-stu-id="a7bfa-214">Sample a texture.</span></span>                                                                                                 |          |           | <span data-ttu-id="a7bfa-215">x</span><span class="sxs-lookup"><span data-stu-id="a7bfa-215">x</span></span>        | <span data-ttu-id="a7bfa-216">x</span><span class="sxs-lookup"><span data-stu-id="a7bfa-216">x</span></span>         |          |           |
| [<span data-ttu-id="a7bfa-217">SampleBias</span><span class="sxs-lookup"><span data-stu-id="a7bfa-217">SampleBias</span></span>](dx-graphics-hlsl-to-samplebias.md)                                   | <span data-ttu-id="a7bfa-218">Muestrear una textura, después de aplicar el valor de sesgo al nivel de mapa mip.</span><span class="sxs-lookup"><span data-stu-id="a7bfa-218">Sample a texture, after applying the bias value to the mipmap level.</span></span>                                              |          |           | <span data-ttu-id="a7bfa-219">x</span><span class="sxs-lookup"><span data-stu-id="a7bfa-219">x</span></span>        | <span data-ttu-id="a7bfa-220">x</span><span class="sxs-lookup"><span data-stu-id="a7bfa-220">x</span></span>         |          |           |
| [<span data-ttu-id="a7bfa-221">SampleCmp</span><span class="sxs-lookup"><span data-stu-id="a7bfa-221">SampleCmp</span></span>](dx-graphics-hlsl-to-samplecmp.md)                                     | <span data-ttu-id="a7bfa-222">Muestrear una textura mediante un valor de comparación para rechazar muestras.</span><span class="sxs-lookup"><span data-stu-id="a7bfa-222">Sample a texture, using a comparison value to reject samples.</span></span>                                                     |          |           | <span data-ttu-id="a7bfa-223">x</span><span class="sxs-lookup"><span data-stu-id="a7bfa-223">x</span></span>        | <span data-ttu-id="a7bfa-224">x</span><span class="sxs-lookup"><span data-stu-id="a7bfa-224">x</span></span>         |          |           |
| [<span data-ttu-id="a7bfa-225">SampleCmpLevelZero</span><span class="sxs-lookup"><span data-stu-id="a7bfa-225">SampleCmpLevelZero</span></span>](dx-graphics-hlsl-to-samplecmplevelzero.md)                   | <span data-ttu-id="a7bfa-226">Muestrear una textura (solo mipmap nivel 0), usando un valor de comparación para rechazar muestras.</span><span class="sxs-lookup"><span data-stu-id="a7bfa-226">Sample a texture (mipmap level 0 only), using a comparison value to reject samples.</span></span>                               | <span data-ttu-id="a7bfa-227">x</span><span class="sxs-lookup"><span data-stu-id="a7bfa-227">x</span></span>        | <span data-ttu-id="a7bfa-228">x</span><span class="sxs-lookup"><span data-stu-id="a7bfa-228">x</span></span>         | <span data-ttu-id="a7bfa-229">x</span><span class="sxs-lookup"><span data-stu-id="a7bfa-229">x</span></span>        | <span data-ttu-id="a7bfa-230">x</span><span class="sxs-lookup"><span data-stu-id="a7bfa-230">x</span></span>         | <span data-ttu-id="a7bfa-231">x</span><span class="sxs-lookup"><span data-stu-id="a7bfa-231">x</span></span>        | <span data-ttu-id="a7bfa-232">x</span><span class="sxs-lookup"><span data-stu-id="a7bfa-232">x</span></span>         |
| [<span data-ttu-id="a7bfa-233">SampleGrad</span><span class="sxs-lookup"><span data-stu-id="a7bfa-233">SampleGrad</span></span>](dx-graphics-hlsl-to-samplegrad.md)                                   | <span data-ttu-id="a7bfa-234">Muestrear una textura mediante un degradado para influir en la forma en que se calcula la ubicación de la muestra.</span><span class="sxs-lookup"><span data-stu-id="a7bfa-234">Sample a texture using a gradient to influence the way the sample location is calculated.</span></span>                         | <span data-ttu-id="a7bfa-235">x</span><span class="sxs-lookup"><span data-stu-id="a7bfa-235">x</span></span>        | <span data-ttu-id="a7bfa-236">x</span><span class="sxs-lookup"><span data-stu-id="a7bfa-236">x</span></span>         | <span data-ttu-id="a7bfa-237">x</span><span class="sxs-lookup"><span data-stu-id="a7bfa-237">x</span></span>        | <span data-ttu-id="a7bfa-238">x</span><span class="sxs-lookup"><span data-stu-id="a7bfa-238">x</span></span>         | <span data-ttu-id="a7bfa-239">x</span><span class="sxs-lookup"><span data-stu-id="a7bfa-239">x</span></span>        | <span data-ttu-id="a7bfa-240">x</span><span class="sxs-lookup"><span data-stu-id="a7bfa-240">x</span></span>         |
| [<span data-ttu-id="a7bfa-241">SampleLevel</span><span class="sxs-lookup"><span data-stu-id="a7bfa-241">SampleLevel</span></span>](dx-graphics-hlsl-to-samplelevel.md)                                 | <span data-ttu-id="a7bfa-242">Muestrear una textura en el nivel de mapa mip especificado.</span><span class="sxs-lookup"><span data-stu-id="a7bfa-242">Sample a texture on the specified mipmap level.</span></span>                                                                   | <span data-ttu-id="a7bfa-243">x</span><span class="sxs-lookup"><span data-stu-id="a7bfa-243">x</span></span>        | <span data-ttu-id="a7bfa-244">x</span><span class="sxs-lookup"><span data-stu-id="a7bfa-244">x</span></span>         | <span data-ttu-id="a7bfa-245">x</span><span class="sxs-lookup"><span data-stu-id="a7bfa-245">x</span></span>        | <span data-ttu-id="a7bfa-246">x</span><span class="sxs-lookup"><span data-stu-id="a7bfa-246">x</span></span>         | <span data-ttu-id="a7bfa-247">x</span><span class="sxs-lookup"><span data-stu-id="a7bfa-247">x</span></span>        | <span data-ttu-id="a7bfa-248">x</span><span class="sxs-lookup"><span data-stu-id="a7bfa-248">x</span></span>         |



 

### <a name="return-type"></a><span data-ttu-id="a7bfa-249">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a7bfa-249">Return Type</span></span>

<span data-ttu-id="a7bfa-250">El tipo de valor devuelto de un método de objeto de textura es float4 a menos que se especifique lo contrario, a excepción de los objetos de textura con suavizado de alias multimuestreo que siempre necesitan el tipo y el recuento de muestras especificados.</span><span class="sxs-lookup"><span data-stu-id="a7bfa-250">The return type of a texture object method is float4 unless specified otherwise, with the exception of the multisampled anti-aliased texture objects that always need the type and sample count specified.</span></span> <span data-ttu-id="a7bfa-251">El tipo de valor devuelto es el mismo que el tipo de recurso de textura [**(DXGI \_ FORMAT).**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)</span><span class="sxs-lookup"><span data-stu-id="a7bfa-251">The return type is the same as the texture resource type ([**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)).</span></span> <span data-ttu-id="a7bfa-252">En otras palabras, puede ser cualquiera de los tipos siguientes.</span><span class="sxs-lookup"><span data-stu-id="a7bfa-252">In other words, it can be any of the following types.</span></span>



| <span data-ttu-id="a7bfa-253">Tipo</span><span class="sxs-lookup"><span data-stu-id="a7bfa-253">Type</span></span>                       | <span data-ttu-id="a7bfa-254">Description</span><span class="sxs-lookup"><span data-stu-id="a7bfa-254">Description</span></span>                                                                                                                                                             |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7bfa-255">FLOAT</span><span class="sxs-lookup"><span data-stu-id="a7bfa-255">float</span></span>                      | <span data-ttu-id="a7bfa-256">Float de 32 bits (consulte [Reglas de punto flotante para](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-float-rules) ver las diferencias con respecto a IEEE float).</span><span class="sxs-lookup"><span data-stu-id="a7bfa-256">32-bit float (see [Floating-Point Rules](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-float-rules) for differences from IEEE float)</span></span>                            |
| <span data-ttu-id="a7bfa-257">int</span><span class="sxs-lookup"><span data-stu-id="a7bfa-257">int</span></span>                        | <span data-ttu-id="a7bfa-258">Entero de 32 bits con signo</span><span class="sxs-lookup"><span data-stu-id="a7bfa-258">32-bit signed integer</span></span>                                                                                                                                                   |
| <span data-ttu-id="a7bfa-259">unsigned int</span><span class="sxs-lookup"><span data-stu-id="a7bfa-259">unsigned int</span></span>               | <span data-ttu-id="a7bfa-260">Entero de 32 bits sin signo</span><span class="sxs-lookup"><span data-stu-id="a7bfa-260">32-bit unsigned integer</span></span>                                                                                                                                                 |
| <span data-ttu-id="a7bfa-261">snorm</span><span class="sxs-lookup"><span data-stu-id="a7bfa-261">snorm</span></span>                      | <span data-ttu-id="a7bfa-262">Float de 32 bits en el intervalo de -1 a 1 inclusivo (consulte [Reglas](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-float-rules) de punto flotante para ver las diferencias con respecto a IEEE float).</span><span class="sxs-lookup"><span data-stu-id="a7bfa-262">32-bit float in range -1 to 1 inclusive (see [Floating-Point Rules](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-float-rules) for differences from IEEE float)</span></span> |
| <span data-ttu-id="a7bfa-263">unorm</span><span class="sxs-lookup"><span data-stu-id="a7bfa-263">unorm</span></span>                      | <span data-ttu-id="a7bfa-264">Float de 32 bits en el intervalo 0 a 1 inclusivo (consulte [Reglas](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-float-rules) de punto flotante para ver las diferencias con respecto a IEEE float).</span><span class="sxs-lookup"><span data-stu-id="a7bfa-264">32-bit float in range 0 to 1 inclusive (see [Floating-Point Rules](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-float-rules) for differences from IEEE float)</span></span>  |
| <span data-ttu-id="a7bfa-265">cualquier tipo de textura o estructura</span><span class="sxs-lookup"><span data-stu-id="a7bfa-265">any texture type or struct</span></span> | <span data-ttu-id="a7bfa-266">El número de componentes devueltos debe estar entre 1 y 3 inclusive.</span><span class="sxs-lookup"><span data-stu-id="a7bfa-266">The number of components returned must be between 1 and 3 inclusive.</span></span>                                                                                                    |



 

<span data-ttu-id="a7bfa-267">Además, el tipo de valor devuelto puede ser cualquier tipo de textura, incluida una estructura, pero debe ser menor que 4 componentes, como un tipo float1 que devuelve un componente.</span><span class="sxs-lookup"><span data-stu-id="a7bfa-267">In addition, the return type can be any texture type including a structure but, it must be less than 4 components such as a float1 type which returns one component.</span></span>

## <a name="default-values-for-missing-components-in-a-texture"></a><span data-ttu-id="a7bfa-268">Valores predeterminados para los componentes que faltan en una textura</span><span class="sxs-lookup"><span data-stu-id="a7bfa-268">Default Values for Missing Components in a Texture</span></span>

<span data-ttu-id="a7bfa-269">El valor predeterminado de los componentes que faltan en un tipo de recurso de textura es cero para cualquier componente excepto el componente alfa (A); El valor predeterminado de la A que falta es uno.</span><span class="sxs-lookup"><span data-stu-id="a7bfa-269">The default value for missing components in a texture resource type is zero for any component except the alpha component (A); the default value for the missing A is one.</span></span> <span data-ttu-id="a7bfa-270">La forma en que este aparece en el sombreador depende del tipo de recurso de textura.</span><span class="sxs-lookup"><span data-stu-id="a7bfa-270">The way that this one appears to the shader depends on the texture resource type.</span></span> <span data-ttu-id="a7bfa-271">Toma la forma del primer componente con tipo que realmente está presente en el tipo de recurso de textura (empezando por la izquierda en orden RGBA).</span><span class="sxs-lookup"><span data-stu-id="a7bfa-271">It takes the form of the first typed component that is actually present in the texture resource type (starting from the left in RGBA order).</span></span> <span data-ttu-id="a7bfa-272">Si este formulario es UNORM o FLOAT, el valor predeterminado de la A que falta es 1,0f.</span><span class="sxs-lookup"><span data-stu-id="a7bfa-272">If this form is UNORM or FLOAT, the default value for the missing A is 1.0f.</span></span> <span data-ttu-id="a7bfa-273">Si el formulario es SINT o UINT, el valor predeterminado de la A que falta es 0x1.</span><span class="sxs-lookup"><span data-stu-id="a7bfa-273">If the form is SINT or UINT, the default value for the missing A is 0x1.</span></span>

<span data-ttu-id="a7bfa-274">Por ejemplo, cuando un sombreador lee el tipo de recurso de textura [**DXGI \_ FORMAT \_ R24 \_ UNORM \_ X8 \_ TYPELESS,**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) Los valores predeterminados de G y B son cero y el valor predeterminado de A es 1,0f; cuando un sombreador lee el tipo de recurso de textura [**UINT DXGI \_ FORMAT \_ R16G16, \_**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) el valor predeterminado para B es cero y el valor predeterminado para A es 0x00000001; cuando un sombreador lee el tipo de recurso de textura [**\_ DXGI FORMAT \_ R16 \_ SINT,**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) los valores predeterminados para G y B son cero y el valor predeterminado para A es 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="a7bfa-274">For example, when a shader reads the [**DXGI\_FORMAT\_R24\_UNORM\_X8\_TYPELESS**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) texture resource type, the default values for G and B are zero and the default value for A is 1.0f; when a shader reads the [**DXGI\_FORMAT\_R16G16\_UINT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) texture resource type, the default value for B is zero and the default value for A is 0x00000001; when a shader reads the [**DXGI\_FORMAT\_R16\_SINT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) texture resource type, the default values for G and B are zero and the default value for A is 0x00000001.</span></span>

## <a name="example-2"></a><span data-ttu-id="a7bfa-275">Ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="a7bfa-275">Example 2</span></span>

<span data-ttu-id="a7bfa-276">Este es un ejemplo de muestreo de textura mediante un método de textura.</span><span class="sxs-lookup"><span data-stu-id="a7bfa-276">Here is an example of texture sampling using a texture method.</span></span>


```
sampler MySamp;
Texture2D <float4> MyTex;
 
float4 main( float2 TexCoords[2] : TEXCOORD ) : SV_Target
{
    return MyTex.Sample( MySamp, TexCoords[0] ));
}
```



## <a name="minimum-shader-model"></a><span data-ttu-id="a7bfa-277">Modelo mínimo de sombreador</span><span class="sxs-lookup"><span data-stu-id="a7bfa-277">Minimum Shader Model</span></span>

<span data-ttu-id="a7bfa-278">Este objeto se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="a7bfa-278">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="a7bfa-279">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="a7bfa-279">Shader Model</span></span>                                                        | <span data-ttu-id="a7bfa-280">Compatible</span><span class="sxs-lookup"><span data-stu-id="a7bfa-280">Supported</span></span> |
|---------------------------------------------------------------------|-----------|
| <span data-ttu-id="a7bfa-281">[Modelos de sombreador 4](dx-graphics-hlsl-sm4.md) y superiores</span><span class="sxs-lookup"><span data-stu-id="a7bfa-281">[Shader Model 4](dx-graphics-hlsl-sm4.md) and higher shader models</span></span> | <span data-ttu-id="a7bfa-282">sí</span><span class="sxs-lookup"><span data-stu-id="a7bfa-282">yes</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="a7bfa-283">Vea también</span><span class="sxs-lookup"><span data-stu-id="a7bfa-283">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7bfa-284">Shader Model 4</span><span class="sxs-lookup"><span data-stu-id="a7bfa-284">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

