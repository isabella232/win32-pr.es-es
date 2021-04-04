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
# <a name="how-to-implement-tracking-tooltips"></a>Cómo implementar la información sobre herramientas de seguimiento

La información sobre herramientas de seguimiento permanece visible hasta que la aplicación la cierra explícitamente, y puede cambiar la posición de la pantalla de forma dinámica. Son compatibles con la [versión 4,70](common-control-versions.md) y versiones posteriores de los controles comunes.

Para crear una información sobre herramientas de seguimiento, incluya la \_ marca de seguimiento ttf en el miembro **uFlags** de la estructura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) al enviar el mensaje [**TTM \_ ADDTOOL**](ttm-addtool.md) .

La aplicación debe activar (Mostrar) y desactivar (ocultar) manualmente la información sobre herramientas de seguimiento mediante el envío de un mensaje de [**TTM \_ TRACKACTIVATE**](ttm-trackactivate.md) . Mientras que la información sobre herramientas de seguimiento está activa, la aplicación debe especificar la ubicación de la información sobre herramientas mediante el envío de mensajes de [**TTM \_ TRACKPOSITION**](ttm-trackposition.md) al control ToolTip. Dado que la aplicación controla tareas como colocar la información sobre herramientas, el seguimiento de la información sobre herramientas no utiliza la marca de **\_ subclase ttf** ni el mensaje [**\_ RELAYEVENT de TTM**](ttm-relayevent.md) .

El [**mensaje \_ TRACKPOSITION de TTM**](ttm-trackposition.md) hace que el control de información sobre herramientas muestre la ventana con uno de los dos estilos de colocación:

-   De forma predeterminada, la información sobre herramientas se muestra junto a la herramienta correspondiente en una posición que el control elige. La ubicación elegida es relativa a las coordenadas que se proporcionan con este mensaje.
-   Si incluye el valor **\_ absoluto de ttf** en el miembro de la estructura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) , la información sobre herramientas se muestra en la ubicación de píxeles especificada en el mensaje. En este caso, el control no intenta cambiar la ubicación de la ventana de información sobre herramientas de las coordenadas proporcionadas.

## <a name="what-you-need-to-know"></a>Aspectos que debe saber

### <a name="technologies"></a>Tecnologías

-   [Controles de Windows](window-controls.md)

### <a name="prerequisites"></a>Requisitos previos

-   C/C++
-   Programación de la interfaz de usuario de Windows

## <a name="instructions"></a>Instrucciones

### <a name="implement-in-place-tooltips"></a>Implementar In-Place información sobre herramientas

El miembro **uFlags** de la estructura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) que se usa en el ejemplo incluye la **marca \_ absoluta ttf** . Sin esta marca, el control ToolTip elige dónde Mostrar la información sobre herramientas y su posición relativa al cuadro de diálogo puede cambiar repentinamente cuando se mueve el puntero del mouse.

> [!Note]  
> `g_toolItem` es una estructura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) global.

 

En el ejemplo siguiente se muestra cómo crear un control de información sobre herramientas de seguimiento. En el ejemplo se especifica el área de cliente completa de la ventana principal como la herramienta.


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



### <a name="window-procedure-implementation"></a>Implementación del procedimiento de ventana

Cuando el puntero del mouse se encuentra dentro del área cliente, la información sobre herramientas está activa y muestra las coordenadas del cursor, tal como se muestra en la siguiente ilustración.

![captura de pantalla de un cuadro de diálogo; la información sobre herramientas muestra las coordenadas x e y del puntero del mouse](images/tt-tracking.png)

El siguiente código de ejemplo se encuentra en el procedimiento de ventana de un cuadro de diálogo que muestra la información sobre herramientas de seguimiento creada en el ejemplo anterior. La variable booleana global *g \_ TrackingMouse* se usa para determinar si es necesario reactivar la información sobre herramientas y restablecer el seguimiento del mouse para que se notifique a la aplicación cuando el puntero del mouse salga del área cliente del cuadro de diálogo.


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



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar controles ToolTip](using-tooltip-contro.md)
</dt> </dl>

 

 




