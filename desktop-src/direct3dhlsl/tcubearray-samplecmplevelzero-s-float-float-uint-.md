---
title: 'Función SampleCmpLevelZero:: SampleCmpLevelZero (S, Float, Float, uint) para TextureCubeArray'
description: Muestrea solo una textura en el nivel 0 del mipmap y compara el resultado con un valor de comparación y, a continuación, devuelve el estado de la operación. Para TextureCubeArray.
ms.assetid: D73447C6-E77C-4027-B265-24F96C679357
keywords:
- SampleCmpLevelZero de función HLSL
topic_type:
- apiref
api_name:
- SampleCmpLevelZero
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ac042bd2856aa69bbba1293fb91ff74d95c0de53
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/16/2021
ms.locfileid: "103821554"
---
# <a name="samplecmplevelzerosamplecmplevelzerosfloatfloatuint-function-for-texturecubearray"></a><span data-ttu-id="e5518-105">Función SampleCmpLevelZero:: SampleCmpLevelZero (S, Float, Float, uint) para TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="e5518-105">SampleCmpLevelZero::SampleCmpLevelZero(S,float,float,uint) function for TextureCubeArray</span></span>

<span data-ttu-id="e5518-106">Muestrea solo una textura en el nivel 0 del mipmap y compara el resultado con un valor de comparación.</span><span class="sxs-lookup"><span data-stu-id="e5518-106">Samples a texture on mipmap level 0 only and compares the result to a comparison value.</span></span> <span data-ttu-id="e5518-107">Devuelve el estado de la operación.</span><span class="sxs-lookup"><span data-stu-id="e5518-107">Returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5518-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e5518-108">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleCmpLevelZero(
  in  SamplerState S,
  in  float        Location,
  in  float        CompareValue,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="e5518-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e5518-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5518-110">*S* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="e5518-110">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5518-111">Tipo: **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="e5518-111">Type: **SamplerState**</span></span>

<span data-ttu-id="e5518-112">Un [Estado de muestra](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="e5518-112">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="e5518-113">Se trata de un objeto declarado en un archivo de efectos que contiene las asignaciones de estado.</span><span class="sxs-lookup"><span data-stu-id="e5518-113">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="e5518-114">*Ubicación* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="e5518-114">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5518-115">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="e5518-115">Type: **float**</span></span>

<span data-ttu-id="e5518-116">Las coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="e5518-116">The texture coordinates.</span></span> <span data-ttu-id="e5518-117">El tipo de argumento depende del tipo de objeto de textura.</span><span class="sxs-lookup"><span data-stu-id="e5518-117">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="e5518-118">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="e5518-118">Texture-Object Type</span></span>                    | <span data-ttu-id="e5518-119">Tipo de parámetro</span><span class="sxs-lookup"><span data-stu-id="e5518-119">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="e5518-120">Texture1D</span><span class="sxs-lookup"><span data-stu-id="e5518-120">Texture1D</span></span>                              | <span data-ttu-id="e5518-121">FLOAT</span><span class="sxs-lookup"><span data-stu-id="e5518-121">float</span></span>          |
| <span data-ttu-id="e5518-122">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="e5518-122">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="e5518-123">float2</span><span class="sxs-lookup"><span data-stu-id="e5518-123">float2</span></span>         |
| <span data-ttu-id="e5518-124">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="e5518-124">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="e5518-125">float3</span><span class="sxs-lookup"><span data-stu-id="e5518-125">float3</span></span>         |
| <span data-ttu-id="e5518-126">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="e5518-126">TextureCubeArray</span></span>                       | <span data-ttu-id="e5518-127">float4</span><span class="sxs-lookup"><span data-stu-id="e5518-127">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="e5518-128">*CompareValue* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e5518-128">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5518-129">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="e5518-129">Type: **float**</span></span>

<span data-ttu-id="e5518-130">Un valor de punto flotante que se va a utilizar como valor de comparación.</span><span class="sxs-lookup"><span data-stu-id="e5518-130">A floating-point value to use as a comparison value.</span></span>

</dd> <dt>

<span data-ttu-id="e5518-131">*Estado* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="e5518-131">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e5518-132">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="e5518-132">Type: **uint**</span></span>

<span data-ttu-id="e5518-133">Estado de la operación.</span><span class="sxs-lookup"><span data-stu-id="e5518-133">The status of the operation.</span></span> <span data-ttu-id="e5518-134">No se puede tener acceso directamente al estado. en su lugar, pase el estado a la función intrínseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="e5518-134">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="e5518-135">**CheckAccessFullyMapped** devuelve **true** si todos los valores de la operación de **ejemplo**, **recopilación** o **carga** correspondiente han tenido acceso a los mosaicos asignados en un [recurso en mosaico](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="e5518-135">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="e5518-136">Si se tomó algún valor de un mosaico sin asignar, **CheckAccessFullyMapped** devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="e5518-136">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e5518-137">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e5518-137">Return value</span></span>

<span data-ttu-id="e5518-138">Tipo: **[ **\_ formato de DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="e5518-138">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="e5518-139">Formato de textura, que es uno de los valores con tipo que aparecen [**en \_ formato de DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="e5518-139">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="e5518-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="e5518-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5518-141">Métodos SampleCmpLevelZero</span><span class="sxs-lookup"><span data-stu-id="e5518-141">SampleCmpLevelZero methods</span></span>](texturecubearray-samplecmplevelzero.md)
</dt> <dt>

[<span data-ttu-id="e5518-142">**TextureCubeArray**</span><span class="sxs-lookup"><span data-stu-id="e5518-142">**TextureCubeArray**</span></span>](texturecubearray.md)
</dt> </dl>

 

 
