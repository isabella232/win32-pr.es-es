---
description: En este tema se muestra cómo dibujar una línea con GDI Plus.
ms.assetid: 2e7444f8-94a6-40d6-b243-0764e245eec4
title: Dibujo de una línea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5284a178baab624633dd427cad84b35933a72fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985183"
---
# <a name="drawing-a-line"></a><span data-ttu-id="8d4a8-103">Dibujo de una línea</span><span class="sxs-lookup"><span data-stu-id="8d4a8-103">Drawing a Line</span></span>

<span data-ttu-id="8d4a8-104">En este tema se muestra cómo dibujar una línea con GDI Plus.</span><span class="sxs-lookup"><span data-stu-id="8d4a8-104">This topic demonstrates how to draw a line using GDI Plus.</span></span>

<span data-ttu-id="8d4a8-105">Para dibujar una línea en GDI+ de Windows, necesita un objeto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) , un objeto [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) y un objeto [**color**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) .</span><span class="sxs-lookup"><span data-stu-id="8d4a8-105">To draw a line in Windows GDI+ you need a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object, a [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) object, and a [**Color**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) object.</span></span> <span data-ttu-id="8d4a8-106">El objeto **Graphics** proporciona el método [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) y el objeto **Pen** contiene los atributos de la línea, como el color y el ancho.</span><span class="sxs-lookup"><span data-stu-id="8d4a8-106">The **Graphics** object provides the [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) method, and the **Pen** object holds attributes of the line, such as color and width.</span></span> <span data-ttu-id="8d4a8-107">La dirección del objeto **Pen** se pasa como argumento al método **DrawLine** .</span><span class="sxs-lookup"><span data-stu-id="8d4a8-107">The address of the **Pen** object is passed as an argument to the **DrawLine** method.</span></span>

<span data-ttu-id="8d4a8-108">El siguiente programa, que dibuja una línea de (0,0) a (200, 100), consta de tres funciones: **WinMain**, **WndProc** y **OnPaint**.</span><span class="sxs-lookup"><span data-stu-id="8d4a8-108">The following program, which draws a line from (0, 0) to (200, 100), consists of three functions: **WinMain**, **WndProc**, and **OnPaint**.</span></span> <span data-ttu-id="8d4a8-109">Las funciones **WinMain** y **WndProc** proporcionan el código fundamental común a la mayoría de las aplicaciones de Windows.</span><span class="sxs-lookup"><span data-stu-id="8d4a8-109">The **WinMain** and **WndProc** functions provide the fundamental code common to most Windows applications.</span></span> <span data-ttu-id="8d4a8-110">No hay código GDI+ en la función **WndProc** .</span><span class="sxs-lookup"><span data-stu-id="8d4a8-110">There is no GDI+ code in the **WndProc** function.</span></span> <span data-ttu-id="8d4a8-111">La función **WinMain** tiene una pequeña cantidad de código GDI+, es decir, las llamadas necesarias a [**GdiplusStartup**](/windows/win32/api/Gdiplusinit/nf-gdiplusinit-gdiplusstartup) y [**GdiplusShutdown**](/windows/win32/api/Gdiplusinit/nf-gdiplusinit-gdiplusshutdown).</span><span class="sxs-lookup"><span data-stu-id="8d4a8-111">The **WinMain** function has a small amount of GDI+ code, namely the required calls to [**GdiplusStartup**](/windows/win32/api/Gdiplusinit/nf-gdiplusinit-gdiplusstartup) and [**GdiplusShutdown**](/windows/win32/api/Gdiplusinit/nf-gdiplusinit-gdiplusshutdown).</span></span> <span data-ttu-id="8d4a8-112">El código GDI+ que crea realmente un objeto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) y dibuja una línea está en la función **OnPaint** .</span><span class="sxs-lookup"><span data-stu-id="8d4a8-112">The GDI+ code that actually creates a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and draws a line is in the **OnPaint** function.</span></span>

