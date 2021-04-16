---
title: 'Función SampleGrad:: SampleGrad (S, Float, Float, Float, float) para TextureCube'
description: Muestrea una textura, utilizando un degradado para influir en la forma en que se calcula la ubicación de ejemplo, con un valor opcional para Clamp valores de nivel de detalle (LOD) de ejemplo. Para TextureCube
ms.assetid: C5BC71FA-63E3-4DE2-9202-B9C79789AE8E
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
ms.openlocfilehash: e4a51c49d9373dc210cbf216089e4c82835bf2c4
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/16/2021
ms.locfileid: "104548187"
---
# <a name="samplegradsamplegradsfloatfloatfloatfloat-function-for-texturecube"></a><span data-ttu-id="311f1-105">Función SampleGrad:: SampleGrad (S, Float, Float, Float, float) para TextureCube</span><span class="sxs-lookup"><span data-stu-id="311f1-105">SampleGrad::SampleGrad(S,float,float,float,float) function for TextureCube</span></span>

<span data-ttu-id="311f1-106">Muestrea una textura, utilizando un degradado para influir en la forma en que se calcula la ubicación de ejemplo, con un valor opcional para Clamp valores de nivel de detalle (LOD) de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="311f1-106">Samples a texture, using a gradient to influence the way the sample location is calculated, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span>

