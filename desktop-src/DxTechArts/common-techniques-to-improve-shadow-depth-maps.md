---
title: Técnicas habituales para mejorar los mapas de profundidad de sombras
description: En este artículo técnico se proporciona información general sobre algunos algoritmos de mapa de profundidad de sombra comunes y artefactos comunes, y se explican varias técnicas, que abarcan en gran parte del nivel básico al intermedio, que se pueden usar para aumentar la calidad de las asignaciones de instantáneas estándar.
ms.assetid: bf994838-a261-0379-9301-eb9b250d216c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8b25507d7f6b8608d4dacf5fab620bc8a3294c7
ms.sourcegitcommit: 218b1ff779402c3ebe1786679e1aa80a5c0d6c95
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/01/2020
ms.locfileid: "103794182"
---
# <a name="common-techniques-to-improve-shadow-depth-maps"></a>Técnicas habituales para mejorar los mapas de profundidad de sombras

Las asignaciones sombra, introducidas por primera vez en 1978, son una técnica común para agregar sombras a los juegos. Tres décadas después, a pesar de los avances en hardware y software, los artefactos de sombreado, como los bordes de Shimmering, el alias de perspectiva y otros problemas de precisión, se conservan.

En este artículo técnico se proporciona información general sobre algunos algoritmos de mapa de profundidad de sombra comunes y artefactos comunes, y se explican varias técnicas, que abarcan en gran parte del nivel básico al intermedio, que se pueden usar para aumentar la calidad de las asignaciones de instantáneas estándar. Agregar mapas de sombra básicos a un título normalmente es sencillo, pero entender los matices de los artefactos de sombra puede ser desafiante. Este artículo técnico está escrito para el desarrollador de gráficos intermedios que ha implementado sombras, pero no comprende por completo por qué aparecen artefactos específicos y no está seguro de cómo solucionarlos.

La selección de las técnicas correctas para mitigar artefactos específicos no es trivial. Cuando se resuelven las deficiencias en el mapa de sombras, la diferencia de calidad puede ser impresionante (Figura 1). La implementación correcta de estas técnicas mejora drásticamente las sombras estándar. Las técnicas que se explican en este artículo se implementan en el ejemplo de CascadedShadowMaps11 en el SDK de DirectX.

**Figura 1. Sombras con artefactos graves (izquierda) y sombras después de implementar las técnicas descritas en este artículo (derecha)**

![sombras con artefactos graves (izquierda) y sombras después de implementar las técnicas descritas en este artículo (derecha)](images/shadows-before-and-after.jpg)

## <a name="shadow-depth-maps-review"></a>Revisión de mapas de profundidad de sombra

El algoritmo de mapa de profundidad de sombra es un algoritmo de dos pasos. El primer paso genera un mapa de profundidad en el espacio claro. En el segundo paso, este mapa se usa para comparar la profundidad de cada píxel en el espacio claro con su profundidad correspondiente en el mapa de profundidad del espacio de la luz.

**Figura 2. Partes clave de una escena sombra**

![partes clave de una escena sombra](images/key-parts-of-shadow-scene.jpg)

### <a name="pass-1"></a>Paso 1

La escena se muestra en la figura 2. En el primer paso (Figura 3), la geometría se representa en un búfer de profundidad desde el punto de vista de la luz. Más concretamente, el sombreador de vértices transforma la geometría en un espacio de vista clara.

El resultado final de este primer paso es un búfer de profundidad que contiene la información de profundidad de la escena desde el punto de vista de la luz. Ahora se puede usar en el paso 2 para determinar qué píxeles se ocluidos de la luz.

**Figura 3. Primer paso de la asignación de sombra básica**

![primer paso de la asignación de sombra básica](images/first-pass-of-basic-hadow-mapping.png)

### <a name="pass-2"></a>Paso 2

En el segundo paso (Figura 4), el sombreador de vértices transforma cada vértice dos veces. Cada vértice se transforma en el espacio de la vista de la cámara y se pasa al sombreador de píxeles como la posición. Cada vértice también se transforma por la matriz de texturas de vista-proyección de la luz y se pasa al sombreador de píxeles como una coordenada de textura. La matriz View-Projection-Texture es la misma matriz que se usa para representar la escena en Pass 1 con una transformación adicional. Es una transformación que escala y traduce los puntos del espacio de vista (de-1 a 1 en X e y) al espacio de textura (de 0 a 1 en X y de 1 a 0 en Y).

