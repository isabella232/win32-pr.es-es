---
title: 'Función SampleGrad:: SampleGrad (S, Float, Float, Float, Float, uint) para TextureCubeArray'
description: Obtenga información sobre cómo esta función muestra una textura mediante un degradado para influir en la forma en que se calcula la ubicación de ejemplo, con un valor opcional para Clamp valores de nivel de detalle (LOD) de ejemplo en. Para TextureCubeArray.
ms.assetid: 849FAF04-A133-4E5B-967E-0679AE335CCC
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
ms.openlocfilehash: 00adfb5c7a1a95e5462b1bc524a6c7d86f71c2e8
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/16/2021
ms.locfileid: "104987276"
---
# <a name="samplegradsamplegradsfloatfloatfloatfloatuint-function-for-texturecubearray"></a><span data-ttu-id="f5653-105">Función SampleGrad:: SampleGrad (S, Float, Float, Float, Float, uint) para TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="f5653-105">SampleGrad::SampleGrad(S,float,float,float,float,uint) function for TextureCubeArray</span></span>

<span data-ttu-id="f5653-106">Muestrea una textura, utilizando un degradado para influir en la forma en que se calcula la ubicación de ejemplo, con un valor opcional para Clamp valores de nivel de detalle (LOD) de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="f5653-106">Samples a texture, using a gradient to influence the way the sample location is calculated, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span> <span data-ttu-id="f5653-107">Devuelve el estado de la operación.</span><span class="sxs-lookup"><span data-stu-id="f5653-107">Returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5653-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f5653-108">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleGrad(
  in  SamplerState S,
  in  float        Location,
  in  float        DDX,
  in  float        DDY,
  in  float        Clamp,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="f5653-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f5653-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5653-110">*S* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="f5653-110">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5653-111">Tipo: **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="f5653-111">Type: **SamplerState**</span></span>

