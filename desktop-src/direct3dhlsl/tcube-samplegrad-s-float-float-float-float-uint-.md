---
title: 'Función SampleGrad:: SampleGrad (S, Float, Float, Float, Float, uint) para TextureCube'
description: Muestrea una textura, utilizando un degradado para influir en la forma en que se calcula la ubicación de ejemplo, con un valor opcional para Clamp valores de nivel de detalle (LOD) de ejemplo. Para TextureCube.
ms.assetid: 36DF7846-416A-4F2F-A7F8-44EE768CDEE1
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
ms.openlocfilehash: 3e75bccaeac28aefc50620a5dea31fa62b880332
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/16/2021
ms.locfileid: "104548150"
---
# <a name="samplegradsamplegradsfloatfloatfloatfloatuint-function-for-texturecube"></a><span data-ttu-id="ff12b-105">Función SampleGrad:: SampleGrad (S, Float, Float, Float, Float, uint) para TextureCube</span><span class="sxs-lookup"><span data-stu-id="ff12b-105">SampleGrad::SampleGrad(S,float,float,float,float,uint) function for TextureCube</span></span>

<span data-ttu-id="ff12b-106">Muestrea una textura, utilizando un degradado para influir en la forma en que se calcula la ubicación de ejemplo, con un valor opcional para Clamp valores de nivel de detalle (LOD) de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="ff12b-106">Samples a texture, using a gradient to influence the way the sample location is calculated, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span> <span data-ttu-id="ff12b-107">Devuelve el estado de la operación.</span><span class="sxs-lookup"><span data-stu-id="ff12b-107">Returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff12b-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ff12b-108">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="ff12b-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ff12b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff12b-110">*S* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="ff12b-110">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff12b-111">Tipo: **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="ff12b-111">Type: **SamplerState**</span></span>

