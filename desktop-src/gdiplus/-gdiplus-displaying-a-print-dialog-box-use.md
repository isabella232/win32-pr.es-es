---
description: Una manera de obtener un identificador de contexto de dispositivo para una impresora es mostrar un cuadro de diálogo de impresión y permitir al usuario elegir una impresora.
ms.assetid: 73a74186-c916-4ad9-b768-6bc887fd5231
title: Mostrar un cuadro de diálogo Imprimir
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 113c9235e70712a4923ebdc3ad239f533160eb2f84f76ae729d7fadf203ca612
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119036833"
---
# <a name="displaying-a-print-dialog-box"></a>Mostrar un cuadro de diálogo Imprimir

Una manera de obtener un identificador de contexto de dispositivo para una impresora es mostrar un cuadro de diálogo de impresión y permitir al usuario elegir una impresora. La [función PrintDlg](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) (que muestra el cuadro de diálogo) tiene un parámetro que es la dirección de una [estructura PRINTDLG.](/windows/win32/api/commdlg/ns-commdlg-printdlga?redirectedfrom=MSDN) La estructura PRINTDLG tiene varios miembros, pero puede dejar la mayoría de ellos establecidos en sus valores predeterminados. Los dos miembros que debe establecer son **lStructSize** y **Flags.** Establezca **lStructSize en** el tamaño de una variable PRINTDLG y establezca **Flags** en PD \_ RETURNDC. Al **establecer Marcas en** PC RETURNDC se especifica que desea que la función PrintDlg rellene el campo hDC con un identificador de contexto de dispositivo para la impresora elegida \_ por el usuario. 


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
   
   DOCINFO docInfo;
   ZeroMemory(&docInfo, sizeof(docInfo));
   docInfo.cbSize = sizeof(docInfo);
   docInfo.lpszDocName = "GdiplusPrint";
   
   // Create a PRINTDLG structure, and initialize the appropriate fields.
   PRINTDLG printDlg;
   ZeroMemory(&printDlg, sizeof(printDlg));
   printDlg.lStructSize = sizeof(printDlg);
   printDlg.Flags = PD_RETURNDC;
   
   // Display a print dialog box.
   if(!PrintDlg(&printDlg))
   {
      printf("Failure\n");
   }
   else
   {
      // Now that PrintDlg has returned, a device context handle
      // for the chosen printer is in printDlg->hDC.
      
      StartDoc(printDlg.hDC, &docInfo);
      StartPage(printDlg.hDC);
         Graphics* graphics = new Graphics(printDlg.hDC);
         Pen* pen = new Pen(Color(255, 0, 0, 0));
         graphics->DrawRectangle(pen, 200, 500, 200, 150);
         graphics->DrawEllipse(pen, 200, 500, 200, 150);
         graphics->DrawLine(pen, 200, 500, 400, 650);
         delete pen;
         delete graphics;
      EndPage(printDlg.hDC);
      EndDoc(printDlg.hDC); 
   }
   if(printDlg.hDevMode) 
      GlobalFree(printDlg.hDevMode);
   if(printDlg.hDevNames) 
      GlobalFree(printDlg.hDevNames);
   if(printDlg.hDC)
      DeleteDC(printDlg.hDC);
   
   GdiplusShutdown(gdiplusToken);
   return 0;
}
```



 

 
