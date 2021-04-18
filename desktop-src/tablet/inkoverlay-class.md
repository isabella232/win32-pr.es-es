---
description: Representa un objeto que es útil para escenarios de anotación en los que los usuarios no están interesados en realizar el reconocimiento de la entrada de lápiz, sino que están interesados en el tamaño, la forma, el color y la posición de la tinta.
ms.assetid: 61191ab3-075e-458b-9e0f-4bc255687b3c
title: Clase InkOverlay (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkOverlay
- InkOverlay.IInkOverlay
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: bfcc6cc4daedf0ed1bbc43e2ccc78317f9d7e17c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706576"
---
# <a name="inkoverlay-class"></a>InkOverlay (clase)

Representa un objeto que es útil para escenarios de anotación en los que los usuarios no están interesados en realizar el reconocimiento de la entrada de lápiz, sino que están interesados en el tamaño, la forma, el color y la posición de la tinta.

La creación del control **InkOverlay** detrás de un control transparente (como GroupBox con el \_ conjunto de \_ propiedades transparentes WS ex) impedirá que **InkOverlay** recopile la tinta.

**InkOverlay** tiene estos tipos de miembros:

-   [Eventos](#events)
-   [Interfaces](#interfaces)
-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="events"></a>Events

La clase **InkOverlay** tiene estos eventos.



| Evento                                                     | Descripción                                                                                                                                                                                                                                               |
|:----------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CursorButtonDown**](inkcollector-cursorbuttondown.md) | Se produce cuando **InkOverlay** detecta un botón de cursor que está inactivo.<br/>                                                                                                                                                                           |
| [**CursorButtonUp**](inkcollector-cursorbuttonup.md)     | Se produce cuando **InkOverlay** detecta un botón de cursor que está activo.<br/>                                                                                                                                                                             |
| [**CursorDown**](inkcollector-cursordown.md)             | Se produce cuando la sugerencia del cursor se pone en contacto con la superficie de la tableta de la digitalización.<br/>                                                                                                                                                                             |
| [**CursorInRange**](inkcollector-cursorinrange.md)       | Se produce cuando un cursor entra en el intervalo de detección física (proximidad) del contexto de la tableta.<br/>                                                                                                                                                    |
| [**CursorOutOfRange**](inkcollector-cursoroutofrange.md) | Se produce cuando el cursor deja el intervalo de detección física (proximidad) del contexto de la tableta.<br/>                                                                                                                                                  |
| [**DoubleClick**](inkcollector-doubleclick.md)           | Se produce cuando se hace doble clic en el objeto **InkOverlay** .<br/>                                                                                                                                                                                       |
| [**Gesto**](inkcollector-gesture.md)                   | Se produce cuando se reconoce un gesto específico de la aplicación.<br/>                                                                                                                                                                                     |
| [**Eventos**](inkcollector-mousedown.md)               | Se produce cuando el puntero del mouse se encuentra sobre el objeto **InkOverlay** y se presiona un botón del mouse.<br/>                                                                                                                                                 |
| [**MouseMove**](inkcollector-mousemove.md)               | Se produce cuando el puntero del mouse se mueve sobre el objeto **InkOverlay** .<br/>                                                                                                                                                                         |
| [**MouseUp**](inkcollector-mouseup.md)                   | Se produce cuando el puntero del mouse se encuentra sobre el objeto **InkOverlay** y se suelta un botón del mouse.<br/>                                                                                                                                                |
| [**Rueda**](inkcollector-mousewheel.md)             | Se produce cuando la rueda del mouse se mueve mientras el objeto **InkOverlay** tiene el foco.<br/>                                                                                                                                                                   |
| [**NewInAirPackets**](inkcollector-newinairpackets.md)   | Se produce cuando se detecta un paquete en el aire, lo que ocurre cuando un usuario mueve un lápiz cerca de la tableta y el cursor se encuentra dentro de la ventana del objeto **InkOverlay** o el usuario mueve un mouse dentro de la ventana asociada del objeto de objeto **InkOverlay** .<br/> |
| [**NewPackets**](inkcollector-newpackets.md)             | Se produce cuando el objeto **InkOverlay** recibe paquetes.<br/>                                                                                                                                                                                        |
| [**Representan**](inkoverlay-painted.md)                     | Se produce cuando el objeto **InkOverlay** ha terminado de volver a dibujarse.<br/>                                                                                                                                                                          |
| [**Vuelva**](inkoverlay-painting.md)                   | Se produce antes de que el objeto **InkOverlay** se vuelva a dibujar.<br/>                                                                                                                                                                                        |
| [**SelectionChanged**](inkoverlay-selectionchanged.md)   | Se produce cuando la selección de tinta dentro del control ha cambiado, por ejemplo, a través de modificaciones en la interfaz de usuario, procedimientos de cortar y pegar o la propiedad de [**selección**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) .<br/>                                       |
| [**SelectionChanging**](inkoverlay-selectionchanging.md) | Se produce cuando la selección de entrada de lápiz dentro del control está a punto de cambiar, por ejemplo, a través de modificaciones en la interfaz de usuario, procedimientos de cortar y pegar o la propiedad de [**selección**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) .<br/>                                |
| [**SelectionMoved**](inkoverlay-selectionmoved.md)       | Se produce cuando ha cambiado la posición de la selección actual, por ejemplo, a través de las modificaciones en la interfaz de usuario, los procedimientos de cortar y pegar o la propiedad de [**selección**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) .<br/>                                         |
| [**SelectionMoving**](inkoverlay-selectionmoving.md)     | Se produce cuando la posición de la selección actual está a punto de cambiar, por ejemplo, a través de modificaciones en la interfaz de usuario, procedimientos de cortar y pegar o la propiedad de [**selección**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) .<br/>                                  |
| [**SelectionResized**](inkoverlay-selectionresized.md)   | Se produce cuando el tamaño de la selección actual ha cambiado, por ejemplo, a través de modificaciones en la interfaz de usuario, procedimientos de cortar y pegar o la propiedad de [**selección**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) .<br/>                                             |
| [**SelectionResizing**](inkoverlay-selectionresizing.md) | Se produce cuando el tamaño de la selección actual está a punto de cambiar, por ejemplo, a través de modificaciones en la interfaz de usuario, procedimientos de cortar y pegar o la propiedad de [**selección**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) .<br/>                                      |
| [**Stroke**](inkcollector-stroke.md)                     | Se produce cuando el usuario termina de dibujar un nuevo trazo en cualquier tableta.<br/>                                                                                                                                                                              |
| [**StrokesDeleted**](inkoverlay-strokesdeleted.md)       | Se produce después de eliminar los trazos de la propiedad de [**entrada manuscrita**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_ink) .<br/>                                                                                                                                                      |
| [**StrokesDeleting**](inkoverlay-strokesdeleting.md)     | Se produce antes de que se eliminen los trazos de la propiedad de [**entrada de lápiz**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_ink) .<br/>                                                                                                                                                           |
| [**SystemGesture**](inkcollector-systemgesture.md)       | Se produce cuando se reconoce un gesto del sistema.<br/>                                                                                                                                                                                                    |
| [**TabletAdded**](inkcollector-tabletadded.md)           | Se produce cuando se agrega un [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) al sistema.<br/>                                                                                                                                                                        |
| [**TabletRemoved**](inkcollector-tabletremoved.md)       | Se produce cuando se quita una [**tableta**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) del sistema.<br/>                                                                                                                                                                         |



 

### <a name="interfaces"></a>Interfaces

La clase **InkOverlay** define estas interfaces.



| Interfaz       | Descripción                                                          |
|:----------------|:---------------------------------------------------------------------|
| **IInkOverlay** | Este objeto implementa la interfaz com **IInkOverlay** .<br/> |



 

### <a name="methods"></a>Métodos

La clase **InkOverlay** tiene estos métodos.



| Método                                                                              | Descripción                                                                                                                                                |
|:------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Dibujar**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-draw)                                                     | Establece un rectángulo en el que se debe volver a dibujar la entrada manuscrita en el objeto **InkOverlay** .<br/>                                                                   |
| [**GetEventInterest**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-geteventinterest)                           | Devuelve el estado actual de un evento de objeto **InkOverlay** determinado, es decir, si el evento se está escuchando o usando.<br/>                |
| [**GetGestureStatus**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-getgesturestatus)                           | Devuelve si el objeto **InkOverlay** está interesado en un gesto determinado.<br/>                                                                |
| [**GetWindowInputRectangle**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-getwindowinputrectangle)             | Recupera el rectángulo de ventana, en píxeles, en el que se dibuja la entrada de lápiz.<br/>                                                                           |
| [**HitTestSelection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-hittestselection)                             | Determina qué parte de la selección se ha alcanzado durante una prueba de posicionamiento.<br/>                                                                             |
| [**SetAllTabletsMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setalltabletsmode)                         | Este modo permite que el objeto **InkOverlay** recopile tinta de cualquier tableta conectada al Tablet PC.<br/>                                            |
| [**SetEventInterest**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-seteventinterest)                           | Establece si se debe escuchar o usar un evento concreto.<br/>                                                                                   |
| [**SetGestureStatus**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setgesturestatus)                           | Establece el interés del objeto **InkOverlay** en un gesto conocido.<br/>                                                                              |
| [**SetSingleTabletIntegratedMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setsingletabletintegratedmode) | Este modo permite que el objeto **InkOverlay** recopile tinta de una sola tableta. El objeto **InkOverlay** omite la tinta de otras tabletas.<br/> |
| [**SetWindowInputRectangle**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setwindowinputrectangle)             | Establece el rectángulo de la ventana, en píxeles, que se va a usar para asignar la tinta dibujada a la ventana.<br/>                                                                    |



 

### <a name="properties"></a>Propiedades

La clase **InkOverlay** tiene estas propiedades.



| Propiedad                                                                                       | Tipo de acceso           | Descripción                                                                                                                                                                                  |
|:-----------------------------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AttachMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_attachmode)<br/>                                         | Lectura/escritura<br/> | Obtiene o establece el valor que especifica si el objeto **InkOverlay** se adjunta detrás o delante de la ventana conocida.<br/>                                                       |
| [**AutoRedraw**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_autoredraw)<br/>                                       | Lectura/escritura<br/> | Obtiene o establece un valor que especifica si **InkOverlay** vuelve a dibujar la tinta cuando se invalida la ventana.<br/>                                                                   |
| [**CollectingInk**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectingink)<br/>                                 | Solo lectura<br/>  | Obtiene un valor que especifica si la entrada de lápiz se está dibujando actualmente en un objeto **InkOverlay** .<br/>                                                                                     |
| [**Si CollectionMode es**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectionmode)<br/>                               | Lectura/escritura<br/> | Obtiene o establece el modo de recopilación que determina si se reconocen las entradas de lápiz, los movimientos o ambos a medida que el usuario escribe.<br/>                                                                |
| [**Cursores**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_cursors)<br/>                                             | Solo lectura<br/>  | Obtiene la colección de [**cursores**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursors) que está disponible para su uso en la región de entrada manuscrita.<br/>                                                                                |
| [**DefaultDrawingAttributes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_defaultdrawingattributes)<br/>           | Lectura/escritura<br/> | Obtiene o establece el objeto [**InkDrawingAttributes**](inkdrawingattributes-class.md) predeterminado, que especifica los atributos de dibujo que se usan al dibujar y mostrar la entrada de lápiz.<br/> |
| [**DesiredPacketDescription**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_desiredpacketdescription)<br/>           | Lectura/escritura<br/> | Obtiene o establece el interés de los aspectos del paquete asociado a la entrada de lápiz dibujada en el objeto **InkOverlay** .<br/>                                                                            |
| [**DynamicRendering**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_dynamicrendering)<br/>                             | Lectura/escritura<br/> | Obtiene o establece un valor que indica si la entrada de lápiz se representa a medida que se dibuja.<br/>                                                                                                       |
| [**EditingMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_editingmode)<br/>                                       | Lectura/escritura<br/> | Obtiene o establece un valor que indica si **InkOverlay** está en modo de entrada de lápiz, modo de eliminación o modo de selección/edición.<br/>                                                          |
| [**habilitado**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_enabled)<br/>                                             | Lectura/escritura<br/> | Obtiene o establece un valor que especifica si el objeto **InkOverlay** recopila entradas manuscritas.<br/>                                                                                         |
| [**EraserMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_erasermode)<br/>                                         | Lectura/escritura<br/> | Obtiene o establece un valor que indica si la entrada de lápiz se borra por trazo o por punto.<br/>                                                                                                  |
| [**EraserWidth**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_eraserwidth)<br/>                                       | Lectura/escritura<br/> | Obtiene o establece un valor que especifica el ancho de la punta del lápiz de borrador.<br/>                                                                                                              |
| [**Handle**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_hwnd)<br/>                                                 | Lectura/escritura<br/> | Obtiene o establece el identificador de la ventana a la que está asociado el objeto **InkOverlay** .<br/>                                                                                             |
| [**Entrada de lápiz**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_ink)<br/>                                                       | Lectura/escritura<br/> | Obtiene o establece el objeto [**InkDisp**](inkdisp-class.md) asociado al objeto **InkOverlay** .<br/>                                                                       |
| [**MarginX**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_marginx)<br/>                                             | Lectura/escritura<br/> | Obtiene o establece los márgenes a lo largo del eje x, en píxeles.<br/>                                                                                                                             |
| [**Margen**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_marginy)<br/>                                             | Lectura/escritura<br/> | Obtiene o establece los márgenes a lo largo del eje y, en píxeles.<br/>                                                                                                                             |
| [**MouseIcon**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_mouseicon)<br/>                                         | Lectura/escritura<br/> | Obtiene o establece el icono actual del mouse.<br/>                                                                                                                                       |
| [**MousePointer**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_mousepointer)<br/>                                   | Lectura/escritura<br/> | Obtiene o establece un valor que indica el tipo de puntero del mouse que aparece cuando el mouse está encima de una parte determinada del objeto.<br/>                                                |
| [**Representador**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_renderer)<br/>                                           | Lectura/escritura<br/> | Obtiene o establece el objeto [**InkRenderer**](inkrenderer-class.md) que se usa para dibujar la entrada de lápiz.<br/>                                                                                        |
| [**Selección**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection)<br/>                                           | Lectura/escritura<br/> | Obtiene o establece la colección [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) seleccionada actualmente dentro del control **InkOverlay** .<br/>                                                 |
| [**SupportHighContrastInk**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_supporthighcontrastink)<br/>               | Lectura/escritura<br/> | Obtiene o establece un valor que especifica si la entrada de lápiz se representa como un solo color cuando el sistema está en modo de contraste alto.<br/>                                                           |
| [**SupportHighContrastSelectionUI**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_supporthighcontrastselectionui)<br/> | Lectura/escritura<br/> | Obtiene o establece un valor que especifica si toda la interfaz de usuario de selección se dibuja en contraste alto cuando el sistema está en modo de contraste alto.<br/>                                                  |
| [**Tablet**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_tablet)<br/>                                                  | Solo lectura<br/>  | Obtiene el dispositivo de tableta que está usando actualmente el objeto **InkOverlay** para recopilar datos de entrada.<br/>                                                                                        |



 

