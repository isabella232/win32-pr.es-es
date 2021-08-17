---
title: Mapas de instantáneas en cascada
description: Los mapas de sombra en cascada (HSM) son la mejor manera de combatir uno de los errores más frecuentes con alias de perspectiva de sombra.
ms.assetid: d3570d0a-74e0-5b9c-6586-c933f630c4ee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29498dc882133215c910f3bd6caa5966aa0e141aaf4f7a68051834d33f2a3b16
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118649719"
---
# <a name="cascaded-shadow-maps"></a>Mapas de instantáneas en cascada

Los mapas de sombra en cascada (HSM) son la mejor manera de combatir uno de los errores más frecuentes con el sombreado: alias de perspectiva. En este artículo técnico, en el que se da por supuesto que el lector está familiarizado con la asignación de sombras, aborda el tema de los HSM. Concretamente:

-   explica la complejidad de los HSM;
-   proporciona detalles sobre las posibles variaciones de los algoritmos de CSM;
-   describe las dos técnicas de filtrado más comunes: filtrado de porcentaje más cercano (PCF) y filtrado con mapas de sombra de varianza (VSM).
-   identifica y aborda algunos de los problemas comunes asociados con la adición de filtrado a los HSM. Y
-   muestra cómo asignar LOSM a hardware de Direct3D 10 a Direct3D 11.

El código usado en este artículo se puede encontrar en el Kit de desarrollo de software (SDK) de DirectX en los ejemplos CascadedShadowMaps11 y VarianceShadows11. Este artículo será más útil después de implementar las técnicas que se tratan en el artículo técnico, Common [Techniques to Improve Shadow Depth Mapas](/windows/desktop/DxTechArts/common-techniques-to-improve-shadow-depth-maps), .

## <a name="cascaded-shadow-maps-and-perspective-aliasing"></a>Sombreado en cascada Mapas alias de perspectiva

El alias de perspectiva en un mapa de sombras es uno de los problemas más difíciles de superar. En el artículo técnico, Técnicas comunes para mejorar la profundidad de Mapas, se describe el alias de perspectiva y se identifican algunos enfoques para mitigar el problema. En la práctica, los CSM tienden a ser la mejor solución y se suelen emplear en juegos modernos.

El concepto básico de los HSM es fácil de entender. Las distintas áreas del frustum de la cámara requieren mapas de sombra con resoluciones diferentes. Los objetos más cercanos al ojo requieren una resolución mayor que los objetos más lejanos. De hecho, cuando el ojo se mueve muy cerca de la geometría, los píxeles más cercanos al ojo pueden requerir tanta resolución que incluso un mapa de sombras 4096 × 4096 no es suficiente.

La idea básica de los HSM es dividir el frustum en varios frusta. Se representa un mapa de sombras para cada subfrústum; a continuación, el sombreador de píxeles toma muestras del mapa que más se corresponde con la resolución necesaria (Figura 2).

**Figura 1. Cobertura de mapa de sombras**

![cobertura de mapa de sombra](images/shadow-map-coverage.png)

En la figura 1, se muestra la calidad (de izquierda a derecha) de mayor a menor. La serie de cuadrículas que representan mapas de sombra con un frustum de vista (cono invertido en rojo) muestra cómo se ve afectada la cobertura de píxeles con diferentes mapas de sombra de resolución. Las sombras son de la máxima calidad (píxeles blanco) cuando hay una relación de 1:1 asignando píxeles en el espacio claro a los elementos de textura en el mapa de sombras. El alias de perspectiva se produce en forma de mapas de textura grandes y bloques (imagen izquierda) cuando hay demasiados píxeles asignados al mismo texel de sombra. Cuando el mapa de sombras es demasiado grande, se muestrea. En este caso, se omiten los elementos de textura, se introducen artefactos de reluciente y el rendimiento se ve afectado.

**Figura 2. Calidad de la sombra de CSM**

![Calidad de la sombra de csm](images/csm-shadow-quality.png)

En la figura 2 se muestran los recortes de la sección de mayor calidad en cada mapa de sombras de la figura 1. El mapa de sombras con los píxeles más colocados (en el vértice) es el más cercano al ojo. Técnicamente, se trata de mapas del mismo tamaño, con blanco y gris que se usan para ejemplificar el éxito del mapa de sombras en cascada. El blanco es ideal porque muestra una buena cobertura: una relación de 1:1 para píxeles de espacio en los ojos y texturas de mapa de sombra.

Los HSM requieren los pasos siguientes por fotograma.

