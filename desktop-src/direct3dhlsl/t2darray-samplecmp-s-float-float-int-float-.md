---
title: 'Función SampleCmp:: SampleCmp (S, Float, Float, int, float) para Texture2DArray'
description: Obtenga información sobre cómo esta función muestrea una textura con un valor de comparación para rechazar muestras, con un valor opcional para Clamp valores de nivel de detalle (LOD) de ejemplo en. Para Texture2DArray.
ms.assetid: 6455BF80-2A22-43BB-80A2-61FBEC66C348
keywords:
- SampleCmp de función HLSL
topic_type:
- apiref
api_name:
- SampleCmp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0692166766b9f52a1b6b13719c2427438b59835f
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/16/2021
ms.locfileid: "103821594"
---
# <a name="samplecmpsamplecmpsfloatfloatintfloat-function-for-texture2darray"></a><span data-ttu-id="19fb7-105">Función SampleCmp:: SampleCmp (S, Float, Float, int, float) para Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="19fb7-105">SampleCmp::SampleCmp(S,float,float,int,float) function for Texture2DArray</span></span>

<span data-ttu-id="19fb7-106">Muestrea una textura, utilizando un valor de comparación para rechazar muestras, con un valor opcional para Clamp valores de nivel de detalle (LOD) de ejemplo en.</span><span class="sxs-lookup"><span data-stu-id="19fb7-106">Samples a texture, using a comparison value to reject samples, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span>

## <a name="syntax"></a><span data-ttu-id="19fb7-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="19fb7-107">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleCmp(
  in SamplerState S,
  in float        Location,
  in float        CompareValue,
  in int          Offset,
  in float        Clamp
);
```



## <a name="parameters"></a><span data-ttu-id="19fb7-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="19fb7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19fb7-109">*S* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="19fb7-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19fb7-110">Tipo: **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="19fb7-110">Type: **SamplerState**</span></span>

<span data-ttu-id="19fb7-111">Un [Estado de muestra](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="19fb7-111">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="19fb7-112">Se trata de un objeto declarado en un archivo de efectos que contiene las asignaciones de estado.</span><span class="sxs-lookup"><span data-stu-id="19fb7-112">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="19fb7-113">*Ubicación* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="19fb7-113">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19fb7-114">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="19fb7-114">Type: **float**</span></span>

<span data-ttu-id="19fb7-115">Las coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="19fb7-115">The texture coordinates.</span></span> <span data-ttu-id="19fb7-116">El tipo de argumento depende del tipo de objeto de textura.</span><span class="sxs-lookup"><span data-stu-id="19fb7-116">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="19fb7-117">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="19fb7-117">Texture-Object Type</span></span>                    | <span data-ttu-id="19fb7-118">Tipo de parámetro</span><span class="sxs-lookup"><span data-stu-id="19fb7-118">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="19fb7-119">Texture1D</span><span class="sxs-lookup"><span data-stu-id="19fb7-119">Texture1D</span></span>                              | <span data-ttu-id="19fb7-120">FLOAT</span><span class="sxs-lookup"><span data-stu-id="19fb7-120">float</span></span>          |
| <span data-ttu-id="19fb7-121">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="19fb7-121">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="19fb7-122">float2</span><span class="sxs-lookup"><span data-stu-id="19fb7-122">float2</span></span>         |
| <span data-ttu-id="19fb7-123">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="19fb7-123">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="19fb7-124">float3</span><span class="sxs-lookup"><span data-stu-id="19fb7-124">float3</span></span>         |
| <span data-ttu-id="19fb7-125">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="19fb7-125">TextureCubeArray</span></span>                       | <span data-ttu-id="19fb7-126">float4</span><span class="sxs-lookup"><span data-stu-id="19fb7-126">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="19fb7-127">*CompareValue* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="19fb7-127">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19fb7-128">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="19fb7-128">Type: **float**</span></span>

<span data-ttu-id="19fb7-129">Un valor de punto flotante que se va a utilizar como valor de comparación.</span><span class="sxs-lookup"><span data-stu-id="19fb7-129">A floating-point value to use as a comparison value.</span></span>

</dd> <dt>

<span data-ttu-id="19fb7-130">*Desplazamiento* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="19fb7-130">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19fb7-131">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="19fb7-131">Type: **int**</span></span>

<span data-ttu-id="19fb7-132">Desplazamiento de coordenadas de textura opcional, que se puede usar para cualquier tipo de objeto de textura. el desplazamiento se aplica a la ubicación antes del muestreo.</span><span class="sxs-lookup"><span data-stu-id="19fb7-132">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="19fb7-133">Use un desplazamiento solo en un entero miplevel; de lo contrario, puede obtener resultados que no se traduzcan bien al hardware.</span><span class="sxs-lookup"><span data-stu-id="19fb7-133">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="19fb7-134">El tipo de argumento depende del tipo de objeto de textura.</span><span class="sxs-lookup"><span data-stu-id="19fb7-134">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="19fb7-135">Para obtener más información, vea [aplicar desplazamientos enteros](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="19fb7-135">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="19fb7-136">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="19fb7-136">Texture-Object Type</span></span>           | <span data-ttu-id="19fb7-137">Tipo de parámetro</span><span class="sxs-lookup"><span data-stu-id="19fb7-137">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="19fb7-138">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="19fb7-138">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="19fb7-139">int</span><span class="sxs-lookup"><span data-stu-id="19fb7-139">int</span></span>            |
| <span data-ttu-id="19fb7-140">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="19fb7-140">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="19fb7-141">int2</span><span class="sxs-lookup"><span data-stu-id="19fb7-141">int2</span></span>           |
| <span data-ttu-id="19fb7-142">Texture3D</span><span class="sxs-lookup"><span data-stu-id="19fb7-142">Texture3D</span></span>                     | <span data-ttu-id="19fb7-143">int3</span><span class="sxs-lookup"><span data-stu-id="19fb7-143">int3</span></span>           |
| <span data-ttu-id="19fb7-144">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="19fb7-144">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="19fb7-145">no admitido</span><span class="sxs-lookup"><span data-stu-id="19fb7-145">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="19fb7-146">*Abrazadera* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="19fb7-146">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19fb7-147">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="19fb7-147">Type: **float**</span></span>

<span data-ttu-id="19fb7-148">Un valor opcional en el que se van a fijar los valores LOD de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="19fb7-148">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="19fb7-149">Por ejemplo, si se pasa 2.0 f para el valor Clamp, se asegura de que ningún ejemplo individual tenga acceso a un nivel de MIP inferior a 2.0 f.</span><span class="sxs-lookup"><span data-stu-id="19fb7-149">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19fb7-150">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="19fb7-150">Return value</span></span>

<span data-ttu-id="19fb7-151">Tipo: **[ **\_ formato de DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="19fb7-151">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="19fb7-152">Formato de textura, que es uno de los valores con tipo que aparecen [**en \_ formato de DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="19fb7-152">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="19fb7-153">Vea también</span><span class="sxs-lookup"><span data-stu-id="19fb7-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19fb7-154">Métodos SampleCmp</span><span class="sxs-lookup"><span data-stu-id="19fb7-154">SampleCmp methods</span></span>](texture2darray-samplecmp.md)
</dt> </dl>

 

 
