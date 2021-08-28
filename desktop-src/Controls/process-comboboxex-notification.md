---
title: Cómo procesar notificaciones ComboBoxEx
description: En este tema se muestra cómo procesar mensajes de notificación ComboBoxEx.
ms.assetid: 375634BC-CDD6-4D72-A41E-FCBFCBFE7F03
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4ec73c31020283afe5876567a57fc1fbd8a23cee123e9dc417c14c57a86709a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119575495"
---
# <a name="how-to-process-comboboxex-notifications"></a>Cómo procesar notificaciones ComboBoxEx

En este tema se muestra cómo procesar mensajes de notificación ComboBoxEx.

## <a name="what-you-need-to-know"></a>Lo que necesita saber

### <a name="technologies"></a>Tecnologías

-   [Windows Controles](window-controls.md)

### <a name="prerequisites"></a>Prerrequisitos

-   C/C++
-   Windows Interfaz de usuario programación

## <a name="instructions"></a>Instructions


Un control ComboBoxEx notifica a su ventana primaria los eventos mediante el envío [**de mensajes WM \_ NOTIFY.**](wm-notify.md) También pasa los mensajes de [**notificación \_ WM COMMAND**](/windows/desktop/menurc/wm-command) que recibe del cuadro combinado que contiene a la ventana primaria que se va a procesar. Por lo tanto, la aplicación debe estar preparada para procesar los mensajes **WM \_ NOTIFY** de los mensajes ComboBoxEx y **WM \_ COMMAND** que se reenvía desde el control de cuadro combinado secundario ComboBoxEx.

En el ejemplo de esta sección se controlan los mensajes [**WM \_ NOTIFY**](wm-notify.md) y [**WM \_ COMMAND**](/windows/desktop/menurc/wm-command) de un control ComboBoxEx mediante una llamada a una función definida por la aplicación correspondiente para procesar estos mensajes.

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

[Referencia del control ComboBoxEx](bumper-comboboxex-comboboxex-control-reference.md)
</dt> <dt>

[Usar controles ComboBoxEx](/windows/desktop/Controls/using-comboboxex)
</dt> <dt>

[ComboBoxEx](comboboxex-control-reference.md)
</dt> </dl>

 

 