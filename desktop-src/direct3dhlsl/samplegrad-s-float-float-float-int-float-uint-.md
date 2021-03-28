---
title: 'Función SampleGrad:: SampleGrad (S, Float, Float, Float, int, Float, uint) para Texture2D'
description: Muestrea un Texture2D, con un degradado para influir en la forma en que se calcula la ubicación de ejemplo, con un valor opcional para Clamp valores de nivel de detalle (LOD) de ejemplo en.
ms.assetid: 896497E1-A795-4674-AB41-2440A7D0CC76
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
ms.openlocfilehash: 9f1909c792863a3b480b6bdec553db58f7ff8492
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/16/2021
ms.locfileid: "104998850"
---
# <a name="samplegradsamplegradsfloatfloatfloatintfloatuint-function-for-texture2d"></a><span data-ttu-id="46f74-104">Función SampleGrad:: SampleGrad (S, Float, Float, Float, int, Float, uint) para Texture2D</span><span class="sxs-lookup"><span data-stu-id="46f74-104">SampleGrad::SampleGrad(S,float,float,float,int,float,uint) function for Texture2D</span></span>

<span data-ttu-id="46f74-105">Muestrea un [**Texture2D**](sm5-object-texture2d.md), con un degradado para influir en la forma en que se calcula la ubicación de ejemplo, con un valor opcional para Clamp valores de nivel de detalle (LOD) de ejemplo en.</span><span class="sxs-lookup"><span data-stu-id="46f74-105">Samples a [**Texture2D**](sm5-object-texture2d.md), using a gradient to influence the way the sample location is calculated, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span> <span data-ttu-id="46f74-106">Devuelve el estado de la operación.</span><span class="sxs-lookup"><span data-stu-id="46f74-106">Returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="46f74-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="46f74-107">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="46f74-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="46f74-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46f74-109">*S* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="46f74-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46f74-110">Tipo: **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="46f74-110">Type: **SamplerState**</span></span>

