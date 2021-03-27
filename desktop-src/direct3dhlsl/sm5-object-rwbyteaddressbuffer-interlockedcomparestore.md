---
title: 'RWByteAddressBuffer:: InterlockedCompareStore (función)'
description: Ccompares la entrada al valor de comparación, de forma atómica.
ms.assetid: d82a73b6-24a5-4eb3-9f20-15ba263c93d0
keywords:
- InterlockedCompareStore de función HLSL
topic_type:
- apiref
api_name:
- InterlockedCompareStore
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: abaa390ba74657e42b54a5147a7bc4006564a5fb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103904737"
---
# <a name="interlockedcomparestore-function"></a><span data-ttu-id="dc340-104">InterlockedCompareStore función)</span><span class="sxs-lookup"><span data-stu-id="dc340-104">InterlockedCompareStore function</span></span>

<span data-ttu-id="dc340-105">Ccompares la entrada al valor de comparación, de forma atómica.</span><span class="sxs-lookup"><span data-stu-id="dc340-105">Ccompares the input to the comparison value, atomically.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc340-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dc340-106">Syntax</span></span>

``` syntax
void InterlockedCompareStore(
  in UINT dest,
  in UINT compare_value,
  in UINT value
);
```

## <a name="parameters"></a><span data-ttu-id="dc340-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dc340-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc340-108">*dest* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="dc340-108">*dest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc340-109">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="dc340-109">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="dc340-110">Dirección de destino.</span><span class="sxs-lookup"><span data-stu-id="dc340-110">The destination address.</span></span>

</dd> <dt>

<span data-ttu-id="dc340-111">*comparar \_ valor* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="dc340-111">*compare\_value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc340-112">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="dc340-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="dc340-113">El valor de comparación.</span><span class="sxs-lookup"><span data-stu-id="dc340-113">The comparison value.</span></span>

</dd> <dt>

<span data-ttu-id="dc340-114">*valor* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="dc340-114">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc340-115">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="dc340-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="dc340-116">Valor de entrada.</span><span class="sxs-lookup"><span data-stu-id="dc340-116">The input value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dc340-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dc340-117">Return value</span></span>

<span data-ttu-id="dc340-118">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="dc340-118">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="dc340-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dc340-119">Remarks</span></span>

<span data-ttu-id="dc340-120">Esta operación solo se puede realizar en recursos con tipo int o uint y variables de memoria compartida.</span><span class="sxs-lookup"><span data-stu-id="dc340-120">This operation can only be performed on int or uint typed resources and shared memory variables.</span></span> <span data-ttu-id="dc340-121">Hay tres usos posibles para esta función.</span><span class="sxs-lookup"><span data-stu-id="dc340-121">There are three possible uses for this function.</span></span> <span data-ttu-id="dc340-122">El primero es cuando R es un tipo de variable de memoria compartida.</span><span class="sxs-lookup"><span data-stu-id="dc340-122">The first is when R is a shared memory variable type.</span></span> <span data-ttu-id="dc340-123">En este caso, la función realiza la operación en el registro de memoria compartida al que hace referencia dest.</span><span class="sxs-lookup"><span data-stu-id="dc340-123">In this case, the function performs the operation on the shared memory register referenced by dest.</span></span> <span data-ttu-id="dc340-124">El segundo escenario es cuando R es un tipo de variable de recurso.</span><span class="sxs-lookup"><span data-stu-id="dc340-124">The second scenario is when R is a resource variable type.</span></span> <span data-ttu-id="dc340-125">En este escenario, la función realiza la operación en la ubicación del recurso a la que hace referencia dest.</span><span class="sxs-lookup"><span data-stu-id="dc340-125">In this scenario, the function performs the operation on the resource location referenced by dest.</span></span> <span data-ttu-id="dc340-126">Por último, el tercer escenario es cuando R es un tipo de variable local.</span><span class="sxs-lookup"><span data-stu-id="dc340-126">Finally, the third scenario is when R is a local variable type.</span></span> <span data-ttu-id="dc340-127">En este escenario, la función reduce a la operación realizada mediante operaciones locales.</span><span class="sxs-lookup"><span data-stu-id="dc340-127">In this scenario, the function reduces to the operation performed using local operations.</span></span>

<span data-ttu-id="dc340-128">Esta función se admite en los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="dc340-128">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="dc340-129">VS</span><span class="sxs-lookup"><span data-stu-id="dc340-129">VS</span></span>  | <span data-ttu-id="dc340-130">!</span><span class="sxs-lookup"><span data-stu-id="dc340-130">HS</span></span>  | <span data-ttu-id="dc340-131">DS</span><span class="sxs-lookup"><span data-stu-id="dc340-131">DS</span></span>  | <span data-ttu-id="dc340-132">GS</span><span class="sxs-lookup"><span data-stu-id="dc340-132">GS</span></span>  | <span data-ttu-id="dc340-133">PS</span><span class="sxs-lookup"><span data-stu-id="dc340-133">PS</span></span>  | <span data-ttu-id="dc340-134">CS</span><span class="sxs-lookup"><span data-stu-id="dc340-134">CS</span></span>  |
|-----|-----|-----|-----|-----|-----|
| <span data-ttu-id="dc340-135">x</span><span class="sxs-lookup"><span data-stu-id="dc340-135">x</span></span>   | <span data-ttu-id="dc340-136">x</span><span class="sxs-lookup"><span data-stu-id="dc340-136">x</span></span>   | <span data-ttu-id="dc340-137">x</span><span class="sxs-lookup"><span data-stu-id="dc340-137">x</span></span>   | <span data-ttu-id="dc340-138">x</span><span class="sxs-lookup"><span data-stu-id="dc340-138">x</span></span>   | <span data-ttu-id="dc340-139">x</span><span class="sxs-lookup"><span data-stu-id="dc340-139">x</span></span>   | <span data-ttu-id="dc340-140">x</span><span class="sxs-lookup"><span data-stu-id="dc340-140">x</span></span>   |



 

## <a name="see-also"></a><span data-ttu-id="dc340-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="dc340-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc340-142">RWByteAddressBuffer</span><span class="sxs-lookup"><span data-stu-id="dc340-142">RWByteAddressBuffer</span></span>](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[<span data-ttu-id="dc340-143">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="dc340-143">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 