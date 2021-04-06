---
description: En el ejemplo siguiente se usa la función ExitWindows para cerrar la sesión del usuario actual.
ms.assetid: 74be3505-c4bd-4ae2-aaed-700382839006
title: Cómo cerrar la sesión del usuario actual
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e59ce625ae7da8a2a4a901fbb1429ab0f9b638c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001935"
---
# <a name="how-to-log-off-the-current-user"></a><span data-ttu-id="c28d8-103">Cómo cerrar la sesión del usuario actual</span><span class="sxs-lookup"><span data-stu-id="c28d8-103">How to Log Off the Current User</span></span>

<span data-ttu-id="c28d8-104">En el ejemplo siguiente se usa la función [**ExitWindows**](/windows/desktop/api/Winuser/nf-winuser-exitwindows) para cerrar la sesión del usuario actual.</span><span class="sxs-lookup"><span data-stu-id="c28d8-104">The following example uses the [**ExitWindows**](/windows/desktop/api/Winuser/nf-winuser-exitwindows) function to log off the current user.</span></span>

``` syntax
// Log off the current user. 

ExitWindows(0, 0);
```

<span data-ttu-id="c28d8-105">En el ejemplo siguiente se usa la función [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) para cerrar la sesión del usuario actual.</span><span class="sxs-lookup"><span data-stu-id="c28d8-105">The following example uses the [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) function to log off the current user.</span></span>

``` syntax
// Log off the current user. 

ExitWindowsEx(EWX_LOGOFF, 0);
```

<span data-ttu-id="c28d8-106">La aplicación recibe el mensaje de [**\_ QUERYENDSESSION de WM**](wm-queryendsession.md) y muestra un cuadro de diálogo preguntando si es correcto para finalizar la sesión.</span><span class="sxs-lookup"><span data-stu-id="c28d8-106">The application receives the [**WM\_QUERYENDSESSION**](wm-queryendsession.md) message and displays a dialog box asking the whether it is OK to end the session.</span></span> <span data-ttu-id="c28d8-107">Si el usuario hace clic en **sí**, el sistema cierra la sesión del usuario.</span><span class="sxs-lookup"><span data-stu-id="c28d8-107">If the user clicks **Yes**, the system logs off the user.</span></span> <span data-ttu-id="c28d8-108">Si el usuario hace clic en **no**, se cancela el cierre de sesión.</span><span class="sxs-lookup"><span data-stu-id="c28d8-108">If the user clicks **No**, the logoff is canceled.</span></span>

``` syntax
// Process the message in the window procedure. 

case WM_QUERYENDSESSION:  
{ 
    int r; 
    r = MessageBox(NULL,(LPCWSTR)L"End the session?",(LPCWSTR)L"WM_QUERYENDSESSION",MB_YESNO);
 
    // Return TRUE to continue, FALSE to stop. 
 
    return r == IDYES; 
    break; 
}
```

## <a name="related-topics"></a><span data-ttu-id="c28d8-109">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c28d8-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c28d8-110">Cerrando sesión</span><span class="sxs-lookup"><span data-stu-id="c28d8-110">Logging Off</span></span>](logging-off.md)
</dt> </dl>

 

 



