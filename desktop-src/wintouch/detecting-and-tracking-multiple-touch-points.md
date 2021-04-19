---
title: Detección y seguimiento de varios puntos táctiles
description: Detección y seguimiento de varios puntos táctiles
ms.assetid: 7a5c7595-f341-4e11-805f-ed0b9c63cbff
keywords:
- Windows Touch, varios puntos táctiles
- detección de varios puntos táctiles
- seguimiento de varios puntos táctiles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13b9eaf665b850eea8925bd531ffd1e9ec3fcf40
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104488051"
---
# <a name="detecting-and-tracking-multiple-touch-points"></a>Detección y seguimiento de varios puntos táctiles

En los pasos siguientes se explica cómo realizar un seguimiento de varios puntos táctiles mediante Windows Touch.

1.  Cree una aplicación y habilite Windows Touch.
2.  Agregue un controlador para los puntos [**\_ táctiles**](wm-touchdown.md) y de seguimiento de WM.
3.  Dibuje los puntos.

Una vez que la aplicación se esté ejecutando, representará los círculos en cada toque. En la siguiente captura de pantalla se muestra el aspecto que tendrá la aplicación mientras se ejecuta.

![captura de pantalla que muestra una aplicación que representa los puntos táctiles como círculos verdes y amarillos](images/multitouchpoints.png)

## <a name="create-an-application-and-enable-windows-touch"></a>Creación de una aplicación y habilitación de Windows Touch

Comience con una aplicación de Microsoft Win32 mediante el Asistente para Microsoft Visual Studio. Una vez completado el asistente, agregue compatibilidad para los mensajes de Windows Touch estableciendo la versión de Windows en targetver. h e incluyendo Windows. h y windowsx. h en la aplicación. En el código siguiente se muestra cómo establecer la versión de Windows en targetver. h.


```C++
#ifndef WINVER                  // Specifies that the minimum required platform is Windows 7.
#define WINVER 0x0601           // Change this to the appropriate value to target other versions of Windows.
#endif

#ifndef _WIN32_WINNT            // Specifies that the minimum required platform is Windows 7.
#define _WIN32_WINNT 0x0601     // Change this to the appropriate value to target other versions of Windows.
#endif     

#ifndef _WIN32_WINDOWS          // Specifies that the minimum required platform is Windows 98.
#define _WIN32_WINDOWS 0x0410 // Change this to the appropriate value to target Windows Me or later.
#endif

#ifndef _WIN32_IE                       // Specifies that the minimum required platform is Internet Explorer 7.0.
#define _WIN32_IE 0x0700        // Change this to the appropriate value to target other versions of IE.
#endif
```



En el código siguiente se muestra cómo se deben agregar las directivas de inclusión. Además, puede crear algunas variables globales que se usarán más adelante.


```C++
#include <windows.h>    // included for Windows Touch
#include <windowsx.h>   // included for point conversion

#define MAXPOINTS 10

// You will use this array to track touch points
int points[MAXPOINTS][2];

// You will use this array to switch the color / track ids
int idLookup[MAXPOINTS];


// You can make the touch points larger
// by changing this radius value
static int radius      = 50;

// There should be at least as many colors
// as there can be touch points so that you
// can have different colors for each point
COLORREF colors[] = { RGB(153,255,51), 
                      RGB(153,0,0), 
                      RGB(0,153,0), 
                      RGB(255,255,0), 
                      RGB(255,51,204), 
                      RGB(0,0,0),
                      RGB(0,153,0), 
                      RGB(153, 255, 255), 
                      RGB(153,153,255), 
                      RGB(0,51,153)
                    };

```



## <a name="add-handler-for-wm_touch-and-track-points"></a>Agregar controlador para los \_ puntos táctiles y de seguimiento de WM

En primer lugar, declare algunas variables que usa el controlador [**\_ táctil de WM**](wm-touchdown.md) en [**WndProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)).


```C++
int wmId, wmEvent, i, x, y;

UINT cInputs;
PTOUCHINPUT pInputs;
POINT ptInput;   
```



Ahora, inicialice las variables usadas para almacenar los puntos táctiles y registre la ventana para la entrada táctil desde el método **InitInstance** .


```C++
BOOL InitInstance(HINSTANCE hInstance, int nCmdShow)
{
   HWND hWnd;

   hInst = hInstance; // Store instance handle in our global variable

   hWnd = CreateWindow(szWindowClass, szTitle, WS_OVERLAPPEDWINDOW,
      CW_USEDEFAULT, 0, CW_USEDEFAULT, 0, NULL, NULL, hInstance, NULL);

   if (!hWnd) {
      return FALSE;
   }

   // register the window for touch instead of gestures
   RegisterTouchWindow(hWnd, 0);  

   // the following code initializes the points
   for (int i=0; i< MAXPOINTS; i++){
     points[i][0] = -1;
     points[i][1] = -1;
     idLookup[i]  = -1;
   }  

   ShowWindow(hWnd, nCmdShow);
   UpdateWindow(hWnd);

   return TRUE;
}
```



A continuación, controle el mensaje de [**\_ pantalla táctil de WM**](wm-touchdown.md) desde el método [**WndProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) . En el código siguiente se muestra una implementación del controlador para la **\_ función táctil de WM**.


