---
title: Cómo crear un control de pestaña en la ventana principal
description: En el ejemplo de esta sección se muestra cómo crear un control de pestaña y cómo mostrarlo en el área cliente de la ventana principal de la aplicación.
ms.assetid: 24157B8B-177B-471C-9DA0-548D09EA5F89
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 686a9a4fe4f6be95ccdcf3bbcb597c2c48ff3b2d
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104488346"
---
# <a name="how-to-create-a-tab-control-in-the-main-window"></a><span data-ttu-id="5d369-103">Cómo crear un control de pestaña en la ventana principal</span><span class="sxs-lookup"><span data-stu-id="5d369-103">How to Create a Tab Control in the Main Window</span></span>

<span data-ttu-id="5d369-104">En el ejemplo de esta sección se muestra cómo crear un control de pestaña y cómo mostrarlo en el área cliente de la ventana principal de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="5d369-104">The example in this section demonstrates how to create a tab control and display it in the client area of the application's main window.</span></span> <span data-ttu-id="5d369-105">La aplicación muestra una tercera ventana (un control estático) en el área de presentación del control de ficha.</span><span class="sxs-lookup"><span data-stu-id="5d369-105">The application displays a third window (a static control) in the display area of the tab control.</span></span> <span data-ttu-id="5d369-106">La ventana primaria coloca y ajusta el tamaño del control de pestaña y del control estático cuando procesa el mensaje de [**\_ tamaño de WM**](/windows/desktop/winmsg/wm-size) .</span><span class="sxs-lookup"><span data-stu-id="5d369-106">The parent window positions and sizes the tab control and static control when it processes the [**WM\_SIZE**](/windows/desktop/winmsg/wm-size) message.</span></span>

<span data-ttu-id="5d369-107">En este ejemplo hay siete pestañas, una para cada día de la semana.</span><span class="sxs-lookup"><span data-stu-id="5d369-107">There are seven tabs in this example, one for each day of the week.</span></span> <span data-ttu-id="5d369-108">Cuando el usuario selecciona una pestaña, la aplicación muestra el nombre del día correspondiente en el control estático.</span><span class="sxs-lookup"><span data-stu-id="5d369-108">When the user selects a tab, the application displays the name of the corresponding day in the static control.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="5d369-109">Aspectos que debe saber</span><span class="sxs-lookup"><span data-stu-id="5d369-109">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="5d369-110">Tecnologías</span><span class="sxs-lookup"><span data-stu-id="5d369-110">Technologies</span></span>

