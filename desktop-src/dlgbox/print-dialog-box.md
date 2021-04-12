---
title: Cuadro de diálogo Imprimir
description: El cuadro de diálogo Imprimir permite al usuario seleccionar opciones para un trabajo de impresión determinado.
ms.assetid: 34f69b25-8a89-4322-af4c-a80b85a4a973
keywords:
- Interfaz de usuario de Windows, entrada de usuario
- Interfaz de usuario de Windows, biblioteca de cuadros de diálogo comunes
- entrada de usuario, biblioteca de cuadros de diálogo comunes
- capturar la entrada del usuario, la biblioteca de cuadros de diálogo comunes
- Biblioteca de cuadros de diálogo comunes
- cuadros de diálogo comunes
- Cuadro de diálogo Imprimir
- Cuadro de diálogo Configurar impresión
- personalizar cuadro de diálogo Imprimir
- cuadros de diálogo predefinidos
- cuadros de diálogo, imprimir
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fae1dd244391ea16478a0cb4f10803cf622dc64
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149602"
---
# <a name="print-dialog-box"></a>Cuadro de diálogo Imprimir

El cuadro de diálogo **Imprimir** permite al usuario seleccionar opciones para un trabajo de impresión determinado. Por ejemplo, el usuario puede especificar la impresora que se va a usar, el intervalo de páginas que se va a imprimir y el número de copias.

Puede usar la función [**PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) para mostrar una [hoja de propiedades de impresión](print-property-sheet.md), que tiene una página **General** que contiene controles similares al cuadro de diálogo **Imprimir** . La hoja de propiedades también puede tener páginas de propiedades adicionales específicas de la aplicación y específicas del controlador después de la página **General** .

Para crear y mostrar un cuadro de diálogo de **impresión** , inicialice una estructura [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) y pase la estructura a la función [**PRINTDLG**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) .

En la ilustración siguiente se muestra un cuadro de diálogo de **impresión** típico.

![cuadro de diálogo Imprimir](images/printdialogboxxp.png)

Si el usuario hace clic en el botón **Aceptar** , [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) devuelve **true** y usa la estructura [**PrintDlg**](/windows/win32/api/commdlg/ns-commdlg-printdlga) para devolver información sobre las selecciones del usuario. Por ejemplo, los miembros **hDevMode** y **hDevNames** normalmente devuelven los identificadores de memoria globales para las estructuras y [**DEVNAMES**](/windows/win32/api/commdlg/ns-commdlg-devnames) . Puede usar la información de estas estructuras para crear un contexto de dispositivo o un contexto de información para la impresora seleccionada.

Si el usuario cancela el cuadro de diálogo **Imprimir** o se produce un error, [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) devuelve **false**. Puede determinar la causa de un error mediante la función [**CommDlgExtendedError**](/windows/desktop/api/Commdlg/nf-commdlg-commdlgextendederror) para recuperar el valor de error extendido.

El cuadro de diálogo **Imprimir** incluye un grupo de **intervalo de impresión** de botones de radio que indican si el usuario desea imprimir todas las páginas, un intervalo de páginas o solo el texto seleccionado. Antes de llamar a [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)), puede establecer una de las marcas **PD \_ ALLPAGES**, **PD \_ Selection** o **PD \_ PAGENUMS** para indicar qué botón está seleccionado inicialmente. Cuando **PrintDlg** devuelve **true**, la función establece una de estas marcas para indicar las selecciones del usuario. Si se establece **PD \_ PAGENUMS** , los miembros **nFromPage** y **nToPage** de la estructura [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) contienen las páginas de inicio y finalización especificadas por el usuario. Para deshabilitar el botón **de** radio **páginas** y su asociado de y **a** los controles de edición, establezca la marca **PD \_ NOPAGENUMS** . Para deshabilitar el botón de radio **selección** , establezca la marca **PD \_ noselect** .

El cuadro de diálogo incluye un control de edición en el que el usuario puede escribir el número de copias que se van a imprimir. Si el miembro **hDevMode** de la estructura [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) no es **null**, el miembro **dmCopies** de la estructura especifica el valor inicial de este control de edición. Si **hDevMode** es **null**, el miembro **nCopies** de la estructura **PRINTDLG** especifica el valor inicial. Cuando [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) devuelve, **nCopies** normalmente indica el número de copias especificadas por el usuario. Sin embargo, si se establece la marca **PD \_ USEDEVMODECOPIESANDCOLLATE** al crear el cuadro de diálogo, **nCopies** siempre se establece en 1 en la devolución y el miembro **dmCopies** de [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) indica el número de copias que se van a imprimir.

La casilla **intercalar** indica si el usuario desea intercalar las páginas si se imprimen varias copias. La marca de **\_ Intercalación PD** se establece si la casilla **intercalar** está activada. Si la aplicación no admite varias copias o intercalación simulada, establezca la marca **PD \_ USEDEVMODECOPIESANDCOLLATE** en el miembro **Flags** de la estructura [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) . Esto deshabilita la casilla de verificación **intercalar** y el control **de edición número de copias** , a menos que el controlador de impresora admita varias copias e intercalación.

La casilla **imprimir en archivo** indica si el usuario desea enviar la salida a un archivo en lugar de a una impresora. Puede establecer la marca **PD \_ PRINTTOFILE** de modo que la casilla esté activada inicialmente. Para ocultar la casilla, establezca la marca **PD \_ HIDEPRINTTOFILE** . Para deshabilitarlo, establezca la marca **PD \_ DISABLEPRINTTOFILE** . Si el usuario selecciona la opción **imprimir a un archivo** , [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) establece la marca **PD \_ PRINTTOFILE** y devuelve "File:" en el desplazamiento indicado por el miembro **wOutputOffset** de la estructura [**DEVNAMES**](/windows/win32/api/commdlg/ns-commdlg-devnames) . Cuando llame a la función para iniciar la operación de impresión, especifique la cadena "FILE:" en el miembro **lpszOutput** de la estructura. Al especificar esta cadena, el subsistema de impresión consulta al usuario el nombre del archivo de salida.

