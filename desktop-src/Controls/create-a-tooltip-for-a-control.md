---
title: Cómo crear una información sobre herramientas para un control
description: En la función de ejemplo siguiente se crea una información sobre herramientas y se asocia al control cuyo identificador de recurso se pasa.
ms.assetid: FDA3B2A0-1256-4DAC-86CF-8F123894E760
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f341c1be1e749c4e0d6f18caf97a3f897cf429e7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075299"
---
# <a name="how-to-create-a-tooltip-for-a-control"></a><span data-ttu-id="7f5bd-103">Cómo crear una información sobre herramientas para un control</span><span class="sxs-lookup"><span data-stu-id="7f5bd-103">How to Create a Tooltip for a Control</span></span>

<span data-ttu-id="7f5bd-104">En la función de ejemplo siguiente se crea una información sobre herramientas y se asocia al control cuyo identificador de recurso se pasa.</span><span class="sxs-lookup"><span data-stu-id="7f5bd-104">The following example function creates a tooltip and associates it with the control whose resource ID is passed in.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="7f5bd-105">Aspectos que debe saber</span><span class="sxs-lookup"><span data-stu-id="7f5bd-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="7f5bd-106">Tecnologías</span><span class="sxs-lookup"><span data-stu-id="7f5bd-106">Technologies</span></span>

-   [<span data-ttu-id="7f5bd-107">Controles de Windows</span><span class="sxs-lookup"><span data-stu-id="7f5bd-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="7f5bd-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="7f5bd-108">Prerequisites</span></span>

-   <span data-ttu-id="7f5bd-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="7f5bd-109">C/C++</span></span>
-   <span data-ttu-id="7f5bd-110">Programación de la interfaz de usuario de Windows</span><span class="sxs-lookup"><span data-stu-id="7f5bd-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="7f5bd-111">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="7f5bd-111">Instructions</span></span>

### <a name="create-a-tooltip-for-a-control"></a><span data-ttu-id="7f5bd-112">Crear una información sobre herramientas para un control</span><span class="sxs-lookup"><span data-stu-id="7f5bd-112">Create a Tooltip for a Control</span></span>

<span data-ttu-id="7f5bd-113">En la función de ejemplo siguiente se crea una información sobre herramientas y se asocia al control cuyo identificador de recurso se pasa.</span><span class="sxs-lookup"><span data-stu-id="7f5bd-113">The following example function creates a tooltip and associates it with the control whose resource ID is passed in.</span></span>


```C++
// Description:
//   Creates a tooltip for an item in a dialog box. 
// Parameters:
//   idTool - identifier of an dialog box item.
//   nDlg - window handle of the dialog box.
//   pszText - string to use as the tooltip text.
// Returns:
//   The handle to the tooltip.
//
HWND CreateToolTip(int toolID, HWND hDlg, PTSTR pszText)
{
    if (!toolID || !hDlg || !pszText)
    {
        return FALSE;
    }
    // Get the window of the tool.
    HWND hwndTool = GetDlgItem(hDlg, toolID);
    
    // Create the tooltip. g_hInst is the global instance handle.
    HWND hwndTip = CreateWindowEx(NULL, TOOLTIPS_CLASS, NULL,
                              WS_POPUP |TTS_ALWAYSTIP | TTS_BALLOON,
                              CW_USEDEFAULT, CW_USEDEFAULT,
                              CW_USEDEFAULT, CW_USEDEFAULT,
                              hDlg, NULL, 
                              g_hInst, NULL);
    
   if (!hwndTool || !hwndTip)
   {
       return (HWND)NULL;
   }                              
                              
    // Associate the tooltip with the tool.
    TOOLINFO toolInfo = { 0 };
    toolInfo.cbSize = sizeof(toolInfo);
    toolInfo.hwnd = hDlg;
    toolInfo.uFlags = TTF_IDISHWND | TTF_SUBCLASS;
    toolInfo.uId = (UINT_PTR)hwndTool;
    toolInfo.lpszText = pszText;
    SendMessage(hwndTip, TTM_ADDTOOL, 0, (LPARAM)&toolInfo);

    return hwndTip;
}
```



## <a name="related-topics"></a><span data-ttu-id="7f5bd-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7f5bd-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7f5bd-115">Usar controles ToolTip</span><span class="sxs-lookup"><span data-stu-id="7f5bd-115">Using Tooltip Controls</span></span>](using-tooltip-contro.md)
</dt> </dl>

 

 




