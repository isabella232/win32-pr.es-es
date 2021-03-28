---
title: Función InterlockedMax (referencia de HLSL)
description: Realiza un máximo atómico garantizado.
ms.assetid: ea2c67ef-3133-424d-9cc3-81da79aee87e
keywords:
- InterlockedMax de función HLSL
topic_type:
- apiref
api_name:
- InterlockedMax
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 997641b086625532b99e3ae8d17be49cd71ae21f
ms.sourcegitcommit: 12e9b14501d51641b690ee0cf764e2b91eb9a140
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/06/2020
ms.locfileid: "104420157"
---
# <a name="interlockedmax-function-hlsl-reference"></a><span data-ttu-id="c7f2b-104">Función InterlockedMax (referencia de HLSL)</span><span class="sxs-lookup"><span data-stu-id="c7f2b-104">InterlockedMax function (HLSL reference)</span></span>

<span data-ttu-id="c7f2b-105">Realiza un máximo atómico garantizado.</span><span class="sxs-lookup"><span data-stu-id="c7f2b-105">Performs a guaranteed atomic max.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7f2b-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c7f2b-106">Syntax</span></span>

``` syntax
void InterlockedMax(
  in  R dest,
  in  T value,
  out T original_value
);
```

## <a name="parameters"></a><span data-ttu-id="c7f2b-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c7f2b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7f2b-108">*dest* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c7f2b-108">*dest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7f2b-109">Tipo: **R**</span><span class="sxs-lookup"><span data-stu-id="c7f2b-109">Type: **R**</span></span>

<span data-ttu-id="c7f2b-110">Dirección de destino.</span><span class="sxs-lookup"><span data-stu-id="c7f2b-110">The destination address.</span></span>

</dd> <dt>

<span data-ttu-id="c7f2b-111">*valor* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="c7f2b-111">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7f2b-112">Tipo: **T**</span><span class="sxs-lookup"><span data-stu-id="c7f2b-112">Type: **T**</span></span>

<span data-ttu-id="c7f2b-113">Valor de entrada.</span><span class="sxs-lookup"><span data-stu-id="c7f2b-113">The input value.</span></span>

</dd> <dt>

<span data-ttu-id="c7f2b-114">*\_ valor original* \[ fuera\]</span><span class="sxs-lookup"><span data-stu-id="c7f2b-114">*original\_value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c7f2b-115">Tipo: **T**</span><span class="sxs-lookup"><span data-stu-id="c7f2b-115">Type: **T**</span></span>

<span data-ttu-id="c7f2b-116">Opcional.</span><span class="sxs-lookup"><span data-stu-id="c7f2b-116">Optional.</span></span> <span data-ttu-id="c7f2b-117">Valor de entrada original.</span><span class="sxs-lookup"><span data-stu-id="c7f2b-117">The original input value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7f2b-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c7f2b-118">Return value</span></span>

<span data-ttu-id="c7f2b-119">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="c7f2b-119">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c7f2b-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c7f2b-120">Remarks</span></span>

