---
title: 'Texture3D:: sample (S, Float, int, Float, uint) (función)'
description: 'Muestrea una textura con un valor opcional para Clamp valores de nivel de detalle (LOD) de ejemplo en y devuelve el estado de la operación. | Texture3D:: sample (S, Float, int, Float, uint) (función)'
ms.assetid: DB8401A1-1065-4616-BDDE-9ADB59B09C8B
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
ms.openlocfilehash: 1f1704a30ba689d50bc9c551ac6a43a4a38f90a9
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104998037"
---
# <a name="texture3dsamplesfloatintfloatuint-function"></a><span data-ttu-id="ccd5d-105">Texture3D:: sample (S, Float, int, Float, uint) (función)</span><span class="sxs-lookup"><span data-stu-id="ccd5d-105">Texture3D::Sample(S,float,int,float,uint) function</span></span>

<span data-ttu-id="ccd5d-106">Muestrea una textura con un valor opcional para Clamp valores de nivel de detalle (LOD) de ejemplo en y devuelve el estado de la operación.</span><span class="sxs-lookup"><span data-stu-id="ccd5d-106">Samples a texture with an optional value to clamp sample level-of-detail (LOD) values to, and returns status of the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="ccd5d-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ccd5d-107">Syntax</span></span>


``` syntax
DXGI_FORMAT Sample(
  in  SamplerState S,
  in  float        Location,
  in  int          Offset,
  in  float        Clamp,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="ccd5d-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ccd5d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ccd5d-109">*S* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="ccd5d-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ccd5d-110">Un [Estado de muestra](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="ccd5d-110">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="ccd5d-111">Se trata de un objeto declarado en un archivo de efectos que contiene las asignaciones de estado.</span><span class="sxs-lookup"><span data-stu-id="ccd5d-111">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="ccd5d-112">*Ubicación* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="ccd5d-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ccd5d-113">Las coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="ccd5d-113">The texture coordinates.</span></span> <span data-ttu-id="ccd5d-114">El tipo de argumento depende del tipo de objeto de textura.</span><span class="sxs-lookup"><span data-stu-id="ccd5d-114">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="ccd5d-115">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="ccd5d-115">Texture-Object Type</span></span>                    | <span data-ttu-id="ccd5d-116">Tipo de parámetro</span><span class="sxs-lookup"><span data-stu-id="ccd5d-116">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="ccd5d-117">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ccd5d-117">Texture1D</span></span>                              | <span data-ttu-id="ccd5d-118">FLOAT</span><span class="sxs-lookup"><span data-stu-id="ccd5d-118">float</span></span>          |
| <span data-ttu-id="ccd5d-119">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="ccd5d-119">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="ccd5d-120">float2</span><span class="sxs-lookup"><span data-stu-id="ccd5d-120">float2</span></span>         |
| <span data-ttu-id="ccd5d-121">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="ccd5d-121">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="ccd5d-122">float3</span><span class="sxs-lookup"><span data-stu-id="ccd5d-122">float3</span></span>         |
| <span data-ttu-id="ccd5d-123">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="ccd5d-123">TextureCubeArray</span></span>                       | <span data-ttu-id="ccd5d-124">float4</span><span class="sxs-lookup"><span data-stu-id="ccd5d-124">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="ccd5d-125">*Desplazamiento* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ccd5d-125">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ccd5d-126">Desplazamiento de coordenadas de textura opcional, que se puede usar para cualquier tipo de objeto de textura. el desplazamiento se aplica a la ubicación antes del muestreo.</span><span class="sxs-lookup"><span data-stu-id="ccd5d-126">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="ccd5d-127">Use un desplazamiento solo en un entero miplevel; de lo contrario, puede obtener resultados que no se traduzcan bien al hardware.</span><span class="sxs-lookup"><span data-stu-id="ccd5d-127">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="ccd5d-128">El tipo de argumento depende del tipo de objeto de textura.</span><span class="sxs-lookup"><span data-stu-id="ccd5d-128">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="ccd5d-129">Para obtener más información, vea [aplicar desplazamientos enteros](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="ccd5d-129">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="ccd5d-130">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="ccd5d-130">Texture-Object Type</span></span>           | <span data-ttu-id="ccd5d-131">Tipo de parámetro</span><span class="sxs-lookup"><span data-stu-id="ccd5d-131">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="ccd5d-132">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="ccd5d-132">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="ccd5d-133">int</span><span class="sxs-lookup"><span data-stu-id="ccd5d-133">int</span></span>            |
| <span data-ttu-id="ccd5d-134">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="ccd5d-134">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="ccd5d-135">int2</span><span class="sxs-lookup"><span data-stu-id="ccd5d-135">int2</span></span>           |
| <span data-ttu-id="ccd5d-136">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ccd5d-136">Texture3D</span></span>                     | <span data-ttu-id="ccd5d-137">int3</span><span class="sxs-lookup"><span data-stu-id="ccd5d-137">int3</span></span>           |
| <span data-ttu-id="ccd5d-138">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="ccd5d-138">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="ccd5d-139">no admitido</span><span class="sxs-lookup"><span data-stu-id="ccd5d-139">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="ccd5d-140">*Abrazadera* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ccd5d-140">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ccd5d-141">Un valor opcional en el que se van a fijar los valores LOD de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="ccd5d-141">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="ccd5d-142">Por ejemplo, si se pasa 2.0 f para el valor Clamp, se asegura de que ningún ejemplo individual tenga acceso a un nivel de MIP inferior a 2.0 f.</span><span class="sxs-lookup"><span data-stu-id="ccd5d-142">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> <dt>

<span data-ttu-id="ccd5d-143">*Estado* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="ccd5d-143">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ccd5d-144">Estado de la operación.</span><span class="sxs-lookup"><span data-stu-id="ccd5d-144">The status of the operation.</span></span> <span data-ttu-id="ccd5d-145">No se puede tener acceso directamente al estado. en su lugar, pase el estado a la función intrínseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="ccd5d-145">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="ccd5d-146">**CheckAccessFullyMapped** devuelve **true** si todos los valores de la operación de **ejemplo**, **recopilación** o **carga** correspondiente han tenido acceso a los mosaicos asignados en un [recurso en mosaico](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="ccd5d-146">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="ccd5d-147">Si se tomó algún valor de un mosaico sin asignar, **CheckAccessFullyMapped** devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="ccd5d-147">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ccd5d-148">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ccd5d-148">Return value</span></span>

<span data-ttu-id="ccd5d-149">Formato de textura, que es uno de los valores con tipo que aparecen [**en \_ formato de DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="ccd5d-149">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="ccd5d-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="ccd5d-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ccd5d-151">Métodos de ejemplo</span><span class="sxs-lookup"><span data-stu-id="ccd5d-151">Sample methods</span></span>](texture3d-sample.md)
</dt> <dt>

[<span data-ttu-id="ccd5d-152">**Texture3D**</span><span class="sxs-lookup"><span data-stu-id="ccd5d-152">**Texture3D**</span></span>](sm5-object-texture3d.md)
</dt> </dl>

 

 
