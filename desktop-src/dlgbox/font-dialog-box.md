---
title: Cuadro de diálogo Fuente
description: El cuadro de diálogo fuente permite al usuario elegir atributos para una fuente lógica, como la familia de fuentes y el estilo de fuente asociado, el tamaño de los puntos, los efectos (subrayado, tachado y color del texto) y un script (o juego de caracteres).
ms.assetid: e8a996aa-4e34-45d0-a325-9c20b1a6ce07
keywords:
- Interfaz de usuario de Windows, entrada de usuario
- Interfaz de usuario de Windows, biblioteca de cuadros de diálogo comunes
- entrada de usuario, biblioteca de cuadros de diálogo comunes
- capturar la entrada del usuario, la biblioteca de cuadros de diálogo comunes
- Biblioteca de cuadros de diálogo comunes
- cuadros de diálogo comunes
- Fuente (cuadro de diálogo)
- cuadro de diálogo Personalizar fuente
- marcas, fuente (cuadro de diálogo)
- marcas de inicialización
- cuadros de diálogo predefinidos
- cuadros de diálogo, fuente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9a752ce53ecf496c58efb0c346a8c3d67c4f1b1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078305"
---
# <a name="font-dialog-box"></a>Cuadro de diálogo Fuente

El cuadro de diálogo **fuente** permite al usuario elegir atributos para una fuente lógica, como la familia de fuentes y el estilo de fuente asociado, el tamaño de los puntos, los efectos (subrayado, tachado y color del texto) y un script (o juego de caracteres).

Puede crear y mostrar un cuadro de diálogo de **fuente** inicializando una estructura [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) y pasando la estructura a la función [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) .

En la captura de pantalla siguiente se muestra un cuadro de diálogo de **fuente** típico.

![captura de pantalla que muestra el cuadro de diálogo fuente](images/fontdialogboxxp.png)

Si el usuario hace clic en el botón **Aceptar** , la función [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) devuelve **true** y establece la información sobre la selección del usuario en la estructura [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) .

Si el usuario cancela el cuadro de diálogo **fuente** o se produce un error, [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) devuelve **false** y no se define el contenido de la estructura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) . Puede determinar la causa de un error mediante la función [**CommDlgExtendedError**](/windows/desktop/api/Commdlg/nf-commdlg-commdlgextendederror) para recuperar el valor de error extendido.

Los temas siguientes se describen en esta sección.

-   [Marcas de inicialización del cuadro de diálogo fuente](#font-dialog-box-initialization-flags)
-   [Personalizar el cuadro de diálogo fuente en versiones anteriores de Windows](#customizing-the-font-dialog-box-on-earlier-versions-of-windows)
-   [Personalización del cuadro de diálogo fuente en Windows 7](#customizing-the-font-dialog-box-on-windows-7)

## <a name="font-dialog-box-initialization-flags"></a>Marcas de inicialización del cuadro de diálogo fuente

Antes de llamar a [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta), el miembro **Flags** de la estructura [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) debe especificar **CF \_ SCREENFONTS**, **CF \_ PRINTERFONTS** o **CF \_ both** para indicar si el cuadro de diálogo debe mostrar fuentes de pantalla, fuentes de impresora o ambos. Si especifica **CF \_ PRINTERFONTS** o **CF en \_ ambos**, el miembro **HDC** de la estructura **CHOOSEFONT** debe especificar un identificador de un contexto de dispositivo para la impresora.

Si se establece la marca **CF \_ PRINTERFONTS** o **CF \_ both** , la etiqueta tipo de fuente Descripción aparece en la parte inferior del cuadro de diálogo **fuente** .

A partir de Windows 7, las marcas **CF \_ PRINTERFONTS**, **CF \_ SCREENFONTS**, **CF \_** y **CF \_ WYSIWYG** ya no se usan en la función [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) para la enumeración de fuentes. Están obsoletas en Windows 7. Sin embargo, la marca **CF \_ PRINTERFONTS** conserva una función: para mostrar la etiqueta de Descripción del tipo de fuente en la parte inferior del cuadro de diálogo **fuente** .

Puede usar el miembro **Flags** para habilitar o deshabilitar algunos de los controles de cuadro de diálogo **fuente** , y puede usar el miembro **Flags** junto con otros miembros [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) para controlar los valores iniciales de algunos controles.

**Para mostrar los controles que permiten al usuario seleccionar las opciones de tachado, subrayado y color:**

-   Establezca la marca de **\_ efectos de CF** . Puede usar el miembro **rgbColors** de la estructura [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) para especificar un color de fuente inicial.

**Para especificar los valores iniciales de los controles de cuadro de diálogo fuente, estilo de fuente, tamaño, tachado y subrayado:**

1.  Para especificar los valores iniciales de los controles de cuadro de diálogo fuente, estilo de fuente, tamaño, tachado y subrayado:
2.  Establezca la **marca CF \_ INITTOLOGFONTSTRUCT** en el miembro **Flags** , junto con los miembros de la estructura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) a los que apunta **lpLogFont**, para especificar los valores iniciales de los atributos de fuente.
3.  También puede usar las marcas **CF \_ NOFACESEL**, **CF \_ NOSTYLESEL** y **CF \_ NOSIZESEL** para impedir que el cuadro de diálogo **fuente** muestre los valores iniciales de los controles correspondientes. Esto resulta útil cuando se trabaja con una selección de texto que tiene más de un tipo de letra, estilo o tamaño de punto. Estos valores también se establecerán en **marcas** cuando [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) devuelva, si el usuario no ha seleccionado un valor correspondiente.

**Para inicializar el control de estilo de fuente en un nombre de estilo especificado**

-   Establezca la marca **CF \_ USESTYLE** y use el miembro **lpszStyle** para especificar el nombre de estilo.

> [!Note]  
> Para globalizar la aplicación, especifique el estilo mediante los miembros **lfWeight** y **lfItalic** de la estructura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) a la que apunta **lpLogFont**. El nombre de estilo puede cambiar en función del idioma de la interfaz de usuario del sistema.

 

**Para mostrar el botón aplicar**

-   Establezca la marca **CF \_ Apply** y proporcione un procedimiento de enlace para procesar los mensajes de [**\_ comando de WM**](/windows/desktop/menurc/wm-command) para el botón **aplicar** . El procedimiento de enlace puede enviar el mensaje de [**\_ CHOOSEFONT \_ GETLOGFONT de WM**](wm-choosefont-getlogfont.md) al cuadro de diálogo para recuperar la dirección de la estructura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) que contiene las selecciones actuales de la fuente.

