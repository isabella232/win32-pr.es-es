---
description: En este tema se de abordan las interfaces y los métodos específicos necesarios para crear un controlador de vista previa.
ms.assetid: 6c240a63-c184-4b65-9483-794f5de4d695
title: Compilar controladores de vista previa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a810f15fed66d69bce32387249a2e0d678a1eb6c0dd918ec5df2e1ddbeb5be8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032923"
---
# <a name="building-preview-handlers"></a>Compilar controladores de vista previa

En este tema se de abordan las interfaces y los métodos específicos necesarios para crear un controlador de vista previa.

Un controlador de vista previa debe implementar las interfaces siguientes:

-   [IInitializeWithStream::Initialize](#iinitializewithstreaminitialize) (muy preferido), [**IInitializeWithFile**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithfile)o [**IInitializeWithItem**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem)
-   [IObjectWithSite](#iobjectwithsite)
-   [IOleWindow](#iolewindow)
-   [IPreviewHandler](#ipreviewhandler)

Si el controlador de vista previa admite la configuración visual proporcionada por el host, como el color de fondo y la fuente, también debe implementar la siguiente interfaz:

-   [IPreviewHandlerVisuals](#ipreviewhandlervisuals)

En este tema se supone que el controlador de vista previa se inicializa con una secuencia y se registra para una extensión de nombre de archivo determinada.

## <a name="iinitializewithstreaminitialize"></a>IInitializeWithStream::Initialize

Almacene los [**parámetros IStream**](/windows/win32/api/objidl/nn-objidl-istream) y mode para que pueda leer los datos del elemento cuando esté listo para obtener una vista previa del elemento. No cargue los datos en [**Inicializar**](/windows/desktop/api/Propsys/nf-propsys-iinitializewithstream-initialize). Cargue los datos en [**IPreviewHandler::D oPreview**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-dopreview) justo antes de representar.

## <a name="iobjectwithsite"></a>IObjectWithSite

-   [IObjectWithSite::SetSite](#iobjectwithsitesetsite)
-   [IObjectWithSite::GetSite](#iobjectwithsitegetsite)

### <a name="iobjectwithsitesetsite"></a>IObjectWithSite::SetSite

Almacene el [**puntero IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) para su acceso posterior.

Si actualmente tiene una referencia a un [**objeto IPreviewHandlerFrame,**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandlerframe) suéltelo. Use el puntero [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) almacenado para llamar a [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) en el sitio para una nueva **referencia IPreviewHandlerFrame.**

Si actualmente tiene una tabla de aceleradores, destruyéla. Llame a [**IPreviewHandlerFrame::GetWindowContext**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandlerframe-getwindowcontext) para obtener una nueva tabla de aceleradores. Almacene esta tabla. Tenga en cuenta que solo se usa como una lista de teclas de aceleración que admite el marco. Los comandos de las entradas del acelerador se omiten.

### <a name="iobjectwithsitegetsite"></a>IObjectWithSite::GetSite

Devuelve el puntero del sitio, sea cual sea.

## <a name="iolewindow"></a>IOleWindow

-   [IOleWindow::ContextSensitiveHelp](#iolewindowcontextsensitivehelp)
-   [IOleWindow::GetWindow](#iolewindowgetwindow)

### <a name="iolewindowcontextsensitivehelp"></a>IOleWindow::ContextSensitiveHelp

Devuelve E \_ NOTIMPL para este método.

### <a name="iolewindowgetwindow"></a>IOleWindow::GetWindow

Si la ventana del controlador de vista previa existe actualmente, devuelva el **HWND** de esa ventana y S \_ OK. Si la ventana no existe, devuelva E \_ FAIL.

## <a name="ipreviewhandler"></a>IPreviewHandler

-   [IPreviewHandler::SetWindow](#ipreviewhandlersetwindow)
-   [IPreviewHandler::SetRect](#ipreviewhandlersetrect)
-   [IPreviewHandler::D oPreview](#ipreviewhandlerdopreview)
-   [IPreviewHandler::SetFocus](#ipreviewhandlersetfocus)
-   [IPreviewHandler::QueryFocus](#ipreviewhandlerqueryfocus)
-   [IPreviewHandler::TranslateAccelerator](#ipreviewhandlertranslateaccelerator)
-   [IPreviewHandler::Unload](#ipreviewhandlerunload)

### <a name="ipreviewhandlersetwindow"></a>IPreviewHandler::SetWindow

Establezca el *parámetro hwnd* de este método en el elemento primario del HWND del controlador de vista **previa.** Se puede llamar a este método varias veces. Cambie el tamaño de la vista previa para que se represente solo en el área descrita por el *parámetro prc.*

Si el controlador de vista previa está en proceso de representación, use el método [**IPreviewHandler::SetWindow**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-setwindow) para cambiar el elemento primario del controlador de vista previa. Cambie también el área en la que se representa el previewer.

### <a name="ipreviewhandlersetrect"></a>IPreviewHandler::SetRect

Cambie el tamaño de la vista previa para que solo se represente en el área descrita por prc de *este método.*

Si el previewer está en proceso de representación, cambie el área en la que se representa el previewer.

### <a name="ipreviewhandlerdopreview"></a>IPreviewHandler::D oPreview

Aquí es donde se realiza el trabajo real. Puesto que una versión preliminar es dinámica, el contenido de la versión preliminar solo se debe cargar cuando sea necesario. No cargue contenido en la inicialización.

Si la ventana del controlador de vista previa no existe, cándala. Las ventanas del controlador de vista previa deben ser elementos secundarios de la ventana proporcionada por [**IPreviewHandler::SetWindow**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-setwindow). Deben ser el tamaño proporcionado por **IPreviewHandler::SetWindow** e [**IPreviewHandler::SetRect**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-setrect) (lo que se llamó más recientemente).

Una vez que tenga una ventana, cargue los datos de [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) con los que se inicializó el controlador de vista previa y represente los datos en la ventana del controlador de vista previa.

### <a name="ipreviewhandlersetfocus"></a>IPreviewHandler::SetFocus

Se llama a este método cuando el foco entra en el panel de lectura a través de una acción de tabulación. Puesto que se puede especificar como una pestaña hacia delante o una pestaña inversa, use el estado actual de la tecla MAYÚS para decidir si la primera o la última detenerse en el panel de lectura debe recibir el foco.

### <a name="ipreviewhandlerqueryfocus"></a>IPreviewHandler::QueryFocus

Este método debe llamar a [**la función GetFocus**](/windows/win32/api/winuser/nf-winuser-getfocus) y devolver el resultado de esa llamada en el *parámetro phwnd.*

### <a name="ipreviewhandlertranslateaccelerator"></a>IPreviewHandler::TranslateAccelerator

El bombeo de mensajes del proceso del controlador de vista previa llama a este método (ya sea prevhost.exe o un servidor local personalizado) en respuesta a las pulsaciones de tecla del usuario. Los controladores de vista previa deben controlar estas pulsaciones de teclas o reenviarlas a su host según el algoritmo que se detalla a continuación.

Sin embargo, dado que las versiones preliminares son de solo lectura, la entrada de teclado debe ser mínima y las optimizaciones como esta no son necesarias en muchos casos.

Si el acelerador de teclado pasado a este método a través de la bomba de mensajes es un acelerador que el controlador de vista previa acepta, procese y devuelva S \_ OK. Si el controlador no acepta ese acelerador, el mensaje del acelerador se puede devolver hasta el marco que se va a controlar.

Hay dos opciones para reenviar los aceleradores de teclado al marco:

El modelo más sencillo es reenviar todas las pulsaciones de tecla al host mediante [**IPreviewHandlerFrame::TranslateAccelerator**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandlerframe-translateaccelerator). Esto se hace en el ejemplo de controlador de versión preliminar proporcionado con Windows Software Development Kit (SDK). Todos los controladores de versión preliminar de baja integridad deben usar este modelo. Si el controlador de vista previa no controla el acelerador, llame a **IPreviewHandlerFrame::TranslateAccelerator** y devuelva su resultado.

El otro modelo es usar una tabla de aceleradores como optimización para evitar el envío de demasiadas pulsaciones de teclas a través de los límites del proceso:

1.  Cuando [**se llame a IObjectWithSite::SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) en el controlador de versión preliminar, adquiera la tabla de aceleradores a través de [**IPreviewHandlerFrame::GetWindowContext**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandlerframe-getwindowcontext). (Asegúrese de liberar el identificador de la tabla de aceleradores cuando se destruya el controlador de vista previa).
2.  Si el controlador de vista previa controla el acelerador, controle y devuelva S \_ OK.
3.  Si el controlador de vista previa no controla el acelerador, compare el mensaje [**mediante IsAccelerator**](/windows/win32/api/ole2/nf-ole2-isaccelerator) con la tabla de aceleradores adquirida.
4.  Si el acelerador coincide con una entrada de esa tabla de aceleradores, llame a [**IPreviewHandlerFrame::TranslateAccelerator**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandlerframe-translateaccelerator) y devuelva su resultado.
5.  Si el acelerador no coincide con ninguna entrada de la tabla del acelerador, devuelva S \_ FALSE.

### <a name="ipreviewhandlerunload"></a>IPreviewHandler::Unload

Cuando se llama a este método, detenga cualquier representación, libere los recursos asignados mediante la lectura de datos de la secuencia y libere el [**propio IStream.**](/windows/win32/api/objidl/nn-objidl-istream)

Una vez que se llama a este método, el controlador debe reinicializarse antes de cualquier intento de llamar de nuevo a [**IPreviewHandler::D oPreview.**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-dopreview)

## <a name="ipreviewhandlervisuals"></a>IPreviewHandlerVisuals

-   [IPreviewHandlerVisuals::SetBackgroundColor](#ipreviewhandlervisualssetbackgroundcolor)
-   [IPreviewHandlerVisuals::SetFont](#ipreviewhandlervisualssetfont)
-   [IPreviewHandlerVisuals::SetTextColor](#ipreviewhandlervisualssettextcolor)

Estos métodos deben implementarse al dirigir el controlador de vista previa para que responda a los esquemas de color y fuente del host. El host consulta el controlador para [**IPreviewHandlerVisuals**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandlervisuals). Si se admite, el host le proporciona color, fuente y color de texto.

### <a name="ipreviewhandlervisualssetbackgroundcolor"></a>IPreviewHandlerVisuals::SetBackgroundColor

Almacene este color y úselo durante la representación cuando desee proporcionar un color de fondo. Por ejemplo, para rellenar la ventana cuando el controlador se representa en un área menor que el área proporcionada por [**IPreviewHandler::SetWindow**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-setwindow) e [**IPreviewHandler::SetRect**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-setrect). Sin embargo, tenga en cuenta que no debe dibujar fuera del área proporcionada por esos métodos.

Si se llama a este método mientras la vista previa ya se está representando, la representación se debe reiniciar con este color de fondo.

### <a name="ipreviewhandlervisualssetfont"></a>IPreviewHandlerVisuals::SetFont

Almacene esta información de fuente y úsela durante la representación cuando desee mostrar texto coherente con la configuración Windows Vista actual.

### <a name="ipreviewhandlervisualssettextcolor"></a>IPreviewHandlerVisuals::SetTextColor

Almacene esta información de color de texto y úsela durante la representación cuando desee mostrar texto coherente con la configuración Windows Vista actual.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Controladores de vista previa y host de versión preliminar de Shell](preview-handlers.md)
</dt> <dt>

[Cómo registrar un controlador de vista previa](how-to-register-a-preview-handler.md)
</dt> <dt>

[Directrices del controlador de vista previa](preview-handler-guidelines.md)
</dt> </dl>

 

 
