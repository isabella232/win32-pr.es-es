---
title: 'Función SampleCmpLevelZero:: SampleCmpLevelZero (S, Float, Float, int, uint) para Texture1DArray'
description: Obtenga información sobre cómo esta función muestrea una textura en el nivel 0 del mipmap solo y compara el resultado con un valor de comparación. Para Texture1DArray.
ms.assetid: DBC06FEF-DA64-4210-A47C-81EB0F1F9D5A
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
ms.openlocfilehash: 854dc20d732813623ba637ce53029d8098c90908
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/16/2021
ms.locfileid: "104998809"
---
# <a name="samplecmplevelzerosamplecmplevelzerosfloatfloatintuint-function-for-texture1darray"></a><span data-ttu-id="1630c-105">Función SampleCmpLevelZero:: SampleCmpLevelZero (S, Float, Float, int, uint) para Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="1630c-105">SampleCmpLevelZero::SampleCmpLevelZero(S,float,float,int,uint) function for Texture1DArray</span></span>

<span data-ttu-id="1630c-106">Muestrea solo una textura en el nivel 0 del mipmap y compara el resultado con un valor de comparación.</span><span class="sxs-lookup"><span data-stu-id="1630c-106">Samples a texture on mipmap level 0 only and compares the result to a comparison value.</span></span> <span data-ttu-id="1630c-107">Devuelve el estado de la operación.</span><span class="sxs-lookup"><span data-stu-id="1630c-107">Returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="1630c-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1630c-108">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleCmpLevelZero(
  in  SamplerState S,
  in  float        Location,
  in  float        CompareValue,
  in  int          Offset,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="1630c-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1630c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1630c-110">*S* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="1630c-110">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1630c-111">Tipo: **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="1630c-111">Type: **SamplerState**</span></span>

<span data-ttu-id="1630c-112">Un [Estado de muestra](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="1630c-112">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="1630c-113">Se trata de un objeto declarado en un archivo de efectos que contiene las asignaciones de estado.</span><span class="sxs-lookup"><span data-stu-id="1630c-113">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="1630c-114">*Ubicación* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="1630c-114">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1630c-115">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="1630c-115">Type: **float**</span></span>

<span data-ttu-id="1630c-116">Las coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="1630c-116">The texture coordinates.</span></span> <span data-ttu-id="1630c-117">El tipo de argumento depende del tipo de objeto de textura.</span><span class="sxs-lookup"><span data-stu-id="1630c-117">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="1630c-118">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="1630c-118">Texture-Object Type</span></span>                    | <span data-ttu-id="1630c-119">Tipo de parámetro</span><span class="sxs-lookup"><span data-stu-id="1630c-119">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="1630c-120">Texture1D</span><span class="sxs-lookup"><span data-stu-id="1630c-120">Texture1D</span></span>                              | <span data-ttu-id="1630c-121">FLOAT</span><span class="sxs-lookup"><span data-stu-id="1630c-121">float</span></span>          |
| <span data-ttu-id="1630c-122">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="1630c-122">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="1630c-123">float2</span><span class="sxs-lookup"><span data-stu-id="1630c-123">float2</span></span>         |
| <span data-ttu-id="1630c-124">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="1630c-124">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="1630c-125">float3</span><span class="sxs-lookup"><span data-stu-id="1630c-125">float3</span></span>         |
| <span data-ttu-id="1630c-126">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="1630c-126">TextureCubeArray</span></span>                       | <span data-ttu-id="1630c-127">float4</span><span class="sxs-lookup"><span data-stu-id="1630c-127">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="1630c-128">*CompareValue* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1630c-128">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1630c-129">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="1630c-129">Type: **float**</span></span>

<span data-ttu-id="1630c-130">Un valor de punto flotante que se va a utilizar como valor de comparación.</span><span class="sxs-lookup"><span data-stu-id="1630c-130">A floating-point value to use as a comparison value.</span></span>

</dd> <dt>

<span data-ttu-id="1630c-131">*Desplazamiento* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1630c-131">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1630c-132">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="1630c-132">Type: **int**</span></span>

<span data-ttu-id="1630c-133">Desplazamiento de coordenadas de textura opcional, que se puede usar para cualquier tipo de objeto de textura. el desplazamiento se aplica a la ubicación antes del muestreo.</span><span class="sxs-lookup"><span data-stu-id="1630c-133">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="1630c-134">Use un desplazamiento solo en un entero miplevel; de lo contrario, puede obtener resultados que no se traduzcan bien al hardware.</span><span class="sxs-lookup"><span data-stu-id="1630c-134">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="1630c-135">El tipo de argumento depende del tipo de objeto de textura.</span><span class="sxs-lookup"><span data-stu-id="1630c-135">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="1630c-136">Para obtener más información, vea [aplicar desplazamientos enteros](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="1630c-136">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="1630c-137">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="1630c-137">Texture-Object Type</span></span>           | <span data-ttu-id="1630c-138">Tipo de parámetro</span><span class="sxs-lookup"><span data-stu-id="1630c-138">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="1630c-139">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="1630c-139">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="1630c-140">int</span><span class="sxs-lookup"><span data-stu-id="1630c-140">int</span></span>            |
| <span data-ttu-id="1630c-141">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="1630c-141">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="1630c-142">int2</span><span class="sxs-lookup"><span data-stu-id="1630c-142">int2</span></span>           |
| <span data-ttu-id="1630c-143">Texture3D</span><span class="sxs-lookup"><span data-stu-id="1630c-143">Texture3D</span></span>                     | <span data-ttu-id="1630c-144">int3</span><span class="sxs-lookup"><span data-stu-id="1630c-144">int3</span></span>           |
| <span data-ttu-id="1630c-145">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="1630c-145">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="1630c-146">no admitido</span><span class="sxs-lookup"><span data-stu-id="1630c-146">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="1630c-147">*Estado* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="1630c-147">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1630c-148">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="1630c-148">Type: **uint**</span></span>

<span data-ttu-id="1630c-149">Estado de la operación.</span><span class="sxs-lookup"><span data-stu-id="1630c-149">The status of the operation.</span></span> <span data-ttu-id="1630c-150">No se puede tener acceso directamente al estado. en su lugar, pase el estado a la función intrínseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="1630c-150">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="1630c-151">**CheckAccessFullyMapped** devuelve **true** si todos los valores de la operación de **ejemplo**, **recopilación** o **carga** correspondiente han tenido acceso a los mosaicos asignados en un [recurso en mosaico](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="1630c-151">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="1630c-152">Si se tomó algún valor de un mosaico sin asignar, **CheckAccessFullyMapped** devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="1630c-152">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1630c-153">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1630c-153">Return value</span></span>

<span data-ttu-id="1630c-154">Tipo: **[ **\_ formato de DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="1630c-154">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="1630c-155">Formato de textura, que es uno de los valores con tipo que aparecen [**en \_ formato de DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="1630c-155">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="1630c-156">Vea también</span><span class="sxs-lookup"><span data-stu-id="1630c-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1630c-157">Métodos SampleCmpLevelZero</span><span class="sxs-lookup"><span data-stu-id="1630c-157">SampleCmpLevelZero methods</span></span>](texture1darray-samplecmplevelzero.md)
</dt> </dl>

 

 
