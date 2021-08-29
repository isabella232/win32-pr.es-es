---
title: Cómo implementar información sobre herramientas de seguimiento
description: La información sobre herramientas de seguimiento permanece visible hasta que la aplicación las cierra explícitamente y puede cambiar la posición en la pantalla dinámicamente. Son compatibles con la versión 4.70 y posteriores de los controles comunes.
ms.assetid: 4BE1F9E6-92B6-4CA7-B89A-F2162BC86366
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9b2aaf7475f6a4823e0628ab7010ae32bb8424ef0e90e52396ee20cbc7c7e35
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120085604"
---
# <a name="how-to-implement-tracking-tooltips"></a>Cómo implementar información sobre herramientas de seguimiento

La información sobre herramientas de seguimiento permanece visible hasta que la aplicación las cierra explícitamente y puede cambiar la posición en la pantalla dinámicamente. Son compatibles con la [versión 4.70](common-control-versions.md) y posteriores de los controles comunes.

Para crear una información sobre herramientas de seguimiento, incluya la marca TTF TRACK en el \_ **miembro uFlags** de la [**estructura TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) al enviar el [**mensaje \_ ADDTOOL de TTM.**](ttm-addtool.md)

La aplicación debe activar (mostrar) y desactivar (ocultar) manualmente una información sobre herramientas de seguimiento mediante el envío de un [**mensaje \_ TRACKACTIVATE de TTM.**](ttm-trackactivate.md) Mientras la información sobre herramientas de seguimiento está activa, la aplicación debe especificar la ubicación de la información sobre herramientas mediante el envío de mensajes [**\_ TRACKPOSITION de TTM**](ttm-trackposition.md) al control de información sobre herramientas. Dado que la aplicación controla tareas como colocar la información sobre herramientas, la información sobre herramientas de seguimiento no usa la marca **\_ SUBCLASS** de TTF ni el mensaje [**\_ RELAYEVENT de TTM.**](ttm-relayevent.md)

El [**mensaje \_ TRACKPOSITION de TTM**](ttm-trackposition.md) hace que el control de información sobre herramientas muestre la ventana con uno de los dos estilos de selección de ubicación:

-   De forma predeterminada, la información sobre herramientas se muestra junto a la herramienta correspondiente en una posición que elija el control. La ubicación elegida es relativa a las coordenadas que se proporcionan mediante este mensaje.
-   Si incluye el valor **ABSOLUTO de TTF \_** en el miembro de la estructura [**TOOLINFO,**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) la información sobre herramientas se muestra en la ubicación de píxeles especificada en el mensaje. En este caso, el control no intenta cambiar la ubicación de la ventana de información sobre herramientas de las coordenadas que proporcione.

## <a name="what-you-need-to-know"></a>Lo que necesita saber

### <a name="technologies"></a>Tecnologías

-   [Windows Controles](window-controls.md)

### <a name="prerequisites"></a>Requisitos previos

-   C/C++
-   Windows Interfaz de usuario programación

## <a name="instructions"></a>Instructions

### <a name="implement-in-place-tooltips"></a>Implementación de In-Place información sobre herramientas

El **miembro uFlags** de la [**estructura TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) que se usa en el ejemplo incluye la **marca TTF \_ ABSOLUTE.** Sin esta marca, el control de información sobre herramientas elige dónde mostrar la información sobre herramientas y su posición con respecto al cuadro de diálogo puede cambiar repentinamente a medida que se mueve el puntero del mouse.

> [!Note]  
> `g_toolItem` es una estructura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) global.

 

En el ejemplo siguiente se muestra cómo crear un control de información sobre herramientas de seguimiento. En el ejemplo se especifica el área de cliente completa de la ventana principal como herramienta.


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



### <a name="window-procedure-implementation"></a>Implementación de procedimientos de ventana

Cuando el puntero del mouse está dentro del área de cliente, la información sobre herramientas está activa y muestra las coordenadas del cursor, como se muestra en la ilustración siguiente.

![captura de pantalla de un cuadro de diálogo; una información sobre herramientas muestra las coordenadas x e y del puntero del mouse](images/tt-tracking.png)

El código de ejemplo siguiente es del procedimiento de ventana de un cuadro de diálogo que muestra la información sobre herramientas de seguimiento creada en el ejemplo anterior. La variable booleana global *g \_ TrackingMouse* se usa para determinar si es necesario reactivar la información sobre herramientas y restablecer el seguimiento del mouse para que la aplicación se notifique cuando el puntero del mouse salga del área de cliente del cuadro de diálogo.


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

[Uso de controles de información sobre herramientas](using-tooltip-contro.md)
</dt> </dl>

 

 




