---
title: Trasladar comandos BGN/end
description: IRIS GL usa el paradigma Begin/end, pero tiene una función diferente para cada primitiva de gráficos.
ms.assetid: 4191344b-614a-42d6-8a31-7a708f17371e
keywords:
- Comandos de migración de GL de IRIS, BGN/end
- portabilidad de los comandos de BGN/end de IRIS GL
- trasladar a OpenGL desde los comandos de BGN/end de IRIS GL
- Exportación de OpenGL desde los comandos de BGN/end de IRIS GL
- funciones de dibujo, comandos BGN/end
- comandos BGN/end
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c25118d4e5050ea22d4b18fab596dfb9c92f562e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104419024"
---
# <a name="porting-bgnend-commands"></a>Trasladar comandos BGN/end

IRIS GL usa el paradigma Begin/end, pero tiene una función diferente para cada primitiva de gráficos. Por ejemplo, es probable que use **bgnpolygon** y **endpolygon** para dibujar polígonos y **bgnline** y **EndLine** para dibujar líneas. En OpenGL, se usa la estructura [**glBegin**](glbegin.md)  /  [**glEnd**](glend.md) para ambos. En OpenGL se dibuja la mayoría de los objetos geométricos mediante la inclusión de una serie de funciones que especifican vértices, normales, texturas y colores entre pares de llamadas a **glBegin** y **glEnd** . Por ejemplo:

``` syntax
void glBegin( GLenum mode) ; 
   /* vertex list, colors, normals, textures, materials */ 
void glEnd( void );
```

La función **glBegin** toma un parámetro único que especifica el modo de dibujo y, por tanto, el primitivo. A continuación se muestra un ejemplo de código OpenGL que dibuja un polígono y, a continuación, una línea:

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

Con OpenGL, se dibujan diferentes objetos geométricos mediante la especificación de parámetros diferentes para [**glBegin**](glbegin.md). En la tabla siguiente se enumeran los parámetros de **glBegin** de OpenGL que corresponden a las funciones de contabilidad de iris equivalentes.



| Función de GL de IRIS  | Valor del modo glBegin | Significado                                                                                  |
|-------------------|-----------------------|------------------------------------------------------------------------------------------|
| **bgnpoint**      | puntos de contabilidad \_            | Puntos individuales.                                                                       |
| **bgnline**       | \_franja de línea de contabilidad \_       | Serie de segmentos de línea conectados.                                                       |
| **bgnclosedline** | \_bucle de línea de contabilidad \_        | Serie de segmentos de línea conectados, con un segmento agregado entre los vértices primero y último. |
|                   | líneas de contabilidad \_             | Pares de vértices interpretados como segmentos de línea individuales.                               |
| **bgnpolygon**    | Polígono de GL \_           | Límite de un polígono convexo simple.                                                     |
|                   | triángulos de contabilidad \_         | Las tripas de los vértices se interpretan como triángulos.                                            |
| **bgntmesh**      | \_franja de triángulo de GL \_   | Bandas de triángulos vinculadas.                                                              |
|                   | \_ventilador de triángulo GL \_     | Ventiladores vinculados de triángulos.                                                                |
|                   | \_cuádruples de GL             | Cuadruplican de los vértices interpretados como quadrilaterals.                                    |
| **bgnqstrip**     | \_banda cuádruple de GL \_       | Tiras vinculadas de quadrilaterals.                                                         |



 

Para obtener una explicación detallada de las diferencias entre las mallas de triángulo, las tiras y los ventiladores, consulte [migración de triángulos](porting-triangles.md).

No hay ningún límite en el número de vértices que puede especificar entre un par de glEnd de [**glBegin**](glbegin.md)  /  [](glend.md) .

Además de especificar los vértices dentro de un par **glBegin**  /  **glEnd** , puede especificar una actual, las coordenadas de textura actuales y el color actual. En la tabla siguiente se enumeran los comandos válidos dentro de un par **glBegin**  /  **glEnd** .



| Función de GL de IRIS        | Función OpenGL                                                      | Significado                                          |
|-------------------------|----------------------------------------------------------------------|--------------------------------------------------|
| **V2**, **V3**, **V4**  | [glVertex](glvertex-functions.md)                                   | Establece las coordenadas del vértice.                         |
| **RGBColor**, **cpack** | [glColor](glcolor-functions.md)                                     | Establece el color actual.                              |
| **color**               | [glIndex](glindex-functions.md)                                     | Establece el índice de color actual.                        |
| **n3f**                 | [glNormal](glnormal-functions.md)                                   | Establece coordenadas normales del vector.                  |
|                         | [glEvalCoord](glevalcoord-functions.md)                             | Evalúa las asignaciones de uno y dos dimensiones habilitadas. |
| **callobj**             | [**glCallList**](glcalllist.md), [ **glCallLists**](glcalllists.md) | Ejecuta listas de visualización.                        |
| **T2**                  | [glTexCoord](gltexcoord-functions.md)                               | Establece coordenadas de textura.                        |
|                         | [glEdgeFlag](gledgeflag-functions.md)                               | Controla los bordes del dibujo.                          |
| **lmbind**              | [glMaterial](glmaterial-functions.md)                               | Establece las propiedades del material.                        |



 

> [!Note]
>
> Si usa cualquier función de OpenGL que no sea la que se muestra en la tabla anterior dentro de un par de glEnd de [**glBegin**](glbegin.md)  /  [](glend.md) , obtendrá resultados imprevisibles o, posiblemente, un error.

 

 

 




