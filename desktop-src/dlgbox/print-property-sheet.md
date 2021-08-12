---
title: Imprimir hoja de propiedades
description: La hoja de propiedades Imprimir es una interfaz de usuario estándar que permite al usuario especificar las propiedades de un trabajo de impresión determinado.
ms.assetid: b52b71cc-a583-4a21-8a53-501ab442e6f8
keywords:
- Windows Interfaz de usuario,entrada del usuario
- Windows Interfaz de usuario,Common Dialog Box Library
- entrada de usuario, Biblioteca común de cuadros de diálogo
- capturar la entrada del usuario, Biblioteca de cuadros de diálogo común
- Biblioteca común de cuadros de diálogo
- cuadros de diálogo comunes
- Imprimir hoja de propiedades (cuadro de diálogo)
- personalizar hoja de propiedades de impresión (cuadro de diálogo)
- cuadros de diálogo predefinidos
- cuadros de diálogo,Imprimir hoja de propiedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc54bc8065ada207702755e8fc0a1586620f660db9f3acf2a67e32b56e393143
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118280518"
---
# <a name="print-property-sheet"></a>Imprimir hoja de propiedades

La **hoja** de propiedades Imprimir es una interfaz de usuario estándar que permite al usuario especificar las propiedades de un trabajo de impresión determinado. La hoja de propiedades se compone de un conjunto de páginas de propiedades que varían según la impresora o la aplicación. En un subconjunto de páginas de propiedades Windows estándar, algunas impresoras pueden agregar páginas de propiedades específicas del controlador y algunas aplicaciones pueden agregar páginas de propiedades específicas de la aplicación.

Para crear y mostrar una hoja de propiedades **Print,** inicialice una estructura [**PRINTDLGEX**](/windows/win32/api/commdlg/ns-commdlg-printdlgexa) y pase la estructura a la [**función PrintDlgEx.**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85))

En la ilustración siguiente se muestra una hoja **de propiedades print** típica.

![hoja de propiedades de impresora](images/printerpropertypagexp.png)

La mayoría de los [**miembros de la estructura PRINTDLGEX**](/windows/win32/api/commdlg/ns-commdlg-printdlgexa) son idénticos a los de la estructura [**PRINTDLG.**](/windows/win32/api/commdlg/ns-commdlg-printdlga) Para obtener descripciones de cómo usar los miembros de estructura comunes para interactuar con los controles de cuadro de diálogo, vea [Imprimir cuadro de diálogo](print-dialog-box.md). En el resto de este tema se describen las características **de la hoja** de propiedades Imprimir que difieren del cuadro **de** diálogo Imprimir.

