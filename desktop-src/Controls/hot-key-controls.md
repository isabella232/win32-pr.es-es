---
title: Acerca de los controles de tecla de acceso rápido
description: Un control de tecla de acceso rápido es una ventana que permite al usuario escribir una combinación de pulsaciones de teclas que se va a utilizar como tecla de acceso rápido.
ms.assetid: 5f011459-4c30-45d4-9668-19f575b041ce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dec45d61df535025cff00fee6428f604aa670bf3
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "103794013"
---
# <a name="about-hot-key-controls"></a>Acerca de los controles de tecla de acceso rápido

Un control de tecla de acceso rápido es una ventana que permite al usuario escribir una combinación de pulsaciones de teclas que se va a utilizar como tecla de acceso rápido. Una tecla de acceso rápido es una combinación de teclas que el usuario puede presionar para realizar una acción rápidamente. Por ejemplo, un usuario puede crear una tecla de acceso rápido que activa una ventana determinada y la coloca en la parte superior del orden z. El control de tecla de acceso rápido muestra las opciones del usuario y garantiza que el usuario selecciona una combinación de teclas válida. En la captura de pantalla siguiente se muestra cómo aparece un control de tecla de acceso rápido en un cuadro de diálogo después de que el usuario presione la tecla Alt.

![captura de pantalla de un cuadro de diálogo que contiene un control de tecla de acceso rápido](images/hotkey.png)

## <a name="using-hot-key-controls"></a>Usar controles de tecla de acceso rápido

Cuando el usuario escribe una combinación de teclas que se va a utilizar como tecla de acceso rápido, los nombres de las claves aparecen en el control de tecla de acceso rápido. Una combinación de teclas puede constar de una tecla modificadora (como CTRL, ALT o Mayús) y una clave adjunta (como una tecla de carácter, una tecla de dirección, una tecla de función, etc.).

Una vez que el usuario ha elegido una combinación de teclas, la aplicación recupera la combinación de teclas del control de teclas de acceso rápido y la utiliza para configurar una tecla de acceso rápido en el sistema. La información recuperada del control de tecla de acceso rápido incluye una marca que indica la tecla modificadora y el código de tecla virtual de la clave correspondiente.

La aplicación puede usar la información proporcionada por un control de tecla de acceso rápido para configurar una tecla de acceso rápido global o una tecla de acceso rápido específica del subproceso. Una tecla de acceso rápido global está asociada a una ventana determinada; permite al usuario activar la ventana desde cualquier parte del sistema. Una aplicación establece una tecla de acceso rápido global mediante el mensaje de [**\_ SETHOTKEY de WM**](/windows/desktop/inputdev/wm-sethotkey) . Siempre que el usuario presiona una tecla de acceso rápido global, la ventana especificada en **WM \_ SETHOTKEY** recibe un mensaje de [**\_ SYSCOMMAND de WM**](/windows/desktop/menurc/wm-syscommand) que especifica el valor de la tecla de acceso [**\_ rápido SC**](/windows/desktop/inputdev/wm-sethotkey) . Este mensaje activa la ventana que lo recibe. La tecla de acceso rápido sigue siendo válida hasta que se cierre la aplicación que llamó a **WM \_ SETHOTKEY** .

Una tecla de acceso rápido específica del subproceso genera un mensaje de [**\_ Hotkey de WM**](/windows/desktop/inputdev/wm-hotkey) que se publica al principio de un subproceso determinado para que se quite por la siguiente iteración del bucle de mensajes. Una aplicación establece una tecla de acceso rápido específica del subproceso mediante la función [**RegisterHotKey**](/windows/desktop/api/winuser/nf-winuser-registerhotkey) .

### <a name="hot-key-control-messages"></a>Mensajes de control de teclas de acceso rápido

Después de crear un control de tecla de acceso rápido, una aplicación interactúa con él mediante tres mensajes: [**HKM \_ SETRULES**](hkm-setrules.md), [**HKM \_ SETHOTKEY**](hkm-sethotkey.md)y [**HKM \_ GETHOTKEY**](hkm-gethotkey.md).

Una aplicación puede enviar el mensaje de [**\_ SETRULES de HKM**](hkm-setrules.md) para especificar un conjunto de combinaciones de teclas Ctrl, Alt y Mayús que se consideran teclas de acceso rápido no válidas. Si la aplicación especifica una combinación de teclas no válida, también debe especificar una combinación de modificadores predeterminada que se utilizará cuando el usuario seleccione la combinación no válida. Cuando el usuario especifica la combinación no válida, el sistema realiza una operación OR lógica en la combinación no válida y la combinación predeterminada. El resultado se considera una combinación válida; se convierte en una cadena y se muestra en el control.

El mensaje [**HKM \_ SETHOTKEY**](hkm-sethotkey.md) permite a una aplicación establecer la combinación de teclas de acceso rápido para un control de tecla de acceso rápido. Este mensaje también se utiliza normalmente cuando se crea el control de tecla de acceso rápido.