**Para mostrar el botón ayuda**

-   Establezca la marca **CF \_ SHOWHELP** . El miembro **hwndOwner** debe identificar la ventana que recibirá el mensaje registrado [**HELPMSGSTRING**](helpmsgstring.md) cuando el usuario haga clic en el botón **ayuda** .

**Para restringir las fuentes que se muestran en el cuadro de diálogo**

-   Establezca cualquier combinación de las **marcas \_ CF TTONLY**, **CF \_ FIXEDPITCHONLY**, **CF \_ NOVECTORFONTS**, **CF \_ NOVERTFONTS**, **CF \_ SCALABLEONLY** y **CF \_ WYSIWYG** . También puede restringir los estilos disponibles que el cuadro de diálogo muestra para algunas fuentes mediante el valor de **CF \_ nosimulations** .

A partir de Windows 7, la lista de fuentes que se muestran en el cuadro de diálogo se restringe según las fuentes mostradas del usuario. Para quitar la restricción, establezca la marca **CF \_ INACTIVEFONTS** .

**Para restringir los nombres de tipo de letra, los estilos y los tamaños de punto que el usuario puede especificar**

1.  Establezca la marca **CF \_ FORCEFONTEXIST** para restringir al usuario que solo especifique nombres de tipo de letra válidos, estilos y tamaños de punto que se enumeran en el cuadro de diálogo.
2.  Establezca la marca de **\_ límite de CF** para impedir que el usuario especifique los tamaños de punto en el intervalo especificado por los miembros **nSizeMin** y **nSizeMax** .

**Para restringir o deshabilitar el cuadro combinado scripts**

-   Establezca la **marca CF \_ NOSCRIPTSEL** en deshabilitar el cuadro combinado **scripts** o establezca la marca **CF \_ SELECTSCRIPT** para restringir selecciones en el cuadro combinado **scripts** a un juego de caracteres especificado.

## <a name="customizing-the-font-dialog-box-on-earlier-versions-of-windows"></a>Personalizar el cuadro de diálogo fuente en versiones anteriores de Windows

Puede proporcionar una plantilla personalizada para el cuadro de diálogo **fuente** , por ejemplo, si desea incluir controles adicionales que son exclusivos de la aplicación. La función [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) usa la plantilla personalizada en lugar de la plantilla predeterminada.

**Para proporcionar una plantilla personalizada para el cuadro de diálogo fuente**

1.  Cree la plantilla personalizada modificando la plantilla predeterminada especificada en el archivo font. Dlg. Los identificadores de control usados en la plantilla de cuadro de diálogo de fuente predeterminada se definen en el archivo Dlgs. h.
2.  Use la estructura [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) para habilitar la plantilla de la manera siguiente:
    -   Si la plantilla personalizada es un recurso de una aplicación o una biblioteca de vínculos dinámicos, establezca la marca **CF \_ ENABLETEMPLATE** en el miembro **Flags** . Use los miembros **hInstance** y **lpTemplateName** de la estructura para identificar el nombre del módulo y del recurso.
    -   Si la plantilla personalizada ya está en la memoria, establezca la marca **CF \_ ENABLETEMPLATEHANDLE** . Use el miembro **hInstance** para identificar el objeto de memoria que contiene la plantilla.

