---
title: SampleCmp (objeto de textura de HLSL de DirectX)
description: Muestrea una textura y compara un único componente con el valor de comparación especificado.
ms.assetid: e21894c4-e8c5-4c3d-92c1-727964f8fd94
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6991bead4bfc42451c26fe5476b4c114626eb7e8
ms.sourcegitcommit: 0d6365d4e852b09a9100d9cfb9a5334922ebf478
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/17/2020
ms.locfileid: "104997193"
---
# <a name="samplecmp-directx-hlsl-texture-object"></a><span data-ttu-id="4d17a-103">SampleCmp (objeto de textura de HLSL de DirectX)</span><span class="sxs-lookup"><span data-stu-id="4d17a-103">SampleCmp (DirectX HLSL Texture Object)</span></span>

<span data-ttu-id="4d17a-104">Muestrea una textura y compara un único componente con el valor de comparación especificado.</span><span class="sxs-lookup"><span data-stu-id="4d17a-104">Samples a texture and compares a single component against the specified comparison value.</span></span>

<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4d17a-105">Float Object. SampleCmp (</span><span class="sxs-lookup"><span data-stu-id="4d17a-105">float Object.SampleCmp(</span></span> <dl> <span data-ttu-id="4d17a-106">SamplerComparisonState S,</span><span class="sxs-lookup"><span data-stu-id="4d17a-106">SamplerComparisonState S,</span></span><br />
<span data-ttu-id="4d17a-107">Ubicación Float,</span><span class="sxs-lookup"><span data-stu-id="4d17a-107">float Location,</span></span><br />
<span data-ttu-id="4d17a-108">Float CompareValue,</span><span class="sxs-lookup"><span data-stu-id="4d17a-108">float CompareValue,</span></span><br />
<span data-ttu-id="4d17a-109">[desplazamiento int]</span><span class="sxs-lookup"><span data-stu-id="4d17a-109">[int Offset]</span></span><br />
</dl><span data-ttu-id="4d17a-110">);</span><span class="sxs-lookup"><span data-stu-id="4d17a-110">);</span></span></td>
</tr>
</tbody>
</table>
 

<span data-ttu-id="4d17a-111">La comparación es una comparación de un solo componente entre el primer componente almacenado en la textura y el valor de comparación pasado en el método.</span><span class="sxs-lookup"><span data-stu-id="4d17a-111">The comparison is a single-component comparison between the first component stored in the texture, and the comparison value passed into the method.</span></span>

<span data-ttu-id="4d17a-112">Este método solo se puede invocar desde un sombreador de píxeles; no se admite en un sombreador de vértices o de geometría.</span><span class="sxs-lookup"><span data-stu-id="4d17a-112">This method can be invoked only from a pixel shader; it isn't supported in a vertex or geometry shader.</span></span>

## <a name="parameters"></a><span data-ttu-id="4d17a-113">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4d17a-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4d17a-114"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span>*Objeto*</span><span class="sxs-lookup"><span data-stu-id="4d17a-114"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span>*Object*</span></span>
</dt> <dd>

<span data-ttu-id="4d17a-115">Cualquier tipo [de objeto de textura](dx-graphics-hlsl-to-type.md) (excepto Texture2DMS, Texture2DMSArray o Texture3D).</span><span class="sxs-lookup"><span data-stu-id="4d17a-115">Any [texture-object](dx-graphics-hlsl-to-type.md) type (except Texture2DMS, Texture2DMSArray, or Texture3D).</span></span>

</dd> <dt>

<span data-ttu-id="4d17a-116"><span id="S"></span><span id="s"></span>*Seg*</span><span class="sxs-lookup"><span data-stu-id="4d17a-116"><span id="S"></span><span id="s"></span>*S*</span></span>
</dt> <dd>

