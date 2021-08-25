---
description: El control InkPicture proporciona la capacidad de colocar una imagen en una aplicación y permitir que los usuarios agreguen entrada manuscrita encima de ella.
ms.assetid: e9fa6807-6e2a-44ec-9b8f-a560185e4367
title: Referencia del control InkPicture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d93f5727d2f3f049a579e32e5feb0ba0eaa742d2
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122471541"
---
# <a name="inkpicture-control-reference"></a>Referencia del control InkPicture

El control InkPicture proporciona la capacidad de colocar una imagen en una aplicación y permitir que los usuarios agreguen entrada manuscrita encima de ella. Está pensado para escenarios en los que la entrada de lápiz no se reconoce como texto, sino que se almacena como entrada de lápiz.

Se puede crear una instancia del control InkPicture llamando al [**método CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) en C++.

> [!Note]  
> El control InkPicture no está marcado como seguro para scripting. El control InkPicture no debe usarse en html ni ASP.NET páginas.

 

La creación del control InkPicture detrás de un control transparente (por ejemplo, un Control GroupBox con el conjunto de propiedades TRANSPARENT de WS EX) impedirá que InkPicture recopile \_ \_ la entrada de lápiz.

## <a name="members"></a>Miembros



| Enumeración                                      | Descripción                                                                                              |
|--------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [**InkPictureSizeMode**](/windows/desktop/api/msinkaut/ne-msinkaut-inkpicturesizemode) | Define valores que especifican cómo se comporta la imagen de fondo dentro del control InkPicture.<br/> |



 