-   [<span data-ttu-id="5d369-111">Controles de Windows</span><span class="sxs-lookup"><span data-stu-id="5d369-111">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="5d369-112">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="5d369-112">Prerequisites</span></span>

-   <span data-ttu-id="5d369-113">C/C++</span><span class="sxs-lookup"><span data-stu-id="5d369-113">C/C++</span></span>
-   <span data-ttu-id="5d369-114">Programación de la interfaz de usuario de Windows</span><span class="sxs-lookup"><span data-stu-id="5d369-114">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="5d369-115">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="5d369-115">Instructions</span></span>

### <a name="create-a-tab-control-in-the-main-window"></a><span data-ttu-id="5d369-116">Crear un control de pestaña en la ventana principal</span><span class="sxs-lookup"><span data-stu-id="5d369-116">Create a Tab Control in the Main Window</span></span>

<span data-ttu-id="5d369-117">La función siguiente crea el control de pestaña y agrega una pestaña para cada día de la semana.</span><span class="sxs-lookup"><span data-stu-id="5d369-117">The following function creates the tab control and adds a tab for each day of the week.</span></span> <span data-ttu-id="5d369-118">Los nombres de los días se definen como recursos de cadena, numerados consecutivamente a partir de los ID \_ . Domingo (definidos en el archivo de encabezado de recursos de la aplicación).</span><span class="sxs-lookup"><span data-stu-id="5d369-118">The names of the days are defined as string resources, consecutively numbered starting with IDS\_SUNDAY (defined in the application's resource header file).</span></span> <span data-ttu-id="5d369-119">Tanto la ventana primaria como el control de ficha deben tener el estilo de ventana [**WS \_ CLIPSIBLINGS**](/windows/desktop/winmsg/window-styles) .</span><span class="sxs-lookup"><span data-stu-id="5d369-119">Both the parent window and the tab control must have the [**WS\_CLIPSIBLINGS**](/windows/desktop/winmsg/window-styles) window style.</span></span> <span data-ttu-id="5d369-120">La función de inicialización de la aplicación llama a esta función después de crear la ventana principal.</span><span class="sxs-lookup"><span data-stu-id="5d369-120">The application's initialization function calls this function after creating the main window.</span></span>


```C++
#define DAYS_IN_WEEK 7

// Creates a tab control, sized to fit the specified parent window's client
//   area, and adds some tabs. 
// Returns the handle to the tab control. 
// hwndParent - parent window (the application's main window). 
// 
HWND DoCreateTabControl(HWND hwndParent) 
{ 
    RECT rcClient; 
    INITCOMMONCONTROLSEX icex;
    HWND hwndTab; 
    TCITEM tie; 
    int i; 
    TCHAR achTemp[256];  // Temporary buffer for strings.
 
    // Initialize common controls.
    icex.dwSize = sizeof(INITCOMMONCONTROLSEX);
    icex.dwICC = ICC_TAB_CLASSES;
    InitCommonControlsEx(&icex);
    
    // Get the dimensions of the parent window's client area, and 
    // create a tab control child window of that size. Note that g_hInst
    // is the global instance handle.
    GetClientRect(hwndParent, &rcClient); 
    hwndTab = CreateWindow(WC_TABCONTROL, L"", 
        WS_CHILD | WS_CLIPSIBLINGS | WS_VISIBLE, 
        0, 0, rcClient.right, rcClient.bottom, 
        hwndParent, NULL, g_hInst, NULL); 
    if (hwndTab == NULL)
    { 
        return NULL; 
    }
 
    // Add tabs for each day of the week. 
    tie.mask = TCIF_TEXT | TCIF_IMAGE; 
    tie.iImage = -1; 
    tie.pszText = achTemp; 
 
    for (i = 0; i < DAYS_IN_WEEK; i++) 
    { 
        // Load the day string from the string resources. Note that
        // g_hInst is the global instance handle.
        LoadString(g_hInst, IDS_SUNDAY + i, 
                achTemp, sizeof(achTemp) / sizeof(achTemp[0])); 
        if (TabCtrl_InsertItem(hwndTab, i, &tie) == -1) 
        { 
            DestroyWindow(hwndTab); 
            return NULL; 
        } 
    } 
    return hwndTab; 
} 
```



<span data-ttu-id="5d369-121">La función siguiente crea el control estático que reside en el área de presentación del control de pestaña.</span><span class="sxs-lookup"><span data-stu-id="5d369-121">The following function creates the static control that resides in the tab control's display area.</span></span> <span data-ttu-id="5d369-122">La función de inicialización de la aplicación llama a esta función después de crear la ventana principal y el control de pestaña.</span><span class="sxs-lookup"><span data-stu-id="5d369-122">The application's initialization function calls this function after creating the main window and the tab control.</span></span>


```C++
// Creates a child window (a static control) to occupy the tab control's 
//   display area. 
// Returns the handle to the static control. 
// hwndTab - handle of the tab control. 
// 
HWND DoCreateDisplayWindow(HWND hwndTab) 
{ 
    HWND hwndStatic = CreateWindow(WC_STATIC, L"", 
        WS_CHILD | WS_VISIBLE | WS_BORDER, 
        100, 100, 100, 100,        // Position and dimensions; example only.
        hwndTab, NULL, g_hInst,    // g_hInst is the global instance handle
        NULL); 
    return hwndStatic; 
}
```



<span data-ttu-id="5d369-123">Se llama a las funciones de ejemplo siguientes desde el procedimiento de ventana de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="5d369-123">The following example functions are called from the application's window procedure.</span></span> <span data-ttu-id="5d369-124">La aplicación llama a la `OnSize` función al procesar el mensaje de [**\_ tamaño de WM**](/windows/desktop/winmsg/wm-size) para colocar y cambiar el tamaño del control de pestaña para ajustarse al área de cliente de la ventana principal.</span><span class="sxs-lookup"><span data-stu-id="5d369-124">The application calls the `OnSize` function when processing the [**WM\_SIZE**](/windows/desktop/winmsg/wm-size) message to position and size the tab control to fit the main window's client area.</span></span>

<span data-ttu-id="5d369-125">Cuando se selecciona una ficha, el control de pestaña envía un mensaje de notificación de [**WM \_**](wm-notify.md) , especificando el código de notificación de [TCN \_ SELCHANGE](tcn-selchange.md) .</span><span class="sxs-lookup"><span data-stu-id="5d369-125">When a tab is selected, the tab control sends a [**WM\_NOTIFY**](wm-notify.md) message, specifying the [TCN\_SELCHANGE](tcn-selchange.md) notification code.</span></span> <span data-ttu-id="5d369-126">La función de la aplicación `OnNotify` procesa este código de notificación estableciendo el texto del control estático.</span><span class="sxs-lookup"><span data-stu-id="5d369-126">The application's `OnNotify` function processes this notification code by setting the text of the static control.</span></span>


```C++
// Handles the WM_SIZE message for the main window by resizing the 
//   tab control. 
// hwndTab - handle of the tab control.
// lParam - the lParam parameter of the WM_SIZE message.
//
HRESULT OnSize(HWND hwndTab, LPARAM lParam)
{
    RECT rc; 

    if (hwndTab == NULL)
        return E_INVALIDARG;

    // Resize the tab control to fit the client are of main window.
     if (!SetWindowPos(hwndTab, HWND_TOP, 0, 0, GET_X_LPARAM(lParam), GET_Y_LPARAM(lParam), SWP_SHOWWINDOW))
        return E_FAIL;

    return S_OK;
}

// Handles notifications from the tab control, as follows: 
//   TCN_SELCHANGING - always returns FALSE to allow the user to select a 
//     different tab.  
//   TCN_SELCHANGE - loads a string resource and displays it in a static 
//     control on the selected tab.
// hwndTab - handle of the tab control.
// hwndDisplay - handle of the static control. 
// lParam - the lParam parameter of the WM_NOTIFY message.
//
BOOL OnNotify(HWND hwndTab, HWND hwndDisplay, LPARAM lParam)
{
    TCHAR achTemp[256]; // temporary buffer for strings

    switch (((LPNMHDR)lParam)->code)
        {
            case TCN_SELCHANGING:
                {
                    // Return FALSE to allow the selection to change.
                    return FALSE;
                }

            case TCN_SELCHANGE:
                { 
                    int iPage = TabCtrl_GetCurSel(hwndTab); 

                    // Note that g_hInst is the global instance handle.
                    LoadString(g_hInst, IDS_SUNDAY + iPage, achTemp,
                        sizeof(achTemp) / sizeof(achTemp[0])); 
                    LRESULT result = SendMessage(hwndDisplay, WM_SETTEXT, 0,
                        (LPARAM) achTemp); 
                    break;
                } 
        }
        return TRUE;
}
```



## <a name="related-topics"></a><span data-ttu-id="5d369-127">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5d369-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5d369-128">Usar controles de ficha</span><span class="sxs-lookup"><span data-stu-id="5d369-128">Using Tab Controls</span></span>](using-tab-controls.md)
</dt> <dt>

<span data-ttu-id="5d369-129">[Demostración de controles comunes de Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="5d369-129">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 