---
title: 'Función SampleLevel:: SampleLevel (S, Float, Float, int, uint) para Texture2D'
description: Muestrea un Texture2D en el nivel de mipmap especificado y devuelve el estado de la operación.
ms.assetid: B021D42E-9F63-4CCE-939B-F93D91F7CB80
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
ms.openlocfilehash: 1455454649e24bd984948a81837181a7bcdba11a
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/16/2021
ms.locfileid: "104998845"
---
# <a name="samplelevelsamplelevelsfloatfloatintuint-function-for-texture2d"></a><span data-ttu-id="d97be-104">Función SampleLevel:: SampleLevel (S, Float, Float, int, uint) para Texture2D</span><span class="sxs-lookup"><span data-stu-id="d97be-104">SampleLevel::SampleLevel(S,float,float,int,uint) function for Texture2D</span></span>

<span data-ttu-id="d97be-105">Muestrea un [**Texture2D**](sm5-object-texture2d.md) en el nivel de mipmap especificado y devuelve el estado de la operación.</span><span class="sxs-lookup"><span data-stu-id="d97be-105">Samples a [**Texture2D**](sm5-object-texture2d.md) on the specified mipmap level and returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="d97be-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d97be-106">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleLevel(
  in  SamplerState S,
  in  float        Location,
  in  float        LOD,
  in  int          Offset,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="d97be-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d97be-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d97be-108">*S* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="d97be-108">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d97be-109">Tipo: **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="d97be-109">Type: **SamplerState**</span></span>

<span data-ttu-id="d97be-110">Un [Estado de muestra](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="d97be-110">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="d97be-111">Se trata de un objeto declarado en un archivo de efectos que contiene las asignaciones de estado.</span><span class="sxs-lookup"><span data-stu-id="d97be-111">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="d97be-112">*Ubicación* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="d97be-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d97be-113">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="d97be-113">Type: **float**</span></span>

<span data-ttu-id="d97be-114">Las coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="d97be-114">The texture coordinates.</span></span> <span data-ttu-id="d97be-115">El tipo de argumento depende del tipo de objeto de textura.</span><span class="sxs-lookup"><span data-stu-id="d97be-115">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="d97be-116">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="d97be-116">Texture-Object Type</span></span>                    | <span data-ttu-id="d97be-117">Tipo de parámetro</span><span class="sxs-lookup"><span data-stu-id="d97be-117">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="d97be-118">Texture1D</span><span class="sxs-lookup"><span data-stu-id="d97be-118">Texture1D</span></span>                              | <span data-ttu-id="d97be-119">FLOAT</span><span class="sxs-lookup"><span data-stu-id="d97be-119">float</span></span>          |
| <span data-ttu-id="d97be-120">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="d97be-120">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="d97be-121">float2</span><span class="sxs-lookup"><span data-stu-id="d97be-121">float2</span></span>         |
| <span data-ttu-id="d97be-122">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="d97be-122">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="d97be-123">float3</span><span class="sxs-lookup"><span data-stu-id="d97be-123">float3</span></span>         |
| <span data-ttu-id="d97be-124">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="d97be-124">TextureCubeArray</span></span>                       | <span data-ttu-id="d97be-125">float4</span><span class="sxs-lookup"><span data-stu-id="d97be-125">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="d97be-126">*LOD* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d97be-126">*LOD* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d97be-127">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="d97be-127">Type: **float**</span></span>

<span data-ttu-id="d97be-128">\[en \] un número que especifica el nivel de mipmap.</span><span class="sxs-lookup"><span data-stu-id="d97be-128">\[in\] A number that specifies the mipmap level.</span></span> <span data-ttu-id="d97be-129">Si el valor es ≤ 0, se utiliza el nivel de mipmap 0 (mapa más grande).</span><span class="sxs-lookup"><span data-stu-id="d97be-129">If the value is ≤ 0, mipmap level 0 (biggest map) is used.</span></span> <span data-ttu-id="d97be-130">El valor fraccionario (si se proporciona) se usa para interpolar entre dos niveles de mipmap.</span><span class="sxs-lookup"><span data-stu-id="d97be-130">The fractional value (if supplied) is used to interpolate between two mipmap levels.</span></span>

</dd> <dt>

<span data-ttu-id="d97be-131">*Desplazamiento* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d97be-131">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d97be-132">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="d97be-132">Type: **int**</span></span>

<span data-ttu-id="d97be-133">Desplazamiento de coordenadas de textura opcional, que se puede usar para cualquier tipo de objeto de textura. el desplazamiento se aplica a la ubicación antes del muestreo.</span><span class="sxs-lookup"><span data-stu-id="d97be-133">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="d97be-134">Use un desplazamiento solo en un entero miplevel; de lo contrario, puede obtener resultados que no se traduzcan bien al hardware.</span><span class="sxs-lookup"><span data-stu-id="d97be-134">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="d97be-135">El tipo de argumento depende del tipo de objeto de textura.</span><span class="sxs-lookup"><span data-stu-id="d97be-135">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="d97be-136">Para obtener más información, vea [aplicar desplazamientos enteros](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="d97be-136">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="d97be-137">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="d97be-137">Texture-Object Type</span></span>           | <span data-ttu-id="d97be-138">Tipo de parámetro</span><span class="sxs-lookup"><span data-stu-id="d97be-138">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="d97be-139">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="d97be-139">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="d97be-140">int</span><span class="sxs-lookup"><span data-stu-id="d97be-140">int</span></span>            |
| <span data-ttu-id="d97be-141">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="d97be-141">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="d97be-142">int2</span><span class="sxs-lookup"><span data-stu-id="d97be-142">int2</span></span>           |
| <span data-ttu-id="d97be-143">Texture3D</span><span class="sxs-lookup"><span data-stu-id="d97be-143">Texture3D</span></span>                     | <span data-ttu-id="d97be-144">int3</span><span class="sxs-lookup"><span data-stu-id="d97be-144">int3</span></span>           |
| <span data-ttu-id="d97be-145">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="d97be-145">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="d97be-146">no admitido</span><span class="sxs-lookup"><span data-stu-id="d97be-146">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="d97be-147">*Estado* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="d97be-147">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d97be-148">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="d97be-148">Type: **uint**</span></span>

<span data-ttu-id="d97be-149">Estado de la operación.</span><span class="sxs-lookup"><span data-stu-id="d97be-149">The status of the operation.</span></span> <span data-ttu-id="d97be-150">No se puede tener acceso directamente al estado. en su lugar, pase el estado a la función intrínseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="d97be-150">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="d97be-151">**CheckAccessFullyMapped** devuelve **true** si todos los valores de la operación de **ejemplo**, **recopilación** o **carga** correspondiente han tenido acceso a los mosaicos asignados en un [recurso en mosaico](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="d97be-151">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="d97be-152">Si se tomó algún valor de un mosaico sin asignar, **CheckAccessFullyMapped** devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="d97be-152">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d97be-153">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d97be-153">Return value</span></span>

<span data-ttu-id="d97be-154">Tipo: **[ **\_ formato de DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="d97be-154">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="d97be-155">Formato de textura, que es uno de los valores con tipo que aparecen [**en \_ formato de DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="d97be-155">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="d97be-156">Vea también</span><span class="sxs-lookup"><span data-stu-id="d97be-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d97be-157">Métodos SampleLevel</span><span class="sxs-lookup"><span data-stu-id="d97be-157">SampleLevel methods</span></span>](texture2d-samplelevel.md)
</dt> </dl>

 

 
