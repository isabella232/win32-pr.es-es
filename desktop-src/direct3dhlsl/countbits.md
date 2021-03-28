---
title: countbits (función)
description: Cuenta el número de bits (por componente) en el entero de entrada.
ms.assetid: c4fafbc8-e21c-48cb-b433-8241a989ec85
keywords:
- countbits (de función HLSL
topic_type:
- apiref
api_name:
- countbits
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 60d3cd63502c6217e6fb0b0ff17685b2d2b5bf25
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104076884"
---
# <a name="countbits-function"></a><span data-ttu-id="d5038-104">countbits (función)</span><span class="sxs-lookup"><span data-stu-id="d5038-104">countbits function</span></span>

<span data-ttu-id="d5038-105">Cuenta el número de bits (por componente) en el entero de entrada.</span><span class="sxs-lookup"><span data-stu-id="d5038-105">Counts the number of bits (per component) in the input integer.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5038-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d5038-106">Syntax</span></span>

``` syntax
uint countbits(
  in uint value
);
```

## <a name="parameters"></a><span data-ttu-id="d5038-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d5038-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5038-108">*valor* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="d5038-108">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5038-109">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="d5038-109">Type: **uint**</span></span>

<span data-ttu-id="d5038-110">Valor de entrada.</span><span class="sxs-lookup"><span data-stu-id="d5038-110">The input value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5038-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d5038-111">Return value</span></span>

<span data-ttu-id="d5038-112">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="d5038-112">Type: **uint**</span></span>

<span data-ttu-id="d5038-113">Número de bits.</span><span class="sxs-lookup"><span data-stu-id="d5038-113">The number of bits.</span></span>

## <a name="remarks"></a><span data-ttu-id="d5038-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d5038-114">Remarks</span></span>

<span data-ttu-id="d5038-115">También están disponibles las siguientes versiones sobrecargadas:</span><span class="sxs-lookup"><span data-stu-id="d5038-115">The following overloaded versions are also available:</span></span>

``` syntax
uint count_bits(uint value);
uint2 count_bits(uint2 value);
uint3 count_bits(uint3 value);
uint4 count_bits(uint4 value);
```

### <a name="minimum-shader-model"></a><span data-ttu-id="d5038-116">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="d5038-116">Minimum Shader Model</span></span>

<span data-ttu-id="d5038-117">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="d5038-117">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="d5038-118">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="d5038-118">Shader Model</span></span>                                                                | <span data-ttu-id="d5038-119">Compatible</span><span class="sxs-lookup"><span data-stu-id="d5038-119">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="d5038-120">Modelos de sombreador [modelo 5](d3d11-graphics-reference-sm5.md) y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="d5038-120">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="d5038-121">sí</span><span class="sxs-lookup"><span data-stu-id="d5038-121">yes</span></span>       |



 

<span data-ttu-id="d5038-122">Esta función se admite en los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="d5038-122">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="d5038-123">Vértice</span><span class="sxs-lookup"><span data-stu-id="d5038-123">Vertex</span></span> | <span data-ttu-id="d5038-124">Casco</span><span class="sxs-lookup"><span data-stu-id="d5038-124">Hull</span></span> | <span data-ttu-id="d5038-125">Dominio</span><span class="sxs-lookup"><span data-stu-id="d5038-125">Domain</span></span> | <span data-ttu-id="d5038-126">Geometría</span><span class="sxs-lookup"><span data-stu-id="d5038-126">Geometry</span></span> | <span data-ttu-id="d5038-127">Píxel</span><span class="sxs-lookup"><span data-stu-id="d5038-127">Pixel</span></span> | <span data-ttu-id="d5038-128">Compute</span><span class="sxs-lookup"><span data-stu-id="d5038-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="d5038-129">x</span><span class="sxs-lookup"><span data-stu-id="d5038-129">x</span></span>      | <span data-ttu-id="d5038-130">x</span><span class="sxs-lookup"><span data-stu-id="d5038-130">x</span></span>    | <span data-ttu-id="d5038-131">x</span><span class="sxs-lookup"><span data-stu-id="d5038-131">x</span></span>      | <span data-ttu-id="d5038-132">x</span><span class="sxs-lookup"><span data-stu-id="d5038-132">x</span></span>        | <span data-ttu-id="d5038-133">x</span><span class="sxs-lookup"><span data-stu-id="d5038-133">x</span></span>     | <span data-ttu-id="d5038-134">x</span><span class="sxs-lookup"><span data-stu-id="d5038-134">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="d5038-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="d5038-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5038-136">Funciones intrínsecas</span><span class="sxs-lookup"><span data-stu-id="d5038-136">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="d5038-137">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="d5038-137">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




