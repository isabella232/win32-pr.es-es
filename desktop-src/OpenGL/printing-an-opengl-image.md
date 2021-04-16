---
title: Imprimir una imagen de OpenGL
description: Puede imprimir imágenes OpenGL representadas en los metaarchivos mejorados.
ms.assetid: 6099cbe2-82f9-46ec-a3ca-74486c111639
keywords:
- OpenGL en Windows, impresión
- imprimir imágenes OpenGL OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ca0c5260a084796915a7564f793f0e252b5228c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105665868"
---
# <a name="printing-an-opengl-image"></a>Imprimir una imagen de OpenGL

Puede imprimir imágenes OpenGL representadas en los metaarchivos mejorados. Al representar en un dispositivo de impresora (HDC), debe estar respaldado por un administrador de trabajos de impresión de metarchivo. OpenGL usa memoria para la profundidad, el color y otros búferes para almacenar los resultados de gráficos en una impresora. Dado que la resolución de impresora típica requiere una cantidad de memoria significativa para almacenar la salida de gráficos, la impresión de una imagen de OpenGL podría requerir más memoria de la que está disponible en el sistema. Para superar esta limitación, la implementación de OpenGL actual imprime gráficos OpenGL en bandas. Sin embargo, esto aumenta el tiempo necesario para imprimir imágenes OpenGL.

Antes de imprimir una imagen OpenGL, debe llamar a la función [StartDoc](/windows/desktop/api/wingdi/nf-wingdi-startdoca) para completar la inicialización de un contexto de dispositivo de impresora (DC). Después de llamar a **StartDoc**, puede crear contextos de representación (HGLRC) para representarlos en el dispositivo de impresora. Si crea contextos de representación antes de llamar a **StartDoc**, no hay ninguna manera de determinar si un metarchivo está en cola.

En el ejemplo de código siguiente se muestra cómo imprimir una imagen de OpenGL:

``` syntax
HDC            hDC;
DOCINFO        di;
HGLRC          hglrc;

// Call StartDoc to start the document 
StartDoc( hDC, &di );

// Prepare the printer driver to accept data 
StartPage(hDC);

// Create a rendering context using the metafile DC 
hglrc = wglCreateContext ( hDCmetafile );

// Do OpenGL rendering operations here 
    . . .
wglMakeCurrent(NULL, NULL); // Get rid of rendering context 
    . . .
EndPage(hDC); // Finish writing to the page 
EndDoc(hDC); // End the print job
```

Para obtener más información sobre el uso de metaarchivos, vea [operaciones de metarchivo mejorado](/windows/desktop/gdi/enhanced-metafile-operations).

 

 