El sombreador de píxeles recibe la posición interpolada y las coordenadas de textura interpoladas. Todo lo necesario para realizar la prueba de profundidad es ahora en esta coordenada de textura. La prueba de profundidad se puede realizar ahora indizando el búfer de profundidad desde el primer paso con las coordenadas de textura X e y y comparando el valor de profundidad resultante con la coordenada de textura Z.

**Figura 4. Segundo paso de la asignación de sombra básica**

![segundo paso de la asignación de sombra básica](images/second-pass-of-basic-shadow-mapping.png)

## <a name="shadow-map-artifacts"></a>Artefactos de mapa de sombras

El algoritmo de mapa de profundidad de sombra es el algoritmo de sombreado en tiempo real más utilizado, pero todavía produce varios artefactos que requieren mitigación. A continuación se resumen los tipos de artefactos que se pueden producir.

### <a name="perspective-aliasing"></a>Alias de perspectiva

El alias de perspectiva, un artefacto común, se muestra en la figura 5. Se produce cuando la asignación de píxeles en el espacio de la vista a textura en el mapa de sombras no es una relación de uno a uno. Esto se debe a que los píxeles cercanos al plano próximo están más juntos y requieren una resolución de mapa de sombras superior.

En la ilustración 6 se muestra un mapa de sombras y un frustum de vista. Cerca del ojo, los píxeles están más juntos y muchos píxeles se asignan a la misma sombra textura. Los píxeles del plano lejano se distribuyen, lo que reduce el alias de perspectiva.

**Figura 5. Alias de perspectiva alta (izquierda) frente a alias de perspectiva baja (derecha)**

![alias de perspectiva alta (izquierda) frente a alias de perspectiva baja (derecha)](images/high-perspective-aliasing-vs-low-perspective-aliasing.jpg)

Para la imagen a la izquierda, el alias de perspectiva es mayor; hay demasiados píxeles de espacio ocular asignados al mismo textura de mapa de sombras. En la imagen de la derecha, el alias de perspectiva es bajo porque hay una asignación 1:1 entre los píxeles de espacio de ojo y el textura de mapa de sombras.

**Figura 6. Ver el frustum con el mapa de instantáneas**

![ver el frustum con el mapa de instantáneas](images/view-frustum-with-shadow-map.jpg)

Los píxeles claros del plano lejano representan el alias de baja perspectiva y los píxeles oscuros del plano próximo representan un alias de perspectiva alta.

La resolución de mapa de sombras también puede ser demasiado alta. Aunque una resolución mayor es menos apreciable, no obstante, puede dar lugar a objetos pequeños, como hilos de teléfono, no sombras. Además, si la resolución es demasiado alta, pueden producirse graves problemas de rendimiento debido a los patrones de acceso de textura.

Mapas de sombra de perspectiva (PSMs) y mapas de sombra de perspectiva de espacio ligero (LSPSMs) intentan direccionar el alias de la perspectiva mediante la inclinación de la matriz de proyección de la luz para colocar más textura cerca del ojo en el que se necesitan. Desafortunadamente, ninguna de las técnicas puede resolver el alias de perspectiva. La parametrización de la transformación necesaria para asignar píxeles de espacio ocular a textura en la instantánea no se puede enlazar mediante un sesgo lineal. Se requiere una parametrización logarítmica. PSMs colocan muchos detalles cerca del ojo, lo que hace que las sombras lejanas sean de baja calidad o incluso desaparezcan. LSPSMs realiza un mejor trabajo de buscar un medio entre una resolución cada vez mayor cerca del ojo y mantener los detalles suficientes para los objetos alejados. Ambas técnicas degeneraban sombras ortográficas en algunas configuraciones de escena. Esta desgeneración puede ser responsable de la representación de un mapa de sombras independiente para cada cara del frustum de la vista, aunque esto resulta caro. Los mapas de sombras de perspectiva logarítmica (LogPSMs) también representan un mapa independiente por cada aspecto del frustum de la vista. Esta técnica usa la rasterización no lineal para colocar más textura cerca del ojo. El hardware de clase D3D10 y D3D11 no admite la rasterización no lineal. Para obtener más información sobre estas técnicas y algoritmos, vea la sección referencias.

