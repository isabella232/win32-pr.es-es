---
title: Notificaciones de menú
description: .
ms.assetid: 8ff5671e-a666-483c-9ac1-f8be6eb58ffa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d61f5303253fd3201fd9a4510ecf90fa76c10524
ms.sourcegitcommit: e98f40bef170ae9ce30d91ba96b90600b0446a24
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/28/2020
ms.locfileid: "104358787"
---
# <a name="menu-notifications"></a>Notificaciones de menú

## <a name="in-this-section"></a>En esta sección

-   [**comando de WM \_**](wm-command.md)
-   [**CONTEXTMENU de WM \_**](wm-contextmenu.md)
-   [**ENTERMENULOOP de WM \_**](wm-entermenuloop.md)
-   [**EXITMENULOOP de WM \_**](wm-exitmenuloop.md)
-   [**GETTITLEBARINFOEX de WM \_**](wm-gettitlebarinfoex.md)
-   [**MENUCOMMAND de WM \_**](wm-menucommand.md)
-   [**MENUDRAG de WM \_**](wm-menudrag.md)
-   [**MENUGETOBJECT de WM \_**](wm-menugetobject.md)
-   [**MENURBUTTONUP de WM \_**](wm-menurbuttonup.md)
-   [**NEXTMENU de WM \_**](wm-nextmenu.md)
-   [**UNINITMENUPOPUP de WM \_**](wm-uninitmenupopup.md)


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
Ejemplo tomado de [ejemplos clásicos de Windows](https://github.com/microsoft/Windows-classic-samples) en github.

 