| Evento                                                                              | Descripción                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **ChangeUICues**                                                                   | En desuso.<br/>                                                                                                                                                                                                                                                                                             |
| [**Hacer clic**](inkpicture-click.md)                                                  | Se produce cuando un usuario hace clic en el control InkPicture.<br/>                                                                                                                                                                                                                                                       |
| [**Evento CursorButtonDown**](inkpicture-cursorbuttondown.md)                      | Se produce cuando el control [**InkCollector**](inkcollector-class.md) detecta un [**objeto IInkCursorButton**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursorbutton) que está abajo.<br/>                                                                                                                                                         |
| [**Evento CursorButtonUp**](inkpicture-cursorbuttonup.md)                          | Se produce cuando el control InkPicture detecta un [**IInkCursorButton**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursorbutton) que está en marcha.<br/>                                                                                                                                                                                                  |
| [**Evento CursorDown**](inkpicture-cursordown.md)                                  | Se produce cuando la punta del cursor se pone en contacto con la superficie digitalizadora de la tableta.<br/>                                                                                                                                                                                                                                      |
| [**Evento CursorInRange**](inkpicture-cursorinrange.md)                            | Se produce cuando un cursor entra en el intervalo de detección físico (proximidad) del contexto de la tableta.<br/>                                                                                                                                                                                                             |
| [**Evento CursorOutOfRange**](inkpicture-cursoroutofrange.md)                      | Se produce cuando el cursor sale del intervalo de detección físico (proximidad) del contexto de la tableta.<br/>                                                                                                                                                                                                           |
| [**Dblclick**](inkpicture-dblclick.md)                                            | Se produce cuando se hace doble clic en el control InkPicture.<br/> Este método de evento se define en la **\_ interfaz IInkPictureEvents.** La **\_ interfaz IInkPictureEvents** implementa la [**interfaz IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) con un identificador de DISPID \_ IPEDblClick.<br/> |
| [**Evento de gesto**](inkpicture-gesture.md)                                        | Se produce cuando se reconoce un gesto de aplicación.<br/>                                                                                                                                                                                                                                                       |
| [**Control \[ InkPicture del evento KeyDown\]**](inkpicture-keydown.md)                 | Se produce cuando se presiona una tecla y está en la posición de abajo mientras el control InkPicture tiene el foco.<br/>                                                                                                                                                                                                           |
| [**Control \[ InkPicture del evento KeyPress\]**](inkpicture-keypress.md)                | Se produce cuando se presiona una tecla mientras el control InkPicture tiene el foco.<br/>                                                                                                                                                                                                                                    |
| [**KeyUp Event \[ InkPicture Control\]**](inkpicture-keyup.md)                     | Se produce cuando se libera una clave mientras el control InkPicture tiene el foco.<br/>                                                                                                                                                                                                                                   |
| [**MouseDown Event \[ InkPicture Control\]**](inkpicture-mousedown.md)             | Se produce cuando el puntero del mouse está sobre el control InkPicture y se presiona un botón del mouse.<br/>                                                                                                                                                                                                             |
| [**MouseEnter**](inkpicture-mouseenter.md)                                        | Se produce cuando el puntero del mouse entra en el control InkPicture.<br/>                                                                                                                                                                                                                                            |
| [**MouseHover**](inkpicture-mousehover.md)                                        | Se produce cuando el puntero del mouse mantiene el puntero sobre el control InkPicture.<br/>                                                                                                                                                                                                                                       |
| [**MouseLeave**](inkpicture-mouseleave.md)                                        | Se produce cuando el puntero del mouse sale del control InkPicture.<br/>                                                                                                                                                                                                                                            |
| [**MouseMove Event \[ InkPicture Control\]**](inkpicture-mousemove.md)             | Se produce cuando el puntero del mouse se mueve sobre el control InkPicture.<br/>                                                                                                                                                                                                                                     |
| [**MouseUp Event \[ InkPicture Control\]**](inkpicture-mouseup.md)                 | Se produce cuando el puntero del mouse está sobre el control InkPicture y se libera un botón del mouse.<br/>                                                                                                                                                                                                            |
| [**Mousewheel**](inkpicture-mousewheel.md)                                        | Se produce cuando la rueda del mouse se mueve mientras el control InkPicture tiene el foco.<br/>                                                                                                                                                                                                                               |
| [**Evento NewInAirPackets**](inkpicture-newinairpackets.md)                        | Se produce cuando se ve un paquete en el aire.<br/>                                                                                                                                                                                                                                                                   |
| [**Evento NewPackets**](inkpicture-newpackets.md)                                  | Se produce cuando el control InkPicture recibe un paquete.<br/>                                                                                                                                                                                                                                                   |
| [**Pintado**](inkpicture-painted.md)                                              | Se produce cuando el control InkPicture ha terminado de volver a dibujarse.<br/>                                                                                                                                                                                                                                      |
| [**Pintura**](inkpicture-painting.md)                                            | Se produce antes de que el control InkPicture se vuelva a dibujar.<br/>                                                                                                                                                                                                                                                    |
| [**Cambiar de tamaño**](inkpicture-resize.md)                                                | Se produce cuando se cambia el tamaño del control InkPicture.<br/>                                                                                                                                                                                                                                                          |
| [**SelectionChanged**](inkpicture-selectionchanged.md)                            | Se produce cuando la selección de texto dentro del control InkPicture ha cambiado, por ejemplo, mediante modificaciones en la interfaz de usuario, procedimientos de cortar y pegar o la [**propiedad Selection.**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)<br/>                                                                                    |
| [**SelectionChanging**](inkpicture-selectionchanging.md)                          | Se produce cuando la selección de texto dentro del control InkPicture está a punto de cambiar, por ejemplo, mediante modificaciones en la interfaz de usuario, los procedimientos de cortar y pegar o la [**propiedad Selection.**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)<br/>                                                                             |
| [**SelectionMoved**](inkpicture-selectionmoved.md)                                | Se produce cuando la posición de la selección actual ha cambiado, por ejemplo, mediante modificaciones en la interfaz de usuario, los procedimientos de cortar y pegar o la [**propiedad Selection.**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)<br/>                                                                                                  |
| [**SelectionMoving Event \[ InkPicture Control\]**](inkpicture-selectionmoving.md) | Se produce cuando la posición de la selección actual está a punto de cambiar, por ejemplo, mediante modificaciones en la interfaz de usuario, procedimientos de cortar y pegar o la [**propiedad Selection.**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)<br/>                                                                                           |
| [**SelectionResized**](inkpicture-selectionresized.md)                            | Se produce cuando el tamaño de la selección actual ha cambiado, por ejemplo, mediante modificaciones en la interfaz de usuario, los procedimientos de cortar y pegar o la [**propiedad Selection.**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)<br/>                                                                                                      |
| [**SelectionResizing**](inkpicture-selectionresizing.md)                          | Se produce cuando el tamaño de la selección actual está a punto de cambiar, por ejemplo, mediante modificaciones en la interfaz de usuario, los procedimientos de cortar y pegar o la [**propiedad Selection.**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)<br/>                                                                                               |
| [**SizeChanged**](inkpicture-sizechanged.md)                                      | Se produce después de cambiar el tamaño del control InkPicture, en concreto, después de que cambie el valor de la propiedad [**Width**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_width) o [**Height.**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_height)<br/>                                                                                                      |
| [**SizeModeChanged**](inkpicture-sizemodechanged.md)                              | Se produce después de cambiar la propiedad [**SizeMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_sizemode) del control InkPicture.<br/>                                                                                                                                                                                           |
| **StyleChanged**                                                                   | Sin implementar.<br/>                                                                                                                                                                                                                                                                                        |
| [**Golpe**](inkpicture-stroke.md)                                                | Se produce cuando el usuario dibuja un nuevo trazo en cualquier tableta.<br/>                                                                                                                                                                                                                                                  |
| [**StrokesDeleted**](inkpicture-strokesdeleted.md)                                | Se produce después de [**eliminar objetos IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) de la [**propiedad Ink.**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_ink)<br/>                                                                                                                                                                        |
| [**StrokesDeleting**](inkpicture-strokesdeleting.md)                              | Se produce antes de [**que los objetos IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) se eliminen de la [**propiedad Ink.**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_ink)<br/>                                                                                                                                                                             |
| [**SystemColorsChanged**](inkpicture-systemcolorschanged.md)                      | Se produce después de cambiar los colores del sistema.<br/>                                                                                                                                                                                                                                                                  |
| [**SystemGesture**](inkpicture-systemgesture.md)                                  | Se produce cuando se reconoce un gesto del sistema.<br/>                                                                                                                                                                                                                                                             |
| [**Evento de tableta agregada**](inkpicture-tabletadded.md)                                | Se produce cuando se agrega una tableta al sistema.<br/>                                                                                                                                                                                                                                                            |
| [**Evento TabletRemoved**](inkpicture-tabletremoved.md)                            | Se produce cuando se quita una tableta del sistema.<br/>                                                                                                                                                                                                                                                        |



 



