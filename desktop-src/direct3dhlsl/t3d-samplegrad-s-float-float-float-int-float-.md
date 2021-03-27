---
title: 'Función SampleGrad:: SampleGrad (S, Float, Float, Float, int, float) para Texture3D'
description: Muestrea una textura, utilizando un degradado para influir en la forma en que se calcula la ubicación de ejemplo, con un valor opcional para Clamp valores de nivel de detalle (LOD) de ejemplo. Para Texture3D.
ms.assetid: F59D54F8-CC9E-47F8-97DD-735C70939C07
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
ms.openlocfilehash: 6d0bd1c47a82784b2b96a93a7f43ecd158e4782a
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/16/2021
ms.locfileid: "104987331"
---
# <a name="samplegradsamplegradsfloatfloatfloatintfloat-function-for-texture3d"></a><span data-ttu-id="2c026-105">Función SampleGrad:: SampleGrad (S, Float, Float, Float, int, float) para Texture3D</span><span class="sxs-lookup"><span data-stu-id="2c026-105">SampleGrad::SampleGrad(S,float,float,float,int,float) function for Texture3D</span></span>

<span data-ttu-id="2c026-106">Muestrea una textura, utilizando un degradado para influir en la forma en que se calcula la ubicación de ejemplo, con un valor opcional para Clamp valores de nivel de detalle (LOD) de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="2c026-106">Samples a texture, using a gradient to influence the way the sample location is calculated, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c026-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2c026-107">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="2c026-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2c026-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c026-109">*S* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="2c026-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2c026-110">Tipo: **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="2c026-110">Type: **SamplerState**</span></span>

