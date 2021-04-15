---
title: 'SampleBias:: SampleBias (S, Float, Float, int, float) (función)'
description: 'Muestrea una textura, después de aplicar el valor de diferencia al nivel de mipmap, con un valor opcional para Clamp valores de nivel de detalle (LOD) de ejemplo en. | SampleBias:: SampleBias (S, Float, Float, int, float) (función)'
ms.assetid: C252F1D1-51F9-48E3-BD74-3B050E0E16E0
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
ms.openlocfilehash: 16cc939de3bffe32dd26380b05eb65afac05114d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986254"
---
# <a name="samplebiassamplebiassfloatfloatintfloat-function"></a><span data-ttu-id="90ae1-105">SampleBias:: SampleBias (S, Float, Float, int, float) (función)</span><span class="sxs-lookup"><span data-stu-id="90ae1-105">SampleBias::SampleBias(S,float,float,int,float) function</span></span>

<span data-ttu-id="90ae1-106">Muestrea una textura, después de aplicar el valor de diferencia al nivel de mipmap, con un valor opcional para Clamp valores de nivel de detalle (LOD) de ejemplo en.</span><span class="sxs-lookup"><span data-stu-id="90ae1-106">Samples a texture, after applying the bias value to the mipmap level, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span>

## <a name="syntax"></a><span data-ttu-id="90ae1-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="90ae1-107">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleBias(
  in SamplerState S,
  in float        Location,
  in float        Bias,
  in int          Offset,
  in float        Clamp
);
```



## <a name="parameters"></a><span data-ttu-id="90ae1-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="90ae1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90ae1-109">*S* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="90ae1-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90ae1-110">Tipo: **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="90ae1-110">Type: **SamplerState**</span></span>

<span data-ttu-id="90ae1-111">Un [Estado de muestra](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="90ae1-111">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="90ae1-112">Se trata de un objeto declarado en un archivo de efectos que contiene las asignaciones de estado.</span><span class="sxs-lookup"><span data-stu-id="90ae1-112">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="90ae1-113">*Ubicación* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="90ae1-113">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90ae1-114">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="90ae1-114">Type: **float**</span></span>

<span data-ttu-id="90ae1-115">Las coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="90ae1-115">The texture coordinates.</span></span> <span data-ttu-id="90ae1-116">El tipo de argumento depende del tipo de objeto de textura.</span><span class="sxs-lookup"><span data-stu-id="90ae1-116">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="90ae1-117">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="90ae1-117">Texture-Object Type</span></span>                    | <span data-ttu-id="90ae1-118">Tipo de parámetro</span><span class="sxs-lookup"><span data-stu-id="90ae1-118">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="90ae1-119">Texture1D</span><span class="sxs-lookup"><span data-stu-id="90ae1-119">Texture1D</span></span>                              | <span data-ttu-id="90ae1-120">FLOAT</span><span class="sxs-lookup"><span data-stu-id="90ae1-120">float</span></span>          |
| <span data-ttu-id="90ae1-121">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="90ae1-121">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="90ae1-122">float2</span><span class="sxs-lookup"><span data-stu-id="90ae1-122">float2</span></span>         |
| <span data-ttu-id="90ae1-123">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="90ae1-123">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="90ae1-124">float3</span><span class="sxs-lookup"><span data-stu-id="90ae1-124">float3</span></span>         |
| <span data-ttu-id="90ae1-125">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="90ae1-125">TextureCubeArray</span></span>                       | <span data-ttu-id="90ae1-126">float4</span><span class="sxs-lookup"><span data-stu-id="90ae1-126">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="90ae1-127">*Bias* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="90ae1-127">*Bias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90ae1-128">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="90ae1-128">Type: **float**</span></span>

<span data-ttu-id="90ae1-129">El valor de diferencia, que es un número de punto flotante entre 0,0 y 1,0, ambos inclusive, se aplica a un nivel de MIP antes del muestreo.</span><span class="sxs-lookup"><span data-stu-id="90ae1-129">The bias value, which is a floating-point number between 0.0 and 1.0 inclusive, is applied to a mip level before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="90ae1-130">*Desplazamiento* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="90ae1-130">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90ae1-131">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="90ae1-131">Type: **int**</span></span>

<span data-ttu-id="90ae1-132">Desplazamiento de coordenadas de textura opcional, que se puede usar para cualquier tipo de objeto de textura. el desplazamiento se aplica a la ubicación antes del muestreo.</span><span class="sxs-lookup"><span data-stu-id="90ae1-132">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="90ae1-133">Use un desplazamiento solo en un entero miplevel; de lo contrario, puede obtener resultados que no se traduzcan bien al hardware.</span><span class="sxs-lookup"><span data-stu-id="90ae1-133">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="90ae1-134">El tipo de argumento depende del tipo de objeto de textura.</span><span class="sxs-lookup"><span data-stu-id="90ae1-134">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="90ae1-135">Para obtener más información, vea [aplicar desplazamientos enteros](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="90ae1-135">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="90ae1-136">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="90ae1-136">Texture-Object Type</span></span>           | <span data-ttu-id="90ae1-137">Tipo de parámetro</span><span class="sxs-lookup"><span data-stu-id="90ae1-137">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="90ae1-138">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="90ae1-138">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="90ae1-139">int</span><span class="sxs-lookup"><span data-stu-id="90ae1-139">int</span></span>            |
| <span data-ttu-id="90ae1-140">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="90ae1-140">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="90ae1-141">int2</span><span class="sxs-lookup"><span data-stu-id="90ae1-141">int2</span></span>           |
| <span data-ttu-id="90ae1-142">Texture3D</span><span class="sxs-lookup"><span data-stu-id="90ae1-142">Texture3D</span></span>                     | <span data-ttu-id="90ae1-143">int3</span><span class="sxs-lookup"><span data-stu-id="90ae1-143">int3</span></span>           |
| <span data-ttu-id="90ae1-144">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="90ae1-144">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="90ae1-145">no admitido</span><span class="sxs-lookup"><span data-stu-id="90ae1-145">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="90ae1-146">*Abrazadera* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="90ae1-146">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90ae1-147">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="90ae1-147">Type: **float**</span></span>

<span data-ttu-id="90ae1-148">Un valor opcional en el que se van a fijar los valores LOD de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="90ae1-148">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="90ae1-149">Por ejemplo, si se pasa 2.0 f para el valor Clamp, se asegura de que ningún ejemplo individual tenga acceso a un nivel de MIP inferior a 2.0 f.</span><span class="sxs-lookup"><span data-stu-id="90ae1-149">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="90ae1-150">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="90ae1-150">Return value</span></span>

<span data-ttu-id="90ae1-151">Tipo: **[ **\_ formato de DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="90ae1-151">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="90ae1-152">Formato de textura, que es uno de los valores con tipo que aparecen [**en \_ formato de DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="90ae1-152">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="90ae1-153">Vea también</span><span class="sxs-lookup"><span data-stu-id="90ae1-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90ae1-154">Métodos SampleBias</span><span class="sxs-lookup"><span data-stu-id="90ae1-154">SampleBias methods</span></span>](texture3d-samplebias.md)
</dt> <dt>

[<span data-ttu-id="90ae1-155">**Texture3D**</span><span class="sxs-lookup"><span data-stu-id="90ae1-155">**Texture3D**</span></span>](sm5-object-texture3d.md)
</dt> </dl>

 

 
