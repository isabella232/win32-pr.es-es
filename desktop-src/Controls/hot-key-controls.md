---
title: Acerca de los controles de tecla de acceso
description: Un control de tecla de acceso rápido es una ventana que permite al usuario escribir una combinación de pulsaciones de teclas que se usarán como tecla de acceso rápido.
ms.assetid: 5f011459-4c30-45d4-9668-19f575b041ce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 256fcfde87a1fb6603f90e8a2a41cb4f2cc9356f9f45d861efdc6836aa5344fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118672253"
---
# <a name="about-hot-key-controls"></a>Acerca de los controles de tecla de acceso

Un control de tecla de acceso rápido es una ventana que permite al usuario escribir una combinación de pulsaciones de teclas que se usarán como tecla de acceso rápido. Una tecla de acceso rápido es una combinación de teclas que el usuario puede presionar para realizar una acción rápidamente. Por ejemplo, un usuario puede crear una tecla de acceso activo que active una ventana determinada y la lleva a la parte superior del orden Z. El control de tecla de acceso remoto muestra las opciones del usuario y garantiza que el usuario selecciona una combinación de teclas válida. En la captura de pantalla siguiente se muestra cómo aparece un control de tecla de acceso rápido en un cuadro de diálogo después de que el usuario presione la tecla Alt.

![captura de pantalla de un cuadro de diálogo que contiene un control de tecla de acceso](images/hotkey.png)

## <a name="using-hot-key-controls"></a>Usar controles de tecla de acceso

Cuando el usuario escribe una combinación de teclas que se va a usar como tecla de acceso rápido, los nombres de las claves aparecen en el control de tecla de acceso rápido. Una combinación de teclas puede constar de una tecla modificadora (como CTRL, ALT o MAYÚS) y una tecla que lo acompaña (como una tecla de carácter, una tecla de flecha, una tecla de función, y así sucesivamente).

Una vez que el usuario ha elegido una combinación de teclas, la aplicación recupera la combinación de teclas del control de tecla de acceso y la usa para configurar una tecla de acceso remoto en el sistema. La información recuperada del control de tecla de acceso remoto incluye una marca que indica la tecla modificadora y el código de clave virtual de la clave que lo acompaña.

La aplicación puede usar la información proporcionada por un control de tecla de acceso activo para configurar una clave de acceso activo global o una clave de acceso activo específica del subproceso. Una tecla de acceso activa global está asociada a una ventana determinada; permite al usuario activar la ventana desde cualquier parte del sistema. Una aplicación establece una clave de acceso rápido global mediante el mensaje [**\_ SETHOTKEY de WM.**](/windows/desktop/inputdev/wm-sethotkey) Cada vez que el usuario presiona una tecla de acceso rápido global, la ventana especificada en **WM \_ SETHOTKEY** recibe un mensaje [**\_ SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) de WM que especifica el valor [**DE SC \_ HOTKEY.**](/windows/desktop/inputdev/wm-sethotkey) Este mensaje activa la ventana que lo recibe. La tecla de acceso rápido sigue siendo válida hasta que se cierra la aplicación que llamó **a WM \_ SETHOTKEY.**

Una tecla de acceso rápido específica del subproceso genera un mensaje [**WM \_ HOTKEY**](/windows/desktop/inputdev/wm-hotkey) que se publica al principio de un subproceso determinado para que se quite mediante la siguiente iteración del bucle de mensajes. Una aplicación establece una clave de acceso rápido específica del subproceso mediante la [**función RegisterHotKey.**](/windows/desktop/api/winuser/nf-winuser-registerhotkey)

### <a name="hot-key-control-messages"></a>Mensajes de control de teclas de acceso directo

Después de crear un control de tecla de acceso rápido, una aplicación interactúa con él mediante tres mensajes: [**HKM \_ SETRULES,**](hkm-setrules.md) [**HKM \_ SETHOTKEY**](hkm-sethotkey.md)y [**HKM \_ GETHOTKEY**](hkm-gethotkey.md).

Una aplicación puede enviar el mensaje [**\_ HKM SETRULES**](hkm-setrules.md) para especificar un conjunto de combinaciones de teclas CTRL, ALT y MAYÚS que se consideran teclas de acceso rápido no válidas. Si la aplicación especifica una combinación de claves no válida, también debe especificar una combinación de modificadores predeterminada que se usará cuando el usuario seleccione la combinación no válida. Cuando el usuario escribe la combinación no válida, el sistema realiza una operación OR lógica en la combinación no válida y en la combinación predeterminada. El resultado se considera una combinación válida; se convierte en una cadena y se muestra en el control .

