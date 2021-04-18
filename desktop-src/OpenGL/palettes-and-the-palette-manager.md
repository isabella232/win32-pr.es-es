---
title: Paletas y el administrador de paletas
description: El administrador de paletas de Windows, que forma parte de GDI, se centra específicamente en los adaptadores de pantalla de 8 bits con una paleta de hardware de 256 entradas de color.
ms.assetid: 3bfa5077-37ac-4597-98da-f26ad1c107a1
keywords:
- OpenGL en Windows, administrador de paletas
- OpenGL en Windows, paletas de hardware
- Administrador de paletas OpenGL
- paletas de hardware OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3dac7d122ec36201e0156a141efc3291a87c7150
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105665649"
---
# <a name="palettes-and-the-palette-manager"></a>Paletas y el administrador de paletas

El administrador de paletas de Windows, que forma parte de GDI, se centra específicamente en los adaptadores de pantalla de 8 bits con una *paleta de hardware* de 256 entradas de color. Los píxeles de la pantalla se almacenan como un índice de 8 bits en la paleta de hardware. Cada entrada de la paleta de hardware suele definir un color de 24 bits (8 en rojo, verde y azul).

El administrador de paletas mantiene una *paleta del sistema* que es una copia de la paleta de hardware. La paleta del sistema se divide en dos secciones: 20 colores reservados y los colores 236 restantes, que se pueden establecer mediante el administrador de paletas.

Una *paleta lógica* de 20 colores predeterminada se selecciona y se lleva a cabo en un contexto de dispositivo. Puede crear y usar una nueva paleta lógica. Para cambiar la paleta del sistema, seleccione y observe la paleta lógica que creó.

Probablemente creará una paleta lógica para especificar los colores que desea que se muestren en la aplicación de OpenGL. Con ciertas llamadas GDI, puede reemplazar temporalmente la mayoría de la paleta del sistema por una paleta lógica. Con una paleta lógica, puede definir colores de píxeles para la GDI mediante el modo RGBA o el modo de índice de color. El tamaño máximo de una paleta lógica es de 256 colores para dispositivos de 8 bits y 4.096 colores en un dispositivo de color verdadero (16, 24 y 32 bits).

Para obtener más información sobre los modos RGBA y índice de color, consulte [modo RGBA y administración](rgba-mode-and-windows-palette-management.md) de la paleta de Windows y [modos de color OpenGL y administración de paletas de Windows](opengl-color-modes-and-windows-palette-management.md).

 

 




