---
title: 'Función SampleBias:: SampleBias (S, Float, Float, int, Float, uint) para Texture2DArray'
description: 'La función SampleBias:: SampleBias (S, Float, Float, int, Float, uint) para Texture2DArray muestrea una textura después de aplicar el valor de Bias al nivel de mipmap.'
ms.assetid: 38DC341D-477A-4709-AC97-EB796A40C4B2
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
ms.openlocfilehash: ab86510f1450080844a6fe7e476381e81bed1ce1
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/16/2021
ms.locfileid: "104987367"
---
# <a name="samplebiassamplebiassfloatfloatintfloatuint-function-for-texture2darray"></a><span data-ttu-id="1f1d9-104">Función SampleBias:: SampleBias (S, Float, Float, int, Float, uint) para Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="1f1d9-104">SampleBias::SampleBias(S,float,float,int,float,uint) function for Texture2DArray</span></span>

<span data-ttu-id="1f1d9-105">Muestrea una textura, después de aplicar el valor de diferencia al nivel de mipmap, con un valor opcional para Clamp valores de nivel de detalle (LOD) de ejemplo en.</span><span class="sxs-lookup"><span data-stu-id="1f1d9-105">Samples a texture, after applying the bias value to the mipmap level, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span> <span data-ttu-id="1f1d9-106">Devuelve el estado de la operación.</span><span class="sxs-lookup"><span data-stu-id="1f1d9-106">Returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f1d9-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1f1d9-107">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="1f1d9-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1f1d9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f1d9-109">*S* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="1f1d9-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f1d9-110">Tipo: **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="1f1d9-110">Type: **SamplerState**</span></span>

