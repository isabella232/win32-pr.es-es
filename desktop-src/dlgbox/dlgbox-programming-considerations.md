---
title: Consideraciones sobre la programación de cuadros de diálogo
description: Esta información general describe algunas consideraciones de programación relativas a los cuadros de diálogo.
ms.assetid: 49024a0f-ea92-4d56-b063-8e5fcdbd884a
keywords:
- Windows Interfaz de usuario,windowing
- Windows Interfaz de usuario,cuadros de diálogo
- ventanas, cuadros de diálogo
- cuadros de diálogo, acerca de
- procedimientos del cuadro de diálogo
- cuadros de diálogo, procedimientos
- WM_INITDIALOG mensaje
- WM_COMMAND mensaje
- WM_PARENTNOTIFY mensaje
- mensajes de color de control
- cuadros de diálogo, procesamiento de mensajes
- cuadros de diálogo, interfaz de teclado
- cuadros de diálogo, mnemonics
- cuadros de diálogo, personalizados
- cuadros de diálogo personalizados
- cuadros de diálogo, configuración
ms.topic: article
ms.date: 08/25/2020
ms.openlocfilehash: 956f700841b0a3d76b7e071f0232382507394879a0253bc4cbcea533fdbb23bf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119456255"
---
# <a name="dialog-box-programming-considerations"></a>Consideraciones sobre la programación de cuadros de diálogo

Esta información general describe algunas consideraciones de programación relativas a los cuadros de diálogo.

La información general incluye los temas siguientes.

