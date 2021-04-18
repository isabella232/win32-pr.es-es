---
title: 'Función SampleBias:: SampleBias (S, Float, Float, float) para TextureCubeArray'
description: 'La función SampleBias:: SampleBias (S, Float, Float, float) para TextureCubeArray muestrea una textura, después de aplicar el valor de Bias al nivel de mipmap.'
ms.assetid: 6683F115-4F81-4C24-B735-67DB4B52455B
keywords:
- SampleBias de función HLSL
topic_type:
- apiref
api_name:
- SampleBias
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0c57eec224ca92b2584ba7262488530ea7080939
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/02/2021
ms.locfileid: "106187810"
---
# <a name="samplebiassamplebiassfloatfloatfloat-function-for-texturecubearray"></a><span data-ttu-id="ebbb6-104">Función SampleBias:: SampleBias (S, Float, Float, float) para TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="ebbb6-104">SampleBias::SampleBias(S,float,float,float) function for TextureCubeArray</span></span>

<span data-ttu-id="ebbb6-105">Muestrea una textura, después de aplicar el valor de diferencia al nivel de mipmap, con un valor opcional para Clamp valores de nivel de detalle (LOD) de ejemplo en.</span><span class="sxs-lookup"><span data-stu-id="ebbb6-105">Samples a texture, after applying the bias value to the mipmap level, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span>

## <a name="syntax"></a><span data-ttu-id="ebbb6-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ebbb6-106">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleBias(
  in SamplerState S,
  in float        Location,
  in float        Bias,
  in float        Clamp
);
```



## <a name="parameters"></a><span data-ttu-id="ebbb6-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ebbb6-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ebbb6-108">*S* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="ebbb6-108">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ebbb6-109">Tipo: **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="ebbb6-109">Type: **SamplerState**</span></span>

<span data-ttu-id="ebbb6-110">Un [Estado de muestra](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="ebbb6-110">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="ebbb6-111">Se trata de un objeto declarado en un archivo de efectos que contiene las asignaciones de estado.</span><span class="sxs-lookup"><span data-stu-id="ebbb6-111">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="ebbb6-112">*Ubicación* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="ebbb6-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ebbb6-113">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="ebbb6-113">Type: **float**</span></span>

<span data-ttu-id="ebbb6-114">Las coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="ebbb6-114">The texture coordinates.</span></span> <span data-ttu-id="ebbb6-115">El tipo de argumento depende del tipo de objeto de textura.</span><span class="sxs-lookup"><span data-stu-id="ebbb6-115">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="ebbb6-116">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="ebbb6-116">Texture-Object Type</span></span>                    | <span data-ttu-id="ebbb6-117">Tipo de parámetro</span><span class="sxs-lookup"><span data-stu-id="ebbb6-117">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="ebbb6-118">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ebbb6-118">Texture1D</span></span>                              | <span data-ttu-id="ebbb6-119">FLOAT</span><span class="sxs-lookup"><span data-stu-id="ebbb6-119">float</span></span>          |
| <span data-ttu-id="ebbb6-120">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="ebbb6-120">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="ebbb6-121">float2</span><span class="sxs-lookup"><span data-stu-id="ebbb6-121">float2</span></span>         |
| <span data-ttu-id="ebbb6-122">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="ebbb6-122">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="ebbb6-123">float3</span><span class="sxs-lookup"><span data-stu-id="ebbb6-123">float3</span></span>         |
| <span data-ttu-id="ebbb6-124">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="ebbb6-124">TextureCubeArray</span></span>                       | <span data-ttu-id="ebbb6-125">float4</span><span class="sxs-lookup"><span data-stu-id="ebbb6-125">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="ebbb6-126">*Bias* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ebbb6-126">*Bias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ebbb6-127">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="ebbb6-127">Type: **float**</span></span>

<span data-ttu-id="ebbb6-128">El valor de diferencia, que es un número de punto flotante entre 0,0 y 1,0, ambos inclusive, se aplica a un nivel de MIP antes del muestreo.</span><span class="sxs-lookup"><span data-stu-id="ebbb6-128">The bias value, which is a floating-point number between 0.0 and 1.0 inclusive, is applied to a mip level before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="ebbb6-129">*Abrazadera* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ebbb6-129">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ebbb6-130">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="ebbb6-130">Type: **float**</span></span>

<span data-ttu-id="ebbb6-131">Un valor opcional en el que se van a fijar los valores LOD de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="ebbb6-131">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="ebbb6-132">Por ejemplo, si se pasa 2.0 f para el valor Clamp, se asegura de que ningún ejemplo individual tenga acceso a un nivel de MIP inferior a 2.0 f.</span><span class="sxs-lookup"><span data-stu-id="ebbb6-132">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ebbb6-133">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ebbb6-133">Return value</span></span>

<span data-ttu-id="ebbb6-134">Tipo: **[ **\_ formato de DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="ebbb6-134">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="ebbb6-135">Formato de textura, que es uno de los valores con tipo que aparecen [**en \_ formato de DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="ebbb6-135">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="ebbb6-136">Consulte también</span><span class="sxs-lookup"><span data-stu-id="ebbb6-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ebbb6-137">Métodos SampleBias</span><span class="sxs-lookup"><span data-stu-id="ebbb6-137">SampleBias methods</span></span>](texturecubearray-samplebias.md)
</dt> <dt>

[<span data-ttu-id="ebbb6-138">**TextureCubeArray**</span><span class="sxs-lookup"><span data-stu-id="ebbb6-138">**TextureCubeArray**</span></span>](texturecubearray.md)
</dt> </dl>

 

 
