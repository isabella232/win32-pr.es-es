---
title: SampleLevel (objeto de textura de HLSL de DirectX)
description: Muestrea una textura mediante un desplazamiento de nivel de mipmap.
ms.assetid: d61426c8-e09f-4e88-99f6-fa96c4a2b58d
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 73cf7bc0c13987099540cecd49519de35b4b7de1
ms.sourcegitcommit: 0d6365d4e852b09a9100d9cfb9a5334922ebf478
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/17/2020
ms.locfileid: "104149748"
---
# <a name="samplelevel-directx-hlsl-texture-object"></a><span data-ttu-id="0fdfb-103">SampleLevel (objeto de textura de HLSL de DirectX)</span><span class="sxs-lookup"><span data-stu-id="0fdfb-103">SampleLevel (DirectX HLSL Texture Object)</span></span>

<span data-ttu-id="0fdfb-104">Muestrea una textura mediante un desplazamiento de nivel de mipmap.</span><span class="sxs-lookup"><span data-stu-id="0fdfb-104">Samples a texture using a mipmap-level offset.</span></span>



|                                                                                                  |
|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0fdfb-105">&lt;Tipo &gt; de plantilla Object. SampleLevel ( \_ Estado de muestra S, ubicación Float, Float LOD \[ , int offset \] );</span><span class="sxs-lookup"><span data-stu-id="0fdfb-105">&lt;Template Type&gt; Object.SampleLevel( sampler\_state S, float Location, float LOD \[, int Offset\] );</span></span> |



 

<span data-ttu-id="0fdfb-106">Esta función es similar a [Sample](dx-graphics-hlsl-to-sample.md) , salvo que usa el nivel LOD (en el último componente del parámetro Location) para elegir el nivel de mipmap.</span><span class="sxs-lookup"><span data-stu-id="0fdfb-106">This function is similar to [Sample](dx-graphics-hlsl-to-sample.md) except that it uses the LOD level (in the last component of the location parameter) to choose the mipmap level.</span></span> <span data-ttu-id="0fdfb-107">Por ejemplo, una textura 2D usa los dos primeros componentes para las coordenadas UV y el tercer componente para el nivel de mipmap.</span><span class="sxs-lookup"><span data-stu-id="0fdfb-107">For example, a 2D texture uses the first two components for uv coordinates and the third component for the mipmap level.</span></span>

