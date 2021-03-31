---
title: Cómo procesar notificaciones de ComboBoxEx
description: En este tema se muestra cómo procesar mensajes de notificación ComboBoxEx.
ms.assetid: 375634BC-CDD6-4D72-A41E-FCBFCBFE7F03
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a9787e22aa01d51478ca55f0dde5d7ac944decb
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "103995776"
---
# <a name="how-to-process-comboboxex-notifications"></a>Cómo procesar notificaciones de ComboBoxEx

En este tema se muestra cómo procesar mensajes de notificación ComboBoxEx.

## <a name="what-you-need-to-know"></a>Aspectos que debe saber

### <a name="technologies"></a>Tecnologías

-   [Controles de Windows](window-controls.md)

### <a name="prerequisites"></a>Requisitos previos

-   C/C++
-   Programación de la interfaz de usuario de Windows

## <a name="instructions"></a>Instrucciones


Un control ComboBoxEx notifica a su ventana primaria de eventos mediante el envío de mensajes de [**\_ notificación de WM**](wm-notify.md) . También pasa los mensajes de notificación de [**\_ comandos de WM**](/windows/desktop/menurc/wm-command) que recibe del cuadro combinado que contiene en la ventana primaria que se va a procesar. Por lo tanto, la aplicación debe estar preparada para procesar mensajes de **\_ notificación de WM** desde los mensajes de **\_ comando** ComboBoxEx y WM que se reenvían desde el control de cuadro combinado secundario ComboBoxEx.

En el ejemplo de esta sección se tratan los mensajes [**de \_ comandos**](/windows/desktop/menurc/wm-command) de [**\_ Notify**](wm-notify.md) y WM de WM desde un control ComboBoxEx mediante una llamada a una función definida por la aplicación correspondiente para procesar estos mensajes.

## <a name="complete-example"></a>Ejemplo completo


```C++
LRESULT CALLBACK WndProc (HWND hwnd, UINT msg, WPARAM wParam, LPARAM lParam)
{
    switch(msg){

        case WM_COMMAND: // notification from the child ComboBox within the ComboBoxEx control.
            if((HWND)lParam == g_hwndCB)
                DoOldNotify(hwnd,  wParam);  
            break;

        case WM_NOTIFY: // notification from the ComboBoxEx control
            return (DoCBEXNotify(hwnd, lParam));

        case WM_PAINT:
            hdc = BeginPaint(hwnd, &ps);
            EndPaint(hwnd, &ps);
            break;

        case WM_DESTROY:
            PostQuitMessage(0);
            break;

        default:
            return DefWindowProc(hwnd, msg, wParam, lParam);
            break;
    }

    return FALSE;
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de los controles ComboBoxEx](comboboxex-controls.md)
</dt> <dt>

[Referencia de control ComboBoxEx](bumper-comboboxex-comboboxex-control-reference.md)
</dt> <dt>

[Usar controles ComboBoxEx](/windows/desktop/Controls/using-comboboxex)
</dt> <dt>

[ComboBoxEx](comboboxex-control-reference.md)
</dt> </dl>

 

 