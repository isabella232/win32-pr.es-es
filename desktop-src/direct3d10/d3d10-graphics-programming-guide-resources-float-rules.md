---
description: Direct3D 10 admite varias representaciones de punto flotante diferentes. Todos los cálculos de punto flotante operan en un subconjunto definido del comportamiento de punto flotante de precisión única de IEEE 754 32 bits.
ms.assetid: 57221d13-8993-4db3-b1a0-88bdcf6f0167
title: Reglas de punto FFloating (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6909d037b11f9098bb3e0dbad0f1846b79b513e8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705292"
---
# <a name="floating-point-rules-direct3d-10"></a><span data-ttu-id="ea4f6-104">Reglas de punto flotante (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="ea4f6-104">Floating-point rules (Direct3D 10)</span></span>

<span data-ttu-id="ea4f6-105">Direct3D 10 admite varias representaciones de punto flotante diferentes.</span><span class="sxs-lookup"><span data-stu-id="ea4f6-105">Direct3D 10 supports several different floating-point representations.</span></span> <span data-ttu-id="ea4f6-106">Todos los cálculos de punto flotante operan en un subconjunto definido del comportamiento de punto flotante de precisión única de IEEE 754 32 bits.</span><span class="sxs-lookup"><span data-stu-id="ea4f6-106">All floating-point computations operate under a defined subset of the IEEE 754 32-bit single precision floating-point behavior.</span></span>

-   [<span data-ttu-id="ea4f6-107">Reglas de Floating-Point de bits de 32</span><span class="sxs-lookup"><span data-stu-id="ea4f6-107">32-bit Floating-Point Rules</span></span>](#32-bit-floating-point-rules)
    -   [<span data-ttu-id="ea4f6-108">Reglas IEEE-754 aceptadas</span><span class="sxs-lookup"><span data-stu-id="ea4f6-108">Honored IEEE-754 Rules</span></span>](#honored-ieee-754-rules)
    -   [<span data-ttu-id="ea4f6-109">Desviaciones o requisitos adicionales de las reglas IEEE-754</span><span class="sxs-lookup"><span data-stu-id="ea4f6-109">Deviations or Additional Requirements from IEEE-754 Rules</span></span>](#deviations-or-additional-requirements-from-ieee-754-rules)
-   [<span data-ttu-id="ea4f6-110">Reglas de Floating-Point de 16 bits</span><span class="sxs-lookup"><span data-stu-id="ea4f6-110">16-bit Floating-Point Rules</span></span>](#16-bit-floating-point-rules)
-   [<span data-ttu-id="ea4f6-111">Reglas de Floating-Point de 11 bits y de 10 bits</span><span class="sxs-lookup"><span data-stu-id="ea4f6-111">11-bit and 10-bit Floating-Point Rules</span></span>](#11-bit-and-10-bit-floating-point-rules)
-   [<span data-ttu-id="ea4f6-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ea4f6-112">Related topics</span></span>](#related-topics)

## <a name="32-bit-floating-point-rules"></a><span data-ttu-id="ea4f6-113">Reglas de Floating-Point de bits de 32</span><span class="sxs-lookup"><span data-stu-id="ea4f6-113">32-bit Floating-Point Rules</span></span>

<span data-ttu-id="ea4f6-114">Hay dos conjuntos de reglas: los que cumplen con IEEE-754 y los que se desvían del estándar.</span><span class="sxs-lookup"><span data-stu-id="ea4f6-114">There are two sets of rules: those that conform to IEEE-754, and those that deviate from the standard.</span></span>

### <a name="honored-ieee-754-rules"></a><span data-ttu-id="ea4f6-115">Reglas IEEE-754 aceptadas</span><span class="sxs-lookup"><span data-stu-id="ea4f6-115">Honored IEEE-754 Rules</span></span>

<span data-ttu-id="ea4f6-116">Algunas de estas reglas son una opción única en la que IEEE-754 ofrece opciones.</span><span class="sxs-lookup"><span data-stu-id="ea4f6-116">Some of these rules are a single option where IEEE-754 offers choices.</span></span>

-   <span data-ttu-id="ea4f6-117">La división por 0 produce +/-INF, excepto 0/0, que tiene como resultado NaN.</span><span class="sxs-lookup"><span data-stu-id="ea4f6-117">Divide by 0 produces +/- INF, except 0/0 which results in NaN.</span></span>
-   <span data-ttu-id="ea4f6-118">el registro de (+/-) 0 produce-INF.</span><span class="sxs-lookup"><span data-stu-id="ea4f6-118">log of (+/-) 0 produces -INF.</span></span> <span data-ttu-id="ea4f6-119">el registro de un valor negativo (distinto de-0) genera NaN.</span><span class="sxs-lookup"><span data-stu-id="ea4f6-119">log of a negative value (other than -0) produces NaN.</span></span>
-   <span data-ttu-id="ea4f6-120">La raíz cuadrada recíproca (RSQ) o la raíz cuadrada (sqrt) de un número negativo produce NaN.</span><span class="sxs-lookup"><span data-stu-id="ea4f6-120">Reciprocal square root (rsq) or square root (sqrt) of a negative number produces NaN.</span></span> <span data-ttu-id="ea4f6-121">La excepción es-0; sqrt (-0) produce-0 y RSQ (-0) produce-INF.</span><span class="sxs-lookup"><span data-stu-id="ea4f6-121">The exception is -0; sqrt(-0) produces -0, and rsq(-0) produces -INF.</span></span>
-   <span data-ttu-id="ea4f6-122">INF-INF = NaN</span><span class="sxs-lookup"><span data-stu-id="ea4f6-122">INF - INF = NaN</span></span>
-   <span data-ttu-id="ea4f6-123">(+/-) INF/(+/-) INF = NaN</span><span class="sxs-lookup"><span data-stu-id="ea4f6-123">(+/-)INF / (+/-)INF = NaN</span></span>
-   <span data-ttu-id="ea4f6-124">(+/-) INF \* 0 = Nan</span><span class="sxs-lookup"><span data-stu-id="ea4f6-124">(+/-)INF \* 0 = NaN</span></span>
-   <span data-ttu-id="ea4f6-125">NaN (cualquier OP) any-Value = NaN</span><span class="sxs-lookup"><span data-stu-id="ea4f6-125">NaN (any OP) any-value = NaN</span></span>
-   <span data-ttu-id="ea4f6-126">Las comparaciones EQ, GT, GE, LT y LE, cuando uno o ambos operandos es NaN devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="ea4f6-126">The comparisons EQ, GT, GE, LT, and LE, when either or both operands is NaN returns **FALSE**.</span></span>
-   <span data-ttu-id="ea4f6-127">Las comparaciones omiten el signo de 0 (por lo que + 0 es igual a-0).</span><span class="sxs-lookup"><span data-stu-id="ea4f6-127">Comparisons ignore the sign of 0 (so +0 equals -0).</span></span>
-   <span data-ttu-id="ea4f6-128">La comparación NE, cuando uno o ambos operandos son NaN, devuelve **true**.</span><span class="sxs-lookup"><span data-stu-id="ea4f6-128">The comparison NE, when either or both operands is NaN returns **TRUE**.</span></span>
-   <span data-ttu-id="ea4f6-129">Las comparaciones de cualquier valor que no sea NaN con +/-INF devuelven el resultado correcto.</span><span class="sxs-lookup"><span data-stu-id="ea4f6-129">Comparisons of any non-NaN value against +/- INF return the correct result.</span></span>

### <a name="deviations-or-additional-requirements-from-ieee-754-rules"></a><span data-ttu-id="ea4f6-130">Desviaciones o requisitos adicionales de las reglas IEEE-754</span><span class="sxs-lookup"><span data-stu-id="ea4f6-130">Deviations or Additional Requirements from IEEE-754 Rules</span></span>

-   <span data-ttu-id="ea4f6-131">IEEE-754 requiere operaciones de punto flotante para producir un resultado que es el valor representable más cercano a un resultado infinitamente preciso, conocido como de redondeo a la más cercana.</span><span class="sxs-lookup"><span data-stu-id="ea4f6-131">IEEE-754 requires floating-point operations to produce a result that is the nearest representable value to an infinitely-precise result, known as round-to-nearest-even.</span></span> <span data-ttu-id="ea4f6-132">Direct3D 10, sin embargo, define un requisito menos flexible: las operaciones de punto flotante de 32 bits producen un resultado que se encuentra dentro de una unidad: último lugar (1 ULP) del resultado infinitamente preciso.</span><span class="sxs-lookup"><span data-stu-id="ea4f6-132">Direct3D 10, however, defines a looser requirement: 32-bit floating-point operations produce a result that is within one unit-last-place (1 ULP) of the infinitely-precise result.</span></span> <span data-ttu-id="ea4f6-133">Esto significa que, por ejemplo, se permite que el hardware trunque los resultados en 32 bits en lugar de realizar una operación de ida y vuelta más cercana, ya que esto daría como resultado un error de al menos un ULP.</span><span class="sxs-lookup"><span data-stu-id="ea4f6-133">This means that, for example, hardware is allowed to truncate results to 32-bit rather than perform round-to-nearest-even, as that would result in error of at most one ULP.</span></span>
-   <span data-ttu-id="ea4f6-134">No se admiten excepciones de punto flotante, bits de estado ni capturas.</span><span class="sxs-lookup"><span data-stu-id="ea4f6-134">There is no support for floating-point exceptions, status bits or traps.</span></span>
-   <span data-ttu-id="ea4f6-135">Las decimales se vacían en cero con signo en la entrada y la salida de cualquier operación matemática de punto flotante.</span><span class="sxs-lookup"><span data-stu-id="ea4f6-135">Denorms are flushed to sign-preserved zero on input and output of any floating-point mathematical operation.</span></span> <span data-ttu-id="ea4f6-136">Se realizan excepciones para cualquier operación de movimiento de datos e/s que no manipule los datos.</span><span class="sxs-lookup"><span data-stu-id="ea4f6-136">Exceptions are made for any I/O or data movement operation that does not manipulate the data.</span></span>
-   <span data-ttu-id="ea4f6-137">Los Estados que contienen valores de punto flotante, como viewport MinDepth/MaxDepth, valores BorderColor, etc., se pueden proporcionar como valores de desnormativo y se pueden vaciar o no antes de que el hardware los use.</span><span class="sxs-lookup"><span data-stu-id="ea4f6-137">States that contain floating-point values, such as Viewport MinDepth/MaxDepth, BorderColor values etc., may be provided as denorm values and may or may not be flushed before use by the hardware.</span></span>
-   <span data-ttu-id="ea4f6-138">Las operaciones min o Max vacían las desnormativas para la comparación, pero el resultado se puede vaciar o no.</span><span class="sxs-lookup"><span data-stu-id="ea4f6-138">Min or max operations flush denorms for comparison, but the result may or may not be denorm flushed.</span></span>
-   <span data-ttu-id="ea4f6-139">La entrada de NaN en una operación siempre produce NaN en la salida; sin embargo, no es necesario que el patrón de bits exacto del NaN siga siendo el mismo (a menos que la operación sea una instrucción de movimiento sin procesar, que no modifica los datos en absoluto).</span><span class="sxs-lookup"><span data-stu-id="ea4f6-139">NaN input to an operation always produces NaN on output, however the exact bit pattern of the NaN is not required to stay the same (unless the operation is a raw move instruction - which does not alter data at all.)</span></span>
-   <span data-ttu-id="ea4f6-140">Las operaciones min o Max para las que solo un operando es NaN devuelven el otro operando como resultado (contrariamente a las reglas de comparación anteriores).</span><span class="sxs-lookup"><span data-stu-id="ea4f6-140">Min or max operations for which only one operand is NaN return the other operand as the result (contrary to comparison rules above).</span></span> <span data-ttu-id="ea4f6-141">Se trata de una nueva regla IEEE (IEEE 754R), requerida en Direct3D 10.</span><span class="sxs-lookup"><span data-stu-id="ea4f6-141">This is a new IEEE rule (IEEE 754R), required in Direct3D 10.</span></span>
-   <span data-ttu-id="ea4f6-142">Otra nueva regla de IEEE 754R es que min (-0, + 0) = = min (+ 0,-0) = =-0 y Max (-0, + 0) = = Max (+ 0,-0) = = + 0, que respetan el signo, a diferencia de las reglas de comparación de cero con signo (indicado anteriormente).</span><span class="sxs-lookup"><span data-stu-id="ea4f6-142">Another new IEEE 754R rule is that min(-0,+0) == min(+0,-0) == -0, and max(-0,+0) == max(+0,-0) == +0, which honor the sign, in contrast to the comparison rules for signed zero (stated above).</span></span> <span data-ttu-id="ea4f6-143">Direct3D 10 recomienda el comportamiento de IEEE 754R aquí, pero no se aplicará; se permite que el resultado de comparar ceros sea dependiente del orden de los parámetros, mediante una comparación que omite los signos.</span><span class="sxs-lookup"><span data-stu-id="ea4f6-143">Direct3D 10 recommends the IEEE 754R behavior here, but it will not be enforced; it is permissible for the result of comparing zeros to be dependent on the order of parameters, using a comparison that ignores the signs.</span></span>
-   <span data-ttu-id="ea4f6-144">x \* 1.0 f siempre produce x (excepto desnormalización).</span><span class="sxs-lookup"><span data-stu-id="ea4f6-144">x\*1.0f always results in x (except denorm flushed).</span></span>
-   <span data-ttu-id="ea4f6-145">x/1.0 f siempre produce x (excepto desnormalización).</span><span class="sxs-lookup"><span data-stu-id="ea4f6-145">x/1.0f always results in x (except denorm flushed).</span></span>
-   <span data-ttu-id="ea4f6-146">x +/-0.0 f siempre da como resultado x (excepto desnormalización desactivada).</span><span class="sxs-lookup"><span data-stu-id="ea4f6-146">x +/- 0.0f always results in x (except denorm flushed).</span></span> <span data-ttu-id="ea4f6-147">Pero-0 + 0 = + 0.</span><span class="sxs-lookup"><span data-stu-id="ea4f6-147">But -0 + 0 = +0.</span></span>
-   <span data-ttu-id="ea4f6-148">Las operaciones con fusibles (como Mad, DP3) producen resultados que no son menos precisos que los peores pedidos de evaluación en serie de la evaluación de la expansión sin fusibles de la operación.</span><span class="sxs-lookup"><span data-stu-id="ea4f6-148">Fused operations (such as mad, dp3) produce results that are no less accurate than the worst possible serial ordering of evaluation of the unfused expansion of the operation.</span></span> <span data-ttu-id="ea4f6-149">Tenga en cuenta que la definición del peor orden posible, con fines de tolerancia, no es una definición fija para una operación fusionada determinada; depende de los valores concretos de las entradas.</span><span class="sxs-lookup"><span data-stu-id="ea4f6-149">Note that the definition of the worst possible ordering, for the purpose of tolerance, is not a fixed definition for a given fused operation; it depends on the particular values of the inputs.</span></span> <span data-ttu-id="ea4f6-150">En los pasos individuales de la expansión sin fusibles se les permite una tolerancia ULP permitida (o, para las instrucciones que Direct3D 10 llama con una tolerancia más LAX que 1 ULP, se permite la tolerancia más LAX).</span><span class="sxs-lookup"><span data-stu-id="ea4f6-150">The individual steps in the unfused expansion are each allowed 1 ULP tolerance (or for any instructions Direct3D 10 calls out with a more lax tolerance than 1 ULP, the more lax tolerance is allowed).</span></span>
-   <span data-ttu-id="ea4f6-151">Las operaciones con fusibles se adhieren a las mismas reglas NaN que las operaciones sin fusibles.</span><span class="sxs-lookup"><span data-stu-id="ea4f6-151">Fused operations adhere to the same NaN rules as non-fused operations.</span></span>
-   <span data-ttu-id="ea4f6-152">Multiplique y divida cada operación en el nivel de precisión de punto flotante de 32 bits (precisión en 1 ULP).</span><span class="sxs-lookup"><span data-stu-id="ea4f6-152">Multiply and divide each operate at the 32-bit floating-point precision level (accuracy to 1 ULP).</span></span>

## <a name="16-bit-floating-point-rules"></a><span data-ttu-id="ea4f6-153">Reglas de Floating-Point de 16 bits</span><span class="sxs-lookup"><span data-stu-id="ea4f6-153">16-bit Floating-Point Rules</span></span>

<span data-ttu-id="ea4f6-154">Direct3D 10 también admite representaciones de 16 bits de números de punto flotante.</span><span class="sxs-lookup"><span data-stu-id="ea4f6-154">Direct3D 10 also supports 16-bit representations of floating-point numbers.</span></span>

<span data-ttu-id="ea4f6-155">Formato:</span><span class="sxs-lookup"><span data-stu-id="ea4f6-155">Format:</span></span>

-   <span data-ttu-id="ea4f6-156">1 bit (s) de signo en la posición de bit de MSB</span><span class="sxs-lookup"><span data-stu-id="ea4f6-156">1 sign bit (s)in the MSB bit position</span></span>
-   <span data-ttu-id="ea4f6-157">5 bits de exponente sesgado (e)</span><span class="sxs-lookup"><span data-stu-id="ea4f6-157">5 bits of biased exponent (e)</span></span>
-   <span data-ttu-id="ea4f6-158">10 bits de fracción (f), con un bit oculto adicional</span><span class="sxs-lookup"><span data-stu-id="ea4f6-158">10 bits of fraction (f), with an additional hidden bit</span></span>

<span data-ttu-id="ea4f6-159">Un valor de float16 (v) sigue las siguientes reglas:</span><span class="sxs-lookup"><span data-stu-id="ea4f6-159">A float16 value (v) follows the following rules:</span></span>

-   <span data-ttu-id="ea4f6-160">Si e = = 31 y f! = 0, v es NaN independientemente de s</span><span class="sxs-lookup"><span data-stu-id="ea4f6-160">if e == 31 and f != 0, then v is NaN regardless of s</span></span>
-   <span data-ttu-id="ea4f6-161">Si e = = 31 y f = = 0, v = (-1) s \* Infinity (infinito firmado)</span><span class="sxs-lookup"><span data-stu-id="ea4f6-161">if e == 31 and f == 0, then v = (-1)s\*infinity (signed infinity)</span></span>
-   <span data-ttu-id="ea4f6-162">Si e está entre 0 y 31, v = (-1) s \* 2 (e-15) \* (1. f)</span><span class="sxs-lookup"><span data-stu-id="ea4f6-162">if e is between 0 and 31, then v = (-1)s\*2(e-15)\*(1.f)</span></span>
-   <span data-ttu-id="ea4f6-163">Si e = = 0 y f! = 0, v = (-1) s \* 2 (e-14) \* (0. f) (números desnormalizados)</span><span class="sxs-lookup"><span data-stu-id="ea4f6-163">if e == 0 and f != 0, then v = (-1)s\*2(e-14)\*(0.f) (denormalized numbers)</span></span>
-   <span data-ttu-id="ea4f6-164">Si e = = 0 y f = = 0, v = (-1) s \* 0 (con signo de cero)</span><span class="sxs-lookup"><span data-stu-id="ea4f6-164">if e == 0 and f == 0, then v = (-1)s\*0 (signed zero)</span></span>

<span data-ttu-id="ea4f6-165">las reglas de punto flotante de 32 bits también contienen números de punto flotante de 16 bits, ajustados para el diseño de bits descrito anteriormente.</span><span class="sxs-lookup"><span data-stu-id="ea4f6-165">32-bit floating-point rules also hold for 16-bit floating-point numbers, adjusted for the bit layout described above.</span></span> <span data-ttu-id="ea4f6-166">Las excepciones son:</span><span class="sxs-lookup"><span data-stu-id="ea4f6-166">Exceptions to this include:</span></span>

-   <span data-ttu-id="ea4f6-167">Precisión: las operaciones no confundidas en los números de punto flotante de 16 bits producen un resultado que es el valor representable más cercano a un resultado infinitamente preciso (redondear a más cercano incluso, por IEEE-754, aplicado a valores de 16 bits).</span><span class="sxs-lookup"><span data-stu-id="ea4f6-167">Precision: Unfused operations on 16-bit floating-point numbers produce a result that is the nearest representable value to an infinitely-precise result (round to nearest even, per IEEE-754, applied to 16-bit values).</span></span> <span data-ttu-id="ea4f6-168">las reglas de punto flotante de 32 bits se adhieren a una tolerancia ULP, las reglas de punto flotante de 16 bits se adhieren a 0,5 ULP para operaciones no confundidas y 0,6 ULP para operaciones con fusibles.</span><span class="sxs-lookup"><span data-stu-id="ea4f6-168">32-bit floating-point rules adhere to 1 ULP tolerance, 16-bit floating-point rules adhere to 0.5 ULP for unfused operations, and 0.6 ULP for fused operations.</span></span>
-   <span data-ttu-id="ea4f6-169">los números de punto flotante de 16 bits conservan las desnormativas.</span><span class="sxs-lookup"><span data-stu-id="ea4f6-169">16-bit floating-point numbers preserve denorms.</span></span>

## <a name="11-bit-and-10-bit-floating-point-rules"></a><span data-ttu-id="ea4f6-170">Reglas de Floating-Point de 11 bits y de 10 bits</span><span class="sxs-lookup"><span data-stu-id="ea4f6-170">11-bit and 10-bit Floating-Point Rules</span></span>

<span data-ttu-id="ea4f6-171">Direct3D 10 también admite formatos de punto flotante de 11 y 10 bits.</span><span class="sxs-lookup"><span data-stu-id="ea4f6-171">Direct3D 10 also supports 11-bit and 10-bit floating-point formats.</span></span>

<span data-ttu-id="ea4f6-172">Formato:</span><span class="sxs-lookup"><span data-stu-id="ea4f6-172">Format:</span></span>

-   <span data-ttu-id="ea4f6-173">Bit sin signo</span><span class="sxs-lookup"><span data-stu-id="ea4f6-173">No sign bit</span></span>
-   <span data-ttu-id="ea4f6-174">5 bits de exponente sesgado (e)</span><span class="sxs-lookup"><span data-stu-id="ea4f6-174">5 bits of biased exponent (e)</span></span>
-   <span data-ttu-id="ea4f6-175">6 bits de fracción (f) para un formato de 11 bits, 5 bits de fracción (f) para un formato de 10 bits, con un bit oculto adicional en cualquier caso.</span><span class="sxs-lookup"><span data-stu-id="ea4f6-175">6 bits of fraction (f) for an 11-bit format, 5 bits of fraction (f) for a 10-bit format, with an additional hidden bit in either case.</span></span>

<span data-ttu-id="ea4f6-176">Un valor de float11/float10 (v) sigue las siguientes reglas:</span><span class="sxs-lookup"><span data-stu-id="ea4f6-176">A float11/float10 value (v) follows the following rules:</span></span>

-   <span data-ttu-id="ea4f6-177">Si e = = 31 y f! = 0, v es NaN</span><span class="sxs-lookup"><span data-stu-id="ea4f6-177">if e == 31 and f != 0, then v is NaN</span></span>
-   <span data-ttu-id="ea4f6-178">Si e = = 31 y f = = 0, v = + infinito</span><span class="sxs-lookup"><span data-stu-id="ea4f6-178">if e == 31 and f == 0, then v = +infinity</span></span>
-   <span data-ttu-id="ea4f6-179">Si e está entre 0 y 31, v = 2 (e-15) \* (1. f)</span><span class="sxs-lookup"><span data-stu-id="ea4f6-179">if e is between 0 and 31, then v = 2(e-15)\*(1.f)</span></span>
-   <span data-ttu-id="ea4f6-180">Si e = = 0 y f! = 0, v = \* 2 (e-14) \* (0. f) (números desnormalizados)</span><span class="sxs-lookup"><span data-stu-id="ea4f6-180">if e == 0 and f != 0, then v = \*2(e-14)\*(0.f) (denormalized numbers)</span></span>
-   <span data-ttu-id="ea4f6-181">Si e = = 0 y f = = 0, v = 0 (cero)</span><span class="sxs-lookup"><span data-stu-id="ea4f6-181">if e == 0 and f == 0, then v = 0 (zero)</span></span>

<span data-ttu-id="ea4f6-182">las reglas de punto flotante de 32 bits también contienen números de punto flotante de 11 bits y 10 bits, ajustados para el diseño de bits descrito anteriormente.</span><span class="sxs-lookup"><span data-stu-id="ea4f6-182">32-bit floating-point rules also hold for 11-bit and 10-bit floating-point numbers, adjusted for the bit layout described above.</span></span> <span data-ttu-id="ea4f6-183">Entre las excepciones se incluyen:</span><span class="sxs-lookup"><span data-stu-id="ea4f6-183">Exceptions include:</span></span>

-   <span data-ttu-id="ea4f6-184">Precisión: las reglas de punto flotante de 32 bits se adhieren a 0,5 ULP.</span><span class="sxs-lookup"><span data-stu-id="ea4f6-184">Precision: 32-bit floating-point rules adhere to 0.5 ULP.</span></span>
-   <span data-ttu-id="ea4f6-185">los números de punto flotante de 10/11 bits conservan las desnormativas.</span><span class="sxs-lookup"><span data-stu-id="ea4f6-185">10/11-bit floating-point numbers preserve denorms.</span></span>
-   <span data-ttu-id="ea4f6-186">Cualquier operación que daría como resultado un número menor que cero, se fija en cero.</span><span class="sxs-lookup"><span data-stu-id="ea4f6-186">Any operation that would result in a number less than zero, is clamped to zero.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ea4f6-187">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ea4f6-187">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ea4f6-188">Recursos (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="ea4f6-188">Resources (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 



