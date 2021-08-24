---
description: En este tema se muestra cómo dibujar una línea mediante GDI Plus.
ms.assetid: 2e7444f8-94a6-40d6-b243-0764e245eec4
title: Dibujo de una línea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a1e2a330f24cd0d1771458d02b264cdaa493835477b40c95d05ca4bf71c8a1e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119036813"
---
# <a name="drawing-a-line"></a>Dibujo de una línea

En este tema se muestra cómo dibujar una línea mediante GDI Plus.

Para dibujar una línea en Windows GDI+ necesita un objeto [**Graphics,**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) un objeto [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) y un [**objeto Color.**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) El **objeto Graphics** proporciona el método [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) y el **objeto Pen** contiene atributos de la línea, como el color y el ancho. La dirección del objeto **Pen** se pasa como argumento al **método DrawLine.**

El programa siguiente, que dibuja una línea de (0, 0) a (200, 100), consta de tres funciones: **WinMain,** **WndProc** y **OnPaint**. Las **funciones WinMain** y **WndProc** proporcionan el código fundamental común a la mayoría Windows aplicaciones. No hay ningún GDI+ en la **función WndProc.** La **función WinMain** tiene una pequeña cantidad de GDI+ código, es decir, las llamadas necesarias a [**GdiplusStartup**](/windows/win32/api/Gdiplusinit/nf-gdiplusinit-gdiplusstartup) y [**GdiplusShutdown.**](/windows/win32/api/Gdiplusinit/nf-gdiplusinit-gdiplusshutdown) El GDI+ que realmente crea un [**objeto Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) y dibuja una línea está en la **función OnPaint.**

La **función OnPaint** recibe un identificador a un contexto de dispositivo y pasa ese identificador a un constructor [**Graphics.**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) El argumento pasado al constructor [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) es una referencia a un [**objeto Color.**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) Los cuatro números pasados al constructor de color representan los componentes alfa, rojo, verde y azul del color. El componente alfa determina la transparencia del color; 0 es totalmente transparente y 255 es totalmente opaco. Los cuatro números pasados al método [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) representan el punto inicial (0, 0) y el punto final (200, 100) de la línea.


```C++
#include <stdafx.h>
#include <windows.h>
#include <objidl.h>
#include <gdiplus.h>
using namespace Gdiplus;
#pragma comment (lib,"Gdiplus.lib")

VOID OnPaint(HDC hdc)
{
   Graphics graphics(hdc);
   Pen      pen(Color(255, 0, 0, 255));
   graphics.DrawLine(&pen, 0, 0, 200, 100);
}

LRESULT CALLBACK WndProc(HWND, UINT, WPARAM, LPARAM);

INT WINAPI WinMain(HINSTANCE hInstance, HINSTANCE, PSTR, INT iCmdShow)
{
   HWND                hWnd;
   MSG                 msg;
   WNDCLASS            wndClass;
   GdiplusStartupInput gdiplusStartupInput;
   ULONG_PTR           gdiplusToken;
   
   // Initialize GDI+.
   GdiplusStartup(&gdiplusToken, &gdiplusStartupInput, NULL);
   
   wndClass.style          = CS_HREDRAW | CS_VREDRAW;
   wndClass.lpfnWndProc    = WndProc;
   wndClass.cbClsExtra     = 0;
   wndClass.cbWndExtra     = 0;
   wndClass.hInstance      = hInstance;
   wndClass.hIcon          = LoadIcon(NULL, IDI_APPLICATION);
   wndClass.hCursor        = LoadCursor(NULL, IDC_ARROW);
   wndClass.hbrBackground  = (HBRUSH)GetStockObject(WHITE_BRUSH);
   wndClass.lpszMenuName   = NULL;
   wndClass.lpszClassName  = TEXT("GettingStarted");
   
   RegisterClass(&wndClass);
   
   hWnd = CreateWindow(
      TEXT("GettingStarted"),   // window class name
      TEXT("Getting Started"),  // window caption
      WS_OVERLAPPEDWINDOW,      // window style
      CW_USEDEFAULT,            // initial x position
      CW_USEDEFAULT,            // initial y position
      CW_USEDEFAULT,            // initial x size
      CW_USEDEFAULT,            // initial y size
      NULL,                     // parent window handle
      NULL,                     // window menu handle
      hInstance,                // program instance handle
      NULL);                    // creation parameters
      
   ShowWindow(hWnd, iCmdShow);
   UpdateWindow(hWnd);
   
   while(GetMessage(&msg, NULL, 0, 0))
   {
      TranslateMessage(&msg);
      DispatchMessage(&msg);
   }
   
   GdiplusShutdown(gdiplusToken);
   return msg.wParam;
}  // WinMain

LRESULT CALLBACK WndProc(HWND hWnd, UINT message, 
   WPARAM wParam, LPARAM lParam)
{
   HDC          hdc;
   PAINTSTRUCT  ps;
   
   switch(message)
   {
   case WM_PAINT:
      hdc = BeginPaint(hWnd, &ps);
      OnPaint(hdc);
      EndPaint(hWnd, &ps);
      return 0;
   case WM_DESTROY:
      PostQuitMessage(0);
      return 0;
   default:
      return DefWindowProc(hWnd, message, wParam, lParam);
   }
} // WndProc
```



Observe la llamada a [**GdiplusStartup en**](/windows/win32/api/Gdiplusinit/nf-gdiplusinit-gdiplusstartup) la **función WinMain.** El primer parámetro de la **función GdiplusStartup** es la dirección de un \_ ULONG PTR. **GdiplusStartup** rellena esa variable con un token que se pasa más adelante a la [**función GdiplusShutdown.**](/windows/win32/api/Gdiplusinit/nf-gdiplusinit-gdiplusshutdown) El segundo parámetro de la **función GdiplusStartup** es la dirección de una [**estructura GdiplusStartupInput.**](/windows/win32/api/Gdiplusinit/ns-gdiplusinit-gdiplusstartupinput) El código anterior se basa en el constructor **GdiplusStartupInput** predeterminado para establecer los miembros de la estructura correctamente.

 

 



