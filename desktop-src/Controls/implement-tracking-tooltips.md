---
title: Cómo implementar la información sobre herramientas de seguimiento
description: La información sobre herramientas de seguimiento permanece visible hasta que la aplicación la cierra explícitamente, y puede cambiar la posición de la pantalla de forma dinámica. Son compatibles con la versión 4,70 y versiones posteriores de los controles comunes.
ms.assetid: 4BE1F9E6-92B6-4CA7-B89A-F2162BC86366
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a614fef7ed69cd8c2763f9370ce0011d51eb0c82
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075292"
---
# <a name="how-to-implement-tracking-tooltips"></a><span data-ttu-id="8acd7-104">Cómo implementar la información sobre herramientas de seguimiento</span><span class="sxs-lookup"><span data-stu-id="8acd7-104">How to Implement Tracking Tooltips</span></span>

<span data-ttu-id="8acd7-105">La información sobre herramientas de seguimiento permanece visible hasta que la aplicación la cierra explícitamente, y puede cambiar la posición de la pantalla de forma dinámica.</span><span class="sxs-lookup"><span data-stu-id="8acd7-105">Tracking tooltips remain visible until they are explicitly closed by the application, and can change position on the screen dynamically.</span></span> <span data-ttu-id="8acd7-106">Son compatibles con la [versión 4,70](common-control-versions.md) y versiones posteriores de los controles comunes.</span><span class="sxs-lookup"><span data-stu-id="8acd7-106">They are supported by [version 4.70](common-control-versions.md) and later of the common controls.</span></span>

