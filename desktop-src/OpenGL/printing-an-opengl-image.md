---
title: Impresión de una imagen OpenGL
description: Puede imprimir imágenes OpenGL que se representan en metarchivos mejorados.
ms.assetid: 6099cbe2-82f9-46ec-a3ca-74486c111639
keywords:
- OpenGL en Windows, imprimir
- impresión de imágenes OpenGL OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ca0c5260a084796915a7564f793f0e252b5228c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127362025"
---
# <a name="printing-an-opengl-image"></a>Impresión de una imagen OpenGL

Puede imprimir imágenes OpenGL que se representan en metarchivos mejorados. Cuando se representa en un dispositivo de impresora (HDC), debe estar respaldo de un administrador de trabajos de cola de metarchivos. OpenGL usa memoria para profundidad, color y otros búferes para almacenar la salida de gráficos en una impresora. Dado que la resolución de impresora típica requiere una cantidad significativa de memoria para almacenar la salida de gráficos, la impresión de una imagen OpenGL puede requerir más memoria de la que está disponible en el sistema. Para superar esta limitación, la implementación actual de OpenGL imprime gráficos OpenGL en bandas. Sin embargo, esto aumenta el tiempo que se tarda en imprimir imágenes OpenGL.

Antes de imprimir una imagen de OpenGL, debe llamar a la [función StartDoc](/windows/desktop/api/wingdi/nf-wingdi-startdoca) para completar la inicialización de un contexto de dispositivo de impresora (DC). Después de **llamar a StartDoc**, puede crear contextos de representación (HGLRC) para representar en el dispositivo de impresora. Si crea contextos de representación antes de llamar a **StartDoc**, no hay ninguna manera de determinar si un metarchivo está en cola.

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

Para obtener más información sobre el uso de metarchivos, vea [Operaciones mejoradas de metarchivo.](/windows/desktop/gdi/enhanced-metafile-operations)

 

 