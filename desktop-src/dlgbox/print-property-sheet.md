---
title: Imprimir hoja de propiedades
description: La hoja de propiedades imprimir es una interfaz de usuario estándar que permite al usuario especificar las propiedades de un trabajo de impresión determinado.
ms.assetid: b52b71cc-a583-4a21-8a53-501ab442e6f8
keywords:
- Interfaz de usuario de Windows, entrada de usuario
- Interfaz de usuario de Windows, biblioteca de cuadros de diálogo comunes
- entrada de usuario, biblioteca de cuadros de diálogo comunes
- capturar la entrada del usuario, la biblioteca de cuadros de diálogo comunes
- Biblioteca de cuadros de diálogo comunes
- cuadros de diálogo comunes
- Cuadro de diálogo Imprimir hoja de propiedades
- cuadro de diálogo Personalizar hoja de propiedades de impresión
- cuadros de diálogo predefinidos
- cuadros de diálogo, hoja de propiedades imprimir
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20905f76af290b3978bec828a382604147297998
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078338"
---
# <a name="print-property-sheet"></a>Imprimir hoja de propiedades

La hoja de propiedades **Imprimir** es una interfaz de usuario estándar que permite al usuario especificar las propiedades de un trabajo de impresión determinado. La hoja de propiedades se compone de un conjunto de páginas de propiedades que varía según la impresora o la aplicación. En un subconjunto de las páginas de propiedades estándar de Windows, algunas impresoras pueden agregar páginas de propiedades específicas del controlador y algunas aplicaciones pueden agregar páginas de propiedades específicas de la aplicación.

Para crear y mostrar una hoja de propiedades de **impresión** , inicialice una estructura [**PRINTDLGEX**](/windows/win32/api/commdlg/ns-commdlg-printdlgexa) y pase la estructura a la función [**PRINTDLGEX**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) .

En la ilustración siguiente se muestra una hoja de propiedades de **impresión** típica.

![hoja de propiedades de la impresora](images/printerpropertypagexp.png)

La mayoría de los miembros de la estructura [**PRINTDLGEX**](/windows/win32/api/commdlg/ns-commdlg-printdlgexa) son idénticos a los de la estructura [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) . Para obtener descripciones sobre cómo usar los miembros de la estructura común para interactuar con los controles de cuadro de diálogo, vea [cuadro de diálogo Imprimir](print-dialog-box.md). En el resto de este tema se describen las características de la hoja de propiedades de **impresión** que difieren del cuadro de diálogo **Imprimir** .

