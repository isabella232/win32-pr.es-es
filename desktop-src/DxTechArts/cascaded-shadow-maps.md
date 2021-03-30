---
title: Mapas de instantáneas en cascada
description: Los mapas de sombras en cascada (CSMs) son la mejor manera de combatir uno de los errores más frecuentes con el alias de perspectiva de sombreado.
ms.assetid: d3570d0a-74e0-5b9c-6586-c933f630c4ee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce6297e46f53bafbbe6abbba1629904f90f78d5e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995439"
---
# <a name="cascaded-shadow-maps"></a>Mapas de instantáneas en cascada

Los mapas de sombras en cascada (CSMs) son la mejor manera de combatir uno de los errores más frecuentes con el sombreado: el alias de perspectiva. En este artículo técnico, en el que se da por supuesto que el lector está familiarizado con la asignación de instantáneas, aborda el tema de CSMs. Concretamente:

-   explica la complejidad de CSMs;
-   proporciona detalles sobre las posibles variaciones de los algoritmos de CSM;
-   describe las dos técnicas de filtrado más comunes: el filtrado de porcentaje más cercano (PCF) y el filtrado con mapas de instantáneas de varianza (VSMs).
-   identifica y aborda algunos de los problemas comunes asociados a la adición de filtrado a CSMs; etc
-   muestra cómo asignar CSMs a Direct3D 10 a través de hardware de Direct3D 11.

El código que se usa en este artículo se puede encontrar en el kit de desarrollo de software (SDK) de DirectX, en los ejemplos de CascadedShadowMaps11 y VarianceShadows11. Este artículo resultará de gran utilidad después de implementar las técnicas que se describen en el artículo técnico, se implementan [técnicas comunes para mejorar las asignaciones de profundidad](/windows/desktop/DxTechArts/common-techniques-to-improve-shadow-depth-maps)de la sombra.

## <a name="cascaded-shadow-maps-and-perspective-aliasing"></a>Mapas de sombras en cascada y alias de perspectiva

El alias de perspectiva de un mapa de sombras es uno de los problemas más difíciles de superar. En el artículo técnico, técnicas comunes para mejorar las asignaciones de profundidad de sombra, se describe el alias de perspectiva y se identifican algunos enfoques para mitigar el problema. En la práctica, CSMs tiende a ser la mejor solución y se suele emplear en juegos modernos.

El concepto básico de CSMs es fácil de entender. Las distintas áreas del frustum de la cámara requieren mapas de sombras con distintas resoluciones. Los objetos más cercanos al ojo requieren una resolución mayor que los objetos más lejanos. De hecho, cuando el ojo se desplaza muy cerca de la geometría, los píxeles más cercanos al ojo pueden requerir tanta resolución que incluso una asignación sombra 4096 × 4096 sea insuficiente.

La idea básica de CSMs es particionar el frustum en varios Frusta. Se representa un mapa de sombras para cada subfrustum; a continuación, el sombreador de píxeles muestrea el mapa que más se aproxime a la resolución necesaria (Figura 2).

**Figura 1. Cobertura de mapas de sombras**

![cobertura de mapas de sombras](images/shadow-map-coverage.png)

En la figura 1, se muestra la calidad (de izquierda a derecha) de mayor a menor. La serie de cuadrículas que representan las asignaciones de sombra con un frustum de vista (cono invertido en rojo) muestra cómo se ve afectada la cobertura de píxeles con mapas de sombras de resolución diferentes. Las sombras tienen la máxima calidad (píxeles blancos) cuando hay una relación de 1:1 píxeles en el espacio claro para textura en el mapa de instantáneas. El alias de perspectiva se produce en forma de grandes mapas de texturas de bloque (imagen izquierda) cuando hay demasiados píxeles asignados a la misma sombra textura. Cuando el mapa de sombras es demasiado grande, se muestra en el ejemplo. En este caso, se omiten los textura, se introducen los artefactos de Shimmering y el rendimiento se ve afectado.

**Figura 2. Calidad de sombra CSM**

![calidad de sombra CSM](images/csm-shadow-quality.png)

En la figura 2 se muestran recortes de la sección de mayor calidad de cada mapa de sombras de la ilustración 1. El mapa de sombra con los píxeles más estrechamente colocados (en el vértice) es más cercano a la vista. Técnicamente, se trata de mapas del mismo tamaño, con blanco y gris usados para ejemplificar el éxito de la asignación de instantáneas en cascada. El blanco es idóneo porque muestra una buena cobertura, una relación 1:1 para los píxeles de espacio ocular y el textura de mapa de sombras.

