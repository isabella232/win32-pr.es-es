---
title: 'SampleBias:: SampleBias (S, Float, Float, float) (función)'
description: 'Muestrea una textura, después de aplicar el valor de diferencia al nivel de mipmap, con un valor opcional para Clamp valores de nivel de detalle (LOD) de ejemplo en. | SampleBias:: SampleBias (S, Float, Float, float) (función)'
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
ms.openlocfilehash: 8d95a1b0341e61853a20d313a04d1cde64dde66d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104157076"
---
# <a name="samplebiassamplebiassfloatfloatfloat-function"></a><span data-ttu-id="b3800-105">SampleBias:: SampleBias (S, Float, Float, float) (función)</span><span class="sxs-lookup"><span data-stu-id="b3800-105">SampleBias::SampleBias(S,float,float,float) function</span></span>

<span data-ttu-id="b3800-106">Muestrea una textura, después de aplicar el valor de diferencia al nivel de mipmap, con un valor opcional para Clamp valores de nivel de detalle (LOD) de ejemplo en.</span><span class="sxs-lookup"><span data-stu-id="b3800-106">Samples a texture, after applying the bias value to the mipmap level, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3800-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b3800-107">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleBias(
  in SamplerState S,
  in float        Location,
  in float        Bias,
  in float        Clamp
);
```



## <a name="parameters"></a><span data-ttu-id="b3800-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b3800-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3800-109">*S* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="b3800-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3800-110">Tipo: **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="b3800-110">Type: **SamplerState**</span></span>

<span data-ttu-id="b3800-111">Un [Estado de muestra](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="b3800-111">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="b3800-112">Se trata de un objeto declarado en un archivo de efectos que contiene las asignaciones de estado.</span><span class="sxs-lookup"><span data-stu-id="b3800-112">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="b3800-113">*Ubicación* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="b3800-113">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3800-114">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="b3800-114">Type: **float**</span></span>

<span data-ttu-id="b3800-115">Las coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="b3800-115">The texture coordinates.</span></span> <span data-ttu-id="b3800-116">El tipo de argumento depende del tipo de objeto de textura.</span><span class="sxs-lookup"><span data-stu-id="b3800-116">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="b3800-117">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="b3800-117">Texture-Object Type</span></span>                    | <span data-ttu-id="b3800-118">Tipo de parámetro</span><span class="sxs-lookup"><span data-stu-id="b3800-118">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="b3800-119">Texture1D</span><span class="sxs-lookup"><span data-stu-id="b3800-119">Texture1D</span></span>                              | <span data-ttu-id="b3800-120">FLOAT</span><span class="sxs-lookup"><span data-stu-id="b3800-120">float</span></span>          |
| <span data-ttu-id="b3800-121">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="b3800-121">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="b3800-122">float2</span><span class="sxs-lookup"><span data-stu-id="b3800-122">float2</span></span>         |
| <span data-ttu-id="b3800-123">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="b3800-123">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="b3800-124">float3</span><span class="sxs-lookup"><span data-stu-id="b3800-124">float3</span></span>         |
| <span data-ttu-id="b3800-125">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="b3800-125">TextureCubeArray</span></span>                       | <span data-ttu-id="b3800-126">float4</span><span class="sxs-lookup"><span data-stu-id="b3800-126">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="b3800-127">*Bias* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b3800-127">*Bias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3800-128">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="b3800-128">Type: **float**</span></span>

<span data-ttu-id="b3800-129">El valor de diferencia, que es un número de punto flotante entre 0,0 y 1,0, ambos inclusive, se aplica a un nivel de MIP antes del muestreo.</span><span class="sxs-lookup"><span data-stu-id="b3800-129">The bias value, which is a floating-point number between 0.0 and 1.0 inclusive, is applied to a mip level before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="b3800-130">*Abrazadera* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b3800-130">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3800-131">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="b3800-131">Type: **float**</span></span>

<span data-ttu-id="b3800-132">Un valor opcional en el que se van a fijar los valores LOD de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="b3800-132">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="b3800-133">Por ejemplo, si se pasa 2.0 f para el valor Clamp, se asegura de que ningún ejemplo individual tenga acceso a un nivel de MIP inferior a 2.0 f.</span><span class="sxs-lookup"><span data-stu-id="b3800-133">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3800-134">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b3800-134">Return value</span></span>

<span data-ttu-id="b3800-135">Tipo: **[ **\_ formato de DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="b3800-135">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="b3800-136">Formato de textura, que es uno de los valores con tipo que aparecen [**en \_ formato de DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="b3800-136">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="b3800-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="b3800-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3800-138">Métodos SampleBias</span><span class="sxs-lookup"><span data-stu-id="b3800-138">SampleBias methods</span></span>](texturecubearray-samplebias.md)
</dt> <dt>

[<span data-ttu-id="b3800-139">**TextureCubeArray**</span><span class="sxs-lookup"><span data-stu-id="b3800-139">**TextureCubeArray**</span></span>](texturecubearray.md)
</dt> </dl>

 

 
