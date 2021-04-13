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
# <a name="getting-started-with-windows-touch-gestures"></a><span data-ttu-id="16067-107">Introducción con gestos táctiles de Windows</span><span class="sxs-lookup"><span data-stu-id="16067-107">Getting Started with Windows Touch Gestures</span></span>

<span data-ttu-id="16067-108">En esta sección se describen los pasos básicos para usar gestos de multitoque.</span><span class="sxs-lookup"><span data-stu-id="16067-108">This section describes the basic steps for using multitouch gestures.</span></span>

<span data-ttu-id="16067-109">Normalmente, los siguientes pasos se realizan al usar gestos táctiles de Windows:</span><span class="sxs-lookup"><span data-stu-id="16067-109">The following steps are typically performed when using Windows Touch gestures:</span></span>

1.  <span data-ttu-id="16067-110">Configurar una ventana para recibir gestos.</span><span class="sxs-lookup"><span data-stu-id="16067-110">Set up a window for receiving gestures.</span></span>
2.  <span data-ttu-id="16067-111">Controle los mensajes de gestos.</span><span class="sxs-lookup"><span data-stu-id="16067-111">Handle the gesture messages.</span></span>
3.  <span data-ttu-id="16067-112">Interprete los mensajes de gestos.</span><span class="sxs-lookup"><span data-stu-id="16067-112">Interpret the gesture messages.</span></span>

## <a name="setting-up-a-window-to-receive-gestures"></a><span data-ttu-id="16067-113">Configuración de una ventana para recibir gestos</span><span class="sxs-lookup"><span data-stu-id="16067-113">Setting up a Window to Receive Gestures</span></span>

<span data-ttu-id="16067-114">De forma predeterminada, recibe mensajes de [**\_ gestos de WM**](wm-gesture.md) .</span><span class="sxs-lookup"><span data-stu-id="16067-114">By default, you receive [**WM\_GESTURE**](wm-gesture.md) messages.</span></span>

> [!Note]  
> <span data-ttu-id="16067-115">Si llama a [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow), dejará de recibir mensajes de [**\_ gestos de WM**](wm-gesture.md) .</span><span class="sxs-lookup"><span data-stu-id="16067-115">If you call [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow), you will stop receiving [**WM\_GESTURE**](wm-gesture.md) messages.</span></span> <span data-ttu-id="16067-116">Si no recibe mensajes de **\_ gestos de WM** , asegúrese de que no ha llamado a **RegisterTouchWindow**.</span><span class="sxs-lookup"><span data-stu-id="16067-116">If you are not receiving **WM\_GESTURE** messages, make sure that you haven't called **RegisterTouchWindow**.</span></span>

 

<span data-ttu-id="16067-117">En el código siguiente se muestra una implementación de InitInstance simple.</span><span class="sxs-lookup"><span data-stu-id="16067-117">The following code shows a simple InitInstance implementation.</span></span>


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



## <a name="handling-gesture-messages"></a><span data-ttu-id="16067-118">Control de mensajes de gestos</span><span class="sxs-lookup"><span data-stu-id="16067-118">Handling Gesture Messages</span></span>

<span data-ttu-id="16067-119">De forma similar a la administración de mensajes de entrada táctiles de Windows, puede controlar los mensajes de gestos de muchas maneras.</span><span class="sxs-lookup"><span data-stu-id="16067-119">Similar to handling Windows Touch input messages, you can handle gesture messages in many ways.</span></span> <span data-ttu-id="16067-120">Si está utilizando Win32, puede buscar el mensaje de [**\_ gestos de WM**](wm-gesture.md) en WndProc.</span><span class="sxs-lookup"><span data-stu-id="16067-120">If you are using Win32, you can check for the [**WM\_GESTURE**](wm-gesture.md) message in WndProc.</span></span> <span data-ttu-id="16067-121">Si va a crear otro tipo de aplicación, puede Agregar el mensaje **de \_ movimiento de WM** al mapa de mensajes y, a continuación, implementar un controlador personalizado.</span><span class="sxs-lookup"><span data-stu-id="16067-121">If you are creating another type of application, you can add the **WM\_GESTURE** message to the message map and then implement a custom handler.</span></span>

<span data-ttu-id="16067-122">En el código siguiente se muestra cómo se pueden controlar los mensajes de gestos.</span><span class="sxs-lookup"><span data-stu-id="16067-122">The following code shows how gesture messages could be handled.</span></span>


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



## <a name="interpreting-the-gesture-messages"></a><span data-ttu-id="16067-123">Interpretar los mensajes de gestos</span><span class="sxs-lookup"><span data-stu-id="16067-123">Interpreting the Gesture Messages</span></span>

<span data-ttu-id="16067-124">La función [**GetGestureInfo**](/windows/desktop/api/winuser/nf-winuser-getgestureinfo) se usa para interpretar un mensaje de gesto en una estructura que describe el gesto.</span><span class="sxs-lookup"><span data-stu-id="16067-124">The [**GetGestureInfo**](/windows/desktop/api/winuser/nf-winuser-getgestureinfo) function is used to interpret a gesture message into a structure describing the gesture.</span></span> <span data-ttu-id="16067-125">La estructura [**GESTUREINFO**](/windows/win32/api/winuser/ns-winuser-gestureinfo)contiene información sobre el gesto, como la ubicación en la que se realizó el gesto y el tipo de gesto.</span><span class="sxs-lookup"><span data-stu-id="16067-125">The structure, [**GESTUREINFO**](/windows/win32/api/winuser/ns-winuser-gestureinfo), has information about the gesture such as the location where the gesture was performed and the type of gesture.</span></span> <span data-ttu-id="16067-126">En el código siguiente se muestra cómo se puede recuperar e interpretar un mensaje de gesto.</span><span class="sxs-lookup"><span data-stu-id="16067-126">The following code shows how you can retrieve and interpret a gesture message.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="16067-127">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="16067-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="16067-128">Gestos táctiles de Windows</span><span class="sxs-lookup"><span data-stu-id="16067-128">Windows Touch Gestures</span></span>](guide-multi-touch-gestures.md)
</dt> </dl>

 

 




