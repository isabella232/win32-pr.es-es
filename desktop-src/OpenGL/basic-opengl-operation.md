---
title: Operación básica de OpenGL
description: Operación básica de OpenGL
ms.assetid: ad4c9321-a9e3-40c5-af80-0ad6a8b9f380
keywords:
- OpenGL, operaciones básicas
- OpenGL, procesamiento de datos
- OpenGL, fases de procesamiento
- OpenGL, mostrar listas
- Mostrar listas OpenGL
- OpenGL, evaluadores
- los evaluadores OpenGL
- OpenGL, operaciones por vértice
- operaciones por vértices OpenGL
- OpenGL, ensamblado primitivo
- ensamblado primitivo OpenGL
- OpenGL, rasterización
- rasterización OpenGL
- OpenGL, operaciones por fragmento
- operaciones por fragmento OpenGL
- framebuffers, operaciones básicas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77f6b9fb8c8ca4efb05d9050e0de3da807b213e7
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "104003286"
---
# <a name="basic-opengl-operation"></a>Operación básica de OpenGL

En el diagrama siguiente se ilustra el modo en que OpenGL procesa los datos. Como se muestra, los comandos se escriben desde la izquierda y continúan a través de una canalización de procesamiento. Algunos comandos especifican los objetos geométricos que se van a dibujar y otros controlan cómo se administran los objetos durante varias fases de procesamiento.

![Diagrama que muestra las fases de canalización de procesamiento de datos de OpenGL.](images/basic01.png)

Las fases de procesamiento de la operación básica de OpenGL son las siguientes:

-   **Mostrar lista** En lugar de que todos los comandos continúen inmediatamente a través de la canalización, puede optar por acumular algunos en una lista de visualización para procesarlos más adelante.
-   **Evaluador** La fase Evaluadora del procesamiento proporciona una manera eficaz de aproximar la geometría de curva y de superficie mediante la evaluación de los comandos polinómicos de valores de entrada.
-   **Operaciones por vértice y ensamblado primitivo** OpenGL procesa primitivespoints, segmentos de línea y polygonsall geométricos que se describen en los vértices. Los vértices se transforman y se iluminan, y los primitivos se recortan a la ventanilla como preparación para la rasterización.
-   **Rasterización** La fase de rasterización genera una serie de direcciones de búfer de fotogramas y valores asociados mediante una descripción bidimensional de un punto, segmento de línea o polígono. Cada fragmento generado se introduce en la última fase, en las operaciones por fragmento.
-   **Operaciones por fragmento** Estas son las operaciones finales realizadas en los datos antes de que se almacenen como píxeles en el fotogramas.

    Las operaciones por fragmento incluyen actualizaciones condicionales para fotogramas basadas en valores z entrantes y almacenados previamente (para el almacenamiento en búfer z) y la combinación de colores de píxeles entrantes con colores almacenados, así como enmascaramiento y otras operaciones lógicas en valores de píxeles.

Los datos se pueden escribir en forma de píxeles en lugar de vértices. Los datos en forma de píxeles, como puede describir una imagen para su uso en la asignación de texturas, omiten la primera fase del procesamiento descrito anteriormente y, en su lugar, se procesan como píxeles, en la fase de operaciones de píxeles. En las siguientes operaciones de píxeles, los datos de píxeles son:

-   Se almacena como memoria de textura, para su uso en la fase de rasterización.
-   Rasterizado, con los fragmentos resultantes combinados en el fotogramas como si se hubieran generado a partir de datos geométricos.

 

 




