---
title: Cuadro de diálogo Imprimir
description: El cuadro de diálogo Imprimir permite al usuario seleccionar opciones para un trabajo de impresión determinado.
ms.assetid: 34f69b25-8a89-4322-af4c-a80b85a4a973
keywords:
- Windows Interfaz de usuario,entrada del usuario
- Windows Interfaz de usuario,Common Dialog Box Library
- entrada de usuario, Biblioteca común de cuadros de diálogo
- capturar la entrada del usuario, Biblioteca de cuadros de diálogo común
- Biblioteca común de cuadros de diálogo
- cuadros de diálogo comunes
- Cuadro de diálogo Imprimir
- Instalación de impresión (cuadro de diálogo)
- personalizar el cuadro de diálogo Imprimir
- cuadros de diálogo predefinidos
- cuadros de diálogo, Imprimir
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0afd8cfa31a83f664e859cd93acc9d28543b7ab00dcb8f130fdbac329cd1429e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117720927"
---
# <a name="print-dialog-box"></a>Cuadro de diálogo Imprimir

El **cuadro de** diálogo Imprimir permite al usuario seleccionar opciones para un trabajo de impresión determinado. Por ejemplo, el usuario puede especificar la impresora que se va a usar, el intervalo de páginas que se van a imprimir y el número de copias.

Puede usar la función [**PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) para mostrar una hoja de propiedades de impresión [,](print-property-sheet.md)que tiene una página **General** que contiene controles similares al cuadro **de diálogo** Imprimir. La hoja de propiedades también puede tener páginas de propiedades adicionales específicas de la aplicación y específicas del controlador después de la **página General.**

Para crear y mostrar un **cuadro de diálogo** Imprimir, inicialice una estructura [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) y pase la estructura a la [**función PrintDlg.**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85))

En la ilustración siguiente se muestra un cuadro **de diálogo Imprimir** típico.

![cuadro de diálogo imprimir](images/printdialogboxxp.png)

Si el usuario  hace clic en el botón Aceptar, [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) devuelve **TRUE** y usa la estructura [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) para devolver información sobre las selecciones del usuario. Por ejemplo, los **miembros hDevMode** y **hDevNames** normalmente devuelven identificadores de memoria global para las estructuras [**y DEVNAMES.**](/windows/win32/api/commdlg/ns-commdlg-devnames) Puede usar la información de estas estructuras para crear un contexto de dispositivo o un contexto de información para la impresora seleccionada.

Si el usuario cancela el cuadro **de diálogo** Imprimir o se produce un error, [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) devuelve **FALSE.** Puede determinar la causa de un error mediante la función [**CommDlgExtendedError**](/windows/desktop/api/Commdlg/nf-commdlg-commdlgextendederror) para recuperar el valor de error extendido.

El **cuadro de** diálogo Imprimir incluye un grupo **intervalo** de impresión de botones de radio que indican si el usuario desea imprimir todas las páginas, un intervalo de páginas o solo el texto seleccionado. Antes de [**llamar a PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)), puede establecer una de las marcas **PD \_ ALLPAGES,** **PD \_ SELECTION** o **PD \_ PAGENUMS** para indicar qué botón está seleccionado inicialmente. Cuando **PrintDlg devuelve** **TRUE**, la función establece una de estas marcas para indicar las selecciones del usuario. Si **se establece PD \_ PAGENUMS,** los miembros **nFromPage** y **nToPage** de la estructura [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) contienen las páginas inicial y final especificadas por el usuario. Para deshabilitar el **botón de** radio Pages y sus controles **De** y **Para** editar asociados, establezca la marca **PD \_ NOPAGENUMS.** Para deshabilitar el **botón de** radio Selección, establezca la marca **PD \_ NOSELECTION.**

El cuadro de diálogo incluye un control de edición en el que el usuario puede escribir el número de copias que se imprimirán. Si el **miembro hDevMode** de la estructura [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) no es **NULL,** el **miembro dmCopies** de la estructura especifica el valor inicial para este control de edición. Si **hDevMode** es **NULL,** el **miembro nCopies** de la **estructura PRINTDLG** especifica el valor inicial. Cuando [**PrintDlg devuelve**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) un resultado, **nCopies** suele indicar el número de copias especificado por el usuario. Sin embargo, si establece la marca **\_ PD USEDEVMODECOPIESANDCOLLATE** al crear el cuadro de diálogo, **nCopies** siempre se establece en 1 en la devolución y el miembro **dmCopies** de [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) indica el número de copias que se imprimirán.

La **casilla Intercalar** indica si el usuario desea intercalar las páginas si se imprimen varias copias. La **marca \_ COLLATE de PD** se establece si la casilla **Intercalar** está activada. Si la aplicación no admite varias copias o intercalación simulada, establezca la marca **\_ PD USEDEVMODECOPIESANDCOLLATE** en el miembro **Flags** de la [**estructura PRINTDLG.**](/windows/win32/api/commdlg/ns-commdlg-printdlga) Esto deshabilita la casilla **Intercalar y** el control de edición Número de copias a menos que el controlador de impresora admita varias copias e intercalación. 

La **casilla Imprimir en archivo** indica si el usuario desea enviar la salida a un archivo en lugar de a una impresora. Puede establecer la marca **\_ PD PRINTTOFILE** para que la casilla esté activada inicialmente. Para ocultar la casilla, establezca la **marca \_ HIDEPRINTTOFILE de PD.** Para deshabilitarlo, establezca la **marca \_ PD DISABLEPRINTTOFILE.** Si el usuario  selecciona la opción Imprimir en archivo, [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) establece la marca **\_ PD PRINTTOFILE** y devuelve "FILE:" en el desplazamiento indicado por el miembro **wOutputOffset** de la estructura [**DEVNAMES.**](/windows/win32/api/commdlg/ns-commdlg-devnames) Cuando llame a la función para iniciar la operación de impresión, especifique esta cadena "FILE:" en el **miembro lpszOutput** de la estructura . Al especificar esta cadena, el subsistema de impresión consulta al usuario el nombre del archivo de salida.

