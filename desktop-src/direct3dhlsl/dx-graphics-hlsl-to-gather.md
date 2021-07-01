---
title: Recopilar (objeto de textura HLSL de DirectX)
description: Obtiene las cuatro muestras (solo componente rojo) que se usarían para la interpolación bilineal al muestrear una textura.
ms.assetid: a394d8c2-99cc-4a38-9ac9-34afc666ebe0
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4659ba19e9fa950a659969f2491533858f4658fb
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120550"
---
# <a name="gather-directx-hlsl-texture-object"></a><span data-ttu-id="398ab-103">Recopilar (objeto de textura HLSL de DirectX)</span><span class="sxs-lookup"><span data-stu-id="398ab-103">Gather (DirectX HLSL Texture Object)</span></span>

<span data-ttu-id="398ab-104">Obtiene las cuatro muestras (solo componente rojo) que se usarían para la interpolación bilineal al muestrear una textura.</span><span class="sxs-lookup"><span data-stu-id="398ab-104">Gets the four samples (red component only) that would be used for bilinear interpolation when sampling a texture.</span></span>

<span data-ttu-id="398ab-105">&lt;Template Type &gt; 4 Object.Gather( sampler \_ state S, float2 \| 3 \| 4 Location \[ , int2 Offset \] );</span><span class="sxs-lookup"><span data-stu-id="398ab-105">&lt;Template Type&gt;4 Object.Gather( sampler\_state S, float2\|3\|4 Location \[, int2 Offset\] );</span></span>



 

## <a name="parameters"></a><span data-ttu-id="398ab-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="398ab-106">Parameters</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="398ab-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="398ab-107">Item</span></span></th>
<th><span data-ttu-id="398ab-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="398ab-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="398ab-109"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Objeto</em></span><span class="sxs-lookup"><span data-stu-id="398ab-109"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Object</em></span></span><br/></td>
<td><span data-ttu-id="398ab-110">Se <a href="dx-graphics-hlsl-to-type.md">admiten los siguientes</a> tipos de objeto de textura: Texture2D, Texture2DArray, TextureCube, TextureCubeArray.</span><span class="sxs-lookup"><span data-stu-id="398ab-110">The following <a href="dx-graphics-hlsl-to-type.md">texture-object</a> types are supported: Texture2D, Texture2DArray, TextureCube, TextureCubeArray.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="398ab-111"><span id="S"></span><span id="s"></span><em>S</em></span><span class="sxs-lookup"><span data-stu-id="398ab-111"><span id="S"></span><span id="s"></span><em>S</em></span></span><br/></td>
<td><span data-ttu-id="398ab-112">[in] Un <a href="dx-graphics-hlsl-sampler.md">estado sampler</a>.</span><span class="sxs-lookup"><span data-stu-id="398ab-112">[in] A <a href="dx-graphics-hlsl-sampler.md">Sampler state</a>.</span></span> <span data-ttu-id="398ab-113">Se trata de un objeto declarado en un archivo de efecto que contiene asignaciones de estado.</span><span class="sxs-lookup"><span data-stu-id="398ab-113">This is an object declared in an effect file that contains state assignments.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="398ab-114"><span id="Location"></span><span id="location"></span><span id="LOCATION"></span><em>Ubicación</em></span><span class="sxs-lookup"><span data-stu-id="398ab-114"><span id="Location"></span><span id="location"></span><span id="LOCATION"></span><em>Location</em></span></span><br/></td>
<td><span data-ttu-id="398ab-115">[in] Coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="398ab-115">[in] The texture coordinates.</span></span> <span data-ttu-id="398ab-116">El tipo de argumento depende del tipo texture-object.</span><span class="sxs-lookup"><span data-stu-id="398ab-116">The argument type is dependent on the texture-object type.</span></span> <br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="398ab-117">Texture-Object type</span><span class="sxs-lookup"><span data-stu-id="398ab-117">Texture-Object Type</span></span></th>
<th><span data-ttu-id="398ab-118">Tipo de parámetro</span><span class="sxs-lookup"><span data-stu-id="398ab-118">Parameter Type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="398ab-119">Texture2D</span><span class="sxs-lookup"><span data-stu-id="398ab-119">Texture2D</span></span></td>
<td><span data-ttu-id="398ab-120">float2</span><span class="sxs-lookup"><span data-stu-id="398ab-120">float2</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="398ab-121">Texture2DArray, TextureCube</span><span class="sxs-lookup"><span data-stu-id="398ab-121">Texture2DArray, TextureCube</span></span></td>
<td><span data-ttu-id="398ab-122">float3</span><span class="sxs-lookup"><span data-stu-id="398ab-122">float3</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="398ab-123">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="398ab-123">TextureCubeArray</span></span> </td>
<td><span data-ttu-id="398ab-124">float4</span><span class="sxs-lookup"><span data-stu-id="398ab-124">float4</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="398ab-125"><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span><em>Compensar</em></span><span class="sxs-lookup"><span data-stu-id="398ab-125"><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span><em>Offset</em></span></span></p></td>
<td><p><span data-ttu-id="398ab-126">[in] Desplazamiento de coordenadas de textura opcional, que se puede usar para cualquier tipo de objeto de textura; el desplazamiento se aplica a la ubicación antes del muestreo.</span><span class="sxs-lookup"><span data-stu-id="398ab-126">[in] An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="398ab-127">El tipo de argumento depende del tipo texture-object.</span><span class="sxs-lookup"><span data-stu-id="398ab-127">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="398ab-128">En el caso de los sombreadores que tienen como destino Shader Model 5.0 y superiores, los 6 bits menos significativos de cada valor de desplazamiento se respetan como un valor con firma, lo que produce el intervalo [-32..31].</span><span class="sxs-lookup"><span data-stu-id="398ab-128">For shaders targeting Shader Model 5.0 and above, the 6 least significant bits of each offset value is honored as a signed value, yielding [-32..31] range.</span></span> <span data-ttu-id="398ab-129">Para los sombreadores de modelos de sombreador anteriores, los desplazamientos deben ser enteros inmediatos entre -8 y 7.</span><span class="sxs-lookup"><span data-stu-id="398ab-129">For previous shader model shaders, offsets need to be immediate integers between -8 and 7.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="398ab-130">Texture-Object type</span><span class="sxs-lookup"><span data-stu-id="398ab-130">Texture-Object Type</span></span></th>
<th><span data-ttu-id="398ab-131">Tipo de parámetro</span><span class="sxs-lookup"><span data-stu-id="398ab-131">Parameter Type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="398ab-132">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="398ab-132">Texture2D, Texture2DArray</span></span></td>
<td><span data-ttu-id="398ab-133">int2</span><span class="sxs-lookup"><span data-stu-id="398ab-133">int2</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="398ab-134">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="398ab-134">TextureCube, TextureCubeArray</span></span> </td>
<td><span data-ttu-id="398ab-135">no admitido</span><span class="sxs-lookup"><span data-stu-id="398ab-135">not supported</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="return-value"></a><span data-ttu-id="398ab-136">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="398ab-136">Return Value</span></span>

