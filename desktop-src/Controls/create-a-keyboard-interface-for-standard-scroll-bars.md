---
title: Cómo crear una interfaz de teclado para barras de desplazamiento estándar
description: Aunque un control de barra de desplazamiento proporciona una interfaz de teclado integrada, una barra de desplazamiento estándar no lo hace.
ms.assetid: 249D0077-6E61-479A-91D5-A4BD9752B82E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f25994639a40a6380bbf2f9cc0075e8a78b9e15787dbdf1babf0e6a15550faf1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119698745"
---
# <a name="how-to-create-a-keyboard-interface-for-standard-scroll-bars"></a>Cómo crear una interfaz de teclado para barras de desplazamiento estándar

Aunque un control de barra de desplazamiento proporciona una interfaz de teclado integrada, una barra de desplazamiento estándar no lo hace. Para implementar una interfaz de teclado para una barra de desplazamiento estándar, un procedimiento de ventana debe procesar el mensaje [**WM \_ KEYDOWN**](/windows/desktop/inputdev/wm-keydown) y examinar el código de clave virtual especificado por el *parámetro wParam.* Si el código de clave virtual corresponde a una tecla de flecha, el procedimiento de ventana se envía a sí mismo un mensaje [**WM \_ HSCROLL**](wm-hscroll.md) o [**WM \_ VSCROLL**](wm-vscroll.md) con la palabra de orden bajo del parámetro *wParam* establecida en el código de solicitud de barra de desplazamiento adecuado.

Por ejemplo, cuando el usuario presiona la tecla de flecha ARRIBA, el procedimiento de ventana recibe un mensaje [**WM \_ KEYDOWN**](/windows/desktop/inputdev/wm-keydown) con *wParam* igual a VK \_ UP. En respuesta, el procedimiento de ventana se envía a sí mismo un mensaje [**\_ VSCROLL de WM**](wm-vscroll.md) con la palabra de orden bajo *de wParam* establecida en el código de \_ solicitud LINEUP de SB.

## <a name="what-you-need-to-know"></a>Lo que necesita saber

### <a name="technologies"></a>Tecnologías

-   [Windows Controles](window-controls.md)

### <a name="prerequisites"></a>Prerrequisitos

-   C/C++
-   Windows Interfaz de usuario programación

## <a name="instructions"></a>Instructions

### <a name="create-a-keyboard-interface-for-a-standard-scroll-bar"></a>Crear una interfaz de teclado para una barra de desplazamiento estándar

En el ejemplo de código siguiente se muestra cómo incluir una interfaz de teclado para una barra de desplazamiento estándar.


```C++
    case WM_KEYDOWN: 
    {
        WORD wScrollNotify = 0xFFFF;

        switch (wParam) 
        { 
            case VK_UP: 
                wScrollNotify = SB_LINEUP; 
                break; 
 
            case VK_PRIOR: 
                wScrollNotify = SB_PAGEUP; 
                break; 
 
            case VK_NEXT: 
                wScrollNotify = SB_PAGEDOWN; 
                break; 
 
            case VK_DOWN: 
                wScrollNotify = SB_LINEDOWN; 
                break; 
 
            case VK_HOME: 
                wScrollNotify = SB_TOP; 
                break; 
 
            case VK_END: 
                wScrollNotify = SB_BOTTOM; 
                break; 
        } 
 
        if (wScrollNotify != -1) 
            SendMessage(hwnd, WM_VSCROLL, MAKELONG(wScrollNotify, 0), 0L); 
 
        break; 
    }
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar barras de desplazamiento](using-scroll-bars.md)
</dt> <dt>

[Windows demostración de controles comunes (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 