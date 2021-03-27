---
title: 'Función SampleCmp:: SampleCmp (S, Float, Float, int, Float, uint) para Texture2DArray'
description: Esta función muestrea una textura con un valor de comparación para rechazar muestras, con un valor opcional para Clamp valores de nivel de detalle (LOD) de ejemplo en. Para Texture2DArray.
ms.assetid: 847A6B79-3A66-4209-AB01-7C1FDA8A433A
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
ms.openlocfilehash: cc8957ca2f6c1eb3e4a665b5d6df134c854ccc3c
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/16/2021
ms.locfileid: "104280541"
---
# <a name="samplecmpsamplecmpsfloatfloatintfloatuint-function-for-texture2darray"></a><span data-ttu-id="8a487-105">Función SampleCmp:: SampleCmp (S, Float, Float, int, Float, uint) para Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="8a487-105">SampleCmp::SampleCmp(S,float,float,int,float,uint) function for Texture2DArray</span></span>

<span data-ttu-id="8a487-106">Muestrea una textura, utilizando un valor de comparación para rechazar muestras, con un valor opcional para Clamp valores de nivel de detalle (LOD) de ejemplo en.</span><span class="sxs-lookup"><span data-stu-id="8a487-106">Samples a texture, using a comparison value to reject samples, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span> <span data-ttu-id="8a487-107">Devuelve el estado de la operación.</span><span class="sxs-lookup"><span data-stu-id="8a487-107">Returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a487-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8a487-108">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleCmp(
  in  SamplerState S,
  in  float        Location,
  in  float        CompareValue,
  in  int          Offset,
  in  float        Clamp,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="8a487-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8a487-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a487-110">*S* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="8a487-110">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a487-111">Tipo: **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="8a487-111">Type: **SamplerState**</span></span>

