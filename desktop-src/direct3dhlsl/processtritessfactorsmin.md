---
title: ProcessTriTessFactorsMin función)
description: Genera los factores de teselación corregidos para un tri patch. | ProcessTriTessFactorsMin función)
ms.assetid: fa1e19c2-fadf-42d4-9574-834eaf871393
keywords:
- ProcessTriTessFactorsMin de función HLSL
topic_type:
- apiref
api_name:
- ProcessTriTessFactorsMin
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 33f82c7935d47813d833ccc21a7ec0134adee1cc
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104547558"
---
# <a name="processtritessfactorsmin-function"></a><span data-ttu-id="9feeb-105">ProcessTriTessFactorsMin función)</span><span class="sxs-lookup"><span data-stu-id="9feeb-105">ProcessTriTessFactorsMin function</span></span>

<span data-ttu-id="9feeb-106">Genera los factores de teselación corregidos para un tri patch.</span><span class="sxs-lookup"><span data-stu-id="9feeb-106">Generates the corrected tessellation factors for a tri patch.</span></span>

## <a name="syntax"></a><span data-ttu-id="9feeb-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9feeb-107">Syntax</span></span>

``` syntax
void ProcessTriTessFactorsMin(
  in  float3 RawEdgeFactors,
  in  float InsideScale,
  out float3 RoundedEdgeTessFactors,
  out float RoundedInsideTessFactors,
  out float UnroundedInsideTessFactors
);
```

## <a name="parameters"></a><span data-ttu-id="9feeb-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9feeb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9feeb-109">*RawEdgeFactors* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9feeb-109">*RawEdgeFactors* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9feeb-110">Tipo: **float3**</span><span class="sxs-lookup"><span data-stu-id="9feeb-110">Type: **float3**</span></span>

<span data-ttu-id="9feeb-111">Factores de teselación perimetral que se pasan a la fase del teselador.</span><span class="sxs-lookup"><span data-stu-id="9feeb-111">The edge tessellation factors, passed into the tessellator stage.</span></span>

</dd> <dt>

<span data-ttu-id="9feeb-112">*InsideScale* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9feeb-112">*InsideScale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9feeb-113">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="9feeb-113">Type: **float**</span></span>

<span data-ttu-id="9feeb-114">Factor de escala aplicado a los factores de teselación de UV calculados por la fase de teselación.</span><span class="sxs-lookup"><span data-stu-id="9feeb-114">The scale factor applied to the UV tessellation factors computed by the tessellation stage.</span></span> <span data-ttu-id="9feeb-115">El intervalo permitido para InsideScale es de 0,0 a 1,0.</span><span class="sxs-lookup"><span data-stu-id="9feeb-115">The allowable range for InsideScale is 0.0 to 1.0.</span></span>

</dd> <dt>

<span data-ttu-id="9feeb-116">*RoundedEdgeTessFactors* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="9feeb-116">*RoundedEdgeTessFactors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9feeb-117">Tipo: **float3**</span><span class="sxs-lookup"><span data-stu-id="9feeb-117">Type: **float3**</span></span>

<span data-ttu-id="9feeb-118">Los factores de teselación perimetral redondeados calculados por la fase del teselador.</span><span class="sxs-lookup"><span data-stu-id="9feeb-118">The rounded edge-tessellation factors calculated by the tessellator stage.</span></span>

</dd> <dt>

<span data-ttu-id="9feeb-119">*RoundedInsideTessFactors* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="9feeb-119">*RoundedInsideTessFactors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9feeb-120">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="9feeb-120">Type: **float**</span></span>

<span data-ttu-id="9feeb-121">Los factores de teselación redondeados calculados por la fase del teselador para los bordes interiores.</span><span class="sxs-lookup"><span data-stu-id="9feeb-121">The rounded tessellation factors calculated by the tessellator stage for inside edges.</span></span>

</dd> <dt>

<span data-ttu-id="9feeb-122">*UnroundedInsideTessFactors* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="9feeb-122">*UnroundedInsideTessFactors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9feeb-123">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="9feeb-123">Type: **float**</span></span>

<span data-ttu-id="9feeb-124">Los factores de teselación calculados por la fase del teselador para los bordes interiores.</span><span class="sxs-lookup"><span data-stu-id="9feeb-124">The tessellation factors calculated by the tessellator stage for inside edges.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9feeb-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9feeb-125">Return value</span></span>

<span data-ttu-id="9feeb-126">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="9feeb-126">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9feeb-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9feeb-127">Remarks</span></span>

<span data-ttu-id="9feeb-128">Genera los factores de teselación corregidos para un tri patch, calculando el factor de teselación interior como el mínimo de los factores de teselación perimetral, que se escalan por InsideScale.</span><span class="sxs-lookup"><span data-stu-id="9feeb-128">Generates the corrected tessellation factors for a tri patch, computing the inside tessellation factor as the minimum of the edge tessellation factors, which is then scaled by InsideScale.</span></span> <span data-ttu-id="9feeb-129">Después, el resultado se redondea según el modo de partición, pero los resultados no redondeados están disponibles mediante el parámetro UnroundedInsideTessFactor.</span><span class="sxs-lookup"><span data-stu-id="9feeb-129">The result is then rounded based on the partitioning mode, but the unrounded results are available using the UnroundedInsideTessFactor parameter.</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="9feeb-130">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="9feeb-130">Minimum Shader Model</span></span>

<span data-ttu-id="9feeb-131">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="9feeb-131">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="9feeb-132">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="9feeb-132">Shader Model</span></span>                                                                | <span data-ttu-id="9feeb-133">Compatible</span><span class="sxs-lookup"><span data-stu-id="9feeb-133">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="9feeb-134">Modelos de sombreador [modelo 5](d3d11-graphics-reference-sm5.md) y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="9feeb-134">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="9feeb-135">sí</span><span class="sxs-lookup"><span data-stu-id="9feeb-135">yes</span></span>       |



 

<span data-ttu-id="9feeb-136">Esta función se admite en los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="9feeb-136">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="9feeb-137">Vértice</span><span class="sxs-lookup"><span data-stu-id="9feeb-137">Vertex</span></span> | <span data-ttu-id="9feeb-138">Casco</span><span class="sxs-lookup"><span data-stu-id="9feeb-138">Hull</span></span> | <span data-ttu-id="9feeb-139">Dominio</span><span class="sxs-lookup"><span data-stu-id="9feeb-139">Domain</span></span> | <span data-ttu-id="9feeb-140">Geometría</span><span class="sxs-lookup"><span data-stu-id="9feeb-140">Geometry</span></span> | <span data-ttu-id="9feeb-141">Píxel</span><span class="sxs-lookup"><span data-stu-id="9feeb-141">Pixel</span></span> | <span data-ttu-id="9feeb-142">Compute</span><span class="sxs-lookup"><span data-stu-id="9feeb-142">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="9feeb-143">x</span><span class="sxs-lookup"><span data-stu-id="9feeb-143">x</span></span>    |        |          |       |         |



 

## <a name="see-also"></a><span data-ttu-id="9feeb-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="9feeb-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9feeb-145">Funciones intrínsecas</span><span class="sxs-lookup"><span data-stu-id="9feeb-145">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="9feeb-146">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="9feeb-146">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