CSMs requiere los siguientes pasos por fotograma.

1.  Divida el frustum en subfrusta.
2.  Calcule una proyección ortográfica para cada subfrustum.
3.  Representar un mapa de instantáneas para cada subfrustum.
4.  Representar la escena.

    1.  Enlazar los mapas de sombras y representar.
    2.  El sombreador de vértices hace lo siguiente:

        -   Calcula las coordenadas de textura para cada subfrustum claro (a menos que la coordenada de textura necesaria se calcule en el sombreador de píxeles).
        -   Transforma y ilumina el vértice, y así sucesivamente.

    3.  El sombreador de píxeles hace lo siguiente:

        -   Determina la asignación de instantáneas adecuada.
        -   Transforma las coordenadas de textura si es necesario.
        -   Muestrea la cascada.
        -   Enciende el píxel.

## <a name="partitioning-the-frustum"></a>Crear particiones del frustum

La creación de particiones del frustum es el acto de crear subfrusta. Una técnica para dividir el frustum es calcular los intervalos del cero al 100 por ciento en la dirección Z. Cada intervalo representa después un plano cercano y un plano lejano como un porcentaje del eje Z.

**Figura 3. Ver Frustums con particiones arbitrariamente**

![Ver Frustums con particiones arbitrariamente](images/view-frustums-partitioned-arbitrarily.png)

En la práctica, el recálculo de las divisiones del frustum por fotogramas provoca que los bordes de la sombra se Shimmer. La práctica generalmente aceptada es usar un conjunto estático de intervalos en cascada por escenario. En este escenario, el intervalo a lo largo del eje Z se usa para describir un subfrustum que se produce al particionar el frustum. La determinación de los intervalos de tamaño correctos para una determinada escena depende de varios factores.

### <a name="orientation-of-the-scene-geometry"></a>Orientación de la geometría de la escena

Con respecto a la geometría de la escena, la orientación de la cámara afecta a la selección del intervalo en cascada. Por ejemplo, una cámara muy cerca del suelo, como una cámara de fondo en un juego de fútbol, tiene un conjunto estático de intervalos en cascada diferente al de una cámara del cielo.

La figura 4 muestra algunas cámaras diferentes y sus respectivas particiones. Cuando el intervalo Z de la escena es muy grande, se necesitan más planos divididos. Por ejemplo, cuando el ojo está muy cerca del plano básico, pero los objetos lejanos siguen siendo visibles, pueden ser necesarias varias cascadas. Dividir el frustum de modo que haya más divisiones cerca del ojo (donde el alias de perspectiva cambia el más rápido) también es útil. Cuando la mayor parte de la geometría se agrupa en una pequeña sección (como una vista de sobrecarga o un simulador de vuelos) del frustum de vista, se necesitan menos cascadas.

**Figura 4. Distintas configuraciones requieren diferentes divisiones de frustum**

![distintas configuraciones requieren diferentes divisiones de frustum](images/different-configurations-require different-frustum-splits.png)

Salido Cuando Geometry tiene un intervalo dinámico alto en Z, se necesitan muchos en cascada. Centro Cuando la geometría tiene un intervalo dinámico bajo en Z, hay pocas ventajas de varios Frustums. Correcta Solo se necesitan tres particiones cuando el intervalo dinámico es medio.

### <a name="orientation-of-the-light-and-the-camera"></a>Orientación de la luz y la cámara

Cada matriz de proyección en cascada se ajusta en torno a su subfrustum correspondiente. En las configuraciones en las que la cámara de la vista y las direcciones de la luz son ortogonales, los valores en cascada pueden ajustarse con poca superposición. La superposición es mayor a medida que la luz y la cámara de la vista pasan a la alineación paralela (Figura 5). Cuando la luz y la cámara de la vista son casi paralelas, se denomina "dueling Frusta" y es un escenario muy difícil de la mayoría de los algoritmos de sombreado. No es raro restringir la luz y la cámara para que no se produzca este escenario. Sin embargo, CSMs funcionan mucho mejor que muchos otros algoritmos en este escenario.

**Figura 5. La superposición en cascada aumenta a medida que la dirección clara se vuelve paralela a la dirección de la cámara**

![la superposición en cascada aumenta a medida que la dirección clara se vuelve paralela a la dirección de la cámara](images/cascade-overlap-increases-as-light-direction-becomes.jpg)

