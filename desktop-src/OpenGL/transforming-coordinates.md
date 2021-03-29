---
title: Transformar coordenadas
description: La biblioteca de utilidades OpenGL (GLU) proporciona varias funciones de transformación de matriz de uso frecuente.
ms.assetid: 9ca32be8-3bc0-4fca-a58c-69a4800c3c55
keywords:
- Utilidad OpenGL (GLU), funciones de transformación de matriz
- GLU (utilidad OpenGL), funciones de transformación de matriz
- funciones de transformación de matriz OpenGL
- Utilidad OpenGL (GLU), transformar coordenadas
- GLU (utilidad OpenGL), transformar coordenadas
- transformación de coordenadas OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 504a5a58c723dcccfc54ce2f47a01710133ccc30
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103779471"
---
# <a name="transforming-coordinates"></a>Transformar coordenadas

La biblioteca de utilidades OpenGL (GLU) proporciona varias funciones de transformación de matriz de uso frecuente. Puede configurar una región de visualización ortográfica bidimensional con [**gluOrtho2D**](gluortho2d.md), un volumen de vista de perspectiva estándar con [**gluPerspective**](gluperspective.md), o un volumen de vista centrado en un eyepoint especificado con [**gluLookAt**](glulookat.md). Cada una de estas funciones crea la matriz deseada y la aplica a la matriz actual mediante [**glMultMatrix**](glmultmatrix.md).

La función [**gluPickMatrix**](glupickmatrix.md) simplifica la selección de una matriz de picking mediante la creación de una matriz que restringe el dibujo a una región pequeña de la ventanilla. Si vuelve a representar la escena en el modo de selección después de aplicar esta matriz, se seleccionarán todos los objetos que se dibujen cerca del cursor y la información sobre ellos se almacenará en el búfer de selección. Para obtener más información sobre el modo de selección, vea el tema sobre cómo realizar [la selección y los comentarios.](performing-selection-and-feedback.md)

Para determinar dónde se dibuja un objeto en la ventana, use [**gluProject**](gluproject.md), que convierte las coordenadas del objeto especificado *objx*, *objy* y *Objz* en coordenadas de la ventana mediante *modelMatrix*, *projMatrix* y *viewport*. El resultado se almacena en *Winx*, *Winy* y *Winz*. Si la función se ejecuta correctamente, el valor devuelto es GL \_ true. Si se produce un error en la función, el valor devuelto es GL \_ false.

La función [**gluUnProject**](gluunproject.md) realiza la conversión inversa: transforma las coordenadas de ventana especificadas *Winx*, *Winy* y *Winz* en coordenadas de objeto mediante *modelMatrix*, *projMatrix* y *viewport*. El resultado se almacena en *objx*, *objy* y *objz*. Si la función se ejecuta correctamente, el valor devuelto es GL \_ true. Si se produce un error en la función, el valor devuelto es GL \_ false.

 

 




