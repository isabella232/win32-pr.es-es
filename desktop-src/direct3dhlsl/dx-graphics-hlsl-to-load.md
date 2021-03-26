---
title: Load (objeto de textura de HLSL de DirectX)
description: Lee los datos de textura sin ningún filtrado ni muestreo.
ms.assetid: a2fbda88-29c7-4d28-bd3e-df1d9aa36ee8
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 08d3964788a238492ff7d5189544603b35808465
ms.sourcegitcommit: 4c00910ed754d7d0a68c9a833751d714c06e3b39
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/05/2021
ms.locfileid: "104151935"
---
# <a name="load-directx-hlsl-texture-object"></a><span data-ttu-id="252c6-103">Load (objeto de textura de HLSL de DirectX)</span><span class="sxs-lookup"><span data-stu-id="252c6-103">Load (DirectX HLSL Texture Object)</span></span>

<span data-ttu-id="252c6-104">Lee los datos de textura sin ningún filtrado ni muestreo.</span><span class="sxs-lookup"><span data-stu-id="252c6-104">Reads texel data without any filtering or sampling.</span></span>



<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="252c6-105">RET Object. Load (</span><span class="sxs-lookup"><span data-stu-id="252c6-105">ret Object.Load(</span></span><dl> <span data-ttu-id="252c6-106">Ubicación typeX,</span><span class="sxs-lookup"><span data-stu-id="252c6-106">typeX Location,</span></span><br />
<span data-ttu-id="252c6-107">[typeX SampleIndex, ]</span><span class="sxs-lookup"><span data-stu-id="252c6-107">[typeX SampleIndex, ]</span></span><br />
<span data-ttu-id="252c6-108">[desplazamiento de typeX]</span><span class="sxs-lookup"><span data-stu-id="252c6-108">[typeX Offset ]</span></span><br />
</dl><span data-ttu-id="252c6-109">);</span><span class="sxs-lookup"><span data-stu-id="252c6-109">);</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="252c6-110">typeX denota que hay cuatro tipos posibles: **int**, **INT2**, **INT3** o **INT4**.</span><span class="sxs-lookup"><span data-stu-id="252c6-110">typeX denotes that there are four possible types: **int**, **int2**, **int3** or **int4**.</span></span>

 

## <a name="parameters"></a><span data-ttu-id="252c6-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="252c6-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="252c6-112"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span>*Objeto*</span><span class="sxs-lookup"><span data-stu-id="252c6-112"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span>*Object*</span></span>
</dt> <dd>

<span data-ttu-id="252c6-113">Un tipo [de objeto de textura](dx-graphics-hlsl-to-type.md) (excepto TextureCube o TextureCubeArray).</span><span class="sxs-lookup"><span data-stu-id="252c6-113">A [texture-object](dx-graphics-hlsl-to-type.md) type (except TextureCube or TextureCubeArray).</span></span>

</dd> <dt>

<span data-ttu-id="252c6-114"><span id="Location"></span><span id="location"></span><span id="LOCATION"></span>*Cód*</span><span class="sxs-lookup"><span data-stu-id="252c6-114"><span id="Location"></span><span id="location"></span><span id="LOCATION"></span>*Location*</span></span>
</dt> <dd>

<span data-ttu-id="252c6-115">\[en \] las coordenadas de textura; el último componente especifica el nivel de mipmap.</span><span class="sxs-lookup"><span data-stu-id="252c6-115">\[in\] The texture coordinates; the last component specifies the mipmap level.</span></span> <span data-ttu-id="252c6-116">Este método usa un sistema de coordenadas basado en 0 y no un sistema UV 0,0-1,0.</span><span class="sxs-lookup"><span data-stu-id="252c6-116">This method uses a 0-based coordinate system and not a 0.0-1.0 UV system.</span></span> <span data-ttu-id="252c6-117">El tipo de argumento depende del tipo de objeto de textura.</span><span class="sxs-lookup"><span data-stu-id="252c6-117">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="252c6-118">Tipo de objeto</span><span class="sxs-lookup"><span data-stu-id="252c6-118">Object Type</span></span>                                  | <span data-ttu-id="252c6-119">Tipo de parámetro</span><span class="sxs-lookup"><span data-stu-id="252c6-119">Parameter Type</span></span> |
|----------------------------------------------|----------------|
| <span data-ttu-id="252c6-120">Buffer</span><span class="sxs-lookup"><span data-stu-id="252c6-120">Buffer</span></span>                                       | <span data-ttu-id="252c6-121">int</span><span class="sxs-lookup"><span data-stu-id="252c6-121">int</span></span>            |
| <span data-ttu-id="252c6-122">Texture1D, Texture2DMS</span><span class="sxs-lookup"><span data-stu-id="252c6-122">Texture1D, Texture2DMS</span></span>                       | <span data-ttu-id="252c6-123">int2</span><span class="sxs-lookup"><span data-stu-id="252c6-123">int2</span></span>           |
| <span data-ttu-id="252c6-124">Texture1DArray, Texture 2D, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="252c6-124">Texture1DArray, Texture 2D, Texture2DMSArray</span></span> | <span data-ttu-id="252c6-125">int3</span><span class="sxs-lookup"><span data-stu-id="252c6-125">int3</span></span>           |
| <span data-ttu-id="252c6-126">Texture2DArray, Texture3D</span><span class="sxs-lookup"><span data-stu-id="252c6-126">Texture2DArray, Texture3D</span></span>                    | <span data-ttu-id="252c6-127">int4</span><span class="sxs-lookup"><span data-stu-id="252c6-127">int4</span></span>           |



 

