---
title: Configurar página (cuadro de diálogo)
description: Muestra un cuadro de diálogo modal que permite al usuario elegir la configuración que incluye el tipo de papel, el origen del papel, la orientación de la página y el ancho de los márgenes de página.
ms.assetid: debde0a0-07d4-46ed-a936-e517eab1852d
keywords:
- Windows Interfaz de usuario,entrada de usuario
- Windows Interfaz de usuario,Common Dialog Box Library
- entrada de usuario,Biblioteca común de cuadros de diálogo
- capturar la entrada del usuario, Biblioteca de cuadros de diálogo común
- Biblioteca común de cuadros de diálogo
- cuadros de diálogo comunes
- Configurar página (cuadro de diálogo)
- personalizar el cuadro de diálogo Configurar página
- hooks,Page Setup (Cuadro de diálogo)
- cuadros de diálogo predefinidos
- cuadros de diálogo, Configuración de página
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1af64357be8bd39217c6527dc81f7ac426f5e06e183de92b3bb479f4633c75d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119741664"
---
# <a name="page-setup-dialog-box"></a>Configurar página (cuadro de diálogo)

Muestra un cuadro de diálogo modal que permite al usuario establecer los siguientes atributos de la página impresa:

-   El tipo de papel (sobre, legal, letra, entre otros)
-   El origen de papel (fuente manual, fuente de camión, fuente de hoja, y así sucesivamente)
-   Orientación de la página (vertical u horizontal)
-   Ancho de los márgenes de página

Para crear y mostrar un cuadro **de diálogo Configuración** de página, inicialice una estructura [**PAGESETUPDLG**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga) y pase la estructura a la [**función PageSetupDlg.**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) Sin embargo, los atributos presentados en el cuadro de diálogo varían en función de las capacidades de la impresora. En la ilustración siguiente se muestra un cuadro **de diálogo de configuración de** página típico.

![cuadro de diálogo de configuración de página](images/pagesetupdialogboxxp.png)

Si el usuario  hace clic en el botón Aceptar, [**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) devuelve **TRUE** después de establecer varios miembros en la estructura [**PAGESETUPDLG**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga) para especificar las selecciones del usuario. Los **miembros ptPaperSize** **y rtMargin** contienen los valores especificados por el usuario. Los **miembros hDevMode** y **hDevNames** contienen identificadores de memoria globales para las estructuras [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) y [**DEVNAMES.**](/windows/win32/api/commdlg/ns-commdlg-devnames) Estas estructuras contienen información de página adicional, así como información sobre la impresora. Puede usar esta información para preparar la salida que se enviará a la impresora seleccionada.

Si el usuario cancela el cuadro **de** diálogo Configuración de página o se produce un error, [**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) devuelve **FALSE.** Para determinar la causa del error, llame a la [**función CommDlgExtendedError**](/windows/desktop/api/Commdlg/nf-commdlg-commdlgextendederror) para recuperar el valor de error extendido.

En esta sección se de tratan los temas siguientes.

