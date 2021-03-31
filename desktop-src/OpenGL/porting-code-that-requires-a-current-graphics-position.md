---
title: Código de puerto que necesita una posición de gráficos actual
description: OpenGL no mantiene una posición de gráficos actual. Las funciones de GL de IRIS que dependen de la posición actual de los gráficos, como Move, Draw y RMV, no tienen ningún equivalente en OpenGL.
ms.assetid: d6c42d9c-6fbb-4b72-8097-285d19b619c2
keywords:
- Migración de la contabilidad de IRIS, posición de gráficos actual
- trasladar de IRIS GL, posición de gráficos actual
- trasladar a OpenGL desde IRIS GL, posición de gráficos actual
- Exportación de OpenGL desde IRIS GL, posición de gráficos actual
- posición de los gráficos actuales
- posiciones de trama
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd7e7cbbaf0a22385c83569775758e24f70cd210
ms.sourcegitcommit: b95a94ffffda33f9ebbdd41787c01866444b4cf4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/27/2019
ms.locfileid: "103785134"
---
# <a name="port-code-that-needs-a-current-graphics-position"></a>Código de puerto que necesita una posición de gráficos actual

OpenGL no mantiene una posición de gráficos actual. Las funciones de GL de IRIS que dependen de la posición actual de los gráficos, como **Move**, **Draw** y **RMV**, no tienen ningún equivalente en OpenGL.

Las versiones anteriores de IRIS GL incluían comandos de dibujo que se basan en la posición actual de los gráficos, aunque no se recomienda su uso. Tendrá que volver a escribir el código si se basó en la posición actual de los gráficos de cualquier manera, o si se usara cualquiera de las siguientes rutinas:

-   **dibujar** y **desplace**
-   **PMV**, **PDR** y **PCLOS**
-   **RDR**, **RMV**, **rpdr** y **rpmv**
-   **getgpos**

OpenGL tiene un concepto de posición de trama que corresponde a la posición de carácter actual de la contabilidad de IRIS. Para obtener más información sobre el posicionamiento de tramas, vea [portar operaciones de píxeles](porting-pixel-operations.md).

En este tema se incluye información sobre lo siguiente.

-   [Trasladar comandos de borrado de pantalla y de búfer](porting-screen-and-buffer-clearing-commands.md)
-   [Portabilidad de funciones de transformación y de matriz](porting-matrix-and-transformation-functions.md)
-   [Trasladar código de modo MSINGLE](porting-msingle-mode-code.md)
-   [Portabilidad de funciones que obtienen matrices y transformaciones](porting-functions-that-get-matrices-and-transformations.md)
-   [Trasladar las ventanillas, Screenmasks y Scrboxes](porting-viewports--screenmasks--and-scrboxes.md)
-   [Trasladar los planos de recorte](porting-clipping-planes.md)

 

 




