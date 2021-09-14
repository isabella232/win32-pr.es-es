---
title: Paletas y el administrador de paletas
description: El administrador Windows paletas, que forma parte del GDI, tiene como destino específicamente adaptadores de pantalla de 8 bits con una paleta de hardware de 256 entradas de color.
ms.assetid: 3bfa5077-37ac-4597-98da-f26ad1c107a1
keywords:
- OpenGL en Windows, administrador de paletas
- OpenGL en Windows, paletas de hardware
- Administrador de paletas OpenGL
- paletas de hardware OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3dac7d122ec36201e0156a141efc3291a87c7150
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127259895"
---
# <a name="palettes-and-the-palette-manager"></a>Paletas y el administrador de paletas

El administrador Windows paletas, que forma parte del GDI, tiene como destino específicamente adaptadores de pantalla de 8 bits con una paleta de *hardware* de 256 entradas de color. Los píxeles de la pantalla se almacenan como un índice de 8 bits en la paleta de hardware. Cada entrada de la paleta de hardware normalmente define un color de 24 bits (8 de rojo, verde y azul).

El Administrador de paletas mantiene una *paleta del sistema* que es una copia de la paleta de hardware. La paleta del sistema se divide en dos secciones: 20 colores reservados y los 236 colores restantes, que puede establecer mediante el Administrador de paletas.

Se selecciona una paleta lógica de 20 *colores* predeterminada y se realiza en un contexto de dispositivo. Puede crear y usar una nueva paleta lógica. Para cambiar la paleta del sistema, seleccione y dé cuenta de la paleta lógica que ha creado.

Probablemente creará una paleta lógica para especificar los colores que desea mostrar en la aplicación OpenGL. Con determinadas llamadas GDI, puede reemplazar temporalmente la mayoría de la paleta del sistema por una paleta lógica. Con una paleta lógica, puede definir colores de píxeles para el GDI mediante rgba o el modo de índice de color. El tamaño máximo de una paleta lógica es de 256 colores para dispositivos de 8 bits y 4096 colores en un dispositivo de color verdadero (16, 24 y 32 bits).

Para obtener más información sobre los modos RGBA e índice de color, vea [RgbA Mode and Windows Palette Management](rgba-mode-and-windows-palette-management.md) y [OpenGL Color Modes and Windows Palette Management](opengl-color-modes-and-windows-palette-management.md).

 

 