<span data-ttu-id="398ab-137">Vector de cuatro componentes, con cuatro componentes de datos rojos, cuyo tipo es el mismo que el tipo de plantilla de la textura.</span><span class="sxs-lookup"><span data-stu-id="398ab-137">A four-component vector, with four components of red data, whose type is the same as the texture's template type.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="398ab-138">Modelo mínimo de sombreador</span><span class="sxs-lookup"><span data-stu-id="398ab-138">Minimum Shader Model</span></span>

<span data-ttu-id="398ab-139">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="398ab-139">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="398ab-140">vs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="398ab-140">vs\_4\_0</span></span> | <span data-ttu-id="398ab-141">vs \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="398ab-141">vs\_4\_1</span></span>  | <span data-ttu-id="398ab-142">ps \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="398ab-142">ps\_4\_0</span></span> | <span data-ttu-id="398ab-143">ps \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="398ab-143">ps\_4\_1</span></span>  | <span data-ttu-id="398ab-144">gs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="398ab-144">gs\_4\_0</span></span> | <span data-ttu-id="398ab-145">gs \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="398ab-145">gs\_4\_1</span></span>  |
|----------|-----------|----------|-----------|----------|-----------|
|          | <span data-ttu-id="398ab-146">x</span><span class="sxs-lookup"><span data-stu-id="398ab-146">x</span></span>         |          | <span data-ttu-id="398ab-147">x</span><span class="sxs-lookup"><span data-stu-id="398ab-147">x</span></span>         |          | <span data-ttu-id="398ab-148">x</span><span class="sxs-lookup"><span data-stu-id="398ab-148">x</span></span>         |



 

1.  <span data-ttu-id="398ab-149">TextureCubeArray está disponible en El modelo de sombreador 4.1 o superior.</span><span class="sxs-lookup"><span data-stu-id="398ab-149">TextureCubeArray is available in Shader Model 4.1 or higher.</span></span>
2.  <span data-ttu-id="398ab-150">El modelo de sombreador 4.1 está disponible en Direct3D 10.1 o posterior.</span><span class="sxs-lookup"><span data-stu-id="398ab-150">Shader Model 4.1 is available in Direct3D 10.1 or higher.</span></span>

## <a name="example"></a><span data-ttu-id="398ab-151">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="398ab-151">Example</span></span>


```
Texture2D<int1> Tex2d;
Texture2DArray<int2> Tex2dArray;
TextureCube<int3> TexCube;
TextureCubeArray<float2> TexCubeArray;

SamplerState s;

int4 main (float4 f : SV_Position) : SV_Target
{
    int2 iOffset = int2(2,3);

    int4 i1 = Tex2d.Gather(s, f.xy);
    int4 i2 = Tex2d.Gather(s, f.xy, iOffset);

    int4 i3 = Tex2dArray.Gather(s, f.xyz);
    int4 i4 = Tex2dArray.Gather(s, f.xyz, iOffset);

    int4 i5 = TexCube.Gather(s, f.xyzw);

    float4 f6 = TexCubeArray.Gather(s, f.xyzw);

    return i1+i2+i3+i4+i5+int4(i6);
}
  
```



## <a name="related-topics"></a><span data-ttu-id="398ab-152">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="398ab-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="398ab-153">Texture-Object</span><span class="sxs-lookup"><span data-stu-id="398ab-153">Texture-Object</span></span>](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

 





