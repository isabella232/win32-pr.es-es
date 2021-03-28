---
title: Función InterlockedCompareExchange (referencia de HLSL)
description: Compara de forma atómica el destino con el valor de comparación. Si son idénticos, el destino se sobrescribe con el valor de entrada. El valor original se establece en el valor original del destino.
ms.assetid: 85d1ba58-8e79-41cd-abd6-7ffff59839c7
keywords:
- InterlockedCompareExchange de función HLSL
topic_type:
- apiref
api_name:
- InterlockedCompareExchange
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 74bc189996752d754599bf4547e8baa4d9fb74cc
ms.sourcegitcommit: 12e9b14501d51641b690ee0cf764e2b91eb9a140
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/06/2020
ms.locfileid: "104997025"
---
# <a name="interlockedcompareexchange-function-hlsl-reference"></a><span data-ttu-id="0b4a5-106">Función InterlockedCompareExchange (referencia de HLSL)</span><span class="sxs-lookup"><span data-stu-id="0b4a5-106">InterlockedCompareExchange function (HLSL reference)</span></span>

<span data-ttu-id="0b4a5-107">Compara de forma atómica el destino con el valor de comparación.</span><span class="sxs-lookup"><span data-stu-id="0b4a5-107">Atomically compares the destination with the comparison value.</span></span> <span data-ttu-id="0b4a5-108">Si son idénticos, el destino se sobrescribe con el valor de entrada.</span><span class="sxs-lookup"><span data-stu-id="0b4a5-108">If they are identical, the destination is overwritten with the input value.</span></span> <span data-ttu-id="0b4a5-109">El valor original se establece en el valor original del destino.</span><span class="sxs-lookup"><span data-stu-id="0b4a5-109">The original value is set to the destination's original value.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b4a5-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0b4a5-110">Syntax</span></span>

``` syntax
void InterlockedCompareExchange(
  in  R dest,
  in  T compare_value,
  in  T value,
  out T original_value
);
```

## <a name="parameters"></a><span data-ttu-id="0b4a5-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0b4a5-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b4a5-112">*dest* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0b4a5-112">*dest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b4a5-113">Tipo: **R**</span><span class="sxs-lookup"><span data-stu-id="0b4a5-113">Type: **R**</span></span>

<span data-ttu-id="0b4a5-114">Dirección de destino.</span><span class="sxs-lookup"><span data-stu-id="0b4a5-114">The destination address.</span></span>

</dd> <dt>

<span data-ttu-id="0b4a5-115">*comparar \_ valor* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="0b4a5-115">*compare\_value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b4a5-116">Tipo: **T**</span><span class="sxs-lookup"><span data-stu-id="0b4a5-116">Type: **T**</span></span>

<span data-ttu-id="0b4a5-117">El valor de comparación.</span><span class="sxs-lookup"><span data-stu-id="0b4a5-117">The comparison value.</span></span>

</dd> <dt>

<span data-ttu-id="0b4a5-118">*valor* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="0b4a5-118">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b4a5-119">Tipo: **T**</span><span class="sxs-lookup"><span data-stu-id="0b4a5-119">Type: **T**</span></span>

<span data-ttu-id="0b4a5-120">Valor de entrada.</span><span class="sxs-lookup"><span data-stu-id="0b4a5-120">The input value.</span></span>

</dd> <dt>

<span data-ttu-id="0b4a5-121">*\_ valor original* \[ fuera\]</span><span class="sxs-lookup"><span data-stu-id="0b4a5-121">*original\_value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0b4a5-122">Tipo: **T**</span><span class="sxs-lookup"><span data-stu-id="0b4a5-122">Type: **T**</span></span>

<span data-ttu-id="0b4a5-123">El valor original.</span><span class="sxs-lookup"><span data-stu-id="0b4a5-123">The original value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0b4a5-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0b4a5-124">Return value</span></span>

<span data-ttu-id="0b4a5-125">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="0b4a5-125">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0b4a5-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0b4a5-126">Remarks</span></span>

