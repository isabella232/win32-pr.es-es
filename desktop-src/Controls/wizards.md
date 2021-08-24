---
title: Cómo crear asistentes
description: Un asistente es un tipo de hoja de propiedades que proporciona una manera sencilla y eficaz de guiar a los usuarios a través de un procedimiento.
ms.assetid: f8def159-0a68-4d7f-9840-c7b6b906ed08
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4254b448c719e3e1397fceadfcdc28475eaeae588f6f1eb0f0168cea07327d3d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119655840"
---
# <a name="how-to-create-wizards"></a>Cómo crear asistentes

Un asistente es un tipo de hoja de propiedades que proporciona una manera sencilla y eficaz de guiar a los usuarios a través de un procedimiento.

Los asistentes son una de las claves para simplificar la experiencia del usuario. Permiten realizar una operación compleja, como la configuración de una aplicación, y dividirla en una serie de pasos sencillos. En cada punto del proceso, puede proporcionar una explicación de lo que se necesita y mostrar controles que permiten al usuario realizar selecciones y escribir texto.

Un asistente es realmente un tipo de hoja de propiedades. Una hoja de propiedades es básicamente un contenedor para una colección de *páginas*, donde cada página es un cuadro de diálogo independiente. Mientras que las hojas de propiedades normales permiten al usuario acceder a cualquier página en cualquier momento, los asistentes presentan páginas en secuencia. En lugar de pestañas, los botones se usan para navegar hacia delante y hacia atrás. La aplicación controla el orden en el que se muestran las páginas y se puede modificar en función de la entrada del usuario.

Hay dos estilos principales de asistente: el estilo Wizard97 anterior y el estilo Deer introducido en Windows Vista. Para obtener ilustraciones, vea [Acerca de las hojas de propiedades](property-sheets.md). (Un tercer estilo, usando solo el PSH \_ Wizard o PSH WIZARD LITE marca, presenta una secuencia simple de hojas de \_ \_ propiedades sin encabezados ni marcas de agua).

> [!Note]  
> Una "marca de agua" en el contexto de los asistentes es un mapa de bits que aparece en el margen izquierdo de algunas páginas.

 

En la explicación de la mayoría de este documento se da por supuesto que está implementando un asistente para un sistema con la versión [5.80](common-control-versions.md) o posterior de los controles comunes. Si intenta usar el estilo Wizard97 con versiones anteriores de los controles comunes, la aplicación puede compilarse, pero no se mostrará correctamente. Para obtener una explicación sobre cómo crear un asistente compatible con Wizard97 en sistemas anteriores, vea Asistentes compatibles con versiones anteriores más adelante en este tema.

## <a name="what-you-need-to-know"></a>Lo que necesita saber

### <a name="technologies"></a>Tecnologías

-   [Windows Controles](window-controls.md)

### <a name="prerequisites"></a>Prerrequisitos

-   C/C++
-   Windows Interfaz de usuario programación

## <a name="instructions"></a>Instructions

### <a name="wizard-implementation"></a>Implementación del asistente

Implementar un asistente es similar a implementar una hoja de propiedades normal. En el nivel más básico, se trata de establecer una de las siguientes marcas o combinaciones de marcas en la estructura [**PROPSHEETHEADER**](pss-propsheetheader.md) que define la hoja de propiedades.



| Marca                           | Estilo                                                                                                                                                 |
|--------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| ASISTENTE PARA \_ PSH                    | Un asistente simple sin encabezados ni mapas de bits.                                                                                                           |
| PSH \_ WIZARD \_ LITE              | Similar a PSH WIZARD, con algunas pequeñas diferencias en la apariencia; por ejemplo, el divisor situado encima de los botones se establece en el ancho completo \_ de la ventana. |
| PSH \_ WIZARD97                  | Asistente97 con encabezados (opcionales), mapas de bits de encabezado y marcas de agua.                                                                            |
| PSH \_ WIZARD \| PSH \_ AEROWIZARD | Un asistente de Avión. Los asistentes de Avión no usan marcas de agua ni mapas de bits de encabezado. Requieren el modelo de apartamento de un solo subproceso (STA).                         |



 

El procedimiento básico para implementar un asistente es el siguiente:

