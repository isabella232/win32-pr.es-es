---
title: Ejemplo (objeto de textura HLSL de DirectX)
description: Muestrea una textura. | Ejemplo (objeto de textura HLSL de DirectX)
ms.assetid: 788ba4b4-8013-411f-9a19-fb9983386fa0
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2374063d222d06576f720fed2aa7fb714bcccf04
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/09/2021
ms.locfileid: "111825752"
---
# <a name="sample-directx-hlsl-texture-object"></a><span data-ttu-id="ce908-104">Ejemplo (objeto de textura HLSL de DirectX)</span><span class="sxs-lookup"><span data-stu-id="ce908-104">Sample (DirectX HLSL Texture Object)</span></span>

<span data-ttu-id="ce908-105">Muestrea una textura.</span><span class="sxs-lookup"><span data-stu-id="ce908-105">Samples a texture.</span></span>

<span data-ttu-id="ce908-106">&lt;Template Type &gt; Object.Sample( sampler \_ state S, float Location \[ , int Offset \] );</span><span class="sxs-lookup"><span data-stu-id="ce908-106">&lt;Template Type&gt; Object.Sample( sampler\_state S, float Location \[, int Offset\] );</span></span>

## <a name="parameters"></a><span data-ttu-id="ce908-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ce908-107">Parameters</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ce908-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="ce908-108">Item</span></span></th>
<th><span data-ttu-id="ce908-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="ce908-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ce908-110"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Objeto</em></span><span class="sxs-lookup"><span data-stu-id="ce908-110"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Object</em></span></span><br/></td>
<td><span data-ttu-id="ce908-111">Cualquier <a href="dx-graphics-hlsl-to-type.md">tipo de objeto de</a> textura (excepto Texture2DMS y Texture2DMSArray).</span><span class="sxs-lookup"><span data-stu-id="ce908-111">Any <a href="dx-graphics-hlsl-to-type.md">texture-object</a> type (except Texture2DMS and Texture2DMSArray).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ce908-112"><span id="S"></span><span id="s"></span><em>S</em></span><span class="sxs-lookup"><span data-stu-id="ce908-112"><span id="S"></span><span id="s"></span><em>S</em></span></span><br/></td>
<td><span data-ttu-id="ce908-113">[in] Un <a href="dx-graphics-hlsl-sampler.md">estado sampler</a>.</span><span class="sxs-lookup"><span data-stu-id="ce908-113">[in] A <a href="dx-graphics-hlsl-sampler.md">Sampler state</a>.</span></span> <span data-ttu-id="ce908-114">Se trata de un objeto declarado en un archivo de efecto que contiene asignaciones de estado.</span><span class="sxs-lookup"><span data-stu-id="ce908-114">This is an object declared in an effect file that contains state assignments.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ce908-115"><span id="Location"></span><span id="location"></span><span id="LOCATION"></span><em>Ubicación</em></span><span class="sxs-lookup"><span data-stu-id="ce908-115"><span id="Location"></span><span id="location"></span><span id="LOCATION"></span><em>Location</em></span></span><br/></td>
<td><span data-ttu-id="ce908-116">[in] Coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="ce908-116">[in] The texture coordinates.</span></span> <span data-ttu-id="ce908-117">El tipo de argumento depende del tipo texture-object.</span><span class="sxs-lookup"><span data-stu-id="ce908-117">The argument type is dependent on the texture-object type.</span></span> <br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="ce908-118">Texture-Object type</span><span class="sxs-lookup"><span data-stu-id="ce908-118">Texture-Object Type</span></span></th>
<th><span data-ttu-id="ce908-119">Tipo de parámetro</span><span class="sxs-lookup"><span data-stu-id="ce908-119">Parameter Type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ce908-120">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ce908-120">Texture1D</span></span></td>
<td><span data-ttu-id="ce908-121">FLOAT</span><span class="sxs-lookup"><span data-stu-id="ce908-121">float</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ce908-122">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="ce908-122">Texture1DArray, Texture2D</span></span></td>
<td><span data-ttu-id="ce908-123">float2</span><span class="sxs-lookup"><span data-stu-id="ce908-123">float2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ce908-124">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="ce908-124">Texture2DArray, Texture3D, TextureCube</span></span></td>
<td><span data-ttu-id="ce908-125">float3</span><span class="sxs-lookup"><span data-stu-id="ce908-125">float3</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ce908-126">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="ce908-126">TextureCubeArray</span></span> </td>
<td><span data-ttu-id="ce908-127">float4</span><span class="sxs-lookup"><span data-stu-id="ce908-127">float4</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ce908-128"><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span><em>Compensar</em></span><span class="sxs-lookup"><span data-stu-id="ce908-128"><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span><em>Offset</em></span></span></p></td>
<td><p><span data-ttu-id="ce908-129">[in] Desplazamiento de coordenadas de textura opcional, que se puede usar para cualquier tipo de objeto de textura; el desplazamiento se aplica a la ubicación antes del muestreo.</span><span class="sxs-lookup"><span data-stu-id="ce908-129">[in] An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="ce908-130">Los desplazamientos de textura deben ser estáticos.</span><span class="sxs-lookup"><span data-stu-id="ce908-130">The texture offsets need to be static.</span></span> <span data-ttu-id="ce908-131">El tipo de argumento depende del tipo texture-object.</span><span class="sxs-lookup"><span data-stu-id="ce908-131">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="ce908-132">Para obtener más información, vea <a href="/windows/win32/direct3dhlsl/dx-graphics-hlsl-to-sample#applying-texture-coordinate-offsets">Aplicar desplazamientos de coordenadas de textura.</a></span><span class="sxs-lookup"><span data-stu-id="ce908-132">For more info, see <a href="/windows/win32/direct3dhlsl/dx-graphics-hlsl-to-sample#applying-texture-coordinate-offsets">Applying texture coordinate offsets</a>.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="ce908-133">Texture-Object type</span><span class="sxs-lookup"><span data-stu-id="ce908-133">Texture-Object Type</span></span></th>
<th><span data-ttu-id="ce908-134">Tipo de parámetro</span><span class="sxs-lookup"><span data-stu-id="ce908-134">Parameter Type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ce908-135">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="ce908-135">Texture1D, Texture1DArray</span></span></td>
<td><span data-ttu-id="ce908-136">int</span><span class="sxs-lookup"><span data-stu-id="ce908-136">int</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ce908-137">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="ce908-137">Texture2D, Texture2DArray</span></span></td>
<td><span data-ttu-id="ce908-138">int2</span><span class="sxs-lookup"><span data-stu-id="ce908-138">int2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ce908-139">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ce908-139">Texture3D</span></span></td>
<td><span data-ttu-id="ce908-140">int3</span><span class="sxs-lookup"><span data-stu-id="ce908-140">int3</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ce908-141">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="ce908-141">TextureCube, TextureCubeArray</span></span> </td>
<td><span data-ttu-id="ce908-142">no admitido</span><span class="sxs-lookup"><span data-stu-id="ce908-142">not supported</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>

