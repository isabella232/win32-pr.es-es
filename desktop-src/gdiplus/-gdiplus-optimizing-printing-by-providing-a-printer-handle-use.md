---
description: Uno de los constructores de la clase Graphics recibe un identificador de contexto de dispositivo y un identificador de impresora.
ms.assetid: 9be67cb2-4bf9-4758-af03-7d92dd04feaf
title: Optimización de la impresión mediante el suministro de un identificador de impresora
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a247af3de037e220432c424c408b4055690ff861
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072417"
---
# <a name="optimizing-printing-by-providing-a-printer-handle"></a>Optimización de la impresión mediante el suministro de un identificador de impresora

Uno de los constructores de la clase [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) recibe un identificador de contexto de dispositivo y un identificador de impresora. Al enviar comandos Windows GDI+ a determinadas impresoras PostScript, el rendimiento será mejor si crea el objeto **Graphics** con ese constructor determinado.

La siguiente aplicación de consola llama [a GetDefaultPrinter](../printdocs/getdefaultprinter.md) para obtener el nombre de la impresora predeterminada. El código pasa el nombre de la impresora a [CreateDC](/windows/win32/api/wingdi/nf-wingdi-createdcw) para obtener un identificador de contexto de dispositivo para la impresora. El código también pasa el nombre de la impresora a [OpenPrinter](../printdocs/openprinter.md) para obtener un identificador de impresora. Tanto el identificador de contexto del dispositivo como el identificador de impresora se pasan al constructor [**Graphics.**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) A continuación, se dibujan dos figuras en la impresora.

> [!Note]  
> La [función GetDefaultPrinter](../printdocs/getdefaultprinter.md) solo se admite en Windows 2000 y versiones posteriores.

 


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



 

 
