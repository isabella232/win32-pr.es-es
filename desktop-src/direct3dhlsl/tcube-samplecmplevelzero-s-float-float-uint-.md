---
title: 'Función SampleCmpLevelZero:: SampleCmpLevelZero (S, Float, Float, uint) para TextureCube'
description: Muestrea solo una textura en el nivel 0 del mipmap y compara el resultado con un valor de comparación. Devuelve el estado de la operación. Para TextureCube.
ms.assetid: FE40307D-B9BE-434F-A6EF-7CA3C5BC7D70
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
ms.openlocfilehash: ff58c51919e575260c71f7b58d8f3d0fda6c1dd1
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/16/2021
ms.locfileid: "104987318"
---
# <a name="samplecmplevelzerosamplecmplevelzerosfloatfloatuint-function-for-texturecube"></a><span data-ttu-id="b13c2-106">Función SampleCmpLevelZero:: SampleCmpLevelZero (S, Float, Float, uint) para TextureCube</span><span class="sxs-lookup"><span data-stu-id="b13c2-106">SampleCmpLevelZero::SampleCmpLevelZero(S,float,float,uint) function for TextureCube</span></span>

<span data-ttu-id="b13c2-107">Muestrea solo una textura en el nivel 0 del mipmap y compara el resultado con un valor de comparación.</span><span class="sxs-lookup"><span data-stu-id="b13c2-107">Samples a texture on mipmap level 0 only and compares the result to a comparison value.</span></span> <span data-ttu-id="b13c2-108">Devuelve el estado de la operación.</span><span class="sxs-lookup"><span data-stu-id="b13c2-108">Returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="b13c2-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b13c2-109">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleCmpLevelZero(
  in  SamplerState S,
  in  float        Location,
  in  float        CompareValue,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="b13c2-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b13c2-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b13c2-111">*S* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="b13c2-111">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b13c2-112">Tipo: **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="b13c2-112">Type: **SamplerState**</span></span>

<span data-ttu-id="b13c2-113">Un [Estado de muestra](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="b13c2-113">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="b13c2-114">Se trata de un objeto declarado en un archivo de efectos que contiene las asignaciones de estado.</span><span class="sxs-lookup"><span data-stu-id="b13c2-114">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="b13c2-115">*Ubicación* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="b13c2-115">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b13c2-116">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="b13c2-116">Type: **float**</span></span>

<span data-ttu-id="b13c2-117">Las coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="b13c2-117">The texture coordinates.</span></span> <span data-ttu-id="b13c2-118">El tipo de argumento depende del tipo de objeto de textura.</span><span class="sxs-lookup"><span data-stu-id="b13c2-118">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="b13c2-119">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="b13c2-119">Texture-Object Type</span></span>                    | <span data-ttu-id="b13c2-120">Tipo de parámetro</span><span class="sxs-lookup"><span data-stu-id="b13c2-120">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="b13c2-121">Texture1D</span><span class="sxs-lookup"><span data-stu-id="b13c2-121">Texture1D</span></span>                              | <span data-ttu-id="b13c2-122">FLOAT</span><span class="sxs-lookup"><span data-stu-id="b13c2-122">float</span></span>          |
| <span data-ttu-id="b13c2-123">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="b13c2-123">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="b13c2-124">float2</span><span class="sxs-lookup"><span data-stu-id="b13c2-124">float2</span></span>         |
| <span data-ttu-id="b13c2-125">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="b13c2-125">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="b13c2-126">float3</span><span class="sxs-lookup"><span data-stu-id="b13c2-126">float3</span></span>         |
| <span data-ttu-id="b13c2-127">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="b13c2-127">TextureCubeArray</span></span>                       | <span data-ttu-id="b13c2-128">float4</span><span class="sxs-lookup"><span data-stu-id="b13c2-128">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="b13c2-129">*CompareValue* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b13c2-129">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b13c2-130">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="b13c2-130">Type: **float**</span></span>

<span data-ttu-id="b13c2-131">Un valor de punto flotante que se va a utilizar como valor de comparación.</span><span class="sxs-lookup"><span data-stu-id="b13c2-131">A floating-point value to use as a comparison value.</span></span>

</dd> <dt>

<span data-ttu-id="b13c2-132">*Estado* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="b13c2-132">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b13c2-133">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="b13c2-133">Type: **uint**</span></span>

<span data-ttu-id="b13c2-134">Estado de la operación.</span><span class="sxs-lookup"><span data-stu-id="b13c2-134">The status of the operation.</span></span> <span data-ttu-id="b13c2-135">No se puede tener acceso directamente al estado. en su lugar, pase el estado a la función intrínseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="b13c2-135">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="b13c2-136">**CheckAccessFullyMapped** devuelve **true** si todos los valores de la operación de **ejemplo**, **recopilación** o **carga** correspondiente han tenido acceso a los mosaicos asignados en un [recurso en mosaico](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="b13c2-136">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="b13c2-137">Si se tomó algún valor de un mosaico sin asignar, **CheckAccessFullyMapped** devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="b13c2-137">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b13c2-138">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b13c2-138">Return value</span></span>

<span data-ttu-id="b13c2-139">Tipo: **[ **\_ formato de DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="b13c2-139">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="b13c2-140">Formato de textura, que es uno de los valores con tipo que aparecen [**en \_ formato de DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="b13c2-140">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="b13c2-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="b13c2-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b13c2-142">Métodos SampleCmpLevelZero</span><span class="sxs-lookup"><span data-stu-id="b13c2-142">SampleCmpLevelZero methods</span></span>](texturecube-samplecmplevelzero.md)
</dt> <dt>

[<span data-ttu-id="b13c2-143">**TextureCube**</span><span class="sxs-lookup"><span data-stu-id="b13c2-143">**TextureCube**</span></span>](texturecube.md)
</dt> </dl>

 

 
