---
title: Técnicas habituales para mejorar los mapas de profundidad de sombras
description: En este artículo técnico se proporciona información general sobre algunos algoritmos comunes de mapas de profundidad de sombra y artefactos comunes, y se explican varias técnicas, que van desde básicas a intermedias, que se pueden usar para aumentar la calidad de los mapas de sombra estándar.
ms.assetid: bf994838-a261-0379-9301-eb9b250d216c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aafff1b537830ae0ee681ed32932cca2b6274a4d9da3e0471ef498e0bef2d483
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120102539"
---
# <a name="common-techniques-to-improve-shadow-depth-maps"></a>Técnicas habituales para mejorar los mapas de profundidad de sombras

Los mapas de sombras, introducidos por primera vez en 1978, son una técnica común para agregar sombras a los juegos. Tres décadas después, a pesar de los avances en hardware y software, los artefactos de sombra (es decir, bordes brillantes, alias de perspectiva y otros problemas de precisión) persisten.

En este artículo técnico se proporciona información general sobre algunos algoritmos comunes de mapas de profundidad de sombra y artefactos comunes, y se explican varias técnicas, que van desde básicas a intermedias, que se pueden usar para aumentar la calidad de los mapas de sombra estándar. Agregar mapas de sombra básicos a un título suele ser sencillo, pero comprender los matices de los artefactos de sombra puede ser un desafío. Este artículo técnico está escrito para el desarrollador de gráficos intermedio que ha implementado sombras, pero no entiende totalmente por qué aparecen artefactos específicos y no está seguro de cómo trabajar en torno a ellos.

No es posible seleccionar las técnicas correctas para mitigar artefactos específicos. Cuando se abordan las deficiencias del mapa de sombras, la diferencia de calidad puede ser impresionante (Figura 1). La implementación correcta de estas técnicas mejora drásticamente las sombras estándar. Las técnicas que se explican en este artículo se implementan en el ejemplo CascadedShadowMaps11 del SDK de DirectX.

**Figura 1. Sombras con artefactos graves (izquierda) y sombras después de implementar las técnicas descritas en este artículo (derecha)**

![sombras con artefactos graves (izquierda) y sombras después de implementar las técnicas descritas en este artículo (derecha)](images/shadows-before-and-after.jpg)

## <a name="shadow-depth-maps-review"></a>Shadow Depth Mapas Review

El algoritmo de mapa de profundidad de sombra es un algoritmo de dos pases. El primer paso genera un mapa de profundidad en el espacio claro. En el segundo paso, este mapa se usa para comparar la profundidad de cada píxel en el espacio claro con su profundidad correspondiente en el mapa de profundidad del espacio claro.

**Figura 2. Partes clave de una escena de sombra**

![partes clave de una escena de sombra](images/key-parts-of-shadow-scene.jpg)

### <a name="pass-1"></a>Paso 1

La escena se muestra en la figura 2. En el primer paso (Figura 3), la geometría se representa en un búfer de profundidad desde el punto de vista de la luz. Más concretamente, el sombreador de vértices transforma la geometría en un espacio de vista ligera.

El resultado final de este primer paso es un búfer de profundidad que contiene la información de profundidad de la escena desde el punto de vista de la luz. Ahora se puede usar en el paso 2 para determinar qué píxeles se ocultan a partir de la luz.

**Figura 3. Primer paso de la asignación de sombras básica**

![primer paso de la asignación de sombras básica](images/first-pass-of-basic-hadow-mapping.png)

### <a name="pass-2"></a>Paso 2

En el segundo paso (Figura 4), el sombreador de vértices transforma cada vértice dos veces. Cada vértice se transforma en el espacio de vista de la cámara y se pasa al sombreador de píxeles como posición. Cada vértice también se transforma mediante la matriz view-projection-texture de la luz y se pasa al sombreador de píxeles como una coordenada de textura. La matriz view-projection-texture es la misma matriz que se usa para representar la escena en el paso 1 con una transformación adicional. Se trata de una transformación que escala y traduce los puntos del espacio de vista (de -1 a 1 en X e Y) al espacio de textura (de 0 a 1 en X y de 1 a 0 en Y).

