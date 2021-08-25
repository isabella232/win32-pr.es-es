---
description: El Windows GDI+ para dibujar en una impresora es similar al uso de GDI+ para dibujar en la pantalla de un equipo. Para dibujar en una impresora, obtenga un identificador de contexto de dispositivo para la impresora y, a continuación, pase ese identificador a un constructor gráfico.
ms.assetid: a76cca57-6ed8-44cd-a9f6-f2692d14b68a
title: Envío de la salida de GDI+ a una impresora
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51116e27f3ef4e457d2d3cf8d39b26c1a5e2275da4b964bd4de58ec273db1e2b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119943785"
---
# <a name="sending-gdi-output-to-a-printer"></a>Envío de la salida de GDI+ a una impresora

El Windows GDI+ para dibujar en una impresora es similar al uso de GDI+ para dibujar en la pantalla de un equipo. Para dibujar en una impresora, obtenga un identificador de contexto de dispositivo para la impresora y, a continuación, pase ese identificador a un constructor [**gráfico.**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics)

La siguiente aplicación de consola dibuja una línea, un rectángulo y una elipse en una impresora denominada MyPrinter:


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

   // Get a device context for the printer.
   HDC hdcPrint = CreateDC(NULL, TEXT("\\\\printserver\\print1"), NULL, NULL);

   DOCINFO docInfo;
   ZeroMemory(&docInfo, sizeof(docInfo));
   docInfo.cbSize = sizeof(docInfo);
   docInfo.lpszDocName = "GdiplusPrint";

   StartDoc(hdcPrint, &docInfo);
   StartPage(hdcPrint);
      Graphics* graphics = new Graphics(hdcPrint);
      Pen* pen = new Pen(Color(255, 0, 0, 0));
      graphics->DrawLine(pen, 50, 50, 350, 550);
      graphics->DrawRectangle(pen, 50, 50, 300, 500);
      graphics->DrawEllipse(pen, 50, 50, 300, 500);
      delete pen;
      delete graphics;
   EndPage(hdcPrint);
   EndDoc(hdcPrint);
   
   DeleteDC(hdcPrint);
   GdiplusShutdown(gdiplusToken);
   return 0;
}
```



En el código anterior, los tres comandos de dibujo GDI+ están entre las llamadas a las funciones [StartDoc](/windows/win32/api/wingdi/nf-wingdi-startdocw) y [EndDoc,](/windows/win32/api/wingdi/nf-wingdi-enddoc) cada una de las cuales recibe el identificador de contexto del dispositivo de impresora. Todos los comandos gráficos entre StartDoc y EndDoc se enrutan a un metarchivo temporal. Después de la llamada a EndDoc, el controlador de impresora convierte los datos del metarchivo en el formato requerido por la impresora específica que se está utilizando.

> [!Note]  
> Si la cola no está habilitada para la impresora que se usa, la salida de gráficos no se enruta a un metarchivo. En su lugar, el controlador de impresora procesa los comandos gráficos individuales y, a continuación, los envía a la impresora.

 

Por lo general, no querrá codificar de forma automática el nombre de una impresora como se hizo en la aplicación de consola anterior. Una alternativa a la codificación rígida del nombre es llamar a [GetDefaultPrinter](../printdocs/getdefaultprinter.md) para obtener el nombre de la impresora predeterminada. Antes de llamar a GetDefaultPrinter, debe asignar un búfer lo suficientemente grande como para contener el nombre de la impresora. Puede determinar el tamaño del búfer necesario llamando a GetDefaultPrinter y pasando **NULL** como primer argumento.

> [!Note]  
> La [función GetDefaultPrinter](../printdocs/getdefaultprinter.md) solo se admite en Windows 2000 y versiones posteriores.

 

La siguiente aplicación de consola obtiene el nombre de la impresora predeterminada y, a continuación, dibuja un rectángulo y una elipse en esa impresora. La [**llamada Graphics::D rawRectangle**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) se encuentra entre las llamadas a [StartPage](/windows/win32/api/wingdi/nf-wingdi-startpage) y [EndPage](/windows/win32/api/wingdi/nf-wingdi-endpage), por lo que el rectángulo está en una página por sí mismo. De forma similar, la elipse está en una página por sí misma.


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

   DWORD size;
   HDC hdcPrint;

   DOCINFO docInfo;
   ZeroMemory(&docInfo, sizeof(docInfo));
   docInfo.cbSize = sizeof(docInfo);
   docInfo.lpszDocName = "GdiplusPrint";

   // Get the size of the default printer name.
   GetDefaultPrinter(NULL, &size);

   // Allocate a buffer large enough to hold the printer name.
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

      StartDoc(hdcPrint, &docInfo);
         Graphics* graphics;
         Pen* pen = new Pen(Color(255, 0, 0, 0));

         StartPage(hdcPrint);
            graphics = new Graphics(hdcPrint);
            graphics->DrawRectangle(pen, 50, 50, 200, 300);
            delete graphics;
         EndPage(hdcPrint);

         StartPage(hdcPrint);
            graphics = new Graphics(hdcPrint);
            graphics->DrawEllipse(pen, 50, 50, 200, 300);
            delete graphics;
         EndPage(hdcPrint);

         delete pen;
      EndDoc(hdcPrint);

      DeleteDC(hdcPrint);
   }

   delete buffer;

   GdiplusShutdown(gdiplusToken);
   return 0;
}
```



 

 
