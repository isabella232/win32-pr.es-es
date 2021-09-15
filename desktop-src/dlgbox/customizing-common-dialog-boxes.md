---
title: Personalizar cuadros de diálogo comunes
description: En este tema se describe cómo usar cuadros de diálogo comunes.
ms.assetid: 31ba9deb-32e6-455c-be0e-ff8bcc691c80
keywords:
- Biblioteca común de cuadros de diálogo, personalización
- cuadros de diálogo comunes, personalizar
- personalizar cuadros de diálogo comunes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7eaa71c4f6fc6aa038ef150eb53935f6b3ec280
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359318"
---
# <a name="customizing-common-dialog-boxes"></a>Personalizar cuadros de diálogo comunes

Puede usar los cuadros de diálogo comunes en su formato estándar o puede personalizarlos. Desde la perspectiva del usuario, la principal ventaja del cuadro de diálogo común es su apariencia y funcionalidad coherentes de la aplicación a la aplicación. Por lo tanto, es importante personalizar un cuadro de diálogo común solo cuando sea absolutamente necesario para una aplicación. De lo contrario, se pierde la apariencia coherente y la interfaz de codificación simple. Las personalizaciones adecuadas dejan intactos tantos controles originales como sea posible. Aumentar el tamaño del cuadro de diálogo o agregar nuevos controles en el espacio ya disponible en el cuadro de diálogo es una personalización adecuada. Ocultar controles originales o cambiar la funcionalidad prevista de los controles originales es una personalización menos adecuada.

En esta sección se de abordan los métodos siguientes para personalizar un cuadro de diálogo común:

