---
title: Cómo crear asistentes
description: Un asistente es un tipo de hoja de propiedades que proporciona una manera sencilla y eficaz de guiar a los usuarios a través de un procedimiento.
ms.assetid: f8def159-0a68-4d7f-9840-c7b6b906ed08
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fedd35bd0454e0d78ddbe74d832543e58d0a8fc7
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/19/2021
ms.locfileid: "105660107"
---
# <a name="how-to-create-wizards"></a>Cómo crear asistentes

Un asistente es un tipo de hoja de propiedades que proporciona una manera sencilla y eficaz de guiar a los usuarios a través de un procedimiento.

Los asistentes son una de las claves para simplificar la experiencia del usuario. Permiten realizar una operación compleja, como la configuración de una aplicación, y dividirla en una serie de pasos sencillos. En cada punto del proceso, puede proporcionar una explicación de lo que se necesita y mostrar los controles que permiten al usuario realizar selecciones y escribir texto.

Un asistente es realmente un tipo de hoja de propiedades. Una hoja de propiedades es esencialmente un contenedor para una colección de *páginas*, donde cada página es un cuadro de diálogo independiente. Mientras que las hojas de propiedades normales permiten que el usuario tenga acceso a cualquier página en cualquier momento, los asistentes presentan las páginas en secuencia. En lugar de pestañas, los botones se utilizan para navegar hacia delante y hacia atrás. La aplicación controla el orden en que se muestran las páginas y se puede modificar en función de los datos proporcionados por el usuario.

Hay dos estilos principales del asistente: el estilo Wizard97 anterior y el estilo Aero introducido en Windows Vista. Para ver ilustraciones, consulte Acerca de las [hojas de propiedades](property-sheets.md). (Un tercer estilo, con solo el PSH \_ \_La marca Lite del asistente o del Asistente para PSH \_ muestra una secuencia simple de hojas de propiedades sin encabezados ni marcas de agua).

> [!Note]  
> Una "marca de agua" en el contexto de los asistentes es un mapa de bits que aparece en el margen izquierdo de algunas páginas.

 

En la mayor parte de este documento se da por supuesto que está implementando un asistente para un sistema con la [versión 5,80](common-control-versions.md) o posterior de los controles comunes. Si intenta usar el estilo Wizard97 con versiones anteriores de los controles comunes, la aplicación puede compilarse pero no se mostrará correctamente. Para obtener una explicación sobre cómo crear un asistente compatible con Wizard97 en sistemas anteriores, vea asistentes compatibles con versiones anteriores en este tema.

## <a name="what-you-need-to-know"></a>Aspectos que debe saber

### <a name="technologies"></a>Tecnologías

-   [Controles de Windows](window-controls.md)

### <a name="prerequisites"></a>Requisitos previos

-   C/C++
-   Programación de la interfaz de usuario de Windows

## <a name="instructions"></a>Instrucciones

### <a name="wizard-implementation"></a>Implementación del asistente

La implementación de un asistente es similar a la implementación de una hoja de propiedades normal. En el nivel más básico, es cuestión de establecer una de las siguientes marcas o combinaciones de marcas en la estructura [**PROPSHEETHEADER**](pss-propsheetheader.md) que define la hoja de propiedades.



| Marca                           | Estilo                                                                                                                                                 |
|--------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_Asistente para PSH                    | Un sencillo asistente sin encabezados ni mapas de bits.                                                                                                           |
| \_Asistente para PSH \_ Lite              | Similar al Asistente para PSH \_ , con algunas pequeñas diferencias de apariencia; por ejemplo, el divisor situado encima de los botones se establece en el ancho completo de la ventana. |
| PSH \_ WIZARD97                  | Un asistente de Wizard97 con encabezados (opcionales), mapas de bits de encabezado y marcas de agua.                                                                            |
| \_Asistente para PSH \| PSH \_ AEROWIZARD | Un asistente de Aero. Los asistentes de Aero no utilizan marcas de agua ni mapas de bits de encabezado. Requieren el modelo de contenedor uniproceso (STA).                         |



 

