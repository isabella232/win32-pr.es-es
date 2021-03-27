---
title: 'Función SampleCmp:: SampleCmp (S, Float, Float, int, float) para Texture2D'
description: Esta función muestrea un Texture2D con un valor de comparación para rechazar ejemplos, con un valor opcional para Clamp valores de nivel de detalle (LOD) de ejemplo en.
ms.assetid: 1B5E6559-2524-4557-8F43-7AF258C39FB2
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
ms.openlocfilehash: 9df6a84fff7c6988ed9333584a7196fa06ad30ec
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/16/2021
ms.locfileid: "104987378"
---
# <a name="samplecmpsamplecmpsfloatfloatintfloat-function-for-texture2d"></a><span data-ttu-id="72908-104">Función SampleCmp:: SampleCmp (S, Float, Float, int, float) para Texture2D</span><span class="sxs-lookup"><span data-stu-id="72908-104">SampleCmp::SampleCmp(S,float,float,int,float) function for Texture2D</span></span>

<span data-ttu-id="72908-105">Muestrea un [**Texture2D**](sm5-object-texture2d.md), con un valor de comparación para rechazar ejemplos, con un valor opcional para Clamp valores de nivel de detalle (LOD) de ejemplo en.</span><span class="sxs-lookup"><span data-stu-id="72908-105">Samples a [**Texture2D**](sm5-object-texture2d.md), using a comparison value to reject samples, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span>

## <a name="syntax"></a><span data-ttu-id="72908-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="72908-106">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleCmp(
  in SamplerState S,
  in float        Location,
  in float        CompareValue,
  in int          Offset,
  in float        Clamp
);
```



## <a name="parameters"></a><span data-ttu-id="72908-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="72908-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="72908-108">*S* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="72908-108">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72908-109">Tipo: **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="72908-109">Type: **SamplerState**</span></span>

<span data-ttu-id="72908-110">Un [Estado de muestra](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="72908-110">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="72908-111">Se trata de un objeto declarado en un archivo de efectos que contiene las asignaciones de estado.</span><span class="sxs-lookup"><span data-stu-id="72908-111">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="72908-112">*Ubicación* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="72908-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72908-113">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="72908-113">Type: **float**</span></span>

<span data-ttu-id="72908-114">Las coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="72908-114">The texture coordinates.</span></span> <span data-ttu-id="72908-115">El tipo de argumento depende del tipo de objeto de textura.</span><span class="sxs-lookup"><span data-stu-id="72908-115">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="72908-116">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="72908-116">Texture-Object Type</span></span>                    | <span data-ttu-id="72908-117">Tipo de parámetro</span><span class="sxs-lookup"><span data-stu-id="72908-117">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="72908-118">Texture1D</span><span class="sxs-lookup"><span data-stu-id="72908-118">Texture1D</span></span>                              | <span data-ttu-id="72908-119">FLOAT</span><span class="sxs-lookup"><span data-stu-id="72908-119">float</span></span>          |
| <span data-ttu-id="72908-120">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="72908-120">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="72908-121">float2</span><span class="sxs-lookup"><span data-stu-id="72908-121">float2</span></span>         |
| <span data-ttu-id="72908-122">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="72908-122">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="72908-123">float3</span><span class="sxs-lookup"><span data-stu-id="72908-123">float3</span></span>         |
| <span data-ttu-id="72908-124">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="72908-124">TextureCubeArray</span></span>                       | <span data-ttu-id="72908-125">float4</span><span class="sxs-lookup"><span data-stu-id="72908-125">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="72908-126">*CompareValue* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="72908-126">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72908-127">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="72908-127">Type: **float**</span></span>

<span data-ttu-id="72908-128">Un valor de punto flotante que se va a utilizar como valor de comparación.</span><span class="sxs-lookup"><span data-stu-id="72908-128">A floating-point value to use as a comparison value.</span></span>

</dd> <dt>

<span data-ttu-id="72908-129">*Desplazamiento* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="72908-129">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72908-130">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="72908-130">Type: **int**</span></span>

<span data-ttu-id="72908-131">Desplazamiento de coordenadas de textura opcional, que se puede usar para cualquier tipo de objeto de textura. el desplazamiento se aplica a la ubicación antes del muestreo.</span><span class="sxs-lookup"><span data-stu-id="72908-131">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="72908-132">Use un desplazamiento solo en un entero miplevel; de lo contrario, puede obtener resultados que no se traduzcan bien al hardware.</span><span class="sxs-lookup"><span data-stu-id="72908-132">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="72908-133">El tipo de argumento depende del tipo de objeto de textura.</span><span class="sxs-lookup"><span data-stu-id="72908-133">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="72908-134">Para obtener más información, vea [aplicar desplazamientos enteros](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="72908-134">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="72908-135">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="72908-135">Texture-Object Type</span></span>           | <span data-ttu-id="72908-136">Tipo de parámetro</span><span class="sxs-lookup"><span data-stu-id="72908-136">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="72908-137">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="72908-137">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="72908-138">int</span><span class="sxs-lookup"><span data-stu-id="72908-138">int</span></span>            |
| <span data-ttu-id="72908-139">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="72908-139">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="72908-140">int2</span><span class="sxs-lookup"><span data-stu-id="72908-140">int2</span></span>           |
| <span data-ttu-id="72908-141">Texture3D</span><span class="sxs-lookup"><span data-stu-id="72908-141">Texture3D</span></span>                     | <span data-ttu-id="72908-142">int3</span><span class="sxs-lookup"><span data-stu-id="72908-142">int3</span></span>           |
| <span data-ttu-id="72908-143">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="72908-143">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="72908-144">no admitido</span><span class="sxs-lookup"><span data-stu-id="72908-144">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="72908-145">*Abrazadera* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="72908-145">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72908-146">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="72908-146">Type: **float**</span></span>

<span data-ttu-id="72908-147">Un valor opcional en el que se van a fijar los valores LOD de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="72908-147">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="72908-148">Por ejemplo, si se pasa 2.0 f para el valor Clamp, se asegura de que ningún ejemplo individual tenga acceso a un nivel de MIP inferior a 2.0 f.</span><span class="sxs-lookup"><span data-stu-id="72908-148">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="72908-149">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="72908-149">Return value</span></span>

<span data-ttu-id="72908-150">Tipo: **[ **\_ formato de DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="72908-150">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="72908-151">Formato de textura, que es uno de los valores con tipo que aparecen [**en \_ formato de DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="72908-151">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="72908-152">Vea también</span><span class="sxs-lookup"><span data-stu-id="72908-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72908-153">Métodos SampleCmp</span><span class="sxs-lookup"><span data-stu-id="72908-153">SampleCmp methods</span></span>](texture2d-samplecmp.md)
</dt> </dl>

 

 
