---
title: countbits (función)
description: Cuenta el número de bits (por componente) establecido en el entero de entrada.
ms.assetid: c4fafbc8-e21c-48cb-b433-8241a989ec85
keywords:
- función countbits HLSL
topic_type:
- apiref
api_name:
- countbits
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 357aceca6e2aea261a9e94212b58ff6308c99560
ms.sourcegitcommit: 435ea8f5bf06808ffa7dce39afb0ee6de842ba2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2021
ms.locfileid: "107925628"
---
# <a name="countbits-function"></a><span data-ttu-id="236e9-104">countbits (función)</span><span class="sxs-lookup"><span data-stu-id="236e9-104">countbits function</span></span>

<span data-ttu-id="236e9-105">Cuenta el número de bits (por componente) establecido en el entero de entrada.</span><span class="sxs-lookup"><span data-stu-id="236e9-105">Counts the number of bits (per component) set in the input integer.</span></span>

## <a name="syntax"></a><span data-ttu-id="236e9-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="236e9-106">Syntax</span></span>

``` syntax
uint countbits(
  in uint value
);
```

## <a name="parameters"></a><span data-ttu-id="236e9-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="236e9-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="236e9-108">*value* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="236e9-108">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="236e9-109">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="236e9-109">Type: **uint**</span></span>

<span data-ttu-id="236e9-110">Valor de entrada.</span><span class="sxs-lookup"><span data-stu-id="236e9-110">The input value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="236e9-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="236e9-111">Return value</span></span>

<span data-ttu-id="236e9-112">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="236e9-112">Type: **uint**</span></span>

<span data-ttu-id="236e9-113">Número de bits.</span><span class="sxs-lookup"><span data-stu-id="236e9-113">The number of bits.</span></span>

## <a name="remarks"></a><span data-ttu-id="236e9-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="236e9-114">Remarks</span></span>

<span data-ttu-id="236e9-115">También están disponibles las siguientes versiones sobrecargadas:</span><span class="sxs-lookup"><span data-stu-id="236e9-115">The following overloaded versions are also available:</span></span>

``` syntax
uint count_bits(uint value);
uint2 count_bits(uint2 value);
uint3 count_bits(uint3 value);
uint4 count_bits(uint4 value);
```

### <a name="minimum-shader-model"></a><span data-ttu-id="236e9-116">Modelo mínimo de sombreador</span><span class="sxs-lookup"><span data-stu-id="236e9-116">Minimum Shader Model</span></span>

<span data-ttu-id="236e9-117">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="236e9-117">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="236e9-118">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="236e9-118">Shader Model</span></span>                                                                | <span data-ttu-id="236e9-119">Compatible</span><span class="sxs-lookup"><span data-stu-id="236e9-119">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="236e9-120">[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md) y modelos de sombreador posteriores</span><span class="sxs-lookup"><span data-stu-id="236e9-120">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="236e9-121">sí</span><span class="sxs-lookup"><span data-stu-id="236e9-121">yes</span></span>       |



 

<span data-ttu-id="236e9-122">Esta función se admite en los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="236e9-122">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="236e9-123">Vértice</span><span class="sxs-lookup"><span data-stu-id="236e9-123">Vertex</span></span> | <span data-ttu-id="236e9-124">Casco</span><span class="sxs-lookup"><span data-stu-id="236e9-124">Hull</span></span> | <span data-ttu-id="236e9-125">Domain</span><span class="sxs-lookup"><span data-stu-id="236e9-125">Domain</span></span> | <span data-ttu-id="236e9-126">Geometría</span><span class="sxs-lookup"><span data-stu-id="236e9-126">Geometry</span></span> | <span data-ttu-id="236e9-127">Píxel</span><span class="sxs-lookup"><span data-stu-id="236e9-127">Pixel</span></span> | <span data-ttu-id="236e9-128">Proceso</span><span class="sxs-lookup"><span data-stu-id="236e9-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="236e9-129">x</span><span class="sxs-lookup"><span data-stu-id="236e9-129">x</span></span>      | <span data-ttu-id="236e9-130">x</span><span class="sxs-lookup"><span data-stu-id="236e9-130">x</span></span>    | <span data-ttu-id="236e9-131">x</span><span class="sxs-lookup"><span data-stu-id="236e9-131">x</span></span>      | <span data-ttu-id="236e9-132">x</span><span class="sxs-lookup"><span data-stu-id="236e9-132">x</span></span>        | <span data-ttu-id="236e9-133">x</span><span class="sxs-lookup"><span data-stu-id="236e9-133">x</span></span>     | <span data-ttu-id="236e9-134">x</span><span class="sxs-lookup"><span data-stu-id="236e9-134">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="236e9-135">Consulte también</span><span class="sxs-lookup"><span data-stu-id="236e9-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="236e9-136">Funciones intrínsecas</span><span class="sxs-lookup"><span data-stu-id="236e9-136">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="236e9-137">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="236e9-137">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




