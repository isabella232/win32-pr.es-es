---
title: 'Función SampleBias:: SampleBias (S, Float, Float, int, Float, uint) para Texture1DArray'
description: 'Muestrea una textura, después de aplicar el valor de diferencia al nivel de mipmap, con un valor opcional para Clamp valores de nivel de detalle (LOD) de ejemplo en. | Función SampleBias:: SampleBias (S, Float, Float, int, Float, uint) para Texture1DArray'
ms.assetid: 6136674B-38F4-4081-82D6-0731604EB1A3
keywords:
- SampleBias de función HLSL
topic_type:
- apiref
api_name:
- SampleBias
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4050503525345803a105d7717e96f6aa7b5c43cd
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/16/2021
ms.locfileid: "104548174"
---
# <a name="samplebiassamplebiassfloatfloatintfloatuint-function-for-texture1darray"></a><span data-ttu-id="633cf-105">Función SampleBias:: SampleBias (S, Float, Float, int, Float, uint) para Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="633cf-105">SampleBias::SampleBias(S,float,float,int,float,uint) function for Texture1DArray</span></span>

<span data-ttu-id="633cf-106">Muestrea una textura, después de aplicar el valor de diferencia al nivel de mipmap, con un valor opcional para Clamp valores de nivel de detalle (LOD) de ejemplo en.</span><span class="sxs-lookup"><span data-stu-id="633cf-106">Samples a texture, after applying the bias value to the mipmap level, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span> <span data-ttu-id="633cf-107">Devuelve el estado de la operación.</span><span class="sxs-lookup"><span data-stu-id="633cf-107">Returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="633cf-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="633cf-108">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleBias(
  in  SamplerState S,
  in  float        Location,
  in  float        Bias,
  in  int          Offset,
  in  float        Clamp,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="633cf-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="633cf-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="633cf-110">*S* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="633cf-110">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="633cf-111">Tipo: **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="633cf-111">Type: **SamplerState**</span></span>

