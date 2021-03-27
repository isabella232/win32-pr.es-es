---
title: 'RWByteAddressBuffer:: InterlockedXor (función)'
description: Realiza una XOR atómica en el valor.
ms.assetid: 692f8b5e-a81e-4700-8a8d-3594aba85671
keywords:
- InterlockedXor de función HLSL
topic_type:
- apiref
api_name:
- InterlockedXor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 920ae912c599b66a03a25d7bc8ecc9b199036b26
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995276"
---
# <a name="interlockedxor-function"></a><span data-ttu-id="1501c-104">InterlockedXor función)</span><span class="sxs-lookup"><span data-stu-id="1501c-104">InterlockedXor function</span></span>

<span data-ttu-id="1501c-105">Realiza una **XOR** atómica en el valor.</span><span class="sxs-lookup"><span data-stu-id="1501c-105">Performs an atomic **XOR** on the value.</span></span>

## <a name="syntax"></a><span data-ttu-id="1501c-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1501c-106">Syntax</span></span>

``` syntax
void InterlockedXor(
  in  UINT dest,
  in  UINT value,
  out UINT original_value
);
```

## <a name="parameters"></a><span data-ttu-id="1501c-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1501c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1501c-108">*dest* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1501c-108">*dest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1501c-109">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="1501c-109">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="1501c-110">Dirección de destino.</span><span class="sxs-lookup"><span data-stu-id="1501c-110">The destination address.</span></span>

</dd> <dt>

<span data-ttu-id="1501c-111">*valor* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="1501c-111">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1501c-112">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="1501c-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="1501c-113">Valor de entrada.</span><span class="sxs-lookup"><span data-stu-id="1501c-113">The input value.</span></span>

</dd> <dt>

<span data-ttu-id="1501c-114">*\_ valor original* \[ fuera\]</span><span class="sxs-lookup"><span data-stu-id="1501c-114">*original\_value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1501c-115">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="1501c-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="1501c-116">El valor original.</span><span class="sxs-lookup"><span data-stu-id="1501c-116">The original value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1501c-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1501c-117">Return value</span></span>

<span data-ttu-id="1501c-118">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="1501c-118">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1501c-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1501c-119">Remarks</span></span>

<span data-ttu-id="1501c-120">Esta operación solo se puede realizar en recursos con tipo **int** o **uint** y variables de memoria compartida.</span><span class="sxs-lookup"><span data-stu-id="1501c-120">This operation can be performed only on **INT** or **UINT** typed resources and shared memory variables.</span></span> <span data-ttu-id="1501c-121">Hay tres usos posibles para esta función.</span><span class="sxs-lookup"><span data-stu-id="1501c-121">There are three possible uses for this function.</span></span> <span data-ttu-id="1501c-122">El primero es cuando R es un tipo de variable de memoria compartida.</span><span class="sxs-lookup"><span data-stu-id="1501c-122">The first is when R is a shared memory variable type.</span></span> <span data-ttu-id="1501c-123">En este caso, la función realiza una **XOR** atómica con el valor del registro de memoria compartida al que hace referencia *dest*.</span><span class="sxs-lookup"><span data-stu-id="1501c-123">In this case, the function performs an atomic **XOR** with the value of the shared memory register referenced by *dest*.</span></span> <span data-ttu-id="1501c-124">El segundo escenario es cuando R es un tipo de variable de recurso.</span><span class="sxs-lookup"><span data-stu-id="1501c-124">The second scenario is when R is a resource variable type.</span></span> <span data-ttu-id="1501c-125">En este escenario, la función realiza una **XOR** atómica con el valor de la ubicación del recurso al que hace referencia *dest*.</span><span class="sxs-lookup"><span data-stu-id="1501c-125">In this scenario, the function performs an atomic **XOR** with the value of the resource location referenced by *dest*.</span></span> <span data-ttu-id="1501c-126">Por último, el tercer escenario es cuando R es un tipo de variable local.</span><span class="sxs-lookup"><span data-stu-id="1501c-126">Finally, the third scenario is when R is a local variable type.</span></span> <span data-ttu-id="1501c-127">En este escenario, la función reduce a una **XOR** de los valores de *dest* y *Value*.</span><span class="sxs-lookup"><span data-stu-id="1501c-127">In this scenario, the function reduces to an **XOR** of the values of *dest* and *value*.</span></span> <span data-ttu-id="1501c-128">El resultado de la operación reemplaza el valor de *dest*.</span><span class="sxs-lookup"><span data-stu-id="1501c-128">The result of the operation replaces the value in *dest*.</span></span> <span data-ttu-id="1501c-129">La función sobrecargada tiene una variable de salida adicional que se establecerá en el valor original de *dest*.</span><span class="sxs-lookup"><span data-stu-id="1501c-129">The overloaded function has an additional output variable which will be set to the original value of *dest*.</span></span> <span data-ttu-id="1501c-130">Esta operación sobrecargada solo está disponible cuando R es legible y grabable.</span><span class="sxs-lookup"><span data-stu-id="1501c-130">This overloaded operation is available only when R is readable and writable.</span></span>

<span data-ttu-id="1501c-131">Esta función se admite en los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="1501c-131">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="1501c-132">VS</span><span class="sxs-lookup"><span data-stu-id="1501c-132">VS</span></span>  | <span data-ttu-id="1501c-133">!</span><span class="sxs-lookup"><span data-stu-id="1501c-133">HS</span></span>  | <span data-ttu-id="1501c-134">DS</span><span class="sxs-lookup"><span data-stu-id="1501c-134">DS</span></span>  | <span data-ttu-id="1501c-135">GS</span><span class="sxs-lookup"><span data-stu-id="1501c-135">GS</span></span>  | <span data-ttu-id="1501c-136">PS</span><span class="sxs-lookup"><span data-stu-id="1501c-136">PS</span></span>  | <span data-ttu-id="1501c-137">CS</span><span class="sxs-lookup"><span data-stu-id="1501c-137">CS</span></span>  |
|-----|-----|-----|-----|-----|-----|
| <span data-ttu-id="1501c-138">x</span><span class="sxs-lookup"><span data-stu-id="1501c-138">x</span></span>   |  <span data-ttu-id="1501c-139">x</span><span class="sxs-lookup"><span data-stu-id="1501c-139">x</span></span>  | <span data-ttu-id="1501c-140">x</span><span class="sxs-lookup"><span data-stu-id="1501c-140">x</span></span>   | <span data-ttu-id="1501c-141">x</span><span class="sxs-lookup"><span data-stu-id="1501c-141">x</span></span>   | <span data-ttu-id="1501c-142">x</span><span class="sxs-lookup"><span data-stu-id="1501c-142">x</span></span>   | <span data-ttu-id="1501c-143">x</span><span class="sxs-lookup"><span data-stu-id="1501c-143">x</span></span>   |



 

## <a name="see-also"></a><span data-ttu-id="1501c-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="1501c-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1501c-145">RWByteAddressBuffer</span><span class="sxs-lookup"><span data-stu-id="1501c-145">RWByteAddressBuffer</span></span>](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[<span data-ttu-id="1501c-146">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="1501c-146">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 