## <a name="return-value"></a><span data-ttu-id="ce908-143">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ce908-143">Return value</span></span>

<span data-ttu-id="ce908-144">El tipo de plantilla de la textura, que puede ser un vector de uno o varios componentes.</span><span class="sxs-lookup"><span data-stu-id="ce908-144">The texture's template type, which may be a single- or multi-component vector.</span></span> <span data-ttu-id="ce908-145">El formato se basa en EL [**FORMATO DXGI de la \_ textura.**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)</span><span class="sxs-lookup"><span data-stu-id="ce908-145">The format is based on the texture's [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="ce908-146">Modelo mínimo de sombreador</span><span class="sxs-lookup"><span data-stu-id="ce908-146">Minimum Shader Model</span></span>

<span data-ttu-id="ce908-147">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="ce908-147">This function is supported in the following shader models.</span></span>

| <span data-ttu-id="ce908-148">vs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="ce908-148">vs\_4\_0</span></span> | <span data-ttu-id="ce908-149">vs \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="ce908-149">vs\_4\_1</span></span>  | <span data-ttu-id="ce908-150">ps \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="ce908-150">ps\_4\_0</span></span> | <span data-ttu-id="ce908-151">ps \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="ce908-151">ps\_4\_1</span></span>  | <span data-ttu-id="ce908-152">gs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="ce908-152">gs\_4\_0</span></span> | <span data-ttu-id="ce908-153">gs \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="ce908-153">gs\_4\_1</span></span>  |
|----------|-----------|----------|-----------|----------|-----------|
|          |           | <span data-ttu-id="ce908-154">x</span><span class="sxs-lookup"><span data-stu-id="ce908-154">x</span></span>        | <span data-ttu-id="ce908-155">x</span><span class="sxs-lookup"><span data-stu-id="ce908-155">x</span></span>         |          |           |

1.  <span data-ttu-id="ce908-156">TextureCubeArray está disponible en Shader Model 4.1 o superior.</span><span class="sxs-lookup"><span data-stu-id="ce908-156">TextureCubeArray is available in Shader Model 4.1 or higher.</span></span>
2.  <span data-ttu-id="ce908-157">El modelo de sombreador 4.1 está disponible en Direct3D 10.1 o posterior.</span><span class="sxs-lookup"><span data-stu-id="ce908-157">Shader Model 4.1 is available in Direct3D 10.1 or higher.</span></span>

## <a name="example"></a><span data-ttu-id="ce908-158">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ce908-158">Example</span></span>

<span data-ttu-id="ce908-159">Este ejemplo de código parcial se basa en el archivo BasicHLSL11.fx del [ejemplo BasicHLSL11](https://github.com/microsoftarchive/msdn-code-gallery-community-a-c/tree/master/Basic%20DXUT%20Win32%20Samples/%5BC%2B%2B%5D-Basic%20DXUT%20Win32%20Samples/C%2B%2B/BasicHLSL11).</span><span class="sxs-lookup"><span data-stu-id="ce908-159">This partial code example is based on the BasicHLSL11.fx file in the [BasicHLSL11 Sample](https://github.com/microsoftarchive/msdn-code-gallery-community-a-c/tree/master/Basic%20DXUT%20Win32%20Samples/%5BC%2B%2B%5D-Basic%20DXUT%20Win32%20Samples/C%2B%2B/BasicHLSL11).</span></span>

```
// Object Declarations
Texture2D g_MeshTexture;            // Color texture for mesh

SamplerState MeshTextureSampler
{
    Filter = MIN_MAG_MIP_LINEAR;
    AddressU = Wrap;
    AddressV = Wrap;
};

struct VS_OUTPUT
{
    float4 Position   : SV_POSITION; // vertex position 
    float4 Diffuse    : COLOR0;      // vertex diffuse color (note that COLOR0 is clamped from 0..1)
    float2 TextureUV  : TEXCOORD0;   // vertex texture coords 
};

VS_OUTPUT In;

// Shader body calling the intrinsic function
   ...
        Output.RGBColor = g_MeshTexture.Sample(MeshTextureSampler, In.TextureUV) * In.Diffuse;
```

## <a name="remarks"></a><span data-ttu-id="ce908-160">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ce908-160">Remarks</span></span>

<span data-ttu-id="ce908-161">El muestreo de textura usa la posición del texel para buscar un valor de texel.</span><span class="sxs-lookup"><span data-stu-id="ce908-161">Texture sampling uses the texel position to look up a texel value.</span></span> <span data-ttu-id="ce908-162">Se puede aplicar un desplazamiento a la posición antes de la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="ce908-162">An offset can be applied to the position before lookup.</span></span> <span data-ttu-id="ce908-163">El estado del muestreador contiene las opciones de muestreo y filtrado.</span><span class="sxs-lookup"><span data-stu-id="ce908-163">The sampler state contains the sampling and filtering options.</span></span> <span data-ttu-id="ce908-164">Este método se puede invocar dentro de un sombreador de píxeles, pero no se admite en un sombreador de vértices o un sombreador de geometría.</span><span class="sxs-lookup"><span data-stu-id="ce908-164">This method can be invoked within a pixel shader, but it is not supported in a vertex shader or a geometry shader.</span></span>

<span data-ttu-id="ce908-165">Use un desplazamiento solo en un miplevel entero; De lo contrario, puede obtener resultados diferentes en función de la implementación de hardware o la configuración del controlador.</span><span class="sxs-lookup"><span data-stu-id="ce908-165">Use an offset only at an integer miplevel; otherwise, you may get different results depending on hardware implementation or driver settings.</span></span>

### <a name="calculating-texel-positions"></a><span data-ttu-id="ce908-166">Cálculo de posiciones de textura</span><span class="sxs-lookup"><span data-stu-id="ce908-166">Calculating texel positions</span></span>

<span data-ttu-id="ce908-167">Las coordenadas de textura son valores de punto flotante que hacen referencia a los datos de textura, lo que también se conoce como espacio de textura normalizado.</span><span class="sxs-lookup"><span data-stu-id="ce908-167">Texture coordinates are floating-point values that reference texture data, which is also known as normalized texture space.</span></span> <span data-ttu-id="ce908-168">Los modos de ajuste de direcciones se aplican en este orden (coordenadas de textura + desplazamientos + modo de ajuste) para modificar las coordenadas de textura fuera del \[ intervalo 0...1. \]</span><span class="sxs-lookup"><span data-stu-id="ce908-168">Address wrapping modes are applied in this order (texture coordinates + offsets + wrap mode) to modify texture coordinates outside the \[0...1\] range.</span></span>

<span data-ttu-id="ce908-169">Para las matrices de textura, un valor adicional en el parámetro location especifica un índice en una matriz de texturas.</span><span class="sxs-lookup"><span data-stu-id="ce908-169">For texture arrays, an additional value in the location parameter specifies an index into a texture array.</span></span> <span data-ttu-id="ce908-170">Este índice se trata como un valor float escalado (en lugar del espacio normalizado para coordenadas de textura estándar).</span><span class="sxs-lookup"><span data-stu-id="ce908-170">This index is treated as a scaled float value (instead of the normalized space for standard texture coordinates).</span></span> <span data-ttu-id="ce908-171">La conversión a un índice entero se realiza en el orden siguiente (float + round-to-nearest-even integer + clamp to the array range).</span><span class="sxs-lookup"><span data-stu-id="ce908-171">The conversion to an integer index is done in the following order (float + round-to-nearest-even integer + clamp to the array range).</span></span>

### <a name="applying-texture-coordinate-offsets"></a><span data-ttu-id="ce908-172">Aplicar desplazamientos de coordenadas de textura</span><span class="sxs-lookup"><span data-stu-id="ce908-172">Applying texture coordinate offsets</span></span>

<span data-ttu-id="ce908-173">El parámetro offset modifica las coordenadas de textura, en el espacio de textura.</span><span class="sxs-lookup"><span data-stu-id="ce908-173">The offset parameter modifies the texture coordinates, in texel space.</span></span> <span data-ttu-id="ce908-174">Aunque las coordenadas de textura son números de punto flotante normalizados, el desplazamiento aplica un desplazamiento entero.</span><span class="sxs-lookup"><span data-stu-id="ce908-174">Even though texture coordinates are normalized floating-point numbers, the offset applies an integer offset.</span></span> <span data-ttu-id="ce908-175">Tenga en cuenta también que los desplazamientos de textura deben ser estáticos.</span><span class="sxs-lookup"><span data-stu-id="ce908-175">Also note that the texture offsets need to be static.</span></span>

<span data-ttu-id="ce908-176">El formato de datos devuelto viene determinado por el formato de textura.</span><span class="sxs-lookup"><span data-stu-id="ce908-176">The data format returned is determined by the texture format.</span></span> <span data-ttu-id="ce908-177">Por ejemplo, si el recurso de textura se definió con el formato DXGI FORMAT A8B8G8R8 UNORM SRGB, la operación de muestreo convierte los elementos de textura muestreados de \_ \_ gamma \_ 2.0 a 1.0, filtra y escribe el resultado como un valor de punto flotante en el \_ \[ intervalo 0..1. \]</span><span class="sxs-lookup"><span data-stu-id="ce908-177">For example, if the texture resource was defined with the DXGI\_FORMAT\_A8B8G8R8\_UNORM\_SRGB format, the sampling operation converts sampled texels from gamma 2.0 to 1.0, filter, and writes the result as a floating-point value in the range \[0..1\].</span></span>

## <a name="related-topics"></a><span data-ttu-id="ce908-178">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ce908-178">Related topics</span></span>

[<span data-ttu-id="ce908-179">Texture-Object</span><span class="sxs-lookup"><span data-stu-id="ce908-179">Texture-Object</span></span>](dx-graphics-hlsl-to-type.md)
