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
# <a name="menu-notifications"></a><span data-ttu-id="42c73-103">Notificaciones de menú</span><span class="sxs-lookup"><span data-stu-id="42c73-103">Menu Notifications</span></span>

## <a name="in-this-section"></a><span data-ttu-id="42c73-104">En esta sección</span><span class="sxs-lookup"><span data-stu-id="42c73-104">In This Section</span></span>

-   [<span data-ttu-id="42c73-105">**comando de WM \_**</span><span class="sxs-lookup"><span data-stu-id="42c73-105">**WM\_COMMAND**</span></span>](wm-command.md)
-   [<span data-ttu-id="42c73-106">**CONTEXTMENU de WM \_**</span><span class="sxs-lookup"><span data-stu-id="42c73-106">**WM\_CONTEXTMENU**</span></span>](wm-contextmenu.md)
-   [<span data-ttu-id="42c73-107">**ENTERMENULOOP de WM \_**</span><span class="sxs-lookup"><span data-stu-id="42c73-107">**WM\_ENTERMENULOOP**</span></span>](wm-entermenuloop.md)
-   [<span data-ttu-id="42c73-108">**EXITMENULOOP de WM \_**</span><span class="sxs-lookup"><span data-stu-id="42c73-108">**WM\_EXITMENULOOP**</span></span>](wm-exitmenuloop.md)
-   [<span data-ttu-id="42c73-109">**GETTITLEBARINFOEX de WM \_**</span><span class="sxs-lookup"><span data-stu-id="42c73-109">**WM\_GETTITLEBARINFOEX**</span></span>](wm-gettitlebarinfoex.md)
-   [<span data-ttu-id="42c73-110">**MENUCOMMAND de WM \_**</span><span class="sxs-lookup"><span data-stu-id="42c73-110">**WM\_MENUCOMMAND**</span></span>](wm-menucommand.md)
-   [<span data-ttu-id="42c73-111">**MENUDRAG de WM \_**</span><span class="sxs-lookup"><span data-stu-id="42c73-111">**WM\_MENUDRAG**</span></span>](wm-menudrag.md)
-   [<span data-ttu-id="42c73-112">**MENUGETOBJECT de WM \_**</span><span class="sxs-lookup"><span data-stu-id="42c73-112">**WM\_MENUGETOBJECT**</span></span>](wm-menugetobject.md)
-   [<span data-ttu-id="42c73-113">**MENURBUTTONUP de WM \_**</span><span class="sxs-lookup"><span data-stu-id="42c73-113">**WM\_MENURBUTTONUP**</span></span>](wm-menurbuttonup.md)
-   [<span data-ttu-id="42c73-114">**NEXTMENU de WM \_**</span><span class="sxs-lookup"><span data-stu-id="42c73-114">**WM\_NEXTMENU**</span></span>](wm-nextmenu.md)
-   [<span data-ttu-id="42c73-115">**UNINITMENUPOPUP de WM \_**</span><span class="sxs-lookup"><span data-stu-id="42c73-115">**WM\_UNINITMENUPOPUP**</span></span>](wm-uninitmenupopup.md)


## <a name="example"></a><span data-ttu-id="42c73-116">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="42c73-116">Example</span></span>

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
<span data-ttu-id="42c73-117">Ejemplo tomado de [ejemplos clásicos de Windows](https://github.com/microsoft/Windows-classic-samples) en github.</span><span class="sxs-lookup"><span data-stu-id="42c73-117">Example taken from [Windows classic samples](https://github.com/microsoft/Windows-classic-samples) on GitHub.</span></span>

 