<span data-ttu-id="4d17a-117">\[en \] un estado de comparación de muestra, que es el estado de la muestra más un estado de comparación (una función de comparación y un filtro de comparación).</span><span class="sxs-lookup"><span data-stu-id="4d17a-117">\[in\] A sampler-comparison state, which is the sampler state plus a comparison state (a comparison function and a comparison filter).</span></span> <span data-ttu-id="4d17a-118">Vea el [tipo de muestra](dx-graphics-hlsl-sampler.md) para obtener más información y un ejemplo.</span><span class="sxs-lookup"><span data-stu-id="4d17a-118">See the [sampler type](dx-graphics-hlsl-sampler.md) for details and an example.</span></span>

</dd> <dt>

<span data-ttu-id="4d17a-119"><span id="Location"></span><span id="location"></span><span id="LOCATION"></span>*Cód*</span><span class="sxs-lookup"><span data-stu-id="4d17a-119"><span id="Location"></span><span id="location"></span><span id="LOCATION"></span>*Location*</span></span>
</dt> <dd>

<span data-ttu-id="4d17a-120">\[en \] las coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="4d17a-120">\[in\] The texture coordinates.</span></span> <span data-ttu-id="4d17a-121">El tipo de argumento depende del tipo de objeto de textura.</span><span class="sxs-lookup"><span data-stu-id="4d17a-121">The argument type is dependent on the texture-object type.</span></span>

| <span data-ttu-id="4d17a-122">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="4d17a-122">Texture-Object Type</span></span>          | <span data-ttu-id="4d17a-123">Tipo de parámetro</span><span class="sxs-lookup"><span data-stu-id="4d17a-123">Parameter Type</span></span> |
|------------------------------|----------------|
| <span data-ttu-id="4d17a-124">Texture1D</span><span class="sxs-lookup"><span data-stu-id="4d17a-124">Texture1D</span></span>                    | <span data-ttu-id="4d17a-125">FLOAT</span><span class="sxs-lookup"><span data-stu-id="4d17a-125">float</span></span>          |
| <span data-ttu-id="4d17a-126">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="4d17a-126">Texture1DArray, Texture2D</span></span>    | <span data-ttu-id="4d17a-127">float2</span><span class="sxs-lookup"><span data-stu-id="4d17a-127">float2</span></span>         |
| <span data-ttu-id="4d17a-128">Texture2DArray ¹, TextureCube</span><span class="sxs-lookup"><span data-stu-id="4d17a-128">Texture2DArray¹, TextureCube</span></span> | <span data-ttu-id="4d17a-129">float3</span><span class="sxs-lookup"><span data-stu-id="4d17a-129">float3</span></span>         |
| <span data-ttu-id="4d17a-130">TextureCubeArray ¹</span><span class="sxs-lookup"><span data-stu-id="4d17a-130">TextureCubeArray¹</span></span>            | <span data-ttu-id="4d17a-131">float4</span><span class="sxs-lookup"><span data-stu-id="4d17a-131">float4</span></span>         |

</dd> <dt>

<span data-ttu-id="4d17a-132"><span id="CompareValue"></span><span id="comparevalue"></span><span id="COMPAREVALUE"></span>*CompareValue*</span><span class="sxs-lookup"><span data-stu-id="4d17a-132"><span id="CompareValue"></span><span id="comparevalue"></span><span id="COMPAREVALUE"></span>*CompareValue*</span></span>
</dt> <dd>

<span data-ttu-id="4d17a-133">Un valor de punto flotante que se va a utilizar como valor de comparación.</span><span class="sxs-lookup"><span data-stu-id="4d17a-133">A floating-point value to use as a comparison value.</span></span>

</dd> <dt>

<span data-ttu-id="4d17a-134"><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span>*Posición*</span><span class="sxs-lookup"><span data-stu-id="4d17a-134"><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span>*Offset*</span></span>
</dt> <dd>

