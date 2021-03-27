---
title: 'Función SampleCmp:: SampleCmp (S, Float, Float, Float, uint) para TextureCube'
description: 'Esta función muestrea una textura con un valor de comparación para rechazar muestras, con un valor opcional para Clamp valores de nivel de detalle (LOD) de ejemplo en. | Función SampleCmp:: SampleCmp (S, Float, Float, Float, uint) para TextureCube'
ms.assetid: 050E2856-1E93-4C69-8213-EEC082E82D40
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
ms.openlocfilehash: b73bf86b0c24feae87ea0bb4150d313fff604002
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/16/2021
ms.locfileid: "104987283"
---
# <a name="samplecmpsamplecmpsfloatfloatfloatuint-function-for-texturecube"></a><span data-ttu-id="6983d-105">Función SampleCmp:: SampleCmp (S, Float, Float, Float, uint) para TextureCube</span><span class="sxs-lookup"><span data-stu-id="6983d-105">SampleCmp::SampleCmp(S,float,float,float,uint) function for TextureCube</span></span>

<span data-ttu-id="6983d-106">Muestrea una textura, utilizando un valor de comparación para rechazar muestras, con un valor opcional para Clamp valores de nivel de detalle (LOD) de ejemplo en.</span><span class="sxs-lookup"><span data-stu-id="6983d-106">Samples a texture, using a comparison value to reject samples, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span> <span data-ttu-id="6983d-107">Devuelve el estado de la operación.</span><span class="sxs-lookup"><span data-stu-id="6983d-107">Returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="6983d-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6983d-108">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleCmp(
  in  SamplerState S,
  in  float        Location,
  in  float        CompareValue,
  in  float        Clamp,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="6983d-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6983d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6983d-110">*S* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="6983d-110">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6983d-111">Tipo: **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="6983d-111">Type: **SamplerState**</span></span>

<span data-ttu-id="6983d-112">Un [Estado de muestra](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="6983d-112">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="6983d-113">Se trata de un objeto declarado en un archivo de efectos que contiene las asignaciones de estado.</span><span class="sxs-lookup"><span data-stu-id="6983d-113">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="6983d-114">*Ubicación* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="6983d-114">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6983d-115">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="6983d-115">Type: **float**</span></span>

<span data-ttu-id="6983d-116">Las coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="6983d-116">The texture coordinates.</span></span> <span data-ttu-id="6983d-117">El tipo de argumento depende del tipo de objeto de textura.</span><span class="sxs-lookup"><span data-stu-id="6983d-117">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="6983d-118">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="6983d-118">Texture-Object Type</span></span>                    | <span data-ttu-id="6983d-119">Tipo de parámetro</span><span class="sxs-lookup"><span data-stu-id="6983d-119">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="6983d-120">Texture1D</span><span class="sxs-lookup"><span data-stu-id="6983d-120">Texture1D</span></span>                              | <span data-ttu-id="6983d-121">FLOAT</span><span class="sxs-lookup"><span data-stu-id="6983d-121">float</span></span>          |
| <span data-ttu-id="6983d-122">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="6983d-122">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="6983d-123">float2</span><span class="sxs-lookup"><span data-stu-id="6983d-123">float2</span></span>         |
| <span data-ttu-id="6983d-124">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="6983d-124">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="6983d-125">float3</span><span class="sxs-lookup"><span data-stu-id="6983d-125">float3</span></span>         |
| <span data-ttu-id="6983d-126">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="6983d-126">TextureCubeArray</span></span>                       | <span data-ttu-id="6983d-127">float4</span><span class="sxs-lookup"><span data-stu-id="6983d-127">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="6983d-128">*CompareValue* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6983d-128">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6983d-129">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="6983d-129">Type: **float**</span></span>

<span data-ttu-id="6983d-130">Un valor de punto flotante que se va a utilizar como valor de comparación.</span><span class="sxs-lookup"><span data-stu-id="6983d-130">A floating-point value to use as a comparison value.</span></span>

</dd> <dt>

<span data-ttu-id="6983d-131">*Abrazadera* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6983d-131">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6983d-132">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="6983d-132">Type: **float**</span></span>

<span data-ttu-id="6983d-133">Un valor opcional en el que se van a fijar los valores LOD de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="6983d-133">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="6983d-134">Por ejemplo, si se pasa 2.0 f para el valor Clamp, se asegura de que ningún ejemplo individual tenga acceso a un nivel de MIP inferior a 2.0 f.</span><span class="sxs-lookup"><span data-stu-id="6983d-134">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> <dt>

<span data-ttu-id="6983d-135">*Estado* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="6983d-135">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6983d-136">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="6983d-136">Type: **uint**</span></span>

<span data-ttu-id="6983d-137">Estado de la operación.</span><span class="sxs-lookup"><span data-stu-id="6983d-137">The status of the operation.</span></span> <span data-ttu-id="6983d-138">No se puede tener acceso directamente al estado. en su lugar, pase el estado a la función intrínseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="6983d-138">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="6983d-139">**CheckAccessFullyMapped** devuelve **true** si todos los valores de la operación de **ejemplo**, **recopilación** o **carga** correspondiente han tenido acceso a los mosaicos asignados en un [recurso en mosaico](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="6983d-139">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="6983d-140">Si se tomó algún valor de un mosaico sin asignar, **CheckAccessFullyMapped** devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="6983d-140">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6983d-141">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6983d-141">Return value</span></span>

<span data-ttu-id="6983d-142">Tipo: **[ **\_ formato de DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="6983d-142">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="6983d-143">Formato de textura, que es uno de los valores con tipo que aparecen [**en \_ formato de DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="6983d-143">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="6983d-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="6983d-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6983d-145">Métodos SampleCmp</span><span class="sxs-lookup"><span data-stu-id="6983d-145">SampleCmp methods</span></span>](texturecube-samplecmp.md)
</dt> <dt>

[<span data-ttu-id="6983d-146">**TextureCube**</span><span class="sxs-lookup"><span data-stu-id="6983d-146">**TextureCube**</span></span>](texturecube.md)
</dt> </dl>

 

 