-   [Inicializar el cuadro de diálogo Configuración de página](#initializing-the-page-setup-dialog-box)
-   [Personalización del cuadro de diálogo Configurar página](#customizing-the-page-setup-dialog-box)
-   [Personalizar la página de ejemplo](#customizing-the-sample-page)

## <a name="initializing-the-page-setup-dialog-box"></a>Inicializar el cuadro de diálogo Configuración de página

De forma predeterminada, el **cuadro de diálogo Configuración** de página muestra información sobre la impresora predeterminada actual. Para dirigir el cuadro de diálogo para mostrar información sobre una impresora específica, establezca los miembros de una estructura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) o [**DEVNAMES**](/windows/win32/api/commdlg/ns-commdlg-devnames) y asigne los identificadores de memoria global de estas estructuras al miembro correspondiente en [**PAGESETUPDLG**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga). Si especifica el nombre de una impresora que no está instalada actualmente, el cuadro de diálogo muestra un mensaje de error. Para evitar que el cuadro de diálogo muestre mensajes de error, use el **valor \_ DE PSD NOWARNING.** Para recuperar información sobre la impresora predeterminada sin mostrar el cuadro **de** diálogo Configuración de página, use el **valor \_ PSD RETURNDEFAULT.**

Si el sistema de medida predeterminado es pulgadas, el cuadro de diálogo usa milésimas de pulgadas como unidad de medida predeterminada. Si el sistema de medida predeterminado es métrica, el cuadro de diálogo usa centésimas de milímetros como unidad de medida predeterminada. Para invalidar la unidad de medida predeterminada, establezca la marca **PSD \_ INHUHUTEDTHSOFMILLIMETERS** o **PSD \_ INTHOUSANDTHSOFINCHES** en el miembro **Flags** de la estructura [**PAGESETUPDLG.**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga)

De forma predeterminada, los valores iniciales de los márgenes son de una pulgada. Si establece la marca **PSD \_ MARGINS,** el cuadro de diálogo muestra los valores de margen iniciales especificados en el **miembro rtMargin.** Los valores mínimos predeterminados que el usuario puede especificar para los márgenes son los márgenes mínimos permitidos por la impresora. Si establece la marca **\_ PSD MINMARGINS,** el cuadro de diálogo aplica los márgenes mínimos especificados en el **miembro rtMinMargin.**

Para evitar que los usuarios seleccionen determinadas opciones, establezca cualquier combinación de las marcas siguientes para deshabilitar los controles correspondientes.



| Marca                        | Significado                                                                  |
|-----------------------------|--------------------------------------------------------------------------|
| **PSD \_ DISABLEMARGINS**     | Deshabilita los controles de edición en los que el usuario entra en la configuración de margen. |
| **PSD \_ DISABLEORIENTATION** | Deshabilita los botones **de** radio **Vertical y** Horizontal.               |
| **PSD \_ DISABLEPAPER**       | Deshabilita los controles para seleccionar el tamaño del papel y el origen del papel.     |
| **PSD \_ DISABLEPRINTER**     | Deshabilita el **botón** Impresora.                                         |



 

## <a name="customizing-the-page-setup-dialog-box"></a>Personalización del cuadro de diálogo Configurar página

Puede proporcionar una plantilla  personalizada para el cuadro de diálogo Configuración de página, por ejemplo, si desea incluir controles adicionales que sean únicos para la aplicación. La [**función PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) usa la plantilla personalizada en lugar de la plantilla predeterminada.

**Para proporcionar una plantilla personalizada para el cuadro de diálogo Configuración de página**

1.  Cree la plantilla personalizada modificando la plantilla predeterminada especificada en el archivo Prnsetup.dlg. Los identificadores de control usados en la plantilla de cuadro de diálogo **configuración** de página predeterminada se definen en el archivo Dlgs.h.
2.  Use la [**estructura PAGESETUPDLG**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga) para habilitar la plantilla de la siguiente manera:
    -   -   Si la plantilla personalizada es un recurso de una aplicación o biblioteca de vínculos dinámicos, establezca la marca **\_ PSD ENABLEPAGESETUPTEMPLATE** en el **miembro Flags.** Use los **miembros hInstance** y **lpPageSetupTemplateName** de la estructura para identificar el módulo y el nombre del recurso.

            -O bien-

        -   Si la plantilla personalizada ya está en memoria, establezca la **\_ marca PSD ENABLEPAGESETUPTEMPLATEHANDLE.** Use el **miembro hPageSetupTemplate** para identificar el objeto de memoria que contiene la plantilla.

Para filtrar los mensajes enviados al procedimiento del cuadro de diálogo, puede proporcionar un procedimiento de enlace [**PageSetupHook.**](/windows/win32/api/commdlg/nc-commdlg-lppagesetuphook) Si usa una plantilla personalizada para definir controles adicionales, debe proporcionar un procedimiento de enlace **PageSetupHook** para procesar la entrada de los controles. Además, puede proporcionar un procedimiento de enlace [**PagePaintHook**](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) para personalizar el contenido de la página de ejemplo que se muestra en el cuadro de diálogo **Configurar** página. Para obtener más información sobre el **procedimiento de enlace PagePaintHook,** vea [Personalizar la página de ejemplo](#customizing-the-sample-page).

**Para habilitar un procedimiento de enlace de PageSetupHook**

1.  Establezca la **marca PSD \_ ENABLEPAGESETUPHOOK** en el **miembro Flags** de la [**estructura PAGESETUPDLG.**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga)
2.  Especifique la dirección del procedimiento de enlace en el **miembro lpfnPageSetupHook.**

Después de procesar su [**mensaje WM \_ INITDIALOG,**](wm-initdialog.md) el procedimiento del cuadro de diálogo envía un mensaje **WM \_ INITDIALOG** al procedimiento de enlace [**PageSetupHook.**](/windows/win32/api/commdlg/nc-commdlg-lppagesetuphook) El *parámetro lParam* de este mensaje es un puntero a la [**estructura PAGESETUPDLG**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga) utilizada para inicializar el cuadro de diálogo.

## <a name="customizing-the-sample-page"></a>Personalizar la página de ejemplo

El **cuadro de diálogo Configuración** de página incluye una imagen de una página de ejemplo que muestra cómo afectan las selecciones del usuario a la apariencia de la salida impresa. La imagen consta de un rectángulo que representa el tipo de papel o sobre seleccionado, con un rectángulo de línea de puntos que representa los márgenes actuales y caracteres parciales (texto griego) para mostrar el aspecto del texto en la página impresa.

Al llamar a la [**función PageSetupDlg,**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) puede proporcionar un procedimiento de enlace [**PagePaintHook**](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) para personalizar la apariencia de la página de ejemplo.

**Para habilitar un procedimiento de enlace PagePaintHook**

1.  Establezca la **marca PSD \_ ENABLEPAGEPAINTHOOK** en el **miembro Flags** de la [**estructura PAGESETUPDLG.**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga)
2.  Especifique la dirección del procedimiento de enlace en el **miembro lpfnPagePaintHook.**

Cada vez que el cuadro de diálogo está a punto de dibujar el contenido de la página de ejemplo, el procedimiento de enlace recibe los mensajes siguientes en el orden en que se enumeran.



| Mensaje                                                  | Significado                                                                                                                                          |
|----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PÁGINA \_ DE PSD \_ DE WMSETUPDLG**](wm-psd-pagesetupdlg.md)     | El cuadro de diálogo está a punto de dibujar la página de ejemplo. El procedimiento de enlace puede usar este mensaje para prepararse para dibujar el contenido de la página de ejemplo.     |
| [**WM \_ PSD \_ FULLPAGERECT**](wm-psd-fullpagerect.md)     | El cuadro de diálogo está a punto de dibujar la página de ejemplo. Este mensaje especifica el rectángulo delimitador de la página de ejemplo.                               |
| [**WM \_ PSD \_ MINMARGINRECT**](wm-psd-minmarginrect.md)   | El cuadro de diálogo está a punto de dibujar la página de ejemplo. Este mensaje especifica el rectángulo de margen.                                                    |
| [**WM \_ PSD \_ MARGINRECT**](wm-psd-marginrect.md)         | El cuadro de diálogo está a punto de dibujar el rectángulo de margen.                                                                                            |
| [**WM \_ PSD \_ GREEKTEXTRECT**](wm-psd-greektextrect.md)   | El cuadro de diálogo está a punto de dibujar el texto griego dentro del rectángulo de margen.                                                                      |
| [**WM \_ PSD \_ ENVSTAMPRECT**](wm-psd-envstamprect.md)     | El cuadro de diálogo está a punto de dibujarse en el rectángulo de marca de sobre de una página de ejemplo de sobre. Este mensaje se envía solo para sobres.             |
| [**WM \_ PSD \_ YAFULLPAGERECT**](wm-psd-yafullpagerect.md) | El cuadro de diálogo está a punto de dibujar la parte de la dirección de retorno de una página de ejemplo de sobre. Este mensaje se envía para sobres y otros tamaños de papel. |



 

Si el procedimiento de enlace devuelve **TRUE** para cualquiera de los tres primeros mensajes de una secuencia de dibujo [**(WM \_ PSD \_ PAGESETUPDLG,**](wm-psd-pagesetupdlg.md) [**WM \_ PSD \_ FULLPAGERECT**](wm-psd-fullpagerect.md)o [**WM \_ PSD \_ MINMARGINRECT),**](wm-psd-minmarginrect.md)el cuadro de diálogo no envía más mensajes y no dibuja en la página de ejemplo hasta la próxima vez que el sistema necesite volver a dibujar la página de ejemplo. Si el procedimiento de enlace devuelve **FALSE para** los tres mensajes, el cuadro de diálogo envía los mensajes restantes de la secuencia de dibujo.

Si el procedimiento de enlace devuelve **TRUE para** cualquiera de los mensajes restantes de una secuencia de dibujo, el cuadro de diálogo no dibuja la parte correspondiente de la página de ejemplo. Si el procedimiento de enlace **devuelve FALSE para** cualquiera de estos mensajes, el cuadro de diálogo dibuja esa parte de la página de ejemplo.

Para evitar que el cuadro de diálogo dibujo el contenido de la página de ejemplo, puede establecer la marca **PSD \_ DISABLEPAGEPAINTING.** Esta marca no afecta al procedimiento de enlace [**PagePaintHook,**](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) que todavía recibe todos los mensajes **DE WM \_ \_ \* PSD** y puede dibujar el contenido de la página de ejemplo.

 

 