El sombreador de píxeles recibe la posición interpolada y las coordenadas de textura interpoladas. Todo lo necesario para realizar la prueba de profundidad ahora está en esta coordenada de textura. La prueba de profundidad ahora se puede realizar indexando el búfer de profundidad desde el primer paso con las coordenadas de textura X e Y y comparando el valor de profundidad resultante con la coordenada de textura Z.

**Figura 4. Segundo paso de la asignación de sombras básica**

![segundo paso de la asignación de sombras básica](images/second-pass-of-basic-shadow-mapping.png)

## <a name="shadow-map-artifacts"></a>Shadow Map Artifacts

El algoritmo de mapa de profundidad de sombra es el algoritmo de sombreado en tiempo real más usado, pero sigue generando varios artefactos que requieren mitigación. Los tipos de artefactos que pueden producirse se resumen a continuación.

### <a name="perspective-aliasing"></a>Alias de perspectiva

El alias de perspectiva, un artefacto común, se muestra en la figura 5. Se produce cuando la asignación de píxeles en el espacio de vista a los elementos de textura del mapa de sombras no es una relación uno a uno. Esto se debe a que los píxeles cercanos al plano cercano están más cerca y requieren una mayor resolución de mapa de sombras.

En la figura 6 se muestra un mapa de sombras y un gráfico de vistas. Cerca del ojo, los píxeles están más cerca y muchos píxeles se asignan a los mismos texturas de sombra. Los píxeles del plano lejano se reparten, lo que reduce el alias de perspectiva.

**Figura 5. Alias de perspectiva alta (izquierda) frente a alias de perspectiva baja (derecha)**

![alias de perspectiva alta (izquierda) frente a alias de perspectiva baja (derecha)](images/high-perspective-aliasing-vs-low-perspective-aliasing.jpg)

Para la imagen de la izquierda, el alias de perspectiva es mayor; hay demasiados píxeles de espacio en los ojos asignados a los mismos elementos de textura del mapa de sombras. En la imagen de la derecha, el alias de perspectiva es bajo porque hay una asignación de 1:1 entre los píxeles de espacio de los ojos y los texturas del mapa de sombras.

**Figura 6. Visualización del frustum con un mapa de sombras**

![ver el frustum con el mapa de sombras](images/view-frustum-with-shadow-map.jpg)

Los píxeles claros del plano lejano representan alias de perspectiva baja y los píxeles oscuros del plano cercano representan alias de perspectiva alta.

La resolución del mapa de sombras también puede ser demasiado alta. Aunque una resolución más alta es menos perceptible, puede dar lugar a objetos pequeños, como los cables telefónicos, no a la conversión de sombras. Además, tener una resolución demasiado alta puede causar problemas graves de rendimiento debido a los patrones de acceso de textura.

Los mapas de sombra de perspectiva (PSM) y los mapas de sombra de perspectiva de espacio claro (LSPSM) intentan abordar el alias de perspectiva sesgando la matriz de proyección de la luz para colocar más elementos de textura cerca del ojo donde se necesitan. Desafortunadamente, ninguna técnica es capaz de resolver el alias de perspectiva. La parametrización de la transformación necesaria para asignar píxeles de espacio en los ojos a los elementos de textura del mapa de sombras no se puede enlazar mediante un sesgo lineal. Se requiere una parametrización logarítmica. Las PSM ponen demasiados detalles cerca del ojo, lo que hace que las sombras lejanas sean de baja calidad o incluso desaparezcan. Los LSPSM hacen un mejor trabajo de encontrar un punto intermedio entre aumentar la resolución cerca del ojo y dejar suficientes detalles para los objetos lejos. Ambas técnicas degeneran a sombras ortográficas en algunas configuraciones de escena. Esta degradación se puede contrarresta mediante la representación de un mapa de sombras independiente para cada cara del frustum de vista, aunque esto es costoso. Los mapas de sombra de perspectiva logarítmica (LogPSMs) también representan un mapa independiente por cara del frustum de vista. Esta técnica usa la rasterización no lineal para colocar más elementos de textura cerca del ojo. El hardware de las clases D3D10 y D3D11 no admite la rasterización no lineal. Para obtener más información sobre estas técnicas y algoritmos, vea la sección Referencias.

