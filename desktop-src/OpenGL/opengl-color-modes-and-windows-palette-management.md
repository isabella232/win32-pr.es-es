---
title: Modos de color de OpenGL y administración de paleta de Windows
description: La implementación de Microsoft de OpenGL en Windows admite dos modos de datos de píxeles de color y modos RGBA y de índice de color. Windows proporcionan dos maneras análogas de controlar la administración de colores y paletas de color verdadero.
ms.assetid: 4a731119-8704-4ae1-a564-4a1955051236
keywords:
- OpenGL en Windows, modos de color
- OpenGL en Windows, administración de paletas
- Administración de paletas OpenGL
- modos de color OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa3d63778301ec55b962f3f66e79d99cee09be9d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104356977"
---
# <a name="opengl-color-modes-and-windows-palette-management"></a>Modos de color de OpenGL y administración de paleta de Windows

La implementación de Microsoft de OpenGL en Windows admite dos modos de datos de píxeles de color: los modos RGBA y índice de color. Windows proporcionan dos maneras análogas de controlar el color: verdadero color y administración de la paleta.

Los dispositivos de color verdadero, capaces de aceptar 16, 24 o más bits de información de color por píxel, pueden mostrar decenas de miles, decenas de millones o más colores simultáneamente. Sin embargo, surgen complicaciones cuando una aplicación tiene que administrar el modo RGBA o el índice de color en un dispositivo de tipo paleta. Los dispositivos de tipo paleta, como una pantalla VGA de 256 colores, están limitados en el número de colores que se pueden mostrar simultáneamente. Las aplicaciones deben controlar una serie de detalles complicados para usar correctamente los dispositivos de tipo Palette. Dado que los programas en modo de índice de color no usan una paleta de hardware, son más difíciles de usar con dispositivos de color verdadero que los programas que usan el modo RGBA.

 

 