```C++
case WM_TOUCH:        
  cInputs = LOWORD(wParam);
  pInputs = new TOUCHINPUT[cInputs];
  if (pInputs){
    if (GetTouchInputInfo((HTOUCHINPUT)lParam, cInputs, pInputs, sizeof(TOUCHINPUT))){
      for (int i=0; i < static_cast<INT>(cInputs); i++){
        TOUCHINPUT ti = pInputs[i];
        index = GetContactIndex(ti.dwID);
        if (ti.dwID != 0 && index < MAXPOINTS){                            
          // Do something with your touch input handle
          ptInput.x = TOUCH_COORD_TO_PIXEL(ti.x);
          ptInput.y = TOUCH_COORD_TO_PIXEL(ti.y);
          ScreenToClient(hWnd, &ptInput);
          
          if (ti.dwFlags & TOUCHEVENTF_UP){                      
            points[index][0] = -1;
            points[index][1] = -1;                
          }else{
            points[index][0] = ptInput.x;
            points[index][1] = ptInput.y;                
          }
        }
      }
    }
    // If you handled the message and don't want anything else done with it, you can close it
    CloseTouchInputHandle((HTOUCHINPUT)lParam);
    delete [] pInputs;
  }else{
    // Handle the error here 
  }  
```



> [!Note]  
> Para poder usar la función [**ScreenToClient**](/windows/desktop/api/winuser/nf-winuser-screentoclient) , debe tener compatibilidad con PPP alta en la aplicación. Para obtener más información acerca de la compatibilidad con alta resolución de PPP, consulte la sección [alta de PPP]( ../hidpi/high-dpi-desktop-application-development-on-windows.md) de MSDN.

 

Ahora, cuando un usuario toca la pantalla, las posiciones en las que está tocando se almacenarán en la matriz de puntos. El miembro **dwID** de la estructura [**TOUCHINPUT**](/windows/win32/api/winuser/ns-winuser-touchinput) almacena un identificador que dependerá del hardware.

Para solucionar el problema del miembro dwID que depende del hardware, el controlador de mayúsculas y minúsculas de [**WM \_**](wm-touchdown.md) usa una función, **GetContactIndex**, que asigna el miembro **dwID** de la estructura [**TOUCHINPUT**](/windows/win32/api/winuser/ns-winuser-touchinput) a un punto que se dibuja en la pantalla. En el código siguiente se muestra una implementación de esta función.


```C++
// This function is used to return an index given an ID
int GetContactIndex(int dwID){
  for (int i=0; i < MAXPOINTS; i++){
    if (idLookup[i] == -1){
      idLookup[i] = dwID;
      return i;
    }else{
      if (idLookup[i] == dwID){
        return i;
      }
    }
  }
  // Out of contacts
  return -1;
}
```



## <a name="draw-the-points"></a>Dibujar los puntos

Declare las siguientes variables para la rutina de dibujo.


```C++
    // For double buffering
    static HDC memDC       = 0;
    static HBITMAP hMemBmp = 0;
    HBITMAP hOldBmp        = 0;
   
    // For drawing / fills
    PAINTSTRUCT ps;
    HDC hdc;
    
    // For tracking dwId to points
    int index;
```



El contexto de presentación de memoria *memDC* se usa para almacenar un contexto de gráficos temporal que se intercambia con el contexto de presentación representado, *HDC*, para eliminar el parpadeo. Implemente la rutina de dibujo, que toma los puntos que ha almacenado y dibuja un círculo en los puntos. En el código siguiente se muestra cómo puede implementar el controlador de [**\_ Paint de WM**](/windows/desktop/gdi/wm-paint) .


```C++
  case WM_PAINT:
    hdc = BeginPaint(hWnd, &ps);    
    RECT client;
    GetClientRect(hWnd, &client);        
  
    // start double buffering
    if (!memDC){
      memDC = CreateCompatibleDC(hdc);
    }
    hMemBmp = CreateCompatibleBitmap(hdc, client.right, client.bottom);
    hOldBmp = (HBITMAP)SelectObject(memDC, hMemBmp);          
  
    FillRect(memDC, &client, CreateSolidBrush(RGB(255,255,255)));
     
    //Draw Touched Points                
    for (i=0; i < MAXPOINTS; i++){        
      SelectObject( memDC, CreateSolidBrush(colors[i]));           
      x = points[i][0];
      y = points[i][1];
      if  (x >0 && y>0){              
        Ellipse(memDC, x - radius, y - radius, x+ radius, y + radius);
      }
    }
  
    BitBlt(hdc, 0,0, client.right, client.bottom, memDC, 0,0, SRCCOPY);      

    EndPaint(hWnd, &ps);
    break;
```



Al ejecutar la aplicación, ahora debería tener un aspecto similar al de la ilustración del principio de esta sección.

Por diversión, puede dibujar algunas líneas adicionales alrededor de los puntos de toque. En la captura de pantalla siguiente se muestra cómo la aplicación podría mirar con algunas líneas adicionales dibujadas alrededor de los círculos.

![captura de pantalla que muestra una aplicación que representa los puntos táctiles como círculos con líneas a través de los centros y la intersección de los bordes de los puntos táctiles](images/multitouchpointsfun.png)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Entrada táctil de Windows](guide-multi-touch-input.md)
</dt> </dl>

 

 