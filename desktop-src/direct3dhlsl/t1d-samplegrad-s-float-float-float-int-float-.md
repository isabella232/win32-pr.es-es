---
title: 'Función SampleGrad:: SampleGrad (S, Float, Float, Float, int, float) para Texture1D'
description: La función muestrea una textura, utilizando un degradado para influir en la forma en que se calcula la ubicación de ejemplo, con un valor opcional para Clamp valores de nivel de detalle (LOD) de ejemplo en.
ms.assetid: 34A79CB6-0C45-40ED-845C-77C08F1DEC57
keywords:
- SampleGrad de función HLSL
topic_type:
- apiref
api_name:
- SampleGrad
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8c6222d8fa9548e3154abf7605fc5032dd67235a
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/16/2021
ms.locfileid: "104987349"
---
# <a name="samplegradsamplegradsfloatfloatfloatintfloat-function-for-texture1d"></a><span data-ttu-id="3a279-104">Función SampleGrad:: SampleGrad (S, Float, Float, Float, int, float) para Texture1D</span><span class="sxs-lookup"><span data-stu-id="3a279-104">SampleGrad::SampleGrad(S,float,float,float,int,float) function for Texture1D</span></span>

<span data-ttu-id="3a279-105">Muestrea una textura, utilizando un degradado para influir en la forma en que se calcula la ubicación de ejemplo, con un valor opcional para Clamp valores de nivel de detalle (LOD) de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="3a279-105">Samples a texture, using a gradient to influence the way the sample location is calculated, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a279-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3a279-106">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleGrad(
  in SamplerState S,
  in float        Location,
  in float        DDX,
  in float        DDY,
  in int          Offset,
  in float        Clamp
);
```



## <a name="parameters"></a><span data-ttu-id="3a279-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3a279-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a279-108">*S* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="3a279-108">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a279-109">Tipo: **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="3a279-109">Type: **SamplerState**</span></span>

<span data-ttu-id="3a279-110">Un [Estado de muestra](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="3a279-110">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="3a279-111">Se trata de un objeto declarado en un archivo de efectos que contiene las asignaciones de estado.</span><span class="sxs-lookup"><span data-stu-id="3a279-111">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="3a279-112">*Ubicación* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="3a279-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a279-113">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="3a279-113">Type: **float**</span></span>

<span data-ttu-id="3a279-114">Las coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="3a279-114">The texture coordinates.</span></span> <span data-ttu-id="3a279-115">El tipo de argumento depende del tipo de objeto de textura.</span><span class="sxs-lookup"><span data-stu-id="3a279-115">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="3a279-116">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="3a279-116">Texture-Object Type</span></span>                    | <span data-ttu-id="3a279-117">Tipo de parámetro</span><span class="sxs-lookup"><span data-stu-id="3a279-117">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="3a279-118">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3a279-118">Texture1D</span></span>                              | <span data-ttu-id="3a279-119">FLOAT</span><span class="sxs-lookup"><span data-stu-id="3a279-119">float</span></span>          |
| <span data-ttu-id="3a279-120">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="3a279-120">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="3a279-121">float2</span><span class="sxs-lookup"><span data-stu-id="3a279-121">float2</span></span>         |
| <span data-ttu-id="3a279-122">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="3a279-122">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="3a279-123">float3</span><span class="sxs-lookup"><span data-stu-id="3a279-123">float3</span></span>         |
| <span data-ttu-id="3a279-124">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="3a279-124">TextureCubeArray</span></span>                       | <span data-ttu-id="3a279-125">float4</span><span class="sxs-lookup"><span data-stu-id="3a279-125">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="3a279-126">*DDX* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="3a279-126">*DDX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a279-127">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="3a279-127">Type: **float**</span></span>

<span data-ttu-id="3a279-128">La tasa de cambio de la geometría de la superficie en la dirección x.</span><span class="sxs-lookup"><span data-stu-id="3a279-128">The rate of change of the surface geometry in the x direction.</span></span> <span data-ttu-id="3a279-129">El tipo de argumento depende del tipo de objeto de textura.</span><span class="sxs-lookup"><span data-stu-id="3a279-129">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="3a279-130">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="3a279-130">Texture-Object Type</span></span>                      | <span data-ttu-id="3a279-131">Tipo de parámetro</span><span class="sxs-lookup"><span data-stu-id="3a279-131">Parameter Type</span></span> |
|------------------------------------------|----------------|
| <span data-ttu-id="3a279-132">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="3a279-132">Texture1D, Texture1DArray</span></span>                | <span data-ttu-id="3a279-133">FLOAT</span><span class="sxs-lookup"><span data-stu-id="3a279-133">float</span></span>          |
| <span data-ttu-id="3a279-134">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="3a279-134">Texture2D, Texture2DArray</span></span>                | <span data-ttu-id="3a279-135">float2</span><span class="sxs-lookup"><span data-stu-id="3a279-135">float2</span></span>         |
| <span data-ttu-id="3a279-136">Texture3D, TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="3a279-136">Texture3D, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="3a279-137">float3</span><span class="sxs-lookup"><span data-stu-id="3a279-137">float3</span></span>         |
| <span data-ttu-id="3a279-138">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="3a279-138">Texture2DMS, Texture2DMSArray</span></span>            | <span data-ttu-id="3a279-139">no admitido</span><span class="sxs-lookup"><span data-stu-id="3a279-139">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="3a279-140">*DDY* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3a279-140">*DDY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a279-141">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="3a279-141">Type: **float**</span></span>

<span data-ttu-id="3a279-142">La tasa de cambio de la geometría de la superficie en la dirección y.</span><span class="sxs-lookup"><span data-stu-id="3a279-142">The rate of change of the surface geometry in the y direction.</span></span> <span data-ttu-id="3a279-143">El tipo de argumento depende del tipo de objeto de textura.</span><span class="sxs-lookup"><span data-stu-id="3a279-143">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="3a279-144">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="3a279-144">Texture-Object Type</span></span>                      | <span data-ttu-id="3a279-145">Tipo de parámetro</span><span class="sxs-lookup"><span data-stu-id="3a279-145">Parameter Type</span></span> |
|------------------------------------------|----------------|
| <span data-ttu-id="3a279-146">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="3a279-146">Texture1D, Texture1DArray</span></span>                | <span data-ttu-id="3a279-147">FLOAT</span><span class="sxs-lookup"><span data-stu-id="3a279-147">float</span></span>          |
| <span data-ttu-id="3a279-148">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="3a279-148">Texture2D, Texture2DArray</span></span>                | <span data-ttu-id="3a279-149">float2</span><span class="sxs-lookup"><span data-stu-id="3a279-149">float2</span></span>         |
| <span data-ttu-id="3a279-150">Texture3D, TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="3a279-150">Texture3D, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="3a279-151">float3</span><span class="sxs-lookup"><span data-stu-id="3a279-151">float3</span></span>         |
| <span data-ttu-id="3a279-152">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="3a279-152">Texture2DMS, Texture2DMSArray</span></span>            | <span data-ttu-id="3a279-153">no admitido</span><span class="sxs-lookup"><span data-stu-id="3a279-153">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="3a279-154">*Desplazamiento* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3a279-154">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a279-155">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="3a279-155">Type: **int**</span></span>

<span data-ttu-id="3a279-156">Desplazamiento de coordenadas de textura opcional, que se puede usar para cualquier tipo de objeto de textura. el desplazamiento se aplica a la ubicación antes del muestreo.</span><span class="sxs-lookup"><span data-stu-id="3a279-156">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="3a279-157">Use un desplazamiento solo en un entero miplevel; de lo contrario, puede obtener resultados que no se traduzcan bien al hardware.</span><span class="sxs-lookup"><span data-stu-id="3a279-157">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="3a279-158">El tipo de argumento depende del tipo de objeto de textura.</span><span class="sxs-lookup"><span data-stu-id="3a279-158">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="3a279-159">Para obtener más información, vea [aplicar desplazamientos enteros](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="3a279-159">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="3a279-160">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="3a279-160">Texture-Object Type</span></span>           | <span data-ttu-id="3a279-161">Tipo de parámetro</span><span class="sxs-lookup"><span data-stu-id="3a279-161">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="3a279-162">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="3a279-162">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="3a279-163">int</span><span class="sxs-lookup"><span data-stu-id="3a279-163">int</span></span>            |
| <span data-ttu-id="3a279-164">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="3a279-164">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="3a279-165">int2</span><span class="sxs-lookup"><span data-stu-id="3a279-165">int2</span></span>           |
| <span data-ttu-id="3a279-166">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3a279-166">Texture3D</span></span>                     | <span data-ttu-id="3a279-167">int3</span><span class="sxs-lookup"><span data-stu-id="3a279-167">int3</span></span>           |
| <span data-ttu-id="3a279-168">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="3a279-168">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="3a279-169">no admitido</span><span class="sxs-lookup"><span data-stu-id="3a279-169">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="3a279-170">*Abrazadera* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3a279-170">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a279-171">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="3a279-171">Type: **float**</span></span>

<span data-ttu-id="3a279-172">Un valor opcional en el que se van a fijar los valores LOD de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="3a279-172">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="3a279-173">Por ejemplo, si se pasa 2.0 f para el valor Clamp, se asegura de que ningún ejemplo individual tenga acceso a un nivel de MIP inferior a 2.0 f.</span><span class="sxs-lookup"><span data-stu-id="3a279-173">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a279-174">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3a279-174">Return value</span></span>

<span data-ttu-id="3a279-175">Tipo: **[ **\_ formato de DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="3a279-175">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="3a279-176">Formato de textura, que es uno de los valores con tipo que aparecen [**en \_ formato de DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="3a279-176">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="3a279-177">Vea también</span><span class="sxs-lookup"><span data-stu-id="3a279-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a279-178">Métodos SampleGrad</span><span class="sxs-lookup"><span data-stu-id="3a279-178">SampleGrad methods</span></span>](texture1d-samplegrad.md)
</dt> </dl>

 

 
