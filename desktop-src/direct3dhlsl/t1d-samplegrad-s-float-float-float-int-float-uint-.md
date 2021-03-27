---
title: 'Función SampleGrad:: SampleGrad (S, Float, Float, Float, int, Float, uint) para Texture1D'
description: Muestrea una textura, utilizando un degradado para influir en la forma en que se calcula la ubicación de ejemplo, con un valor opcional para Clamp valores de nivel de detalle (LOD) de ejemplo. Para Texture1D.
ms.assetid: E2B131AC-99E6-493A-91EE-EB0D3EE7FA8B
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
ms.openlocfilehash: 3a5f95a87f46e94c971dd19989ffa670e6993e8f
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/16/2021
ms.locfileid: "104003998"
---
# <a name="samplegradsamplegradsfloatfloatfloatintfloatuint-function-for-texture1d"></a><span data-ttu-id="c1c47-105">Función SampleGrad:: SampleGrad (S, Float, Float, Float, int, Float, uint) para Texture1D</span><span class="sxs-lookup"><span data-stu-id="c1c47-105">SampleGrad::SampleGrad(S,float,float,float,int,float,uint) function for Texture1D</span></span>

<span data-ttu-id="c1c47-106">Muestrea una textura, utilizando un degradado para influir en la forma en que se calcula la ubicación de ejemplo, con un valor opcional para Clamp valores de nivel de detalle (LOD) de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="c1c47-106">Samples a texture, using a gradient to influence the way the sample location is calculated, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span> <span data-ttu-id="c1c47-107">Devuelve el estado de la operación.</span><span class="sxs-lookup"><span data-stu-id="c1c47-107">Returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1c47-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c1c47-108">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleGrad(
  in  SamplerState S,
  in  float        Location,
  in  float        DDX,
  in  float        DDY,
  in  int          Offset,
  in  float        Clamp,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="c1c47-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c1c47-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1c47-110">*S* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="c1c47-110">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1c47-111">Tipo: **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="c1c47-111">Type: **SamplerState**</span></span>

