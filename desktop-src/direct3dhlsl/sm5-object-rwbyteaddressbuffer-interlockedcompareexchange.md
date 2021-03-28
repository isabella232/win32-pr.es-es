---
title: 'RWByteAddressBuffer:: InterlockedCompareExchange (función)'
description: Compara la entrada con el valor de comparación e intercambia el resultado, de forma atómica.
ms.assetid: 9d6e8d95-5157-49a7-8a79-f3ca6ba87ebb
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
ms.openlocfilehash: 18c7e5d58fe926d09e7ec48ee12a2336627d5db2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793006"
---
# <a name="interlockedcompareexchange-function"></a><span data-ttu-id="5134c-104">InterlockedCompareExchange función)</span><span class="sxs-lookup"><span data-stu-id="5134c-104">InterlockedCompareExchange function</span></span>

<span data-ttu-id="5134c-105">Compara la entrada con el valor de comparación e intercambia el resultado, de forma atómica.</span><span class="sxs-lookup"><span data-stu-id="5134c-105">Compares the input to the comparison value and exchanges the result, atomically.</span></span>

## <a name="syntax"></a><span data-ttu-id="5134c-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5134c-106">Syntax</span></span>

``` syntax
void InterlockedCompareExchange(
  in  UINT dest,
  in  UINT compare_value,
  in  UINT value,
  out UINT original_value
);
```

## <a name="parameters"></a><span data-ttu-id="5134c-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5134c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5134c-108">*dest* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5134c-108">*dest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5134c-109">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="5134c-109">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="5134c-110">Dirección de destino.</span><span class="sxs-lookup"><span data-stu-id="5134c-110">The destination address.</span></span>

</dd> <dt>

<span data-ttu-id="5134c-111">*comparar \_ valor* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="5134c-111">*compare\_value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5134c-112">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="5134c-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="5134c-113">El valor de comparación.</span><span class="sxs-lookup"><span data-stu-id="5134c-113">The comparison value.</span></span>

</dd> <dt>

<span data-ttu-id="5134c-114">*valor* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="5134c-114">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5134c-115">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="5134c-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="5134c-116">Valor de entrada.</span><span class="sxs-lookup"><span data-stu-id="5134c-116">The input value.</span></span>

</dd> <dt>

<span data-ttu-id="5134c-117">*\_ valor original* \[ fuera\]</span><span class="sxs-lookup"><span data-stu-id="5134c-117">*original\_value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5134c-118">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="5134c-118">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="5134c-119">El valor original.</span><span class="sxs-lookup"><span data-stu-id="5134c-119">The original value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5134c-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5134c-120">Return value</span></span>

<span data-ttu-id="5134c-121">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="5134c-121">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5134c-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5134c-122">Remarks</span></span>

<span data-ttu-id="5134c-123">Compara de forma atómica el valor de *dest* con *el \_ valor de comparación*, almacena el valor en *dest* si los valores coinciden, devuelve el valor original de *dest* en el *\_ valor original*.</span><span class="sxs-lookup"><span data-stu-id="5134c-123">Atomically compares the value in *dest* to *compare\_value*, stores value in *dest* if the values match, returns the original value of *dest* in *original\_value*.</span></span> <span data-ttu-id="5134c-124">Esta operación solo se puede realizar en recursos con tipo **int** o *uint* y variables de memoria compartida.</span><span class="sxs-lookup"><span data-stu-id="5134c-124">This operation can only be performed on **int** or *uint* typed resources and shared memory variables.</span></span> <span data-ttu-id="5134c-125">Hay tres usos posibles para esta función.</span><span class="sxs-lookup"><span data-stu-id="5134c-125">There are three possible uses for this function.</span></span> <span data-ttu-id="5134c-126">El primero es cuando R es un tipo de variable de memoria compartida.</span><span class="sxs-lookup"><span data-stu-id="5134c-126">The first is when R is a shared memory variable type.</span></span> <span data-ttu-id="5134c-127">En este caso, la función realiza la operación en el registro de memoria compartida al que hace referencia *dest*.</span><span class="sxs-lookup"><span data-stu-id="5134c-127">In this case, the function performs the operation on the shared memory register referenced by *dest*.</span></span> <span data-ttu-id="5134c-128">El segundo escenario es cuando R es un tipo de variable de recurso.</span><span class="sxs-lookup"><span data-stu-id="5134c-128">The second scenario is when R is a resource variable type.</span></span> <span data-ttu-id="5134c-129">En este escenario, la función realiza la operación en la ubicación del recurso a la que hace referencia *dest*.</span><span class="sxs-lookup"><span data-stu-id="5134c-129">In this scenario, the function performs the operation on the resource location referenced by *dest*.</span></span> <span data-ttu-id="5134c-130">Por último, el tercer escenario es cuando R es un tipo de variable local.</span><span class="sxs-lookup"><span data-stu-id="5134c-130">Finally, the third scenario is when R is a local variable type.</span></span> <span data-ttu-id="5134c-131">En este escenario, la función reduce a la operación realizada mediante operaciones locales.</span><span class="sxs-lookup"><span data-stu-id="5134c-131">In this scenario, the function reduces to the operation performed using local operations.</span></span> <span data-ttu-id="5134c-132">Esta operación solo está disponible cuando R es legible y grabable.</span><span class="sxs-lookup"><span data-stu-id="5134c-132">This operation is only available when R is readable and writable.</span></span>

