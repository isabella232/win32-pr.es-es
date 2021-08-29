---
description: En el ejemplo siguiente se usa la función ExitWindows para cerrar la sesión del usuario actual.
ms.assetid: 74be3505-c4bd-4ae2-aaed-700382839006
title: Cómo cerrar la sesión del usuario actual
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 029f7b1a68973f248162871572284a2dd20ffaaf34618a7e986035abf5f78f89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119664385"
---
# <a name="how-to-log-off-the-current-user"></a>Cómo cerrar la sesión del usuario actual

En el ejemplo siguiente se usa [**la función ExitWindows**](/windows/desktop/api/Winuser/nf-winuser-exitwindows) para cerrar la sesión del usuario actual.

``` syntax
// Log off the current user. 

ExitWindows(0, 0);
```

En el ejemplo siguiente se usa [**la función ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) para cerrar la sesión del usuario actual.

``` syntax
// Log off the current user. 

ExitWindowsEx(EWX_LOGOFF, 0);
```

La aplicación recibe el [**mensaje WM \_ QUERYENDSESSION**](wm-queryendsession.md) y muestra un cuadro de diálogo que pregunta si es correcto finalizar la sesión. Si el usuario hace clic **en Sí**, el sistema cierra la sesión del usuario. Si el usuario hace clic **en No**, se cancela el cierre de sesión.

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

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Cerrar sesión](logging-off.md)
</dt> </dl>

 

 



