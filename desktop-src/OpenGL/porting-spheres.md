---
title: Porte de esferas
description: Al portear esferas a OpenGL, tenga en cuenta los siguientes puntos
ms.assetid: ca6bb515-076d-45fc-bcdd-3d71877560fb
keywords:
- Porte de IRIS GL, esferas
- porting from IRIS GL,spheres
- porting to OpenGL from IRIS GL,spheres
- Porte de OpenGL desde IRIS GL, esferas
- funciones de dibujo, esferas
- Esferas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f48ac31c0204111173d9eb2d31a3119873ef45b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073986"
---
# <a name="porting-spheres"></a>Porte de esferas

Al portear esferas a OpenGL, tenga en cuenta los siguientes puntos:

-   No se puede controlar el tipo de primitivas utilizadas para dibujar la esfera. Puede controlar la precisión del dibujo de otra manera: use los parámetros de segmentos y pilas. Los segmentos son así; las pilas son latitudinales.
-   Las esferas se dibujan centradas en el origen. En lugar de especificar la ubicación, como se hace con la función **sphdraw** de IRIS GL, anteponga una llamada a la función [**GLU gluSphere**](glusphere.md) con una traducción.
-   La biblioteca sphere aún no está disponible para OpenGL.

En la tabla siguiente se enumeran las funciones GL de IRIS para dibujar esferas y sus funciones GLU equivalentes cuando estén disponibles.



| Función IRIS GL | Función GLU                                 | Significado                                       |
|------------------|----------------------------------------------|-----------------------------------------------|
| **sphobj**       | [**gluNewQuadric**](glunewquadric.md)       | Crea un nuevo objeto sphere.                  |
| **sphfree**      | [**gluDeleteQuadric**](gludeletequadric.md) | Elimina el objeto sphere y la memoria libre usada.   |
| **sphdraw**      | [**gluSphere**](glusphere.md)               | Dibuja una esfera.                               |
| **sphmode**      |                                              | Establece atributos de esfera.                       |
| **sphrotmatrix** |                                              | Controla la orientación de la esfera.                  |
| **sphgnpolys**   |                                              | Devuelve el número de polígonos de la esfera actual. |



 

??

 

 




