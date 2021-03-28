---
title: 'SampleBias:: SampleBias (S, Float, Float, int, float) (función)'
description: Muestrea un Texture2D, después de aplicar el valor de diferencia al nivel de mipmap, con un valor opcional para Clamp valores de nivel de detalle (LOD) de ejemplo en.
ms.assetid: 4E4A1188-DE45-4A43-B54D-4CA2E66707E3
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
ms.openlocfilehash: d91ce53da6dbf2c1e39f23967d1c1dc36085e764
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104078670"
---
# <a name="samplebiassamplebiassfloatfloatintfloat-function"></a><span data-ttu-id="31e19-104">SampleBias:: SampleBias (S, Float, Float, int, float) (función)</span><span class="sxs-lookup"><span data-stu-id="31e19-104">SampleBias::SampleBias(S,float,float,int,float) function</span></span>

<span data-ttu-id="31e19-105">Muestrea un [**Texture2D**](sm5-object-texture2d.md), después de aplicar el valor de diferencia al nivel de mipmap, con un valor opcional para Clamp valores de nivel de detalle (LOD) de ejemplo en.</span><span class="sxs-lookup"><span data-stu-id="31e19-105">Samples a [**Texture2D**](sm5-object-texture2d.md), after applying the bias value to the mipmap level, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span>

## <a name="syntax"></a><span data-ttu-id="31e19-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="31e19-106">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleBias(
  in SamplerState S,
  in float        Location,
  in float        Bias,
  in int          Offset,
  in float        Clamp
);
```



## <a name="parameters"></a><span data-ttu-id="31e19-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="31e19-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31e19-108">*S* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="31e19-108">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31e19-109">Tipo: **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="31e19-109">Type: **SamplerState**</span></span>

<span data-ttu-id="31e19-110">Un [Estado de muestra](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="31e19-110">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="31e19-111">Se trata de un objeto declarado en un archivo de efectos que contiene las asignaciones de estado.</span><span class="sxs-lookup"><span data-stu-id="31e19-111">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="31e19-112">*Ubicación* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="31e19-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31e19-113">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="31e19-113">Type: **float**</span></span>

<span data-ttu-id="31e19-114">Las coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="31e19-114">The texture coordinates.</span></span> <span data-ttu-id="31e19-115">El tipo de argumento depende del tipo de objeto de textura.</span><span class="sxs-lookup"><span data-stu-id="31e19-115">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="31e19-116">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="31e19-116">Texture-Object Type</span></span>                    | <span data-ttu-id="31e19-117">Tipo de parámetro</span><span class="sxs-lookup"><span data-stu-id="31e19-117">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="31e19-118">Texture1D</span><span class="sxs-lookup"><span data-stu-id="31e19-118">Texture1D</span></span>                              | <span data-ttu-id="31e19-119">FLOAT</span><span class="sxs-lookup"><span data-stu-id="31e19-119">float</span></span>          |
| <span data-ttu-id="31e19-120">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="31e19-120">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="31e19-121">float2</span><span class="sxs-lookup"><span data-stu-id="31e19-121">float2</span></span>         |
| <span data-ttu-id="31e19-122">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="31e19-122">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="31e19-123">float3</span><span class="sxs-lookup"><span data-stu-id="31e19-123">float3</span></span>         |
| <span data-ttu-id="31e19-124">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="31e19-124">TextureCubeArray</span></span>                       | <span data-ttu-id="31e19-125">float4</span><span class="sxs-lookup"><span data-stu-id="31e19-125">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="31e19-126">*Bias* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="31e19-126">*Bias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31e19-127">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="31e19-127">Type: **float**</span></span>

<span data-ttu-id="31e19-128">El valor de diferencia, que es un número de punto flotante entre 0,0 y 1,0, ambos inclusive, se aplica a un nivel de MIP antes del muestreo.</span><span class="sxs-lookup"><span data-stu-id="31e19-128">The bias value, which is a floating-point number between 0.0 and 1.0 inclusive, is applied to a mip level before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="31e19-129">*Desplazamiento* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="31e19-129">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31e19-130">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="31e19-130">Type: **int**</span></span>

<span data-ttu-id="31e19-131">Desplazamiento de coordenadas de textura opcional, que se puede usar para cualquier tipo de objeto de textura. el desplazamiento se aplica a la ubicación antes del muestreo.</span><span class="sxs-lookup"><span data-stu-id="31e19-131">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="31e19-132">Use un desplazamiento solo en un entero miplevel; de lo contrario, puede obtener resultados que no se traduzcan bien al hardware.</span><span class="sxs-lookup"><span data-stu-id="31e19-132">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="31e19-133">El tipo de argumento depende del tipo de objeto de textura.</span><span class="sxs-lookup"><span data-stu-id="31e19-133">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="31e19-134">Para obtener más información, vea [aplicar desplazamientos enteros](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="31e19-134">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="31e19-135">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="31e19-135">Texture-Object Type</span></span>           | <span data-ttu-id="31e19-136">Tipo de parámetro</span><span class="sxs-lookup"><span data-stu-id="31e19-136">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="31e19-137">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="31e19-137">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="31e19-138">int</span><span class="sxs-lookup"><span data-stu-id="31e19-138">int</span></span>            |
| <span data-ttu-id="31e19-139">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="31e19-139">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="31e19-140">int2</span><span class="sxs-lookup"><span data-stu-id="31e19-140">int2</span></span>           |
| <span data-ttu-id="31e19-141">Texture3D</span><span class="sxs-lookup"><span data-stu-id="31e19-141">Texture3D</span></span>                     | <span data-ttu-id="31e19-142">int3</span><span class="sxs-lookup"><span data-stu-id="31e19-142">int3</span></span>           |
| <span data-ttu-id="31e19-143">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="31e19-143">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="31e19-144">no admitido</span><span class="sxs-lookup"><span data-stu-id="31e19-144">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="31e19-145">*Abrazadera* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="31e19-145">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31e19-146">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="31e19-146">Type: **float**</span></span>

<span data-ttu-id="31e19-147">Un valor opcional en el que se van a fijar los valores LOD de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="31e19-147">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="31e19-148">Por ejemplo, si se pasa 2.0 f para el valor Clamp, se asegura de que ningún ejemplo individual tenga acceso a un nivel de MIP inferior a 2.0 f.</span><span class="sxs-lookup"><span data-stu-id="31e19-148">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31e19-149">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="31e19-149">Return value</span></span>

<span data-ttu-id="31e19-150">Tipo: **[ **\_ formato de DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="31e19-150">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="31e19-151">Formato de textura, que es uno de los valores con tipo que aparecen [**en \_ formato de DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="31e19-151">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="31e19-152">Vea también</span><span class="sxs-lookup"><span data-stu-id="31e19-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31e19-153">Métodos SampleBias</span><span class="sxs-lookup"><span data-stu-id="31e19-153">SampleBias methods</span></span>](texture2d-samplebias.md)
</dt> </dl>

 

 