1.  Particionar el frustum en subfrusta.
2.  Calcule una proyección ortográfica para cada subfrústum.
3.  Represente un mapa de sombras para cada subfrústum.
4.  Represente la escena.

    1.  Enlace los mapas de sombras y la representación.
    2.  El sombreador de vértices hace lo siguiente:

        -   Calcula las coordenadas de textura para cada subfrústum claro (a menos que se calcule la coordenada de textura necesaria en el sombreador de píxeles).
        -   Transforma y enciende el vértice, y así sucesivamente.

    3.  El sombreador de píxeles hace lo siguiente:

        -   Determina el mapa de sombras adecuado.
        -   Transforma las coordenadas de textura si es necesario.
        -   Muestrea la cascada.
        -   Enciende el píxel.

## <a name="partitioning-the-frustum"></a>Creación de particiones del frustum

Crear particiones del frustum es el acto de crear subfrusta. Una técnica para dividir el frustum es calcular intervalos del cero al cien por cien en la dirección Z. A continuación, cada intervalo representa un plano cercano y un plano lejano como un porcentaje del eje Z.

**Figura 3. Ver los frustums particionados arbitrariamente**

![ver los frustums particionados arbitrariamente](images/view-frustums-partitioned-arbitrarily.png)

En la práctica, volver a calcular las divisiones del frustum por fotograma hace que los bordes de la sombra se resplandecienten. La práctica generalmente aceptada es usar un conjunto estático de intervalos en cascada por escenario. En este escenario, el intervalo a lo largo del eje Z se usa para describir un subfrusto que se produce al crear particiones del frustum. La determinación de los intervalos de tamaño correctos para una escena determinada depende de varios factores.

### <a name="orientation-of-the-scene-geometry"></a>Orientación de la geometría de la escena

Con respecto a la geometría de la escena, la orientación de la cámara afecta a la selección del intervalo de cascada. Por ejemplo, una cámara muy cerca del suelo, como una cámara de tierra en un partido de fútbol, tiene un conjunto estático diferente de intervalos en cascada que una cámara en el cielo.

En la figura 4 se muestran algunas cámaras diferentes y sus respectivas particiones. Cuando el intervalo Z de la escena es muy grande, se requieren más planos divididos. Por ejemplo, cuando el ojo está muy cerca del plano del suelo, pero los objetos lejanos siguen siendo visibles, pueden ser necesarias varias cascadas. Dividir el frustum para que más divisiones estén cerca del ojo (donde el alias de perspectiva cambia más rápido) también es útil. Cuando la mayor parte de la geometría se agrupa en una sección pequeña (como una vista de sobrecarga o un simulador de vuelos) del frustum de la vista, se necesita menos cascadas.

**Figura 4. Las distintas configuraciones requieren divisiones de frustum diferentes**

![diferentes configuraciones requieren diferentes divisiones de frustum](images/different-configurations-require-different-frustum-splits.png)

(Izquierda) Cuando la geometría tiene un intervalo dinámico alto en Z, se requieren muchas cascadas. (Centro) Cuando la geometría tiene un rango dinámico bajo en Z, hay poca ventaja de varios frustums. (Derecha) Solo se necesitan tres particiones cuando el intervalo dinámico es medio.

### <a name="orientation-of-the-light-and-the-camera"></a>Orientación de la luz y la cámara

La matriz de proyección de cada cascada se ajusta estrechamente alrededor de su subfrusto correspondiente. En configuraciones donde la cámara de vista y las direcciones de la luz son ortogonales, las cascadas se pueden ajustar estrechamente con poca superposición. La superposición se hace más grande a medida que la luz y la cámara de vista se mueven a la alineación paralela (figura 5). Cuando la luz y la cámara de vista son casi paralelas, se denomina "dueling frusta" y es un escenario muy difícil para la mayoría de los algoritmos de sombra. No es raro restringir la luz y la cámara para que este escenario no se produzca. Sin embargo, los CSM tienen un rendimiento mucho mejor que muchos otros algoritmos en este escenario.

**Figura 5. La superposición en cascada aumenta a medida que la dirección de la luz se vuelve paralela con la dirección de la cámara**

![la superposición en cascada aumenta a medida que la dirección de la luz se vuelve paralela con la dirección de la cámara](images/cascade-overlap-increases-as-light-direction-becomes.jpg)

Muchas implementaciones de CSM usan frusta de tamaño fijo. El sombreador de píxeles puede usar la profundidad Z para indexar en la matriz de cascadas cuando el frustum se divide en intervalos de tamaño fijo.

## <a name="calculating-a-view-frustum-bound"></a>Calcular un límite View-Frustum datos

Una vez seleccionados los intervalos de frustum, la subfrusta se crea con uno de estos dos elementos: ajustar a la escena y ajustarse a la cascada.

### <a name="fit-to-scene"></a>Ajustar a la escena

