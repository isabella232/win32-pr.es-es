---
title: Crear una ventana de MCIWnd
description: Crear una ventana de MCIWnd
ms.assetid: bd45e813-5807-43cd-bef1-03285df9a018
keywords:
- Ventana de MCIWnd, crear
- MCIWndCreate función)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c205e87acf3e5f529d4b5cc9c9163b7fe887fe04
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105676133"
---
# <a name="creating-an-mciwnd-window"></a><span data-ttu-id="882dd-105">Crear una ventana de MCIWnd</span><span class="sxs-lookup"><span data-stu-id="882dd-105">Creating an MCIWnd Window</span></span>

<span data-ttu-id="882dd-106">La función [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) se registra y crea una ventana MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="882dd-106">The [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) function registers and creates an MCIWnd window.</span></span> <span data-ttu-id="882dd-107">La ventana puede ser una ventana primaria, secundaria o emergente.</span><span class="sxs-lookup"><span data-stu-id="882dd-107">The window can be a parent, child, or pop-up window.</span></span> <span data-ttu-id="882dd-108">En el ejemplo siguiente se crea una ventana de MCIWnd como una ventana secundaria y se permite que el usuario controle la reproducción mediante el acceso a la barra de menús y los botones de **reproducción**, **detención** y **menú** .</span><span class="sxs-lookup"><span data-stu-id="882dd-108">The following example creates an MCIWnd window as a child window and lets the user control playback by providing access to the trackbar and the **Play**, **Stop**, and **Menu** buttons.</span></span> <span data-ttu-id="882dd-109">En el ejemplo se especifica un identificador de una ventana primaria y se especifica **null** para los estilos de ventana, por lo que los estilos de ventana predeterminados WS \_ Child, WS \_ Border y WS \_ visible se usan para crear la ventana MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="882dd-109">The example specifies a handle of a parent window and specifies **NULL** for the window styles, so the default window styles of WS\_CHILD, WS\_BORDER, and WS\_VISIBLE are used to create the MCIWnd window.</span></span>


```C++
// Global variable and constants 
// extern HINSTANCE g_hinst;       instance handle 
// extern HWND g_hwndMCIWnd;       MCIWnd window handle 
 
case WM_COMMAND: 
    switch (wParam) { 
    case IDM_CREATEMCIWND: 
        g_hwndMCIWnd = MCIWndCreate(hwnd, g_hinst, NULL, 
            "sample.avi"); 
        break;    
    } 
    break; 
```



> [!Note]  
> <span data-ttu-id="882dd-110">También puede especificar **null** tanto para el identificador de ventana primario como para los estilos de ventana, en cuyo caso los estilos de ventana predeterminados SERÍAn WS \_ superpuesto y WS \_ visible.</span><span class="sxs-lookup"><span data-stu-id="882dd-110">You could also specify **NULL** for both the parent window handle and the window styles, in which case the default window styles would be WS\_OVERLAPPED and WS\_VISIBLE.</span></span>

 

 

 




