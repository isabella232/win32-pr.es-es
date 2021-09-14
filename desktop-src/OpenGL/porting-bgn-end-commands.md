---
title: Porting bgn/end Commands
description: IRIS GL usa el paradigma de inicio y fin, pero tiene una función diferente para cada primitivo gráfico.
ms.assetid: 4191344b-614a-42d6-8a31-7a708f17371e
keywords:
- Porte de IRIS GL, comandos bgn/end
- porting from IRIS GL,bgn/end commands (porting from IRIS GL,bgn/end commands)
- porting to OpenGL from IRIS GL,bgn/end commands (porting to OpenGL from IRIS GL,bgn/end commands)
- Porte de OpenGL desde IRIS GL, comandos bgn/end
- funciones de dibujo, comandos bgn/end
- comandos bgn/end
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c25118d4e5050ea22d4b18fab596dfb9c92f562e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074023"
---
# <a name="porting-bgnend-commands"></a>Porting bgn/end Commands

IRIS GL usa el paradigma de inicio y fin, pero tiene una función diferente para cada primitivo gráfico. Por ejemplo, probablemente use **bgnpolygon** y **endpolygon** para dibujar polígonos, y **bgnline** y **endline** para dibujar líneas. En OpenGL, se usa la [**estructura glBegin**](glbegin.md)  /  [**glEnd**](glend.md) para ambos. En OpenGL se dibujan la mayoría de los objetos geométricos mediante la especificación de una serie de funciones que especifican vértices, normales, texturas y colores entre pares de **llamadas glBegin** y **glEnd.** Por ejemplo:

``` syntax
void glBegin( GLenum mode) ; 
   /* vertex list, colors, normals, textures, materials */ 
void glEnd( void );
```

La **función glBegin** toma un único parámetro que especifica el modo de dibujo y, por tanto, el primitivo. Este es un ejemplo de código OpenGL que dibuja un polígono y, a continuación, una línea:

``` syntax
glBegin( GL_POLYGON ) ; 
   glVertex2f(20.0, 10.0); 
   glVertex2f(10.0, 30.0); 
   glVertex2f(20.0, 50.0); 
   glVertex2f(40.0, 50.0); 
   glVertex2f(50.0, 30.0); 
   glVertex2f(40.0, 10.0); 
glEnd(); 
glBegin( GL_LINES ) ; 
   glVertex2i(100,100); 
   glVertex2i(500,500); 
glEnd();
```

Con OpenGL, puede dibujar diferentes objetos geométricos especificando parámetros diferentes para [**glBegin**](glbegin.md). En la tabla siguiente se enumeran los parámetros **glBegin** de OpenGL que corresponden a funciones GL de IRIS equivalentes.



| Función GL de IRIS  | Valor del modo glBegin | Significado                                                                                  |
|-------------------|-----------------------|------------------------------------------------------------------------------------------|
| **bgnpoint**      | PUNTOS \_ GL            | Puntos individuales.                                                                       |
| **bgnline**       | FRANJA \_ DE LÍNEA \_ GL       | Serie de segmentos de línea conectados.                                                       |
| **bgnclosedline** | BUCLE \_ DE LÍNEA \_ GL        | Serie de segmentos de línea conectados, con un segmento agregado entre el primer y el último vértice. |
|                   | LÍNEAS \_ GL             | Pares de vértices interpretados como segmentos de línea individuales.                               |
| **bgnpolygon**    | POLÍGONO \_ GL           | Límite de un polígono convexa simple.                                                     |
|                   | TRIÁNGULOS \_ GL         | Triples de vértices interpretados como triángulos.                                            |
| **bgntmesh**      | FRANJA \_ DE TRIÁNGULO \_ GL   | Franjas vinculadas de triángulos.                                                              |
|                   | GL \_ TRIANGLE \_ FAN     | Ventiladores vinculados de triángulos.                                                                |
|                   | GL \_ QUADS             | Triángulos de vértices interpretados como cuadríteros.                                    |
| **bgnqstrip**     | GL \_ QUAD \_ STRIP       | Franjas vinculadas de cuadriláteros.                                                         |



 

Para obtener una explicación detallada de las diferencias entre las mallas de triángulos, las bandas y los ventiladores, vea [Porting Triangles](porting-triangles.md).

No hay ningún límite en el número de vértices que puede especificar entre un [**par glBegin**](glbegin.md)  /  [**glEnd.**](glend.md)

Además de especificar vértices dentro de un par **glBegin**  /  **glEnd,** puede especificar las coordenadas de textura actuales normales y actuales, así como un color actual. En la tabla siguiente se enumeran los comandos válidos dentro de **un par glBegin**  /  **glEnd.**



| Función GL de IRIS        | Función OpenGL                                                      | Significado                                          |
|-------------------------|----------------------------------------------------------------------|--------------------------------------------------|
| **v2,** **v3,** **v4**  | [glVertex](glvertex-functions.md)                                   | Establece coordenadas de vértice.                         |
| **RGBcolor**, **cpack** | [glColor](glcolor-functions.md)                                     | Establece el color actual.                              |
| **color**               | [glIndex](glindex-functions.md)                                     | Establece el índice de color actual.                        |
| **n3f**                 | [glNormal](glnormal-functions.md)                                   | Establece coordenadas vectoriales normales.                  |
|                         | [glEvalCoord](glevalcoord-functions.md)                             | Evalúa los mapas unidimensionales y bidimensionales habilitados. |
| **callobj**             | [**glCallList**](glcalllist.md), [ **glCallLists**](glcalllists.md) | Ejecuta listas de visualización.                        |
| **t2**                  | [glTexCoord](gltexcoord-functions.md)                               | Establece coordenadas de textura.                        |
|                         | [glEdgeFlag](gledgeflag-functions.md)                               | Controla los bordes de dibujo.                          |
| **lmbind**              | [glMaterial](glmaterial-functions.md)                               | Establece las propiedades de material.                        |



 

> [!Note]
>
> Si usa cualquier función OpenGL que no sea la enumerada en la tabla anterior dentro de un par [**glBegin**](glbegin.md)glEnd, se obtienen resultados impredecibles  /  [](glend.md) o, posiblemente, un error.

 

 

 