El procedimiento básico para implementar un asistente es el siguiente:

1.  Cree una plantilla de cuadro de diálogo para cada página.
2.  Defina las páginas mediante la creación de una estructura [**PROPSHEETPAGE**](pss-propsheetpage.md) para cada página. Esta estructura define la página y contiene punteros a la plantilla de cuadro de diálogo y a cualquier mapa de bits u otros recursos.
3.  Pase la estructura [**PROPSHEETPAGE**](pss-propsheetpage.md) que se creó en el paso anterior a la función [**CreatePropertySheetPage**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea) para crear el identificador HPROPSHEETPAGE de la página.
4.  Defina el asistente mediante la creación de una estructura [**PROPSHEETHEADER**](pss-propsheetheader.md) para él.
5.  Pase la estructura [**PROPSHEETHEADER**](pss-propsheetheader.md) a la función [**hoja**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) para mostrar el asistente.
6.  Implemente procedimientos de cuadro de diálogo para cada página con el fin de controlar los mensajes de notificación de los controles de la página y los botones del asistente y para procesar otros mensajes de mensajería de Windows.

### <a name="create-the-dialog-box-templates"></a>Crear las plantillas de cuadro de diálogo

Hay dos tipos básicos de página del asistente: exterior y interior. Las páginas exteriores son la introducción (bienvenida) y las páginas de finalización. Todas las demás son páginas interiores.

**Plantillas de cuadro de diálogo de página exterior**

El diseño básico de las páginas de introducción y finalización es idéntico. En la ilustración siguiente se muestra una página de introducción de Wizard97 de ejemplo, con una marca de agua de marcador de posición.

![captura de pantalla que muestra una página del asistente con un gráfico a la izquierda, el título y el texto del cuerpo de los botones derecho y atrás, siguiente y cancelar en la parte inferior](images/wiz97exterior.png)

En el caso de las páginas de Wizard97 exterior, la plantilla de cuadro de diálogo es 317x193 unidades de cuadro de diálogo. Rellena todo el asistente, excepto el título y la banda de la parte inferior que contiene los botones **atrás**, **siguiente** y **Cancelar** . El lado izquierdo de la plantilla, que está reservado para un mapa de bits de "marca de agua", no debe contener ningún control. La marca de agua se especifica en la estructura [**PROPSHEETHEADER**](pss-propsheetheader.md) del asistente y se agrega a la página automáticamente. Debe permitir el espacio al diseñar la plantilla de recursos.

Al crear el mapa de bits de la marca de agua, tenga en cuenta que el cuadro de diálogo puede aumentar de tamaño si, por ejemplo, el usuario elige una fuente grande del sistema. Otros idiomas también suelen tener distintas métricas de fuentes. Cuando la página aumenta de tamaño, el área reservada para la marca de agua se obtiene proporcionalmente. Sin embargo, no puede cambiar el mapa de bits de la marca de agua ni el mapa de bits estirado para rellenar el área más grande. En su lugar, el mapa de bits se deja en su tamaño original en la parte superior izquierda del área reservada. La parte del área reservada más grande que no está incluida en la marca de agua se rellena automáticamente con el color del píxel superior izquierdo del mapa de bits.

Si necesita tener mapas de bits de una marca de agua de tamaño diferente para distintas métricas de fuente, existen dos soluciones posibles:

-   Obtenga las métricas de fuente antes de crear el asistente y especifique un mapa de bits de marca de agua de tamaño adecuado.
-   No especifique un mapa de bits de marca de agua al crear el asistente. Wizard97 dejará el área de marca de agua en blanco. A continuación, dibuje un mapa de bits de tamaño adecuado en el área reservada para la marca de agua.

Puede colocar controles en el área situada a la derecha de la marca de agua como lo haría con un cuadro de diálogo normal. El color de fondo de esta área viene determinado por el sistema y no requiere ninguna acción por su parte. Normalmente, se colocan dos controles estáticos en esta área. La parte superior contiene el título y utiliza una fuente Negrita grande (de 12 puntos Verdana negrita para Wizard97). El otro, que es para texto explicativo, usa la fuente del cuadro de diálogo estándar.

