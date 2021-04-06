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
# <a name="how-to-log-off-the-current-user"></a>Cómo cerrar la sesión del usuario actual

En el ejemplo siguiente se usa la función [**ExitWindows**](/windows/desktop/api/Winuser/nf-winuser-exitwindows) para cerrar la sesión del usuario actual.

``` syntax
// Log off the current user. 

ExitWindows(0, 0);
```

En el ejemplo siguiente se usa la función [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) para cerrar la sesión del usuario actual.

``` syntax
// Log off the current user. 

ExitWindowsEx(EWX_LOGOFF, 0);
```

La aplicación recibe el mensaje de [**\_ QUERYENDSESSION de WM**](wm-queryendsession.md) y muestra un cuadro de diálogo preguntando si es correcto para finalizar la sesión. Si el usuario hace clic en **sí**, el sistema cierra la sesión del usuario. Si el usuario hace clic en **no**, se cancela el cierre de sesión.

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

[Cerrando sesión](logging-off.md)
</dt> </dl>

 

 