<span data-ttu-id="252c6-128">Por ejemplo, para tener acceso a una textura 2D, proporcione coordenadas UV para los dos primeros componentes y un nivel de mipmap para el tercer componente.</span><span class="sxs-lookup"><span data-stu-id="252c6-128">For example, to access a 2D texture, supply UV coordinates for the first two components and a mipmap level for the third component.</span></span>

> [!Note]  
> <span data-ttu-id="252c6-129">Cuando una o varias de las coordenadas de la *Ubicación* superan las dimensiones del nivel de mipmap u, v o w de la textura, **Load** devuelve cero en todos los componentes.</span><span class="sxs-lookup"><span data-stu-id="252c6-129">When one or more of the coordinates in *Location* exceed the u, v, or w mipmap level dimensions of the texture, **Load** returns zero in all components.</span></span> <span data-ttu-id="252c6-130">Direct3D garantiza que se devuelva cero para cualquier recurso al que se tenga acceso fuera de los límites.</span><span class="sxs-lookup"><span data-stu-id="252c6-130">Direct3D guarantees to return zero for any resource that is accessed out of bounds.</span></span>

 

</dd> <dt>

<span data-ttu-id="252c6-131"><span id="SampleIndex"></span><span id="sampleindex"></span><span id="SAMPLEINDEX"></span>*SampleIndex*</span><span class="sxs-lookup"><span data-stu-id="252c6-131"><span id="SampleIndex"></span><span id="sampleindex"></span><span id="SAMPLEINDEX"></span>*SampleIndex*</span></span>
</dt> <dd>

<span data-ttu-id="252c6-132">\[en \] un índice de muestreo opcional.</span><span class="sxs-lookup"><span data-stu-id="252c6-132">\[in\] An optional sampling index.</span></span>



| <span data-ttu-id="252c6-133">Tipo de textura</span><span class="sxs-lookup"><span data-stu-id="252c6-133">Texture Type</span></span>                                                                                                   | <span data-ttu-id="252c6-134">Tipo de parámetro</span><span class="sxs-lookup"><span data-stu-id="252c6-134">Parameter Type</span></span> |
|----------------------------------------------------------------------------------------------------------------|----------------|
| <span data-ttu-id="252c6-135">Texture1D, Texture1DArray, Texture2D, Texture2DArray, Texture3D, Texture2DArray, TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="252c6-135">Texture1D, Texture1DArray, Texture2D, Texture2DArray, Texture3D, Texture2DArray, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="252c6-136">no admitido</span><span class="sxs-lookup"><span data-stu-id="252c6-136">not supported</span></span>  |
| <span data-ttu-id="252c6-137">Texture2DMS, Texture2DMSArray ¹</span><span class="sxs-lookup"><span data-stu-id="252c6-137">Texture2DMS, Texture2DMSArray¹</span></span>                                                                                 | <span data-ttu-id="252c6-138">int</span><span class="sxs-lookup"><span data-stu-id="252c6-138">int</span></span>            |



 

> [!Note]  
> <span data-ttu-id="252c6-139">*SampleIndex* solo está disponible para las texturas de varios ejemplos.</span><span class="sxs-lookup"><span data-stu-id="252c6-139">*SampleIndex* is only available for multi-sample textures.</span></span>

 

</dd> <dt>

<span data-ttu-id="252c6-140"><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span>*Posición*</span><span class="sxs-lookup"><span data-stu-id="252c6-140"><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span>*Offset*</span></span>
</dt> <dd>

<span data-ttu-id="252c6-141">\[en \] un desplazamiento opcional aplicado a las coordenadas de textura antes del muestreo.</span><span class="sxs-lookup"><span data-stu-id="252c6-141">\[in\] An optional offset applied to the texture coordinates before sampling.</span></span> <span data-ttu-id="252c6-142">El tipo de desplazamiento depende del tipo de objeto de textura y debe ser estático.</span><span class="sxs-lookup"><span data-stu-id="252c6-142">The offset type is dependent on the texture-object type, and needs to be static.</span></span>