La diferencia principal entre las páginas introducción y finalización son los botones del asistente y el texto de los controles estáticos. Normalmente, las páginas de introducción tienen un botón **siguiente** y otro **hacia atrás** , con solo el botón **siguiente** habilitado. Las páginas de finalización tienen el botón **atrás** habilitado y el botón **siguiente** se sustituye por un botón **Finalizar** .

> [!Note]  
> En los asistentes de Aero, el botón **atrás** se sustituye por un botón de flecha en la barra de título.

 

Puede modificar el texto del botón **Finalizar** mediante el envío del asistente a un [**mensaje \_ SETFINISHTEXT de PSM**](psm-setfinishtext.md) . De forma predeterminada, el botón **Finalizar** no incluye una tecla de aceleración. Para definir una tecla de aceleración, incluya una y comercial en la cadena de texto que pase a PSM \_ SETFINISHTEXT. Por ejemplo, "&finalizar" define ' F ' como la tecla de aceleración.

**Plantillas del cuadro de diálogo página interior**

Las páginas interiores tienen una apariencia algo diferente que las páginas exteriores. En la ilustración siguiente se muestra una página interior Wizard97 de ejemplo, con un mapa de bits de encabezado de marcador de posición.

![captura de pantalla de una página del asistente con texto de título y subtítulo y un gráfico en la parte superior, texto en el medio y botones en la parte inferior](images/wiz97interior.png)

La hoja de propiedades controla el área de encabezado de la parte superior de la página, por lo que no se incluye en la plantilla. El contenido del encabezado se especifica en la estructura [**PROPSHEETPAGE**](pss-propsheetpage.md) de la página y en la estructura [**PROPSHEETHEADER**](pss-propsheetheader.md) del asistente. Dado que la página interior debe encajar entre el encabezado y los botones, la plantilla del cuadro de diálogo Wizard97 es 317x143 unidades de cuadro de diálogo, algo más pequeñas que la plantilla para las páginas exteriores.

En la ilustración siguiente se muestra un asistente de Aero que se creó a partir de la misma plantilla.

![captura de pantalla que difiere de la anterior al tener un área de título en la parte superior y los botones siguiente y cancelar en la parte inferior](images/wizardaerointerior.png)

### <a name="define-the-wizard-pages"></a>Definir las páginas del asistente

Después de crear las plantillas de cuadro de diálogo y los recursos relacionados, como mapas de bits y tablas de cadenas, puede crear las páginas de la hoja de propiedades. El procedimiento es similar al de las hojas de propiedades estándar. En primer lugar, rellene los miembros adecuados de una estructura [**PROPSHEETPAGE**](pss-propsheetpage.md) . (Algunos miembros son específicos de los asistentes). Después, llame a la función [**CreatePropertySheetPage**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea) para crear el identificador HPROPSHEETPAGE de la página.

Se pueden establecer las siguientes marcas relacionadas con el asistente en el miembro **dwFlags** de la estructura [**PROPSHEETPAGE**](pss-propsheetpage.md) .



| Marca                   | Descripción                                                                                                                         |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| PSP \_ HIDEHEADER        | Establezca esta marca para las páginas exteriores en Wizard97. El encabezado no se muestra y se puede mostrar una marca de agua.                                |
| PSP \_ USEHEADERTITLE    | Establezca esta marca para las páginas interiores para colocar un título en el área de encabezado de Wizard97 o en la parte superior del área de cliente en un asistente de Aero. |
| PSP \_ USEHEADERSUBTITLE | Establezca esta marca para que las páginas interiores colocan un subtítulo en el área de encabezado de Wizard97.                                                  |



 

