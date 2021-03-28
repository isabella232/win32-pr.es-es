---
title: Process2DQuadTessFactorsMax función)
description: Genera los factores de teselación corregidos para una revisión cuádruple. | Process2DQuadTessFactorsMax función)
ms.assetid: 1de95946-d82d-42ba-93d7-ab8383fd5018
keywords:
- Process2DQuadTessFactorsMax de función HLSL
topic_type:
- apiref
api_name:
- Process2DQuadTessFactorsMax
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d090c102671ec89fa347db95da2b21b5f11adcfe
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104998052"
---
# <a name="process2dquadtessfactorsmax-function"></a><span data-ttu-id="4ce0f-105">Process2DQuadTessFactorsMax función)</span><span class="sxs-lookup"><span data-stu-id="4ce0f-105">Process2DQuadTessFactorsMax function</span></span>

<span data-ttu-id="4ce0f-106">Genera los factores de teselación corregidos para una revisión cuádruple.</span><span class="sxs-lookup"><span data-stu-id="4ce0f-106">Generates the corrected tessellation factors for a quad patch.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ce0f-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4ce0f-107">Syntax</span></span>

``` syntax
void Process2DQuadTessFactorsMax(
  in  float4 RawEdgeFactors,
  in  float2 InsideScale,
  out float4 RoundedEdgeTessFactors,
  out float2 RoundedInsideTessFactors,
  out float2 UnroundedInsideTessFactors
);
```

## <a name="parameters"></a><span data-ttu-id="4ce0f-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4ce0f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4ce0f-109">*RawEdgeFactors* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4ce0f-109">*RawEdgeFactors* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ce0f-110">Tipo: **FLOAT4**</span><span class="sxs-lookup"><span data-stu-id="4ce0f-110">Type: **float4**</span></span>

<span data-ttu-id="4ce0f-111">Factores de teselación perimetral que se pasan a la fase del teselador.</span><span class="sxs-lookup"><span data-stu-id="4ce0f-111">The edge tessellation factors, passed into the tessellator stage.</span></span>

</dd> <dt>

<span data-ttu-id="4ce0f-112">*InsideScale* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4ce0f-112">*InsideScale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ce0f-113">Tipo: **float2**</span><span class="sxs-lookup"><span data-stu-id="4ce0f-113">Type: **float2**</span></span>

<span data-ttu-id="4ce0f-114">Factor de escala aplicado a los factores de teselación de UV calculados por la fase de teselación.</span><span class="sxs-lookup"><span data-stu-id="4ce0f-114">The scale factor applied to the UV tessellation factors computed by the tessellation stage.</span></span> <span data-ttu-id="4ce0f-115">El intervalo permitido para InsideScale es de 0,0 a 1,0.</span><span class="sxs-lookup"><span data-stu-id="4ce0f-115">The allowable range for InsideScale is 0.0 to 1.0.</span></span>

</dd> <dt>

<span data-ttu-id="4ce0f-116">*RoundedEdgeTessFactors* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="4ce0f-116">*RoundedEdgeTessFactors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4ce0f-117">Tipo: **FLOAT4**</span><span class="sxs-lookup"><span data-stu-id="4ce0f-117">Type: **float4**</span></span>

<span data-ttu-id="4ce0f-118">Los factores de teselación perimetral redondeados calculados por la fase del teselador.</span><span class="sxs-lookup"><span data-stu-id="4ce0f-118">The rounded edge-tessellation factors calculated by the tessellator stage.</span></span>

</dd> <dt>

<span data-ttu-id="4ce0f-119">*RoundedInsideTessFactors* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="4ce0f-119">*RoundedInsideTessFactors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4ce0f-120">Tipo: **float2**</span><span class="sxs-lookup"><span data-stu-id="4ce0f-120">Type: **float2**</span></span>

<span data-ttu-id="4ce0f-121">Los factores de teselación redondeados calculados por la fase del teselador para los bordes interiores.</span><span class="sxs-lookup"><span data-stu-id="4ce0f-121">The rounded tessellation factors calculated by the tessellator stage for inside edges.</span></span>