1.  Cree una plantilla de cuadro de diálogo para cada página.
2.  Defina las páginas mediante la creación de [**una estructura PROPSHEETPAGE**](pss-propsheetpage.md) para cada página. Esta estructura define la página y contiene punteros a la plantilla de cuadro de diálogo y a cualquier mapa de bits u otros recursos.
3.  Pase la [**estructura PROPSHEETPAGE**](pss-propsheetpage.md) que se creó en el paso anterior a la función [**CreatePropertySheetPage**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea) para crear el identificador HPROPSHEETPAGE de la página.
4.  Defina el asistente mediante la creación [**de una estructura PROPSHEETHEADER**](pss-propsheetheader.md) para él.
5.  Pase la [**estructura PROPSHEETHEADER**](pss-propsheetheader.md) a la [**función PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) para mostrar el asistente.
6.  Implemente procedimientos de cuadro de diálogo para que cada página controle los mensajes de notificación de los controles de la página y los botones del asistente y procese otros Windows mensajes.

### <a name="create-the-dialog-box-templates"></a>Crear las plantillas de cuadro de diálogo

Hay dos tipos básicos de página del asistente: exterior e interior. Las páginas exteriores son las páginas de introducción (bienvenida) y finalización. Todas las demás son páginas interiores.

**Plantillas de cuadro de diálogo Página exterior**

El diseño básico de las páginas de introducción y finalización es idéntico. En la ilustración siguiente se muestra una página de introducción del Asistente97 de ejemplo, con una marca de agua de marcador de posición.

![captura de pantalla que muestra una página del asistente con un gráfico a la izquierda, el texto del título y el cuerpo a la derecha y los botones Atrás, Siguiente y Cancelar en la parte inferior](images/wiz97exterior.png)

Para las páginas exteriores del Asistente97, la plantilla de cuadro de diálogo es 317 x 193 unidades de diálogo. Rellena todo el asistente, excepto el título y la banda de la parte inferior que contiene los botones **Atrás,** **Siguiente** **y** Cancelar. El lado izquierdo de la plantilla, que está reservado para un mapa de bits de "marca de agua", no debe contener ningún control. La marca de agua se especifica en la estructura [**PROPSHEETHEADER**](pss-propsheetheader.md) del asistente y se agrega automáticamente a la página. Debe permitir espacio para él al diseñar la plantilla de recursos.

Al crear el mapa de bits de marca de agua, tenga en cuenta que el cuadro de diálogo puede aumentar de tamaño si, por ejemplo, el usuario elige una fuente de sistema grande. Los distintos lenguajes también tienden a tener métricas de fuente diferentes. Cuando la página crece, el área reservada para la marca de agua aumenta proporcionalmente. Sin embargo, no se puede cambiar el mapa de bits de marca de agua ni se extiende el mapa de bits para rellenar el área más grande. En su lugar, el mapa de bits se deja en su tamaño original en la parte superior izquierda del área reservada. La parte del área reservada más grande que no está cubierta por la marca de agua se rellena automáticamente con el color del píxel superior izquierdo del mapa de bits.

Si necesita tener mapas de bits de marca de agua de diferentes tamaños para diferentes métricas de fuente, dos posibles soluciones son:

-   Obtenga las métricas de fuente antes de crear el asistente y especifique un mapa de bits de marca de agua de tamaño adecuado.
-   No especifique un mapa de bits de marca de agua al crear el asistente. Wizard97 dejará el área de marca de agua en blanco. A continuación, dibuje un mapa de bits con el tamaño adecuado en el área reservada para la marca de agua.

Puede colocar controles en el área a la derecha de la marca de agua como lo haría para un cuadro de diálogo normal. El sistema determina el color de fondo de esta área y no requiere ninguna acción por su parte. Normalmente, se coloca dos controles estáticos en esta área. La parte superior contiene el título y usa una fuente en negrita grande (Verdana Bold de 12 puntos para Wizard97). El otro, que es para texto explicativo, usa la fuente de cuadro de diálogo estándar.

La principal diferencia entre las páginas de introducción y finalización son los botones del asistente y el texto de los controles estáticos. Normalmente, las páginas de introducción tienen **los** botones Siguiente y **Atrás,** con solo **el botón** Siguiente habilitado. Las páginas de finalización tienen **habilitado el** botón Atrás y **el** botón Siguiente se reemplaza por un **botón** Finalizar.

> [!Note]  
> En Asistentes para Avión, el **botón** Atrás se reemplaza por un botón de flecha en la barra de título.

 

