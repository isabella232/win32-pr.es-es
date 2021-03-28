---
title: 'RWByteAddressBuffer:: InterlockedAdd (función)'
description: Agrega el valor, de forma atómica.
ms.assetid: 27274aae-1e75-4626-9997-57c4e9393000
keywords:
- InterlockedAdd de función HLSL
topic_type:
- apiref
api_name:
- InterlockedAdd
api_location:
- winnt.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d352ed97df15ce076c10950c6da94aaeaff0f2d0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104997073"
---
# <a name="interlockedadd-function"></a><span data-ttu-id="f9012-104">InterlockedAdd función)</span><span class="sxs-lookup"><span data-stu-id="f9012-104">InterlockedAdd function</span></span>

<span data-ttu-id="f9012-105">Agrega el valor, de forma atómica.</span><span class="sxs-lookup"><span data-stu-id="f9012-105">Adds the value, atomically.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9012-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f9012-106">Syntax</span></span>

``` syntax
void InterlockedAdd(
  in  UINT dest,
  in  UINT value,
  out UINT original_value
);
```

## <a name="parameters"></a><span data-ttu-id="f9012-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f9012-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9012-108">*dest* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f9012-108">*dest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f9012-109">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="f9012-109">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="f9012-110">Dirección de destino.</span><span class="sxs-lookup"><span data-stu-id="f9012-110">The destination address.</span></span>

</dd> <dt>

<span data-ttu-id="f9012-111">*valor* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="f9012-111">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f9012-112">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="f9012-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="f9012-113">Valor de entrada.</span><span class="sxs-lookup"><span data-stu-id="f9012-113">The input value.</span></span>

</dd> <dt>

<span data-ttu-id="f9012-114">*\_ valor original* \[ fuera\]</span><span class="sxs-lookup"><span data-stu-id="f9012-114">*original\_value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f9012-115">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="f9012-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="f9012-116">El valor original.</span><span class="sxs-lookup"><span data-stu-id="f9012-116">The original value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f9012-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f9012-117">Return value</span></span>

<span data-ttu-id="f9012-118">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="f9012-118">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f9012-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f9012-119">Remarks</span></span>

<span data-ttu-id="f9012-120">Esta operación solo se puede realizar en recursos con tipo int o uint y variables de memoria compartida.</span><span class="sxs-lookup"><span data-stu-id="f9012-120">This operation can be performed only on int or uint typed resources and shared memory variables.</span></span> <span data-ttu-id="f9012-121">Hay tres usos posibles para esta función.</span><span class="sxs-lookup"><span data-stu-id="f9012-121">There are three possible uses for this function.</span></span> <span data-ttu-id="f9012-122">El primero es cuando R es un tipo de variable de memoria compartida.</span><span class="sxs-lookup"><span data-stu-id="f9012-122">The first is when R is a shared memory variable type.</span></span> <span data-ttu-id="f9012-123">En este caso, la función realiza un agregado atómico de valor al registro de memoria compartida al que hace referencia dest.</span><span class="sxs-lookup"><span data-stu-id="f9012-123">In this case, the function performs an atomic add of value to the shared memory register referenced by dest.</span></span> <span data-ttu-id="f9012-124">El segundo escenario es cuando R es un tipo de variable de recurso.</span><span class="sxs-lookup"><span data-stu-id="f9012-124">The second scenario is when R is a resource variable type.</span></span> <span data-ttu-id="f9012-125">En este escenario, la función realiza una adición atómica del valor a la ubicación del recurso al que hace referencia dest.</span><span class="sxs-lookup"><span data-stu-id="f9012-125">In this scenario, the function performs an atomic add of the value to the resource location referenced by dest.</span></span> <span data-ttu-id="f9012-126">Por último, el tercer escenario es cuando R es un tipo de variable local.</span><span class="sxs-lookup"><span data-stu-id="f9012-126">Finally, the third scenario is when R is a local variable type.</span></span> <span data-ttu-id="f9012-127">En este escenario, la función reduce hasta una suma del valor de DEST y Value, almacenados en dest.</span><span class="sxs-lookup"><span data-stu-id="f9012-127">In this scenario, the function reduces to a sum of the value of dest and value, stored in dest.</span></span> <span data-ttu-id="f9012-128">La función sobrecargada tiene una variable de salida adicional que se establecerá en el valor original de dest.</span><span class="sxs-lookup"><span data-stu-id="f9012-128">The overloaded function has an additional output variable which will be set to the original value of dest.</span></span> <span data-ttu-id="f9012-129">Esta operación sobrecargada solo está disponible cuando R es legible y grabable.</span><span class="sxs-lookup"><span data-stu-id="f9012-129">This overloaded operation is only available when R is readable and writable.</span></span>

<span data-ttu-id="f9012-130">Esta función se admite en los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="f9012-130">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="f9012-131">VS</span><span class="sxs-lookup"><span data-stu-id="f9012-131">VS</span></span>  | <span data-ttu-id="f9012-132">!</span><span class="sxs-lookup"><span data-stu-id="f9012-132">HS</span></span>  | <span data-ttu-id="f9012-133">DS</span><span class="sxs-lookup"><span data-stu-id="f9012-133">DS</span></span>  | <span data-ttu-id="f9012-134">GS</span><span class="sxs-lookup"><span data-stu-id="f9012-134">GS</span></span>  | <span data-ttu-id="f9012-135">PS</span><span class="sxs-lookup"><span data-stu-id="f9012-135">PS</span></span>  | <span data-ttu-id="f9012-136">CS</span><span class="sxs-lookup"><span data-stu-id="f9012-136">CS</span></span>  |
|-----|-----|-----|-----|-----|-----|
| <span data-ttu-id="f9012-137">x</span><span class="sxs-lookup"><span data-stu-id="f9012-137">x</span></span>   | <span data-ttu-id="f9012-138">x</span><span class="sxs-lookup"><span data-stu-id="f9012-138">x</span></span>   | <span data-ttu-id="f9012-139">x</span><span class="sxs-lookup"><span data-stu-id="f9012-139">x</span></span>   | <span data-ttu-id="f9012-140">x</span><span class="sxs-lookup"><span data-stu-id="f9012-140">x</span></span>   | <span data-ttu-id="f9012-141">x</span><span class="sxs-lookup"><span data-stu-id="f9012-141">x</span></span>   | <span data-ttu-id="f9012-142">x</span><span class="sxs-lookup"><span data-stu-id="f9012-142">x</span></span>   |



 

## <a name="requirements"></a><span data-ttu-id="f9012-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f9012-143">Requirements</span></span>




## <a name="see-also"></a><span data-ttu-id="f9012-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="f9012-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9012-145">RWByteAddressBuffer</span><span class="sxs-lookup"><span data-stu-id="f9012-145">RWByteAddressBuffer</span></span>](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[<span data-ttu-id="f9012-146">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="f9012-146">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

