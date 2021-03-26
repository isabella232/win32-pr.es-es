---
description: Usar GDI+ de Windows para dibujar en una impresora es similar a usar GDI+ para dibujar en una pantalla del equipo. Para dibujar en una impresora, obtenga un identificador de contexto de dispositivo para la impresora y, a continuación, pase ese identificador a un constructor gráfico.
ms.assetid: a76cca57-6ed8-44cd-a9f6-f2692d14b68a
title: Envío de la salida de GDI+ a una impresora
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96c1c4f6c05e4918663284e6d7747952040dcddf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082493"
---
# <a name="sending-gdi-output-to-a-printer"></a><span data-ttu-id="a6e62-104">Envío de la salida de GDI+ a una impresora</span><span class="sxs-lookup"><span data-stu-id="a6e62-104">Sending GDI+ Output to a Printer</span></span>

<span data-ttu-id="a6e62-105">Usar GDI+ de Windows para dibujar en una impresora es similar a usar GDI+ para dibujar en una pantalla del equipo.</span><span class="sxs-lookup"><span data-stu-id="a6e62-105">Using Windows GDI+ to draw on a printer is similar to using GDI+ to draw on a computer screen.</span></span> <span data-ttu-id="a6e62-106">Para dibujar en una impresora, obtenga un identificador de contexto de dispositivo para la impresora y, a continuación, pase ese identificador a un constructor [**gráfico**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="a6e62-106">To draw on a printer, obtain a device context handle for the printer and then pass that handle to a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) constructor.</span></span>

<span data-ttu-id="a6e62-107">La siguiente aplicación de consola dibuja una línea, un rectángulo y una elipse en una impresora denominada alprinter:</span><span class="sxs-lookup"><span data-stu-id="a6e62-107">The following console application draws a line, a rectangle, and an ellipse on a printer named MyPrinter:</span></span>


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



<span data-ttu-id="a6e62-108">En el código anterior, los tres comandos de dibujo de GDI+ están entre las llamadas a las funciones [StartDoc](/windows/win32/api/wingdi/nf-wingdi-startdocw) y [EndDoc](/windows/win32/api/wingdi/nf-wingdi-enddoc) , cada una de las cuales recibe el identificador de contexto del dispositivo de impresora.</span><span class="sxs-lookup"><span data-stu-id="a6e62-108">In the preceding code, the three GDI+ drawing commands are in between calls to the [StartDoc](/windows/win32/api/wingdi/nf-wingdi-startdocw) and [EndDoc](/windows/win32/api/wingdi/nf-wingdi-enddoc) functions, each of which receives the printer device context handle.</span></span> <span data-ttu-id="a6e62-109">Todos los comandos de gráficos entre StartDoc y EndDoc se enrutan a un metarchivo temporal.</span><span class="sxs-lookup"><span data-stu-id="a6e62-109">All graphics commands between StartDoc and EndDoc are routed to a temporary metafile.</span></span> <span data-ttu-id="a6e62-110">Después de la llamada a EndDoc, el controlador de impresora convierte los datos del metarchivo en el formato requerido por la impresora específica que se está usando.</span><span class="sxs-lookup"><span data-stu-id="a6e62-110">After the call to EndDoc, the printer driver converts the data in the metafile into the format required by the specific printer being used.</span></span>

> [!Note]  
> <span data-ttu-id="a6e62-111">Si la cola de impresión no está habilitada para la impresora que se está usando, la salida de gráficos no se enruta a un metarchivo.</span><span class="sxs-lookup"><span data-stu-id="a6e62-111">If spooling is not enabled for the printer being used, the graphics output is not routed to a metafile.</span></span> <span data-ttu-id="a6e62-112">En su lugar, los comandos de gráficos individuales los procesa el controlador de impresora y, a continuación, se envían a la impresora.</span><span class="sxs-lookup"><span data-stu-id="a6e62-112">Instead, individual graphics commands are processed by the printer driver and then sent to the printer.</span></span>

 

<span data-ttu-id="a6e62-113">Por lo general, no querrá codificar de forma rígida el nombre de una impresora tal como se hizo en la aplicación de consola anterior.</span><span class="sxs-lookup"><span data-stu-id="a6e62-113">Generally you won't want to hard-code the name of a printer as was done in the preceding console application.</span></span> <span data-ttu-id="a6e62-114">Una alternativa a la codificación rígida del nombre es llamar a [GetDefaultPrinter](../printdocs/getdefaultprinter.md) para obtener el nombre de la impresora predeterminada.</span><span class="sxs-lookup"><span data-stu-id="a6e62-114">One alternative to hard-coding the name is to call [GetDefaultPrinter](../printdocs/getdefaultprinter.md) to obtain the name of the default printer.</span></span> <span data-ttu-id="a6e62-115">Antes de llamar a GetDefaultPrinter, debe asignar un búfer lo suficientemente grande como para contener el nombre de la impresora.</span><span class="sxs-lookup"><span data-stu-id="a6e62-115">Before you call GetDefaultPrinter, you must allocate a buffer large enough to hold the printer name.</span></span> <span data-ttu-id="a6e62-116">Puede determinar el tamaño del búfer necesario llamando a GetDefaultPrinter, pasando **null** como primer argumento.</span><span class="sxs-lookup"><span data-stu-id="a6e62-116">You can determine the size of the required buffer by calling GetDefaultPrinter, passing **NULL** as the first argument.</span></span>

> [!Note]  
> <span data-ttu-id="a6e62-117">La función [GetDefaultPrinter](../printdocs/getdefaultprinter.md) solo se admite en Windows 2000 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="a6e62-117">The [GetDefaultPrinter](../printdocs/getdefaultprinter.md) function is supported only on Windows 2000 and later.</span></span>

 

<span data-ttu-id="a6e62-118">La siguiente aplicación de consola obtiene el nombre de la impresora predeterminada y, a continuación, dibuja un rectángulo y una elipse en esa impresora.</span><span class="sxs-lookup"><span data-stu-id="a6e62-118">The following console application gets the name of the default printer and then draws a rectangle and an ellipse on that printer.</span></span> <span data-ttu-id="a6e62-119">La llamada de [**gráficos::D rawrectangle**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) se encuentra entre las llamadas a [StartPage](/windows/win32/api/wingdi/nf-wingdi-startpage) y [EndPage](/windows/win32/api/wingdi/nf-wingdi-endpage), por lo que el rectángulo está en una página por sí mismo.</span><span class="sxs-lookup"><span data-stu-id="a6e62-119">The [**Graphics::DrawRectangle**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) call is in between calls to [StartPage](/windows/win32/api/wingdi/nf-wingdi-startpage) and [EndPage](/windows/win32/api/wingdi/nf-wingdi-endpage), so the rectangle is on a page by itself.</span></span> <span data-ttu-id="a6e62-120">Del mismo modo, la elipse se encuentra en una página.</span><span class="sxs-lookup"><span data-stu-id="a6e62-120">Similarly, the ellipse is on a page by itself.</span></span>


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



 

 
