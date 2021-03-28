---
title: 'Función SampleCmpLevelZero:: SampleCmpLevelZero (S, Float, Float, int, uint) para Texture2D'
description: Muestrea un Texture2D solo en el nivel 0 de mipmap y compara el resultado con un valor de comparación y, a continuación, devuelve el estado de la operación. Para Texture2D.
ms.assetid: AEFE424F-2C77-434C-B9C0-8173778CB108
keywords:
- SampleCmpLevelZero de función HLSL
topic_type:
- apiref
api_name:
- SampleCmpLevelZero
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3a28dddeb687093a76f4f8bc60c96777468abc9f
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/16/2021
ms.locfileid: "104998856"
---
# <a name="samplecmplevelzerosamplecmplevelzerosfloatfloatintuint-function-for-texture2d"></a><span data-ttu-id="c9cf4-105">Función SampleCmpLevelZero:: SampleCmpLevelZero (S, Float, Float, int, uint) para Texture2D</span><span class="sxs-lookup"><span data-stu-id="c9cf4-105">SampleCmpLevelZero::SampleCmpLevelZero(S,float,float,int,uint) function for Texture2D</span></span>

<span data-ttu-id="c9cf4-106">Muestrea un [**Texture2D**](sm5-object-texture2d.md) solo en el nivel 0 de mipmap y compara el resultado con un valor de comparación.</span><span class="sxs-lookup"><span data-stu-id="c9cf4-106">Samples a [**Texture2D**](sm5-object-texture2d.md) on mipmap level 0 only and compares the result to a comparison value.</span></span> <span data-ttu-id="c9cf4-107">Devuelve el estado de la operación.</span><span class="sxs-lookup"><span data-stu-id="c9cf4-107">Returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9cf4-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c9cf4-108">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleCmpLevelZero(
  in  SamplerState S,
  in  float        Location,
  in  float        CompareValue,
  in  int          Offset,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="c9cf4-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c9cf4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9cf4-110">*S* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="c9cf4-110">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9cf4-111">Tipo: **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="c9cf4-111">Type: **SamplerState**</span></span>

