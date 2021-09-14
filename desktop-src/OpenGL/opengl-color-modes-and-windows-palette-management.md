---
title: Modos de color OpenGL y administración Windows paleta de colores
description: La implementación de Microsoft de OpenGL en Windows admite dos modos de datos de píxeles de color RGBA y modos de índice de color. Windows dos formas análogas de controlar el color verdadero del color y la administración de paletas.
ms.assetid: 4a731119-8704-4ae1-a564-4a1955051236
keywords:
- OpenGL en Windows, modos de color
- OpenGL en Windows, administración de paletas
- Administración de paletas OpenGL
- modos de color OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa3d63778301ec55b962f3f66e79d99cee09be9d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127265631"
---
# <a name="opengl-color-modes-and-windows-palette-management"></a>Modos de color OpenGL y administración Windows paleta de colores

La implementación de Microsoft de OpenGL en Windows admite dos modos de datos de píxeles de color: RGBA y modos de índice de color. Windows dos formas análogas de controlar el color: administración de colores verdaderos y paletas.

Los dispositivos de color verdadero, que pueden aceptar 16, 24 o más bits de información de color por píxel, pueden mostrar decenas de miles, decenas de millones o más colores simultáneamente. Sin embargo, las complejidades surgen cuando una aplicación tiene que administrar el modo RGBA o de índice de color en un dispositivo de tipo paleta. Los dispositivos de tipo paleta, como una pantalla VGA de 256 colores, están limitados en el número de colores que pueden mostrar simultáneamente. Las aplicaciones deben controlar una serie de detalles complicados para usar correctamente dispositivos de tipo paleta. Dado que los programas de modo de índice de color no usan una paleta de hardware, son más difíciles de usar con dispositivos de color verdadero que con programas que usan el modo RGBA.

 

 