Los mapas de sombra en cascada (HSM) son la técnica más popular para trabajar con alias de perspectiva. Aunque los CSM se pueden combinar con PSM y LSPSM, no es necesario. El uso de CSM para corregir errores de alias de perspectiva se soluciona en el artículo complementario, [Cascaded Shadow Mapas](/windows/desktop/DxTechArts/cascaded-shadow-maps).

### <a name="projective-aliasing"></a>Alias projective

El alias proyectado es más difícil de mostrar que el alias de perspectiva. Las sombras resaltadas en la figura 7 muestran errores de alias de proyecto. El alias proyectativo se produce cuando la asignación entre los elementos de textura del espacio de la cámara a los elementos de textura en el espacio claro no es una relación uno a uno. esto se debe a la orientación de la geometría con respecto a la cámara ligera. El alias proyectativo se produce cuando el plano tangente de la geometría se convierte en paralelo a los rayos de luz.

**Figura 7. Alias de alto proyecto frente a alias con poco proyecto**

![alias de alto proyecto frente a alias con poco proyecto](images/high-projective-aliasing-vs-low%20projective-aliasing.jpg)

Las técnicas usadas para mitigar los errores de alias de perspectiva también mitigan el alias de proyecto. El alias proyectativo se produce cuando la superficie normal es ortogonal a la luz; estas superficies deben recibir menos luz en función de ecuaciones de iluminación difusa.

### <a name="shadow-acne-and-erroneous-self-shadowing"></a>Sombras sombrío y Self-Shadowing

La sombra sombra (Figura 8), un término sinónimo de sombras erróneas, se produce cuando el mapa de sombras cuantifica la profundidad de un texel completo. Cuando el sombreador compara una profundidad real con este valor, es tan probable que se sombree a sí mismo como si no se le sombree.

Otra razón para la sombra es que el texel del espacio claro está tan cerca de la profundidad del texel correspondiente en el mapa de profundidad que los errores de precisión hacen que la prueba de profundidad no se pueda realizar correctamente. Una razón de esta diferencia de precisión es que el hardware de rasterización de función fija calculó el mapa de profundidad, mientras que el sombreador calculó la profundidad que se está comparando. Los alias proyectativos también pueden provocar sombras.

**Figura 8. Artefacto de sombra de sombra**

![artefacto de sombra](images/shadow-acne-artifact.jpg)

Como se muestra en la imagen izquierda, algunos píxeles no pudieron realizar la prueba de profundidad y crearon artefactos y patrones moiré. Con el fin de reducir la sombra automática errónea, los límites del plano cercano y el plano lejano para el frustum de la vista del espacio claro se deben calcular lo más estrechamente posible. El sesgo de profundidad basado en la escala de pendiente y otros tipos de sesgo son otras soluciones que se usan para mitigar la sombra.

### <a name="peter-panning"></a>Peter Panning

El término *Peter Panning* deriva su nombre de un carácter de libro para niños cuya sombra se desasocia y quién puede sobresalir. Este artefacto hace que los objetos con sombras que faltan parezcan desasociarse y flotar sobre la superficie (Figura 9).

**Figura 9. Artefacto de Peter Panning**

![artefacto de movimiento panorámico de Peter](images/peter-panning-artifact.jpg)

En la imagen de la izquierda, la sombra se desasocia del objeto, lo que crea un efecto flotante.

Una técnica para quitar la superficie es agregar algún valor a la posición de píxel en el espacio claro. esto se denomina agregar un desplazamiento de profundidad. Peter Panning se traduce cuando el desplazamiento de profundidad usado es demasiado grande. En este caso, el desplazamiento de profundidad hace que la prueba de profundidad pase erróneamente. Al igual que la sombra, Peter Panning se resiente cuando no hay precisión suficiente en el búfer de profundidad. Calcular planos estrechos cerca y planos lejanos también ayuda a evitar Peter Panning.

## <a name="techniques-to-improve-shadow-maps"></a>Técnicas para mejorar las instantáneas Mapas

