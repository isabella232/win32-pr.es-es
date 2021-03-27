---
title: EvaluateAttributeAtSample función)
description: Evalúa en la ubicación de ejemplo indizada.
ms.assetid: b5886004-5960-461d-a0d2-f4c3b0d09d94
keywords:
- EvaluateAttributeAtSample de función HLSL
topic_type:
- apiref
api_name:
- EvaluateAttributeAtSample
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b183f86599d08a6892e33c169b938dc09a2b55de
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "103783677"
---
# <a name="evaluateattributeatsample-function"></a><span data-ttu-id="1026b-104">EvaluateAttributeAtSample función)</span><span class="sxs-lookup"><span data-stu-id="1026b-104">EvaluateAttributeAtSample function</span></span>

<span data-ttu-id="1026b-105">Evalúa en la ubicación de ejemplo indizada.</span><span class="sxs-lookup"><span data-stu-id="1026b-105">Evaluates at the indexed sample location.</span></span>

## <a name="syntax"></a><span data-ttu-id="1026b-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1026b-106">Syntax</span></span>

``` syntax
numeric EvaluateAttributeAtSample(
  in attrib numeric value,
  in uint sampleindex
);
```

## <a name="parameters"></a><span data-ttu-id="1026b-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1026b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1026b-108">*valor* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="1026b-108">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1026b-109">Tipo: **attrib Numeric**</span><span class="sxs-lookup"><span data-stu-id="1026b-109">Type: **attrib numeric**</span></span>

<span data-ttu-id="1026b-110">Valor de entrada.</span><span class="sxs-lookup"><span data-stu-id="1026b-110">The input value.</span></span>

</dd> <dt>

<span data-ttu-id="1026b-111">*sampleindex* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1026b-111">*sampleindex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1026b-112">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="1026b-112">Type: **uint**</span></span>

<span data-ttu-id="1026b-113">Ubicación de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="1026b-113">The sample location.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1026b-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1026b-114">Remarks</span></span>

<span data-ttu-id="1026b-115">El modo de interpolación puede ser **lineal** o **lineal \_ sin \_ perspectiva** en la variable.</span><span class="sxs-lookup"><span data-stu-id="1026b-115">Interpolation mode can be **linear** or **linear\_no\_perspective** on the variable.</span></span> <span data-ttu-id="1026b-116">Se omite el uso de **centroide** o **Sample** .</span><span class="sxs-lookup"><span data-stu-id="1026b-116">Use of **centroid** or **sample** is ignored.</span></span> <span data-ttu-id="1026b-117">También se permiten atributos con interpolación constante, en cuyo caso se omite el índice de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="1026b-117">Attributes with constant interpolation are also allowed, in which case the sample index is ignored.</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="1026b-118">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="1026b-118">Minimum Shader Model</span></span>

<span data-ttu-id="1026b-119">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="1026b-119">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="1026b-120">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="1026b-120">Shader Model</span></span>                                                                | <span data-ttu-id="1026b-121">Compatible</span><span class="sxs-lookup"><span data-stu-id="1026b-121">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="1026b-122">Modelos de sombreador [modelo 5](d3d11-graphics-reference-sm5.md) y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="1026b-122">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="1026b-123">sí</span><span class="sxs-lookup"><span data-stu-id="1026b-123">yes</span></span>       |



 

<span data-ttu-id="1026b-124">Esta función se admite en los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="1026b-124">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="1026b-125">Vértice</span><span class="sxs-lookup"><span data-stu-id="1026b-125">Vertex</span></span> | <span data-ttu-id="1026b-126">Casco</span><span class="sxs-lookup"><span data-stu-id="1026b-126">Hull</span></span> | <span data-ttu-id="1026b-127">Dominio</span><span class="sxs-lookup"><span data-stu-id="1026b-127">Domain</span></span> | <span data-ttu-id="1026b-128">Geometría</span><span class="sxs-lookup"><span data-stu-id="1026b-128">Geometry</span></span> | <span data-ttu-id="1026b-129">Píxel</span><span class="sxs-lookup"><span data-stu-id="1026b-129">Pixel</span></span> | <span data-ttu-id="1026b-130">Compute</span><span class="sxs-lookup"><span data-stu-id="1026b-130">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="1026b-131">x</span><span class="sxs-lookup"><span data-stu-id="1026b-131">x</span></span>     |         |



 

## <a name="see-also"></a><span data-ttu-id="1026b-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="1026b-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1026b-133">Funciones intrínsecas</span><span class="sxs-lookup"><span data-stu-id="1026b-133">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="1026b-134">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="1026b-134">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




