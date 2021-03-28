---
title: Interbloqueo (función, referencia de HLSL)
description: Realiza una atómica o atómica garantizada.
ms.assetid: ecbe6b2f-8eff-41d7-9ca3-4487c9ffeaf6
keywords:
- HLSL de la función interbloquet
topic_type:
- apiref
api_name:
- InterlockedOr
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 36ab900416d6d04e0e47a843aa345c1a01318c50
ms.sourcegitcommit: 12e9b14501d51641b690ee0cf764e2b91eb9a140
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/06/2020
ms.locfileid: "104997032"
---
# <a name="interlockedor-function-hlsl-reference"></a><span data-ttu-id="7d7b8-104">Interbloqueo (función, referencia de HLSL)</span><span class="sxs-lookup"><span data-stu-id="7d7b8-104">InterlockedOr function (HLSL reference)</span></span>

<span data-ttu-id="7d7b8-105">Realiza una atómica o atómica garantizada.</span><span class="sxs-lookup"><span data-stu-id="7d7b8-105">Performs a guaranteed atomic or.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d7b8-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7d7b8-106">Syntax</span></span>

``` syntax
void InterlockedOr(
  in  R dest,
  in  T value,
  out T original_value
);
```

## <a name="parameters"></a><span data-ttu-id="7d7b8-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7d7b8-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d7b8-108">*dest* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7d7b8-108">*dest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7d7b8-109">Tipo: **R**</span><span class="sxs-lookup"><span data-stu-id="7d7b8-109">Type: **R**</span></span>

<span data-ttu-id="7d7b8-110">Dirección de destino.</span><span class="sxs-lookup"><span data-stu-id="7d7b8-110">The destination address.</span></span>

</dd> <dt>

<span data-ttu-id="7d7b8-111">*valor* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="7d7b8-111">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7d7b8-112">Tipo: **T**</span><span class="sxs-lookup"><span data-stu-id="7d7b8-112">Type: **T**</span></span>

<span data-ttu-id="7d7b8-113">Valor de entrada.</span><span class="sxs-lookup"><span data-stu-id="7d7b8-113">The input value.</span></span>

</dd> <dt>

<span data-ttu-id="7d7b8-114">*\_ valor original* \[ fuera\]</span><span class="sxs-lookup"><span data-stu-id="7d7b8-114">*original\_value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7d7b8-115">Tipo: **T**</span><span class="sxs-lookup"><span data-stu-id="7d7b8-115">Type: **T**</span></span>

<span data-ttu-id="7d7b8-116">Opcional.</span><span class="sxs-lookup"><span data-stu-id="7d7b8-116">Optional.</span></span> <span data-ttu-id="7d7b8-117">Valor de entrada original.</span><span class="sxs-lookup"><span data-stu-id="7d7b8-117">The original input value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7d7b8-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7d7b8-118">Return value</span></span>

<span data-ttu-id="7d7b8-119">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="7d7b8-119">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7d7b8-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7d7b8-120">Remarks</span></span>