<span data-ttu-id="1f1d9-111">Un [Estado de muestra](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="1f1d9-111">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="1f1d9-112">Se trata de un objeto declarado en un archivo de efectos que contiene las asignaciones de estado.</span><span class="sxs-lookup"><span data-stu-id="1f1d9-112">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="1f1d9-113">*Ubicación* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="1f1d9-113">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f1d9-114">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="1f1d9-114">Type: **float**</span></span>

<span data-ttu-id="1f1d9-115">Las coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="1f1d9-115">The texture coordinates.</span></span> <span data-ttu-id="1f1d9-116">El tipo de argumento depende del tipo de objeto de textura.</span><span class="sxs-lookup"><span data-stu-id="1f1d9-116">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="1f1d9-117">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="1f1d9-117">Texture-Object Type</span></span>                    | <span data-ttu-id="1f1d9-118">Tipo de parámetro</span><span class="sxs-lookup"><span data-stu-id="1f1d9-118">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="1f1d9-119">Texture1D</span><span class="sxs-lookup"><span data-stu-id="1f1d9-119">Texture1D</span></span>                              | <span data-ttu-id="1f1d9-120">FLOAT</span><span class="sxs-lookup"><span data-stu-id="1f1d9-120">float</span></span>          |
| <span data-ttu-id="1f1d9-121">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="1f1d9-121">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="1f1d9-122">float2</span><span class="sxs-lookup"><span data-stu-id="1f1d9-122">float2</span></span>         |
| <span data-ttu-id="1f1d9-123">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="1f1d9-123">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="1f1d9-124">float3</span><span class="sxs-lookup"><span data-stu-id="1f1d9-124">float3</span></span>         |
| <span data-ttu-id="1f1d9-125">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="1f1d9-125">TextureCubeArray</span></span>                       | <span data-ttu-id="1f1d9-126">float4</span><span class="sxs-lookup"><span data-stu-id="1f1d9-126">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="1f1d9-127">*Bias* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1f1d9-127">*Bias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f1d9-128">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="1f1d9-128">Type: **float**</span></span>

<span data-ttu-id="1f1d9-129">El valor de diferencia, que es un número de punto flotante entre 0,0 y 1,0, ambos inclusive, se aplica a un nivel de MIP antes del muestreo.</span><span class="sxs-lookup"><span data-stu-id="1f1d9-129">The bias value, which is a floating-point number between 0.0 and 1.0 inclusive, is applied to a mip level before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="1f1d9-130">*Desplazamiento* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1f1d9-130">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f1d9-131">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="1f1d9-131">Type: **int**</span></span>

<span data-ttu-id="1f1d9-132">Desplazamiento de coordenadas de textura opcional, que se puede usar para cualquier tipo de objeto de textura. el desplazamiento se aplica a la ubicación antes del muestreo.</span><span class="sxs-lookup"><span data-stu-id="1f1d9-132">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="1f1d9-133">Use un desplazamiento solo en un entero miplevel; de lo contrario, puede obtener resultados que no se traduzcan bien al hardware.</span><span class="sxs-lookup"><span data-stu-id="1f1d9-133">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="1f1d9-134">El tipo de argumento depende del tipo de objeto de textura.</span><span class="sxs-lookup"><span data-stu-id="1f1d9-134">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="1f1d9-135">Para obtener más información, vea [aplicar desplazamientos enteros](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="1f1d9-135">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="1f1d9-136">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="1f1d9-136">Texture-Object Type</span></span>           | <span data-ttu-id="1f1d9-137">Tipo de parámetro</span><span class="sxs-lookup"><span data-stu-id="1f1d9-137">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="1f1d9-138">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="1f1d9-138">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="1f1d9-139">int</span><span class="sxs-lookup"><span data-stu-id="1f1d9-139">int</span></span>            |
| <span data-ttu-id="1f1d9-140">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="1f1d9-140">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="1f1d9-141">int2</span><span class="sxs-lookup"><span data-stu-id="1f1d9-141">int2</span></span>           |
| <span data-ttu-id="1f1d9-142">Texture3D</span><span class="sxs-lookup"><span data-stu-id="1f1d9-142">Texture3D</span></span>                     | <span data-ttu-id="1f1d9-143">int3</span><span class="sxs-lookup"><span data-stu-id="1f1d9-143">int3</span></span>           |
| <span data-ttu-id="1f1d9-144">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="1f1d9-144">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="1f1d9-145">no admitido</span><span class="sxs-lookup"><span data-stu-id="1f1d9-145">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="1f1d9-146">*Abrazadera* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1f1d9-146">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f1d9-147">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="1f1d9-147">Type: **float**</span></span>

<span data-ttu-id="1f1d9-148">Un valor opcional en el que se van a fijar los valores LOD de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="1f1d9-148">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="1f1d9-149">Por ejemplo, si se pasa 2.0 f para el valor Clamp, se asegura de que ningún ejemplo individual tenga acceso a un nivel de MIP inferior a 2.0 f.</span><span class="sxs-lookup"><span data-stu-id="1f1d9-149">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> <dt>

<span data-ttu-id="1f1d9-150">*Estado* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="1f1d9-150">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1f1d9-151">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="1f1d9-151">Type: **uint**</span></span>

<span data-ttu-id="1f1d9-152">Estado de la operación.</span><span class="sxs-lookup"><span data-stu-id="1f1d9-152">The status of the operation.</span></span> <span data-ttu-id="1f1d9-153">No se puede tener acceso directamente al estado. en su lugar, pase el estado a la función intrínseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="1f1d9-153">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="1f1d9-154">**CheckAccessFullyMapped** devuelve **true** si todos los valores de la operación de **ejemplo**, **recopilación** o **carga** correspondiente han tenido acceso a los mosaicos asignados en un [recurso en mosaico](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="1f1d9-154">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="1f1d9-155">Si se tomó algún valor de un mosaico sin asignar, **CheckAccessFullyMapped** devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="1f1d9-155">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f1d9-156">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1f1d9-156">Return value</span></span>

<span data-ttu-id="1f1d9-157">Tipo: **[ **\_ formato de DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="1f1d9-157">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="1f1d9-158">Formato de textura, que es uno de los valores con tipo que aparecen [**en \_ formato de DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="1f1d9-158">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="1f1d9-159">Vea también</span><span class="sxs-lookup"><span data-stu-id="1f1d9-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f1d9-160">Métodos SampleBias</span><span class="sxs-lookup"><span data-stu-id="1f1d9-160">SampleBias methods</span></span>](texture2darray-samplebias.md)
</dt> </dl>

 

 
