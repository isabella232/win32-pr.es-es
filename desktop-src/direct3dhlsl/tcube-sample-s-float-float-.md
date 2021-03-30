---
title: 'TextureCube:: sample (S, Float, float) (función)'
description: 'Muestrea una textura con un valor opcional para Clamp valores de nivel de detalle (LOD) de ejemplo en. | TextureCube:: sample (S, Float, float) (función)'
ms.assetid: 7DB25135-46B5-48E2-91D0-A45D355179D6
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
ms.openlocfilehash: 2ce841eb68e426fc76032d45353f2b439f0f3e4b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104279939"
---
# <a name="texturecubesamplesfloatfloat-function"></a><span data-ttu-id="01d31-105">TextureCube:: sample (S, Float, float) (función)</span><span class="sxs-lookup"><span data-stu-id="01d31-105">TextureCube::Sample(S,float,float) function</span></span>

<span data-ttu-id="01d31-106">Muestrea una textura con un valor opcional para Clamp valores de nivel de detalle (LOD) de ejemplo en.</span><span class="sxs-lookup"><span data-stu-id="01d31-106">Samples a texture with an optional value to clamp sample level-of-detail (LOD) values to.</span></span>

## <a name="syntax"></a><span data-ttu-id="01d31-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="01d31-107">Syntax</span></span>


``` syntax
DXGI_FORMAT Sample(
  in SamplerState S,
  in float        Location,
  in float        Clamp
);
```



## <a name="parameters"></a><span data-ttu-id="01d31-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="01d31-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01d31-109">*S* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="01d31-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01d31-110">Tipo: **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="01d31-110">Type: **SamplerState**</span></span>

<span data-ttu-id="01d31-111">Un [Estado de muestra](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="01d31-111">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="01d31-112">Se trata de un objeto declarado en un archivo de efectos que contiene las asignaciones de estado.</span><span class="sxs-lookup"><span data-stu-id="01d31-112">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="01d31-113">*Ubicación* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="01d31-113">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01d31-114">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="01d31-114">Type: **float**</span></span>

<span data-ttu-id="01d31-115">Las coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="01d31-115">The texture coordinates.</span></span> <span data-ttu-id="01d31-116">El tipo de argumento depende del tipo de objeto de textura.</span><span class="sxs-lookup"><span data-stu-id="01d31-116">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="01d31-117">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="01d31-117">Texture-Object Type</span></span>                    | <span data-ttu-id="01d31-118">Tipo de parámetro</span><span class="sxs-lookup"><span data-stu-id="01d31-118">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="01d31-119">Texture1D</span><span class="sxs-lookup"><span data-stu-id="01d31-119">Texture1D</span></span>                              | <span data-ttu-id="01d31-120">FLOAT</span><span class="sxs-lookup"><span data-stu-id="01d31-120">float</span></span>          |
| <span data-ttu-id="01d31-121">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="01d31-121">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="01d31-122">float2</span><span class="sxs-lookup"><span data-stu-id="01d31-122">float2</span></span>         |
| <span data-ttu-id="01d31-123">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="01d31-123">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="01d31-124">float3</span><span class="sxs-lookup"><span data-stu-id="01d31-124">float3</span></span>         |
| <span data-ttu-id="01d31-125">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="01d31-125">TextureCubeArray</span></span>                       | <span data-ttu-id="01d31-126">float4</span><span class="sxs-lookup"><span data-stu-id="01d31-126">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="01d31-127">*Abrazadera* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="01d31-127">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01d31-128">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="01d31-128">Type: **float**</span></span>

<span data-ttu-id="01d31-129">Un valor opcional en el que se van a fijar los valores LOD de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="01d31-129">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="01d31-130">Por ejemplo, si se pasa 2.0 f para el valor Clamp, se asegura de que ningún ejemplo individual tenga acceso a un nivel de MIP inferior a 2.0 f.</span><span class="sxs-lookup"><span data-stu-id="01d31-130">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01d31-131">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="01d31-131">Return value</span></span>

<span data-ttu-id="01d31-132">Tipo: **[ **\_ formato de DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="01d31-132">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="01d31-133">Formato de textura, que es uno de los valores con tipo que aparecen [**en \_ formato de DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="01d31-133">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="01d31-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="01d31-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01d31-135">Métodos de ejemplo</span><span class="sxs-lookup"><span data-stu-id="01d31-135">Sample methods</span></span>](texturecube-sample.md)
</dt> <dt>

[<span data-ttu-id="01d31-136">**TextureCube**</span><span class="sxs-lookup"><span data-stu-id="01d31-136">**TextureCube**</span></span>](texturecube.md)
</dt> </dl>

 

 
