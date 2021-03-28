---
title: 'SampleLevel:: SampleLevel (S, Float, Float, uint) (función)'
description: 'Muestrea una textura en el nivel de mipmap especificado y devuelve el estado de la operación. | SampleLevel:: SampleLevel (S, Float, Float, uint) (función)'
ms.assetid: 3794D17F-BC70-4D3A-9F2C-ADF900983D2C
keywords:
- SampleLevel de función HLSL
topic_type:
- apiref
api_name:
- SampleLevel
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 356e2779d82e886946e93d2071ae693279c07eb8
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104280072"
---
# <a name="samplelevelsamplelevelsfloatfloatuint-function"></a><span data-ttu-id="58f2c-105">SampleLevel:: SampleLevel (S, Float, Float, uint) (función)</span><span class="sxs-lookup"><span data-stu-id="58f2c-105">SampleLevel::SampleLevel(S,float,float,uint) function</span></span>

<span data-ttu-id="58f2c-106">Muestrea una textura en el nivel de mipmap especificado y devuelve el estado de la operación.</span><span class="sxs-lookup"><span data-stu-id="58f2c-106">Samples a texture on the specified mipmap level and returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="58f2c-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="58f2c-107">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleLevel(
  in  SamplerState S,
  in  float        Location,
  in  float        LOD,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="58f2c-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="58f2c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58f2c-109">*S* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="58f2c-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58f2c-110">Tipo: **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="58f2c-110">Type: **SamplerState**</span></span>

<span data-ttu-id="58f2c-111">Un [Estado de muestra](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="58f2c-111">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="58f2c-112">Se trata de un objeto declarado en un archivo de efectos que contiene las asignaciones de estado.</span><span class="sxs-lookup"><span data-stu-id="58f2c-112">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="58f2c-113">*Ubicación* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="58f2c-113">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58f2c-114">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="58f2c-114">Type: **float**</span></span>

<span data-ttu-id="58f2c-115">Las coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="58f2c-115">The texture coordinates.</span></span> <span data-ttu-id="58f2c-116">El tipo de argumento depende del tipo de objeto de textura.</span><span class="sxs-lookup"><span data-stu-id="58f2c-116">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="58f2c-117">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="58f2c-117">Texture-Object Type</span></span>                    | <span data-ttu-id="58f2c-118">Tipo de parámetro</span><span class="sxs-lookup"><span data-stu-id="58f2c-118">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="58f2c-119">Texture1D</span><span class="sxs-lookup"><span data-stu-id="58f2c-119">Texture1D</span></span>                              | <span data-ttu-id="58f2c-120">FLOAT</span><span class="sxs-lookup"><span data-stu-id="58f2c-120">float</span></span>          |
| <span data-ttu-id="58f2c-121">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="58f2c-121">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="58f2c-122">float2</span><span class="sxs-lookup"><span data-stu-id="58f2c-122">float2</span></span>         |
| <span data-ttu-id="58f2c-123">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="58f2c-123">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="58f2c-124">float3</span><span class="sxs-lookup"><span data-stu-id="58f2c-124">float3</span></span>         |
| <span data-ttu-id="58f2c-125">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="58f2c-125">TextureCubeArray</span></span>                       | <span data-ttu-id="58f2c-126">float4</span><span class="sxs-lookup"><span data-stu-id="58f2c-126">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="58f2c-127">*LOD* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="58f2c-127">*LOD* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58f2c-128">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="58f2c-128">Type: **float**</span></span>

<span data-ttu-id="58f2c-129">\[en \] un número que especifica el nivel de mipmap.</span><span class="sxs-lookup"><span data-stu-id="58f2c-129">\[in\] A number that specifies the mipmap level.</span></span> <span data-ttu-id="58f2c-130">Si el valor es ≤ 0, se utiliza el nivel de mipmap 0 (mapa más grande).</span><span class="sxs-lookup"><span data-stu-id="58f2c-130">If the value is ≤ 0, mipmap level 0 (biggest map) is used.</span></span> <span data-ttu-id="58f2c-131">El valor fraccionario (si se proporciona) se usa para interpolar entre dos niveles de mipmap.</span><span class="sxs-lookup"><span data-stu-id="58f2c-131">The fractional value (if supplied) is used to interpolate between two mipmap levels.</span></span>

</dd> <dt>

<span data-ttu-id="58f2c-132">*Estado* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="58f2c-132">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="58f2c-133">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="58f2c-133">Type: **uint**</span></span>

<span data-ttu-id="58f2c-134">Estado de la operación.</span><span class="sxs-lookup"><span data-stu-id="58f2c-134">The status of the operation.</span></span> <span data-ttu-id="58f2c-135">No se puede tener acceso directamente al estado. en su lugar, pase el estado a la función intrínseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="58f2c-135">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="58f2c-136">**CheckAccessFullyMapped** devuelve **true** si todos los valores de la operación de **ejemplo**, **recopilación** o **carga** correspondiente han tenido acceso a los mosaicos asignados en un [recurso en mosaico](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="58f2c-136">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="58f2c-137">Si se tomó algún valor de un mosaico sin asignar, **CheckAccessFullyMapped** devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="58f2c-137">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="58f2c-138">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="58f2c-138">Return value</span></span>

<span data-ttu-id="58f2c-139">Tipo: **[ **\_ formato de DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="58f2c-139">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="58f2c-140">Formato de textura, que es uno de los valores con tipo que aparecen [**en \_ formato de DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="58f2c-140">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="58f2c-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="58f2c-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58f2c-142">Métodos SampleLevel</span><span class="sxs-lookup"><span data-stu-id="58f2c-142">SampleLevel methods</span></span>](texturecubearray-samplelevel.md)
</dt> <dt>

[<span data-ttu-id="58f2c-143">**TextureCubeArray**</span><span class="sxs-lookup"><span data-stu-id="58f2c-143">**TextureCubeArray**</span></span>](texturecubearray.md)
</dt> </dl>

 

 
