---
title: Cómo usar notificaciones de SysLink
description: Hay dos mensajes de notificación asociados al control SysLink \ 8212; uno para el mouse (NM \_ click (SysLink)) y otro para el teclado ( \_ Return nm).
ms.assetid: 77E80EB2-180B-4EDD-9FB5-9930E8886CA6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 864a2b8942b1244be51f5c284e6ce07d973ed4db
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/17/2020
ms.locfileid: "105656321"
---
# <a name="how-to-use-syslink-notifications"></a><span data-ttu-id="c9de2-103">Cómo usar notificaciones de SysLink</span><span class="sxs-lookup"><span data-stu-id="c9de2-103">How to Use SysLink Notifications</span></span>

<span data-ttu-id="c9de2-104">Hay dos mensajes de notificación asociados al control SysLink: uno para el mouse ([nm \_ click (SysLink)](nm-click-syslink.md)) y otro para el teclado ([nm \_ Return](nm-return.md)).</span><span class="sxs-lookup"><span data-stu-id="c9de2-104">There are two notification messages associated with the SysLink control—one for the mouse ([NM\_CLICK (syslink)](nm-click-syslink.md)), and one for the keyboard ([NM\_RETURN](nm-return.md)).</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="c9de2-105">Aspectos que debe saber</span><span class="sxs-lookup"><span data-stu-id="c9de2-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="c9de2-106">Tecnologías</span><span class="sxs-lookup"><span data-stu-id="c9de2-106">Technologies</span></span>

-   [<span data-ttu-id="c9de2-107">Controles de Windows</span><span class="sxs-lookup"><span data-stu-id="c9de2-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="c9de2-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="c9de2-108">Prerequisites</span></span>

-   <span data-ttu-id="c9de2-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="c9de2-109">C/C++</span></span>
-   <span data-ttu-id="c9de2-110">Programación de la interfaz de usuario de Windows</span><span class="sxs-lookup"><span data-stu-id="c9de2-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="c9de2-111">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="c9de2-111">Instructions</span></span>

### <a name="use-syslink-notifications"></a><span data-ttu-id="c9de2-112">Usar notificaciones de SysLink</span><span class="sxs-lookup"><span data-stu-id="c9de2-112">Use SysLink Notifications</span></span>

<span data-ttu-id="c9de2-113">En el ejemplo de código siguiente se muestra cómo procesar las notificaciones de SysLink que se generan cuando el usuario hace clic en cualquiera de los dos vínculos del [ejemplo anterior](create-syslink-controls.md).</span><span class="sxs-lookup"><span data-stu-id="c9de2-113">The following example code shows how to process the SysLink notifications that are generated when the user clicks either of the two links in the [previous example](create-syslink-controls.md).</span></span> <span data-ttu-id="c9de2-114">Cuando el usuario hace clic en la dirección URL de Internet, se abre la página web asociada en el explorador predeterminado.</span><span class="sxs-lookup"><span data-stu-id="c9de2-114">When the user clicks the Internet URL, the associated webpage opens in the default browser.</span></span> <span data-ttu-id="c9de2-115">Cuando el usuario hace clic en el hipervínculo definido por la aplicación, se muestra un cuadro de mensaje.</span><span class="sxs-lookup"><span data-stu-id="c9de2-115">When the user clicks the application-defined hyperlink, a message box is displayed.</span></span>


```C++
// g_hLink is the handle of the SysLink control.
case WM_NOTIFY:

    switch (((LPNMHDR)lParam)->code)
    {
    
    case NM_CLICK:          // Fall through to the next case.
    
    case NM_RETURN:
        {
            PNMLINK pNMLink = (PNMLINK)lParam;
            LITEM   item    = pNMLink->item;
            
            if ((((LPNMHDR)lParam)->hwndFrom == g_hLink) && (item.iLink == 0))
              {
                ShellExecute(NULL, L"open", item.szUrl, NULL, NULL, SW_SHOW);
              }
            
            else if (wcscmp(item.szID, L"idInfo") == 0)
              {
                MessageBox(hDlg, L"This isn't much help.", L"Example", MB_OK);
              }
            
            break;
        }
    }
    
    break;
```



## <a name="related-topics"></a><span data-ttu-id="c9de2-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c9de2-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c9de2-117">Usar controles SysLink</span><span class="sxs-lookup"><span data-stu-id="c9de2-117">Using SysLink Controls</span></span>](using-syslink-controls.md)
</dt> <dt>

<span data-ttu-id="c9de2-118">[Demostración de controles comunes de Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="c9de2-118">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 