Todo el frusta se puede crear con el mismo plano cercano. Esto obliga a que las cascadas se superpongan. El ejemplo CascadedShadowMaps11 llama a esta técnica adecuada para la escena.

### <a name="fit-to-cascade"></a>Ajustar a Cascade

Como alternativa, frusta se puede crear con el intervalo de partición real que se usa como planos cercanos y lejanos. Esto provoca un ajuste más estricto, pero degenera para ajustarse a la escena en el caso del dueto frusta. Los ejemplos cascadedShadowMaps11 llaman a esta técnica en cascada.

Estos dos métodos se muestran en la figura 6. Ajustar a la cascada desperdicia menos resolución. El problema con la adaptación a la cascada es que la proyección ortográfica crece y se reduce en función de la orientación del frustum de la vista. La técnica de ajuste a la escena completa la proyección ortográfica según el tamaño máximo de la vista frustum, quitando los artefactos que aparecen cuando se mueve la cámara de vista. [Técnicas comunes para mejorar](/windows/desktop/DxTechArts/common-techniques-to-improve-shadow-depth-maps) la profundidad de las sombras Mapas los artefactos que aparecen cuando la luz se mueve en la sección "Mover la luz en incrementos de tamaño de texel".

**Figura 6. Ajustar a la escena frente a ajustarse a la cascada**

![ajustarse a la escena frente a ajustarse a la cascada](images/fit-to-scene-vs-fit-to-cascade.png)

## <a name="render-the-shadow-map"></a>Representación del mapa de sombras

El ejemplo CascadedShadowMaps11 representa los mapas de sombra en un búfer grande. Esto se debe a que PCF en matrices de textura es una característica de Direct3D 10.1. Para cada cascada, se crea una ventanilla que cubre la sección del búfer de profundidad correspondiente a esa cascada. Se enlaza un sombreador de píxeles null porque solo se necesita la profundidad. Por último, la ventanilla y la matriz de sombras correctas se establecen para cada cascada, ya que los mapas de profundidad se representan de una en una en el búfer de sombras principal.

## <a name="render-the-scene"></a>Representación de la escena

El búfer que contiene las sombras ahora está enlazado al sombreador de píxeles. Hay dos métodos para seleccionar la cascada implementada en el ejemplo CascadedShadowMaps11. Estos dos métodos se explican con código de sombreador.

### <a name="interval-based-cascade-selection"></a>Interval-Based selección en cascada

**Figura 7. Selección en cascada basada en intervalos**

![selección en cascada basada en intervalos](images/interval-based-cascade-selection.jpg)

En la selección basada en intervalos (figura 7), el sombreador de vértices calcula la posición en el espacio mundial del vértice.


```C++
Output.vDepth = mul( Input.vPosition, m_mWorldView ).z;
```



El sombreador de píxeles recibe la profundidad interpolada.


```C++
fCurrentPixelDepth = Input.vDepth;
```



La selección en cascada basada en intervalos usa una comparación de vectores y un producto de puntos para determinar la cacade correcta. CASCADE \_ COUNT \_ FLAG especifica el número de cascadas. Los datos \_ m fCascadeFrustumsEyeSpaceDepths \_ restringen las particiones de frustum de vista. Después de la comparación, fComparison contiene un valor de 1 donde el píxel actual es mayor que la barrera y un valor de 0 cuando la cascada actual es menor. Un producto de punto suma estos valores en un índice de matriz.


```C++
        float4 vCurrentPixelDepth = Input.vDepth;
        float4 fComparison = ( vCurrentPixelDepth > m_fCascadeFrustumsEyeSpaceDepths_data[0]);
        float fIndex = dot(
        float4( CASCADE_COUNT_FLAG > 0,
        CASCADE_COUNT_FLAG > 1,
        CASCADE_COUNT_FLAG > 2,
        CASCADE_COUNT_FLAG > 3)
        , fComparison );

        fIndex = min( fIndex, CASCADE_COUNT_FLAG );
        iCurrentCascadeIndex = (int)fIndex;
```



Una vez seleccionada la cascada, la coordenada de textura se debe transformar a la cascada correcta.


```C++
vShadowTexCoord = mul( InterpolatedPosition, m_mShadow[iCascadeIndex] );
```



A continuación, esta coordenada de textura se usa para muestrear la textura con la coordenada X y la coordenada Y. La coordenada Z se usa para realizar la comparación de profundidad final.

### <a name="map-based-cascade-selection"></a>Map-Based selección en cascada