<span data-ttu-id="46f74-111">Un [Estado de muestra](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="46f74-111">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="46f74-112">Se trata de un objeto declarado en un archivo de efectos que contiene las asignaciones de estado.</span><span class="sxs-lookup"><span data-stu-id="46f74-112">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="46f74-113">*Ubicación* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="46f74-113">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46f74-114">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="46f74-114">Type: **float**</span></span>

<span data-ttu-id="46f74-115">Las coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="46f74-115">The texture coordinates.</span></span> <span data-ttu-id="46f74-116">El tipo de argumento depende del tipo de objeto de textura.</span><span class="sxs-lookup"><span data-stu-id="46f74-116">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="46f74-117">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="46f74-117">Texture-Object Type</span></span>                    | <span data-ttu-id="46f74-118">Tipo de parámetro</span><span class="sxs-lookup"><span data-stu-id="46f74-118">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="46f74-119">Texture1D</span><span class="sxs-lookup"><span data-stu-id="46f74-119">Texture1D</span></span>                              | <span data-ttu-id="46f74-120">FLOAT</span><span class="sxs-lookup"><span data-stu-id="46f74-120">float</span></span>          |
| <span data-ttu-id="46f74-121">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="46f74-121">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="46f74-122">float2</span><span class="sxs-lookup"><span data-stu-id="46f74-122">float2</span></span>         |
| <span data-ttu-id="46f74-123">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="46f74-123">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="46f74-124">float3</span><span class="sxs-lookup"><span data-stu-id="46f74-124">float3</span></span>         |
| <span data-ttu-id="46f74-125">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="46f74-125">TextureCubeArray</span></span>                       | <span data-ttu-id="46f74-126">float4</span><span class="sxs-lookup"><span data-stu-id="46f74-126">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="46f74-127">*DDX* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="46f74-127">*DDX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46f74-128">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="46f74-128">Type: **float**</span></span>

<span data-ttu-id="46f74-129">La tasa de cambio de la geometría de la superficie en la dirección x.</span><span class="sxs-lookup"><span data-stu-id="46f74-129">The rate of change of the surface geometry in the x direction.</span></span> <span data-ttu-id="46f74-130">El tipo de argumento depende del tipo de objeto de textura.</span><span class="sxs-lookup"><span data-stu-id="46f74-130">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="46f74-131">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="46f74-131">Texture-Object Type</span></span>                      | <span data-ttu-id="46f74-132">Tipo de parámetro</span><span class="sxs-lookup"><span data-stu-id="46f74-132">Parameter Type</span></span> |
|------------------------------------------|----------------|
| <span data-ttu-id="46f74-133">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="46f74-133">Texture1D, Texture1DArray</span></span>                | <span data-ttu-id="46f74-134">FLOAT</span><span class="sxs-lookup"><span data-stu-id="46f74-134">float</span></span>          |
| <span data-ttu-id="46f74-135">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="46f74-135">Texture2D, Texture2DArray</span></span>                | <span data-ttu-id="46f74-136">float2</span><span class="sxs-lookup"><span data-stu-id="46f74-136">float2</span></span>         |
| <span data-ttu-id="46f74-137">Texture3D, TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="46f74-137">Texture3D, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="46f74-138">float3</span><span class="sxs-lookup"><span data-stu-id="46f74-138">float3</span></span>         |
| <span data-ttu-id="46f74-139">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="46f74-139">Texture2DMS, Texture2DMSArray</span></span>            | <span data-ttu-id="46f74-140">no admitido</span><span class="sxs-lookup"><span data-stu-id="46f74-140">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="46f74-141">*DDY* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="46f74-141">*DDY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46f74-142">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="46f74-142">Type: **float**</span></span>

<span data-ttu-id="46f74-143">La tasa de cambio de la geometría de la superficie en la dirección y.</span><span class="sxs-lookup"><span data-stu-id="46f74-143">The rate of change of the surface geometry in the y direction.</span></span> <span data-ttu-id="46f74-144">El tipo de argumento depende del tipo de objeto de textura.</span><span class="sxs-lookup"><span data-stu-id="46f74-144">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="46f74-145">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="46f74-145">Texture-Object Type</span></span>                      | <span data-ttu-id="46f74-146">Tipo de parámetro</span><span class="sxs-lookup"><span data-stu-id="46f74-146">Parameter Type</span></span> |
|------------------------------------------|----------------|
| <span data-ttu-id="46f74-147">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="46f74-147">Texture1D, Texture1DArray</span></span>                | <span data-ttu-id="46f74-148">FLOAT</span><span class="sxs-lookup"><span data-stu-id="46f74-148">float</span></span>          |
| <span data-ttu-id="46f74-149">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="46f74-149">Texture2D, Texture2DArray</span></span>                | <span data-ttu-id="46f74-150">float2</span><span class="sxs-lookup"><span data-stu-id="46f74-150">float2</span></span>         |
| <span data-ttu-id="46f74-151">Texture3D, TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="46f74-151">Texture3D, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="46f74-152">float3</span><span class="sxs-lookup"><span data-stu-id="46f74-152">float3</span></span>         |
| <span data-ttu-id="46f74-153">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="46f74-153">Texture2DMS, Texture2DMSArray</span></span>            | <span data-ttu-id="46f74-154">no admitido</span><span class="sxs-lookup"><span data-stu-id="46f74-154">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="46f74-155">*Desplazamiento* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="46f74-155">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46f74-156">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="46f74-156">Type: **int**</span></span>

<span data-ttu-id="46f74-157">Desplazamiento de coordenadas de textura opcional, que se puede usar para cualquier tipo de objeto de textura. el desplazamiento se aplica a la ubicación antes del muestreo.</span><span class="sxs-lookup"><span data-stu-id="46f74-157">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="46f74-158">Use un desplazamiento solo en un entero miplevel; de lo contrario, puede obtener resultados que no se traduzcan bien al hardware.</span><span class="sxs-lookup"><span data-stu-id="46f74-158">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="46f74-159">El tipo de argumento depende del tipo de objeto de textura.</span><span class="sxs-lookup"><span data-stu-id="46f74-159">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="46f74-160">Para obtener más información, vea [aplicar desplazamientos enteros](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="46f74-160">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="46f74-161">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="46f74-161">Texture-Object Type</span></span>           | <span data-ttu-id="46f74-162">Tipo de parámetro</span><span class="sxs-lookup"><span data-stu-id="46f74-162">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="46f74-163">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="46f74-163">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="46f74-164">int</span><span class="sxs-lookup"><span data-stu-id="46f74-164">int</span></span>            |
| <span data-ttu-id="46f74-165">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="46f74-165">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="46f74-166">int2</span><span class="sxs-lookup"><span data-stu-id="46f74-166">int2</span></span>           |
| <span data-ttu-id="46f74-167">Texture3D</span><span class="sxs-lookup"><span data-stu-id="46f74-167">Texture3D</span></span>                     | <span data-ttu-id="46f74-168">int3</span><span class="sxs-lookup"><span data-stu-id="46f74-168">int3</span></span>           |
| <span data-ttu-id="46f74-169">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="46f74-169">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="46f74-170">no admitido</span><span class="sxs-lookup"><span data-stu-id="46f74-170">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="46f74-171">*Abrazadera* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="46f74-171">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46f74-172">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="46f74-172">Type: **float**</span></span>

<span data-ttu-id="46f74-173">Un valor opcional en el que se van a fijar los valores LOD de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="46f74-173">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="46f74-174">Por ejemplo, si se pasa 2.0 f para el valor Clamp, se asegura de que ningún ejemplo individual tenga acceso a un nivel de MIP inferior a 2.0 f.</span><span class="sxs-lookup"><span data-stu-id="46f74-174">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> <dt>

<span data-ttu-id="46f74-175">*Estado* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="46f74-175">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="46f74-176">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="46f74-176">Type: **uint**</span></span>

<span data-ttu-id="46f74-177">Estado de la operación.</span><span class="sxs-lookup"><span data-stu-id="46f74-177">The status of the operation.</span></span> <span data-ttu-id="46f74-178">No se puede tener acceso directamente al estado. en su lugar, pase el estado a la función intrínseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="46f74-178">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="46f74-179">**CheckAccessFullyMapped** devuelve **true** si todos los valores de la operación de **ejemplo**, **recopilación** o **carga** correspondiente han tenido acceso a los mosaicos asignados en un [recurso en mosaico](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="46f74-179">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="46f74-180">Si se tomó algún valor de un mosaico sin asignar, **CheckAccessFullyMapped** devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="46f74-180">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46f74-181">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="46f74-181">Return value</span></span>

<span data-ttu-id="46f74-182">Tipo: **[ **\_ formato de DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="46f74-182">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="46f74-183">Formato de textura, que es uno de los valores con tipo que aparecen [**en \_ formato de DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="46f74-183">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="46f74-184">Vea también</span><span class="sxs-lookup"><span data-stu-id="46f74-184">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46f74-185">Métodos SampleGrad</span><span class="sxs-lookup"><span data-stu-id="46f74-185">SampleGrad methods</span></span>](texture2d-samplegrad.md)
</dt> </dl>

 

 