| Método                                                                                   | Descripción                                                                                                                                                                    |
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetEventInterest (método)**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-geteventinterest)                           | Devuelve un valor que indica si el control InkPicture tiene interés en un evento determinado.<br/>                                                                   |
| [**GetGestureStatus**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-getgesturestatus)                                  | Devuelve un valor que indica si el control InkPicture tiene interés en un gesto de aplicación determinado.<br/>                                                     |
| [**Método GetWindowInputRectangle**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-getwindowinputrectangle)             | Devuelve el rectángulo de ventana, en píxeles, dentro del cual se dibuja la entrada manuscrita.<br/>                                                                                                 |
| [**HitTestSelection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-hittestselection)                                  | Devuelve un miembro de la enumeración [**SelectionHitResult,**](/windows/desktop/api/msinkaut/ne-msinkaut-selectionhitresult) que especifica qué parte de una selección, si la hay, se ha alcanzado durante una prueba de posicionamiento.<br/> |
| [**SetAllTabletsMode (método)**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-setalltabletsmode)                         | Permite que el control InkPicture recopile la entrada de lápiz de cualquier tableta conectada al tablet PC.<br/>                                                                            |
| [**Método SetEventInterest**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-seteventinterest)                           | Establece un valor que indica si un control InkPicture tiene interés en un evento especificado.<br/>                                                                        |
| SetFocus                                                                                 | Mueve el foco al control InkPicture.<br/>                                                                                                                          |
| [**SetGestureStatus (método)**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-setgesturestatus)                           | Establece el interés del objeto InkPicture en un gesto de aplicación especificado.<br/>                                                                                      |
| [**SetSingleTabletIntegratedMode (método)**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-setsingletabletintegratedmode) | Establece el control InkPicture para recopilar la entrada de lápiz de una sola tableta conectada al tablet PC. Se omite la entrada de lápiz de otras tabletas.<br/>                                       |
| [**SetWindowInputRectangle (método)**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-setwindowinputrectangle)             | Especifica el rectángulo de ventana que se va a establecer, en coordenadas de ventana, dentro del cual se dibuja la entrada manuscrita.<br/>                                                                            |
| ShowWhatsThis                                                                            | Muestra un tema seleccionado en un archivo de Ayuda mediante el menú emergente "What's This" (¿Qué es esto?) proporcionado por la Ayuda en sistemas operativos de Microsoft Windows de 32 bits (solo en tiempo de diseño).<br/>           |
| ZOrder                                                                                   | Coloca el control en la parte delantera o posterior del orden Z dentro de su nivel gráfico (solo en tiempo de diseño).<br/>                                                               |



 




