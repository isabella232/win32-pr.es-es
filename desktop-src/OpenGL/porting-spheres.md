---
title: Ámbitos de portabilidad
description: 'Al trasladar esferas a OpenGL, tenga en cuenta los puntos siguientes:'
ms.assetid: ca6bb515-076d-45fc-bcdd-3d71877560fb
keywords:
- Migración de la contabilidad de IRIS, esferas
- portabilidad de IRIS GL, esferas
- trasladar a OpenGL desde IRIS GL, esferas
- Exportación de OpenGL desde IRIS GL, esferas
- dibujar funciones, esferas
- esferas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f48ac31c0204111173d9eb2d31a3119873ef45b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418873"
---
# <a name="porting-spheres"></a>Ámbitos de portabilidad

Al trasladar esferas a OpenGL, tenga en cuenta los puntos siguientes:

-   No se puede controlar el tipo de primitivas que se usan para dibujar la esfera. Puede controlar la precisión del dibujo de otra manera: usar los parámetros de segmentos y pilas. Los sectores son longitudinales; las pilas son latitudinal.
-   Los esferas se dibujan centrados en el origen. En lugar de especificar la ubicación, como se hace con la función **sphdraw** de la contabilidad de iris, preceda a una llamada a la función Glu [**gluSphere**](glusphere.md) con una traducción.
-   La biblioteca de esfera todavía no está disponible para OpenGL.

En la tabla siguiente se enumeran las funciones de GL de IRIS para dibujar esferas y sus funciones equivalentes de GLU cuando están disponibles.



| Función de GL de IRIS | GLU función)                                 | Significado                                       |
|------------------|----------------------------------------------|-----------------------------------------------|
| **sphobj**       | [**gluNewQuadric**](glunewquadric.md)       | Crea un nuevo objeto sphere.                  |
| **sphfree**      | [**gluDeleteQuadric**](gludeletequadric.md) | Elimina el objeto de esfera y la memoria libre utilizada.   |
| **sphdraw**      | [**gluSphere**](glusphere.md)               | Dibuja una esfera.                               |
| **sphmode**      |                                              | Establece atributos de esfera.                       |
| **sphrotmatrix** |                                              | Controla la orientación de esfera.                  |
| **sphgnpolys**   |                                              | Devuelve el número de polígonos en la esfera actual. |



 

??

 

 




