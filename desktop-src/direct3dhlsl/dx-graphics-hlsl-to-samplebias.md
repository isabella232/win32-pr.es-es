---
title: SampleBias (objeto de textura HLSL de DirectX)
description: Muestrea una textura después de aplicar el sesgo de entrada al nivel de mapa mip.
ms.assetid: 1bc03ad8-7b69-4001-81c7-64d8c631d68d
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 01087ab36bdbe90ff73643899229c7ec6ccfbdbe
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/09/2021
ms.locfileid: "111826800"
---
# <a name="samplebias-directx-hlsl-texture-object"></a><span data-ttu-id="e5855-103">SampleBias (objeto de textura HLSL de DirectX)</span><span class="sxs-lookup"><span data-stu-id="e5855-103">SampleBias (DirectX HLSL Texture Object)</span></span>

<span data-ttu-id="e5855-104">Muestrea una textura después de aplicar el sesgo de entrada al nivel de mapa mip.</span><span class="sxs-lookup"><span data-stu-id="e5855-104">Samples a texture, after applying the input bias to the mipmap level.</span></span>

<span data-ttu-id="e5855-105">&lt;Template Type &gt; Object.SampleBias( sampler \_ state S, float Location, float Bias \[ , int Offset \] );</span><span class="sxs-lookup"><span data-stu-id="e5855-105">&lt;Template Type&gt; Object.SampleBias( sampler\_state S, float Location, float Bias \[, int Offset\] );</span></span>



 

## <a name="parameters"></a><span data-ttu-id="e5855-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e5855-106">Parameters</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e5855-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="e5855-107">Item</span></span></th>
<th><span data-ttu-id="e5855-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="e5855-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e5855-109"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Objeto</em></span><span class="sxs-lookup"><span data-stu-id="e5855-109"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Object</em></span></span><br/></td>
<td><span data-ttu-id="e5855-110">Cualquier <a href="dx-graphics-hlsl-to-type.md">tipo de objeto de</a> textura (excepto Texture2DMS y Texture2DMSArray).</span><span class="sxs-lookup"><span data-stu-id="e5855-110">Any <a href="dx-graphics-hlsl-to-type.md">texture-object</a> type (except Texture2DMS and Texture2DMSArray).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e5855-111"><span id="S"></span><span id="s"></span><em>S</em></span><span class="sxs-lookup"><span data-stu-id="e5855-111"><span id="S"></span><span id="s"></span><em>S</em></span></span><br/></td>
<td><span data-ttu-id="e5855-112">[in] Un <a href="dx-graphics-hlsl-sampler.md">estado sampler</a>.</span><span class="sxs-lookup"><span data-stu-id="e5855-112">[in] A <a href="dx-graphics-hlsl-sampler.md">Sampler state</a>.</span></span> <span data-ttu-id="e5855-113">Se trata de un objeto declarado en un archivo de efecto que contiene asignaciones de estado.</span><span class="sxs-lookup"><span data-stu-id="e5855-113">This is an object declared in an effect file that contains state assignments.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e5855-114"><span id="Location"></span><span id="location"></span><span id="LOCATION"></span><em>Ubicación</em></span><span class="sxs-lookup"><span data-stu-id="e5855-114"><span id="Location"></span><span id="location"></span><span id="LOCATION"></span><em>Location</em></span></span><br/></td>
<td><span data-ttu-id="e5855-115">[in] Coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="e5855-115">[in] The texture coordinates.</span></span> <span data-ttu-id="e5855-116">El tipo de argumento depende del tipo texture-object.</span><span class="sxs-lookup"><span data-stu-id="e5855-116">The argument type is dependent on the texture-object type.</span></span> <br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="e5855-117">Texture-Object type</span><span class="sxs-lookup"><span data-stu-id="e5855-117">Texture-Object Type</span></span></th>
<th><span data-ttu-id="e5855-118">Tipo de parámetro</span><span class="sxs-lookup"><span data-stu-id="e5855-118">Parameter Type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e5855-119">Texture1D</span><span class="sxs-lookup"><span data-stu-id="e5855-119">Texture1D</span></span></td>
<td><span data-ttu-id="e5855-120">FLOAT</span><span class="sxs-lookup"><span data-stu-id="e5855-120">float</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e5855-121">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="e5855-121">Texture1DArray, Texture2D</span></span></td>
<td><span data-ttu-id="e5855-122">float2</span><span class="sxs-lookup"><span data-stu-id="e5855-122">float2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e5855-123">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="e5855-123">Texture2DArray, Texture3D, TextureCube</span></span></td>
<td><span data-ttu-id="e5855-124">float3</span><span class="sxs-lookup"><span data-stu-id="e5855-124">float3</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e5855-125">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="e5855-125">TextureCubeArray</span></span> </td>
<td><span data-ttu-id="e5855-126">float4</span><span class="sxs-lookup"><span data-stu-id="e5855-126">float4</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e5855-127"><span id="Bias"></span><span id="bias"></span><span id="BIAS"></span><em>predisposición</em></span><span class="sxs-lookup"><span data-stu-id="e5855-127"><span id="Bias"></span><span id="bias"></span><span id="BIAS"></span><em>Bias</em></span></span></p></td>
<td><p><span data-ttu-id="e5855-128">[in] El valor de sesgo, que es un número de punto flotante entre -16,0 y 15,99, se aplica a un nivel de mip antes del muestreo.</span><span class="sxs-lookup"><span data-stu-id="e5855-128">[in] The bias value, which is a floating-point number between -16.0 and 15.99, is applied to a mip level before sampling.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e5855-129"><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span><em>Compensar</em></span><span class="sxs-lookup"><span data-stu-id="e5855-129"><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span><em>Offset</em></span></span></p></td>
<td><p><span data-ttu-id="e5855-130">[in] Desplazamiento de coordenadas de textura opcional, que se puede usar para cualquier tipo de objeto de textura; el desplazamiento se aplica a la ubicación antes del muestreo.</span><span class="sxs-lookup"><span data-stu-id="e5855-130">[in] An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="e5855-131">Los desplazamientos de textura deben ser estáticos.</span><span class="sxs-lookup"><span data-stu-id="e5855-131">The texture offsets need to be static.</span></span> <span data-ttu-id="e5855-132">El tipo de argumento depende del tipo texture-object.</span><span class="sxs-lookup"><span data-stu-id="e5855-132">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="e5855-133">Para obtener más información, vea <a href="/windows/win32/direct3dhlsl/dx-graphics-hlsl-to-sample#applying-texture-coordinate-offsets">Aplicar desplazamientos de coordenadas de textura.</a></span><span class="sxs-lookup"><span data-stu-id="e5855-133">For more info, see <a href="/windows/win32/direct3dhlsl/dx-graphics-hlsl-to-sample#applying-texture-coordinate-offsets">Applying texture coordinate offsets</a>.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="e5855-134">Texture-Object type</span><span class="sxs-lookup"><span data-stu-id="e5855-134">Texture-Object Type</span></span></th>
<th><span data-ttu-id="e5855-135">Tipo de parámetro</span><span class="sxs-lookup"><span data-stu-id="e5855-135">Parameter Type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e5855-136">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="e5855-136">Texture1D, Texture1DArray</span></span></td>
<td><span data-ttu-id="e5855-137">int</span><span class="sxs-lookup"><span data-stu-id="e5855-137">int</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e5855-138">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="e5855-138">Texture2D, Texture2DArray</span></span></td>
<td><span data-ttu-id="e5855-139">int2</span><span class="sxs-lookup"><span data-stu-id="e5855-139">int2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e5855-140">Texture3D</span><span class="sxs-lookup"><span data-stu-id="e5855-140">Texture3D</span></span></td>
<td><span data-ttu-id="e5855-141">int3</span><span class="sxs-lookup"><span data-stu-id="e5855-141">int3</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e5855-142">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="e5855-142">TextureCube, TextureCubeArray</span></span> </td>
<td><span data-ttu-id="e5855-143">no admitido</span><span class="sxs-lookup"><span data-stu-id="e5855-143">not supported</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="return-value"></a><span data-ttu-id="e5855-144">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e5855-144">Return Value</span></span>

