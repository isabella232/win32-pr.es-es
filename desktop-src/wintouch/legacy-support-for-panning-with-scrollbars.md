---
title: Compatibilidad heredada con la panorámica con barras de desplazamiento
description: En esta sección se describe la compatibilidad con la panorámica mediante barras de desplazamiento en aplicaciones basadas en Windows.
ms.assetid: a8906b48-b804-4f3a-bb9b-dc94b632e2f7
keywords:
- Windows Touch, compatibilidad heredada
- panorámica con barras de desplazamiento
- Windows Touch, panorámica con barras de desplazamiento
- Windows Touch, barras de desplazamiento
- barras de desplazamiento, movimiento panorámico
- barras de desplazamiento, compatibilidad heredada
- Windows Touch, gestos
- gestos, panorámica con barras de desplazamiento
- Windows Touch, gestos
- gestos, panorámica con barras de desplazamiento
- gestos, deshabilitar
- Windows Touch, mensajes de la rueda del mouse
- mensajes de la rueda del mouse
- Windows Touch, personalización de movimiento panorámico
- movimiento panorámico, barras de desplazamiento
- panorámica, compatibilidad heredada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57f6b9dd47821205a6aa5b6f07e5053e31597358
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104571479"
---
# <a name="legacy-support-for-panning-with-scroll-bars"></a>Compatibilidad heredada con la panorámica con barras de desplazamiento

En esta sección se describe la compatibilidad con la panorámica mediante barras de desplazamiento en aplicaciones basadas en Windows.

En Windows 7, los gestos de movimiento panorámico generan \_ \* mensajes de desplazamiento de WM para habilitar la compatibilidad heredada con el movimiento panorámico. Dado que es posible que las aplicaciones no admitan todos los mensajes de desplazamiento de WM \_ \* , puede que la panorámica no funcione correctamente. En este tema se describen los pasos que debe seguir para asegurarse de que la experiencia de movimiento panorámico heredada en las aplicaciones funcione como se espera en los usuarios.

## <a name="overview"></a>Información general

En las secciones siguientes se explica cómo habilitar la experiencia de movimiento panorámico heredada:

-   Cree una aplicación con barras de desplazamiento.
-   Deshabilitar gestos.
-   Personalizar la experiencia de movimiento panorámico.

## <a name="create-an-application-with-scroll-bars"></a>Crear una aplicación con barras de desplazamiento

Inicie un nuevo proyecto de Win32 con el Asistente para Microsoft Visual Studio. Asegúrese de que el tipo de aplicación está establecido en la aplicación Windows. No es necesario habilitar la compatibilidad con el Active Template Library (ATL). En la imagen siguiente se muestra el aspecto que tendrá el proyecto después de haberse iniciado.

![captura de pantalla que muestra una ventana sin barras de desplazamiento](images/gpd-1.png)

A continuación, habilite las barras de desplazamiento en la imagen. Cambie el código de creación de la ventana en **InitInstance** para que la llamada a la función [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) cree una ventana con barras de desplazamiento. El código siguiente muestra cómo hacerlo.


```C++
   hWnd = CreateWindow(
      szWindowClass, 
      szTitle, 
      WS_OVERLAPPEDWINDOW | WS_VSCROLL,  // style
      200,                               // x
      200,                               // y
      550,                               // width
      300,                               // height
      NULL,
      NULL,
      hInstance,
      NULL
    );  
```



Después de cambiar el código de creación de la ventana, la aplicación tendrá una barra de desplazamiento. En la imagen siguiente se muestra el aspecto que podría tener la aplicación en este punto.

![captura de pantalla que muestra una ventana con una barra de desplazamiento vertical pero sin texto](images/gpd-2.png)

Después de cambiar el código de creación de la ventana, agregue un objeto de barra de desplazamiento a la aplicación y texto para desplazarse. Coloque el código siguiente en la parte superior del método **WndProc** .


