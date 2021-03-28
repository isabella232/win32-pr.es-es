---
title: 'Función SampleGrad:: SampleGrad (S, Float, Float, Float, int, Float, uint) para Texture1DArray'
description: Obtenga información sobre cómo esta función muestra una textura mediante un degradado para influir en la forma en que se calcula la ubicación de ejemplo.
ms.assetid: 8F0D2A4E-37A9-4141-9EE7-2AACBB29E3C2
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
ms.openlocfilehash: 7a0feca232f09da4dc99ff97f68eaab881f1e9ee
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/16/2021
ms.locfileid: "103821578"
---
# <a name="samplegradsamplegradsfloatfloatfloatintfloatuint-function-for-texture1darray"></a><span data-ttu-id="4e559-104">Función SampleGrad:: SampleGrad (S, Float, Float, Float, int, Float, uint) para Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="4e559-104">SampleGrad::SampleGrad(S,float,float,float,int,float,uint) function for Texture1DArray</span></span>

<span data-ttu-id="4e559-105">Muestrea una textura, utilizando un degradado para influir en la forma en que se calcula la ubicación de ejemplo, con un valor opcional para Clamp valores de nivel de detalle (LOD) de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="4e559-105">Samples a texture, using a gradient to influence the way the sample location is calculated, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span> <span data-ttu-id="4e559-106">Devuelve el estado de la operación.</span><span class="sxs-lookup"><span data-stu-id="4e559-106">Returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e559-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4e559-107">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="4e559-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4e559-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e559-109">*S* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="4e559-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e559-110">Tipo: **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="4e559-110">Type: **SamplerState**</span></span>

