---
title: Recopilar (objeto de textura de HLSL de DirectX)
description: Obtiene los cuatro ejemplos (solo componente rojo) que se utilizarían para la interpolación bilineal al realizar el muestreo de una textura.
ms.assetid: a394d8c2-99cc-4a38-9ac9-34afc666ebe0
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 16c568afc3cfdc0d26472d50599abdf3dbd08301
ms.sourcegitcommit: 0d6365d4e852b09a9100d9cfb9a5334922ebf478
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/17/2020
ms.locfileid: "104984123"
---
# <a name="gather-directx-hlsl-texture-object"></a><span data-ttu-id="a14f2-103">Recopilar (objeto de textura de HLSL de DirectX)</span><span class="sxs-lookup"><span data-stu-id="a14f2-103">Gather (DirectX HLSL Texture Object)</span></span>

<span data-ttu-id="a14f2-104">Obtiene los cuatro ejemplos (solo componente rojo) que se utilizarían para la interpolación bilineal al realizar el muestreo de una textura.</span><span class="sxs-lookup"><span data-stu-id="a14f2-104">Gets the four samples (red component only) that would be used for bilinear interpolation when sampling a texture.</span></span>



|                                                                                                    |
|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a14f2-105">&lt;Tipo de plantilla &gt; 4 Object. Gather ( \_ Estado de muestra S, float2 \| 3 \| 4 ubicación \[ , desplazamiento de INT2 \] );</span><span class="sxs-lookup"><span data-stu-id="a14f2-105">&lt;Template Type&gt;4 Object.Gather( sampler\_state S, float2\|3\|4 Location \[, int2 Offset\] );</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="a14f2-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a14f2-106">Parameters</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a14f2-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="a14f2-107">Item</span></span></th>
<th><span data-ttu-id="a14f2-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="a14f2-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a14f2-109"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Objeto</em></span><span class="sxs-lookup"><span data-stu-id="a14f2-109"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Object</em></span></span><br/></td>
<td><span data-ttu-id="a14f2-110">Se admiten los siguientes tipos <a href="dx-graphics-hlsl-to-type.md">de objeto de textura</a> : Texture2D, Texture2DArray, TextureCube, TextureCubeArray.</span><span class="sxs-lookup"><span data-stu-id="a14f2-110">The following <a href="dx-graphics-hlsl-to-type.md">texture-object</a> types are supported: Texture2D, Texture2DArray, TextureCube, TextureCubeArray.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a14f2-111"><span id="S"></span><span id="s"></span><em>Seg</em></span><span class="sxs-lookup"><span data-stu-id="a14f2-111"><span id="S"></span><span id="s"></span><em>S</em></span></span><br/></td>
<td><span data-ttu-id="a14f2-112">de Un <a href="dx-graphics-hlsl-sampler.md">Estado de muestra</a>.</span><span class="sxs-lookup"><span data-stu-id="a14f2-112">[in] A <a href="dx-graphics-hlsl-sampler.md">Sampler state</a>.</span></span> <span data-ttu-id="a14f2-113">Se trata de un objeto declarado en un archivo de efectos que contiene las asignaciones de estado.</span><span class="sxs-lookup"><span data-stu-id="a14f2-113">This is an object declared in an effect file that contains state assignments.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a14f2-114"><span id="Location"></span><span id="location"></span><span id="LOCATION"></span><em>Cód</em></span><span class="sxs-lookup"><span data-stu-id="a14f2-114"><span id="Location"></span><span id="location"></span><span id="LOCATION"></span><em>Location</em></span></span><br/></td>
<td><span data-ttu-id="a14f2-115">de Coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="a14f2-115">[in] The texture coordinates.</span></span> <span data-ttu-id="a14f2-116">El tipo de argumento depende del tipo de objeto de textura.</span><span class="sxs-lookup"><span data-stu-id="a14f2-116">The argument type is dependent on the texture-object type.</span></span> <br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="a14f2-117">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="a14f2-117">Texture-Object Type</span></span></th>
<th><span data-ttu-id="a14f2-118">Tipo de parámetro</span><span class="sxs-lookup"><span data-stu-id="a14f2-118">Parameter Type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a14f2-119">Texture2D</span><span class="sxs-lookup"><span data-stu-id="a14f2-119">Texture2D</span></span></td>
<td><span data-ttu-id="a14f2-120">float2</span><span class="sxs-lookup"><span data-stu-id="a14f2-120">float2</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a14f2-121">Texture2DArray, TextureCube</span><span class="sxs-lookup"><span data-stu-id="a14f2-121">Texture2DArray, TextureCube</span></span></td>
<td><span data-ttu-id="a14f2-122">float3</span><span class="sxs-lookup"><span data-stu-id="a14f2-122">float3</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a14f2-123">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="a14f2-123">TextureCubeArray</span></span> </td>
<td><span data-ttu-id="a14f2-124">float4</span><span class="sxs-lookup"><span data-stu-id="a14f2-124">float4</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a14f2-125"><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span><em>Posición</em></span><span class="sxs-lookup"><span data-stu-id="a14f2-125"><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span><em>Offset</em></span></span></p></td>
<td><p><span data-ttu-id="a14f2-126">de Desplazamiento de coordenadas de textura opcional, que se puede usar para cualquier tipo de objeto de textura. el desplazamiento se aplica a la ubicación antes del muestreo.</span><span class="sxs-lookup"><span data-stu-id="a14f2-126">[in] An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="a14f2-127">Los desplazamientos de textura deben ser estáticos.</span><span class="sxs-lookup"><span data-stu-id="a14f2-127">The texture offsets need to be static.</span></span> <span data-ttu-id="a14f2-128">El tipo de argumento depende del tipo de objeto de textura.</span><span class="sxs-lookup"><span data-stu-id="a14f2-128">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="a14f2-129">Para obtener más información, vea <a href="dx-graphics-hlsl-to-sample.md">aplicar desplazamientos de coordenadas de textura</a>.</span><span class="sxs-lookup"><span data-stu-id="a14f2-129">For more info, see <a href="dx-graphics-hlsl-to-sample.md">Applying texture coordinate offsets</a>.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="a14f2-130">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="a14f2-130">Texture-Object Type</span></span></th>
<th><span data-ttu-id="a14f2-131">Tipo de parámetro</span><span class="sxs-lookup"><span data-stu-id="a14f2-131">Parameter Type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a14f2-132">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="a14f2-132">Texture2D, Texture2DArray</span></span></td>
<td><span data-ttu-id="a14f2-133">int2</span><span class="sxs-lookup"><span data-stu-id="a14f2-133">int2</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a14f2-134">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="a14f2-134">TextureCube, TextureCubeArray</span></span> </td>
<td><span data-ttu-id="a14f2-135">no admitido</span><span class="sxs-lookup"><span data-stu-id="a14f2-135">not supported</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="return-value"></a><span data-ttu-id="a14f2-136">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a14f2-136">Return Value</span></span>

