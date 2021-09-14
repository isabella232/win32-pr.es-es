---
title: Biblioteca DE IRIS GL Sphere
description: OpenGL no admite la biblioteca iris gl sphere. Puede reemplazar las llamadas a la biblioteca sphere por rutinas de cuádricas de la biblioteca GLU. Para obtener más información sobre la biblioteca GLU, vea la Guía de programación de Open GL y la Biblioteca de la utilidad OpenGL.
ms.assetid: 2b7e6a3d-d2d0-4b54-8dff-8c4d6b113007
keywords:
- Porte de IRIS GL, biblioteca sphere
- porte desde IRIS GL, biblioteca sphere
- porte a OpenGL desde IRIS GL, biblioteca sphere
- Porte de OpenGL desde IRIS GL, biblioteca sphere
- funciones de dibujo, biblioteca sphere
- Biblioteca sphere
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 586974c5874aee73121e536cbadca4564a18c250
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127362006"
---
# <a name="the-iris-gl-sphere-library"></a>Biblioteca DE IRIS GL Sphere

OpenGL no admite la biblioteca iris gl sphere. Puede reemplazar las llamadas a la biblioteca sphere por rutinas de cuádricas de la biblioteca GLU. Para obtener más información sobre la biblioteca GLU, vea la Guía de programación de *Open GL* y la Biblioteca de la [utilidad OpenGL](opengl-utility-library.md).

En la tabla siguiente se enumeran las funciones de cuádigos de OpenGL.



| Función OpenGL                                        | Significado                                                          |
|--------------------------------------------------------|------------------------------------------------------------------|
| [**gluNewQuadric**](glunewquadric.md)                 | Crea un nuevo objeto cuádigo.                                    |
| [**gluDeleteQuadric**](gludeletequadric.md)           | Elimina un objeto cuádigo.                                        |
| [*gluQuadricCallback*](gluquadric.md)                 | Asocia una devolución de llamada a un objeto cuádigo para el control de errores. |
| [**gluQuadricNormals**](gluquadricnormals.md)         | Especifica normales: ninguna normal, una por cara o una por vértice.  |
| [**gluQuadricOrientation**](gluquadricorientation.md) | Especifica la dirección de las normales: hacia fuera o hacia dentro.               |
| [**gluQuadricTexture**](gluquadrictexture.md)         | Activa o desactiva la generación de coordenadas de textura.                   |
| [**gluQuadricDrawstyle**](gluquadricdrawstyle.md)     | Especifica el estilo de dibujo: polígonos, líneas, puntos, y así sucesivamente.     |
| [**gluSphere**](glusphere.md)                         | Dibuja una esfera.                                                  |
| [**gluCylinder**](glucylinder.md)                     | Dibuja un cilindro o un cono.                                        |
| [**gluPartialDisk**](glupartialdisk.md)               | Dibuja un arco.                                                    |
| [**gluDisk**](gludisk.md)                             | Dibuja un círculo o disco.                                          |



 

Puede usar un objeto cuádigo para todos los cuádigos que quiera representar de maneras similares. En el ejemplo de código siguiente se usan dos objetos cuádigos para dibujar cuatro cuádigos, dos de ellos con textura.


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



 

 