| Propiedad | Descripción | 
|----------|-------------|
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_autoredraw"><strong>Propiedad AutoRedraw</strong></a> | Obtiene o establece un valor que especifica si el control InkPicture se vuelve a dibujar cuando se invalida la ventana (si el objeto <a href="inkdisp-class.md"><strong>InkDisp</strong></a> asociado actualmente al control InkPicture se vuelve a dibujar automáticamente cuando la ventana asociada a InkPicture recibe un mensaje WM_PAINT).<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_backcolor"><strong>Backcolor</strong></a> | Obtiene o establece el color de fondo del control InkPicture. El color de fondo predeterminado es el color de fondo de la ventana del sistema, que suele ser blanco.<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_collectingink"><strong>CollectingInk (propiedad)</strong></a> | Obtiene el valor que especifica si el control InkPicture recopila entrada de lápiz (solo en tiempo de ejecución).<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_collectionmode"><strong>CollectionMode</strong></a> | Obtiene o establece el modo de colección que determina si la entrada de lápiz, los gestos o la entrada de lápiz y los gestos se reconocen a medida que el usuario escribe.<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_cursors"><strong>Cursors (propiedad)</strong></a> | Obtiene la <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursors"><strong>colección IInkCursors</strong></a> disponible para su uso en la región de entrada manuscrita del control InkPicture.<br /> | 
| <a href="/previous-versions/windows/desktop/legacy/ms703274(v=vs.85)"><strong>CustomStrokes</strong></a> | Obtiene la <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkcustomstrokes"><strong>colección IInkCustomStrokes</strong></a> que se va a conservar con la entrada de lápiz (solo en tiempo de diseño).<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_defaultdrawingattributes"><strong>Propiedad DefaultDrawingAttributes</strong></a> | Obtiene o establece la colección <a href="inkdrawingattributes-class.md"><strong>InkDrawingAttributes</strong></a> predeterminada que se va a usar al dibujar y mostrar la entrada de lápiz (solo en tiempo de ejecución).<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_desiredpacketdescription"><strong>Propiedad DesiredPacketDescription</strong></a> | Obtiene o establece la descripción del paquete del control InkPicture (solo en tiempo de ejecución).<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_dynamicrendering"><strong>Propiedad DynamicRendering</strong></a> | Obtiene o establece el valor que especifica si el control InkPicture representa dinámicamente la entrada de lápiz a medida que se recopila.<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_editingmode"><strong>EditingMode</strong></a> | Obtiene o establece un valor que especifica si el control InkPicture está en modo de entrada de lápiz, en modo de eliminación o en modo de selección o edición.<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_enabled"><strong>Habilitado</strong></a> | Obtiene o establece un valor que determina si el control InkPicture puede responder a eventos generados por el usuario.<br /><blockquote>[!Note]<br />Esta propiedad es equivalente a la <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_inkenabled"><strong>propiedad InkEnabled.</strong></a></blockquote><br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_erasermode"><strong>EraserMode</strong></a> | Obtiene o establece el valor que especifica si la entrada manuscrita se borra por trazo o por punto.<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_eraserwidth"><strong>EraserWidth</strong></a> | Obtiene o establece el valor que especifica el ancho de la punta del lápiz de borrador.<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_hwnd"><strong>Hwnd</strong></a> | Obtiene el identificador de ventana al que está enlazado el control InkPicture. (solo en tiempo de ejecución)<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_ink"><strong>Entrada de lápiz</strong></a> | Obtiene o establece el <a href="inkdisp-class.md"><strong>objeto InkDisp</strong></a> asociado al control InkPicture (solo en tiempo de ejecución).<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_inkenabled"><strong>InkEnabled</strong></a> | Obtiene o establece un valor que especifica si el control InkPicture recopila entradas de lápiz (paquetes en el aire, cursor en eventos de intervalo, y así sucesivamente).<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_marginx"><strong>Propiedad MarginX</strong></a> | Obtiene o establece el margen del eje X alrededor del rectángulo de la ventana en coordenadas de pantalla.<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_marginy"><strong>Propiedad MarginY</strong></a> | Obtiene o establece el margen del eje Y alrededor del rectángulo de la ventana en coordenadas de pantalla.<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_mouseicon"><strong>Propiedad MouseIcon</strong></a> | Obtiene o establece el icono del mouse personalizado actual.<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_mousepointer"><strong>Propiedad MousePointer</strong></a> | Obtiene o establece un valor que indica el tipo de puntero del mouse que aparece cuando el mouse está sobre una parte determinada del control InkPicture.<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_picture"><strong>Imagen</strong></a> | Obtiene el archivo de gráficos que aparece en el control InkPicture.<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_renderer"><strong>Renderer (propiedad)</strong></a> | Obtiene o establece el <a href="inkrenderer-class.md"><strong>objeto InkRenderer</strong></a> que se usa para dibujar entrada manuscrita en el control InkPicture (solo en tiempo de ejecución).<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection"><strong>Número de selección</strong></a> | Obtiene la <a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">colección InkStrokes</a> seleccionada actualmente dentro del control InkPicture (solo en tiempo de ejecución).<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_sizemode"><strong>SizeMode</strong></a> | Obtiene o establece cómo el control controla la ubicación y el tamaño de la imagen.<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_supporthighcontrastink"><strong>Propiedad SupportHighContrastInk</strong></a> | Obtiene un valor que especifica si la entrada de lápiz se representa como un solo color, Color = COLOR_WINDOWTEXT (de la llamada a GetSystemMetrics) cuando el sistema está en modo contraste alto automático.<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_supporthighcontrastselectionui"><strong>SupportHighContrastSelectionUI</strong></a> | Obtiene o establece un valor que especifica si todas las interfaces de usuario de selección (rectángulo de selección y identificadores de selección) se dibujan en contraste alto cuando el sistema está en modo contraste alto selección.<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_tablet"><strong>Propiedad de tableta</strong></a> | Obtiene el <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet"><strong>objeto IInkTablet</strong></a> que el control InkPicture usa actualmente para recopilar la entrada.<br /> | 




 

