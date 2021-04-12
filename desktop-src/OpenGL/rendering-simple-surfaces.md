---
title: Representación de superficies simples
description: La biblioteca GLU incluye un conjunto de funciones para dibujar varias superficies simples (esferas, cilindros, discos y partes de discos) en una variedad de estilos y orientaciones. Estas funciones se describen en detalle en el manual de referencia de OpenGL.
ms.assetid: 403bdf8d-de4c-49e2-87d0-11109061b4c2
keywords:
- Utilidad OpenGL (GLU), superficies simples
- GLU (utilidad OpenGL), superficies simples
- superficies simples OpenGL
- Utilidad OpenGL (GLU), esferas
- GLU (utilidad OpenGL), esferas
- esferas OpenGL
- Utilidad OpenGL (GLU), cilindros
- GLU (utilidad OpenGL), cilindros
- cilindros de OpenGL
- Utilidad OpenGL (GLU), discos
- GLU (utilidad OpenGL), discos
- discos OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab766c661f89cbdec30b3295dfef8dc85b59f7fe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104419177"
---
# <a name="rendering-simple-surfaces"></a>Representación de superficies simples

La biblioteca GLU incluye un conjunto de funciones para dibujar varias superficies simples (esferas, cilindros, discos y partes de discos) en una variedad de estilos y orientaciones. Estas funciones se describen en detalle en el *manual de referencia de OpenGL*.

**Para representar superficies simples**

1.  Cree un objeto quadric con [**gluNewQuadric**](glunewquadric.md).

    Para destruir este objeto cuando haya terminado, use [**gluDeleteQuadric**](gludeletequadric.md).

2.  Especifique el estilo de representación que desee, como se muestra a continuación, con la función adecuada (a menos que esté satisfecho con los valores predeterminados):
    -   Si se deben generar normales de superficie y, en caso afirmativo, si debe haber una normal por vértice o una normal por cara: [ **gluQuadricNormals**](gluquadricnormals.md)
    -   Indica si se deben generar coordenadas de textura: [ **gluQuadricTexture**](gluquadrictexture.md)
    -   Qué lado del quadric se debe considerar fuera y en el interior: [ **gluQuadricOrientation**](gluquadricorientation.md)
    -   Si quadric se debe dibujar como un conjunto de polígonos, líneas o puntos: [ **gluQuadricDrawStyle**](gluquadricdrawstyle.md)
3.  Después de especificar el estilo de representación, invoque la función de representación para el tipo deseado del objeto quadric: [**gluSphere**](glusphere.md), [**gluCylinder**](glucylinder.md), [**gluDisk**](gludisk.md)o [**gluPartialDisk**](glupartialdisk.md).

    Si se produce un error durante la representación, se invoca la función de control de errores que ha especificado con [*gluQuadricCallBack*](gluquadric.md) .

Use el *\* radio*, el *alto* y argumentos similares, en lugar de la función [**glScale**](glscale.md) , para escalar el Quadrics, de modo que no tenga que volver a normalizar las normales de longitud de unidad que se generan. Para forzar cálculos de iluminación con una granularidad más fina, especialmente si la especulación del material es alta, establezca los argumentos *bucles* y *pilas* en valores distintos de 1.

 

 




