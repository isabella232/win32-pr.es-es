---
title: Notificaciones de menú
description: Notificaciones de menú
ms.assetid: 8ff5671e-a666-483c-9ac1-f8be6eb58ffa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f593e3007dff82241dc9e917a6cfa140cc443679
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127268519"
---
# <a name="menu-notifications"></a>Notificaciones de menú

## <a name="in-this-section"></a>En esta sección

-   [**COMANDO \_ WM**](wm-command.md)
-   [**CONTEXTMENU de WM \_**](wm-contextmenu.md)
-   [**WM \_ ENTERMENULOOP**](wm-entermenuloop.md)
-   [**WM \_ EXITMENULOOP**](wm-exitmenuloop.md)
-   [**WM \_ GETTITLEBARINFOEX**](wm-gettitlebarinfoex.md)
-   [**WM \_ MENUCOMMAND**](wm-menucommand.md)
-   [**WM \_ MENUDRAG**](wm-menudrag.md)
-   [**WM \_ MENUGETOBJECT**](wm-menugetobject.md)
-   [**WM \_ MENURBUTTONUP**](wm-menurbuttonup.md)
-   [**WM \_ NEXTMENU**](wm-nextmenu.md)
-   [**WM \_ UNINITMENUPOPUP**](wm-uninitmenupopup.md)


## <a name="example"></a>Ejemplo

```c
BOOL AboutDlg (
    HWND hDlg, 
    UINT message, 
    WPARAM wParam, 
    LPARAM lParam)
{
    BOOL bRet = FALSE;
    
    switch (message) 
    {
        case WM_INITDIALOG:
            bRet = TRUE;
            break;

        case WM_COMMAND:
            if (wParam == IDOK ||
                wParam == IDCANCEL) 
            {
                EndDialog(hDlg, TRUE);
                bRet = TRUE;
            }
            break;
    }

    return bRet;
}
```
Ejemplo tomado de [Windows ejemplos clásicos](https://github.com/microsoft/Windows-classic-samples) en GitHub.

 