## <a name="remarks"></a>Comentarios

La interfaz de usuario en tiempo de ejecución del control InkPicture es una ventana con un fondo opaco (color único, fondo de imagen o ambos) que contiene entrada manuscrita.

Puede usar el control InkPicture para representar la entrada de lápiz en Microsoft Windows 2000, Windows Server 2003, cualquier edición de Windows XP que no sea Windows XP Tablet PC Edition y cualquier versión de Windows Vista. Sin embargo, puede escribir entrada de lápiz, aceptar gestos o reconocer la escritura a mano solo en las condiciones siguientes:

-   La entrada de lápiz se puede especificar y reconocer Windows vista o XP Tablet PC Edition 2005.
-   Los gestos también se pueden reconocer.
-   La escritura a mano se puede reconocer como texto si la escritura a mano se originó en máquinas que ejecutan versiones anteriores de Windows siempre que los reconocedores estén presentes.

Si usa Windows 2000, Windows Server 2003, cualquier edición de Windows XP que no sea Windows XP Tablet PC Edition 2005, puede asignar valores a las propiedades ambientales del control InkPicture y, a continuación, copiar y pegar la entrada de lápiz en otras aplicaciones. Sin embargo, el valor de su propiedad InkEnabled siempre será **FALSE.**

Los objetos [**InkDisp**](inkdisp-class.md) persistentes se pueden cargar y mostrar en todas las ediciones de Windows Vista y XP y en sistemas que solo tienen instalado el Kit de desarrollo de software (SDK) de Windows XP Tablet PC Edition. Los objetos **InkDisp** solo se pueden convertir en texto (reconocido), si se instala Windows Vista o Windows XP Tablet PC Edition 2005.

Si las operaciones de este control no se realiza correctamente, se devuelve un HRESULT legal. Si se produce una condición de error, compruebe el HRESULT devuelto con el error.

Para obtener más información sobre los controles de entrada de lápiz, vea [Ink](ink-controls.md).

Para obtener información sobre qué subprocesos provoca eventos concretos, vea [Subprocesos](threads-on-which-an-event-can-fire.md)en los que un evento puede generar .

Para mejorar el rendimiento de la aplicación, elimine manualmente un control InkPicture cuando ya no sea necesario.

> [!Note]  
> Cuando un control InkPicture se superpone con otro control, como **groupBox** establecido en transparente, InkPicture no recopilará lápiz. InkPicture debe ser el control de nivel superior en el orden Z o debe ser un elemento secundario de **GroupBox.**

 

## <a name="com-implementation"></a>Implementación com

Este objeto implementa la **interfaz COM IInkPicture.**

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia del control InkEdit](inkedit-control-reference.md)
</dt> <dt>

[**InkOverlay (clase)**](inkoverlay-class.md)
</dt> </dl>

