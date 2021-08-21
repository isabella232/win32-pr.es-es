---
title: Tareas iniciales con Windows táctiles
description: En esta sección se describen los pasos básicos para usar gestos multitáctil.
ms.assetid: 0ffe222a-a0ac-498b-a4ca-85cfb1caba93
keywords:
- Windows Táctil, gestos
- Windows Touch,messages
- gestos, acerca de
- gestos, mensajes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c47b114eebc80946652d7118cc4eaab23092b779fa8897053aae229072fbc428
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118030342"
---
# <a name="getting-started-with-windows-touch-gestures"></a>Tareas iniciales con Windows táctiles

En esta sección se describen los pasos básicos para usar gestos multitáctil.

Normalmente, los pasos siguientes se realizan al usar Windows táctiles:

1.  Configure una ventana para recibir gestos.
2.  Controle los mensajes de gesto.
3.  Interpretar los mensajes de gesto.

## <a name="setting-up-a-window-to-receive-gestures"></a>Configuración de una ventana para recibir gestos

De forma predeterminada, recibe mensajes [**\_ WM GESTURE.**](wm-gesture.md)

> [!Note]  
> Si llama a [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow), dejará de recibir mensajes [**\_ WM GESTURE.**](wm-gesture.md) Si no recibe mensajes **DE WM \_ GESTURE,** asegúrese de que no ha llamado a **RegisterTouchWindow.**

 

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



## <a name="handling-gesture-messages"></a>Control de mensajes de gesto

De forma similar a Windows los mensajes de entrada táctiles, puede controlar los mensajes de gestos de muchas maneras. Si usa Win32, puede buscar el mensaje [**WM \_ GESTURE**](wm-gesture.md) en WndProc. Si va a crear otro tipo de aplicación, puede agregar el mensaje **WM \_ GESTURE** al mapa de mensajes y, a continuación, implementar un controlador personalizado.

El código siguiente muestra cómo se podrían controlar los mensajes de gestos.


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



## <a name="interpreting-the-gesture-messages"></a>Interpretación de los mensajes de gesto

La [**función GetGestureInfo**](/windows/desktop/api/winuser/nf-winuser-getgestureinfo) se usa para interpretar un mensaje de gesto en una estructura que describe el gesto. La [**estructura, GESTUREINFO**](/windows/win32/api/winuser/ns-winuser-gestureinfo), tiene información sobre el gesto, como la ubicación donde se realizó el gesto y el tipo de gesto. El código siguiente muestra cómo recuperar e interpretar un mensaje de gesto.


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

[Windows Gestos táctiles](guide-multi-touch-gestures.md)
</dt> </dl>

 

 




