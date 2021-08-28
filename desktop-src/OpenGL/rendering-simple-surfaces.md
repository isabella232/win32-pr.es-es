---
title: Representación de superficies simples
description: La biblioteca GLU incluye un conjunto de funciones para dibujar varias superficies simples (esferas, cilindros, discos y partes de discos) en una variedad de estilos y orientaciones. Estas funciones se describen en detalle en el Manual de referencia de OpenGL.
ms.assetid: 403bdf8d-de4c-49e2-87d0-11109061b4c2
keywords:
- Utilidad OpenGL (GLU),superficies simples
- GLU (utilidad OpenGL),superficies simples
- Superficies simples OpenGL
- Utilidad OpenGL (GLU),spheres
- GLU (utilidad OpenGL),spheres
- Spheres OpenGL
- Utilidad OpenGL (GLU),cilindros
- GLU (utilidad OpenGL), cilindros
- cilindros OpenGL
- Utilidad OpenGL (GLU),disks
- GLU (utilidad OpenGL),disks
- discos OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4010a9cc1c0cfac58f1a99572ebae43233dce552237c17f42d66cc1c50013986
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119776835"
---
# <a name="rendering-simple-surfaces"></a>Representación de superficies simples

La biblioteca GLU incluye un conjunto de funciones para dibujar varias superficies simples (esferas, cilindros, discos y partes de discos) en una variedad de estilos y orientaciones. Estas funciones se describen en detalle en el *Manual de referencia de OpenGL.*

**Para representar superficies simples**

1.  Cree un objeto cuádigo [**con gluNewQuadric.**](glunewquadric.md)

    Para destruir este objeto cuando haya terminado con él, use [**gluDeleteQuadric**](gludeletequadric.md).

2.  Especifique el estilo de representación deseado, como se muestra a continuación, con la función adecuada (a menos que esté satisfecho con los valores predeterminados):
    -   Si se deben generar normales de superficie y, si es así, si debe haber un normal por vértice o uno normal por cara: [ **gluQuadricNormals**](gluquadricnormals.md)
    -   Si se deben generar coordenadas de textura: [ **gluQuadricTexture**](gluquadrictexture.md)
    -   Qué lado del cuádigo debe considerarse el exterior y cuál es el interior: [ **gluQuadricOrientation**](gluquadricorientation.md)
    -   Si el cuádigo debe dibujarse como un conjunto de polígonos, líneas o puntos: [ **gluQuadricDrawStyle**](gluquadricdrawstyle.md)
3.  Después de especificar el estilo de representación, invoque la función de representación para el tipo deseado de objeto cuádigo: [**gluSphere**](glusphere.md), [**gluCylinder,**](glucylinder.md) [**gluDisk**](gludisk.md)o [**gluPartialDisk.**](glupartialdisk.md)

    Si se produce un error durante la representación, se invoca la función de control de errores que ha especificado con [*gluQuadricCallBack.*](gluquadric.md)

Use *\* los argumentos Radius*, *height* y similares, en lugar de la función [**glScale,**](glscale.md) para escalar los cuádigos, de modo que no tenga que volver a normalizar los normales de longitud de unidad que se generan. Para forzar los cálculos de iluminación con una granularidad más fina, especialmente si la especulación del material es alta, establezca los argumentos de *bucles* y pilas en valores *distintos* de 1.

 

 




