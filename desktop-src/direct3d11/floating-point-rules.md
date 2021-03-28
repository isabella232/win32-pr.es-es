---
title: Reglas de punto flotante (Direct3D 11)
description: Direct3D 11 admite varias representaciones de punto flotante. Todos los cálculos de punto flotante operan en un subconjunto definido de las reglas de punto flotante de precisión única de IEEE 754 32 bits.
ms.assetid: 33F21BD0-FDF8-4D35-95C0-0A3920814CB6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d83c87db0daa69c0393d0399ece5bdb6cf01d519
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104420827"
---
# <a name="floating-point-rules-direct3d-11"></a>Reglas de punto flotante (Direct3D 11)

Direct3D 11 admite varias representaciones de punto flotante. Todos los cálculos de punto flotante operan en un subconjunto definido de las reglas de punto flotante de precisión única de IEEE 754 32 bits.

-   [reglas de punto flotante de 32 bits](#32-bit-floating-point-rules)
    -   [Reglas IEEE-754 aceptadas](#honored-ieee-754-rules)
    -   [Desviaciones o requisitos adicionales de las reglas IEEE-754](#deviations-or-additional-requirements-from-ieee-754-rules)
-   [reglas de punto flotante de 64 bits (precisión doble)](#64-bit-double-precision-floating-point-rules)
-   [reglas de punto flotante de 16 bits](#16-bit-floating-point-rules)
-   [reglas de punto flotante de 11 bits y de 10 bits](#11-bit-and-10-bit-floating-point-rules)
-   [Temas relacionados](#related-topics)

## <a name="32-bit-floating-point-rules"></a>reglas de punto flotante de 32 bits

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

-   IEEE-754 requiere operaciones de punto flotante para producir un resultado que es el valor representable más cercano a un resultado infinitamente preciso, conocido como de redondeo a la más cercana. Direct3D 11 define el mismo requisito: las operaciones de punto flotante de 32 bits producen un resultado que se encuentra dentro del 0,5 de la unidad (ULP) del resultado infinitamente preciso. Esto significa que, por ejemplo, se permite que el hardware trunque los resultados en 32 bits en lugar de realizar una operación de ida y vuelta más cercana, ya que esto daría como resultado un error de como máximo 0,5 ULP. Esta regla solo se aplica a la suma, resta y multiplicación.
-   No se admiten excepciones de punto flotante, bits de estado ni capturas.
-   Las decimales se vacían en cero con signo en la entrada y la salida de cualquier operación matemática de punto flotante. Se realizan excepciones para cualquier operación de movimiento de datos o de e/s que no manipule los datos.
-   Los Estados que contienen valores de punto flotante, como viewport MinDepth/MaxDepth, valores BorderColor, se pueden proporcionar como valores de desnormativo y se pueden vaciar o no antes de que el hardware los use.
-   Las operaciones min o Max vacían las desnormativas para la comparación, pero el resultado se puede vaciar o no.
-   La entrada de NaN en una operación siempre produce NaN en la salida. Pero no es necesario que el patrón de bits exacto del NaN siga siendo el mismo (a menos que la operación sea una instrucción de movimiento sin procesar, que no modifica los datos).
-   Las operaciones min o Max para las que solo un operando es NaN devuelven el otro operando como el resultado (en oposición a las reglas de comparación que hemos visto anteriormente). Se trata de una regla de 754R de IEEE.

    La especificación IEEE-754R para las operaciones de punto flotante min y Max indica que si una de las entradas a min o Max es un valor QNaN silencioso, el resultado de la operación es el otro parámetro. Por ejemplo:

    ```C++
    min(x,QNaN) == min(QNaN,x) == x (same for max)
    ```

    

    Una revisión de la especificación IEEE-754R adoptó un comportamiento diferente para min y Max cuando una entrada es un valor SNaN de "Signaling" frente a un valor QNaN:

    ```C++
    min(x,SNaN) == min(SNaN,x) == QNaN (same for max)
     
    ```

    

    Por lo general, Direct3D sigue los estándares de aritmética: IEEE-754 y IEEE-754R. Pero en este caso, tenemos una desviación.

    Las reglas aritméticas en Direct3D 10 y versiones posteriores no hacen ninguna distinción entre los valores NaN y de señalización insilenciosos (QNaN frente a SNaN). Todos los valores NaN se controlan de la misma manera. En el caso de min y Max, el comportamiento de Direct3D para cualquier valor NaN es como el modo en que QNaN se controla en la definición de IEEE-754R. (Por integridad: si ambas entradas son NaN, se devuelve cualquier valor NaN).

-   Otra regla de IEEE 754R es que min (-0, + 0) = = min (+ 0,-0) = =-0 y Max (-0, + 0) = = Max (+ 0,-0) = = + 0, que respeta el signo, a diferencia de las reglas de comparación de cero con signo (como vimos anteriormente). Direct3D recomienda el comportamiento de IEEE 754R aquí, pero no lo aplica. se permite que el resultado de comparar ceros sea dependiente del orden de los parámetros, mediante una comparación que omite los signos.
-   x \* 1.0 f siempre produce x (excepto desnormalización).
-   x/1.0 f siempre produce x (excepto desnormalización).
-   x +/-0.0 f siempre da como resultado x (excepto desnormalización desactivada). Pero-0 + 0 = + 0.
-   Las operaciones con fusibles (como Mad, DP3) producen resultados que no son menos precisos que los peores pedidos de evaluación en serie de la evaluación de la expansión sin fusibles de la operación. La definición del peor orden posible, con fines de tolerancia, no es una definición fija para una operación fusionada determinada; depende de los valores concretos de las entradas. En los pasos individuales de la expansión sin fusibles se les permite una tolerancia ULP permitida (o, para las instrucciones que Direct3D llama con una tolerancia más LAX que 1 ULP, se permite la tolerancia más LAX).
-   Las operaciones con fusibles se adhieren a las mismas reglas NaN que las operaciones sin fusibles.
-   sqrt y RCP tienen 1 tolerancia ULP. Las instrucciones de raíz cuadrada recíproca y recíproca del sombreador, [**RCP**](/previous-versions/windows/desktop/legacy/hh447205(v=vs.85)) y [**RSQ**](/windows/desktop/direct3dhlsl/rsq--sm4---asm-), tienen su propio requisito de precisión relajada independiente.
-   Multiplique y divida cada operación en el nivel de precisión de punto flotante de 32 bits (precisión de 0,5 ULP para multiplicar, 1,0 ULP para recíproco). Si x/y se implementa directamente, los resultados deben tener una precisión mayor o igual que un método de dos pasos.

## <a name="64-bit-double-precision-floating-point-rules"></a>reglas de punto flotante de 64 bits (precisión doble)

Los controladores de hardware y de pantalla admiten opcionalmente el punto flotante de precisión doble. Para indicar la compatibilidad, al llamar a [**ID3D11Device:: CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) con la [**característica de D3D11 \_ \_ Double**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_feature), el controlador establece **DoublePrecisionFloatShaderOps** de datos de características de [**D3D11 \_ \_ \_**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_doubles) en true. A continuación, el controlador y el hardware deben admitir todas las instrucciones de punto flotante de precisión doble.

Las instrucciones de doble precisión siguen los requisitos de comportamiento de IEEE 754R.

La compatibilidad con la generación de valores desnormalizados es necesaria para los datos de precisión doble (comportamiento de vaciado a cero). Del mismo modo, las instrucciones no leen los datos no normalizados como cero con signo, respetan el valor de desnormativo.

## <a name="16-bit-floating-point-rules"></a>reglas de punto flotante de 16 bits

Direct3D 11 también admite representaciones de 16 bits de números de punto flotante.

Formato:

-   1 bit (s) de signo en la posición de bit de MSB
-   5 bits de exponente sesgado (e)
-   10 bits de fracción (f), con un bit oculto adicional

Un valor float16 (v) sigue estas reglas:

-   Si e = = 31 y f! = 0, v es NaN independientemente de s
-   Si e = = 31 y f = = 0, v = (-1) s \* Infinity (infinito firmado)
-   Si e está entre 0 y 31, v = (-1) s \* 2 (e-15) \* (1. f)
-   Si e = = 0 y f! = 0, v = (-1) s \* 2 (e-14) \* (0. f) (números desnormalizados)
-   Si e = = 0 y f = = 0, v = (-1) s \* 0 (con signo de cero)

las reglas de punto flotante de 32 bits también contienen números de punto flotante de 16 bits, ajustados para el diseño de bits descrito anteriormente. Las excepciones son:

-   Precisión: las operaciones no confundidas en los números de punto flotante de 16 bits producen un resultado que es el valor representable más cercano a un resultado infinitamente preciso (redondear a más cercano incluso, por IEEE-754, aplicado a valores de 16 bits). las reglas de punto flotante de 32 bits se adhieren a una tolerancia ULP, las reglas de punto flotante de 16 bits se adhieren a 0,5 ULP para operaciones no confundidas y 0,6 ULP para operaciones con fusibles.
-   los números de punto flotante de 16 bits conservan las desnormativas.

## <a name="11-bit-and-10-bit-floating-point-rules"></a>reglas de punto flotante de 11 bits y de 10 bits

Direct3D 11 también admite formatos de punto flotante de 11 bits y de 10 bits.

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
-   Cualquier operación que daría como resultado un número menor que cero se fija en cero.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Recursos](overviews-direct3d-11-resources.md)
</dt> <dt>

[Texturas](overviews-direct3d-11-resources-textures.md)
</dt> </dl>

 

 