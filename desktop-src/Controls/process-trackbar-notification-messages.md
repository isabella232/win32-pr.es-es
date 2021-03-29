---
title: Cómo procesar mensajes de notificación de TrackBar
description: Trackbars notifique a su ventana primaria de las acciones del usuario mediante el envío de un mensaje primario a WM \_ HSCROLL o WM \_ VSCROLL.
ms.assetid: 83F47A3E-E607-49C2-A8B5-BC8A321D90BB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c723ad1bebb5c9f3ec8c4e7aefdc658e0881aef6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103774544"
---
# <a name="how-to-process-trackbar-notification-messages"></a>Cómo procesar mensajes de notificación de TrackBar

Trackbars notifique a su ventana primaria de las acciones del usuario mediante el envío de un mensaje primario a [**WM \_ HSCROLL**](wm-hscroll.md) o [**WM \_ VSCROLL**](wm-vscroll.md) .

## <a name="what-you-need-to-know"></a>Aspectos que debe saber

### <a name="technologies"></a>Tecnologías

-   [Controles de Windows](window-controls.md)

### <a name="prerequisites"></a>Requisitos previos

-   C/C++
-   Programación de la interfaz de usuario de Windows

## <a name="instructions"></a>Instrucciones

### <a name="process-trackbar-notification-messages"></a>Procesar mensajes de notificación de TrackBar

El siguiente ejemplo de código es una función a la que se llama cuando la ventana primaria de la barra de control recibe un mensaje de [**\_ HSCROLL de WM**](wm-hscroll.md) . La barra de error de este ejemplo tiene el estilo [**TBS \_ ENABLESELRANGE**](trackbar-control-styles.md) . La posición del control deslizante se compara con el intervalo de selección, y el control deslizante se mueve a la posición inicial o final del intervalo de selección cuando sea necesario.


```
// TBNotifications - handles trackbar notifications received 
// in the wParam parameter of WM_HSCROLL. This function simply 
// ensures that the slider remains within the selection range. 

VOID WINAPI TBNotifications( 
    WPARAM wParam,  // wParam of WM_HSCROLL message 
    HWND hwndTrack, // handle of trackbar window 
    UINT iSelMin,   // minimum value of trackbar selection 
    UINT iSelMax)   // maximum value of trackbar selection 
    { 
    DWORD dwPos;    // current position of slider 

    switch (LOWORD(wParam)) { 
    
        case TB_ENDTRACK:
          
            dwPos = SendMessage(hwndTrack, TBM_GETPOS, 0, 0); 
            
            if (dwPos > iSelMax) 
                SendMessage(hwndTrack, TBM_SETPOS, 
                    (WPARAM) TRUE,       // redraw flag 
                    (LPARAM) iSelMax); 
                    
            else if (dwPos < iSelMin) 
                SendMessage(hwndTrack, TBM_SETPOS, 
                    (WPARAM) TRUE,       // redraw flag 
                    (LPARAM) iSelMin); 
            
            break; 

        default: 
        
            break; 
        } 
} 
```



## <a name="remarks"></a>Observaciones

Un cuadro de diálogo que contiene una barra de propiedades de estilo [**TBS \_ Vert**](trackbar-control-styles.md) puede utilizar esta función cuando recibe un mensaje de [**\_ VSCROLL de WM**](wm-vscroll.md) .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar controles TrackBar](using-trackbar-controls.md)
</dt> </dl>

 

 




