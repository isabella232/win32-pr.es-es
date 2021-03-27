---
title: 'Función SampleGrad:: SampleGrad (S, Float, Float, Float, int, float) para Texture2DArray'
description: Obtenga información sobre cómo esta función muestra una textura mediante un degradado para influir en la forma en que se calcula la ubicación de ejemplo, con un valor opcional para Clamp valores de nivel de detalle (LOD) de ejemplo en. Para Texture2DArray.
ms.assetid: CBC940D5-FC09-498D-9C7A-3CBAB2EC2D4D
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
ms.openlocfilehash: 032d2b228800ffca654704c85a72d5ada76e65ef
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/16/2021
ms.locfileid: "104987361"
---
# <a name="samplegradsamplegradsfloatfloatfloatintfloat-function-for-texture2darray"></a><span data-ttu-id="bb4a3-105">Función SampleGrad:: SampleGrad (S, Float, Float, Float, int, float) para Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="bb4a3-105">SampleGrad::SampleGrad(S,float,float,float,int,float) function for Texture2DArray</span></span>

<span data-ttu-id="bb4a3-106">Muestrea una textura, utilizando un degradado para influir en la forma en que se calcula la ubicación de ejemplo, con un valor opcional para Clamp valores de nivel de detalle (LOD) de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="bb4a3-106">Samples a texture, using a gradient to influence the way the sample location is calculated, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb4a3-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bb4a3-107">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="bb4a3-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bb4a3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb4a3-109">*S* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="bb4a3-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb4a3-110">Tipo: **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="bb4a3-110">Type: **SamplerState**</span></span>