Agregar sombras a un título es un proceso. El primer paso es hacer que los mapas de sombra básicos funcionen. La segunda es asegurarse de que todos los cálculos básicos se realizan de forma óptima: frusta cabe lo más estrechamente posible, los planos cercanos o lejanos se ajustan estrechamente, se usa el sesgo de escala de pendiente, y así sucesivamente. Una vez habilitadas las sombras básicas y tener un aspecto lo más bueno posible, el desarrollador tiene una idea mejor de qué algoritmos son necesarios para conseguir que las sombras sean lo suficientemente precisas. En esta sección se dan sugerencias básicas que pueden ser necesarias para obtener mapas de sombra básicos que buscan lo mejor posible.

### <a name="slope-scale-depth-bias"></a>Slope-Scale sesgo de profundidad

Como se mencionó anteriormente, el sobresalto propio puede dar lugar a sombras. Agregar demasiado sesgo puede dar lugar a Peter Panning. Además, los polígonos con pendientes empinadas (en relación con la luz) sufren más de los alias proyectativos que los polígonos con pendientes superficiales (en relación con la luz). Por este problema, cada valor del mapa de profundidad puede necesitar un desplazamiento diferente en función de la pendiente del polígono con respecto a la luz.

El hardware de Direct3D 10 tiene la capacidad de sesgo de un polígono en función de su pendiente con respecto a la dirección de la vista. Esto tiene el efecto de aplicar un sesgo grande a un polígono que se ve de forma perimetral en la dirección de la luz, pero no aplicar ningún sesgo a un polígono orientado directamente a la luz. En la figura 10 se muestra cómo se pueden alternar dos píxeles vecinos entre sombreados y no sombreados al realizar pruebas con la misma pendiente no sesida.

**Figura 10. Sesgo de profundidad escalada de pendiente en comparación con la profundidad no sesgada**

![sesgo de profundidad escalada de pendiente en comparación con la profundidad no sesgada](images/slope-scaled-depth-bias-compared-to-unbiased-depth.png)

### <a name="calculating-a-tight-projection"></a>Calcular una proyección ajustada

Ajustar estrechamente la proyección de la luz al frustum de la vista aumenta la cobertura del mapa de sombras. En la figura 11 se muestra que el uso de una proyección arbitraria o el ajuste de la proyección a los límites de la escena da como resultado un alias de perspectiva superior.

**Figura 11. Frustum de sombra arbitrario y frustum de sombra caben en la escena**

![frustum de sombra arbitrario y frustum de sombra caben en la escena](images/arbitrary-shadow-frustum-and-shadow-frustum-fit-to-scene.jpg)

La vista se encuentra desde el punto de vista de la luz. El trapezoide representa el frustum de la cámara de vista. La cuadrícula dibujada sobre la imagen representa el mapa de sombras. La imagen de la derecha muestra que el mismo mapa de sombras de resolución crea más cobertura de textura cuando se ajusta más estrechamente a la escena.

En la figura 12 se muestran los frustums que se ajustan correctamente. Para calcular la proyección, los ocho puntos que son el frustum de la vista se transforman en espacio claro. A continuación, se encuentran los valores mínimo y máximo en X e Y. Estos valores son los límites de una proyección ortográfica.

**Figura 12. Ajuste de proyección de sombra para ver el frustum**

![ajuste de proyección de sombra para ver el frustum](images/shadow-projection-fit-to-view-frustum.jpg)

También es posible recortar el frustum a la escena AABB para obtener un límite más estricto. Esto no se recomienda en todos los casos porque esto puede cambiar el tamaño de la proyección de la cámara de luz de marco a marco. Muchas técnicas, como las descritas en la sección Mover la luz Texel-Sized incrementos, dan mejores resultados cuando el tamaño de la proyección de la luz permanece constante en cada fotograma.

### <a name="calculating-the-near-plane-and-far-plane"></a>Calcular el plano cercano y el plano lejano

El plano cercano y el plano lejano son las partes finales necesarias para calcular la matriz de proyección. Cuando más juntos estén los planos, más precisos son los valores del búfer de profundidad.

El búfer de profundidad puede ser de 16 bits, 24 o 32 bits, con valores entre 0 y 1. Por lo general, los búferes de profundidad son puntos fijos, con los valores cercanos al plano cercano agrupados más estrechamente que los valores cercanos al plano lejano. El grado de precisión disponible para el búfer de profundidad viene determinado por la relación entre el plano cercano y el plano lejano. El uso del plano cercano o lejano más estricto posible podría permitir el uso de un búfer de profundidad de 16 bits. Un búfer de profundidad de 16 bits podría reducir el uso de memoria a la vez que aumenta la velocidad de procesamiento.

