---
title: Cómo crear controles rebar
description: Una aplicación crea un control rebar llamando a la función CreateWindowEx y especificando REBARCLASSNAME como clase de ventana.
ms.assetid: F17CC2A4-BDC6-48A6-9AF5-19FCF65CC39A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19b38cd49e8e6016dafad5ec07c77be570a5a430
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "103793983"
---
# <a name="how-to-create-rebar-controls"></a><span data-ttu-id="68710-103">Cómo crear controles rebar</span><span class="sxs-lookup"><span data-stu-id="68710-103">How to Create Rebar Controls</span></span>

<span data-ttu-id="68710-104">Una aplicación crea un control rebar llamando a la función [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) y especificando [**REBARCLASSNAME**](common-control-window-classes.md) como clase de ventana.</span><span class="sxs-lookup"><span data-stu-id="68710-104">An application creates a rebar control by calling the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function, specifying [**REBARCLASSNAME**](common-control-window-classes.md) as the window class.</span></span> <span data-ttu-id="68710-105">La aplicación debe registrar primero la clase de ventana mediante una llamada a la función [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) , especificando el \_ \_ bit de las clases de ICC Cool en la estructura [**InitCommonControlsEx**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) correspondiente.</span><span class="sxs-lookup"><span data-stu-id="68710-105">The application must first register the window class by calling the [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) function, specifying the ICC\_COOL\_CLASSES bit in the accompanying [**INITCOMMONCONTROLSEX**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) structure.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="68710-106">Aspectos que debe saber</span><span class="sxs-lookup"><span data-stu-id="68710-106">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="68710-107">Tecnologías</span><span class="sxs-lookup"><span data-stu-id="68710-107">Technologies</span></span>

-   [<span data-ttu-id="68710-108">Controles de Windows</span><span class="sxs-lookup"><span data-stu-id="68710-108">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="68710-109">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="68710-109">Prerequisites</span></span>

-   <span data-ttu-id="68710-110">C/C++</span><span class="sxs-lookup"><span data-stu-id="68710-110">C/C++</span></span>
-   <span data-ttu-id="68710-111">Programación de la interfaz de usuario de Windows</span><span class="sxs-lookup"><span data-stu-id="68710-111">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="68710-112">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="68710-112">Instructions</span></span>

### <a name="create-a-rebar-control"></a><span data-ttu-id="68710-113">Crear un control rebar</span><span class="sxs-lookup"><span data-stu-id="68710-113">Create a Rebar Control</span></span>

<span data-ttu-id="68710-114">En el ejemplo siguiente se crea un control rebar con dos bandas: una que contiene un cuadro combinado y otra que contiene una barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="68710-114">The following example creates a rebar control with two bands—one that contains a combo box, and another one that contains a toolbar.</span></span> <span data-ttu-id="68710-115">(Vea la ilustración en [acerca de los controles rebar](rebar-controls.md)). Estos controles se crean por separado y se pasan a la función de ejemplo como parámetros.</span><span class="sxs-lookup"><span data-stu-id="68710-115">(See the illustration in [About Rebar Controls](rebar-controls.md).) These controls are created separately, and are passed to the example function as parameters.</span></span>


```C++
#define NUMBUTTONS 3

HWND CreateRebar(HWND hwndOwner, HWND hwndToolbar, HWND hwndCombo)
{
    // Check parameters.
    if ((hwndToolbar == NULL) || (hwndCombo == NULL))
    {
        return NULL;
    }

    // Initialize common controls.
    INITCOMMONCONTROLSEX icex;
    icex.dwSize = sizeof(INITCOMMONCONTROLSEX);
    icex.dwICC   = ICC_COOL_CLASSES | ICC_BAR_CLASSES;
    InitCommonControlsEx(&icex);

    // Create the rebar.
    HWND hwndRebar = CreateWindowEx(WS_EX_TOOLWINDOW,
        REBARCLASSNAME,
        NULL,
        WS_CHILD | WS_VISIBLE | WS_CLIPSIBLINGS |
        WS_CLIPCHILDREN | RBS_VARHEIGHT |
        CCS_NODIVIDER | RBS_BANDBORDERS,
        0,0,0,0,
        hwndOwner,
        NULL,
        g_hInst, // global instance handle
        NULL);

    if(!hwndRebar)
    {
        return NULL;
    }

    // Initialize band info used by both bands.
    REBARBANDINFO rbBand = { sizeof(REBARBANDINFO) };
    rbBand.fMask  = 
          RBBIM_STYLE       // fStyle is valid.
        | RBBIM_TEXT        // lpText is valid.
        | RBBIM_CHILD       // hwndChild is valid.
        | RBBIM_CHILDSIZE   // child size members are valid.
        | RBBIM_SIZE;       // cx is valid
    rbBand.fStyle = RBBS_CHILDEDGE | RBBS_GRIPPERALWAYS;  

    // Get the height of the toolbar.
    DWORD dwBtnSize = (DWORD)SendMessage(hwndToolbar, TB_GETBUTTONSIZE, 0,0);

    // Set values unique to the band with the toolbar.
    rbBand.lpText = TEXT("");
    rbBand.hwndChild = hwndToolbar;
    rbBand.cyChild = LOWORD(dwBtnSize);
    rbBand.cxMinChild = NUMBUTTONS * HIWORD(dwBtnSize);
    rbBand.cyMinChild = LOWORD(dwBtnSize);
    // The default width is the width of the buttons.
    rbBand.cx = 0;

    // Add the band that has the toolbar.
    SendMessage(hwndRebar, RB_INSERTBAND, (WPARAM)-1, (LPARAM)&rbBand);

    // Set values unique to the band with the combo box.
    RECT rc;
    GetWindowRect(hwndCombo, &rc);
    rbBand.lpText = TEXT("Font");
    rbBand.hwndChild = hwndCombo;
    rbBand.cxMinChild = 0;
    rbBand.cyMinChild = rc.bottom - rc.top;
    // The default width should be set to some value wider than the text. The combo 
    // box itself will expand to fill the band.
    rbBand.cx = 100;

    // Add the band that has the combo box.
    SendMessage(hwndRebar, RB_INSERTBAND, (WPARAM)-1, (LPARAM)&rbBand);
    
    return (hwndRebar);
}
```



## <a name="related-topics"></a><span data-ttu-id="68710-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="68710-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="68710-117">Usar controles rebar</span><span class="sxs-lookup"><span data-stu-id="68710-117">Using Rebar Controls</span></span>](using-rebar-controls.md)
</dt> <dt>

[<span data-ttu-id="68710-118">Acerca de los controles rebar</span><span class="sxs-lookup"><span data-stu-id="68710-118">About Rebar Controls</span></span>](rebar-controls.md)
</dt> <dt>

<span data-ttu-id="68710-119">[Demostración de controles comunes de Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="68710-119">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 