<span data-ttu-id="ff12b-112">Un [Estado de muestra](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="ff12b-112">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="ff12b-113">Se trata de un objeto declarado en un archivo de efectos que contiene las asignaciones de estado.</span><span class="sxs-lookup"><span data-stu-id="ff12b-113">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="ff12b-114">*Ubicación* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="ff12b-114">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff12b-115">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="ff12b-115">Type: **float**</span></span>

<span data-ttu-id="ff12b-116">Las coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="ff12b-116">The texture coordinates.</span></span> <span data-ttu-id="ff12b-117">El tipo de argumento depende del tipo de objeto de textura.</span><span class="sxs-lookup"><span data-stu-id="ff12b-117">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="ff12b-118">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="ff12b-118">Texture-Object Type</span></span>                    | <span data-ttu-id="ff12b-119">Tipo de parámetro</span><span class="sxs-lookup"><span data-stu-id="ff12b-119">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="ff12b-120">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ff12b-120">Texture1D</span></span>                              | <span data-ttu-id="ff12b-121">FLOAT</span><span class="sxs-lookup"><span data-stu-id="ff12b-121">float</span></span>          |
| <span data-ttu-id="ff12b-122">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="ff12b-122">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="ff12b-123">float2</span><span class="sxs-lookup"><span data-stu-id="ff12b-123">float2</span></span>         |
| <span data-ttu-id="ff12b-124">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="ff12b-124">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="ff12b-125">float3</span><span class="sxs-lookup"><span data-stu-id="ff12b-125">float3</span></span>         |
| <span data-ttu-id="ff12b-126">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="ff12b-126">TextureCubeArray</span></span>                       | <span data-ttu-id="ff12b-127">float4</span><span class="sxs-lookup"><span data-stu-id="ff12b-127">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="ff12b-128">*DDX* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="ff12b-128">*DDX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff12b-129">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="ff12b-129">Type: **float**</span></span>

<span data-ttu-id="ff12b-130">La tasa de cambio de la geometría de la superficie en la dirección x.</span><span class="sxs-lookup"><span data-stu-id="ff12b-130">The rate of change of the surface geometry in the x direction.</span></span> <span data-ttu-id="ff12b-131">El tipo de argumento depende del tipo de objeto de textura.</span><span class="sxs-lookup"><span data-stu-id="ff12b-131">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="ff12b-132">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="ff12b-132">Texture-Object Type</span></span>                      | <span data-ttu-id="ff12b-133">Tipo de parámetro</span><span class="sxs-lookup"><span data-stu-id="ff12b-133">Parameter Type</span></span> |
|------------------------------------------|----------------|
| <span data-ttu-id="ff12b-134">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="ff12b-134">Texture1D, Texture1DArray</span></span>                | <span data-ttu-id="ff12b-135">FLOAT</span><span class="sxs-lookup"><span data-stu-id="ff12b-135">float</span></span>          |
| <span data-ttu-id="ff12b-136">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="ff12b-136">Texture2D, Texture2DArray</span></span>                | <span data-ttu-id="ff12b-137">float2</span><span class="sxs-lookup"><span data-stu-id="ff12b-137">float2</span></span>         |
| <span data-ttu-id="ff12b-138">Texture3D, TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="ff12b-138">Texture3D, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="ff12b-139">float3</span><span class="sxs-lookup"><span data-stu-id="ff12b-139">float3</span></span>         |
| <span data-ttu-id="ff12b-140">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="ff12b-140">Texture2DMS, Texture2DMSArray</span></span>            | <span data-ttu-id="ff12b-141">no admitido</span><span class="sxs-lookup"><span data-stu-id="ff12b-141">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="ff12b-142">*DDY* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ff12b-142">*DDY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff12b-143">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="ff12b-143">Type: **float**</span></span>

<span data-ttu-id="ff12b-144">La tasa de cambio de la geometría de la superficie en la dirección y.</span><span class="sxs-lookup"><span data-stu-id="ff12b-144">The rate of change of the surface geometry in the y direction.</span></span> <span data-ttu-id="ff12b-145">El tipo de argumento depende del tipo de objeto de textura.</span><span class="sxs-lookup"><span data-stu-id="ff12b-145">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="ff12b-146">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="ff12b-146">Texture-Object Type</span></span>                      | <span data-ttu-id="ff12b-147">Tipo de parámetro</span><span class="sxs-lookup"><span data-stu-id="ff12b-147">Parameter Type</span></span> |
|------------------------------------------|----------------|
| <span data-ttu-id="ff12b-148">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="ff12b-148">Texture1D, Texture1DArray</span></span>                | <span data-ttu-id="ff12b-149">FLOAT</span><span class="sxs-lookup"><span data-stu-id="ff12b-149">float</span></span>          |
| <span data-ttu-id="ff12b-150">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="ff12b-150">Texture2D, Texture2DArray</span></span>                | <span data-ttu-id="ff12b-151">float2</span><span class="sxs-lookup"><span data-stu-id="ff12b-151">float2</span></span>         |
| <span data-ttu-id="ff12b-152">Texture3D, TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="ff12b-152">Texture3D, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="ff12b-153">float3</span><span class="sxs-lookup"><span data-stu-id="ff12b-153">float3</span></span>         |
| <span data-ttu-id="ff12b-154">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="ff12b-154">Texture2DMS, Texture2DMSArray</span></span>            | <span data-ttu-id="ff12b-155">no admitido</span><span class="sxs-lookup"><span data-stu-id="ff12b-155">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="ff12b-156">*Abrazadera* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ff12b-156">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff12b-157">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="ff12b-157">Type: **float**</span></span>

<span data-ttu-id="ff12b-158">Un valor opcional en el que se van a fijar los valores LOD de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="ff12b-158">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="ff12b-159">Por ejemplo, si se pasa 2.0 f para el valor Clamp, se asegura de que ningún ejemplo individual tenga acceso a un nivel de MIP inferior a 2.0 f.</span><span class="sxs-lookup"><span data-stu-id="ff12b-159">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> <dt>

<span data-ttu-id="ff12b-160">*Estado* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="ff12b-160">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ff12b-161">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="ff12b-161">Type: **uint**</span></span>

<span data-ttu-id="ff12b-162">Estado de la operación.</span><span class="sxs-lookup"><span data-stu-id="ff12b-162">The status of the operation.</span></span> <span data-ttu-id="ff12b-163">No se puede tener acceso directamente al estado. en su lugar, pase el estado a la función intrínseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="ff12b-163">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="ff12b-164">**CheckAccessFullyMapped** devuelve **true** si todos los valores de la operación de **ejemplo**, **recopilación** o **carga** correspondiente han tenido acceso a los mosaicos asignados en un [recurso en mosaico](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="ff12b-164">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="ff12b-165">Si se tomó algún valor de un mosaico sin asignar, **CheckAccessFullyMapped** devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="ff12b-165">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ff12b-166">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ff12b-166">Return value</span></span>

<span data-ttu-id="ff12b-167">Tipo: **[ **\_ formato de DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="ff12b-167">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="ff12b-168">Formato de textura, que es uno de los valores con tipo que aparecen [**en \_ formato de DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="ff12b-168">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="ff12b-169">Vea también</span><span class="sxs-lookup"><span data-stu-id="ff12b-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff12b-170">Métodos SampleGrad</span><span class="sxs-lookup"><span data-stu-id="ff12b-170">SampleGrad methods</span></span>](texturecube-samplegrad.md)
</dt> <dt>

[<span data-ttu-id="ff12b-171">**TextureCube**</span><span class="sxs-lookup"><span data-stu-id="ff12b-171">**TextureCube**</span></span>](texturecube.md)
</dt> </dl>

 

 