</dd> <dt>

<span data-ttu-id="4ce0f-122">*UnroundedInsideTessFactors* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="4ce0f-122">*UnroundedInsideTessFactors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4ce0f-123">Tipo: **float2**</span><span class="sxs-lookup"><span data-stu-id="4ce0f-123">Type: **float2**</span></span>

<span data-ttu-id="4ce0f-124">Los factores de teselación calculados por la fase del teselador para los bordes interiores.</span><span class="sxs-lookup"><span data-stu-id="4ce0f-124">The tessellation factors calculated by the tessellator stage for inside edges.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4ce0f-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4ce0f-125">Return value</span></span>

<span data-ttu-id="4ce0f-126">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="4ce0f-126">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4ce0f-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4ce0f-127">Remarks</span></span>

<span data-ttu-id="4ce0f-128">Genera los factores de teselación corregidos para una revisión cuádruple, calculando los factores de teselación interiores como el máximo de los factores de teselación perimetral.</span><span class="sxs-lookup"><span data-stu-id="4ce0f-128">Generates the corrected tessellation factors for a quad patch, computing the inside tessellation factors as the maximum of the edge tessellation factors.</span></span> <span data-ttu-id="4ce0f-129">Los factores de teselación de ti y V dentro de se calculan de forma independiente mediante los valores máximos de los lados opuestos del dominio y, a continuación, se escalan por InsideScale.</span><span class="sxs-lookup"><span data-stu-id="4ce0f-129">The U and V inside tessellation factors are computed independently using the maximums of opposing sides of the domain, then are scaled by InsideScale.</span></span> <span data-ttu-id="4ce0f-130">Después, el resultado se redondea según el modo de partición, pero los resultados no redondeados están disponibles mediante el parámetro UnroundedInsideTessFactors.</span><span class="sxs-lookup"><span data-stu-id="4ce0f-130">The result is then rounded based on the partitioning mode, but the unrounded results are available using the UnroundedInsideTessFactors parameter.</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="4ce0f-131">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="4ce0f-131">Minimum Shader Model</span></span>

<span data-ttu-id="4ce0f-132">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="4ce0f-132">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="4ce0f-133">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="4ce0f-133">Shader Model</span></span>                                                                | <span data-ttu-id="4ce0f-134">Compatible</span><span class="sxs-lookup"><span data-stu-id="4ce0f-134">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="4ce0f-135">Modelos de sombreador [modelo 5](d3d11-graphics-reference-sm5.md) y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="4ce0f-135">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="4ce0f-136">sí</span><span class="sxs-lookup"><span data-stu-id="4ce0f-136">yes</span></span>       |



 

<span data-ttu-id="4ce0f-137">Esta función se admite en los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="4ce0f-137">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="4ce0f-138">Vértice</span><span class="sxs-lookup"><span data-stu-id="4ce0f-138">Vertex</span></span> | <span data-ttu-id="4ce0f-139">Casco</span><span class="sxs-lookup"><span data-stu-id="4ce0f-139">Hull</span></span> | <span data-ttu-id="4ce0f-140">Dominio</span><span class="sxs-lookup"><span data-stu-id="4ce0f-140">Domain</span></span> | <span data-ttu-id="4ce0f-141">Geometría</span><span class="sxs-lookup"><span data-stu-id="4ce0f-141">Geometry</span></span> | <span data-ttu-id="4ce0f-142">Píxel</span><span class="sxs-lookup"><span data-stu-id="4ce0f-142">Pixel</span></span> | <span data-ttu-id="4ce0f-143">Compute</span><span class="sxs-lookup"><span data-stu-id="4ce0f-143">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="4ce0f-144">x</span><span class="sxs-lookup"><span data-stu-id="4ce0f-144">x</span></span>    |        |          |       |         |



 

## <a name="see-also"></a><span data-ttu-id="4ce0f-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="4ce0f-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ce0f-146">Funciones intrínsecas</span><span class="sxs-lookup"><span data-stu-id="4ce0f-146">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="4ce0f-147">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="4ce0f-147">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