> [!Note]  
> <span data-ttu-id="5134c-133">Si llama a **InterlockedCompareExchange** en un bucle for o [**While**](dx-graphics-hlsl-while.md) del sombreador [**de**](dx-graphics-hlsl-for.md) cálculo, para compilar correctamente, debe usar el atributo **\[ Allow \_ UAV \_ Condition \]** en dicho bucle.</span><span class="sxs-lookup"><span data-stu-id="5134c-133">If you call **InterlockedCompareExchange** in a [**for**](dx-graphics-hlsl-for.md) or [**while**](dx-graphics-hlsl-while.md) compute shader loop, to properly compile, you must use the **\[allow\_uav\_condition\]** attribute on that loop.</span></span>

 

<span data-ttu-id="5134c-134">Esta función se admite en los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="5134c-134">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="5134c-135">VS</span><span class="sxs-lookup"><span data-stu-id="5134c-135">VS</span></span>  | <span data-ttu-id="5134c-136">!</span><span class="sxs-lookup"><span data-stu-id="5134c-136">HS</span></span>  | <span data-ttu-id="5134c-137">DS</span><span class="sxs-lookup"><span data-stu-id="5134c-137">DS</span></span>  | <span data-ttu-id="5134c-138">GS</span><span class="sxs-lookup"><span data-stu-id="5134c-138">GS</span></span>  | <span data-ttu-id="5134c-139">PS</span><span class="sxs-lookup"><span data-stu-id="5134c-139">PS</span></span>  | <span data-ttu-id="5134c-140">CS</span><span class="sxs-lookup"><span data-stu-id="5134c-140">CS</span></span>  |
|-----|-----|-----|-----|-----|-----|
| <span data-ttu-id="5134c-141">x</span><span class="sxs-lookup"><span data-stu-id="5134c-141">x</span></span>   | <span data-ttu-id="5134c-142">x</span><span class="sxs-lookup"><span data-stu-id="5134c-142">x</span></span>   | <span data-ttu-id="5134c-143">x</span><span class="sxs-lookup"><span data-stu-id="5134c-143">x</span></span>   | <span data-ttu-id="5134c-144">x</span><span class="sxs-lookup"><span data-stu-id="5134c-144">x</span></span>   | <span data-ttu-id="5134c-145">x</span><span class="sxs-lookup"><span data-stu-id="5134c-145">x</span></span>   | <span data-ttu-id="5134c-146">x</span><span class="sxs-lookup"><span data-stu-id="5134c-146">x</span></span>   |



 

## <a name="see-also"></a><span data-ttu-id="5134c-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="5134c-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5134c-148">RWByteAddressBuffer</span><span class="sxs-lookup"><span data-stu-id="5134c-148">RWByteAddressBuffer</span></span>](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[<span data-ttu-id="5134c-149">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="5134c-149">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 