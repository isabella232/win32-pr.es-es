---
title: Consideraciones sobre la programación de cuadros de diálogo
description: En esta información general se describen algunas consideraciones de programación relativas a los cuadros de diálogo.
ms.assetid: 49024a0f-ea92-4d56-b063-8e5fcdbd884a
keywords:
- Interfaz de usuario de Windows, ventanas
- Interfaz de usuario de Windows, cuadros de diálogo
- ventanas, cuadros de diálogo
- cuadros de diálogo, acerca de
- procedimientos del cuadro de diálogo
- cuadros de diálogo, procedimientos
- Mensaje WM_INITDIALOG
- Mensaje WM_COMMAND
- Mensaje WM_PARENTNOTIFY
- mensajes de color de control
- cuadros de diálogo, procesamiento de mensajes
- cuadros de diálogo, interfaz de teclado
- cuadros de diálogo, teclas de tecla
- cuadros de diálogo, personalizados
- cuadros de diálogo personalizados
- cuadros de diálogo, configuración
ms.topic: article
ms.date: 08/25/2020
ms.openlocfilehash: 790abe7c76cdb99f86b2a90a133b15faae721e0e
ms.sourcegitcommit: f7cf41ffc79d1ffead9de2fc61677201f94b423a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2020
ms.locfileid: "105695772"
---
# <a name="dialog-box-programming-considerations"></a>Consideraciones sobre la programación de cuadros de diálogo

En esta información general se describen algunas consideraciones de programación relativas a los cuadros de diálogo.

La información general incluye los temas siguientes.

