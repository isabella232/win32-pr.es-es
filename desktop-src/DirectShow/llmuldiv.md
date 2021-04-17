---
description: La función llMulDiv implementa la fórmula ((a \* b) + RND)/c, donde cada término es un valor de 64 bits.
ms.assetid: cd5073b9-27c7-42ee-8487-2d4ea29f77d4
title: función llMulDiv (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Int64x32Div32
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e45d22eec1536517bd2b57d875dd596e4a1e28db
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670753"
---
# <a name="llmuldiv-function"></a><span data-ttu-id="5ad81-103">llMulDiv función)</span><span class="sxs-lookup"><span data-stu-id="5ad81-103">llMulDiv function</span></span>

<span data-ttu-id="5ad81-104">La `llMulDiv` función implementa la fórmula `((a*b)+rnd)/c` donde cada término es un valor de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="5ad81-104">The `llMulDiv` function implements the formula `((a*b)+rnd)/c` where each term is a 64-bit value.</span></span>

<span data-ttu-id="5ad81-105">Las marcas de tiempo y los tiempos de búsqueda son valores de 64 bits, por lo que esta función es útil para realizar conversiones en sistemas de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="5ad81-105">Time stamps and seek times are 64-bit values, so this function is useful for performing conversions on 32-bit systems.</span></span> <span data-ttu-id="5ad81-106">Por ejemplo, la fórmula para bytes por segundo es</span><span class="sxs-lookup"><span data-stu-id="5ad81-106">For example, the formula for bytes-per-second is</span></span>


```C++
(Number of Bytes * Reference Time) / 10,000,000
```



<span data-ttu-id="5ad81-107">que se puede calcular como `llMulDiv(nBytes, rtTime, 10000000, 0)` .</span><span class="sxs-lookup"><span data-stu-id="5ad81-107">which can be calculated as `llMulDiv(nBytes, rtTime, 10000000, 0)`.</span></span> <span data-ttu-id="5ad81-108">Use el parámetro *RND* como factor de redondeo.</span><span class="sxs-lookup"><span data-stu-id="5ad81-108">Use the *rnd* parameter as a rounding factor.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ad81-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5ad81-109">Syntax</span></span>


```C++
LONGLONG WINAPI Int64x32Div32(
   LONGLONG a,
   LONGLONG b,
   LONGLONG c,
   LONGLONG rnd
);
```



## <a name="parameters"></a><span data-ttu-id="5ad81-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5ad81-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ad81-111">*un*</span><span class="sxs-lookup"><span data-stu-id="5ad81-111">*a*</span></span> 
</dt> <dd>

<span data-ttu-id="5ad81-112">Multiplicando.</span><span class="sxs-lookup"><span data-stu-id="5ad81-112">Multiplicand.</span></span>

</dd> <dt>

<span data-ttu-id="5ad81-113">*b*</span><span class="sxs-lookup"><span data-stu-id="5ad81-113">*b*</span></span> 
</dt> <dd>

<span data-ttu-id="5ad81-114">Multiplicador.</span><span class="sxs-lookup"><span data-stu-id="5ad81-114">Multiplier.</span></span>

</dd> <dt>

<span data-ttu-id="5ad81-115">*c*</span><span class="sxs-lookup"><span data-stu-id="5ad81-115">*c*</span></span> 
</dt> <dd>

<span data-ttu-id="5ad81-116">Divisor.</span><span class="sxs-lookup"><span data-stu-id="5ad81-116">Divisor.</span></span>

</dd> <dt>

<span data-ttu-id="5ad81-117">*NúmAleat*</span><span class="sxs-lookup"><span data-stu-id="5ad81-117">*rnd*</span></span> 
</dt> <dd>

<span data-ttu-id="5ad81-118">Factor de redondeo.</span><span class="sxs-lookup"><span data-stu-id="5ad81-118">Rounding factor.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ad81-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5ad81-119">Return value</span></span>

<span data-ttu-id="5ad81-120">Devuelve el `(a * b + rnd)/c` cálculo o uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="5ad81-120">Returns either the `(a * b + rnd)/c` calculation or one of the following values.</span></span>



| <span data-ttu-id="5ad81-121">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="5ad81-121">Return code</span></span>                                                                                       | <span data-ttu-id="5ad81-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="5ad81-122">Description</span></span>                                                              |
|---------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5ad81-123"><dt>**0x7FFFFFFFFFFFFFFF**</dt></span><span class="sxs-lookup"><span data-stu-id="5ad81-123"><dt>**0x7FFFFFFFFFFFFFFF**</dt></span></span> </dl> | <span data-ttu-id="5ad81-124">Se produjo un desbordamiento porque el resultado es demasiado grande (positivo).</span><span class="sxs-lookup"><span data-stu-id="5ad81-124">Overflow occurred because the result is too large (positive).</span></span><br/> |
| <dl> <span data-ttu-id="5ad81-125"><dt>**0x8000000000000000**</dt></span><span class="sxs-lookup"><span data-stu-id="5ad81-125"><dt>**0x8000000000000000**</dt></span></span> </dl> | <span data-ttu-id="5ad81-126">Se produjo un desbordamiento porque el resultado es demasiado grande (negativo).</span><span class="sxs-lookup"><span data-stu-id="5ad81-126">Overflow occurred because the result is too large (negative).</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="5ad81-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5ad81-127">Remarks</span></span>

<span data-ttu-id="5ad81-128">El redondeo en la división es hacia cero.</span><span class="sxs-lookup"><span data-stu-id="5ad81-128">Rounding on the division is toward zero.</span></span> <span data-ttu-id="5ad81-129">La división por cero se cuenta como una condición de desbordamiento.</span><span class="sxs-lookup"><span data-stu-id="5ad81-129">Division by zero is counted as an overflow condition.</span></span>

## <a name="requirements"></a><span data-ttu-id="5ad81-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5ad81-130">Requirements</span></span>



| <span data-ttu-id="5ad81-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="5ad81-131">Requirement</span></span> | <span data-ttu-id="5ad81-132">Value</span><span class="sxs-lookup"><span data-stu-id="5ad81-132">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ad81-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5ad81-133">Header</span></span><br/>  | <dl> <span data-ttu-id="5ad81-134"><dt>Wxutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5ad81-134"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="5ad81-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5ad81-135">Library</span></span><br/> | <dl> <span data-ttu-id="5ad81-136"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="5ad81-136"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ad81-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="5ad81-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ad81-138">Funciones auxiliares misceláneas</span><span class="sxs-lookup"><span data-stu-id="5ad81-138">Miscellaneous Helper Functions</span></span>](miscellaneous-helper-functions.md)
</dt> <dt>

[<span data-ttu-id="5ad81-139">**Int64x32Div32**</span><span class="sxs-lookup"><span data-stu-id="5ad81-139">**Int64x32Div32**</span></span>](int64x32div32.md)
</dt> </dl>

 

 