El [**mensaje \_ SETHOTKEY**](hkm-sethotkey.md) de HKM permite a una aplicación establecer la combinación de teclas de acceso rápido para un control de tecla de acceso rápido. Este mensaje también se usa normalmente cuando se crea el control de tecla de acceso remoto.

Las aplicaciones usan el [**mensaje \_ GETHOTKEY**](hkm-gethotkey.md) de HKM para recuperar el código de clave virtual y las marcas modificadoras de la clave de acceso rápido elegida por el usuario.

### <a name="hot-key-control-notifications"></a>Notificaciones de control de teclas de acceso

El control de tecla de acceso remoto no envía ningún código de notificación a través del [**mensaje WM \_ NOTIFY.**](wm-notify.md) Sin embargo, enviará la notificación [EN \_ CHANGE](en-change.md) a través del mensaje [**WM \_ COMMAND**](/windows/desktop/menurc/wm-command) cuando el usuario cambie el contenido del control.

### <a name="default-hot-key-message-processing"></a>Procesamiento predeterminado de mensajes de clave de acceso rápido

En esta sección se describen los mensajes de ventana que controla el procedimiento de ventana para la clase de ventana [**HOTKEY \_ CLASS**](common-control-window-classes.md) predefinida utilizada con controles de tecla de acceso rápido.

|    Message                                            |    Procesamiento realizado                               |
|------------------------------------------------|--------------------------------------------------------------|
| [**WM \_ CHAR**](/windows/desktop/inputdev/wm-char)               | Recupera el código de clave virtual.             |
| [**WM \_ CREATE**](/windows/desktop/winmsg/wm-create)             | Inicializa el control de tecla de acceso remoto, borra las reglas de tecla de acceso y usa la fuente del sistema.   |
| [**WM \_ ERASEBND**](/windows/desktop/winmsg/wm-erasebkgnd)     | Oculta el caret, llama a la [**función DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) y vuelve a mostrar el caret.   |
| [**WM \_ GETDLGCODE**](/windows/desktop/dlgbox/wm-getdlgcode)     | Devuelve una combinación de los [**valores \_ WANTCHARS**](/windows/desktop/dlgbox/wm-getdlgcode) y [**\_ DLGC WANTARROWS de DLGC.**](/windows/desktop/dlgbox/wm-getdlgcode)   |
| [**WM \_ GETFONT**](/windows/desktop/winmsg/wm-getfont)           | Recupera la fuente.                         |
| [**WM \_ KEYDOWN**](/windows/desktop/inputdev/wm-keydown)         | Llama a [**la función DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) si la clave es ENTER, TAB, SPACE BAR, DEL, ESC o BACKSPACE. Si la tecla es MAYÚS, CTRL o ALT, comprueba si la combinación es válida y, si es así, establece la tecla de acceso rápido mediante la combinación. Todas las demás claves se establecen como teclas de acceso rápido sin comprobar primero su validez. |
| [**WM \_ KEYUP**](/windows/desktop/inputdev/wm-keyup)             | Recupera el código de clave virtual.             |
| [**WM \_ KILLFOCUS**](/windows/desktop/inputdev/wm-killfocus)     | Destruye el caret.                         |
| [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) | Establece el foco en la ventana.               |
| [**WM \_ NCCREATE**](/windows/desktop/winmsg/wm-nccreate)         | Establece el [**estilo de ventana \_ \_ CLIENTEDGE de WS EX.**](/windows/desktop/winmsg/extended-window-styles)        |
| [**WM \_ PAINT**](/windows/desktop/gdi/wm-paint)                  | Pinta el control de tecla de acceso remoto.                 |
| [**WM \_ SETFOCUS**](/windows/desktop/inputdev/wm-setfocus)       | Crea y muestra el caret.                |
| [**WM \_ SETFONT**](/windows/desktop/winmsg/wm-setfont)           | Establece la fuente.                              |
| [**WM \_ SYSCHAR**](/windows/desktop/menurc/wm-syschar)           | Recupera el código de clave virtual.             |
| [**WM \_ SYSKEYDOWN**](/windows/desktop/inputdev/wm-syskeydown)   | Llama a [**la función DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) si la clave es ENTER, TAB, SPACE BAR, DEL, ESC o BACKSPACE. Si la tecla es MAYÚS, CTRL o ALT, comprueba si la combinación es válida y, si es así, establece la tecla de acceso rápido mediante la combinación. Todas las demás claves se establecen como teclas de acceso rápido sin comprobar primero su validez. |
| [**WM \_ SYSKEYUP**](/windows/desktop/inputdev/wm-syskeyup)       | Recupera el código de clave virtual.             |
