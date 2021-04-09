---
description: El control InkPicture proporciona la capacidad de colocar una imagen en una aplicación y permitir que los usuarios agreguen tinta encima de ella.
ms.assetid: e9fa6807-6e2a-44ec-9b8f-a560185e4367
title: Referencia del control InkPicture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8caaf1970394338f858cd0fdff0dab58153f53b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104003073"
---
# <a name="inkpicture-control-reference"></a>Referencia del control InkPicture

El control InkPicture proporciona la capacidad de colocar una imagen en una aplicación y permitir que los usuarios agreguen tinta encima de ella. Está diseñado para escenarios en los que la tinta no se reconoce como texto, sino que se almacena como entrada de lápiz.

Se puede crear una instancia del control InkPicture llamando al método [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) en C++.

> [!Note]  
> El control InkPicture no está marcado como seguro para el scripting. El control InkPicture no debe usarse en páginas HTML o ASP.NET.

 

La creación del control InkPicture detrás de un control transparente (como GroupBox con el \_ conjunto de \_ propiedades transparentes WS ex) impedirá que el InkPicture recopile la tinta.

## <a name="members"></a>Miembros



| Enumeración                                      | Descripción                                                                                              |
|--------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [**InkPictureSizeMode**](/windows/desktop/api/msinkaut/ne-msinkaut-inkpicturesizemode) | Define valores que especifican el comportamiento de la imagen de fondo dentro del control InkPicture.<br/> |



 



