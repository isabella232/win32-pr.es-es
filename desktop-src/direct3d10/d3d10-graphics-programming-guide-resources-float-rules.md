---
description: Direct3D 10 admite varias representaciones de punto flotante diferentes. Todos los cálculos de punto flotante funcionan en un subconjunto definido del comportamiento de punto flotante de precisión sencilla IEEE 754 de 32 bits.
ms.assetid: 57221d13-8993-4db3-b1a0-88bdcf6f0167
title: Reglas de punto de conexión (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d7f575810b1efb1bde65dd1c80de98837a0a0274c6b394207b612874f289054
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118100987"
---
# <a name="floating-point-rules-direct3d-10"></a>Reglas de punto flotante (Direct3D 10)

Direct3D 10 admite varias representaciones de punto flotante diferentes. Todos los cálculos de punto flotante funcionan en un subconjunto definido del comportamiento de punto flotante de precisión sencilla IEEE 754 de 32 bits.

-   [Reglas de Floating-Point de 32 bits](#32-bit-floating-point-rules)
    -   [Reglas de IEEE-754 respetadas](#honored-ieee-754-rules)
    -   [Desviaciones o requisitos adicionales de las reglas IEEE-754](#deviations-or-additional-requirements-from-ieee-754-rules)
-   [Reglas de Floating-Point de 16 bits](#16-bit-floating-point-rules)
-   [Reglas de Floating-Point de 11 bits y 10 bits](#11-bit-and-10-bit-floating-point-rules)
-   [Temas relacionados](#related-topics)

## <a name="32-bit-floating-point-rules"></a>Reglas de Floating-Point de 32 bits

Hay dos conjuntos de reglas: las que se ajustan a IEEE-754 y las que se desvía del estándar.

### <a name="honored-ieee-754-rules"></a>Reglas IEEE-754 respetadas

Algunas de estas reglas son una única opción en la que IEEE-754 ofrece opciones.

-   Dividir por 0 genera +/- INF, excepto 0/0, lo que da como resultado NaN.
-   El registro de (+/-) 0 genera -INF. El registro de un valor negativo (distinto de -0) genera NaN.
-   La raíz cuadrada mutua (rsq) o la raíz cuadrada (sqrt) de un número negativo genera NaN. La excepción es -0; sqrt(-0) genera -0 y rsq(-0) genera -INF.
-   INF - INF = NaN
-   (+/-) INF / (+/-)INF = NaN
-   (+/-) INF \* 0 = NaN
-   NaN (cualquier op) any-value = NaN
-   Las comparaciones EQ, GT, GE, LT y LE, cuando uno o ambos operandos son NaN devuelve **FALSE.**
-   Las comparaciones omiten el signo 0 (por lo que +0 es igual a -0).
-   La comparación NE, cuando uno o ambos operandos son NaN devuelve **TRUE.**
-   Las comparaciones de cualquier valor que no sea NaN con +/- INF devuelven el resultado correcto.

### <a name="deviations-or-additional-requirements-from-ieee-754-rules"></a>Desviaciones o requisitos adicionales de las reglas IEEE-754

-   IEEE-754 requiere que las operaciones de punto flotante produzcan un resultado que sea el valor representable más cercano a un resultado infinitamente preciso, conocido como round-to-nearest-even. Sin embargo, Direct3D 10 define un requisito más flexible: las operaciones de punto flotante de 32 bits generan un resultado que se encuentra dentro de una unidad de último lugar (1 ULP) del resultado infinitamente preciso. Esto significa que, por ejemplo, el hardware puede truncar los resultados a 32 bits en lugar de realizar la operación de ida y vuelta a la par más cercana, ya que se produciría un error de, como máximo, un ULP.
-   No se admiten excepciones de punto flotante, bits de estado o capturas.
-   Los desnormados se vacían hasta el cero conservado en signo en la entrada y salida de cualquier operación matemática de punto flotante. Se realizan excepciones para cualquier operación de E/S o movimiento de datos que no manipula los datos.
-   Los estados que contienen valores de punto flotante, como Viewport MinDepth/MaxDepth, borderColor, etc., se pueden proporcionar como valores de desnormado y pueden o no vaciarse antes de que el hardware lo use.
-   Las operaciones mínimas o máximas vacían los desnormados para la comparación, pero el resultado puede o no vaciarse.
-   La entrada naN en una operación siempre genera NaN en la salida, pero no es necesario que el patrón de bits exacto del NaN permanezca igual (a menos que la operación sea una instrucción de movimiento sin procesar, que no modifica los datos en absoluto).
-   Las operaciones mínimas o máximas para las que solo un operando es NaN devuelven el otro operando como resultado (al contrario de las reglas de comparación anteriores). Se trata de una nueva regla IEEE (IEEE 754R), necesaria en Direct3D 10.
-   Otra nueva regla IEEE 754R es que min(-0,+0) == min(+0,-0) == -0 y max(-0,+0) == max(+0,-0) == +0, que respetan el signo, a diferencia de las reglas de comparación para el cero con signo (indicado anteriormente). Direct3D 10 recomienda aquí el comportamiento IEEE 754R, pero no se aplicará. está permitido para que el resultado de comparar ceros dependa del orden de los parámetros, mediante una comparación que omite los signos.
-   x \* 1.0f siempre da como resultado x (excepto desnorma vaciado).
-   x/1.0f siempre da como resultado x (excepto desnorma vaciado).
-   x +/- 0,0f siempre da como resultado x (excepto desnorma vaciado). Pero -0 + 0 = +0.
-   Las operaciones fusionadas (como locas, dp3) generan resultados que no son menos precisos que el peor orden de serie posible de evaluación de la expansión sin fusionar de la operación. Tenga en cuenta que la definición del peor orden posible, para la tolerancia, no es una definición fija para una operación fusionada determinada; depende de los valores concretos de las entradas. Cada uno de los pasos individuales de la expansión sin fusionar permite una tolerancia ULP (o para cualquier instrucción que direct3D 10 llame con una tolerancia lax más lax que 1 ULP, se permite más tolerancia lax).
-   Las operaciones fusionadas se adhieren a las mismas reglas de NaN que las operaciones no fusionadas.
-   Multiplique y divida cada operación en el nivel de precisión de punto flotante de 32 bits (precisión a 1 ULP).

## <a name="16-bit-floating-point-rules"></a>Reglas de Floating-Point de 16 bits

Direct3D 10 también admite representaciones de 16 bits de números de punto flotante.

Formato:

-   1 bit (s) de signo en la posición de bits de MSB
-   5 bits de exponente sesgado (e)
-   10 bits de fracción (f), con un bit oculto adicional

Un valor float16 (v) sigue las reglas siguientes:

-   si e == 31 y f != 0, v es NaN independientemente de s
-   si e == 31 y f == 0, v = (-1)s \* infinity (infinito con signo)
-   si e está entre 0 y 31, v = (-1)s \* 2(e-15) \* (1.f)
-   si e == 0 y f != 0, v = (-1)s \* 2(e-14) \* (0.f) (números desnormalizados)
-   si e == 0 y f == 0, v = (-1)s \* 0 (con signo cero)

Las reglas de punto flotante de 32 bits también se mantienen para números de punto flotante de 16 bits, ajustados para el diseño de bits descrito anteriormente. Las excepciones son:

-   Precisión: las operaciones sin fusionar en números de punto flotante de 16 bits generan un resultado que es el valor representable más cercano a un resultado infinitamente preciso (round to nearest even, per IEEE-754, applied to 16-bit values). Las reglas de punto flotante de 32 bits se adhieren a la tolerancia ULP 1, las reglas de punto flotante de 16 bits se adhieren a 0,5 ULP para las operaciones sin fusionar y 0,6 ULP para las operaciones fusionadas.
-   Los números de punto flotante de 16 bits conservan los desnormados.

## <a name="11-bit-and-10-bit-floating-point-rules"></a>Reglas de 11 y 10 bits Floating-Point bits

Direct3D 10 también admite formatos de punto flotante de 11 y 10 bits.

Formato:

-   Sin bit de signo
-   5 bits de exponente sesgado (e)
-   6 bits de fracción (f) para un formato de 11 bits, 5 bits de fracción (f) para un formato de 10 bits, con un bit oculto adicional en cualquier caso.

Un valor float11/float10 (v) sigue las reglas siguientes:

-   si e == 31 y f != 0, v es NaN
-   si e == 31 y f == 0, v = +infinity
-   si e está entre 0 y 31, v = 2(e-15) \* (1.f)
-   si e == 0 y f != 0, v = \* 2(e-14) \* (0.f) (números desnormalizados)
-   si e == 0 y f == 0, v = 0 (cero)

Las reglas de punto flotante de 32 bits también se mantienen para números de punto flotante de 11 y 10 bits, ajustados para el diseño de bits descrito anteriormente. Entre las excepciones se incluyen:

-   Precisión: las reglas de punto flotante de 32 bits se adhieren a 0,5 ULP.
-   Los números de punto flotante de 10/11 bits conservan los desnormados.
-   Cualquier operación que daría lugar a un número menor que cero, se fija en cero.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Recursos (Direct3D 10)](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 



