---
title: Personalización de cuadros de diálogo comunes
description: En este tema se describe cómo usar los cuadros de diálogo comunes.
ms.assetid: 31ba9deb-32e6-455c-be0e-ff8bcc691c80
keywords:
- Biblioteca de cuadros de diálogo comunes, personalizar
- cuadros de diálogo comunes, personalizar
- Personalización de cuadros de diálogo comunes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7eaa71c4f6fc6aa038ef150eb53935f6b3ec280
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421305"
---
# <a name="customizing-common-dialog-boxes"></a>Personalización de cuadros de diálogo comunes

Puede usar los cuadros de diálogo comunes en su formulario estándar, o puede personalizarlos. Desde el punto de vista del usuario, la ventaja principal del cuadro de diálogo común es la apariencia y la funcionalidad coherentes de la aplicación a la aplicación. Por lo tanto, es importante que personalice un cuadro de diálogo común solo cuando sea absolutamente necesario para una aplicación. De lo contrario, se pierden la apariencia coherente y la interfaz de codificación simple. Las personalizaciones adecuadas dejan intactos todos los controles originales posibles. Aumentar el tamaño del cuadro de diálogo o agregar nuevos controles en el espacio que ya está disponible en el cuadro de diálogo es una personalización adecuada. Ocultar los controles originales o cambiar de otra manera la funcionalidad prevista de los controles originales es una personalización menos adecuada.

En esta sección se describen los métodos siguientes para personalizar un cuadro de diálogo común:

-   [Plantillas personalizadas](#custom-templates)
-   [Procedimientos de enlace para cuadros de diálogo comunes](#hook-procedures-for-common-dialog-boxes)
-   [Mensajes de cuadro de diálogo comunes](#common-dialog-messages)
-   [Ayuda y soporte técnico](#help-support)
    -   [Ayuda contextual](#context-sensitive-help)
    -   [Botón Ayuda](#the-help-button)

## <a name="custom-templates"></a>Plantillas personalizadas

Los cuadros de diálogo comunes tienen plantillas predeterminadas que definen el número, el tipo y la posición de los controles estándar en el cuadro de diálogo. Puede definir una plantilla personalizada para proporcionar a los usuarios acceso a controles adicionales que son únicos para la aplicación.

En el caso de todos los cuadros de diálogo comunes, excepto los cuadros de diálogo **abrir** y **Guardar como** , modifique la plantilla predeterminada para crear una plantilla personalizada que reemplace la plantilla predeterminada. La plantilla personalizada define el tipo y la posición de los controles estándar, así como los controles adicionales.

Al crear una plantilla de cuadro de diálogo personalizada modificando la plantilla de cuadro de diálogo predeterminada, asegúrese de que los identificadores de los controles agregados sean únicos y no entren en conflicto con los identificadores de los controles estándar. En la tabla siguiente se muestra el nombre del archivo de plantilla predeterminado y el archivo de inclusión para cada uno de los tipos de cuadro de diálogo comunes.



| Tipo de cuadro de diálogo               | Archivo de plantilla | Incluir archivo |
|-------------------------------|---------------|--------------|
| **Color**                     | Color. Dlg     | ColorDlg. h   |
| **Buscar**                      | Textobuscado. Dlg  | Dlgs. h       |
| **Fuente**                      | Font. Dlg      | Dlgs. h       |
| **Abrir** (selección múltiple) | FileOpen. Dlg  | Dlgs. h       |
| **Abrir** (selección única)   | FileOpen. Dlg  | Dlgs. h       |
| **Configurar página**                | Prnsetup. Dlg  | Dlgs. h       |
| **Imprimir**                     | Prnsetup. Dlg  | Dlgs. h       |
| **Configuración de impresión** (obsoleto)    | Prnsetup. Dlg  | Dlgs. h       |
| **Sustituya**                   | Textobuscado. Dlg  | Dlgs. h       |



 

Para habilitar una plantilla personalizada, debe establecer una marca en el miembro **Flags** de la estructura correspondiente para el cuadro de diálogo. Si la plantilla es un recurso de una biblioteca de vínculos dinámicos o de aplicación, establezca una marca **ENABLETEMPLATE** en el miembro **Flags** y use los miembros **hInstance** y **lpTemplateName** de la estructura para identificar el nombre del módulo y del recurso. Si la plantilla ya está en memoria, establezca una marca **ENABLETEMPLATEHANDLE** en el miembro **Flags** y use el miembro **hInstance** para identificar el objeto de memoria que contiene la plantilla.

En la mayoría de los casos, también debe habilitar un procedimiento de enlace para que el cuadro de diálogo admita y procese la entrada para los controles adicionales de la plantilla personalizada.

En el caso de los cuadros de diálogo **abrir** y **Guardar como** del explorador, las plantillas predeterminadas no están disponibles para su modificación. En su lugar, la plantilla personalizada define un cuadro de diálogo secundario que incluye solo los elementos que se van a agregar al cuadro de diálogo estándar. La plantilla personalizada también puede definir un control estático que especifique la ubicación del clúster de controles estándar en el cuadro de diálogo secundario. Para obtener más información, vea [plantillas personalizadas de estilo de explorador](open-and-save-as-dialog-boxes.md).

## <a name="hook-procedures-for-common-dialog-boxes"></a>Procedimientos de enlace para cuadros de diálogo comunes

Para cada uno de los cuadros de diálogo comunes, puede habilitar un procedimiento de enlace para procesar los mensajes desde el procedimiento de cuadro de diálogo predeterminado. Hay dos tipos generales de procedimientos de enlace de diálogo comunes:

-   El procedimiento de enlace estándar que se usa con los cuadros de diálogo más comunes
-   El procedimiento de enlace de estilo de explorador compatible con los cuadros de diálogo **abrir** y **Guardar como**

Cuando se proporciona un procedimiento de enlace estándar para uno de los cuadros de diálogo comunes, el procedimiento de cuadro de diálogo predeterminado controla sus mensajes como se indica a continuación.



| Message                                 | Controlar                                                                                                                                                                                                             |
|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**INITDIALOG de WM \_**](wm-initdialog.md) | El procedimiento de cuadro de diálogo predeterminado procesa el mensaje antes de pasarlo al procedimiento de enlace. El parámetro *lParam* del mensaje es un puntero a la estructura de inicialización especificada cuando se creó el cuadro de diálogo. |
| Todos los demás mensajes                      | El procedimiento de enlace recibe el mensaje en primer lugar. Después, el valor devuelto del procedimiento de enlace determina si el procedimiento de cuadro de diálogo predeterminado procesa el mensaje o lo omite.                                     |



 

En el caso de los cuadros de diálogo **abrir** y **Guardar como** del estilo del explorador, el procedimiento de enlace no recibe los mensajes destinados a los controles estándar en el cuadro de diálogo. En su lugar, recibe mensajes de notificación del cuadro de diálogo y los mensajes de cualquier control adicional que haya definido en una plantilla personalizada. Para obtener más información, vea [procedimientos de enlace de estilo del explorador](open-and-save-as-dialog-boxes.md).

Para habilitar un procedimiento de enlace, establezca un valor de **ENABLEHOOK** en el miembro **Flags** de la estructura correspondiente para el cuadro de diálogo. Si se establece una marca **ENABLEHOOK** , un miembro **lpfnHook** de la estructura debe especificar la dirección del procedimiento de enlace.

En la tabla siguiente se muestra el tipo de procedimiento de enlace que se debe proporcionar para cada uno de los cuadros de diálogo comunes.



| Tipo de cuadro de diálogo                          | Procedimiento de enlace                                      |
|------------------------------------------|-----------------------------------------------------|
| **Color**                                | [*CCHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpcchookproc)                      |
| **Buscar** o **reemplazar**                  | [*FRHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpfrhookproc)                      |
| **Fuente**                                 | [*CFHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc)                      |
| **Abrir** o **Guardar como** (estilo del explorador) | [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)                    |
| **Abrir** o **Guardar como** (estilo anterior)      | [*OFNHookProcOldStyle*](/previous-versions/windows/desktop/legacy/ms646932(v=vs.85)) |
| **Imprimir**                                | [*PrintHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpprinthookproc)                |
| **Configurar página**                           | [*PageSetupHook*](/windows/win32/api/commdlg/nc-commdlg-lppagesetuphook)                |



 

En el cuadro de diálogo **Configurar página** , también puede especificar un procedimiento de enlace [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) . Se trata de un procedimiento de enlace especial que puede usar para personalizar la apariencia de la página de ejemplo que se muestra en el cuadro de diálogo **Configurar página** .

> [!Note]  
> El cuadro de diálogo Configurar **impresión** ha sido sustituido por el cuadro de diálogo **Configurar página** . Las aplicaciones deben usar el cuadro de diálogo **Configurar página** . Sin embargo, para la compatibilidad, la función [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) sigue siendo compatible con la presentación del cuadro de diálogo **configuración de impresión** . Puede proporcionar un procedimiento de enlace [*SetupHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpsetuphookproc) para el cuadro de diálogo **configuración de impresión** .

 

## <a name="common-dialog-messages"></a>Mensajes de cuadro de diálogo comunes

Los cuadros de diálogo comunes usan mensajes para notificar al procedimiento de ventana o al procedimiento de enlace cuando se producen determinados eventos. Además, hay mensajes que se pueden enviar a un cuadro de diálogo común para recuperar información o para controlar el comportamiento o la apariencia del cuadro de diálogo. En esta sección se describen los mensajes de diálogo comunes registrados por la función [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) , los mensajes usados por el cuadro de diálogo **fuente** y el cuadro de diálogo **Configurar página** , y los mensajes que usan los cuadros de diálogo **abrir** y **Guardar como** del estilo Explorador.

La biblioteca de cuadros de diálogo comunes define un conjunto de cadenas de mensaje. Puede pasar una constante asociada a una de estas cadenas de mensaje a [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) para obtener un identificador de mensaje. Después, puede utilizar el identificador para detectar y procesar los mensajes enviados desde un cuadro de diálogo común, o para enviar mensajes a un cuadro de diálogo común. En la tabla siguiente se muestran las constantes de mensaje y se describe su uso.



| Supuestos                               | Use                                                                                                                                                                                                                                                                                                                                                                                                                    |
|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**COLOROKSTRING**](colorokstring.md) | Un cuadro de diálogo de **color** envía este mensaje al procedimiento de enlace cuando el usuario selecciona un color y hace clic en el botón **Aceptar** . El procedimiento de enlace puede aceptar el color o rechazarlo y forzar que el cuadro de diálogo permanezca abierto.                                                                                                                                                                                             |
| [**FILEOKSTRING**](fileokstring.md)   | Un cuadro de diálogo **abrir** o **Guardar como** envía este mensaje al procedimiento de enlace cuando el usuario selecciona un nombre de archivo y hace clic en el botón **Aceptar** . El procedimiento de enlace puede aceptar el nombre de archivo o rechazarlo y forzar que el cuadro de diálogo permanezca abierto. En el caso de los cuadros de diálogo **abrir** y **Guardar como** del explorador, este mensaje se ha sustituido por el mensaje de notificación [**\_ FILEOK de la red CDN**](cdn-fileok.md) .<br/> |
| [**FINDMSGSTRING**](findmsgstring.md) | Un cuadro de diálogo **Buscar** o **reemplazar** envía este mensaje al procedimiento de ventana de su ventana primaria cuando el usuario hace clic en **Buscar siguiente**, **reemplazar** o **reemplazar todo**, o cierra el cuadro de diálogo. El parámetro *lParam* del mensaje es un puntero a una estructura [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) que contiene la entrada del usuario.                                                                               |
| [**HELPMSGSTRING**](helpmsgstring.md) | Todos los cuadros de diálogo comunes envían este mensaje al procedimiento de ventana de la ventana primaria cuando el usuario hace clic en el botón **ayuda** . En el caso de los cuadros de diálogo **abrir** y **Guardar como** del explorador, este mensaje se ha sustituido por el mensaje de notificación de la [**\_ ayuda de CDN**](cdn-help.md) .<br/>                                                                                                                    |
| [**LBSELCHSTRING**](lbselchstring.md) | Un cuadro de diálogo **abrir** o **Guardar como** envía este mensaje al procedimiento de enlace cuando el usuario cambia la selección en el cuadro de lista **nombre de archivo** . En el caso de los cuadros de diálogo **abrir** y **Guardar como** del explorador, este mensaje se ha sustituido por el mensaje de notificación [**\_ SELCHANGE de la red CDN**](cdn-selchange.md) .<br/>                                                                                           |
| [**SETRGBSTRING**](setrgbstring.md)   | Un procedimiento de enlace puede enviar este mensaje a un cuadro de diálogo de **color** para establecer la selección de color actual.                                                                                                                                                                                                                                                                                                                   |
| [**SHAREVISTRING**](sharevistring.md) | Un cuadro de diálogo **abrir** o **Guardar como** envía este mensaje al procedimiento de enlace si se produce una infracción de uso compartido para el archivo seleccionado cuando el usuario hace clic en el botón **Aceptar** . En el caso de los cuadros de diálogo **abrir** y **Guardar como** del explorador, este mensaje se ha sustituido por el mensaje de notificación [**\_ SHAREVIOLATION de la red CDN**](cdn-shareviolation.md) .<br/>                                                        |



 

Algunos cuadros de diálogo comunes envían y reciben otros mensajes de ventana. El procedimiento de enlace de un cuadro de diálogo de **fuente** puede enviar cualquiera de los mensajes de **\_ CHOOSEFONT \_ \* de WM** al cuadro de diálogo **fuente** . Para obtener más información, vea [fuente (cuadro de diálogo)](font-dialog-box.md). El cuadro de diálogo **Configurar página** envía los mensajes **\_ PSD \_ \* de WM** si ha habilitado un procedimiento de enlace [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) . Para obtener más información, vea [cuadro de diálogo Configurar página](page-setup-dialog-box.md).

Los cuadros de diálogo **abrir** y **Guardar como** del estilo Explorador admiten un conjunto de mensajes predefinidos. Esto incluye los mensajes de notificación enviados en forma de mensaje de notificación de [**WM \_**](../controls/wm-notify.md) al procedimiento de enlace y los mensajes que el procedimiento de enlace puede enviar al cuadro de diálogo. Para obtener una lista completa de estos mensajes, vea [procedimientos de enlace de estilo del explorador](open-and-save-as-dialog-boxes.md).

## <a name="help-support"></a>Ayuda y soporte técnico

Los cuadros de diálogo comunes proporcionan ayuda contextual para los controles estándar del cuadro de diálogo. Para proporcionar ayuda adicional para un cuadro de diálogo común, puede mostrar un botón **ayuda** y procesar los mensajes generados cuando el usuario hace clic en el botón. El botón **ayuda** es un complemento de la ayuda contextual predeterminada. El botón **ayuda** es útil para describir el uso general del cuadro de diálogo a medida que se aplica a la aplicación.

-   [Ayuda contextual](#context-sensitive-help)
-   [Botón Ayuda](#the-help-button)

### <a name="context-sensitive-help"></a>Context-Sensitive ayuda

Todos los cuadros de diálogo comunes proporcionan ayuda contextual para los controles estándar del cuadro de diálogo. El usuario puede mostrar la ayuda de los controles individuales mediante cualquiera de los métodos siguientes:

-   Seleccionar el control y presionar la tecla F1.
-   Haciendo clic **en el** en la barra de título y después haga clic en un control.
-   Hacer clic con el botón secundario del mouse sobre un control.

Si personaliza un cuadro de diálogo agregando nuevos controles, también debe ampliar la ayuda para estos controles procesando las solicitudes de ayuda en el procedimiento de enlace. El procedimiento de enlace recibe los mensajes siguientes cuando el usuario solicita ayuda.



| Acción del usuario                                                           | Message                                      |
|-----------------------------------------------------------------------|----------------------------------------------|
| Haga clic con el botón secundario del mouse sobre un control.                          | [**CONTEXTMENU de WM \_**](/windows/desktop/menurc/wm-contextmenu) |
| Presionó la tecla F1.                                                   | [**ayuda de WM \_**](../shell/wm-help.md)               |
| ¿Hizo clic en **?** en la barra de título y, a continuación, haga clic en un control. | [**ayuda de WM \_**](../shell/wm-help.md)               |



 

Debe procesar estos mensajes para los controles que ha agregado, pero deje que el procedimiento de cuadro de diálogo predeterminado procese los mensajes para los controles estándar. Para obtener más información sobre cómo procesar estos mensajes, vea la [ayuda](/previous-versions/windows/desktop/legacy/bb776786(v=vs.85))de.

### <a name="the-help-button"></a>Botón Ayuda

Puede mostrar un botón **ayuda** en cualquiera de los cuadros de diálogo comunes si establece un valor de **SHOWHELP** en el miembro **Flags** de la estructura de inicialización del cuadro de diálogo. Si muestra el botón **ayuda** , debe procesar la solicitud del usuario para obtener ayuda. El procesamiento puede realizarse en uno de los procedimientos de ventana de la aplicación o en un procedimiento de enlace para el cuadro de diálogo. Normalmente, se procesa la solicitud de ayuda mediante una llamada a la función [**WinHelp**](/windows/win32/api/winuser/nf-winuser-winhelpa) .

Para procesar los mensajes de ayuda en uno de los procedimientos de ventana, debe obtener un identificador de mensaje para la cadena definida por el valor [**HELPMSGSTRING**](helpmsgstring.md) e identificar la ventana para recibir mensajes. Para obtener el identificador de mensaje, especifique **HELPMSGSTRING** como parámetro en una llamada a la función [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) . Al crear el cuadro de diálogo, use el miembro **hwndOwner** de la estructura de inicialización del cuadro de diálogo para identificar la ventana que va a recibir los mensajes. El procedimiento de cuadro de diálogo envía el mensaje al procedimiento de ventana siempre que el usuario hace clic en el botón **ayuda** .

Para procesar los mensajes de ayuda en un procedimiento de enlace, debe procesar el mensaje del [**\_ comando de WM**](/windows/desktop/menurc/wm-command) . El procedimiento de enlace proporciona ayuda si el parámetro *wParam* de este mensaje indica que el usuario hizo clic en el botón **ayuda** . El identificador del botón **ayuda** es la constante **pshHelp** definida en el archivo Dlgs. h.

Los procedimientos de enlace para los cuadros de diálogo **abrir** y **Guardar como** del estilo de explorador no reciben mensajes de [**\_ comando de WM**](/windows/desktop/menurc/wm-command) para el botón **ayuda** . En su lugar, el cuadro de diálogo envía un mensaje de notificación de [**\_ ayuda de CDN**](cdn-help.md) al procedimiento de enlace cuando se hace clic en el botón **ayuda** .

 

