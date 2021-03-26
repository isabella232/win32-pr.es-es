---
title: Función InterlockedAdd (referencia de HLSL)
description: Realiza un agregado atómico garantizado de valor a la variable de recurso dest.
ms.assetid: b3b9cf5c-0da0-4c72-a83f-a0d96f1cac32
keywords:
- InterlockedAdd de función HLSL
topic_type:
- apiref
api_name:
- InterlockedAdd
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1d58965ea47fcad8452979a8c8ffe5b289392850
ms.sourcegitcommit: 12e9b14501d51641b690ee0cf764e2b91eb9a140
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/06/2020
ms.locfileid: "104420154"
---
# <a name="interlockedadd-function-hlsl-reference"></a><span data-ttu-id="2f430-104">Función InterlockedAdd (referencia de HLSL)</span><span class="sxs-lookup"><span data-stu-id="2f430-104">InterlockedAdd function (HLSL reference)</span></span>

<span data-ttu-id="2f430-105">Realiza un agregado atómico garantizado de valor a la variable de recurso dest.</span><span class="sxs-lookup"><span data-stu-id="2f430-105">Performs a guaranteed atomic add of value to the dest resource variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f430-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2f430-106">Syntax</span></span>

``` syntax
void InterlockedAdd(
  in  R dest,
  in  T value,
  out T original_value
);
```

## <a name="parameters"></a><span data-ttu-id="2f430-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2f430-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f430-108">*dest* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2f430-108">*dest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f430-109">Tipo: **R**</span><span class="sxs-lookup"><span data-stu-id="2f430-109">Type: **R**</span></span>

<span data-ttu-id="2f430-110">Dirección de destino.</span><span class="sxs-lookup"><span data-stu-id="2f430-110">The destination address.</span></span>

</dd> <dt>

<span data-ttu-id="2f430-111">*valor* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="2f430-111">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f430-112">Tipo: **T**</span><span class="sxs-lookup"><span data-stu-id="2f430-112">Type: **T**</span></span>

<span data-ttu-id="2f430-113">Valor de entrada.</span><span class="sxs-lookup"><span data-stu-id="2f430-113">The input value.</span></span>

</dd> <dt>

<span data-ttu-id="2f430-114">*\_ valor original* \[ fuera\]</span><span class="sxs-lookup"><span data-stu-id="2f430-114">*original\_value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2f430-115">Tipo: **T**</span><span class="sxs-lookup"><span data-stu-id="2f430-115">Type: **T**</span></span>

<span data-ttu-id="2f430-116">Opcional.</span><span class="sxs-lookup"><span data-stu-id="2f430-116">Optional.</span></span> <span data-ttu-id="2f430-117">Valor de entrada original.</span><span class="sxs-lookup"><span data-stu-id="2f430-117">The original input value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f430-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2f430-118">Return value</span></span>

<span data-ttu-id="2f430-119">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="2f430-119">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2f430-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2f430-120">Remarks</span></span>

<span data-ttu-id="2f430-121">Esta operación solo se puede realizar en recursos con tipo int o uint y variables de memoria compartida.</span><span class="sxs-lookup"><span data-stu-id="2f430-121">This operation can only be performed on int or uint typed resources and shared memory variables.</span></span> <span data-ttu-id="2f430-122">Hay dos usos posibles para esta función.</span><span class="sxs-lookup"><span data-stu-id="2f430-122">There are two possible uses for this function.</span></span> <span data-ttu-id="2f430-123">El primero es cuando R es un tipo de variable de memoria compartida.</span><span class="sxs-lookup"><span data-stu-id="2f430-123">The first is when R is a shared memory variable type.</span></span> <span data-ttu-id="2f430-124">En este caso, la función realiza un agregado atómico de valor al registro de memoria compartida al que hace referencia dest.</span><span class="sxs-lookup"><span data-stu-id="2f430-124">In this case, the function performs an atomic add of value to the shared memory register referenced by dest.</span></span> <span data-ttu-id="2f430-125">El segundo escenario es cuando R es un tipo de variable de recurso.</span><span class="sxs-lookup"><span data-stu-id="2f430-125">The second scenario is when R is a resource variable type.</span></span> <span data-ttu-id="2f430-126">En este escenario, la función realiza un agregado atómico de valor a la ubicación del recurso al que hace referencia dest.</span><span class="sxs-lookup"><span data-stu-id="2f430-126">In this scenario, the function performs an atomic add of value to the resource location referenced by dest.</span></span> <span data-ttu-id="2f430-127">La función sobrecargada tiene una variable de salida adicional que se establecerá en el valor original de dest.</span><span class="sxs-lookup"><span data-stu-id="2f430-127">The overloaded function has an additional output variable which will be set to the original value of dest.</span></span> <span data-ttu-id="2f430-128">Esta operación sobrecargada solo está disponible cuando R es legible y grabable.</span><span class="sxs-lookup"><span data-stu-id="2f430-128">This overloaded operation is only available when R is readable and writable.</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="2f430-129">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="2f430-129">Minimum Shader Model</span></span>

<span data-ttu-id="2f430-130">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="2f430-130">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="2f430-131">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="2f430-131">Shader Model</span></span>                                                                | <span data-ttu-id="2f430-132">Compatible</span><span class="sxs-lookup"><span data-stu-id="2f430-132">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="2f430-133">Modelos de sombreador [modelo 5](d3d11-graphics-reference-sm5.md) y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="2f430-133">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="2f430-134">sí</span><span class="sxs-lookup"><span data-stu-id="2f430-134">yes</span></span>       |



 

<span data-ttu-id="2f430-135">Esta función se admite en los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="2f430-135">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="2f430-136">Vértice</span><span class="sxs-lookup"><span data-stu-id="2f430-136">Vertex</span></span> | <span data-ttu-id="2f430-137">Casco</span><span class="sxs-lookup"><span data-stu-id="2f430-137">Hull</span></span> | <span data-ttu-id="2f430-138">Dominio</span><span class="sxs-lookup"><span data-stu-id="2f430-138">Domain</span></span> | <span data-ttu-id="2f430-139">Geometría</span><span class="sxs-lookup"><span data-stu-id="2f430-139">Geometry</span></span> | <span data-ttu-id="2f430-140">Píxel</span><span class="sxs-lookup"><span data-stu-id="2f430-140">Pixel</span></span> | <span data-ttu-id="2f430-141">Compute</span><span class="sxs-lookup"><span data-stu-id="2f430-141">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="2f430-142">x</span><span class="sxs-lookup"><span data-stu-id="2f430-142">x</span></span>      | <span data-ttu-id="2f430-143">x</span><span class="sxs-lookup"><span data-stu-id="2f430-143">x</span></span>    | <span data-ttu-id="2f430-144">x</span><span class="sxs-lookup"><span data-stu-id="2f430-144">x</span></span>      | <span data-ttu-id="2f430-145">x</span><span class="sxs-lookup"><span data-stu-id="2f430-145">x</span></span>        | <span data-ttu-id="2f430-146">x</span><span class="sxs-lookup"><span data-stu-id="2f430-146">x</span></span>     | <span data-ttu-id="2f430-147">x</span><span class="sxs-lookup"><span data-stu-id="2f430-147">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="2f430-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="2f430-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f430-149">Funciones intrínsecas</span><span class="sxs-lookup"><span data-stu-id="2f430-149">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="2f430-150">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="2f430-150">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




