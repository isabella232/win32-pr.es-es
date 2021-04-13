---
title: SampleBias (objeto de textura de HLSL de DirectX)
description: Muestrea una textura, después de aplicar la diferencia de entrada al nivel de mipmap.
ms.assetid: 1bc03ad8-7b69-4001-81c7-64d8c631d68d
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e710b8a6c7dd2983c6d0c635d16356f95d0b4fe7
ms.sourcegitcommit: 0d6365d4e852b09a9100d9cfb9a5334922ebf478
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/17/2020
ms.locfileid: "104421684"
---
# <a name="samplebias-directx-hlsl-texture-object"></a><span data-ttu-id="7bace-103">SampleBias (objeto de textura de HLSL de DirectX)</span><span class="sxs-lookup"><span data-stu-id="7bace-103">SampleBias (DirectX HLSL Texture Object)</span></span>

<span data-ttu-id="7bace-104">Muestrea una textura, después de aplicar la diferencia de entrada al nivel de mipmap.</span><span class="sxs-lookup"><span data-stu-id="7bace-104">Samples a texture, after applying the input bias to the mipmap level.</span></span>



|                                                                                                  |
|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7bace-105">&lt;Tipo &gt; de plantilla Object. SampleBias ( \_ Estado de muestra S, ubicación Float, inclinación Float \[ , desplazamiento int \] );</span><span class="sxs-lookup"><span data-stu-id="7bace-105">&lt;Template Type&gt; Object.SampleBias( sampler\_state S, float Location, float Bias \[, int Offset\] );</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="7bace-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7bace-106">Parameters</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7bace-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="7bace-107">Item</span></span></th>
<th><span data-ttu-id="7bace-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="7bace-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7bace-109"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Objeto</em></span><span class="sxs-lookup"><span data-stu-id="7bace-109"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Object</em></span></span><br/></td>
<td><span data-ttu-id="7bace-110">Cualquier tipo <a href="dx-graphics-hlsl-to-type.md">de objeto de textura</a> (excepto Texture2DMS y Texture2DMSArray).</span><span class="sxs-lookup"><span data-stu-id="7bace-110">Any <a href="dx-graphics-hlsl-to-type.md">texture-object</a> type (except Texture2DMS and Texture2DMSArray).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7bace-111"><span id="S"></span><span id="s"></span><em>Seg</em></span><span class="sxs-lookup"><span data-stu-id="7bace-111"><span id="S"></span><span id="s"></span><em>S</em></span></span><br/></td>
<td><span data-ttu-id="7bace-112">de Un <a href="dx-graphics-hlsl-sampler.md">Estado de muestra</a>.</span><span class="sxs-lookup"><span data-stu-id="7bace-112">[in] A <a href="dx-graphics-hlsl-sampler.md">Sampler state</a>.</span></span> <span data-ttu-id="7bace-113">Se trata de un objeto declarado en un archivo de efectos que contiene las asignaciones de estado.</span><span class="sxs-lookup"><span data-stu-id="7bace-113">This is an object declared in an effect file that contains state assignments.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7bace-114"><span id="Location"></span><span id="location"></span><span id="LOCATION"></span><em>Cód</em></span><span class="sxs-lookup"><span data-stu-id="7bace-114"><span id="Location"></span><span id="location"></span><span id="LOCATION"></span><em>Location</em></span></span><br/></td>
<td><span data-ttu-id="7bace-115">de Coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="7bace-115">[in] The texture coordinates.</span></span> <span data-ttu-id="7bace-116">El tipo de argumento depende del tipo de objeto de textura.</span><span class="sxs-lookup"><span data-stu-id="7bace-116">The argument type is dependent on the texture-object type.</span></span> <br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="7bace-117">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="7bace-117">Texture-Object Type</span></span></th>
<th><span data-ttu-id="7bace-118">Tipo de parámetro</span><span class="sxs-lookup"><span data-stu-id="7bace-118">Parameter Type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7bace-119">Texture1D</span><span class="sxs-lookup"><span data-stu-id="7bace-119">Texture1D</span></span></td>
<td><span data-ttu-id="7bace-120">FLOAT</span><span class="sxs-lookup"><span data-stu-id="7bace-120">float</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7bace-121">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="7bace-121">Texture1DArray, Texture2D</span></span></td>
<td><span data-ttu-id="7bace-122">float2</span><span class="sxs-lookup"><span data-stu-id="7bace-122">float2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7bace-123">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="7bace-123">Texture2DArray, Texture3D, TextureCube</span></span></td>
<td><span data-ttu-id="7bace-124">float3</span><span class="sxs-lookup"><span data-stu-id="7bace-124">float3</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7bace-125">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="7bace-125">TextureCubeArray</span></span> </td>
<td><span data-ttu-id="7bace-126">float4</span><span class="sxs-lookup"><span data-stu-id="7bace-126">float4</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7bace-127"><span id="Bias"></span><span id="bias"></span><span id="BIAS"></span><em>Parcial</em></span><span class="sxs-lookup"><span data-stu-id="7bace-127"><span id="Bias"></span><span id="bias"></span><span id="BIAS"></span><em>Bias</em></span></span></p></td>
<td><p><span data-ttu-id="7bace-128">de El valor de diferencia, que es un número de punto flotante entre-16,0 y 15,99, se aplica a un nivel de MIP antes del muestreo.</span><span class="sxs-lookup"><span data-stu-id="7bace-128">[in] The bias value, which is a floating-point number between -16.0 and 15.99, is applied to a mip level before sampling.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7bace-129"><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span><em>Posición</em></span><span class="sxs-lookup"><span data-stu-id="7bace-129"><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span><em>Offset</em></span></span></p></td>
<td><p><span data-ttu-id="7bace-130">de Desplazamiento de coordenadas de textura opcional, que se puede usar para cualquier tipo de objeto de textura. el desplazamiento se aplica a la ubicación antes del muestreo.</span><span class="sxs-lookup"><span data-stu-id="7bace-130">[in] An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="7bace-131">Los desplazamientos de textura deben ser estáticos.</span><span class="sxs-lookup"><span data-stu-id="7bace-131">The texture offsets need to be static.</span></span> <span data-ttu-id="7bace-132">El tipo de argumento depende del tipo de objeto de textura.</span><span class="sxs-lookup"><span data-stu-id="7bace-132">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="7bace-133">Para obtener más información, vea <a href="/windows/win32/direct3dhlsl/dx-graphics-hlsl-to-sample#applying-texture-coordinate-offsets">aplicar desplazamientos de coordenadas de textura</a>.</span><span class="sxs-lookup"><span data-stu-id="7bace-133">For more info, see <a href="/windows/win32/direct3dhlsl/dx-graphics-hlsl-to-sample#applying-texture-coordinate-offsets">Applying texture coordinate offsets</a>.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="7bace-134">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="7bace-134">Texture-Object Type</span></span></th>
<th><span data-ttu-id="7bace-135">Tipo de parámetro</span><span class="sxs-lookup"><span data-stu-id="7bace-135">Parameter Type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7bace-136">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="7bace-136">Texture1D, Texture1DArray</span></span></td>
<td><span data-ttu-id="7bace-137">int</span><span class="sxs-lookup"><span data-stu-id="7bace-137">int</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7bace-138">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="7bace-138">Texture2D, Texture2DArray</span></span></td>
<td><span data-ttu-id="7bace-139">int2</span><span class="sxs-lookup"><span data-stu-id="7bace-139">int2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7bace-140">Texture3D</span><span class="sxs-lookup"><span data-stu-id="7bace-140">Texture3D</span></span></td>
<td><span data-ttu-id="7bace-141">int3</span><span class="sxs-lookup"><span data-stu-id="7bace-141">int3</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7bace-142">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="7bace-142">TextureCube, TextureCubeArray</span></span> </td>
<td><span data-ttu-id="7bace-143">no admitido</span><span class="sxs-lookup"><span data-stu-id="7bace-143">not supported</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="return-value"></a><span data-ttu-id="7bace-144">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7bace-144">Return Value</span></span>