| <span data-ttu-id="252c6-143">Tipo de textura</span><span class="sxs-lookup"><span data-stu-id="252c6-143">Texture Type</span></span>                                             | <span data-ttu-id="252c6-144">Tipo de parámetro</span><span class="sxs-lookup"><span data-stu-id="252c6-144">Parameter Type</span></span> |
|----------------------------------------------------------|----------------|
| <span data-ttu-id="252c6-145">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="252c6-145">Texture1D, Texture1DArray</span></span>                                | <span data-ttu-id="252c6-146">int</span><span class="sxs-lookup"><span data-stu-id="252c6-146">int</span></span>            |
| <span data-ttu-id="252c6-147">Texture2D, Texture2DArray, Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="252c6-147">Texture2D, Texture2DArray, Texture2DMS, Texture2DMSArray</span></span> | <span data-ttu-id="252c6-148">int2</span><span class="sxs-lookup"><span data-stu-id="252c6-148">int2</span></span>           |
| <span data-ttu-id="252c6-149">Texture3D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="252c6-149">Texture3D, Texture2DArray</span></span>                                | <span data-ttu-id="252c6-150">int3</span><span class="sxs-lookup"><span data-stu-id="252c6-150">int3</span></span>           |



 

> [!Note]  
> <span data-ttu-id="252c6-151">Si usa *offset* con texturas de varios ejemplos, también debe especificar *SampleIndex*.</span><span class="sxs-lookup"><span data-stu-id="252c6-151">If you use *Offset* with multi-sample textures, you must also specify *SampleIndex*.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="252c6-152">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="252c6-152">Return Value</span></span>

<span data-ttu-id="252c6-153">El tipo de valor devuelto coincide con el tipo en la declaración del *objeto* .</span><span class="sxs-lookup"><span data-stu-id="252c6-153">The return type matches the type in the *Object* declaration.</span></span> <span data-ttu-id="252c6-154">Por ejemplo, un objeto Texture2D que se declaró como "Texture2d <uint4> de la cartexture;" tiene un valor devuelto de tipo **uint4**.</span><span class="sxs-lookup"><span data-stu-id="252c6-154">For example, a Texture2D object that was declared as "Texture2d<uint4> myTexture;" has a return value of type **uint4**.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="252c6-155">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="252c6-155">Minimum Shader Model</span></span>

<span data-ttu-id="252c6-156">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="252c6-156">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="252c6-157">vs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="252c6-157">vs\_4\_0</span></span> | <span data-ttu-id="252c6-158">vs \_ 4 \_ 1 ¹</span><span class="sxs-lookup"><span data-stu-id="252c6-158">vs\_4\_1¹</span></span> | <span data-ttu-id="252c6-159">PS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="252c6-159">ps\_4\_0</span></span> | <span data-ttu-id="252c6-160">PS \_ 4 \_ 1 ¹</span><span class="sxs-lookup"><span data-stu-id="252c6-160">ps\_4\_1¹</span></span> | <span data-ttu-id="252c6-161">GS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="252c6-161">gs\_4\_0</span></span> | <span data-ttu-id="252c6-162">GS \_ 4 \_ 1 ¹</span><span class="sxs-lookup"><span data-stu-id="252c6-162">gs\_4\_1¹</span></span> |
|----------|-----------|----------|-----------|----------|-----------|
| <span data-ttu-id="252c6-163">x</span><span class="sxs-lookup"><span data-stu-id="252c6-163">x</span></span>        | <span data-ttu-id="252c6-164">x</span><span class="sxs-lookup"><span data-stu-id="252c6-164">x</span></span>         | <span data-ttu-id="252c6-165">x</span><span class="sxs-lookup"><span data-stu-id="252c6-165">x</span></span>        | <span data-ttu-id="252c6-166">x</span><span class="sxs-lookup"><span data-stu-id="252c6-166">x</span></span>         | <span data-ttu-id="252c6-167">x</span><span class="sxs-lookup"><span data-stu-id="252c6-167">x</span></span>        | <span data-ttu-id="252c6-168">x</span><span class="sxs-lookup"><span data-stu-id="252c6-168">x</span></span>         |



 

-   <span data-ttu-id="252c6-169">El modelo de sombreador 4,1 está disponible en Direct3D 10,1 o superior.</span><span class="sxs-lookup"><span data-stu-id="252c6-169">Shader Model 4.1 is available in Direct3D 10.1 or higher.</span></span>

## <a name="example"></a><span data-ttu-id="252c6-170">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="252c6-170">Example</span></span>

<span data-ttu-id="252c6-171">Este ejemplo de código parcial procede del archivo Paint. FX en el [ejemplo AdvancedParticles](https://msdn.microsoft.com/library/Ee416394(v=VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="252c6-171">This partial code example is from the Paint.fx file in the [AdvancedParticles Sample](https://msdn.microsoft.com/library/Ee416394(v=VS.85).aspx).</span></span>


```
// Object Declarations
Buffer<float4> g_ParticleBuffer;

// Shader body calling the intrinsic function
float4 PSPaint(PSQuadIn input) : SV_Target
{       
    ... 
    for( int i=g_ParticleStart; i<g_NumParticles; i+=g_ParticleStep )
    {
        ... 
        // load the particle
        float4 particlePos = g_ParticleBuffer.Load( i*4 );
        float4 particleColor = g_ParticleBuffer.Load( (i*4) + 2 );
        ...     
    }
    ...
}   
```



## <a name="related-topics"></a><span data-ttu-id="252c6-172">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="252c6-172">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="252c6-173">Texture-objeto</span><span class="sxs-lookup"><span data-stu-id="252c6-173">Texture-Object</span></span>](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

 




