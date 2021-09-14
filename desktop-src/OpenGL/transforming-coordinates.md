---
title: Transformar coordenadas
description: La biblioteca de la utilidad OpenGL (GLU) proporciona varias funciones de transformación de matriz usadas con frecuencia.
ms.assetid: 9ca32be8-3bc0-4fca-a58c-69a4800c3c55
keywords:
- Utilidad OpenGL (GLU),funciones de transformación de matriz
- GLU (utilidad OpenGL),funciones de transformación de matriz
- Funciones de transformación de matriz OpenGL
- Utilidad OpenGL (GLU), transformar coordenadas
- GLU (utilidad OpenGL), transformar coordenadas
- transformación de coordenadas OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 504a5a58c723dcccfc54ce2f47a01710133ccc30
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127362000"
---
# <a name="transforming-coordinates"></a>Transformar coordenadas

La biblioteca de la utilidad OpenGL (GLU) proporciona varias funciones de transformación de matriz usadas con frecuencia. Puede configurar una región de visualización ortográfica bidimensional con [**gluOrtho2D,**](gluortho2d.md)un volumen de vista de perspectiva estándar mediante [**gluPerspective**](gluperspective.md)o un volumen de vista centrado en un punto de vista especificado con [**gluLookAt**](glulookat.md). Cada una de estas funciones crea la matriz deseada y la aplica a la matriz actual mediante [**glMultMatrix**](glmultmatrix.md).

La [**función gluPickMatrix**](glupickmatrix.md) simplifica la selección de una matriz de selección mediante la creación de una matriz que restringe el dibujo a una pequeña región de la ventanilla. Si vuelve a representar la escena en modo de selección después de aplicar esta matriz, se seleccionarán todos los objetos que se dibujarían cerca del cursor y la información sobre ellos se almacenará en el búfer de selección. Para obtener más información sobre el modo de selección, vea "Realizar selección y comentarios" [Realizando selección y comentarios.](performing-selection-and-feedback.md)

Para determinar dónde se dibuja un objeto en la ventana, use [**gluProject**](gluproject.md), que convierte las coordenadas de objeto *especificadas objx*, *objy* y *objz* en coordenadas de ventana mediante *modelMatrix*, *projMatrix* y *viewport*. El resultado se almacena en *winx,* *winy* y *winz.* Si la función se realiza correctamente, el valor devuelto es GL \_ TRUE. Si se produce un error en la función, el valor devuelto es GL \_ FALSE.

La función [**gluUnProject**](gluunproject.md) realiza la conversión inversa: transforma las coordenadas de ventana especificadas *winx,* *winy* y *winz* en coordenadas de objeto mediante *modelMatrix*, *projMatrix* y *viewport.* El resultado se almacena en *objx*, *objy* y *objz*. Si la función se realiza correctamente, el valor devuelto es GL \_ TRUE. Si se produce un error en la función, el valor devuelto es GL \_ FALSE.

 

 




