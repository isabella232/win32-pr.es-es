---
title: Configurar página (cuadro de diálogo)
description: Muestra un cuadro de diálogo modal que permite al usuario elegir la configuración que incluye el tipo de papel, el origen del papel, la orientación de la página y el ancho de los márgenes de la página.
ms.assetid: debde0a0-07d4-46ed-a936-e517eab1852d
keywords:
- Interfaz de usuario de Windows, entrada de usuario
- Interfaz de usuario de Windows, biblioteca de cuadros de diálogo comunes
- entrada de usuario, biblioteca de cuadros de diálogo comunes
- capturar la entrada del usuario, la biblioteca de cuadros de diálogo comunes
- Biblioteca de cuadros de diálogo comunes
- cuadros de diálogo comunes
- Configurar página (cuadro de diálogo)
- cuadro de diálogo Personalizar la configuración de página
- enlaces, cuadro de diálogo Configurar página
- cuadros de diálogo predefinidos
- cuadros de diálogo, configurar página
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4b9a8f7f30a8313017dc3a124cdccb7d00c872b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149603"
---
# <a name="page-setup-dialog-box"></a>Configurar página (cuadro de diálogo)

Muestra un cuadro de diálogo modal que permite al usuario establecer los atributos siguientes de la página impresa:

-   El tipo de papel (sobre, legal, carta, etc.)
-   El origen del papel (alimentación manual, alimentación del tractor, alimentador de hojas, etc.)
-   Orientación de la página (vertical u horizontal)
-   El ancho de los márgenes de página

Para crear y mostrar un cuadro de diálogo **Configurar página** , inicialice una estructura [**PAGESETUPDLG**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga) y pase la estructura a la función [**PAGESETUPDLG**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) . Sin embargo, los atributos presentados en el cuadro de diálogo varían en función de las capacidades de la impresora. En la ilustración siguiente se muestra un cuadro de diálogo de **configuración de página** típico.

![cuadro de diálogo Configurar página](images/pagesetupdialogboxxp.png)

Si el usuario hace clic en el botón **Aceptar** , [**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) devuelve **true** después de establecer varios miembros en la estructura [**PageSetupDlg**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga) para especificar las selecciones del usuario. Los miembros **ptPaperSize** y **rtMargin** contienen los valores especificados por el usuario. Los miembros **hDevMode** y **hDevNames** contienen los identificadores de memoria globales para las estructuras [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) y [**DEVNAMES**](/windows/win32/api/commdlg/ns-commdlg-devnames) . Estas estructuras contienen información de página adicional, así como información acerca de la impresora. Puede usar esta información para preparar la salida que se va a enviar a la impresora seleccionada.

Si el usuario cancela el cuadro de diálogo **Configurar página** o se produce un error, [**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) devuelve **false**. Para determinar la causa del error, llame a la función [**CommDlgExtendedError**](/windows/desktop/api/Commdlg/nf-commdlg-commdlgextendederror) para recuperar el valor de error extendido.

En esta sección se tratan los temas siguientes.