Las aplicaciones usan el mensaje [**HKM \_ GETHOTKEY**](hkm-gethotkey.md) para recuperar el código de tecla virtual y los marcadores modificadores de la tecla de acceso rápido elegida por el usuario.

### <a name="hot-key-control-notifications"></a>Notificaciones del control de teclas de acceso rápido

El control de teclas de acceso rápido no envía ningún código de notificación a través del mensaje de notificación de [**WM \_**](wm-notify.md) . Sin embargo, se enviará la notificación de [ \_ cambio en](en-change.md) el a través del mensaje de [**\_ comando de WM**](/windows/desktop/menurc/wm-command) cuando el usuario cambie el contenido del control.

### <a name="default-hot-key-message-processing"></a>Procesamiento de mensajes de tecla de acceso rápido predeterminado

En esta sección se describen los mensajes de ventana que se controlan mediante el procedimiento de ventana de la clase de ventana de [**\_ clase Hotkey**](common-control-window-classes.md) predefinida utilizada con los controles de tecla de acceso rápido.



|                                                |                                                                                                                                                                                                                                                                                                                                               |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Mensaje**                                    | **Procesamiento realizado**                                                                                                                                                                                                                                                                                                                      |
| [**carácter de WM \_**](/windows/desktop/inputdev/wm-char)               | Recupera el código de tecla virtual.                                                                                                                                                                                                                                                                                                               |
| [**creación de WM \_**](/windows/desktop/winmsg/wm-create)             | Inicializa el control de tecla de acceso rápido, borra todas las reglas de teclas de acceso rápido y usa la fuente del sistema.                                                                                                                                                                                                                                                          |
| [**ERASEBKGND de WM \_**](/windows/desktop/winmsg/wm-erasebkgnd)     | Oculta el símbolo de intercalación, llama a la función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) y muestra de nuevo el símbolo de intercalación.                                                                                                                                                                                                                                     |
| [**GETDLGCODE de WM \_**](/windows/desktop/dlgbox/wm-getdlgcode)     | Devuelve una combinación de los valores de [**DLGC \_ WANTCHARS**](/windows/desktop/dlgbox/wm-getdlgcode) y [**DLGC \_ WANTARROWS**](/windows/desktop/dlgbox/wm-getdlgcode) .                                                                                                                                               |
| [**GETFONT de WM \_**](/windows/desktop/winmsg/wm-getfont)           | Recupera la fuente.                                                                                                                                                                                                                                                                                                                           |
| [**KEYDOWN de WM \_**](/windows/desktop/inputdev/wm-keydown)         | Llama a la función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) si la clave es Enter, Tab, Space Bar, del, ESC o retroceso. Si la tecla es Mayús, CTRL o ALT, comprueba si la combinación es válida y, si es así, establece la tecla de acceso rápido mediante la combinación. Todas las demás claves se establecen como teclas de acceso rápido sin su validez comprobada en primer lugar. |
| [**KEYUP de WM \_**](/windows/desktop/inputdev/wm-keyup)             | Recupera el código de tecla virtual.                                                                                                                                                                                                                                                                                                               |
| [**KILLFOCUS de WM \_**](/windows/desktop/inputdev/wm-killfocus)     | Destruye el símbolo de intercalación.                                                                                                                                                                                                                                                                                                                           |
| [**LBUTTONDOWN de WM \_**](/windows/desktop/inputdev/wm-lbuttondown) | Establece el foco en la ventana.                                                                                                                                                                                                                                                                                                                 |
| [**NCCREATE de WM \_**](/windows/desktop/winmsg/wm-nccreate)         | Establece el estilo de ventana [**WS \_ ex \_ CLIENTEDGE**](/windows/desktop/winmsg/extended-window-styles) .                                                                                                                                                                                                                              |
| [**pintura de WM \_**](/windows/desktop/gdi/wm-paint)                  | Dibuja el control de tecla de acceso rápido.                                                                                                                                                                                                                                                                                                                   |
| [**SETFOCUS de WM \_**](/windows/desktop/inputdev/wm-setfocus)       | Crea y muestra el símbolo de intercalación.                                                                                                                                                                                                                                                                                                                  |
| [**WM \_**](/windows/desktop/winmsg/wm-setfont)           | Establece la fuente.                                                                                                                                                                                                                                                                                                                                |
| [**SYSCHAR de WM \_**](/windows/desktop/menurc/wm-syschar)           | Recupera el código de tecla virtual.                                                                                                                                                                                                                                                                                                               |
| [**SYSKEYDOWN de WM \_**](/windows/desktop/inputdev/wm-syskeydown)   | Llama a la función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) si la clave es Enter, Tab, Space Bar, del, ESC o retroceso. Si la tecla es Mayús, CTRL o ALT, comprueba si la combinación es válida y, si es así, establece la tecla de acceso rápido mediante la combinación. Todas las demás claves se establecen como teclas de acceso rápido sin su validez comprobada en primer lugar. |
| [**SYSKEYUP de WM \_**](/windows/desktop/inputdev/wm-syskeyup)       | Recupera el código de tecla virtual.                                                                                                                                                                                                                                                                                                               |



 

 

 