<span data-ttu-id="4d17a-135">\[en \] un desplazamiento de coordenadas de textura opcional, que se puede usar para cualquier tipo de objeto de textura, el desplazamiento se aplica a la ubicación antes del muestreo.</span><span class="sxs-lookup"><span data-stu-id="4d17a-135">\[in\] An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="4d17a-136">Los desplazamientos de textura deben ser estáticos.</span><span class="sxs-lookup"><span data-stu-id="4d17a-136">The texture offsets need to be static.</span></span> <span data-ttu-id="4d17a-137">El tipo de argumento depende del tipo de objeto de textura.</span><span class="sxs-lookup"><span data-stu-id="4d17a-137">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="4d17a-138">Para obtener más información, vea [aplicar desplazamientos de coordenadas de textura](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="4d17a-138">For more info, see [Applying texture coordinate offsets](dx-graphics-hlsl-to-sample.md).</span></span>

| <span data-ttu-id="4d17a-139">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="4d17a-139">Texture-Object Type</span></span>            | <span data-ttu-id="4d17a-140">Tipo de parámetro</span><span class="sxs-lookup"><span data-stu-id="4d17a-140">Parameter Type</span></span> |
|--------------------------------|----------------|
| <span data-ttu-id="4d17a-141">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="4d17a-141">Texture1D, Texture1DArray</span></span>      | <span data-ttu-id="4d17a-142">int</span><span class="sxs-lookup"><span data-stu-id="4d17a-142">int</span></span>            |
| <span data-ttu-id="4d17a-143">Texture2D, Texture2DArray ¹</span><span class="sxs-lookup"><span data-stu-id="4d17a-143">Texture2D, Texture2DArray¹</span></span>     | <span data-ttu-id="4d17a-144">int2</span><span class="sxs-lookup"><span data-stu-id="4d17a-144">int2</span></span>           |
| <span data-ttu-id="4d17a-145">TextureCube, TextureCubeArray ¹</span><span class="sxs-lookup"><span data-stu-id="4d17a-145">TextureCube, TextureCubeArray¹</span></span> | <span data-ttu-id="4d17a-146">No compatible</span><span class="sxs-lookup"><span data-stu-id="4d17a-146">Not supported</span></span>  |

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4d17a-147">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4d17a-147">Return Value</span></span>

<span data-ttu-id="4d17a-148">Devuelve un valor de punto flotante en el intervalo de \[ 0.. 1 \] .</span><span class="sxs-lookup"><span data-stu-id="4d17a-148">Returns a floating-point value in the range \[0..1\].</span></span>

<span data-ttu-id="4d17a-149">Para cada textura capturada (según la configuración de muestra del modo de filtro), **SampleCmp** realiza una comparación del valor z (tercer componente de la entrada) del sombreador con el valor textura (1 si se pasa la comparación; en caso contrario, 0).</span><span class="sxs-lookup"><span data-stu-id="4d17a-149">For each texel fetched (based on the sampler configuration of the filter mode), **SampleCmp** performs a comparison of the z value (3rd component of input) from the shader against the texel value (1 if the comparison passes; otherwise 0).</span></span> <span data-ttu-id="4d17a-150">A continuación, **SampleCmp** combina estos 0 y 1 resultados para cada textura, como en el filtrado de textura normal (no un promedio) y devuelve el \[ valor 0.. 1 resultante \] al sombreador.</span><span class="sxs-lookup"><span data-stu-id="4d17a-150">**SampleCmp** then blends these 0 and 1 results for each texel together as in normal texture filtering (not an average) and returns the resulting \[0..1\] value to the shader.</span></span>

## <a name="remarks"></a><span data-ttu-id="4d17a-151">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4d17a-151">Remarks</span></span>

<span data-ttu-id="4d17a-152">El filtrado de comparación proporciona una operación de filtrado básica que resulta útil para el filtrado porcentual y más detallado.</span><span class="sxs-lookup"><span data-stu-id="4d17a-152">Comparison filtering provides a basic filtering operation that is useful for percentage-closer-depth filtering.</span></span>

<span data-ttu-id="4d17a-153">Cuando se usa este método en un recurso de punto flotante (en lugar de un formato normalizado con o sin signo), el valor de comparación no se fija automáticamente entre 0,0 y 1,0.</span><span class="sxs-lookup"><span data-stu-id="4d17a-153">When using this method on a floating-point resource (Instead of a signed-normalized or unsigned-normalized format), the comparison value is not automatically clamped between 0.0 and 1.0.</span></span> <span data-ttu-id="4d17a-154">Por lo tanto, puede ser necesaria una abrazadera manual del valor de comparación para las técnicas de sombreado comunes.</span><span class="sxs-lookup"><span data-stu-id="4d17a-154">Therefore, a manual clamp of the comparison value may be necessary for common shadowing techniques.</span></span>

<span data-ttu-id="4d17a-155">Use un desplazamiento solo en un entero miplevel; de lo contrario, puede obtener resultados diferentes en función de la implementación del hardware o de la configuración del controlador.</span><span class="sxs-lookup"><span data-stu-id="4d17a-155">Use an offset only at an integer miplevel; otherwise, you may get different results depending on hardware implementation or driver settings.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="4d17a-156">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="4d17a-156">Minimum Shader Model</span></span>

<span data-ttu-id="4d17a-157">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="4d17a-157">This function is supported in the following shader models.</span></span>

| <span data-ttu-id="4d17a-158">vs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="4d17a-158">vs\_4\_0</span></span> | <span data-ttu-id="4d17a-159">vs \_ 4 \_ 1 ²</span><span class="sxs-lookup"><span data-stu-id="4d17a-159">vs\_4\_1²</span></span> | <span data-ttu-id="4d17a-160">PS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="4d17a-160">ps\_4\_0</span></span> | <span data-ttu-id="4d17a-161">PS \_ 4 \_ 1 ²</span><span class="sxs-lookup"><span data-stu-id="4d17a-161">ps\_4\_1²</span></span> | <span data-ttu-id="4d17a-162">GS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="4d17a-162">gs\_4\_0</span></span> | <span data-ttu-id="4d17a-163">GS \_ 4 \_ 1 ²</span><span class="sxs-lookup"><span data-stu-id="4d17a-163">gs\_4\_1²</span></span> |
|----------|-----------|----------|-----------|----------|-----------|
|          |           | <span data-ttu-id="4d17a-164">x ¹</span><span class="sxs-lookup"><span data-stu-id="4d17a-164">x¹</span></span>       | <span data-ttu-id="4d17a-165">x</span><span class="sxs-lookup"><span data-stu-id="4d17a-165">x</span></span>         |          |           |

1.  <span data-ttu-id="4d17a-166">Texture2DArray y TextureCubeArray están disponibles en el modelo de sombreador 4,1 o superior.</span><span class="sxs-lookup"><span data-stu-id="4d17a-166">Texture2DArray and TextureCubeArray are available in Shader Model 4.1 or higher.</span></span>
2.  <span data-ttu-id="4d17a-167">El modelo de sombreador 4,1 está disponible en Direct3D 10,1 o superior.</span><span class="sxs-lookup"><span data-stu-id="4d17a-167">Shader Model 4.1 is available in Direct3D 10.1 or higher.</span></span>

> [!NOTE]  
> <span data-ttu-id="4d17a-168">**SampleCmp** también está disponible en \_ \_ \_ los niveles 9 \_ 1 y 4 0 nivel 9 3 de PS 4 \_ \_ \_ \_ , cuando se usan las técnicas que se describen en [implementación de búferes de sombras para el nivel de características 9 de Direct3D](/previous-versions/windows/apps/jj262110(v=win.10)).</span><span class="sxs-lookup"><span data-stu-id="4d17a-168">**SampleCmp** is also available in ps 4\_0\_level\_9\_1 and 4\_0\_level\_9\_3 when you use the techniques that are described in [Implementing shadow buffers for Direct3D feature level 9](/previous-versions/windows/apps/jj262110(v=win.10)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4d17a-169">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4d17a-169">Related topics</span></span>

[<span data-ttu-id="4d17a-170">Texture-objeto</span><span class="sxs-lookup"><span data-stu-id="4d17a-170">Texture-Object</span></span>](dx-graphics-hlsl-to-type.md)