Puede personalizar una hoja de propiedades de **impresión** especificando una plantilla de cuadro de diálogo personalizada para la parte inferior de la página **General** y especificando páginas de propiedades adicionales para seguir la página **General** . Para obtener más información, vea [personalizar la hoja de propiedades de impresión](#customizing-the-print-property-sheet).

Puede implementar un objeto de devolución de llamada para recibir notificaciones y mensajes de la función [**PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) mientras se muestra la hoja de propiedades. Las aplicaciones que proporcionan plantillas personalizadas o páginas adicionales utilizan el objeto de devolución de llamada para comunicarse con la hoja de propiedades. Para obtener más información, vea [callback (objeto) para la hoja de propiedades Print](#callback-object-for-the-print-property-sheet).

La hoja de propiedades **Imprimir** proporciona compatibilidad para especificar varios intervalos de páginas no contiguos que se van a imprimir. El miembro **lpPageRanges** de la estructura [**PRINTDLGEX**](/windows/win32/api/commdlg/ns-commdlg-printdlgexa) especifica una matriz de estructuras [**PRINTPAGERANGE**](/windows/win32/api/commdlg/ns-commdlg-printpagerange) en la que cada estructura especifica un intervalo de páginas.

La hoja de propiedades **Imprimir** muestra un botón de radio **Página actual** como parte del grupo **intervalo de páginas** de botones de radio. Para controlar el botón de opción **Página actual** , use las marcas **PD \_ CURRENTPAGE** y **PD \_ NOCURRENTPAGE** en el miembro **Flags** de la estructura [**PRINTDLGEX**](/windows/win32/api/commdlg/ns-commdlg-printdlgexa) .

En esta sección se tratan los temas siguientes.

-   [Personalización de la hoja de propiedades de impresión](#customizing-the-print-property-sheet)
-   [Objeto de devolución de llamada para la hoja de propiedades de impresión](#callback-object-for-the-print-property-sheet)

## <a name="customizing-the-print-property-sheet"></a>Personalización de la hoja de propiedades de impresión

Puede personalizar la hoja de propiedades de **impresión** de las siguientes maneras:

-   Proporcione una plantilla personalizada para la parte inferior de la página **General** . Esto le permite incluir controles adicionales que son exclusivos de la aplicación. La función [**PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) usa la plantilla personalizada en lugar de la plantilla predeterminada.
-   Proporcione páginas de propiedades adicionales para seguir la página **General** .
-   Proporcione un objeto de devolución de llamada. Para obtener más información, vea [callback (objeto) para la hoja de propiedades Print](#callback-object-for-the-print-property-sheet).

No se puede cambiar la parte superior de la página **General** . No se pueden cambiar las páginas de propiedades proporcionadas por el controlador de impresora.

Para proporcionar una plantilla personalizada para la página general:

1.  Cree una plantilla personalizada para la parte inferior de la página **General** modificando la plantilla PRINTDLGEXORD especificada en el archivo prnsetup. Dlg. Normalmente, la plantilla personalizada debe tener el mismo tamaño que la plantilla predeterminada. Sin embargo, puede ampliar la plantilla personalizada si especifica la marca **PD \_ USELARGETEMPLATE** para crear una página **General** más grande. Los identificadores de control que se usan en la plantilla de cuadro de diálogo de **impresión** predeterminada se definen en el archivo Dlgs. h.
2.  Use la estructura [**PRINTDLGEX**](/windows/win32/api/commdlg/ns-commdlg-printdlgexa) para habilitar la plantilla de la manera siguiente:
    -   Si la plantilla personalizada es un recurso de una biblioteca de vínculos dinámicos o de aplicación, establezca la marca **PD \_ ENABLEPRINTTEMPLATE** en el miembro **Flags** . Use los miembros **hInstance** y **lpPrintTemplateName** de la estructura para identificar el nombre del módulo y del recurso.

        -O bien-

    -   Si la plantilla personalizada ya está en la memoria, establezca la marca **PD \_ ENABLEPRINTTEMPLATEHANDLE** . Use el miembro **hInstance** para identificar el objeto de memoria que contiene la plantilla.

3.  Si usa una plantilla personalizada para definir controles adicionales, debe proporcionar un objeto de devolución de llamada para procesar la entrada para los controles. El objeto de devolución de llamada implementa un método [**IPrintDialogCallback:: HandleMessage**](/windows/win32/api/commdlg/nf-commdlg-iprintdialogcallback-handlemessage) que recibe los mensajes enviados al cuadro de diálogo personalizado.

Para proporcionar páginas de propiedades adicionales

1.  Utilice la función para crear las páginas adicionales.
2.  Use el miembro **lphPropertyPages** de la estructura [**PRINTDLGEX**](/windows/win32/api/commdlg/ns-commdlg-printdlgexa) para especificar una matriz de identificadores para las páginas adicionales.

    Los procedimientos del cuadro de diálogo especificados al crear cada página procesan los mensajes enviados a las páginas.

3.  Es posible que desee proporcionar un objeto de devolución de llamada que implemente la interfaz. La función [**PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) usa esta interfaz para pasar a la aplicación un puntero a una interfaz [**IPrintDialogServices**](/windows/win32/api/commdlg/nn-commdlg-iprintdialogservices) . Los procedimientos del cuadro de diálogo de las páginas de propiedades adicionales pueden utilizar esta interfaz para recuperar información acerca de la impresora seleccionada actualmente.

## <a name="callback-object-for-the-print-property-sheet"></a>Objeto de devolución de llamada para la hoja de propiedades de impresión

Una aplicación que muestra una hoja de propiedades de **impresión** puede implementar un objeto de devolución de llamada para recibir notificaciones y mensajes de la función [**PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) mientras se muestra la hoja de propiedades. Para proporcionar un objeto de devolución de llamada, especifique un puntero al objeto en el miembro **lpCallback** de la estructura [**PRINTDLGEX**](/windows/win32/api/commdlg/ns-commdlg-printdlgexa) .

El objeto de devolución de llamada debe implementar la interfaz [**IPrintDialogCallback**](/windows/win32/api/commdlg/nn-commdlg-iprintdialogcallback) . La función [**PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) llama a los métodos **IPrintDialogCallback** en las situaciones siguientes:

-   Cuando se ha inicializado el cuadro de diálogo
-   Cuando el usuario selecciona una impresora diferente de la lista de impresoras instaladas que se muestra en la hoja de propiedades
-   Cuando recibe mensajes para el cuadro de diálogo secundario en la parte inferior de la página **General** de la hoja de propiedades

El objeto de devolución de llamada también debe implementar la interfaz [**IObjectWithSite**](/windows/win32/api/ocidl/nn-ocidl-iobjectwithsite) . La función [**PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) llama al método para pasar un puntero a una interfaz [**IPrintDialogServices**](/windows/win32/api/commdlg/nn-commdlg-iprintdialogservices) a una aplicación. Los métodos [**IPrintDialogCallback**](/windows/win32/api/commdlg/nn-commdlg-iprintdialogcallback) pueden usar la interfaz **IPrintDialogServices** para recuperar información acerca de la impresora seleccionada actualmente. La interfaz **IPrintDialogServices** también es útil para las aplicaciones que crean páginas adicionales para seguir la página **General** de la hoja de propiedades **Imprimir** . Los procedimientos del cuadro de diálogo para las páginas adicionales pueden llamar a métodos **IPrintDialogServices** .

 

 