Si ha establecido PSP \_ USEHEADERTITLE o PSP \_ USEHEADERSUBTITLE, asigne el texto del título y el subtítulo a los miembros **pszHeaderTitle** y **pszHeaderSubtitle** , respectivamente. Al asignar cadenas de texto a miembros de las estructuras [**PROPSHEETPAGE**](pss-propsheetpage.md) y [**PROPSHEETHEADER**](pss-propsheetheader.md) , puede asignar un puntero de cadena o utilizar la macro **MAKEINTRESOURCE** para asignar un valor de un recurso de cadena. El recurso de cadena se carga desde el módulo especificado en el miembro **hInstance** de la estructura **PROPSHEETHEADER** del asistente.

Cuando llame a [**CreatePropertySheetPage**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea) para crear una página, asigne el resultado a un elemento de una matriz de identificadores de HPROPSHEETPAGE. Esta matriz se utiliza al crear la hoja de propiedades. El índice de matriz del identificador de una página determina el orden predeterminado en el que se muestra. Después de crear el identificador de HPROPSHEETPAGE de una página, puede volver a usar la misma estructura [**PROPSHEETPAGE**](pss-propsheetpage.md) para crear la siguiente página asignando nuevos valores a los miembros pertinentes.

Una manera alternativa de crear páginas es usar estructuras [**PROPSHEETPAGE**](pss-propsheetpage.md) independientes para cada página y crear una matriz de estructuras. Esta matriz se usa en lugar de una matriz de identificadores de HPROPSHEETPAGE al crear la hoja de propiedades. El uso de estructuras **PROPSHEETPAGE** independientes elimina la necesidad de llamar a [**CreatePropertySheetPage**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea) , pero utiliza más memoria. De lo contrario, no hay ninguna diferencia significativa entre los dos enfoques.

En el ejemplo siguiente se define una página interior de Wizard97 asignando valores a una estructura [**PROPSHEETPAGE**](pss-propsheetpage.md) . En este ejemplo, el título, el subtítulo y la plantilla de cuadro de diálogo de la página se identifican por sus identificadores de recurso. A continuación, se llama a la función [**CreatePropertySheetPage**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea) para crear el identificador HPROPSHEETPAGE de la página. Dado que será la segunda página que aparece, el identificador se asigna a la matriz de identificadores, *ahpsp*, con un índice de 1.


```C++
// g_hInstance is the global HINSTANCE of the application.
// IntPage1DlgProc is the dialog procedure for this page.
// ahpsp is an array of HPROPSHEETPAGE handles.

PROPSHEETPAGE psp = { sizeof(psp) };

psp.hInstance         = g_hInstance;
psp.dwFlags           = PSP_USEHEADERTITLE | PSP_USEHEADERSUBTITLE;
psp.lParam            = (LPARAM) &wizdata;
psp.pszHeaderTitle    = MAKEINTRESOURCE(IDS_TITLE1);
psp.pszHeaderSubTitle = MAKEINTRESOURCE(IDS_SUBTITLE1);
psp.pszTemplate       = MAKEINTRESOURCE(IDD_INTERIOR1);
psp.pfnDlgProc        = IntPage1DlgProc;

ahpsp[1] = CreatePropertySheetPage(&psp);
```



### <a name="custom-page-data"></a>Datos de página personalizados

Cuando se crea una página, se pueden asignar datos personalizados a ella mediante el miembro **lParam** de la estructura [**PROPSHEETPAGE**](pss-propsheetpage.md) , normalmente mediante la asignación de un puntero a una estructura definida por el usuario.

Cuando se selecciona la página por primera vez, el procedimiento del cuadro de diálogo recibe un mensaje de [**\_ INITDIALOG de WM**](/windows/desktop/dlgbox/wm-initdialog) . El valor *lParam* del mensaje apunta a una copia de de la estructura [**PROPSHEETPAGE**](pss-propsheetpage.md) de la página, desde la que puede recuperar los datos personalizados. Después, puede almacenar estos datos para su uso en mensajes posteriores mediante [**SetWindowLongPtr**](/windows/desktop/api/winuser/nf-winuser-setwindowlongptra) con GWL \_ USERDATA como parámetro de índice. Varias páginas pueden tener un puntero a los mismos datos y cualquier cambio realizado en los datos de una página está disponible para las demás páginas de sus procedimientos de diálogo.