Puede modificar el texto en el botón **Finalizar** enviando al asistente un [**mensaje \_ SETFINISHTEXT de PSM.**](psm-setfinishtext.md) De forma predeterminada, **el botón** Finalizar no incluye un acelerador de teclado. Para definir un acelerador de teclado, incluya una yerba en la cadena de texto que pase a PSM \_ SETFINISHTEXT. Por ejemplo, "&Finalizar" define "F" como el acelerador de teclado.

**Plantillas de cuadro de diálogo De página interior**

Las páginas interiores tienen un aspecto ligeramente diferente al de las páginas exteriores. En la ilustración siguiente se muestra una página interior del Asistente97 de ejemplo, con un mapa de bits de encabezado de marcador de posición.

![captura de pantalla de una página del asistente con texto de título y subtítulo y un gráfico en la parte superior, texto en el centro y botones en la parte inferior](images/wiz97interior.png)

La hoja de propiedades controla el área de encabezado de la parte superior de la página, por lo que no se incluye en la plantilla. El contenido del encabezado se especifica en la estructura [**PROPSHEETPAGE**](pss-propsheetpage.md) de la página y en la [**estructura PROPSHEETHEADER del**](pss-propsheetheader.md) asistente. Dado que la página interior debe caber entre el encabezado y los botones, la plantilla del cuadro de diálogo Wizard97 es 317 x 143 unidades de diálogo, algo más pequeña que la plantilla para las páginas exteriores.

En la ilustración siguiente se muestra un Asistente para Avión que se creó a partir de la misma plantilla.

![captura de pantalla que difiere de la anterior al tener un área de título en la parte superior y solo los botones siguiente y cancelar en la parte inferior](images/wizardaerointerior.png)

### <a name="define-the-wizard-pages"></a>Definir las páginas del asistente

Después de crear las plantillas de cuadro de diálogo y los recursos relacionados, como mapas de bits y tablas de cadenas, puede crear las páginas de la hoja de propiedades. El procedimiento es similar al de las hojas de propiedades estándar. En primer lugar, rellene los miembros adecuados de una [**estructura PROPSHEETPAGE.**](pss-propsheetpage.md) (Algunos miembros son específicos de los asistentes). A continuación, [**llame a la función CreatePropertySheetPage**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea) para crear el identificador HPROPSHEETPAGE de la página.

Las siguientes marcas relacionadas con el asistente se pueden establecer en el **miembro dwFlags** de la [**estructura PROPSHEETPAGE.**](pss-propsheetpage.md)



| Marca                   | Descripción                                                                                                                         |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| PSP \_ HIDEHEADER        | Establezca esta marca para las páginas exteriores en el Asistente97. No se muestra el encabezado y se puede mostrar una marca de agua.                                |
| USEHEADERTITLE de PSP \_    | Establezca esta marca para que las páginas interiores coloquen un título en el área de encabezado en El Asistente97 o en la parte superior del área de cliente en un Asistente para Avión. |
| \_USEHEADERSUBTITLE de PSP | Establezca esta marca para que las páginas interiores coloquen un subtítulo en el área de encabezado del Asistente97.                                                  |



 

Si ha establecido PSP USEHEADERTITLE o PSP USEHEADERSUBTITLE, asigne el título y el texto del subtítulo a los miembros \_ \_ **pszHeaderTitle** y **pszHeaderSubtitle,** respectivamente. Al asignar cadenas de texto a miembros de las estructuras [**PROPSHEETPAGE**](pss-propsheetpage.md) y [**PROPSHEETHEADER,**](pss-propsheetheader.md) puede asignar un puntero de cadena o usar la macro **MAKEINTRESOURCE** para asignar un valor desde un recurso de cadena. El recurso de cadena se carga desde el módulo especificado en el **miembro hInstance** de la **estructura PROPSHEETHEADER del** asistente.

Cuando llame a [**CreatePropertySheetPage para**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea) crear una página, asigne el resultado a un elemento de una matriz de identificadores HPROPSHEETPAGE. Esta matriz se usa al crear la hoja de propiedades. El índice de matriz del identificador de una página determina el orden predeterminado en el que se muestra. Después de crear el identificador HPROPSHEETPAGE de una página, puede reutilizar la misma estructura [**PROPSHEETPAGE**](pss-propsheetpage.md) para crear la página siguiente mediante la asignación de nuevos valores a los miembros pertinentes.