| Evento                                                                              | Descripción                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **ChangeUICues**                                                                   | En desuso.<br/>                                                                                                                                                                                                                                                                                             |
| [**Hizo**](inkpicture-click.md)                                                  | Se produce cuando un usuario hace clic en el control InkPicture.<br/>                                                                                                                                                                                                                                                       |
| [**Evento CursorButtonDown**](inkpicture-cursorbuttondown.md)                      | Se produce cuando el control [**InkCollector**](inkcollector-class.md) detecta un objeto [**IInkCursorButton**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursorbutton) que está inactivo.<br/>                                                                                                                                                         |
| [**Evento CursorButtonUp**](inkpicture-cursorbuttonup.md)                          | Se produce cuando el control InkPicture detecta un [**IInkCursorButton**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursorbutton) que está activo.<br/>                                                                                                                                                                                                  |
| [**Evento CursorDown**](inkpicture-cursordown.md)                                  | Se produce cuando la sugerencia del cursor se pone en contacto con la superficie de la tableta de la digitalización.<br/>                                                                                                                                                                                                                                      |
| [**Evento CursorInRange**](inkpicture-cursorinrange.md)                            | Se produce cuando un cursor entra en el intervalo de detección física (proximidad) del contexto de la tableta.<br/>                                                                                                                                                                                                             |
| [**Evento CursorOutOfRange**](inkpicture-cursoroutofrange.md)                      | Se produce cuando el cursor deja el intervalo de detección física (proximidad) del contexto de la tableta.<br/>                                                                                                                                                                                                           |
| [**DblClick**](inkpicture-dblclick.md)                                            | Se produce cuando se hace doble clic en el control InkPicture.<br/> Este método de evento se define en la interfaz **\_ IInkPictureEvents** . La interfaz **\_ IInkPictureEvents** implementa la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) con un identificador de DISPID \_ IPEDblClick.<br/> |
| [**Evento de gesto**](inkpicture-gesture.md)                                        | Se produce cuando se reconoce un gesto de aplicación.<br/>                                                                                                                                                                                                                                                       |
| [**Evento KeyDown ( \[ control InkPicture)\]**](inkpicture-keydown.md)                 | Se produce cuando se presiona una tecla y en la posición hacia abajo mientras el control InkPicture tiene el foco.<br/>                                                                                                                                                                                                           |
| [**Control InkPicture del evento KeyPress \[\]**](inkpicture-keypress.md)                | Se produce cuando se presiona una tecla mientras el control InkPicture tiene el foco.<br/>                                                                                                                                                                                                                                    |
| [**KeyUp Event \[ InkPicture (control)\]**](inkpicture-keyup.md)                     | Se produce cuando se suelta una tecla mientras el control InkPicture tiene el foco.<br/>                                                                                                                                                                                                                                   |
| [**MouseDown ( \[ control de evento InkPicture)\]**](inkpicture-mousedown.md)             | Se produce cuando el puntero del mouse se encuentra sobre el control InkPicture y se presiona un botón del mouse.<br/>                                                                                                                                                                                                             |
| [**MouseEnter**](inkpicture-mouseenter.md)                                        | Se produce cuando el puntero del Mouse entra en el control InkPicture.<br/>                                                                                                                                                                                                                                            |
| [**MouseHover**](inkpicture-mousehover.md)                                        | Se produce cuando el puntero del mouse se desplaza sobre el control InkPicture.<br/>                                                                                                                                                                                                                                       |
| [**MouseLeave**](inkpicture-mouseleave.md)                                        | Se produce cuando el puntero del mouse sale del control InkPicture.<br/>                                                                                                                                                                                                                                            |
| [**Control InkPicture del evento MouseMove \[\]**](inkpicture-mousemove.md)             | Se produce cuando el puntero del mouse se mueve sobre el control InkPicture.<br/>                                                                                                                                                                                                                                     |
| [**MouseUp Event \[ InkPicture (control)\]**](inkpicture-mouseup.md)                 | Se produce cuando el puntero del mouse se encuentra sobre el control InkPicture y se suelta un botón del mouse.<br/>                                                                                                                                                                                                            |
| [**Rueda**](inkpicture-mousewheel.md)                                        | Se produce cuando se mueve la rueda del mouse mientras el control InkPicture tiene el foco.<br/>                                                                                                                                                                                                                               |
| [**Evento NewInAirPackets**](inkpicture-newinairpackets.md)                        | Se produce cuando se detecta un paquete en el aire.<br/>                                                                                                                                                                                                                                                                   |
| [**Evento NewPackets**](inkpicture-newpackets.md)                                  | Se produce cuando el control InkPicture recibe un paquete.<br/>                                                                                                                                                                                                                                                   |
| [**Representan**](inkpicture-painted.md)                                              | Se produce cuando el control InkPicture ha terminado de volver a dibujarse.<br/>                                                                                                                                                                                                                                      |
| [**Vuelva**](inkpicture-painting.md)                                            | Se produce antes de que el control InkPicture se vuelva a dibujar.<br/>                                                                                                                                                                                                                                                    |
| [**Cambiar de tamaño**](inkpicture-resize.md)                                                | Se produce cuando se cambia el tamaño del control InkPicture.<br/>                                                                                                                                                                                                                                                          |
| [**SelectionChanged**](inkpicture-selectionchanged.md)                            | Se produce cuando la selección de texto dentro del control InkPicture ha cambiado, por ejemplo, a través de modificaciones en la interfaz de usuario, procedimientos de cortar y pegar o la propiedad de [**selección**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) .<br/>                                                                                    |
| [**SelectionChanging**](inkpicture-selectionchanging.md)                          | Se produce cuando la selección de texto dentro del control InkPicture está a punto de cambiar, por ejemplo, a través de las modificaciones en la interfaz de usuario, los procedimientos de cortar y pegar o la propiedad de [**selección**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) .<br/>                                                                             |
| [**SelectionMoved**](inkpicture-selectionmoved.md)                                | Se produce cuando ha cambiado la posición de la selección actual, por ejemplo, a través de las modificaciones en la interfaz de usuario, los procedimientos de cortar y pegar o la propiedad de [**selección**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) .<br/>                                                                                                  |
| [**SelectionMoving \[ control InkPicture de evento\]**](inkpicture-selectionmoving.md) | Se produce cuando la posición de la selección actual está a punto de cambiar, por ejemplo, a través de modificaciones en la interfaz de usuario, procedimientos de cortar y pegar o la propiedad de [**selección**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) .<br/>                                                                                           |
| [**SelectionResized**](inkpicture-selectionresized.md)                            | Se produce cuando el tamaño de la selección actual ha cambiado, por ejemplo, a través de modificaciones en la interfaz de usuario, procedimientos de cortar y pegar o la propiedad de [**selección**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) .<br/>                                                                                                      |
| [**SelectionResizing**](inkpicture-selectionresizing.md)                          | Se produce cuando el tamaño de la selección actual está a punto de cambiar, por ejemplo, a través de modificaciones en la interfaz de usuario, procedimientos de cortar y pegar o la propiedad de [**selección**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) .<br/>                                                                                               |
| [**SizeChanged**](inkpicture-sizechanged.md)                                      | Se produce después de cambiar el tamaño del control InkPicture, en concreto, después de que cambie el valor de la propiedad [**width**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_width) o [**height**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_height) .<br/>                                                                                                      |
| [**SizeModeChanged**](inkpicture-sizemodechanged.md)                              | Se produce después de cambiarse la propiedad [**SizeMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_sizemode) del control InkPicture.<br/>                                                                                                                                                                                           |
| **StyleChanged**                                                                   | Sin implementar.<br/>                                                                                                                                                                                                                                                                                        |
| [**Stroke**](inkpicture-stroke.md)                                                | Se produce cuando el usuario dibuja un nuevo trazo en cualquier tableta.<br/>                                                                                                                                                                                                                                                  |
| [**StrokesDeleted**](inkpicture-strokesdeleted.md)                                | Se produce después de eliminar los objetos [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) de la propiedad [**Ink**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_ink) .<br/>                                                                                                                                                                        |
| [**StrokesDeleting**](inkpicture-strokesdeleting.md)                              | Se produce antes de que se eliminen los objetos [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) de la propiedad [**Ink**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_ink) .<br/>                                                                                                                                                                             |
| [**SystemColorsChanged**](inkpicture-systemcolorschanged.md)                      | Se produce después de que cambien los colores del sistema.<br/>                                                                                                                                                                                                                                                                  |
| [**SystemGesture**](inkpicture-systemgesture.md)                                  | Se produce cuando se reconoce un gesto del sistema.<br/>                                                                                                                                                                                                                                                             |
| [**Evento TabletAdded**](inkpicture-tabletadded.md)                                | Se produce cuando se agrega una tableta al sistema.<br/>                                                                                                                                                                                                                                                            |
| [**Evento TabletRemoved**](inkpicture-tabletremoved.md)                            | Se produce cuando se quita una tableta del sistema.<br/>                                                                                                                                                                                                                                                        |



 