### <a name="aabb-based-near-plane-and-far-plane"></a>AABB-Based plano cercano y plano lejano

Una manera sencilla e sencilla de calcular el plano cercano y el plano lejano es transformar el volumen delimitador de la escena en espacio claro. El valor de coordenada Z más pequeño es el plano cercano y el valor de coordenada Z más grande es el plano lejano. Para muchas configuraciones de la escena y la luz, este enfoque es suficiente. Sin embargo, el peor escenario puede provocar una pérdida significativa de precisión en el búfer de profundidad. En la figura 13 se muestra este escenario. Aquí, el intervalo del plano cercano al plano lejano es cuatro veces mayor que el necesario.

El frustum de la vista de la figura 13 se eligió a propósito para ser pequeño. Un pequeño frustum de vista se muestra en una escena muy grande que consta de pilares que se extienden fuera de la cámara de vista. El uso de scene AABB para los planos cercanos y lejanos no es óptimo. El algoritmo de CSM descrito en el artículo Mapas sobre sombras en cascada debe calcular planos cercanos y lejanos para los frustums muy pequeños. [](/windows/desktop/DxTechArts/cascaded-shadow-maps)

**Figura 13. Planos cercanos y lejanos basados en scene AABB**

![planos cercanos y lejanos basados en la escena aabb](images/near-far-%20planes-based-on-scene-aabb.jpg)

### <a name="frustum-based-near-plane-and-far-plane"></a>Frustum-Based plano cercano y plano lejano

Otra técnica para calcular los planos cercanos y lejanos es transformar el frustum en espacio claro y usar los valores mínimos y máximos de Z como planos cercanos y lejanos, respectivamente. En la figura 14 se muestran los dos problemas con este enfoque. En primer lugar, el cálculo es demasiado conservador, como se muestra cuando el frustum se extiende más allá de la geometría de la escena. En segundo lugar, el plano cercano podría ser demasiado estrecho, lo que provocaría que se recortara el sombreador.

**Figura 14. Planos cercanos y lejanos basados únicamente en el frustum de la vista**

![planos cercanos y lejanos basados únicamente en el frustum de la vista](images/near-far-planes-based-solely-on-view-frustum.jpg)

### <a name="light-frustum-intersected-with-scene-to-calculate-near-and-far-planes"></a>Frustum claro intersecado con la escena para calcular planos cercanos y lejanos

La manera adecuada de calcular los planos cercanos y lejanos se muestra en la figura 15. Cuatro de los planos del frusto de luz ortográfica se calcularon utilizando el mínimo y el máximo de las coordenadas X e Y del frustum de vista en el espacio claro. Los dos últimos planos del frustum de vista ortogonal son los planos cercanos y lejanos. Para encontrar estos planos, los límites de la escena se recortan en los cuatro planos de frustum claros conocidos. Los valores Z más pequeños y mayores del límite recién recortado representan el plano cercano y el plano lejano, respectivamente.

El código que realiza esta operación se encuentra en el ejemplo CascadedShadowMaps11. Los ocho puntos que son el AABB del mundo se transforman en espacio claro. La transformación de los puntos en espacio claro simplifica las pruebas de recorte. Los cuatro planos conocidos del frustum claro ahora se pueden representar como líneas. El volumen de límite de escenas en el espacio claro se puede representar como seis cuadrículos. Estos 6 cuadráteros se pueden convertir en 12 triángulos para el recorte basado en triángulos. Los triángulos se recortan en los planos conocidos del frustum de la vista (se trata de líneas horizontales y verticales en X e Y en el espacio claro). Cuando se encuentra un punto de intersección en X e Y, el triángulo 3D se recorta en ese punto. Los valores Z mínimo y máximo de todos los triángulos recortados son el plano cercano y el plano lejano. El ejemplo CascadedShadowMaps11 muestra cómo realizar este recorte en la **función ComputeNearAndFar.**

Hay dos técnicas más que podrían usarse para calcular los planos más estrechos posibles, tanto cercanos como lejanos. Estas técnicas no se muestran en el ejemplo CascadedShadowMaps.