Muchas implementaciones de CSM usan Frusta de tamaño fijo. El sombreador de píxeles puede usar la profundidad Z para indexar en la matriz de valores en cascada cuando el frustum se divide en intervalos de tamaño fijo.

## <a name="calculating-a-view-frustum-bound"></a>Calcular un View-Frustum enlazado

Una vez seleccionados los intervalos de frustum, los subfrusta se crean con uno de los dos: ajustar a la escena y ajustar a la cascada.

### <a name="fit-to-scene"></a>Ajustar a la escena

Todas las Frusta se pueden crear con el mismo plano próximo. Esto obliga a que las cascadas se superpongan. El ejemplo CascadedShadowMaps11 llama a esta técnica ajustada a la escena.

### <a name="fit-to-cascade"></a>Ajustar a cascada

Como alternativa, se puede crear Frusta con el intervalo de partición real que se usa como plano Near y Far. Esto hace que el ajuste sea más estrecho, pero se desgenera para ajustarse a la escena en el caso de Dueling Frusta. Los ejemplos de CascadedShadowMaps11 llama a esta técnica en cascada.

Estos dos métodos se muestran en la figura 6. Ajustarse a los residuos en cascada menos resolución. El problema de encajar en cascada es que la proyección ortográfica aumenta y disminuye en función de la orientación del frustum de vista. La técnica ajustar a la escena rellena la proyección ortográfica por el tamaño máximo del frustum de la vista quitando los artefactos que aparecen cuando se mueve la cámara de vista. Las [técnicas comunes para mejorar las asignaciones de profundidad de sombra](/windows/desktop/DxTechArts/common-techniques-to-improve-shadow-depth-maps) se redirigen a los artefactos que aparecen cuando la luz se mueve en la sección "mover la luz en incrementos de tamaño de textura".

**Figura 6. Ajustar a la escena y ajustarse a la cascada**

![ajustar a la escena en lugar de ajustarse a la cascada](images/fit-to-scene-vs-fit-to-cascade.png)

## <a name="render-the-shadow-map"></a>Representar la instantánea

El ejemplo CascadedShadowMaps11 representa las asignaciones de instantáneas en un búfer de gran tamaño. Esto se debe a que PCF en las matrices de textura es una característica de Direct3D 10,1. Para cada cascada, se crea una ventanilla que cubre la sección del búfer de profundidad correspondiente a esa cascada. Un sombreador de píxeles nulo se enlaza porque solo se necesita la profundidad. Por último, se establecen la ventanilla y la matriz de instantáneas correctas para cada cascada, ya que las asignaciones de profundidad se representan de una en una en el búfer de la sombra principal.

## <a name="render-the-scene"></a>Representación de la escena

El búfer que contiene las sombras se enlaza ahora al sombreador de píxeles. Hay dos métodos para seleccionar la implementación en cascada en el ejemplo CascadedShadowMaps11. Estos dos métodos se explican con el código del sombreador.

### <a name="interval-based-cascade-selection"></a>Selección en cascada Interval-Based

**Figura 7. Selección en cascada basada en intervalos**

![selección en cascada basada en intervalos](images/interval-based-cascade-selection.jpg)

En la selección basada en intervalos (Figura 7), el sombreador de vértices calcula la posición en el espacio universal del vértice.


```C++
Output.vDepth = mul( Input.vPosition, m_mWorldView ).z;
```



El sombreador de píxeles recibe la profundidad interpolada.


```C++
fCurrentPixelDepth = Input.vDepth;
```



La selección en cascada basada en intervalos usa una comparación de vectores y un producto de punto para determinar el cacade correcto. La \_ marca de recuento en cascada \_ especifica el número de cascadas. Los datos de m \_ fCascadeFrustumsEyeSpaceDepths \_ restringen las particiones de frustum de vista. Después de la comparación, fComparison contiene un valor de 1, donde el píxel actual es mayor que la barrera y un valor de 0 cuando la cascada actual es menor. Un producto de punto suma estos valores en un índice de matriz.


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



Una vez seleccionada la opción Cascade, la coordenada de textura debe transformarse en cascada correcta.


```C++
vShadowTexCoord = mul( InterpolatedPosition, m_mShadow[iCascadeIndex] );
```



Esta coordenada de textura se usa para muestrear la textura con la coordenada X y la coordenada Y. La coordenada Z se usa para realizar la comparación de profundidad final.

### <a name="map-based-cascade-selection"></a>Selección en cascada Map-Based

