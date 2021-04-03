---
title: La canalización de transformación de Direct3D
description: En este artículo se proporciona una explicación técnica para que los desarrolladores de aplicaciones de Direct3D establezcan los parámetros de la canalización de transformación de Direct3D mediante la manipulación directa de las matrices de Direct3D.
ms.assetid: 48ae49f0-1162-c292-4bd4-34da5aadd2df
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2b97a87293a840ccd9641b1418c2005cf73a855
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/04/2021
ms.locfileid: "103913942"
---
# <a name="the-direct3d-transformation-pipeline"></a>La canalización de transformación de Direct3D

En este artículo se proporciona una explicación técnica para que los desarrolladores de aplicaciones de Direct3D establezcan los parámetros de la canalización de transformación de Direct3D mediante la manipulación directa de las matrices de Direct3D.

-   [Información general](#overview)
-   [La canalización de transformación](#the-transformation-pipeline)
-   [Sugerencias de uso](#usage-tips)

## <a name="overview"></a>Información general

Direct3D usa tres transformaciones para cambiar las coordenadas del modelo 3D por coordenadas de píxeles (espacio de pantalla). Estas transformaciones son transformación universal, transformación de vista y transformación de proyección.

Transformación universal controla cómo se transforman las coordenadas del modelo en coordenadas universales. La transformación universal puede incluir traducciones, giros y escalado, pero no se aplica a las luces. Para obtener más información sobre cómo trabajar con las transformaciones del mundo, vea [universal Transform](/windows/desktop/direct3d9/world-transform).

La transformación de vista controla la transición de coordenadas universales a "espacio de la cámara", que determina la posición de la cámara en el mundo. Para obtener un ejemplo de cómo trabajar con transformaciones de vista, vea vista de la [transformación](/windows/desktop/direct3d9/view-transform).

La transformación de proyección cambia la geometría del espacio de la cámara a "espacio de recorte" y aplica la distorsión de la perspectiva. El término "espacio de recorte" se refiere al modo en que la geometría se recorta en el volumen de la vista durante esta transformación. Para obtener un ejemplo de cómo trabajar con transformaciones de proyección, consulte [transformación de proyección](/windows/desktop/direct3d9/projection-transform).

Por último, la geometría en el espacio de recorte se transforma en coordenadas de píxeles (espacio de pantalla). Esta transformación se controla mediante la configuración de la ventanilla.

Los vértices de recorte y transformación deben tener lugar en el espacio homogéneo (simplemente Put, espacio en el que el sistema de coordenadas incluye un cuarto elemento), pero el resultado final de la mayoría de las aplicaciones deben ser coordenadas tridimensionales (3D) no homogéneas definidas en "espacio de pantalla". Esto significa que tanto los vértices de entrada como el volumen de recorte deben traducirse en un espacio homogéneo para realizar el recorte y, a continuación, convertirse en el espacio no homogéneo que se va a mostrar.

Las tres transformaciones de Direct3D (mundo, vista y transformación de proyección) están definidas por matrices de Direct3D. Una matriz de Direct3D es una matriz homogénea 4x4 definida por una estructura [**D3DMATRIX**](/windows/desktop/direct3d9/d3dmatrix) . Aunque las matrices de Direct3D no son objetos estándar, no se representan mediante una interfaz COM, puede crearlas y establecerlas tal y como lo haría con cualquier otro objeto de Direct3D. Para obtener más información sobre las matrices de Direct3D, vea [transformaciones](/windows/desktop/direct3d9/transforms).

## <a name="the-transformation-pipeline"></a>La canalización de transformación

Si el vértice de la coordenada del modelo viene dado por PM = (XM, YM, ZM, 1), las transformaciones que se muestran en la siguiente ilustración se aplican a las coordenadas de la pantalla de proceso PS = (XS, calendario, ZS, WS).

![espacio de modelo para transformación de espacio de pantalla](images/d3dxfrm61.gif)

Estas son las descripciones de las fases que se muestran en la ilustración anterior:

1.  World Matrix Mworld transforma los vértices del espacio del modelo al espacio del mundo. Esta matriz se establece mediante:

    ``` syntax
        d3dDevice->SetTransform (D3DTRANSFORMSTATE_WORLD, matrix address) 
    ```

    La implementación de Direct3D supone que la última columna de esta matriz es (0, 0, 0, 1). No se devuelve ningún error si el usuario especifica una matriz con una última columna diferente, pero la iluminación y la niebla serán incorrectas.

2.  View Matrix MView transforma los vértices del espacio universal en el espacio de la cámara. Esta matriz se establece mediante:

    ``` syntax
        d3dDevice->SetTransform (D3DTRANSFORMSTATE_VIEW, matrix address) 
    ```

    La implementación de Direct3D supone que la última columna de esta matriz es (0, 0, 0, 1). No se devuelve ningún error si el usuario especifica una matriz con una última columna distinta, pero la iluminación y la niebla serán incorrectas.

3.  La matriz de proyección Mproj transforma los vértices del espacio de la cámara en el espacio de proyección. Esta matriz se establece mediante:

    ``` syntax
        d3dDevice->SetTransform (D3DTRANSFORMSTATE_PROJECTION, matrix address) 
    ```

    La última columna de la matriz de proyección debe ser (0, 0, 1, 0) o (0, 0, a, 0) para los efectos de niebla e iluminación correctos. se prefiere el formato (0, 0, 1, 0).

    El volumen de recorte para todos los puntos XP = (XP, es, ZP, WP) en el espacio de proyección se define de la siguiente manera:

    ``` syntax
        -Wp < Xp <= Wp 
        -Wp < Yp <= Wp 
        0 < Zp <= Wp 
    ```

    Se recortarán todos los puntos que no cumplan estas ecuaciones.

    Si un volumen de vista se define como:

    -   Ancho de la ventana de la pantalla en el espacio de la cámara en el plano de recorte cercano
    -   Alto de la ventana de la pantalla sh en el espacio de la cámara en el plano de recorte cercano
    -   Zn: distancia al plano de recorte cercano a lo largo de los ejes Z del espacio de la cámara
    -   ZF: distancia al plano de recorte lejano a lo largo de los ejes Z del espacio de la cámara

    después, una matriz de proyección de perspectiva se podría escribir de la siguiente manera:

    ![Muestra una matriz de proyección de perspectiva.](images/d3dxfrm62.gif)

    donde mij son miembros de Mproj.

    Para la proyección ortogonal que tenemos:

    ![proyección ortogonal](images/d3dxfrm63.gif)

    Direct3D supone que la matriz de proyección de perspectiva tiene el siguiente formato:

    ![matriz de proyección de perspectiva](images/d3dxfrm64.gif)

    Si la matriz de proyección de perspectiva no tiene este formato, habrá algunos artefactos. Por ejemplo, la niebla de tabla no funcionará.

4.  Direct3D permite al usuario cambiar el volumen de la imagen de la siguiente manera:

    ![cambiar el volumen del clip](images/d3dxfrm65.gif)

    Esto se puede volver a escribir de la siguiente manera:

    ![cambiar el volumen de clip reescrito](images/d3dxfrm66.gif)

    donde:

    ``` syntax
        Cx, Cy - dvClipX, dvClipY from D3DVIEWPORT9  
        Cw, Ch - dvClipWidth, dvClipHeight from D3DVIEWPORT9  
        Zmin, Zmax - dvMinZ, dvMaxZ from D3DVIEWPORT9  
    ```

    Esta transformación puede proporcionar mayor precisión y es equivalente a escalar y desplazar el volumen de recorte.

    La matriz de Mclip correspondiente es:

    ![matriz mclip](images/d3dxfrm67.gif)

    Un vértice se transforma por:

    ``` syntax
        dvClipWidth = 2   
        dvClipHeight = 2   
        dvClipX = -1   
        dvClipY = 1   
        dvMinZ = 0   
        dvMaxZ = 1   
    ```

    Si no desea escalar el volumen de clip, puede establecer los parámetros de la ventanilla en valores predeterminados:

    ``` syntax
        (Xc, Yc, Zc, Wc) = (Xp, Yp, Zp, Wp) * Mclip   
    ```

5.  La fase de recorte es opcional si el usuario especifica la \_ marca D3DDP DONOTCLIP en una llamada DrawPrimitive. En este caso, se pueden combinar todas las matrices (incluido MVS).
6.  La matriz de escala de ventanilla MVS escala las coordenadas para que estén dentro de la ventana de ventanilla y voltea el eje Y de arriba a abajo:

    ![matriz de escala de ventanilla MVS](images/d3dxfrm68.gif)

    donde:

    ``` syntax
        dwX, dwY - viewport offsets in pixels from D3DVIEWPORT9 
        dwWidth, dwHeight - viewport width and height in pixels from D3DVIEWPORT9    
    ```

7.  Por último, las coordenadas de pantalla se calculan y se pasan al rasterizador:

    ![coordenadas de pantalla calculadas y pasadas al rasterizador](images/d3dxfrm69.gif)

## <a name="usage-tips"></a>Sugerencias de uso

A continuación se muestran algunas sugerencias sobre cómo usar la canalización de transformación de Direct3D:

-   La última columna del mundo y las matrices de la vista deben ser (0, 0, 0, 1) o la iluminación será incorrecta.
-   Establezca los parámetros de la ventanilla para compilar una matriz de Mclip de identidad, a menos que comprenda exactamente lo que se necesita para.

    ``` syntax
        dvClipWidth = 2 
        dvClipHeight = 2
        dvClipX = -1
        dvClipY = 1
        dvMinZ = 0 
        dvMaxZ = 1
    ```

 

 