```C++
    TEXTMETRIC tm;     
    SCROLLINFO si; 
     
    // These variables are required to display text. 
    static int xClient;     // width of client area 
    static int yClient;     // height of client area 
    static int xClientMax;  // maximum width of client area 
     
    static int xChar;       // horizontal scrolling unit 
    static int yChar;       // vertical scrolling unit 
    static int xUpper;      // average width of uppercase letters 
     
    static int xPos;        // current horizontal scrolling position 
    static int yPos;        // current vertical scrolling position 
     
    int i;                  // loop counter 
    int x, y;               // horizontal and vertical coordinates
     
    int FirstLine;          // first line in the invalidated area 
    int LastLine;           // last line in the invalidated area 
    HRESULT hr;
    int abcLength = 0;  // length of an abc[] item

    int lines = 0;

    // Create an array of lines to display. 
    static const int LINES=28;
    static LPCWSTR abc[] = { 
       L"anteater",  L"bear",      L"cougar", 
       L"dingo",     L"elephant",  L"falcon", 
       L"gazelle",   L"hyena",     L"iguana", 
       L"jackal",    L"kangaroo",  L"llama", 
       L"moose",     L"newt",      L"octopus", 
       L"penguin",   L"quail",     L"rat", 
       L"squid",     L"tortoise",  L"urus", 
       L"vole",      L"walrus",    L"xylophone", 
       L"yak",       L"zebra",
       L"This line contains words, but no character. Go figure.",
       L""
     };        
```



A continuación, implemente la lógica de la aplicación para configurar los cálculos de texto para las métricas de texto. El código siguiente debe reemplazar el caso existente de **\_ Create de WM** en la función **WndProc** .


```C++
    case WM_CREATE : 
        // Get the handle to the client area's device context. 
        hdc = GetDC (hWnd); 
 
        // Extract font dimensions from the text metrics. 
        GetTextMetrics (hdc, &tm); 
        xChar = tm.tmAveCharWidth; 
        xUpper = (tm.tmPitchAndFamily & 1 ? 3 : 2) * xChar/2; 
        yChar = tm.tmHeight + tm.tmExternalLeading; 
 
        // Free the device context. 
        ReleaseDC (hWnd, hdc); 
 
        // Set an arbitrary maximum width for client area. 
        // (xClientMax is the sum of the widths of 48 average 
        // lowercase letters and 12 uppercase letters.) 
        xClientMax = 48 * xChar + 12 * xUpper; 
 
        return 0;
```



A continuación, implemente la lógica de la aplicación para volver a calcular el bloque de texto cuando se cambie el tamaño de la ventana. El código siguiente debe colocarse en el cambio de mensaje en **WndProc**.


```C++
    case WM_SIZE: 
 
        // Retrieve the dimensions of the client area. 
        yClient = HIWORD (lParam); 
        xClient = LOWORD (lParam); 
 
        // Set the vertical scrolling range and page size
        si.cbSize = sizeof(si); 
        si.fMask  = SIF_RANGE | SIF_PAGE; 
        si.nMin   = 0; 
        si.nMax   = LINES - 1; 
        si.nPage  = yClient / yChar; 
        SetScrollInfo(hWnd, SB_VERT, &si, TRUE); 
 
        // Set the horizontal scrolling range and page size. 
        si.cbSize = sizeof(si); 
        si.fMask  = SIF_RANGE | SIF_PAGE; 
        si.nMin   = 0; 
        si.nMax   = 2 + xClientMax / xChar; 
        si.nPage  = xClient / xChar; 
        SetScrollInfo(hWnd, SB_HORZ, &si, TRUE);            
        return 0;
```



A continuación, implemente la lógica de la aplicación para los mensajes de desplazamiento vertical. El código siguiente debe colocarse en el cambio de mensaje en **WndProc**.


```C++
        case WM_VSCROLL:
         // Get all the vertical scroll bar information
         si.cbSize = sizeof (si);
         si.fMask  = SIF_ALL;
         GetScrollInfo (hWnd, SB_VERT, &si);
         // Save the position for comparison later on
         yPos = si.nPos;
         switch (LOWORD (wParam))
         {
         // user clicked the HOME keyboard key
         case SB_TOP:
             si.nPos = si.nMin;
             break;
              
         // user clicked the END keyboard key
         case SB_BOTTOM:
             si.nPos = si.nMax;
             break;
              
         // user clicked the top arrow
         case SB_LINEUP:
             si.nPos -= 1;
             break;
              
         // user clicked the bottom arrow
         case SB_LINEDOWN:
             si.nPos += 1;
             break;
              
         // user clicked the scroll bar shaft above the scroll box
         case SB_PAGEUP:
             si.nPos -= si.nPage;
             break;
              
         // user clicked the scroll bar shaft below the scroll box
         case SB_PAGEDOWN:
             si.nPos += si.nPage;
             break;
              
         // user dragged the scroll box
         case SB_THUMBTRACK:
             si.nPos = si.nTrackPos;
             break;

         // user positioned the scroll box
         // This message is the one used by Windows Touch
         case SB_THUMBPOSITION:
             si.nPos = HIWORD(wParam);
             break;
                            
         default:
              break; 
         }
         // Set the position and then retrieve it.  Due to adjustments
         //   by Windows it may not be the same as the value set.
         si.fMask = SIF_POS;
         SetScrollInfo (hWnd, SB_VERT, &si, TRUE);
         GetScrollInfo (hWnd, SB_VERT, &si);
         // If the position has changed, scroll window and update it
         if (si.nPos != yPos)
         {                    
          ScrollWindow(hWnd, 0, yChar * (yPos - si.nPos), NULL, NULL);
          UpdateWindow (hWnd);
         }
         break;
```