La selección basada en mapas (Figura 8) realiza pruebas en los cuatro lados de las cascadas para buscar el mapa más estrecho que cubre el píxel específico. En lugar de calcular la posición en el espacio universal, el sombreador de vértices calcula la posición del espacio de la vista para cada cascada. El sombreador de píxeles itera en las cascadas para escalar y desplazar las coordenadas de textura de modo que indexen la cascada actual. A continuación, se prueba la coordenada de textura con los límites de textura. Cuando los valores X e y de la coordenada de textura se encuentran dentro de una cascada, se usan para muestrear la textura. La coordenada Z se usa para realizar la comparación de profundidad final.

**Ilustración 8. Selección en cascada basada en mapas**

![selección en cascada basada en mapas](images/map-based-cascade-selection.jpg)

### <a name="interval-based-selection-vs-map-based-selection"></a>Interval-Based selección frente a Map-Based selección

La selección basada en intervalos es ligeramente más rápida que la selección basada en asignación, ya que la selección en cascada se puede realizar directamente. La selección basada en mapas debe intersectar la coordenada de textura con los límites en cascada.

La selección basada en mapas usa la cascada de forma más eficaz cuando las asignaciones de sombras no se alinean perfectamente (vea la figura 8).

## <a name="blend-between-cascades"></a>Blend entre cascadas

VSMs (que se describe más adelante en este artículo) y técnicas de filtrado como PCF se pueden usar con CSMs de baja resolución para producir sombras flexibles. Desafortunadamente, esto da como resultado una costura visible (Figura 9) entre las capas en cascada porque no coincide con la resolución. La solución consiste en crear una banda entre los mapas de instantáneas donde se realiza la prueba de sombra para ambos en cascada. A continuación, el sombreador se interpola linealmente entre los dos valores en función de la ubicación del píxel en la banda de mezcla. Los ejemplos CascadedShadowMaps11 y VarianceShadows11 proporcionan un control deslizante de la interfaz gráfica de usuario que se puede usar para aumentar y disminuir esta banda de desenfoque. El sombreador realiza una bifurcación dinámica para que la mayoría de los píxeles solo se lean de la cascada actual.

**Ilustración 9. Costuras en cascada**

![costuras en cascada](images/cascade-seams.jpg)

Salido Se pueden ver las costuras visibles donde se superponen las cascadas. Correcta Cuando se mezclan las cascadas entre, no se produce ninguna costura.

## <a name="filtering-shadow-maps"></a>Filtrar mapas de instantáneas

### <a name="pcf"></a>PCF

El filtrado de mapas de sombras normales no produce sombras desenfocadas y suavizadas. El hardware de filtrado desenfoca los valores de profundidad y, a continuación, compara los valores desenfocados con el espacio de textura. El margen duro resultante de la prueba de superación o error sigue existiendo. Desenfocar mapas de sombra solo sirve para trasladar erróneamente el borde duro. PCF permite filtrar en mapas de instantáneas. La idea general de PCF es calcular un porcentaje del píxel en la sombra en función del número de submuestras que superan la prueba de profundidad sobre el número total de submuestras.

El hardware de Direct3D 10 y Direct3D 11 puede realizar PCF. La entrada a un muestreador PCF consta de la coordenada de textura y un valor de profundidad de comparación. Para simplificar, PCF se explica con un filtro de cuatro punteos. La muestra de textura lee la textura cuatro veces, de forma similar a un filtro estándar. Sin embargo, el resultado devuelto es un porcentaje de los píxeles que superaron la prueba de profundidad. En la figura 10 se muestra cómo un píxel que pasa una de las cuatro pruebas de profundidad es el 25 por ciento de la sombra. El valor real devuelto es una interpolación lineal basada en las coordenadas subtexel de las lecturas de textura para producir un degradado suave. Sin esta interpolación lineal, el PCF de cuatro punteos solo podría devolver cinco valores: {0,0, 0,25, 0,5, 0,75, 1,0}.

**Figura 10. Imagen filtrada PCF, con el 25 por ciento del píxel seleccionado incluido**

![imagen filtrada PCF, con el 25 por ciento del píxel seleccionado incluido](images/pcf-filtered-image.png)

También es posible hacer PCF sin compatibilidad de hardware o extender PCF a kernels más grandes. Algunas técnicas incluso muestra con un kernel ponderado. Para ello, cree un kernel (por ejemplo, un gaussiano) para una cuadrícula N × N. Los pesos deben agregar hasta 1. A continuación, la textura se muestrea en horas N2. Cada ejemplo se escala según los pesos correspondientes en el kernel. En el ejemplo CascadedShadowMaps11 se usa este enfoque.