<span data-ttu-id="4e559-111">Un [Estado de muestra](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="4e559-111">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="4e559-112">Se trata de un objeto declarado en un archivo de efectos que contiene las asignaciones de estado.</span><span class="sxs-lookup"><span data-stu-id="4e559-112">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="4e559-113">*Ubicación* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="4e559-113">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e559-114">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="4e559-114">Type: **float**</span></span>

<span data-ttu-id="4e559-115">Las coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="4e559-115">The texture coordinates.</span></span> <span data-ttu-id="4e559-116">El tipo de argumento depende del tipo de objeto de textura.</span><span class="sxs-lookup"><span data-stu-id="4e559-116">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="4e559-117">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="4e559-117">Texture-Object Type</span></span>                    | <span data-ttu-id="4e559-118">Tipo de parámetro</span><span class="sxs-lookup"><span data-stu-id="4e559-118">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="4e559-119">Texture1D</span><span class="sxs-lookup"><span data-stu-id="4e559-119">Texture1D</span></span>                              | <span data-ttu-id="4e559-120">FLOAT</span><span class="sxs-lookup"><span data-stu-id="4e559-120">float</span></span>          |
| <span data-ttu-id="4e559-121">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="4e559-121">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="4e559-122">float2</span><span class="sxs-lookup"><span data-stu-id="4e559-122">float2</span></span>         |
| <span data-ttu-id="4e559-123">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="4e559-123">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="4e559-124">float3</span><span class="sxs-lookup"><span data-stu-id="4e559-124">float3</span></span>         |
| <span data-ttu-id="4e559-125">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="4e559-125">TextureCubeArray</span></span>                       | <span data-ttu-id="4e559-126">float4</span><span class="sxs-lookup"><span data-stu-id="4e559-126">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="4e559-127">*DDX* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="4e559-127">*DDX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e559-128">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="4e559-128">Type: **float**</span></span>

<span data-ttu-id="4e559-129">La tasa de cambio de la geometría de la superficie en la dirección x.</span><span class="sxs-lookup"><span data-stu-id="4e559-129">The rate of change of the surface geometry in the x direction.</span></span> <span data-ttu-id="4e559-130">El tipo de argumento depende del tipo de objeto de textura.</span><span class="sxs-lookup"><span data-stu-id="4e559-130">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="4e559-131">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="4e559-131">Texture-Object Type</span></span>                      | <span data-ttu-id="4e559-132">Tipo de parámetro</span><span class="sxs-lookup"><span data-stu-id="4e559-132">Parameter Type</span></span> |
|------------------------------------------|----------------|
| <span data-ttu-id="4e559-133">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="4e559-133">Texture1D, Texture1DArray</span></span>                | <span data-ttu-id="4e559-134">FLOAT</span><span class="sxs-lookup"><span data-stu-id="4e559-134">float</span></span>          |
| <span data-ttu-id="4e559-135">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="4e559-135">Texture2D, Texture2DArray</span></span>                | <span data-ttu-id="4e559-136">float2</span><span class="sxs-lookup"><span data-stu-id="4e559-136">float2</span></span>         |
| <span data-ttu-id="4e559-137">Texture3D, TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="4e559-137">Texture3D, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="4e559-138">float3</span><span class="sxs-lookup"><span data-stu-id="4e559-138">float3</span></span>         |
| <span data-ttu-id="4e559-139">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="4e559-139">Texture2DMS, Texture2DMSArray</span></span>            | <span data-ttu-id="4e559-140">no admitido</span><span class="sxs-lookup"><span data-stu-id="4e559-140">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="4e559-141">*DDY* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4e559-141">*DDY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e559-142">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="4e559-142">Type: **float**</span></span>

<span data-ttu-id="4e559-143">La tasa de cambio de la geometría de la superficie en la dirección y.</span><span class="sxs-lookup"><span data-stu-id="4e559-143">The rate of change of the surface geometry in the y direction.</span></span> <span data-ttu-id="4e559-144">El tipo de argumento depende del tipo de objeto de textura.</span><span class="sxs-lookup"><span data-stu-id="4e559-144">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="4e559-145">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="4e559-145">Texture-Object Type</span></span>                      | <span data-ttu-id="4e559-146">Tipo de parámetro</span><span class="sxs-lookup"><span data-stu-id="4e559-146">Parameter Type</span></span> |
|------------------------------------------|----------------|
| <span data-ttu-id="4e559-147">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="4e559-147">Texture1D, Texture1DArray</span></span>                | <span data-ttu-id="4e559-148">FLOAT</span><span class="sxs-lookup"><span data-stu-id="4e559-148">float</span></span>          |
| <span data-ttu-id="4e559-149">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="4e559-149">Texture2D, Texture2DArray</span></span>                | <span data-ttu-id="4e559-150">float2</span><span class="sxs-lookup"><span data-stu-id="4e559-150">float2</span></span>         |
| <span data-ttu-id="4e559-151">Texture3D, TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="4e559-151">Texture3D, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="4e559-152">float3</span><span class="sxs-lookup"><span data-stu-id="4e559-152">float3</span></span>         |
| <span data-ttu-id="4e559-153">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="4e559-153">Texture2DMS, Texture2DMSArray</span></span>            | <span data-ttu-id="4e559-154">no admitido</span><span class="sxs-lookup"><span data-stu-id="4e559-154">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="4e559-155">*Desplazamiento* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4e559-155">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e559-156">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="4e559-156">Type: **int**</span></span>

<span data-ttu-id="4e559-157">Desplazamiento de coordenadas de textura opcional, que se puede usar para cualquier tipo de objeto de textura. el desplazamiento se aplica a la ubicación antes del muestreo.</span><span class="sxs-lookup"><span data-stu-id="4e559-157">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="4e559-158">Use un desplazamiento solo en un entero miplevel; de lo contrario, puede obtener resultados que no se traduzcan bien al hardware.</span><span class="sxs-lookup"><span data-stu-id="4e559-158">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="4e559-159">El tipo de argumento depende del tipo de objeto de textura.</span><span class="sxs-lookup"><span data-stu-id="4e559-159">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="4e559-160">Para obtener más información, vea [aplicar desplazamientos enteros](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="4e559-160">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="4e559-161">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="4e559-161">Texture-Object Type</span></span>           | <span data-ttu-id="4e559-162">Tipo de parámetro</span><span class="sxs-lookup"><span data-stu-id="4e559-162">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="4e559-163">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="4e559-163">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="4e559-164">int</span><span class="sxs-lookup"><span data-stu-id="4e559-164">int</span></span>            |
| <span data-ttu-id="4e559-165">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="4e559-165">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="4e559-166">int2</span><span class="sxs-lookup"><span data-stu-id="4e559-166">int2</span></span>           |
| <span data-ttu-id="4e559-167">Texture3D</span><span class="sxs-lookup"><span data-stu-id="4e559-167">Texture3D</span></span>                     | <span data-ttu-id="4e559-168">int3</span><span class="sxs-lookup"><span data-stu-id="4e559-168">int3</span></span>           |
| <span data-ttu-id="4e559-169">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="4e559-169">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="4e559-170">no admitido</span><span class="sxs-lookup"><span data-stu-id="4e559-170">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="4e559-171">*Abrazadera* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4e559-171">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e559-172">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="4e559-172">Type: **float**</span></span>

<span data-ttu-id="4e559-173">Un valor opcional en el que se van a fijar los valores LOD de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="4e559-173">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="4e559-174">Por ejemplo, si se pasa 2.0 f para el valor Clamp, se asegura de que ningún ejemplo individual tenga acceso a un nivel de MIP inferior a 2.0 f.</span><span class="sxs-lookup"><span data-stu-id="4e559-174">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> <dt>

<span data-ttu-id="4e559-175">*Estado* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="4e559-175">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4e559-176">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="4e559-176">Type: **uint**</span></span>

<span data-ttu-id="4e559-177">Estado de la operación.</span><span class="sxs-lookup"><span data-stu-id="4e559-177">The status of the operation.</span></span> <span data-ttu-id="4e559-178">No se puede tener acceso directamente al estado. en su lugar, pase el estado a la función intrínseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="4e559-178">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="4e559-179">**CheckAccessFullyMapped** devuelve **true** si todos los valores de la operación de **ejemplo**, **recopilación** o **carga** correspondiente han tenido acceso a los mosaicos asignados en un [recurso en mosaico](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="4e559-179">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="4e559-180">Si se tomó algún valor de un mosaico sin asignar, **CheckAccessFullyMapped** devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="4e559-180">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e559-181">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4e559-181">Return value</span></span>

<span data-ttu-id="4e559-182">Tipo: **[ **\_ formato de DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="4e559-182">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="4e559-183">Formato de textura, que es uno de los valores con tipo que aparecen [**en \_ formato de DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="4e559-183">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="4e559-184">Vea también</span><span class="sxs-lookup"><span data-stu-id="4e559-184">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e559-185">Métodos SampleGrad</span><span class="sxs-lookup"><span data-stu-id="4e559-185">SampleGrad methods</span></span>](texture1darray-samplegrad.md)
</dt> </dl>

 

 