A continuación, actualice el código para volver a dibujar la ventana. El código siguiente debe reemplazar el caso **de \_ Paint de WM** predeterminado en **WndProc**.


```C++
    case WM_PAINT:
         // Prepare the window for painting
         hdc = BeginPaint (hWnd, &ps);
         // Get vertical scroll bar position
         si.cbSize = sizeof (si);
         si.fMask  = SIF_POS;
         GetScrollInfo (hWnd, SB_VERT, &si);
         yPos = si.nPos;
         // Get horizontal scroll bar position
         GetScrollInfo (hWnd, SB_HORZ, &si);
         xPos = si.nPos;
         // Find painting limits
         FirstLine = max (0, yPos + ps.rcPaint.top / yChar);
         LastLine = min (LINES - 1, yPos + ps.rcPaint.bottom / yChar);
         
         
         
         for (i = FirstLine; i <= LastLine; i++)         
         {
              x = xChar * (1 - xPos);
              y = yChar * (i - yPos);
              
              // Note that "55" in the following depends on the 
              // maximum size of an abc[] item.
              //
              abcLength = wcslen(abc[i]);
              hr = S_OK;
              if ((FAILED(hr)))
              {
                 MessageBox(hWnd, L"err", L"err", NULL);
              }else{
                  TextOut(hdc, x, y, abc[i], abcLength);
              }
              
         }
         // Indicate that painting is finished
         EndPaint (hWnd, &ps);
         return 0;
```



Ahora, al compilar y ejecutar la aplicación, debe tener el texto reutilizable y una barra de desplazamiento vertical. En la imagen siguiente se muestra el aspecto que podría tener la aplicación.

![captura de pantalla que muestra una ventana con una barra de desplazamiento vertical y texto](images/gpd-3.png)

## <a name="disable-flicks"></a>Deshabilitar gestos

Para mejorar la experiencia de movimiento panorámico en la aplicación, debe desactivar los gestos. Para ello, establezca las propiedades de la ventana en el valor *hWnd* cuando se inicializa. Los valores usados para los gestos se almacenan en el encabezado tpcshrd. h, que también se debe incluir. El código siguiente debe colocarse en las directivas de inclusión y en la función **InitInstance** después de haber creado el *hWnd*.

> [!Note]  
> Esto resulta útil para las aplicaciones que requieren comentarios inmediatos sobre un evento Touch o Pen Down en lugar de probar un umbral de tiempo o de distancia.

 


```C++
#include <tpcshrd.h>
```




```C++
[...]
BOOL InitInstance(HINSTANCE hInstance, int nCmdShow){
[...]
  
```




```C++
   const DWORD_PTR dwHwndTabletProperty = 
    TABLET_DISABLE_PRESSANDHOLD | // disables press and hold (right-click) gesture
    TABLET_DISABLE_PENTAPFEEDBACK | // disables UI feedback on pen up (waves)
    TABLET_DISABLE_PENBARRELFEEDBACK | // disables UI feedback on pen button down (circle)
    TABLET_DISABLE_FLICKS; // disables pen flicks (back, forward, drag down, drag up)
   
   SetProp(hWnd, MICROSOFT_TABLETPENSERVICE_PROPERTY, reinterpret_cast<HANDLE>(dwHwndTabletProperty));
```



## <a name="customize-the-panning-experience"></a>Personalización de la experiencia de movimiento panorámico

Es posible que desee una experiencia de movimiento panorámico diferente a la de las ofertas de Windows 7 de forma predeterminada. Para mejorar la experiencia de movimiento panorámico, debe agregar el controlador para el mensaje de [**\_ gesto de WM**](wm-gesture.md) . Para obtener más información, consulte [mejorar la experiencia de movimiento panorámico Single-Finger](improving-the-single-finger-panning-experience.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Gestos táctiles de Windows](guide-multi-touch-gestures.md)
</dt> </dl>

 

 