-   [Inicializando el cuadro de diálogo Configurar página](#initializing-the-page-setup-dialog-box)
-   [Personalización del cuadro de diálogo Configurar página](#customizing-the-page-setup-dialog-box)
-   [Personalización de la página de ejemplo](#customizing-the-sample-page)

## <a name="initializing-the-page-setup-dialog-box"></a>Inicializando el cuadro de diálogo Configurar página

De forma predeterminada, el cuadro de diálogo **Configurar página** muestra información sobre la impresora predeterminada actual. Para dirigir el cuadro de diálogo para mostrar información sobre una impresora específica, establezca los miembros de una estructura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) o [**DEVNAMES**](/windows/win32/api/commdlg/ns-commdlg-devnames) y asigne los identificadores de memoria globales de estas estructuras al miembro correspondiente de [**PAGESETUPDLG**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga). Si especifica el nombre de una impresora que no está instalada actualmente, el cuadro de diálogo muestra un mensaje de error. Para evitar que el cuadro de diálogo muestre los mensajes de error, use el valor **PSD \_ nowarning** . Para recuperar información acerca de la impresora predeterminada sin mostrar el cuadro de diálogo **Configurar página** , use el valor **PSD \_ RETURNDEFAULT** .

Si el sistema de medida predeterminado es pulgadas, el cuadro de diálogo utiliza milésimas de pulgadas como unidad de medida predeterminada. Si el sistema de medida predeterminado es métrico, el cuadro de diálogo utiliza centésimas de milímetro como unidad de medida predeterminada. Para invalidar la unidad de medida predeterminada, establezca la marca **PSD \_ INHUNDREDTHSOFMILLIMETERS** o **PSD \_ INTHOUSANDTHSOFINCHES** en el miembro **Flags** de la estructura [**PAGESETUPDLG**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga) .

De forma predeterminada, los valores iniciales de los márgenes son de una pulgada. Si establece la marca **de \_ márgenes PSD** , el cuadro de diálogo muestra los valores de margen iniciales especificados en el miembro **rtMargin** . Los valores mínimos predeterminados que el usuario puede especificar para los márgenes son los márgenes mínimos permitidos por la impresora. Si establece la marca **PSD \_ MINMARGINS** , el cuadro de diálogo aplica los márgenes mínimos especificados en el miembro **rtMinMargin** .

Para evitar que los usuarios seleccionen determinadas opciones, establezca cualquier combinación de las marcas siguientes para deshabilitar los controles correspondientes.



| Marca                        | Significado                                                                  |
|-----------------------------|--------------------------------------------------------------------------|
| **\_DISABLEMARGINS PSD**     | Deshabilita los controles de edición en los que el usuario especifica la configuración de los márgenes. |
| **\_DISABLEORIENTATION PSD** | Deshabilita los botones de radio **vertical** y **horizontal** .               |
| **\_DISABLEPAPER PSD**       | Deshabilita los controles para seleccionar el tamaño del papel y el origen del papel.     |
| **\_DISABLEPRINTER PSD**     | Deshabilita el botón **impresora** .                                         |



 

## <a name="customizing-the-page-setup-dialog-box"></a>Personalización del cuadro de diálogo Configurar página

Puede proporcionar una plantilla personalizada para el cuadro de diálogo **Configurar página** , por ejemplo, si desea incluir controles adicionales que sean únicos para la aplicación. La función [**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) usa la plantilla personalizada en lugar de la plantilla predeterminada.

**Para proporcionar una plantilla personalizada para el cuadro de diálogo Configurar página**

1.  Cree la plantilla personalizada modificando la plantilla predeterminada especificada en el archivo prnsetup. Dlg. Los identificadores de control que se usan en la plantilla de cuadro de diálogo **configuración de página** predeterminada se definen en el archivo Dlgs. h.
2.  Use la estructura [**PAGESETUPDLG**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga) para habilitar la plantilla de la manera siguiente:
    -   -   Si la plantilla personalizada es un recurso de una biblioteca de vínculos dinámicos o de aplicación, establezca la marca **PSD \_ ENABLEPAGESETUPTEMPLATE** en el miembro **Flags** . Use los miembros **hInstance** y **lpPageSetupTemplateName** de la estructura para identificar el nombre del módulo y del recurso.

            -O bien-

        -   Si la plantilla personalizada ya está en la memoria, establezca la marca **PSD \_ ENABLEPAGESETUPTEMPLATEHANDLE** . Use el miembro **hPageSetupTemplate** para identificar el objeto de memoria que contiene la plantilla.

Para filtrar los mensajes enviados al procedimiento del cuadro de diálogo, puede proporcionar un procedimiento de enlace [**PageSetupHook**](/windows/win32/api/commdlg/nc-commdlg-lppagesetuphook) . Si usa una plantilla personalizada para definir controles adicionales, debe proporcionar un procedimiento de enlace **PageSetupHook** para procesar la entrada para los controles. Además, puede proporcionar un procedimiento de enlace [**PagePaintHook**](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) para personalizar el contenido de la página de ejemplo que se muestra en el cuadro de diálogo **Configurar página** . Para obtener más información sobre el procedimiento de enlace **PagePaintHook** , consulte [personalizar la página de ejemplo](#customizing-the-sample-page).

**Para habilitar un procedimiento de enlace PageSetupHook**

1.  Establezca la marca de **\_ ENABLEPAGESETUPHOOK PSD** en el miembro **Flags** de la estructura [**PAGESETUPDLG**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga) .
2.  Especifique la dirección del procedimiento de enlace en el miembro **lpfnPageSetupHook** .

Después de procesar el mensaje de [**\_ INITDIALOG de WM**](wm-initdialog.md) , el procedimiento de cuadro de diálogo envía un mensaje de **WM \_ INITDIALOG** al procedimiento de enlace [**PageSetupHook**](/windows/win32/api/commdlg/nc-commdlg-lppagesetuphook) . El parámetro *lParam* de este mensaje es un puntero a la estructura [**PAGESETUPDLG**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga) que se usa para inicializar el cuadro de diálogo.

## <a name="customizing-the-sample-page"></a>Personalización de la página de ejemplo

El cuadro de diálogo **Configurar página** incluye una imagen de una página de ejemplo que muestra cómo afectan las selecciones del usuario a la apariencia de la salida impresa. La imagen está formada por un rectángulo que representa el papel o el tipo de sobre seleccionado, con un rectángulo de línea de puntos que representa los márgenes actuales y caracteres parciales (texto griego) para mostrar el aspecto del texto en la página impresa.

Cuando llame a la función [**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) , puede proporcionar un procedimiento de enlace [**PagePaintHook**](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) para personalizar la apariencia de la página de ejemplo.

**Para habilitar un procedimiento de enlace PagePaintHook**

1.  Establezca la marca de **\_ ENABLEPAGEPAINTHOOK PSD** en el miembro **Flags** de la estructura [**PAGESETUPDLG**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga) .
2.  Especifique la dirección del procedimiento de enlace en el miembro **lpfnPagePaintHook** .

Cada vez que el cuadro de diálogo está a punto de dibujar el contenido de la página de ejemplo, el procedimiento de enlace recibe los mensajes siguientes en el orden en que aparecen.



| Mensaje                                                  | Significado                                                                                                                                          |
|----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_PAGESETUPDLG de PSD de WM \_**](wm-psd-pagesetupdlg.md)     | El cuadro de diálogo está a punto de dibujar la página de ejemplo. El procedimiento de enlace puede utilizar este mensaje para preparar la creación de contenido de la página de ejemplo.     |
| [**\_FULLPAGERECT de PSD de WM \_**](wm-psd-fullpagerect.md)     | El cuadro de diálogo está a punto de dibujar la página de ejemplo. Este mensaje especifica el rectángulo delimitador de la página de ejemplo.                               |
| [**\_MINMARGINRECT de PSD de WM \_**](wm-psd-minmarginrect.md)   | El cuadro de diálogo está a punto de dibujar la página de ejemplo. Este mensaje especifica el rectángulo del margen.                                                    |
| [**\_MARGINRECT de PSD de WM \_**](wm-psd-marginrect.md)         | El cuadro de diálogo está a punto de dibujar el rectángulo del margen.                                                                                            |
| [**\_GREEKTEXTRECT de PSD de WM \_**](wm-psd-greektextrect.md)   | El cuadro de diálogo está a punto de dibujar el texto griego dentro del rectángulo del margen.                                                                      |
| [**\_ENVSTAMPRECT de PSD de WM \_**](wm-psd-envstamprect.md)     | El cuadro de diálogo está a punto de dibujar en el rectángulo de la marca de sobre de una página de ejemplo de sobre. Este mensaje se envía solo para los sobres.             |
| [**\_YAFULLPAGERECT de PSD de WM \_**](wm-psd-yafullpagerect.md) | El cuadro de diálogo está a punto de dibujar la parte de la dirección de retorno de una página de ejemplo de sobre. Este mensaje se envía para los sobres y otros tamaños de papel. |



 

Si el procedimiento de enlace devuelve **true** para cualquiera de los tres primeros mensajes de una secuencia de dibujo ([**WM \_ PSD \_ PAGESETUPDLG**](wm-psd-pagesetupdlg.md), [**WM \_ PSD \_ FULLPAGERECT**](wm-psd-fullpagerect.md)o [**WM \_ PSD \_ MINMARGINRECT**](wm-psd-minmarginrect.md)), el cuadro de diálogo no envía más mensajes y no se dibuja en la página de ejemplo hasta la próxima vez que el sistema debe volver a dibujar la página de ejemplo. Si el procedimiento de enlace devuelve **false** para los tres mensajes, el cuadro de diálogo envía el resto de los mensajes de la secuencia de dibujo.

Si el procedimiento de enlace devuelve **true** para cualquiera de los mensajes restantes en una secuencia de dibujo, el cuadro de diálogo no dibuja la parte correspondiente de la página de ejemplo. Si el procedimiento de enlace devuelve **false** para cualquiera de estos mensajes, el cuadro de diálogo dibuja esa parte de la página de ejemplo.

Para evitar que el cuadro de diálogo dibuje el contenido de la página de ejemplo, puede establecer la marca **PSD \_ DISABLEPAGEPAINTING** . Esta marca no afecta al procedimiento de enlace [**PagePaintHook**](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) , que sigue recibiendo todos los **mensajes \_ PSD \_ \* de WM** y puede dibujar el contenido de la página de ejemplo.

 

 