### <a name="depth-bias"></a>Tendencia de profundidad

La diferencia de profundidad es incluso más importante cuando se usan kernels PCF grandes. Solo es válido para comparar la profundidad de espacio claro de un píxel con el píxel al que se asigna en el mapa de profundidad. Los vecinos del textura de mapa de profundidad hacen referencia a una posición diferente. Es probable que esta profundidad sea similar, pero puede ser muy diferente en función de la escena. En la figura 11 se resaltan los artefactos que se producen. Una sola profundidad se compara con tres texturas vecinos en el mapa de instantáneas. Una de las pruebas de profundidad produce un error errónea porque su profundidad no se correlaciona con la profundidad calculada de espacio claro de la geometría actual. La solución recomendada para este problema es usar un desplazamiento mayor. Pero es demasiado grande de un desplazamiento. sin embargo, se puede producir la panorámica de Peter. Calcular un plano cerca y un plano lejano ayuda a reducir los efectos del uso de un desplazamiento.

**Figura 11. Sombra automática errónea**

![sombra automática errónea](images/erroneous-self-shadowing.png)

Los resultados de la ocultación automática erróneos de la comparación de los píxeles de la profundidad del espacio claro con el textura en el mapa de instantáneas que no se correlacionan. La profundidad en el espacio claro se correlaciona con Shadow textura 2 en el mapa de profundidad. Textura 1 es mayor que la profundidad de espacio claro, mientras que 2 es igual y 3 es menor. Textura 2 y 3 superan la prueba de profundidad, mientras que textura 1 produce un error.

### <a name="calculating-a-per-texel-depth-bias-with-ddx-and-ddy-for-large-pcfs"></a>Calcular una diferencia de profundidad de Per-Texel con DDX y DDY para PCFs grandes

Calcular una desviación de profundidad por textura con **DDX** y **DDY** para PCFs grande es una técnica que calcula la diferencia de profundidad correcta, suponiendo que la superficie es plana, para el textura de mapa de sombra adyacente.

Esta técnica ajusta la profundidad de comparación a un plano mediante la información derivada. Dado que esta técnica es complejamente compleja, solo debe usarse cuando una GPU tiene ciclos de proceso para la reserva. Cuando se usan kernels muy grandes, esta puede ser la única técnica que se usa para quitar los artefactos de sombra automática sin causar la panorámica de Peter.

En la ilustración 12 se destaca el problema. La profundidad en el espacio claro se conoce para el textura que se está comparando. Se desconocen las profundidades de espacio claro que se corresponden con el textura vecino en el mapa de profundidad.

**Figura 12. Mapa de profundidad y escena**

![mapa de profundidad y escena](images/scene-and-depth-map.png)

La escena representada se muestra a la izquierda y el mapa de profundidad con un bloque textura de ejemplo se muestra a la derecha. El textura de espacio de ojo se asigna al píxel con la etiqueta D en el centro del bloque. Esta comparación es precisa. La profundidad correcta en el espacio ocular en correlación con los píxeles en que se desconoce el vecino D. Solo es posible asignar el textura adyacente al espacio ocular si se supone que el píxel pertenece al mismo triángulo que D.

La profundidad se conoce para el textura que se correlaciona con la posición de espacio claro. La profundidad es desconocida para los texturas vecinos en el mapa de profundidad.

En un nivel alto, esta técnica usa las operaciones HLSL **DDX** y **DDY** para buscar el derivado de la posición de espacio claro. Esto no es trivial porque las operaciones derivadas devuelven el degradado de la profundidad del espacio claro con respecto al espacio de la pantalla. Para convertir esto en un degradado de la profundidad del espacio claro con respecto al espacio de luz, se debe calcular una matriz de conversión.

### <a name="explanation-with-shader-code"></a>Explicación con el código del sombreador

Los detalles del resto del algoritmo se proporcionan como una explicación del código del sombreador que realiza esta operación. Este código se puede encontrar en el ejemplo CascadedShadowMaps11. En la figura 13 se muestra cómo se asignan las coordenadas de textura de espacio claro a la asignación de profundidad y cómo se pueden usar los derivados en X e y para crear una matriz de transformación.

**Figura 13. Espacio de pantalla para la matriz de espacio claro**

![espacio de pantalla para la matriz de espacio claro](images/screen-space-to-light-space-matrix.png)

