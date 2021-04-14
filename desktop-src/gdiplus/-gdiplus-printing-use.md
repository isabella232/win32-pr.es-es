---
description: Con unos pocos ajustes secundarios en el código, puede enviar la salida GDI+ de Windows a una impresora en lugar de a una pantalla.
ms.assetid: be6286e9-d125-40ad-b33e-b4e734ac2709
title: Imprimir (GDI+)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e3b60010bcb63c553a96c5d70826f3fe0d3d4aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985138"
---
# <a name="printing-gdi"></a><span data-ttu-id="14881-103">Imprimir (GDI+)</span><span class="sxs-lookup"><span data-stu-id="14881-103">Printing (GDI+)</span></span>

<span data-ttu-id="14881-104">Con unos pocos ajustes secundarios en el código, puede enviar la salida GDI+ de Windows a una impresora en lugar de a una pantalla.</span><span class="sxs-lookup"><span data-stu-id="14881-104">With a few minor adjustments to your code, you can send Windows GDI+ output to a printer rather than to a screen.</span></span> <span data-ttu-id="14881-105">Para dibujar en una impresora, obtenga un identificador de contexto de dispositivo para la impresora y pase ese identificador a un constructor [**gráfico**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="14881-105">To draw on a printer, obtain a device context handle for the printer and pass that handle to a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) constructor.</span></span> <span data-ttu-id="14881-106">Coloque los comandos de dibujo de GDI+ entre las llamadas a [StartDoc](/windows/win32/api/wingdi/nf-wingdi-startdocw) y [EndDoc](/windows/win32/api/wingdi/nf-wingdi-enddoc).</span><span class="sxs-lookup"><span data-stu-id="14881-106">Place your GDI+ drawing commands in between calls to [StartDoc](/windows/win32/api/wingdi/nf-wingdi-startdocw) and [EndDoc](/windows/win32/api/wingdi/nf-wingdi-enddoc).</span></span>

<span data-ttu-id="14881-107">En los temas siguientes se explica con más detalle el envío de salidas GDI+ a las impresoras:</span><span class="sxs-lookup"><span data-stu-id="14881-107">The following topics cover sending GDI+ output to printers in more detail:</span></span>

-   [<span data-ttu-id="14881-108">Envío de la salida de GDI+ a una impresora</span><span class="sxs-lookup"><span data-stu-id="14881-108">Sending GDI+ Output to a Printer</span></span>](-gdiplus-sending-gdi-output-to-a-printer-use.md)
-   [<span data-ttu-id="14881-109">Mostrar un cuadro de diálogo de impresión</span><span class="sxs-lookup"><span data-stu-id="14881-109">Displaying a Print Dialog Box</span></span>](-gdiplus-displaying-a-print-dialog-box-use.md)
-   [<span data-ttu-id="14881-110">Optimización de la impresión mediante el suministro de un identificador de impresora</span><span class="sxs-lookup"><span data-stu-id="14881-110">Optimizing Printing by Providing a Printer Handle</span></span>](-gdiplus-optimizing-printing-by-providing-a-printer-handle-use.md)

 

 



