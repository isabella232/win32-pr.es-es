---
title: 'Función SampleLevel:: SampleLevel (S, Float, Float, int, uint) para Texture1DArray'
description: 'Muestrea una textura en el nivel de mipmap especificado y devuelve el estado de la operación. Para Texture1DArray. | SampleLevel:: SampleLevel (S, Float, Float, int, uint) (función)'
ms.assetid: 6BF31C44-B933-481E-9FB2-D606E3F91036
keywords:
- SampleLevel de función HLSL
topic_type:
- apiref
api_name:
- SampleLevel
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6ee1248ee72044e6a7d8a688753f0a61c7fb4e60
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/16/2021
ms.locfileid: "104362834"
---
# <a name="samplelevelsamplelevelsfloatfloatintuint-function-for-texture1darray"></a><span data-ttu-id="71808-106">Función SampleLevel:: SampleLevel (S, Float, Float, int, uint) para Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="71808-106">SampleLevel::SampleLevel(S,float,float,int,uint) function for Texture1DArray</span></span>

<span data-ttu-id="71808-107">Muestrea una textura en el nivel de mipmap especificado y devuelve el estado de la operación.</span><span class="sxs-lookup"><span data-stu-id="71808-107">Samples a texture on the specified mipmap level and returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="71808-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="71808-108">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleLevel(
  in  SamplerState S,
  in  float        Location,
  in  float        LOD,
  in  int          Offset,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="71808-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="71808-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71808-110">*S* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="71808-110">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71808-111">Tipo: **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="71808-111">Type: **SamplerState**</span></span>

<span data-ttu-id="71808-112">Un [Estado de muestra](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="71808-112">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="71808-113">Se trata de un objeto declarado en un archivo de efectos que contiene las asignaciones de estado.</span><span class="sxs-lookup"><span data-stu-id="71808-113">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="71808-114">*Ubicación* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="71808-114">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71808-115">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="71808-115">Type: **float**</span></span>

<span data-ttu-id="71808-116">Las coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="71808-116">The texture coordinates.</span></span> <span data-ttu-id="71808-117">El tipo de argumento depende del tipo de objeto de textura.</span><span class="sxs-lookup"><span data-stu-id="71808-117">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="71808-118">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="71808-118">Texture-Object Type</span></span>                    | <span data-ttu-id="71808-119">Tipo de parámetro</span><span class="sxs-lookup"><span data-stu-id="71808-119">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="71808-120">Texture1D</span><span class="sxs-lookup"><span data-stu-id="71808-120">Texture1D</span></span>                              | <span data-ttu-id="71808-121">FLOAT</span><span class="sxs-lookup"><span data-stu-id="71808-121">float</span></span>          |
| <span data-ttu-id="71808-122">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="71808-122">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="71808-123">float2</span><span class="sxs-lookup"><span data-stu-id="71808-123">float2</span></span>         |
| <span data-ttu-id="71808-124">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="71808-124">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="71808-125">float3</span><span class="sxs-lookup"><span data-stu-id="71808-125">float3</span></span>         |
| <span data-ttu-id="71808-126">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="71808-126">TextureCubeArray</span></span>                       | <span data-ttu-id="71808-127">float4</span><span class="sxs-lookup"><span data-stu-id="71808-127">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="71808-128">*LOD* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="71808-128">*LOD* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71808-129">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="71808-129">Type: **float**</span></span>

<span data-ttu-id="71808-130">\[en \] un número que especifica el nivel de mipmap.</span><span class="sxs-lookup"><span data-stu-id="71808-130">\[in\] A number that specifies the mipmap level.</span></span> <span data-ttu-id="71808-131">Si el valor es ≤ 0, se utiliza el nivel de mipmap 0 (mapa más grande).</span><span class="sxs-lookup"><span data-stu-id="71808-131">If the value is ≤ 0, mipmap level 0 (biggest map) is used.</span></span> <span data-ttu-id="71808-132">El valor fraccionario (si se proporciona) se usa para interpolar entre dos niveles de mipmap.</span><span class="sxs-lookup"><span data-stu-id="71808-132">The fractional value (if supplied) is used to interpolate between two mipmap levels.</span></span>

</dd> <dt>

<span data-ttu-id="71808-133">*Desplazamiento* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="71808-133">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71808-134">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="71808-134">Type: **int**</span></span>

<span data-ttu-id="71808-135">Desplazamiento de coordenadas de textura opcional, que se puede usar para cualquier tipo de objeto de textura. el desplazamiento se aplica a la ubicación antes del muestreo.</span><span class="sxs-lookup"><span data-stu-id="71808-135">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="71808-136">Use un desplazamiento solo en un entero miplevel; de lo contrario, puede obtener resultados que no se traduzcan bien al hardware.</span><span class="sxs-lookup"><span data-stu-id="71808-136">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="71808-137">El tipo de argumento depende del tipo de objeto de textura.</span><span class="sxs-lookup"><span data-stu-id="71808-137">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="71808-138">Para obtener más información, vea [aplicar desplazamientos enteros](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="71808-138">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="71808-139">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="71808-139">Texture-Object Type</span></span>           | <span data-ttu-id="71808-140">Tipo de parámetro</span><span class="sxs-lookup"><span data-stu-id="71808-140">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="71808-141">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="71808-141">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="71808-142">int</span><span class="sxs-lookup"><span data-stu-id="71808-142">int</span></span>            |
| <span data-ttu-id="71808-143">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="71808-143">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="71808-144">int2</span><span class="sxs-lookup"><span data-stu-id="71808-144">int2</span></span>           |
| <span data-ttu-id="71808-145">Texture3D</span><span class="sxs-lookup"><span data-stu-id="71808-145">Texture3D</span></span>                     | <span data-ttu-id="71808-146">int3</span><span class="sxs-lookup"><span data-stu-id="71808-146">int3</span></span>           |
| <span data-ttu-id="71808-147">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="71808-147">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="71808-148">no admitido</span><span class="sxs-lookup"><span data-stu-id="71808-148">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="71808-149">*Estado* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="71808-149">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="71808-150">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="71808-150">Type: **uint**</span></span>

<span data-ttu-id="71808-151">Estado de la operación.</span><span class="sxs-lookup"><span data-stu-id="71808-151">The status of the operation.</span></span> <span data-ttu-id="71808-152">No se puede tener acceso directamente al estado. en su lugar, pase el estado a la función intrínseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="71808-152">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="71808-153">**CheckAccessFullyMapped** devuelve **true** si todos los valores de la operación de **ejemplo**, **recopilación** o **carga** correspondiente han tenido acceso a los mosaicos asignados en un [recurso en mosaico](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="71808-153">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="71808-154">Si se tomó algún valor de un mosaico sin asignar, **CheckAccessFullyMapped** devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="71808-154">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71808-155">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="71808-155">Return value</span></span>

<span data-ttu-id="71808-156">Tipo: **[ **\_ formato de DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="71808-156">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="71808-157">Formato de textura, que es uno de los valores con tipo que aparecen [**en \_ formato de DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="71808-157">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="71808-158">Vea también</span><span class="sxs-lookup"><span data-stu-id="71808-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71808-159">Métodos SampleLevel</span><span class="sxs-lookup"><span data-stu-id="71808-159">SampleLevel methods</span></span>](texture1darray-samplelevel.md)
</dt> </dl>

 

 