<span data-ttu-id="2c026-111">Un [Estado de muestra](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="2c026-111">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="2c026-112">Se trata de un objeto declarado en un archivo de efectos que contiene las asignaciones de estado.</span><span class="sxs-lookup"><span data-stu-id="2c026-112">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="2c026-113">*Ubicación* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="2c026-113">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2c026-114">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="2c026-114">Type: **float**</span></span>

<span data-ttu-id="2c026-115">Las coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="2c026-115">The texture coordinates.</span></span> <span data-ttu-id="2c026-116">El tipo de argumento depende del tipo de objeto de textura.</span><span class="sxs-lookup"><span data-stu-id="2c026-116">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="2c026-117">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="2c026-117">Texture-Object Type</span></span>                    | <span data-ttu-id="2c026-118">Tipo de parámetro</span><span class="sxs-lookup"><span data-stu-id="2c026-118">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="2c026-119">Texture1D</span><span class="sxs-lookup"><span data-stu-id="2c026-119">Texture1D</span></span>                              | <span data-ttu-id="2c026-120">FLOAT</span><span class="sxs-lookup"><span data-stu-id="2c026-120">float</span></span>          |
| <span data-ttu-id="2c026-121">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="2c026-121">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="2c026-122">float2</span><span class="sxs-lookup"><span data-stu-id="2c026-122">float2</span></span>         |
| <span data-ttu-id="2c026-123">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="2c026-123">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="2c026-124">float3</span><span class="sxs-lookup"><span data-stu-id="2c026-124">float3</span></span>         |
| <span data-ttu-id="2c026-125">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="2c026-125">TextureCubeArray</span></span>                       | <span data-ttu-id="2c026-126">float4</span><span class="sxs-lookup"><span data-stu-id="2c026-126">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="2c026-127">*DDX* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="2c026-127">*DDX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2c026-128">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="2c026-128">Type: **float**</span></span>

<span data-ttu-id="2c026-129">La tasa de cambio de la geometría de la superficie en la dirección x.</span><span class="sxs-lookup"><span data-stu-id="2c026-129">The rate of change of the surface geometry in the x direction.</span></span> <span data-ttu-id="2c026-130">El tipo de argumento depende del tipo de objeto de textura.</span><span class="sxs-lookup"><span data-stu-id="2c026-130">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="2c026-131">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="2c026-131">Texture-Object Type</span></span>                      | <span data-ttu-id="2c026-132">Tipo de parámetro</span><span class="sxs-lookup"><span data-stu-id="2c026-132">Parameter Type</span></span> |
|------------------------------------------|----------------|
| <span data-ttu-id="2c026-133">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="2c026-133">Texture1D, Texture1DArray</span></span>                | <span data-ttu-id="2c026-134">FLOAT</span><span class="sxs-lookup"><span data-stu-id="2c026-134">float</span></span>          |
| <span data-ttu-id="2c026-135">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="2c026-135">Texture2D, Texture2DArray</span></span>                | <span data-ttu-id="2c026-136">float2</span><span class="sxs-lookup"><span data-stu-id="2c026-136">float2</span></span>         |
| <span data-ttu-id="2c026-137">Texture3D, TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="2c026-137">Texture3D, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="2c026-138">float3</span><span class="sxs-lookup"><span data-stu-id="2c026-138">float3</span></span>         |
| <span data-ttu-id="2c026-139">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="2c026-139">Texture2DMS, Texture2DMSArray</span></span>            | <span data-ttu-id="2c026-140">no admitido</span><span class="sxs-lookup"><span data-stu-id="2c026-140">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="2c026-141">*DDY* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2c026-141">*DDY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2c026-142">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="2c026-142">Type: **float**</span></span>

<span data-ttu-id="2c026-143">La tasa de cambio de la geometría de la superficie en la dirección y.</span><span class="sxs-lookup"><span data-stu-id="2c026-143">The rate of change of the surface geometry in the y direction.</span></span> <span data-ttu-id="2c026-144">El tipo de argumento depende del tipo de objeto de textura.</span><span class="sxs-lookup"><span data-stu-id="2c026-144">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="2c026-145">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="2c026-145">Texture-Object Type</span></span>                      | <span data-ttu-id="2c026-146">Tipo de parámetro</span><span class="sxs-lookup"><span data-stu-id="2c026-146">Parameter Type</span></span> |
|------------------------------------------|----------------|
| <span data-ttu-id="2c026-147">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="2c026-147">Texture1D, Texture1DArray</span></span>                | <span data-ttu-id="2c026-148">FLOAT</span><span class="sxs-lookup"><span data-stu-id="2c026-148">float</span></span>          |
| <span data-ttu-id="2c026-149">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="2c026-149">Texture2D, Texture2DArray</span></span>                | <span data-ttu-id="2c026-150">float2</span><span class="sxs-lookup"><span data-stu-id="2c026-150">float2</span></span>         |
| <span data-ttu-id="2c026-151">Texture3D, TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="2c026-151">Texture3D, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="2c026-152">float3</span><span class="sxs-lookup"><span data-stu-id="2c026-152">float3</span></span>         |
| <span data-ttu-id="2c026-153">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="2c026-153">Texture2DMS, Texture2DMSArray</span></span>            | <span data-ttu-id="2c026-154">no admitido</span><span class="sxs-lookup"><span data-stu-id="2c026-154">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="2c026-155">*Desplazamiento* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2c026-155">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2c026-156">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="2c026-156">Type: **int**</span></span>

<span data-ttu-id="2c026-157">Desplazamiento de coordenadas de textura opcional, que se puede usar para cualquier tipo de objeto de textura. el desplazamiento se aplica a la ubicación antes del muestreo.</span><span class="sxs-lookup"><span data-stu-id="2c026-157">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="2c026-158">Use un desplazamiento solo en un entero miplevel; de lo contrario, puede obtener resultados que no se traduzcan bien al hardware.</span><span class="sxs-lookup"><span data-stu-id="2c026-158">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="2c026-159">El tipo de argumento depende del tipo de objeto de textura.</span><span class="sxs-lookup"><span data-stu-id="2c026-159">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="2c026-160">Para obtener más información, vea [aplicar desplazamientos enteros](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="2c026-160">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="2c026-161">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="2c026-161">Texture-Object Type</span></span>           | <span data-ttu-id="2c026-162">Tipo de parámetro</span><span class="sxs-lookup"><span data-stu-id="2c026-162">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="2c026-163">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="2c026-163">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="2c026-164">int</span><span class="sxs-lookup"><span data-stu-id="2c026-164">int</span></span>            |
| <span data-ttu-id="2c026-165">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="2c026-165">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="2c026-166">int2</span><span class="sxs-lookup"><span data-stu-id="2c026-166">int2</span></span>           |
| <span data-ttu-id="2c026-167">Texture3D</span><span class="sxs-lookup"><span data-stu-id="2c026-167">Texture3D</span></span>                     | <span data-ttu-id="2c026-168">int3</span><span class="sxs-lookup"><span data-stu-id="2c026-168">int3</span></span>           |
| <span data-ttu-id="2c026-169">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="2c026-169">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="2c026-170">no admitido</span><span class="sxs-lookup"><span data-stu-id="2c026-170">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="2c026-171">*Abrazadera* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2c026-171">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2c026-172">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="2c026-172">Type: **float**</span></span>

<span data-ttu-id="2c026-173">Un valor opcional en el que se van a fijar los valores LOD de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="2c026-173">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="2c026-174">Por ejemplo, si se pasa 2.0 f para el valor Clamp, se asegura de que ningún ejemplo individual tenga acceso a un nivel de MIP inferior a 2.0 f.</span><span class="sxs-lookup"><span data-stu-id="2c026-174">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c026-175">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2c026-175">Return value</span></span>

<span data-ttu-id="2c026-176">Tipo: **[ **\_ formato de DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="2c026-176">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="2c026-177">Formato de textura, que es uno de los valores con tipo que aparecen [**en \_ formato de DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="2c026-177">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="2c026-178">Vea también</span><span class="sxs-lookup"><span data-stu-id="2c026-178">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c026-179">Métodos SampleGrad</span><span class="sxs-lookup"><span data-stu-id="2c026-179">SampleGrad methods</span></span>](texture3d-samplegrad.md)
</dt> <dt>

[<span data-ttu-id="2c026-180">**Texture3D**</span><span class="sxs-lookup"><span data-stu-id="2c026-180">**Texture3D**</span></span>](sm5-object-texture3d.md)
</dt> </dl>

 

 
