---
title: Acerca de las hojas de propiedades
description: Una hoja de propiedades es una ventana que permite al usuario ver y editar las propiedades de un elemento.
ms.assetid: 93676a64-7980-48cd-8615-23b14a118e1c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3256959b588e2109740033692c0c528889fc939f
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/19/2021
ms.locfileid: "105649463"
---
# <a name="about-property-sheets"></a>Acerca de las hojas de propiedades

Una *hoja de propiedades* es una ventana que permite al usuario ver y editar las propiedades de un elemento. Por ejemplo, una aplicación de hoja de cálculo puede utilizar una hoja de propiedades para permitir al usuario establecer las propiedades de fuente y borde de una celda, o para ver y establecer las propiedades de un dispositivo, como una unidad de disco, una impresora o un mouse.

En esta sección se tratan los temas siguientes.

-   [Aspectos básicos de la hoja de propiedades](#property-sheet-basics)
-   [Cuadros de diálogo de hoja de propiedades](#property-sheet-dialog-boxes)
-   [Páginas](#pages)
-   [Creación de hojas de propiedades](#property-sheet-creation)
-   [Agregar y quitar páginas](#adding-and-removing-pages)
-   [Título y etiquetas de página de la hoja de propiedades](#property-sheet-title-and-page-labels)
-   [Activación de página](#page-activation)
-   [Botón ayuda](#help-button)
    -   [Quitar el botón ayuda de la barra de título](#removing-the-caption-bar-help-button)
-   [Botones aceptar, cancelar y aplicar](#ok-cancel-and-apply-buttons)
-   [Asistentes](#wizards)

## <a name="property-sheet-basics"></a>Aspectos básicos de la hoja de propiedades

Para implementar hojas de propiedades en la aplicación, incluya el archivo de encabezado Prsht. h en el proyecto. Prsht. h contiene todos los identificadores utilizados con hojas de propiedades.

Una hoja de propiedades contiene una o varias ventanas secundarias superpuestas denominadas páginas, cada una de las cuales contiene ventanas de control para establecer un grupo de propiedades relacionadas. Por ejemplo, una página puede contener los controles para establecer las propiedades de fuente de un elemento, incluido el estilo de tipo, el tamaño de punto, el color, etc. Cada página tiene una pestaña que el usuario puede seleccionar para devolver la página al primer plano de la hoja de propiedades. Por ejemplo, la aplicación Date-Time panel de control muestra la siguiente hoja de propiedades.

![captura de pantalla de una hoja de propiedades con dos pestañas, una de las cuales muestra un reloj y un control de calendario mensual](images/propsheet1.png)

Una hoja de propiedades estándar con varias páginas con pestañas permite al usuario el acceso aleatorio a todas las propiedades. Si es más adecuado que las propiedades se establezcan en secuencia, puede usar un [Asistente](#wizards).

## <a name="property-sheet-dialog-boxes"></a>Cuadros de diálogo de hoja de propiedades

En realidad, una hoja de propiedades y las páginas que contiene son cuadros de diálogo. La hoja de propiedades es un cuadro de diálogo definido por el sistema que administra las páginas y proporciona un contenedor común para ellas. Un cuadro de diálogo de hoja de propiedades puede ser modal o no modal. Incluye un marco, una barra de título y cuatro botones: **Aceptar**, **Cancelar**, **aplicar** y, opcionalmente, **ayuda**. Los procedimientos del cuadro de diálogo para las páginas reciben códigos de notificación en forma de mensajes de notificación de [**WM \_**](wm-notify.md) cuando el usuario hace clic en los botones.

> [!NOTE]  
> No toda la información de esta sección se aplica a los asistentes, que tienen una apariencia y un comportamiento algo distintos. Por ejemplo, los asistentes tienen un conjunto diferente de botones y ninguna pestaña. Para obtener más información, vea [crear asistentes](wizards.md).

Cada página de una hoja de propiedades es un cuadro de diálogo no modal definido por la aplicación que administra las ventanas de control utilizadas para ver y editar las propiedades de un elemento. Proporcione la plantilla de cuadro de diálogo que se usa para crear cada página, así como el procedimiento de cuadro de diálogo que administra los controles y establece las propiedades del elemento correspondiente.

Una hoja de propiedades envía códigos de notificación al procedimiento de cuadro de diálogo de una página cuando la página obtiene o pierde la activación y cuando el usuario hace clic en el botón **Aceptar**, **Cancelar**, **aplicar** o **ayuda** . Las notificaciones se envían en forma de mensajes [**de \_ notificación de WM**](wm-notify.md) . El parámetro *lParam* es la dirección de una estructura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que incluye el identificador de ventana del cuadro de diálogo de la hoja de propiedades.

Algunos códigos de notificación requieren una página para devolver **true** o **false** en respuesta al mensaje [**de \_ notificación de WM**](wm-notify.md) . Para ello, la página debe usar la función [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) para establecer el valor de **DWL \_ MSGRESULT** para el cuadro de diálogo de página en **true** o **false**.

## <a name="pages"></a>Páginas

Una hoja de propiedades debe contener al menos una página, pero no puede contener más del valor de **MAXPROPPAGES** tal y como se define en los archivos de encabezado de Windows. Cada página tiene un índice basado en cero que la hoja de propiedades asigna según el orden en que se agrega la página a la hoja de propiedades. Los índices se utilizan en los mensajes que se envían a la hoja de propiedades.

Una página de propiedades puede contener un cuadro de diálogo anidado. Si lo hace, debe incluir el estilo [**WS \_ ex \_ CONTROLPARENT**](/windows/desktop/winmsg/extended-window-styles) para el cuadro de diálogo de nivel superior y llamar a la función [**IsDialogMessage**](/windows/desktop/api/winuser/nf-winuser-isdialogmessagea) con el identificador del cuadro de diálogo primario. Esto garantiza que el usuario puede utilizar las teclas de teclas y las teclas de navegación del cuadro de diálogo para desplazar el foco a los controles del cuadro de diálogo anidado.

Cada página tiene un icono y una etiqueta correspondientes. La hoja de propiedades crea una pestaña para cada página y muestra el icono y la etiqueta en la pestaña. Se espera que todas las páginas de la hoja de propiedades utilicen una fuente que no sea negrita. Para asegurarse de que la fuente no está en negrita, especifique el estilo **\_ 3DLOOK de DS** en la plantilla de cuadro de diálogo.

El procedimiento de cuadro de diálogo de una página no debe llamar a la función [**EndDialog**](/windows/desktop/api/winuser/nf-winuser-enddialog) . Al hacerlo, se destruirá toda la hoja de propiedades, no solo la página.

El tamaño mínimo de una página de la hoja de propiedades es 212 unidades de cuadro de diálogo horizontalmente y 114 unidades de cuadro de diálogo verticalmente. Si un cuadro de diálogo de página es menor que este, la página se ampliará hasta que cumpla el tamaño mínimo. El archivo de encabezado Prsht. h contiene tres conjuntos de tamaños recomendados para las páginas de la hoja de propiedades, como se muestra en la tabla siguiente.

|  Tamaño                |   Descripción                                                   |
|----------------------|-----------------------------------------------------------------|
| **PROP \_ SM \_ CXDLG**  | Ancho, en unidades de cuadro de diálogo, de una pequeña página de hoja de propiedades.         |
| **PROP \_ SM \_ CYDLG**  | Alto, en unidades de cuadro de diálogo, de una pequeña página de hoja de propiedades.        |
| **PROP \_ Med \_ CXDLG** | Ancho, en unidades de cuadro de diálogo, de una página de hoja de propiedades de tamaño medio.  |
| **PROP \_ Med \_ CYDLG** | Alto, en unidades de cuadro de diálogo, de una página de hoja de propiedades de tamaño medio. |
| **PROP \_ LG \_ CXDLG**  | Ancho, en unidades de cuadro de diálogo, de una página grande de la hoja de propiedades.         |
| **PROP \_ LG \_ CYDLG**  | Alto, en unidades de cuadro de diálogo, de una página grande de la hoja de propiedades.        |

El uso de estos tamaños recomendados le ayudará a garantizar la coherencia visual entre la aplicación y otras aplicaciones de Microsoft Windows.

En el editor de recursos de Microsoft Visual Studio, puede crear una página del tamaño adecuado en el cuadro de diálogo **Agregar recurso** . Expanda el nodo cuadro de diálogo y seleccione **IDD \_ PropPage \_ Large**, **IDD \_ PropPage \_ Medium** o **IDD \_ PropPage \_ Small**.

La hoja de propiedades se ajusta automáticamente para adaptarse a la página más grande.

## <a name="property-sheet-creation"></a>Creación de hojas de propiedades

Antes de crear una hoja de propiedades, debe definir una o más páginas. Esto implica rellenar una estructura [**PROPSHEETPAGE**](pss-propsheetpage.md) con información sobre la página (su icono, etiqueta, plantilla de cuadro de diálogo, procedimiento de cuadro de diálogo, etc.) y, a continuación, especificar la dirección de la estructura en una llamada a la función [**CreatePropertySheetPage**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea) . La función devuelve un identificador al tipo HPROPSHEETPAGE que identifica la página de forma única.

Para crear una hoja de propiedades, especifique la dirección de una estructura [**PROPSHEETHEADER**](pss-propsheetheader.md) en una llamada a la función [**hoja**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) . La estructura define el icono y el título de la hoja de propiedades y también incluye la dirección de una matriz de identificadores HPROPSHEETPAGE que se obtienen mediante [**CreatePropertySheetPage**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea). Cuando **hoja** crea la hoja de propiedades, incluye las páginas identificadas en la matriz. Las páginas aparecen en la hoja de propiedades en el mismo orden en que se encuentran en la matriz.

Otra manera de asignar páginas a una hoja de propiedades consiste en especificar una matriz de estructuras [**PROPSHEETPAGE**](pss-propsheetpage.md) en lugar de una matriz de identificadores de **HPROPSHEETPAGE** . En este caso, [**hoja**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) crea identificadores para las páginas antes de agregarlas a la hoja de propiedades.

Cuando se crea una página, el procedimiento del cuadro de diálogo recibe un mensaje de [**\_ INITDIALOG de WM**](/windows/desktop/dlgbox/wm-initdialog) . El parámetro *lParam* del mensaje es un puntero a una copia de la estructura [**PROPSHEETPAGE**](pss-propsheetpage.md) que se define cuando se crea la página. En concreto, cuando se crea una página, se puede usar el miembro **lParam** de la estructura para pasar información definida por la aplicación al procedimiento del cuadro de diálogo. A excepción del miembro **lParam** , esta estructura debe tratarse como de solo lectura. La modificación de cualquier cosa que no sea **lParam** tendrá consecuencias imprevisibles.

Cuando el sistema pasa posteriormente una copia de la estructura [**PROPSHEETPAGE**](pss-propsheetpage.md) de la página a la aplicación, utiliza el mismo puntero. Se pasarán los cambios a la estructura. Dado que el sistema omite el miembro **lParam** , se puede modificar para enviar información a otras partes de la aplicación. Por ejemplo, puede usar **lParam** para pasar información a la función de devolución de llamada [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) de la página.

[**Hoja**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) establece automáticamente el tamaño y la posición inicial de una hoja de propiedades. La posición se basa en la posición de la ventana propietaria y el tamaño se basa en la página más grande especificada en la matriz de páginas cuando se creó la hoja de propiedades. Si desea que las páginas coincidan con el ancho de los cuatro botones en la parte inferior de la hoja de propiedades, establezca el ancho de la página más ancha en 190 unidades de cuadro de diálogo.

El tamaño de una hoja de propiedades se calcula a partir de las propiedades *width* y *height* de la plantilla de cuadro de diálogo en el archivo de recursos. Consulte recurso de [**cuadro de diálogo**](/windows/desktop/menurc/dialog-resource) o [**recurso de DIALOGEX**](/windows/desktop/menurc/dialogex-resource) para obtener más detalles. Sin embargo, tenga en cuenta que, por motivos de compatibilidad, las dimensiones se calculan en relación con la fuente de MS Shell Dlg en lugar de la fuente usada por la página. Si diseña una página que usa otra fuente, se puede usar una de las sugerencias siguientes.

-   Ajuste las dimensiones de la plantilla de cuadro de diálogo para compensar la diferencia de tamaño entre la fuente MS Shell Dlg y la fuente que la página usa realmente. Por ejemplo, si elige una fuente que sea dos veces más ancha que MS Shell Dlg, establezca la propiedad width de la plantilla de cuadro de diálogo en el doble del uso normal.
-   Use una plantilla de [**DIALOGEX**](/windows/desktop/menurc/dialogex-resource) y establezca el estilo de cuadro de diálogo **\_ SHELLFONT de DS** . En ese caso, el administrador de la hoja de propiedades interpreta las dimensiones de la plantilla de cuadro de diálogo en relación con la fuente utilizada por la plantilla de cuadro de diálogo.

## <a name="adding-and-removing-pages"></a>Agregar y quitar páginas

Después de crear una hoja de propiedades, una aplicación puede Agregar una página al final del conjunto de páginas existente mediante el envío de un mensaje de [**PSM \_**](psm-addpage.md) . Para insertar una página entre las páginas existentes, envíe un mensaje de [**PropSheet \_ InsertPage**](/windows/desktop/api/Prsht/nf-prsht-propsheet_insertpage) . Tenga en cuenta que el tamaño de la hoja de propiedades no puede cambiar una vez que se ha creado. Las páginas agregadas o insertadas no deben ser mayores que la página más grande que se encuentra actualmente en la hoja de propiedades. Para quitar una página, envíe un mensaje de [**PSM \_ REMOVEPAGE**](psm-removepage.md) .

Cuando se define una página, se puede especificar la dirección de una función de devolución de llamada [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) que la hoja de propiedades llama cuando se crea o se quita la página. El uso de *PropSheetPageProc* le ofrece la oportunidad de realizar operaciones de inicialización y limpieza para páginas individuales.

> [!NOTE]  
> Se producen varios mensajes y una llamada de función mientras la hoja de propiedades manipula la lista de páginas. Mientras se realiza esta acción, el intento de modificar la lista de páginas tendrá resultados imprevisibles. No agregue, inserte o quite páginas en su implementación de [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka)o mientras controla las siguientes notificaciones y mensajes de Windows.
>
> -   [PSN \_ aplicar](psn-apply.md)
> -   [PSN \_ KILLACTIVE](psn-killactive.md)
> -   [restablecimiento de PSN \_](psn-reset.md)
> -   [PSN \_ SETACTIVE](psn-setactive.md)
> -   [PSN \_ WIZBACK](psn-wizback.md)
> -   [PSN \_ WIZNEXT](psn-wiznext.md)
> -   [**INITDIALOG de WM \_**](/windows/desktop/dlgbox/wm-initdialog)
> -   [**destrucción de WM \_**](/windows/desktop/winmsg/wm-destroy)

Si es necesario modificar una página de hoja de propiedades mientras se controla uno de estos mensajes o mientras [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) está en funcionamiento, publique un mensaje de Windows privado. La aplicación no recibirá ese mensaje hasta que el administrador de la hoja de propiedades haya finalizado sus tareas, en cuyo momento será seguro modificar la lista de páginas.

Cuando se destruye una hoja de propiedades, se destruyen automáticamente todas las páginas que se han agregado a ella. Las páginas se destruyen en orden inverso al especificado en la matriz utilizada para crear las páginas. Para destruir una página creada por la función [**CreatePropertySheetPage**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea) pero que no se agregó a la hoja de propiedades, utilice la función [**DestroyPropertySheetPage**](/windows/desktop/api/Prsht/nf-prsht-destroypropertysheetpage) .

## <a name="property-sheet-title-and-page-labels"></a>Título y etiquetas de página de la hoja de propiedades

El título de una hoja de propiedades se especifica en la estructura [**PROPSHEETHEADER**](pss-propsheetheader.md) utilizada para crear la hoja de propiedades. Si el miembro **dwFlags** incluye el **valor \_ PROPTITLE de PSH** , la hoja de propiedades agrega el sufijo "Properties" o el prefijo "Properties for", dependiendo de la versión. Puede cambiar el título después de crear una hoja de propiedades mediante el mensaje [**\_ SETTITLE de PSM**](psm-settitle.md) . En un asistente de Aero, este mensaje se puede usar para cambiar dinámicamente el título de una página interior.

De forma predeterminada, una hoja de propiedades utiliza la cadena de nombre especificada en la plantilla de cuadro de diálogo como etiqueta de una página. Puede invalidar la cadena de nombre incluyendo el valor de **PSP \_ USETITLE** en el miembro **DwFlags** de la estructura [**PROPSHEETPAGE**](pss-propsheetpage.md) que define la página. Cuando se especifica **PSP \_ USETITLE** , el miembro **pszTitle** debe contener la dirección de la cadena de etiqueta de la página.

## <a name="page-activation"></a>Activación de página

Una hoja de propiedades solo puede tener una página activa a la vez. La página que tiene la activación está en primer plano de la pila de páginas superpuestas. El usuario activa una página seleccionando su pestaña; una aplicación activa una página mediante el mensaje [**\_ SETCURSEL de PSM**](psm-setcursel.md) .

La hoja de propiedades envía el código de notificación [PSN \_ KILLACTIVE](psn-killactive.md) a la página que está a punto de perder la activación. En respuesta, la página debe validar cualquier cambio que haya realizado el usuario en la página. Si la página requiere una entrada adicional por el usuario antes de perder la activación, utilice la función [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) para establecer el valor de **DWL \_ MSGRESULT** de la página en **true**. Además, la página debe mostrar un cuadro de mensaje que describa el problema y proporcione la acción recomendada. Establezca **DWL \_ MSGRESULT** en **false** cuando sea correcto perder la activación.

Antes de que la página que obtiene la activación esté visible, la hoja de propiedades envía el código de notificación [PSN \_ SETACTIVE](psn-setactive.md) a la página. La página debe responder inicializando sus ventanas de control.

## <a name="help-button"></a>Botón ayuda

Las hojas de propiedades pueden mostrar dos botones de ayuda: un botón de ayuda de la hoja de propiedades que se muestra en la parte inferior del marco, junto a los botones **Aceptar** / **Cancelar** / **aplicación** y un botón de barra de título estándar que proporciona ayuda contextual.

El botón ayuda de la hoja de propiedades es opcional y se puede habilitar en una página por página. Para mostrar el botón ayuda de la hoja de propiedades de una o varias páginas:

-   Establezca la marca de **\_ TieneAyuda de PSH** en el miembro **DwFlags** de la estructura [**PROPSHEETHEADER**](pss-propsheetheader.md) de la hoja de propiedades.
-   En cada página que muestre un botón ayuda, establezca la marca **PSP \_ TieneAyuda** en el miembro **DwFlags** de la estructura [**PROPSHEETPAGE**](pss-propsheetpage.md) de la página.

Cuando el usuario hace clic en el botón ayuda, la página activa recibe un código de notificación de [ \_ ayuda de PSN](psn-help.md) . La página debe responder mostrando información de ayuda, normalmente mediante una llamada a la función [**WinHelp**](/windows/desktop/api/winuser/nf-winuser-winhelpa) .

### <a name="removing-the-caption-bar-help-button"></a>Quitar el botón ayuda de la barra de título

El botón ayuda de la barra de título se muestra de forma predeterminada, por lo que siempre está disponible la ayuda contextual para los botones Aceptar/Cancelar/aplicar. Sin embargo, este botón se puede quitar, si es necesario. Para quitar el botón ayuda de la barra de título de la hoja de propiedades:

-   En el caso de las versiones de los controles comunes anteriores a la [versión 5,80](common-control-versions.md), debe implementar una [**función de devolución de llamada de hoja de propiedades**](/windows/desktop/api/Prsht/nc-prsht-pfnpropsheetcallback).
-   Para la [versión 5,80](common-control-versions.md) y posteriores de los controles comunes, puede simplemente establecer la \_ marca PSH NOCONTEXTHELP en el miembro **DwFlags** de la estructura [**PROPSHEETHEADER**](pss-propsheetheader.md) de la hoja de propiedades. Sin embargo, si necesita compatibilidad con versiones anteriores de las versiones de control comunes anteriores, debe implementar la función de devolución de llamada.

Para implementar una función de devolución de llamada de la hoja de propiedades que quita el botón ayuda de la barra de título:

-   Establezca la marca **PSH \_ USECALLBACK** en el miembro **DwFlags** de la estructura [**PROPSHEETHEADER**](pss-propsheetheader.md) de la hoja de propiedades.
-   Establezca el miembro **pfnCallBack** de la estructura [**PROPSHEETHEADER**](pss-propsheetheader.md) para que apunte a la función de devolución de llamada.
-   Implemente la función de devolución de llamada. Cuando esta función recibe el mensaje **PSCB \_ precreate** , también recibirá un puntero a la plantilla de cuadro de diálogo de la hoja de propiedades. Quite el **estilo \_ CONTEXTHELP de DS** de esta plantilla.

En el ejemplo siguiente se muestra cómo implementar este tipo de función de devolución de llamada:

```cpp
int CALLBACK RemoveContextHelpProc(HWND hwnd, UINT message, LPARAM lParam)
{
    switch (message) 
    {
    case PSCB_PRECREATE:
        // Remove the DS_CONTEXTHELP style from the
        // dialog box template
        if (((LPDLGTEMPLATEEX)lParam)->signature ==    
           0xFFFF)
           {
            ((LPDLGTEMPLATEEX)lParam)->style 
            &= ~DS_CONTEXTHELP;
        }
        else {
            ((LPDLGTEMPLATE)lParam)->style 
            &= ~DS_CONTEXTHELP;
        }
        return TRUE;
    }
    return TRUE;
}
```

Si no se define la estructura [**DLGTEMPLATEEX**](/windows/desktop/dlgbox/dlgtemplateex) , incluya la siguiente declaración:

```cpp
#include <pshpack1.h>

typedef struct DLGTEMPLATEEX
{
    WORD dlgVer;
    WORD signature;
    DWORD helpID;
    DWORD exStyle;
    DWORD style;
    WORD cDlgItems;
    short x;
    short y;
    short cx;
    short cy;
} DLGTEMPLATEEX, *LPDLGTEMPLATEEX;

#include <poppack.h>
```

## <a name="ok-cancel-and-apply-buttons"></a>Botones aceptar, cancelar y aplicar

Los botones **Aceptar** y **aplicar** son similares; ambos dirigen las páginas de la hoja de propiedades para validar y aplicar los cambios de propiedad que ha realizado el usuario. La única diferencia es que al hacer clic en el botón **Aceptar** , la hoja de propiedades se destruirá una vez aplicados los cambios.

Cuando el usuario hace clic en el botón **Aceptar** o **aplicar** , la hoja de propiedades envía una notificación de [PSN \_ KILLACTIVE](psn-killactive.md) a la página activa, lo que le permite validar los cambios del usuario. Si los cambios son válidos, la página debe llamar a la función [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) con el valor de **DWL \_ MSGRESULT** establecido en **false**. Si los cambios del usuario no son válidos, la página debe establecer **DWL \_ MSGRESULT** en **true** y mostrar un cuadro de diálogo que informa al usuario del problema. La página permanece activa hasta que se establece el valor de **DWL \_ MSGRESULT** en **false** en respuesta a un \_ mensaje KILLACTIVE de PSN.

Después de que una página responda a una notificación de [ \_ KILLACTIVE de PSN](psn-killactive.md) al establecer **DWL \_ MSGRESULT** en **false**, la hoja de propiedades enviará una notificación [PSN \_ aplicar](psn-apply.md) a cada página. Cuando una página recibe esta notificación, debe aplicar las nuevas propiedades al elemento correspondiente. Para indicar a la hoja de propiedades que los cambios son válidos para la página, llame a [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) con **DWL \_ MSGRESULT** establecido en **PSNRET \_ NoError**. Si los cambios no son válidos para la página, devuelva un error. Al hacerlo, se evita que la hoja de propiedades se destruya y se devuelva el foco a la página que recibió la notificación de aplicación de PSN \_ o a la página que tenía el foco cuando se presionó el botón **aplicar** . Para devolver un error e indicar la página que recibirá el foco, establezca **DWL \_ MSGRESULT** en uno de los valores siguientes.

-   **PSNRET \_ NO válido**. La hoja de propiedades no se destruirá y se devolverá el foco a esta página.
-   **PSNRET \_ \_NOCHANGEPAGE no válido**. La hoja de propiedades no se destruirá y el foco se devolverá a la página que tenía el foco cuando se presionó el botón.

Una aplicación puede usar el mensaje [**PSM \_ Apply**](psm-apply.md) para simular la selección del botón **aplicar** .

Inicialmente, el botón **aplicar** está deshabilitado cuando se activa una página, lo que indica que aún no hay ningún cambio en la propiedad que aplicar. Cuando la página recibe la entrada a través de uno de sus controles que indica que el usuario ha editado una propiedad, la página debe enviar el mensaje de [**\_ cambio de PSM**](psm-changed.md) a la hoja de propiedades. El mensaje hace que la hoja de propiedades habilite el botón **aplicar** . Si el usuario hace clic en el botón **aplicar** o **Cancelar** , la página debe reinicializar sus controles y, a continuación, enviar el mensaje [**PSM \_ sin cambios**](psm-unchanged.md) para deshabilitar de nuevo el botón **aplicar** .

A veces, el botón **aplicar** hace que una página realice un cambio en una hoja de propiedades y el cambio no se puede deshacer. Cuando esto sucede, la página debe enviar el mensaje de [**PSM \_ CANCELTOCLOSE**](psm-canceltoclose.md) a la hoja de propiedades. El mensaje hace que la hoja de propiedades cambie el texto del botón **Aceptar** a "cerrar", lo que indica que los cambios aplicados no se pueden cancelar.

A veces, una página realiza un cambio en la configuración del sistema que requiere que se reinicie Windows o que el sistema se reinicie antes de que el cambio surta efecto. Después de realizar este cambio, una página debe enviar el mensaje [**PSM \_ RESTARTWINDOWS**](psm-restartwindows.md) o [**PSM \_ REBOOTSYSTEM**](psm-rebootsystem.md) a la hoja de propiedades. Estos mensajes hacen que la función [**hoja**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) devuelva el valor de **identificador \_ PSRESTARTWINDOWS** o **ID \_ PSREBOOTSYSTEM** después de la destrucción de la hoja de propiedades.

Cuando un usuario hace clic en el botón **Cancelar** , la hoja de propiedades envía el código de notificación de [ \_ restablecimiento de PSN](psn-reset.md) a todas las páginas, lo que indica que la hoja de propiedades está a punto de ser destruida. Una página debe utilizar la notificación para realizar operaciones de limpieza.

## <a name="wizards"></a>Asistentes

Un asistente es un tipo especial de hoja de propiedades. Los asistentes están diseñados para presentar las páginas de una en una en una secuencia controlada por la aplicación. En lugar de seleccionar un grupo de páginas al hacer clic en una pestaña, los usuarios navegan hacia delante y hacia atrás por la secuencia, una página a la vez, haciendo clic en los botones. Por ejemplo, en la siguiente captura de pantalla se muestra la Página principal del Asistente para agregar hardware:

![captura de pantalla de la Página principal de un asistente](images/wizard97.png)

En la captura de pantalla siguiente se muestra la primera página de un asistente de Aero, el nuevo estilo introducido en Windows Vista.

![captura de pantalla de la primera página de un asistente de Aero](images/wizardaero.png)

Vea [crear asistentes](wizards.md) para obtener una descripción completa de los asistentes.
