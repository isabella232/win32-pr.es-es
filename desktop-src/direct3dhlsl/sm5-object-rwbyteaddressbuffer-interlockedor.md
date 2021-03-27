---
title: 'RWByteAddressBuffer:: Interlocked (función)'
description: Realiza una expresión atómica o en el valor.
ms.assetid: 3a05619b-db97-4cf1-af3c-12c376e605a6
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
ms.openlocfilehash: 14b902f70919c79ed3e313671ede709f284a1490
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995277"
---
# <a name="interlockedor-function"></a><span data-ttu-id="21765-104">Interbloqueo (función)</span><span class="sxs-lookup"><span data-stu-id="21765-104">InterlockedOr function</span></span>

<span data-ttu-id="21765-105">Realiza una expresión atómica **o** en el valor.</span><span class="sxs-lookup"><span data-stu-id="21765-105">Performs an atomic **OR** on the value.</span></span>

## <a name="syntax"></a><span data-ttu-id="21765-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="21765-106">Syntax</span></span>

``` syntax
void InterlockedOr(
  in  UINT dest,
  in  UINT value,
  out UINT original_value
);
```

## <a name="parameters"></a><span data-ttu-id="21765-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="21765-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21765-108">*dest* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="21765-108">*dest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21765-109">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="21765-109">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="21765-110">Dirección de destino.</span><span class="sxs-lookup"><span data-stu-id="21765-110">The destination address.</span></span>

</dd> <dt>

<span data-ttu-id="21765-111">*valor* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="21765-111">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21765-112">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="21765-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="21765-113">Valor de entrada.</span><span class="sxs-lookup"><span data-stu-id="21765-113">The input value.</span></span>

</dd> <dt>

<span data-ttu-id="21765-114">*\_ valor original* \[ fuera\]</span><span class="sxs-lookup"><span data-stu-id="21765-114">*original\_value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="21765-115">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="21765-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="21765-116">El valor original.</span><span class="sxs-lookup"><span data-stu-id="21765-116">The original value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21765-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="21765-117">Return value</span></span>

<span data-ttu-id="21765-118">Nada</span><span class="sxs-lookup"><span data-stu-id="21765-118">Nothing</span></span>

## <a name="remarks"></a><span data-ttu-id="21765-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="21765-119">Remarks</span></span>

<span data-ttu-id="21765-120">Esta operación solo se puede realizar en recursos con tipo **int** o **uint** y variables de memoria compartida.</span><span class="sxs-lookup"><span data-stu-id="21765-120">This operation can be performed only on **INT** or **UINT** typed resources and shared memory variables.</span></span> <span data-ttu-id="21765-121">Hay tres usos posibles para esta función.</span><span class="sxs-lookup"><span data-stu-id="21765-121">There are three possible uses for this function.</span></span> <span data-ttu-id="21765-122">El primero es cuando R es un tipo de variable de memoria compartida.</span><span class="sxs-lookup"><span data-stu-id="21765-122">The first is when R is a shared memory variable type.</span></span> <span data-ttu-id="21765-123">En este caso, la función realiza una atomicidad **o** con el valor del registro de memoria compartida al que hace referencia *dest*.</span><span class="sxs-lookup"><span data-stu-id="21765-123">In this case, the function performs an atomic **OR** with the value of the shared memory register referenced by *dest*.</span></span> <span data-ttu-id="21765-124">El segundo escenario es cuando R es un tipo de variable de recurso.</span><span class="sxs-lookup"><span data-stu-id="21765-124">The second scenario is when R is a resource variable type.</span></span> <span data-ttu-id="21765-125">En este escenario, la función realiza una atomicidad **o** con el valor de la ubicación del recurso al que hace referencia *dest*.</span><span class="sxs-lookup"><span data-stu-id="21765-125">In this scenario, the function performs an atomic **OR** with the value of the resource location referenced by *dest*.</span></span> <span data-ttu-id="21765-126">Por último, el tercer escenario es cuando R es un tipo de variable local.</span><span class="sxs-lookup"><span data-stu-id="21765-126">Finally, the third scenario is when R is a local variable type.</span></span> <span data-ttu-id="21765-127">En este escenario, la función se reduce a **o** con los valores de *dest* y *Value*.</span><span class="sxs-lookup"><span data-stu-id="21765-127">In this scenario, the function reduces to an **OR** with the values of *dest* and *value*.</span></span> <span data-ttu-id="21765-128">El resultado de la operación reemplaza el valor de *dest*.</span><span class="sxs-lookup"><span data-stu-id="21765-128">The result of the operation replaces the value of *dest*.</span></span> <span data-ttu-id="21765-129">La función sobrecargada tiene una variable de salida adicional, que se establecerá en el valor original de *dest*.</span><span class="sxs-lookup"><span data-stu-id="21765-129">The overloaded function has an additional output variable, which will be set to the original value of *dest*.</span></span> <span data-ttu-id="21765-130">Esta operación sobrecargada solo está disponible cuando R es legible y grabable.</span><span class="sxs-lookup"><span data-stu-id="21765-130">This overloaded operation is available only when R is readable and writable.</span></span>

<span data-ttu-id="21765-131">Esta función se admite en los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="21765-131">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="21765-132">VS</span><span class="sxs-lookup"><span data-stu-id="21765-132">VS</span></span>  | <span data-ttu-id="21765-133">!</span><span class="sxs-lookup"><span data-stu-id="21765-133">HS</span></span>  | <span data-ttu-id="21765-134">DS</span><span class="sxs-lookup"><span data-stu-id="21765-134">DS</span></span>  | <span data-ttu-id="21765-135">GS</span><span class="sxs-lookup"><span data-stu-id="21765-135">GS</span></span>  | <span data-ttu-id="21765-136">PS</span><span class="sxs-lookup"><span data-stu-id="21765-136">PS</span></span>  | <span data-ttu-id="21765-137">CS</span><span class="sxs-lookup"><span data-stu-id="21765-137">CS</span></span>  |
|-----|-----|-----|-----|-----|-----|
| <span data-ttu-id="21765-138">x</span><span class="sxs-lookup"><span data-stu-id="21765-138">x</span></span>   |  <span data-ttu-id="21765-139">x</span><span class="sxs-lookup"><span data-stu-id="21765-139">x</span></span>  | <span data-ttu-id="21765-140">x</span><span class="sxs-lookup"><span data-stu-id="21765-140">x</span></span>   | <span data-ttu-id="21765-141">x</span><span class="sxs-lookup"><span data-stu-id="21765-141">x</span></span>   | <span data-ttu-id="21765-142">x</span><span class="sxs-lookup"><span data-stu-id="21765-142">x</span></span>   | <span data-ttu-id="21765-143">x</span><span class="sxs-lookup"><span data-stu-id="21765-143">x</span></span>   |



 

## <a name="see-also"></a><span data-ttu-id="21765-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="21765-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21765-145">RWByteAddressBuffer</span><span class="sxs-lookup"><span data-stu-id="21765-145">RWByteAddressBuffer</span></span>](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[<span data-ttu-id="21765-146">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="21765-146">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 