| Método                                                                                   | Descripción                                                                                                                                                                    |
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Método GetEventInterest**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-geteventinterest)                           | Devuelve un valor que indica si el control InkPicture tiene interés en un evento determinado.<br/>                                                                   |
| [**GetGestureStatus**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-getgesturestatus)                                  | Devuelve un valor que indica si el control InkPicture tiene interés en un gesto de aplicación determinado.<br/>                                                     |
| [**Método GetWindowInputRectangle**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-getwindowinputrectangle)             | Devuelve el rectángulo de ventana, en píxeles, en el que se dibuja la entrada de lápiz.<br/>                                                                                                 |
| [**HitTestSelection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-hittestselection)                                  | Devuelve un miembro de la enumeración [**SelectionHitResult**](/windows/desktop/api/msinkaut/ne-msinkaut-selectionhitresult) , que especifica qué parte de una selección, si la hay, se alcanzó durante una prueba de posicionamiento.<br/> |
| [**Método SetAllTabletsMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-setalltabletsmode)                         | Permite que el control InkPicture recopile entradas de lápiz de cualquier tableta conectada al Tablet PC.<br/>                                                                            |
| [**Método SetEventInterest**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-seteventinterest)                           | Establece un valor que indica si un control InkPicture tiene interés en un evento especificado.<br/>                                                                        |
| SetFocus                                                                                 | Mueve el foco al control InkPicture.<br/>                                                                                                                          |
| [**Método SetGestureStatus**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-setgesturestatus)                           | Establece el interés del objeto InkPicture en un gesto de aplicación especificado.<br/>                                                                                      |
| [**Método SetSingleTabletIntegratedMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-setsingletabletintegratedmode) | Establece el control InkPicture para recopilar la tinta de una sola tableta conectada al Tablet PC. Se omite la tinta de otras tabletas.<br/>                                       |
| [**Método SetWindowInputRectangle**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-setwindowinputrectangle)             | Especifica el rectángulo de ventana que se va a establecer, en coordenadas de la ventana, en la que se dibuja la tinta.<br/>                                                                            |
| ShowWhatsThis                                                                            | Muestra un tema seleccionado en un archivo de ayuda mediante el cuadro emergente "Qué es esto" proporcionado por la ayuda de los sistemas operativos Microsoft Windows de 32 bits (solo en tiempo de diseño).<br/>           |
| Z                                                                                   | Coloca el control al principio o al final del orden z dentro de su nivel gráfico (solo en tiempo de diseño).<br/>                                                               |



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Propiedad</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_autoredraw"><strong>AutoRedraw (propiedad)</strong></a></td>
<td>Obtiene o establece un valor que especifica si el control InkPicture se vuelve a dibujar cuando se invalida la ventana (si el objeto <a href="inkdisp-class.md"><strong>InkDisp</strong></a> asociado actualmente al control InkPicture se vuelve a dibujar automáticamente cuando la ventana asociada a InkPicture recibe un mensaje WM_PAINT).<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_backcolor"><strong>BackColor</strong></a></td>
<td>Obtiene o establece el color de fondo del control InkPicture. El color de fondo predeterminado es el color de fondo de la ventana del sistema, que suele ser blanco.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_collectingink"><strong>Propiedad CollectingInk</strong></a></td>
<td>Obtiene el valor que especifica si el control InkPicture está recopilando la entrada de lápiz (solo en tiempo de ejecución).<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_collectionmode"><strong>Si CollectionMode es</strong></a></td>
<td>Obtiene o establece el modo de recopilación que determina si se reconocen la tinta, los gestos o la entrada de lápiz y los gestos a medida que el usuario escribe.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_cursors"><strong>Cursor (propiedad)</strong></a></td>
<td>Obtiene la colección <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursors"><strong>IInkCursors</strong></a> disponible para su uso en la región de entrada manuscrita del control InkPicture.<br/></td>
</tr>
<tr class="even">
<td><a href="/previous-versions/windows/desktop/legacy/ms703274(v=vs.85)"><strong>CustomStrokes</strong></a></td>
<td>Obtiene la colección <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkcustomstrokes"><strong>IInkCustomStrokes</strong></a> que se va a conservar con la entrada de lápiz (solo en tiempo de diseño).<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_defaultdrawingattributes"><strong>Propiedad DefaultDrawingAttributes</strong></a></td>
<td>Obtiene o establece la colección <a href="inkdrawingattributes-class.md"><strong>InkDrawingAttributes</strong></a> predeterminada que se va a usar al dibujar y mostrar la entrada de lápiz (solo en tiempo de ejecución).<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_desiredpacketdescription"><strong>Propiedad DesiredPacketDescription</strong></a></td>
<td>Obtiene o establece la descripción del paquete del control InkPicture (solo en tiempo de ejecución).<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_dynamicrendering"><strong>Propiedad DynamicRendering</strong></a></td>
<td>Obtiene o establece el valor que especifica si el control InkPicture representa dinámicamente la entrada de lápiz a medida que se recopila.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_editingmode"><strong>EditingMode</strong></a></td>
<td>Obtiene o establece un valor que especifica si el control InkPicture está en modo de entrada de lápiz, modo de eliminación o modo de edición o selección.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_enabled"><strong>habilitado</strong></a></td>
<td>Obtiene o establece un valor que determina si el control InkPicture puede responder a los eventos generados por el usuario.<br/>
<blockquote>
[!Note]<br />
Esta propiedad es equivalente a la propiedad <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_inkenabled"><strong>InkEnabled</strong></a> .
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_erasermode"><strong>EraserMode</strong></a></td>
<td>Obtiene o establece el valor que especifica si la entrada de lápiz se borra por trazo o por punto.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_eraserwidth"><strong>EraserWidth</strong></a></td>
<td>Obtiene o establece el valor que especifica el ancho de la punta del lápiz de borrador.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_hwnd"><strong>Identificador</strong></a></td>
<td>Obtiene el identificador de ventana al que está enlazado el control InkPicture. (solo en tiempo de ejecución)<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_ink"><strong>Entrada de lápiz</strong></a></td>
<td>Obtiene o establece el objeto <a href="inkdisp-class.md"><strong>InkDisp</strong></a> que está asociado al control InkPicture (solo en tiempo de ejecución).<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_inkenabled"><strong>InkEnabled</strong></a></td>
<td>Obtiene o establece un valor que especifica si el control InkPicture recopila entradas manuscritas (paquetes en el aire, cursor en eventos de intervalo, etc.).<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_marginx"><strong>Propiedad MarginX</strong></a></td>
<td>Obtiene o establece el margen del eje x alrededor del rectángulo de la ventana en coordenadas de la pantalla.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_marginy"><strong>Propiedad marginy</strong></a></td>
<td>Obtiene o establece el margen del eje y alrededor del rectángulo de la ventana en coordenadas de la pantalla.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_mouseicon"><strong>Propiedad MouseIcon</strong></a></td>
<td>Obtiene o establece el icono actual del mouse.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_mousepointer"><strong>MousePointer (propiedad)</strong></a></td>
<td>Obtiene o establece un valor que indica el tipo de puntero del mouse que aparece cuando el mouse está encima de una parte determinada del control InkPicture.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_picture"><strong>Imagen</strong></a></td>
<td>Obtiene el archivo de gráficos que se va a mostrar en el control InkPicture.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_renderer"><strong>Renderer (propiedad)</strong></a></td>
<td>Obtiene o establece el objeto <a href="inkrenderer-class.md"><strong>InkRenderer</strong></a> que se usa para dibujar la entrada de lápiz en el control InkPicture (solo en tiempo de ejecución).<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection"><strong>Selección</strong></a></td>
<td>Obtiene la colección <a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes</a> actualmente seleccionada dentro del control InkPicture (solo en tiempo de ejecución).<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_sizemode"><strong>SizeMode</strong></a></td>
<td>Obtiene o establece cómo controla el control la posición y el tamaño de la imagen.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_supporthighcontrastink"><strong>Propiedad SupportHighContrastInk</strong></a></td>
<td>Obtiene un valor que especifica si la entrada de lápiz se representa como un solo color, color = COLOR_WINDOWTEXT (de la llamada a GetSystemMetrics) cuando el sistema está en modo de contraste alto.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_supporthighcontrastselectionui"><strong>SupportHighContrastSelectionUI</strong></a></td>
<td>Obtiene o establece un valor que especifica si todas las interfaces de usuario de selección (el cuadro de límite de selección y los controladores de selección) se dibujan en contraste alto cuando el sistema está en modo de contraste alto.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_tablet"><strong>Propiedad de Tablet PC</strong></a></td>
<td>Obtiene el objeto <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet"><strong>IInkTablet</strong></a> que el control InkPicture está usando actualmente para recopilar la entrada.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Observaciones