-   [Plantillas personalizadas](#custom-templates)
-   [Procedimientos de enlace para cuadros de diálogo comunes](#hook-procedures-for-common-dialog-boxes)
-   [Mensajes de diálogo comunes](#common-dialog-messages)
-   [Ayuda de soporte técnico](#help-support)
    -   [Ayuda contextual](#context-sensitive-help)
    -   [Botón Ayuda](#the-help-button)

## <a name="custom-templates"></a>Plantillas personalizadas

Los cuadros de diálogo comunes tienen plantillas predeterminadas que definen el número, el tipo y la posición de los controles estándar en el cuadro de diálogo. Puede definir una plantilla personalizada para proporcionar a los usuarios acceso a controles adicionales que son únicos para la aplicación.

Para todos los cuadros de  diálogo comunes excepto los cuadros de diálogo Abrir y Guardar **como** de estilo explorador, modifique la plantilla predeterminada para crear una plantilla personalizada que reemplace la plantilla predeterminada. La plantilla personalizada define el tipo y la posición de los controles estándar, así como los controles adicionales.

Al crear una plantilla de cuadro de diálogo personalizada modificando la plantilla de cuadro de diálogo predeterminada, asegúrese de que los identificadores de los controles agregados sean únicos y no entren en conflicto con los identificadores de los controles estándar. En la tabla siguiente se muestra el nombre del archivo de plantilla predeterminado e incluye el archivo para cada uno de los tipos de cuadro de diálogo comunes.



| Tipo de cuadro de diálogo               | Archivo de plantilla | Incluir archivo |
|-------------------------------|---------------|--------------|
| **Color**                     | Color.dlg     | ColorDlg.h   |
| **Buscar**                      | Findtext.dlg  | Dlgs.h       |
| **Font**                      | Font.dlg      | Dlgs.h       |
| **Abrir** (selección múltiple) | Fileopen.dlg  | Dlgs.h       |
| **Abrir** (selección única)   | Fileopen.dlg  | Dlgs.h       |
| **Configuración de la página**                | Prnsetup.dlg  | Dlgs.h       |
| **Imprimir**                     | Prnsetup.dlg  | Dlgs.h       |
| **Instalación de impresión** (obsoleto)    | Prnsetup.dlg  | Dlgs.h       |
| **Sustituya**                   | Findtext.dlg  | Dlgs.h       |



 

Para habilitar una plantilla personalizada, debe establecer una marca en el **miembro Flags** de la estructura correspondiente del cuadro de diálogo. Si la plantilla es un recurso de una aplicación o biblioteca de vínculos **dinámicos,** establezca una marca **ENABLETEMPLATE** en el miembro Flags y use los **miembros hInstance** y **lpTemplateName** de la estructura para identificar el módulo y el nombre del recurso. Si la plantilla ya está en memoria, establezca una marca **ENABLETEMPLATEHANDLE** en el miembro **Flags** y use el **miembro hInstance** para identificar el objeto de memoria que contiene la plantilla.

En la mayoría de los casos, también debe habilitar un procedimiento de enlace para que el cuadro de diálogo admita y procese la entrada de los controles adicionales de la plantilla personalizada.

Para los cuadros de diálogo Abrir **y** Guardar **como** de estilo explorador, las plantillas predeterminadas no están disponibles para su modificación. En su lugar, la plantilla personalizada define un cuadro de diálogo secundario que incluye solo los elementos que se van a agregar al cuadro de diálogo estándar. La plantilla personalizada también puede definir un control estático que especifique la ubicación del clúster de controles estándar en el cuadro de diálogo secundario. Para obtener más información, vea [Plantillas personalizadas de estilo explorador.](open-and-save-as-dialog-boxes.md)

## <a name="hook-procedures-for-common-dialog-boxes"></a>Procedimientos de enlace para cuadros de diálogo comunes

Para cada uno de los cuadros de diálogo comunes, puede habilitar un procedimiento de enlace para procesar mensajes del procedimiento de cuadro de diálogo predeterminado. Hay dos tipos generales de procedimientos comunes de enlace de diálogo:

-   Procedimiento de enlace estándar usado con los cuadros de diálogo más comunes
-   Procedimiento de enlace de estilo explorador admitido por los **cuadros de** diálogo Abrir **y** Guardar como

Cuando se proporciona un procedimiento de enlace estándar para uno de los cuadros de diálogo comunes, el procedimiento de cuadro de diálogo predeterminado controla sus mensajes como se muestra a continuación.



| Message                                 | Controlar                                                                                                                                                                                                             |
|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WM \_ INITDIALOG**](wm-initdialog.md) | El procedimiento de cuadro de diálogo predeterminado procesa el mensaje antes de pasarlo al procedimiento de enlace. El parámetro *lParam del mensaje* es un puntero a la estructura de inicialización especificada cuando se creó el diálogo. |
| Todos los demás mensajes                      | El procedimiento de enlace recibe primero el mensaje. A continuación, el valor devuelto del procedimiento de enlace determina si el procedimiento de diálogo predeterminado procesa el mensaje o lo omite.                                     |



 

Para los cuadros de **diálogo** Abrir y Guardar **como** de estilo explorador, el procedimiento de enlace no recibe mensajes destinados a los controles estándar del cuadro de diálogo. En su lugar, recibe los mensajes de notificación del cuadro de diálogo y los mensajes de los controles adicionales definidos en una plantilla personalizada. Para obtener más información, vea [Explorer-Style Hook Procedures](open-and-save-as-dialog-boxes.md).

Para habilitar un procedimiento de enlace, establezca un **valor ENABLEHOOK** en el **miembro Flags** de la estructura correspondiente para el cuadro de diálogo. Si se establece una marca **ENABLEHOOK,** un **miembro lpfnHook** de la estructura debe especificar la dirección del procedimiento de enlace.

En la tabla siguiente se muestra el tipo de procedimiento de enlace que se debe proporcionar para cada uno de los cuadros de diálogo comunes.



| Tipo de cuadro de diálogo                          | Procedimiento de enlace                                      |
|------------------------------------------|-----------------------------------------------------|
| **Color**                                | [*CCHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpcchookproc)                      |
| **Buscar** o **reemplazar**                  | [*FRHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpfrhookproc)                      |
| **Font**                                 | [*CFHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc)                      |
| **Abrir** o **guardar como** (estilo explorador) | [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)                    |
| **Abrir** o **guardar como** (estilo antiguo)      | [*OFNHookProcOldStyle*](/previous-versions/windows/desktop/legacy/ms646932(v=vs.85)) |
| **Imprimir**                                | [*PrintHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpprinthookproc)                |
| **Configuración de la página**                           | [*PageSetupHook*](/windows/win32/api/commdlg/nc-commdlg-lppagesetuphook)                |



 

Para el **cuadro de diálogo Configuración** de página, también puede especificar un procedimiento de enlace [*PagePaintHook.*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) Se trata de un procedimiento de enlace especial que puede usar para personalizar la apariencia de la página de ejemplo que se muestra en el cuadro de diálogo **Configuración** de página.

> [!Note]  
> El **cuadro de diálogo Instalar** impresión se ha reemplazado por el cuadro de diálogo **Configurar** página . Las aplicaciones deben usar el **cuadro de diálogo Configurar** página . Sin embargo, por compatibilidad, la [**función PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) sigue siendo compatible con la presentación del cuadro **de diálogo Instalación** de impresión. Puede proporcionar un procedimiento [*de enlace SetupHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpsetuphookproc) para el cuadro **de diálogo Instalación** de impresión .

 

## <a name="common-dialog-messages"></a>Mensajes de diálogo comunes

Los cuadros de diálogo comunes usan mensajes para notificar el procedimiento de ventana o el procedimiento de enlace cuando se producen determinados eventos. Además, hay mensajes que puede enviar a un cuadro de diálogo común para recuperar información o para controlar el comportamiento o la apariencia del cuadro de diálogo. En esta sección se describen los mensajes de diálogo comunes  registrados  por la función [**RegisterWindowMessage,**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) los  mensajes  usados por el cuadro de diálogo Fuente y el cuadro de diálogo Configuración de página y los mensajes usados por los cuadros de diálogo Abrir y Guardar como del estilo explorador.

La biblioteca común de cuadros de diálogo define un conjunto de cadenas de mensaje. Puede pasar una constante asociada a una de estas cadenas de mensaje [**a RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) para obtener un identificador de mensaje. A continuación, puede usar el identificador para detectar y procesar los mensajes enviados desde un cuadro de diálogo común o para enviar mensajes a un cuadro de diálogo común. En la tabla siguiente se muestran las constantes del mensaje y se describe su uso.



| Contants                               | Uso                                                                                                                                                                                                                                                                                                                                                                                                                    |
|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**COLOROKSTRING**](colorokstring.md) | Un **cuadro** de diálogo Color envía este mensaje al procedimiento de enlace cuando el usuario selecciona un color y hace clic en el **botón** Aceptar. El procedimiento de enlace puede aceptar el color o rechazarlo y forzar que el cuadro de diálogo permanezca abierto.                                                                                                                                                                                             |
| [**FILEOKSTRING**](fileokstring.md)   | Un **cuadro** de **diálogo Abrir** o Guardar como envía este mensaje al procedimiento de enlace cuando el usuario selecciona un nombre de archivo y hace clic en el **botón** Aceptar. El procedimiento de enlace puede aceptar el nombre de archivo o rechazarlo y forzar que el cuadro de diálogo permanezca abierto. En el caso de **los cuadros** de diálogo Abrir y Guardar **como** de estilo explorador, este mensaje se ha reemplazado por el CDN [**notificación \_ FILEOK.**](cdn-fileok.md)<br/> |
| [**FINDMSGSTRING**](findmsgstring.md) | Un **cuadro** de **diálogo** Buscar o reemplazar envía este mensaje al procedimiento de ventana de su ventana primaria cuando el usuario hace clic en Buscar **siguiente,** Reemplazar **o** Reemplazar **todo,** o cierra el cuadro de diálogo. El parámetro *lParam del* mensaje es un puntero a una estructura [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) que contiene la entrada del usuario.                                                                               |
| [**HELPMSGSTRING**](helpmsgstring.md) | Todos los cuadros de diálogo comunes envían este mensaje al procedimiento de ventana de su ventana primaria cuando el usuario hace clic en el **botón Ayuda.** En el caso de **los cuadros** de diálogo Abrir y Guardar **como** de estilo explorador, este mensaje se ha reemplazado por el CDN de [**notificación \_ help.**](cdn-help.md)<br/>                                                                                                                    |
| [**LBSELCHSTRING**](lbselchstring.md) | Un **cuadro** de diálogo **Abrir** o Guardar como envía este mensaje al procedimiento de enlace cuando el usuario cambia la selección en el cuadro de **lista Nombre** de archivo . Para los cuadros **de** diálogo Abrir y Guardar **como** de estilo explorador, este mensaje se ha reemplazado por el CDN de notificación [**\_ SELCHANGE.**](cdn-selchange.md)<br/>                                                                                           |
| [**SETRGBSTRING**](setrgbstring.md)   | Un procedimiento de enlace puede enviar este mensaje a un **cuadro de** diálogo Color para establecer la selección de color actual.                                                                                                                                                                                                                                                                                                                   |
| [**SHAREVISTRING**](sharevistring.md) | Un **cuadro de** diálogo Abrir o Guardar como envía este mensaje al procedimiento de enlace si se produce una infracción de uso compartido para el archivo seleccionado cuando el usuario hace clic en el **botón** Aceptar.  En el caso de **los** cuadros de **diálogo** Abrir y Guardar como de estilo explorador, este mensaje se ha reemplazado por el CDN de notificación [**\_ SHAREVIOLATION.**](cdn-shareviolation.md)<br/>                                                        |



 

Algunos cuadros de diálogo comunes envían y reciben otros mensajes de ventana. El procedimiento de enlace para **un cuadro de diálogo** Fuente puede enviar cualquiera de los mensajes WM **\_ CHOOSEFONT _ al cuadro de diálogo \_ \* *_* Fuente** . Para obtener más información, vea [Font Dialog Box](font-dialog-box.md). El **cuadro de diálogo Configuración** de página envía los mensajes * WM *\_ PSD \_ \** _ si ha habilitado un procedimiento de enlace [_PagePaintHook*.](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) Para obtener más información, vea [Cuadro de diálogo Configurar página](page-setup-dialog-box.md).

Los cuadros de diálogo Abrir y Guardar **como** **de** estilo explorador admiten un conjunto de mensajes predefinidos. Estos incluyen mensajes de notificación enviados en forma de mensaje [**WM \_ NOTIFY**](../controls/wm-notify.md) al procedimiento de enlace y mensajes que el procedimiento de enlace puede enviar al cuadro de diálogo. Para obtener una lista completa de estos mensajes, vea [Explorer-Style Hook Procedures](open-and-save-as-dialog-boxes.md).

## <a name="help-support"></a>Ayuda de soporte técnico

Los cuadros de diálogo comunes proporcionan ayuda contextual para los controles estándar del cuadro de diálogo. Para proporcionar ayuda adicional para un cuadro  de diálogo común, puede mostrar un botón Ayuda y procesar los mensajes generados cuando el usuario hace clic en el botón. El **botón** Ayuda es un complemento de la ayuda contextual predeterminada. El **botón** Ayuda es útil para describir el propósito general del cuadro de diálogo a medida que se aplica a la aplicación.

-   [Ayuda contextual](#context-sensitive-help)
-   [Botón Ayuda](#the-help-button)

### <a name="context-sensitive-help"></a>Context-Sensitive Ayuda

Todos los cuadros de diálogo comunes proporcionan ayuda contextual para los controles estándar del cuadro de diálogo. El usuario puede mostrar ayuda para controles individuales mediante cualquiera de los métodos siguientes:

-   Seleccionar el control y presionar la tecla F1.
-   Al hacer clic en **?** en la barra de título y, posteriormente, haciendo clic en un control .
-   Haga clic con el botón derecho del mouse sobre un control.

Si personaliza un cuadro de diálogo mediante la adición de nuevos controles, también debe ampliar la compatibilidad de ayuda para estos controles mediante el procesamiento de solicitudes de ayuda en el procedimiento de enlace. El procedimiento de enlace recibe los mensajes siguientes cuando el usuario solicita ayuda.



| Acción del usuario                                                           | Message                                      |
|-----------------------------------------------------------------------|----------------------------------------------|
| Haga clic con el botón derecho del mouse sobre un control.                          | [**WM \_ CONTEXTMENU**](/windows/desktop/menurc/wm-contextmenu) |
| Presione la tecla F1.                                                   | [**WM \_ HELP**](../shell/wm-help.md)               |
| Se ha hecho clic en **?** en la barra de título y, a continuación, ha hecho clic en un control . | [**WM \_ HELP**](../shell/wm-help.md)               |



 

Debe procesar estos mensajes para los controles que ha agregado, pero deje que el procedimiento del cuadro de diálogo predeterminado procese los mensajes de los controles estándar. Para obtener más información sobre cómo procesar estos mensajes, vea [Ayuda de](/previous-versions/windows/desktop/legacy/bb776786(v=vs.85)).

### <a name="the-help-button"></a>Botón Ayuda

Puede mostrar un botón **Ayuda** en cualquiera de los cuadros de diálogo comunes estableciendo un valor **SHOWHELP** en el miembro **Flags** de la estructura de inicialización del cuadro de diálogo. Si muestra el botón **Ayuda,** debe procesar la solicitud de ayuda del usuario. El procesamiento se puede realizar en uno de los procedimientos de ventana de la aplicación o en un procedimiento de enlace para el cuadro de diálogo. Normalmente, procesaría la solicitud de ayuda mediante una llamada a la [**función WinHelp.**](/windows/win32/api/winuser/nf-winuser-winhelpa)

Para procesar mensajes de ayuda en uno de los procedimientos de la ventana, debe obtener un identificador de mensaje para la cadena definida por el valor [**HELPMSGSTRING**](helpmsgstring.md) e identificar la ventana para recibir mensajes. Para obtener el identificador del mensaje, especifique **HELPMSGSTRING como** parámetro en una llamada a la [**función RegisterWindowMessage.**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) Al crear el cuadro de diálogo, use el **miembro hwndOwner** de la estructura de inicialización del cuadro de diálogo para identificar la ventana que va a recibir los mensajes. El procedimiento del cuadro de diálogo envía el mensaje al procedimiento de ventana cada vez que el usuario hace clic en el **botón** Ayuda.

Para procesar los mensajes de ayuda en un procedimiento de enlace, debe procesar el [**mensaje WM \_ COMMAND.**](/windows/desktop/menurc/wm-command) El procedimiento de enlace proporciona ayuda si el *parámetro wParam* de este mensaje indica que el usuario hizo clic en el **botón Ayuda.** El identificador del botón **Ayuda** es la **constante pshHelp** definida en el archivo Dlgs.h.

Los procedimientos de  enlace para los cuadros de diálogo Abrir y Guardar **como** de estilo Explorador no reciben mensajes [**WM \_ COMMAND**](/windows/desktop/menurc/wm-command) para el **botón Ayuda.** En su lugar, el cuadro de diálogo CDN mensaje de notificación [**\_ DE AYUDA**](cdn-help.md) al procedimiento de enlace cuando se hace clic en **el** botón Ayuda.

 

