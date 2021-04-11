---
title: Controles personalizados
description: Esta sección contiene información sobre los controles personalizados o definidos por la aplicación.
ms.assetid: 220f7058-db04-46d0-acee-ed5e676790b3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e82ed9394ec06257e524153b86ef487f4507f35b
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104149640"
---
# <a name="custom-controls"></a>Controles personalizados

Esta sección contiene información sobre los controles personalizados o definidos por la aplicación.

Se tratan los temas siguientes.

-   [Crear controles de Owner-Drawn](#creating-owner-drawn-controls)
-   [Subclase de la clase de ventana de un control existente](#subclassing-the-window-class-of-an-existing-control)
-   [Implementar una clase de ventana Application-Defined](#implementing-an-application-defined-window-class)
-   [Enviar notificaciones desde un control](#sending-notifications-from-a-control)
-   [Accesibilidad](#accessibility)
-   [Temas relacionados](#related-topics)

## <a name="creating-owner-drawn-controls"></a>Crear controles de Owner-Drawn

Los botones, los menús, los controles de texto estático, los cuadros de lista y los cuadros combinados se pueden crear con una marca de estilo dibujado por el propietario. Cuando un control tiene el estilo dibujado por el propietario, el sistema controla la interacción del usuario con el control como de costumbre, realizando tareas como detectar cuándo un usuario ha elegido un botón y notificando al propietario del botón el evento. Sin embargo, dado que el control está dibujado por el propietario, la ventana primaria del control es responsable de la apariencia visual del control. La ventana primaria recibe un mensaje cada vez que se debe dibujar el control.

En el caso de los botones y los controles de texto estático, el estilo dibujado por el propietario afecta al modo en que el sistema dibuja todo el control. En los cuadros de lista y cuadros combinados, la ventana primaria dibuja los elementos dentro del control y el control dibuja su propio esquema. Por ejemplo, una aplicación puede personalizar un cuadro de lista para que muestre un mapa de bits pequeño junto a cada elemento de la lista.

En el ejemplo de código siguiente se muestra cómo crear un control de texto estático dibujado por el propietario. Supongamos que se ha definido Unicode.


```
// g_myStatic is a global HWND variable.
g_myStatic = CreateWindowEx(0, L"STATIC", L"Some static text", 
            WS_CHILD | WS_VISIBLE | SS_OWNERDRAW, 
            25, 125, 150, 20, hDlg, 0, 0, 0);
```



En el ejemplo siguiente, en el procedimiento de ventana del cuadro de diálogo que contiene el control creado en el ejemplo anterior, se controla el mensaje de Windows de [**WM \_**](wm-drawitem.md) mostrando el texto en un color personalizado con la fuente predeterminada. Tenga en cuenta que no es necesario llamar a [**BeginPaint**](/windows/desktop/api/winuser/nf-winuser-beginpaint) y [**EndPaint**](/windows/desktop/api/winuser/nf-winuser-endpaint) cuando se controla **WM \_ DRAWITEM**.


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



Para obtener más información sobre los controles dibujados por el propietario, vea [crear un cuadro de lista dibujado por el propietario](using-list-boxes.md) y [cuadros combinados dibujados](about-combo-boxes.md)por el propietario.

## <a name="subclassing-the-window-class-of-an-existing-control"></a>Subclase de la clase de ventana de un control existente

La creación de subclases de un control existente es otra manera de crear un control personalizado. El procedimiento de subclase puede modificar los comportamientos seleccionados del control procesando los mensajes que afectan a los comportamientos seleccionados. El resto de mensajes pasan al procedimiento de ventana original para el control. Por ejemplo, una aplicación puede mostrar un mapa de bits pequeño junto al texto en un control de edición de una sola línea de solo lectura mediante la subclase del control y el procesamiento del mensaje de [**\_ dibujo de WM**](/windows/desktop/gdi/wm-paint) . Para obtener más información, vea [About Window Procedures](/windows/desktop/winmsg/about-window-procedures) and [Subclassing Controls](subclassing-overview.md).

## <a name="implementing-an-application-defined-window-class"></a>Implementar una clase de ventana Application-Defined

Para crear un control que no esté basado explícitamente en un control existente, la aplicación debe crear y registrar una clase de ventana. El proceso para registrar una clase de ventana definida por la aplicación para un control personalizado es igual que registrar una clase para una ventana normal. Para crear un control personalizado, especifique el nombre de la clase de ventana en la función [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) o en una plantilla de cuadro de diálogo. Cada clase debe tener un nombre único, un procedimiento de ventana correspondiente y otra información.

Como mínimo, el procedimiento de ventana dibuja el control. Si una aplicación utiliza el control para permitir que el usuario escriba información, el procedimiento de ventana también procesa los mensajes de entrada desde el teclado y el mouse y envía mensajes de notificación a la ventana primaria. Además, si el control admite mensajes de control, el procedimiento de ventana procesa los mensajes que le envía la ventana primaria u otras ventanas. Por ejemplo, los controles suelen procesar el mensaje de [**WM \_ GETDLGCODE**](/windows/desktop/dlgbox/wm-getdlgcode) enviado por cuadros de diálogo para dirigir un cuadro de diálogo para procesar la entrada del teclado de una manera determinada.

El procedimiento de ventana de un control definido por la aplicación debe procesar cualquier mensaje de control predefinido en la tabla siguiente si el mensaje afecta a la operación del control.



| Message                                          | Recomendación                                                                                                                                                                                                                                  |
|--------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GETDLGCODE de WM \_**](/windows/desktop/dlgbox/wm-getdlgcode)       | Procesa si el control usa las teclas entrar, ESC, TAB o de dirección. La función [**IsDialogMessage**](/windows/desktop/api/winuser/nf-winuser-isdialogmessagea) envía este mensaje a los controles de un cuadro de diálogo para determinar si se deben procesar las claves o pasarlas al control. |
| [**GETFONT de WM \_**](/windows/desktop/winmsg/wm-getfont)             | Procesar si el mensaje de [**WM \_ SETFONT**](/windows/desktop/winmsg/wm-setfont) también se ha procesado.                                                                                                                                                                  |
| [**GETTEXT de WM \_**](/windows/desktop/winmsg/wm-gettext)             | Procesa si el texto del control no es igual que el título especificado por la función [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) .                                                                                                                 |
| [**GETTEXTLENGTH de WM \_**](/windows/desktop/winmsg/wm-gettextlength) | Procesa si el texto del control no es igual que el título especificado por la función [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) .                                                                                                                 |
| [**KILLFOCUS de WM \_**](/windows/desktop/inputdev/wm-killfocus)       | Proceso si el control muestra un símbolo de intercalación, un rectángulo de foco u otro elemento para indicar que tiene el foco de entrada.                                                                                                                            |
| [**SETFOCUS de WM \_**](/windows/desktop/inputdev/wm-setfocus)         | Proceso si el control muestra un símbolo de intercalación, un rectángulo de foco u otro elemento para indicar que tiene el foco de entrada.                                                                                                                            |
| [**SETTEXT de WM \_**](/windows/desktop/winmsg/wm-settext)             | Procesa si el texto del control no es igual que el título especificado por la función [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) .                                                                                                                 |
| [**WM \_**](/windows/desktop/winmsg/wm-setfont)             | Procesa si el control muestra texto. El sistema envía este mensaje al crear un cuadro de diálogo que tenga el \_ estilo de DS SETFONT.                                                                                                                  |



 

Los mensajes de control definidos por la aplicación son específicos del control dado y se deben enviar explícitamente al control mediante una función [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) o [**SendDlgItemMessage**](/windows/desktop/api/winuser/nf-winuser-senddlgitemmessagea) . El valor numérico de cada mensaje debe ser único y no debe entrar en conflicto con los valores de otros mensajes de ventana. Para asegurarse de que los valores de mensaje definidos por la aplicación no entren en conflicto, una aplicación debe crear cada valor agregando un número único al valor de [**\_ usuario de WM**](/windows/desktop/winmsg/wm-user) .

## <a name="sending-notifications-from-a-control"></a>Enviar notificaciones desde un control

Es posible que sea necesario que los controles personalizados envíen notificaciones de eventos a la ventana primaria para que la aplicación host pueda responder a estos eventos. Por ejemplo, una vista de lista personalizada puede enviar una notificación cuando el usuario selecciona un elemento y otra notificación cuando se hace doble clic en un elemento.

Las notificaciones se envían [**como \_ comandos de WM**](/windows/desktop/menurc/wm-command) o mensajes de [**\_ notificación de WM**](wm-notify.md) . **WM \_** Los mensajes de notificación contienen más información que los mensajes de **\_ comandos de WM** .

El identificador de control es un número único que la aplicación usa para identificar el control que envía el mensaje. La aplicación establece el identificador de un control cuando crea el control. La aplicación especifica el identificador en el parámetro *hMenu* de la función [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) o en el miembro **ID** de la estructura [**DLGITEMTEMPLATEEX**](/windows/desktop/dlgbox/dlgitemtemplateex) .

Dado que el propio control no establece el identificador de control, el control debe recuperar el identificador antes de poder enviar mensajes de notificación. Un control debe usar la función [**GetDlgCtrlID**](/windows/desktop/api/winuser/nf-winuser-getdlgctrlid) para recuperar su propio identificador de control. Aunque el identificador de control se especifica como el identificador de menú cuando se crea el control, la función [**GetMenu**](/windows/desktop/api/winuser/nf-winuser-getmenu) no se puede usar para recuperar el identificador. Como alternativa, un control puede recuperar el identificador del miembro **hMenu** de la estructura [**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) mientras se procesa el mensaje [**de \_ creación de WM**](/windows/desktop/winmsg/wm-create) .

En los ejemplos siguientes, donde *hwndControl* es el identificador de la ventana de control y CN \_ VALUECHANGED es una definición de notificación personalizada, se muestran las dos formas de enviar una notificación específica del control.


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



Tenga en cuenta que la estructura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) puede formar parte de una estructura mayor definida por el control que contiene información adicional. En el ejemplo, los valores antiguos y nuevos del control pueden estar contenidos en esta estructura. (Estas estructuras extendidas se usan con muchas notificaciones estándar; por ejemplo, vea [LVN \_ INSERTITEM](lvn-insertitem.md), que usa la estructura [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) ).

## <a name="accessibility"></a>Accesibilidad

Todos los controles comunes son compatibles con Microsoft Active Accessibility (MSAA), que permite el acceso mediante programación a aplicaciones de tecnología accesible como lectores de pantalla. MSAA también habilita la automatización de la interfaz de usuario, una tecnología más reciente, para interactuar con los controles.

Los controles personalizados deben implementar la interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) (para admitir MSAA) o las interfaces de automatización de la interfaz de usuario, o ambas. De lo contrario, los productos de tecnología accesible podrán obtener únicamente información muy limitada sobre la ventana de control, no tendrán acceso a las propiedades del control y no podrán desencadenar eventos en el control.

Para obtener más información sobre cómo lograr el control accesible, vea [API de automatización de Windows](/windows/desktop/WinAuto/windows-automation-api-portal).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Vista**
</dt> <dt>

[Referencia de control general](common-control-reference.md)
</dt> <dt>

[Personalizar la apariencia de un control mediante el dibujo personalizado](custom-draw.md)
</dt> <dt>

[Mensajes de control](control-messages.md)
</dt> <dt>

[Usar estilos visuales con controles de Owner-Drawn](using-visual-styles.md)
</dt> </dl>

 

 