### <a name="define-the-wizard-property-sheet"></a>Definir la hoja de propiedades del asistente

Al igual que con las hojas de propiedades normales, la hoja de propiedades del asistente se define rellenando los miembros de una estructura [**PROPSHEETHEADER**](pss-propsheetheader.md) . Esta estructura le permite especificar las páginas que componen el asistente y el orden predeterminado en el que se muestran, junto con varios parámetros relacionados. A continuación, inicie el asistente mediante una llamada a la función [**hoja**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) .

En el estilo Wizard97, se omite el miembro **pszCaption** de la estructura [**PROPSHEETHEADER**](pss-propsheetheader.md) . En su lugar, el asistente muestra el título que se especifica en la plantilla de cuadro de diálogo de la página actual. Si la plantilla no tiene un título, se muestra el título de la página anterior. Por lo tanto, para mostrar el mismo título en todas las páginas, especifique el título en la plantilla para la página de introducción.

En el estilo del asistente de Aero, el título del cuadro de diálogo se toma de **pszCaption**.

Si ha creado una matriz de identificadores HPROPSHEETPAGE para las páginas, asigne la matriz al miembro **phpage** . Si en su lugar ha creado una matriz de estructuras [**PROPSHEETPAGE**](pss-propsheetpage.md) , asigne la matriz al miembro **ppsp** y establezca la marca PSH \_ PROPSHEETPAGE en el miembro **dwFlags** .

En el ejemplo siguiente se asignan valores a *PSH*, una estructura [**PROPSHEETHEADER**](pss-propsheetheader.md) y se llama a la función [**hoja**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) para iniciar el asistente. El Asistente para Wizard97 tiene marcas de agua y gráficos de encabezado, especificados por sus identificadores de recursos. La matriz *ahpsp* contiene todos los identificadores de HPROPSHEETPAGE y define el orden predeterminado en el que se muestran.


```C++
// g_hInstance is the global HINSTANCE of the application.
// ahpsp is an array of HPROPSHEETPAGE handles.

PROPSHEETHEADER psh = { sizeof(psh) };

psh.hInstance      = g_hInstance;
psh.hwndParent     = NULL;
psh.phpage         = ahpsp;
psh.dwFlags        = PSH_WIZARD97 | PSH_WATERMARK | PSH_HEADER;
psh.pszbmWatermark = MAKEINTRESOURCE(IDB_WATERMARK);
psh.pszbmHeader    = MAKEINTRESOURCE(IDB_BANNER);
psh.nStartPage     = 0;
psh.nPages         = 4;

PropertySheet(&psh);
```



### <a name="the-dialog-box-procedure"></a>El procedimiento de cuadro de diálogo

Cada página del asistente necesita un procedimiento de cuadro de diálogo para procesar los mensajes de Windows, especialmente las notificaciones de sus controles y del asistente. Los tres mensajes que casi todos los asistentes deben ser capaces de controlar son [**WM \_ INITDIALOG**](/windows/desktop/dlgbox/wm-initdialog), [**WM \_ Destroy**](/windows/desktop/winmsg/wm-destroy)y [**WM \_ Notify**](wm-notify.md).

El mensaje de [**\_ notificación de WM**](wm-notify.md) se recibe antes de que se muestre la página y cuando se hace clic en cualquiera de los botones del asistente. El parámetro *lParam* del mensaje es un puntero a una estructura de encabezado [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) . El identificador de la notificación se encuentra en el miembro de **código** de la estructura. Las cuatro notificaciones que la mayoría de los asistentes deben controlar son las siguientes.



