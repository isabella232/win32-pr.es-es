---
title: 'Función SampleCmpLevelZero:: SampleCmpLevelZero (S, Float, Float, int, uint) para Texture1D'
description: Muestrea solo una textura en el nivel 0 del mipmap y compara el resultado con un valor de comparación y, a continuación, devuelve el estado de la operación. Para Texture1D.
ms.assetid: A2F7FD4A-49D8-41B3-A5AF-7B54A8B5266C
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
ms.openlocfilehash: a63644cff0bcc5a437ff4ae3e1dffba8f5a0676c
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/16/2021
ms.locfileid: "104280543"
---
# <a name="samplecmplevelzerosamplecmplevelzerosfloatfloatintuint-function-for-texture1d"></a><span data-ttu-id="938d3-105">Función SampleCmpLevelZero:: SampleCmpLevelZero (S, Float, Float, int, uint) para Texture1D</span><span class="sxs-lookup"><span data-stu-id="938d3-105">SampleCmpLevelZero::SampleCmpLevelZero(S,float,float,int,uint) function for Texture1D</span></span>

<span data-ttu-id="938d3-106">Muestrea solo una textura en el nivel 0 del mipmap y compara el resultado con un valor de comparación.</span><span class="sxs-lookup"><span data-stu-id="938d3-106">Samples a texture on mipmap level 0 only and compares the result to a comparison value.</span></span> <span data-ttu-id="938d3-107">Devuelve el estado de la operación.</span><span class="sxs-lookup"><span data-stu-id="938d3-107">Returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="938d3-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="938d3-108">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleCmpLevelZero(
  in  SamplerState S,
  in  float        Location,
  in  float        CompareValue,
  in  int          Offset,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="938d3-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="938d3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="938d3-110">*S* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="938d3-110">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="938d3-111">Tipo: **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="938d3-111">Type: **SamplerState**</span></span>

<span data-ttu-id="938d3-112">Un [Estado de muestra](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="938d3-112">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="938d3-113">Se trata de un objeto declarado en un archivo de efectos que contiene las asignaciones de estado.</span><span class="sxs-lookup"><span data-stu-id="938d3-113">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="938d3-114">*Ubicación* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="938d3-114">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="938d3-115">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="938d3-115">Type: **float**</span></span>

<span data-ttu-id="938d3-116">Las coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="938d3-116">The texture coordinates.</span></span> <span data-ttu-id="938d3-117">El tipo de argumento depende del tipo de objeto de textura.</span><span class="sxs-lookup"><span data-stu-id="938d3-117">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="938d3-118">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="938d3-118">Texture-Object Type</span></span>                    | <span data-ttu-id="938d3-119">Tipo de parámetro</span><span class="sxs-lookup"><span data-stu-id="938d3-119">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="938d3-120">Texture1D</span><span class="sxs-lookup"><span data-stu-id="938d3-120">Texture1D</span></span>                              | <span data-ttu-id="938d3-121">FLOAT</span><span class="sxs-lookup"><span data-stu-id="938d3-121">float</span></span>          |
| <span data-ttu-id="938d3-122">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="938d3-122">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="938d3-123">float2</span><span class="sxs-lookup"><span data-stu-id="938d3-123">float2</span></span>         |
| <span data-ttu-id="938d3-124">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="938d3-124">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="938d3-125">float3</span><span class="sxs-lookup"><span data-stu-id="938d3-125">float3</span></span>         |
| <span data-ttu-id="938d3-126">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="938d3-126">TextureCubeArray</span></span>                       | <span data-ttu-id="938d3-127">float4</span><span class="sxs-lookup"><span data-stu-id="938d3-127">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="938d3-128">*CompareValue* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="938d3-128">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="938d3-129">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="938d3-129">Type: **float**</span></span>

<span data-ttu-id="938d3-130">Un valor de punto flotante que se va a utilizar como valor de comparación.</span><span class="sxs-lookup"><span data-stu-id="938d3-130">A floating-point value to use as a comparison value.</span></span>

</dd> <dt>

<span data-ttu-id="938d3-131">*Desplazamiento* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="938d3-131">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="938d3-132">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="938d3-132">Type: **int**</span></span>

<span data-ttu-id="938d3-133">Desplazamiento de coordenadas de textura opcional, que se puede usar para cualquier tipo de objeto de textura. el desplazamiento se aplica a la ubicación antes del muestreo.</span><span class="sxs-lookup"><span data-stu-id="938d3-133">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="938d3-134">Use un desplazamiento solo en un entero miplevel; de lo contrario, puede obtener resultados que no se traduzcan bien al hardware.</span><span class="sxs-lookup"><span data-stu-id="938d3-134">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="938d3-135">El tipo de argumento depende del tipo de objeto de textura.</span><span class="sxs-lookup"><span data-stu-id="938d3-135">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="938d3-136">Para obtener más información, vea [aplicar desplazamientos enteros](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="938d3-136">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="938d3-137">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="938d3-137">Texture-Object Type</span></span>           | <span data-ttu-id="938d3-138">Tipo de parámetro</span><span class="sxs-lookup"><span data-stu-id="938d3-138">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="938d3-139">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="938d3-139">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="938d3-140">int</span><span class="sxs-lookup"><span data-stu-id="938d3-140">int</span></span>            |
| <span data-ttu-id="938d3-141">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="938d3-141">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="938d3-142">int2</span><span class="sxs-lookup"><span data-stu-id="938d3-142">int2</span></span>           |
| <span data-ttu-id="938d3-143">Texture3D</span><span class="sxs-lookup"><span data-stu-id="938d3-143">Texture3D</span></span>                     | <span data-ttu-id="938d3-144">int3</span><span class="sxs-lookup"><span data-stu-id="938d3-144">int3</span></span>           |
| <span data-ttu-id="938d3-145">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="938d3-145">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="938d3-146">no admitido</span><span class="sxs-lookup"><span data-stu-id="938d3-146">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="938d3-147">*Estado* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="938d3-147">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="938d3-148">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="938d3-148">Type: **uint**</span></span>

<span data-ttu-id="938d3-149">Estado de la operación.</span><span class="sxs-lookup"><span data-stu-id="938d3-149">The status of the operation.</span></span> <span data-ttu-id="938d3-150">No se puede tener acceso directamente al estado. en su lugar, pase el estado a la función intrínseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="938d3-150">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="938d3-151">**CheckAccessFullyMapped** devuelve **true** si todos los valores de la operación de **ejemplo**, **recopilación** o **carga** correspondiente han tenido acceso a los mosaicos asignados en un [recurso en mosaico](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="938d3-151">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="938d3-152">Si se tomó algún valor de un mosaico sin asignar, **CheckAccessFullyMapped** devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="938d3-152">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="938d3-153">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="938d3-153">Return value</span></span>

<span data-ttu-id="938d3-154">Tipo: **[ **\_ formato de DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="938d3-154">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="938d3-155">Formato de textura, que es uno de los valores con tipo que aparecen [**en \_ formato de DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="938d3-155">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="938d3-156">Vea también</span><span class="sxs-lookup"><span data-stu-id="938d3-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="938d3-157">Métodos SampleCmpLevelZero</span><span class="sxs-lookup"><span data-stu-id="938d3-157">SampleCmpLevelZero methods</span></span>](texture1d-samplecmplevelzero.md)
</dt> </dl>

 

 