<span data-ttu-id="633cf-112">Un [Estado de muestra](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="633cf-112">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="633cf-113">Se trata de un objeto declarado en un archivo de efectos que contiene las asignaciones de estado.</span><span class="sxs-lookup"><span data-stu-id="633cf-113">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="633cf-114">*Ubicación* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="633cf-114">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="633cf-115">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="633cf-115">Type: **float**</span></span>

<span data-ttu-id="633cf-116">Las coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="633cf-116">The texture coordinates.</span></span> <span data-ttu-id="633cf-117">El tipo de argumento depende del tipo de objeto de textura.</span><span class="sxs-lookup"><span data-stu-id="633cf-117">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="633cf-118">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="633cf-118">Texture-Object Type</span></span>                    | <span data-ttu-id="633cf-119">Tipo de parámetro</span><span class="sxs-lookup"><span data-stu-id="633cf-119">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="633cf-120">Texture1D</span><span class="sxs-lookup"><span data-stu-id="633cf-120">Texture1D</span></span>                              | <span data-ttu-id="633cf-121">FLOAT</span><span class="sxs-lookup"><span data-stu-id="633cf-121">float</span></span>          |
| <span data-ttu-id="633cf-122">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="633cf-122">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="633cf-123">float2</span><span class="sxs-lookup"><span data-stu-id="633cf-123">float2</span></span>         |
| <span data-ttu-id="633cf-124">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="633cf-124">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="633cf-125">float3</span><span class="sxs-lookup"><span data-stu-id="633cf-125">float3</span></span>         |
| <span data-ttu-id="633cf-126">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="633cf-126">TextureCubeArray</span></span>                       | <span data-ttu-id="633cf-127">float4</span><span class="sxs-lookup"><span data-stu-id="633cf-127">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="633cf-128">*Bias* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="633cf-128">*Bias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="633cf-129">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="633cf-129">Type: **float**</span></span>

<span data-ttu-id="633cf-130">El valor de diferencia, que es un número de punto flotante entre 0,0 y 1,0, ambos inclusive, se aplica a un nivel de MIP antes del muestreo.</span><span class="sxs-lookup"><span data-stu-id="633cf-130">The bias value, which is a floating-point number between 0.0 and 1.0 inclusive, is applied to a mip level before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="633cf-131">*Desplazamiento* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="633cf-131">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="633cf-132">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="633cf-132">Type: **int**</span></span>

<span data-ttu-id="633cf-133">Desplazamiento de coordenadas de textura opcional, que se puede usar para cualquier tipo de objeto de textura. el desplazamiento se aplica a la ubicación antes del muestreo.</span><span class="sxs-lookup"><span data-stu-id="633cf-133">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="633cf-134">Use un desplazamiento solo en un entero miplevel; de lo contrario, puede obtener resultados que no se traduzcan bien al hardware.</span><span class="sxs-lookup"><span data-stu-id="633cf-134">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="633cf-135">El tipo de argumento depende del tipo de objeto de textura.</span><span class="sxs-lookup"><span data-stu-id="633cf-135">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="633cf-136">Para obtener más información, vea [aplicar desplazamientos enteros](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="633cf-136">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="633cf-137">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="633cf-137">Texture-Object Type</span></span>           | <span data-ttu-id="633cf-138">Tipo de parámetro</span><span class="sxs-lookup"><span data-stu-id="633cf-138">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="633cf-139">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="633cf-139">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="633cf-140">int</span><span class="sxs-lookup"><span data-stu-id="633cf-140">int</span></span>            |
| <span data-ttu-id="633cf-141">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="633cf-141">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="633cf-142">int2</span><span class="sxs-lookup"><span data-stu-id="633cf-142">int2</span></span>           |
| <span data-ttu-id="633cf-143">Texture3D</span><span class="sxs-lookup"><span data-stu-id="633cf-143">Texture3D</span></span>                     | <span data-ttu-id="633cf-144">int3</span><span class="sxs-lookup"><span data-stu-id="633cf-144">int3</span></span>           |
| <span data-ttu-id="633cf-145">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="633cf-145">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="633cf-146">no admitido</span><span class="sxs-lookup"><span data-stu-id="633cf-146">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="633cf-147">*Abrazadera* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="633cf-147">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="633cf-148">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="633cf-148">Type: **float**</span></span>

<span data-ttu-id="633cf-149">Un valor opcional en el que se van a fijar los valores LOD de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="633cf-149">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="633cf-150">Por ejemplo, si se pasa 2.0 f para el valor Clamp, se asegura de que ningún ejemplo individual tenga acceso a un nivel de MIP inferior a 2.0 f.</span><span class="sxs-lookup"><span data-stu-id="633cf-150">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> <dt>

<span data-ttu-id="633cf-151">*Estado* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="633cf-151">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="633cf-152">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="633cf-152">Type: **uint**</span></span>

<span data-ttu-id="633cf-153">Estado de la operación.</span><span class="sxs-lookup"><span data-stu-id="633cf-153">The status of the operation.</span></span> <span data-ttu-id="633cf-154">No se puede tener acceso directamente al estado. en su lugar, pase el estado a la función intrínseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="633cf-154">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="633cf-155">**CheckAccessFullyMapped** devuelve **true** si todos los valores de la operación de **ejemplo**, **recopilación** o **carga** correspondiente han tenido acceso a los mosaicos asignados en un [recurso en mosaico](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="633cf-155">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="633cf-156">Si se tomó algún valor de un mosaico sin asignar, **CheckAccessFullyMapped** devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="633cf-156">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="633cf-157">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="633cf-157">Return value</span></span>

<span data-ttu-id="633cf-158">Tipo: **[ **\_ formato de DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="633cf-158">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="633cf-159">Formato de textura, que es uno de los valores con tipo que aparecen [**en \_ formato de DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="633cf-159">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="633cf-160">Vea también</span><span class="sxs-lookup"><span data-stu-id="633cf-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="633cf-161">Métodos SampleBias</span><span class="sxs-lookup"><span data-stu-id="633cf-161">SampleBias methods</span></span>](texture1darray-samplebias.md)
</dt> </dl>

 

 
