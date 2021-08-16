---
title: Cuadro de diálogo Fuente
description: El cuadro de diálogo Fuente permite al usuario elegir atributos para una fuente lógica, como familia de fuentes y estilo de fuente asociado, tamaño de punto, efectos (subrayado, tachado y color de texto) y un script (o juego de caracteres).
ms.assetid: e8a996aa-4e34-45d0-a325-9c20b1a6ce07
keywords:
- Windows Interfaz de usuario,entrada del usuario
- Windows Interfaz de usuario,Common Dialog Box Library
- entrada de usuario, Biblioteca común de cuadros de diálogo
- capturar la entrada del usuario, Biblioteca de cuadros de diálogo común
- Biblioteca común de cuadros de diálogo
- cuadros de diálogo comunes
- Fuente (cuadro de diálogo)
- personalizar fuente (cuadro de diálogo)
- flags,Font (cuadro de diálogo)
- marcas de inicialización
- cuadros de diálogo predefinidos
- cuadros de diálogo, Fuente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8544fcb60e499a360f60d1701863a11138d3f16fb06a770a9a2763800d908e12
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118785897"
---
# <a name="font-dialog-box"></a>Cuadro de diálogo Fuente

El **cuadro de** diálogo Fuente permite al usuario elegir atributos para una fuente lógica, como familia de fuentes y estilo de fuente asociado, tamaño de punto, efectos (subrayado, tachado y color de texto) y un script (o juego de caracteres).

Para crear y mostrar un **cuadro de diálogo Fuente,** inicialice una [**estructura CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) y pase la estructura a [**la función ChooseFont.**](/windows/win32/api/commdlg/ns-commdlg-choosefonta)

En la siguiente captura de pantalla se muestra un cuadro **de diálogo Fuente** típico.

![captura de pantalla que muestra el cuadro de diálogo de fuente](images/fontdialogboxxp.png)

Si el usuario hace clic **en** el botón Aceptar, la función [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) devuelve **TRUE** y establece la información sobre la selección del usuario en la [**estructura CHOOSEFONT.**](/windows/win32/api/commdlg/ns-commdlg-choosefonta)

Si el usuario cancela el cuadro de diálogo **Fuente** o se produce un error, [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) devuelve **FALSE** y el contenido de la estructura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) no está definido. Puede determinar la causa de un error mediante la función [**CommDlgExtendedError**](/windows/desktop/api/Commdlg/nf-commdlg-commdlgextendederror) para recuperar el valor de error extendido.

En esta sección se tratan los temas siguientes.

-   [Marcas de inicialización del cuadro de diálogo Fuente](#font-dialog-box-initialization-flags)
-   [Personalizar el cuadro de diálogo Fuente en versiones anteriores de Windows](#customizing-the-font-dialog-box-on-earlier-versions-of-windows)
-   [Personalización del cuadro de diálogo Fuente en Windows 7](#customizing-the-font-dialog-box-on-windows-7)

## <a name="font-dialog-box-initialization-flags"></a>Marcas de inicialización del cuadro de diálogo Fuente

Antes de llamar [**a ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta), el miembro **Flags** de la estructura CHOOSEFONT debe especificar **CF \_ SCREENFONTS,** CF **\_ PRINTERFONTS** o **CF \_ BOTH** para indicar si el cuadro de diálogo debe mostrar fuentes de pantalla, fuentes de impresora o ambas. [](/windows/win32/api/commdlg/ns-commdlg-choosefonta) Si especifica **CF \_ PRINTERFONTS** o **CF \_ BOTH**, el **miembro hDC** de la estructura **CHOOSEFONT** debe especificar un identificador para un contexto de dispositivo para la impresora.

Si se **establece la marca CF \_ PRINTERFONTS** o **CF \_ BOTH,** la etiqueta de descripción del tipo de fuente aparece en la parte inferior del **cuadro de** diálogo Fuente.

A partir de Windows 7, las marcas **\_ CF PRINTERFONTS,** **CF \_ SCREENFONTS,** **CF \_ BOTH** y **CF \_ WYSIWYG** ya no se usan en la función [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) para la enumeración de fuentes. Están obsoletos en Windows 7. Sin embargo, **la marca \_ PRINTERFONTS de CF** conserva una función: para mostrar la etiqueta de descripción del tipo de fuente en la parte inferior del cuadro **de** diálogo Fuente.

Puede usar el miembro **Flags** para habilitar  o deshabilitar algunos de los controles de cuadro de diálogo Fuente y puede usar el miembro **Flags** junto con otros miembros [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) para controlar los valores iniciales de algunos controles.

**Para mostrar los controles que permiten al usuario seleccionar opciones de tachado, subrayado y color:**

-   Establezca la **marca CF \_ EFFECTS.** Puede usar el miembro **rgbColors** de la [**estructura CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) para especificar un color de fuente inicial.

**Para especificar los valores iniciales de los controles de cuadro de diálogo Fuente, Estilo de fuente, Tamaño, Tachador y Subrayado:**

1.  Para especificar los valores iniciales de los controles de cuadro de diálogo Fuente, Estilo de fuente, Tamaño, Tachador y Subrayado:
2.  Establezca la marca **CF \_ INITTOLOGFONTSTRUCT** en el miembro **Flags,** junto con los miembros de la estructura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) a la que apunta **lpLogFont**, para especificar los valores iniciales de los atributos de fuente.
3.  También puede usar las marcas **CF \_ NOFACESEL**, **CF \_ NOSTYLESEL** y  **CF \_ NOSIZESEL** para evitar que el cuadro de diálogo Fuente muestre los valores iniciales de los controles correspondientes. Esto resulta útil cuando se trabaja con una selección de texto que tiene más de un tipo de letra, estilo o tamaño de punto. Estos valores también se establecerán en **Marcas cuando** se devuelva [**ChooseFont,**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) si el usuario no ha seleccionado un valor correspondiente.

**Para inicializar el control Estilo de fuente en un nombre de estilo especificado**

-   Establezca la **marca \_ USESTYLE de CF** y use el miembro **lpszStyle** para especificar el nombre del estilo.

> [!Note]  
> Para globalizar la aplicación, especifique el estilo mediante los miembros **lfWeight** y **lfItalic** de la estructura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) a la que **apunta lpLogFont**. El nombre de estilo puede cambiar en función del idioma de la interfaz de usuario del sistema.

 

**Para mostrar el botón Aplicar**

-   Establezca la **marca CF \_ APPLY** y proporcione un procedimiento de enlace para procesar [**mensajes WM \_ COMMAND**](/windows/desktop/menurc/wm-command) para el **botón** Aplicar. El procedimiento de enlace puede enviar el mensaje [**\_ \_ GETLOGFONT**](wm-choosefont-getlogfont.md) de WM CHOOSEFONT al cuadro de diálogo para recuperar la dirección de la estructura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) que contiene las selecciones actuales para la fuente.