| Código                                | Descripción                                 |
|-------------------------------------|---------------------------------------------|
| [PSN \_ SETACTIVE](psn-setactive.md) | Se envía antes de que se muestre la página.          |
| [PSN \_ WIZBACK](psn-wizback.md)     | Se envía cuando se hace clic en el botón **atrás** .   |
| [PSN \_ WIZNEXT](psn-wiznext.md)     | Se envía cuando se hace clic en el botón **siguiente** .   |
| [PSN \_ WIZFINISH](psn-wizfinish.md) | Se envía cuando se hace clic en el botón **Finalizar** . |



 

### <a name="handle-wm_initdialog-and-wm_destroy"></a>Administrar WM \_ INITDIALOG y WM \_ Destroy

Cuando una página está a punto de mostrarse por primera vez, el procedimiento del cuadro de diálogo recibe un mensaje de [**\_ INITDIALOG de WM**](/windows/desktop/dlgbox/wm-initdialog) . El control de este mensaje permite al asistente realizar las tareas de inicialización necesarias, como almacenar datos personalizados o establecer fuentes.

Cuando se destruya la hoja de propiedades, recibirá un mensaje de [**\_ destrucción de WM**](/windows/desktop/winmsg/wm-destroy) . El sistema destruye automáticamente el asistente, pero el control de este mensaje le permite realizar cualquier limpieza necesaria.

### <a name="handle-psn_setactive"></a>Controlar PSN \_ SETACTIVE

El código de notificación [PSN \_ SETACTIVE](psn-setactive.md) se envía cada vez que una página está a punto de ser visible. La primera vez que se visita una página, PSN \_ SETACTIVE sigue el mensaje de [**\_ INITDIALOG de WM**](/windows/desktop/dlgbox/wm-initdialog) . Si posteriormente se vuelve a visitar la página, recibirá una notificación de PSN \_ SETACTIVE. Normalmente, esta notificación se controla para inicializar los datos de la página y habilitar los botones adecuados.

De forma predeterminada, el asistente muestra los botones **atrás**, **siguiente** y **Cancelar** , con todos los botones habilitados. Para deshabilitar un botón o mostrar **Finalizar** en lugar de **siguiente**, debe enviar un mensaje de [**PSM \_ SETWIZBUTTONS**](psm-setwizbuttons.md) . Después de enviar este mensaje, el estado de los botones se conserva hasta que otro mensaje de **PSM \_ SETWIZBUTTONS** lo modifique, incluso si se selecciona una nueva página. Normalmente, todos los controladores de [ \_ SETACTIVE de PSN](psn-setactive.md) envían este mensaje para asegurarse de que cada página tiene el estado de botón correcto.

Puede cambiar el estado del botón con este mensaje en cualquier momento. Por ejemplo, puede que desee que el botón **siguiente** esté deshabilitado inicialmente. Una vez que un usuario ha especificado toda la información necesaria, puede enviar otro mensaje de [**PSM \_ SETWIZBUTTONS**](psm-setwizbuttons.md) para habilitar el botón **siguiente** y permitir que el usuario pase a la página siguiente.

En el fragmento de código siguiente se usa la macro [**PropSheet \_ SetWizButtons**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setwizbuttons) para habilitar los botones **atrás** y **siguiente** en una página interior antes de que se muestre.


```C++
case WM_NOTIFY :
    {
        LPNMHDR pnmh = (LPNMHDR)lParam;
        
        switch(pnmh->code)
        {
        
        ...
        
        case PSN_SETACTIVE :
        
            ...
            
            // This is an interior page.
            PropSheet_SetWizButtons(hwnd, PSWIZB_NEXT | PSWIZB_BACK);
            
            ...
        }
    ...
    
    }
```



### <a name="handle-psn_wiznext-psnwizback-and-psn_wizfinish"></a>Administrar PSN \_ WIZNEXT, PSNWIZBACK y PSN \_ WIZFINISH

Cuando se haga clic en un botón **siguiente** o **atrás** , recibirá un código de notificación [PSN \_ WIZNEXT](psn-wiznext.md) o [PSN \_ WIZBACK](psn-wizback.md) . De forma predeterminada, el asistente pasa automáticamente a la página siguiente o anterior en el orden definido al crear la hoja de propiedades. Una razón habitual para controlar estas notificaciones es evitar que el usuario cambie las páginas o invalide el orden de página predeterminado.

