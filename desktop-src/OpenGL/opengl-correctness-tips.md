---
title: Corrección de OpenGL Sugerencias
description: Corrección de OpenGL Sugerencias
ms.assetid: 48397fbf-823d-4ea0-adfd-2c639e20e38f
keywords:
- OpenGL, sugerencias de corrección
- OpenGL, procedimientos recomendados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5294d2e989591216ea8cf66aa380933718776f2d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127265628"
---
# <a name="opengl-correctness-tips"></a>Corrección de OpenGL Sugerencias

Siga estas instrucciones para crear aplicaciones OpenGL que se realicen según lo previsto:

-   Supongamos que el comportamiento de error por parte de una implementación de OpenGL puede cambiar en una versión futura de OpenGL. La semántica de errores de OpenGL puede cambiar en futuras revisiones.
-   Use la matriz de proyección para contraer toda la geometría en un solo plano. Si se usa la matriz modelview, pueden producirse errores en las características de OpenGL que funcionan en coordenadas de los ojos (como la iluminación y los planos de recorte definidos por la aplicación).
-   No realice cambios exhaustivos en una sola matriz. Por ejemplo, no animar una rotación llamando continuamente [**a glRotate**](glrotate.md) con un ángulo incremental. En su lugar, use [**glLoadIdentity**](glloadidentity.md) para inicializar la matriz dada para cada fotograma y, a continuación, llame **a glRotate** con el ángulo completo deseado para ese fotograma.
-   Espere que varios pases a través de una base de datos de representación generen los mismos fragmentos de píxeles solo si este comportamiento está garantizado por las reglas de invariables establecidas para una implementación de OpenGL compatible. De lo contrario, varios pases podrían generar distintos conjuntos de fragmentos.
-   No espere que se notimenten errores mientras se define una lista de visualización. Los comandos de una lista de visualización generan errores solo cuando se ejecuta la lista.
-   Para optimizar el funcionamiento del búfer de profundidad, coloque el plano de referencia cercano lo más lejos posible del punto de vista.
-   Llame [**a glFlush para**](glflush.md) forzar la ejecución de todos los comandos de OpenGL anteriores. No cuente con [**glGet o**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) [**glIsEnabled para**](glisenabled.md) vaciar el flujo de representación. Los comandos de consulta vacían la mayor parte de la secuencia necesaria para devolver datos válidos, pero no necesariamente completan todos los comandos de representación pendientes.
-   Desactive el dithering al representar imágenes previamente vinculadas (por ejemplo, cuando se llama a [**glCopyPixels).**](glcopypixels.md)
-   Use el intervalo completo del búfer de acumulación. Por ejemplo, si acumula cuatro imágenes, escale cada una en un trimestre a medida que se acumule.
-   Para obtener la rasterización bidimensional exacta, especifique cuidadosamente la proyección ortográfica y los vértices de las primitivas que se van a rasterizar. Especifique la proyección ortográfica con coordenadas de enteros, como se muestra en el ejemplo siguiente.

    ``` syntax
    gluOrtho2D(0, width, 0, height); 
    ```

    El ancho *y alto* de *los parámetros* son las dimensiones de la ventanilla. Dada esta matriz de proyección, coloque los vértices de polígono y las posiciones de imagen de píxeles en coordenadas enteras para rasterizar de forma predecible. Por ejemplo, [glRecti](glrect-functions.md)( 0, 0, 1, 1 ) rellena de forma confiable el píxel inferior izquierdo de la ventanilla y [glRasterPos2i](glrasterpos-functions.md)( 0, 0 ) coloca de forma confiable una imagen sin aplanar en el píxel inferior izquierdo de la ventanilla. Sin embargo, los vértices de punto, los vértices de línea y las posiciones de mapa de bits deben colocarse en ubicaciones de medio entero. Por ejemplo, una línea dibujada de (*x* (1), 0,5) a (*x* (2) , 0,5) se representará de forma confiable a lo largo de la fila inferior de píxeles de la ventanilla y un punto dibujado en (0,5, 0,5) rellenará de forma confiable el mismo píxel que glRecti( 0, 0, 1, 1 ).

    Un riesgo óptimo que permite especificar todas las primitivas en posiciones de enteros, a la vez que se garantiza una rasterización predecible, es traducir *x* e *y* por 0,375, como se muestra en el ejemplo de código siguiente. Este tipo de traducción mantiene los bordes de imagen de píxeles y polígonos de forma segura lejos de los centros de píxeles, mientras mueve los vértices de línea lo suficientemente cerca de los centros de píxeles.

    ``` syntax
    glViewport(0, 0, width, height);
    glMatrixMode(GL_PROJECTION);
    glLoadIdentity( );
    gluOrtho2D(0, width, 0, height);
    glMatrixMode(GL_MODELVIEW);
    glLoadIdentity( );
    glTranslatef(0.375, 0.375, 0.0);
    /* render all primitives at integer positions */
    ```

-   Evite usar coordenadas *de vértice w negativas* y coordenadas de *textura q* negativas. Es posible que OpenGL no recorte estas coordenadas correctamente y pueda realizar errores de interpolación al sombrear primitivas definidas por dichas coordenadas.

 

 