<span data-ttu-id="a14f2-137">Un vector de cuatro componentes, con cuatro componentes de datos rojos, cuyo tipo es el mismo que el tipo de plantilla de la textura.</span><span class="sxs-lookup"><span data-stu-id="a14f2-137">A four-component vector, with four components of red data, whose type is the same as the texture's template type.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="a14f2-138">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="a14f2-138">Minimum Shader Model</span></span>

<span data-ttu-id="a14f2-139">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="a14f2-139">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="a14f2-140">vs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a14f2-140">vs\_4\_0</span></span> | <span data-ttu-id="a14f2-141">vs \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="a14f2-141">vs\_4\_1</span></span>  | <span data-ttu-id="a14f2-142">PS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a14f2-142">ps\_4\_0</span></span> | <span data-ttu-id="a14f2-143">PS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="a14f2-143">ps\_4\_1</span></span>  | <span data-ttu-id="a14f2-144">GS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a14f2-144">gs\_4\_0</span></span> | <span data-ttu-id="a14f2-145">GS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="a14f2-145">gs\_4\_1</span></span>  |
|----------|-----------|----------|-----------|----------|-----------|
|          | <span data-ttu-id="a14f2-146">x</span><span class="sxs-lookup"><span data-stu-id="a14f2-146">x</span></span>         |          | <span data-ttu-id="a14f2-147">x</span><span class="sxs-lookup"><span data-stu-id="a14f2-147">x</span></span>         |          | <span data-ttu-id="a14f2-148">x</span><span class="sxs-lookup"><span data-stu-id="a14f2-148">x</span></span>         |



 

1.  <span data-ttu-id="a14f2-149">TextureCubeArray está disponible en el modelo de sombreador 4,1 o superior.</span><span class="sxs-lookup"><span data-stu-id="a14f2-149">TextureCubeArray is available in Shader Model 4.1 or higher.</span></span>
2.  <span data-ttu-id="a14f2-150">El modelo de sombreador 4,1 está disponible en Direct3D 10,1 o superior.</span><span class="sxs-lookup"><span data-stu-id="a14f2-150">Shader Model 4.1 is available in Direct3D 10.1 or higher.</span></span>

## <a name="example"></a><span data-ttu-id="a14f2-151">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a14f2-151">Example</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="a14f2-152">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a14f2-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a14f2-153">Texture-objeto</span><span class="sxs-lookup"><span data-stu-id="a14f2-153">Texture-Object</span></span>](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

 





