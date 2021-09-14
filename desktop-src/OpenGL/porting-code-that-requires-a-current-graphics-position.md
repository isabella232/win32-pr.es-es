---
title: Código de puerto que necesita una posición de gráficos actual
description: OpenGL no mantiene una posición de gráficos actual. Las funciones GL de IRIS que dependen de la posición de gráficos actual, como mover, dibujar y rmv, no tienen equivalentes en OpenGL.
ms.assetid: d6c42d9c-6fbb-4b72-8097-285d19b619c2
keywords:
- Porte de IRIS GL, posición de gráficos actual
- porting from IRIS GL,current graphics position
- porting to OpenGL from IRIS GL,current graphics position
- Porte openGL desde IRIS GL, posición de gráficos actual
- posición de gráficos actual
- Posiciones de trama
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd7e7cbbaf0a22385c83569775758e24f70cd210
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127169206"
---
# <a name="port-code-that-needs-a-current-graphics-position"></a>Código de puerto que necesita una posición de gráficos actual

OpenGL no mantiene una posición de gráficos actual. Las funciones GL de IRIS que dependen de la posición de gráficos actual, como mover **,** dibujar y **rmv,** no tienen equivalentes en OpenGL.

Las versiones anteriores de IRIS GL incluían comandos de dibujo que se basaban en la posición de gráficos actual, aunque se ha desaconsejado su uso. Tendrá que volver a escribir el código si se ha basado en la posición actual de los gráficos de cualquier manera, o si ha usado cualquiera de las rutinas siguientes:

-   **dibujar** y **mover**
-   **pmv,** **pdr** y **pclos**
-   **rdr,** **rmv,** **rpdr** y **rpmv**
-   **getgpos**

OpenGL tiene un concepto de posición de trama que corresponde a la posición del carácter actual de IRIS GL. Para obtener más información sobre el posicionamiento de trama, [vea Porting Pixel Operations](porting-pixel-operations.md).

En este tema se incluye información sobre lo siguiente.

-   [Comandos de borrado de búfer y pantalla de porte](porting-screen-and-buffer-clearing-commands.md)
-   [Porting Matrix and Transformation Functions](porting-matrix-and-transformation-functions.md)
-   [Porting MSINGLE Mode Code](porting-msingle-mode-code.md)
-   [Porte de funciones que obtienen matrices y transformaciones](porting-functions-that-get-matrices-and-transformations.md)
-   [Porting Viewports, Screenmasks y Scrboxes](porting-viewports--screenmasks--and-scrboxes.md)
-   [Porte de planos de recorte](porting-clipping-planes.md)

 

 