**Para mostrar el botón Ayuda**

-   Establezca la **marca \_ SHOWHELP de CF.** El **miembro hwndOwner** debe identificar la ventana para recibir el mensaje registrado [**HELPMSGSTRING**](helpmsgstring.md) cuando el usuario hace clic en el **botón Ayuda.**

**Para restringir las fuentes que se muestran en el cuadro de diálogo**

-   Establezca cualquier combinación de las marcas **CF \_ TTONLY**, **CF \_ FIXEDPITFONTLY**, **CF \_ NOVECTORFONTS**, **CF \_ NOVERTFONTS,** **CF \_ SCALABLEONLY** y **CF \_ WYSIWYG.** También puede restringir los estilos disponibles que muestra el cuadro de diálogo para algunas fuentes mediante el **valor \_ CF NOSIMULATIONS.**

A partir Windows 7, la lista de fuentes que se muestran en el cuadro de diálogo está restringida en función de las fuentes mostradas por el usuario. Para quitar la restricción, establezca la **marca CF \_ INACTIVEFONTS.**

**Para restringir los nombres de tipo de letra, los estilos y los tamaños de punto que el usuario puede especificar**

1.  Establezca la **marca \_ CF FORCEFONTEXIST** para restringir al usuario la especificación solo de nombres de tipo de letra, estilos y tamaños de punto válidos enumerados en el cuadro de diálogo.
2.  Establezca la **marca \_ CF LIMITSIZE** para restringir al usuario la especificación de tamaños de punto en el intervalo especificado por los miembros **nSizeMin** y **nSizeMax.**

**Para restringir o deshabilitar el cuadro combinado Scripts**

-   Establezca la **marca \_ CF NOSCRIPTSEL** para deshabilitar el cuadro combinado **Scripts** o establezca la marca **CF \_ SELECTSCRIPT** para restringir las selecciones del cuadro combinado **Scripts** a un juego de caracteres especificado.

## <a name="customizing-the-font-dialog-box-on-earlier-versions-of-windows"></a>Personalizar el cuadro de diálogo Fuente en versiones anteriores de Windows

Puede proporcionar una plantilla  personalizada para el cuadro de diálogo Fuente, por ejemplo, si desea incluir controles adicionales que son únicos para la aplicación. La [**función ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) usa la plantilla personalizada en lugar de la plantilla predeterminada.

**Para proporcionar una plantilla personalizada para el cuadro de diálogo Fuente**

1.  Cree la plantilla personalizada modificando la plantilla predeterminada especificada en el archivo Font.dlg. Los identificadores de control usados en la plantilla de cuadro de diálogo Fuente predeterminada se definen en el archivo Dlgs.h.
2.  Use la [**estructura CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) para habilitar la plantilla de la siguiente manera:
    -   Si la plantilla personalizada es un recurso de una aplicación o biblioteca de vínculos dinámicos, establezca la marca **\_ ENABLETEMPLATE** de CF en el **miembro Flags.** Use los **miembros hInstance** y **lpTemplateName** de la estructura para identificar el módulo y el nombre del recurso.
    -   Si la plantilla personalizada ya está en memoria, establezca la **\_ marca ENABLETEMPLATEHANDLE de CF.** Use el **miembro hInstance** para identificar el objeto de memoria que contiene la plantilla.