La selección basada en mapa (figura 8) prueba en los cuatro lados de las cascadas para encontrar el mapa más ajustado que cubre el píxel específico. En lugar de calcular la posición en el espacio del mundo, el sombreador de vértices calcula la posición del espacio de vista para cada cascada. El sombreador de píxeles recorre en iteración las cascadas para escalar y desplazar las coordenadas de textura para indexar la cascada actual. A continuación, la coordenada de textura se prueba con los límites de textura. Cuando los valores X e Y de la coordenada de textura se encuentran dentro de una cascada, se usan para muestrear la textura. La coordenada Z se usa para realizar la comparación de profundidad final.

**Figura 8. Selección en cascada basada en mapa**

![selección en cascada basada en mapa](images/map-based-cascade-selection.jpg)

### <a name="interval-based-selection-vs-map-based-selection"></a>Interval-Based selección frente a Map-Based selección

La selección basada en intervalos es ligeramente más rápida que la selección basada en mapa porque la selección en cascada se puede realizar directamente. La selección basada en mapa debe formar una intersección con la coordenada de textura con los límites en cascada.

La selección basada en mapas usa la cascada de forma más eficaz cuando los mapas de sombras no se alinean perfectamente (consulte la figura 8).

## <a name="blend-between-cascades"></a>Combinación entre cascadas

Los VSM (que se analizan más adelante en este artículo) y las técnicas de filtrado, como PCF, se pueden usar con CSM de baja resolución para generar sombras flexibles. Desafortunadamente, esto da como resultado una siam visible (Figura 9) entre capas en cascada porque la resolución no coincide. La solución es crear una banda entre mapas de sombras donde se realiza la prueba de sombras para ambas cascadas. A continuación, el sombreador interpola linealmente entre los dos valores en función de la ubicación del píxel en la banda de mezcla. Los ejemplos CascadedShadowMaps11 y VarianceShadows11 proporcionan un control deslizante de gui que se puede usar para aumentar y disminuir esta banda de desenfoque. El sombreador realiza una rama dinámica para que la gran mayoría de píxeles solo se lean desde la cascada actual.

**Figura 9. Mares en cascada**

![mares en cascada](images/cascade-seams.jpg)

(Izquierda) Se puede ver una siam visible donde las cascadas se superponen. (Derecha) Cuando las cascadas se mezclan entre sí, no se produce ninguna fusión.

## <a name="filtering-shadow-maps"></a>Filtrado de instantáneas Mapas

### <a name="pcf"></a>Pcf

El filtrado de mapas de sombras normales no genera sombras débiles y desenfoque. El hardware de filtrado desenfoca los valores de profundidad y, a continuación, compara esos valores desenfocados con el texel del espacio claro. El borde duro resultante de la prueba de superación o error sigue existiendo. Los mapas de sombras desenfocados solo sirven para mover erróneamente el borde duro. PCF habilita el filtrado en mapas de sombras. La idea general de PCF es calcular un porcentaje del píxel en la sombra en función del número de submuestras que pasan la prueba de profundidad sobre el número total de submuestras.

El hardware de Direct3D 10 y Direct3D 11 puede realizar PCF. La entrada a un muestreador pcf consta de la coordenada de textura y un valor de profundidad de comparación. Para simplificar, PCF se explica con un filtro de cuatro pulsaciones. El muestreador de textura lee la textura cuatro veces, de forma similar a un filtro estándar. Sin embargo, el resultado devuelto es un porcentaje de los píxeles que pasaron la prueba de profundidad. En la figura 10 se muestra cómo un píxel que supera una de las cuatro pruebas de profundidad tiene un 25 por ciento de sombra. El valor real devuelto es una interpolación lineal basada en las coordenadas de subterfucioxel de las lecturas de textura para generar un degradado suave. Sin esta interpolación lineal, el PCF de cuatro pulsaciones solo podría devolver cinco valores: { 0.0, 0.25, 0.5, 0.75, 1.0 }.

**Figura 10. Imagen filtrada por PCF, con el 25 por ciento del píxel seleccionado cubierto**

![imagen filtrada por pcf, con el 25 por ciento del píxel seleccionado cubierto](images/pcf-filtered-image.png)

También es posible realizar PCF sin compatibilidad con hardware o extender PCF a kernels más grandes. Algunas técnicas incluso se muestrea con un kernel ponderado. Para ello, cree un kernel (como un gaussiano) para una cuadrícula N × N. Las ponderaciones deben sumar hasta 1. A continuación, la textura se muestrea N2 veces. Cada muestra se escala según los pesos correspondientes en el kernel. El ejemplo CascadedShadowMaps11 usa este enfoque.

### <a name="depth-bias"></a>Sesgo de profundidad