De forma predeterminada, el **cuadro de** diálogo Imprimir muestra inicialmente información sobre la impresora predeterminada actual. Para mostrar información de otra impresora instalada, inicialice y una estructura [**DEVNAMES**](/windows/win32/api/commdlg/ns-commdlg-devnames) y asigne el identificador de memoria global a la estructura a los **miembros hDevMode** y **hDevNames.** El nombre del dispositivo que especifique en el miembro **dmDeviceName** de la estructura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) y en el **miembro wDriverOffset** de la estructura **DEVNAMES** debe identificar un dispositivo de impresora que también aparece en la sección Dispositivos del archivo \[ \] Win.ini. Si el dispositivo no aparece, [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) devuelve un error.

Puede dirigir [**PrintDlg para**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) crear un contexto de dispositivo o contexto de información para la impresora estableciendo la marca **PD \_ RETURNDC** o **PD \_ RETURNIC** en el miembro **Flags** de la [**estructura PRINTDLG.**](/windows/win32/api/commdlg/ns-commdlg-printdlga) La función devuelve un identificador al contexto del dispositivo o al contexto de información en el **miembro hDC.** Si usa la marca **\_ PD RETURNDC,** puede usar el contexto del dispositivo para generar la salida de la impresora.

Para recuperar información sobre la impresora predeterminada sin mostrar el **cuadro de** diálogo Imprimir, establezca la marca **PD \_ RETURNDEFAULT.** En este caso, [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) devuelve inmediatamente después de establecer los miembros **hDevMode** y **hDevNames** en identificadores para las estructuras que contienen la información.

De forma predeterminada, [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) muestra cuadros de mensaje cuando se producen errores. Por ejemplo, la función muestra un mensaje de error si no hay ninguna impresora instalada. Para evitar que la función muestre estos mensajes de advertencia, establezca la **\_ marca NOWARNING de PD.**

En esta sección se tratan los temas siguientes.

-   [Personalizar el cuadro de diálogo Imprimir](#customizing-the-print-dialog-box)
-   [Instalación de impresión (cuadro de diálogo)](#print-setup-dialog-box)

## <a name="customizing-the-print-dialog-box"></a>Personalizar el cuadro de diálogo Imprimir

Puede proporcionar una plantilla personalizada para el **cuadro** de diálogo Imprimir, por ejemplo, si desea incluir controles adicionales que sean únicos para la aplicación. La [**función PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) usa la plantilla personalizada en lugar de la plantilla predeterminada.

Para proporcionar una plantilla personalizada para el cuadro **de diálogo** Imprimir:

1.  Cree la plantilla personalizada modificando la plantilla predeterminada especificada en el archivo Prnsetup.dlg. Los identificadores de control usados en la plantilla **de cuadro de** diálogo Imprimir predeterminada se definen en el archivo Dlgs.h.
2.  Use la [**estructura PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) para habilitar la plantilla de la manera siguiente:
    -   Si la plantilla personalizada es un recurso de una aplicación o biblioteca de vínculos dinámicos, establezca la marca **\_ PD ENABLEPRINTTEMPLATE** en el **miembro Flags.** Use los **miembros hInstance** y **lpPrintTemplateName** de la estructura para identificar el módulo y el nombre del recurso.

        -O bien-

    -   Si la plantilla personalizada ya está en memoria, establezca la **\_ marca PD ENABLEPRINTTEMPLATEHANDLE.** Use el **miembro hPrintTemplate** para identificar el objeto de memoria que contiene la plantilla.

Puede proporcionar un procedimiento [**de enlace PrintHookProc**](/windows/win32/api/commdlg/nc-commdlg-lpprinthookproc) para el **cuadro de diálogo** Imprimir. El procedimiento de enlace puede procesar los mensajes enviados al cuadro de diálogo. También puede enviar mensajes al cuadro de diálogo. Si usa una plantilla personalizada para definir controles adicionales, debe proporcionar un procedimiento de enlace para procesar la entrada de los controles.

Para habilitar un procedimiento de enlace para el **cuadro de diálogo** Imprimir:

1.  Establezca la **marca \_ PD ENABLEPRINTHOOK en** el miembro **Flags** de la [**estructura PRINTDLG.**](/windows/win32/api/commdlg/ns-commdlg-printdlga)
2.  Especifique la dirección del procedimiento de enlace en el **miembro lpfnPrintHook.**

Después de procesar [**su mensaje \_ WM INITDIALOG,**](wm-initdialog.md) el procedimiento del cuadro de diálogo envía un mensaje **WM \_ INITDIALOG** al procedimiento de enlace. El *parámetro lParam* de este mensaje es un puntero a la [**estructura PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) utilizada para inicializar el cuadro de diálogo.

## <a name="print-setup-dialog-box"></a>Instalación de impresión (cuadro de diálogo)

Puede crear y mostrar un cuadro de **diálogo Instalación** de impresión estableciendo la marca **PD \_ PRINTSETUP** en una llamada a la [**función PrintDlg.**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) Sin embargo, **el cuadro de diálogo Instalación** de impresión se ha reemplazado por el cuadro de diálogo Configurar página y no debe usarse en nuevas aplicaciones. 

Las marcas siguientes solo se aplican al cuadro **de diálogo Instalación** de impresión:

-   **PD \_ ENABLESETUPHOOK**
-   **PD \_ ENABLESETUPTEMPLATE**
-   **PD \_ ENABLESETUPTEMPLATEHANDLE**

 

 