---
title: ProcessIsolineTessFactors función)
description: Genera los factores de teselación redondeada para un Isoline.
ms.assetid: 0816b3e0-cb03-4a7a-9732-e84c637b3d48
keywords:
- ProcessIsolineTessFactors de función HLSL
topic_type:
- apiref
api_name:
- ProcessIsolineTessFactors
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 10da0e5bf0f2138c57da3fcfe962bc6a88800068
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "103784355"
---
# <a name="processisolinetessfactors-function"></a><span data-ttu-id="314bf-104">ProcessIsolineTessFactors función)</span><span class="sxs-lookup"><span data-stu-id="314bf-104">ProcessIsolineTessFactors function</span></span>

<span data-ttu-id="314bf-105">Genera los factores de teselación redondeada para un Isoline.</span><span class="sxs-lookup"><span data-stu-id="314bf-105">Generates the rounded tessellation factors for an isoline.</span></span>

## <a name="syntax"></a><span data-ttu-id="314bf-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="314bf-106">Syntax</span></span>

``` syntax
void ProcessIsolineTessFactors(
  in  float RawDetailFactor,
  in  float RawDensityFactor,
  out float RoundedDetailFactor,
  out float RoundedDensityFactor
);
```

## <a name="parameters"></a><span data-ttu-id="314bf-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="314bf-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="314bf-108">*RawDetailFactor* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="314bf-108">*RawDetailFactor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="314bf-109">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="314bf-109">Type: **float**</span></span>

<span data-ttu-id="314bf-110">Factor de detalle deseado.</span><span class="sxs-lookup"><span data-stu-id="314bf-110">The desired detail factor.</span></span>

</dd> <dt>

<span data-ttu-id="314bf-111">*RawDensityFactor* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="314bf-111">*RawDensityFactor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="314bf-112">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="314bf-112">Type: **float**</span></span>

<span data-ttu-id="314bf-113">Factor de densidad deseado.</span><span class="sxs-lookup"><span data-stu-id="314bf-113">The desired density factor.</span></span>

</dd> <dt>

<span data-ttu-id="314bf-114">*RoundedDetailFactor* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="314bf-114">*RoundedDetailFactor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="314bf-115">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="314bf-115">Type: **float**</span></span>

<span data-ttu-id="314bf-116">Factor de detalle redondeado con un intervalo que puede usar el del teselador.</span><span class="sxs-lookup"><span data-stu-id="314bf-116">The rounded detail factor clamped to a range that can be used by the tessellator.</span></span>

</dd> <dt>

<span data-ttu-id="314bf-117">*RoundedDensityFactor* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="314bf-117">*RoundedDensityFactor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="314bf-118">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="314bf-118">Type: **float**</span></span>

<span data-ttu-id="314bf-119">El factor de densidad redondeada fijado a un rangethat puede ser utilizado por el del teselador.</span><span class="sxs-lookup"><span data-stu-id="314bf-119">The rounded density factor clamped to a rangethat can be used by the tessellator.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="314bf-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="314bf-120">Return value</span></span>

<span data-ttu-id="314bf-121">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="314bf-121">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="314bf-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="314bf-122">Remarks</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="314bf-123">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="314bf-123">Minimum Shader Model</span></span>

<span data-ttu-id="314bf-124">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="314bf-124">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="314bf-125">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="314bf-125">Shader Model</span></span>                                                                | <span data-ttu-id="314bf-126">Compatible</span><span class="sxs-lookup"><span data-stu-id="314bf-126">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="314bf-127">Modelos de sombreador [modelo 5](d3d11-graphics-reference-sm5.md) y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="314bf-127">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="314bf-128">sí</span><span class="sxs-lookup"><span data-stu-id="314bf-128">yes</span></span>       |



 

<span data-ttu-id="314bf-129">Esta función se admite en los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="314bf-129">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="314bf-130">Vértice</span><span class="sxs-lookup"><span data-stu-id="314bf-130">Vertex</span></span> | <span data-ttu-id="314bf-131">Casco</span><span class="sxs-lookup"><span data-stu-id="314bf-131">Hull</span></span> | <span data-ttu-id="314bf-132">Dominio</span><span class="sxs-lookup"><span data-stu-id="314bf-132">Domain</span></span> | <span data-ttu-id="314bf-133">Geometría</span><span class="sxs-lookup"><span data-stu-id="314bf-133">Geometry</span></span> | <span data-ttu-id="314bf-134">Píxel</span><span class="sxs-lookup"><span data-stu-id="314bf-134">Pixel</span></span> | <span data-ttu-id="314bf-135">Compute</span><span class="sxs-lookup"><span data-stu-id="314bf-135">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="314bf-136">x</span><span class="sxs-lookup"><span data-stu-id="314bf-136">x</span></span>    |        |          |       |         |



 

## <a name="see-also"></a><span data-ttu-id="314bf-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="314bf-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="314bf-138">Funciones intrínsecas</span><span class="sxs-lookup"><span data-stu-id="314bf-138">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="314bf-139">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="314bf-139">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




