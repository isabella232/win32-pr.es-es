---
title: ProcessTriTessFactorsMax función)
description: Genera los factores de teselación corregidos para un tri patch. | ProcessTriTessFactorsMax función)
ms.assetid: a24cc1a8-5e6e-4963-b36b-e2265475580e
keywords:
- ProcessTriTessFactorsMax de función HLSL
topic_type:
- apiref
api_name:
- ProcessTriTessFactorsMax
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b5c17fe1dd9f3457a4104178e61af3589ba9f72d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104547563"
---
# <a name="processtritessfactorsmax-function"></a><span data-ttu-id="fc0a3-105">ProcessTriTessFactorsMax función)</span><span class="sxs-lookup"><span data-stu-id="fc0a3-105">ProcessTriTessFactorsMax function</span></span>

<span data-ttu-id="fc0a3-106">Genera los factores de teselación corregidos para un tri patch.</span><span class="sxs-lookup"><span data-stu-id="fc0a3-106">Generates the corrected tessellation factors for a tri patch.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc0a3-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fc0a3-107">Syntax</span></span>

``` syntax
void ProcessTriTessFactorsMax(
  in  float3 RawEdgeFactors,
  in  float InsideScale,
  out float3 RoundedEdgeTessFactors,
  out float RoundedInsideTessFactor,
  out float UnroundedInsideTessFactor
);
```

## <a name="parameters"></a><span data-ttu-id="fc0a3-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fc0a3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc0a3-109">*RawEdgeFactors* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fc0a3-109">*RawEdgeFactors* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc0a3-110">Tipo: **float3**</span><span class="sxs-lookup"><span data-stu-id="fc0a3-110">Type: **float3**</span></span>

<span data-ttu-id="fc0a3-111">Factores de teselación perimetral que se pasan a la fase del teselador.</span><span class="sxs-lookup"><span data-stu-id="fc0a3-111">The edge tessellation factors, passed into the tessellator stage.</span></span>

</dd> <dt>

<span data-ttu-id="fc0a3-112">*InsideScale* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fc0a3-112">*InsideScale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc0a3-113">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="fc0a3-113">Type: **float**</span></span>

<span data-ttu-id="fc0a3-114">Factor de escala aplicado a los factores de teselación de UV calculados por la fase de teselación.</span><span class="sxs-lookup"><span data-stu-id="fc0a3-114">The scale factor applied to the UV tessellation factors computed by the tessellation stage.</span></span> <span data-ttu-id="fc0a3-115">El intervalo permitido para InsideScale es de 0,0 a 1,0.</span><span class="sxs-lookup"><span data-stu-id="fc0a3-115">The allowable range for InsideScale is 0.0 to 1.0.</span></span>

</dd> <dt>

<span data-ttu-id="fc0a3-116">*RoundedEdgeTessFactors* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="fc0a3-116">*RoundedEdgeTessFactors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fc0a3-117">Tipo: **float3**</span><span class="sxs-lookup"><span data-stu-id="fc0a3-117">Type: **float3**</span></span>

<span data-ttu-id="fc0a3-118">Los factores de teselación perimetral redondeados calculados por la fase del teselador.</span><span class="sxs-lookup"><span data-stu-id="fc0a3-118">The rounded edge-tessellation factors calculated by the tessellator stage.</span></span>

</dd> <dt>

<span data-ttu-id="fc0a3-119">*RoundedInsideTessFactor* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="fc0a3-119">*RoundedInsideTessFactor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fc0a3-120">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="fc0a3-120">Type: **float**</span></span>

<span data-ttu-id="fc0a3-121">Los factores de teselación calculados por la fase del teselador y se redondean.</span><span class="sxs-lookup"><span data-stu-id="fc0a3-121">The tessellation factors calculated by the tessellator stage, and rounded.</span></span>

</dd> <dt>

<span data-ttu-id="fc0a3-122">*UnroundedInsideTessFactor* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="fc0a3-122">*UnroundedInsideTessFactor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fc0a3-123">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="fc0a3-123">Type: **float**</span></span>

<span data-ttu-id="fc0a3-124">Los factores de teselación de UV originales, no redondeados calculados por la fase de teselación.</span><span class="sxs-lookup"><span data-stu-id="fc0a3-124">The original, unrounded, UV tessellation factors computed by the tessellation stage.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fc0a3-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fc0a3-125">Return value</span></span>

<span data-ttu-id="fc0a3-126">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="fc0a3-126">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fc0a3-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fc0a3-127">Remarks</span></span>

<span data-ttu-id="fc0a3-128">Genera los factores de teselación corregidos para un tri patch, calculando el factor de teselación interior como el máximo de los factores de teselación perimetral, que se escalan por InsideScale.</span><span class="sxs-lookup"><span data-stu-id="fc0a3-128">Generates the corrected tessellation factors for a tri patch, computing the inside tessellation factor as the maximum of the edge tessellation factors, which is then scaled by InsideScale.</span></span> <span data-ttu-id="fc0a3-129">Después, el resultado se redondea según el modo de partición, pero los resultados no redondeados están disponibles mediante el parámetro UnroundedInsideTessFactor.</span><span class="sxs-lookup"><span data-stu-id="fc0a3-129">The result is then rounded based on the partitioning mode, but the unrounded results are available using the UnroundedInsideTessFactor parameter.</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="fc0a3-130">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="fc0a3-130">Minimum Shader Model</span></span>

<span data-ttu-id="fc0a3-131">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="fc0a3-131">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="fc0a3-132">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="fc0a3-132">Shader Model</span></span>                                                                | <span data-ttu-id="fc0a3-133">Compatible</span><span class="sxs-lookup"><span data-stu-id="fc0a3-133">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="fc0a3-134">Modelos de sombreador [modelo 5](d3d11-graphics-reference-sm5.md) y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="fc0a3-134">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="fc0a3-135">sí</span><span class="sxs-lookup"><span data-stu-id="fc0a3-135">yes</span></span>       |



 

<span data-ttu-id="fc0a3-136">Esta función se admite en los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="fc0a3-136">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="fc0a3-137">Vértice</span><span class="sxs-lookup"><span data-stu-id="fc0a3-137">Vertex</span></span> | <span data-ttu-id="fc0a3-138">Casco</span><span class="sxs-lookup"><span data-stu-id="fc0a3-138">Hull</span></span> | <span data-ttu-id="fc0a3-139">Dominio</span><span class="sxs-lookup"><span data-stu-id="fc0a3-139">Domain</span></span> | <span data-ttu-id="fc0a3-140">Geometría</span><span class="sxs-lookup"><span data-stu-id="fc0a3-140">Geometry</span></span> | <span data-ttu-id="fc0a3-141">Píxel</span><span class="sxs-lookup"><span data-stu-id="fc0a3-141">Pixel</span></span> | <span data-ttu-id="fc0a3-142">Compute</span><span class="sxs-lookup"><span data-stu-id="fc0a3-142">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="fc0a3-143">x</span><span class="sxs-lookup"><span data-stu-id="fc0a3-143">x</span></span>    |        |          |       |         |



 

## <a name="see-also"></a><span data-ttu-id="fc0a3-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="fc0a3-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc0a3-145">Funciones intrínsecas</span><span class="sxs-lookup"><span data-stu-id="fc0a3-145">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="fc0a3-146">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="fc0a3-146">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




