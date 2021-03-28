---
title: SampleGrad (objeto de textura de HLSL de DirectX)
description: Muestrea una textura mediante un degradado para influir en la forma en que se calcula la ubicación de ejemplo. | SampleGrad (objeto de textura de HLSL de DirectX)
ms.assetid: f3d73296-23c4-4178-b89e-6f84cfcb48a5
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 236c453f3636452cbba8ed6000b2416e5187898d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104279986"
---
# <a name="samplegrad-directx-hlsl-texture-object"></a><span data-ttu-id="ec267-104">SampleGrad (objeto de textura de HLSL de DirectX)</span><span class="sxs-lookup"><span data-stu-id="ec267-104">SampleGrad (DirectX HLSL Texture Object)</span></span>

<span data-ttu-id="ec267-105">Muestrea una textura mediante un degradado para influir en la forma en que se calcula la ubicación de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="ec267-105">Samples a texture using a gradient to influence the way the sample location is calculated.</span></span>



|                                                                                                            |
|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec267-106">&lt;Tipo &gt; de plantilla Object. SampleGrad ( \_ Estado de muestra S, ubicación Float, Float DDX, Float DDY \[ , int offset \] );</span><span class="sxs-lookup"><span data-stu-id="ec267-106">&lt;Template Type&gt; Object.SampleGrad( sampler\_state S, float Location, float DDX, float DDY \[, int Offset\] );</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="ec267-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ec267-107">Parameters</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ec267-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="ec267-108">Item</span></span></th>
<th><span data-ttu-id="ec267-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="ec267-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ec267-110"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Objeto</em></span><span class="sxs-lookup"><span data-stu-id="ec267-110"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Object</em></span></span><br/></td>
<td><span data-ttu-id="ec267-111">Cualquier tipo <a href="dx-graphics-hlsl-to-type.md">de objeto de textura</a> (excepto Texture2DMS y Texture2DMSArray).</span><span class="sxs-lookup"><span data-stu-id="ec267-111">Any <a href="dx-graphics-hlsl-to-type.md">texture-object</a> type (except Texture2DMS and Texture2DMSArray).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ec267-112"><span id="S"></span><span id="s"></span><em>Seg</em></span><span class="sxs-lookup"><span data-stu-id="ec267-112"><span id="S"></span><span id="s"></span><em>S</em></span></span><br/></td>
<td><span data-ttu-id="ec267-113">de Un <a href="dx-graphics-hlsl-sampler.md">Estado de muestra</a>.</span><span class="sxs-lookup"><span data-stu-id="ec267-113">[in] A <a href="dx-graphics-hlsl-sampler.md">Sampler state</a>.</span></span> <span data-ttu-id="ec267-114">Se trata de un objeto declarado en un archivo de efectos que contiene las asignaciones de estado.</span><span class="sxs-lookup"><span data-stu-id="ec267-114">This is an object declared in an effect file that contains state assignments.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ec267-115"><span id="Location"></span><span id="location"></span><span id="LOCATION"></span><em>Cód</em></span><span class="sxs-lookup"><span data-stu-id="ec267-115"><span id="Location"></span><span id="location"></span><span id="LOCATION"></span><em>Location</em></span></span><br/></td>
<td><span data-ttu-id="ec267-116">de Coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="ec267-116">[in] The Texture coordinates.</span></span> <span data-ttu-id="ec267-117">El tipo de argumento depende del tipo de objeto de textura.</span><span class="sxs-lookup"><span data-stu-id="ec267-117">The argument type is dependent on the texture-object type.</span></span> <br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="ec267-118">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="ec267-118">Texture-Object Type</span></span></th>
<th><span data-ttu-id="ec267-119">Tipo de parámetro</span><span class="sxs-lookup"><span data-stu-id="ec267-119">Parameter Type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ec267-120">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ec267-120">Texture1D</span></span></td>
<td><span data-ttu-id="ec267-121">FLOAT</span><span class="sxs-lookup"><span data-stu-id="ec267-121">float</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ec267-122">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="ec267-122">Texture1DArray, Texture2D</span></span></td>
<td><span data-ttu-id="ec267-123">float2</span><span class="sxs-lookup"><span data-stu-id="ec267-123">float2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ec267-124">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="ec267-124">Texture2DArray, Texture3D, TextureCube</span></span></td>
<td><span data-ttu-id="ec267-125">float3</span><span class="sxs-lookup"><span data-stu-id="ec267-125">float3</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ec267-126">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="ec267-126">TextureCubeArray</span></span> </td>
<td><span data-ttu-id="ec267-127">float4</span><span class="sxs-lookup"><span data-stu-id="ec267-127">float4</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ec267-128">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="ec267-128">Texture2DMS, Texture2DMSArray</span></span></td>
<td><span data-ttu-id="ec267-129">no admitido</span><span class="sxs-lookup"><span data-stu-id="ec267-129">not supported</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec267-130"><span id="DDX"></span><span id="ddx"></span><em>DDX</em></span><span class="sxs-lookup"><span data-stu-id="ec267-130"><span id="DDX"></span><span id="ddx"></span><em>DDX</em></span></span></p></td>
<td><p><span data-ttu-id="ec267-131">de La tasa de cambio de la geometría de la superficie en la dirección x.</span><span class="sxs-lookup"><span data-stu-id="ec267-131">[in] The rate of change of the surface geometry in the x direction.</span></span> <span data-ttu-id="ec267-132">El tipo de argumento depende del tipo de objeto de textura.</span><span class="sxs-lookup"><span data-stu-id="ec267-132">The argument type is dependent on the texture-object type.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="ec267-133">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="ec267-133">Texture-Object Type</span></span></th>
<th><span data-ttu-id="ec267-134">Tipo de parámetro</span><span class="sxs-lookup"><span data-stu-id="ec267-134">Parameter Type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ec267-135">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="ec267-135">Texture1D, Texture1DArray</span></span></td>
<td><span data-ttu-id="ec267-136">FLOAT</span><span class="sxs-lookup"><span data-stu-id="ec267-136">float</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ec267-137">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="ec267-137">Texture2D, Texture2DArray</span></span></td>
<td><span data-ttu-id="ec267-138">float2</span><span class="sxs-lookup"><span data-stu-id="ec267-138">float2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ec267-139">Texture3D, TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="ec267-139">Texture3D, TextureCube, TextureCubeArray</span></span> </td>
<td><span data-ttu-id="ec267-140">float3</span><span class="sxs-lookup"><span data-stu-id="ec267-140">float3</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ec267-141">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="ec267-141">Texture2DMS, Texture2DMSArray</span></span></td>
<td><span data-ttu-id="ec267-142">no admitido</span><span class="sxs-lookup"><span data-stu-id="ec267-142">not supported</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec267-143"><span id="DDY"></span><span id="ddy"></span><em>DDY</em></span><span class="sxs-lookup"><span data-stu-id="ec267-143"><span id="DDY"></span><span id="ddy"></span><em>DDY</em></span></span></p></td>
<td><p><span data-ttu-id="ec267-144">de La tasa de cambio de la geometría de la superficie en la dirección y.</span><span class="sxs-lookup"><span data-stu-id="ec267-144">[in] The rate of change of the surface geometry in the y direction.</span></span> <span data-ttu-id="ec267-145">El tipo de argumento depende del tipo de objeto de textura.</span><span class="sxs-lookup"><span data-stu-id="ec267-145">The argument type is dependent on the texture-object type.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="ec267-146">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="ec267-146">Texture-Object Type</span></span></th>
<th><span data-ttu-id="ec267-147">Tipo de parámetro</span><span class="sxs-lookup"><span data-stu-id="ec267-147">Parameter Type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ec267-148">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="ec267-148">Texture1D, Texture1DArray</span></span></td>
<td><span data-ttu-id="ec267-149">FLOAT</span><span class="sxs-lookup"><span data-stu-id="ec267-149">float</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ec267-150">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="ec267-150">Texture2D, Texture2DArray</span></span></td>
<td><span data-ttu-id="ec267-151">float2</span><span class="sxs-lookup"><span data-stu-id="ec267-151">float2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ec267-152">Texture3D, TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="ec267-152">Texture3D, TextureCube, TextureCubeArray</span></span> </td>
<td><span data-ttu-id="ec267-153">float3</span><span class="sxs-lookup"><span data-stu-id="ec267-153">float3</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ec267-154">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="ec267-154">Texture2DMS, Texture2DMSArray</span></span></td>
<td><span data-ttu-id="ec267-155">no admitido</span><span class="sxs-lookup"><span data-stu-id="ec267-155">not supported</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec267-156"><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span><em>Posición</em></span><span class="sxs-lookup"><span data-stu-id="ec267-156"><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span><em>Offset</em></span></span></p></td>
<td><p><span data-ttu-id="ec267-157">de Desplazamiento de coordenadas de textura opcional, que se puede usar para cualquier tipo de objeto de textura.</span><span class="sxs-lookup"><span data-stu-id="ec267-157">[in] An optional texture coordinate offset, which can be used for any texture-object types.</span></span> <span data-ttu-id="ec267-158">El desplazamiento se aplica a la ubicación antes del muestreo.</span><span class="sxs-lookup"><span data-stu-id="ec267-158">The offset is applied to the location before sampling.</span></span> <span data-ttu-id="ec267-159">Use un desplazamiento solo en un entero miplevel; de lo contrario, puede obtener resultados que no se traduzcan bien al hardware.</span><span class="sxs-lookup"><span data-stu-id="ec267-159">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="ec267-160">El tipo de argumento depende del tipo de objeto de textura.</span><span class="sxs-lookup"><span data-stu-id="ec267-160">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="ec267-161">Para obtener más información, vea<a href="dx-graphics-hlsl-to-sample.md">aplicar desplazamientos enteros</a>.</span><span class="sxs-lookup"><span data-stu-id="ec267-161">For more info, see<a href="dx-graphics-hlsl-to-sample.md">Applying Integer Offsets</a>.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="ec267-162">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="ec267-162">Texture-Object Type</span></span></th>
<th><span data-ttu-id="ec267-163">Tipo de parámetro</span><span class="sxs-lookup"><span data-stu-id="ec267-163">Parameter Type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ec267-164">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="ec267-164">Texture1D, Texture1DArray</span></span></td>
<td><span data-ttu-id="ec267-165">int</span><span class="sxs-lookup"><span data-stu-id="ec267-165">int</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ec267-166">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="ec267-166">Texture2D, Texture2DArray</span></span></td>
<td><span data-ttu-id="ec267-167">int2</span><span class="sxs-lookup"><span data-stu-id="ec267-167">int2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ec267-168">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ec267-168">Texture3D</span></span></td>
<td><span data-ttu-id="ec267-169">int3</span><span class="sxs-lookup"><span data-stu-id="ec267-169">int3</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ec267-170">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="ec267-170">TextureCube, TextureCubeArray</span></span> </td>
<td><span data-ttu-id="ec267-171">no admitido</span><span class="sxs-lookup"><span data-stu-id="ec267-171">not supported</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ec267-172">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="ec267-172">Texture2DMS, Texture2DMSArray</span></span></td>
<td><span data-ttu-id="ec267-173">no admitido</span><span class="sxs-lookup"><span data-stu-id="ec267-173">not supported</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="return-value"></a><span data-ttu-id="ec267-174">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ec267-174">Return Value</span></span>