-   Incluso los planos más cercanos y lejanos se podrían calcular mediante la intersección de una jerarquía de una escena o de objetos individuales de una escena con el frustum claro. Esto sería computacionalmente más complejo. Aunque no se muestra en el ejemplo CascadedShadowMaps11, podría ser una técnica válida para algunos iconos.
-   El plano lejano se podría calcular tomando el mínimo de:

    -   Profundidad más grande del frustum de la vista en el espacio claro.
    -   Profundidad más grande de la intersección de la vista frustum y la escena AABB.

Este enfoque puede ser problemático cuando se usa con mapas de sombra en cascada donde es posible indexar fuera de un frustum de vista. En este caso, es posible que falte geometría en el mapa de sombras.

**Figura 15. Planos cercanos y lejanos basados en la intersección de los cuatro planos calculados del frusto claro y la geometría delimitadora de la escena**

![planos cercanos y lejanos basados en la intersección de los cuatro planos calculados del frusto claro y la geometría delimitadora de la escena](images/near-far-plane-based-on-intersection-of-four.jpg)

### <a name="moving-the-light-in-texel-sized-increments"></a>Mover la luz en Texel-Sized incrementos

Un artefacto común en los mapas de sombras es el efecto de borde resplandeciente. A medida que se mueve la cámara, los píxeles que aparecen a lo largo de los bordes de las sombras se i brighten y darken. Esto no se puede ver en imágenes fijas, pero es muy perceptible y distrae en tiempo real. En la figura 16 se resalta este problema y en la figura 17 se muestra el aspecto de los bordes de las sombras.

El error del borde resplandeciente se produce porque la matriz de proyección de luz se vuelve a calcular cada vez que se mueve la cámara. Esto crea diferencias sutiles en los mapas de sombra generados. Todos los factores siguientes pueden influir en la matriz creada para enlazar la escena.

-   Tamaño del frustum de vista
-   Orientación del frustum de vista
-   Ubicación de la luz
-   Ubicación de la cámara

Cada vez que cambia esta matriz, los bordes de las sombras pueden cambiar.

**Figura 16. Bordes de sombra resplandecientes**

![bordes de sombra resplandecientes](images/shimmering-shadow-edges.jpg)

Los píxeles a lo largo del borde de la sombra entra y sale de la sombra a medida que la cámara se mueve de izquierda a derecha.

**Figura 17. Sombras sin bordes relucientes**

![sombras sin bordes relucientes](images/shadows-without-shimmering-edges.jpg)

Los bordes de sombra permanecen constantes a medida que la cámara se mueve de izquierda a derecha.

Para las luces direccionales, la solución a este problema es redondear el valor mínimo o máximo en X e Y (que son los límites de proyección ortográfica) a incrementos de tamaño de píxel. Esto se puede hacer con una operación de división, una operación de planta y una multiplicación.


```C++
        vLightCameraOrthographicMin /= vWorldUnitsPerTexel;
        vLightCameraOrthographicMin = XMVectorFloor( vLightCameraOrthographicMin );
        vLightCameraOrthographicMin *= vWorldUnitsPerTexel;
        vLightCameraOrthographicMax /= vWorldUnitsPerTexel;
        vLightCameraOrthographicMax = XMVectorFloor( vLightCameraOrthographicMax );
        vLightCameraOrthographicMax *= vWorldUnitsPerTexel;
```



El valor vWorldUnitsPerTexel se calcula tomando un límite de la frustum de vista y dividiendo por el tamaño del búfer.


```C++
        FLOAT fWorldUnitsPerTexel = fCascadeBound /
        (float)m_CopyOfCascadeConfig.m_iBufferSize;
        vWorldUnitsPerTexel = XMVectorSet( fWorldUnitsPerTexel, fWorldUnitsPerTexel,                            0.0f, 0.0f );
```



Al delimitar el tamaño máximo de la frustum de vista, se produce un ajuste más flexible para la proyección ortográfica.

Es importante tener en cuenta que la textura es de 1 píxel de ancho y alto cuando se usa esta técnica. Esto evita que las coordenadas de sombra se indexe fuera del mapa de sombras.

### <a name="back-face-and-front-face"></a>Back Face y Front Face

