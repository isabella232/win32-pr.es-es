---
title: 'Función SampleBias:: SampleBias (S, Float, Float, Float, uint) para TextureCube'
description: 'La función SampleBias:: SampleBias (S, Float, Float, Float, uint) para TextureCube muestrea una textura después de aplicar el valor de Bias al nivel de mipmap.'
ms.assetid: A2F10B9B-5DF2-4389-83A9-F6A29781BF0A
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
ms.openlocfilehash: 116749acdc23bb8ac2fd057139bf8ef7c8f5ddcc
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/02/2021
ms.locfileid: "106187686"
---
# <a name="samplebiassamplebiassfloatfloatfloatuint-function-for-texturecube"></a><span data-ttu-id="f8fce-104">Función SampleBias:: SampleBias (S, Float, Float, Float, uint) para TextureCube</span><span class="sxs-lookup"><span data-stu-id="f8fce-104">SampleBias::SampleBias(S,float,float,float,uint) function for TextureCube</span></span>

<span data-ttu-id="f8fce-105">Muestrea una textura, después de aplicar el valor de diferencia al nivel de mipmap, con un valor opcional para Clamp valores de nivel de detalle (LOD) de ejemplo en.</span><span class="sxs-lookup"><span data-stu-id="f8fce-105">Samples a texture, after applying the bias value to the mipmap level, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span> <span data-ttu-id="f8fce-106">Devuelve el estado de la operación.</span><span class="sxs-lookup"><span data-stu-id="f8fce-106">Returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8fce-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f8fce-107">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleBias(
  in  SamplerState S,
  in  float        Location,
  in  float        Bias,
  in  float        Clamp,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="f8fce-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f8fce-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8fce-109">*S* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="f8fce-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8fce-110">Tipo: **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="f8fce-110">Type: **SamplerState**</span></span>

<span data-ttu-id="f8fce-111">Un [Estado de muestra](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="f8fce-111">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="f8fce-112">Se trata de un objeto declarado en un archivo de efectos que contiene las asignaciones de estado.</span><span class="sxs-lookup"><span data-stu-id="f8fce-112">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="f8fce-113">*Ubicación* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="f8fce-113">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8fce-114">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="f8fce-114">Type: **float**</span></span>

<span data-ttu-id="f8fce-115">Las coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="f8fce-115">The texture coordinates.</span></span> <span data-ttu-id="f8fce-116">El tipo de argumento depende del tipo de objeto de textura.</span><span class="sxs-lookup"><span data-stu-id="f8fce-116">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="f8fce-117">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="f8fce-117">Texture-Object Type</span></span>                    | <span data-ttu-id="f8fce-118">Tipo de parámetro</span><span class="sxs-lookup"><span data-stu-id="f8fce-118">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="f8fce-119">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f8fce-119">Texture1D</span></span>                              | <span data-ttu-id="f8fce-120">FLOAT</span><span class="sxs-lookup"><span data-stu-id="f8fce-120">float</span></span>          |
| <span data-ttu-id="f8fce-121">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="f8fce-121">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="f8fce-122">float2</span><span class="sxs-lookup"><span data-stu-id="f8fce-122">float2</span></span>         |
| <span data-ttu-id="f8fce-123">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="f8fce-123">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="f8fce-124">float3</span><span class="sxs-lookup"><span data-stu-id="f8fce-124">float3</span></span>         |
| <span data-ttu-id="f8fce-125">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="f8fce-125">TextureCubeArray</span></span>                       | <span data-ttu-id="f8fce-126">float4</span><span class="sxs-lookup"><span data-stu-id="f8fce-126">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="f8fce-127">*Bias* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f8fce-127">*Bias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8fce-128">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="f8fce-128">Type: **float**</span></span>

<span data-ttu-id="f8fce-129">El valor de diferencia, que es un número de punto flotante entre 0,0 y 1,0, ambos inclusive, se aplica a un nivel de MIP antes del muestreo.</span><span class="sxs-lookup"><span data-stu-id="f8fce-129">The bias value, which is a floating-point number between 0.0 and 1.0 inclusive, is applied to a mip level before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="f8fce-130">*Abrazadera* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f8fce-130">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8fce-131">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="f8fce-131">Type: **float**</span></span>

<span data-ttu-id="f8fce-132">Un valor opcional en el que se van a fijar los valores LOD de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="f8fce-132">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="f8fce-133">Por ejemplo, si se pasa 2.0 f para el valor Clamp, se asegura de que ningún ejemplo individual tenga acceso a un nivel de MIP inferior a 2.0 f.</span><span class="sxs-lookup"><span data-stu-id="f8fce-133">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> <dt>

<span data-ttu-id="f8fce-134">*Estado* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="f8fce-134">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f8fce-135">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="f8fce-135">Type: **uint**</span></span>

<span data-ttu-id="f8fce-136">Estado de la operación.</span><span class="sxs-lookup"><span data-stu-id="f8fce-136">The status of the operation.</span></span> <span data-ttu-id="f8fce-137">No se puede tener acceso directamente al estado. en su lugar, pase el estado a la función intrínseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="f8fce-137">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="f8fce-138">**CheckAccessFullyMapped** devuelve **true** si todos los valores de la operación de **ejemplo**, **recopilación** o **carga** correspondiente han tenido acceso a los mosaicos asignados en un [recurso en mosaico](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="f8fce-138">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="f8fce-139">Si se tomó algún valor de un mosaico sin asignar, **CheckAccessFullyMapped** devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="f8fce-139">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8fce-140">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f8fce-140">Return value</span></span>

<span data-ttu-id="f8fce-141">Tipo: **[ **\_ formato de DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="f8fce-141">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="f8fce-142">Formato de textura, que es uno de los valores con tipo que aparecen [**en \_ formato de DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="f8fce-142">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="f8fce-143">Consulte también</span><span class="sxs-lookup"><span data-stu-id="f8fce-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8fce-144">Métodos SampleBias</span><span class="sxs-lookup"><span data-stu-id="f8fce-144">SampleBias methods</span></span>](texturecube-samplebias.md)
</dt> <dt>

[<span data-ttu-id="f8fce-145">**TextureCube**</span><span class="sxs-lookup"><span data-stu-id="f8fce-145">**TextureCube**</span></span>](texturecube.md)
</dt> </dl>

 

 
