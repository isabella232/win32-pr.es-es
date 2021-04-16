---
title: Biblioteca de Sphere GL de IRIS
description: OpenGL no es compatible con la biblioteca de esfera GL de IRIS. Puede reemplazar las llamadas de la biblioteca de esferas por las rutinas de Quadrics de la biblioteca de GLU. Para obtener más información acerca de la biblioteca GLU, vea la guía de programación de Open GL y la biblioteca de utilidades OpenGL.
ms.assetid: 2b7e6a3d-d2d0-4b54-8dff-8c4d6b113007
keywords:
- Migración de la contabilidad de IRIS, biblioteca de esferas
- portabilidad de IRIS GL, biblioteca de esferas
- trasladar a OpenGL desde IRIS GL, biblioteca de esferas
- Exportación de OpenGL desde IRIS GL, biblioteca de esferas
- funciones de dibujo, biblioteca Sphere
- Biblioteca de esferas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 586974c5874aee73121e536cbadca4564a18c250
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357263"
---
# <a name="the-iris-gl-sphere-library"></a>Biblioteca de Sphere GL de IRIS

OpenGL no es compatible con la biblioteca de esfera GL de IRIS. Puede reemplazar las llamadas de la biblioteca de esferas por las rutinas de Quadrics de la biblioteca de GLU. Para obtener más información acerca de la biblioteca GLU, vea la *Guía de programación de Open GL* y la [biblioteca de utilidades OpenGL](opengl-utility-library.md).

En la tabla siguiente se enumeran las funciones de Quadrics de OpenGL.



| Función OpenGL                                        | Significado                                                          |
|--------------------------------------------------------|------------------------------------------------------------------|
| [**gluNewQuadric**](glunewquadric.md)                 | Crea un nuevo objeto quadric.                                    |
| [**gluDeleteQuadric**](gludeletequadric.md)           | Elimina un objeto quadric.                                        |
| [*gluQuadricCallback*](gluquadric.md)                 | Asocia una devolución de llamada a un objeto quadric para el control de errores. |
| [**gluQuadricNormals**](gluquadricnormals.md)         | Especifica las normales: no hay normal, una por cara o una por vértice.  |
| [**gluQuadricOrientation**](gluquadricorientation.md) | Especifica la dirección de las normales: hacia fuera o hacia adentro.               |
| [**gluQuadricTexture**](gluquadrictexture.md)         | Activa o desactiva la generación de coordenadas de textura.                   |
| [**gluQuadricDrawstyle**](gluquadricdrawstyle.md)     | Especifica el estilo de dibujo: polígonos, líneas, puntos, etc.     |
| [**gluSphere**](glusphere.md)                         | Dibuja una esfera.                                                  |
| [**gluCylinder**](glucylinder.md)                     | Dibuja un cilindro o un cono.                                        |
| [**gluPartialDisk**](glupartialdisk.md)               | Dibuja un arco.                                                    |
| [**gluDisk**](gludisk.md)                             | Dibuja un círculo o un disco.                                          |



 

Puede usar un objeto quadric para todos los Quadrics que quiera representar de maneras similares. En el ejemplo de código siguiente se usan dos objetos quadric para dibujar cuatro Quadrics, dos de ellos con textura.


```C++
GLUquadricObj    *texturedQuad, *plainQuad; 
 
texturedQuad = gluNewQuadric(void); 
gluQuadricTexture(texturedQuad, GL_TRUE); 
gluQuadricOrientation(texturedQuad, GLU_OUTSIDE); 
gluQuadricDrawStyle(texturedQuad, GLU_FILL); 
 
plainQuad = gluNewQuadric(void); 
gluQuadricDrawStyle(plainQuad, GLU_LINE); 
 
glColor3f (1.0, 1.0, 1.0); 
 
gluSphere(texturedQuad, 5.0, 20, 20); 
glTranslatef(10.0, 10.0, 0.0); 
gluCylinder(texturedQuad, 2.5, 5, 5, 10, 10); 
glTranslatef(10.0, 10.0, 0.0); 
gluDisk(plainQuad, 2.0, 5.0, 10, 10); 
glTranslatef(10.0, 10.0, 0.0); 
gluSphere(plainQuad, 5.0, 20, 20);
```



 

 




