---
title: Funciones glu
description: Funciones glu
ms.assetid: 8304a291-1a26-42bc-8887-386732980722
keywords:
- Funciones de la biblioteca OpenGL,GLU
- Referencia de OpenGL, funciones de la biblioteca GLU
- Biblioteca glu, funciones
- Utilidad OpenGL (GLU),Functions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fae3ece873f4e1e015861f597c0d51ebfc3436de
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127173573"
---
# <a name="glu-functions"></a>Funciones glu

En esta sección se incluyen páginas de referencia, en orden alfabético, para todas las funciones de la biblioteca de la utilidad OpenGL. Para obtener información general sobre estas funciones, vea [Biblioteca de la utilidad OpenGL](opengl-utility-library.md).



| Función                                                                                           | Descripción                                                                                              |
|----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [**gluBeginCurve**](glubegincurve.md), [ **gluEndCurve**](gluendcurve.md)                         | Delimitar una definición de curva B-Spline lógica no uniforme[(SPLINEBS).](using-nurbs-curves-and-surfaces.md) |
| [**gluBeginPolygon**](glubeginpolygon.md), [ **gluEndPolygon**](gluendpolygon.md)                 | Delimitar una descripción de polígono.                                                                           |
| [**gluBeginSurface**](glubeginsurface.md), [ **gluEndSurface**](gluendsurface.md)                 | Delimitar una definición de superficie DE DSLBS.                                                                      |
| [**gluBeginTrim**](glubegintrim.md), [ **gluEndTrim**](gluendtrim.md)                             | Delimitar una definición de bucle de recorte DE DSLBS.                                                                |
| [**gluBuild1DMipmaps**](glubuild1dmipmaps.md)                                                     | Crea mapas MIP 1D.                                                                                     |
| [**gluBuild2DMipmaps**](glubuild2dmipmaps.md)                                                     | Crea mapas MIP 2D.                                                                                     |
| [**gluCylinder**](glucylinder.md)                                                                 | Dibuja un cilindro.                                                                                        |
| [**gluDeleteNurbsRenderer**](gludeletenurbsrenderer.md)                                           | Destruye un objeto DETEBS.                                                                                 |
| [**gluDeleteQuadric**](gludeletequadric.md)                                                       | Destruye un objeto cuádigo.                                                                               |
| [**gluDeleteTess**](gludeletetess.md)                                                             | Destruye un objeto de teselación.                                                                          |
| [**gluDisk**](gludisk.md)                                                                         | Dibuja un disco.                                                                                            |
| [**gluErrorString**](gluerrorstring.md)                                                           | Genera una cadena de error a partir de un código de error de OpenGL o GLU. La cadena de error es solo ANSI.                |
| [**gluGetNurbsProperty**](glugetnurbsproperty.md)                                                 | Recupera una propiedad DE LABS.                                                                              |
| [**gluGetString**](glugetstring.md)                                                               | Recupera una cadena que describe el número de versión de GLU o las llamadas de extensión DE GLU admitidas.               |
| [**gluGetTessProperty**](glugettessproperty.md)                                                   | Recupera una propiedad de objeto de teselación.                                                                |
| [**gluLoadSamplingMatrices**](gluloadsamplingmatrices.md)                                         | Carga matrices de muestreo y selección de LABS.                                                               |
| [**gluLookAt**](glulookat.md)                                                                     | Define una transformación de visualización.                                                                        |
| [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)                                                 | Crea un objeto DEBS.                                                                                  |
| [**gluNewQuadric**](glunewquadric.md)                                                             | Crea un objeto cuádigo.                                                                                |
| [**gluNewTess**](glunewtess.md)                                                                   | Crea un objeto de teselación.                                                                           |
| [**gluNextContour**](glunextcontour.md)                                                           | Marca el principio de otro contorno.                                                                  |
| [*gluNurbsCallback*](glunurbs.md)                                                                 | Define una devolución de llamada para un objeto DELEBS.                                                                   |
| [**gluNurbsCurve**](glunurbscurve.md)                                                             | Define la forma de una curva DE ASEBS.                                                                      |
| [**gluNurbsProperty**](glunurbsproperty.md)                                                       | Establece una propiedad DE LABS.                                                                                   |
| [**gluNurbsSurface**](glunurbssurface.md)                                                         | Define la forma de una superficie DE LABS.                                                                    |
| [**gluOrtho2D**](gluortho2d.md)                                                                   | Define una matriz de proyección ortográfica 2D.                                                            |
| [**gluPartialDisk**](glupartialdisk.md)                                                           | Dibuja un arco de un disco.                                                                                  |
| [**gluPerspective**](gluperspective.md)                                                           | Configura una matriz de proyección de perspectiva.                                                                 |
| [**gluPickMatrix**](glupickmatrix.md)                                                             | Define una región de selección.                                                                                |
| [**gluProject**](gluproject.md)                                                                   | Mapas coordenadas de objeto a coordenadas de ventana.                                                           |
| [**gluPwlCurve**](glupwlcurve.md)                                                                 | Describe una curva de recorte LINEAR DE TRIMBS por fragmentos.                                                       |
| [*gluQuadricCallback*](gluquadric.md)                                                             | Define una devolución de llamada para un objeto cuádigo.                                                                 |
| [**gluQuadricDrawStyle**](gluquadricdrawstyle.md)                                                 | Especifica el estilo de dibujo deseado para los cuádigos.                                                           |
| [**gluQuadricNormals**](gluquadricnormals.md)                                                     | Especifica qué tipo de normales se van a usar para los cuádigos.                                              |
| [**gluQuadricOrientation**](gluquadricorientation.md)                                             | Especifica la orientación dentro o fuera de los cuádigos.                                                    |
| [**gluQuadricTexture**](gluquadrictexture.md)                                                     | Especifica si se van a texturar los cuádigos.                                                           |
| [**gluScaleImage**](gluscaleimage.md)                                                             | Escala una imagen a un tamaño arbitrario.                                                                    |
| [**gluSphere**](glusphere.md)                                                                     | Dibuja una esfera.                                                                                          |
| [**gluTessBeginContour**](glutessbegincontour.md), [ **gluTessEndContour**](glutessendcontour.md) | Delimitar una descripción de contorno.                                                                           |
| [**gluTessBeginPolygon**](glutessbeginpolygon.md), [ **gluTessEndPolygon**](glutessendpolygon.md) | Delimitar una descripción de polígono.                                                                           |
| [*gluTessCallback*](glutess.md)                                                                   | Define una devolución de llamada para un objeto de teselación.                                                            |
| [**gluTessNormal**](glutessnormal.md)                                                             | Especifica un valor normal para un polígono.                                                                        |
| [**gluTessProperty**](glutessproperty.md)                                                         | Establece la propiedad de un objeto de teselación.                                                              |
| [**gluTessVertex**](glutessvertex.md)                                                             | Especifica un vértice en un polígono.                                                                         |
| [**gluUnProject**](gluunproject.md)                                                               | Mapas coordenadas de ventana a coordenadas de objeto.                                                           |



 

 

 