<span data-ttu-id="c7f2b-121">Esta operación solo se puede realizar en los recursos con tipo int y uint y las variables de memoria compartida.</span><span class="sxs-lookup"><span data-stu-id="c7f2b-121">This operation can only be performed on int and uint typed resources and shared memory variables.</span></span> <span data-ttu-id="c7f2b-122">Hay dos usos posibles para esta función.</span><span class="sxs-lookup"><span data-stu-id="c7f2b-122">There are two possible uses for this function.</span></span> <span data-ttu-id="c7f2b-123">El primero es cuando R es un tipo de variable de memoria compartida.</span><span class="sxs-lookup"><span data-stu-id="c7f2b-123">The first is when R is a shared memory variable type.</span></span> <span data-ttu-id="c7f2b-124">En este caso, la función realiza un valor máximo atómico del valor en el registro de memoria compartida al que hace referencia dest.</span><span class="sxs-lookup"><span data-stu-id="c7f2b-124">In this case, the function performs an atomic max of value to the shared memory register referenced by dest.</span></span> <span data-ttu-id="c7f2b-125">El segundo escenario es cuando R es un tipo de variable de recurso.</span><span class="sxs-lookup"><span data-stu-id="c7f2b-125">The second scenario is when R is a resource variable type.</span></span> <span data-ttu-id="c7f2b-126">En este escenario, la función realiza un máximo atómico de valor en la ubicación del recurso al que hace referencia dest.</span><span class="sxs-lookup"><span data-stu-id="c7f2b-126">In this scenario, the function performs an atomic max of value to the resource location referenced by dest.</span></span> <span data-ttu-id="c7f2b-127">La función sobrecargada tiene una variable de salida adicional que se establecerá en el valor original de dest.</span><span class="sxs-lookup"><span data-stu-id="c7f2b-127">The overloaded function has an additional output variable which will be set to the original value of dest.</span></span> <span data-ttu-id="c7f2b-128">Esta operación sobrecargada solo está disponible cuando R es legible y grabable.</span><span class="sxs-lookup"><span data-stu-id="c7f2b-128">This overloaded operation is only available when R is readable and writable.</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="c7f2b-129">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="c7f2b-129">Minimum Shader Model</span></span>

<span data-ttu-id="c7f2b-130">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="c7f2b-130">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="c7f2b-131">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="c7f2b-131">Shader Model</span></span>                                                                | <span data-ttu-id="c7f2b-132">Compatible</span><span class="sxs-lookup"><span data-stu-id="c7f2b-132">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="c7f2b-133">Modelos de sombreador [modelo 5](d3d11-graphics-reference-sm5.md) y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="c7f2b-133">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="c7f2b-134">sí</span><span class="sxs-lookup"><span data-stu-id="c7f2b-134">yes</span></span>       |



 

<span data-ttu-id="c7f2b-135">Esta función se admite en los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="c7f2b-135">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="c7f2b-136">Vértice</span><span class="sxs-lookup"><span data-stu-id="c7f2b-136">Vertex</span></span> | <span data-ttu-id="c7f2b-137">Casco</span><span class="sxs-lookup"><span data-stu-id="c7f2b-137">Hull</span></span> | <span data-ttu-id="c7f2b-138">Dominio</span><span class="sxs-lookup"><span data-stu-id="c7f2b-138">Domain</span></span> | <span data-ttu-id="c7f2b-139">Geometría</span><span class="sxs-lookup"><span data-stu-id="c7f2b-139">Geometry</span></span> | <span data-ttu-id="c7f2b-140">Píxel</span><span class="sxs-lookup"><span data-stu-id="c7f2b-140">Pixel</span></span> | <span data-ttu-id="c7f2b-141">Compute</span><span class="sxs-lookup"><span data-stu-id="c7f2b-141">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="c7f2b-142">x</span><span class="sxs-lookup"><span data-stu-id="c7f2b-142">x</span></span>      |  <span data-ttu-id="c7f2b-143">x</span><span class="sxs-lookup"><span data-stu-id="c7f2b-143">x</span></span>   |  <span data-ttu-id="c7f2b-144">x</span><span class="sxs-lookup"><span data-stu-id="c7f2b-144">x</span></span>     |  <span data-ttu-id="c7f2b-145">x</span><span class="sxs-lookup"><span data-stu-id="c7f2b-145">x</span></span>       | <span data-ttu-id="c7f2b-146">x</span><span class="sxs-lookup"><span data-stu-id="c7f2b-146">x</span></span>     | <span data-ttu-id="c7f2b-147">x</span><span class="sxs-lookup"><span data-stu-id="c7f2b-147">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="c7f2b-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="c7f2b-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7f2b-149">Funciones intrínsecas</span><span class="sxs-lookup"><span data-stu-id="c7f2b-149">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="c7f2b-150">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="c7f2b-150">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