## <a name="mfc-implementation-notes"></a>Notas de implementación de MFC

Si ha adjuntado el objeto InkOverlay a un objeto CView, libere el objeto InkOverlay en respuesta al mensaje de destrucción de WM, \_ tal como se muestra en el ejemplo siguiente:


```C++
BOOL CRecognitionAlternatesSampleCppView::OnWndMsg(UINT msg, WPARAM wp, PARAM lp, LRESULT *pLR)
{
    if(WM_DESTROY == msg)
        m_spInkOverlay.Release();
    return CView::OnWndMsg(msg, wp, lp, pLR);
}
```



## <a name="remarks"></a>Observaciones

Se puede crear una instancia de este objeto llamando al método [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) en C++.

El objeto **InkOverlay** es idóneo para tomar notas y scribbling básicas. El uso previsto principal de este objeto es mostrar la entrada de lápiz como entrada de lápiz.

En general, la interfaz de usuario en tiempo de ejecución para este objeto es una ventana transparente con tinta opaca.

Los eventos [**MouseDown**](inkcollector-mousedown.md), [**MouseMove**](inkcollector-mousemove.md), [**MouseUp**](inkcollector-mouseup.md)y [**MouseWheel**](inkcollector-mousewheel.md) devuelven coordenadas x e y en píxeles, y no las unidades HIMETRIC asociadas al espacio de la tinta. Esto se debe a que estos eventos reemplazan los eventos de mouse de las aplicaciones que no reconocen el lápiz y estas aplicaciones entienden solo los píxeles.