Los mapas de sombras en cascada (CSMs) son la técnica más popular para tratar con el alias de perspectiva. Aunque CSMs se puede combinar con PSMs y LSPSMs, no es necesario. El uso de CSMs para corregir errores de alias de perspectiva se trata en el artículo complementario, [mapas de instantáneas en cascada](/windows/desktop/DxTechArts/cascaded-shadow-maps).

### <a name="projective-aliasing"></a>Alias proyectado

El alias proyectado es más difícil de mostrar que el alias de perspectiva. Las sombras destiendes resaltadas en la figura 7 muestran errores de alias proyectados. El alias proyectado se produce cuando la asignación entre textura en el espacio de la cámara a textura en el espacio de la luz no es una relación de uno a uno; Esto se debe a la orientación de la geometría con respecto a la cámara ligera. El suavizado de contornos se produce como el plano tangente de la geometría se convierte en paralelo a los rayos claros.

**Figura 7. Alias de proyección alta frente a alias bajo de proyecto**

![alias de proyección alta frente a alias bajo de proyecto](images/high-projective-aliasing-vs-low%20projective-aliasing.jpg)

Las técnicas que se usan para mitigar los errores de alias de perspectiva también mitigan el alias proyectado. El alias proyectado se produce cuando la superficie normal es ortogonal a la luz; estas superficies deben recibir menos luz en función de las ecuaciones de iluminación difusa.

### <a name="shadow-acne-and-erroneous-self-shadowing"></a>Sombra acne y Self-Shadowing errónea

Shadow Acne (Figura 8), un término sinónimo de sombra automática errónea, se produce cuando la asignación de instantáneas cuantifica la profundidad sobre un textura completo. Cuando el sombreador compara una profundidad real con este valor, es probable que se realice una sombra automática, ya que no se realizará la sombra.

Otro motivo de la sombra acne es que el textura en el espacio de la luz está tan cerca de la profundidad de la textura correspondiente en el mapa de profundidad que los errores de precisión hacen que la prueba de profundidad falle erróneamente. Una razón para esta diferencia de precisión es que el mapa de profundidad se calculó por el hardware de rasterización de funciones fijas, mientras que la profundidad que se compara fue calculada por el sombreador. El alias proyectado también puede producir sombras acne.

**Ilustración 8. Artefacto acne de sombra**

![artefacto acne de sombra](images/shadow-acne-artifact.jpg)

Tal y como se muestra en la imagen izquierda, algunos de los píxeles no pudieron realizar la prueba de profundidad y crearon artefactos moteados y patrones trama moiré. Con el fin de reducir la sombra automática errónea, los límites del plano próximo y el plano lejano del frustum de la vista del espacio de la luz deben calcularse de la forma más estricta posible. La diferencia de profundidad basada en la escala de pendiente y otros tipos de sesgo son otras soluciones que se usan para mitigar la acne de sombra.

### <a name="peter-panning"></a>Movimiento panorámico de Peter

El término *movimiento panorámico de Peter* deriva su nombre del carácter de libro de un elemento secundario cuya sombra se desconectó y que podría volar. Este artefacto hace que los objetos a los que les faltan sombras parezcan desasociados y flotando por encima de la superficie (Figura 9).

**Ilustración 9. El artefacto de movimiento panorámico Peter**

![el artefacto de movimiento panorámico Peter](images/peter-panning-artifact.jpg)

En la imagen de la izquierda, la sombra se separa del objeto, lo que crea un efecto flotante.

Una técnica para quitar Surface acne es agregar algún valor a la posición en píxeles en el espacio de la luz. Esto se denomina agregar un desplazamiento de profundidad. Peter el movimiento panorámico se produce cuando el desplazamiento de profundidad utilizado es demasiado grande. En este caso, el desplazamiento de profundidad hace que la prueba de profundidad pase erróneamente. Al igual que Shadow acne, Peter saning se agrava cuando no hay suficiente precisión en el búfer de profundidad. Calcular los planos cercanos y los planos lejanos también ayuda a evitar la panorámica de Peter.

## <a name="techniques-to-improve-shadow-maps"></a>Técnicas para mejorar las asignaciones de instantáneas