<span data-ttu-id="7d7b8-121">Esta operación solo se puede realizar en recursos con tipo int o uint y variables de memoria compartida.</span><span class="sxs-lookup"><span data-stu-id="7d7b8-121">This operation can only be performed on int or uint typed resources and shared memory variables.</span></span> <span data-ttu-id="7d7b8-122">Hay dos usos posibles para esta función.</span><span class="sxs-lookup"><span data-stu-id="7d7b8-122">There are two possible uses for this function.</span></span> <span data-ttu-id="7d7b8-123">El primero es cuando R es un tipo de variable de memoria compartida.</span><span class="sxs-lookup"><span data-stu-id="7d7b8-123">The first is when R is a shared memory variable type.</span></span> <span data-ttu-id="7d7b8-124">En este caso, la función realiza una atomicidad o de valor en el registro de memoria compartida al que hace referencia dest.</span><span class="sxs-lookup"><span data-stu-id="7d7b8-124">In this case, the function performs an atomic or of value to the shared memory register referenced by dest.</span></span> <span data-ttu-id="7d7b8-125">El segundo escenario es cuando R es un tipo de variable de recurso.</span><span class="sxs-lookup"><span data-stu-id="7d7b8-125">The second scenario is when R is a resource variable type.</span></span> <span data-ttu-id="7d7b8-126">En este escenario, la función realiza una atómica o de valor en la ubicación del recurso al que hace referencia dest.</span><span class="sxs-lookup"><span data-stu-id="7d7b8-126">In this scenario, the function performs an atomic or of value to the resource location referenced by dest.</span></span> <span data-ttu-id="7d7b8-127">La función sobrecargada tiene una variable de salida adicional que se establecerá en el valor original de dest.</span><span class="sxs-lookup"><span data-stu-id="7d7b8-127">The overloaded function has an additional output variable which will be set to the original value of dest.</span></span> <span data-ttu-id="7d7b8-128">Esta operación sobrecargada solo está disponible cuando R es legible y grabable.</span><span class="sxs-lookup"><span data-stu-id="7d7b8-128">This overloaded operation is only available when R is readable and writable.</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="7d7b8-129">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="7d7b8-129">Minimum Shader Model</span></span>

<span data-ttu-id="7d7b8-130">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="7d7b8-130">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="7d7b8-131">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="7d7b8-131">Shader Model</span></span>                                                                | <span data-ttu-id="7d7b8-132">Compatible</span><span class="sxs-lookup"><span data-stu-id="7d7b8-132">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="7d7b8-133">Modelos de sombreador [modelo 5](d3d11-graphics-reference-sm5.md) y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="7d7b8-133">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="7d7b8-134">sí</span><span class="sxs-lookup"><span data-stu-id="7d7b8-134">yes</span></span>       |



 

<span data-ttu-id="7d7b8-135">Esta función se admite en los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="7d7b8-135">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="7d7b8-136">Vértice</span><span class="sxs-lookup"><span data-stu-id="7d7b8-136">Vertex</span></span> | <span data-ttu-id="7d7b8-137">Casco</span><span class="sxs-lookup"><span data-stu-id="7d7b8-137">Hull</span></span> | <span data-ttu-id="7d7b8-138">Dominio</span><span class="sxs-lookup"><span data-stu-id="7d7b8-138">Domain</span></span> | <span data-ttu-id="7d7b8-139">Geometría</span><span class="sxs-lookup"><span data-stu-id="7d7b8-139">Geometry</span></span> | <span data-ttu-id="7d7b8-140">Píxel</span><span class="sxs-lookup"><span data-stu-id="7d7b8-140">Pixel</span></span> | <span data-ttu-id="7d7b8-141">Compute</span><span class="sxs-lookup"><span data-stu-id="7d7b8-141">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="7d7b8-142">x</span><span class="sxs-lookup"><span data-stu-id="7d7b8-142">x</span></span>      |  <span data-ttu-id="7d7b8-143">x</span><span class="sxs-lookup"><span data-stu-id="7d7b8-143">x</span></span>   |  <span data-ttu-id="7d7b8-144">x</span><span class="sxs-lookup"><span data-stu-id="7d7b8-144">x</span></span>     |  <span data-ttu-id="7d7b8-145">x</span><span class="sxs-lookup"><span data-stu-id="7d7b8-145">x</span></span>       | <span data-ttu-id="7d7b8-146">x</span><span class="sxs-lookup"><span data-stu-id="7d7b8-146">x</span></span>     | <span data-ttu-id="7d7b8-147">x</span><span class="sxs-lookup"><span data-stu-id="7d7b8-147">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="7d7b8-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="7d7b8-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d7b8-149">Funciones intrínsecas</span><span class="sxs-lookup"><span data-stu-id="7d7b8-149">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="7d7b8-150">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="7d7b8-150">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