Los derivados de la posición de espacio claro en X e y se usan para crear esta matriz.

El primer paso es calcular el derivado de la posición del espacio de la vista clara.


```C++
          float3 vShadowTexDDX = ddx (vShadowMapTextureCoordViewSpace);
          float3 vShadowTexDDY = ddy (vShadowMapTextureCoordViewSpace);
```



Las GPU de clase de Direct3D 11 calculan estos derivados ejecutando 2 × 2 cuádruple de píxeles en paralelo y restando las coordenadas de textura del vecino en X para **DDX** y del vecino en y para **DDY**. Estos dos derivados forman las filas de una matriz de 2 × 2. En su forma actual, esta matriz se puede usar para convertir los píxeles adyacentes del espacio de pantalla en las pendientes de espacio ligero. Sin embargo, se necesita el inverso de esta matriz. Matriz que transforma los píxeles adyacentes de espacio claro en las pendientes de espacio de pantalla.


```C++
          float2x2 matScreentoShadow = float2x2( vShadowTexDDX.xy, vShadowTexDDY.xy );
          float fInvDeterminant = 1.0f / fDeterminant;

          float2x2 matShadowToScreen = float2x2 (
          matScreentoShadow._22 * fInvDeterminant,
          matScreentoShadow._12 * -fInvDeterminant,
          matScreentoShadow._21 * -fInvDeterminant,
          matScreentoShadow._11 * fInvDeterminant );
```



**Figura 14. Espacio claro en el espacio de pantalla**

![espacio claro en el espacio de pantalla](images/light-space-to-screen-space.png)

A continuación, esta matriz se usa para transformar los dos textura por encima y a la derecha de la textura actual. Estos vecinos se representan como un desplazamiento desde el textura actual.


```C++
          float2 vRightShadowTexelLocation = float2( m_fTexelSize, 0.0f );
          float2 vUpShadowTexelLocation = float2( 0.0f, m_fTexelSize );
          float2 vRightTexelDepthRatio = mul( vRightShadowTexelLocation,
          matShadowToScreen );
          float2 vUpTexelDepthRatio = mul( vUpShadowTexelLocation,
          matShadowToScreen );
```



Por último, la relación que crea la matriz se multiplica por los derivados de profundidad para calcular los desplazamientos de profundidad para los píxeles circundantes.


```C++
            float fUpTexelDepthDelta =
            vUpTexelDepthRatio.x * vShadowTexDDX.z
            + vUpTexelDepthRatio.y * vShadowTexDDY.z;
            float fRightTexelDepthDelta =
            vRightTexelDepthRatio.x * vShadowTexDDX.z
            + vRightTexelDepthRatio.y * vShadowTexDDY.z;
```



Estos pesos se pueden usar ahora en un bucle PCF para agregar un desplazamiento a la posición.


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



## <a name="pcf-and-csms"></a>PCF y CSMs

PCF no funciona en las matrices de texturas en Direct3D 10. Para usar PCF, todas las cascadas se almacenan en un Atlas de textura grande.

### <a name="derivative-based-offset"></a>Derivative-Based desplazamiento

La adición de los desplazamientos basados en derivado para CSMs presenta algunos desafíos. Esto se debe a un cálculo derivado dentro del control de flujo divergente. El problema se produce debido a una forma fundamental de usar las GPU. Las GPU de Direct3D 11 funcionan en 2 × 2 cuádruples de píxeles. Para realizar una derivada, las GPU generalmente restan la copia del píxel actual de una variable de la copia del píxel adyacente de esa misma variable. La forma en que esto ocurre varía de una GPU a una GPU. Las coordenadas de textura se determinan mediante la selección en cascada basada en el mapa o en el intervalo. Algunos píxeles de un píxel cuádruple eligen una en cascada diferente que el resto de los píxeles. Esto da como resultado las costuras visibles entre los mapas de instantáneas, ya que los desplazamientos basados en el derivado ahora están completamente incorrectos. La solución consiste en realizar el derivado de las coordenadas de textura del espacio de vista clara. Estas coordenadas son las mismas para cada cascada.

### <a name="padding-for-pcf-kernels"></a>Relleno de kernels PCF

El índice de kernels PCF está fuera de una partición en cascada si no se rellena el búfer de la sombra. La solución consiste en rellenar el borde exterior de la cascada en la mitad del tamaño del kernel PCF. Esto se debe implementar en el sombreador que selecciona la cascada y en la matriz de proyección que deben representar la cascada lo suficientemente grande como para conservar el borde.

