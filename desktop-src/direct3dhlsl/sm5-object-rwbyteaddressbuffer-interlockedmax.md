---
title: 'RWByteAddressBuffer:: InterlockedMax (función)'
description: Busca el valor máximo, de forma atómica.
ms.assetid: 2e78065f-c1ee-47ac-a826-c8a46c730c4a
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
ms.openlocfilehash: e77f925a0950d3731af58c2c6835867640760371
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104997100"
---
# <a name="interlockedmax-function"></a><span data-ttu-id="e1d61-104">InterlockedMax función)</span><span class="sxs-lookup"><span data-stu-id="e1d61-104">InterlockedMax function</span></span>

<span data-ttu-id="e1d61-105">Busca el valor máximo, de forma atómica.</span><span class="sxs-lookup"><span data-stu-id="e1d61-105">Finds the maximum value, atomically.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1d61-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e1d61-106">Syntax</span></span>

``` syntax
void InterlockedMax(
  in  UINT dest,
  in  UINT value,
  out UINT original_value
);
```

## <a name="parameters"></a><span data-ttu-id="e1d61-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e1d61-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e1d61-108">*dest* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e1d61-108">*dest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1d61-109">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e1d61-109">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="e1d61-110">Dirección de destino.</span><span class="sxs-lookup"><span data-stu-id="e1d61-110">The destination address.</span></span>

</dd> <dt>

<span data-ttu-id="e1d61-111">*valor* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="e1d61-111">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1d61-112">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e1d61-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="e1d61-113">Valor de entrada.</span><span class="sxs-lookup"><span data-stu-id="e1d61-113">The input value.</span></span>

</dd> <dt>

<span data-ttu-id="e1d61-114">*\_ valor original* \[ fuera\]</span><span class="sxs-lookup"><span data-stu-id="e1d61-114">*original\_value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e1d61-115">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e1d61-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="e1d61-116">El valor original.</span><span class="sxs-lookup"><span data-stu-id="e1d61-116">The original value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e1d61-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e1d61-117">Return value</span></span>

<span data-ttu-id="e1d61-118">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="e1d61-118">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e1d61-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e1d61-119">Remarks</span></span>

<span data-ttu-id="e1d61-120">Esta operación solo se puede realizar en los recursos con tipo int y uint y las variables de memoria compartida.</span><span class="sxs-lookup"><span data-stu-id="e1d61-120">This operation can only be performed on int and uint typed resources and shared memory variables.</span></span> <span data-ttu-id="e1d61-121">Hay tres usos posibles para esta función.</span><span class="sxs-lookup"><span data-stu-id="e1d61-121">There are three possible uses for this function.</span></span> <span data-ttu-id="e1d61-122">El primero es cuando R es un tipo de variable de memoria compartida.</span><span class="sxs-lookup"><span data-stu-id="e1d61-122">The first is when R is a shared memory variable type.</span></span> <span data-ttu-id="e1d61-123">En este caso, la función realiza un máximo atómico del valor en el registro de memoria compartida al que hace referencia dest.</span><span class="sxs-lookup"><span data-stu-id="e1d61-123">In this case, the function performs an atomic maximum of the value to the shared memory register referenced by dest.</span></span> <span data-ttu-id="e1d61-124">El segundo escenario es cuando R es un tipo de variable de recurso.</span><span class="sxs-lookup"><span data-stu-id="e1d61-124">The second scenario is when R is a resource variable type.</span></span> <span data-ttu-id="e1d61-125">En este escenario, la función realiza un máximo atómico del valor en la ubicación del recurso al que hace referencia dest.</span><span class="sxs-lookup"><span data-stu-id="e1d61-125">In this scenario, the function performs an atomic maximum of the value to the resource location referenced by dest.</span></span> <span data-ttu-id="e1d61-126">Por último, el tercer escenario es cuando R es un tipo de variable local.</span><span class="sxs-lookup"><span data-stu-id="e1d61-126">Finally, the third scenario is when R is a local variable type.</span></span> <span data-ttu-id="e1d61-127">En este escenario, la función reduce hasta un máximo del valor de DEST y Value, almacenado en dest.</span><span class="sxs-lookup"><span data-stu-id="e1d61-127">In this scenario, the function reduces to a maximum of the value of dest and value, stored in dest.</span></span> <span data-ttu-id="e1d61-128">La función sobrecargada tiene una variable de salida adicional que se establecerá en el valor original de dest.</span><span class="sxs-lookup"><span data-stu-id="e1d61-128">The overloaded function has an additional output variable which will be set to the original value of dest.</span></span> <span data-ttu-id="e1d61-129">Esta operación sobrecargada solo está disponible cuando R es legible y grabable.</span><span class="sxs-lookup"><span data-stu-id="e1d61-129">This overloaded operation is only available when R is readable and writable.</span></span>

<span data-ttu-id="e1d61-130">Esta función se admite en los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="e1d61-130">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="e1d61-131">VS</span><span class="sxs-lookup"><span data-stu-id="e1d61-131">VS</span></span>  | <span data-ttu-id="e1d61-132">!</span><span class="sxs-lookup"><span data-stu-id="e1d61-132">HS</span></span>  | <span data-ttu-id="e1d61-133">DS</span><span class="sxs-lookup"><span data-stu-id="e1d61-133">DS</span></span>  | <span data-ttu-id="e1d61-134">GS</span><span class="sxs-lookup"><span data-stu-id="e1d61-134">GS</span></span>  | <span data-ttu-id="e1d61-135">PS</span><span class="sxs-lookup"><span data-stu-id="e1d61-135">PS</span></span>  | <span data-ttu-id="e1d61-136">CS</span><span class="sxs-lookup"><span data-stu-id="e1d61-136">CS</span></span>  |
|-----|-----|-----|-----|-----|-----|
| <span data-ttu-id="e1d61-137">x</span><span class="sxs-lookup"><span data-stu-id="e1d61-137">x</span></span>   | <span data-ttu-id="e1d61-138">x</span><span class="sxs-lookup"><span data-stu-id="e1d61-138">x</span></span>   | <span data-ttu-id="e1d61-139">x</span><span class="sxs-lookup"><span data-stu-id="e1d61-139">x</span></span>   | <span data-ttu-id="e1d61-140">x</span><span class="sxs-lookup"><span data-stu-id="e1d61-140">x</span></span>   | <span data-ttu-id="e1d61-141">x</span><span class="sxs-lookup"><span data-stu-id="e1d61-141">x</span></span>   | <span data-ttu-id="e1d61-142">x</span><span class="sxs-lookup"><span data-stu-id="e1d61-142">x</span></span>   |



 

## <a name="see-also"></a><span data-ttu-id="e1d61-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="e1d61-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1d61-144">RWByteAddressBuffer</span><span class="sxs-lookup"><span data-stu-id="e1d61-144">RWByteAddressBuffer</span></span>](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[<span data-ttu-id="e1d61-145">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="e1d61-145">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 