El sesgo de profundidad es aún más importante cuando se usan kernels de PCF grandes. Solo es válido comparar la profundidad de espacio claro de un píxel con el píxel al que se asigna en el mapa de profundidad. Los vecinos del texel del mapa de profundidad hacen referencia a una posición diferente. Es probable que esta profundidad sea similar, pero puede ser muy diferente en función de la escena. En la figura 11 se resaltan los artefactos que se producen. Una sola profundidad se compara con tres elementos de textura vecinos en el mapa de sombras. Se produce un error en una de las pruebas de profundidad porque su profundidad no se correlaciona con la profundidad de espacio claro calculada de la geometría actual. La solución recomendada para este problema es usar un desplazamiento mayor. Sin embargo, un desplazamiento demasiado grande puede dar lugar a Peter Panning. Calcular un plano cercano estrecho y un plano lejano ayuda a reducir los efectos del uso de un desplazamiento.

**Figura 11. Auto-shadowing erróneo**

![auto-shadowing erróneo](images/erroneous-self-shadowing.png)

El auto shadowing erróneo se debe a la comparación de píxeles de la profundidad del espacio claro con los elementos de textura del mapa de sombras que no se correlacionan. La profundidad del espacio claro se correlaciona con el texel de sombra 2 en el mapa de profundidad. El texel 1 es mayor que la profundidad del espacio claro, mientras que 2 es igual y 3 es menor. Los elementos Texel 2 y 3 pasan la prueba de profundidad, mientras que Texel 1 produce un error.

### <a name="calculating-a-per-texel-depth-bias-with-ddx-and-ddy-for-large-pcfs"></a>Calcular un sesgo Per-Texel profundidad con DDX y DDY para PCF grandes

Calcular un sesgo de profundidad por texel con ddx y **ddy** para PCF grandes es una técnica que calcula el sesgo de profundidad correcto (suponiendo que la superficie sea plana) para el **texel** del mapa de sombra adyacente.

Esta técnica ajusta la profundidad de comparación a un plano mediante la información derivada. Dado que esta técnica es computacionalmente compleja, solo se debe usar cuando una GPU tiene ciclos de proceso que ahorrar. Cuando se usan kernels muy grandes, esta puede ser la única técnica que funciona para quitar artefactos de sombras propias sin provocar que Peter Panning.

En la figura 12 se resalta el problema. La profundidad en el espacio claro se conoce por el elemento de textura que se está comparando. Se desconocen las profundidades de espacio claro que corresponden a los elementos de textura vecinos del mapa de profundidad.

**Figura 12. Mapa de profundidad y escena**

![mapa de profundidad y escena](images/scene-and-depth-map.png)

La escena representada se muestra a la izquierda y el mapa de profundidad con un bloque de texel de ejemplo se muestra a la derecha. El texel de espacio en los ojos se asigna al píxel etiquetado como D en el centro del bloque. Esta comparación es precisa. Profundidad correcta en el espacio de los ojos que se correlaciona con los píxeles desconocidos del vecino D. La asignación de los elementos de textura vecinos al espacio de los ojos solo es posible si se supone que el píxel pertenece al mismo triángulo que D.

La profundidad se conoce por el texel que se correlaciona con la posición del espacio claro. La profundidad es desconocida para los elementos de textura vecinos del mapa de profundidad.

En un nivel alto, esta técnica usa las operaciones **HLSL ddx** y **ddy** para buscar el derivado de la posición de espacio claro. Esto no es interesante porque las operaciones derivadas devuelven el degradado de la profundidad del espacio claro con respecto al espacio de pantalla. Para convertir esto en un degradado de la profundidad del espacio claro con respecto al espacio claro, se debe calcular una matriz de conversión.

### <a name="explanation-with-shader-code"></a>Explicación con código de sombreador

Los detalles del resto del algoritmo se dan como una explicación del código del sombreador que realiza esta operación. Este código se puede encontrar en el ejemplo CascadedShadowMaps11. En la figura 13 se muestra cómo las coordenadas de textura de espacio claro se asignan al mapa de profundidad y cómo se pueden usar los derivados de X e Y para crear una matriz de transformación.

**Figura 13. Espacio de pantalla a matriz de espacio claro**

![espacio de pantalla a matriz de espacio claro](images/screen-space-to-light-space-matrix.png)

Los derivados de la posición de espacio claro en X e Y se usan para crear esta matriz.

El primer paso consiste en calcular el derivado de la posición del espacio de la vista de la luz.


```C++
          float3 vShadowTexDDX = ddx (vShadowMapTextureCoordViewSpace);
          float3 vShadowTexDDY = ddy (vShadowMapTextureCoordViewSpace);
```



Las GPU de clase Direct3D 11 calculan estos derivados ejecutando 2 × 2 cuadránxeles en paralelo y restando las coordenadas de textura del vecino en X para **ddx** y del vecino en Y para **ddy**. Estos dos derivados son las filas de una matriz de 2 × 2. En su forma actual, esta matriz podría usarse para convertir píxeles vecinos del espacio de pantalla en pendientes de espacio claro. Sin embargo, se necesita el inverso de esta matriz. Se necesita una matriz que transforma los píxeles vecinos del espacio claro en pendientes de espacio de pantalla.


