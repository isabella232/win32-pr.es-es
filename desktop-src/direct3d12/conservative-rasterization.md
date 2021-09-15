---
title: Rasterización conservadora de Direct3D 12
description: La rasterización conservadora agrega cierta certeza a la representación de píxeles, lo que resulta útil en particular para los algoritmos de detección de colisiones.
ms.assetid: 081199AD-1702-4EC8-95AD-B1148C676199
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e4fae3489d54ab7b6b7abfda56f54dd8d970962
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127570908"
---
# <a name="direct3d-12-conservative-rasterization"></a>Rasterización conservadora de Direct3D 12

La rasterización conservadora agrega cierta certeza a la representación de píxeles, lo que resulta útil en particular para los algoritmos de detección de colisiones.

-   [Información general](#overview)
-   [Interacciones con la canalización](#interactions-with-the-pipeline)
    -   [Interacción de reglas de rasterización](#rasterization-rules-interaction)
    -   [Interacción multimuestreo](#multisampling-interaction)
    -   [Interacción de SampleMask](#samplemask-interaction)
    -   [Interacción de la prueba de profundidad y galería de símbolos](#depthstencil-test-interaction)
    -   [Interacción de píxeles del asistente](#helper-pixel-interaction)
    -   [Interacción de cobertura de salida](#output-coverage-interaction)
    -   [Interacción inputCoverage](#inputcoverage-interaction)
    -   [Interacción de InnerCoverage](#innercoverage-interaction)
    -   [Interacción de interpolación de atributos](#attribute-interpolation-interaction)
    -   [Interacción de recorte](#clipping-interaction)
    -   [Interacción de la distancia de recorte](#clip-distance-interaction)
    -   [Interacción de rasterización independiente de destino](#target-independent-rasterization-interaction)
    -   [Interacción de topología primitiva de IA](#ia-primitive-topology-interaction)
    -   [Interacción de consultas](#query-interaction)
    -   [Interacción del estado Cull](#cull-state-interaction)
    -   [Interacción de IsFrontFace](#isfrontface-interaction)
    -   [Interacción de los modos de relleno](#fill-modes-interaction)
-   [Detalles de la implementación](#implementation-details)
-   [Resumen de API](#api-summary)
-   [Temas relacionados](#related-topics)

## <a name="overview"></a>Información general

La rasterización conservadora significa que todos los píxeles que están cubiertos parcialmente por un primitivo representado se rasterizan, lo que significa que se invoca el sombreador de píxeles. El comportamiento normal es el muestreo, que no se usa si está habilitada la rasterización conservadora.

La rasterización conservadora es útil en una serie de situaciones, incluida la certeza en la detección de colisiones, la selección de oclusión y la representación en mosaico.

Por ejemplo, en la ilustración siguiente se muestra un triángulo verde representado mediante rasterización conservadora, como aparecería en el rasterizador (es decir, mediante coordenadas de vértice de punto fijo 16,8). El área marrones se conoce como "región de incertidumbre", una región conceptual que representa los límites extendidos del triángulo, necesario para garantizar que la primitiva del rasterizador es conservadora con respecto a las coordenadas de vértice de punto flotante originales. Los cuadrados rojos de cada vértice muestran cómo se calcula la región de incertidumbre: como un cuadrado desasociado.

Los cuadrados grises grandes muestran los píxeles que se representarán. Los cuadrados de color rojo muestran píxeles representados mediante la "regla superior izquierda", que entra en juego a medida que el borde del triángulo cruza el borde de los píxeles. Puede haber falsos positivos (conjunto de píxeles que no deberían haber sido) que el sistema normalmente, pero no siempre cull.

![la regla superior izquierda](images/conservative-rasterization-0.png)

## <a name="interactions-with-the-pipeline"></a>Interacciones con la canalización

### <a name="rasterization-rules-interaction"></a>Interacción de reglas de rasterización

En el modo de rasterización conservadora, las reglas de rasterización se aplican de la misma manera que cuando el modo de rasterización conservadora no está habilitado con excepciones para la regla de Top-Left, descrita anteriormente, y la cobertura de píxeles. 16.8 Fixed-Point se debe usar la precisión del rasterizador.

Los píxeles que no se cubrirían si el hardware usaba coordenadas de vértice de punto flotante completa solo se pueden incluir si se encuentran dentro de una región de incertidumbre que no tiene más de medio píxel en el dominio de punto fijo. Se espera que el hardware futuro llegue a la región de incertidumbre más apretada especificada en el nivel 2. Tenga en cuenta que este requisito impide que los triángulos de aslo se extienda más de lo necesario.

También se aplica una región de incertidumbre válida similar, pero es más estricta, ya que ninguna implementación requiere una región de incertidumbre mayor `InnerCoverage` para este caso. Consulte [Interacción de InnerCoverage](#innercoverage-interaction) para obtener más detalles.

Las regiones de incertidumbre interna y externa deben ser mayores o iguales que el tamaño de la mitad de la cuadrícula de sub píxeles, o 1/512 de un píxel, en el dominio de punto fijo. Esta es la región de incertidumbre mínima válida. 1/512 procede de la representación de coordenadas rasterizadora de punto fijo de 16,8 y la regla de redondeo a punto más cercano que se aplica al convertir coordenadas de vértice de punto flotante en coordenadas de punto fijo 16,8. 1/512 puede cambiar si cambia la precisión del rasterizador. Si una implementación implementa esta región de mínima incertidumbre, debe seguir la regla de Top-Left cuando un borde o una esquina de la región de incertidumbre se encuentra a lo largo del borde o la esquina de un píxel. Los bordes recortados de la región de incertidumbre deben tratarse como el vértice más cercano, lo que significa que cuenta como dos bordes: los dos que se unen en el vértice asociado. Top-Left regla es necesaria cuando se usa la región de incertidumbre mínima porque, si no es así, una implementación de rasterización conservadora no podría rasterizar píxeles que podrían cubrirse cuando el modo de rasterización conservadora está deshabilitado.

En el diagrama siguiente se muestra una región de incertidumbre externa válida producida al barrido de un cuadrado alrededor de los bordes de la primitiva en el dominio de punto fijo (es decir, los vértices se han cuantificado mediante la representación de punto fijo de 16,8). Las dimensiones de este cuadrado se basan en el tamaño válido de la región de incertidumbre externa: para el 1/2 de un píxel, el cuadrado tiene 1 píxel de ancho y alto; para 1/512 de un píxel, el cuadrado es 1/256 de un píxel de ancho y alto. El triángulo verde representa una primitiva determinada, la línea de puntos rojos representa el límite de la rasterización conservadora sobrestimada, los cuadrados negros sólidos representan el cuadrado que se representa a lo largo de los bordes primitivos y el área azul a cuadros es la región de incertidumbre externa:

![región de incertidumbre externa.](images/outercoverage.jpg)

### <a name="multisampling-interaction"></a>Interacción multimuestreo

Independientemente del número de muestras de las superficies **renderTarget** / **DepthStencil** (o si *forcedSampleCount* se usa o no), todas las muestras se tratan para los píxeles rasterizados por rasterización conservadora. Las ubicaciones de ejemplo individuales no se prueban si se encuentran en la primitiva o no.

### <a name="samplemask-interaction"></a>Interacción de SampleMask

El estado de rasterizador *sampleMask* se aplica de la misma manera que cuando la rasterización conservadora no está habilitada para , pero no afecta (es decir, no está `InputCoverage` `InnerCoverage` and'ed en una entrada declarada con `InnerCoverage` ). Esto se debe a que no está relacionado con si las muestras de MSAA se enmascaran: 0 solo significa que no se garantiza que el píxel esté totalmente cubierto, no que no se actualizará ninguna `InnerCoverage` `InnerCoverage` muestra.

### <a name="depthstencil-test-interaction"></a>Interacción de la prueba de profundidad y galería de símbolos

Las pruebas de profundidad y galería de símbolos proceden de un píxel rasterizado de forma conservadora de la misma manera que si todas las muestras se cubren cuando la rasterización conservadora no está habilitada.

Continuar con todas las muestras cubiertas puede provocar la extrapolación de profundidad, que es válida y debe fijarse a la ventanilla como se especifica cuando la rasterización conservadora no está habilitada. Esto es similar a cuando se usan modos de interpolación de frecuencia de píxeles en **renderTarget** con un recuento de muestras mayor que 1, aunque en el caso de la rasterización conservadora, es el valor de profundidad que entra en la prueba de profundidad de función fija que se puede extrapolar.

El comportamiento de la selección de profundidad temprana con extrapolación de profundidad no está definido. Esto se debe a que algún hardware de selección de profundidad temprana no puede admitir correctamente valores de profundidad extrapolados. Sin embargo, el comportamiento de la selección de profundidad temprana en presencia de extrapolación de profundidad es problemático incluso con hardware que puede admitir valores de profundidad extrapolados. Este problema se puede resolver mediante la fijación de la profundidad de entrada del sombreador de píxeles a los valores de profundidad mínimo y máximo de la primitiva que se va a rasterizar y escribir ese valor en (el registro de profundidad de salida del sombreador de `oDepth` píxeles). Las implementaciones son necesarias para deshabilitar la selección de profundidad temprana en este caso, debido a la `oDepth` escritura.

### <a name="helper-pixel-interaction"></a>Interacción de píxeles del asistente

Las reglas de píxeles del asistente se aplican de la misma manera que cuando la rasterización conservadora no está habilitada. Como parte de esto, todos los píxeles, incluidos los píxeles del asistente, deben informar con precisión `InputCoverage` como se especifica en la sección de `InputCoverage` interacción. Por lo tanto, los píxeles no cubiertos informan de la cobertura 0.

### <a name="output-coverage-interaction"></a>Interacción de cobertura de salida

La cobertura de salida ( ) se comporta para un píxel rasterizado de forma conservadora, al igual que cuando la rasterización conservadora no está habilitada `oMask` con todos los ejemplos cubiertos.

### <a name="inputcoverage-interaction"></a>Interacción inputCoverage

En el modo rasterización conservadora, este registro de entrada se rellena como si todas las muestras se cubren cuando la rasterización conservadora no está habilitada para un píxel determinado con rasterización conservadora. Es decir, se aplican todas las interacciones existentes (por ejemplo, se aplica *SampleMask)* y los primeros n bits de la LSB se establecen en 1 para un píxel rasterizado de forma conservadora, dado un ejemplo n por píxel `InputCoverage` **RenderTarget** o **búfer DepthStencil** enlazado en la fusión de salida o un ejemplo *n ForcedSampleCount*.  El resto de los bits son 0.

Esta entrada está disponible en un sombreador independientemente del uso de rasterización conservadora, aunque la rasterización conservadora cambia su comportamiento para mostrar solo todas las muestras cubiertas (o ninguna para los píxeles del asistente).

### <a name="innercoverage-interaction"></a>Interacción de InnerCoverage

Esta característica es necesaria y solo está disponible en el nivel 3. El tiempo de ejecución producirá un error en la creación del sombreador para los sombreadores que usan este modo cuando una implementación admite un nivel inferior al nivel 3.

El sombreador de píxeles tiene disponible un entero escalar de 32 bits System Generate Value: `InnerCoverage` . Se trata de un campo de bits que tiene el bit 0 del LSB establecido en 1 para un píxel determinado con rasterización conservadora, solo cuando se garantiza que ese píxel está completamente dentro de la primitiva actual. Todos los demás bits de registro de entrada deben establecerse en 0 cuando el bit 0 no está establecido, pero no están definidos cuando el bit 0 se establece en 1 (básicamente, este campo de bits representa un valor booleano donde false debe ser exactamente 0, pero true puede ser cualquier valor impar (es decir, un bit 0 establecido) distinto de cero). Esta entrada se usa para la información de rasterización conservadora subestimada. Informa al sombreador de píxeles si el píxel actual se encuentra completamente dentro de la geometría.

Esto debe tener en cuenta el error de ajuste en resoluciones mayores o iguales que la resolución en la que funciona el draw actual. No debe haber falsos positivos (establecer bits cuando el píxel no está totalmente cubierto para cualquier error de ajuste en resoluciones mayores o iguales que la resolución en la que está funcionando el draw actual), pero se permiten `InnerCoverage` falsos negativos. En resumen, la implementación no debe identificar incorrectamente los píxeles como totalmente cubiertos que no estarían con coordenadas de vértice de punto flotante completa en el rasterizador.

Los píxeles que se cubrirían por completo si el hardware usaba coordenadas de vértice de punto flotante completa solo se pueden omitir si intersecan con la región de incertidumbre interna, que no debe ser mayor que el tamaño de la cuadrícula de subpíxeles, o 1/256 de un píxel, en el dominio de punto fijo. Dicho de otro modo, los píxeles completamente dentro del límite interno de la región de incertidumbre interna deben marcarse como totalmente cubiertos. El límite interno de la región de incertidumbre se ilustra en el diagrama siguiente con la línea de puntos negra en negrita. 1/256 procede de la representación de coordenadas de rasterizador de punto fijo 16,8, que puede cambiar si cambia la precisión del rasterizador. Esta región de incertidumbre es suficiente para tener en cuenta el error de ajuste causado por la conversión de coordenadas de vértice de punto flotante en coordenadas de vértice de punto fijo en el rasterizador.

Aquí también se aplican los mismos requisitos mínimos de región de incertidumbre de 1/512 definidos en la interacción de reglas de rasterización.

En el diagrama siguiente se muestra una región de incertidumbre interna válida producida al barrido de un cuadrado alrededor de los bordes de la primitiva en el dominio de punto fijo (es decir, los vértices se han cuantificado mediante la representación de punto fijo de 16,8). Las dimensiones de este cuadrado se basan en el tamaño válido de la región de incertidumbre interna: para 1/256 de un píxel, el cuadrado es 1/128 de píxel de ancho y alto. El triángulo verde representa una primitiva determinada, la línea de puntos negra en negrita representa el límite de la región de incertidumbre interna, los cuadrados negros sólidos representan el cuadrado que se representa a lo largo de los bordes primitivos y el área de color naranja a la que se hace el checkered es la región de incertidumbre interna:

![reqion de incertidumbre interna.](images/innercoverage.jpg)

El uso de no afecta a si un píxel se rasteriza de forma conservadora, es decir, el uso de uno de estos modos no afecta a los píxeles que se rasterizan cuando está habilitado el modo `InnerCoverage` `InputCoverage` rasterización conservadora. Por lo tanto, cuando se usa y el sombreador de píxeles está procesando un píxel que no está completamente cubierto por la geometría, su valor será 0, pero la invocación del sombreador de píxeles tendrá ejemplos `InnerCoverage` actualizados. Esto es diferente de cuando `InputCoverage` es 0, lo que significa que no se actualizará ninguna muestra.

Esta entrada es mutuamente excluyente con `InputCoverage` : no se pueden usar ambos.

Para tener acceso a , debe declararse como un único componente de uno de los registros de entrada del `InnerCoverage` sombreador de píxeles. El modo de interpolación de la declaración debe ser constante (no se aplica la interpolación).

El campo de bits no se ve afectado por las pruebas de profundidad o galería de símbolos, ni por el estado `InnerCoverage` *rasterizador samplemask.*

Esta entrada solo es válida en el modo de rasterización conservadora. Cuando la rasterización conservadora no está habilitada, `InnerCoverage` genera un valor indefinido.

Las invocaciones del sombreador de píxeles causadas por la necesidad de píxeles auxiliares, pero que de lo contrario no están cubiertas por la primitiva, deben tener el registro `InnerCoverage` establecido en 0.

### <a name="attribute-interpolation-interaction"></a>Interacción de interpolación de atributos

Los modos de interpolación de atributos no se modifican y avanzan de la misma manera que cuando la rasterización conservadora no está habilitada, donde se usan los vértices con escala de ventanilla y con conversión de punto fijo. Dado que todas las muestras de un píxel con rasterización conservadora se consideran cubiertas, es válido que los valores se puedan extrapolar, de forma similar a cuando se usan modos de interpolación de frecuencia de píxeles en **renderTarget** con un recuento de muestras mayor que 1. Los modos de interpolación centroide generan resultados idénticos al modo de interpolación no centroide correspondiente; La noción de centroide no tiene sentido en este escenario, donde la cobertura de ejemplo solo está completa o 0.

La rasterización conservadora permite que los triángulos degenerados produzcan invocaciones de sombreador de píxeles, por lo que los triángulos degenerados deben usar los valores asignados al vértice 0 para todos los valores interpolados.

### <a name="clipping-interaction"></a>Interacción de recorte

Cuando el modo de rasterización conservadora está habilitado y el clip de profundidad está deshabilitado (cuando *depthclipEnable* Rasterizer State está establecido en FALSE), puede haber variaciones en la interpolación de atributos para segmentos de una primitiva que se encuentran fuera del intervalo 0 <= z <= w, dependiendo de la implementación: los valores constantes se usan desde un punto en el que la primitiva forma una intersección con el plano pertinente (cerca o lejos) o la interpolación de atributos se comporta como cuando se deshabilita el modo de rasterización conservadora. Sin embargo, el comportamiento del valor de profundidad es el mismo independientemente del modo de rasterización conservadora, es decir, las primitivas que se encuentran fuera del intervalo de profundidad deben seguir teniendo el valor del límite más cercano del intervalo de profundidad de la ventanilla. El comportamiento de interpolación de atributos dentro del intervalo 0 <= z <= w debe permanecer sin cambios.

### <a name="clip-distance-interaction"></a>Interacción de la distancia de recorte

La distancia de recorte es válida cuando el modo de rasterización conservadora está habilitado y se comporta para un píxel rasterizado conservadoramente, al igual que cuando la rasterización conservadora no está habilitada con todas las muestras cubiertas.

Tenga en cuenta que la rasterización conservadora puede provocar la extrapolación de la coordenada del vértice W, lo que puede provocar que W <= 0. Esto podría hacer que las implementaciones de clip distance por píxel funcionen en una distancia de recorte que se ha dividido en perspectiva por un valor W no válido. Las implementaciones de clip distance deben protegerse frente a la invocación de rasterización para píxeles donde la coordenada de vérticeS <= 0 (por ejemplo, debido a la extrapolación cuando se encuentra en el modo de rasterización conservadora).

### <a name="target-independent-rasterization-interaction"></a>Interacción de rasterización independiente de destino

El modo de rasterización conservadora es compatible con la rasterización independiente de destino (TIR). Se aplican las reglas y restricciones de TIR, que se comportan para un píxel rasterizado de forma conservadora como si se cubren todas las muestras.

### <a name="ia-primitive-topology-interaction"></a>Interacción de la topología primitiva de IA

La rasterización conservadora no se define para primitivas de línea o punto. Por lo tanto, las topologías primitivas que especifican puntos o líneas generan un comportamiento indefinido si se alimentan a la unidad de rasterizador cuando está habilitada la rasterización conservadora.

La validación de la capa de depuración comprueba que las aplicaciones no usan estas topologías primitivas.

### <a name="query-interaction"></a>Interacción de consultas

En el caso de un píxel con rasterización conservadora, las consultas se comportan como cuando la rasterización conservadora no está habilitada cuando se cubren todas las muestras. Por ejemplo, para un píxel de rasterización conservadora, D3D12 \_ QUERY \_ TYPE OCCLUSION y \_ D3D12 \_ QUERY TYPE PIPELINE \_ \_ \_ STATISTICS (from [**D3D12 \_ QUERY \_ TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_query_type)) deben comportarse como lo harían cuando la rasterización conservadora no está habilitada cuando se cubren todas las muestras.

Las invocaciones del sombreador de píxeles deben incrementarse por cada píxel rasterizado conservador en el modo de rasterización conservadora.

### <a name="cull-state-interaction"></a>Interacción de estado Cull

Todos los estados Cull son válidos en el modo de rasterización conservadora y siguen las mismas reglas que cuando la rasterización conservadora no está habilitada.

Al comparar la rasterización conservadora entre resoluciones a sí misma o sin la rasterización conservadora habilitada, existe la posibilidad de que algunas primitivas tengan una cara no coincidente (es decir, una hacia atrás, la otra orientada hacia delante). Las aplicaciones pueden evitar esta incertidumbre si se usa D3D12 \_ CULL \_ MODE NONE \_ (from [**D3D12 \_ CULL \_ MODE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_cull_mode)) y no se usa el valor `IsFrontFace` generado por el sistema.

### <a name="isfrontface-interaction"></a>Interacción de IsFrontFace

El valor generado por el sistema es válido para su uso en el modo de rasterización conservadora y sigue el comportamiento definido cuando la rasterización conservadora `IsFrontFace` no está habilitada.

### <a name="fill-modes-interaction"></a>Interacción de los modos de relleno

El único modo FILL de [**D3D12 \_ \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_fill_mode) válido para la rasterización conservadora es D3D12 FILL SOLID, cualquier otro modo de relleno es un parámetro no válido para el \_ estado de \_ Rasterizer.

Esto se debe a que la especificación funcional D3D12 especifica que el modo de relleno de wireframe debe convertir los bordes del triángulo en líneas y seguir las reglas de rasterización de línea y no se ha definido el comportamiento de rasterización de línea conservadora.

## <a name="implementation-details"></a>Detalles de la implementación

El tipo de rasterización admitido en Direct3D 12 a veces se conoce como "rasterización conservadora sobreestimada". También existe el concepto de "Rasterización conservadora subestimizada", lo que significa que solo se rasterizan los píxeles que están totalmente cubiertos por una primitiva representado. La información de rasterización conservadora subvalora está disponible a través del sombreador de píxeles mediante el uso de datos de cobertura de entrada, y solo está disponible la rasterización conservadora sobrestimada como modo de rasterización.

Si alguna parte de una primitiva se superpone a un píxel, ese píxel se considera cubierto y, a continuación, se rasteriza. Cuando un borde o una esquina de un primitivo se encuentra a lo largo del borde o la esquina de un píxel, la aplicación de la "regla superior izquierda" es específica de la implementación. Sin embargo, para las implementaciones que admiten triángulos degenerados, un triángulo degenerado a lo largo de un borde o una esquina debe cubrir al menos un píxel.

Las implementaciones de rasterización conservadoras pueden variar en hardware diferente y producen falsos positivos, lo que significa que pueden decidir incorrectamente que se cubren píxeles. Esto puede ocurrir debido a detalles específicos de la implementación, como errores primitivos de crecimiento o ajuste inherentes a las coordenadas de vértice de punto fijo que se usan en la rasterización. La razón por la que los falsos positivos (con respecto a las coordenadas de vértice de punto fijo) son válidos es porque se necesita cierta cantidad de falsos positivos para permitir que una implementación realice la evaluación de cobertura en los vértices posteriores al ajuste (es decir, coordenadas de vértice que se han convertido de punto flotante al punto fijo 16.8 usado en el rasterizador), pero respetan la cobertura producida por las coordenadas de vértice de punto flotante originales.

Las implementaciones de rasterización conservadora no generan falsos negativos con respecto a las coordenadas de vértice de punto flotante para primitivas post snap no degeneradas: si alguna parte de una primitiva se superpone a cualquier parte de un píxel, ese píxel se rasteriza.

Los triángulos que son degenerados (índices duplicados en un búfer de índice o colisionador en 3D) o que se vuelven degenerados después de la conversión de punto fijo (vértices de colisión en el rasterizador), pueden ser o no culled; ambos son comportamientos válidos. Los triángulos degenerados deben considerarse orientados hacia atrás, por lo que, si una aplicación requiere un comportamiento específico, puede usar la selección de cara posterior o probar la orientación frontal. Los triángulos degenerados usan los valores asignados a Vértice 0 para todos los valores interpolados.

Hay tres niveles de compatibilidad con hardware, además de la posibilidad de que el hardware no admita esta característica.

-   El nivel 1 aplica una región de incertidumbre máxima de 1/2 píxeles y no admite degenerados posteriores a la instantánea. Esto es bueno para la representación en mosaico, un atlas de textura, la generación de mapas claros y los mapas de sombra de subpíxeles.
-   El nivel 2 reduce la región de incertidumbre máxima a 1/256 y requiere que los degenerados posteriores a la instantánea no se puedan realizar. Este nivel es útil para la aceleración de algoritmos basada en CPU (por ejemplo, vóxelización).
-   El nivel 3 mantiene una región de incertidumbre máxima de 1/256 y agrega compatibilidad con la cobertura de entrada interna. La cobertura de entrada interna agrega el nuevo valor al lenguaje de `SV_InnerCoverage` sombreado de alto nivel (HLSL). Se trata de un entero escalar de 32 bits que se puede especificar en la entrada de un sombreador de píxeles y representa la información de rasterización conservadora infravalora (es decir, si se garantiza que un píxel esté totalmente cubierto). Este nivel es útil para la selección de oclusión.

## <a name="api-summary"></a>API summary

Los métodos, estructuras, enumeraciones y clases auxiliares siguientes hacen referencia a la rasterización conservadora:

-   [**D3D12 \_ RASTERIZER \_ DESC:**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rasterizer_desc) estructura que mantiene la descripción del rasterizador.
-   [**D3D12 \_ MODO \_ RASTERIZATION \_ CONSERVADOR:**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_conservative_rasterization_mode) valores de enumeración para el modo (on o off).
-   [**D3D12 \_ FEATURE \_ DATA \_ D3D12 \_ OPTIONS:**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options) estructura que mantiene el nivel de soporte técnico.
-   [**D3D12 \_ NIVEL \_ DE RASTERIZACIÓN \_ CONSERVADOR:**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_conservative_rasterization_tier) valores de enumeración para cada nivel de compatibilidad del hardware.
-   [**CheckFeatureSupport:**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) método para acceder a las características admitidas.
-   [**CD3DX12 \_ RASTERIZER \_ DESC:**](cd3dx12-rasterizer-desc.md) clase auxiliar para crear descripciones de rasterizador.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tutoriales de vídeo de aprendizaje avanzado de DirectX: Rasterización conservadora](https://www.youtube.com/watch?v=zL0oSY_YmDY)
</dt> <dt>

[Vistas ordenadas por el rasterizador](rasterizer-order-views.md)
</dt> <dt>

[Representación](rendering.md)
</dt> </dl>

 

 




