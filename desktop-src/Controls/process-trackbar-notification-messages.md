---
title: Cómo procesar mensajes de notificación de la barra de seguimiento
description: Las barras de seguimiento notifican a su ventana primaria las acciones del usuario enviando al elemento primario un mensaje \_ VSCROLL de WM HSCROLL \_ o WM.
ms.assetid: 83F47A3E-E607-49C2-A8B5-BC8A321D90BB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e211a468c5c107a96fc6b28d12feed219799450828db07be87cd8887b5816bd1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119540325"
---
# <a name="how-to-process-trackbar-notification-messages"></a>Cómo procesar mensajes de notificación de la barra de seguimiento

Las barras de seguimiento notifican a su ventana primaria las acciones del usuario mediante el envío de un mensaje [**\_ VSCROLL**](wm-vscroll.md) de [**WM \_ HSCROLL**](wm-hscroll.md) o WM al elemento primario.

## <a name="what-you-need-to-know"></a>Lo que necesita saber

### <a name="technologies"></a>Tecnologías

-   [Windows Controles](window-controls.md)

### <a name="prerequisites"></a>Prerrequisitos

-   C/C++
-   Windows Interfaz de usuario programación

## <a name="instructions"></a>Instructions

### <a name="process-trackbar-notification-messages"></a>Procesar mensajes de notificación de la barra de seguimiento

El ejemplo de código siguiente es una función a la que se llama cuando la ventana primaria de la barra de seguimiento recibe un [**mensaje \_ HSCROLL de WM.**](wm-hscroll.md) La barra de seguimiento de este ejemplo tiene el [**estilo \_ TBS ENABLESELRANGE.**](trackbar-control-styles.md) La posición del control deslizante se compara con el intervalo de selección y el control deslizante se mueve a la posición inicial o final del intervalo de selección cuando es necesario.


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



## <a name="remarks"></a>Comentarios

Un cuadro de diálogo que contiene una barra de seguimiento [**de estilo \_ TBS VERT**](trackbar-control-styles.md) puede usar esta función cuando recibe un [**mensaje \_ VSCROLL de WM.**](wm-vscroll.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar controles Trackbar](using-trackbar-controls.md)
</dt> </dl>

 

 




