---
title: Funciones de GLU
description: Funciones de GLU
ms.assetid: 8304a291-1a26-42bc-8887-386732980722
keywords:
- Funciones de la biblioteca OpenGL y GLU
- Referencia de OpenGL, funciones de la biblioteca GLU
- Biblioteca GLU, funciones
- Utilidad OpenGL (GLU), funciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fae3ece873f4e1e015861f597c0d51ebfc3436de
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418571"
---
# <a name="glu-functions"></a>Funciones de GLU

En esta sección se incluyen páginas de referencia, en orden alfabético, para todas las funciones de la biblioteca de utilidades de OpenGL. Para obtener información general acerca de estas funciones, vea [biblioteca de utilidades OpenGL](opengl-utility-library.md).



| Función                                                                                           | Descripción                                                                                              |
|----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [**gluBeginCurve**](glubegincurve.md), [ **gluEndCurve**](gluendcurve.md)                         | Delimita una definición de curva B-spline racional ([NURBS](using-nurbs-curves-and-surfaces.md)) no uniforme. |
| [**gluBeginPolygon**](glubeginpolygon.md), [ **gluEndPolygon**](gluendpolygon.md)                 | Delimite una descripción de polígono.                                                                           |
| [**gluBeginSurface**](glubeginsurface.md), [ **gluEndSurface**](gluendsurface.md)                 | Delimite una definición de superficie de NURBS.                                                                      |
| [**gluBeginTrim**](glubegintrim.md), [ **gluEndTrim**](gluendtrim.md)                             | Delimite una definición de bucle de recorte de NURBS.                                                                |
| [**gluBuild1DMipmaps**](glubuild1dmipmaps.md)                                                     | Crea mapas de bits 1D.                                                                                     |
| [**gluBuild2DMipmaps**](glubuild2dmipmaps.md)                                                     | Crea mapas de bits 2D.                                                                                     |
| [**gluCylinder**](glucylinder.md)                                                                 | Dibuja un cilindro.                                                                                        |
| [**gluDeleteNurbsRenderer**](gludeletenurbsrenderer.md)                                           | Destruye un objeto NURBS.                                                                                 |
| [**gluDeleteQuadric**](gludeletequadric.md)                                                       | Destruye un objeto quadric.                                                                               |
| [**gluDeleteTess**](gludeletetess.md)                                                             | Destruye un objeto de teselación.                                                                          |
| [**gluDisk**](gludisk.md)                                                                         | Dibuja un disco.                                                                                            |
| [**gluErrorString**](gluerrorstring.md)                                                           | Genera una cadena de error a partir de un código de error OpenGL o GLU. La cadena de error es sólo ANSI.                |
| [**gluGetNurbsProperty**](glugetnurbsproperty.md)                                                 | Recupera una propiedad NURBS.                                                                              |
| [**gluGetString**](glugetstring.md)                                                               | Recupera una cadena que describe el número de versión de GLU o las llamadas de extensión GLU admitidas.               |
| [**gluGetTessProperty**](glugettessproperty.md)                                                   | Recupera una propiedad de objeto de teselación.                                                                |
| [**gluLoadSamplingMatrices**](gluloadsamplingmatrices.md)                                         | Carga el muestreo de NURBS y matrices de selección.                                                               |
| [**gluLookAt**](glulookat.md)                                                                     | Define una transformación de visualización.                                                                        |
| [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)                                                 | Crea un objeto NURBS.                                                                                  |
| [**gluNewQuadric**](glunewquadric.md)                                                             | Crea un objeto quadric.                                                                                |
| [**gluNewTess**](glunewtess.md)                                                                   | Crea un objeto de teselación.                                                                           |
| [**gluNextContour**](glunextcontour.md)                                                           | Marca el principio de otro contorno.                                                                  |
| [*gluNurbsCallback*](glunurbs.md)                                                                 | Define una devolución de llamada para un objeto NURBS.                                                                   |
| [**gluNurbsCurve**](glunurbscurve.md)                                                             | Define la forma de una curva NURBS.                                                                      |
| [**gluNurbsProperty**](glunurbsproperty.md)                                                       | Establece una propiedad de NURBS.                                                                                   |
| [**gluNurbsSurface**](glunurbssurface.md)                                                         | Define la forma de una superficie NURBS.                                                                    |
| [**gluOrtho2D**](gluortho2d.md)                                                                   | Define una matriz de proyección ortográfica 2D.                                                            |
| [**gluPartialDisk**](glupartialdisk.md)                                                           | Dibuja un arco de un disco.                                                                                  |
| [**gluPerspective**](gluperspective.md)                                                           | Configura una matriz de proyección en perspectiva.                                                                 |
| [**gluPickMatrix**](glupickmatrix.md)                                                             | Define una región de picking.                                                                                |
| [**gluProject**](gluproject.md)                                                                   | Asigna coordenadas de objeto a las coordenadas de la ventana.                                                           |
| [**gluPwlCurve**](glupwlcurve.md)                                                                 | Describe una curva de recorte de NURBS lineal a trozos.                                                       |
| [*gluQuadricCallback*](gluquadric.md)                                                             | Define una devolución de llamada para un objeto quadric.                                                                 |
| [**gluQuadricDrawStyle**](gluquadricdrawstyle.md)                                                 | Especifica el estilo de dibujo deseado para Quadrics.                                                           |
| [**gluQuadricNormals**](gluquadricnormals.md)                                                     | Especifica el tipo de normalización que se va a usar para Quadrics.                                              |
| [**gluQuadricOrientation**](gluquadricorientation.md)                                             | Especifica la orientación interior o externa para Quadrics.                                                    |
| [**gluQuadricTexture**](gluquadrictexture.md)                                                     | Especifica si se va a aplicar textura a Quadrics.                                                           |
| [**gluScaleImage**](gluscaleimage.md)                                                             | Escala una imagen a un tamaño arbitrario.                                                                    |
| [**gluSphere**](glusphere.md)                                                                     | Dibuja una esfera.                                                                                          |
| [**gluTessBeginContour**](glutessbegincontour.md), [ **gluTessEndContour**](glutessendcontour.md) | Delimite una descripción de perfil.                                                                           |
| [**gluTessBeginPolygon**](glutessbeginpolygon.md), [ **gluTessEndPolygon**](glutessendpolygon.md) | Delimite una descripción de polígono.                                                                           |
| [*gluTessCallback*](glutess.md)                                                                   | Define una devolución de llamada para un objeto de teselación.                                                            |
| [**gluTessNormal**](glutessnormal.md)                                                             | Especifica una normal para un polígono.                                                                        |
| [**gluTessProperty**](glutessproperty.md)                                                         | Establece la propiedad de un objeto de teselación.                                                              |
| [**gluTessVertex**](glutessvertex.md)                                                             | Especifica un vértice en un polígono.                                                                         |
| [**gluUnProject**](gluunproject.md)                                                               | Asigna coordenadas de ventana a coordenadas de objeto.                                                           |



 

 

 