-   [Procedimientos de cuadro de diálogo](#dialog-box-procedures)
    -   [El mensaje \_ WM INITDIALOG](wm-initdialog.md)
    -   [El mensaje \_ WM COMMAND](/windows/desktop/menurc/wm-command)
    -   [Mensaje \_ PARENTNOTIFY de WM](/previous-versions/windows/desktop/inputmsg/wm-parentnotify)
    -   [Mensajes de color de control](#control-color-messages)
    -   [Procesamiento de mensajes predeterminado del cuadro de diálogo](#dialog-box-default-message-processing)
-   [Interfaz de teclado del cuadro de diálogo](#dialog-box-keyboard-interface)
    -   [El estilo \_ TABSTOP de WS](/windows/desktop/winmsg/window-styles)
    -   [El estilo de WS \_ GROUP](/windows/desktop/winmsg/window-styles)
    -   [Mnemónicas](#mnemonics)
-   [Cuadro de diálogo Configuración](#dialog-box-settings)
    -   [Botones de radio y casillas](#radio-buttons-and-check-boxes)
    -   [Controles de edición de cuadro de diálogo](#dialog-box-edit-controls)
    -   [Cuadros de lista, cuadros combinados y listas de directorios](#list-boxes-combo-boxes-and-directory-listings)
    -   [Mensajes de control de cuadro de diálogo](#dialog-box-control-messages)
-   [Cuadros de diálogo personalizados](#custom-dialog-boxes)

## <a name="dialog-box-procedures"></a>Procedimientos de cuadro de diálogo

Un procedimiento de cuadro de diálogo es similar a un procedimiento de ventana en el que el sistema envía mensajes al procedimiento cuando tiene información que proporcionar o tareas para llevar a cabo. A diferencia de un procedimiento de ventana, un procedimiento de cuadro de diálogo nunca llama a la [**función DefWindowProc.**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) En su lugar, **devuelve TRUE** si procesa un mensaje o **FALSE** si no lo hace.

Cada procedimiento de cuadro de diálogo tiene el formato siguiente:

```cpp
BOOL CALLBACK DlgProc(HWND hwndDlg, UINT message, WPARAM wParam, LPARAM lParam) 
{ 
    switch (message) 
    { 
 
        // Place message cases here. 
 
        default: 
            return FALSE; 
    } 
}
```

Los parámetros de procedimiento tienen el mismo propósito que en un procedimiento de ventana, y el *parámetro hwndDlg* recibe el identificador de ventana del cuadro de diálogo.

La mayoría de los procedimientos de cuadro de diálogo procesan el mensaje [**\_ WM INITDIALOG**](wm-initdialog.md) y los [**mensajes WM \_ COMMAND**](/windows/desktop/menurc/wm-command) enviados por los controles, pero procesan pocos mensajes si hay otros. Si un procedimiento de cuadro de diálogo no procesa un mensaje, debe devolver **FALSE** para que el sistema procese los mensajes internamente. La única excepción a esta regla es el **mensaje \_ INITDIALOG de WM.** El procedimiento del cuadro de diálogo debe devolver **TRUE para** dirigir el sistema para procesar aún más el mensaje **WM \_ INITDIALOG.** En cualquier caso, el procedimiento no debe llamar [**a DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).

- [El mensaje \_ WM INITDIALOG](#the-wm_initdialog-message)
- [El mensaje \_ WM COMMAND](#the-wm_command-message)
- [Mensaje \_ PARENTNOTIFY de WM](#the-wm_parentnotify-message)
- [Mensajes de color de control](#control-color-messages)
- [Procesamiento de mensajes predeterminado del cuadro de diálogo](#dialog-box-default-message-processing)

### <a name="the-wm_initdialog-message"></a>El mensaje \_ WM INITDIALOG

El sistema no envía un mensaje [**WM \_ CREATE**](/windows/desktop/winmsg/wm-create) al procedimiento del cuadro de diálogo. En su lugar, envía un [**mensaje \_ WM INITDIALOG**](wm-initdialog.md) cuando crea el cuadro de diálogo y todos sus controles, pero antes de mostrar el cuadro de diálogo. El procedimiento debe llevar a cabo cualquier inicialización necesaria para asegurarse de que el cuadro de diálogo muestra la configuración actual asociada a la tarea. Por ejemplo, cuando un cuadro de diálogo contiene un control para mostrar la unidad y el directorio actuales, el procedimiento debe determinar la unidad y el directorio actuales y establecer el control en ese valor.

El procedimiento puede inicializar controles mediante funciones como [**SetDlgItemText**](/windows/desktop/api/Winuser/nf-winuser-setdlgitemtexta) y [**CheckDlgButton**](https://msdn.microsoft.com/library/Cc410649(v=MSDN.10).aspx). Dado que los controles son ventanas, el procedimiento también puede manipularlos mediante funciones de administración de ventanas como [**EnableWindow**](/windows/desktop/api/winuser/nf-winuser-enablewindow) y [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus). El procedimiento puede recuperar el identificador de ventana de un control mediante la [**función GetDlgItem.**](/windows/desktop/api/Winuser/nf-winuser-getdlgitem)

El procedimiento del cuadro de diálogo puede cambiar el contenido, el estado y la posición de cualquier control según sea necesario. Por ejemplo, en un cuadro de diálogo que  contiene un cuadro de  lista de nombres de archivo y un botón Abrir, el procedimiento puede deshabilitar el botón Abrir hasta que el usuario seleccione un archivo de la lista. En este ejemplo, la plantilla de cuadro de  diálogo especifica el estilo [**WS \_ DISABLED**](/windows/desktop/winmsg/window-styles) para el botón Abrir y el sistema deshabilita automáticamente el botón al crearlo. Cuando el procedimiento del cuadro de diálogo recibe un mensaje de notificación del cuadro de lista que indica que el usuario ha seleccionado un archivo, el procedimiento llama a la función [**EnableWindow**](/windows/desktop/api/winuser/nf-winuser-enablewindow) para habilitar el **botón** Abrir.

Para mostrar un icono personalizado en la barra de título del cuadro de diálogo, el controlador [**WM \_ INITDIALOG**](wm-initdialog.md) puede enviar el mensaje [**\_ SETICON**](/windows/desktop/winmsg/wm-seticon) de WM al cuadro de diálogo.

Si la aplicación crea el cuadro de diálogo mediante una de las funciones [**DialogBoxParam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxparama), [**DialogBoxIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirectparama), [**CreateDialogParam**](/windows/desktop/api/Winuser/nf-winuser-createdialogparama)o [**CreateDialogIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirectparama), el parámetro *lParam* para el mensaje [**WM \_ INITDIALOG**](wm-initdialog.md) contiene el parámetro adicional pasado a la función. Normalmente, las aplicaciones usan este parámetro adicional para pasar un puntero a información de inicialización adicional al procedimiento del cuadro de diálogo, pero el procedimiento del cuadro de diálogo debe determinar el significado del parámetro. Si la aplicación usa otra función para crear el cuadro de diálogo, el sistema establece el *parámetro lParam* en **NULL.**

Antes de volver del [**mensaje \_ WM INITDIALOG,**](wm-initdialog.md) el procedimiento debe determinar si debe establecer el foco de entrada en un control especificado. Si el procedimiento del cuadro de diálogo devuelve **TRUE**, el sistema establece automáticamente el foco de entrada en el control cuyo identificador de ventana está en el *parámetro wParam.* Si el control que recibe el foco predeterminado no es adecuado, puede establecer el foco en el control adecuado mediante la [**función SetFocus.**](/windows/desktop/api/winuser/nf-winuser-setfocus) Si el procedimiento establece el foco de entrada, debe devolver **FALSE** para evitar que el sistema estableciendo el foco predeterminado. El control que recibe el foco de entrada predeterminado siempre es el primer control especificado en la plantilla que está visible, no deshabilitado y tiene el estilo [ \_ TABSTOP de WS.](/windows/desktop/winmsg/window-styles) Si no existe este control, el sistema establece el foco de entrada predeterminado en el primer control de la plantilla.

### <a name="the-wm_command-message"></a>El mensaje \_ WM COMMAND

Un control puede enviar un [**mensaje \_ WM COMMAND**](/windows/desktop/menurc/wm-command) al procedimiento del cuadro de diálogo cuando el usuario lleva a cabo una acción en el control . Estos mensajes, denominados mensajes de notificación, informan del procedimiento de entrada del usuario y le permiten llevar a cabo las respuestas adecuadas.

Todos los controles predefinidos, excepto los controles estáticos, envían mensajes de notificación para las acciones de usuario seleccionadas. Por ejemplo, un botón de inserción envía el [**mensaje de notificación \_ CLICKED**](../controls/bn-clicked.md) de BN cada vez que el usuario hace clic en él. En todos los casos, la palabra de orden bajo del parámetro *wParam* contiene el identificador de control, la palabra de orden superior *de wParam* contiene el código de notificación y el parámetro *lParam* contiene el identificador de la ventana de control.

El procedimiento del cuadro de diálogo debe supervisar y procesar los mensajes de notificación. En concreto, el procedimiento debe procesar los mensajes que tengan los identificadores IDOK o IDCANCEL; estos mensajes representan una solicitud del usuario para cerrar el cuadro de diálogo. El procedimiento debe cerrar el cuadro de diálogo mediante la función [**EndDialog**](/windows/desktop/api/Winuser/nf-winuser-enddialog) para los cuadros de diálogo modales y la [**función DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) para los cuadros de diálogo modeless.

El sistema también envía mensajes [**WM \_ COMMAND**](/windows/desktop/menurc/wm-command) al procedimiento del cuadro de  diálogo si el cuadro de diálogo tiene un menú, como el menú de la ventana, y el usuario hace clic en un elemento de menú. En concreto, el sistema envía un mensaje **WM \_ COMMAND** con el parámetro *wParam* establecido en **IDCANCEL** cada vez que el usuario hace clic en Cerrar en el menú de la ventana del cuadro de diálogo.  El mensaje es casi idéntico al mensaje de notificación enviado por el botón **Cancelar** y debe procesarse exactamente de la misma manera.

### <a name="the-wm_parentnotify-message"></a>Mensaje \_ PARENTNOTIFY de WM

Un control envía un mensaje [**\_ PARENTNOTIFY de WM**](/previous-versions/windows/desktop/inputmsg/wm-parentnotify) cada vez que el usuario presiona un botón del mouse mientras apunta al control. Algunas aplicaciones interpretan este mensaje como una señal para llevar a cabo una acción relacionada con el control, como mostrar una línea de texto que describa el propósito del control.

El sistema también envía [**mensajes \_ PARENTNOTIFY de WM**](/previous-versions/windows/desktop/inputmsg/wm-parentnotify) cuando crea y destruye una ventana, pero no para los controles creados a partir de una plantilla de cuadro de diálogo. El sistema evita estos mensajes especificando el estilo **WS \_ EX \_ NOPARENTNOTIFY** al crear los controles. Una aplicación no puede invalidar este comportamiento predeterminado a menos que cree sus propios controles para el cuadro de diálogo.

### <a name="control-color-messages"></a>Control-Color mensajes

Los controles y el sistema pueden enviar mensajes de color de control cuando desean que el procedimiento del cuadro de diálogo pinte el fondo de un control u otra ventana mediante un pincel y colores específicos. Esto puede ser útil cuando las aplicaciones invalidan los colores predeterminados usados en los cuadros de diálogo y sus controles. A continuación se encuentran los mensajes de color de control, que han reemplazado al **\_ mensaje WM CTLCOLOR.**

-   [**WM \_ CTLCOLORBTN**](../controls/wm-ctlcolorbtn.md)
-   [**WM \_ CTLCOLORDLG**](wm-ctlcolordlg.md)
-   [**WM \_ CTLCOLOREDIT**](../controls/wm-ctlcoloredit.md)
-   [**WM \_ CTLCOLORLISTBOX**](../controls/wm-ctlcolorlistbox.md)
-   [**WM \_ CTLCOLORSCROLLBAR**](../controls/wm-ctlcolorscrollbar.md)
-   [**WM \_ CTLCOLORSTATIC**](../controls/wm-ctlcolorstatic.md)

Un control envía un mensaje de color de control al procedimiento del cuadro de diálogo justo antes de pintar su propio fondo. El mensaje permite al procedimiento especificar qué pincel usar y establecer los colores de fondo y primer plano. El procedimiento especifica un pincel devolviendo el controlador de pincel. Para establecer los colores de fondo y primer plano, el procedimiento usa las funciones [**SetBkColor**](/windows/desktop/api/wingdi/nf-wingdi-setbkcolor) y [**SetTextColor**](/windows/desktop/api/wingdi/nf-wingdi-settextcolor) con el contexto del dispositivo para mostrar del control. El mensaje de color de control pasa un identificador al contexto del dispositivo para mostrar al procedimiento del parámetro *wParam del* mensaje.

El sistema envía un [**mensaje \_ WM CTLCOLORDLG**](wm-ctlcolordlg.md) al procedimiento del cuadro de diálogo si el procedimiento no procesa el [**mensaje \_ ERASEB DOMAINND de WM.**](/windows/desktop/winmsg/wm-erasebkgnd) La clase de cuadro de diálogo predefinida no tiene un pincel de fondo de clase, por lo que este mensaje permite al procedimiento definir su propio fondo sin tener que incluir el código para llevar a cabo el trabajo.

En cualquier caso, cuando un procedimiento de cuadro de diálogo no procesa un mensaje de color de control, el sistema usa un pincel con el color de ventana predeterminado para pintar el fondo de todos los controles y ventanas, excepto las barras de desplazamiento. Una aplicación puede recuperar el color de ventana predeterminado pasando el **valor DE COLOR \_ WINDOW** a la [**función GetSysColor.**](/windows/desktop/api/winuser/nf-winuser-getsyscolor) Mientras se pinta el fondo, el color de primer plano del contexto del dispositivo para mostrar se establece en el color de texto predeterminado (**COLOR \_ WINDOWTEXT**). Para las barras de desplazamiento, el sistema usa un pincel que tiene el color predeterminado de la barra de desplazamiento **(COLOR \_ SCROLLBAR**). En este caso, los colores de fondo y primer plano del contexto del dispositivo de presentación se establecen en blanco y negro, respectivamente.

### <a name="dialog-box-default-message-processing"></a>Procesamiento de mensajes predeterminado del cuadro de diálogo

El procedimiento de ventana para la clase de cuadro de diálogo predefinida lleva a cabo el procesamiento predeterminado para todos los mensajes que el procedimiento del cuadro de diálogo no procesa. Cuando el procedimiento del cuadro de diálogo **devuelve FALSE** para cualquier mensaje, el procedimiento de ventana predefinido comprueba los mensajes y lleva a cabo las siguientes acciones predeterminadas:



| Message                                            | Acción predeterminada                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DM \_ GETDEFID**](dm-getdefid.md)                | Puede enviar este mensaje a un cuadro de diálogo. El cuadro de diálogo devuelve el identificador de control del botón de inserción predeterminado, si el cuadro de diálogo tiene uno; de lo contrario, devuelve cero.                                                                                                                                                                                                                                                                                                                      |
| [**REPOSICIÓN \_ DE DM**](dm-reposition.md)            | Puede enviar este mensaje a un cuadro de diálogo de nivel superior. El cuadro de diálogo se vuelve a colocar para que se ajuste al área de escritorio.                                                                                                                                                                                                                                                                                                                                                                       |
| [**DM \_ SETDEFID**](dm-setdefid.md)                | Puede enviar este mensaje a un cuadro de diálogo. El cuadro de diálogo establece el botón de inserción predeterminado en el control especificado por el identificador de control en el *parámetro wParam.*                                                                                                                                                                                                                                                                                                                             |
| [**WM \_ ACTIVATE**](/windows/desktop/inputdev/wm-activate)           | Restaura el foco de entrada al control identificado por el identificador guardado previamente si el cuadro de diálogo está activado. De lo contrario, el procedimiento guarda el identificador en el control que tiene el foco de entrada.                                                                                                                                                                                                                                                                                               |
| [**WM \_ CHARTOITEM**](../controls/wm-chartoitem.md)         | Devuelve cero.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [**WM \_ CLOSE**](/windows/desktop/winmsg/wm-close)                   | Envía el [**mensaje de notificación \_ CLICKED**](../controls/bn-clicked.md) de BN al cuadro de diálogo, **especificando IDCANCEL** como identificador de control. Si el cuadro de diálogo tiene un identificador de control IDCANCEL y el control está deshabilitado actualmente, el procedimiento suena una advertencia y no publica el mensaje.                                                                                                                                                                                              |
| [**COMPAREITEM de WM \_**](../controls/wm-compareitem.md)       | Devuelve cero.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [**WM \_ ERASEBND**](/windows/desktop/winmsg/wm-erasebkgnd)         | Rellena el área de cliente del cuadro de diálogo utilizando el pincel devuelto desde el mensaje [**\_ WM CTLCOLORDLG**](wm-ctlcolordlg.md) o con el color de ventana predeterminado.                                                                                                                                                                                                                                                                                                                                 |
| [**WM \_ GETFONT**](/windows/desktop/winmsg/wm-getfont)               | Devuelve un identificador a la fuente del cuadro de diálogo definido por la aplicación.                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [**WM \_ INITDIALOG**](wm-initdialog.md)            | Devuelve cero.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown)     | Envía un [**mensaje \_ CB SHOWDROPDOWN**](../controls/cb-showdropdown.md) al cuadro combinado que tiene el foco de entrada, lo que indica al control que oculte su cuadro de lista desplegable. El procedimiento llama [**a DefWindowProc para**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) completar la acción predeterminada.                                                                                                                                                                                                                                      |
| [**WM \_ NCDESTROY**](/windows/desktop/winmsg/wm-ncdestroy)           | Libera la memoria global asignada para los controles de edición en el cuadro de diálogo (se aplica a los cuadros de diálogo que especifican el estilo [**\_ LOCALEDIT de DS)**](dialog-box-styles.md) y libera cualquier fuente definida por la aplicación (se aplica a los cuadros de diálogo que especifican el estilo [**DS \_ SETFONT**](dialog-box-styles.md) o [**DS \_ SHELLFONT).**](dialog-box-styles.md) El procedimiento llama a la [**función DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) para completar la acción predeterminada. |
| [**WM \_ NCLBUTTONDOWN**](/windows/desktop/inputdev/wm-nclbuttondown) | Envía un [**mensaje \_ CB SHOWDROPDOWN**](../controls/cb-showdropdown.md) al cuadro combinado que tiene el foco de entrada, lo que indica al control que oculte su cuadro de lista desplegable. El procedimiento llama [**a DefWindowProc para**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) completar la acción predeterminada.                                                                                                                                                                                                                                      |
| [**WM \_ NEXTDLGCTL**](wm-nextdlgctl.md)            | Establece el foco de entrada en el control siguiente o anterior del cuadro de diálogo, en el control identificado por el identificador en el parámetro *wParam* o en el primer control del cuadro de diálogo que está visible, no deshabilitado, y tiene el estilo [**\_ TABSTOP de WS.**](/windows/desktop/winmsg/window-styles) El procedimiento omite este mensaje si la ventana actual con el foco de entrada no es un control.                                                                                                                  |
| [**WM \_ SETFOCUS**](/windows/desktop/inputdev/wm-setfocus)           | Establece el foco de entrada en el control identificado por un identificador de ventana de control guardado previamente. Si no existe ningún identificador de este tipo, el procedimiento establece el foco de entrada en el primer control de la plantilla de cuadro de diálogo que está visible, no deshabilitado, y tiene el estilo [**\_ TABSTOP de WS.**](/windows/desktop/winmsg/window-styles) Si no existe este control, el procedimiento establece el foco de entrada en el primer control de la plantilla.                                                                                          |
| [**WM \_ SHOWWINDOW**](/windows/desktop/winmsg/wm-showwindow)         | Guarda un identificador en el control que tiene el foco de entrada si se oculta el cuadro de diálogo y, a continuación, llama a [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) para completar la acción predeterminada.                                                                                                                                                                                                                                                                                                                     |
| [**WM \_ SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand)         | Guarda un identificador en el control que tiene el foco de entrada si se minimiza el cuadro de diálogo y, a continuación, llama a [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) para completar la acción predeterminada.                                                                                                                                                                                                                                                                                                                  |
| [**WM \_ VKEYTOITEM**](../controls/wm-vkeytoitem.md)         | Devuelve cero.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |

El procedimiento de ventana predefinido pasa todos los demás mensajes [**a DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) para su procesamiento predeterminado.

## <a name="dialog-box-keyboard-interface"></a>Interfaz de teclado del cuadro de diálogo

El sistema proporciona una interfaz de teclado especial para los cuadros de diálogo que lleva a cabo un procesamiento especial para varias teclas. La interfaz genera mensajes que corresponden a determinados botones del cuadro de diálogo o cambia el foco de entrada de un control a otro. A continuación se encuentran las claves usadas en esta interfaz y sus respectivas acciones.


| Clave            | Acción                                                                                                                                                                    |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ALT+*mnemotécnica* | Mueve el foco de entrada al primer control (con el estilo [**\_ TABSTOP de WS)**](/windows/desktop/winmsg/window-styles) después del control estático que contiene el mnemónico especificado.        |
| ABAJO           | Mueve el foco de entrada al siguiente control del grupo.                                                                                                                   |
| ENTRAR          | Envía un [**mensaje WM \_ COMMAND**](/windows/desktop/menurc/wm-command) al procedimiento del cuadro de diálogo. El *parámetro wParam* se establece en IDOK o identificador de control del botón de inserción predeterminado. |
| ESC            | Envía un [**mensaje WM \_ COMMAND**](/windows/desktop/menurc/wm-command) al procedimiento del cuadro de diálogo. El *parámetro wParam* se establece en IDCANCEL.                                              |
| LEFT           | Mueve el foco de entrada al control anterior del grupo.                                                                                                               |
| *Mnemónica*     | Mueve el foco de entrada al primer control (con el estilo [**\_ TABSTOP de WS)**](/windows/desktop/winmsg/window-styles) después del control estático que contiene el mnemónico especificado.        |
| RIGHT          | Mueve el foco de entrada al siguiente control del grupo.                                                                                                                   |
| MAYÚS+TAB      | Mueve el foco de entrada al control anterior que tiene el [**estilo \_ TABSTOP de WS.**](/windows/desktop/winmsg/window-styles)                                                                |
| TAB            | Mueve el foco de entrada al siguiente control que tiene el [**estilo \_ TABSTOP de WS.**](/windows/desktop/winmsg/window-styles)                                                                    |
| UP             | Mueve el foco de entrada al control anterior del grupo.                                                                                                               |

El sistema proporciona automáticamente la interfaz de teclado para todos los cuadros de diálogo modales. No proporciona la interfaz para los cuadros de diálogo de modeless a menos que la aplicación llame a la función [**IsDialogMessage**](/windows/desktop/api/Winuser/nf-winuser-isdialogmessagea) para filtrar los mensajes en su bucle de mensajes principal. Esto significa que la aplicación debe pasar el mensaje a **IsDialogMessage** inmediatamente después de recuperar el mensaje de la cola de mensajes. La función procesa los mensajes si es para el cuadro de diálogo y devuelve un valor distinto de cero para indicar que el mensaje se ha procesado y no se debe pasar a la función [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) o [**DispatchMessage.**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage)

Dado que la interfaz de teclado del cuadro de diálogo usa teclas de dirección para moverse entre los controles de un cuadro de diálogo, una aplicación no puede usar estas teclas para desplazarse por el contenido de ningún cuadro de diálogo modal ni de ningún cuadro de diálogo no modal para el que se llame a [**IsDialogMessage.**](/windows/desktop/api/Winuser/nf-winuser-isdialogmessagea) Cuando un cuadro de diálogo tiene barras de desplazamiento, la aplicación debe proporcionar una interfaz de teclado alternativa para las barras de desplazamiento. Tenga en cuenta que la interfaz del mouse para desplazarse está disponible cuando el sistema incluye un mouse.

### <a name="the-ws_tabstop-style"></a>El estilo \_ TABSTOP de WS

El [**estilo \_ TABSTOP**](/windows/desktop/winmsg/window-styles) de WS especifica los controles a los que el usuario puede moverse presionando la tecla TAB o las teclas MAYÚS+TAB.

Cuando el usuario presiona TAB o MAYÚS+TAB, el sistema determina primero si el control que tiene actualmente el foco de entrada procesa estas teclas. Envía al control un mensaje [**\_ GETDLGCODE**](wm-getdlgcode.md) de WM y, si el control devuelve DLGC WANTTAB, el sistema pasa las \_ claves al control. De lo contrario, el sistema usa la función [**GetNextDlgTabItem**](/windows/desktop/api/Winuser/nf-winuser-getnextdlgtabitem) para buscar el siguiente control que está visible, no deshabilitado, y que tiene el estilo [**\_ TABSTOP de WS.**](/windows/desktop/winmsg/window-styles) La búsqueda comienza con el control que tiene actualmente el foco de entrada y continúa en el orden en que se crearon los controles, es decir, el orden en que se definen en la plantilla de cuadro de diálogo. Cuando el sistema localiza un control que tiene las características necesarias, el sistema le mueve el foco de entrada.

Si la búsqueda del siguiente control con el estilo [**\_ TABSTOP**](/windows/desktop/winmsg/window-styles) de WS encuentra una ventana con el estilo **WS \_ EX \_ CONTROLPARENT,** el sistema busca de forma recursiva en los secundarios de la ventana.

Una aplicación también puede usar [**GetNextDlgTabItem para**](/windows/desktop/api/Winuser/nf-winuser-getnextdlgtabitem) buscar controles que tengan el estilo [**\_ TABSTOP de WS.**](/windows/desktop/winmsg/window-styles) La función recupera el identificador de ventana del control siguiente o anterior que tiene el estilo **\_ TABSTOP** de WS sin mover el foco de entrada.

### <a name="the-ws_group-style"></a>Estilo de WS \_ GROUP

De forma predeterminada, el sistema mueve el foco de entrada al control siguiente o anterior cada vez que el usuario presiona una tecla de dirección. Siempre que el control actual con el foco de entrada no procese estas teclas y el control siguiente o anterior no sea un control estático, el sistema sigue desplazando el foco de entrada a través de todos los controles del cuadro de diálogo a medida que el usuario sigue pulsando las teclas de dirección.

Una aplicación puede usar el [**estilo WS \_ GROUP**](/windows/desktop/winmsg/window-styles) para modificar este comportamiento predeterminado. El estilo marca el principio de un grupo de controles. Si un control del grupo tiene el foco de entrada cuando el usuario comienza a presionar las teclas de dirección, el foco permanece en el grupo. En general, el primer control de un grupo debe tener el estilo **WS \_ GROUP** y todos los demás controles del grupo no deben tener este estilo. Todos los controles del grupo deben ser contiguos, es decir, se deben haber creado consecutivamente sin ningún control que intervena.

Cuando el usuario presiona una tecla de dirección, el sistema determina primero si el control actual que tiene el foco de entrada procesa las teclas de dirección. El sistema envía un [**mensaje \_ GETDLGCODE**](wm-getdlgcode.md) de WM al control y, si el control devuelve el valor **DE \_ DLGC WANTARROWS,** pasa la clave al control. De lo contrario, el sistema usa [**la función GetNextDlgGroupItem**](/windows/desktop/api/Winuser/nf-winuser-getnextdlggroupitem) para determinar el siguiente control del grupo.

[**GetNextDlgGroupItem busca**](/windows/desktop/api/Winuser/nf-winuser-getnextdlggroupitem) controles en el orden (o orden inverso) que se crearon. Si el usuario presiona la tecla RIGHT o DOWN, **GetNextDlgGroupItem** devuelve el siguiente control si ese control no tiene el estilo [**WS \_ GROUP.**](/windows/desktop/winmsg/window-styles) De lo contrario, la función invierte el orden de la búsqueda y devuelve el primer control que tiene el **estilo DE GRUPO \_ de WS.** Si el usuario presiona la tecla LEFT o UP, la función devuelve el control anterior a menos que el control actual ya tenga el **estilo WS \_ GROUP.** Si el control actual tiene este estilo, la función invierte el orden de la búsqueda, busca el primer control que tiene el estilo **WS \_ GROUP** y devuelve el control que precede inmediatamente al control ubicado.

Si la búsqueda del siguiente control en el grupo encuentra una ventana con el estilo **WS \_ EX \_ CONTROLPARENT,** el sistema busca de forma recursiva en los secundarios de la ventana.

Una vez que el sistema tiene el control siguiente o anterior, envía un mensaje [**\_ GETDLGCODE**](wm-getdlgcode.md) de WM al control para determinar el tipo de control. A continuación, el sistema mueve el foco de entrada al control si no es un control estático. Si el control es un botón de radio automático, el sistema le envía un mensaje [**\_ BM CLICK.**](../controls/bm-click.md) Una aplicación también puede usar [**GetNextDlgGroupItem**](/windows/desktop/api/Winuser/nf-winuser-getnextdlggroupitem) para buscar controles en un grupo.

Por lo general, el primer control del grupo combina los estilos [**WS \_ GROUP**](/windows/desktop/winmsg/window-styles) y [**WS \_ TABSTOP**](/windows/desktop/winmsg/window-styles) para que el usuario pueda moverse de un grupo a otro mediante la tecla TAB. Si el grupo contiene botones de radio, la aplicación debe aplicar el estilo **\_ TABSTOP** de WS solo al primer control del grupo. El sistema mueve automáticamente el estilo cuando el usuario se mueve entre los controles del grupo. Esto garantiza que el foco de entrada siempre estará en el control seleccionado más recientemente cuando el usuario se mueva al grupo mediante la tecla TAB.

### <a name="mnemonics"></a>Mnemónicas

Una mnemotécnica es una letra o dígito seleccionados en la etiqueta de un botón o en el texto de un control estático. El sistema mueve el foco de entrada al control asociado con la tecla mnemotécnica cada vez que el usuario presiona la tecla que corresponde a la tecla mnemotécnica o presiona esta tecla y la tecla ALT en combinación. Los métodos mnemotécnicos proporcionan una manera rápida de que el usuario se mueva a un control especificado mediante el teclado.

Una aplicación crea una mnemotécnica para un control insertando la yandida (&) inmediatamente antes de la letra o dígito seleccionados en la etiqueta o el texto del control. En la mayoría de los casos, la cadena terminada en NULL proporcionada con el control en la plantilla de cuadro de diálogo contiene la yand. Sin embargo, una aplicación puede crear un elemento mnemónico en cualquier momento reemplazando la etiqueta o el texto existentes de un control mediante la [**función SetDlgItemText.**](/windows/desktop/api/Winuser/nf-winuser-setdlgitemtexta) Solo se puede especificar un elemento mnemotécnico para cada control. Aunque se recomienda, la característica mnemotécnica de un cuadro de diálogo no debe ser única.

Cuando el usuario presiona una tecla de letra o dígito, el sistema determina primero si el control actual que tiene el foco de entrada procesa la tecla. El sistema envía un mensaje [**\_ GETDLGCODE**](wm-getdlgcode.md) de WM al control y, si el control devuelve el valor **DE DLGC \_ WANTALLKEYS** o **DLG \_ WANTMESSAGE,** el sistema pasa la clave al control. De lo contrario, busca un control cuyo valor mnemotécnico coincida con la letra o el dígito especificados. Continúa buscando hasta que encuentra un control o ha examinado todos los controles. Durante la búsqueda, omite los controles estáticos que tienen el estilo [**\_ SS NOPREFIX.**](../controls/static-control-styles.md)

Si la búsqueda de un control con una función mnemotécnica correspondiente encuentra una ventana con el estilo **WS \_ EX \_ CONTROLPARENT,** el sistema busca de forma recursiva en los secundarios de la ventana.

Si el sistema encuentra un control estático y el control no está deshabilitado, el sistema mueve el foco de entrada al primer control después del control estático que está visible, no deshabilitado, y que tiene el estilo [**\_ TABSTOP de WS.**](/windows/desktop/winmsg/window-styles) Si el sistema encuentra algún otro control que tenga una mnemotécnica correspondiente, mueve el foco de entrada a ese control. Si el control es un botón de inserción predeterminado, el sistema envía un mensaje de notificación [**\_ CLICKED**](../controls/bn-clicked.md) de BN al procedimiento del cuadro de diálogo. Si el control es otro estilo de botón y no hay ningún otro control en el cuadro de diálogo que tenga el mismo mnemónico, el sistema envía el mensaje [**BM \_ CLICK**](../controls/bm-click.md) al control.

## <a name="dialog-box-settings"></a>Cuadro de diálogo Configuración

La configuración del cuadro de diálogo son las selecciones y valores actuales de los controles del cuadro de diálogo. El procedimiento del cuadro de diálogo es responsable de inicializar los controles a esta configuración al crear el cuadro de diálogo. También es responsable de recuperar la configuración actual de los controles antes de destruir el cuadro de diálogo. Los métodos usados para inicializar y recuperar la configuración dependen del tipo de control.

Para obtener más información, vea los temas siguientes:

-   [Botones de radio y casillas](#radio-buttons-and-check-boxes)
-   [Controles de edición de cuadro de diálogo](#dialog-box-edit-controls)
-   [Cuadros de lista, cuadros combinados y listas de directorios](#list-boxes-combo-boxes-and-directory-listings)
-   [Mensajes de control de cuadro de diálogo](#dialog-box-control-messages)

### <a name="radio-buttons-and-check-boxes"></a>Botones de radio y casillas

Los cuadros de diálogo usan botones de radio y casillas para permitir al usuario elegir entre una lista de opciones. Los botones de radio permiten al usuario elegir entre opciones mutuamente excluyentes; Las casillas permiten al usuario elegir una combinación de opciones.

El procedimiento del cuadro de diálogo puede establecer el estado inicial de una casilla mediante la [**función CheckDlgButton,**](https://msdn.microsoft.com/library/Cc410649(v=MSDN.10).aspx) que establece o borra la casilla. En el caso de los botones de radio de un grupo de botones de radio mutuamente excluyentes, el procedimiento del cuadro de diálogo puede usar la función [**CheckRadioButton**](https://msdn.microsoft.com/library/Cc410654(v=MSDN.10).aspx) para establecer el botón de radio adecuado y borrar automáticamente cualquier otro botón de radio.

Antes de que finalice un cuadro de diálogo, el procedimiento del cuadro de diálogo puede comprobar el estado de cada botón de radio y la casilla mediante la función [**IsDlgButtonChecked,**](https://msdn.microsoft.com/library/Cc364806(v=MSDN.10).aspx) que devuelve el estado actual del botón. Normalmente, un cuadro de diálogo guarda esta información para inicializar los botones la próxima vez que cree el cuadro de diálogo.

### <a name="dialog-box-edit-controls"></a>Controles de edición de cuadro de diálogo

Muchos cuadros de diálogo tienen controles de edición que permiten al usuario proporcionar texto como entrada. La mayoría de los procedimientos de cuadro de diálogo inicializan un control de edición cuando se inicia por primera vez el cuadro de diálogo. Por ejemplo, el procedimiento del cuadro de diálogo puede colocar un nombre de archivo propuesto en el control que el usuario puede seleccionar, modificar o reemplazar. El procedimiento del cuadro de diálogo puede establecer el texto en un control de edición mediante la función [**SetDlgItemText,**](/windows/desktop/api/Winuser/nf-winuser-setdlgitemtexta) que copia texto de un búfer especificado en el control de edición. Cuando el control de edición recibe el foco de entrada, selecciona automáticamente el texto completo para su edición.

Dado que los controles de edición no devuelven automáticamente su texto al cuadro de diálogo, el procedimiento del cuadro de diálogo debe recuperar el texto antes de que finalice. Puede recuperar el texto mediante la función [**GetDlgItemText,**](/windows/desktop/api/Winuser/nf-winuser-getdlgitemtexta) que copia el texto del control de edición en un búfer. El procedimiento del cuadro de diálogo normalmente guarda este texto para inicializar el control de edición más adelante o lo pasa a la ventana primaria para su procesamiento.

Algunos cuadros de diálogo usan controles de edición que permiten al usuario escribir números. El procedimiento del cuadro de diálogo puede recuperar un número de un control de edición mediante la función [**GetDlgItemInt,**](/windows/desktop/api/Winuser/nf-winuser-getdlgitemint) que recupera el texto del control de edición y convierte el texto en un valor decimal. El usuario tipos el número en dígitos decimales. Puede ser con signo o sin signo. El procedimiento del cuadro de diálogo puede mostrar un entero mediante la [**función SetDlgItemInt.**](/windows/desktop/api/Winuser/nf-winuser-setdlgitemint) **SetDlgItemInt** convierte un entero con signo o sin signo en una cadena de dígitos decimales.

### <a name="list-boxes-combo-boxes-and-directory-listings"></a>Cuadros de lista, cuadros combinados y listas de directorios

Algunos cuadros de diálogo muestran listas de nombres de los que el usuario puede seleccionar uno o varios nombres. Para mostrar una lista de nombres de archivo, por ejemplo, un cuadro de diálogo suele usar un cuadro de lista y las funciones [**DlgDirList**](https://msdn.microsoft.com/library/Cc410788(v=MSDN.10).aspx) y [**DlgDirSelectEx.**](https://msdn.microsoft.com/library/Cc410769(v=MSDN.10).aspx) La **función DlgDirList** rellena automáticamente un cuadro de lista con los nombres de archivo del directorio actual. La **función DlgDirSelect** recupera el nombre de archivo seleccionado del cuadro de lista. Juntas, estas dos funciones proporcionan una manera cómoda de que un cuadro de diálogo muestre una lista de directorios para que el usuario pueda seleccionar un archivo sin tener que escribir su nombre y ubicación.

Un cuadro de diálogo también puede usar un cuadro combinado para mostrar una lista de nombres de archivo. La [**función DlgDirListComboBox**](https://msdn.microsoft.com/library/Cc410798(v=MSDN.10).aspx) rellena automáticamente una parte del cuadro de lista del cuadro combinado con los nombres de archivo del directorio actual. La [**función DlgDirSelectComboBoxEx**](https://msdn.microsoft.com/library/Cc410768(v=MSDN.10).aspx) recupera un nombre de archivo seleccionado de la parte del cuadro de lista.

### <a name="dialog-box-control-messages"></a>Mensajes de control de cuadro de diálogo

Muchos controles reconocen mensajes predefinidos que, cuando los reciben los controles, hacen que realicen alguna acción. Por ejemplo, el mensaje [**\_ BM SETCHECK**](../controls/bm-setcheck.md) establece la casilla en una casilla y el mensaje [**EM \_ GETSEL**](../controls/em-getsel.md) recupera la parte del texto del control que está seleccionada actualmente. Los mensajes de control ofrecen a un procedimiento de diálogo un acceso mayor y flexible a los controles que las funciones estándar, por lo que a menudo se usan cuando el cuadro de diálogo requiere interacciones complejas con el usuario.

Un procedimiento de cuadro de diálogo puede enviar un mensaje a un control si se proporciona el identificador de control y se usa la función [**SendDlgItemMessage,**](/windows/desktop/api/Winuser/nf-winuser-senddlgitemmessagea) que es idéntica a la función [**SendMessage,**](/windows/desktop/api/winuser/nf-winuser-sendmessage) salvo que usa un identificador de control en lugar de un identificador de ventana para identificar el control que va a recibir el mensaje. Un mensaje especificado puede requerir que el procedimiento de diálogo envíe parámetros con el mensaje y que el mensaje tenga los valores devueltos correspondientes. La operación y los requisitos de cada mensaje de control dependen del propósito del mensaje y del control que lo procesa.

Para obtener más información sobre los mensajes de control, [vea Windows Controls](../controls/window-controls.md).

## <a name="custom-dialog-boxes"></a>Cuadros de diálogo personalizados

Una aplicación puede crear cuadros de diálogo personalizados mediante una clase de ventana definida por la aplicación para los cuadros de diálogo en lugar de usar la clase de cuadro de diálogo predefinida. Las aplicaciones suelen usar este método cuando un cuadro de diálogo es su ventana principal, pero también es útil para crear cuadros de diálogo modales y no modales para aplicaciones que tienen ventanas superpuestas estándar.

La clase de ventana definida por la aplicación permite a la aplicación definir un procedimiento de ventana para el cuadro de diálogo y procesar los mensajes antes de enviarlos al procedimiento del cuadro de diálogo. También permite a la aplicación definir un icono de clase, un pincel de fondo de clase y un menú de clases para el cuadro de diálogo. La aplicación debe registrar la clase de ventana antes de intentar crear un cuadro de diálogo y debe proporcionar a la plantilla de cuadro de diálogo el valor atom o el nombre de la clase de ventana.

Muchas aplicaciones crean una nueva clase de cuadro de diálogo recuperando primero la información de clase para la clase de cuadro de diálogo predefinida y pasándosela a la función [**GetClassInfo,**](/windows/desktop/api/winuser/nf-winuser-getclassinfoa) que rellena una estructura [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) con la información. La aplicación modifica los miembros individuales de la estructura, como el nombre de clase, el pincel y el icono, y luego registra la nueva clase mediante la [**función RegisterClass.**](/windows/desktop/api/winuser/nf-winuser-registerclassa) Si una aplicación rellena la estructura **WNDCLASS** por sí misma, debe establecer el miembro **cbWndExtra** en **DLGWINDOWEXTRA,** que es el número de bytes adicionales que requiere el sistema para cada cuadro de diálogo. Si una aplicación también usa bytes adicionales para cada cuadro de diálogo, deben superar los bytes adicionales requeridos por el sistema.

El procedimiento de ventana para el cuadro de diálogo personalizado tiene los mismos parámetros y requisitos que cualquier otro procedimiento de ventana. Sin embargo, a diferencia de otros procedimientos de ventana, el procedimiento de ventana de este cuadro de diálogo debe llamar a la función [**DefDlgProc**](/windows/desktop/api/Winuser/nf-winuser-defdlgprocw) en lugar de a la función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) para los mensajes que no procese. **DefDlgProc lleva** a cabo el mismo procesamiento de mensajes predeterminado que el procedimiento de ventana para el cuadro de diálogo predefinido, que incluye llamar al procedimiento del cuadro de diálogo.

Una aplicación también puede crear cuadros de diálogo personalizados mediante la creación de subclases del procedimiento de ventana del cuadro de diálogo predefinido. La [**función SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) permite a una aplicación especificar el procedimiento de ventana para una ventana especificada. La aplicación también puede intentar crear subclases mediante la función [**SetClassLong,**](/windows/desktop/api/winuser/nf-winuser-setclasslonga) pero esto afecta a todos los cuadros de diálogo del sistema, no solo a los que pertenecen a la aplicación.

Las aplicaciones que crean cuadros de diálogo personalizados a veces proporcionan una interfaz de teclado alternativa para los cuadros de diálogo. En el caso de los cuadros de diálogo no modelo, esto puede significar que la aplicación no llama a la función [**IsDialogMessage**](/windows/desktop/api/Winuser/nf-winuser-isdialogmessagea) y, en su lugar, procesa toda la entrada de teclado en el procedimiento de ventana personalizado. En tales casos, la aplicación puede usar el mensaje [**\_ WM NEXTDLGCTL**](wm-nextdlgctl.md) para minimizar el código necesario para mover el foco de entrada de un control a otro. Este mensaje, cuando se pasa a [**DefDlgProc,**](/windows/desktop/api/Winuser/nf-winuser-defdlgprocw)mueve el foco de entrada a un control especificado y actualiza la apariencia de los controles, como mover el borde del botón de inserción predeterminado o establecer un botón de radio automático.
