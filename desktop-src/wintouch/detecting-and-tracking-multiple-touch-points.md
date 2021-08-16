---
title: Detección y seguimiento de varios puntos táctiles
description: Detección y seguimiento de varios puntos táctiles
ms.assetid: 7a5c7595-f341-4e11-805f-ed0b9c63cbff
keywords:
- Windows Táctil, varios puntos táctiles
- detectar varios puntos táctiles
- seguimiento de varios puntos táctiles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4a5b8086988dc1a87b5596d5a0ac74ec1f1df5ce4b85d928cbe306b791d17b0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118436075"
---
# <a name="detecting-and-tracking-multiple-touch-points"></a>Detección y seguimiento de varios puntos táctiles

En los pasos siguientes se explica cómo realizar un seguimiento de varios puntos táctiles mediante Windows Touch.

1.  Cree una aplicación y habilite Windows Touch.
2.  Agregue un controlador para [**WM \_ TOUCH y**](wm-touchdown.md) puntos de seguimiento.
3.  Dibuje los puntos.

Una vez que la aplicación se ejecute, se representarán círculos bajo cada toque. En la siguiente captura de pantalla se muestra el aspecto de la aplicación mientras se ejecuta.

![captura de pantalla que muestra una aplicación que representa puntos táctiles como círculos verdes y amarillos](images/multitouchpoints.png)

## <a name="create-an-application-and-enable-windows-touch"></a>Crear una aplicación y habilitar Windows Touch

Comience con una aplicación Win32 de Microsoft mediante el asistente Microsoft Visual Studio aplicaciones. Una vez completado el asistente, agregue compatibilidad con los mensajes de Windows Touch estableciendo la versión de Windows en targetver.h e incluyendo windows.h y windowsx.h en la aplicación. El código siguiente muestra cómo establecer la versión Windows en targetver.h.


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



El código siguiente muestra cómo se deben agregar las directivas include. Además, puede crear algunas variables globales que se usarán más adelante.


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



## <a name="add-handler-for-wm_touch-and-track-points"></a>Agregar controlador para WM \_ TOUCH y puntos de seguimiento

En primer lugar, declare algunas variables usadas por el [**controlador WM \_ TOUCH**](wm-touchdown.md) en [**WndProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)).


```C++
int wmId, wmEvent, i, x, y;

UINT cInputs;
PTOUCHINPUT pInputs;
POINT ptInput;   
```



Ahora, inicialice las variables usadas para almacenar puntos táctiles y registre la ventana para la entrada táctil desde el **método InitInstance.**


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



A continuación, [**controle el mensaje WM \_ TOUCH**](wm-touchdown.md) del [**método WndProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) El código siguiente muestra una implementación del controlador para **WM \_ TOUCH**.


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
> Para usar la función [**ScreenToClient,**](/windows/desktop/api/winuser/nf-winuser-screentoclient) debe tener compatibilidad con valores altos de PPP en la aplicación. Para obtener más información sobre la compatibilidad con valores altos de PPP, consulte la [sección Valores altos de PPP]( ../hidpi/high-dpi-desktop-application-development-on-windows.md) de MSDN.

 

Ahora, cuando un usuario toca la pantalla, las posiciones que está tocándose se almacenarán en la matriz de puntos. El **miembro dwID** de la [**estructura TOUCHINPUT**](/windows/win32/api/winuser/ns-winuser-touchinput) almacena un identificador que dependerá del hardware.

Para solucionar el problema del miembro dwID que depende del hardware, el controlador de casos [**WM \_ TOUCH**](wm-touchdown.md) usa una función, **GetContactIndex**, que asigna el miembro **dwID** de la estructura [**TOUCHINPUT**](/windows/win32/api/winuser/ns-winuser-touchinput) a un punto que se dibuja en la pantalla. El código siguiente muestra una implementación de esta función.


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



El contexto de presentación de memoria *memDC* se usa para almacenar un contexto de gráficos temporal que se intercambia con el contexto de presentación representado, *hdc*, para eliminar el parpadeo. Implemente la rutina de dibujo, que toma los puntos que ha almacenado y dibuja un círculo en los puntos. El código siguiente muestra cómo podría implementar el [**controlador WM \_ PAINT.**](/windows/desktop/gdi/wm-paint)


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



Al ejecutar la aplicación, ahora debería tener un aspecto parecido al de la ilustración al principio de esta sección.

Para disfrutar, puede dibujar algunas líneas adicionales alrededor de los puntos táctiles. En la siguiente captura de pantalla se muestra el aspecto de la aplicación con algunas líneas adicionales dibujadas alrededor de los círculos.

![captura de pantalla que muestra una aplicación que representa puntos táctiles como círculos con líneas a través de los centros e intersección con los bordes de los puntos táctiles](images/multitouchpointsfun.png)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Windows Entrada táctil](guide-multi-touch-input.md)
</dt> </dl>

 

 