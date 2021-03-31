---
title: Cómo crear una interfaz de teclado para las barras de desplazamiento estándar
description: Aunque un control de barra de desplazamiento proporciona una interfaz de teclado integrada, no existe una barra de desplazamiento estándar.
ms.assetid: 249D0077-6E61-479A-91D5-A4BD9752B82E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43b739638d95d9f3e530718f8e9b9e6168069420
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "103904846"
---
# <a name="how-to-create-a-keyboard-interface-for-standard-scroll-bars"></a>Cómo crear una interfaz de teclado para las barras de desplazamiento estándar

Aunque un control de barra de desplazamiento proporciona una interfaz de teclado integrada, no existe una barra de desplazamiento estándar. Para implementar una interfaz de teclado para una barra de desplazamiento estándar, un procedimiento de ventana debe procesar el mensaje de [**\_ KEYDOWN de WM**](/windows/desktop/inputdev/wm-keydown) y examinar el código de la clave virtual especificado por el parámetro *wParam* . Si el código de la clave virtual corresponde a una tecla de dirección, el procedimiento de ventana se envía a sí mismo un mensaje de [**WM \_ HSCROLL**](wm-hscroll.md) o [**WM \_ VSCROLL**](wm-vscroll.md) con la palabra de orden inferior del parámetro *wParam* establecida en el código de solicitud de la barra de desplazamiento correspondiente.

Por ejemplo, cuando el usuario presiona la tecla de dirección arriba, el procedimiento de ventana recibe un mensaje [**\_ KEYDOWN de WM**](/windows/desktop/inputdev/wm-keydown) con *wParam* igual a VK \_ up. En respuesta, el procedimiento de ventana se envía a sí mismo un mensaje de [**WM \_ VSCROLL**](wm-vscroll.md) con la palabra de orden inferior de *wParam* establecida en el código de solicitud de la línea de SB \_ .

## <a name="what-you-need-to-know"></a>Aspectos que debe saber

### <a name="technologies"></a>Tecnologías

-   [Controles de Windows](window-controls.md)

### <a name="prerequisites"></a>Requisitos previos

-   C/C++
-   Programación de la interfaz de usuario de Windows

## <a name="instructions"></a>Instrucciones

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

[Demostración de controles comunes de Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 