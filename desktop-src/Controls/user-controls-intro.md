---
title: Controles personalizados
description: Esta sección contiene información sobre los controles personalizados o definidos por la aplicación.
ms.assetid: 220f7058-db04-46d0-acee-ed5e676790b3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12d1a31a44f1f71d99088f7729c2de6d5fdb597e14507f5f994dfaca1b96613d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120059715"
---
# <a name="custom-controls"></a>Controles personalizados

Esta sección contiene información sobre los controles personalizados o definidos por la aplicación.

Se tratan los temas siguientes.

-   [Crear Owner-Drawn controles](#creating-owner-drawn-controls)
-   [Subclases de la clase Window de un control existente](#subclassing-the-window-class-of-an-existing-control)
-   [Implementar una clase Application-Defined window](#implementing-an-application-defined-window-class)
-   [Envío de notificaciones desde un control](#sending-notifications-from-a-control)
-   [Accesibilidad](#accessibility)
-   [Temas relacionados](#related-topics)

## <a name="creating-owner-drawn-controls"></a>Crear Owner-Drawn controles

Los botones, menús, controles de texto estático, cuadros de lista y cuadros combinados se pueden crear con una marca de estilo dibujada por el propietario. Cuando un control tiene el estilo dibujado por el propietario, el sistema controla la interacción del usuario con el control como de costumbre, realizando tareas como detectar cuándo un usuario ha elegido un botón y notificar al propietario del evento. Sin embargo, dado que el control está dibujado por el propietario, la ventana primaria del control es responsable de la apariencia visual del control. La ventana primaria recibe un mensaje cada vez que se debe dibujar el control.

En el caso de los botones y los controles de texto estático, el estilo dibujado por el propietario afecta a la forma en que el sistema dibuja todo el control. Para los cuadros de lista y los cuadros combinados, la ventana primaria dibuja los elementos dentro del control y el control dibuja su propio contorno. Por ejemplo, una aplicación puede personalizar un cuadro de lista para que muestre un mapa de bits pequeño junto a cada elemento de la lista.

En el código de ejemplo siguiente se muestra cómo crear un control de texto estático dibujado por el propietario. Suponga que Unicode está definido.


```
// g_myStatic is a global HWND variable.
g_myStatic = CreateWindowEx(0, L"STATIC", L"Some static text", 
            WS_CHILD | WS_VISIBLE | SS_OWNERDRAW, 
            25, 125, 150, 20, hDlg, 0, 0, 0);
```



En el ejemplo siguiente, en el procedimiento de ventana del cuadro de diálogo que contiene el control creado en el ejemplo anterior, el mensaje [**\_ DRAWITEM**](wm-drawitem.md) de WM se controla mostrando el texto en un color personalizado, utilizando la fuente predeterminada. Tenga en cuenta que no es necesario llamar a [**BeginPaint**](/windows/desktop/api/winuser/nf-winuser-beginpaint) y [**EndPaint**](/windows/desktop/api/winuser/nf-winuser-endpaint) al controlar **WM \_ DRAWITEM**.


```
case WM_DRAWITEM:
{
    LPDRAWITEMSTRUCT pDIS = (LPDRAWITEMSTRUCT)lParam;
    if (pDIS->hwndItem == g_myStatic)
    {
        SetTextColor(pDIS->hDC, RGB(100, 0, 100));
        WCHAR staticText[99];
        int len = SendMessage(myStatic, WM_GETTEXT, 
            ARRAYSIZE(staticText), (LPARAM)staticText);
        TextOut(pDIS->hDC, pDIS->rcItem.left, pDIS->rcItem.top, staticText, len);
    }
    return TRUE;
}
```



Para obtener más información sobre los controles dibujados por el propietario, vea Crear un cuadro de lista [dibujado](using-list-boxes.md) por el propietario y [Cuadros combinados dibujados por el propietario](about-combo-boxes.md).

## <a name="subclassing-the-window-class-of-an-existing-control"></a>Subclases de la clase Window de un control existente

La creación de subclases de un control existente es otra manera de crear un control personalizado. El procedimiento de subclase puede modificar los comportamientos seleccionados del control procesando los mensajes que afectan a los comportamientos seleccionados. Todos los demás mensajes pasan al procedimiento de ventana original para el control . Por ejemplo, una aplicación puede mostrar un mapa de bits pequeño junto al texto en un control de edición de una sola línea de solo lectura mediante la subclase del control y el procesamiento del [**mensaje \_ WM PAINT.**](/windows/desktop/gdi/wm-paint) Para obtener más información, vea [Acerca de los procedimientos de ventana](/windows/desktop/winmsg/about-window-procedures) y los controles de [subclases](subclassing-overview.md).

## <a name="implementing-an-application-defined-window-class"></a>Implementar una clase Application-Defined window

Para crear un control que no se base explícitamente en un control existente, la aplicación debe crear y registrar una clase de ventana. El proceso para registrar una clase de ventana definida por la aplicación para un control personalizado es el mismo que el registro de una clase para una ventana normal. Para crear un control personalizado, especifique el nombre de la clase de ventana en la [**función CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) o en una plantilla de cuadro de diálogo. Cada clase debe tener un nombre único, un procedimiento de ventana correspondiente y otra información.

Como mínimo, el procedimiento de ventana dibuja el control . Si una aplicación usa el control para permitir que el usuario escriba información, el procedimiento de ventana también procesa los mensajes de entrada del teclado y el mouse y envía mensajes de notificación a la ventana primaria. Además, si el control admite mensajes de control, el procedimiento de ventana procesa los mensajes que le envía la ventana primaria u otras ventanas. Por ejemplo, los controles suelen procesar el mensaje [**\_ GETDLGCODE de WM**](/windows/desktop/dlgbox/wm-getdlgcode) enviado por los cuadros de diálogo para dirigir un cuadro de diálogo para procesar la entrada de teclado de una manera determinada.

El procedimiento de ventana para un control definido por la aplicación debe procesar cualquier mensaje de control predefinido en la tabla siguiente si el mensaje afecta al funcionamiento del control.



| Message                                          | Recomendación                                                                                                                                                                                                                                  |
|--------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WM \_ GETDLGCODE**](/windows/desktop/dlgbox/wm-getdlgcode)       | Procese si el control usa las teclas de dirección ENTER, ESC, TAB o . La [**función IsDialogMessage**](/windows/desktop/api/winuser/nf-winuser-isdialogmessagea) envía este mensaje a los controles de un cuadro de diálogo para determinar si se deben procesar las claves o pasarlas al control. |
| [**WM \_ GETFONT**](/windows/desktop/winmsg/wm-getfont)             | Procese si también se procesa el mensaje [**\_ WM SETFONT.**](/windows/desktop/winmsg/wm-setfont)                                                                                                                                                                  |
| [**WM \_ GETTEXT**](/windows/desktop/winmsg/wm-gettext)             | Procese si el texto del control no es el mismo que el título especificado por la [**función CreateWindowEx.**](/windows/desktop/api/winuser/nf-winuser-createwindowexa)                                                                                                                 |
| [**WM \_ GETTEXTLENGTH**](/windows/desktop/winmsg/wm-gettextlength) | Procese si el texto del control no es el mismo que el título especificado por la [**función CreateWindowEx.**](/windows/desktop/api/winuser/nf-winuser-createwindowexa)                                                                                                                 |
| [**WM \_ KILLFOCUS**](/windows/desktop/inputdev/wm-killfocus)       | Procese si el control muestra un caret, un rectángulo de foco u otro elemento para indicar que tiene el foco de entrada.                                                                                                                            |
| [**WM \_ SETFOCUS**](/windows/desktop/inputdev/wm-setfocus)         | Procese si el control muestra un caret, un rectángulo de foco u otro elemento para indicar que tiene el foco de entrada.                                                                                                                            |
| [**WM \_ SETTEXT**](/windows/desktop/winmsg/wm-settext)             | Procese si el texto del control no es el mismo que el título especificado por la [**función CreateWindowEx.**](/windows/desktop/api/winuser/nf-winuser-createwindowexa)                                                                                                                 |
| [**WM \_ SETFONT**](/windows/desktop/winmsg/wm-setfont)             | Procese si el control muestra texto. El sistema envía este mensaje al crear un cuadro de diálogo con el estilo \_ DS SETFONT.                                                                                                                  |



 

Los mensajes de control definidos por la aplicación son específicos del control especificado y se deben enviar explícitamente al control mediante una [**función SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) o [**SendDlgItemMessage.**](/windows/desktop/api/winuser/nf-winuser-senddlgitemmessagea) El valor numérico de cada mensaje debe ser único y no debe estar en conflicto con los valores de otros mensajes de ventana. Para asegurarse de que los valores de mensaje definidos por la aplicación no entren en conflicto, una aplicación debe crear cada valor agregando un número único al [**valor DE USUARIO \_ DE WM.**](/windows/desktop/winmsg/wm-user)

## <a name="sending-notifications-from-a-control"></a>Envío de notificaciones desde un control

Es posible que se necesiten controles personalizados para enviar notificaciones de eventos a la ventana primaria para que la aplicación host pueda responder a estos eventos. Por ejemplo, una vista de lista personalizada podría enviar una notificación cuando el usuario selecciona un elemento y otra notificación cuando se hace doble clic en un elemento.

Las notificaciones se envían como [**mensajes WM \_ COMMAND**](/windows/desktop/menurc/wm-command) [**o WM \_ NOTIFY.**](wm-notify.md) **WM \_ Los mensajes NOTIFY** llevan más información que **los mensajes WM \_ COMMAND.**

El identificador de control es un número único que la aplicación usa para identificar el control que envía el mensaje. La aplicación establece el identificador de un control cuando crea el control. La aplicación especifica el identificador en el parámetro *hMenu* de la función [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) o en el miembro **id** de la [**estructura DLGITEMTEMPLATEEX.**](/windows/desktop/dlgbox/dlgitemtemplateex)

Dado que el propio control no establece el identificador de control, el control debe recuperar el identificador para poder enviar mensajes de notificación. Un control debe usar la [**función GetDlgCtrlID**](/windows/desktop/api/winuser/nf-winuser-getdlgctrlid) para recuperar su propio identificador de control. Aunque el identificador de control se especifica como identificador de menú cuando se crea el control, la [**función GetMenu**](/windows/desktop/api/winuser/nf-winuser-getmenu) no se puede usar para recuperar el identificador. Como alternativa, un control puede recuperar el identificador del **miembro hMenu** en la [**estructura CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) mientras se procesa [**el mensaje WM \_ CREATE.**](/windows/desktop/winmsg/wm-create)

En los ejemplos siguientes, donde *hwndControl* es el identificador de la ventana de control y CN VALUECHANGED es una definición de notificación personalizada, se muestran las dos maneras de enviar una notificación específica \_ del control.


```
 // Send as WM_COMMAND.
SendMessage(GetParent(hwndControl), 
    WM_COMMAND,
    MAKEWPARAM(GetDlgCtrlID(hwndControl), CN_VALUECHANGED),
    (LPARAM)hwndControl);

// Send as WM_NOTIFY.           
NMHDR nmh;
nmh.code = CN_VALUECHANGED;
nmh.idFrom = GetDlgCtrlID(hwndControl);
nmh.hwndFrom = hwndControl;
SendMessage(GetParent(hwndControl), 
    WM_NOTIFY, 
    (WPARAM)hwndControl, 
    (LPARAM)&nmh);
```



Tenga en cuenta [**que la estructura NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) puede formar parte de una estructura más grande definida por el control que contiene información adicional. En el ejemplo, los valores antiguos y nuevos del control podrían estar contenidos en esta estructura. (Estas estructuras extendidas se usan con muchas notificaciones estándar; por ejemplo, vea [LVN \_ INSERTITEM](lvn-insertitem.md), que usa la [**estructura NMLISTVIEW).**](/windows/win32/api/commctrl/ns-commctrl-nmlistview)

## <a name="accessibility"></a>Accesibilidad

Todos los controles comunes admiten Microsoft Active Accessibility (MSAA), que permite el acceso mediante programación a aplicaciones de tecnología accesible, como lectores de pantalla. MSAA también permite a Automatización de la interfaz de usuario, una tecnología más reciente, interactuar con los controles.

Los controles personalizados deben implementar la [**interfaz IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) (para admitir MSAA) o Automatización de la interfaz de usuario interfaces, o ambas. De lo contrario, los productos de tecnología accesible solo podrán obtener información muy limitada sobre la ventana de control, no tendrán acceso a las propiedades del control y no podrán desencadenar eventos en el control.

Para obtener más información sobre cómo hacer que el control sea accesible, [consulte Windows Automation API](/windows/desktop/WinAuto/windows-automation-api-portal).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Conceptual**
</dt> <dt>

[Referencia general de control](common-control-reference.md)
</dt> <dt>

[Personalizar la apariencia de un control mediante un dibujo personalizado](custom-draw.md)
</dt> <dt>

[Mensajes de control](control-messages.md)
</dt> <dt>

[Usar estilos visuales con Owner-Drawn controles](using-visual-styles.md)
</dt> </dl>

 

 