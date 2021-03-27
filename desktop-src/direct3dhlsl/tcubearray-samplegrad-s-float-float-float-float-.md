---
title: 'Función SampleGrad:: SampleGrad (S, Float, Float, Float, float) para TextureCubeArray'
description: Obtenga información sobre cómo esta función muestra una textura mediante un degradado para influir en la forma en que se calcula la ubicación de ejemplo. Para TextureCubeArray.
ms.assetid: 0C7DC9AA-3F0A-47E4-852F-7AE25CF67EA3
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
ms.openlocfilehash: 5320f47a5ae4db5bd96232dfa0a1d55b54f29c25
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/16/2021
ms.locfileid: "103821559"
---
# <a name="samplegradsamplegradsfloatfloatfloatfloat-function-for-texturecubearray"></a><span data-ttu-id="b15af-105">Función SampleGrad:: SampleGrad (S, Float, Float, Float, float) para TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="b15af-105">SampleGrad::SampleGrad(S,float,float,float,float) function for TextureCubeArray</span></span>

<span data-ttu-id="b15af-106">Muestrea una textura, utilizando un degradado para influir en la forma en que se calcula la ubicación de ejemplo, con un valor opcional para Clamp valores de nivel de detalle (LOD) de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="b15af-106">Samples a texture, using a gradient to influence the way the sample location is calculated, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span>

