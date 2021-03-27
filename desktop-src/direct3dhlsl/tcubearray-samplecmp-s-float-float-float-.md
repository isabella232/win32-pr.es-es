---
title: 'Función SampleCmp:: SampleCmp (S, Float, Float, float) para TextureCubeArray'
description: 'Muestrea una textura, utilizando un valor de comparación para rechazar muestras, con un valor opcional para Clamp valores de nivel de detalle (LOD) de ejemplo en. | Función SampleCmp:: SampleCmp (S, Float, Float, float) para TextureCubeArray'
ms.assetid: A8824A82-A3FD-4FEE-BC10-56843997BBCE
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
ms.openlocfilehash: e65b1747d03b3a0555267f7b57e95a4d5aba54da
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/16/2021
ms.locfileid: "104987271"
---
# <a name="samplecmpsamplecmpsfloatfloatfloat-function-for-texturecubearray"></a><span data-ttu-id="01beb-105">Función SampleCmp:: SampleCmp (S, Float, Float, float) para TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="01beb-105">SampleCmp::SampleCmp(S,float,float,float) function for TextureCubeArray</span></span>

<span data-ttu-id="01beb-106">Muestrea una textura, utilizando un valor de comparación para rechazar muestras, con un valor opcional para Clamp valores de nivel de detalle (LOD) de ejemplo en.</span><span class="sxs-lookup"><span data-stu-id="01beb-106">Samples a texture, using a comparison value to reject samples, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span>

## <a name="syntax"></a><span data-ttu-id="01beb-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="01beb-107">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleCmp(
  in SamplerState S,
  in float        Location,
  in float        CompareValue,
  in float        Clamp
);
```



## <a name="parameters"></a><span data-ttu-id="01beb-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="01beb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01beb-109">*S* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="01beb-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01beb-110">Tipo: **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="01beb-110">Type: **SamplerState**</span></span>

<span data-ttu-id="01beb-111">Un [Estado de muestra](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="01beb-111">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="01beb-112">Se trata de un objeto declarado en un archivo de efectos que contiene las asignaciones de estado.</span><span class="sxs-lookup"><span data-stu-id="01beb-112">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="01beb-113">*Ubicación* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="01beb-113">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01beb-114">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="01beb-114">Type: **float**</span></span>

<span data-ttu-id="01beb-115">Las coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="01beb-115">The texture coordinates.</span></span> <span data-ttu-id="01beb-116">El tipo de argumento depende del tipo de objeto de textura.</span><span class="sxs-lookup"><span data-stu-id="01beb-116">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="01beb-117">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="01beb-117">Texture-Object Type</span></span>                    | <span data-ttu-id="01beb-118">Tipo de parámetro</span><span class="sxs-lookup"><span data-stu-id="01beb-118">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="01beb-119">Texture1D</span><span class="sxs-lookup"><span data-stu-id="01beb-119">Texture1D</span></span>                              | <span data-ttu-id="01beb-120">FLOAT</span><span class="sxs-lookup"><span data-stu-id="01beb-120">float</span></span>          |
| <span data-ttu-id="01beb-121">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="01beb-121">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="01beb-122">float2</span><span class="sxs-lookup"><span data-stu-id="01beb-122">float2</span></span>         |
| <span data-ttu-id="01beb-123">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="01beb-123">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="01beb-124">float3</span><span class="sxs-lookup"><span data-stu-id="01beb-124">float3</span></span>         |
| <span data-ttu-id="01beb-125">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="01beb-125">TextureCubeArray</span></span>                       | <span data-ttu-id="01beb-126">float4</span><span class="sxs-lookup"><span data-stu-id="01beb-126">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="01beb-127">*CompareValue* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="01beb-127">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01beb-128">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="01beb-128">Type: **float**</span></span>

<span data-ttu-id="01beb-129">Un valor de punto flotante que se va a utilizar como valor de comparación.</span><span class="sxs-lookup"><span data-stu-id="01beb-129">A floating-point value to use as a comparison value.</span></span>

</dd> <dt>

<span data-ttu-id="01beb-130">*Abrazadera* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="01beb-130">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01beb-131">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="01beb-131">Type: **float**</span></span>

<span data-ttu-id="01beb-132">Un valor opcional en el que se van a fijar los valores LOD de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="01beb-132">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="01beb-133">Por ejemplo, si se pasa 2.0 f para el valor Clamp, se asegura de que ningún ejemplo individual tenga acceso a un nivel de MIP inferior a 2.0 f.</span><span class="sxs-lookup"><span data-stu-id="01beb-133">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01beb-134">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="01beb-134">Return value</span></span>

<span data-ttu-id="01beb-135">Tipo: **[ **\_ formato de DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="01beb-135">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="01beb-136">Formato de textura, que es uno de los valores con tipo que aparecen [**en \_ formato de DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="01beb-136">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="01beb-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="01beb-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01beb-138">Métodos SampleCmp</span><span class="sxs-lookup"><span data-stu-id="01beb-138">SampleCmp methods</span></span>](texturecubearray-samplecmp.md)
</dt> <dt>

[<span data-ttu-id="01beb-139">**TextureCubeArray**</span><span class="sxs-lookup"><span data-stu-id="01beb-139">**TextureCubeArray**</span></span>](texturecubearray.md)
</dt> </dl>

 

 