Agregar sombras a un título es un proceso. El primer paso es conseguir que funcionen los mapas de instantáneas básicos. La segunda consiste en asegurarse de que todos los cálculos básicos se realicen de forma óptima: Frusta con la mayor precisión posible, que los planos cercanos y alejados se ajustan de manera estricta, se usa la diferencia de escala de pendiente, etc. Una vez que las sombras básicas están habilitadas y tienen la apariencia que sea posible, el desarrollador tiene una idea más clara de los algoritmos que son necesarios para obtener las sombras con suficiente fidelidad. En esta sección se proporcionan sugerencias básicas que pueden ser necesarias para obtener mapas de instantáneas básicos.

### <a name="slope-scale-depth-bias"></a>Slope-Scale sesgo de profundidad

Como se mencionó anteriormente, la sombra automática puede conducir a la sombra de acne. Agregar demasiadas sesgo puede dar lugar a la panorámica de Peter. Además, los polígonos con pendientes pendientes (con respecto a la luz) sufren más de un alias proyectado que polígonos con pendientes superficiales (con respecto a la luz). Debido a esto, cada valor de mapa de profundidad puede necesitar un desplazamiento diferente en función de la pendiente del polígono con respecto a la luz.

El hardware de Direct3D 10 tiene la capacidad de sesgar un polígono en función de su pendiente con respecto a la dirección de la vista. Esto tiene el efecto de aplicar una gran diferencia a un polígono que se ve borde hacia arriba en la dirección de la luz, pero no aplica ningún sesgo a un polígono que enfrente directamente la luz. En la figura 10 se muestra cómo dos píxeles adyacentes pueden alternar entre el sombreado y el sombreado al realizar pruebas en la misma pendiente no sesgada.

**Figura 10. Profundidad escalada de pendiente: diferencia respecto a profundidad no sesgada**

![profundidad escalada de pendiente: diferencia respecto a profundidad no sesgada](images/slope-scaled-depth-bias-compared-to-unbiased-depth.png)

### <a name="calculating-a-tight-projection"></a>Calcular una proyección estrecha

Ajustar estrechamente la proyección de la luz al frustum de la vista aumenta la cobertura de la asignación de sombras. En la figura 11 se muestra que el uso de una proyección arbitraria, o la conexión de la proyección a los límites de la escena, da como resultado un alias de perspectiva mayor.

**Figura 11. El frustum de sombra y el frustum de sombra arbitrarios se ajustan a la escena**

![el frustum de sombra y el frustum de sombra arbitrarios se ajustan a la escena](images/arbitrary-shadow-frustum-and-shadow-frustum-fit-to-scene.jpg)

La vista es desde el punto de vista de la luz. El trapezoide representa el frustum de la cámara de la vista. La cuadrícula dibujada sobre la imagen representa la asignación de instantáneas. La imagen de la derecha muestra que la misma asignación de sombra de resolución crea más cobertura de textura cuando se ajusta mejor a la escena.

En la ilustración 12 se muestran Frustums que se ajustan correctamente. Para calcular la proyección, los ocho puntos que componen el frustum de la vista se transforman en el espacio de la luz. A continuación, se encuentran los valores mínimo y máximo de X e y. Estos valores componen los límites de una proyección ortográfica.

**Figura 12. Ajuste de proyección de sombra para ver el frustum**

![ajuste de proyección de sombra para ver el frustum](images/shadow-projection-fit-to-view-frustum.jpg)

También es posible recortar el frustum al AABB de escenas para obtener un límite más estricto. Esto no se recomienda en todos los casos, ya que esto puede cambiar el tamaño de la proyección de la cámara Light de fotograma a fotograma. Muchas técnicas, como las descritas en la sección mover la luz Texel-Sized incrementos, proporcionan mejores resultados cuando el tamaño de la proyección de la luz permanece constante en cada fotograma.

### <a name="calculating-the-near-plane-and-far-plane"></a>Cálculo del plano próximo y del plano lejano

El plano cercano y el plano lejano son las piezas finales necesarias para calcular la matriz de proyección. Cuanto más juntos sean los planos, más precisos serán los valores en el búfer de profundidad.

