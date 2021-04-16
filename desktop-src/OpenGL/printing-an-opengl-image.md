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
# <a name="printing-an-opengl-image"></a><span data-ttu-id="570aa-105">Imprimir una imagen de OpenGL</span><span class="sxs-lookup"><span data-stu-id="570aa-105">Printing an OpenGL Image</span></span>

<span data-ttu-id="570aa-106">Puede imprimir imágenes OpenGL representadas en los metaarchivos mejorados.</span><span class="sxs-lookup"><span data-stu-id="570aa-106">You can print OpenGL images rendered in enhanced metafiles.</span></span> <span data-ttu-id="570aa-107">Al representar en un dispositivo de impresora (HDC), debe estar respaldado por un administrador de trabajos de impresión de metarchivo.</span><span class="sxs-lookup"><span data-stu-id="570aa-107">When you render to a printer device (HDC) it must be backed by a metafile spooler.</span></span> <span data-ttu-id="570aa-108">OpenGL usa memoria para la profundidad, el color y otros búferes para almacenar los resultados de gráficos en una impresora.</span><span class="sxs-lookup"><span data-stu-id="570aa-108">OpenGL uses memory for depth, color, and other buffers to store graphics output to a printer.</span></span> <span data-ttu-id="570aa-109">Dado que la resolución de impresora típica requiere una cantidad de memoria significativa para almacenar la salida de gráficos, la impresión de una imagen de OpenGL podría requerir más memoria de la que está disponible en el sistema.</span><span class="sxs-lookup"><span data-stu-id="570aa-109">Because typical printer resolution requires a significant amount of memory to store the graphics output, printing an OpenGL image might require more memory than is available in the system.</span></span> <span data-ttu-id="570aa-110">Para superar esta limitación, la implementación de OpenGL actual imprime gráficos OpenGL en bandas.</span><span class="sxs-lookup"><span data-stu-id="570aa-110">To overcome this limitation, the current implementation of OpenGL prints OpenGL graphics in bands.</span></span> <span data-ttu-id="570aa-111">Sin embargo, esto aumenta el tiempo necesario para imprimir imágenes OpenGL.</span><span class="sxs-lookup"><span data-stu-id="570aa-111">However, this increases the time it takes to print OpenGL images.</span></span>

<span data-ttu-id="570aa-112">Antes de imprimir una imagen OpenGL, debe llamar a la función [StartDoc](/windows/desktop/api/wingdi/nf-wingdi-startdoca) para completar la inicialización de un contexto de dispositivo de impresora (DC).</span><span class="sxs-lookup"><span data-stu-id="570aa-112">Before you print an OpenGL image, you must call the [StartDoc](/windows/desktop/api/wingdi/nf-wingdi-startdoca) function to complete the initialization of a printer device context (DC).</span></span> <span data-ttu-id="570aa-113">Después de llamar a **StartDoc**, puede crear contextos de representación (HGLRC) para representarlos en el dispositivo de impresora.</span><span class="sxs-lookup"><span data-stu-id="570aa-113">After calling **StartDoc**, you can create rendering contexts (HGLRC) to render to the printer device.</span></span> <span data-ttu-id="570aa-114">Si crea contextos de representación antes de llamar a **StartDoc**, no hay ninguna manera de determinar si un metarchivo está en cola.</span><span class="sxs-lookup"><span data-stu-id="570aa-114">If you create rendering contexts before calling **StartDoc**, there is no way to determine whether a metafile is spooled.</span></span>

<span data-ttu-id="570aa-115">En el ejemplo de código siguiente se muestra cómo imprimir una imagen de OpenGL:</span><span class="sxs-lookup"><span data-stu-id="570aa-115">The following code sample shows how to print an OpenGL image:</span></span>

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

<span data-ttu-id="570aa-116">Para obtener más información sobre el uso de metaarchivos, vea [operaciones de metarchivo mejorado](/windows/desktop/gdi/enhanced-metafile-operations).</span><span class="sxs-lookup"><span data-stu-id="570aa-116">For more information on using metafiles, see [Enhanced Metafile Operations](/windows/desktop/gdi/enhanced-metafile-operations).</span></span>

 

 