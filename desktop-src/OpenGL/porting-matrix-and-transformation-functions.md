---
title: Porting Matrix and Transformation Functions
description: IRIS GL y OpenGL controlan matrices y transformaciones de forma similar.
ms.assetid: 732ba65a-d776-43ea-a605-0f59209c9a46
keywords:
- Porte de IRIS GL, matrices
- porting from IRIS GL,matrices
- porting to OpenGL from IRIS GL,matrices
- Porte de OpenGL desde IRIS GL,matrices
- matrices
- Porte de IRIS GL, transformaciones
- porting from IRIS GL,transformations
- porte a OpenGL desde IRIS GL, transformaciones
- Porte de OpenGL desde IRIS GL, transformaciones
- transformaciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 755e2dc0ed6b53f3a2ee5ef5310369b734a58cba27481b8b478eef63fdfe5722
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118132607"
---
# <a name="porting-matrix-and-transformation-functions"></a>Porting Matrix and Transformation Functions

IRIS GL y OpenGL controlan matrices y transformaciones de forma similar. Pero hay varias diferencias que hay que tener en cuenta al portear código de IRIS GL:

-   En OpenGL siempre está en modo de doble matriz; no hay ningún modo de matriz única.
-   Los ángulos se miden en grados, en lugar de en décimas de grados.
-   Las llamadas a la matriz de proyección, como [**glFrustum**](glfrustum.md) y [**glOrtho,**](glortho.md)ahora se multiplican en la matriz actual, en lugar de cargarse en la matriz actual.
-   La función OpenGL, [**glRotate,**](glrotate.md)es muy diferente de **girar**. Puede girar alrededor de cualquier eje arbitrario, en lugar de limitarse a los ejes x, y y z-. Por ejemplo, puede traducir:

    ```C++
    rotate(200*(i+1), 'z');
    ```

    

    a:

    ```C++
    glRotate(.1*(200*(i+1), 0.0, 0.0, 1.0);
    ```

    

    Al traducir de **girar** a **glRotate,** se cambia a grados desde las décimas de grados y se reemplaza "z" por un vector para el eje Z.

-   OpenGL no tiene ningún equivalente a la **función polarview.** Puede reemplazarlo fácilmente por una traducción y tres rotaciones. Por ejemplo, puede traducir:

    ```C++
    polarview(distance, azimuth, incidence, twist);
     
    ```

    

    a:

    ```C++
    glTranslatef( 0.0, 0.0, -distance); 
    glRotatef( -twist * 10.0, 0.0, 0.0, 1.0); 
    glRotatef( -incidence * 10.0, 1.0, 0.0, 0.0); 
    glRotatef( -azimuth * 10.0, 0.0, 0.0, 1.0);
    ```

    

En la tabla siguiente se enumeran las funciones de matriz OpenGL y sus funciones GL de IRIS equivalentes.



| Función IRIS GL              | Función OpenGL                                                                        | Significado                                                                                                                                                                        |
|-------------------------------|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Mmode**                     | [**glMatrixMode**](glmatrixmode.md)                                                   | Establece el modo de matriz actual.                                                                                                                                                      |
|                               | [**glLoadIdentity**](glloadidentity.md)                                               | Reemplaza la matriz actual por la matriz de identidad.                                                                                                                              |
| **loadmatrix**                | [**glLoadMatrixf**](glloadmatrix.md),[**glLoadMatrixd**](glloadmatrix.md)<br/> | Reemplaza la matriz actual por la matriz especificada.                                                                                                                             |
| **multmatrix**                | [**glMultMatrixf**](glmultmatrix.md),[**glMultMatrixd**](glmultmatrix.md)<br/> | Multiplica previamente la matriz actual con la matriz especificada (tenga en cuenta que **multmatrix** se ha multiplicado previamente).                                                                            |
| **mapw**, **mapw2**           | [**gluUnProject**](gluunproject.md)                                                   | Proyecta coordenadas de espacio mundial en el espacio de objetos (vea [**también gluProject**](gluproject.md)).                                                                                  |
| **Ortho**                     | [**glOrtho**](glortho.md)                                                             | Multiplica la matriz actual por una matriz de proyección ortográfica.                                                                                                                |
| **ortho2**                    | [**gluOrtho2D**](gluortho2d.md)                                                       | Define una matriz de proyección ortográfica bidimensional.                                                                                                                      |
| **Perspectiva**               | [**gluPerspective**](gluperspective.md)                                               | Define una matriz de proyección de perspectiva.                                                                                                                                       |
| **picksize**                  | [**gluPickMatrix**](glupickmatrix.md)                                                 | Define una región de selección.                                                                                                                                                      |
| **popmatrix**                 | [**glPopMatrix**](glpopmatrix.md)                                                     | Muestra la pila de matriz actual, reemplazando la matriz actual por la que está debajo.                                                                                                 |
| **pushmatrix**                | [**glPushMatrix**](glpushmatrix.md)                                                   | Inserta la pila de la matriz actual en una, duplicando la matriz actual.                                                                                                       |
| **rotate**,**rot**<br/> | [**glRotated**](glrotate.md),[**glRotatef**](glrotate.md)<br/>                 | Gira el sistema de coordenadas actual según el ángulo especificado sobre el vector desde el origen hasta el punto dado. Tenga en **cuenta que** la rotación gira solo sobre los ejes X, Y y Z. |
| **scale**                     | [**glScaled**](glscale.md),[**glScalef**](glscale.md)<br/>                     | Multiplica la matriz actual por una matriz de escalado.                                                                                                                                 |
| **Traducir**                 | [**glTranslatef**](gltranslate.md),[**glTranslated**](gltranslate.md)<br/>     | Mueve el origen del sistema de coordenadas al punto especificado, multiplicando la matriz actual por una matriz de traducción.                                                              |
| **Ventana**                    | [**glFrustum**](glfrustum.md)                                                         | Dadas las coordenadas para los planos de recorte, multiplica la matriz actual por una matriz de perspectiva.                                                                                  |



 

OpenGL tiene tres modos de matriz, que se establecen [**con glMatrixMode**](glmatrixmode.md). En la tabla siguiente se enumeran los modos disponibles como parámetros para **glMatrixMode**.



| Modo de matriz IRIS GL | Modo OpenGL    | Significado                                  | Profundidad de pila mínima |
|---------------------|----------------|------------------------------------------|-----------------|
| **MTEXTURE**        | TEXTURA \_ GL    | Funciona en la pila de la matriz de textura.    | 2               |
| **MVIEWING**        | GL \_ MODELVIEW  | Funciona en la pila de la matriz de vistas del modelo. | 32              |
| **MPROJECTION**     | PROYECCIÓN \_ DE GL | Funciona en la pila de la matriz de proyección. | 2               |



 

 

 