<span data-ttu-id="e5855-145">El tipo de plantilla de la textura, que puede ser un vector de uno o varios componentes.</span><span class="sxs-lookup"><span data-stu-id="e5855-145">The texture's template type, which may be a single- or multi-component vector.</span></span> <span data-ttu-id="e5855-146">El formato se basa en EL [**FORMATO DXGI de la \_ textura.**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)</span><span class="sxs-lookup"><span data-stu-id="e5855-146">The format is based on the texture's [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="e5855-147">Modelo mínimo de sombreador</span><span class="sxs-lookup"><span data-stu-id="e5855-147">Minimum Shader Model</span></span>

<span data-ttu-id="e5855-148">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="e5855-148">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="e5855-149">vs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="e5855-149">vs\_4\_0</span></span> | <span data-ttu-id="e5855-150">vs \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="e5855-150">vs\_4\_1</span></span>  | <span data-ttu-id="e5855-151">ps \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="e5855-151">ps\_4\_0</span></span> | <span data-ttu-id="e5855-152">ps \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="e5855-152">ps\_4\_1</span></span>  | <span data-ttu-id="e5855-153">gs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="e5855-153">gs\_4\_0</span></span> | <span data-ttu-id="e5855-154">gs \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="e5855-154">gs\_4\_1</span></span>  |
|----------|-----------|----------|-----------|----------|-----------|
|          |           | <span data-ttu-id="e5855-155">x</span><span class="sxs-lookup"><span data-stu-id="e5855-155">x</span></span>        | <span data-ttu-id="e5855-156">x</span><span class="sxs-lookup"><span data-stu-id="e5855-156">x</span></span>         |          |           |



 

1.  <span data-ttu-id="e5855-157">TextureCubeArray está disponible en Shader Model 4.1 o superior.</span><span class="sxs-lookup"><span data-stu-id="e5855-157">TextureCubeArray is available in Shader Model 4.1 or higher.</span></span>
2.  <span data-ttu-id="e5855-158">El modelo de sombreador 4.1 está disponible en Direct3D 10.1 o posterior.</span><span class="sxs-lookup"><span data-stu-id="e5855-158">Shader Model 4.1 is available in Direct3D 10.1 or higher.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e5855-159">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e5855-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e5855-160">Texture-Object</span><span class="sxs-lookup"><span data-stu-id="e5855-160">Texture-Object</span></span>](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