<span data-ttu-id="c9cf4-112">Un [Estado de muestra](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="c9cf4-112">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="c9cf4-113">Se trata de un objeto declarado en un archivo de efectos que contiene las asignaciones de estado.</span><span class="sxs-lookup"><span data-stu-id="c9cf4-113">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="c9cf4-114">*Ubicación* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="c9cf4-114">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9cf4-115">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="c9cf4-115">Type: **float**</span></span>

<span data-ttu-id="c9cf4-116">Las coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="c9cf4-116">The texture coordinates.</span></span> <span data-ttu-id="c9cf4-117">El tipo de argumento depende del tipo de objeto de textura.</span><span class="sxs-lookup"><span data-stu-id="c9cf4-117">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="c9cf4-118">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="c9cf4-118">Texture-Object Type</span></span>                    | <span data-ttu-id="c9cf4-119">Tipo de parámetro</span><span class="sxs-lookup"><span data-stu-id="c9cf4-119">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="c9cf4-120">Texture1D</span><span class="sxs-lookup"><span data-stu-id="c9cf4-120">Texture1D</span></span>                              | <span data-ttu-id="c9cf4-121">FLOAT</span><span class="sxs-lookup"><span data-stu-id="c9cf4-121">float</span></span>          |
| <span data-ttu-id="c9cf4-122">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="c9cf4-122">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="c9cf4-123">float2</span><span class="sxs-lookup"><span data-stu-id="c9cf4-123">float2</span></span>         |
| <span data-ttu-id="c9cf4-124">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="c9cf4-124">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="c9cf4-125">float3</span><span class="sxs-lookup"><span data-stu-id="c9cf4-125">float3</span></span>         |
| <span data-ttu-id="c9cf4-126">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="c9cf4-126">TextureCubeArray</span></span>                       | <span data-ttu-id="c9cf4-127">float4</span><span class="sxs-lookup"><span data-stu-id="c9cf4-127">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="c9cf4-128">*CompareValue* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c9cf4-128">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9cf4-129">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="c9cf4-129">Type: **float**</span></span>

<span data-ttu-id="c9cf4-130">Un valor de punto flotante que se va a utilizar como valor de comparación.</span><span class="sxs-lookup"><span data-stu-id="c9cf4-130">A floating-point value to use as a comparison value.</span></span>

</dd> <dt>

<span data-ttu-id="c9cf4-131">*Desplazamiento* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c9cf4-131">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9cf4-132">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="c9cf4-132">Type: **int**</span></span>

<span data-ttu-id="c9cf4-133">Desplazamiento de coordenadas de textura opcional, que se puede usar para cualquier tipo de objeto de textura. el desplazamiento se aplica a la ubicación antes del muestreo.</span><span class="sxs-lookup"><span data-stu-id="c9cf4-133">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="c9cf4-134">Use un desplazamiento solo en un entero miplevel; de lo contrario, puede obtener resultados que no se traduzcan bien al hardware.</span><span class="sxs-lookup"><span data-stu-id="c9cf4-134">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="c9cf4-135">El tipo de argumento depende del tipo de objeto de textura.</span><span class="sxs-lookup"><span data-stu-id="c9cf4-135">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="c9cf4-136">Para obtener más información, vea [aplicar desplazamientos enteros](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="c9cf4-136">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="c9cf4-137">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="c9cf4-137">Texture-Object Type</span></span>           | <span data-ttu-id="c9cf4-138">Tipo de parámetro</span><span class="sxs-lookup"><span data-stu-id="c9cf4-138">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="c9cf4-139">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="c9cf4-139">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="c9cf4-140">int</span><span class="sxs-lookup"><span data-stu-id="c9cf4-140">int</span></span>            |
| <span data-ttu-id="c9cf4-141">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="c9cf4-141">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="c9cf4-142">int2</span><span class="sxs-lookup"><span data-stu-id="c9cf4-142">int2</span></span>           |
| <span data-ttu-id="c9cf4-143">Texture3D</span><span class="sxs-lookup"><span data-stu-id="c9cf4-143">Texture3D</span></span>                     | <span data-ttu-id="c9cf4-144">int3</span><span class="sxs-lookup"><span data-stu-id="c9cf4-144">int3</span></span>           |
| <span data-ttu-id="c9cf4-145">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="c9cf4-145">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="c9cf4-146">no admitido</span><span class="sxs-lookup"><span data-stu-id="c9cf4-146">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="c9cf4-147">*Estado* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="c9cf4-147">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c9cf4-148">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="c9cf4-148">Type: **uint**</span></span>

<span data-ttu-id="c9cf4-149">Estado de la operación.</span><span class="sxs-lookup"><span data-stu-id="c9cf4-149">The status of the operation.</span></span> <span data-ttu-id="c9cf4-150">No se puede tener acceso directamente al estado. en su lugar, pase el estado a la función intrínseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="c9cf4-150">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="c9cf4-151">**CheckAccessFullyMapped** devuelve **true** si todos los valores de la operación de **ejemplo**, **recopilación** o **carga** correspondiente han tenido acceso a los mosaicos asignados en un [recurso en mosaico](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="c9cf4-151">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="c9cf4-152">Si se tomó algún valor de un mosaico sin asignar, **CheckAccessFullyMapped** devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="c9cf4-152">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9cf4-153">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c9cf4-153">Return value</span></span>

<span data-ttu-id="c9cf4-154">Tipo: **[ **\_ formato de DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="c9cf4-154">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="c9cf4-155">Formato de textura, que es uno de los valores con tipo que aparecen [**en \_ formato de DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="c9cf4-155">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="c9cf4-156">Vea también</span><span class="sxs-lookup"><span data-stu-id="c9cf4-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9cf4-157">Métodos SampleCmpLevelZero</span><span class="sxs-lookup"><span data-stu-id="c9cf4-157">SampleCmpLevelZero methods</span></span>](texture2d-samplecmplevelzero.md)
</dt> </dl>

 

 