<span data-ttu-id="c1c47-112">Un [Estado de muestra](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="c1c47-112">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="c1c47-113">Se trata de un objeto declarado en un archivo de efectos que contiene las asignaciones de estado.</span><span class="sxs-lookup"><span data-stu-id="c1c47-113">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="c1c47-114">*Ubicación* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="c1c47-114">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1c47-115">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="c1c47-115">Type: **float**</span></span>

<span data-ttu-id="c1c47-116">Las coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="c1c47-116">The texture coordinates.</span></span> <span data-ttu-id="c1c47-117">El tipo de argumento depende del tipo de objeto de textura.</span><span class="sxs-lookup"><span data-stu-id="c1c47-117">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="c1c47-118">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="c1c47-118">Texture-Object Type</span></span>                    | <span data-ttu-id="c1c47-119">Tipo de parámetro</span><span class="sxs-lookup"><span data-stu-id="c1c47-119">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="c1c47-120">Texture1D</span><span class="sxs-lookup"><span data-stu-id="c1c47-120">Texture1D</span></span>                              | <span data-ttu-id="c1c47-121">FLOAT</span><span class="sxs-lookup"><span data-stu-id="c1c47-121">float</span></span>          |
| <span data-ttu-id="c1c47-122">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="c1c47-122">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="c1c47-123">float2</span><span class="sxs-lookup"><span data-stu-id="c1c47-123">float2</span></span>         |
| <span data-ttu-id="c1c47-124">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="c1c47-124">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="c1c47-125">float3</span><span class="sxs-lookup"><span data-stu-id="c1c47-125">float3</span></span>         |
| <span data-ttu-id="c1c47-126">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="c1c47-126">TextureCubeArray</span></span>                       | <span data-ttu-id="c1c47-127">float4</span><span class="sxs-lookup"><span data-stu-id="c1c47-127">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="c1c47-128">*DDX* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="c1c47-128">*DDX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1c47-129">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="c1c47-129">Type: **float**</span></span>

<span data-ttu-id="c1c47-130">La tasa de cambio de la geometría de la superficie en la dirección x.</span><span class="sxs-lookup"><span data-stu-id="c1c47-130">The rate of change of the surface geometry in the x direction.</span></span> <span data-ttu-id="c1c47-131">El tipo de argumento depende del tipo de objeto de textura.</span><span class="sxs-lookup"><span data-stu-id="c1c47-131">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="c1c47-132">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="c1c47-132">Texture-Object Type</span></span>                      | <span data-ttu-id="c1c47-133">Tipo de parámetro</span><span class="sxs-lookup"><span data-stu-id="c1c47-133">Parameter Type</span></span> |
|------------------------------------------|----------------|
| <span data-ttu-id="c1c47-134">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="c1c47-134">Texture1D, Texture1DArray</span></span>                | <span data-ttu-id="c1c47-135">FLOAT</span><span class="sxs-lookup"><span data-stu-id="c1c47-135">float</span></span>          |
| <span data-ttu-id="c1c47-136">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="c1c47-136">Texture2D, Texture2DArray</span></span>                | <span data-ttu-id="c1c47-137">float2</span><span class="sxs-lookup"><span data-stu-id="c1c47-137">float2</span></span>         |
| <span data-ttu-id="c1c47-138">Texture3D, TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="c1c47-138">Texture3D, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="c1c47-139">float3</span><span class="sxs-lookup"><span data-stu-id="c1c47-139">float3</span></span>         |
| <span data-ttu-id="c1c47-140">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="c1c47-140">Texture2DMS, Texture2DMSArray</span></span>            | <span data-ttu-id="c1c47-141">no admitido</span><span class="sxs-lookup"><span data-stu-id="c1c47-141">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="c1c47-142">*DDY* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c1c47-142">*DDY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1c47-143">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="c1c47-143">Type: **float**</span></span>

<span data-ttu-id="c1c47-144">La tasa de cambio de la geometría de la superficie en la dirección y.</span><span class="sxs-lookup"><span data-stu-id="c1c47-144">The rate of change of the surface geometry in the y direction.</span></span> <span data-ttu-id="c1c47-145">El tipo de argumento depende del tipo de objeto de textura.</span><span class="sxs-lookup"><span data-stu-id="c1c47-145">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="c1c47-146">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="c1c47-146">Texture-Object Type</span></span>                      | <span data-ttu-id="c1c47-147">Tipo de parámetro</span><span class="sxs-lookup"><span data-stu-id="c1c47-147">Parameter Type</span></span> |
|------------------------------------------|----------------|
| <span data-ttu-id="c1c47-148">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="c1c47-148">Texture1D, Texture1DArray</span></span>                | <span data-ttu-id="c1c47-149">FLOAT</span><span class="sxs-lookup"><span data-stu-id="c1c47-149">float</span></span>          |
| <span data-ttu-id="c1c47-150">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="c1c47-150">Texture2D, Texture2DArray</span></span>                | <span data-ttu-id="c1c47-151">float2</span><span class="sxs-lookup"><span data-stu-id="c1c47-151">float2</span></span>         |
| <span data-ttu-id="c1c47-152">Texture3D, TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="c1c47-152">Texture3D, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="c1c47-153">float3</span><span class="sxs-lookup"><span data-stu-id="c1c47-153">float3</span></span>         |
| <span data-ttu-id="c1c47-154">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="c1c47-154">Texture2DMS, Texture2DMSArray</span></span>            | <span data-ttu-id="c1c47-155">no admitido</span><span class="sxs-lookup"><span data-stu-id="c1c47-155">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="c1c47-156">*Desplazamiento* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c1c47-156">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1c47-157">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="c1c47-157">Type: **int**</span></span>

<span data-ttu-id="c1c47-158">Desplazamiento de coordenadas de textura opcional, que se puede usar para cualquier tipo de objeto de textura. el desplazamiento se aplica a la ubicación antes del muestreo.</span><span class="sxs-lookup"><span data-stu-id="c1c47-158">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="c1c47-159">Use un desplazamiento solo en un entero miplevel; de lo contrario, puede obtener resultados que no se traduzcan bien al hardware.</span><span class="sxs-lookup"><span data-stu-id="c1c47-159">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="c1c47-160">El tipo de argumento depende del tipo de objeto de textura.</span><span class="sxs-lookup"><span data-stu-id="c1c47-160">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="c1c47-161">Para obtener más información, vea [aplicar desplazamientos enteros](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="c1c47-161">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="c1c47-162">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="c1c47-162">Texture-Object Type</span></span>           | <span data-ttu-id="c1c47-163">Tipo de parámetro</span><span class="sxs-lookup"><span data-stu-id="c1c47-163">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="c1c47-164">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="c1c47-164">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="c1c47-165">int</span><span class="sxs-lookup"><span data-stu-id="c1c47-165">int</span></span>            |
| <span data-ttu-id="c1c47-166">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="c1c47-166">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="c1c47-167">int2</span><span class="sxs-lookup"><span data-stu-id="c1c47-167">int2</span></span>           |
| <span data-ttu-id="c1c47-168">Texture3D</span><span class="sxs-lookup"><span data-stu-id="c1c47-168">Texture3D</span></span>                     | <span data-ttu-id="c1c47-169">int3</span><span class="sxs-lookup"><span data-stu-id="c1c47-169">int3</span></span>           |
| <span data-ttu-id="c1c47-170">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="c1c47-170">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="c1c47-171">no admitido</span><span class="sxs-lookup"><span data-stu-id="c1c47-171">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="c1c47-172">*Abrazadera* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c1c47-172">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1c47-173">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="c1c47-173">Type: **float**</span></span>

<span data-ttu-id="c1c47-174">Un valor opcional en el que se van a fijar los valores LOD de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="c1c47-174">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="c1c47-175">Por ejemplo, si se pasa 2.0 f para el valor Clamp, se asegura de que ningún ejemplo individual tenga acceso a un nivel de MIP inferior a 2.0 f.</span><span class="sxs-lookup"><span data-stu-id="c1c47-175">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> <dt>

<span data-ttu-id="c1c47-176">*Estado* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="c1c47-176">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c1c47-177">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="c1c47-177">Type: **uint**</span></span>

<span data-ttu-id="c1c47-178">Estado de la operación.</span><span class="sxs-lookup"><span data-stu-id="c1c47-178">The status of the operation.</span></span> <span data-ttu-id="c1c47-179">No se puede tener acceso directamente al estado. en su lugar, pase el estado a la función intrínseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="c1c47-179">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="c1c47-180">**CheckAccessFullyMapped** devuelve **true** si todos los valores de la operación de **ejemplo**, **recopilación** o **carga** correspondiente han tenido acceso a los mosaicos asignados en un [recurso en mosaico](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="c1c47-180">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="c1c47-181">Si se tomó algún valor de un mosaico sin asignar, **CheckAccessFullyMapped** devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="c1c47-181">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1c47-182">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c1c47-182">Return value</span></span>

<span data-ttu-id="c1c47-183">Tipo: **[ **\_ formato de DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="c1c47-183">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="c1c47-184">Formato de textura, que es uno de los valores con tipo que aparecen [**en \_ formato de DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="c1c47-184">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="c1c47-185">Vea también</span><span class="sxs-lookup"><span data-stu-id="c1c47-185">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1c47-186">Métodos SampleGrad</span><span class="sxs-lookup"><span data-stu-id="c1c47-186">SampleGrad methods</span></span>](texture1d-samplegrad.md)
</dt> </dl>

 

 