## <a name="syntax"></a><span data-ttu-id="b15af-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b15af-107">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleGrad(
  in SamplerState S,
  in float        Location,
  in float        DDX,
  in float        DDY,
  in float        Clamp
);
```



## <a name="parameters"></a><span data-ttu-id="b15af-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b15af-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b15af-109">*S* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="b15af-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b15af-110">Tipo: **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="b15af-110">Type: **SamplerState**</span></span>

<span data-ttu-id="b15af-111">Un [Estado de muestra](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="b15af-111">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="b15af-112">Se trata de un objeto declarado en un archivo de efectos que contiene las asignaciones de estado.</span><span class="sxs-lookup"><span data-stu-id="b15af-112">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="b15af-113">*Ubicación* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="b15af-113">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b15af-114">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="b15af-114">Type: **float**</span></span>

<span data-ttu-id="b15af-115">Las coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="b15af-115">The texture coordinates.</span></span> <span data-ttu-id="b15af-116">El tipo de argumento depende del tipo de objeto de textura.</span><span class="sxs-lookup"><span data-stu-id="b15af-116">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="b15af-117">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="b15af-117">Texture-Object Type</span></span>                    | <span data-ttu-id="b15af-118">Tipo de parámetro</span><span class="sxs-lookup"><span data-stu-id="b15af-118">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="b15af-119">Texture1D</span><span class="sxs-lookup"><span data-stu-id="b15af-119">Texture1D</span></span>                              | <span data-ttu-id="b15af-120">FLOAT</span><span class="sxs-lookup"><span data-stu-id="b15af-120">float</span></span>          |
| <span data-ttu-id="b15af-121">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="b15af-121">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="b15af-122">float2</span><span class="sxs-lookup"><span data-stu-id="b15af-122">float2</span></span>         |
| <span data-ttu-id="b15af-123">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="b15af-123">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="b15af-124">float3</span><span class="sxs-lookup"><span data-stu-id="b15af-124">float3</span></span>         |
| <span data-ttu-id="b15af-125">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="b15af-125">TextureCubeArray</span></span>                       | <span data-ttu-id="b15af-126">float4</span><span class="sxs-lookup"><span data-stu-id="b15af-126">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="b15af-127">*DDX* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="b15af-127">*DDX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b15af-128">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="b15af-128">Type: **float**</span></span>

<span data-ttu-id="b15af-129">La tasa de cambio de la geometría de la superficie en la dirección x.</span><span class="sxs-lookup"><span data-stu-id="b15af-129">The rate of change of the surface geometry in the x direction.</span></span> <span data-ttu-id="b15af-130">El tipo de argumento depende del tipo de objeto de textura.</span><span class="sxs-lookup"><span data-stu-id="b15af-130">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="b15af-131">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="b15af-131">Texture-Object Type</span></span>                      | <span data-ttu-id="b15af-132">Tipo de parámetro</span><span class="sxs-lookup"><span data-stu-id="b15af-132">Parameter Type</span></span> |
|------------------------------------------|----------------|
| <span data-ttu-id="b15af-133">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="b15af-133">Texture1D, Texture1DArray</span></span>                | <span data-ttu-id="b15af-134">FLOAT</span><span class="sxs-lookup"><span data-stu-id="b15af-134">float</span></span>          |
| <span data-ttu-id="b15af-135">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="b15af-135">Texture2D, Texture2DArray</span></span>                | <span data-ttu-id="b15af-136">float2</span><span class="sxs-lookup"><span data-stu-id="b15af-136">float2</span></span>         |
| <span data-ttu-id="b15af-137">Texture3D, TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="b15af-137">Texture3D, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="b15af-138">float3</span><span class="sxs-lookup"><span data-stu-id="b15af-138">float3</span></span>         |
| <span data-ttu-id="b15af-139">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="b15af-139">Texture2DMS, Texture2DMSArray</span></span>            | <span data-ttu-id="b15af-140">no admitido</span><span class="sxs-lookup"><span data-stu-id="b15af-140">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="b15af-141">*DDY* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b15af-141">*DDY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b15af-142">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="b15af-142">Type: **float**</span></span>

<span data-ttu-id="b15af-143">La tasa de cambio de la geometría de la superficie en la dirección y.</span><span class="sxs-lookup"><span data-stu-id="b15af-143">The rate of change of the surface geometry in the y direction.</span></span> <span data-ttu-id="b15af-144">El tipo de argumento depende del tipo de objeto de textura.</span><span class="sxs-lookup"><span data-stu-id="b15af-144">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="b15af-145">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="b15af-145">Texture-Object Type</span></span>                      | <span data-ttu-id="b15af-146">Tipo de parámetro</span><span class="sxs-lookup"><span data-stu-id="b15af-146">Parameter Type</span></span> |
|------------------------------------------|----------------|
| <span data-ttu-id="b15af-147">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="b15af-147">Texture1D, Texture1DArray</span></span>                | <span data-ttu-id="b15af-148">FLOAT</span><span class="sxs-lookup"><span data-stu-id="b15af-148">float</span></span>          |
| <span data-ttu-id="b15af-149">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="b15af-149">Texture2D, Texture2DArray</span></span>                | <span data-ttu-id="b15af-150">float2</span><span class="sxs-lookup"><span data-stu-id="b15af-150">float2</span></span>         |
| <span data-ttu-id="b15af-151">Texture3D, TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="b15af-151">Texture3D, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="b15af-152">float3</span><span class="sxs-lookup"><span data-stu-id="b15af-152">float3</span></span>         |
| <span data-ttu-id="b15af-153">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="b15af-153">Texture2DMS, Texture2DMSArray</span></span>            | <span data-ttu-id="b15af-154">no admitido</span><span class="sxs-lookup"><span data-stu-id="b15af-154">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="b15af-155">*Abrazadera* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b15af-155">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b15af-156">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="b15af-156">Type: **float**</span></span>

<span data-ttu-id="b15af-157">Un valor opcional en el que se van a fijar los valores LOD de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="b15af-157">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="b15af-158">Por ejemplo, si se pasa 2.0 f para el valor Clamp, se asegura de que ningún ejemplo individual tenga acceso a un nivel de MIP inferior a 2.0 f.</span><span class="sxs-lookup"><span data-stu-id="b15af-158">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b15af-159">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b15af-159">Return value</span></span>

<span data-ttu-id="b15af-160">Tipo: **[ **\_ formato de DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="b15af-160">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="b15af-161">Formato de textura, que es uno de los valores con tipo que aparecen [**en \_ formato de DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="b15af-161">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="b15af-162">Vea también</span><span class="sxs-lookup"><span data-stu-id="b15af-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b15af-163">Métodos SampleGrad</span><span class="sxs-lookup"><span data-stu-id="b15af-163">SampleGrad methods</span></span>](texturecubearray-samplegrad.md)
</dt> <dt>

[<span data-ttu-id="b15af-164">**TextureCubeArray**</span><span class="sxs-lookup"><span data-stu-id="b15af-164">**TextureCubeArray**</span></span>](texturecubearray.md)
</dt> </dl>

 

 
