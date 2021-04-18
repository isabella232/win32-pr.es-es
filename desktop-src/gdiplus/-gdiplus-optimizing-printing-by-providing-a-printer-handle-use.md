---
description: Uno de los constructores de la clase Graphics recibe un identificador de contexto de dispositivo y un identificador de impresora.
ms.assetid: 9be67cb2-4bf9-4758-af03-7d92dd04feaf
title: Optimización de la impresión mediante el suministro de un identificador de impresora
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a247af3de037e220432c424c408b4055690ff861
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984446"
---
# <a name="optimizing-printing-by-providing-a-printer-handle"></a><span data-ttu-id="75cb4-103">Optimización de la impresión mediante el suministro de un identificador de impresora</span><span class="sxs-lookup"><span data-stu-id="75cb4-103">Optimizing Printing by Providing a Printer Handle</span></span>

<span data-ttu-id="75cb4-104">Uno de los constructores de la clase [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) recibe un identificador de contexto de dispositivo y un identificador de impresora.</span><span class="sxs-lookup"><span data-stu-id="75cb4-104">One of the constructors for the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class receives a device context handle and a printer handle.</span></span> <span data-ttu-id="75cb4-105">Cuando se envían comandos GDI+ de Windows a determinadas impresoras PostScript, el rendimiento será mejor si se crea el objeto **Graphics** con ese constructor en particular.</span><span class="sxs-lookup"><span data-stu-id="75cb4-105">When you send Windows GDI+ commands to certain PostScript printers, the performance will be better if you create your **Graphics** object with that particular constructor.</span></span>

<span data-ttu-id="75cb4-106">La siguiente aplicación de consola llama a [GetDefaultPrinter](../printdocs/getdefaultprinter.md) para obtener el nombre de la impresora predeterminada.</span><span class="sxs-lookup"><span data-stu-id="75cb4-106">The following console application calls [GetDefaultPrinter](../printdocs/getdefaultprinter.md) to get the name of the default printer.</span></span> <span data-ttu-id="75cb4-107">El código pasa el nombre de la impresora a [CreateDC](/windows/win32/api/wingdi/nf-wingdi-createdcw) para obtener un identificador de contexto de dispositivo para la impresora.</span><span class="sxs-lookup"><span data-stu-id="75cb4-107">The code passes the printer name to [CreateDC](/windows/win32/api/wingdi/nf-wingdi-createdcw) to obtain a device context handle for the printer.</span></span> <span data-ttu-id="75cb4-108">El código también pasa el nombre de la impresora a [OpenPrinter](../printdocs/openprinter.md) para obtener un identificador de impresora.</span><span class="sxs-lookup"><span data-stu-id="75cb4-108">The code also passes the printer name to [OpenPrinter](../printdocs/openprinter.md) to obtain a printer handle.</span></span> <span data-ttu-id="75cb4-109">Tanto el identificador de contexto del dispositivo como el identificador de la impresora se pasan al constructor de [**gráficos**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="75cb4-109">Both the device context handle and the printer handle are passed to the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) constructor.</span></span> <span data-ttu-id="75cb4-110">A continuación, se dibujan dos figuras en la impresora.</span><span class="sxs-lookup"><span data-stu-id="75cb4-110">Then two figures are drawn on the printer.</span></span>

> [!Note]  
> <span data-ttu-id="75cb4-111">La función [GetDefaultPrinter](../printdocs/getdefaultprinter.md) solo se admite en Windows 2000 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="75cb4-111">The [GetDefaultPrinter](../printdocs/getdefaultprinter.md) function is supported only on Windows 2000 and later.</span></span>

 


```
#include <windows.h>
#include <gdiplus.h>
#include <stdio.h>
using namespace Gdiplus;

INT main()
{
   // Initialize GDI+.
   GdiplusStartupInput gdiplusStartupInput;
   ULONG_PTR gdiplusToken;
   GdiplusStartup(&gdiplusToken, &gdiplusStartupInput, NULL);

   DWORD   size;
   HDC     hdcPrint;
   HANDLE  printerHandle;

   DOCINFO docInfo;
   ZeroMemory(&docInfo, sizeof(docInfo));
   docInfo.cbSize = sizeof(docInfo);
   docInfo.lpszDocName = "GdiplusPrint";

   // Get the length of the printer name.
   GetDefaultPrinter(NULL, &size);
   TCHAR* buffer = new TCHAR[size];

   // Get the printer name.
   if(!GetDefaultPrinter(buffer, &size))
   {
      printf("Failure");
   }
   else
   {
      // Get a device context for the printer.
      hdcPrint = CreateDC(NULL, buffer, NULL, NULL);

      // Get a printer handle.
      OpenPrinter(buffer, &printerHandle, NULL);

      StartDoc(hdcPrint, &docInfo);
      StartPage(hdcPrint);
         Graphics* graphics = new Graphics(hdcPrint, printerHandle);
         Pen* pen = new Pen(Color(255, 0, 0, 0));
         graphics->DrawRectangle(pen, 200, 500, 200, 150);
         graphics->DrawEllipse(pen, 200, 500, 200, 150);
         delete(pen);
         delete(graphics);
      EndPage(hdcPrint);
      EndDoc(hdcPrint);

      ClosePrinter(printerHandle);
      DeleteDC(hdcPrint);
   }

   delete buffer;
   
   GdiplusShutdown(gdiplusToken);
   return 0;
}
```



 

 
