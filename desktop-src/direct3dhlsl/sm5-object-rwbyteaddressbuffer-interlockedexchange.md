---
title: 'RWByteAddressBuffer:: InterlockedExchange (función)'
description: Intercambia un valor, de forma atómica.
ms.assetid: a50f4cba-a7a2-44b0-9de7-003b4c7a947f
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
ms.openlocfilehash: 47c51374b7dcd62ac208e0aa8811a8d693ce0ac6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104997044"
---
# <a name="interlockedexchange-function"></a><span data-ttu-id="ed8cd-104">InterlockedExchange función)</span><span class="sxs-lookup"><span data-stu-id="ed8cd-104">InterlockedExchange function</span></span>

<span data-ttu-id="ed8cd-105">Intercambia un valor, de forma atómica.</span><span class="sxs-lookup"><span data-stu-id="ed8cd-105">Exchanges a value, atomically.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed8cd-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ed8cd-106">Syntax</span></span>

``` syntax
void InterlockedExchange(
  in  UINT dest,
  in  UINT value,
  out UINT original_value
);
```

## <a name="parameters"></a><span data-ttu-id="ed8cd-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ed8cd-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed8cd-108">*dest* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ed8cd-108">*dest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed8cd-109">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ed8cd-109">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="ed8cd-110">Dirección de destino.</span><span class="sxs-lookup"><span data-stu-id="ed8cd-110">The destination address.</span></span>

</dd> <dt>

<span data-ttu-id="ed8cd-111">*valor* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="ed8cd-111">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed8cd-112">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ed8cd-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="ed8cd-113">Valor de entrada.</span><span class="sxs-lookup"><span data-stu-id="ed8cd-113">The input value.</span></span>

</dd> <dt>

<span data-ttu-id="ed8cd-114">*\_ valor original* \[ fuera\]</span><span class="sxs-lookup"><span data-stu-id="ed8cd-114">*original\_value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ed8cd-115">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ed8cd-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="ed8cd-116">El valor original.</span><span class="sxs-lookup"><span data-stu-id="ed8cd-116">The original value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed8cd-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ed8cd-117">Return value</span></span>

<span data-ttu-id="ed8cd-118">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="ed8cd-118">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ed8cd-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ed8cd-119">Remarks</span></span>

<span data-ttu-id="ed8cd-120">Esta operación solo se puede realizar en recursos de tipo escalar y variables de memoria compartida.</span><span class="sxs-lookup"><span data-stu-id="ed8cd-120">This operation can only be performed on scalar-typed resources and shared memory variables.</span></span> <span data-ttu-id="ed8cd-121">Hay tres usos posibles para esta función.</span><span class="sxs-lookup"><span data-stu-id="ed8cd-121">There are three possible uses for this function.</span></span> <span data-ttu-id="ed8cd-122">El primero es cuando R es un tipo de variable de memoria compartida.</span><span class="sxs-lookup"><span data-stu-id="ed8cd-122">The first is when R is a shared memory variable type.</span></span> <span data-ttu-id="ed8cd-123">En este caso, la función realiza la operación en el registro de memoria compartida al que hace referencia dest.</span><span class="sxs-lookup"><span data-stu-id="ed8cd-123">In this case, the function performs the operation on the shared memory register referenced by dest.</span></span> <span data-ttu-id="ed8cd-124">El segundo escenario es cuando R es un tipo de variable de recurso.</span><span class="sxs-lookup"><span data-stu-id="ed8cd-124">The second scenario is when R is a resource variable type.</span></span> <span data-ttu-id="ed8cd-125">En este escenario, la función realiza la operación en la ubicación del recurso a la que hace referencia dest.</span><span class="sxs-lookup"><span data-stu-id="ed8cd-125">In this scenario, the function performs the operation on the resource location referenced by dest.</span></span> <span data-ttu-id="ed8cd-126">Por último, el tercer escenario es cuando R es un tipo de variable local.</span><span class="sxs-lookup"><span data-stu-id="ed8cd-126">Finally, the third scenario is when R is a local variable type.</span></span> <span data-ttu-id="ed8cd-127">En este escenario, la función reduce a la operación realizada mediante operaciones locales.</span><span class="sxs-lookup"><span data-stu-id="ed8cd-127">In this scenario, the function reduces to the operation performed using local operations.</span></span> <span data-ttu-id="ed8cd-128">Esta operación solo está disponible cuando R es legible y grabable.</span><span class="sxs-lookup"><span data-stu-id="ed8cd-128">This operation is only available when R is readable and writable.</span></span>

<span data-ttu-id="ed8cd-129">Esta función se admite en los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="ed8cd-129">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="ed8cd-130">VS</span><span class="sxs-lookup"><span data-stu-id="ed8cd-130">VS</span></span>  | <span data-ttu-id="ed8cd-131">!</span><span class="sxs-lookup"><span data-stu-id="ed8cd-131">HS</span></span>  | <span data-ttu-id="ed8cd-132">DS</span><span class="sxs-lookup"><span data-stu-id="ed8cd-132">DS</span></span>  | <span data-ttu-id="ed8cd-133">GS</span><span class="sxs-lookup"><span data-stu-id="ed8cd-133">GS</span></span>  | <span data-ttu-id="ed8cd-134">PS</span><span class="sxs-lookup"><span data-stu-id="ed8cd-134">PS</span></span>  | <span data-ttu-id="ed8cd-135">CS</span><span class="sxs-lookup"><span data-stu-id="ed8cd-135">CS</span></span>  |
|-----|-----|-----|-----|-----|-----|
|  <span data-ttu-id="ed8cd-136">x</span><span class="sxs-lookup"><span data-stu-id="ed8cd-136">x</span></span>  |  <span data-ttu-id="ed8cd-137">x</span><span class="sxs-lookup"><span data-stu-id="ed8cd-137">x</span></span>  |  <span data-ttu-id="ed8cd-138">x</span><span class="sxs-lookup"><span data-stu-id="ed8cd-138">x</span></span>  |  <span data-ttu-id="ed8cd-139">x</span><span class="sxs-lookup"><span data-stu-id="ed8cd-139">x</span></span>  | <span data-ttu-id="ed8cd-140">x</span><span class="sxs-lookup"><span data-stu-id="ed8cd-140">x</span></span>   | <span data-ttu-id="ed8cd-141">x</span><span class="sxs-lookup"><span data-stu-id="ed8cd-141">x</span></span>   |



 

## <a name="see-also"></a><span data-ttu-id="ed8cd-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="ed8cd-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed8cd-143">RWByteAddressBuffer</span><span class="sxs-lookup"><span data-stu-id="ed8cd-143">RWByteAddressBuffer</span></span>](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[<span data-ttu-id="ed8cd-144">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="ed8cd-144">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 