---
title: Cómo crear una información sobre herramientas para un área rectangular
description: En el ejemplo siguiente se muestra cómo crear un control ToolTip estándar para todo el área cliente de una ventana.
ms.assetid: 6AF1CE6E-AD63-4F84-9759-14FE4F16092B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f8daf62bf2ba85c8750fd07a1b9122b0360fc11
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103774190"
---
# <a name="how-to-create-a-tooltip-for-a-rectangular-area"></a><span data-ttu-id="58c49-103">Cómo crear una información sobre herramientas para un área rectangular</span><span class="sxs-lookup"><span data-stu-id="58c49-103">How to Create a Tooltip for a Rectangular Area</span></span>

<span data-ttu-id="58c49-104">En el ejemplo siguiente se muestra cómo crear un control ToolTip estándar para todo el área cliente de una ventana.</span><span class="sxs-lookup"><span data-stu-id="58c49-104">The following example demonstrates how to create a standard tooltip control for a window's entire client area.</span></span>

<span data-ttu-id="58c49-105">En la ilustración siguiente se muestra la información sobre herramientas que se muestra cuando el puntero del mouse se encuentra dentro de la ventana de cliente de un cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="58c49-105">The following illustration shows the tooltip that is displayed when the mouse pointer is within the client window of a dialog box.</span></span> <span data-ttu-id="58c49-106">El identificador del cuadro de diálogo se pasó a la función mostrada en el ejemplo anterior.</span><span class="sxs-lookup"><span data-stu-id="58c49-106">The handle of the dialog box was passed to the function shown in the preceding example.</span></span>

![captura de pantalla de un cuadro de diálogo; el puntero del mouse está dentro de la ventana del cliente y la información sobre herramientas está visible](images/tt-rectangle.png)

## <a name="what-you-need-to-know"></a><span data-ttu-id="58c49-108">Aspectos que debe saber</span><span class="sxs-lookup"><span data-stu-id="58c49-108">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="58c49-109">Tecnologías</span><span class="sxs-lookup"><span data-stu-id="58c49-109">Technologies</span></span>

-   [<span data-ttu-id="58c49-110">Controles de Windows</span><span class="sxs-lookup"><span data-stu-id="58c49-110">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="58c49-111">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="58c49-111">Prerequisites</span></span>

-   <span data-ttu-id="58c49-112">C/C++</span><span class="sxs-lookup"><span data-stu-id="58c49-112">C/C++</span></span>
-   <span data-ttu-id="58c49-113">Programación de la interfaz de usuario de Windows</span><span class="sxs-lookup"><span data-stu-id="58c49-113">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="58c49-114">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="58c49-114">Instructions</span></span>

### <a name="create-a-tooltip-for-a-rectangular-area"></a><span data-ttu-id="58c49-115">Crear una información sobre herramientas para un área rectangular</span><span class="sxs-lookup"><span data-stu-id="58c49-115">Create a Tooltip for a Rectangular Area</span></span>

<span data-ttu-id="58c49-116">En el ejemplo siguiente se muestra cómo crear un control ToolTip estándar para todo el área cliente de una ventana.</span><span class="sxs-lookup"><span data-stu-id="58c49-116">The following example demonstrates how to create a standard tooltip control for a window's entire client area.</span></span>


```C++
void CreateToolTipForRect(HWND hwndParent)
{
    // Create a tooltip.
    HWND hwndTT = CreateWindowEx(WS_EX_TOPMOST, TOOLTIPS_CLASS, NULL, 
                                 WS_POPUP | TTS_NOPREFIX | TTS_ALWAYSTIP, 
                                 CW_USEDEFAULT, CW_USEDEFAULT, CW_USEDEFAULT, CW_USEDEFAULT, 
                                 hwndParent, NULL, g_hInst,NULL);

    SetWindowPos(hwndTT, HWND_TOPMOST, 0, 0, 0, 0, 
                 SWP_NOMOVE | SWP_NOSIZE | SWP_NOACTIVATE);

    // Set up "tool" information. In this case, the "tool" is the entire parent window.
    
    TOOLINFO ti = { 0 };
    ti.cbSize   = sizeof(TOOLINFO);
    ti.uFlags   = TTF_SUBCLASS;
    ti.hwnd     = hwndParent;
    ti.hinst    = g_hInst;
    ti.lpszText = TEXT("This is your tooltip string.");;
    
    GetClientRect (hwndParent, &ti.rect);

    // Associate the tooltip with the "tool" window.
    SendMessage(hwndTT, TTM_ADDTOOL, 0, (LPARAM) (LPTOOLINFO) &ti); 
} 
```



## <a name="related-topics"></a><span data-ttu-id="58c49-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="58c49-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="58c49-118">Usar controles ToolTip</span><span class="sxs-lookup"><span data-stu-id="58c49-118">Using Tooltip Controls</span></span>](using-tooltip-contro.md)
</dt> </dl>

 

 




