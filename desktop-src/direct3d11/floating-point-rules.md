---
title: Reglas de punto flotante (Direct3D 11)
description: Direct3D 11 admite varias representaciones de punto flotante. Todos los cálculos de punto flotante funcionan en un subconjunto definido de las reglas de punto flotante de precisión sencilla IEEE 754 de 32 bits.
ms.assetid: 33F21BD0-FDF8-4D35-95C0-0A3920814CB6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d83c87db0daa69c0393d0399ece5bdb6cf01d519
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126963820"
---
# <a name="floating-point-rules-direct3d-11"></a>Reglas de punto flotante (Direct3D 11)

Direct3D 11 admite varias representaciones de punto flotante. Todos los cálculos de punto flotante funcionan en un subconjunto definido de las reglas de punto flotante de precisión sencilla IEEE 754 de 32 bits.

-   [Reglas de punto flotante de 32 bits](#32-bit-floating-point-rules)
    -   [Reglas de IEEE-754 respetadas](#honored-ieee-754-rules)
    -   [Desviaciones o requisitos adicionales de las reglas IEEE-754](#deviations-or-additional-requirements-from-ieee-754-rules)
-   [Reglas de punto flotante de 64 bits (precisión doble)](#64-bit-double-precision-floating-point-rules)
-   [Reglas de punto flotante de 16 bits](#16-bit-floating-point-rules)
-   [Reglas de punto flotante de 11 y 10 bits](#11-bit-and-10-bit-floating-point-rules)
-   [Temas relacionados](#related-topics)

## <a name="32-bit-floating-point-rules"></a>Reglas de punto flotante de 32 bits

Hay dos conjuntos de reglas: las que se ajustan a IEEE-754 y las que se desvía del estándar.

### <a name="honored-ieee-754-rules"></a>Reglas de IEEE-754 respetadas

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
-   La ne de comparación, cuando uno o ambos operandos son NaN devuelve **TRUE**.
-   Las comparaciones de cualquier valor que no sea NaN con +/- INF devuelven el resultado correcto.

### <a name="deviations-or-additional-requirements-from-ieee-754-rules"></a>Desviaciones o requisitos adicionales de las reglas IEEE-754

-   IEEE-754 requiere que las operaciones de punto flotante produzcan un resultado que sea el valor representable más cercano a un resultado infinitamente preciso, conocido como round-to-nearest-even. Direct3D 11 define el mismo requisito: las operaciones de punto flotante de 32 bits generan un resultado que se encuentra dentro de 0,5 unidades de último lugar (ULP) del resultado infinitamente preciso. Esto significa que, por ejemplo, el hardware puede truncar los resultados a 32 bits en lugar de realizar la operación de ida y vuelta a la par más cercana, ya que se produciría un error de como máximo de 0,5 ULP. Esta regla solo se aplica a la suma, resta y multiplicación.
-   No se admiten excepciones de punto flotante, bits de estado o capturas.
-   Los desnormados se vacían hasta el cero conservado en signo en la entrada y salida de cualquier operación matemática de punto flotante. Se realizan excepciones para cualquier operación de E/S o movimiento de datos que no manipula los datos.
-   Los estados que contienen valores de punto flotante, como Viewport MinDepth/MaxDepth, BorderColor, se pueden proporcionar como valores de desnormado y pueden o no vaciarse antes de que el hardware los use.
-   Las operaciones mínimas o máximas vacían los desnormados para la comparación, pero el resultado puede o no vaciarse.
-   La entrada naN en una operación siempre genera NaN en la salida. Pero no es necesario que el patrón de bits exacto del NaN permanezca igual (a menos que la operación sea una instrucción de movimiento sin procesar, que no modifica los datos).
-   Las operaciones mínimas o máximas para las que solo un operando es NaN devuelven el otro operando como resultado (al contrario de las reglas de comparación que hemos visto anteriormente). Se trata de una regla IEEE 754R.

    La especificación IEEE-754R para operaciones de punto flotante mínima y máxima indica que si una de las entradas a min o max es un valor QNaN silencioso, el resultado de la operación es el otro parámetro. Por ejemplo:

    ```C++
    min(x,QNaN) == min(QNaN,x) == x (same for max)
    ```

    

    Una revisión de la especificación IEEE-754R adoptó un comportamiento diferente para min y max cuando una entrada es un valor SNaN de "señalización" frente a un valor QNaN:

    ```C++
    min(x,SNaN) == min(SNaN,x) == QNaN (same for max)
     
    ```

    

    Por lo general, Direct3D sigue los estándares aritméticos: IEEE-754 e IEEE-754R. Pero en este caso, tenemos una desviación.

    Las reglas aritméticas de Direct3D 10 y versiones posteriores no distinguen entre valores NaN silenciosos y de señalización (QNaN frente a SNaN). Todos los valores NaN se controlan de la misma manera. En el caso de min y max, el comportamiento de Direct3D para cualquier valor NaN es como cómo se controla QNaN en la definición IEEE-754R. (Para mayor integridad: si ambas entradas son NaN, se devuelve cualquier valor NaN).

-   Otra regla IEEE 754R es que min(-0,+0) == min(+0,-0) == -0 y max(-0,+0) == max(+0,-0) == +0, que respeta el signo, a diferencia de las reglas de comparación de cero con signo (como vimos anteriormente). Direct3D recomienda aquí el comportamiento IEEE 754R, pero no lo aplica. está permitido para que el resultado de comparar ceros dependa del orden de los parámetros, mediante una comparación que omite los signos.
-   x \* 1.0f siempre da como resultado x (excepto desnorma vaciado).
-   x/1.0f siempre da como resultado x (excepto desnorma vaciado).
-   x +/- 0,0f siempre da como resultado x (excepto desnorma vaciado). Pero -0 + 0 = +0.
-   Las operaciones fusionadas (como locas, dp3) generan resultados que no son menos precisos que el peor orden de serie posible de evaluación de la expansión sin fusionar de la operación. La definición de la peor ordenación posible, con fines de tolerancia, no es una definición fija para una operación fusionada determinada; depende de los valores concretos de las entradas. Cada uno de los pasos individuales de la expansión sin fusionar permite una tolerancia ULP (o para cualquier instrucción que direct3D llame con una tolerancia más lax que 1 ULP, se permite más tolerancia lax).
-   Las operaciones fusionadas se adhieren a las mismas reglas de NaN que las operaciones no fusionadas.
-   sqrt y rcp tienen una tolerancia ULP. Las instrucciones de raíz cuadrada recíproco y recíproco del sombreador, [**rcp**](/previous-versions/windows/desktop/legacy/hh447205(v=vs.85)) y [**rsq,**](/windows/desktop/direct3dhlsl/rsq--sm4---asm-)tienen su propio requisito de precisión relajada independiente.
-   Multiplique y divida cada operación en el nivel de precisión de punto flotante de 32 bits (precisión a 0,5 ULP para multiplicación, 1,0 ULP para recíproco). Si x/y se implementa directamente, los resultados deben ser de mayor o igual precisión que un método de dos pasos.

## <a name="64-bit-double-precision-floating-point-rules"></a>Reglas de punto flotante de 64 bits (precisión doble)

Los controladores de hardware y visualización admiten opcionalmente el punto flotante de precisión doble. Para indicar compatibilidad, al llamar a [**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) con [**D3D11 \_ FEATURE \_ DOUBLES,**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_feature)el controlador establece **DoublePrecisionFloatShaderOps** de [**D3D11 \_ FEATURE DATA \_ \_ DOUBLES**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_doubles) en TRUE. A continuación, el controlador y el hardware deben admitir todas las instrucciones de punto flotante de precisión doble.

Las instrucciones de precisión doble siguen los requisitos de comportamiento de IEEE 754R.

La compatibilidad con la generación de valores desnormalizados es necesaria para los datos de precisión doble (sin comportamiento de vaciado a cero). Del mismo modo, las instrucciones no leen los datos desnormalizados como un cero con firma, respetan el valor de desnorma.

## <a name="16-bit-floating-point-rules"></a>Reglas de punto flotante de 16 bits

Direct3D 11 también admite representaciones de 16 bits de números de punto flotante.

Formato:

-   1 bit (s) de signo en la posición de bits de MSB
-   5 bits de exponente sesgado (e)
-   10 bits de fracción (f), con un bit oculto adicional

Un valor float16 (v) sigue estas reglas:

-   si e == 31 y f != 0, v es NaN independientemente de s
-   si e == 31 y f == 0, v = (-1)s \* infinity (infinito con signo)
-   si e está entre 0 y 31, v = (-1)s \* 2(e-15) \* (1.f)
-   si e == 0 y f != 0, v = (-1)s \* 2(e-14) \* (0.f) (números desnormalizados)
-   si e == 0 y f == 0, v = (-1)s \* 0 (con signo cero)

Las reglas de punto flotante de 32 bits también se mantienen para números de punto flotante de 16 bits, ajustados para el diseño de bits descrito anteriormente. Las excepciones son:

-   Precisión: las operaciones sin fusionar en números de punto flotante de 16 bits generan un resultado que es el valor representable más cercano a un resultado infinitamente preciso (redondear al par más cercano, por IEEE-754, aplicado a valores de 16 bits). Las reglas de punto flotante de 32 bits se adhieren a la tolerancia ULP 1, las reglas de punto flotante de 16 bits se adhieren a 0,5 ULP para las operaciones sin fusionar y 0,6 ULP para las operaciones fusionadas.
-   Los números de punto flotante de 16 bits conservan los desnormados.

## <a name="11-bit-and-10-bit-floating-point-rules"></a>Reglas de punto flotante de 11 y 10 bits

Direct3D 11 también admite formatos de punto flotante de 11 y 10 bits.

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
-   Cualquier operación que daría lugar a un número menor que cero se fija a cero.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Recursos](overviews-direct3d-11-resources.md)
</dt> <dt>

[Texturas](overviews-direct3d-11-resources-textures.md)
</dt> </dl>

 

 