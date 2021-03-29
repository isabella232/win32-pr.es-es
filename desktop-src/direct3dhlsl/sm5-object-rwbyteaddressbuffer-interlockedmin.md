---
title: 'RWByteAddressBuffer:: InterlockedMin (función)'
description: Busca el valor mínimo, de forma atómica.
ms.assetid: bf650b2e-9c6c-4458-9565-1e9ec76a1472
keywords:
- InterlockedMin de función HLSL
topic_type:
- apiref
api_name:
- InterlockedMin
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b818a1fa0897d103e7d609a676212c6db428935f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104077774"
---
# <a name="interlockedmin-function"></a><span data-ttu-id="67243-104">InterlockedMin función)</span><span class="sxs-lookup"><span data-stu-id="67243-104">InterlockedMin function</span></span>

<span data-ttu-id="67243-105">Busca el valor mínimo, de forma atómica.</span><span class="sxs-lookup"><span data-stu-id="67243-105">Finds the minimum value, atomically.</span></span>

## <a name="syntax"></a><span data-ttu-id="67243-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="67243-106">Syntax</span></span>

``` syntax
void InterlockedMin(
  in  UINT dest,
  in  UINT value,
  out UINT original_value
);
```

## <a name="parameters"></a><span data-ttu-id="67243-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="67243-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="67243-108">*dest* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="67243-108">*dest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="67243-109">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="67243-109">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="67243-110">Dirección de destino.</span><span class="sxs-lookup"><span data-stu-id="67243-110">The destination address.</span></span>

</dd> <dt>

<span data-ttu-id="67243-111">*valor* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="67243-111">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="67243-112">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="67243-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="67243-113">Valor de entrada.</span><span class="sxs-lookup"><span data-stu-id="67243-113">The input value.</span></span>

</dd> <dt>

<span data-ttu-id="67243-114">*\_ valor original* \[ fuera\]</span><span class="sxs-lookup"><span data-stu-id="67243-114">*original\_value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="67243-115">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="67243-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="67243-116">El valor original.</span><span class="sxs-lookup"><span data-stu-id="67243-116">The original value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="67243-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="67243-117">Return value</span></span>

<span data-ttu-id="67243-118">Nada</span><span class="sxs-lookup"><span data-stu-id="67243-118">Nothing</span></span>

## <a name="remarks"></a><span data-ttu-id="67243-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="67243-119">Remarks</span></span>

<span data-ttu-id="67243-120">Esta operación solo se puede realizar en los recursos con tipo int y uint y las variables de memoria compartida.</span><span class="sxs-lookup"><span data-stu-id="67243-120">This operation can only be performed on int and uint typed resources and shared memory variables.</span></span> <span data-ttu-id="67243-121">Hay tres usos posibles para esta función.</span><span class="sxs-lookup"><span data-stu-id="67243-121">There are three possible uses for this function.</span></span> <span data-ttu-id="67243-122">El primero es cuando R es un tipo de variable de memoria compartida.</span><span class="sxs-lookup"><span data-stu-id="67243-122">The first is when R is a shared memory variable type.</span></span> <span data-ttu-id="67243-123">En este caso, la función realiza un mínimo atómico del valor en el registro de memoria compartida al que hace referencia dest.</span><span class="sxs-lookup"><span data-stu-id="67243-123">In this case, the function performs an atomic minimum of the value to the shared memory register referenced by dest.</span></span> <span data-ttu-id="67243-124">El segundo escenario es cuando R es un tipo de variable de recurso.</span><span class="sxs-lookup"><span data-stu-id="67243-124">The second scenario is when R is a resource variable type.</span></span> <span data-ttu-id="67243-125">En este escenario, la función realiza un mínimo atómico del valor en la ubicación del recurso a la que hace referencia dest.</span><span class="sxs-lookup"><span data-stu-id="67243-125">In this scenario, the function performs an atomic minimum of the value to the resource location referenced by dest.</span></span> <span data-ttu-id="67243-126">Por último, el tercer escenario es cuando R es un tipo de variable local.</span><span class="sxs-lookup"><span data-stu-id="67243-126">Finally, the third scenario is when R is a local variable type.</span></span> <span data-ttu-id="67243-127">En este escenario, la función reduce a un mínimo el valor de DEST y Value, almacenado en dest.</span><span class="sxs-lookup"><span data-stu-id="67243-127">In this scenario, the function reduces to a minimum of the value of dest and value, stored in dest.</span></span> <span data-ttu-id="67243-128">La función sobrecargada tiene una variable de salida adicional que se establecerá en el valor original de dest.</span><span class="sxs-lookup"><span data-stu-id="67243-128">The overloaded function has an additional output variable which will be set to the original value of dest.</span></span> <span data-ttu-id="67243-129">Esta operación sobrecargada solo está disponible cuando R es legible y grabable.</span><span class="sxs-lookup"><span data-stu-id="67243-129">This overloaded operation is only available when R is readable and writable.</span></span>

<span data-ttu-id="67243-130">Esta función se admite en los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="67243-130">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="67243-131">VS</span><span class="sxs-lookup"><span data-stu-id="67243-131">VS</span></span>  | <span data-ttu-id="67243-132">!</span><span class="sxs-lookup"><span data-stu-id="67243-132">HS</span></span>  | <span data-ttu-id="67243-133">DS</span><span class="sxs-lookup"><span data-stu-id="67243-133">DS</span></span>  | <span data-ttu-id="67243-134">GS</span><span class="sxs-lookup"><span data-stu-id="67243-134">GS</span></span>  | <span data-ttu-id="67243-135">PS</span><span class="sxs-lookup"><span data-stu-id="67243-135">PS</span></span>  | <span data-ttu-id="67243-136">CS</span><span class="sxs-lookup"><span data-stu-id="67243-136">CS</span></span>  |
|-----|-----|-----|-----|-----|-----|
| <span data-ttu-id="67243-137">x</span><span class="sxs-lookup"><span data-stu-id="67243-137">x</span></span>   |  <span data-ttu-id="67243-138">x</span><span class="sxs-lookup"><span data-stu-id="67243-138">x</span></span>  | <span data-ttu-id="67243-139">x</span><span class="sxs-lookup"><span data-stu-id="67243-139">x</span></span>   | <span data-ttu-id="67243-140">x</span><span class="sxs-lookup"><span data-stu-id="67243-140">x</span></span>   | <span data-ttu-id="67243-141">x</span><span class="sxs-lookup"><span data-stu-id="67243-141">x</span></span>   | <span data-ttu-id="67243-142">x</span><span class="sxs-lookup"><span data-stu-id="67243-142">x</span></span>   |



 

## <a name="see-also"></a><span data-ttu-id="67243-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="67243-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67243-144">RWByteAddressBuffer</span><span class="sxs-lookup"><span data-stu-id="67243-144">RWByteAddressBuffer</span></span>](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[<span data-ttu-id="67243-145">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="67243-145">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 