## <a name="parameters"></a><span data-ttu-id="0fdfb-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0fdfb-108">Parameters</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0fdfb-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="0fdfb-109">Item</span></span></th>
<th><span data-ttu-id="0fdfb-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="0fdfb-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0fdfb-111"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Objeto</em></span><span class="sxs-lookup"><span data-stu-id="0fdfb-111"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Object</em></span></span><br/></td>
<td><span data-ttu-id="0fdfb-112">Cualquier tipo <a href="dx-graphics-hlsl-to-type.md">de objeto de textura</a> (excepto Texture2DMS y Texture2DMSArray).</span><span class="sxs-lookup"><span data-stu-id="0fdfb-112">Any <a href="dx-graphics-hlsl-to-type.md">texture-object</a> type (except Texture2DMS and Texture2DMSArray).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0fdfb-113"><span id="S"></span><span id="s"></span><em>Seg</em></span><span class="sxs-lookup"><span data-stu-id="0fdfb-113"><span id="S"></span><span id="s"></span><em>S</em></span></span><br/></td>
<td><span data-ttu-id="0fdfb-114">de Un <a href="dx-graphics-hlsl-sampler.md">Estado de muestra</a>.</span><span class="sxs-lookup"><span data-stu-id="0fdfb-114">[in] A <a href="dx-graphics-hlsl-sampler.md">Sampler state</a>.</span></span> <span data-ttu-id="0fdfb-115">Se trata de un objeto declarado en un archivo de efectos que contiene las asignaciones de estado.</span><span class="sxs-lookup"><span data-stu-id="0fdfb-115">This is an object declared in an effect file that contains state assignments.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0fdfb-116"><span id="Location"></span><span id="location"></span><span id="LOCATION"></span><em>Cód</em></span><span class="sxs-lookup"><span data-stu-id="0fdfb-116"><span id="Location"></span><span id="location"></span><span id="LOCATION"></span><em>Location</em></span></span><br/></td>
<td><span data-ttu-id="0fdfb-117">de Coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="0fdfb-117">[in] The texture coordinates.</span></span> <span data-ttu-id="0fdfb-118">El tipo de argumento depende del tipo de objeto de textura.</span><span class="sxs-lookup"><span data-stu-id="0fdfb-118">The argument type is dependent on the texture-object type.</span></span> <br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="0fdfb-119">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="0fdfb-119">Texture-Object Type</span></span></th>
<th><span data-ttu-id="0fdfb-120">Tipo de parámetro</span><span class="sxs-lookup"><span data-stu-id="0fdfb-120">Parameter Type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0fdfb-121">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0fdfb-121">Texture1D</span></span></td>
<td><span data-ttu-id="0fdfb-122">FLOAT</span><span class="sxs-lookup"><span data-stu-id="0fdfb-122">float</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0fdfb-123">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="0fdfb-123">Texture1DArray, Texture2D</span></span></td>
<td><span data-ttu-id="0fdfb-124">float2</span><span class="sxs-lookup"><span data-stu-id="0fdfb-124">float2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0fdfb-125">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="0fdfb-125">Texture2DArray, Texture3D, TextureCube</span></span></td>
<td><span data-ttu-id="0fdfb-126">float3</span><span class="sxs-lookup"><span data-stu-id="0fdfb-126">float3</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0fdfb-127">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="0fdfb-127">TextureCubeArray</span></span> </td>
<td><span data-ttu-id="0fdfb-128">float4</span><span class="sxs-lookup"><span data-stu-id="0fdfb-128">float4</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="0fdfb-129">Si el objeto Texture es una matriz, el último componente es el índice de la matriz.</span><span class="sxs-lookup"><span data-stu-id="0fdfb-129">If the texture object is an array, the last component is the array index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0fdfb-130"><span id="LOD"></span><span id="lod"></span><em>LOD</em></span><span class="sxs-lookup"><span data-stu-id="0fdfb-130"><span id="LOD"></span><span id="lod"></span><em>LOD</em></span></span></p></td>
<td><p><span data-ttu-id="0fdfb-131">de Número que especifica el nivel de mipmap.</span><span class="sxs-lookup"><span data-stu-id="0fdfb-131">[in] A number that specifies the mipmap level.</span></span> <span data-ttu-id="0fdfb-132">Si el valor es = 0, se usa zero'th (el mapa más grande).</span><span class="sxs-lookup"><span data-stu-id="0fdfb-132">If the value is = 0, the zero'th (biggest map) is used.</span></span> <span data-ttu-id="0fdfb-133">El valor fraccionario (si se proporciona) se usa para interpolar entre dos niveles de mipmap.</span><span class="sxs-lookup"><span data-stu-id="0fdfb-133">The fractional value (if supplied) is used to interpolate between two mipmap levels.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0fdfb-134"><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span><em>Posición</em></span><span class="sxs-lookup"><span data-stu-id="0fdfb-134"><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span><em>Offset</em></span></span></p></td>
<td><p><span data-ttu-id="0fdfb-135">de Desplazamiento de coordenadas de textura opcional, que se puede usar para cualquier tipo de objeto de textura. el desplazamiento se aplica a la ubicación antes del muestreo.</span><span class="sxs-lookup"><span data-stu-id="0fdfb-135">[in] An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="0fdfb-136">Los desplazamientos de textura deben ser estáticos.</span><span class="sxs-lookup"><span data-stu-id="0fdfb-136">The texture offsets need to be static.</span></span> <span data-ttu-id="0fdfb-137">El tipo de argumento depende del tipo de objeto de textura.</span><span class="sxs-lookup"><span data-stu-id="0fdfb-137">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="0fdfb-138">Para obtener más información, vea <a href="/windows/win32/direct3dhlsl/dx-graphics-hlsl-to-sample#applying-texture-coordinate-offsets">aplicar desplazamientos de coordenadas de textura</a>.</span><span class="sxs-lookup"><span data-stu-id="0fdfb-138">For more info, see <a href="/windows/win32/direct3dhlsl/dx-graphics-hlsl-to-sample#applying-texture-coordinate-offsets">Applying texture coordinate offsets</a>.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="0fdfb-139">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="0fdfb-139">Texture-Object Type</span></span></th>
<th><span data-ttu-id="0fdfb-140">Tipo de parámetro</span><span class="sxs-lookup"><span data-stu-id="0fdfb-140">Parameter Type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0fdfb-141">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="0fdfb-141">Texture1D, Texture1DArray</span></span></td>
<td><span data-ttu-id="0fdfb-142">int</span><span class="sxs-lookup"><span data-stu-id="0fdfb-142">int</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0fdfb-143">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="0fdfb-143">Texture2D, Texture2DArray</span></span></td>
<td><span data-ttu-id="0fdfb-144">int2</span><span class="sxs-lookup"><span data-stu-id="0fdfb-144">int2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0fdfb-145">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0fdfb-145">Texture3D</span></span></td>
<td><span data-ttu-id="0fdfb-146">int3</span><span class="sxs-lookup"><span data-stu-id="0fdfb-146">int3</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0fdfb-147">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="0fdfb-147">TextureCube, TextureCubeArray</span></span> </td>
<td><span data-ttu-id="0fdfb-148">no admitido</span><span class="sxs-lookup"><span data-stu-id="0fdfb-148">not supported</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="return-value"></a><span data-ttu-id="0fdfb-149">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0fdfb-149">Return Value</span></span>