Para evitar que el usuario cambie de página, controle la notificación del botón, llame a la función [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) con el valor de DWL \_ MSGRESULT establecido en – 1 y devuelva **true**. Por ejemplo:


```C++
case PSN_WIZNEXT :

        ...
        
        // Do not go to the next page yet.
        SetWindowLong(hwnd, DWL_MSGRESULT, -1);
        
        return TRUE;
        
        ...
```



Para invalidar el orden estándar e ir a una página determinada, llame a [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) con el valor de DWL \_ MSGRESULT establecido en el identificador de recurso del cuadro de diálogo de la página y devuelva **true**. Por ejemplo:


```C++
case PSN_WIZNEXT :

        ...
        
        // Go straight to the completion page.
        SetWindowLong(hwnd, DWL_MSGRESULT, IDD_FINISH);
        
        return TRUE;
        
        ...
```



Cuando se haga clic en el botón **Finalizar** o **Cancelar** , recibirá un código de notificación [PSN \_ WIZFINISH](psn-wizfinish.md) o [PSN \_ RESET](psn-reset.md) , respectivamente. Cuando se hace clic en cualquiera de estos botones, el sistema lo destruye automáticamente. Sin embargo, puede controlar estas notificaciones si necesita realizar tareas de limpieza antes de que se destruya el asistente. Para evitar que el asistente se destruya cuando reciba una notificación de \_ WIZFINISH de PSN, llame a [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) con el valor de DWL \_ MSGRESULT establecido en **true** y devuelva **true**. Por ejemplo:


```C++
case PSN_WIZFINISH :

        ...
        
        // Not finished yet.
        SetWindowLong(hwnd, DWL_MSGRESULT, TRUE);
        
        return TRUE;
        
        ...
```



### <a name="backward-compatible-wizards"></a>Asistentes compatibles con versiones anteriores

En la sección anterior se supone que está implementando un asistente para un sistema con la [versión 5](common-control-versions.md) o posterior de los controles comunes.

Si está escribiendo un asistente para sistemas con versiones anteriores de los controles comunes, muchas de las características descritas en la sección anterior no estarán disponibles. Varios de los miembros de las estructuras [**PROPSHEETHEADER**](pss-propsheetheader.md) y [**PROPSHEETPAGE**](pss-propsheetpage.md) que usa el estilo Wizard97 solo se admiten en los controles comunes versión 5 y posteriores. Sin embargo, sigue siendo posible implementar un asistente *compatible con versiones anteriores* con una apariencia similar a la del estilo Wizard97. Para ello, debe implementar explícitamente lo siguiente:

-   Agregue el gráfico de marca de agua a la plantilla de cuadro de diálogo para las páginas introducción y finalización.
-   Haga que todas las plantillas tengan el mismo tamaño. No hay ningún área de encabezado definida por el sistema independiente para las páginas interiores.
-   Cree el área del encabezado de la página interior explícitamente en las plantillas.
-   No use un gráfico de encabezado porque puede entrar en conflicto con el título o el subtítulo si cambia el tamaño del asistente.

Para obtener más información sobre los asistentes compatibles con versiones anteriores, consulte Asistente para la compatibilidad con [versiones anteriores 97](/previous-versions//ms737910(v=vs.85)).

## <a name="remarks"></a>Observaciones

Para obtener una descripción completa de los problemas de diseño de Wizard97, vea la [especificación de Wizard97](/previous-versions//ms738248(v=vs.85)), en otra parte de la Windows SDK. En este documento se proporcionan instrucciones para las dimensiones de los cuadros de diálogo, las dimensiones y los colores de los mapas de bits y la colocación de los controles.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar hojas de propiedades](using-property-sheets.md)
</dt> <dt>

[Demostración de controles comunes de Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 