El búfer de profundidad puede ser de 16 bits, de 24 bits o de 32 bits, con valores entre 0 y 1. Por lo general, los búferes de profundidad son de punto fijo, y los valores cercanos al plano cercano se agrupan más estrechamente que los valores cercanos al plano lejano. El grado de precisión disponible para el búfer de profundidad viene determinado por la relación entre el plano cercano y el plano lejano. El uso del plano Near/Far más estrecho posible podría permitir el uso de un búfer de profundidad de 16 bits. Un búfer de profundidad de 16 bits podría reducir el uso de memoria al tiempo que aumenta la velocidad de procesamiento.

### <a name="aabb-based-near-plane-and-far-plane"></a>AABB-Based plano próximo y plano lejano

Una manera fácil y Naive de calcular el plano cercano y el plano lejano es transformar el volumen de límite de la escena en el espacio de la luz. El menor valor de la coordenada Z es el plano cercano y el mayor valor de la coordenada Z es el plano lejano. Este enfoque es suficiente para muchas configuraciones de la escena y la luz. Sin embargo, en el peor de los casos, se puede producir una pérdida significativa de precisión en el búfer de profundidad. La figura 13 muestra este escenario. Aquí el intervalo del plano próximo al plano lejano es cuatro veces más grande de lo necesario.

El frustum de vista de la figura 13 se eligió intencionadamente para ser pequeño. Un frustum de vista pequeño se muestra en una escena muy grande que se compone de pilares que se extienden desde la cámara de vista. El uso del AABB de escenas para los planos Near y Far no es óptimo. El algoritmo CSM descrito en el artículo técnico de [mapas de instantáneas en cascada](/windows/desktop/DxTechArts/cascaded-shadow-maps) debe calcular planos cercanos y alejados para un Frustums muy pequeño.

**Figura 13. Planos cercanos y lejanos basados en la escena AABB**

![planos cercanos y lejanos basados en la escena AABB](images/near-far-%20planes-based-on-scene-aabb.jpg)

### <a name="frustum-based-near-plane-and-far-plane"></a>Frustum-Based plano próximo y plano lejano

Otra técnica para calcular los planos Near y Far es transformar el frustum en el espacio de luz y usar los valores mínimo y máximo en Z como los planos cercano y lejano, respectivamente. En la figura 14 se ilustran los dos problemas de este enfoque. En primer lugar, el cálculo es demasiado conservador, como se muestra cuando el frustum se extiende más allá de la geometría de la escena. En segundo lugar, el plano próximo podría estar demasiado apretado, lo que provocaría la recorte de las sombras.

**Figura 14. Planos Near y Far basados únicamente en el frustum de vista**

![planos Near y Far basados únicamente en el frustum de vista](images/near-far-planes-based-solely-on-view-frustum.jpg)

### <a name="light-frustum-intersected-with-scene-to-calculate-near-and-far-planes"></a>Frustum ligero intersectado con la escena para calcular planos cercanos y alejados

La manera adecuada de calcular los planos Near y Far se muestra en la figura 15. Cuatro de los planos del frustum de la luz ortográfica se calcularon usando los valores mínimo y máximo de las coordenadas X e y del frustum de la vista en el espacio de la luz. Los dos últimos planos del frustum de vista ortogonal son los planos próximo y lejano. Para encontrar estos planos, los límites de la escena se recortan con los cuatro planos de frustum ligeros conocidos. Los valores Z más pequeños y mayores del límite recién recortado representan el plano próximo y el plano lejano, respectivamente.

El código que realiza esta operación se encuentra en el ejemplo CascadedShadowMaps11. Los ocho puntos que componen el AABB del mundo se transforman en un espacio de luz. La transformación de los puntos en el espacio claro simplifica las pruebas de recorte. Los cuatro planes conocidos del frustum de luz ahora se pueden representar como líneas. El volumen de límite de escenas en el espacio claro se puede representar como seis quadrilaterals. Estos 6 quadrilaterals se pueden convertir en 12 triángulos para el recorte basado en triángulo. Los triángulos se recortan de los planos conocidos del frustum de vista (son líneas horizontales y verticales en X e y en el espacio de la luz). Cuando se encuentra un punto de intersección en X e y, el triángulo 3D se recorta en ese punto. Los valores Z mínimo y máximo de todos los triángulos recortados son el plano próximo y el plano lejano. En el ejemplo CascadedShadowMaps11 se muestra cómo realizar este recorte en la función **ComputeNearAndFar** .

