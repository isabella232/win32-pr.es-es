---
title: Función de ejemplo (S, Float, int, Float, uint) (referencia de HLSL)
description: Muestrea un Texture2D con un valor opcional para Clamp valores de nivel de detalle (LOD) de ejemplo en y devuelve el estado de la operación.
ms.assetid: 1B9F48C4-DDB9-4547-B4AF-81A3ADA44C3F
keywords:
- HLSL de la función de ejemplo
topic_type:
- apiref
api_name:
- Sample
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9b378cb4031acecb8e0018053c7547e1948cc3e6
ms.sourcegitcommit: 0d6365d4e852b09a9100d9cfb9a5334922ebf478
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/17/2020
ms.locfileid: "103797565"
---
# <a name="samplesfloatintfloatuint-function-hlsl-reference"></a><span data-ttu-id="b6b31-104">Función de ejemplo (S, Float, int, Float, uint) (referencia de HLSL)</span><span class="sxs-lookup"><span data-stu-id="b6b31-104">Sample(S,float,int,float,uint) function (HLSL reference)</span></span>

<span data-ttu-id="b6b31-105">Muestrea un [**Texture2D**](sm5-object-texture2d.md) con un valor opcional para Clamp valores de nivel de detalle (LOD) de ejemplo en y devuelve el estado de la operación.</span><span class="sxs-lookup"><span data-stu-id="b6b31-105">Samples a [**Texture2D**](sm5-object-texture2d.md) with an optional value to clamp sample level-of-detail (LOD) values to, and returns status of the operation.</span></span>

> [!Note]  
> <span data-ttu-id="b6b31-106">Requiere el [modelo de sombreador 5](d3d11-graphics-reference-sm5.md) o superior.</span><span class="sxs-lookup"><span data-stu-id="b6b31-106">Requires [shader model 5](d3d11-graphics-reference-sm5.md) or higher.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="b6b31-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b6b31-107">Syntax</span></span>

``` syntax
DXGI_FORMAT Sample(
  in  SamplerState S,
  in  float Location,
  in  int Offset,
  in  float Clamp,
  out uint Status
);
```

