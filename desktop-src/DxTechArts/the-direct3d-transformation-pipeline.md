---
title: Canalización de transformación de Direct3D
description: En este artículo se proporciona una explicación técnica para los desarrolladores de aplicaciones de Direct3D sobre cómo establecer los parámetros de la canalización de transformación de Direct3D mediante la manipulación directa de matrices de Direct3D.
ms.assetid: 48ae49f0-1162-c292-4bd4-34da5aadd2df
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6377e3b17cfb4ceb6eda1f4cf59a93c12fd3e6b2f7e43f29f622ed6ee12c271
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118152375"
---
# <a name="the-direct3d-transformation-pipeline"></a>Canalización de transformación de Direct3D

En este artículo se proporciona una explicación técnica para los desarrolladores de aplicaciones de Direct3D sobre cómo establecer los parámetros de la canalización de transformación de Direct3D mediante la manipulación directa de matrices de Direct3D.

-   [Información general](#overview)
-   [Canalización de transformación](#the-transformation-pipeline)
-   [Uso Sugerencias](#usage-tips)

## <a name="overview"></a>Información general

Direct3D usa tres transformaciones para cambiar las coordenadas del modelo 3D a coordenadas de píxeles (espacio de pantalla). Estas transformaciones son la transformación del mundo, la transformación de vista y la transformación de proyección.

La transformación mundial controla cómo se transforman las coordenadas del modelo en coordenadas globales. La transformación mundial puede incluir traducciones, rotaciones y escalas, pero no se aplica a las luces. Para obtener más información sobre cómo trabajar con transformaciones del mundo, vea [World Transform](/windows/desktop/direct3d9/world-transform).

La transformación de vista controla la transición de las coordenadas del mundo al "espacio de la cámara", lo que determina la posición de la cámara en el mundo. Para obtener un ejemplo de cómo trabajar con transformaciones de vista, vea [Ver transformación](/windows/desktop/direct3d9/view-transform).

La transformación de proyección cambia la geometría del espacio de la cámara a "espacio de recorte" y aplica la distorsión de la perspectiva. El término "espacio de recorte" hace referencia a cómo se recorta la geometría al volumen de vista durante esta transformación. Para obtener un ejemplo de cómo trabajar con transformaciones de proyección, vea [Projection Transform](/windows/desktop/direct3d9/projection-transform).

Por último, la geometría del espacio de recorte se transforma en coordenadas de píxeles (espacio de pantalla). Esta transformación se controla mediante la configuración de la ventanilla.

Los vértices de recorte y transformación deben tener lugar en un espacio homogéneo (simplemente, espacio en el que el sistema de coordenadas incluye un cuarto elemento), pero el resultado final para la mayoría de las aplicaciones debe ser coordenadas tridimensionales no homogéneos (3D) definidas en "espacio de pantalla". Esto significa que los vértices de entrada y el volumen de recorte deben traducirse en un espacio homogéneo para realizar el recorte y, a continuación, traducirse de nuevo en un espacio no homogéneo que se va a mostrar.

Las tres transformaciones de Direct3D (transformación de mundo, vista y proyección) se definen mediante matrices de Direct3D. Una matriz Direct3D es una matriz homogéneo de 4x4 definida por una [**estructura D3DMATRIX.**](/windows/desktop/direct3d9/d3dmatrix) Aunque las matrices de Direct3D no son objetos estándar (no se representan mediante una interfaz COM), puede crearlas y establecerlas igual que cualquier otro objeto de Direct3D. Para obtener más información sobre las matrices de Direct3D, vea [Transformaciones.](/windows/desktop/direct3d9/transforms)

## <a name="the-transformation-pipeline"></a>Canalización de transformación

Si pm = (Xm, Ym, Zm, 1) da un vértice en la coordenada del modelo), las transformaciones que se muestran en la ilustración siguiente se aplican a las coordenadas de pantalla de proceso Ps = (Xs, Ys, Zs, Ws).

![model space to screen space transformation](images/d3dxfrm61.gif)

Estas son las descripciones de las fases que se muestran en la ilustración anterior:

1.  La matriz mundial Mworld transforma los vértices del espacio del modelo al espacio mundial. Esta matriz se establece mediante:

    ``` syntax
        d3dDevice->SetTransform (D3DTRANSFORMSTATE_WORLD, matrix address) 
    ```

    La implementación de Direct3D supone que la última columna de esta matriz es (0, 0, 0, 1). No se devuelve ningún error si el usuario especifica una matriz con una última columna diferente, pero la iluminación y la iluminación serán incorrectas.

2.  La matriz de vistas Mview transforma los vértices del espacio mundial al espacio de la cámara. Esta matriz se establece mediante:

    ``` syntax
        d3dDevice->SetTransform (D3DTRANSFORMSTATE_VIEW, matrix address) 
    ```

    La implementación de Direct3D supone que la última columna de esta matriz es (0, 0, 0, 1). No se devuelve ningún error si el usuario especifica una matriz con una última columna diferente, pero la iluminación y la iluminación serán incorrectas.

3.  La matriz de proyección Mproj transforma los vértices del espacio de la cámara al espacio de proyección. Esta matriz se establece mediante:

    ``` syntax
        d3dDevice->SetTransform (D3DTRANSFORMSTATE_PROJECTION, matrix address) 
    ```

    La última columna de la matriz de proyección debe ser (0, 0, 1, 0) o (0, 0, a, 0) para los efectos correctos de iluminación y de color; Se prefiere el formato (0, 0, 1, 0).

    El volumen de recorte para todos los puntos Xp = (Xp, Yp, Zp, Wp) en el espacio de proyección se define como:

    ``` syntax
        -Wp < Xp <= Wp 
        -Wp < Yp <= Wp 
        0 < Zp <= Wp 
    ```

    Todos los puntos que no cumplan estas ecuaciones se recortarán.

    Si un volumen de vista se define como:

    -   Ancho de la ventana de pantalla sw-screen en el espacio de la cámara en un plano de recorte cercano
    -   Altura de la ventana sh-screen en el espacio de la cámara en un plano de recorte cercano
    -   Distancia Zn al plano de recorte cercano a lo largo de los ejes Z en el espacio de la cámara
    -   Distancia hacia el plano de recorte lejano a lo largo de los ejes Z en el espacio de la cámara

    a continuación, se podría escribir una matriz de proyección de perspectiva como se muestra a continuación:

    ![Muestra una matriz de proyección de perspectiva.](images/d3dxfrm62.gif)

    donde Mij es miembro de Mproj.

    Para la proyección ortogonal, tenemos:

    ![proyección ortogonal](images/d3dxfrm63.gif)

    Direct3D supone que la matriz de proyección de perspectiva tiene el formato:

    ![Matriz de proyección de perspectiva](images/d3dxfrm64.gif)

    Si la matriz de proyección de perspectiva no tiene este formato, habrá algunos artefactos. Por ejemplo, table no funcionará.

4.  Direct3D permite al usuario cambiar el volumen de recorte de la manera siguiente:

    ![cambiar el volumen de recorte](images/d3dxfrm65.gif)

    Esto se puede reescribir de la siguiente forma:

    ![cambiar el volumen de recorte reescrito](images/d3dxfrm66.gif)

    donde:

    ``` syntax
        Cx, Cy - dvClipX, dvClipY from D3DVIEWPORT9  
        Cw, Ch - dvClipWidth, dvClipHeight from D3DVIEWPORT9  
        Zmin, Zmax - dvMinZ, dvMaxZ from D3DVIEWPORT9  
    ```

    Esta transformación puede proporcionar una mayor precisión y equivale a escalar y desplazar el volumen de recorte.

    La matriz Mclip correspondiente es:

    ![Matriz de mclip](images/d3dxfrm67.gif)

    Un vértice se transforma mediante:

    ``` syntax
        dvClipWidth = 2   
        dvClipHeight = 2   
        dvClipX = -1   
        dvClipY = 1   
        dvMinZ = 0   
        dvMaxZ = 1   
    ```

    Si no desea escalar el volumen de recorte, puede establecer los parámetros de ventanilla en los valores predeterminados:

    ``` syntax
        (Xc, Yc, Zc, Wc) = (Xp, Yp, Zp, Wp) * Mclip   
    ```

5.  La fase de recorte es opcional si el usuario especifica la marca D3DDP \_ DONOTCLIP en una llamada a DrawPrimitive. En este caso, se pueden combinar todas las matrices (incluidos los mvs).
6.  La matriz de escala de ventanilla Mvs escala las coordenadas para que se encuentran dentro de la ventana de ventanilla y voltea el eje Y de arriba abajo:

    ![mvs de matriz de escala de ventanilla](images/d3dxfrm68.gif)

    donde:

    ``` syntax
        dwX, dwY - viewport offsets in pixels from D3DVIEWPORT9 
        dwWidth, dwHeight - viewport width and height in pixels from D3DVIEWPORT9    
    ```

7.  Por último, las coordenadas de pantalla se calculan y se pasan al rasterizador:

    ![coordenadas de pantalla calculadas y pasadas al rasterizador](images/d3dxfrm69.gif)

## <a name="usage-tips"></a>Uso Sugerencias

Estas son algunas sugerencias para usar la canalización de transformación de Direct3D:

-   La última columna del mundo y las matrices de vistas deben ser (0, 0, 0, 1) o la iluminación será incorrecta.
-   Establezca los parámetros de la ventanilla para crear una matriz de Mclip de identidad, a menos que comprenda exactamente para qué se necesita.

    ``` syntax
        dvClipWidth = 2 
        dvClipHeight = 2
        dvClipX = -1
        dvClipY = 1
        dvMinZ = 0 
        dvMaxZ = 1
    ```

 

 