<span data-ttu-id="bb4a3-111">Un [Estado de muestra](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="bb4a3-111">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="bb4a3-112">Se trata de un objeto declarado en un archivo de efectos que contiene las asignaciones de estado.</span><span class="sxs-lookup"><span data-stu-id="bb4a3-112">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="bb4a3-113">*Ubicación* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="bb4a3-113">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb4a3-114">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="bb4a3-114">Type: **float**</span></span>

<span data-ttu-id="bb4a3-115">Las coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="bb4a3-115">The texture coordinates.</span></span> <span data-ttu-id="bb4a3-116">El tipo de argumento depende del tipo de objeto de textura.</span><span class="sxs-lookup"><span data-stu-id="bb4a3-116">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="bb4a3-117">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="bb4a3-117">Texture-Object Type</span></span>                    | <span data-ttu-id="bb4a3-118">Tipo de parámetro</span><span class="sxs-lookup"><span data-stu-id="bb4a3-118">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="bb4a3-119">Texture1D</span><span class="sxs-lookup"><span data-stu-id="bb4a3-119">Texture1D</span></span>                              | <span data-ttu-id="bb4a3-120">FLOAT</span><span class="sxs-lookup"><span data-stu-id="bb4a3-120">float</span></span>          |
| <span data-ttu-id="bb4a3-121">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="bb4a3-121">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="bb4a3-122">float2</span><span class="sxs-lookup"><span data-stu-id="bb4a3-122">float2</span></span>         |
| <span data-ttu-id="bb4a3-123">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="bb4a3-123">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="bb4a3-124">float3</span><span class="sxs-lookup"><span data-stu-id="bb4a3-124">float3</span></span>         |
| <span data-ttu-id="bb4a3-125">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="bb4a3-125">TextureCubeArray</span></span>                       | <span data-ttu-id="bb4a3-126">float4</span><span class="sxs-lookup"><span data-stu-id="bb4a3-126">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="bb4a3-127">*DDX* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="bb4a3-127">*DDX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb4a3-128">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="bb4a3-128">Type: **float**</span></span>

<span data-ttu-id="bb4a3-129">La tasa de cambio de la geometría de la superficie en la dirección x.</span><span class="sxs-lookup"><span data-stu-id="bb4a3-129">The rate of change of the surface geometry in the x direction.</span></span> <span data-ttu-id="bb4a3-130">El tipo de argumento depende del tipo de objeto de textura.</span><span class="sxs-lookup"><span data-stu-id="bb4a3-130">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="bb4a3-131">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="bb4a3-131">Texture-Object Type</span></span>                      | <span data-ttu-id="bb4a3-132">Tipo de parámetro</span><span class="sxs-lookup"><span data-stu-id="bb4a3-132">Parameter Type</span></span> |
|------------------------------------------|----------------|
| <span data-ttu-id="bb4a3-133">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="bb4a3-133">Texture1D, Texture1DArray</span></span>                | <span data-ttu-id="bb4a3-134">FLOAT</span><span class="sxs-lookup"><span data-stu-id="bb4a3-134">float</span></span>          |
| <span data-ttu-id="bb4a3-135">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="bb4a3-135">Texture2D, Texture2DArray</span></span>                | <span data-ttu-id="bb4a3-136">float2</span><span class="sxs-lookup"><span data-stu-id="bb4a3-136">float2</span></span>         |
| <span data-ttu-id="bb4a3-137">Texture3D, TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="bb4a3-137">Texture3D, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="bb4a3-138">float3</span><span class="sxs-lookup"><span data-stu-id="bb4a3-138">float3</span></span>         |
| <span data-ttu-id="bb4a3-139">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="bb4a3-139">Texture2DMS, Texture2DMSArray</span></span>            | <span data-ttu-id="bb4a3-140">no admitido</span><span class="sxs-lookup"><span data-stu-id="bb4a3-140">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="bb4a3-141">*DDY* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="bb4a3-141">*DDY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb4a3-142">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="bb4a3-142">Type: **float**</span></span>

<span data-ttu-id="bb4a3-143">La tasa de cambio de la geometría de la superficie en la dirección y.</span><span class="sxs-lookup"><span data-stu-id="bb4a3-143">The rate of change of the surface geometry in the y direction.</span></span> <span data-ttu-id="bb4a3-144">El tipo de argumento depende del tipo de objeto de textura.</span><span class="sxs-lookup"><span data-stu-id="bb4a3-144">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="bb4a3-145">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="bb4a3-145">Texture-Object Type</span></span>                      | <span data-ttu-id="bb4a3-146">Tipo de parámetro</span><span class="sxs-lookup"><span data-stu-id="bb4a3-146">Parameter Type</span></span> |
|------------------------------------------|----------------|
| <span data-ttu-id="bb4a3-147">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="bb4a3-147">Texture1D, Texture1DArray</span></span>                | <span data-ttu-id="bb4a3-148">FLOAT</span><span class="sxs-lookup"><span data-stu-id="bb4a3-148">float</span></span>          |
| <span data-ttu-id="bb4a3-149">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="bb4a3-149">Texture2D, Texture2DArray</span></span>                | <span data-ttu-id="bb4a3-150">float2</span><span class="sxs-lookup"><span data-stu-id="bb4a3-150">float2</span></span>         |
| <span data-ttu-id="bb4a3-151">Texture3D, TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="bb4a3-151">Texture3D, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="bb4a3-152">float3</span><span class="sxs-lookup"><span data-stu-id="bb4a3-152">float3</span></span>         |
| <span data-ttu-id="bb4a3-153">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="bb4a3-153">Texture2DMS, Texture2DMSArray</span></span>            | <span data-ttu-id="bb4a3-154">no admitido</span><span class="sxs-lookup"><span data-stu-id="bb4a3-154">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="bb4a3-155">*Desplazamiento* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="bb4a3-155">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb4a3-156">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="bb4a3-156">Type: **int**</span></span>

<span data-ttu-id="bb4a3-157">Desplazamiento de coordenadas de textura opcional, que se puede usar para cualquier tipo de objeto de textura. el desplazamiento se aplica a la ubicación antes del muestreo.</span><span class="sxs-lookup"><span data-stu-id="bb4a3-157">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="bb4a3-158">Use un desplazamiento solo en un entero miplevel; de lo contrario, puede obtener resultados que no se traduzcan bien al hardware.</span><span class="sxs-lookup"><span data-stu-id="bb4a3-158">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="bb4a3-159">El tipo de argumento depende del tipo de objeto de textura.</span><span class="sxs-lookup"><span data-stu-id="bb4a3-159">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="bb4a3-160">Para obtener más información, vea [aplicar desplazamientos enteros](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="bb4a3-160">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="bb4a3-161">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="bb4a3-161">Texture-Object Type</span></span>           | <span data-ttu-id="bb4a3-162">Tipo de parámetro</span><span class="sxs-lookup"><span data-stu-id="bb4a3-162">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="bb4a3-163">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="bb4a3-163">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="bb4a3-164">int</span><span class="sxs-lookup"><span data-stu-id="bb4a3-164">int</span></span>            |
| <span data-ttu-id="bb4a3-165">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="bb4a3-165">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="bb4a3-166">int2</span><span class="sxs-lookup"><span data-stu-id="bb4a3-166">int2</span></span>           |
| <span data-ttu-id="bb4a3-167">Texture3D</span><span class="sxs-lookup"><span data-stu-id="bb4a3-167">Texture3D</span></span>                     | <span data-ttu-id="bb4a3-168">int3</span><span class="sxs-lookup"><span data-stu-id="bb4a3-168">int3</span></span>           |
| <span data-ttu-id="bb4a3-169">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="bb4a3-169">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="bb4a3-170">no admitido</span><span class="sxs-lookup"><span data-stu-id="bb4a3-170">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="bb4a3-171">*Abrazadera* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="bb4a3-171">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb4a3-172">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="bb4a3-172">Type: **float**</span></span>

<span data-ttu-id="bb4a3-173">Un valor opcional en el que se van a fijar los valores LOD de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="bb4a3-173">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="bb4a3-174">Por ejemplo, si se pasa 2.0 f para el valor Clamp, se asegura de que ningún ejemplo individual tenga acceso a un nivel de MIP inferior a 2.0 f.</span><span class="sxs-lookup"><span data-stu-id="bb4a3-174">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb4a3-175">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bb4a3-175">Return value</span></span>

<span data-ttu-id="bb4a3-176">Tipo: **[ **\_ formato de DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="bb4a3-176">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="bb4a3-177">Formato de textura, que es uno de los valores con tipo que aparecen [**en \_ formato de DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="bb4a3-177">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="bb4a3-178">Vea también</span><span class="sxs-lookup"><span data-stu-id="bb4a3-178">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb4a3-179">Métodos SampleGrad</span><span class="sxs-lookup"><span data-stu-id="bb4a3-179">SampleGrad methods</span></span>](texture2darray-samplegrad.md)
</dt> <dt>

[<span data-ttu-id="bb4a3-180">**Texture2DArray**</span><span class="sxs-lookup"><span data-stu-id="bb4a3-180">**Texture2DArray**</span></span>](sm5-object-texture2darray.md)
</dt> </dl>

 

 