Una manera alternativa de crear páginas es usar estructuras [**PROPSHEETPAGE**](pss-propsheetpage.md) independientes para cada página y crear una matriz de estructuras. Esta matriz se usa en lugar de una matriz de identificadores HPROPSHEETPAGE al crear la hoja de propiedades. El uso **de estructuras PROPSHEETPAGE** independientes elimina la necesidad de llamar a [**CreatePropertySheetPage,**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea) pero usa más memoria. De lo contrario, no hay ninguna diferencia significativa entre los dos enfoques.

En el ejemplo siguiente se define una página Interior Wizard97 mediante la asignación de valores a una [**estructura PROPSHEETPAGE.**](pss-propsheetpage.md) En este ejemplo, el título, el subtítulo y la plantilla de cuadro de diálogo de la página se identifican por sus identificadores de recursos. A continuación, se llama a la función [**CreatePropertySheetPage**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea) para crear el identificador HPROPSHEETPAGE de la página. Dado que será la segunda página que aparecerá, el identificador se asigna a la matriz de identificadores, *ahpsp*, con un índice de 1.


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

Al crear una página, puede asignarle datos personalizados mediante el miembro **lParam** de la estructura [**PROPSHEETPAGE,**](pss-propsheetpage.md) normalmente asignándose un puntero a una estructura definida por el usuario.

Cuando se selecciona la página por primera vez, su procedimiento de cuadro de diálogo recibe un [**mensaje \_ WM INITDIALOG.**](/windows/desktop/dlgbox/wm-initdialog) El valor *lParam* del mensaje apunta a una copia de la estructura [**PROPSHEETPAGE**](pss-propsheetpage.md) de la página, desde la que puede recuperar los datos personalizados. A continuación, puede almacenar estos datos para usarlos en mensajes posteriores mediante [**SetWindowLongPtr**](/windows/desktop/api/winuser/nf-winuser-setwindowlongptra) con GWL \_ USERDATA como parámetro de índice. Varias páginas pueden tener un puntero a los mismos datos y cualquier cambio en los datos realizados por una página está disponible para las demás páginas en sus procedimientos de diálogo.

### <a name="define-the-wizard-property-sheet"></a>Definir la hoja de propiedades del asistente

Al igual que con las hojas de propiedades normales, la hoja de propiedades del asistente se define rellenando los miembros de una [**estructura PROPSHEETHEADER.**](pss-propsheetheader.md) Esta estructura permite especificar las páginas que forma el asistente y el orden predeterminado en el que se muestran, junto con varios parámetros relacionados. A continuación, inicie el asistente mediante una llamada [**a la función PropertySheet.**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta)

En el estilo Wizard97, se omite el **miembro pszCaption** de la [**estructura PROPSHEETHEADER.**](pss-propsheetheader.md) En su lugar, el asistente muestra el título especificado en la plantilla de cuadro de diálogo de la página actual. Si la plantilla no tiene un título, se muestra el título de la página anterior. Por lo tanto, para mostrar el mismo título en todas las páginas, especifique el título en la plantilla de la página de introducción.

En el estilo del Asistente para Avión, el título del cuadro de diálogo se toma de **pszCaption**.

Si ha creado una matriz de identificadores HPROPSHEETPAGE para las páginas, asigne la matriz al **miembro phpage.** Si en su lugar ha creado una matriz de estructuras [**PROPSHEETPAGE,**](pss-propsheetpage.md) asigne la matriz al miembro **ppsp** y establezca la marca PSH PROPSHEETPAGE en el \_ miembro **dwFlags.**

En el ejemplo siguiente se asignan valores a *psh*, una estructura [**PROPSHEETHEADER**](pss-propsheetheader.md) y se llama a la [**función PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) para iniciar el asistente. El asistente de estilo Wizard97 tiene gráficos de marca de agua y de encabezado, especificados por sus identificadores de recursos. La *matriz ahpsp* contiene todos los identificadores HPROPSHEETPAGE y define el orden predeterminado en el que se muestran.


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



### <a name="the-dialog-box-procedure"></a>Procedimiento del cuadro de diálogo