Puede proporcionar un procedimiento de enlace [**CFHookProc**](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc) para el cuadro de diálogo **fuente** . El procedimiento de enlace puede procesar los mensajes enviados al cuadro de diálogo y enviar mensajes al cuadro de diálogo. Si usa una plantilla personalizada para definir controles adicionales, debe proporcionar un procedimiento de enlace para procesar la entrada para los controles.

**Para habilitar un procedimiento de enlace para el cuadro de diálogo fuente**

1.  Establezca la marca **CF \_ ENABLEHOOK** en el miembro **Flags** de la estructura [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) .
2.  Especifique la dirección del procedimiento de enlace en el miembro **lpfnHook** .

Después de procesar el mensaje de [**\_ INITDIALOG de WM**](wm-initdialog.md) , el procedimiento de cuadro de diálogo envía un mensaje de **WM \_ INITDIALOG** al procedimiento de enlace. El parámetro *lParam* de este mensaje es un puntero a la estructura [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) que se usa para inicializar el cuadro de diálogo.

El procedimiento de enlace puede enviar los mensajes [**WM \_ CHOOSEFONT \_ GETLOGFONT**](wm-choosefont-getlogfont.md), [**WM \_ CHOOSEFONT \_ SETLOGFONT**](wm-choosefont-setlogfont.md)y [**WM \_ CHOOSEFONT \_ SETFLAGS**](wm-choosefont-setflags.md) al cuadro de diálogo para obtener y establecer los valores actuales y los marcadores del cuadro de diálogo.

## <a name="customizing-the-font-dialog-box-on-windows-7"></a>Personalización del cuadro de diálogo fuente en Windows 7

En la captura de pantalla siguiente se muestra un cuadro de diálogo de **fuente** típico en Windows 7.

![captura de pantalla que muestra el cuadro fuente dialob](images/fontdialogboxwin7.png)

En versiones anteriores de Windows, el archivo de plantilla Font. Dlg contiene una plantilla ChooseFont predeterminada. El archivo de plantilla Font. Dlg en Windows 7 contiene dos plantillas predeterminadas: la predeterminada de las versiones anteriores de Windows y la nueva plantilla ChooseFont de Windows 7. Por lo tanto, cuando Personalice el cuadro de diálogo **fuente** en Windows 7, debe tener en cuenta los siguientes problemas.

1.  Use la nueva plantilla al crear plantillas personalizadas para las aplicaciones que se ejecutan en Windows 7. Esta nueva plantilla contiene un control de vínculo en el que el usuario puede hacer clic para iniciar la ventana **fuentes del panel de control** , como se muestra en la siguiente captura de pantalla.

    ![captura de pantalla que muestra el panel de control fuente en Windows 7](images/fontcontrolpanelforwin7.png)

2.  Para usar este control de vínculo, la aplicación que realiza la llamada debe usar la COMCTL32.DLL versión 6 o posterior. De lo contrario, la función [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) devuelve un error cuando intenta crear el control de vínculo en la plantilla personalizada. Para determinar si este control está habilitado, compile la aplicación que realiza la llamada en COMCTL32.DLL versión 6,0. Para obtener más información, vea [habilitar estilos visuales con controles comunes](/previous-versions//ms649781(v=vs.85)).
3.  Si la aplicación usa COMCTL32.DLL versión 5,0 o anterior, debe hacer lo siguiente al crear una plantilla personalizada:

    -   Especifique el control como un **pulsador**. El control usado para iniciar el **Panel de control fuentes** aparecerá como un botón en lugar de como un vínculo.
    -   Reemplace el texto siguiente en la fuente. Dlg:

        `CONTROL         "<A>Show more fonts</A>", IDC_MANAGE_LINK, "SysLink", WS_TABSTOP, 7, 199, 227, 9`

        con el siguiente texto:

        `PUSHBUTTON      "S&how more fonts", IDC_MANAGE_LINK, 7, 199, 74, 14 , WS_TABSTOP`

    -   Para asegurarse de que la aplicación usa una plantilla personalizada, debe especificar una plantilla personalizada con la marca **CF \_ ENABLETEMPLATE** , crear una plantilla personalizada basada en la plantilla ChooseFont de Windows 7 y, a continuación, habilitar opcionalmente un procedimiento de enlace.

        Si habilita un procedimiento de enlace sin crear una plantilla personalizada, se cargará la plantilla predeterminada de ChooseFont para versiones anteriores de Windows.

> [!Note]  
> Debe especificar el tipo de control **control** o **PUSHBUTTON** en la nueva plantilla, en función de la versión de COMMCTL.DLL con la que se compile la aplicación. Tenga en cuenta también que las características específicas de Windows 7, como la presentación WYSIWYG de listas de fuentes y familias extendidas, no están disponibles cuando las aplicaciones se ejecutan en versiones anteriores del sistema operativo Windows.

 

 

 