De forma predeterminada, el cuadro de diálogo **Imprimir** muestra información sobre la impresora predeterminada actual. Para mostrar información de otra impresora instalada, inicialice y una estructura [**DEVNAMES**](/windows/win32/api/commdlg/ns-commdlg-devnames) y asigne el identificador de memoria global a la estructura a los miembros **hDevMode** y **hDevNames** . El nombre del dispositivo que especifique en el miembro **dmDeviceName** de la estructura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) y en el miembro **wDriverOffset** de la estructura **DEVNAMES** debe identificar un dispositivo de impresora que también aparezca en \[ la \] sección dispositivos del archivo de Win.ini. Si el dispositivo no aparece en la lista, [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) devuelve un error.

Puede dirigir [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) para crear un contexto de información o contexto de dispositivo para la impresora mediante el establecimiento de la **marca \_ devuelta** de **PD \_ RETURNDC** o PD en el miembro **Flags** de la estructura [**PrintDlg**](/windows/win32/api/commdlg/ns-commdlg-printdlga) . La función devuelve un identificador para el contexto del dispositivo o el contexto de información en el miembro **HDC** . Si usa la marca **PD \_ RETURNDC** , puede utilizar el contexto de dispositivo para generar la salida de la impresora.

Para recuperar información acerca de la impresora predeterminada sin mostrar el cuadro de diálogo **Imprimir** , establezca la marca **PD \_ RETURNDEFAULT** . En este caso, [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) devuelve inmediatamente después de establecer los miembros **hDevMode** y **hDevNames** en los identificadores de las estructuras que contienen la información.

De forma predeterminada, [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) muestra cuadros de mensaje cuando se producen errores. Por ejemplo, la función muestra un mensaje de error si no hay ninguna impresora instalada. Para evitar que la función muestre estos mensajes de advertencia, establezca la marca **PD \_ nowarning** .

Los temas siguientes se describen en esta sección.

-   [Personalización del cuadro de diálogo Imprimir](#customizing-the-print-dialog-box)
-   [Cuadro de diálogo Configurar impresión](#print-setup-dialog-box)

## <a name="customizing-the-print-dialog-box"></a>Personalización del cuadro de diálogo Imprimir

Puede proporcionar una plantilla personalizada para el cuadro de diálogo **Imprimir** , por ejemplo, si desea incluir controles adicionales que sean únicos para la aplicación. La función [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) usa la plantilla personalizada en lugar de la plantilla predeterminada.

Para proporcionar una plantilla personalizada para el cuadro de diálogo **Imprimir** :

1.  Cree la plantilla personalizada modificando la plantilla predeterminada especificada en el archivo prnsetup. Dlg. Los identificadores de control que se usan en la plantilla de cuadro de diálogo de **impresión** predeterminada se definen en el archivo Dlgs. h.
2.  Use la estructura [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) para habilitar la plantilla de la manera siguiente:
    -   Si la plantilla personalizada es un recurso de una biblioteca de vínculos dinámicos o de aplicación, establezca la marca **PD \_ ENABLEPRINTTEMPLATE** en el miembro **Flags** . Use los miembros **hInstance** y **lpPrintTemplateName** de la estructura para identificar el nombre del módulo y del recurso.

        -O bien-

    -   Si la plantilla personalizada ya está en la memoria, establezca la marca **PD \_ ENABLEPRINTTEMPLATEHANDLE** . Use el miembro **hPrintTemplate** para identificar el objeto de memoria que contiene la plantilla.

Puede proporcionar un procedimiento de enlace [**PrintHookProc**](/windows/win32/api/commdlg/nc-commdlg-lpprinthookproc) para el cuadro de diálogo **Imprimir** . El procedimiento de enlace puede procesar los mensajes enviados al cuadro de diálogo. También puede enviar mensajes al cuadro de diálogo. Si usa una plantilla personalizada para definir controles adicionales, debe proporcionar un procedimiento de enlace para procesar la entrada para los controles.

Para habilitar un procedimiento de enlace para el cuadro de diálogo **Imprimir** :

1.  Establezca la marca **PD \_ ENABLEPRINTHOOK** en el miembro **Flags** de la estructura [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) .
2.  Especifique la dirección del procedimiento de enlace en el miembro **lpfnPrintHook** .

Después de procesar el mensaje de [**\_ INITDIALOG de WM**](wm-initdialog.md) , el procedimiento de cuadro de diálogo envía un mensaje de **WM \_ INITDIALOG** al procedimiento de enlace. El parámetro *lParam* de este mensaje es un puntero a la estructura [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) que se usa para inicializar el cuadro de diálogo.

## <a name="print-setup-dialog-box"></a>Cuadro de diálogo Configurar impresión

Puede crear y mostrar un cuadro de diálogo de **configuración de impresión** estableciendo la marca **PD \_ PRINTSETUP** en una llamada a la función [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) . Sin embargo, el cuadro de diálogo Configuración de **impresión** ha sido sustituido por el cuadro de diálogo **Configurar página** y no debe usarse en aplicaciones nuevas.

Las marcas siguientes solo se aplican al cuadro de diálogo **Configurar impresión** :

-   **PD \_ ENABLESETUPHOOK**
-   **PD \_ ENABLESETUPTEMPLATE**
-   **PD \_ ENABLESETUPTEMPLATEHANDLE**

 

 