<span data-ttu-id="0fdfb-150">Tipo de plantilla de la textura, que puede ser un vector de un solo componente o de varios componentes.</span><span class="sxs-lookup"><span data-stu-id="0fdfb-150">The texture's template type, which may be a single- or multi-component vector.</span></span> <span data-ttu-id="0fdfb-151">El formato se basa en el formato de [**DXGI \_**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)de la textura.</span><span class="sxs-lookup"><span data-stu-id="0fdfb-151">The format is based on the texture's [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="0fdfb-152">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="0fdfb-152">Minimum Shader Model</span></span>

<span data-ttu-id="0fdfb-153">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="0fdfb-153">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="0fdfb-154">vs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="0fdfb-154">vs\_4\_0</span></span> | <span data-ttu-id="0fdfb-155">vs \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="0fdfb-155">vs\_4\_1</span></span>  | <span data-ttu-id="0fdfb-156">PS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="0fdfb-156">ps\_4\_0</span></span> | <span data-ttu-id="0fdfb-157">PS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="0fdfb-157">ps\_4\_1</span></span>  | <span data-ttu-id="0fdfb-158">GS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="0fdfb-158">gs\_4\_0</span></span> | <span data-ttu-id="0fdfb-159">GS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="0fdfb-159">gs\_4\_1</span></span>  |
|----------|-----------|----------|-----------|----------|-----------|
| <span data-ttu-id="0fdfb-160">x</span><span class="sxs-lookup"><span data-stu-id="0fdfb-160">x</span></span>        | <span data-ttu-id="0fdfb-161">x</span><span class="sxs-lookup"><span data-stu-id="0fdfb-161">x</span></span>         | <span data-ttu-id="0fdfb-162">x</span><span class="sxs-lookup"><span data-stu-id="0fdfb-162">x</span></span>        | <span data-ttu-id="0fdfb-163">x</span><span class="sxs-lookup"><span data-stu-id="0fdfb-163">x</span></span>         | <span data-ttu-id="0fdfb-164">x</span><span class="sxs-lookup"><span data-stu-id="0fdfb-164">x</span></span>        | <span data-ttu-id="0fdfb-165">x</span><span class="sxs-lookup"><span data-stu-id="0fdfb-165">x</span></span>         |



 

1.  <span data-ttu-id="0fdfb-166">TextureCubeArray está disponible en el modelo de sombreador 4,1 o superior.</span><span class="sxs-lookup"><span data-stu-id="0fdfb-166">TextureCubeArray is available in Shader Model 4.1 or higher.</span></span>
2.  <span data-ttu-id="0fdfb-167">El modelo de sombreador 4,1 está disponible en Direct3D 10,1 o superior.</span><span class="sxs-lookup"><span data-stu-id="0fdfb-167">Shader Model 4.1 is available in Direct3D 10.1 or higher.</span></span>

## <a name="example"></a><span data-ttu-id="0fdfb-168">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="0fdfb-168">Example</span></span>

<span data-ttu-id="0fdfb-169">Este ejemplo de código parcial procede del archivo Instancing. FX en el [ejemplo Instancing10](https://msdn.microsoft.com/library/Ee416415(v=VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="0fdfb-169">This partial code example is from the Instancing.fx file in the [Instancing10 Sample](https://msdn.microsoft.com/library/Ee416415(v=VS.85).aspx).</span></span>


```
// Object Declarations
Texture1D g_txRandom;

SamplerState g_samPoint
{
    Filter = MIN_MAG_MIP_POINT;
    AddressU = Wrap;
    AddressV = Wrap;
};

    
// Shader body calling the intrinsic function
float3 RandomDir(float fOffset)
{   
    float tCoord = (fOffset) / 300.0;
    return g_txRandom.SampleLevel( g_samPoint, tCoord, 0 );
   ...

```



## <a name="related-topics"></a><span data-ttu-id="0fdfb-170">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0fdfb-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0fdfb-171">Texture-objeto</span><span class="sxs-lookup"><span data-stu-id="0fdfb-171">Texture-Object</span></span>](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