Puede personalizar una **hoja** de propiedades Imprimir especificando una plantilla de cuadro de diálogo personalizada para la parte inferior de la página **General** y especificando páginas de propiedades adicionales para seguir la **página General.** Para obtener más información, vea [Personalización de la hoja de propiedades de impresión](#customizing-the-print-property-sheet).

Puede implementar un objeto de devolución de llamada para recibir notificaciones y mensajes de la [**función PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) mientras se muestra la hoja de propiedades. Las aplicaciones que proporcionan plantillas personalizadas o páginas adicionales usan el objeto de devolución de llamada para comunicarse con la hoja de propiedades. Para obtener más información, vea [Callback Object for the Print Property Sheet](#callback-object-for-the-print-property-sheet).

La **hoja** de propiedades Imprimir proporciona compatibilidad para especificar varios intervalos de páginas no largos que se van a imprimir. El **miembro lpPageRanges** de la estructura [**PRINTDLGEX**](/windows/win32/api/commdlg/ns-commdlg-printdlgexa) especifica una matriz de estructuras [**PRINTPAGERANGE**](/windows/win32/api/commdlg/ns-commdlg-printpagerange) en las que cada estructura especifica un intervalo de páginas.

La **hoja de** propiedades Imprimir muestra un botón de radio **Página** actual como parte del grupo Intervalo **de** páginas de botones de radio. Para controlar el **botón de** radio Página actual, use las marcas **PD \_ CURRENTPAGE** y **PD \_ NOCURRENTPAGE** en el miembro **Flags** de la [**estructura PRINTDLGEX.**](/windows/win32/api/commdlg/ns-commdlg-printdlgexa)

En esta sección se tratan los temas siguientes.

-   [Personalización de la hoja de propiedades de impresión](#customizing-the-print-property-sheet)
-   [Objeto de devolución de llamada para la hoja de propiedades de impresión](#callback-object-for-the-print-property-sheet)

## <a name="customizing-the-print-property-sheet"></a>Personalización de la hoja de propiedades de impresión

Puede personalizar la hoja **de** propiedades Imprimir de las maneras siguientes:

-   Proporcione una plantilla personalizada para la parte inferior de la **página General.** Esto le permite incluir controles adicionales que son únicos para la aplicación. La [**función PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) usa la plantilla personalizada en lugar de la plantilla predeterminada.
-   Proporcione páginas de propiedades adicionales para seguir la **página General.**
-   Proporcione un objeto de devolución de llamada. Para obtener más información, vea [Callback Object for the Print Property Sheet](#callback-object-for-the-print-property-sheet).

No se puede cambiar la parte superior de la **página General.** No se pueden cambiar las páginas de propiedades proporcionadas por el controlador de impresora.

Para proporcionar una plantilla personalizada para la página General:

1.  Cree una plantilla personalizada para la parte inferior de la página **General** modificando la plantilla PRINTDLGEXORD especificada en el archivo Prnsetup.dlg. Normalmente, la plantilla personalizada debe tener el mismo tamaño que la plantilla predeterminada. Sin embargo, puede ampliar la plantilla personalizada si especifica la marca **\_ USELARGETEMPLATE de PD** para crear una página general **más** grande. Los identificadores de control usados en la plantilla **de cuadro de** diálogo Imprimir predeterminada se definen en el archivo Dlgs.h.
2.  Use la [**estructura PRINTDLGEX**](/windows/win32/api/commdlg/ns-commdlg-printdlgexa) para habilitar la plantilla de la manera siguiente:
    -   Si la plantilla personalizada es un recurso de una aplicación o biblioteca de vínculos dinámicos, establezca la marca **\_ PD ENABLEPRINTTEMPLATE** en el **miembro Flags.** Use los **miembros hInstance** y **lpPrintTemplateName** de la estructura para identificar el módulo y el nombre del recurso.

        -O bien-

    -   Si la plantilla personalizada ya está en memoria, establezca la **\_ marca PD ENABLEPRINTTEMPLATEHANDLE.** Use el **miembro hInstance** para identificar el objeto de memoria que contiene la plantilla.

3.  Si usa una plantilla personalizada para definir controles adicionales, debe proporcionar un objeto de devolución de llamada para procesar la entrada de los controles. El objeto de devolución de llamada implementa un [**método IPrintDialogCallback::HandleMessage**](/windows/win32/api/commdlg/nf-commdlg-iprintdialogcallback-handlemessage) que recibe los mensajes enviados al cuadro de diálogo personalizado.

Para proporcionar páginas de propiedades adicionales

1.  Use la función para crear las páginas adicionales.
2.  Use el **miembro lphPropertyPages** de la [**estructura PRINTDLGEX**](/windows/win32/api/commdlg/ns-commdlg-printdlgexa) para especificar una matriz de identificadores para las páginas adicionales.

    Los procedimientos de cuadro de diálogo especificados al crear cada página procesan los mensajes enviados a las páginas.

3.  Es posible que desee proporcionar un objeto de devolución de llamada que implemente la interfaz . La [**función PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) usa esta interfaz para pasar a la aplicación un puntero a una [**interfaz IPrintDialogServices.**](/windows/win32/api/commdlg/nn-commdlg-iprintdialogservices) Los procedimientos del cuadro de diálogo para las páginas de propiedades adicionales pueden usar esta interfaz para recuperar información sobre la impresora seleccionada actualmente.

## <a name="callback-object-for-the-print-property-sheet"></a>Objeto de devolución de llamada para la hoja de propiedades de impresión

Una aplicación que muestra una hoja de propiedades **Print** puede implementar un objeto de devolución de llamada para recibir notificaciones y mensajes de la [**función PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) mientras se muestra la hoja de propiedades. Para proporcionar un objeto de devolución de llamada, especifique un puntero al objeto en el **miembro lpCallback** de la [**estructura PRINTDLGEX.**](/windows/win32/api/commdlg/ns-commdlg-printdlgexa)

El objeto de devolución de llamada debe implementar la [**interfaz IPrintDialogCallback.**](/windows/win32/api/commdlg/nn-commdlg-iprintdialogcallback) La [**función PrintDlgEx llama**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) a los **métodos IPrintDialogCallback** en las situaciones siguientes:

-   Cuando se ha inicializado el cuadro de diálogo
-   Cuando el usuario selecciona una impresora diferente de la lista de impresoras instaladas que muestra la hoja de propiedades
-   Cuando recibe mensajes para el cuadro de diálogo secundario de la parte inferior de la página General de la hoja **de** propiedades

El objeto de devolución de llamada también debe implementar la [**interfaz IObjectWithSite.**](/windows/win32/api/ocidl/nn-ocidl-iobjectwithsite) La [**función PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) llama al método para pasar un puntero a una [**interfaz IPrintDialogServices**](/windows/win32/api/commdlg/nn-commdlg-iprintdialogservices) a una aplicación. Los [**métodos IPrintDialogCallback**](/windows/win32/api/commdlg/nn-commdlg-iprintdialogcallback) pueden usar la **interfaz IPrintDialogServices** para recuperar información sobre la impresora seleccionada actualmente. La **interfaz IPrintDialogServices** también es útil para las aplicaciones que crean páginas adicionales para seguir la página **General** de la hoja de propiedades **Imprimir.** Los procedimientos del cuadro de diálogo para las páginas adicionales pueden llamar a **métodos IPrintDialogServices.**

 

 