```C++
          float2x2 matScreentoShadow = float2x2( vShadowTexDDX.xy, vShadowTexDDY.xy );
          float fInvDeterminant = 1.0f / fDeterminant;

          float2x2 matShadowToScreen = float2x2 (
          matScreentoShadow._22 * fInvDeterminant,
          matScreentoShadow._12 * -fInvDeterminant,
          matScreentoShadow._21 * -fInvDeterminant,
          matScreentoShadow._11 * fInvDeterminant );
```



**Figura 14. Espacio claro a espacio en pantalla**

![espacio claro a espacio de pantalla](images/light-space-to-screen-space.png)

A continuación, esta matriz se usa para transformar los dos elementos de textura anteriores y a la derecha del elemento texel actual. Estos vecinos se representan como un desplazamiento del elemento de textura actual.


```C++
          float2 vRightShadowTexelLocation = float2( m_fTexelSize, 0.0f );
          float2 vUpShadowTexelLocation = float2( 0.0f, m_fTexelSize );
          float2 vRightTexelDepthRatio = mul( vRightShadowTexelLocation,
          matShadowToScreen );
          float2 vUpTexelDepthRatio = mul( vUpShadowTexelLocation,
          matShadowToScreen );
```



La relación que crea la matriz se multiplica finalmente por los derivados de profundidad para calcular los desplazamientos de profundidad de los píxeles vecinos.


```C++
            float fUpTexelDepthDelta =
            vUpTexelDepthRatio.x * vShadowTexDDX.z
            + vUpTexelDepthRatio.y * vShadowTexDDY.z;
            float fRightTexelDepthDelta =
            vRightTexelDepthRatio.x * vShadowTexDDX.z
            + vRightTexelDepthRatio.y * vShadowTexDDY.z;
```



Estos pesos ahora se pueden usar en un bucle PCF para agregar un desplazamiento a la posición.


```C++
    for( int x = m_iPCFBlurForLoopStart; x < m_iPCFBlurForLoopEnd; ++x ) 
    {
        for( int y = m_iPCFBlurForLoopStart; y < m_iPCFBlurForLoopEnd; ++y )
            {
            if ( USE_DERIVATIVES_FOR_DEPTH_OFFSET_FLAG )
            {
            depthcompare += fRightTexelDepthDelta * ( (float) x ) +
            fUpTexelDepthDelta * ( (float) y );
            }
            // Compare the transformed pixel depth to the depth read
            // from the map.
            fPercentLit += g_txShadow.SampleCmpLevelZero( g_samShadow,
            float2(
            vShadowTexCoord.x + ( ( (float) x ) * m_fNativeTexelSizeInX ) ,
            vShadowTexCoord.y + ( ( (float) y ) * m_fTexelSize )
            ),
            depthcompare
            );
            }
     }
```



## <a name="pcf-and-csms"></a>PCF y CSM

PCF no funciona en matrices de textura en Direct3D 10. Para usar PCF, todas las cascadas se almacenan en un atlas de textura grande.

### <a name="derivative-based-offset"></a>Derivative-Based offset

Agregar los desplazamientos basados en derivados para los HSM presenta algunos desafíos. Esto se debe a un cálculo derivado dentro del control de flujo divergente. El problema se produce debido a una forma fundamental de funcionamiento de las GPU. Las GPU de Direct3D11 funcionan en 2 × 2 cuadránxeles de píxeles. Para realizar un derivado, las GPU suelen restar la copia del píxel actual de una variable de la copia del píxel vecino de esa misma variable. La forma en que esto sucede varía de GPU a GPU. Las coordenadas de textura se determinan mediante la selección en cascada basada en mapas o en intervalos. Algunos píxeles de un cuadránxel eligen una cascada diferente a la del resto de los píxeles. Esto da como resultado unas juntas visibles entre los mapas de sombras porque los desplazamientos basados en derivados ahora son completamente incorrectos. La solución es realizar el derivado en coordenadas de textura de espacio de vista ligera. Estas coordenadas son las mismas para cada cascada.

### <a name="padding-for-pcf-kernels"></a>Relleno para kernels pcf

Índice de kernels de PCF fuera de una partición en cascada si no se agrega el búfer de sombra. La solución es que el borde exterior de la cascada se asemeja a la mitad del tamaño del kernel de PCF. Esto debe implementarse en el sombreador que selecciona la cascada y en la matriz de proyección que debe representar la cascada lo suficientemente grande como para conservar el borde.

## <a name="variance-shadow-maps"></a>Sombra de varianza Mapas

