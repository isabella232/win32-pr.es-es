---
title: Operación básica de OpenGL
description: Operación básica de OpenGL
ms.assetid: ad4c9321-a9e3-40c5-af80-0ad6a8b9f380
keywords:
- OpenGL, operaciones básicas
- OpenGL, procesamiento de datos
- OpenGL, fases de procesamiento
- OpenGL, mostrar listas
- mostrar listas OpenGL
- OpenGL, evaluadores
- evaluadores OpenGL
- OpenGL, operaciones por vértice
- operaciones por vértice OpenGL
- OpenGL, ensamblado primitivo
- ensamblado primitivo OpenGL
- OpenGL, rasterización
- rasterización OpenGL
- OpenGL, operaciones por fragmento
- operaciones por fragmento OpenGL
- framebuffers,operaciones básicas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f72f6abed7d06a93985b798e72efbf4d6ec0901e7ad9fb4614f5bf81590cefcf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119554725"
---
# <a name="basic-opengl-operation"></a>Operación básica de OpenGL

En el diagrama siguiente se muestra cómo OpenGL procesa los datos. Como se muestra, los comandos escriben desde la izquierda y pasan por una canalización de procesamiento. Algunos comandos especifican los objetos geométricos que se van a dibujar y otros controlan cómo se controlan los objetos durante varias fases de procesamiento.

![Diagrama que muestra las fases de canalización de procesamiento de datos de OpenGL.](images/basic01.png)

Las fases de procesamiento de la operación básica de OpenGL son las siguientes:

-   **Mostrar lista** En lugar de hacer que todos los comandos continúen inmediatamente a través de la canalización, puede optar por acumular algunos de ellos en una lista de visualización para su procesamiento más adelante.
-   **Evaluador** La fase de procesamiento del evaluador proporciona una manera eficaz de aproximar la geometría de curva y superficie mediante la evaluación de comandos polinómicos de valores de entrada.
-   **Operaciones por vértice y ensamblado primitivo** OpenGL procesa puntos primitivos geométricos, segmentos de línea y polígonos que se describen mediante vértices. Los vértices se transforman y se encienden, y los primitivos se recortan a la ventanilla como preparación para la rasterización.
-   **Rasterización** La fase de rasterización genera una serie de direcciones de búfer de fotogramas y valores asociados mediante una descripción bidimensional de un punto, segmento de línea o polígono. Cada fragmento que se produce se introduce en la última fase, las operaciones por fragmento.
-   **Operaciones por fragmento** Estas son las operaciones finales realizadas en los datos antes de almacenarse como píxeles en el búfer de fotogramas.

    Las operaciones por fragmento incluyen actualizaciones condicionales del búfer de fotogramas en función de los valores z entrantes y previamente almacenados (para el almacenamiento en búfer z) y la combinación de colores de píxeles entrantes con colores almacenados, así como enmascaramiento y otras operaciones lógicas en valores de píxel.

Los datos se pueden introducir en forma de píxeles en lugar de vértices. Los datos en forma de píxeles, como pueden describir una imagen para su uso en la asignación de texturas, omiten la primera fase de procesamiento descrita anteriormente y, en su lugar, se procesan como píxeles, en la fase de operaciones de píxeles. En las siguientes operaciones de píxel, los datos de píxeles son:

-   Se almacena como memoria de textura, para su uso en la fase de rasterización.
-   Rasterizado, con los fragmentos resultantes combinados en el búfer de fotogramas como si se hubieran generado a partir de datos geométricos.

 

 




