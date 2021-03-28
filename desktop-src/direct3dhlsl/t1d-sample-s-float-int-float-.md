---
title: 'Texture1D:: sample (S, Float, int, float) (función)'
description: 'Muestrea una textura con un valor opcional para Clamp valores de nivel de detalle (LOD) de ejemplo en. | Texture1D:: sample (S, Float, int, float) (función)'
ms.assetid: D2E2E143-8240-43AA-AD70-BD793B3CFD19
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
ms.openlocfilehash: f119955a66f7aec336ce52d730d54a5f11756527
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104083664"
---
# <a name="texture1dsamplesfloatintfloat-function"></a><span data-ttu-id="ecff7-105">Texture1D:: sample (S, Float, int, float) (función)</span><span class="sxs-lookup"><span data-stu-id="ecff7-105">Texture1D::Sample(S,float,int,float) function</span></span>

<span data-ttu-id="ecff7-106">Muestrea una textura con un valor opcional para Clamp valores de nivel de detalle (LOD) de ejemplo en.</span><span class="sxs-lookup"><span data-stu-id="ecff7-106">Samples a texture with an optional value to clamp sample level-of-detail (LOD) values to.</span></span>

## <a name="syntax"></a><span data-ttu-id="ecff7-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ecff7-107">Syntax</span></span>


``` syntax
DXGI_FORMAT Sample(
  in SamplerState S,
  in float        Location,
  in int          Offset,
  in float        Clamp
);
```



## <a name="parameters"></a><span data-ttu-id="ecff7-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ecff7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ecff7-109">*S* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="ecff7-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ecff7-110">Tipo: **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="ecff7-110">Type: **SamplerState**</span></span>

<span data-ttu-id="ecff7-111">Un [Estado de muestra](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="ecff7-111">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="ecff7-112">Se trata de un objeto declarado en un archivo de efectos que contiene las asignaciones de estado.</span><span class="sxs-lookup"><span data-stu-id="ecff7-112">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="ecff7-113">*Ubicación* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="ecff7-113">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ecff7-114">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="ecff7-114">Type: **float**</span></span>

<span data-ttu-id="ecff7-115">Las coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="ecff7-115">The texture coordinates.</span></span> <span data-ttu-id="ecff7-116">El tipo de argumento depende del tipo de objeto de textura.</span><span class="sxs-lookup"><span data-stu-id="ecff7-116">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="ecff7-117">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="ecff7-117">Texture-Object Type</span></span>                    | <span data-ttu-id="ecff7-118">Tipo de parámetro</span><span class="sxs-lookup"><span data-stu-id="ecff7-118">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="ecff7-119">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ecff7-119">Texture1D</span></span>                              | <span data-ttu-id="ecff7-120">FLOAT</span><span class="sxs-lookup"><span data-stu-id="ecff7-120">float</span></span>          |
| <span data-ttu-id="ecff7-121">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="ecff7-121">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="ecff7-122">float2</span><span class="sxs-lookup"><span data-stu-id="ecff7-122">float2</span></span>         |
| <span data-ttu-id="ecff7-123">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="ecff7-123">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="ecff7-124">float3</span><span class="sxs-lookup"><span data-stu-id="ecff7-124">float3</span></span>         |
| <span data-ttu-id="ecff7-125">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="ecff7-125">TextureCubeArray</span></span>                       | <span data-ttu-id="ecff7-126">float4</span><span class="sxs-lookup"><span data-stu-id="ecff7-126">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="ecff7-127">*Desplazamiento* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ecff7-127">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ecff7-128">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="ecff7-128">Type: **int**</span></span>

<span data-ttu-id="ecff7-129">Desplazamiento de coordenadas de textura opcional, que se puede usar para cualquier tipo de objeto de textura. el desplazamiento se aplica a la ubicación antes del muestreo.</span><span class="sxs-lookup"><span data-stu-id="ecff7-129">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="ecff7-130">Use un desplazamiento solo en un entero miplevel; de lo contrario, puede obtener resultados que no se traduzcan bien al hardware.</span><span class="sxs-lookup"><span data-stu-id="ecff7-130">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="ecff7-131">El tipo de argumento depende del tipo de objeto de textura.</span><span class="sxs-lookup"><span data-stu-id="ecff7-131">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="ecff7-132">Para obtener más información, vea [aplicar desplazamientos enteros](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="ecff7-132">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="ecff7-133">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="ecff7-133">Texture-Object Type</span></span>           | <span data-ttu-id="ecff7-134">Tipo de parámetro</span><span class="sxs-lookup"><span data-stu-id="ecff7-134">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="ecff7-135">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="ecff7-135">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="ecff7-136">int</span><span class="sxs-lookup"><span data-stu-id="ecff7-136">int</span></span>            |
| <span data-ttu-id="ecff7-137">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="ecff7-137">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="ecff7-138">int2</span><span class="sxs-lookup"><span data-stu-id="ecff7-138">int2</span></span>           |
| <span data-ttu-id="ecff7-139">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ecff7-139">Texture3D</span></span>                     | <span data-ttu-id="ecff7-140">int3</span><span class="sxs-lookup"><span data-stu-id="ecff7-140">int3</span></span>           |
| <span data-ttu-id="ecff7-141">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="ecff7-141">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="ecff7-142">no admitido</span><span class="sxs-lookup"><span data-stu-id="ecff7-142">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="ecff7-143">*Abrazadera* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ecff7-143">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ecff7-144">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="ecff7-144">Type: **float**</span></span>

<span data-ttu-id="ecff7-145">Un valor opcional en el que se van a fijar los valores LOD de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="ecff7-145">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="ecff7-146">Por ejemplo, si se pasa 2.0 f para el valor Clamp, se asegura de que ningún ejemplo individual tenga acceso a un nivel de MIP inferior a 2.0 f.</span><span class="sxs-lookup"><span data-stu-id="ecff7-146">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ecff7-147">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ecff7-147">Return value</span></span>

<span data-ttu-id="ecff7-148">Tipo: **[ **\_ formato de DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="ecff7-148">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="ecff7-149">Formato de textura, que es uno de los valores con tipo que aparecen [**en \_ formato de DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="ecff7-149">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="ecff7-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="ecff7-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ecff7-151">Métodos de ejemplo</span><span class="sxs-lookup"><span data-stu-id="ecff7-151">Sample methods</span></span>](texture1d-sample.md)
</dt> </dl>

 

 