## <a name="syntax"></a><span data-ttu-id="311f1-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="311f1-107">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleGrad(
  in SamplerState S,
  in float        Location,
  in float        DDX,
  in float        DDY,
  in float        Clamp
);
```



## <a name="parameters"></a><span data-ttu-id="311f1-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="311f1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="311f1-109">*S* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="311f1-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="311f1-110">Tipo: **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="311f1-110">Type: **SamplerState**</span></span>

<span data-ttu-id="311f1-111">Un [Estado de muestra](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="311f1-111">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="311f1-112">Se trata de un objeto declarado en un archivo de efectos que contiene las asignaciones de estado.</span><span class="sxs-lookup"><span data-stu-id="311f1-112">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="311f1-113">*Ubicación* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="311f1-113">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="311f1-114">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="311f1-114">Type: **float**</span></span>

<span data-ttu-id="311f1-115">Las coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="311f1-115">The texture coordinates.</span></span> <span data-ttu-id="311f1-116">El tipo de argumento depende del tipo de objeto de textura.</span><span class="sxs-lookup"><span data-stu-id="311f1-116">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="311f1-117">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="311f1-117">Texture-Object Type</span></span>                    | <span data-ttu-id="311f1-118">Tipo de parámetro</span><span class="sxs-lookup"><span data-stu-id="311f1-118">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="311f1-119">Texture1D</span><span class="sxs-lookup"><span data-stu-id="311f1-119">Texture1D</span></span>                              | <span data-ttu-id="311f1-120">FLOAT</span><span class="sxs-lookup"><span data-stu-id="311f1-120">float</span></span>          |
| <span data-ttu-id="311f1-121">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="311f1-121">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="311f1-122">float2</span><span class="sxs-lookup"><span data-stu-id="311f1-122">float2</span></span>         |
| <span data-ttu-id="311f1-123">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="311f1-123">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="311f1-124">float3</span><span class="sxs-lookup"><span data-stu-id="311f1-124">float3</span></span>         |
| <span data-ttu-id="311f1-125">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="311f1-125">TextureCubeArray</span></span>                       | <span data-ttu-id="311f1-126">float4</span><span class="sxs-lookup"><span data-stu-id="311f1-126">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="311f1-127">*DDX* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="311f1-127">*DDX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="311f1-128">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="311f1-128">Type: **float**</span></span>

<span data-ttu-id="311f1-129">La tasa de cambio de la geometría de la superficie en la dirección x.</span><span class="sxs-lookup"><span data-stu-id="311f1-129">The rate of change of the surface geometry in the x direction.</span></span> <span data-ttu-id="311f1-130">El tipo de argumento depende del tipo de objeto de textura.</span><span class="sxs-lookup"><span data-stu-id="311f1-130">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="311f1-131">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="311f1-131">Texture-Object Type</span></span>                      | <span data-ttu-id="311f1-132">Tipo de parámetro</span><span class="sxs-lookup"><span data-stu-id="311f1-132">Parameter Type</span></span> |
|------------------------------------------|----------------|
| <span data-ttu-id="311f1-133">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="311f1-133">Texture1D, Texture1DArray</span></span>                | <span data-ttu-id="311f1-134">FLOAT</span><span class="sxs-lookup"><span data-stu-id="311f1-134">float</span></span>          |
| <span data-ttu-id="311f1-135">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="311f1-135">Texture2D, Texture2DArray</span></span>                | <span data-ttu-id="311f1-136">float2</span><span class="sxs-lookup"><span data-stu-id="311f1-136">float2</span></span>         |
| <span data-ttu-id="311f1-137">Texture3D, TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="311f1-137">Texture3D, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="311f1-138">float3</span><span class="sxs-lookup"><span data-stu-id="311f1-138">float3</span></span>         |
| <span data-ttu-id="311f1-139">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="311f1-139">Texture2DMS, Texture2DMSArray</span></span>            | <span data-ttu-id="311f1-140">no admitido</span><span class="sxs-lookup"><span data-stu-id="311f1-140">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="311f1-141">*DDY* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="311f1-141">*DDY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="311f1-142">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="311f1-142">Type: **float**</span></span>

<span data-ttu-id="311f1-143">La tasa de cambio de la geometría de la superficie en la dirección y.</span><span class="sxs-lookup"><span data-stu-id="311f1-143">The rate of change of the surface geometry in the y direction.</span></span> <span data-ttu-id="311f1-144">El tipo de argumento depende del tipo de objeto de textura.</span><span class="sxs-lookup"><span data-stu-id="311f1-144">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="311f1-145">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="311f1-145">Texture-Object Type</span></span>                      | <span data-ttu-id="311f1-146">Tipo de parámetro</span><span class="sxs-lookup"><span data-stu-id="311f1-146">Parameter Type</span></span> |
|------------------------------------------|----------------|
| <span data-ttu-id="311f1-147">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="311f1-147">Texture1D, Texture1DArray</span></span>                | <span data-ttu-id="311f1-148">FLOAT</span><span class="sxs-lookup"><span data-stu-id="311f1-148">float</span></span>          |
| <span data-ttu-id="311f1-149">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="311f1-149">Texture2D, Texture2DArray</span></span>                | <span data-ttu-id="311f1-150">float2</span><span class="sxs-lookup"><span data-stu-id="311f1-150">float2</span></span>         |
| <span data-ttu-id="311f1-151">Texture3D, TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="311f1-151">Texture3D, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="311f1-152">float3</span><span class="sxs-lookup"><span data-stu-id="311f1-152">float3</span></span>         |
| <span data-ttu-id="311f1-153">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="311f1-153">Texture2DMS, Texture2DMSArray</span></span>            | <span data-ttu-id="311f1-154">no admitido</span><span class="sxs-lookup"><span data-stu-id="311f1-154">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="311f1-155">*Abrazadera* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="311f1-155">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="311f1-156">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="311f1-156">Type: **float**</span></span>

<span data-ttu-id="311f1-157">Un valor opcional en el que se van a fijar los valores LOD de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="311f1-157">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="311f1-158">Por ejemplo, si se pasa 2.0 f para el valor Clamp, se asegura de que ningún ejemplo individual tenga acceso a un nivel de MIP inferior a 2.0 f.</span><span class="sxs-lookup"><span data-stu-id="311f1-158">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="311f1-159">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="311f1-159">Return value</span></span>

<span data-ttu-id="311f1-160">Tipo: **[ **\_ formato de DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="311f1-160">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="311f1-161">Formato de textura, que es uno de los valores con tipo que aparecen [**en \_ formato de DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="311f1-161">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="311f1-162">Vea también</span><span class="sxs-lookup"><span data-stu-id="311f1-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="311f1-163">Métodos SampleGrad</span><span class="sxs-lookup"><span data-stu-id="311f1-163">SampleGrad methods</span></span>](texturecube-samplegrad.md)
</dt> <dt>

[<span data-ttu-id="311f1-164">**TextureCube**</span><span class="sxs-lookup"><span data-stu-id="311f1-164">**TextureCube**</span></span>](texturecube.md)
</dt> </dl>

 

 