Los VSM (consulte [Mapas de sombras](https://portal.acm.org/citation.cfm?doid=1111411.1111440) de varianza de Hsmy y Lauguideen para obtener más información) habilitan el filtrado directo de mapas de sombras. Al usar VSM, se puede usar toda la potencia del hardware de filtrado de texturas. Se puede usar el filtrado trilineal y anisotropico (figura 15). Además, los VSM se pueden desenfocar directamente a través de la convolución. Los VSM tienen algunos inconvenientes; Se deben almacenar dos canales de datos de profundidad (profundidad y profundidad al cuadrado). Cuando las sombras se superponen, es habitual la iluminación. Sin embargo, funcionan bien con resoluciones más bajas y se pueden combinar con los HSM.

**Figura 15. Filtrado anisotropico**

![filtrado anisotropico](images/anisotropic-filtering.png)

### <a name="algorithm-details"></a>Detalles del algoritmo

Los VSM funcionan representando la profundidad y la profundidad al cuadrado en un mapa de sombras de dos canales. Este mapa de sombras de dos canales se puede desenfocar y filtrar como una textura normal. A continuación, el algoritmo usa la desigualdad de Chónbychev en el sombreador de píxeles para calcular la fracción del área de píxeles que superaría la prueba de profundidad.

El sombreador de píxeles captura los valores de profundidad y profundidad al cuadrado.


```C++
        float  fAvgZ  = mapDepth.x; // Filtered z
        float  fAvgZ2 = mapDepth.y; // Filtered z-squared
```



Se realiza la comparación de profundidad.


```C++
        if ( fDepth <= fAvgZ )
        {
        fPercentLit = 1;
        }
```



Si se produce un error en la comparación de profundidad, se calcula el porcentaje del píxel que se enciende. La varianza se calcula como promedio de cuadrados menos cuadrado de promedio.


```C++
        float variance = ( fAvgZ2 ) − ( fAvgZ * fAvgZ );
        variance = min( 1.0f, max( 0.0f, variance + 0.00001f ) );
```



El valor fPercentLit se calcula con la desigualdad de Chábychev.


```C++
        float mean           = fAvgZ;
        float d              = fDepth - mean;
        float fPercentLit    = variance / ( variance + d*d );
```



## <a name="light-bleeding"></a>Luz desaforal

El mayor inconveniente de los VSM es la ligera (figura 16). La pérdida de luz se produce cuando varios castores de sombra se ocultan entre sí a lo largo de los bordes. Los VSM sombren los bordes de las sombras en función de las diferencias de profundidad. Cuando las sombras se superponen entre sí, existe una disparidad de profundidad en el centro de una región que debe ser sombreada. Se trata de un problema con el uso del algoritmo VSM.

**Figura 16. Iluminación de VSM**

![vsm light ladrar](images/vsm-light-bleeding.png)

Una solución parcial al problema es elevar fPercentLit a una potencia. Esto tiene el efecto de atenuar el desenfoque, lo que puede provocar artefactos en los que la disparidad de profundidad es pequeña. A veces existe un valor mágico que mitiga el problema.


```C++
fPercentLit = pow( p_max, MAGIC_NUMBER );
```



Una alternativa a elevar el porcentaje encendido a una potencia es evitar configuraciones en las que las sombras se superponen. Incluso las configuraciones de sombra muy ajustadas tienen varias restricciones en la luz, la cámara y la geometría. La pérdida de luz también se abate mediante texturas de mayor resolución.

Los mapas de sombras de varianza por capas (LVSM) resuelven el problema a costa de dividir el frustum en capas que son de color azul a la luz. El número de mapas necesarios sería bastante grande cuando también se usan los CSM.

Además, Andrew Lauguideen, coautor del documento sobre VSM y autor de un documento sobre LVSM, ha analizado la combinación de mapas de sombra exponenciales (ESM) con VSM para contrarreste la mezcla de luz en un foro [beyond3D](https://forum.beyond3d.com/showthread.php?t=47427).

## <a name="vsms-with-csms"></a>VSMs con HSM

El ejemplo VarianceShadow11 combina VSMs y CSM. La combinación es bastante sencilla. El ejemplo sigue los mismos pasos que el ejemplo CascadedShadowMaps11. Dado que no se usa PCF, las sombras se desenfoca en una convolución separable de dos paso. No usar PCF también permite que el ejemplo use matrices de textura en lugar de un atlas de textura. PCF en matrices de textura es una característica de Direct3D 10.1.

### <a name="gradients-with-csms"></a>Degradados con HSM

El uso de degradados con LOSM puede producir una coomecha a lo largo del borde entre dos cascadas, como se muestra en la figura 17. La instrucción de ejemplo usa derivados entre píxeles para calcular la información, como el nivel de mapa mip, que necesita el filtro. Esto provoca un problema en particular para la selección de mapa mip o el filtrado anisotropico. Cuando los píxeles de un quad toman ramas diferentes en el sombreador, los derivados calculados por el hardware de GPU no son válidos. Esto da como resultado unaam irregular a lo largo del mapa de sombras.

**Figura 17. Seams on cascade borders due to anisotropic filtering with divergent flow control (Marms on cascade borders due to anisotropic filtering with divergent flow control) (Marms on cascade borders due to anisotropic filtering with divergent flow**

![seams on cascade borders due to anisotropic filtering with divergent flow control (marms on cascade borders due to anisotropic filtering with divergent flow control) (seams on cascade borders due to anisotropic filtering with divergent flow](images/seams-on-cascade-borders-due-to-anisotropic.jpg)

Este problema se resuelve al calcular los derivados de la posición en el espacio de vista ligera. la coordenada del espacio de vista ligera no es específica de la cascada seleccionada. Los derivados calculados se pueden escalar mediante la parte de escala de la matriz de proyección y textura al nivel de mapa mip correcto.


```C++
        float3 vShadowTexCoordDDX = ddx( vShadowMapTextureCoordViewSpace );
        vShadowTexCoordDDX *= m_vCascadeScale[iCascade].xyz;
        float3 vShadowTexCoordDDY = ddy( vShadowMapTextureCoordViewSpace );
        vShadowTexCoordDDY *= m_vCascadeScale[iCascade].xyz;

        mapDepth += g_txShadow.SampleGrad( g_samShadow, vShadowTexCoord.xyz,
        vShadowTexCoordDDX, vShadowTexCoordDDY );
```



## <a name="vsms-compared-to-standard-shadows-with-pcf"></a>VSM comparados con las sombras estándar con PCF

Tanto los VSM como PCF intentan aproximarse a la fracción del área de píxeles que superaría la prueba de profundidad. Los VSM funcionan con hardware de filtrado y se pueden desenfocar con kernels separables. Los kernels de convolución separables son considerablemente más baratos de implementar que un kernel completo. Además, los VSM comparan una profundidad de espacio claro con un valor en el mapa de profundidad de espacio claro. Esto significa que los VSM no tienen los mismos problemas de desplazamiento que PCF. Técnicamente, los VSM son la profundidad de muestreo en un área mayor, así como realizar un análisis estadístico. Esto es menos preciso que PCF. En la práctica, los VSM hacen un trabajo muy bueno de combinación, lo que hace que sea necesario menos desplazamiento. Como se ha descrito anteriormente, el inconveniente número uno de los VSM es la ligera.

Los VSM y PCF representan un equilibrio entre la potencia de proceso de GPU y el ancho de banda de textura de GPU. Los VSM requieren que se realicen más cálculos matemáticos para calcular la varianza. PCF requiere más ancho de banda de memoria de textura. Los kernels de PCF grandes pueden convertirse rápidamente en cuellos de botella por ancho de banda de textura. Con la potencia de cálculo de GPU creciendo más rápidamente que el ancho de banda de GPU, los VSM se están convirtiendo en los más prácticos de los dos algoritmos. Los VSM también se ven mejor con mapas de sombra de resolución inferior debido a la combinación y el filtrado.

## <a name="summary"></a>Resumen

Los HSM ofrecen una solución al problema de alias de perspectiva. Hay varias configuraciones posibles para obtener la fidelidad visual necesaria para un título. PcF y VSM se usan ampliamente y se deben combinar con los HSM para reducir el alias.

## <a name="references"></a>Referencias

Doney, W. and Launellen, A. [Variance shadow maps](https://portal.acm.org/citation.cfm?doid=1111411.1111440). En SI3D '06: Proceedings of the 2006 symposium on Interactive 3D graphics and games (Si3D 06: procedimientos del coloquio de 2006 sobre gráficos y juegos 3D interactivos). 2006. pp. 161–165. Nueva York, NUEVA YORK, EE. UU.: ACM Press.

Lauguideen, Andrew y Mc Cool, Michael. [Mapas de sombra de varianza por capas.](https://portal.acm.org/citation.cfm?id=1375714.1375739&coll=GUIDE&dl=GUIDE&CFID=45360327&CFTOKEN=34578992) Procedimientos de la interfaz gráfica 2008, 28-30 de mayo de 2008, Toronto, Toronto, Canadá.

Engel, Woflmid F. Sección 4. Instantáneas en cascada Mapas. ShaderX5, Advanced Rendering Techniques, Shader F. Engel, Ed. Charles River Media, Boston, Massachusts. 2006. pp. 197–206.

 

 