---
title: 'Texture2DMS:: sample. Operador (función)'
description: 'Recupera un valor del recurso en la ubicación y el índice de ejemplo proporcionados. | Texture2DMS:: sample. Operador (función)'
ms.assetid: 5bc24129-b690-44dd-ae85-8533b10befaa
keywords:
- AdventureWorks. Función de operador HLSL
topic_type:
- apiref
api_name:
- sample.Operator
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1a73577fa67992b212b4769059f1523e584acbaf
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104280187"
---
# <a name="texture2dmssampleoperator----function"></a><span data-ttu-id="2011b-105">Texture2DMS:: sample. Operador (función)</span><span class="sxs-lookup"><span data-stu-id="2011b-105">Texture2DMS::sample.Operator    function</span></span>

<span data-ttu-id="2011b-106">Recupera un valor del recurso en la ubicación y el índice de ejemplo proporcionados.</span><span class="sxs-lookup"><span data-stu-id="2011b-106">Retrieves a value from the resource at the location and sample index provided.</span></span>

## <a name="syntax"></a><span data-ttu-id="2011b-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2011b-107">Syntax</span></span>

``` syntax
R sample.Operator[][](
  in uint sampleSlice,
  in uint2 pos
);
```

## <a name="parameters"></a><span data-ttu-id="2011b-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2011b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2011b-109">*sampleSlice* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2011b-109">*sampleSlice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2011b-110">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="2011b-110">Type: **uint**</span></span>

<span data-ttu-id="2011b-111">Índice del segmento de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="2011b-111">The sample slice index.</span></span>

</dd> <dt>

<span data-ttu-id="2011b-112">*PDV* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="2011b-112">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2011b-113">Tipo: **uint2**</span><span class="sxs-lookup"><span data-stu-id="2011b-113">Type: **uint2**</span></span>

<span data-ttu-id="2011b-114">Posición de índice.</span><span class="sxs-lookup"><span data-stu-id="2011b-114">The index position.</span></span> <span data-ttu-id="2011b-115">Los componentes contienen las coordenadas (x, y).</span><span class="sxs-lookup"><span data-stu-id="2011b-115">The components contain the (x, y) coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2011b-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2011b-116">Return value</span></span>

<span data-ttu-id="2011b-117">Tipo: **R**</span><span class="sxs-lookup"><span data-stu-id="2011b-117">Type: **R**</span></span>

<span data-ttu-id="2011b-118">Variable de recurso de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="2011b-118">A read-only resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="2011b-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2011b-119">Remarks</span></span>

### <a name="usage-example"></a><span data-ttu-id="2011b-120">Ejemplo de uso</span><span class="sxs-lookup"><span data-stu-id="2011b-120">Usage Example</span></span>


```
Texture2DMS<float4, 8> tex;

float4 main( float3 tcoord : texturecoord0 ) : SV_Target
{
     return s_msTexture.sample[2][tcoord];
}
```



<span data-ttu-id="2011b-121">Esta función se admite para los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="2011b-121">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="2011b-122">Vértice</span><span class="sxs-lookup"><span data-stu-id="2011b-122">Vertex</span></span> | <span data-ttu-id="2011b-123">Casco</span><span class="sxs-lookup"><span data-stu-id="2011b-123">Hull</span></span> | <span data-ttu-id="2011b-124">Dominio</span><span class="sxs-lookup"><span data-stu-id="2011b-124">Domain</span></span> | <span data-ttu-id="2011b-125">Geometría</span><span class="sxs-lookup"><span data-stu-id="2011b-125">Geometry</span></span> | <span data-ttu-id="2011b-126">Píxel</span><span class="sxs-lookup"><span data-stu-id="2011b-126">Pixel</span></span> | <span data-ttu-id="2011b-127">Compute</span><span class="sxs-lookup"><span data-stu-id="2011b-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="2011b-128">x</span><span class="sxs-lookup"><span data-stu-id="2011b-128">x</span></span>      | <span data-ttu-id="2011b-129">x</span><span class="sxs-lookup"><span data-stu-id="2011b-129">x</span></span>    | <span data-ttu-id="2011b-130">x</span><span class="sxs-lookup"><span data-stu-id="2011b-130">x</span></span>      | <span data-ttu-id="2011b-131">x</span><span class="sxs-lookup"><span data-stu-id="2011b-131">x</span></span>        | <span data-ttu-id="2011b-132">x</span><span class="sxs-lookup"><span data-stu-id="2011b-132">x</span></span>     | <span data-ttu-id="2011b-133">x</span><span class="sxs-lookup"><span data-stu-id="2011b-133">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="2011b-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="2011b-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2011b-135">Texture2DMS</span><span class="sxs-lookup"><span data-stu-id="2011b-135">Texture2DMS</span></span>](sm5-object-texture2dms.md)
</dt> <dt>

[<span data-ttu-id="2011b-136">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="2011b-136">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




