---
description: En este tema se describen las interfaces y los métodos específicos necesarios para crear un controlador de vista previa.
ms.assetid: 6c240a63-c184-4b65-9483-794f5de4d695
title: Crear controladores de vista previa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a309873cf082071d5f426ce0ba6d039107c59665
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360169"
---
# <a name="building-preview-handlers"></a>Crear controladores de vista previa

En este tema se describen las interfaces y los métodos específicos necesarios para crear un controlador de vista previa.

Un controlador de vista previa debe implementar las interfaces siguientes:

-   [IInitializeWithStream:: Initialize](#iinitializewithstreaminitialize) (muy recomendable), [**IInitializeWithFile**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithfile)o [**IInitializeWithItem**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem)
-   [IObjectWithSite](#iobjectwithsite)
-   [IOleWindow](#iolewindow)
-   [IPreviewHandler](#ipreviewhandler)

Si el controlador de vista previa admite la configuración visual proporcionada por el host, como el color de fondo y la fuente, también debe implementar la siguiente interfaz:

-   [IPreviewHandlerVisuals](#ipreviewhandlervisuals)

En este tema se supone que el controlador de vista previa se inicializa con una secuencia y está registrado para una extensión de nombre de archivo determinada.

## <a name="iinitializewithstreaminitialize"></a>IInitializeWithStream:: Initialize

Almacene los parámetros de modo [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) y para poder leer los datos del elemento cuando esté listo para obtener una vista previa del elemento. No cargue los datos en [**Initialize**](/windows/desktop/api/Propsys/nf-propsys-iinitializewithstream-initialize). Cargue los datos en [**IPreviewHandler::D opreview**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-dopreview) justo antes de representarlo.

## <a name="iobjectwithsite"></a>IObjectWithSite

-   [IObjectWithSite:: SetSite](#iobjectwithsitesetsite)
-   [IObjectWithSite:: GetSite](#iobjectwithsitegetsite)

### <a name="iobjectwithsitesetsite"></a>IObjectWithSite:: SetSite

Almacene el puntero [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) para el acceso posterior.

Si actualmente tiene una referencia a un objeto [**IPreviewHandlerFrame**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandlerframe) , suéltelo. Use el puntero [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) almacenado para llamar a [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) en el sitio para obtener una nueva referencia de **IPreviewHandlerFrame** .

Si actualmente tiene una tabla de aceleradores, destruyala. Llame a [**IPreviewHandlerFrame:: GetWindowContext**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandlerframe-getwindowcontext) para obtener una nueva tabla de aceleradores. Almacene esta tabla. Tenga en cuenta que solo se utiliza como una lista de teclas de aceleración que admite el marco. Los comandos de las entradas de acelerador se omiten.

### <a name="iobjectwithsitegetsite"></a>IObjectWithSite:: GetSite

Devuelve el puntero del sitio, sea cual sea su valor.

## <a name="iolewindow"></a>IOleWindow

-   [IOleWindow::ContextSensitiveHelp](#iolewindowcontextsensitivehelp)
-   [IOleWindow::GetWindow](#iolewindowgetwindow)

### <a name="iolewindowcontextsensitivehelp"></a>IOleWindow::ContextSensitiveHelp

Devuelve E \_ NOTIMPL para este método.

### <a name="iolewindowgetwindow"></a>IOleWindow::GetWindow

Si la ventana del controlador de vista previa existe actualmente, devuelva el **hWnd** de esa ventana y el valor \_ correcto. Si la ventana no existe, se devuelve E \_ produce un error.

## <a name="ipreviewhandler"></a>IPreviewHandler

-   [IPreviewHandler:: SetWindow](#ipreviewhandlersetwindow)
-   [IPreviewHandler::SetRect](#ipreviewhandlersetrect)
-   [IPreviewHandler::D oPreview](#ipreviewhandlerdopreview)
-   [IPreviewHandler:: SetFocus](#ipreviewhandlersetfocus)
-   [IPreviewHandler::QueryFocus](#ipreviewhandlerqueryfocus)
-   [IPreviewHandler:: TranslateAccelerator](#ipreviewhandlertranslateaccelerator)
-   [IPreviewHandler:: Unload](#ipreviewhandlerunload)

### <a name="ipreviewhandlersetwindow"></a>IPreviewHandler:: SetWindow

Establezca el parámetro *hWnd* de este método en el elemento primario del **hWnd** del controlador de vista previa. Se puede llamar a este método varias veces. Cambie el tamaño de la vista previa para que se represente solo en el área descrita por el parámetro *PRC* .

Si el objeto de vista previa está en proceso de representación, utilice el método [**IPreviewHandler:: SetWindow**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-setwindow) para cambiar el elemento primario del control de vista previa. Cambie también el área en la que se representa la vista previa.

### <a name="ipreviewhandlersetrect"></a>IPreviewHandler::SetRect

Cambie el tamaño de la vista previa para que solo se represente en el área descrita por la *RPC* de este método.

Si el previsor está en proceso de representación, cambie el área en la que se representa el previsualizador.

### <a name="ipreviewhandlerdopreview"></a>IPreviewHandler::D oPreview

Aquí es donde se realiza el trabajo real. Puesto que una vista previa es dinámica, el contenido de la vista previa solo debe cargarse cuando sea necesario. No cargue el contenido en la inicialización.

Si la ventana controlador de vista previa no existe, créela. Las ventanas del controlador de vista previa deben ser elementos secundarios de la ventana proporcionada por [**IPreviewHandler:: SetWindow**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-setwindow). Deben ser el tamaño proporcionado por **IPreviewHandler:: SetWindow** y [**IPreviewHandler:: SetRect**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-setrect) (lo que se llamó más recientemente).

Una vez que tenga una ventana, cargue los datos de la [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) en la que se ha inicializado el controlador de vista previa y represente los datos en la ventana del controlador de vista previa.

### <a name="ipreviewhandlersetfocus"></a>IPreviewHandler:: SetFocus

Se llama a este método cuando el foco entra en el panel de lectura a través de una acción de tabulación. Dado que se puede escribir como una pestaña de avance o una pestaña inversa, use el estado actual de la tecla Mayús para decidir si la primera o última posición de tabulación en el panel de lectura debe recibir el foco.

### <a name="ipreviewhandlerqueryfocus"></a>IPreviewHandler::QueryFocus

Este método debe llamar a la función [**GetFocus**](/windows/win32/api/winuser/nf-winuser-getfocus) y devolver el resultado de esa llamada en el parámetro *phwnd* .

### <a name="ipreviewhandlertranslateaccelerator"></a>IPreviewHandler:: TranslateAccelerator

Este método es invocado por el bombeo de mensajes del proceso del controlador de vista previa (ya sea prevhost.exe o un servidor local personalizado) en respuesta a las pulsaciones de teclas del usuario. Los controladores de vista previa deben controlar estas pulsaciones de teclas o reenviarlas a su host según el algoritmo que se detalla a continuación.

Sin embargo, dado que las vistas previas son de solo lectura, la entrada de teclado debe ser mínima y las optimizaciones como esta no se necesitan en muchos casos.

Si el acelerador de teclado que se pasa a este método a través del bombeo de mensajes es un acelerador que el controlador de vista previa acepta, procese y devuelva los elementos \_ correctos. Si el controlador no acepta ese acelerador, el mensaje del acelerador se puede devolver hasta el fotograma que se va a controlar.

Hay dos opciones para reenviar aceleradores de teclado al fotograma:

El modelo más sencillo es reenviar todas las pulsaciones de tecla al host mediante [**IPreviewHandlerFrame:: TranslateAccelerator**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandlerframe-translateaccelerator). Esto se hace en el ejemplo de controlador de vista previa proporcionado con el kit de desarrollo de software (SDK) de Windows. Todos los controladores de vista previa de baja integridad deben usar este modelo. Si el controlador de vista previa no controla el acelerador, llame a **IPreviewHandlerFrame:: TranslateAccelerator** y devuelva su resultado.

El otro modelo es usar una tabla de aceleradores como una optimización para evitar el envío de demasiadas pulsaciones de tecla en los límites del proceso:

1.  Cuando se llama a [**IObjectWithSite:: SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) en el controlador de vista previa, adquiera la tabla de aceleradores a través de [**IPreviewHandlerFrame:: GetWindowContext**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandlerframe-getwindowcontext). (Asegúrese de liberar el identificador de la tabla de aceleradores cuando se destruya el controlador de vista previa).
2.  Si el controlador de vista previa controla el acelerador, debe controlarlo y devolver S \_ correcto.
3.  Si el controlador de vista previa no controla el acelerador, compare el mensaje con [**IsAccelerator**](/windows/win32/api/ole2/nf-ole2-isaccelerator) en la tabla de aceleradores adquirida.
4.  Si el acelerador coincide con una entrada de esa tabla de aceleradores, llame a [**IPreviewHandlerFrame:: TranslateAccelerator**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandlerframe-translateaccelerator) y devuelva su resultado.
5.  Si el acelerador no coincide con ninguna entrada de la tabla de aceleradores, devuelve S \_ false.

### <a name="ipreviewhandlerunload"></a>IPreviewHandler:: Unload

Cuando se llama a este método, se detiene cualquier representación, se liberan los recursos asignados mediante la lectura de los datos de la secuencia y se libera la propia [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) .

Una vez que se llama a este método, se debe reinicializar el controlador antes de cualquier intento de llamar a [**IPreviewHandler::D opreview**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-dopreview) de nuevo.

## <a name="ipreviewhandlervisuals"></a>IPreviewHandlerVisuals

-   [IPreviewHandlerVisuals::SetBackgroundColor](#ipreviewhandlervisualssetbackgroundcolor)
-   [IPreviewHandlerVisuals:: SetFont](#ipreviewhandlervisualssetfont)
-   [IPreviewHandlerVisuals::SetTextColor](#ipreviewhandlervisualssettextcolor)

Estos métodos deben implementarse al dirigir el controlador de vista previa para responder a los esquemas de fuente y color del host. El host consulta el controlador de [**IPreviewHandlerVisuals**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandlervisuals). Si se detecta que es compatible, el host le proporciona color, fuente y color de texto.

### <a name="ipreviewhandlervisualssetbackgroundcolor"></a>IPreviewHandlerVisuals::SetBackgroundColor

Almacene este color y úselo durante la representación cuando desee proporcionar un color de fondo. Por ejemplo, para rellenar la ventana cuando el controlador se representa en un área menor que el área proporcionada por [**IPreviewHandler:: SetWindow**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-setwindow) y [**IPreviewHandler:: SetRect**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-setrect). Sin embargo, tenga en cuenta que no debe dibujar fuera del área proporcionada por esos métodos.

Si se llama a este método mientras ya se está representando la vista previa, la representación debe reiniciarse con este color de fondo.

### <a name="ipreviewhandlervisualssetfont"></a>IPreviewHandlerVisuals:: SetFont

Almacene esta información de fuente y úsela durante la representación cuando desee mostrar texto coherente con la configuración actual de Windows Vista.

### <a name="ipreviewhandlervisualssettextcolor"></a>IPreviewHandlerVisuals::SetTextColor

Almacene esta información de color del texto y úsela durante la representación cuando desee mostrar texto coherente con la configuración actual de Windows Vista.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Controladores de vista previa y host de vista previa de Shell](preview-handlers.md)
</dt> <dt>

[Cómo registrar un controlador de vista previa](how-to-register-a-preview-handler.md)
</dt> <dt>

[Instrucciones de controlador de vista previa](preview-handler-guidelines.md)
</dt> </dl>

 

 
