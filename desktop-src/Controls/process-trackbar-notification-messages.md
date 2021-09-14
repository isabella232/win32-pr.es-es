---
title: Cómo procesar mensajes de notificación de la barra de seguimiento
description: Las barras de seguimiento notifican a su ventana primaria las acciones del usuario enviando al elemento primario un mensaje \_ WM HSCROLL o WM \_ VSCROLL.
ms.assetid: 83F47A3E-E607-49C2-A8B5-BC8A321D90BB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c723ad1bebb5c9f3ec8c4e7aefdc658e0881aef6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167629"
---
# <a name="how-to-process-trackbar-notification-messages"></a>Cómo procesar mensajes de notificación de la barra de seguimiento

Las barras de seguimiento notifican a su ventana primaria las acciones del usuario enviando al elemento primario un mensaje [**\_ WM HSCROLL**](wm-hscroll.md) [**o WM \_ VSCROLL.**](wm-vscroll.md)

## <a name="what-you-need-to-know"></a>Lo que necesita saber

### <a name="technologies"></a>Tecnologías

-   [Windows Controles](window-controls.md)

### <a name="prerequisites"></a>Requisitos previos

-   C/C++
-   Windows Interfaz de usuario programación

## <a name="instructions"></a>Instrucciones

### <a name="process-trackbar-notification-messages"></a>Procesar mensajes de notificación de la barra de seguimiento

El ejemplo de código siguiente es una función a la que se llama cuando la ventana primaria de la barra de seguimiento recibe un [**mensaje \_ WM HSCROLL.**](wm-hscroll.md) La barra de seguimiento de este ejemplo tiene el [**estilo \_ ENABLESELRANGE de TBS.**](trackbar-control-styles.md) La posición del control deslizante se compara con el intervalo de selección y el control deslizante se mueve a la posición inicial o final del intervalo de selección cuando sea necesario.


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

Un cuadro de diálogo que contiene una barra de [**seguimiento de estilo \_ VERT**](trackbar-control-styles.md) de TBS puede usar esta función cuando recibe un [**mensaje \_ VSCROLL de WM.**](wm-vscroll.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar controles trackbar](using-trackbar-controls.md)
</dt> </dl>

 

 