Cada página del asistente necesita un procedimiento de cuadro de diálogo para procesar Windows mensajes, especialmente las notificaciones de sus controles y el asistente. Los tres mensajes que casi todos los asistentes deben poder controlar son [**WM \_ INITDIALOG,**](/windows/desktop/dlgbox/wm-initdialog) [**WM \_ DESTROY**](/windows/desktop/winmsg/wm-destroy)y [**WM \_ NOTIFY.**](wm-notify.md)

El [**mensaje \_ WM NOTIFY**](wm-notify.md) se recibe antes de que se muestre la página y cuando se haga clic en cualquiera de los botones del asistente. El *parámetro lParam* del mensaje es un puntero a una estructura [**de encabezado NMHDR.**](/windows/desktop/api/richedit/ns-richedit-nmhdr) El identificador de la notificación se encuentra en el miembro de código de **la** estructura. Las cuatro notificaciones que la mayoría de los asistentes deben controlar son las siguientes.



| Código                                | Descripción                                 |
|-------------------------------------|---------------------------------------------|
| [PSN \_ SETACTIVE](psn-setactive.md) | Se envía antes de que se muestre la página.          |
| [PSN \_ WIZBACK](psn-wizback.md)     | Se envía cuando **se hace clic** en el botón Atrás.   |
| [PSN \_ WIZNEXT](psn-wiznext.md)     | Se envía cuando **se hace clic** en el botón Siguiente.   |
| [PSN \_ WIZFINISH](psn-wizfinish.md) | Se envía cuando **se hace clic** en el botón Finalizar. |



 

### <a name="handle-wm_initdialog-and-wm_destroy"></a>Controlar WM \_ INITDIALOG y WM \_ DESTROY

Cuando una página está a punto de mostrarse por primera vez, su procedimiento de cuadro de diálogo recibe un [**mensaje \_ WM INITDIALOG.**](/windows/desktop/dlgbox/wm-initdialog) El control de este mensaje permite al asistente realizar las tareas de inicialización necesarias, como almacenar datos personalizados o establecer fuentes.

Cuando se destruye la hoja de propiedades, recibe un [**mensaje WM \_ DESTROY.**](/windows/desktop/winmsg/wm-destroy) El sistema destruye automáticamente el asistente, pero el control de este mensaje le permite realizar cualquier limpieza necesaria.

### <a name="handle-psn_setactive"></a>Controlar PSN \_ SETACTIVE

El [código de notificación \_ SETACTIVE](psn-setactive.md) de PSN se envía cada vez que una página está a punto de hacerse visible. La primera vez que se visita una página, PSN \_ SETACTIVE sigue el [**mensaje WM \_ INITDIALOG.**](/windows/desktop/dlgbox/wm-initdialog) Si la página se vuelve a visitar posteriormente, recibe solo una notificación \_ SETACTIVE de PSN. Normalmente, esta notificación se controla para inicializar los datos de la página y habilitar los botones adecuados.

De forma predeterminada, el asistente  **muestra los botones Atrás,** **Siguiente** y Cancelar, con todos los botones habilitados. Para deshabilitar un botón o mostrar **Finalizar en** **lugar** de Siguiente , debe enviar un mensaje [**\_ SETWIZBUTTONS de PSM.**](psm-setwizbuttons.md) Una vez enviado este mensaje, el estado de los botones se conserva hasta que otro mensaje **\_ SETWIZBUTTONS** de PSM lo modifica, incluso si se selecciona una nueva página. Normalmente, todos [los controladores \_ SETACTIVE de PSN](psn-setactive.md) envían este mensaje para asegurarse de que cada página tiene el estado de botón correcto.

Puede cambiar el estado del botón con este mensaje en cualquier momento. Por ejemplo, puede que desee que el **botón** Siguiente se deshabilite inicialmente. Después de que un usuario haya especificado toda la información necesaria, puede  enviar otro mensaje [**DE PSM \_ SETWIZBUTTONS**](psm-setwizbuttons.md) para habilitar el botón Siguiente y permitir que el usuario continúe con la página siguiente.

El fragmento de código siguiente usa la macro [**\_ PropSheet SetWizButtons**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setwizbuttons) para habilitar los botones **Atrás** y Siguiente en una página interior antes de que se muestre. 


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



### <a name="handle-psn_wiznext-psnwizback-and-psn_wizfinish"></a>Controlar PSN \_ WIZNEXT, PSNWIZBACK y PSN \_ WIZFINISH