Los mapas de sombras se deben representar con la selección de cara posterior estándar, un proceso que omite la rasterización de objetos que el visor no puede ver y acelera la representación de la escena. Otra opción común es representar mapas de sombra con la selección de caras frontales habilitada, lo que significa que se eliminan los objetos que miran al visor. El argumento para esto es que ayuda con el sombreado propio, ya que la geometría que forma la parte posterior de los objetos está ligeramente desfasada. Hay dos problemas con esta idea.

-   Cualquier objeto con geometría incorrecta de la cara frontal o de la cara posterior provoca artefactos en el mapa de sombras. Sin embargo, tener geometría de cara frontal o de cara posterior incorrecta provocará otros problemas, por lo que puede ser seguro suponer que la geometría de cara frontal y de cara posterior se realiza correctamente. Puede que no sea práctico crear caras de fondo para geometría basada en sprites, como el foliage.
-   Es más probable que peter panning y shadow gaps cerca de la base de objetos como las paredes se produzcan porque la disparidad de profundidad de la sombra es demasiado pequeña.

### <a name="shadow-mapfriendly-geometry"></a>Mapa de sombra: geometría fácil de usar

La creación de geometría que funciona bien en mapas de sombras permite más flexibilidad al combatir artefactos como Peter Panning y shadow shadow shadow.

Los bordes duros son problemáticos para el sombreado propio. La disparidad de profundidad cerca de la punta del borde es muy pequeña. Incluso un desplazamiento pequeño puede hacer que los objetos pierdan sus sombras (Figura 18).

**Figura 18. Los bordes nítidos provocan artefactos derivados de la disparidad de baja profundidad con desplazamientos**

![los bordes nítidos provocan artefactos derivados de la disparidad de baja profundidad con desplazamientos](images/sharp-edges-cause%20artifacts.jpg)

Los objetos estrechos, como las paredes, deben tener respaldos aunque nunca estén visibles. Esto aumentará la disparidad de profundidad.

También es importante asegurarse de que la dirección en la que se encuentra la geometría es correcta. es decir, el exterior de un objeto debe estar orientado hacia atrás y el interior de un objeto debe estar orientado hacia delante. Esto es importante para la representación con la selección de la cara posterior habilitada, así como para combatir los efectos del sesgo de profundidad.

## <a name="summary"></a>Resumen

Las técnicas descritas en este artículo se pueden usar para aumentar la calidad de los mapas de sombra estándar. El siguiente paso consiste en ver técnicas que pueden funcionar bien con mapas de sombras estándar. Los HSM se recomiendan como una técnica superior para combatir el alias de perspectiva. El filtrado de porcentaje más cercano o los mapas de sombras de varianza se pueden usar para sombrer los bordes de sombra. Para más información, consulte [el Mapas cascaded shadow](/windows/desktop/DxTechArts/cascaded-shadow-maps) Mapas.

Doney, W., and Lauguideen, A. [Variance Shadow Mapas](https://portal.acm.org/citation.cfm?doid=1111411.1111440). Marchas sobre gráficos 3D interactivos, Procedimientos del 2006 Desequiendo sobre gráficos y juegos 3D interactivos. 2006, pp. 161–165.

Engel, Woflmatriz F. Sección 4. Instantáneas en cascada Mapas. ShaderX5, *Advanced Rendering Techniques*, Shader F. Engel, Ed. Charles River Media, Boston, Massachusts. 2006. pp. 197–206.

Stamminger, Marc y Dr dragkis, Antonio. [Sombra de perspectiva Mapas](https://portal.acm.org/citation.cfm?id=566616). International Conference on Computer Graphics and Interactive Techniques, *Proceedings of the 29th Annual Conference on Computer Graphics and Interactive Techniques*. 2002, pp 557–562.

Wimmer, M., Scherzer, D. y Purgathofer, W. [Light Space Perspective Shadow Mapas](https://www.cg.tuwien.ac.at/research/vr/lispsm/shadows_egsr2004_revised.pdf). Eurographics Symposium on Rendering. 2004. Revisado el 10 de junio de 2005. [Techn inerte DeSebat Wien](https://www.cg.tuwien.ac.at/research/vr/lispsm/).

 

 