La interfaz de usuario en tiempo de ejecución para el control InkPicture es una ventana con un fondo opaco (color único, Fondo de imagen o ambos) que contiene tinta opaca.

Puede usar el control InkPicture para representar la entrada manuscrita en Microsoft Windows 2000, Windows Server 2003, cualquier edición de Windows XP que no sea Windows XP Tablet PC Edition y cualquier versión de Windows Vista. Sin embargo, puede escribir entradas manuscritas, aceptar gestos o reconocer escritura a mano solo en las siguientes condiciones:

-   La entrada manuscrita se puede proporcionar e reconocer si está instalado Windows Vista o XP Tablet PC Edition 2005.
-   También se pueden reconocer los gestos.
-   La escritura a mano se puede reconocer como texto si la escritura a mano se origina en máquinas que ejecutan versiones anteriores de Windows, siempre y cuando estén presentes los reconocedores.

Si usa Windows 2000, Windows Server 2003, cualquier edición de Windows XP que no sea Windows XP Tablet PC Edition 2005, puede asignar valores a las propiedades de ambiente del control InkPicture y, después, copiar y pegar la entrada de lápiz en otras aplicaciones. Sin embargo, el valor de su propiedad InkEnabled siempre será **false**.

Los objetos [**InkDisp**](inkdisp-class.md) persistentes se pueden cargar y mostrar en todas las ediciones de Windows Vista y XP, y en sistemas que solo tienen instalado el kit de desarrollo de software (SDK) de Windows XP Tablet PC Edition. Los objetos **InkDisp** solo se pueden convertir en texto (reconocido) si Windows Vista o Windows XP Tablet PC Edition 2005 está instalado.

Si las operaciones en este control no se realizan correctamente, se devuelve un valor HRESULT legal. Si se producen condiciones de error, compruebe el valor HRESULT devuelto con el error.

Para obtener más información acerca de los controles de entrada manuscrita, vea [Ink](ink-controls.md).

Para obtener información sobre los subprocesos que producen eventos concretos, vea [subprocesos en los que se puede activar un evento](threads-on-which-an-event-can-fire.md).

Para mejorar el rendimiento de la aplicación, elimine manualmente un control InkPicture cuando ya no sea necesario.

> [!Note]  
> Cuando un control InkPicture se superpone con otro control, como un **GroupBox** establecido en transparente, el InkPicture no recopilará entradas de lápiz. El InkPicture debe ser el control de nivel superior en el orden Z o debe ser un elemento secundario del **GroupBox**.

 

## <a name="com-implementation"></a>Implementación COM

Este objeto implementa la interfaz com **IInkPicture** .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de control InkEdit](inkedit-control-reference.md)
</dt> <dt>

[**InkOverlay (clase)**](inkoverlay-class.md)
</dt> </dl>

