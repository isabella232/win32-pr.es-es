---
title: 'RWByteAddressBuffer:: InterlockedAnd (función)'
description: And el valor, de forma atómica.
ms.assetid: c4024be0-3884-4af9-8075-76774c7c6178
keywords:
- InterlockedAnd de función HLSL
topic_type:
- apiref
api_name:
- InterlockedAnd
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a389da886b193815c7d4b2c1fe0a86db1f068fc7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104420895"
---
# <a name="interlockedand-function"></a><span data-ttu-id="2ec5e-104">InterlockedAnd función)</span><span class="sxs-lookup"><span data-stu-id="2ec5e-104">InterlockedAnd function</span></span>

<span data-ttu-id="2ec5e-105">And el valor, de forma atómica.</span><span class="sxs-lookup"><span data-stu-id="2ec5e-105">Ands the value, atomically.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ec5e-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2ec5e-106">Syntax</span></span>

``` syntax
void InterlockedAnd(
  in  UINT dest,
  in  UINT value,
  out UINT original_value
);
```

## <a name="parameters"></a><span data-ttu-id="2ec5e-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2ec5e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ec5e-108">*dest* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2ec5e-108">*dest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ec5e-109">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="2ec5e-109">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="2ec5e-110">Dirección de destino.</span><span class="sxs-lookup"><span data-stu-id="2ec5e-110">The destination address.</span></span>

</dd> <dt>

<span data-ttu-id="2ec5e-111">*valor* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="2ec5e-111">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ec5e-112">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="2ec5e-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="2ec5e-113">Valor de entrada.</span><span class="sxs-lookup"><span data-stu-id="2ec5e-113">The input value.</span></span>

</dd> <dt>

<span data-ttu-id="2ec5e-114">*\_ valor original* \[ fuera\]</span><span class="sxs-lookup"><span data-stu-id="2ec5e-114">*original\_value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2ec5e-115">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="2ec5e-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="2ec5e-116">El valor original.</span><span class="sxs-lookup"><span data-stu-id="2ec5e-116">The original value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ec5e-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2ec5e-117">Return value</span></span>

<span data-ttu-id="2ec5e-118">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="2ec5e-118">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2ec5e-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2ec5e-119">Remarks</span></span>

<span data-ttu-id="2ec5e-120">Esta operación solo se puede realizar en recursos con tipo int o uint y variables de memoria compartida.</span><span class="sxs-lookup"><span data-stu-id="2ec5e-120">This operation can only be performed on int or uint typed resources and shared memory variables.</span></span> <span data-ttu-id="2ec5e-121">Hay tres usos posibles para esta función.</span><span class="sxs-lookup"><span data-stu-id="2ec5e-121">There are three possible uses for this function.</span></span> <span data-ttu-id="2ec5e-122">El primero es cuando R es un tipo de variable de memoria compartida.</span><span class="sxs-lookup"><span data-stu-id="2ec5e-122">The first is when R is a shared memory variable type.</span></span> <span data-ttu-id="2ec5e-123">En este caso, la función realiza un carácter atómico y de valor en el registro de memoria compartida al que hace referencia dest.</span><span class="sxs-lookup"><span data-stu-id="2ec5e-123">In this case, the function performs an atomic and of value to the shared memory register referenced by dest.</span></span> <span data-ttu-id="2ec5e-124">El segundo escenario es cuando R es un tipo de variable de recurso.</span><span class="sxs-lookup"><span data-stu-id="2ec5e-124">The second scenario is when R is a resource variable type.</span></span> <span data-ttu-id="2ec5e-125">En este escenario, la función realiza un carácter atómico y de valor en la ubicación del recurso a la que hace referencia dest.</span><span class="sxs-lookup"><span data-stu-id="2ec5e-125">In this scenario, the function performs an atomic and of value to the resource location referenced by dest.</span></span> <span data-ttu-id="2ec5e-126">Por último, el tercer escenario es cuando R es un tipo de variable local.</span><span class="sxs-lookup"><span data-stu-id="2ec5e-126">Finally, the third scenario is when R is a local variable type.</span></span> <span data-ttu-id="2ec5e-127">En este escenario, la función se reduce a y del valor de DEST y Value, almacenados en dest.</span><span class="sxs-lookup"><span data-stu-id="2ec5e-127">In this scenario, the function reduces to an and of the value of dest and value, stored in dest.</span></span> <span data-ttu-id="2ec5e-128">La función sobrecargada tiene una variable de salida adicional que se establecerá en el valor original de dest.</span><span class="sxs-lookup"><span data-stu-id="2ec5e-128">The overloaded function has an additional output variable which will be set to the original value of dest.</span></span> <span data-ttu-id="2ec5e-129">Esta operación sobrecargada solo está disponible cuando R es legible y grabable.</span><span class="sxs-lookup"><span data-stu-id="2ec5e-129">This overloaded operation is only available when R is readable and writable.</span></span>

<span data-ttu-id="2ec5e-130">Esta función se admite en los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="2ec5e-130">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="2ec5e-131">VS</span><span class="sxs-lookup"><span data-stu-id="2ec5e-131">VS</span></span>  | <span data-ttu-id="2ec5e-132">!</span><span class="sxs-lookup"><span data-stu-id="2ec5e-132">HS</span></span>  | <span data-ttu-id="2ec5e-133">DS</span><span class="sxs-lookup"><span data-stu-id="2ec5e-133">DS</span></span>  | <span data-ttu-id="2ec5e-134">GS</span><span class="sxs-lookup"><span data-stu-id="2ec5e-134">GS</span></span>  | <span data-ttu-id="2ec5e-135">PS</span><span class="sxs-lookup"><span data-stu-id="2ec5e-135">PS</span></span>  | <span data-ttu-id="2ec5e-136">CS</span><span class="sxs-lookup"><span data-stu-id="2ec5e-136">CS</span></span>  |
|-----|-----|-----|-----|-----|-----|
| <span data-ttu-id="2ec5e-137">x</span><span class="sxs-lookup"><span data-stu-id="2ec5e-137">x</span></span>   | <span data-ttu-id="2ec5e-138">x</span><span class="sxs-lookup"><span data-stu-id="2ec5e-138">x</span></span>   |  <span data-ttu-id="2ec5e-139">x</span><span class="sxs-lookup"><span data-stu-id="2ec5e-139">x</span></span>  | <span data-ttu-id="2ec5e-140">x</span><span class="sxs-lookup"><span data-stu-id="2ec5e-140">x</span></span>   | <span data-ttu-id="2ec5e-141">x</span><span class="sxs-lookup"><span data-stu-id="2ec5e-141">x</span></span>   | <span data-ttu-id="2ec5e-142">x</span><span class="sxs-lookup"><span data-stu-id="2ec5e-142">x</span></span>   |



 

## <a name="see-also"></a><span data-ttu-id="2ec5e-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="2ec5e-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ec5e-144">RWByteAddressBuffer</span><span class="sxs-lookup"><span data-stu-id="2ec5e-144">RWByteAddressBuffer</span></span>](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[<span data-ttu-id="2ec5e-145">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="2ec5e-145">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 