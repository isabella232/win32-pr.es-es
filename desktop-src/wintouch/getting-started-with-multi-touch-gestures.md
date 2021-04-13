---
title: Introducción con gestos táctiles de Windows
description: En esta sección se describen los pasos básicos para usar gestos de multitoque.
ms.assetid: 0ffe222a-a0ac-498b-a4ca-85cfb1caba93
keywords:
- Windows Touch, gestos
- Windows Touch, mensajes
- gestos, acerca de
- gestos, mensajes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 506fee0667e6eb38469bda10af9ded0ea6d3439f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418405"
---
# <a name="getting-started-with-windows-touch-gestures"></a>Introducción con gestos táctiles de Windows

En esta sección se describen los pasos básicos para usar gestos de multitoque.

Normalmente, los siguientes pasos se realizan al usar gestos táctiles de Windows:

1.  Configurar una ventana para recibir gestos.
2.  Controle los mensajes de gestos.
3.  Interprete los mensajes de gestos.

## <a name="setting-up-a-window-to-receive-gestures"></a>Configuración de una ventana para recibir gestos

De forma predeterminada, recibe mensajes de [**\_ gestos de WM**](wm-gesture.md) .

> [!Note]  
> Si llama a [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow), dejará de recibir mensajes de [**\_ gestos de WM**](wm-gesture.md) . Si no recibe mensajes de **\_ gestos de WM** , asegúrese de que no ha llamado a **RegisterTouchWindow**.

 

En el código siguiente se muestra una implementación de InitInstance simple.


```C++
#include <windows.h>


BOOL InitInstance(HINSTANCE hInstance, int nCmdShow)
{
   HWND hWnd;

   hInst = hInstance; // Store instance handle in our global variable

   hWnd = CreateWindow(szWindowClass, szTitle, WS_OVERLAPPEDWINDOW,
      CW_USEDEFAULT, 0, CW_USEDEFAULT, 0, NULL, NULL, hInstance, NULL);

   if (!hWnd)
   {
      return FALSE;
   }

   ShowWindow(hWnd, nCmdShow);
   UpdateWindow(hWnd);

   return TRUE;
}
```



## <a name="handling-gesture-messages"></a>Control de mensajes de gestos

De forma similar a la administración de mensajes de entrada táctiles de Windows, puede controlar los mensajes de gestos de muchas maneras. Si está utilizando Win32, puede buscar el mensaje de [**\_ gestos de WM**](wm-gesture.md) en WndProc. Si va a crear otro tipo de aplicación, puede Agregar el mensaje **de \_ movimiento de WM** al mapa de mensajes y, a continuación, implementar un controlador personalizado.

En el código siguiente se muestra cómo se pueden controlar los mensajes de gestos.


```C++
LRESULT CALLBACK WndProc(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam)
{
    int wmId, wmEvent;
    PAINTSTRUCT ps;
    HDC hdc;

    switch (message)
    {    
    case WM_GESTURE:
            // Insert handler code here to interpret the gesture.            
            return DecodeGesture(hWnd, message, wParam, lParam);            
```



## <a name="interpreting-the-gesture-messages"></a>Interpretar los mensajes de gestos

La función [**GetGestureInfo**](/windows/desktop/api/winuser/nf-winuser-getgestureinfo) se usa para interpretar un mensaje de gesto en una estructura que describe el gesto. La estructura [**GESTUREINFO**](/windows/win32/api/winuser/ns-winuser-gestureinfo)contiene información sobre el gesto, como la ubicación en la que se realizó el gesto y el tipo de gesto. En el código siguiente se muestra cómo se puede recuperar e interpretar un mensaje de gesto.


```C++
  LRESULT DecodeGesture(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam){
    // Create a structure to populate and retrieve the extra message info.
    GESTUREINFO gi;  
    
    ZeroMemory(&gi, sizeof(GESTUREINFO));
    
    gi.cbSize = sizeof(GESTUREINFO);

    BOOL bResult  = GetGestureInfo((HGESTUREINFO)lParam, &gi);
    BOOL bHandled = FALSE;

    if (bResult){
        // now interpret the gesture
        switch (gi.dwID){
           case GID_ZOOM:
               // Code for zooming goes here     
               bHandled = TRUE;
               break;
           case GID_PAN:
               // Code for panning goes here
               bHandled = TRUE;
               break;
           case GID_ROTATE:
               // Code for rotation goes here
               bHandled = TRUE;
               break;
           case GID_TWOFINGERTAP:
               // Code for two-finger tap goes here
               bHandled = TRUE;
               break;
           case GID_PRESSANDTAP:
               // Code for roll over goes here
               bHandled = TRUE;
               break;
           default:
               // A gesture was not recognized
               break;
        }
    }else{
        DWORD dwErr = GetLastError();
        if (dwErr > 0){
            //MessageBoxW(hWnd, L"Error!", L"Could not retrieve a GESTUREINFO structure.", MB_OK);
        }
    }
    if (bHandled){
        return 0;
    }else{
        return DefWindowProc(hWnd, message, wParam, lParam);
    }
  }
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Gestos táctiles de Windows](guide-multi-touch-gestures.md)
</dt> </dl>

 

 