<span data-ttu-id="8d4a8-113">La función **OnPaint** recibe un identificador a un contexto de dispositivo y pasa ese identificador a un constructor de [**gráficos**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="8d4a8-113">The **OnPaint** function receives a handle to a device context and passes that handle to a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) constructor.</span></span> <span data-ttu-id="8d4a8-114">El argumento pasado al constructor [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) es una referencia a un objeto [**color**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) .</span><span class="sxs-lookup"><span data-stu-id="8d4a8-114">The argument passed to the [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) constructor is a reference to a [**Color**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) object.</span></span> <span data-ttu-id="8d4a8-115">Los cuatro números que se pasan al constructor de color representan los componentes alfa, rojo, verde y azul del color.</span><span class="sxs-lookup"><span data-stu-id="8d4a8-115">The four numbers passed to the color constructor represent the alpha, red, green, and blue components of the color.</span></span> <span data-ttu-id="8d4a8-116">El componente alfa determina la transparencia del color; 0 es totalmente transparente y 255 es totalmente opaco.</span><span class="sxs-lookup"><span data-stu-id="8d4a8-116">The alpha component determines the transparency of the color; 0 is fully transparent and 255 is fully opaque.</span></span> <span data-ttu-id="8d4a8-117">Los cuatro números pasados al método [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) representan el punto inicial (0,0) y el punto final (200, 100) de la línea.</span><span class="sxs-lookup"><span data-stu-id="8d4a8-117">The four numbers passed to the [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) method represent the starting point (0, 0) and the ending point (200, 100) of the line.</span></span>


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



<span data-ttu-id="8d4a8-118">Observe la llamada a [**GdiplusStartup**](/windows/win32/api/Gdiplusinit/nf-gdiplusinit-gdiplusstartup) en la función **WinMain** .</span><span class="sxs-lookup"><span data-stu-id="8d4a8-118">Note the call to [**GdiplusStartup**](/windows/win32/api/Gdiplusinit/nf-gdiplusinit-gdiplusstartup) in the **WinMain** function.</span></span> <span data-ttu-id="8d4a8-119">El primer parámetro de la función **GdiplusStartup** es la dirección de un ulong \_ PTR.</span><span class="sxs-lookup"><span data-stu-id="8d4a8-119">The first parameter of the **GdiplusStartup** function is the address of a ULONG\_PTR.</span></span> <span data-ttu-id="8d4a8-120">**GdiplusStartup** rellena esa variable con un token que se pasa posteriormente a la función [**GdiplusShutdown**](/windows/win32/api/Gdiplusinit/nf-gdiplusinit-gdiplusshutdown) .</span><span class="sxs-lookup"><span data-stu-id="8d4a8-120">**GdiplusStartup** fills that variable with a token that is later passed to the [**GdiplusShutdown**](/windows/win32/api/Gdiplusinit/nf-gdiplusinit-gdiplusshutdown) function.</span></span> <span data-ttu-id="8d4a8-121">El segundo parámetro de la función **GdiplusStartup** es la dirección de una estructura [**GdiplusStartupInput**](/windows/win32/api/Gdiplusinit/ns-gdiplusinit-gdiplusstartupinput) .</span><span class="sxs-lookup"><span data-stu-id="8d4a8-121">The second parameter of the **GdiplusStartup** function is the address of a [**GdiplusStartupInput**](/windows/win32/api/Gdiplusinit/ns-gdiplusinit-gdiplusstartupinput) structure.</span></span> <span data-ttu-id="8d4a8-122">El código anterior se basa en el constructor predeterminado **GdiplusStartupInput** para establecer los miembros de la estructura de forma adecuada.</span><span class="sxs-lookup"><span data-stu-id="8d4a8-122">The preceding code relies on the default **GdiplusStartupInput** constructor to set the structure members appropriately.</span></span>

 

 