<span data-ttu-id="7bace-145">Tipo de plantilla de la textura, que puede ser un vector de un solo componente o de varios componentes.</span><span class="sxs-lookup"><span data-stu-id="7bace-145">The texture's template type, which may be a single- or multi-component vector.</span></span> <span data-ttu-id="7bace-146">El formato se basa en el formato de [**DXGI \_**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)de la textura.</span><span class="sxs-lookup"><span data-stu-id="7bace-146">The format is based on the texture's [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="7bace-147">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="7bace-147">Minimum Shader Model</span></span>

<span data-ttu-id="7bace-148">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="7bace-148">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="7bace-149">vs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="7bace-149">vs\_4\_0</span></span> | <span data-ttu-id="7bace-150">vs \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="7bace-150">vs\_4\_1</span></span>  | <span data-ttu-id="7bace-151">PS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="7bace-151">ps\_4\_0</span></span> | <span data-ttu-id="7bace-152">PS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="7bace-152">ps\_4\_1</span></span>  | <span data-ttu-id="7bace-153">GS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="7bace-153">gs\_4\_0</span></span> | <span data-ttu-id="7bace-154">GS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="7bace-154">gs\_4\_1</span></span>  |
|----------|-----------|----------|-----------|----------|-----------|
|          |           | <span data-ttu-id="7bace-155">x</span><span class="sxs-lookup"><span data-stu-id="7bace-155">x</span></span>        | <span data-ttu-id="7bace-156">x</span><span class="sxs-lookup"><span data-stu-id="7bace-156">x</span></span>         |          |           |



 

1.  <span data-ttu-id="7bace-157">TextureCubeArray está disponible en el modelo de sombreador 4,1 o superior.</span><span class="sxs-lookup"><span data-stu-id="7bace-157">TextureCubeArray is available in Shader Model 4.1 or higher.</span></span>
2.  <span data-ttu-id="7bace-158">El modelo de sombreador 4,1 está disponible en Direct3D 10,1 o superior.</span><span class="sxs-lookup"><span data-stu-id="7bace-158">Shader Model 4.1 is available in Direct3D 10.1 or higher.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7bace-159">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7bace-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7bace-160">Texture-objeto</span><span class="sxs-lookup"><span data-stu-id="7bace-160">Texture-Object</span></span>](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

