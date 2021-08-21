---
title: Porte de esferas
description: Al portear esferas a OpenGL, tenga en cuenta los siguientes puntos
ms.assetid: ca6bb515-076d-45fc-bcdd-3d71877560fb
keywords:
- Porte de IRIS GL, esferas
- porting from IRIS GL,spheres
- porte a OpenGL desde IRIS GL, esferas
- Porte de OpenGL desde IRIS GL,spheres
- funciones de dibujo, esferas
- Esferas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af1e0666393e923767d342d215622e0ed58bfa7b1b620e045a0054b31918a7a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118358315"
---
# <a name="porting-spheres"></a>Porte de esferas

Al portear esferas a OpenGL, tenga en cuenta los siguientes puntos:

-   No se puede controlar el tipo de primitivas usadas para dibujar la esfera. Puede controlar la precisión del dibujo de otra manera: use los parámetros de segmentos y pilas. Los segmentos son muy diferentes; las pilas son latitudinales.
-   Las esferas se dibujan centradas en el origen. En lugar de especificar la ubicación, como se hace con la función **sphdraw** de IRIS GL, preceda una llamada a la función [**gluSphere de**](glusphere.md) GLU con una traducción.
-   La biblioteca sphere aún no está disponible para OpenGL.

En la tabla siguiente se enumeran las funciones GL de IRIS para dibujar esferas y sus funciones GLU equivalentes cuando estén disponibles.



| Función GL de IRIS | Función GLU                                 | Significado                                       |
|------------------|----------------------------------------------|-----------------------------------------------|
| **sphobj**       | [**gluNewQuadric**](glunewquadric.md)       | Crea un nuevo objeto sphere.                  |
| **sphfree**      | [**gluDeleteQuadric**](gludeletequadric.md) | Elimina el objeto sphere y la memoria libre usada.   |
| **sphdraw**      | [**gluSphere**](glusphere.md)               | Dibuja una esfera.                               |
| **sphmode**      |                                              | Establece atributos de esfera.                       |
| **sphrotmatrix** |                                              | Controla la orientación de la esfera.                  |
| **sphgnpolys**   |                                              | Devuelve el número de polígonos en la esfera actual. |



 

??

 

 