<span data-ttu-id="0b4a5-127">Compara atómicamente el valor al que hace referencia *dest* con *el \_ valor de Compare*, almacena el *valor* en la ubicación a la que hace referencia *dest* si los valores coinciden, devuelve el valor original de *dest* en el *\_ valor original*.</span><span class="sxs-lookup"><span data-stu-id="0b4a5-127">Atomically compares the value referenced by *dest* with *compare\_value*, stores *value* in the location referenced by *dest* if the values match, returns the original value of *dest* in *original\_value*.</span></span> <span data-ttu-id="0b4a5-128">Esta operación solo se puede realizar en recursos con tipo **int** o **uint** y variables de memoria compartida.</span><span class="sxs-lookup"><span data-stu-id="0b4a5-128">This operation can only be performed on **int** or **uint** typed resources and shared memory variables.</span></span> <span data-ttu-id="0b4a5-129">Hay dos usos posibles para esta función.</span><span class="sxs-lookup"><span data-stu-id="0b4a5-129">There are two possible uses for this function.</span></span> <span data-ttu-id="0b4a5-130">El primero es cuando R es un tipo de variable de memoria compartida.</span><span class="sxs-lookup"><span data-stu-id="0b4a5-130">The first is when R is a shared memory variable type.</span></span> <span data-ttu-id="0b4a5-131">En este caso, la función realiza la operación en el registro de memoria compartida al que hace referencia *dest*.</span><span class="sxs-lookup"><span data-stu-id="0b4a5-131">In this case, the function performs the operation on the shared memory register referenced by *dest*.</span></span> <span data-ttu-id="0b4a5-132">El segundo escenario es cuando R es un tipo de variable de recurso.</span><span class="sxs-lookup"><span data-stu-id="0b4a5-132">The second scenario is when R is a resource variable type.</span></span> <span data-ttu-id="0b4a5-133">En este escenario, la función realiza la operación en la ubicación del recurso a la que hace referencia *dest*.</span><span class="sxs-lookup"><span data-stu-id="0b4a5-133">In this scenario, the function performs the operation on the resource location referenced by *dest*.</span></span> <span data-ttu-id="0b4a5-134">Esta operación solo está disponible cuando R es legible y grabable.</span><span class="sxs-lookup"><span data-stu-id="0b4a5-134">This operation is only available when R is readable and writable.</span></span>

> [!Note]  
> <span data-ttu-id="0b4a5-135">Si llama a **InterlockedCompareExchange** en un bucle for o [**While**](dx-graphics-hlsl-while.md) del sombreador [**de**](dx-graphics-hlsl-for.md) cálculo, para compilar correctamente, debe usar el atributo **\[ Allow \_ UAV \_ Condition \]** en dicho bucle.</span><span class="sxs-lookup"><span data-stu-id="0b4a5-135">If you call **InterlockedCompareExchange** in a [**for**](dx-graphics-hlsl-for.md) or [**while**](dx-graphics-hlsl-while.md) compute shader loop, to properly compile, you must use the **\[allow\_uav\_condition\]** attribute on that loop.</span></span>

 

### <a name="minimum-shader-model"></a><span data-ttu-id="0b4a5-136">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="0b4a5-136">Minimum Shader Model</span></span>

<span data-ttu-id="0b4a5-137">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="0b4a5-137">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="0b4a5-138">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="0b4a5-138">Shader Model</span></span>                                                                | <span data-ttu-id="0b4a5-139">Compatible</span><span class="sxs-lookup"><span data-stu-id="0b4a5-139">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="0b4a5-140">Modelos de sombreador [modelo 5](d3d11-graphics-reference-sm5.md) y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="0b4a5-140">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="0b4a5-141">sí</span><span class="sxs-lookup"><span data-stu-id="0b4a5-141">yes</span></span>       |



 

<span data-ttu-id="0b4a5-142">Esta función se admite en los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="0b4a5-142">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="0b4a5-143">Vértice</span><span class="sxs-lookup"><span data-stu-id="0b4a5-143">Vertex</span></span> | <span data-ttu-id="0b4a5-144">Casco</span><span class="sxs-lookup"><span data-stu-id="0b4a5-144">Hull</span></span> | <span data-ttu-id="0b4a5-145">Dominio</span><span class="sxs-lookup"><span data-stu-id="0b4a5-145">Domain</span></span> | <span data-ttu-id="0b4a5-146">Geometría</span><span class="sxs-lookup"><span data-stu-id="0b4a5-146">Geometry</span></span> | <span data-ttu-id="0b4a5-147">Píxel</span><span class="sxs-lookup"><span data-stu-id="0b4a5-147">Pixel</span></span> | <span data-ttu-id="0b4a5-148">Compute</span><span class="sxs-lookup"><span data-stu-id="0b4a5-148">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="0b4a5-149">x</span><span class="sxs-lookup"><span data-stu-id="0b4a5-149">x</span></span>      |  <span data-ttu-id="0b4a5-150">x</span><span class="sxs-lookup"><span data-stu-id="0b4a5-150">x</span></span>   |  <span data-ttu-id="0b4a5-151">x</span><span class="sxs-lookup"><span data-stu-id="0b4a5-151">x</span></span>     |  <span data-ttu-id="0b4a5-152">x</span><span class="sxs-lookup"><span data-stu-id="0b4a5-152">x</span></span>       | <span data-ttu-id="0b4a5-153">x</span><span class="sxs-lookup"><span data-stu-id="0b4a5-153">x</span></span>     | <span data-ttu-id="0b4a5-154">x</span><span class="sxs-lookup"><span data-stu-id="0b4a5-154">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="0b4a5-155">Vea también</span><span class="sxs-lookup"><span data-stu-id="0b4a5-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b4a5-156">Funciones intrínsecas</span><span class="sxs-lookup"><span data-stu-id="0b4a5-156">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="0b4a5-157">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="0b4a5-157">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