-   [Procedimientos del cuadro de diálogo](#dialog-box-procedures)
    -   [El mensaje de INITDIALOG de WM \_](wm-initdialog.md)
    -   [Mensaje del \_ comando de WM](/windows/desktop/menurc/wm-command)
    -   [El mensaje de PARENTNOTIFY de WM \_](/previous-versions/windows/desktop/inputmsg/wm-parentnotify)
    -   [Mensajes de color de control](#control-color-messages)
    -   [Procesamiento de mensajes predeterminado del cuadro de diálogo](#dialog-box-default-message-processing)
-   [Interfaz de teclado de cuadro de diálogo](#dialog-box-keyboard-interface)
    -   [Estilo de WS \_ TABSTOP](/windows/desktop/winmsg/window-styles)
    -   [Estilo de \_ grupo de WS](/windows/desktop/winmsg/window-styles)
    -   [Teclas](#mnemonics)
-   [Configuración del cuadro de diálogo](#dialog-box-settings)
    -   [Botones de radio y casillas](#radio-buttons-and-check-boxes)
    -   [Controles de edición del cuadro de diálogo](#dialog-box-edit-controls)
    -   [Cuadros de lista, cuadros combinados y listas de directorios](#list-boxes-combo-boxes-and-directory-listings)
    -   [Mensajes de control de cuadro de diálogo](#dialog-box-control-messages)
-   [Cuadros de diálogo personalizados](#custom-dialog-boxes)

## <a name="dialog-box-procedures"></a>Procedimientos del cuadro de diálogo

Un procedimiento de cuadro de diálogo es similar a un procedimiento de ventana en el que el sistema envía mensajes al procedimiento cuando contiene información que se debe dar a las tareas de o. A diferencia de un procedimiento de ventana, un procedimiento de cuadro de diálogo nunca llama a la función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) . En su lugar, devuelve **true** si procesa un mensaje o **false** si no lo hace.

Cada procedimiento del cuadro de diálogo tiene el formato siguiente:

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

Los parámetros de procedimiento tienen el mismo propósito que en un procedimiento de ventana, con el parámetro *hwndDlg* que recibe el identificador de ventana del cuadro de diálogo.

La mayoría de los procedimientos de cuadro de diálogo procesan el mensaje de [**WM \_ INITDIALOG**](wm-initdialog.md) y los mensajes de [**\_ comandos de WM**](/windows/desktop/menurc/wm-command) enviados por los controles, pero procesan algunos si se trata de otros mensajes. Si un procedimiento de cuadro de diálogo no procesa un mensaje, debe devolver **false** para indicar al sistema que procese los mensajes internamente. La única excepción a esta regla es el mensaje de **\_ INITDIALOG de WM** . El procedimiento del cuadro de diálogo debe devolver **true** para indicar al sistema que procese aún más el mensaje de **\_ INITDIALOG de WM** . En cualquier caso, el procedimiento no debe llamar a [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).

- [El mensaje de INITDIALOG de WM \_](#the-wm_initdialog-message)
- [Mensaje del \_ comando de WM](#the-wm_command-message)
- [El mensaje de PARENTNOTIFY de WM \_](#the-wm_parentnotify-message)
- [Mensajes de color de control](#control-color-messages)
- [Procesamiento de mensajes predeterminado del cuadro de diálogo](#dialog-box-default-message-processing)

### <a name="the-wm_initdialog-message"></a>El mensaje de INITDIALOG de WM \_

El sistema no envía un mensaje [**de \_ creación de WM**](/windows/desktop/winmsg/wm-create) al procedimiento del cuadro de diálogo. En su lugar, envía un mensaje de [**\_ INITDIALOG de WM**](wm-initdialog.md) cuando crea el cuadro de diálogo y todos sus controles, pero antes de que se muestre el cuadro de diálogo. El procedimiento debe llevar a cabo cualquier inicialización necesaria para asegurarse de que el cuadro de diálogo muestra la configuración actual asociada a la tarea. Por ejemplo, cuando un cuadro de diálogo contiene un control para mostrar la unidad y el directorio actuales, el procedimiento debe determinar la unidad y el directorio actuales y establecer el control en ese valor.

El procedimiento puede inicializar los controles mediante funciones como [**SetDlgItemText**](/windows/desktop/api/Winuser/nf-winuser-setdlgitemtexta) y [**CheckDlgButton**](https://msdn.microsoft.com/library/Cc410649(v=MSDN.10).aspx). Dado que los controles son Windows, el procedimiento también puede manipularlos mediante funciones de administración de ventanas como [**EnableWindow**](/windows/desktop/api/winuser/nf-winuser-enablewindow) y [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus). El procedimiento puede recuperar el identificador de ventana de un control mediante la función [**GetDlgItem**](/windows/desktop/api/Winuser/nf-winuser-getdlgitem) .

El procedimiento de cuadro de diálogo puede cambiar el contenido, el estado y la posición de cualquier control según sea necesario. Por ejemplo, en un cuadro de diálogo que contiene un cuadro de lista de nombres de archivo y un botón **abrir** , el procedimiento puede deshabilitar el botón **abrir** hasta que el usuario seleccione un archivo de la lista. En este ejemplo, la plantilla de cuadro de diálogo especifica el estilo de [**WS \_ deshabilitado**](/windows/desktop/winmsg/window-styles) para el botón **abrir** y el sistema deshabilita automáticamente el botón al crearlo. Cuando el procedimiento del cuadro de diálogo recibe un mensaje de notificación del cuadro de lista que indica que el usuario ha seleccionado un archivo, el procedimiento llama a la función [**EnableWindow**](/windows/desktop/api/winuser/nf-winuser-enablewindow) para habilitar el botón **abrir** .

Para mostrar un icono personalizado en la barra de título del cuadro de diálogo, el controlador de [**\_ INITDIALOG de WM**](wm-initdialog.md) puede enviar el mensaje de [**WM \_ SETICON**](/windows/desktop/winmsg/wm-seticon) al cuadro de diálogo.

Si la aplicación crea el cuadro de diálogo mediante una de las funciones [**DialogBoxParam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxparama), [**DialogBoxIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirectparama), [**CreateDialogParam**](/windows/desktop/api/Winuser/nf-winuser-createdialogparama)o [**CreateDialogIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirectparama), el parámetro *lParam* del mensaje de [**WM \_ INITDIALOG**](wm-initdialog.md) contiene el parámetro adicional que se pasa a la función. Normalmente, las aplicaciones usan este parámetro adicional para pasar un puntero a información adicional de inicialización al procedimiento del cuadro de diálogo, pero el procedimiento del cuadro de diálogo debe determinar el significado del parámetro. Si la aplicación usa otra función para crear el cuadro de diálogo, el sistema establece el parámetro *lParam* en **null**.

Antes de volver del mensaje de [**\_ INITDIALOG de WM**](wm-initdialog.md) , el procedimiento debe determinar si debe establecer el foco de entrada en un control especificado. Si el procedimiento del cuadro de diálogo devuelve **true**, el sistema establece automáticamente el foco de entrada en el control cuyo identificador de ventana está en el parámetro *wParam* . Si el control que recibe el foco predeterminado no es adecuado, puede establecer el foco en el control adecuado mediante la función [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus) . Si el procedimiento establece el foco de entrada, debe devolver **false** para evitar que el sistema establezca el foco predeterminado. El control que recibe el foco de entrada predeterminado siempre es el primer control especificado en la plantilla que es visible, no deshabilitado y tiene el estilo [WS \_ TABSTOP](/windows/desktop/winmsg/window-styles) . Si no existe tal control, el sistema establece el foco de entrada predeterminado en el primer control de la plantilla.

### <a name="the-wm_command-message"></a>Mensaje del \_ comando de WM

Un control puede enviar un mensaje de [**\_ comando de WM**](/windows/desktop/menurc/wm-command) al procedimiento del cuadro de diálogo cuando el usuario lleva a cabo una acción en el control. Estos mensajes, denominados mensajes de notificación, informan al procedimiento de datos proporcionados por el usuario y permiten que se lleven a cabo las respuestas adecuadas.

Todos los controles predefinidos, excepto los controles estáticos, envían mensajes de notificación para las acciones del usuario seleccionadas. Por ejemplo, un botón de reenvío envía el mensaje de notificación en el que se [**\_ hace clic en el BN**](../controls/bn-clicked.md) cada vez que el usuario hace clic en el botón. En todos los casos, la palabra de orden inferior del parámetro *wParam* contiene el identificador de control, la palabra de orden superior de *wParam* contiene el código de notificación y el parámetro *lParam* contiene el identificador de la ventana de control.

El procedimiento de cuadro de diálogo debe supervisar y procesar los mensajes de notificación. En concreto, el procedimiento debe procesar los mensajes que tienen los identificadores IDOK o IDCANCEL; Estos mensajes representan una solicitud del usuario para cerrar el cuadro de diálogo. El procedimiento debe cerrar el cuadro de diálogo mediante la función [**EndDialog**](/windows/desktop/api/Winuser/nf-winuser-enddialog) para los cuadros de diálogo modales y la función [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) para los cuadros de diálogo no modales.

El sistema también envía mensajes de [**\_ comandos de WM**](/windows/desktop/menurc/wm-command) al procedimiento del cuadro de diálogo si el cuadro de diálogo tiene un menú, como el menú **ventana** , y el usuario hace clic en un elemento de menú. En concreto, el sistema envía un mensaje de **\_ comando de WM** con el parámetro *wParam* establecido en **IDCANCEL** siempre que el usuario haga clic en **cerrar** en el menú ventana del cuadro de diálogo. El mensaje es casi idéntico al mensaje de notificación enviado por el botón **Cancelar** y debe procesarse exactamente de la misma manera.

### <a name="the-wm_parentnotify-message"></a>El mensaje de PARENTNOTIFY de WM \_

Un control envía un mensaje de [**WM \_ PARENTNOTIFY**](/previous-versions/windows/desktop/inputmsg/wm-parentnotify) cada vez que el usuario presiona un botón del mouse mientras señala el control. Algunas aplicaciones interpretan este mensaje como una señal para llevar a cabo una acción relacionada con el control, como mostrar una línea de texto que describe el propósito del control.

El sistema también envía mensajes de [**WM \_ PARENTNOTIFY**](/previous-versions/windows/desktop/inputmsg/wm-parentnotify) cuando crea y destruye una ventana, pero no para los controles creados a partir de una plantilla de cuadro de diálogo. El sistema impide estos mensajes mediante la especificación del estilo **WS \_ ex \_ NOPARENTNOTIFY** al crear los controles. Una aplicación no puede invalidar este comportamiento predeterminado a menos que cree sus propios controles para el cuadro de diálogo.

### <a name="control-color-messages"></a>Mensajes de Control-Color

Los controles y el sistema pueden enviar mensajes de color de control cuando deseen que el procedimiento del cuadro de diálogo pinte el fondo de un control u otra ventana utilizando un pincel y colores específicos. Esto puede ser útil cuando las aplicaciones invalidan los colores predeterminados usados en los cuadros de diálogo y sus controles. A continuación se muestran los mensajes de color de control, que han reemplazado el mensaje de **\_ CTLCOLOR de WM** .

-   [**CTLCOLORBTN de WM \_**](../controls/wm-ctlcolorbtn.md)
-   [**CTLCOLORDLG de WM \_**](wm-ctlcolordlg.md)
-   [**CTLCOLOREDIT de WM \_**](../controls/wm-ctlcoloredit.md)
-   [**CTLCOLORLISTBOX de WM \_**](../controls/wm-ctlcolorlistbox.md)
-   [**CTLCOLORSCROLLBAR de WM \_**](../controls/wm-ctlcolorscrollbar.md)
-   [**CTLCOLORSTATIC de WM \_**](../controls/wm-ctlcolorstatic.md)

Un control envía un mensaje de color de control al procedimiento del cuadro de diálogo justo antes de que dibuje su propio fondo. El mensaje permite al procedimiento especificar qué pincel usar y establecer los colores de fondo y de primer plano. El procedimiento especifica un pincel devolviendo el identificador del pincel. Para establecer los colores de fondo y de primer plano, el procedimiento usa las funciones [**SetBkColor**](/windows/desktop/api/wingdi/nf-wingdi-setbkcolor) y [**SetTextColor**](/windows/desktop/api/wingdi/nf-wingdi-settextcolor) con el contexto de dispositivo de pantalla del control. El mensaje de color de control pasa un identificador al contexto de dispositivo de pantalla al procedimiento en el parámetro *wParam* del mensaje.

El sistema envía un mensaje de [**WM \_ CTLCOLORDLG**](wm-ctlcolordlg.md) al procedimiento del cuadro de diálogo si el procedimiento no procesa el mensaje de [**\_ ERASEBKGND de WM**](/windows/desktop/winmsg/wm-erasebkgnd) . La clase de cuadro de diálogo predefinida no tiene un pincel de fondo de clase, por lo que este mensaje permite que el procedimiento defina su propio fondo sin necesidad de incluir el código para llevar a cabo el trabajo.

En cualquier caso, cuando un procedimiento de cuadro de diálogo no procesa un mensaje de color de control, el sistema usa un pincel con el color de ventana predeterminado para pintar el fondo de todos los controles y ventanas, excepto las barras de desplazamiento. Una aplicación puede recuperar el color de ventana predeterminado pasando el valor de la **\_ ventana de color** a la función [**GetSysColor**](/windows/desktop/api/winuser/nf-winuser-getsyscolor) . Mientras se pinta el fondo, el color de primer plano del contexto de dispositivo de pantalla se establece en el color de texto predeterminado (**color \_ WINDOWTEXT**). En el caso de las barras de desplazamiento, el sistema utiliza un pincel que tiene el color predeterminado de la barra de desplazamiento (**color \_ ScrollBar**). En este caso, los colores de fondo y de primer plano del contexto de dispositivo de pantalla se establecen en blanco y negro, respectivamente.

### <a name="dialog-box-default-message-processing"></a>Procesamiento de mensajes predeterminado del cuadro de diálogo

El procedimiento de ventana de la clase de cuadro de diálogo predefinido lleva a cabo el procesamiento predeterminado para todos los mensajes que no procesa el procedimiento de cuadro de diálogo. Cuando el procedimiento del cuadro de diálogo devuelve **false** para cualquier mensaje, el procedimiento de ventana predefinido comprueba los mensajes y realiza las acciones predeterminadas siguientes:



| Message                                            | Acción predeterminada                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DM \_ GETDEFID**](dm-getdefid.md)                | Puede enviar este mensaje a un cuadro de diálogo. El cuadro de diálogo devuelve el identificador del control del botón de opción predeterminado, si el cuadro de diálogo tiene uno; de lo contrario, devuelve cero.                                                                                                                                                                                                                                                                                                                      |
| [**reposición de DM \_**](dm-reposition.md)            | Puede enviar este mensaje a un cuadro de diálogo de nivel superior. El cuadro de diálogo cambia de posición para que quepa en el área del escritorio.                                                                                                                                                                                                                                                                                                                                                                       |
| [**DM \_ SETDEFID**](dm-setdefid.md)                | Puede enviar este mensaje a un cuadro de diálogo. El cuadro de diálogo establece el botón de opción predeterminado para el control especificado por el identificador del control en el parámetro *wParam* .                                                                                                                                                                                                                                                                                                                             |
| [**activación de WM \_**](/windows/desktop/inputdev/wm-activate)           | Restaura el foco de entrada en el control identificado por el identificador guardado anteriormente si el cuadro de diálogo está activado. De lo contrario, el procedimiento guarda el identificador del control que tiene el foco de entrada.                                                                                                                                                                                                                                                                                               |
| [**CHARTOITEM de WM \_**](../controls/wm-chartoitem.md)         | Devuelve cero.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [**cierre de WM \_**](/windows/desktop/winmsg/wm-close)                   | Envía el mensaje de notificación en el que se ha [**\_ pulsado BN**](../controls/bn-clicked.md) al cuadro de diálogo, especificando **IDCANCEL** como identificador de control. Si el cuadro de diálogo tiene un identificador de control IDCANCEL y el control está deshabilitado actualmente, el procedimiento emite una advertencia y no expone el mensaje.                                                                                                                                                                                              |
| [**COMPAREITEM de WM \_**](../controls/wm-compareitem.md)       | Devuelve cero.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [**ERASEBKGND de WM \_**](/windows/desktop/winmsg/wm-erasebkgnd)         | Rellena el área cliente del cuadro de diálogo mediante el pincel devuelto desde el mensaje de [**\_ CTLCOLORDLG de WM**](wm-ctlcolordlg.md) o con el color de la ventana predeterminado.                                                                                                                                                                                                                                                                                                                                 |
| [**GETFONT de WM \_**](/windows/desktop/winmsg/wm-getfont)               | Devuelve un identificador para la fuente del cuadro de diálogo definido por la aplicación.                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [**INITDIALOG de WM \_**](wm-initdialog.md)            | Devuelve cero.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [**LBUTTONDOWN de WM \_**](/windows/desktop/inputdev/wm-lbuttondown)     | Envía un mensaje [**CB \_ SHOWDROPDOWN**](../controls/cb-showdropdown.md) al cuadro combinado que tiene el foco de entrada y dirige el control para ocultar el cuadro de lista desplegable. El procedimiento llama a [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) para completar la acción predeterminada.                                                                                                                                                                                                                                      |
| [**NCDESTROY de WM \_**](/windows/desktop/winmsg/wm-ncdestroy)           | Libera la memoria global asignada para los controles de edición en el cuadro de diálogo (se aplica a los cuadros de diálogo que especifican el estilo [**\_ LOCALEDIT de DS**](dialog-box-styles.md) ) y libera cualquier fuente definida por la aplicación (se aplica a los cuadros de diálogo que especifican el estilo [**DS \_ SETFONT**](dialog-box-styles.md) o [**DS \_ SHELLFONT**](dialog-box-styles.md) ). El procedimiento llama a la función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) para completar la acción predeterminada. |
| [**NCLBUTTONDOWN de WM \_**](/windows/desktop/inputdev/wm-nclbuttondown) | Envía un mensaje [**CB \_ SHOWDROPDOWN**](../controls/cb-showdropdown.md) al cuadro combinado que tiene el foco de entrada y dirige el control para ocultar el cuadro de lista desplegable. El procedimiento llama a [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) para completar la acción predeterminada.                                                                                                                                                                                                                                      |
| [**NEXTDLGCTL de WM \_**](wm-nextdlgctl.md)            | Establece el foco de entrada en el control siguiente o anterior del cuadro de diálogo, en el control identificado por el identificador del parámetro *wParam* o en el primer control del cuadro de diálogo visible, no deshabilitado y tiene el estilo [**WS \_ TABSTOP**](/windows/desktop/winmsg/window-styles) . El procedimiento omite este mensaje si la ventana actual con el foco de entrada no es un control.                                                                                                                  |
| [**SETFOCUS de WM \_**](/windows/desktop/inputdev/wm-setfocus)           | Establece el foco de entrada en el control identificado por un identificador de ventana de control previamente guardado. Si no existe tal identificador, el procedimiento establece el foco de entrada en el primer control de la plantilla de cuadro de diálogo visible, no deshabilitado y tiene el estilo [**WS \_ TABSTOP**](/windows/desktop/winmsg/window-styles) . Si no existe tal control, el procedimiento establece el foco de entrada en el primer control de la plantilla.                                                                                          |
| [**\_SHOWWINDOW SHOWWINDOW**](/windows/desktop/winmsg/wm-showwindow)         | Guarda un identificador del control que tiene el foco de entrada si se oculta el cuadro de diálogo y, a continuación, llama a [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) para completar la acción predeterminada.                                                                                                                                                                                                                                                                                                                     |
| [**SYSCOMMAND de WM \_**](/windows/desktop/menurc/wm-syscommand)         | Guarda un identificador del control que tiene el foco de entrada si el cuadro de diálogo se está minimizando y, a continuación, llama a [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) para completar la acción predeterminada.                                                                                                                                                                                                                                                                                                                  |
| [**VKEYTOITEM de WM \_**](../controls/wm-vkeytoitem.md)         | Devuelve cero.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |

El procedimiento de ventana predefinido pasa todos los demás mensajes a [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) para el procesamiento predeterminado.

## <a name="dialog-box-keyboard-interface"></a>Interfaz de teclado de cuadro de diálogo

El sistema proporciona una interfaz de teclado especial para los cuadros de diálogo que llevan a cabo un procesamiento especial para varias claves. La interfaz genera mensajes que corresponden a determinados botones del cuadro de diálogo o cambia el foco de entrada de un control a otro. A continuación se muestran las claves usadas en esta interfaz y sus acciones respectivas.


| Clave            | Acción                                                                                                                                                                    |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ALT +*tecla de tecla* | Mueve el foco de entrada al primer control (con el estilo [**WS \_ TABSTOP**](/windows/desktop/winmsg/window-styles) ) después del control estático que contiene el mnemotécnico especificado.        |
| ABAJO           | Mueve el foco de entrada al siguiente control del grupo.                                                                                                                   |
| ENTRAR          | Envía un mensaje de [**\_ comando de WM**](/windows/desktop/menurc/wm-command) al procedimiento del cuadro de diálogo. El parámetro *wParam* se establece en IDOK o en el identificador de control del botón de opción predeterminado. |
| ESC            | Envía un mensaje de [**\_ comando de WM**](/windows/desktop/menurc/wm-command) al procedimiento del cuadro de diálogo. El parámetro *wParam* se establece en IDCANCEL.                                              |
| LEFT           | Mueve el foco de entrada al control anterior del grupo.                                                                                                               |
| *tecla*     | Mueve el foco de entrada al primer control (con el estilo [**WS \_ TABSTOP**](/windows/desktop/winmsg/window-styles) ) después del control estático que contiene el mnemotécnico especificado.        |
| RIGHT          | Mueve el foco de entrada al siguiente control del grupo.                                                                                                                   |
| MAYÚS+TAB      | Mueve el foco de entrada al control anterior que tiene el estilo de [**WS \_ TABSTOP**](/windows/desktop/winmsg/window-styles) .                                                                |
| TAB            | Mueve el foco de entrada al siguiente control que tiene el estilo de [**WS \_ TABSTOP**](/windows/desktop/winmsg/window-styles) .                                                                    |
| UP             | Mueve el foco de entrada al control anterior del grupo.                                                                                                               |

El sistema proporciona automáticamente la interfaz de teclado para todos los cuadros de diálogo modales. No proporciona la interfaz para los cuadros de diálogo no modales a menos que la aplicación llame a la función [**IsDialogMessage**](/windows/desktop/api/Winuser/nf-winuser-isdialogmessagea) para filtrar los mensajes en su bucle de mensajes principal. Esto significa que la aplicación debe pasar el mensaje a **IsDialogMessage** inmediatamente después de recuperar el mensaje de la cola de mensajes. La función procesa los mensajes si es para el cuadro de diálogo y devuelve un valor distinto de cero para indicar que el mensaje se ha procesado y no se debe pasar a la función [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) o [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage) .

Dado que la interfaz de teclado del cuadro de diálogo usa las teclas de dirección para moverse entre los controles de un cuadro de diálogo, una aplicación no puede usar estas teclas para desplazarse por el contenido de ningún cuadro de diálogo modal ni de ningún cuadro de diálogo no modal para el que se llama a [**IsDialogMessage**](/windows/desktop/api/Winuser/nf-winuser-isdialogmessagea) . Cuando un cuadro de diálogo tiene barras de desplazamiento, la aplicación debe proporcionar una interfaz de teclado alternativa para las barras de desplazamiento. Tenga en cuenta que la interfaz del mouse para el desplazamiento está disponible cuando el sistema incluye un mouse.

### <a name="the-ws_tabstop-style"></a>Estilo de WS \_ TABSTOP

El estilo [**WS \_ TABSTOP**](/windows/desktop/winmsg/window-styles) especifica los controles a los que se puede mover el usuario presionando las teclas TAB o Mayús + Tab.

Cuando el usuario presiona la tecla TAB o MAYÚS + TAB, el sistema determina primero si el control que actualmente tiene el foco de entrada procesa estas claves. Envía el control a un mensaje de [**WM \_ GETDLGCODE**](wm-getdlgcode.md) y, si el control devuelve DLGC \_ WANTTAB, el sistema pasa las teclas al control. De lo contrario, el sistema utiliza la función [**GetNextDlgTabItem**](/windows/desktop/api/Winuser/nf-winuser-getnextdlgtabitem) para buscar el siguiente control que está visible, no deshabilitado y que tiene el estilo [**WS \_ TABSTOP**](/windows/desktop/winmsg/window-styles) . La búsqueda comienza con el control que actualmente tiene el foco de entrada y continúa en el orden en que se crearon los controles, es decir, el orden en el que se definen en la plantilla de cuadro de diálogo. Cuando el sistema busca un control que tenga las características necesarias, el sistema le mueve el foco de entrada.

Si la búsqueda del control siguiente con el estilo [**WS \_ TABSTOP**](/windows/desktop/winmsg/window-styles) encuentra una ventana con el estilo **WS \_ ex \_ CONTROLPARENT** , el sistema busca en los elementos secundarios de la ventana de forma recursiva.

Una aplicación también puede usar [**GetNextDlgTabItem**](/windows/desktop/api/Winuser/nf-winuser-getnextdlgtabitem) para buscar controles que tengan el estilo [**WS \_ TABSTOP**](/windows/desktop/winmsg/window-styles) . La función recupera el identificador de ventana del control siguiente o anterior que tiene el estilo **WS \_ TABSTOP** sin mover el foco de entrada.

### <a name="the-ws_group-style"></a>Estilo de \_ grupo de WS

De forma predeterminada, el sistema mueve el foco de entrada al control siguiente o anterior cada vez que el usuario presiona una tecla de dirección. Siempre que el control actual con el foco de entrada no procese estas claves y el control siguiente o anterior no sea un control estático, el sistema seguirá moviendo el foco de entrada a través de todos los controles del cuadro de diálogo cuando el usuario siga presionando las teclas de dirección.

Una aplicación puede usar el estilo de [**\_ Grupo WS**](/windows/desktop/winmsg/window-styles) para modificar este comportamiento predeterminado. El estilo marca el principio de un grupo de controles. Si un control del grupo tiene el foco de entrada cuando el usuario comienza a presionar las teclas de dirección, el foco permanece en el grupo. En general, el primer control de un grupo debe tener el estilo de **\_ Grupo WS** y el resto de controles del grupo no debe tener este estilo. Todos los controles del grupo deben ser contiguos; es decir, deben haberse creado consecutivamente sin controles intermedios.

Cuando el usuario presiona una tecla de dirección, el sistema determina primero si el control actual que tiene el foco de entrada procesa las teclas de dirección. El sistema envía un mensaje de [**WM \_ GETDLGCODE**](wm-getdlgcode.md) al control y, si el control devuelve el valor de **\_ WANTARROWS de DLGC** , pasa la clave al control. De lo contrario, el sistema utiliza la función [**GetNextDlgGroupItem**](/windows/desktop/api/Winuser/nf-winuser-getnextdlggroupitem) para determinar el siguiente control del grupo.

[**GetNextDlgGroupItem**](/windows/desktop/api/Winuser/nf-winuser-getnextdlggroupitem) busca los controles en el orden (o en orden inverso) que se crearon. Si el usuario presiona la tecla derecha o abajo, **GetNextDlgGroupItem** devuelve el siguiente control si el control no tiene el estilo [**de \_ grupo de WS**](/windows/desktop/winmsg/window-styles) . De lo contrario, la función invierte el orden de la búsqueda y devuelve el primer control que tiene el estilo de **\_ grupo de WS** . Si el usuario presiona la tecla izquierda o arriba, la función devuelve el control anterior a menos que el control actual ya tenga el estilo de **\_ grupo de WS** . Si el control actual tiene este estilo, la función invierte el orden de la búsqueda, busca el primer control que tenga el estilo de **\_ Grupo WS** y devuelve el control que precede inmediatamente al control ubicado.

Si la búsqueda del siguiente control en el grupo encuentra una ventana con el estilo **WS \_ ex \_ CONTROLPARENT** , el sistema busca en los elementos secundarios de la ventana de forma recursiva.

Después de que el sistema tenga el control siguiente o anterior, envía un mensaje de [**WM \_ GETDLGCODE**](wm-getdlgcode.md) al control para determinar el tipo de control. Después, el sistema mueve el foco de entrada al control si no es un control estático. Si el control es un botón de radio automático, el sistema le envía un mensaje de [**\_ clic de BM**](../controls/bm-click.md) . Una aplicación también puede usar [**GetNextDlgGroupItem**](/windows/desktop/api/Winuser/nf-winuser-getnextdlggroupitem) para buscar controles en un grupo.

Por lo general, el primer control del grupo combina los estilos WS [**\_ Group**](/windows/desktop/winmsg/window-styles) y [**WS \_ TABSTOP**](/windows/desktop/winmsg/window-styles) para que el usuario pueda moverse de un grupo a un grupo mediante la tecla TAB. Si el grupo contiene botones de radio, la aplicación debe aplicar el estilo **WS \_ TABSTOP** solo al primer control del grupo. El sistema mueve automáticamente el estilo cuando el usuario se mueve entre los controles del grupo. Esto garantiza que el foco de entrada siempre estará en el control seleccionado más recientemente cuando el usuario se mueva al grupo mediante la tecla TAB.

### <a name="mnemonics"></a>Teclas

Un mnemotécnico es una letra o un dígito seleccionados en la etiqueta de un botón o en el texto de un control estático. El sistema mueve el foco de entrada al control asociado con el mnemotécnico siempre que el usuario presiona la tecla que se corresponde con el mnemotécnico o presiona esta tecla y la tecla ALT en combinación. Las teclas de método abreviado proporcionan una forma rápida para que el usuario se mueva a un control especificado mediante el teclado.

Una aplicación crea un mnemotécnico para un control insertando el símbolo de y comercial (&) inmediatamente antes de la letra o el dígito seleccionados en la etiqueta o el texto del control. En la mayoría de los casos, la cadena terminada en null que se proporciona con el control en la plantilla de cuadro de diálogo contiene el símbolo de y comercial. Sin embargo, una aplicación puede crear un mnemotécnico en cualquier momento reemplazando la etiqueta o el texto existente del control mediante la función [**SetDlgItemText**](/windows/desktop/api/Winuser/nf-winuser-setdlgitemtexta) . Solo se puede especificar un mnemotécnico para cada control. Aunque se recomienda, los mnemónicos de un cuadro de diálogo no deben ser únicos.

Cuando el usuario presiona una tecla de letra o de dígito, el sistema determina primero si el control actual que tiene el foco de entrada procesa la clave. El sistema envía un mensaje de [**WM \_ GETDLGCODE**](wm-getdlgcode.md) al control y, si el control devuelve el valor **DLGC \_ WANTALLKEYS** o **Dlg \_ WANTMESSAGE** , el sistema pasa la clave al control. De lo contrario, busca un control cuyo mnemotécnico coincida con la letra o el dígito especificados. Continúa buscando hasta que encuentra un control o examina todos los controles. Durante la búsqueda, omite los controles estáticos que tienen el estilo [**SS \_ noprefix**](../controls/static-control-styles.md) .

Si la búsqueda de un control con un mnemotécnico coincidente encuentra una ventana con el estilo **WS \_ ex \_ CONTROLPARENT** , el sistema busca en los elementos secundarios de la ventana de forma recursiva.

Si el sistema encuentra un control estático y el control no está deshabilitado, el sistema mueve el foco de entrada al primer control después del control estático visible, no deshabilitado y que tiene el estilo [**WS \_ TABSTOP**](/windows/desktop/winmsg/window-styles) . Si el sistema localiza algún otro control que tenga una tecla de teclas coincidentes, mueve el foco de entrada a ese control. Si el control es un botón de método de envío predeterminado, el sistema envía un mensaje de notificación de [**BN \_ en**](../controls/bn-clicked.md) el procedimiento de cuadro de diálogo. Si el control es otro estilo de botón y no hay ningún otro control en el cuadro de diálogo que tenga el mismo mnemotécnico, el sistema envía el mensaje de [**\_ clic de BM**](../controls/bm-click.md) al control.

## <a name="dialog-box-settings"></a>Configuración del cuadro de diálogo

La configuración del cuadro de diálogo son las selecciones actuales y los valores de los controles del cuadro de diálogo. El procedimiento de cuadro de diálogo es responsable de inicializar los controles en esta configuración al crear el cuadro de diálogo. También es responsable de recuperar la configuración actual de los controles antes de destruir el cuadro de diálogo. Los métodos que se usan para inicializar y recuperar la configuración dependen del tipo de control.

Para obtener más información, vea los temas siguientes:

-   [Botones de radio y casillas](#radio-buttons-and-check-boxes)
-   [Controles de edición del cuadro de diálogo](#dialog-box-edit-controls)
-   [Cuadros de lista, cuadros combinados y listas de directorios](#list-boxes-combo-boxes-and-directory-listings)
-   [Mensajes de control de cuadro de diálogo](#dialog-box-control-messages)

### <a name="radio-buttons-and-check-boxes"></a>Botones de radio y casillas

Los cuadros de diálogo usan botones de radio y casillas para permitir que el usuario elija una lista de opciones. Los botones de radio permiten al usuario elegir entre opciones mutuamente excluyentes. las casillas permiten al usuario seleccionar una combinación de opciones.

El procedimiento de cuadro de diálogo puede establecer el estado inicial de una casilla mediante la función [**CheckDlgButton**](https://msdn.microsoft.com/library/Cc410649(v=MSDN.10).aspx) , que establece o desactiva la casilla. En el caso de los botones de radio de un grupo de botones de radio mutuamente excluyentes, el procedimiento del cuadro de diálogo puede usar la función [**CheckRadioButton**](https://msdn.microsoft.com/library/Cc410654(v=MSDN.10).aspx) para establecer el botón de radio adecuado y borrar automáticamente cualquier otro botón de radio.

Antes de que finalice un cuadro de diálogo, el procedimiento del cuadro de diálogo puede comprobar el estado de cada botón de radio y casilla mediante la función [**IsDlgButtonChecked**](https://msdn.microsoft.com/library/Cc364806(v=MSDN.10).aspx) , que devuelve el estado actual del botón. Un cuadro de diálogo normalmente guarda esta información para inicializar los botones la próxima vez que se crea el cuadro de diálogo.

### <a name="dialog-box-edit-controls"></a>Controles de edición del cuadro de diálogo

Muchos cuadros de diálogo tienen controles de edición que permiten al usuario proporcionar texto como entrada. La mayoría de los procedimientos de cuadro de diálogo inicializan un control de edición cuando se inicia por primera vez el cuadro de diálogo. Por ejemplo, el procedimiento de cuadro de diálogo puede colocar un nombre de archivo propuesto en el control que el usuario puede seleccionar, modificar o reemplazar. El procedimiento de cuadro de diálogo puede establecer el texto en un control de edición mediante la función [**SetDlgItemText**](/windows/desktop/api/Winuser/nf-winuser-setdlgitemtexta) , que copia el texto de un búfer especificado en el control de edición. Cuando el control de edición recibe el foco de entrada, selecciona automáticamente el texto completo para su edición.

Dado que los controles de edición no devuelven automáticamente su texto al cuadro de diálogo, el procedimiento del cuadro de diálogo debe recuperar el texto antes de finalizar. Puede recuperar el texto mediante la función [**GetDlgItemText**](/windows/desktop/api/Winuser/nf-winuser-getdlgitemtexta) , que copia el texto del control de edición en un búfer. Normalmente, el procedimiento de cuadro de diálogo guarda este texto para inicializar el control de edición más adelante o lo pasa a la ventana primaria para su procesamiento.

Algunos cuadros de diálogo usan controles de edición que permiten al usuario escribir números. El procedimiento de cuadro de diálogo puede recuperar un número de un control de edición mediante la función [**GetDlgItemInt**](/windows/desktop/api/Winuser/nf-winuser-getdlgitemint) , que recupera el texto del control de edición y convierte el texto en un valor decimal. El usuario escribe el número en dígitos decimales. Puede ser con signo o sin signo. El procedimiento de cuadro de diálogo puede mostrar un entero mediante la función [**SetDlgItemInt**](/windows/desktop/api/Winuser/nf-winuser-setdlgitemint) . **SetDlgItemInt** convierte un entero con o sin signo en una cadena de dígitos decimales.

### <a name="list-boxes-combo-boxes-and-directory-listings"></a>Cuadros de lista, cuadros combinados y listas de directorios

Algunos cuadros de diálogo muestran listas de nombres desde los que el usuario puede seleccionar uno o varios nombres. Para mostrar una lista de nombres de archivo, por ejemplo, un cuadro de diálogo utiliza normalmente un cuadro de lista y las funciones [**DlgDirList**](https://msdn.microsoft.com/library/Cc410788(v=MSDN.10).aspx) y [**DlgDirSelectEx**](https://msdn.microsoft.com/library/Cc410769(v=MSDN.10).aspx) . La función **DlgDirList** rellena automáticamente un cuadro de lista con los nombres de archivo del directorio actual. La función **DlgDirSelect** recupera el nombre de archivo seleccionado del cuadro de lista. Juntas, estas dos funciones proporcionan una manera cómoda de que un cuadro de diálogo muestre una lista de directorios para que el usuario pueda seleccionar un archivo sin tener que escribir su nombre y ubicación.

Un cuadro de diálogo también puede usar un cuadro combinado para mostrar una lista de nombres de archivo. La función [**DlgDirListComboBox**](https://msdn.microsoft.com/library/Cc410798(v=MSDN.10).aspx) rellena automáticamente una parte del cuadro de lista del cuadro combinado con los nombres de archivo en el directorio actual. La función [**DlgDirSelectComboBoxEx**](https://msdn.microsoft.com/library/Cc410768(v=MSDN.10).aspx) recupera un nombre de archivo seleccionado de la parte del cuadro de lista.

### <a name="dialog-box-control-messages"></a>Mensajes de control de cuadro de diálogo

Muchos controles reconocen mensajes predefinidos que, cuando los reciben los controles, pueden llevar a cabo alguna acción. Por ejemplo, el mensaje [**BM \_ SETCHECK**](../controls/bm-setcheck.md) establece la marca en una casilla y el mensaje [**\_ GETSEL em**](../controls/em-getsel.md) recupera la parte del texto del control que está seleccionada actualmente. Los mensajes de control proporcionan un procedimiento de diálogo mayor y más flexible a los controles que las funciones estándar, por lo que se suelen usar cuando el cuadro de diálogo requiere interacciones complejas con el usuario.

Un procedimiento de cuadro de diálogo puede enviar un mensaje a un control proporcionando el identificador de control y utilizando la función [**SendDlgItemMessage**](/windows/desktop/api/Winuser/nf-winuser-senddlgitemmessagea) , que es idéntica a la función [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) , salvo que usa un identificador de control en lugar de un identificador de ventana para identificar el control que va a recibir el mensaje. Un mensaje especificado puede requerir que el procedimiento de cuadro de diálogo envíe parámetros con el mensaje, y el mensaje puede tener los valores devueltos correspondientes. La operación y los requisitos de cada mensaje de control dependen del propósito del mensaje y del control que lo procesa.

Para obtener más información sobre los mensajes de control, vea [controles de Windows](../controls/window-controls.md).

## <a name="custom-dialog-boxes"></a>Cuadros de diálogo personalizados

Una aplicación puede crear cuadros de diálogo personalizados mediante el uso de una clase de ventana definida por la aplicación para los cuadros de diálogo en lugar de utilizar la clase de cuadro de diálogo predefinida. Normalmente, las aplicaciones usan este método cuando un cuadro de diálogo es su ventana principal, pero también es útil para crear cuadros de diálogo modales y no modales para las aplicaciones que tienen ventanas estándar superpuestas.

La clase de ventana definida por la aplicación permite a la aplicación definir un procedimiento de ventana para el cuadro de diálogo y procesar los mensajes antes de enviarlos al procedimiento del cuadro de diálogo. También permite que la aplicación defina un icono de clase, un pincel de fondo de clase y un menú de clase para el cuadro de diálogo. La aplicación debe registrar la clase de ventana antes de intentar crear un cuadro de diálogo y debe proporcionar la plantilla de cuadro de diálogo con el valor Atom o el nombre de la clase de ventana.

Muchas aplicaciones crean una nueva clase de cuadro de diálogo recuperando primero la información de clase de la clase de cuadro de diálogo predefinida y pasándola a la función [**GetClassInfo**](/windows/desktop/api/winuser/nf-winuser-getclassinfoa) , que rellena una estructura [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) con la información. La aplicación modifica los miembros individuales de la estructura, como el nombre de clase, el pincel y el icono, y registra la nueva clase mediante la función [**RegisterClass**](/windows/desktop/api/winuser/nf-winuser-registerclassa) . Si una aplicación rellena la estructura **WNDCLASS** por sí misma, debe establecer el miembro **cbWndExtra** en **DLGWINDOWEXTRA**, que es el número de bytes adicionales que el sistema necesita para cada cuadro de diálogo. Si una aplicación también usa bytes adicionales para cada cuadro de diálogo, debe superar los bytes adicionales que requiere el sistema.

El procedimiento de ventana del cuadro de diálogo personalizado tiene los mismos parámetros y requisitos que cualquier otro procedimiento de ventana. Sin embargo, a diferencia de otros procedimientos de ventana, el procedimiento de ventana para este cuadro de diálogo debe llamar a la función [**DefDlgProc**](/windows/desktop/api/Winuser/nf-winuser-defdlgprocw) en lugar de a la función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) para los mensajes que no procese. **DefDlgProc** lleva a cabo el mismo procesamiento de mensajes predeterminado que el procedimiento de ventana para el cuadro de diálogo predefinido, que incluye la llamada al procedimiento del cuadro de diálogo.

Una aplicación también puede crear cuadros de diálogo personalizados mediante la creación de subclases del procedimiento de ventana del cuadro de diálogo predefinido. La función [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) permite a una aplicación especificar el procedimiento de ventana para una ventana especificada. La aplicación también puede tratar de subclases mediante la función [**SetClassLong**](/windows/desktop/api/winuser/nf-winuser-setclasslonga) , pero esto afecta a todos los cuadros de diálogo del sistema, no solo a los que pertenecen a la aplicación.

Las aplicaciones que crean cuadros de diálogo personalizados a veces proporcionan una interfaz de teclado alternativa para los cuadros de diálogo. En el caso de los cuadros de diálogo no modales, esto puede significar que la aplicación no llama a la función [**IsDialogMessage**](/windows/desktop/api/Winuser/nf-winuser-isdialogmessagea) y, en su lugar, procesa toda la entrada del teclado en el procedimiento de ventana personalizado. En tales casos, la aplicación puede usar el mensaje de [**\_ NEXTDLGCTL de WM**](wm-nextdlgctl.md) para minimizar el código necesario para desplazar el foco de entrada de un control a otro. Este mensaje, cuando se pasa a [**DefDlgProc**](/windows/desktop/api/Winuser/nf-winuser-defdlgprocw), mueve el foco de entrada a un control especificado y actualiza la apariencia de los controles, como mover el borde del botón de opción predeterminado o establecer un botón de radio automático.
