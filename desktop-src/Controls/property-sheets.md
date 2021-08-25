---
title: Acerca de las hojas de propiedades
description: Una hoja de propiedades es una ventana que permite al usuario ver y editar las propiedades de un elemento.
ms.assetid: 93676a64-7980-48cd-8615-23b14a118e1c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 241d5ed4299a0771d9f2b4df6f17929474c7f4868edf7bcaf1ade5baa7e572b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119914720"
---
# <a name="about-property-sheets"></a>Acerca de las hojas de propiedades

Una *hoja de* propiedades es una ventana que permite al usuario ver y editar las propiedades de un elemento. Por ejemplo, una aplicación de hoja de cálculo puede usar una hoja de propiedades para permitir al usuario establecer las propiedades de fuente y borde de una celda o para ver y establecer las propiedades de un dispositivo, como una unidad de disco, una impresora o un mouse.

En esta sección se tratan los temas siguientes.

-   [Conceptos básicos de la hoja de propiedades](#property-sheet-basics)
-   [Cuadros de diálogo de hoja de propiedades](#property-sheet-dialog-boxes)
-   [Páginas](#pages)
-   [Creación de la hoja de propiedades](#property-sheet-creation)
-   [Agregar y quitar páginas](#adding-and-removing-pages)
-   [Etiquetas de página y título de hoja de propiedades](#property-sheet-title-and-page-labels)
-   [Activación de página](#page-activation)
-   [Botón Ayuda](#help-button)
    -   [Quitar el botón ayuda de la barra de subtítulos](#removing-the-caption-bar-help-button)
-   [Botones Aceptar, Cancelar y Aplicar](#ok-cancel-and-apply-buttons)
-   [Asistentes](#wizards)

## <a name="property-sheet-basics"></a>Conceptos básicos de la hoja de propiedades

Para implementar hojas de propiedades en la aplicación, incluya el archivo de encabezado Prsht.h en el proyecto. Prsht.h contiene todos los identificadores usados con las hojas de propiedades.

Una hoja de propiedades contiene una o varias ventanas secundarias superpuestas denominadas páginas, cada una de las que contiene ventanas de control para establecer un grupo de propiedades relacionadas. Por ejemplo, una página puede contener los controles para establecer las propiedades de fuente de un elemento, incluido el estilo de tipo, el tamaño de punto, el color, y así sucesivamente. Cada página tiene una pestaña que el usuario puede seleccionar para poner la página en primer plano de la hoja de propiedades. Por ejemplo, la aplicación Date-Time panel de control muestra la siguiente hoja de propiedades.

![captura de pantalla de una hoja de propiedades con dos pestañas, una de las cuales muestra un reloj y un control de calendario mensual](images/propsheet1.png)

Una hoja de propiedades estándar con varias páginas con pestañas permite al usuario el acceso aleatorio a todas las propiedades. Si es más adecuado tener propiedades establecidas en secuencia, puede usar un [asistente](#wizards).

## <a name="property-sheet-dialog-boxes"></a>Cuadros de diálogo de hoja de propiedades

Una hoja de propiedades y las páginas que contiene son realmente cuadros de diálogo. La hoja de propiedades es un cuadro de diálogo definido por el sistema que administra las páginas y proporciona un contenedor común para ellas. Un cuadro de diálogo de hoja de propiedades puede ser modal o no modal. Incluye un marco, una barra de título y cuatro botones: **Aceptar,** **Cancelar,** **Aplicar** y (opcionalmente) **Ayuda**. Los procedimientos de cuadro de diálogo de las páginas reciben códigos de notificación en forma de [**mensajes \_ WM NOTIFY**](wm-notify.md) cuando el usuario hace clic en los botones.

> [!NOTE]  
> No toda la información de esta sección se aplica a los asistentes, que tienen una apariencia y un comportamiento ligeramente diferentes. Por ejemplo, los asistentes tienen un conjunto diferente de botones y ninguna pestaña. Para obtener más información, vea [Crear asistentes.](wizards.md)

Cada página de una hoja de propiedades es un cuadro de diálogo modeless definido por la aplicación que administra las ventanas de control utilizadas para ver y editar las propiedades de un elemento. Proporcione la plantilla de cuadro de diálogo utilizada para crear cada página, así como el procedimiento de cuadro de diálogo que administra los controles y establece las propiedades del elemento correspondiente.

Una hoja de propiedades envía códigos de notificación al procedimiento del cuadro de diálogo de una página cuando la página  está ganando o pierde la activación y cuando el usuario hace clic en el botón **Aceptar,** **Cancelar,** Aplicar o Ayuda. Las notificaciones se envían en forma de mensajes [**WM \_ NOTIFY.**](wm-notify.md) El *parámetro lParam* es la dirección de una estructura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que incluye el identificador de ventana en el cuadro de diálogo de la hoja de propiedades.

Algunos códigos de notificación requieren que una página devuelva **TRUE** o **FALSE** en respuesta al [**mensaje WM \_ NOTIFY.**](wm-notify.md) Para ello, la página debe usar la función [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) para establecer el valor **\_ MSGRESULT** de DWL del cuadro de diálogo de página en **TRUE** o **FALSE.**

## <a name="pages"></a>Páginas

Una hoja de propiedades debe contener al menos una página, pero no puede contener más que el valor de **MAXPROPPAGES,** tal como se define en los archivos de encabezado Windows archivo. Cada página tiene un índice de base cero que la hoja de propiedades asigna según el orden en que se agrega la página a la hoja de propiedades. Los índices se usan en los mensajes que se envían a la hoja de propiedades.

Una página de propiedades puede contener un cuadro de diálogo anidado. Si es así, debe incluir el estilo [**WS \_ EX \_ CONTROLPARENT**](/windows/desktop/winmsg/extended-window-styles) para el cuadro de diálogo de nivel superior y llamar a la función [**IsDialogMessage**](/windows/desktop/api/winuser/nf-winuser-isdialogmessagea) con el identificador para el cuadro de diálogo primario. Esto garantiza que el usuario puede usar mnemonics y las teclas de navegación del cuadro de diálogo para mover el foco a los controles del cuadro de diálogo anidado.

Cada página tiene un icono y una etiqueta correspondientes. La hoja de propiedades crea una pestaña para cada página y muestra el icono y la etiqueta en la pestaña. Se espera que todas las páginas de hoja de propiedades usen una fuente nobold. Para asegurarse de que la fuente no está en negrita, especifique el estilo **DS \_ 3DLOOK** en la plantilla de cuadro de diálogo.

El procedimiento de cuadro de diálogo de una página no debe llamar a [**la función EndDialog.**](/windows/desktop/api/winuser/nf-winuser-enddialog) Si lo hace, destruirá toda la hoja de propiedades, no solo la página.

El tamaño mínimo de una página de hoja de propiedades es 212 unidades de diálogo horizontalmente y 114 unidades de diálogo verticalmente. Si un cuadro de diálogo de página es menor que este, la página se ampliará hasta que cumpla el tamaño mínimo. El archivo de encabezado Prsht.h contiene tres conjuntos de tamaños recomendados para las páginas de hoja de propiedades, como se muestra en la tabla siguiente.

|  Size                |   Descripción                                                   |
|----------------------|-----------------------------------------------------------------|
| **PROP \_ SM \_ CXDLG**  | Ancho, en unidades de diálogo, de una página de hoja de propiedades pequeña.         |
| **PROP \_ SM \_ CYDLG**  | Alto, en unidades de diálogo, de una página de hoja de propiedades pequeña.        |
| **PROP \_ MED \_ CXDLG** | Ancho, en unidades de diálogo, de una página de hoja de propiedades de tamaño medio.  |
| **PROP \_ CG \_ CYDLG** | Alto, en unidades de diálogo, de una página de hoja de propiedades de tamaño medio. |
| **PROP \_ LG \_ CXDLG**  | Ancho, en unidades de diálogo, de una página de hoja de propiedades grande.         |
| **PROP \_ LG \_ CYDLG**  | Alto, en unidades de diálogo, de una página de hoja de propiedades grande.        |

El uso de estos tamaños recomendados ayudará a garantizar la coherencia visual entre la aplicación y otras aplicaciones Windows Microsoft.

En el Microsoft Visual Studio de recursos, puede crear una página con el tamaño adecuado en el **cuadro de diálogo** Agregar recurso. Expanda el nodo Cuadro de diálogo y **seleccione IDD \_ PROPPAGE \_ LARGE**, **IDD \_ PROPPAGE \_ MEDIUM** o **IDD \_ PROPPAGE \_ SMALL**.

El tamaño de la hoja de propiedades se ajusta automáticamente para dar cabida a la página más grande.

## <a name="property-sheet-creation"></a>Creación de la hoja de propiedades

Antes de crear una hoja de propiedades, debe definir una o varias páginas. Esto implica rellenar una estructura [**PROPSHEETPAGE**](pss-propsheetpage.md) con información sobre la página (su icono, etiqueta, plantilla de cuadro de diálogo, procedimiento de cuadro de diálogo, y así sucesivamente) y, a continuación, especificar la dirección de la estructura en una llamada a la [**función CreatePropertySheetPage.**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea) La función devuelve un identificador al tipo HPROPSHEETPAGE que identifica de forma única la página.

Para crear una hoja de propiedades, especifique la dirección de una [**estructura PROPSHEETHEADER**](pss-propsheetheader.md) en una llamada a la [**función PropertySheet.**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) La estructura define el icono y el título de la hoja de propiedades y también incluye la dirección de una matriz de identificadores HPROPSHEETPAGE que se obtienen mediante [**CreatePropertySheetPage**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea). Cuando **PropertySheet** crea la hoja de propiedades, incluye las páginas identificadas en la matriz. Las páginas aparecen en la hoja de propiedades en el mismo orden en que están contenidas en la matriz.

Otra manera de asignar páginas a una hoja de propiedades es especificar una matriz de estructuras [**PROPSHEETPAGE**](pss-propsheetpage.md) en lugar de una matriz de **identificadores HPROPSHEETPAGE.** En este caso, [**PropertySheet crea**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) identificadores para las páginas antes de agregarlos a la hoja de propiedades.

Cuando se crea una página, su procedimiento de cuadro de diálogo recibe un [**mensaje \_ WM INITDIALOG.**](/windows/desktop/dlgbox/wm-initdialog) El parámetro *lParam* del mensaje es un puntero a una copia de la estructura [**PROPSHEETPAGE**](pss-propsheetpage.md) que se define cuando se crea la página. En concreto, cuando se crea una página, el miembro **lParam** de la estructura se puede usar para pasar información definida por la aplicación al procedimiento del cuadro de diálogo. A excepción del **miembro lParam,** esta estructura debe tratarse como de solo lectura. Modificar cualquier cosa que no **sea lParam** tendrá consecuencias imprevisibles.

Cuando el sistema pasa posteriormente una copia de la estructura [**PROPSHEETPAGE**](pss-propsheetpage.md) de la página a la aplicación, usa el mismo puntero. Los cambios en la estructura se pasarán. Dado que el sistema omite el miembro **lParam,** se puede modificar para enviar información a otras partes de la aplicación. Por ejemplo, puede usar **lParam** para pasar información a la función de devolución de llamada [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) de la página.

[**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) establece automáticamente el tamaño y la posición inicial de una hoja de propiedades. La posición se basa en la posición de la ventana de propietario y el tamaño se basa en la página más grande especificada en la matriz de páginas cuando se creó la hoja de propiedades. Si desea que las páginas coincidan con el ancho de los cuatro botones de la parte inferior de la hoja de propiedades, establezca el ancho de la página más ancha en 190 unidades de diálogo.

El tamaño de una hoja de propiedades se calcula a partir de las propiedades *de* ancho y *alto* de la plantilla de diálogo en el archivo de recursos. Consulte [**Recurso DIALOG o**](/windows/desktop/menurc/dialog-resource) Recurso [**DIALOGEX**](/windows/desktop/menurc/dialogex-resource) para obtener más detalles. Sin embargo, tenga en cuenta que, por motivos de compatibilidad, las dimensiones se calculan con respecto a la fuente Dlg de MS Shell en lugar de a la fuente utilizada por la página. Si diseña una página que usa otra fuente, se puede usar una de las siguientes sugerencias.

-   Ajuste las dimensiones de la plantilla de diálogo para compensar la diferencia de tamaño entre la fuente Dlg de MS Shell y la fuente que usa realmente la página. Por ejemplo, si elige una fuente que tiene el doble de ancho que dlg de Shell de MS, establezca la propiedad width de la plantilla de diálogo en el doble del uso normal.
-   Use una [**plantilla DIALOGEX**](/windows/desktop/menurc/dialogex-resource) y establezca el estilo de diálogo **\_ SHELLFONT de DS.** En ese caso, el administrador de hojas de propiedades interpreta las dimensiones de la plantilla de diálogo en relación con la fuente utilizada por la plantilla de diálogo.

## <a name="adding-and-removing-pages"></a>Agregar y quitar páginas

Después de crear una hoja de propiedades, una aplicación puede agregar una página al final del conjunto de páginas existente enviando un mensaje [**\_ ADDPAGE de PSM.**](psm-addpage.md) Para insertar una página entre páginas existentes, envíe un [**mensaje \_ de PropSheet InsertPage.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_insertpage) Tenga en cuenta que el tamaño de la hoja de propiedades no puede cambiar después de crearla. Las páginas agregadas o insertadas no deben ser mayores que la página más grande actualmente en la hoja de propiedades. Para quitar una página, envíe un [**mensaje \_ REMOVEPAGE de PSM.**](psm-removepage.md)

Al definir una página, puede especificar la dirección de una función de devolución de llamada [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) a la que llama la hoja de propiedades al crear o quitar la página. El *uso de PropSheetPageProc* ofrece la oportunidad de realizar operaciones de inicialización y limpieza para páginas individuales.

> [!NOTE]  
> Se producen varios mensajes y una llamada de función mientras la hoja de propiedades manipula la lista de páginas. Mientras se realiza esta acción, el intento de modificar la lista de páginas tendrá resultados impredecibles. No agregue, inserte ni quite páginas en la implementación de [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka)o mientras controle las siguientes notificaciones y Windows mensajes.
>
> -   [PSN \_ APPLY](psn-apply.md)
> -   [PSN \_ KILLACTIVE](psn-killactive.md)
> -   [RESTABLECIMIENTO DE \_ PSN](psn-reset.md)
> -   [PSN \_ SETACTIVE](psn-setactive.md)
> -   [PSN \_ WIZBACK](psn-wizback.md)
> -   [PSN \_ WIZNEXT](psn-wiznext.md)
> -   [**WM \_ INITDIALOG**](/windows/desktop/dlgbox/wm-initdialog)
> -   [**WM \_ DESTROY**](/windows/desktop/winmsg/wm-destroy)

Si surge la necesidad de modificar una página de hoja de propiedades mientras se administra uno de estos mensajes o mientras [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) está en funcionamiento, publique un mensaje Windows privado. La aplicación no recibirá ese mensaje hasta que el administrador de la hoja de propiedades haya finalizado sus tareas, momento en el que será seguro modificar la lista de páginas.

Cuando se destruye una hoja de propiedades, destruye automáticamente todas las páginas que se le han agregado. Las páginas se destruyen en orden inverso a partir del especificado en la matriz utilizada para crear las páginas. Para destruir una página creada por la función [**CreatePropertySheetPage**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea) pero que no se agregó a la hoja de propiedades, use la [**función DestroyPropertySheetPage.**](/windows/desktop/api/Prsht/nf-prsht-destroypropertysheetpage)

## <a name="property-sheet-title-and-page-labels"></a>Título y etiquetas de página de la hoja de propiedades

Especifique el título de una hoja de propiedades en la [**estructura PROPSHEETHEADER**](pss-propsheetheader.md) utilizada para crear la hoja de propiedades. Si el **miembro dwFlags** incluye el valor **\_ PSH PROPTITLE,** la hoja de propiedades agrega el sufijo "Properties" o el prefijo "Properties for", dependiendo de la versión. Puede cambiar el título después de crear una hoja de propiedades mediante el mensaje [**\_ SETTITLE de PSM.**](psm-settitle.md) En un asistente de Aero, este mensaje se puede usar para cambiar dinámicamente el título de una página interior.

De forma predeterminada, una hoja de propiedades usa la cadena de nombre especificada en la plantilla de cuadro de diálogo como etiqueta de una página. Puede invalidar la cadena de nombre si incluye el valor **\_ USETITLE de PSP** en el miembro **dwFlags** de la estructura [**PROPSHEETPAGE**](pss-propsheetpage.md) que define la página. Cuando **se especifica PSP \_ USETITLE,** el **miembro pszTitle** debe contener la dirección de la cadena de etiqueta de la página.

## <a name="page-activation"></a>Activación de páginas

Una hoja de propiedades solo puede tener una página activa a la vez. La página que tiene la activación está en primer plano de la pila superpuesta de páginas. El usuario activa una página seleccionando su pestaña. una aplicación activa una página mediante el mensaje [**\_ SETCURSEL de PSM.**](psm-setcursel.md)

La hoja de propiedades envía [el código de notificación \_ KILLACTIVE](psn-killactive.md) de PSN a la página que está a punto de perder la activación. En respuesta, la página debe validar los cambios realizados por el usuario en la página. Si la página requiere una entrada de usuario adicional antes de perder la activación, use la función [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) para establecer el valor **\_ MSGRESULT de DWL** de la página en **TRUE.** Además, la página debe mostrar un cuadro de mensaje que describe el problema y proporciona la acción recomendada. Establezca **\_ MSGRESULT de DWL** en **FALSE** cuando sea correcto perder la activación.

Antes de que la página que obtiene la activación sea visible, la hoja de propiedades envía el código de [notificación \_ SETACTIVE](psn-setactive.md) de PSN a la página. La página debe responder inicializando sus ventanas de control.

## <a name="help-button"></a>Botón Ayuda

Las hojas de propiedades pueden mostrar dos botones de Ayuda: un botón Ayuda de hoja de propiedades que se muestra en la parte inferior del marco, junto a los botones Aceptar Cancelar aplicación y un botón de barra de subtítulos estándar que proporciona ayuda /  /  contextual.

El botón Ayuda de la hoja de propiedades es opcional y se puede habilitar en una página por página. Para mostrar el botón Ayuda de la hoja de propiedades para una o varias páginas:

-   Establezca la **marca \_ PSH HASHELP** en el **miembro dwFlags** de la estructura [**PROPSHEETHEADER**](pss-propsheetheader.md) de la hoja de propiedades.
-   Para cada página que mostrará un botón Ayuda, establezca la marca **\_ PSP HASHELP** en el **miembro dwFlags** de la estructura [**PROPSHEETPAGE de la**](pss-propsheetpage.md) página.

Cuando el usuario hace clic en el botón Ayuda, la página activa recibe un código de notificación de LA AYUDA de [PSN. \_ ](psn-help.md) La página debe responder mostrando información de Ayuda, normalmente llamando a la [**función WinHelp.**](/windows/desktop/api/winuser/nf-winuser-winhelpa)

### <a name="removing-the-caption-bar-help-button"></a>Quitar el botón ayuda de la barra de subtítulos

El botón Ayuda de la barra de subtítulos se muestra de forma predeterminada, por lo que la Ayuda contextual siempre está disponible para los botones Aceptar, Cancelar o Aplicar. Sin embargo, este botón se puede quitar, si es necesario. Para quitar el botón Ayuda de la barra de subtítulos de una hoja de propiedades:

-   Para las versiones de los controles comunes anteriores a la [versión 5.80](common-control-versions.md), debe implementar una función de devolución de llamada de [**hoja de propiedades**](/windows/desktop/api/Prsht/nc-prsht-pfnpropsheetcallback).
-   Para la [versión 5.80](common-control-versions.md) y posteriores de los controles comunes, simplemente puede establecer la marca PSH NOCONTEXTHELP en el miembro dwFlags de la estructura \_ [**PROPSHEETHEADER**](pss-propsheetheader.md) de la hoja de  propiedades. Sin embargo, si necesita compatibilidad con versiones anteriores de control comunes, debe implementar la función de devolución de llamada.

Para implementar una función de devolución de llamada de hoja de propiedades que quita el botón Ayuda de la barra de subtítulos:

-   Establezca la **marca PSH \_ USECALLBACK** en el **miembro dwFlags** de la estructura [**PROPSHEETHEADER**](pss-propsheetheader.md) de la hoja de propiedades.
-   Establezca el **miembro pfnCallBack** de la [**estructura PROPSHEETHEADER**](pss-propsheetheader.md) para que apunte a la función de devolución de llamada.
-   Implemente la función de devolución de llamada. Cuando esta función recibe el **mensaje \_ PSCB PRECREATE,** también recibirá un puntero a la plantilla de cuadro de diálogo de la hoja de propiedades. Quite el **estilo \_ CONTEXTHELP de DS** de esta plantilla.

En el ejemplo siguiente se muestra cómo implementar esta función de devolución de llamada:

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

Si la [**estructura DLGTEMPLATEEX**](/windows/desktop/dlgbox/dlgtemplateex) no está definida, incluya la siguiente declaración:

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

## <a name="ok-cancel-and-apply-buttons"></a>Botones Aceptar, Cancelar y Aplicar

Los **botones Aceptar** **y Aplicar** son similares; ambos dirigen las páginas de una hoja de propiedades para validar y aplicar los cambios de propiedad realizados por el usuario. La única diferencia es que al hacer clic en el **botón** Aceptar, la hoja de propiedades se destruye después de aplicar los cambios.

Cuando el usuario hace  clic en el botón **Aceptar** o Aplicar, la hoja de propiedades envía una notificación [ \_ KILLACTIVE](psn-killactive.md) de PSN a la página activa, lo que le ofrece la oportunidad de validar los cambios del usuario. Si los cambios son válidos, la página debe llamar a la función [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) con el valor **\_ MSGRESULT de DWL** establecido en **FALSE.** Si los cambios del usuario no son válidos, la página debe establecer **\_ MSGRESULT** de DWL en **TRUE** y mostrar un cuadro de diálogo que informe al usuario del problema. La página permanece activa hasta que establece **DWL \_ MSGRESULT** en **FALSE** en respuesta a un mensaje \_ KILLACTIVE de PSN.

Después de que una página responda a una notificación [ \_ KILLACTIVE](psn-killactive.md) de PSN estableciendo **DWL \_ MSGRESULT** en **FALSE,** la hoja de propiedades enviará una notificación [ \_ PSN APPLY](psn-apply.md) a cada página. Cuando una página recibe esta notificación, debe aplicar las nuevas propiedades al elemento correspondiente. Para indicar a la hoja de propiedades que los cambios son válidos para la página, llame a [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) con **\_ MSGRESULT DWL** establecido en **PSNRET \_ NOERROR**. Si los cambios no son válidos para la página, devuelva un error. Si lo hace, evita que se destruya la hoja de propiedades y devuelve el foco a la página que recibió la notificación PSN APPLY o a la página que tenía el foco cuando se presionó el \_ botón Aplicar.  Para devolver un error e indicar qué página recibirá el foco, establezca **DWL \_ MSGRESULT** en uno de los valores siguientes.

-   **PSNRET \_ No es válido.** La hoja de propiedades no se destruirá y el foco se devolverá a esta página.
-   **PSNRET \_ \_NOCHANGEPAGE NO VÁLIDO.** La hoja de propiedades no se destruirá y el foco se devolverá a la página que tenía el foco cuando se presionó el botón.

Una aplicación puede usar el [**mensaje \_ PSM APPLY**](psm-apply.md) para simular la selección del **botón** Aplicar.

El **botón** Aplicar se deshabilita inicialmente cuando una página se activa, lo que indica que aún no hay ningún cambio de propiedad que aplicar. Cuando la página recibe la entrada a través de uno de sus controles que indica que el usuario ha editado una propiedad, la página debe enviar el mensaje [**PSM \_ CHANGED**](psm-changed.md) a la hoja de propiedades. El mensaje hace que la hoja de propiedades habilite el **botón** Aplicar. Si posteriormente el usuario  hace  clic en el botón Aplicar o Cancelar, la página debe reinicializar sus controles y, a continuación, enviar el mensaje [**\_ PSM UNCHANGED**](psm-unchanged.md) para deshabilitar de nuevo el **botón** Aplicar.

A **veces,** el botón Aplicar hace que una página realice un cambio en una hoja de propiedades y el cambio no se puede deshacer. Cuando esto sucede, la página debe enviar el [**mensaje \_ CANCELTOCLOSE de PSM**](psm-canceltoclose.md) a la hoja de propiedades. El mensaje hace que la hoja  de propiedades cambie el texto del botón Aceptar a "Cerrar", lo que indica que los cambios aplicados no se pueden cancelar.

A veces, una página realiza un cambio en la configuración del sistema que Windows reiniciar o reiniciar el sistema antes de que el cambio suba efecto. Después de realizar este cambio, una página debe enviar el mensaje [**PSM \_ RESTARTWINDOWS**](psm-restartwindows.md) o [**PSM \_ REBOOTSYSTEM**](psm-rebootsystem.md) a la hoja de propiedades. Estos mensajes hacen que [**la función PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) devuelva el valor **\_ PSRESTARTWINDOWS** o **ID \_ PSREBOOTSYSTEM** del identificador después de destruir la hoja de propiedades.

Cuando un usuario  hace clic en el botón Cancelar, la hoja de propiedades envía el código de notificación [ \_ de PSN RESET](psn-reset.md) a todas las páginas, lo que indica que la hoja de propiedades está a punto de destruirse. Una página debe usar la notificación para realizar operaciones de limpieza.

## <a name="wizards"></a>Asistentes

Un asistente es un tipo especial de hoja de propiedades. Los asistentes están diseñados para presentar páginas de una en una secuencia controlada por la aplicación. En lugar de seleccionar de un grupo de páginas haciendo clic en una pestaña, los usuarios navegan hacia delante y hacia atrás por la secuencia, una página a la vez, haciendo clic en botones. Por ejemplo, la siguiente captura de pantalla muestra la página principal del Asistente para agregar hardware:

![captura de pantalla de la página principal de un asistente](images/wizard97.png)

En la siguiente captura de pantalla se muestra la primera página de un asistente de Avión, el nuevo estilo introducido en Windows Vista.

![captura de pantalla de la primera página de un asistente de avión](images/wizardaero.png)

Vea [Crear asistentes para](wizards.md) obtener una explicación completa de los asistentes.