> [!Caution]  
> Si va a establecer la propiedad [**AttachMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_attachmode) del objeto **InkOverlay** en Infront, cree el objeto **InkOverlay** en el subproceso en el que se está ejecutando el formulario. La aplicación puede dejar de responder si el objeto **InkOverlay** se crea en un subproceso diferente y su propiedad **AttachMode** se establece en Infront.

 

> [!Note]  
> El objeto **InkOverlay** no se puede liberar de forma segura en un subproceso que no sea de interfaz de usuario.

 

Para mejorar el rendimiento de la aplicación, elimine el objeto **InkOverlay** cuando ya no lo necesite.

Si ha adjuntado el objeto InkOverlay a un objeto CView, libere el objeto InkOverlay en respuesta al mensaje de destrucción de WM, \_ tal como se muestra en el ejemplo siguiente:


```C++
BOOL CRecognitionAlternatesSampleCppView::OnWndMsg(UINT msg, WPARAM wp, PARAM lp, LRESULT *pLR)
{
    if(WM_DESTROY == msg)
        m_spInkOverlay.Release();
    return CView::OnWndMsg(msg, wp, lp, pLR);
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/>                                                       |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                           |
| Encabezado<br/>                   | <dl> <dt>Msinkaut. h (también requiere Msinkaut \_ i. c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**InkCollector (clase)**](inkcollector-class.md)
</dt> <dt>

[Referencia del control InkPicture](inkpicture-control-reference.md)
</dt> <dt>

[Referencia de control InkEdit](inkedit-control-reference.md)
</dt> </dl>

 