Puede proporcionar un procedimiento [**de enlace CFHookProc**](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc) para el cuadro **de diálogo** Fuente . El procedimiento de enlace puede procesar los mensajes enviados al cuadro de diálogo y enviar mensajes al cuadro de diálogo. Si usa una plantilla personalizada para definir controles adicionales, debe proporcionar un procedimiento de enlace para procesar la entrada de los controles.

**Para habilitar un procedimiento de enlace para el cuadro de diálogo Fuente**

1.  Establezca la **marca \_ CF ENABLEHOOK** en el **miembro Flags** de la [**estructura CHOOSEFONT.**](/windows/win32/api/commdlg/ns-commdlg-choosefonta)
2.  Especifique la dirección del procedimiento de enlace en el **miembro lpfnHook.**

Después de procesar [**el mensaje \_ WM INITDIALOG,**](wm-initdialog.md) el procedimiento del cuadro de diálogo envía un **mensaje WM \_ INITDIALOG** al procedimiento de enlace. El *parámetro lParam* de este mensaje es un puntero a la [**estructura CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) que se usa para inicializar el cuadro de diálogo.

El procedimiento de enlace puede enviar los mensajes [**WM \_ CHOOSEFONT \_ GETLOGFONT,**](wm-choosefont-getlogfont.md) [**WM \_ CHOOSEFONT \_ SETLOGFONT**](wm-choosefont-setlogfont.md)y [**WM \_ CHOOSEFONT \_ SETFLAGS**](wm-choosefont-setflags.md) al cuadro de diálogo para obtener y establecer los valores y marcas actuales del cuadro de diálogo.

## <a name="customizing-the-font-dialog-box-on-windows-7"></a>Personalización del cuadro de diálogo Fuente en Windows 7

En la siguiente captura de pantalla se muestra un cuadro **de diálogo** Fuente típico Windows 7.

![captura de pantalla que muestra el cuadro dialob de fuente](images/fontdialogboxwin7.png)

En versiones Windows anteriores, el archivo de plantilla font.dlg contiene una plantilla ChooseFont predeterminada. El archivo de plantilla font.dlg de Windows 7 contiene dos plantillas predeterminadas: la plantilla predeterminada de versiones anteriores de Windows y la nueva plantilla ChooseFont Windows 7. Por lo tanto, al personalizar el **cuadro de** diálogo Fuente Windows 7, debe tener en cuenta los siguientes problemas.

1.  Use la nueva plantilla al crear plantillas personalizadas para las aplicaciones que se ejecutan Windows 7. Esta nueva plantilla contiene un control de vínculo en el que el usuario puede hacer clic para iniciar la ventana **Fuentes Panel de control,** como se muestra en la siguiente captura de pantalla.

    ![captura de pantalla que muestra el panel de control de fuentes en Windows 7](images/fontcontrolpanelforwin7.png)

2.  Para usar este control de vínculo, la aplicación que realiza la llamada debe usar COMCTL32.DLL versión 6 o posterior. De lo contrario, [**la función ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) devuelve un error cuando intenta crear el control de vínculo en la plantilla personalizada. Para determinar si este control está habilitado, compile la aplicación que realiza la llamada COMCTL32.DLL versión 6.0. Para obtener más información, vea [Habilitar estilos visuales con controles comunes.](/previous-versions//ms649781(v=vs.85))
3.  Si la aplicación usa COMCTL32.DLL versión 5.0 o anterior, debe hacer lo siguiente al crear una plantilla personalizada:

    -   Especifique el control como **PUSHBUTTON.** El control que se usa para iniciar **Panel de control** fuentes aparecerá como un botón en lugar de como un vínculo.
    -   Reemplace el texto siguiente en font.dlg:

        `CONTROL         "<A>Show more fonts</A>", IDC_MANAGE_LINK, "SysLink", WS_TABSTOP, 7, 199, 227, 9`

        con el texto siguiente:

        `PUSHBUTTON      "S&how more fonts", IDC_MANAGE_LINK, 7, 199, 74, 14 , WS_TABSTOP`

    -   Para asegurarse de que la aplicación usa una plantilla personalizada, debe especificar una plantilla personalizada con la marca **\_ CF ENABLETEMPLATE,** crear una plantilla personalizada basada en la plantilla ChooseFont de Windows 7 y, opcionalmente, habilitar un procedimiento de enlace.

        Si habilita un procedimiento de enlace sin crear una plantilla personalizada, se cargará la plantilla ChooseFont predeterminada para versiones Windows anteriores.

> [!Note]  
> Debe especificar el tipo **de control CONTROL** o **PUSHBUTTON** en la nueva plantilla, en función de la versión de COMMCTL.DLL con la que se compila la aplicación. Tenga en cuenta también que Windows 7 características específicas, como la presentación WYSIWYG de listas de fuentes y familias extendidas, no están disponibles cuando las aplicaciones se ejecutan en versiones anteriores del sistema operativo Windows.

 

 

 