Hay dos técnicas más que se pueden usar para calcular los planos más estrechos y cercanos posibles. Estas técnicas no se muestran en el ejemplo CascadedShadowMaps.

-   Incluso los planos Near y Far más estrechos se pueden calcular intersectando una jerarquía de una escena o objetos individuales en una escena en el frustum ligero. Esto sería cada vez más complejo. Aunque no se muestra en el ejemplo CascadedShadowMaps11, podría ser una técnica válida para algunos iconos.
-   El plano lejano podría calcularse tomando el mínimo de:

    -   La profundidad más grande del frustum de la vista en el espacio de la luz.
    -   La profundidad más grande de la intersección del frustum de la vista y el AABB de la escena.

Este enfoque puede ser problemático cuando se usa con mapas de instantáneas en cascada donde es posible indexar fuera de un frustum de vista. En este caso, es posible que falte geometría en la asignación de instantáneas.

**Figura 15. Planos Near y Far basados en la intersección de los cuatro planos calculados del frustum de luz y la geometría de límite de la escena**

![planos Near y Far basados en la intersección de los cuatro planos calculados del frustum de luz y la geometría de límite de la escena](images/near-far-plane-based-on-intersection-of-four.jpg)

### <a name="moving-the-light-in-texel-sized-increments"></a>Mover la luz en incrementos de Texel-Sized

Un artefacto común en las asignaciones sombra es el efecto de borde Shimmering. A medida que se mueve la cámara, los píxeles a lo largo de los bordes de las sombras iluminan y oscurecen. Esto no se puede apreciar en imágenes fijas, pero es muy perceptible y distrae en tiempo real. En la figura 16 se resalta este problema y la figura 17 muestra cómo deben ser los bordes de la sombra.

El error Shimmering Edge se produce porque la matriz de proyección ligera se está recalculando cada vez que se mueve la cámara. Esto crea diferencias sutiles en las asignaciones de instantáneas generadas. Todos los factores siguientes pueden influir en la matriz creada para enlazar la escena.

-   Tamaño del frustum de vista
-   Orientación del frustum de vista
-   Ubicación de la luz
-   Ubicación de la cámara

Cada vez que esta matriz cambia, los bordes de las sombras pueden cambiar.

**Figura 16. Bordes de sombra Shimmering**

![bordes de sombra Shimmering](images/shimmering-shadow-edges.jpg)

Los píxeles a lo largo del borde de la sombra entran y salen de la sombra cuando la cámara se mueve de izquierda a derecha.

**Figura 17. Sombras sin bordes Shimmering**

![sombras sin bordes Shimmering](images/shadows-without-shimmering-edges.jpg)

Los bordes de sombra permanecen constantes cuando la cámara se mueve de izquierda a derecha.

En el caso de las luces direccionales, la solución a este problema es redondear el valor mínimo o máximo en X e y (que componen los límites de la proyección ortográfica) a incrementos de tamaño en píxeles. Esto puede hacerse con una operación de división, una operación de piso y una multiplicación.


```C++
        vLightCameraOrthographicMin /= vWorldUnitsPerTexel;
        vLightCameraOrthographicMin = XMVectorFloor( vLightCameraOrthographicMin );
        vLightCameraOrthographicMin *= vWorldUnitsPerTexel;
        vLightCameraOrthographicMax /= vWorldUnitsPerTexel;
        vLightCameraOrthographicMax = XMVectorFloor( vLightCameraOrthographicMax );
        vLightCameraOrthographicMax *= vWorldUnitsPerTexel;
```



El valor vWorldUnitsPerTexel se calcula tomando como límite el frustum de la vista y dividiéndolo por el tamaño del búfer.


```C++
        FLOAT fWorldUnitsPerTexel = fCascadeBound /
        (float)m_CopyOfCascadeConfig.m_iBufferSize;
        vWorldUnitsPerTexel = XMVectorSet( fWorldUnitsPerTexel, fWorldUnitsPerTexel,                            0.0f, 0.0f );
```



El límite del tamaño máximo del frustum de la vista da lugar a un ajuste más flexible para la proyección ortográfica.

Es importante tener en cuenta que la textura es 1 píxel más grande en ancho y alto cuando se usa esta técnica. Esto mantiene las coordenadas de sombra de la indización fuera de la instantánea.

