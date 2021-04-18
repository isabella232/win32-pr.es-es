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
# <a name="floating-point-rules-direct3d-10"></a>Reglas de punto flotante (Direct3D 10)

Direct3D 10 admite varias representaciones de punto flotante diferentes. Todos los cálculos de punto flotante operan en un subconjunto definido del comportamiento de punto flotante de precisión única de IEEE 754 32 bits.

-   [Reglas de Floating-Point de bits de 32](#32-bit-floating-point-rules)
    -   [Reglas IEEE-754 aceptadas](#honored-ieee-754-rules)
    -   [Desviaciones o requisitos adicionales de las reglas IEEE-754](#deviations-or-additional-requirements-from-ieee-754-rules)
-   [Reglas de Floating-Point de 16 bits](#16-bit-floating-point-rules)
-   [Reglas de Floating-Point de 11 bits y de 10 bits](#11-bit-and-10-bit-floating-point-rules)
-   [Temas relacionados](#related-topics)

## <a name="32-bit-floating-point-rules"></a>Reglas de Floating-Point de bits de 32

Hay dos conjuntos de reglas: los que cumplen con IEEE-754 y los que se desvían del estándar.

### <a name="honored-ieee-754-rules"></a>Reglas IEEE-754 aceptadas

Algunas de estas reglas son una opción única en la que IEEE-754 ofrece opciones.

-   La división por 0 produce +/-INF, excepto 0/0, que tiene como resultado NaN.
-   el registro de (+/-) 0 produce-INF. el registro de un valor negativo (distinto de-0) genera NaN.
-   La raíz cuadrada recíproca (RSQ) o la raíz cuadrada (sqrt) de un número negativo produce NaN. La excepción es-0; sqrt (-0) produce-0 y RSQ (-0) produce-INF.
-   INF-INF = NaN
-   (+/-) INF/(+/-) INF = NaN
-   (+/-) INF \* 0 = Nan
-   NaN (cualquier OP) any-Value = NaN
-   Las comparaciones EQ, GT, GE, LT y LE, cuando uno o ambos operandos es NaN devuelve **false**.
-   Las comparaciones omiten el signo de 0 (por lo que + 0 es igual a-0).
-   La comparación NE, cuando uno o ambos operandos son NaN, devuelve **true**.
-   Las comparaciones de cualquier valor que no sea NaN con +/-INF devuelven el resultado correcto.

### <a name="deviations-or-additional-requirements-from-ieee-754-rules"></a>Desviaciones o requisitos adicionales de las reglas IEEE-754

-   IEEE-754 requiere operaciones de punto flotante para producir un resultado que es el valor representable más cercano a un resultado infinitamente preciso, conocido como de redondeo a la más cercana. Direct3D 10, sin embargo, define un requisito menos flexible: las operaciones de punto flotante de 32 bits producen un resultado que se encuentra dentro de una unidad: último lugar (1 ULP) del resultado infinitamente preciso. Esto significa que, por ejemplo, se permite que el hardware trunque los resultados en 32 bits en lugar de realizar una operación de ida y vuelta más cercana, ya que esto daría como resultado un error de al menos un ULP.
-   No se admiten excepciones de punto flotante, bits de estado ni capturas.
-   Las decimales se vacían en cero con signo en la entrada y la salida de cualquier operación matemática de punto flotante. Se realizan excepciones para cualquier operación de movimiento de datos e/s que no manipule los datos.
-   Los Estados que contienen valores de punto flotante, como viewport MinDepth/MaxDepth, valores BorderColor, etc., se pueden proporcionar como valores de desnormativo y se pueden vaciar o no antes de que el hardware los use.
-   Las operaciones min o Max vacían las desnormativas para la comparación, pero el resultado se puede vaciar o no.
-   La entrada de NaN en una operación siempre produce NaN en la salida; sin embargo, no es necesario que el patrón de bits exacto del NaN siga siendo el mismo (a menos que la operación sea una instrucción de movimiento sin procesar, que no modifica los datos en absoluto).
-   Las operaciones min o Max para las que solo un operando es NaN devuelven el otro operando como resultado (contrariamente a las reglas de comparación anteriores). Se trata de una nueva regla IEEE (IEEE 754R), requerida en Direct3D 10.
-   Otra nueva regla de IEEE 754R es que min (-0, + 0) = = min (+ 0,-0) = =-0 y Max (-0, + 0) = = Max (+ 0,-0) = = + 0, que respetan el signo, a diferencia de las reglas de comparación de cero con signo (indicado anteriormente). Direct3D 10 recomienda el comportamiento de IEEE 754R aquí, pero no se aplicará; se permite que el resultado de comparar ceros sea dependiente del orden de los parámetros, mediante una comparación que omite los signos.
-   x \* 1.0 f siempre produce x (excepto desnormalización).
-   x/1.0 f siempre produce x (excepto desnormalización).
-   x +/-0.0 f siempre da como resultado x (excepto desnormalización desactivada). Pero-0 + 0 = + 0.
-   Las operaciones con fusibles (como Mad, DP3) producen resultados que no son menos precisos que los peores pedidos de evaluación en serie de la evaluación de la expansión sin fusibles de la operación. Tenga en cuenta que la definición del peor orden posible, con fines de tolerancia, no es una definición fija para una operación fusionada determinada; depende de los valores concretos de las entradas. En los pasos individuales de la expansión sin fusibles se les permite una tolerancia ULP permitida (o, para las instrucciones que Direct3D 10 llama con una tolerancia más LAX que 1 ULP, se permite la tolerancia más LAX).
-   Las operaciones con fusibles se adhieren a las mismas reglas NaN que las operaciones sin fusibles.
-   Multiplique y divida cada operación en el nivel de precisión de punto flotante de 32 bits (precisión en 1 ULP).

## <a name="16-bit-floating-point-rules"></a>Reglas de Floating-Point de 16 bits

Direct3D 10 también admite representaciones de 16 bits de números de punto flotante.

Formato:

-   1 bit (s) de signo en la posición de bit de MSB
-   5 bits de exponente sesgado (e)
-   10 bits de fracción (f), con un bit oculto adicional

Un valor de float16 (v) sigue las siguientes reglas:

-   Si e = = 31 y f! = 0, v es NaN independientemente de s
-   Si e = = 31 y f = = 0, v = (-1) s \* Infinity (infinito firmado)
-   Si e está entre 0 y 31, v = (-1) s \* 2 (e-15) \* (1. f)
-   Si e = = 0 y f! = 0, v = (-1) s \* 2 (e-14) \* (0. f) (números desnormalizados)
-   Si e = = 0 y f = = 0, v = (-1) s \* 0 (con signo de cero)

las reglas de punto flotante de 32 bits también contienen números de punto flotante de 16 bits, ajustados para el diseño de bits descrito anteriormente. Las excepciones son:

-   Precisión: las operaciones no confundidas en los números de punto flotante de 16 bits producen un resultado que es el valor representable más cercano a un resultado infinitamente preciso (redondear a más cercano incluso, por IEEE-754, aplicado a valores de 16 bits). las reglas de punto flotante de 32 bits se adhieren a una tolerancia ULP, las reglas de punto flotante de 16 bits se adhieren a 0,5 ULP para operaciones no confundidas y 0,6 ULP para operaciones con fusibles.
-   los números de punto flotante de 16 bits conservan las desnormativas.

## <a name="11-bit-and-10-bit-floating-point-rules"></a>Reglas de Floating-Point de 11 bits y de 10 bits

Direct3D 10 también admite formatos de punto flotante de 11 y 10 bits.

Formato:

-   Bit sin signo
-   5 bits de exponente sesgado (e)
-   6 bits de fracción (f) para un formato de 11 bits, 5 bits de fracción (f) para un formato de 10 bits, con un bit oculto adicional en cualquier caso.

Un valor de float11/float10 (v) sigue las siguientes reglas:

-   Si e = = 31 y f! = 0, v es NaN
-   Si e = = 31 y f = = 0, v = + infinito
-   Si e está entre 0 y 31, v = 2 (e-15) \* (1. f)
-   Si e = = 0 y f! = 0, v = \* 2 (e-14) \* (0. f) (números desnormalizados)
-   Si e = = 0 y f = = 0, v = 0 (cero)

las reglas de punto flotante de 32 bits también contienen números de punto flotante de 11 bits y 10 bits, ajustados para el diseño de bits descrito anteriormente. Entre las excepciones se incluyen:

-   Precisión: las reglas de punto flotante de 32 bits se adhieren a 0,5 ULP.
-   los números de punto flotante de 10/11 bits conservan las desnormativas.
-   Cualquier operación que daría como resultado un número menor que cero, se fija en cero.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Recursos (Direct3D 10)](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 