<span data-ttu-id="8acd7-107">Para crear una información sobre herramientas de seguimiento, incluya la \_ marca de seguimiento ttf en el miembro **uFlags** de la estructura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) al enviar el mensaje [**TTM \_ ADDTOOL**](ttm-addtool.md) .</span><span class="sxs-lookup"><span data-stu-id="8acd7-107">To create a tracking tooltip, include the TTF\_TRACK flag in the **uFlags** member of the [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure when sending the [**TTM\_ADDTOOL**](ttm-addtool.md) message.</span></span>

<span data-ttu-id="8acd7-108">La aplicación debe activar (Mostrar) y desactivar (ocultar) manualmente la información sobre herramientas de seguimiento mediante el envío de un mensaje de [**TTM \_ TRACKACTIVATE**](ttm-trackactivate.md) .</span><span class="sxs-lookup"><span data-stu-id="8acd7-108">Your application must manually activate (show) and deactivate (hide) a tracking tooltip by sending a [**TTM\_TRACKACTIVATE**](ttm-trackactivate.md) message.</span></span> <span data-ttu-id="8acd7-109">Mientras que la información sobre herramientas de seguimiento está activa, la aplicación debe especificar la ubicación de la información sobre herramientas mediante el envío de mensajes de [**TTM \_ TRACKPOSITION**](ttm-trackposition.md) al control ToolTip.</span><span class="sxs-lookup"><span data-stu-id="8acd7-109">While a tracking tooltip is active, your application must specify the location of the tooltip by sending [**TTM\_TRACKPOSITION**](ttm-trackposition.md) messages to the tooltip control.</span></span> <span data-ttu-id="8acd7-110">Dado que la aplicación controla tareas como colocar la información sobre herramientas, el seguimiento de la información sobre herramientas no utiliza la marca de **\_ subclase ttf** ni el mensaje [**\_ RELAYEVENT de TTM**](ttm-relayevent.md) .</span><span class="sxs-lookup"><span data-stu-id="8acd7-110">Because the application handles tasks such as positioning the tooltip, tracking tooltips do not use the **TTF\_SUBCLASS** flag or the [**TTM\_RELAYEVENT**](ttm-relayevent.md) message.</span></span>

<span data-ttu-id="8acd7-111">El [**mensaje \_ TRACKPOSITION de TTM**](ttm-trackposition.md) hace que el control de información sobre herramientas muestre la ventana con uno de los dos estilos de colocación:</span><span class="sxs-lookup"><span data-stu-id="8acd7-111">The [**TTM\_TRACKPOSITION**](ttm-trackposition.md) message causes the tooltip control to display the window using one of two placement styles:</span></span>

-   <span data-ttu-id="8acd7-112">De forma predeterminada, la información sobre herramientas se muestra junto a la herramienta correspondiente en una posición que el control elige.</span><span class="sxs-lookup"><span data-stu-id="8acd7-112">By default, the tooltip is displayed next to the corresponding tool in a position that the control chooses.</span></span> <span data-ttu-id="8acd7-113">La ubicación elegida es relativa a las coordenadas que se proporcionan con este mensaje.</span><span class="sxs-lookup"><span data-stu-id="8acd7-113">The location chosen is relative to the coordinates that you provide by using this message.</span></span>
-   <span data-ttu-id="8acd7-114">Si incluye el valor **\_ absoluto de ttf** en el miembro de la estructura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) , la información sobre herramientas se muestra en la ubicación de píxeles especificada en el mensaje.</span><span class="sxs-lookup"><span data-stu-id="8acd7-114">If you include the **TTF\_ABSOLUTE** value in the member of the [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure, the tooltip is displayed at the pixel location specified in the message.</span></span> <span data-ttu-id="8acd7-115">En este caso, el control no intenta cambiar la ubicación de la ventana de información sobre herramientas de las coordenadas proporcionadas.</span><span class="sxs-lookup"><span data-stu-id="8acd7-115">In this case, the control does not attempt to change the tooltip window's location from the coordinates you provide.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="8acd7-116">Aspectos que debe saber</span><span class="sxs-lookup"><span data-stu-id="8acd7-116">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="8acd7-117">Tecnologías</span><span class="sxs-lookup"><span data-stu-id="8acd7-117">Technologies</span></span>

-   [<span data-ttu-id="8acd7-118">Controles de Windows</span><span class="sxs-lookup"><span data-stu-id="8acd7-118">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="8acd7-119">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="8acd7-119">Prerequisites</span></span>

-   <span data-ttu-id="8acd7-120">C/C++</span><span class="sxs-lookup"><span data-stu-id="8acd7-120">C/C++</span></span>
-   <span data-ttu-id="8acd7-121">Programación de la interfaz de usuario de Windows</span><span class="sxs-lookup"><span data-stu-id="8acd7-121">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="8acd7-122">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="8acd7-122">Instructions</span></span>

### <a name="implement-in-place-tooltips"></a><span data-ttu-id="8acd7-123">Implementar In-Place información sobre herramientas</span><span class="sxs-lookup"><span data-stu-id="8acd7-123">Implement In-Place Tooltips</span></span>

<span data-ttu-id="8acd7-124">El miembro **uFlags** de la estructura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) que se usa en el ejemplo incluye la **marca \_ absoluta ttf** .</span><span class="sxs-lookup"><span data-stu-id="8acd7-124">The **uFlags** member of the [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure that is used in the example includes the **TTF\_ABSOLUTE** flag.</span></span> <span data-ttu-id="8acd7-125">Sin esta marca, el control ToolTip elige dónde Mostrar la información sobre herramientas y su posición relativa al cuadro de diálogo puede cambiar repentinamente cuando se mueve el puntero del mouse.</span><span class="sxs-lookup"><span data-stu-id="8acd7-125">Without this flag, the tooltip control chooses where to display the tooltip, and its position relative to the dialog box may change suddenly as the mouse pointer moves.</span></span>

> [!Note]  
> <span data-ttu-id="8acd7-126">`g_toolItem` es una estructura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) global.</span><span class="sxs-lookup"><span data-stu-id="8acd7-126">`g_toolItem` is a global [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure.</span></span>

 

<span data-ttu-id="8acd7-127">En el ejemplo siguiente se muestra cómo crear un control de información sobre herramientas de seguimiento.</span><span class="sxs-lookup"><span data-stu-id="8acd7-127">The following example demonstrates how to create a tracking tooltip control.</span></span> <span data-ttu-id="8acd7-128">En el ejemplo se especifica el área de cliente completa de la ventana principal como la herramienta.</span><span class="sxs-lookup"><span data-stu-id="8acd7-128">The example specifies the main window's entire client area as the tool.</span></span>


```C++
HWND CreateTrackingToolTip(int toolID, HWND hDlg, WCHAR* pText)
{
    // Create a tooltip.
    HWND hwndTT = CreateWindowEx(WS_EX_TOPMOST, TOOLTIPS_CLASS, NULL, 
                                 WS_POPUP | TTS_NOPREFIX | TTS_ALWAYSTIP, 
                                 CW_USEDEFAULT, CW_USEDEFAULT, CW_USEDEFAULT, CW_USEDEFAULT, 
                                 hDlg, NULL, g_hInst,NULL);

    if (!hwndTT)
    {
      return NULL;
    }

    // Set up the tool information. In this case, the "tool" is the entire parent window.
    
    g_toolItem.cbSize   = sizeof(TOOLINFO);
    g_toolItem.uFlags   = TTF_IDISHWND | TTF_TRACK | TTF_ABSOLUTE;
    g_toolItem.hwnd     = hDlg;
    g_toolItem.hinst    = g_hInst;
    g_toolItem.lpszText = pText;
    g_toolItem.uId      = (UINT_PTR)hDlg;
    
    GetClientRect (hDlg, &g_toolItem.rect);

    // Associate the tooltip with the tool window.
    
    SendMessage(hwndTT, TTM_ADDTOOL, 0, (LPARAM) (LPTOOLINFO) &g_toolItem); 
    
    return hwndTT;
}
            
```



### <a name="window-procedure-implementation"></a><span data-ttu-id="8acd7-129">Implementación del procedimiento de ventana</span><span class="sxs-lookup"><span data-stu-id="8acd7-129">Window Procedure Implementation</span></span>

<span data-ttu-id="8acd7-130">Cuando el puntero del mouse se encuentra dentro del área cliente, la información sobre herramientas está activa y muestra las coordenadas del cursor, tal como se muestra en la siguiente ilustración.</span><span class="sxs-lookup"><span data-stu-id="8acd7-130">When the mouse pointer is within the client area, the tooltip is active and displays the cursor coordinates, as shown in the following illustration.</span></span>

![captura de pantalla de un cuadro de diálogo; la información sobre herramientas muestra las coordenadas x e y del puntero del mouse](images/tt-tracking.png)

<span data-ttu-id="8acd7-132">El siguiente código de ejemplo se encuentra en el procedimiento de ventana de un cuadro de diálogo que muestra la información sobre herramientas de seguimiento creada en el ejemplo anterior.</span><span class="sxs-lookup"><span data-stu-id="8acd7-132">The following example code is from the window procedure for a dialog box that displays the tracking tooltip created in the preceding example.</span></span> <span data-ttu-id="8acd7-133">La variable booleana global *g \_ TrackingMouse* se usa para determinar si es necesario reactivar la información sobre herramientas y restablecer el seguimiento del mouse para que se notifique a la aplicación cuando el puntero del mouse salga del área cliente del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="8acd7-133">The global Boolean variable *g\_TrackingMouse* is used to determine whether it is necessary to reactivate the tooltip and reset mouse tracking so that the application is notified when the mouse pointer leaves the client area of the dialog box.</span></span>


```
//g_hwndTrackingTT is a global HWND variable

case WM_INITDIALOG:

        InitCommonControls();
        g_hwndTrackingTT = CreateTrackingToolTip(IDC_BUTTON1, hDlg, L"");
        return TRUE;

case WM_MOUSELEAVE: // The mouse pointer has left our window. Deactivate the tooltip.
    
    SendMessage(g_hwndTrackingTT, TTM_TRACKACTIVATE, (WPARAM)FALSE, (LPARAM)&g_toolItem);
    g_TrackingMouse = FALSE;
    return FALSE;

case WM_MOUSEMOVE:

    static int oldX, oldY;
    int newX, newY;

    if (!g_TrackingMouse)   // The mouse has just entered the window.
    {                       // Request notification when the mouse leaves.
    
        TRACKMOUSEEVENT tme = { sizeof(TRACKMOUSEEVENT) };
        tme.hwndTrack       = hDlg;
        tme.dwFlags         = TME_LEAVE;
        
        TrackMouseEvent(&tme);

        // Activate the tooltip.
        SendMessage(g_hwndTrackingTT, TTM_TRACKACTIVATE, (WPARAM)TRUE, (LPARAM)&g_toolItem);
        
        g_TrackingMouse = TRUE;
    }

    newX = GET_X_LPARAM(lParam);
    newY = GET_Y_LPARAM(lParam);

    // Make sure the mouse has actually moved. The presence of the tooltip 
    // causes Windows to send the message continuously.
    
    if ((newX != oldX) || (newY != oldY))
    {
        oldX = newX;
        oldY = newY;
            
        // Update the text.
        WCHAR coords[12];
        swprintf_s(coords, ARRAYSIZE(coords), L"%d, %d", newX, newY);
        
        g_toolItem.lpszText = coords;
        SendMessage(g_hwndTrackingTT, TTM_SETTOOLINFO, 0, (LPARAM)&g_toolItem);

        // Position the tooltip. The coordinates are adjusted so that the tooltip does not overlap the mouse pointer.
        
        POINT pt = { newX, newY }; 
        ClientToScreen(hDlg, &pt);
        SendMessage(g_hwndTrackingTT, TTM_TRACKPOSITION, 0, (LPARAM)MAKELONG(pt.x + 10, pt.y - 20));
    }
    return FALSE;
```



## <a name="related-topics"></a><span data-ttu-id="8acd7-134">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8acd7-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8acd7-135">Usar controles ToolTip</span><span class="sxs-lookup"><span data-stu-id="8acd7-135">Using Tooltip Controls</span></span>](using-tooltip-contro.md)
</dt> </dl>

 

 