Cuando se **hace clic** **en** un botón Siguiente o Atrás, recibirá un código de notificación [ \_ WIZNEXT](psn-wiznext.md) o [ \_ PSN WIZBACK de PSN.](psn-wizback.md) De forma predeterminada, el asistente pasa automáticamente a la página siguiente o anterior en el orden definido cuando se crea la hoja de propiedades. Una razón común para controlar estas notificaciones es impedir que el usuario cambie de página o invalidar el orden de página predeterminado.

Para evitar que el usuario cambie de página, controle la notificación de botón, llame a la función [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) con el valor MSGRESULT de DWL establecido \_ en –1 y devuelva **TRUE.** Por ejemplo:


```C++
case PSN_WIZNEXT :

        ...
        
        // Do not go to the next page yet.
        SetWindowLong(hwnd, DWL_MSGRESULT, -1);
        
        return TRUE;
        
        ...
```



Para invalidar el orden estándar e ir a una página determinada, llame a [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) con el valor MSGRESULT de DWL establecido en el identificador de recurso del cuadro de diálogo de la página y devuelva \_ **TRUE**. Por ejemplo:


```C++
case PSN_WIZNEXT :

        ...
        
        // Go straight to the completion page.
        SetWindowLong(hwnd, DWL_MSGRESULT, IDD_FINISH);
        
        return TRUE;
        
        ...
```



Cuando se **hace** clic **en el botón** Finalizar o Cancelar, recibirá un código de notificación [ \_ WIZFINISH](psn-wizfinish.md) o PSN RESET de [PSN, \_](psn-reset.md) respectivamente. Cuando se hace clic en cualquiera de estos botones, el sistema destruye automáticamente el asistente. Sin embargo, puede controlar estas notificaciones si necesita realizar tareas de limpieza antes de que se destruya el asistente. Para evitar que el asistente se destruya cuando reciba una notificación WIZFINISH de PSN, llame a SetWindowLong con el valor MSGRESULT de DWL establecido en TRUE y devuelva \_ [](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) \_ **TRUE.**  Por ejemplo:


```C++
case PSN_WIZFINISH :

        ...
        
        // Not finished yet.
        SetWindowLong(hwnd, DWL_MSGRESULT, TRUE);
        
        return TRUE;
        
        ...
```



### <a name="backward-compatible-wizards"></a>Asistentes compatibles con versiones anteriores

En la sección anterior se da por supuesto que está implementando un asistente para un sistema con la [versión 5](common-control-versions.md) o posterior de los controles comunes.

Si va a escribir un asistente para sistemas con versiones anteriores de los controles comunes, muchas de las características que se han analizado en la sección anterior no estarán disponibles. Algunos de los miembros de las estructuras [**PROPSHEETHEADER**](pss-propsheetheader.md) y [**PROPSHEETPAGE**](pss-propsheetpage.md) que usa el estilo Wizard97 solo son compatibles con los controles comunes versión 5 y posteriores. Sin embargo, todavía es posible implementar un asistente *compatible* con versiones anteriores con una apariencia similar a la del estilo Wizard97. Para ello, debe implementar explícitamente lo siguiente:

-   Agregue el gráfico de marca de agua a la plantilla de cuadro de diálogo para las páginas de introducción y finalización.
-   Haga que todas las plantillas tienen el mismo tamaño. No hay ningún área de encabezado independiente definida por el sistema para las páginas interiores.
-   Cree el área de encabezado de la página interior explícitamente en las plantillas.
-   No use un gráfico de encabezado porque puede estar en conflicto con el título o el subtítulo si el asistente cambia de tamaño.

Para obtener más información sobre los asistentes compatibles con versiones anteriores, vea Asistente para versiones anteriores [compatibles 97.](/previous-versions//ms737910(v=vs.85))

## <a name="remarks"></a>Comentarios

Para obtener una explicación completa de los problemas de diseño del Asistente97, consulte la especificación [Wizard97](/previous-versions//ms738248(v=vs.85)), en otra parte del SDK Windows. Este documento contiene directrices para aspectos como las dimensiones de los cuadros de diálogo, las dimensiones y los colores del mapa de bits y la colocación de controles.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar hojas de propiedades](using-property-sheets.md)
</dt> <dt>

[Windows demostración de controles comunes (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 