### <a name="back-face-and-front-face"></a>Cara posterior y cara frontal

Las asignaciones sombra deben representarse con la selección de datos de retroceso estándar, un proceso que omite la rasterización de objetos que el visor no puede ver y acelera la representación de la escena. Otra opción común es representar las asignaciones de sombra con la selección frontal habilitada, lo que significa que se eliminan los objetos que están orientados al visor. El argumento para esto es que ayuda con la sombra automática, ya que la geometría que conforman la parte posterior de los objetos es ligeramente desplazada. Hay dos problemas con esta idea.

-   Cualquier objeto con geometría de delante o de cara frontal incorrecta provoca artefactos en el mapa de instantáneas. Sin embargo, si la geometría de cara frontal o de cara trasera es incorrecta, se producirán otros problemas, por lo que puede ser seguro suponer que la geometría del anverso y el frontal se realiza correctamente. Es posible que no resulte práctico crear caras inversas para geometría basada en Sprite como follaje.
-   Peter es más probable que se produzcan los huecos de movimiento panorámico y sombra cerca de la base de objetos, como las paredes, porque la disparidad de la profundidad de la sombra es demasiado pequeña.

### <a name="shadow-mapfriendly-geometry"></a>Mapa de sombras: geometría descriptiva

Crear geometría que funcione bien en mapas de sombras permite más flexibilidad a la hora de combatir artefactos como Peter saning y Shadow acne.

Los bordes fuertes son problemáticos para la sombra automática. La disparidad de profundidad cerca de la punta del borde es muy pequeña. Incluso un pequeño desplazamiento puede hacer que los objetos pierdan sus sombras (Figura 18).

**Figura 18. Los bordes nítidos provocan la derivación de artefactos de disparidad de baja profundidad con desplazamientos**

![los bordes nítidos provocan la derivación de artefactos de disparidad de baja profundidad con desplazamientos](images/sharp-edges-cause%20artifacts.jpg)

Los objetos estrechos, como las paredes, deben tener copias de seguridad incluso si nunca están visibles. Esto aumentará la disparidad de profundidad.

También es importante asegurarse de que la dirección a la que está orientada la geometría sea correcta. es decir, el exterior de un objeto debe volverse a enfrente y el interior de un objeto debe estar delante de la cara. Esto es importante para la representación con la selección de la selección de la cara posterior habilitada, así como para combatir los efectos de la tendencia de profundidad.

## <a name="summary"></a>Resumen

Las técnicas descritas en este artículo se pueden usar para aumentar la calidad de las asignaciones de instantáneas estándar. El siguiente paso consiste en examinar técnicas que pueden funcionar bien con las asignaciones de instantáneas estándar. Se recomienda CSMs como técnica superior para combatir el alias de perspectiva. El filtro de porcentaje más cercano o las instantáneas de varianza se pueden usar para suavizar los bordes de la sombra. Para obtener más información, consulte el artículo técnico sobre [mapas de sombras en cascada](/windows/desktop/DxTechArts/cascaded-shadow-maps) .

Donnelly, W., y Lauritzen [,.](https://portal.acm.org/citation.cfm?doid=1111411.1111440) Symposium en gráficos 3D interactivos, procedimientos de 2006 Symposium en gráficos y juegos 3D interactivos. 2006, PP. 161 – 165.

Engel, Woflgang F. sección 4. Mapas de instantáneas en cascada. ShaderX5, *técnicas de representación avanzadas*, Wolfgang F. Engel, Ed. Charles River media, Boston, Massachusetts. 2006. PP. 197:206.

Stamminger, Marc y Drettakis, George. [Mapas de instantáneas de perspectiva](https://portal.acm.org/citation.cfm?id=566616). Conferencia Internacional sobre gráficos de equipos y técnicas interactivas, *procedimientos de la Conferencia 29 anual sobre gráficos informáticos y técnicas interactivas*. 2002, PP 557 – 562.

Wimmer, M., Scherzer, D. y Purgathofer, W. indicadores de [sombra de perspectiva de espacio claro](https://www.cg.tuwien.ac.at/research/vr/lispsm/shadows_egsr2004_revised.pdf). Eurographics Symposium en representación. 2004. Revisado el 10 de junio de 2005. [Technische Universität Wien](https://www.cg.tuwien.ac.at/research/vr/lispsm/).

 

 
