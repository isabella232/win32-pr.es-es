---
title: 'TextureCubeArray:: sample (S, Float, Float, uint) (función)'
description: 'Muestrea una textura con un valor opcional para Clamp valores de nivel de detalle (LOD) de ejemplo en y devuelve el estado de la operación. | TextureCubeArray:: sample (S, Float, Float, uint) (función)'
ms.assetid: 5645841D-A32E-452E-873C-E070CF6A4C00
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
ms.openlocfilehash: 24e6d77698507f0d1673b66954db8e78466ac728
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "103820626"
---
# <a name="texturecubearraysamplesfloatfloatuint-function"></a><span data-ttu-id="1ec7c-105">TextureCubeArray:: sample (S, Float, Float, uint) (función)</span><span class="sxs-lookup"><span data-stu-id="1ec7c-105">TextureCubeArray::Sample(S,float,float,uint) function</span></span>

<span data-ttu-id="1ec7c-106">Muestrea una textura con un valor opcional para Clamp valores de nivel de detalle (LOD) de ejemplo en y devuelve el estado de la operación.</span><span class="sxs-lookup"><span data-stu-id="1ec7c-106">Samples a texture with an optional value to clamp sample level-of-detail (LOD) values to, and returns status of the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ec7c-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1ec7c-107">Syntax</span></span>


``` syntax
DXGI_FORMAT Sample(
  in  SamplerState S,
  in  float        Location,
  in  float        Clamp,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="1ec7c-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1ec7c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ec7c-109">*S* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="1ec7c-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ec7c-110">Un [Estado de muestra](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="1ec7c-110">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="1ec7c-111">Se trata de un objeto declarado en un archivo de efectos que contiene las asignaciones de estado.</span><span class="sxs-lookup"><span data-stu-id="1ec7c-111">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="1ec7c-112">*Ubicación* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="1ec7c-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ec7c-113">Las coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="1ec7c-113">The texture coordinates.</span></span> <span data-ttu-id="1ec7c-114">El tipo de argumento depende del tipo de objeto de textura.</span><span class="sxs-lookup"><span data-stu-id="1ec7c-114">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="1ec7c-115">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="1ec7c-115">Texture-Object Type</span></span>                    | <span data-ttu-id="1ec7c-116">Tipo de parámetro</span><span class="sxs-lookup"><span data-stu-id="1ec7c-116">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="1ec7c-117">Texture1D</span><span class="sxs-lookup"><span data-stu-id="1ec7c-117">Texture1D</span></span>                              | <span data-ttu-id="1ec7c-118">FLOAT</span><span class="sxs-lookup"><span data-stu-id="1ec7c-118">float</span></span>          |
| <span data-ttu-id="1ec7c-119">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="1ec7c-119">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="1ec7c-120">float2</span><span class="sxs-lookup"><span data-stu-id="1ec7c-120">float2</span></span>         |
| <span data-ttu-id="1ec7c-121">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="1ec7c-121">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="1ec7c-122">float3</span><span class="sxs-lookup"><span data-stu-id="1ec7c-122">float3</span></span>         |
| <span data-ttu-id="1ec7c-123">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="1ec7c-123">TextureCubeArray</span></span>                       | <span data-ttu-id="1ec7c-124">float4</span><span class="sxs-lookup"><span data-stu-id="1ec7c-124">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="1ec7c-125">*Abrazadera* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1ec7c-125">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ec7c-126">Un valor opcional en el que se van a fijar los valores LOD de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="1ec7c-126">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="1ec7c-127">Por ejemplo, si se pasa 2.0 f para el valor Clamp, se asegura de que ningún ejemplo individual tenga acceso a un nivel de MIP inferior a 2.0 f.</span><span class="sxs-lookup"><span data-stu-id="1ec7c-127">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> <dt>

<span data-ttu-id="1ec7c-128">*Estado* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="1ec7c-128">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1ec7c-129">Estado de la operación.</span><span class="sxs-lookup"><span data-stu-id="1ec7c-129">The status of the operation.</span></span> <span data-ttu-id="1ec7c-130">No se puede tener acceso directamente al estado. en su lugar, pase el estado a la función intrínseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="1ec7c-130">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="1ec7c-131">**CheckAccessFullyMapped** devuelve **true** si todos los valores de la operación de **ejemplo**, **recopilación** o **carga** correspondiente han tenido acceso a los mosaicos asignados en un [recurso en mosaico](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="1ec7c-131">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="1ec7c-132">Si se tomó algún valor de un mosaico sin asignar, **CheckAccessFullyMapped** devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="1ec7c-132">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ec7c-133">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1ec7c-133">Return value</span></span>

<span data-ttu-id="1ec7c-134">Formato de textura, que es uno de los valores con tipo que aparecen [**en \_ formato de DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="1ec7c-134">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="1ec7c-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="1ec7c-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ec7c-136">Métodos de ejemplo</span><span class="sxs-lookup"><span data-stu-id="1ec7c-136">Sample methods</span></span>](texturecubearray-sample.md)
</dt> <dt>

[<span data-ttu-id="1ec7c-137">**TextureCubeArray**</span><span class="sxs-lookup"><span data-stu-id="1ec7c-137">**TextureCubeArray**</span></span>](texturecubearray.md)
</dt> </dl>

 

 