<span data-ttu-id="ec267-175">Tipo de plantilla de la textura, que puede ser un vector de un solo componente o de varios componentes.</span><span class="sxs-lookup"><span data-stu-id="ec267-175">The texture's template type, which may be a single- or multi-component vector.</span></span> <span data-ttu-id="ec267-176">El formato se basa en el formato de [**DXGI \_**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)de la textura.</span><span class="sxs-lookup"><span data-stu-id="ec267-176">The format is based on the texture's [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="ec267-177">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="ec267-177">Minimum Shader Model</span></span>

<span data-ttu-id="ec267-178">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="ec267-178">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="ec267-179">vs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="ec267-179">vs\_4\_0</span></span> | <span data-ttu-id="ec267-180">vs \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="ec267-180">vs\_4\_1</span></span>  | <span data-ttu-id="ec267-181">PS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="ec267-181">ps\_4\_0</span></span> | <span data-ttu-id="ec267-182">PS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="ec267-182">ps\_4\_1</span></span>  | <span data-ttu-id="ec267-183">GS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="ec267-183">gs\_4\_0</span></span> | <span data-ttu-id="ec267-184">GS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="ec267-184">gs\_4\_1</span></span>  |
|----------|-----------|----------|-----------|----------|-----------|
| <span data-ttu-id="ec267-185">x</span><span class="sxs-lookup"><span data-stu-id="ec267-185">x</span></span>        | <span data-ttu-id="ec267-186">x</span><span class="sxs-lookup"><span data-stu-id="ec267-186">x</span></span>         | <span data-ttu-id="ec267-187">x</span><span class="sxs-lookup"><span data-stu-id="ec267-187">x</span></span>        | <span data-ttu-id="ec267-188">x</span><span class="sxs-lookup"><span data-stu-id="ec267-188">x</span></span>         | <span data-ttu-id="ec267-189">x</span><span class="sxs-lookup"><span data-stu-id="ec267-189">x</span></span>        | <span data-ttu-id="ec267-190">x</span><span class="sxs-lookup"><span data-stu-id="ec267-190">x</span></span>         |



 

1.  <span data-ttu-id="ec267-191">TextureCubeArray está disponible en el modelo de sombreador 4,1 o superior.</span><span class="sxs-lookup"><span data-stu-id="ec267-191">TextureCubeArray is available in Shader Model 4.1 or higher.</span></span>
2.  <span data-ttu-id="ec267-192">El modelo de sombreador 4,1 está disponible en Direct3D 10,1 o superior.</span><span class="sxs-lookup"><span data-stu-id="ec267-192">Shader Model 4.1 is available in Direct3D 10.1 or higher.</span></span>

## <a name="example"></a><span data-ttu-id="ec267-193">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ec267-193">Example</span></span>

<span data-ttu-id="ec267-194">Este ejemplo de código parcial procede del archivo MotionBlur. FX en el [ejemplo MotionBlur10](https://msdn.microsoft.com/library/Ee416417(v=VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="ec267-194">This partial code example is from the MotionBlur.fx file in the [MotionBlur10 Sample](https://msdn.microsoft.com/library/Ee416417(v=VS.85).aspx).</span></span>


```
// Object Declarations
Texture2D g_txDiffuse;

SamplerState g_samLinear
{
    Filter = ANISOTROPIC;
    MaxAnisotropy = 8;
    AddressU = Wrap;
    AddressV = Wrap;
};

struct VSSceneOut
{
    float4 Pos : SV_POSITION;
    float4 Color : COLOR0;
    float2 Tex : TEXCOORD;
    float2 Aniso : ANISOTROPY;
};

float4 PSSceneMain( VSSceneOut Input ) : SV_TARGET
{
    float2 ddx = Input.Aniso;
    float2 ddy = Input.Aniso;
    
    // Shader body calling the intrinsic function
    float4 diff = g_txDiffuse.SampleGrad( g_samLinear, Input.Tex, ddx, ddy);
    
    ...
}
```



## <a name="related-topics"></a><span data-ttu-id="ec267-195">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ec267-195">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ec267-196">Texture-objeto</span><span class="sxs-lookup"><span data-stu-id="ec267-196">Texture-Object</span></span>](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

