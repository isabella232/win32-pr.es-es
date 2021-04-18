---
title: 'Texture2DArray:: sample (S, Float, int, Float, uint) (función)'
description: 'Muestrea una textura con un valor opcional para Clamp valores de nivel de detalle (LOD) de ejemplo en y devuelve el estado de la operación. | Texture2DArray:: sample (S, Float, int, Float, uint) (función)'
ms.assetid: 0F9DBC0D-F35D-4A7A-B8F5-1EFBF7E14615
keywords:
- HLSL de la función de ejemplo
topic_type:
- apiref
api_name:
- Sample
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e2027377a1659aa46fcf10e39f39b21e2243c943
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986258"
---
# <a name="texture2darraysamplesfloatintfloatuint-function"></a><span data-ttu-id="a30cb-105">Texture2DArray:: sample (S, Float, int, Float, uint) (función)</span><span class="sxs-lookup"><span data-stu-id="a30cb-105">Texture2DArray::Sample(S,float,int,float,uint) function</span></span>

<span data-ttu-id="a30cb-106">Muestrea una textura con un valor opcional para Clamp valores de nivel de detalle (LOD) de ejemplo en y devuelve el estado de la operación.</span><span class="sxs-lookup"><span data-stu-id="a30cb-106">Samples a texture with an optional value to clamp sample level-of-detail (LOD) values to, and returns status of the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="a30cb-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a30cb-107">Syntax</span></span>


``` syntax
DXGI_FORMAT Sample(
  in  SamplerState S,
  in  float        Location,
  in  int          Offset,
  in  float        Clamp,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="a30cb-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a30cb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a30cb-109">*S* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="a30cb-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a30cb-110">Un [Estado de muestra](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="a30cb-110">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="a30cb-111">Se trata de un objeto declarado en un archivo de efectos que contiene las asignaciones de estado.</span><span class="sxs-lookup"><span data-stu-id="a30cb-111">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="a30cb-112">*Ubicación* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="a30cb-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a30cb-113">Las coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="a30cb-113">The texture coordinates.</span></span> <span data-ttu-id="a30cb-114">El tipo de argumento depende del tipo de objeto de textura.</span><span class="sxs-lookup"><span data-stu-id="a30cb-114">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="a30cb-115">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="a30cb-115">Texture-Object Type</span></span>                    | <span data-ttu-id="a30cb-116">Tipo de parámetro</span><span class="sxs-lookup"><span data-stu-id="a30cb-116">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="a30cb-117">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a30cb-117">Texture1D</span></span>                              | <span data-ttu-id="a30cb-118">FLOAT</span><span class="sxs-lookup"><span data-stu-id="a30cb-118">float</span></span>          |
| <span data-ttu-id="a30cb-119">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="a30cb-119">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="a30cb-120">float2</span><span class="sxs-lookup"><span data-stu-id="a30cb-120">float2</span></span>         |
| <span data-ttu-id="a30cb-121">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="a30cb-121">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="a30cb-122">float3</span><span class="sxs-lookup"><span data-stu-id="a30cb-122">float3</span></span>         |
| <span data-ttu-id="a30cb-123">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="a30cb-123">TextureCubeArray</span></span>                       | <span data-ttu-id="a30cb-124">float4</span><span class="sxs-lookup"><span data-stu-id="a30cb-124">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="a30cb-125">*Desplazamiento* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a30cb-125">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a30cb-126">Desplazamiento de coordenadas de textura opcional, que se puede usar para cualquier tipo de objeto de textura. el desplazamiento se aplica a la ubicación antes del muestreo.</span><span class="sxs-lookup"><span data-stu-id="a30cb-126">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="a30cb-127">Use un desplazamiento solo en un entero miplevel; de lo contrario, puede obtener resultados que no se traduzcan bien al hardware.</span><span class="sxs-lookup"><span data-stu-id="a30cb-127">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="a30cb-128">El tipo de argumento depende del tipo de objeto de textura.</span><span class="sxs-lookup"><span data-stu-id="a30cb-128">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="a30cb-129">Para obtener más información, vea [aplicar desplazamientos enteros](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="a30cb-129">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="a30cb-130">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="a30cb-130">Texture-Object Type</span></span>           | <span data-ttu-id="a30cb-131">Tipo de parámetro</span><span class="sxs-lookup"><span data-stu-id="a30cb-131">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="a30cb-132">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="a30cb-132">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="a30cb-133">int</span><span class="sxs-lookup"><span data-stu-id="a30cb-133">int</span></span>            |
| <span data-ttu-id="a30cb-134">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="a30cb-134">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="a30cb-135">int2</span><span class="sxs-lookup"><span data-stu-id="a30cb-135">int2</span></span>           |
| <span data-ttu-id="a30cb-136">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a30cb-136">Texture3D</span></span>                     | <span data-ttu-id="a30cb-137">int3</span><span class="sxs-lookup"><span data-stu-id="a30cb-137">int3</span></span>           |
| <span data-ttu-id="a30cb-138">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="a30cb-138">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="a30cb-139">no admitido</span><span class="sxs-lookup"><span data-stu-id="a30cb-139">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="a30cb-140">*Abrazadera* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a30cb-140">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a30cb-141">Un valor opcional en el que se van a fijar los valores LOD de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="a30cb-141">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="a30cb-142">Por ejemplo, si se pasa 2.0 f para el valor Clamp, se asegura de que ningún ejemplo individual tenga acceso a un nivel de MIP inferior a 2.0 f.</span><span class="sxs-lookup"><span data-stu-id="a30cb-142">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> <dt>

<span data-ttu-id="a30cb-143">*Estado* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="a30cb-143">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a30cb-144">Estado de la operación.</span><span class="sxs-lookup"><span data-stu-id="a30cb-144">The status of the operation.</span></span> <span data-ttu-id="a30cb-145">No se puede tener acceso directamente al estado. en su lugar, pase el estado a la función intrínseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="a30cb-145">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="a30cb-146">**CheckAccessFullyMapped** devuelve **true** si todos los valores de la operación de **ejemplo**, **recopilación** o **carga** correspondiente han tenido acceso a los mosaicos asignados en un [recurso en mosaico](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="a30cb-146">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="a30cb-147">Si se tomó algún valor de un mosaico sin asignar, **CheckAccessFullyMapped** devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="a30cb-147">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a30cb-148">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a30cb-148">Return value</span></span>

<span data-ttu-id="a30cb-149">Formato de textura, que es uno de los valores con tipo que aparecen [**en \_ formato de DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="a30cb-149">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="a30cb-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="a30cb-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a30cb-151">Métodos de ejemplo</span><span class="sxs-lookup"><span data-stu-id="a30cb-151">Sample methods</span></span>](texture2darray-sample.md)
</dt> </dl>

 

 
