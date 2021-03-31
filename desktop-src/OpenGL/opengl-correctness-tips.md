---
title: Sugerencias de corrección de OpenGL
description: Sugerencias de corrección de OpenGL
ms.assetid: 48397fbf-823d-4ea0-adfd-2c639e20e38f
keywords:
- OpenGL, sugerencias de corrección
- OpenGL, procedimientos recomendados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5294d2e989591216ea8cf66aa380933718776f2d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418564"
---
# <a name="opengl-correctness-tips"></a>Sugerencias de corrección de OpenGL

Siga estas instrucciones para crear aplicaciones OpenGL que funcionen de la manera que desee:

-   Suponga que el comportamiento de error en la parte de una implementación de OpenGL puede cambiar en una versión futura de OpenGL. La semántica de errores de OpenGL puede cambiar en futuras revisiones.
-   Utilice la matriz de proyección para contraer todas las geometrías en un solo plano. Si se usa la matriz MODELVIEW, las características OpenGL que funcionan en coordenadas oculares (como la iluminación y los planos de recorte definidos por la aplicación) podrían producir un error.
-   No realice cambios importantes en una sola matriz. Por ejemplo, no Anime una rotación llamando continuamente a [**glRotate**](glrotate.md) con un ángulo incremental. En su lugar, use [**glLoadIdentity**](glloadidentity.md) para inicializar la matriz especificada para cada fotograma y, a continuación, llame a **glRotate** con el ángulo completo deseado para ese marco.
-   Se espera que varios pasen a través de una base de datos de representación para generar los mismos fragmentos de píxeles solo si este comportamiento está garantizado por las reglas de invarianza establecidas para una implementación de OpenGL compatible. De lo contrario, es posible que varias fases generen conjuntos distintos de fragmentos.
-   No espere que se notifiquen los errores mientras se define una lista de visualización. Los comandos de una lista de visualización generan errores solo cuando se ejecuta la lista.
-   Para optimizar el funcionamiento del búfer de profundidad, coloque el plano de frustum cerca del punto de vista como sea posible.
-   Llame a [**glFlush**](glflush.md) para forzar la ejecución de todos los comandos OpenGL anteriores. No cuente en [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) o [**glIsEnabled**](glisenabled.md) para vaciar la secuencia de representación. Los comandos de consulta vacían toda la secuencia que se requiere para devolver datos válidos, pero no necesariamente completa todos los comandos de representación pendientes.
-   Desactive el tramado al representar imágenes pretramadas (por ejemplo, cuando se llama a [**glCopyPixels**](glcopypixels.md) ).
-   Haga uso de la gama completa del búfer de acumulación. Por ejemplo, si acumula cuatro imágenes, escale cada una de ellas a un trimestre a medida que se acumulen.
-   Para obtener una rasterización en dos dimensiones exacta, especifique cuidadosamente la proyección ortográfica y los vértices de las primitivas que se van a Rasterizar. Especifique la proyección ortográfica con coordenadas de enteros, tal como se muestra en el ejemplo siguiente.

    ``` syntax
    gluOrtho2D(0, width, 0, height); 
    ```

    El *ancho* y el *alto* de los parámetros son las dimensiones de la ventanilla. Dada esta matriz de proyección, coloque los vértices del polígono y las posiciones de las imágenes de píxeles en coordenadas enteras para rasterizar de forma predecible. Por ejemplo, [glRecti](glrect-functions.md)(0, 0, 1, 1) rellena de forma confiable el píxel inferior izquierdo de la ventanilla y [glRasterPos2i](glrasterpos-functions.md)(0,0) coloca de forma confiable una imagen no ampliada en el píxel inferior izquierdo de la ventanilla. Sin embargo, los vértices de punto, los vértices de línea y las posiciones de mapa de bits deben colocarse en ubicaciones con un entero medio. Por ejemplo, una línea dibujada desde (*x* (1), 0,5) hasta (*x* (2), 0,5) se representará de forma confiable a lo largo de la fila inferior de píxeles de la ventanilla y un punto dibujado en (0,5, 0,5) rellenará de forma confiable el mismo píxel que glRecti (0, 0, 1, 1).

    Un compromiso óptimo que permite que todos los primitivos se especifiquen en posiciones enteras, al tiempo que se garantiza la rasterización predecible, es convertir *x* e *y* por 0,375, como se muestra en el ejemplo de código siguiente. Este tipo de traducción mantiene los bordes de la imagen de polígonos y píxeles de forma segura fuera de los centros de píxeles, mientras que los vértices de línea se mueven lo suficientemente cerca de los centros de píxeles.

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

-   Evite el uso de coordenadas de *los vértices* negativos y las coordenadas de textura *q* negativas. OpenGL podría no recortar estas coordenadas correctamente y puede hacer errores de interpolación al sombrear los primitivos definidos por tales coordenadas.

 

 




