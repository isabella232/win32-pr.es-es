---
title: Rasterización conservadora de Direct3D 12
description: La rasterización conservadora agrega cierta certeza a la representación en píxeles, lo que resulta útil en especial a los algoritmos de detección de colisiones.
ms.assetid: 081199AD-1702-4EC8-95AD-B1148C676199
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e4fae3489d54ab7b6b7abfda56f54dd8d970962
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/23/2019
ms.locfileid: "104549187"
---
# <a name="direct3d-12-conservative-rasterization"></a>Rasterización conservadora de Direct3D 12

La rasterización conservadora agrega cierta certeza a la representación en píxeles, lo que resulta útil en especial a los algoritmos de detección de colisiones.

-   [Información general](#overview)
-   [Interacciones con la canalización](#interactions-with-the-pipeline)
    -   [Interacción de las reglas de rasterización](#rasterization-rules-interaction)
    -   [Interacción con muestreo múltiple](#multisampling-interaction)
    -   [Interacción con SampleMask](#samplemask-interaction)
    -   [Interacción de prueba de profundidad/estarcido](#depthstencil-test-interaction)
    -   [Interacción de píxeles de la aplicación auxiliar](#helper-pixel-interaction)
    -   [Interacción de la cobertura de salida](#output-coverage-interaction)
    -   [Interacción con InputCoverage](#inputcoverage-interaction)
    -   [Interacción con InnerCoverage](#innercoverage-interaction)
    -   [Interacción de interpolación de atributos](#attribute-interpolation-interaction)
    -   [Interacción de recorte](#clipping-interaction)
    -   [Interacción de distancia del clip](#clip-distance-interaction)
    -   [Interacción de rasterización independiente de destino](#target-independent-rasterization-interaction)
    -   [Interacción de topología de primitivas de IA](#ia-primitive-topology-interaction)
    -   [Interacción de consultas](#query-interaction)
    -   [Interacción del estado de culling](#cull-state-interaction)
    -   [Interacción con IsFrontFace](#isfrontface-interaction)
    -   [Interacción de los modos de relleno](#fill-modes-interaction)
-   [Detalles de implementación](#implementation-details)
-   [Resumen de API](#api-summary)
-   [Temas relacionados](#related-topics)

## <a name="overview"></a>Información general

La rasterización conservadora significa que se rasterizan todos los píxeles que están al menos parcialmente incluidos en una primitiva representada, lo que significa que se invoca el sombreador de píxeles. El comportamiento normal es el muestreo, que no se usa si está habilitada la rasterización conservadora.

La rasterización conservadora es útil en una serie de situaciones, como la certeza de la detección de colisiones, la selección de la oclusión y la representación en mosaico.

Por ejemplo, en la siguiente ilustración se muestra un triángulo verde representado mediante la rasterización conservadora, tal como aparecería en el rasterizador (es decir, con coordenadas de vértice de punto fijo 16,8). El área marrón se conoce como "región de incertidumbre", una región conceptual que representa los límites extendidos del triángulo, necesaria para garantizar que la primitiva en el rasterizador es conservadora con respecto a las coordenadas de vértice de punto flotante originales. Los cuadrados rojos de cada vértice muestran cómo se calcula la región de incertidumbre: como un cuadrado de barrido.

Los cuadrados grises grandes muestran los píxeles que se representarán. Los cuadrados de color rosa muestran los píxeles representados mediante la "regla superior izquierda", que entran en juego cuando el borde del triángulo cruza el borde de los píxeles. Puede haber falsos positivos (píxeles establecidos que no deberían haber) que el sistema normalmente, pero no siempre seleccionará.

![la regla superior izquierda](images/conservative-rasterization-0.png)

## <a name="interactions-with-the-pipeline"></a>Interacciones con la canalización

### <a name="rasterization-rules-interaction"></a>Interacción de las reglas de rasterización

En el modo de rasterización conservador, las reglas de rasterización se aplican de la misma manera que cuando no se habilita el modo de rasterización conservadora con las excepciones para la regla de Top-Left, descrita anteriormente y cobertura de píxeles. 16,8 Fixed-Point se debe usar la precisión del rasterizador.

Los píxeles que no se tratarían si el hardware usara coordenadas de vértices de punto flotante completas solo se pueden incluir si se encuentran dentro de una región de incertidumbre no más de la mitad de un píxel en el dominio de punto fijo. Se espera que el hardware futuro llegue a la región de incertidumbre apretada especificada en el nivel 2. Tenga en cuenta que este requisito evita que los triángulos de astillas se extiendan más de lo necesario.

También se aplica una región de incertidumbre válida similar `InnerCoverage` , pero es más estrecha, ya que no hay implementaciones que requieran una región de incertidumbre más grande para este caso. Consulte [interacción de InnerCoverage](#innercoverage-interaction) para obtener más detalles.

Las regiones de incertidumbre interna y externa deben ser mayores o iguales que el tamaño de la mitad de la cuadrícula de subpíxeles, o 1/512 de un píxel, en el dominio de punto fijo. Esta es la región de incertidumbre mínima válida. 1/512 procede de la representación de coordenadas del rasterizador de punto fijo 16,8 y la regla de redondeo a la más cercana que se aplica cuando se convierten coordenadas de vértices de punto flotante en las coordenadas de punto fijo de 16,8. 1/512 puede cambiar si cambia la precisión del rasterizador. Si una implementación implementa esta región de incertidumbre mínima, debe seguir la regla de Top-Left cuando el borde o la esquina de la región de incertidumbre cae a lo largo del borde o la esquina de un píxel. Los bordes recortados de la región de incertidumbre deben tratarse como el vértice más cercano, lo que significa que cuenta como dos bordes: los dos que se unen en el vértice asociado. Top-Left regla es necesaria cuando se usa la región de incertidumbre mínima, ya que, si no es así, una implementación de rasterización conservadora no podría rasterizar los píxeles que se podrían cubrir cuando el modo de rasterización conservador esté deshabilitado.

En el diagrama siguiente se muestra una región de incertidumbre externa válida que se genera mediante el barrido de un cuadrado alrededor de los bordes de la primitiva en el dominio de punto fijo (es decir, los vértices se han cuantificado por la representación de punto fijo 16,8). Las dimensiones de este cuadrado se basan en el tamaño de la región de incertidumbre externa válida: para 1/2 de un píxel, el cuadrado es 1 píxel en ancho y alto, para 1/512 de un píxel, el cuadrado es 1/256 de un píxel en ancho y alto. El triángulo verde representa un primitivo determinado, la línea de puntos rojo representa el límite de la rasterización conservadora sobreestimada, los cuadrados negros sólidos representan el cuadrado que se barre a lo largo de los bordes primitivos, y el área de la caja de la incertidumbre externa es la región de incertidumbre externa:

![región de incertidumbre externa.](images/outercoverage.jpg)

### <a name="multisampling-interaction"></a>Interacción con muestreo múltiple

Independientemente del número de muestras en las  / superficies **DepthStencil** de RenderTarget (o de si se está usando o no *ForcedSampleCount* ), todas las muestras se describen para los píxeles rasterizados por la rasterización conservadora. Las ubicaciones de ejemplo individuales no se comprueban si se encuentran en el primitivo o no.

### <a name="samplemask-interaction"></a>Interacción con SampleMask

El estado del rasterizador *SampleMask* se aplica de la misma manera que cuando la rasterización conservadora no está habilitada para `InputCoverage` , pero no afecta a `InnerCoverage` (es decir, no se AND'ed en una entrada declarada con `InnerCoverage` ). Esto se debe `InnerCoverage` a que no está relacionado con si se enmascaran los ejemplos de MSAA: 0 `InnerCoverage` solo significa que no se garantiza que el píxel esté totalmente incluido, y no que no se actualizará ningún ejemplo.

### <a name="depthstencil-test-interaction"></a>Interacción de prueba de profundidad/estarcido

Las pruebas de profundidad y estarcido se comprueban para un píxel con rasterización conservadora de la misma manera que si todas las muestras se incluyen cuando la rasterización conservadora no está habilitada.

Continuar con todos los ejemplos que se incluyen pueden provocar la extrapolación de profundidad, que es válida y se debe fijar en la ventanilla tal y como se especifica cuando no se habilita la rasterización conservadora. Esto es similar a cuando se usan los modos de interpolación de frecuencia de píxeles en **RenderTarget** con un recuento de muestras mayor que 1, aunque en el caso de una rasterización conservadora, es el valor de profundidad que entra en la prueba de profundidad de la función fija que se puede extrapolar.

El comportamiento de selección de profundidad temprana con la extrapolación de profundidad es indefinido. Esto se debe a que algunos de los hardware de selección de profundidad de nivel temprano no admiten correctamente los valores de profundidad extrapolada. Sin embargo, el comportamiento de selección de profundidad temprana en la presencia de la extrapolación de profundidad es problemático incluso con hardware que puede admitir valores de profundidad extrapolada. Este problema se puede solucionar si se fija la profundidad de entrada del sombreador de píxeles a los valores de profundidad mínimo y máximo de la primitiva que se está rasterizando y escribiendo el valor en `oDepth` (el registro de profundidad de salida del sombreador de píxeles). Las implementaciones son necesarias para deshabilitar la selección de profundidad temprana en este caso, debido a la `oDepth` escritura.

### <a name="helper-pixel-interaction"></a>Interacción de píxeles de la aplicación auxiliar

Las reglas de píxeles auxiliares se aplican de la misma manera que cuando la rasterización conservadora no está habilitada. Como parte de esto, todos los píxeles, incluidos los píxeles de la aplicación auxiliar, deben notificarse con `InputCoverage` exactitud tal y como se especifica en la `InputCoverage` sección interacción. Por lo tanto, el informe 0 de píxeles totalmente no cubiertos.

### <a name="output-coverage-interaction"></a>Interacción de la cobertura de salida

La cobertura de salida ( `oMask` ) se comporta para un píxel con rasterización conservadora tal como hace cuando la rasterización conservadora no está habilitada con todos los ejemplos cubiertos.

### <a name="inputcoverage-interaction"></a>Interacción con InputCoverage

En el modo de rasterización conservador, este registro de entrada se rellena como si todos los ejemplos se trataran cuando no se habilita la rasterización conservadora para un píxel determinado con rasterización conservadora. Es decir, se aplican todas las interacciones existentes (por ejemplo, se aplica *SampleMask* ) y los primeros n bits de `InputCoverage` la LSB se establecen en 1 para un píxel con rasterización conservadora, dado una muestra n por  píxel y/o búfer de **DepthStencil** enlazado en la **fusión de salida**, o una *ForcedSampleCount* de ejemplo n. El resto de los bits son 0.

Esta entrada está disponible en un sombreador independientemente del uso de la rasterización conservadora, aunque la rasterización conservadora cambia su comportamiento para mostrar solo todos los ejemplos incluidos (o ninguno para los píxeles auxiliares).

### <a name="innercoverage-interaction"></a>Interacción con InnerCoverage

Esta característica es necesaria para y solo está disponible en el nivel 3. El tiempo de ejecución producirá un error en la creación del sombreador para los sombreadores que utilizan este modo cuando una implementación admite un nivel inferior al nivel 3.

El sombreador de píxeles tiene un valor de generación de sistema entero escalar de 32 bits disponible: `InnerCoverage` . Se trata de un campo de bits con un bit 0 de LSB establecido en 1 para un píxel determinado con rasterización conservadora, solo cuando se garantiza que ese píxel está completamente dentro del primitivo actual. El resto de bits de registro de entrada debe establecerse en 0 cuando no se establece el bit 0, pero no están definidos cuando el bit 0 está establecido en 1 (esencialmente, este campo de bits representa un valor booleano en el que false debe ser exactamente 0, pero true puede ser cualquier valor distinto de cero (es decir, bit 0 establecido). Esta entrada se utiliza para la información de rasterización conservadora subestimada. Informa al sombreador de píxeles si el píxel actual está completamente dentro de la geometría.

Este debe tener en cuenta el error de ajuste en resoluciones mayores o iguales que la resolución en la que está funcionando el dibujo actual. No debe haber falsos positivos (estableciendo `InnerCoverage` bits cuando el píxel no está totalmente incluido en los errores de ajuste en resoluciones mayores o iguales que la resolución en la que está funcionando el dibujo actual), pero se permiten falsos negativos. En Resumen, la implementación no debe identificar incorrectamente los píxeles como están totalmente descritos, lo que no sería con coordenadas de vértices de punto flotante completas en el rasterizador.

Los píxeles que se tratarán totalmente si el hardware estaba usando coordenadas de vértices de punto flotante completas solo se pueden omitir si se intersecan con la región de incertidumbre interna, que no debe ser mayor que el tamaño de la cuadrícula de subpíxeles, o 1/256 de un píxel, en el dominio de punto fijo. Dicho de otro modo, los píxeles que están completamente dentro del límite interno de la región de incertidumbre interna deben estar marcados como totalmente descritos. El límite interno de la región de incertidumbre se ilustra en el diagrama siguiente por la línea de puntos negro en negrita. 1/256 procede de la representación de coordenadas del rasterizador de punto fijo 16,8, que puede cambiar si cambia la precisión del rasterizador. Esta región de incertidumbre es suficiente para tener en cuenta el error de ajuste provocado por la conversión de coordenadas de vértices de punto flotante en coordenadas de vértice de punto fijo en el rasterizador.

Los mismos requisitos de la región de incertidumbre mínima de 1/512 definidos en reglas de rasterización también se aplican aquí.

En el diagrama siguiente se muestra una región de incertidumbre interna válida que se genera mediante el barrido de un cuadrado alrededor de los bordes de la primitiva en el dominio de punto fijo (es decir, los vértices se han cuantificado por la representación de punto fijo 16,8). Las dimensiones de este cuadrado se basan en el tamaño de la región de incertidumbre interna válida: para 1/256 de un píxel, el cuadrado es 1/128 de un píxel en ancho y alto. El triángulo verde representa un primitivo determinado, mientras que la línea de puntos negros en negrita representa el límite de la región de incertidumbre interna, los cuadrados negros sólidos representan el cuadrado que se barre a lo largo de los bordes primitivos y el área de la incertidumbre de color naranja es la región de incertidumbre interna:

![reqion de incertidumbre interna.](images/innercoverage.jpg)

El uso de `InnerCoverage` no afecta a si un píxel se rasteriza de manera conservadora, es decir, el uso de uno de estos `InputCoverage` modos no afecta a qué píxeles se rasterizan cuando se habilita el modo de rasterización conservador. Por lo tanto, cuando `InnerCoverage` se usa y el sombreador de píxeles está procesando un píxel que no está completamente incluido en la geometría, su valor será 0, pero la invocación del sombreador de píxeles tendrá las muestras actualizadas. Es diferente de cuando `InputCoverage` es 0, lo que significa que no se actualizará ningún ejemplo.

Esta entrada es mutuamente excluyente con `InputCoverage` : no se pueden usar ambos.

Para tener acceso a `InnerCoverage` , se debe declarar como un componente único de uno de los registros de entrada del sombreador de píxeles. El modo de interpolación en la declaración debe ser constante (no se aplica la interpolación).

El `InnerCoverage` campo de bits no se ve afectado por las pruebas de profundidad/estarcido, ni tampoco por el estado de rasterizador *SampleMask* .

Esta entrada solo es válida en el modo de rasterización conservador. Cuando no se habilita la rasterización conservadora, `InnerCoverage` genera un valor indefinido.

Las invocaciones del sombreador de píxeles provocadas por la necesidad de píxeles de aplicación auxiliar, pero que de otro modo no están incluidos en la primitiva, deben tener el `InnerCoverage` registro establecido en 0.

### <a name="attribute-interpolation-interaction"></a>Interacción de interpolación de atributos

Los modos de interpolación de atributos no cambian y continúan de la misma manera que cuando la rasterización conservadora no está habilitada, donde se usan los vértices con escala de ventanilla y conversión de punto fijo. Dado que se consideran todas las muestras de un píxel con rasterización conservadora, es válido para la extrapolación de los valores, de forma similar a cuando se usan los modos de interpolación de frecuencia de píxeles en **RenderTarget** con un recuento de muestras mayor que 1. Los modos de interpolación centroide producen resultados idénticos al modo de interpolación no centroide correspondiente; la noción de centroide no tiene sentido en este escenario, donde la cobertura de ejemplo solo es Full o 0.

La rasterización conservadora permite que los triángulos degenerados generen invocaciones del sombreador de píxeles; por lo tanto, los triángulos degenerados deben usar los valores asignados al vértice 0 para todos los valores interpolados.

### <a name="clipping-interaction"></a>Interacción de recorte

Cuando está habilitado el modo de rasterización conservador y se deshabilita el clip de profundidad (cuando el estado del rasterizador *DepthClipEnable* está establecido en false), puede haber variaciones en la interpolación de atributos para los segmentos de una primitiva que se encuentran fuera del 0 <= z <= w, dependiendo de la implementación: los valores constantes se utilizan desde un punto en el que el primitivo intersecta con el plano pertinente (Near o Far) o la interpolación de atributos se comporta como cuando el modo de rasterización conservador está deshabilitado. Sin embargo, el comportamiento del valor de profundidad es el mismo, independientemente del modo de rasterización conservador, es decir, los primitivos que se encuentran fuera del intervalo de profundidad deben seguir teniendo el valor del límite más cercano del intervalo de profundidad de la ventanilla. El comportamiento de interpolación de atributo dentro del 0 <= z <= el intervalo de w debe permanecer sin cambios.

### <a name="clip-distance-interaction"></a>Interacción de distancia del clip

La distancia del clip es válida cuando el modo de rasterización conservador está habilitado y se comporta para un píxel con rasterización conservadora, tal como se hace cuando la rasterización conservadora no está habilitada con todos los ejemplos que se incluyen.

Tenga en cuenta que la rasterización conservadora puede producir la extrapolación de la coordenada del vértice W, lo que puede dar lugar a W <= 0. Esto podría provocar que las implementaciones de la distancia de los clips por píxel funcionen en una distancia de recorte que se ha dividido entre un valor W no válido. Las implementaciones de la distancia de clip deben protegerse contra la invocación de rasterización para los píxeles en los que la coordenada de vértices W <= 0 (por ejemplo, debido a la extrapolación en el modo de rasterización conservador).

### <a name="target-independent-rasterization-interaction"></a>Interacción de rasterización independiente de destino

El modo de rasterización conservador es compatible con la rasterización independiente de destino (TIR). Se aplican las reglas y restricciones de TIR, comparando un píxel con rasterización conservadora como si se trataran todos los ejemplos.

### <a name="ia-primitive-topology-interaction"></a>Interacción de topología de primitivas de IA

La rasterización conservadora no se define para los primitivos de línea o punto. Por lo tanto, las topologías primitivas que especifican puntos o líneas producen un comportamiento indefinido si se alimentan a la unidad de rasterizador cuando se habilita la rasterización conservadora.

La validación de la capa de depuración comprueba que las aplicaciones no usan estas topologías primitivas.

### <a name="query-interaction"></a>Interacción de consultas

En el caso de un píxel con rasterización conservadora, las consultas se comportan de la misma manera que cuando la rasterización conservadora no está habilitada cuando se incluyen todas las muestras. Por ejemplo, para un píxel con rasterización conservadora, las estadísticas de tipo de consulta D3D12 \_ \_ y las \_ \_ \_ \_ estadísticas de canalización de tipo de consulta D3D12 \_ (del [**\_ \_ tipo de consulta D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_query_type)) deben comportarse tal y como lo harían si la rasterización conservadora no estuviera habilitada cuando se cubran todas las muestras.

Las invocaciones del sombreador de píxeles deben incrementarse para cada píxel con rasterización conservadora en el modo de rasterización conservador.

### <a name="cull-state-interaction"></a>Interacción del estado de culling

Todos los Estados de selección son válidos en el modo de rasterización conservador y siguen las mismas reglas que cuando la rasterización conservadora no está habilitada.

Al comparar la rasterización conservadora entre resoluciones a sí misma o sin rasterización conservadora habilitada, existe la posibilidad de que algunos primitivos puedan tener una falta de coincidencia (es decir, uno hacia atrás, el otro frente). Las aplicaciones pueden evitar esta incertidumbre mediante \_ el uso \_ \_ del modo de selección de D3D12 no (en el [**\_ \_ modo de selección de D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_cull_mode)) y no usar el valor generado por el `IsFrontFace` sistema.

### <a name="isfrontface-interaction"></a>Interacción con IsFrontFace

El `IsFrontFace` valor generado por el sistema es válido para su uso en el modo de rasterización conservador y sigue el comportamiento definido cuando no se habilita la rasterización conservadora.

### <a name="fill-modes-interaction"></a>Interacción de los modos de relleno

El único [**modo de \_ relleno \_ D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_fill_mode) válido para la rasterización conservadora es D3D12 \_ Fill \_ Solid, cualquier otro modo de relleno es un parámetro no válido para el estado de rasterizador.

Esto se debe a que la especificación funcional de D3D12 especifica que el modo de relleno de trama de alambre debe convertir los bordes de triángulo en líneas y seguir las reglas de rasterización de línea y el comportamiento de rasterización de líneas conservadora no se ha definido.

## <a name="implementation-details"></a>Detalles de la implementación

El tipo de rasterización compatible con Direct3D 12 a veces se conoce como "rasterización conservadora sobreestimada". También existe el concepto de "rasterización conservadora desestimada", lo que significa que solo se rasterizan los píxeles que están totalmente incluidos en una primitiva representada. La información de rasterización conservadora subestimada está disponible a través del sombreador de píxeles mediante el uso de datos de cobertura de entrada y solo está disponible la rasterización conservadora sobreestimada como modo de rasterización.

Si alguna parte de una primitiva se superpone a un píxel, ese píxel se considerará tratado y se rasterizará. Cuando un borde o esquina de una primitiva cae a lo largo del borde o la esquina de un píxel, la aplicación de la "regla superior izquierda" es específica de la implementación. Sin embargo, para las implementaciones que admiten triángulos degenerados, un triángulo degenerado a lo largo de un borde o una esquina debe cubrir al menos un píxel.

Las implementaciones de rasterización conservadora pueden variar en hardware diferente y generar falsos positivos, lo que significa que pueden decidir incorrectamente que los píxeles están incluidos. Esto puede deberse a detalles específicos de la implementación, como los errores primitivos de aumento o ajuste inherentes a las coordenadas de vértices de punto fijo utilizadas en la rasterización. La razón por la que los falsos positivos (con respecto a las coordenadas de vértices de punto fijo) son válidos es que se necesita una cantidad de falsos positivos para permitir que una implementación realice la evaluación de cobertura en los vértices con ajuste de nivel (es decir, las coordenadas de vértices que se han convertido desde el punto flotante al punto fijo 16,8 usado en el rasterizador), pero

Las implementaciones de rasterización conservadora no producen falsos negativos con respecto a las coordenadas de vértices de punto flotante para primitivas posteriores al ajuste no generadas: Si alguna parte de una primitiva se superpone a cualquier parte de un píxel, ese píxel se rasteriza.

Los triángulos degenerados (índices duplicados en un búfer de índice o colineales en 3D), o se convierten en degenerados después de la conversión de punto fijo (vértices colineales en el rasterizador), pueden o no ser reactivados; ambos son comportamientos válidos. Los triángulos degenerados se deben tener en cuenta hacia atrás, por lo que si una aplicación requiere un comportamiento concreto, puede utilizar la selección de la parte trasera o la prueba para orientarse hacia delante. Los triángulos degenerados usan los valores asignados al vértice 0 para todos los valores interpolados.

Hay tres niveles de compatibilidad de hardware, además de la posibilidad de que el hardware no sea compatible con esta característica.

-   El nivel 1 aplica una región de incertidumbre de 1/2 píxeles como máximo y no admite la degeneración posterior al ajuste. Esto es adecuado para la representación en mosaico, un Atlas de textura, la generación de mapas ligeros y las instantáneas de subpíxeles.
-   El nivel 2 reduce la región de incertidumbre máxima a 1/256 y requiere que se devuelvan las desgeneraciones posteriores a la instantánea. Este nivel es útil para la aceleración del algoritmo basado en la CPU (por ejemplo, voxelization).
-   El nivel 3 mantiene una región de incertidumbre 1/256 máxima y agrega compatibilidad con la cobertura de entrada interna. La cobertura de entrada interna agrega el nuevo valor `SV_InnerCoverage` al lenguaje de sombreado de alto nivel (HLSL). Se trata de un entero escalar de 32 bits que se puede especificar en la entrada a un sombreador de píxeles y que representa la información de rasterización conservadora subestimada (es decir, si se garantiza que un píxel está totalmente incluido). Este nivel es útil para la selección de la oclusión.

## <a name="api-summary"></a>API summary

Los siguientes métodos, estructuras, enumeraciones y clases auxiliares hacen referencia a la rasterización conservadora:

-   [**D3D12 \_ RASTERIZAdor \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rasterizer_desc) : estructura que contiene la descripción del rasterizador.
-   [**D3D12 \_ \_ \_ Modo de rasterización conservador**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_conservative_rasterization_mode) : valores de enumeración para el modo (activado o desactivado).
-   [**D3D12 \_ \_Opciones de \_ D3D12 \_ de datos de características**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options) : estructura que contiene el nivel de compatibilidad.
-   [**D3D12 \_ \_ \_ Nivel de rasterización conservador**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_conservative_rasterization_tier) : valores de enumeración para cada nivel de soporte del hardware.
-   [**CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) : método para tener acceso a las características admitidas.
-   [**CD3DX12 \_ RASTERIZAdor \_ DESC**](cd3dx12-rasterizer-desc.md) : clase auxiliar para crear descripciones de rasterizador.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tutoriales de vídeo de aprendizaje avanzado de DirectX: rasterización conservadora](https://www.youtube.com/watch?v=zL0oSY_YmDY)
</dt> <dt>

[Vistas ordenadas de rasterizador](rasterizer-order-views.md)
</dt> <dt>

[Representación](rendering.md)
</dt> </dl>

 

 