## <a name="variance-shadow-maps"></a>Mapas de instantáneas de varianza

VSMs (consulte las [asignaciones sombra](https://portal.acm.org/citation.cfm?doid=1111411.1111440) de la varianza de Donnelly y Lauritzen para obtener más información) habilitación del filtrado de mapas de instantáneas directos. Al usar VSMs, se puede usar toda la eficacia del hardware de filtrado de texturas. Se puede usar el filtrado trilineal y anisotrópico (Figura 15). Además, VSMs se puede desenfocar directamente a través de circunvolución. VSMs tienen algunas desventajas; deben almacenarse dos canales de datos de profundidad (profundidad y profundidad). Cuando las sombras se superponen, es común la claridad. Sin embargo, funcionan bien con resoluciones más bajas y se pueden combinar con CSMs.

**Figura 15. Filtrado anisotrópico**

![filtrado anisotrópico](images/anisotropic-filtering.png)

### <a name="algorithm-details"></a>Detalles del algoritmo

VSMs el trabajo mediante la representación de la profundidad y la profundidad al cuadrado de una asignación de sombra de dos canales. Esta asignación de instantáneas de dos canales se puede Desenfocar y filtrar como una textura normal. A continuación, el algoritmo utiliza la desigualdad de Chebychev en el sombreador de píxeles para calcular la fracción del área de píxeles que pasaría la prueba de profundidad.

El sombreador de píxeles captura los valores de profundidad y de profundidad.


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



Si se produce un error en la comparación de profundidad, se calcula el porcentaje del píxel que está iluminado. La varianza se calcula como promedio de cuadrados menos el cuadrado del promedio.


```C++
        float variance = ( fAvgZ2 ) − ( fAvgZ * fAvgZ );
        variance = min( 1.0f, max( 0.0f, variance + 0.00001f ) );
```



El valor fPercentLit se calcula con la desigualdad de Chebychev.


```C++
        float mean           = fAvgZ;
        float d              = fDepth - mean;
        float fPercentLit    = variance / ( variance + d*d );
```



## <a name="light-bleeding"></a>Sangrado claro

El mayor inconveniente de VSMs es la dessangrado ligera (Figura 16). La purga de luz se produce cuando varios convertidores de sombras se tapaban entre sí a lo largo de los bordes. VSMs sombrear los bordes de las sombras en función de las disparidades de profundidad. Cuando las sombras se superponen entre sí, existe una disparidad de profundidad en el centro de una región que se debe sombrear. Se trata de un problema con el uso del algoritmo de VSM.

**Figura 16. Sangrado claro de VSM**

![sangrado claro de VSM](images/vsm-light-bleeding.png)

Una solución parcial al problema es elevar el fPercentLit a una potencia. Esto tiene el efecto de atenuar el desenfoque, lo que puede producir artefactos donde la disparidad de profundidad es pequeña. A veces existe un valor mágico que soluciona el problema.


```C++
fPercentLit = pow( p_max, MAGIC_NUMBER );
```



Una alternativa a aumentar el porcentaje de iluminación a una potencia es evitar las configuraciones en las que las sombras se superponen. Incluso las configuraciones de sombra muy ajustadas tienen varias restricciones en la luz, la cámara y la geometría. La sangrado de luz también se reduce mediante el uso de texturas de mayor resolución.

Los mapas de sombras de la varianza por capas (LVSMs) resuelven el problema a costa de romper el frustum en capas que son perpendiculares a la luz. El número de asignaciones necesario sería bastante grande cuando también se usan CSMs.

Además, Andrew Lauritzen, coautor of the Paper on VSMs, and Author of a Paper in LVSMs, se ha explicado la combinación de mapas de sombra exponencial (ESMs) con VSMs para contrarrestar la combinación de luz en un [Foro de Beyond3D](https://forum.beyond3d.com/showthread.php?t=47427).

## <a name="vsms-with-csms"></a>VSMs con CSMs

El VarianceShadow11 de ejemplo combina VSMs y CSMs. La combinación es bastante sencilla. El ejemplo sigue los mismos pasos que el ejemplo CascadedShadowMaps11. Dado que no se usa PCF, las sombras se desdibujan en una circunvolución separable de dos pasos. El uso de PCF también permite que el ejemplo use matrices de textura en lugar de un Atlas de textura. PCF en las matrices de textura es una característica de Direct3D 10,1.

### <a name="gradients-with-csms"></a>Degradados con CSMs

El uso de degradados con CSMs puede producir un límite a lo largo del borde entre dos cascadas, como se aprecia en la figura 17. La instrucción de ejemplo utiliza derivados entre píxeles para calcular información, como el nivel de mipmap, que necesita el filtro. Esto provoca un problema en particular para la selección de mipmap o el filtrado anisotrópico. Cuando los píxeles de una cuádruple toman ramas diferentes del sombreador, los derivados calculados por el hardware de la GPU no son válidos. Esto da como resultado un límite escalonado a lo largo de la instantánea.

**Figura 17. Costuras en los bordes en cascada debido al filtrado anisotrópico con control de flujo divergente**

![costuras en los bordes en cascada debido al filtrado anisotrópico con control de flujo divergente](images/seams-on-cascade-borders-due-to-anisotropic.jpg)

Este problema se resuelve calculando los derivados de la posición en el espacio de vista clara; la coordenada de espacio de la vista clara no es específica de la cascada seleccionada. Los derivados calculados se pueden escalar por la parte de la escala de la matriz de textura de proyección al nivel de mipmap adecuado.


```C++
        float3 vShadowTexCoordDDX = ddx( vShadowMapTextureCoordViewSpace );
        vShadowTexCoordDDX *= m_vCascadeScale[iCascade].xyz;
        float3 vShadowTexCoordDDY = ddy( vShadowMapTextureCoordViewSpace );
        vShadowTexCoordDDY *= m_vCascadeScale[iCascade].xyz;

        mapDepth += g_txShadow.SampleGrad( g_samShadow, vShadowTexCoord.xyz,
        vShadowTexCoordDDX, vShadowTexCoordDDY );
```



## <a name="vsms-compared-to-standard-shadows-with-pcf"></a>VSMs en comparación con las sombras estándar con PCF

Tanto VSMs como PCF intentan aproximar la fracción del área de píxeles que pasaría la prueba de profundidad. VSMs trabajar con el hardware de filtrado y se puede desenfocar con kernels separables. Los kernels de circunvolución separables son considerablemente más baratos de implementar que un kernel completo. Además, VSMs compara una profundidad de espacio claro con un valor en el mapa de profundidad del espacio claro. Esto significa que VSMs no tienen los mismos problemas de desplazamiento que PCF. Técnicamente, VSMs son la profundidad de muestreo en un área mayor, así como la realización de un análisis estadístico. Es menos preciso que PCF. En la práctica, VSMs realiza un trabajo muy bueno de la combinación, lo que hace que sea necesario un desplazamiento inferior. Tal y como se ha descrito anteriormente, el número uno de los inconvenientes de VSMs es la sangrado ligera.

VSMs y PCF representan un equilibrio entre la potencia de proceso de GPU y el ancho de banda de textura de GPU. VSMs requiere que se realicen más cálculos para calcular la varianza. PCF requiere más ancho de banda de memoria de textura. Los kernels PCF grandes se pueden poner en cuellos de botella rápidamente en el ancho de banda de textura. Con la potencia de cálculo de GPU que crece más rápidamente que el ancho de banda de GPU, los VSMs se convierten en los dos algoritmos más prácticos. VSMs también es mejor con las sombras de resolución más bajas debido a la mezcla y el filtrado.

## <a name="summary"></a>Resumen

CSMs ofrecen una solución al problema de los alias de perspectiva. Hay varias configuraciones posibles para obtener la fidelidad visual necesaria para un título. PCF y VSMs se usan ampliamente y deben combinarse con CSMs para reducir el alias.

## <a name="references"></a>Referencias

Donnelly, [W. y](https://portal.acm.org/citation.cfm?doid=1111411.1111440)Lauritzen, a. En SI3D ' 06: procedimientos del 2006 Symposium en gráficos y juegos de 3D interactivos. 2006. PP. 161:165. Nueva York, NY, EE. UU.: ACM Press.

Lauritzen, Andrew y McCool, Michael. [Mapas de sombras de varianza por capas](https://portal.acm.org/citation.cfm?id=1375714.1375739&coll=GUIDE&dl=GUIDE&CFID=45360327&CFTOKEN=34578992). Procedimientos de la interfaz de gráficos 2008, de 28 a 30, 2008, Windsor, Ontario y Canadá.

Engel, Woflgang F. sección 4. Mapas de instantáneas en cascada. ShaderX5, técnicas de representación avanzadas, Wolfgang F. Engel, Ed. Charles River media, Boston, Massachusetts. 2006. PP. 197:206.

 

 