## <a name="parameters"></a><span data-ttu-id="b6b31-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b6b31-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6b31-109">*S* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="b6b31-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6b31-110">Un [Estado de muestra](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="b6b31-110">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="b6b31-111">Se trata de un objeto declarado en un archivo de efectos que contiene las asignaciones de estado.</span><span class="sxs-lookup"><span data-stu-id="b6b31-111">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="b6b31-112">*Ubicación* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="b6b31-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6b31-113">Las coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="b6b31-113">The texture coordinates.</span></span> <span data-ttu-id="b6b31-114">El tipo de argumento depende del tipo de objeto de textura.</span><span class="sxs-lookup"><span data-stu-id="b6b31-114">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="b6b31-115">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="b6b31-115">Texture-Object Type</span></span>                    | <span data-ttu-id="b6b31-116">Tipo de parámetro</span><span class="sxs-lookup"><span data-stu-id="b6b31-116">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="b6b31-117">Texture1D</span><span class="sxs-lookup"><span data-stu-id="b6b31-117">Texture1D</span></span>                              | <span data-ttu-id="b6b31-118">FLOAT</span><span class="sxs-lookup"><span data-stu-id="b6b31-118">float</span></span>          |
| <span data-ttu-id="b6b31-119">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="b6b31-119">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="b6b31-120">float2</span><span class="sxs-lookup"><span data-stu-id="b6b31-120">float2</span></span>         |
| <span data-ttu-id="b6b31-121">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="b6b31-121">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="b6b31-122">float3</span><span class="sxs-lookup"><span data-stu-id="b6b31-122">float3</span></span>         |
| <span data-ttu-id="b6b31-123">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="b6b31-123">TextureCubeArray</span></span>                       | <span data-ttu-id="b6b31-124">float4</span><span class="sxs-lookup"><span data-stu-id="b6b31-124">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="b6b31-125">*Desplazamiento* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b6b31-125">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6b31-126">Desplazamiento de coordenadas de textura opcional, que se puede usar para cualquier tipo de objeto de textura. el desplazamiento se aplica a la ubicación antes del muestreo.</span><span class="sxs-lookup"><span data-stu-id="b6b31-126">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="b6b31-127">Los desplazamientos de textura deben ser estáticos.</span><span class="sxs-lookup"><span data-stu-id="b6b31-127">The texture offsets need to be static.</span></span> <span data-ttu-id="b6b31-128">El tipo de argumento depende del tipo de objeto de textura.</span><span class="sxs-lookup"><span data-stu-id="b6b31-128">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="b6b31-129">Para obtener más información, vea [aplicar desplazamientos de coordenadas de textura](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="b6b31-129">For more info, see [Applying texture coordinate offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="b6b31-130">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="b6b31-130">Texture-Object Type</span></span>           | <span data-ttu-id="b6b31-131">Tipo de parámetro</span><span class="sxs-lookup"><span data-stu-id="b6b31-131">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="b6b31-132">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="b6b31-132">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="b6b31-133">int</span><span class="sxs-lookup"><span data-stu-id="b6b31-133">int</span></span>            |
| <span data-ttu-id="b6b31-134">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="b6b31-134">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="b6b31-135">int2</span><span class="sxs-lookup"><span data-stu-id="b6b31-135">int2</span></span>           |
| <span data-ttu-id="b6b31-136">Texture3D</span><span class="sxs-lookup"><span data-stu-id="b6b31-136">Texture3D</span></span>                     | <span data-ttu-id="b6b31-137">int3</span><span class="sxs-lookup"><span data-stu-id="b6b31-137">int3</span></span>           |
| <span data-ttu-id="b6b31-138">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="b6b31-138">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="b6b31-139">no admitido</span><span class="sxs-lookup"><span data-stu-id="b6b31-139">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="b6b31-140">*Abrazadera* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b6b31-140">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6b31-141">Un valor opcional en el que se van a fijar los valores LOD de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="b6b31-141">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="b6b31-142">Por ejemplo, si se pasa 2.0 f para el valor Clamp, se asegura de que ningún ejemplo individual tenga acceso a un nivel de MIP inferior a 2.0 f.</span><span class="sxs-lookup"><span data-stu-id="b6b31-142">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> <dt>

<span data-ttu-id="b6b31-143">*Estado* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="b6b31-143">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b6b31-144">Estado de la operación.</span><span class="sxs-lookup"><span data-stu-id="b6b31-144">The status of the operation.</span></span> <span data-ttu-id="b6b31-145">No se puede tener acceso directamente al estado. en su lugar, pase el estado a la función intrínseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="b6b31-145">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="b6b31-146">**CheckAccessFullyMapped** devuelve **true** si todos los valores de la operación de **ejemplo**, **recopilación** o **carga** correspondiente han tenido acceso a los mosaicos asignados en un [recurso en mosaico](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="b6b31-146">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="b6b31-147">Si se tomó algún valor de un mosaico sin asignar, **CheckAccessFullyMapped** devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="b6b31-147">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6b31-148">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b6b31-148">Return value</span></span>

<span data-ttu-id="b6b31-149">Formato de textura, que es uno de los valores con tipo que aparecen [**en \_ formato de DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="b6b31-149">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="remarks"></a><span data-ttu-id="b6b31-150">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b6b31-150">Remarks</span></span>

<span data-ttu-id="b6b31-151">El muestreo de textura usa la posición textura para buscar un valor textura.</span><span class="sxs-lookup"><span data-stu-id="b6b31-151">Texture sampling uses the texel position to look up a texel value.</span></span> <span data-ttu-id="b6b31-152">Se puede aplicar un desplazamiento a la posición antes de la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="b6b31-152">An offset can be applied to the position before lookup.</span></span> <span data-ttu-id="b6b31-153">El estado de muestra contiene las opciones de muestreo y filtrado.</span><span class="sxs-lookup"><span data-stu-id="b6b31-153">The sampler state contains the sampling and filtering options.</span></span> <span data-ttu-id="b6b31-154">Este método se puede invocar dentro de un sombreador de píxeles, pero no se admite en un sombreador de vértices o un sombreador de geometría.</span><span class="sxs-lookup"><span data-stu-id="b6b31-154">This method can be invoked within a pixel shader, but it is not supported in a vertex shader or a geometry shader.</span></span>

<span data-ttu-id="b6b31-155">Use un desplazamiento solo en un entero miplevel; de lo contrario, puede obtener resultados diferentes en función de la implementación del hardware o de la configuración del controlador.</span><span class="sxs-lookup"><span data-stu-id="b6b31-155">Use an offset only at an integer miplevel; otherwise, you may get different results depending on hardware implementation or driver settings.</span></span>

### <a name="calculating-texel-positions"></a><span data-ttu-id="b6b31-156">Calcular las posiciones de textura</span><span class="sxs-lookup"><span data-stu-id="b6b31-156">Calculating Texel Positions</span></span>

<span data-ttu-id="b6b31-157">Las coordenadas de textura son valores de punto flotante que hacen referencia a los datos de textura, lo que también se conoce como espacio de textura normalizado.</span><span class="sxs-lookup"><span data-stu-id="b6b31-157">Texture coordinates are floating-point values that reference texture data, which is also known as normalized texture space.</span></span> <span data-ttu-id="b6b31-158">Los modos de ajuste de direcciones se aplican en este orden (coordenadas de textura + desplazamientos + modo de ajuste) para modificar las coordenadas de textura fuera del \[ intervalo de 0... 1 \] .</span><span class="sxs-lookup"><span data-stu-id="b6b31-158">Address wrapping modes are applied in this order (texture coordinates + offsets + wrap mode) to modify texture coordinates outside the \[0...1\] range.</span></span>

<span data-ttu-id="b6b31-159">En el caso de las matrices de textura, un valor adicional en el parámetro Location especifica un índice en una matriz de textura.</span><span class="sxs-lookup"><span data-stu-id="b6b31-159">For texture arrays, an additional value in the location parameter specifies an index into a texture array.</span></span> <span data-ttu-id="b6b31-160">Este índice se trata como un valor de punto flotante escalado (en lugar del espacio normalizado para las coordenadas de textura estándar).</span><span class="sxs-lookup"><span data-stu-id="b6b31-160">This index is treated as a scaled float value (instead of the normalized space for standard texture coordinates).</span></span> <span data-ttu-id="b6b31-161">La conversión a un índice de entero se realiza en el orden siguiente (float + Round-to-Even Integer + Clamp al intervalo de la matriz).</span><span class="sxs-lookup"><span data-stu-id="b6b31-161">The conversion to an integer index is done in the following order (float + round-to-nearest-even integer + clamp to the array range).</span></span>

### <a name="applying-texture-coordinate-offsets"></a><span data-ttu-id="b6b31-162">Aplicar desplazamientos de coordenadas de textura</span><span class="sxs-lookup"><span data-stu-id="b6b31-162">Applying Texture Coordinate Offsets</span></span>

<span data-ttu-id="b6b31-163">El parámetro offset modifica las coordenadas de textura, en el espacio textura.</span><span class="sxs-lookup"><span data-stu-id="b6b31-163">The offset parameter modifies the texture coordinates, in texel space.</span></span> <span data-ttu-id="b6b31-164">Aunque las coordenadas de textura son números de punto flotante normalizados, el desplazamiento aplica un desplazamiento entero.</span><span class="sxs-lookup"><span data-stu-id="b6b31-164">Even though texture coordinates are normalized floating-point numbers, the offset applies an integer offset.</span></span> <span data-ttu-id="b6b31-165">Tenga en cuenta también que los desplazamientos de textura deben ser estáticos.</span><span class="sxs-lookup"><span data-stu-id="b6b31-165">Also note that the texture offsets need to be static.</span></span>

<span data-ttu-id="b6b31-166">El formato de datos devuelto viene determinado por el formato de textura.</span><span class="sxs-lookup"><span data-stu-id="b6b31-166">The data format returned is determined by the texture format.</span></span> <span data-ttu-id="b6b31-167">Por ejemplo, si el recurso de textura se definió con el formato de DXGI \_ \_ A8B8G8R8 \_ UNORM \_ sRGB, la operación de muestreo convierte textura muestreadas de gamma 2,0 a 1,0, filtrar y escribe el resultado como un valor de punto flotante en el intervalo \[ 0.. 1 \] .</span><span class="sxs-lookup"><span data-stu-id="b6b31-167">For example, if the texture resource was defined with the DXGI\_FORMAT\_A8B8G8R8\_UNORM\_SRGB format, the sampling operation converts sampled texels from gamma 2.0 to 1.0, filter, and writes the result as a floating-point value in the range \[0..1\].</span></span>

## <a name="see-also"></a><span data-ttu-id="b6b31-168">Vea también</span><span class="sxs-lookup"><span data-stu-id="b6b31-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6b31-169">Métodos de ejemplo</span><span class="sxs-lookup"><span data-stu-id="b6b31-169">Sample methods</span></span>](texture-sample-overload.md)
</dt> <dt>

[<span data-ttu-id="b6b31-170">Texture-objeto</span><span class="sxs-lookup"><span data-stu-id="b6b31-170">Texture-Object</span></span>](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

 
