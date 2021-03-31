---
title: Cerrar la ventana
description: Cuando el usuario cierra una ventana, esa acción desencadena una secuencia de mensajes de ventana.
ms.assetid: f0449f11-0569-4a3a-92bc-bced7e0db516
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6422966d6b0351654632a1c77b7ebf07e2b5ffef
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103904610"
---
# <a name="closing-the-window"></a>Cerrar la ventana

Cuando el usuario cierra una ventana, esa acción desencadena una secuencia de mensajes de ventana.

El usuario puede cerrar una ventana de la aplicación haciendo clic en el botón **cerrar** o usando un método abreviado de teclado, como Alt + F4. Cualquiera de estas acciones hace que la ventana reciba un mensaje de [**\_ cierre de WM**](/windows/desktop/winmsg/wm-close) . El mensaje de **\_ cierre de WM** le ofrece la oportunidad de preguntar al usuario antes de cerrar la ventana. Si realmente desea cerrar la ventana, llame a la función [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) . De lo contrario, simplemente devuelva cero desde el mensaje de **\_ cierre de WM** y el sistema operativo omitirá el mensaje y no destruirá la ventana.

Este es un ejemplo de cómo un programa puede controlar [**el \_ cierre de WM**](/windows/desktop/winmsg/wm-close).

```C++
case WM_CLOSE:
    if (MessageBox(hwnd, L"Really quit?", L"My application", MB_OKCANCEL) == IDOK)
    {
        DestroyWindow(hwnd);
    }
    // Else: User canceled. Do nothing.
    return 0;
```

En este ejemplo, la función [**MessageBox**](/windows/desktop/api/winuser/nf-winuser-messagebox) muestra un cuadro de diálogo modal que contiene los botones **Aceptar** y **Cancelar** . Si el usuario hace clic en **Aceptar**, el programa llama a [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow). De lo contrario, si el usuario hace clic en **Cancelar**, se omite la llamada a **DestroyWindow** y la ventana permanece abierta. En cualquier caso, devuelva cero para indicar que se ha controlado el mensaje.

Si desea cerrar la ventana sin preguntar al usuario, puede llamar simplemente a [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) sin la llamada a [**MessageBox**](/windows/desktop/api/winuser/nf-winuser-messagebox). Sin embargo, en este caso, hay un acceso directo. Recuerde que [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) ejecuta la acción predeterminada para cualquier mensaje de ventana. En el caso de [**\_ Close de WM**](/windows/desktop/winmsg/wm-close), **DefWindowProc** llama automáticamente a **DestroyWindow**. Esto significa que si se omite el mensaje de **\_ cierre de WM** en la instrucción **Switch** , la ventana se destruye de forma predeterminada.

Cuando una ventana está a punto de ser destruida, recibe un mensaje de [**\_ destrucción de WM**](/windows/desktop/winmsg/wm-destroy) . Este mensaje se envía después de quitar la ventana de la pantalla, pero antes de que se produzca la destrucción (en particular, antes de que se destruyan las ventanas secundarias).

En la ventana principal de la aplicación, normalmente responderá a la [**\_ destrucción de WM**](/windows/desktop/winmsg/wm-destroy) mediante una llamada a [**PostQuitMessage**](/windows/desktop/api/winuser/nf-winuser-postquitmessage).

```C++
case WM_DESTROY:
    PostQuitMessage(0);
    return 0;
```

Vimos en la sección de [mensajes de ventana](window-messages.md) que [**PostQuitMessage**](/windows/desktop/api/winuser/nf-winuser-postquitmessage) coloca un mensaje de [**\_ salida de WM**](/windows/desktop/winmsg/wm-quit) en la cola de mensajes, lo que hace que el bucle de mensajes finalice.

Este es un diagrama de flujo en el que se muestra la manera habitual de procesar los mensajes de [**WM \_ Close**](/windows/desktop/winmsg/wm-close) y [**WM \_ Destroy**](/windows/desktop/winmsg/wm-destroy) :

![diagrama de flujo que muestra cómo controlar \- los mensajes de WM Close y WM \- Destroy](images/wmclose01.png)

## <a name="next"></a>Siguientes

[Administración del estado de la aplicación](managing-application-state-.md)