<span data-ttu-id="8a487-112">Un [Estado de muestra](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="8a487-112">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="8a487-113">Se trata de un objeto declarado en un archivo de efectos que contiene las asignaciones de estado.</span><span class="sxs-lookup"><span data-stu-id="8a487-113">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="8a487-114">*Ubicación* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="8a487-114">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a487-115">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="8a487-115">Type: **float**</span></span>

<span data-ttu-id="8a487-116">Las coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="8a487-116">The texture coordinates.</span></span> <span data-ttu-id="8a487-117">El tipo de argumento depende del tipo de objeto de textura.</span><span class="sxs-lookup"><span data-stu-id="8a487-117">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="8a487-118">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="8a487-118">Texture-Object Type</span></span>                    | <span data-ttu-id="8a487-119">Tipo de parámetro</span><span class="sxs-lookup"><span data-stu-id="8a487-119">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="8a487-120">Texture1D</span><span class="sxs-lookup"><span data-stu-id="8a487-120">Texture1D</span></span>                              | <span data-ttu-id="8a487-121">FLOAT</span><span class="sxs-lookup"><span data-stu-id="8a487-121">float</span></span>          |
| <span data-ttu-id="8a487-122">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="8a487-122">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="8a487-123">float2</span><span class="sxs-lookup"><span data-stu-id="8a487-123">float2</span></span>         |
| <span data-ttu-id="8a487-124">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="8a487-124">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="8a487-125">float3</span><span class="sxs-lookup"><span data-stu-id="8a487-125">float3</span></span>         |
| <span data-ttu-id="8a487-126">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="8a487-126">TextureCubeArray</span></span>                       | <span data-ttu-id="8a487-127">float4</span><span class="sxs-lookup"><span data-stu-id="8a487-127">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="8a487-128">*CompareValue* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8a487-128">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a487-129">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="8a487-129">Type: **float**</span></span>

<span data-ttu-id="8a487-130">Un valor de punto flotante que se va a utilizar como valor de comparación.</span><span class="sxs-lookup"><span data-stu-id="8a487-130">A floating-point value to use as a comparison value.</span></span>

</dd> <dt>

<span data-ttu-id="8a487-131">*Desplazamiento* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8a487-131">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a487-132">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="8a487-132">Type: **int**</span></span>

<span data-ttu-id="8a487-133">Desplazamiento de coordenadas de textura opcional, que se puede usar para cualquier tipo de objeto de textura. el desplazamiento se aplica a la ubicación antes del muestreo.</span><span class="sxs-lookup"><span data-stu-id="8a487-133">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="8a487-134">Use un desplazamiento solo en un entero miplevel; de lo contrario, puede obtener resultados que no se traduzcan bien al hardware.</span><span class="sxs-lookup"><span data-stu-id="8a487-134">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="8a487-135">El tipo de argumento depende del tipo de objeto de textura.</span><span class="sxs-lookup"><span data-stu-id="8a487-135">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="8a487-136">Para obtener más información, vea [aplicar desplazamientos enteros](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="8a487-136">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="8a487-137">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="8a487-137">Texture-Object Type</span></span>           | <span data-ttu-id="8a487-138">Tipo de parámetro</span><span class="sxs-lookup"><span data-stu-id="8a487-138">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="8a487-139">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="8a487-139">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="8a487-140">int</span><span class="sxs-lookup"><span data-stu-id="8a487-140">int</span></span>            |
| <span data-ttu-id="8a487-141">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="8a487-141">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="8a487-142">int2</span><span class="sxs-lookup"><span data-stu-id="8a487-142">int2</span></span>           |
| <span data-ttu-id="8a487-143">Texture3D</span><span class="sxs-lookup"><span data-stu-id="8a487-143">Texture3D</span></span>                     | <span data-ttu-id="8a487-144">int3</span><span class="sxs-lookup"><span data-stu-id="8a487-144">int3</span></span>           |
| <span data-ttu-id="8a487-145">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="8a487-145">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="8a487-146">no admitido</span><span class="sxs-lookup"><span data-stu-id="8a487-146">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="8a487-147">*Abrazadera* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8a487-147">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a487-148">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="8a487-148">Type: **float**</span></span>

<span data-ttu-id="8a487-149">Un valor opcional en el que se van a fijar los valores LOD de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="8a487-149">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="8a487-150">Por ejemplo, si se pasa 2.0 f para el valor Clamp, se asegura de que ningún ejemplo individual tenga acceso a un nivel de MIP inferior a 2.0 f.</span><span class="sxs-lookup"><span data-stu-id="8a487-150">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> <dt>

<span data-ttu-id="8a487-151">*Estado* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="8a487-151">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8a487-152">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="8a487-152">Type: **uint**</span></span>

<span data-ttu-id="8a487-153">Estado de la operación.</span><span class="sxs-lookup"><span data-stu-id="8a487-153">The status of the operation.</span></span> <span data-ttu-id="8a487-154">No se puede tener acceso directamente al estado. en su lugar, pase el estado a la función intrínseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="8a487-154">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="8a487-155">**CheckAccessFullyMapped** devuelve **true** si todos los valores de la operación de **ejemplo**, **recopilación** o **carga** correspondiente han tenido acceso a los mosaicos asignados en un [recurso en mosaico](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="8a487-155">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="8a487-156">Si se tomó algún valor de un mosaico sin asignar, **CheckAccessFullyMapped** devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="8a487-156">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a487-157">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8a487-157">Return value</span></span>

<span data-ttu-id="8a487-158">Tipo: **[ **\_ formato de DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="8a487-158">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="8a487-159">Formato de textura, que es uno de los valores con tipo que aparecen [**en \_ formato de DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="8a487-159">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="8a487-160">Vea también</span><span class="sxs-lookup"><span data-stu-id="8a487-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a487-161">Métodos SampleCmp</span><span class="sxs-lookup"><span data-stu-id="8a487-161">SampleCmp methods</span></span>](texture2darray-samplecmp.md)
</dt> <dt>

[<span data-ttu-id="8a487-162">**Texture2DArray**</span><span class="sxs-lookup"><span data-stu-id="8a487-162">**Texture2DArray**</span></span>](sm5-object-texture2darray.md)
</dt> </dl>

 

 
