---
title: Portabilidad de funciones de transformación y de matriz
description: La administración de las matrices y las transformaciones de IRIS GL y OpenGL es similar.
ms.assetid: 732ba65a-d776-43ea-a605-0f59209c9a46
keywords:
- Puerto de GL de IRIS, matrices
- portabilidad de IRIS GL, matrices
- trasladar a OpenGL desde IRIS GL, matrices
- Exportación de OpenGL desde IRIS GL, matrices
- matrices
- Migración de la contabilidad de IRIS, transformaciones
- portabilidad de IRIS GL, transformaciones
- trasladar a OpenGL desde IRIS GL, transformaciones
- Exportación de OpenGL desde IRIS GL, transformaciones
- transformaciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1c6219640085370202b8dbebad9a2e9d4992b4f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357357"
---
# <a name="porting-matrix-and-transformation-functions"></a>Portabilidad de funciones de transformación y de matriz

La administración de las matrices y las transformaciones de IRIS GL y OpenGL es similar. Pero hay varias diferencias que hay que tener en cuenta al migrar código de IRIS GL:

-   En OpenGL siempre está en modo de doble matriz; no hay ningún modo de matriz única.
-   Los ángulos se miden en grados, en lugar de en las décimas de grados.
-   Las llamadas de la matriz de proyección, como [**glFrustum**](glfrustum.md) y [**glOrtho**](glortho.md), ahora se multiplican en la matriz actual, en lugar de cargarse en la matriz actual.
-   La función de OpenGL, [**glRotate**](glrotate.md), es muy diferente de la **rotación**. Puede girar alrededor de cualquier eje arbitrario, en lugar de limitarse a los ejes x, y y z. Por ejemplo, puede traducir:

    ```C++
    rotate(200*(i+1), 'z');
    ```

    

    a:

    ```C++
    glRotate(.1*(200*(i+1), 0.0, 0.0, 1.0);
    ```

    

    Al traducir de **rotar** a **glRotate** , cambie a grados desde las décimas de grado y reemplace ' z ' con un vector para el eje z.

-   OpenGL no tiene equivalente a la función **polarview** . Puede reemplazarlo fácilmente con una traducción y tres giros. Por ejemplo, puede traducir:

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

    

En la tabla siguiente se enumeran las funciones de matriz de OpenGL y sus funciones de contabilidad de IRIS equivalentes.



| Función de GL de IRIS              | Función OpenGL                                                                        | Significado                                                                                                                                                                        |
|-------------------------------|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **mmode**                     | [**glMatrixMode**](glmatrixmode.md)                                                   | Establece el modo de matriz actual.                                                                                                                                                      |
|                               | [**glLoadIdentity**](glloadidentity.md)                                               | Reemplaza la matriz actual por la matriz de identidad.                                                                                                                              |
| **loadmatrix**                | [**glLoadMatrixf**](glloadmatrix.md),[**glLoadMatrixd**](glloadmatrix.md)<br/> | Reemplaza la matriz actual con la matriz especificada.                                                                                                                             |
| **multmatrix**                | [**glMultMatrixf**](glmultmatrix.md),[**glMultMatrixd**](glmultmatrix.md)<br/> | Post: multiplica la matriz actual con la matriz especificada (tenga en cuenta que **multmatrix** se multiplica previamente).                                                                            |
| **mapw**, **mapw2**           | [**gluUnProject**](gluunproject.md)                                                   | Proyecta las coordenadas de espacio mundial en el espacio de objeto (vea también [**gluProject**](gluproject.md)).                                                                                  |
| **ortho**                     | [**glOrtho**](glortho.md)                                                             | Multiplica la matriz actual por una matriz de proyección ortográfica.                                                                                                                |
| **ortho2**                    | [**gluOrtho2D**](gluortho2d.md)                                                       | Define una matriz de proyección ortográfica bidimensional.                                                                                                                      |
| **vista**               | [**gluPerspective**](gluperspective.md)                                               | Define una matriz de proyección de perspectiva.                                                                                                                                       |
| **picksize**                  | [**gluPickMatrix**](glupickmatrix.md)                                                 | Define una región de picking.                                                                                                                                                      |
| **popmatrix**                 | [**glPopMatrix**](glpopmatrix.md)                                                     | Extrae la pila de matriz actual, reemplazando la matriz actual por la que se encuentra debajo de ella.                                                                                                 |
| **pushmatrix**                | [**glPushMatrix**](glpushmatrix.md)                                                   | Empuja la pila actual de la matriz hacia abajo en uno, duplicando la matriz actual.                                                                                                       |
| **rotar**,**Rot**<br/> | [**glRotated**](glrotate.md),[**glRotatef**](glrotate.md)<br/>                 | Gira el sistema de coordenadas actual por el ángulo especificado sobre el vector desde el origen hasta el punto especificado. Tenga en cuenta que **girar** gira solo sobre los ejes x, y y z. |
| **scale**                     | [**glScaled**](glscale.md),[**glScalef**](glscale.md)<br/>                     | Multiplica la matriz actual por una matriz de escala.                                                                                                                                 |
| **Traducir**                 | [**glTranslatef**](gltranslate.md),[**glTranslated**](gltranslate.md)<br/>     | Mueve el origen del sistema de coordenadas al punto especificado, multiplicando la matriz actual por una matriz de traslación.                                                              |
| **ventana**                    | [**glFrustum**](glfrustum.md)                                                         | Las coordenadas especificadas para los planos de recorte, multiplican la matriz actual por una matriz de perspectiva.                                                                                  |



 

OpenGL tiene tres modos de matriz, que se establecen con [**glMatrixMode**](glmatrixmode.md). En la tabla siguiente se enumeran los modos disponibles como parámetros para **glMatrixMode**.



| Modo de matriz de contabilidad de IRIS | Modo OpenGL    | Significado                                  | Profundidad de pila mínima |
|---------------------|----------------|------------------------------------------|-----------------|
| **MTEXTURE**        | \_textura GL    | Opera en la pila de la matriz de textura.    | 2               |
| **MVIEWING**        | GL \_ MODELVIEW  | Funciona en la pila de matrices de la vista de modelo. | 32              |
| **MPROJECTION**     | \_proyección GL | Opera en la pila de la matriz de proyección. | 2               |



 

 

 





