---
title: Función InterlockedExchange (referencia de HLSL)
description: Asigna Value a dest y devuelve el valor original.
ms.assetid: 1e7ce7ff-9e23-47fa-8e76-713f6bf57abf
keywords:
- InterlockedExchange de función HLSL
topic_type:
- apiref
api_name:
- InterlockedExchange
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7c39dc4f68429fa3f070d446f998fd528a99af01
ms.sourcegitcommit: 12e9b14501d51641b690ee0cf764e2b91eb9a140
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/06/2020
ms.locfileid: "104983951"
---
# <a name="interlockedexchange-function-hlsl-reference"></a><span data-ttu-id="42153-104">Función InterlockedExchange (referencia de HLSL)</span><span class="sxs-lookup"><span data-stu-id="42153-104">InterlockedExchange function (HLSL reference)</span></span>

<span data-ttu-id="42153-105">Asigna Value a dest y devuelve el valor original.</span><span class="sxs-lookup"><span data-stu-id="42153-105">Assigns value to dest and returns the original value.</span></span>

## <a name="syntax"></a><span data-ttu-id="42153-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="42153-106">Syntax</span></span>

``` syntax
void InterlockedExchange(
  in  R dest,
  in  T value,
  out T original_value
);
```

## <a name="parameters"></a><span data-ttu-id="42153-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="42153-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42153-108">*dest* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="42153-108">*dest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42153-109">Tipo: **R**</span><span class="sxs-lookup"><span data-stu-id="42153-109">Type: **R**</span></span>

<span data-ttu-id="42153-110">Dirección de destino.</span><span class="sxs-lookup"><span data-stu-id="42153-110">The destination address.</span></span>

</dd> <dt>

<span data-ttu-id="42153-111">*valor* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="42153-111">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42153-112">Tipo: **T**</span><span class="sxs-lookup"><span data-stu-id="42153-112">Type: **T**</span></span>

<span data-ttu-id="42153-113">Valor de entrada.</span><span class="sxs-lookup"><span data-stu-id="42153-113">The input value.</span></span>

</dd> <dt>

<span data-ttu-id="42153-114">*\_ valor original* \[ fuera\]</span><span class="sxs-lookup"><span data-stu-id="42153-114">*original\_value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="42153-115">Tipo: **T**</span><span class="sxs-lookup"><span data-stu-id="42153-115">Type: **T**</span></span>

<span data-ttu-id="42153-116">El valor original.</span><span class="sxs-lookup"><span data-stu-id="42153-116">The original value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42153-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="42153-117">Return value</span></span>

<span data-ttu-id="42153-118">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="42153-118">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="42153-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="42153-119">Remarks</span></span>

<span data-ttu-id="42153-120">Esta operación solo se puede realizar en recursos de tipo escalar y variables de memoria compartida.</span><span class="sxs-lookup"><span data-stu-id="42153-120">This operation can only be performed on scalar-typed resources and shared memory variables.</span></span> <span data-ttu-id="42153-121">Hay dos usos posibles para esta función.</span><span class="sxs-lookup"><span data-stu-id="42153-121">There are two possible uses for this function.</span></span> <span data-ttu-id="42153-122">El primero es cuando R es un tipo de variable de memoria compartida.</span><span class="sxs-lookup"><span data-stu-id="42153-122">The first is when R is a shared memory variable type.</span></span> <span data-ttu-id="42153-123">En este caso, la función realiza la operación en el registro de memoria compartida al que hace referencia dest.</span><span class="sxs-lookup"><span data-stu-id="42153-123">In this case, the function performs the operation on the shared memory register referenced by dest.</span></span> <span data-ttu-id="42153-124">El segundo escenario es cuando R es un tipo de variable de recurso.</span><span class="sxs-lookup"><span data-stu-id="42153-124">The second scenario is when R is a resource variable type.</span></span> <span data-ttu-id="42153-125">En este escenario, la función realiza la operación en la ubicación del recurso a la que hace referencia dest.</span><span class="sxs-lookup"><span data-stu-id="42153-125">In this scenario, the function performs the operation on the resource location referenced by dest.</span></span> <span data-ttu-id="42153-126">Esta operación solo está disponible cuando R es legible y grabable.</span><span class="sxs-lookup"><span data-stu-id="42153-126">This operation is only available when R is readable and writable.</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="42153-127">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="42153-127">Minimum Shader Model</span></span>

<span data-ttu-id="42153-128">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="42153-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="42153-129">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="42153-129">Shader Model</span></span>                                                                | <span data-ttu-id="42153-130">Compatible</span><span class="sxs-lookup"><span data-stu-id="42153-130">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="42153-131">Modelos de sombreador [modelo 5](d3d11-graphics-reference-sm5.md) y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="42153-131">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="42153-132">sí</span><span class="sxs-lookup"><span data-stu-id="42153-132">yes</span></span>       |



 

<span data-ttu-id="42153-133">Esta función se admite en los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="42153-133">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="42153-134">Vértice</span><span class="sxs-lookup"><span data-stu-id="42153-134">Vertex</span></span> | <span data-ttu-id="42153-135">Casco</span><span class="sxs-lookup"><span data-stu-id="42153-135">Hull</span></span> | <span data-ttu-id="42153-136">Dominio</span><span class="sxs-lookup"><span data-stu-id="42153-136">Domain</span></span> | <span data-ttu-id="42153-137">Geometría</span><span class="sxs-lookup"><span data-stu-id="42153-137">Geometry</span></span> | <span data-ttu-id="42153-138">Píxel</span><span class="sxs-lookup"><span data-stu-id="42153-138">Pixel</span></span> | <span data-ttu-id="42153-139">Compute</span><span class="sxs-lookup"><span data-stu-id="42153-139">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="42153-140">x</span><span class="sxs-lookup"><span data-stu-id="42153-140">x</span></span>      |  <span data-ttu-id="42153-141">x</span><span class="sxs-lookup"><span data-stu-id="42153-141">x</span></span>   | <span data-ttu-id="42153-142">x</span><span class="sxs-lookup"><span data-stu-id="42153-142">x</span></span>      |  <span data-ttu-id="42153-143">x</span><span class="sxs-lookup"><span data-stu-id="42153-143">x</span></span>       | <span data-ttu-id="42153-144">x</span><span class="sxs-lookup"><span data-stu-id="42153-144">x</span></span>     | <span data-ttu-id="42153-145">x</span><span class="sxs-lookup"><span data-stu-id="42153-145">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="42153-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="42153-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42153-147">Funciones intrínsecas</span><span class="sxs-lookup"><span data-stu-id="42153-147">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="42153-148">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="42153-148">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




