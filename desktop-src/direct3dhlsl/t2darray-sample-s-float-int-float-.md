---
title: 'Texture2DArray:: sample (S, Float, int, float) (función)'
description: 'Muestrea una textura con un valor opcional para Clamp valores de nivel de detalle (LOD) de ejemplo en. | Texture2DArray:: sample (S, Float, int, float) (función)'
ms.assetid: F6638224-0993-4F55-A8C0-7EC4140204D5
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
ms.openlocfilehash: 8d85e4d7e5662d76c011b1c5684f3fd36e4191ba
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104279994"
---
# <a name="texture2darraysamplesfloatintfloat-function"></a><span data-ttu-id="f7a14-105">Texture2DArray:: sample (S, Float, int, float) (función)</span><span class="sxs-lookup"><span data-stu-id="f7a14-105">Texture2DArray::Sample(S,float,int,float) function</span></span>

<span data-ttu-id="f7a14-106">Muestrea una textura con un valor opcional para Clamp valores de nivel de detalle (LOD) de ejemplo en.</span><span class="sxs-lookup"><span data-stu-id="f7a14-106">Samples a texture with an optional value to clamp sample level-of-detail (LOD) values to.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7a14-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f7a14-107">Syntax</span></span>


``` syntax
DXGI_FORMAT Sample(
  in SamplerState S,
  in float        Location,
  in int          Offset,
  in float        Clamp
);
```



## <a name="parameters"></a><span data-ttu-id="f7a14-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f7a14-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f7a14-109">*S* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="f7a14-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f7a14-110">Un [Estado de muestra](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="f7a14-110">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="f7a14-111">Se trata de un objeto declarado en un archivo de efectos que contiene las asignaciones de estado.</span><span class="sxs-lookup"><span data-stu-id="f7a14-111">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="f7a14-112">*Ubicación* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="f7a14-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f7a14-113">Las coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="f7a14-113">The texture coordinates.</span></span> <span data-ttu-id="f7a14-114">El tipo de argumento depende del tipo de objeto de textura.</span><span class="sxs-lookup"><span data-stu-id="f7a14-114">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="f7a14-115">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="f7a14-115">Texture-Object Type</span></span>                    | <span data-ttu-id="f7a14-116">Tipo de parámetro</span><span class="sxs-lookup"><span data-stu-id="f7a14-116">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="f7a14-117">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f7a14-117">Texture1D</span></span>                              | <span data-ttu-id="f7a14-118">FLOAT</span><span class="sxs-lookup"><span data-stu-id="f7a14-118">float</span></span>          |
| <span data-ttu-id="f7a14-119">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="f7a14-119">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="f7a14-120">float2</span><span class="sxs-lookup"><span data-stu-id="f7a14-120">float2</span></span>         |
| <span data-ttu-id="f7a14-121">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="f7a14-121">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="f7a14-122">float3</span><span class="sxs-lookup"><span data-stu-id="f7a14-122">float3</span></span>         |
| <span data-ttu-id="f7a14-123">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="f7a14-123">TextureCubeArray</span></span>                       | <span data-ttu-id="f7a14-124">float4</span><span class="sxs-lookup"><span data-stu-id="f7a14-124">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="f7a14-125">*Desplazamiento* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f7a14-125">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f7a14-126">Desplazamiento de coordenadas de textura opcional, que se puede usar para cualquier tipo de objeto de textura. el desplazamiento se aplica a la ubicación antes del muestreo.</span><span class="sxs-lookup"><span data-stu-id="f7a14-126">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="f7a14-127">Use un desplazamiento solo en un entero miplevel; de lo contrario, puede obtener resultados que no se traduzcan bien al hardware.</span><span class="sxs-lookup"><span data-stu-id="f7a14-127">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="f7a14-128">El tipo de argumento depende del tipo de objeto de textura.</span><span class="sxs-lookup"><span data-stu-id="f7a14-128">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="f7a14-129">Para obtener más información, vea [aplicar desplazamientos enteros](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="f7a14-129">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="f7a14-130">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="f7a14-130">Texture-Object Type</span></span>           | <span data-ttu-id="f7a14-131">Tipo de parámetro</span><span class="sxs-lookup"><span data-stu-id="f7a14-131">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="f7a14-132">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="f7a14-132">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="f7a14-133">int</span><span class="sxs-lookup"><span data-stu-id="f7a14-133">int</span></span>            |
| <span data-ttu-id="f7a14-134">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="f7a14-134">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="f7a14-135">int2</span><span class="sxs-lookup"><span data-stu-id="f7a14-135">int2</span></span>           |
| <span data-ttu-id="f7a14-136">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f7a14-136">Texture3D</span></span>                     | <span data-ttu-id="f7a14-137">int3</span><span class="sxs-lookup"><span data-stu-id="f7a14-137">int3</span></span>           |
| <span data-ttu-id="f7a14-138">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="f7a14-138">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="f7a14-139">no admitido</span><span class="sxs-lookup"><span data-stu-id="f7a14-139">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="f7a14-140">*Abrazadera* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f7a14-140">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f7a14-141">Un valor opcional en el que se van a fijar los valores LOD de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="f7a14-141">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="f7a14-142">Por ejemplo, si se pasa 2.0 f para el valor Clamp, se asegura de que ningún ejemplo individual tenga acceso a un nivel de MIP inferior a 2.0 f.</span><span class="sxs-lookup"><span data-stu-id="f7a14-142">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f7a14-143">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f7a14-143">Return value</span></span>

<span data-ttu-id="f7a14-144">Formato de textura, que es uno de los valores con tipo que aparecen [**en \_ formato de DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="f7a14-144">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="f7a14-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="f7a14-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7a14-146">Métodos de ejemplo</span><span class="sxs-lookup"><span data-stu-id="f7a14-146">Sample methods</span></span>](texture2darray-sample.md)
</dt> </dl>

 

 
