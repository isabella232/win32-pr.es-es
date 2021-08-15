---
title: Cerrar la ventana
description: Cuando el usuario cierra una ventana, esa acción desencadena una secuencia de mensajes de ventana.
ms.assetid: f0449f11-0569-4a3a-92bc-bced7e0db516
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7aaf6922f730e63fa9ab38a8f6baa9009dabf77b2ffeddc2117dcd09ffc08a9b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119328795"
---
# <a name="closing-the-window"></a>Cerrar la ventana

Cuando el usuario cierra una ventana, esa acción desencadena una secuencia de mensajes de ventana.

El usuario puede cerrar una ventana de la aplicación haciendo clic en el botón **Cerrar** o usando un método abreviado de teclado como ALT+F4. Cualquiera de estas acciones hace que la ventana reciba un [**mensaje WM \_ CLOSE.**](/windows/desktop/winmsg/wm-close) El **mensaje \_ WM CLOSE** le ofrece la oportunidad de preguntar al usuario antes de cerrar la ventana. Si realmente desea cerrar la ventana, llame a la [**función DestroyWindow.**](/windows/desktop/api/winuser/nf-winuser-destroywindow) De lo contrario, simplemente devuelva cero desde el **mensaje WM \_ CLOSE** y el sistema operativo omitirá el mensaje y no destruirá la ventana.

Este es un ejemplo de cómo un programa podría controlar [**WM \_ CLOSE**](/windows/desktop/winmsg/wm-close).

```C++
case WM_CLOSE:
    if (MessageBox(hwnd, L"Really quit?", L"My application", MB_OKCANCEL) == IDOK)
    {
        DestroyWindow(hwnd);
    }
    // Else: User canceled. Do nothing.
    return 0;
```

En este ejemplo, la función [**MessageBox**](/windows/desktop/api/winuser/nf-winuser-messagebox) muestra un cuadro de diálogo modal que contiene **los botones Aceptar** **y** Cancelar. Si el usuario hace clic en **Aceptar,** el programa llama a [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow). De lo contrario, si el usuario hace clic **en Cancelar**, se omite la llamada a **DestroyWindow** y la ventana permanece abierta. En cualquier caso, devuelva cero para indicar que controló el mensaje.

Si desea cerrar la ventana sin preguntar al usuario, simplemente podría llamar a [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) sin la llamada a [**MessageBox**](/windows/desktop/api/winuser/nf-winuser-messagebox). Sin embargo, hay un acceso directo en este caso. Recuerde que [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) ejecuta la acción predeterminada para cualquier mensaje de ventana. En el caso de [**WM \_ CLOSE,**](/windows/desktop/winmsg/wm-close) **DefWindowProc** llama automáticamente a **DestroyWindow**. Esto significa que si omite el **mensaje WM \_ CLOSE** en la **instrucción switch,** la ventana se destruye de forma predeterminada.

Cuando una ventana está a punto de destruirse, recibe un [**mensaje WM \_ DESTROY.**](/windows/desktop/winmsg/wm-destroy) Este mensaje se envía después de quitar la ventana de la pantalla, pero antes de que se produzca la destrucción (en concreto, antes de que se destruyan las ventanas secundarias).

En la ventana principal de la aplicación, normalmente responderá a [**WM \_ DESTROY**](/windows/desktop/winmsg/wm-destroy) llamando a [**PostQuitMessage**](/windows/desktop/api/winuser/nf-winuser-postquitmessage).

```C++
case WM_DESTROY:
    PostQuitMessage(0);
    return 0;
```

Hemos visto en la sección [Mensajes de](window-messages.md) ventana que [**PostQuitMessage**](/windows/desktop/api/winuser/nf-winuser-postquitmessage) coloca un mensaje [**DE SALIDA \_ de WM**](/windows/desktop/winmsg/wm-quit) en la cola de mensajes, lo que hace que el bucle de mensajes finalice.

Este es un gráfico de flujo que muestra la manera típica de procesar [**mensajes WM \_ CLOSE**](/windows/desktop/winmsg/wm-close) [**y WM \_ DESTROY:**](/windows/desktop/winmsg/wm-destroy)

![diagrama de flujo que muestra cómo controlar los mensajes wm \- close y wm \- destroy](images/wmclose01.png)

## <a name="next"></a>Siguientes

[Administración del estado de la aplicación](managing-application-state-.md)