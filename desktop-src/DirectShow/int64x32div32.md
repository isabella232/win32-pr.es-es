---
description: La función Int64x32Div32 implementa la fórmula ((a \* b) + RND)/c, donde a es un valor de 64 bits y b, c y RND son valores de 32 bits.
ms.assetid: 566ac194-5b15-43b7-aa7c-0c18c6f69691
title: Función Int64x32Div32 (Wxutil. h)
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
ms.openlocfilehash: de60ca08b262dbf97aa118bd115bd6dc58576a1d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680962"
---
# <a name="int64x32div32-function"></a><span data-ttu-id="ec71c-103">Int64x32Div32 función)</span><span class="sxs-lookup"><span data-stu-id="ec71c-103">Int64x32Div32 function</span></span>

<span data-ttu-id="ec71c-104">La `Int64x32Div32` función implementa la fórmula `((a*b)+rnd)/c` donde *a* es un valor de 64 bits y *b*, *c* y *RND* son valores de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="ec71c-104">The `Int64x32Div32` function implements the formula `((a*b)+rnd)/c` where *a* is a 64-bit value and *b*, *c*, and *rnd* are 32-bit values.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec71c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ec71c-105">Syntax</span></span>


```C++
LONGLONG WINAPI Int64x32Div32(
   LONGLONG a,
   LONG     b,
   LONG     c,
   LONG     rnd
);
```



## <a name="parameters"></a><span data-ttu-id="ec71c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ec71c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec71c-107">*un*</span><span class="sxs-lookup"><span data-stu-id="ec71c-107">*a*</span></span> 
</dt> <dd>

<span data-ttu-id="ec71c-108">Multiplicando.</span><span class="sxs-lookup"><span data-stu-id="ec71c-108">Multiplicand.</span></span>

</dd> <dt>

<span data-ttu-id="ec71c-109">*b*</span><span class="sxs-lookup"><span data-stu-id="ec71c-109">*b*</span></span> 
</dt> <dd>

<span data-ttu-id="ec71c-110">Multiplicador.</span><span class="sxs-lookup"><span data-stu-id="ec71c-110">Multiplier.</span></span>

</dd> <dt>

<span data-ttu-id="ec71c-111">*c*</span><span class="sxs-lookup"><span data-stu-id="ec71c-111">*c*</span></span> 
</dt> <dd>

<span data-ttu-id="ec71c-112">Divisor.</span><span class="sxs-lookup"><span data-stu-id="ec71c-112">Divisor.</span></span>

</dd> <dt>

<span data-ttu-id="ec71c-113">*NúmAleat*</span><span class="sxs-lookup"><span data-stu-id="ec71c-113">*rnd*</span></span> 
</dt> <dd>

<span data-ttu-id="ec71c-114">Factor de redondeo.</span><span class="sxs-lookup"><span data-stu-id="ec71c-114">Rounding factor.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ec71c-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ec71c-115">Return value</span></span>

<span data-ttu-id="ec71c-116">Devuelve el `(a * b + rnd)/c` cálculo o uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="ec71c-116">Returns either the `(a * b + rnd)/c` calculation or one of the following values.</span></span>



| <span data-ttu-id="ec71c-117">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="ec71c-117">Return code</span></span>                                                                                       | <span data-ttu-id="ec71c-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="ec71c-118">Description</span></span>                                                              |
|---------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ec71c-119"><dt>**0x7FFFFFFFFFFFFFFF**</dt></span><span class="sxs-lookup"><span data-stu-id="ec71c-119"><dt>**0x7FFFFFFFFFFFFFFF**</dt></span></span> </dl> | <span data-ttu-id="ec71c-120">Se produjo un desbordamiento porque el resultado es demasiado grande (positivo).</span><span class="sxs-lookup"><span data-stu-id="ec71c-120">Overflow occurred because the result is too large (positive).</span></span><br/> |
| <dl> <span data-ttu-id="ec71c-121"><dt>**0x8000000000000000**</dt></span><span class="sxs-lookup"><span data-stu-id="ec71c-121"><dt>**0x8000000000000000**</dt></span></span> </dl> | <span data-ttu-id="ec71c-122">Se produjo un desbordamiento porque el resultado es demasiado grande (negativo).</span><span class="sxs-lookup"><span data-stu-id="ec71c-122">Overflow occurred because the result is too large (negative).</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ec71c-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ec71c-123">Remarks</span></span>

<span data-ttu-id="ec71c-124">El redondeo en la división es hacia cero.</span><span class="sxs-lookup"><span data-stu-id="ec71c-124">Rounding on the division is toward zero.</span></span> <span data-ttu-id="ec71c-125">La división por cero se cuenta como una condición de desbordamiento.</span><span class="sxs-lookup"><span data-stu-id="ec71c-125">Division by zero is counted as an overflow condition.</span></span>

<span data-ttu-id="ec71c-126">Las marcas de tiempo y los tiempos de búsqueda son valores de 64 bits, por lo que esta función es útil para realizar conversiones en sistemas de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="ec71c-126">Time stamps and seek times are 64-bit values, so this function is useful for performing conversions on 32-bit systems.</span></span> <span data-ttu-id="ec71c-127">Por ejemplo, en MPEG-1, la referencia del reloj del sistema es 90 kHz o 90.000 TICs por segundo.</span><span class="sxs-lookup"><span data-stu-id="ec71c-127">For example, in MPEG-1 the system clock reference is 90-kHz, or 90,000 ticks per second.</span></span> <span data-ttu-id="ec71c-128">La fórmula que se va a convertir en el tiempo de referencia (unidades 100-nanosegundos) es</span><span class="sxs-lookup"><span data-stu-id="ec71c-128">The formula to convert this to reference time (100-nanosecond units) is</span></span>


```C++
(timestamp * 1000) / 9
```



<span data-ttu-id="ec71c-129">que se puede calcular como `Int64x32Div32(timestamp, 1000, 9, 0)` .</span><span class="sxs-lookup"><span data-stu-id="ec71c-129">which can be calculated as `Int64x32Div32(timestamp, 1000, 9, 0)`.</span></span> <span data-ttu-id="ec71c-130">Use el parámetro *RND* como factor de redondeo.</span><span class="sxs-lookup"><span data-stu-id="ec71c-130">Use the *rnd* parameter as a rounding factor.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec71c-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ec71c-131">Requirements</span></span>



| <span data-ttu-id="ec71c-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="ec71c-132">Requirement</span></span> | <span data-ttu-id="ec71c-133">Value</span><span class="sxs-lookup"><span data-stu-id="ec71c-133">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec71c-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ec71c-134">Header</span></span><br/>  | <dl> <span data-ttu-id="ec71c-135"><dt>Wxutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ec71c-135"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="ec71c-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ec71c-136">Library</span></span><br/> | <dl> <span data-ttu-id="ec71c-137"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="ec71c-137"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ec71c-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="ec71c-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec71c-139">Funciones auxiliares misceláneas</span><span class="sxs-lookup"><span data-stu-id="ec71c-139">Miscellaneous Helper Functions</span></span>](miscellaneous-helper-functions.md)
</dt> <dt>

[<span data-ttu-id="ec71c-140">**llMulDiv**</span><span class="sxs-lookup"><span data-stu-id="ec71c-140">**llMulDiv**</span></span>](llmuldiv.md)
</dt> </dl>

 

 