<span data-ttu-id="f5653-112">Un [Estado de muestra](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="f5653-112">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="f5653-113">Se trata de un objeto declarado en un archivo de efectos que contiene las asignaciones de estado.</span><span class="sxs-lookup"><span data-stu-id="f5653-113">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="f5653-114">*Ubicación* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="f5653-114">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5653-115">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="f5653-115">Type: **float**</span></span>

<span data-ttu-id="f5653-116">Las coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="f5653-116">The texture coordinates.</span></span> <span data-ttu-id="f5653-117">El tipo de argumento depende del tipo de objeto de textura.</span><span class="sxs-lookup"><span data-stu-id="f5653-117">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="f5653-118">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="f5653-118">Texture-Object Type</span></span>                    | <span data-ttu-id="f5653-119">Tipo de parámetro</span><span class="sxs-lookup"><span data-stu-id="f5653-119">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="f5653-120">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f5653-120">Texture1D</span></span>                              | <span data-ttu-id="f5653-121">FLOAT</span><span class="sxs-lookup"><span data-stu-id="f5653-121">float</span></span>          |
| <span data-ttu-id="f5653-122">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="f5653-122">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="f5653-123">float2</span><span class="sxs-lookup"><span data-stu-id="f5653-123">float2</span></span>         |
| <span data-ttu-id="f5653-124">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="f5653-124">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="f5653-125">float3</span><span class="sxs-lookup"><span data-stu-id="f5653-125">float3</span></span>         |
| <span data-ttu-id="f5653-126">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="f5653-126">TextureCubeArray</span></span>                       | <span data-ttu-id="f5653-127">float4</span><span class="sxs-lookup"><span data-stu-id="f5653-127">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="f5653-128">*DDX* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="f5653-128">*DDX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5653-129">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="f5653-129">Type: **float**</span></span>

<span data-ttu-id="f5653-130">La tasa de cambio de la geometría de la superficie en la dirección x.</span><span class="sxs-lookup"><span data-stu-id="f5653-130">The rate of change of the surface geometry in the x direction.</span></span> <span data-ttu-id="f5653-131">El tipo de argumento depende del tipo de objeto de textura.</span><span class="sxs-lookup"><span data-stu-id="f5653-131">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="f5653-132">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="f5653-132">Texture-Object Type</span></span>                      | <span data-ttu-id="f5653-133">Tipo de parámetro</span><span class="sxs-lookup"><span data-stu-id="f5653-133">Parameter Type</span></span> |
|------------------------------------------|----------------|
| <span data-ttu-id="f5653-134">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="f5653-134">Texture1D, Texture1DArray</span></span>                | <span data-ttu-id="f5653-135">FLOAT</span><span class="sxs-lookup"><span data-stu-id="f5653-135">float</span></span>          |
| <span data-ttu-id="f5653-136">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="f5653-136">Texture2D, Texture2DArray</span></span>                | <span data-ttu-id="f5653-137">float2</span><span class="sxs-lookup"><span data-stu-id="f5653-137">float2</span></span>         |
| <span data-ttu-id="f5653-138">Texture3D, TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="f5653-138">Texture3D, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="f5653-139">float3</span><span class="sxs-lookup"><span data-stu-id="f5653-139">float3</span></span>         |
| <span data-ttu-id="f5653-140">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="f5653-140">Texture2DMS, Texture2DMSArray</span></span>            | <span data-ttu-id="f5653-141">no admitido</span><span class="sxs-lookup"><span data-stu-id="f5653-141">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="f5653-142">*DDY* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f5653-142">*DDY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5653-143">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="f5653-143">Type: **float**</span></span>

<span data-ttu-id="f5653-144">La tasa de cambio de la geometría de la superficie en la dirección y.</span><span class="sxs-lookup"><span data-stu-id="f5653-144">The rate of change of the surface geometry in the y direction.</span></span> <span data-ttu-id="f5653-145">El tipo de argumento depende del tipo de objeto de textura.</span><span class="sxs-lookup"><span data-stu-id="f5653-145">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="f5653-146">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="f5653-146">Texture-Object Type</span></span>                      | <span data-ttu-id="f5653-147">Tipo de parámetro</span><span class="sxs-lookup"><span data-stu-id="f5653-147">Parameter Type</span></span> |
|------------------------------------------|----------------|
| <span data-ttu-id="f5653-148">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="f5653-148">Texture1D, Texture1DArray</span></span>                | <span data-ttu-id="f5653-149">FLOAT</span><span class="sxs-lookup"><span data-stu-id="f5653-149">float</span></span>          |
| <span data-ttu-id="f5653-150">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="f5653-150">Texture2D, Texture2DArray</span></span>                | <span data-ttu-id="f5653-151">float2</span><span class="sxs-lookup"><span data-stu-id="f5653-151">float2</span></span>         |
| <span data-ttu-id="f5653-152">Texture3D, TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="f5653-152">Texture3D, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="f5653-153">float3</span><span class="sxs-lookup"><span data-stu-id="f5653-153">float3</span></span>         |
| <span data-ttu-id="f5653-154">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="f5653-154">Texture2DMS, Texture2DMSArray</span></span>            | <span data-ttu-id="f5653-155">no admitido</span><span class="sxs-lookup"><span data-stu-id="f5653-155">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="f5653-156">*Abrazadera* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f5653-156">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5653-157">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="f5653-157">Type: **float**</span></span>

<span data-ttu-id="f5653-158">Un valor opcional en el que se van a fijar los valores LOD de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="f5653-158">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="f5653-159">Por ejemplo, si se pasa 2.0 f para el valor Clamp, se asegura de que ningún ejemplo individual tenga acceso a un nivel de MIP inferior a 2.0 f.</span><span class="sxs-lookup"><span data-stu-id="f5653-159">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> <dt>

<span data-ttu-id="f5653-160">*Estado* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="f5653-160">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f5653-161">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="f5653-161">Type: **uint**</span></span>

<span data-ttu-id="f5653-162">Estado de la operación.</span><span class="sxs-lookup"><span data-stu-id="f5653-162">The status of the operation.</span></span> <span data-ttu-id="f5653-163">No se puede tener acceso directamente al estado. en su lugar, pase el estado a la función intrínseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="f5653-163">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="f5653-164">**CheckAccessFullyMapped** devuelve **true** si todos los valores de la operación de **ejemplo**, **recopilación** o **carga** correspondiente han tenido acceso a los mosaicos asignados en un [recurso en mosaico](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="f5653-164">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="f5653-165">Si se tomó algún valor de un mosaico sin asignar, **CheckAccessFullyMapped** devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="f5653-165">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5653-166">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f5653-166">Return value</span></span>

<span data-ttu-id="f5653-167">Tipo: **[ **\_ formato de DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="f5653-167">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="f5653-168">Formato de textura, que es uno de los valores con tipo que aparecen [**en \_ formato de DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="f5653-168">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="f5653-169">Vea también</span><span class="sxs-lookup"><span data-stu-id="f5653-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5653-170">Métodos SampleGrad</span><span class="sxs-lookup"><span data-stu-id="f5653-170">SampleGrad methods</span></span>](texturecubearray-samplegrad.md)
</dt> <dt>

[<span data-ttu-id="f5653-171">**TextureCubeArray**</span><span class="sxs-lookup"><span data-stu-id="f5653-171">**TextureCubeArray**</span></span>](texturecubearray.md)
</dt> </dl>

 

 
