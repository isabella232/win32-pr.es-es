---
description: Representa un objeto que es útil para escenarios de anotación en los que los usuarios no están interesados en realizar el reconocimiento en la entrada de lápiz, sino que están interesados en el tamaño, la forma, el color y la posición de la entrada de lápiz.
ms.assetid: 61191ab3-075e-458b-9e0f-4bc255687b3c
title: Clase InkOverlay (Msyecciónut.h)
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
ms.openlocfilehash: d1a818c1fef9006abad2dd31da5a41f43aeb3df9a9b75d348d8987938abfcea6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967124"
---
# <a name="inkoverlay-class"></a>InkOverlay (clase)

Representa un objeto que es útil para escenarios de anotación en los que los usuarios no están interesados en realizar el reconocimiento en la entrada de lápiz, sino que están interesados en el tamaño, la forma, el color y la posición de la entrada de lápiz.

La creación del control **InkOverlay** detrás de un control transparente (por ejemplo, un Control GroupBox con la propiedad TRANSPARENT de WS EX) impedirá que \_ \_ **InkOverlay** recopile la entrada de lápiz.

**InkOverlay** tiene estos tipos de miembros:

-   [Eventos](#events)
-   [Interfaces](#interfaces)
-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="events"></a>Eventos

La **clase InkOverlay** tiene estos eventos.



| Evento                                                     | Descripción                                                                                                                                                                                                                                               |
|:----------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CursorButtonDown**](inkcollector-cursorbuttondown.md) | Se produce cuando **InkOverlay** detecta un botón de cursor que está apagado.<br/>                                                                                                                                                                           |
| [**CursorButtonUp**](inkcollector-cursorbuttonup.md)     | Se produce cuando **InkOverlay** detecta un botón de cursor que está en marcha.<br/>                                                                                                                                                                             |
| [**CursorDown**](inkcollector-cursordown.md)             | Se produce cuando la punta del cursor se pone en contacto con la superficie digitalizadora de la tableta.<br/>                                                                                                                                                                             |
| [**CursorInRange**](inkcollector-cursorinrange.md)       | Se produce cuando un cursor entra en el intervalo de detección físico (proximidad) del contexto de la tableta.<br/>                                                                                                                                                    |
| [**CursorOutOfRange**](inkcollector-cursoroutofrange.md) | Se produce cuando el cursor sale del intervalo de detección físico (proximidad) del contexto de la tableta.<br/>                                                                                                                                                  |
| [**Doubleclick**](inkcollector-doubleclick.md)           | Se produce cuando se hace doble clic en el objeto **InkOverlay.**<br/>                                                                                                                                                                                       |
| [**Gesto**](inkcollector-gesture.md)                   | Se produce cuando se reconoce un gesto específico de la aplicación.<br/>                                                                                                                                                                                     |
| [**Mousedown**](inkcollector-mousedown.md)               | Se produce cuando el puntero del mouse está sobre el **objeto InkOverlay** y se presiona un botón del mouse.<br/>                                                                                                                                                 |
| [**Mousemove**](inkcollector-mousemove.md)               | Se produce cuando el puntero del mouse se mueve sobre el **objeto InkOverlay.**<br/>                                                                                                                                                                         |
| [**MouseUp**](inkcollector-mouseup.md)                   | Se produce cuando el puntero del mouse está sobre el **objeto InkOverlay** y se libera un botón del mouse.<br/>                                                                                                                                                |
| [**Mousewheel**](inkcollector-mousewheel.md)             | Se produce cuando la rueda del mouse se mueve mientras el **objeto InkOverlay** tiene el foco.<br/>                                                                                                                                                                   |
| [**NewInAirPackets**](inkcollector-newinairpackets.md)   | Se produce cuando se ve un paquete en el aire, lo que sucede cuando un usuario mueve un lápiz cerca de la tableta y el cursor está dentro de la ventana del objeto **InkOverlay** o el usuario mueve un mouse dentro de la ventana asociada del objeto **InkOverlay.**<br/> |
| [**NewPackets**](inkcollector-newpackets.md)             | Se produce cuando el **objeto InkOverlay** recibe paquetes.<br/>                                                                                                                                                                                        |
| [**Pintado**](inkoverlay-painted.md)                     | Se produce cuando el **objeto InkOverlay** ha terminado de volver a dibujarse.<br/>                                                                                                                                                                          |
| [**Pintura**](inkoverlay-painting.md)                   | Se produce antes de que **el objeto InkOverlay** se vuelva a dibujar.<br/>                                                                                                                                                                                        |
| [**SelectionChanged**](inkoverlay-selectionchanged.md)   | Se produce cuando la selección de entrada de lápiz dentro del control ha cambiado, por ejemplo, mediante modificaciones en la interfaz de usuario, procedimientos de cortar y pegar o la [**propiedad Selection.**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection)<br/>                                       |
| [**SelectionChanging**](inkoverlay-selectionchanging.md) | Se produce cuando la selección de entrada de lápiz dentro del control está a punto de cambiar, por ejemplo, mediante modificaciones en la interfaz de usuario, procedimientos de cortar y pegar o la [**propiedad Selection.**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection)<br/>                                |
| [**SelectionMoved**](inkoverlay-selectionmoved.md)       | Se produce cuando la posición de la selección actual ha cambiado, por ejemplo, mediante modificaciones en la interfaz de usuario, los procedimientos de cortar y pegar o la [**propiedad Selection.**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection)<br/>                                         |
| [**SelectionMoving**](inkoverlay-selectionmoving.md)     | Se produce cuando la posición de la selección actual está a punto de cambiar, por ejemplo, mediante modificaciones en la interfaz de usuario, procedimientos de cortar y pegar o la [**propiedad Selection.**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection)<br/>                                  |
| [**SelectionResized**](inkoverlay-selectionresized.md)   | Se produce cuando el tamaño de la selección actual ha cambiado, por ejemplo, mediante modificaciones en la interfaz de usuario, los procedimientos de cortar y pegar o la [**propiedad Selection.**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection)<br/>                                             |
| [**SelectionResizing**](inkoverlay-selectionresizing.md) | Se produce cuando el tamaño de la selección actual está a punto de cambiar, por ejemplo, mediante modificaciones en la interfaz de usuario, los procedimientos de cortar y pegar o la [**propiedad Selection.**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection)<br/>                                      |
| [**Golpe**](inkcollector-stroke.md)                     | Se produce cuando el usuario termina de dibujar un nuevo trazo en cualquier tableta.<br/>                                                                                                                                                                              |
| [**StrokesDeleted**](inkoverlay-strokesdeleted.md)       | Se produce después de que se hayan eliminado los trazos de la [**propiedad Ink.**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_ink)<br/>                                                                                                                                                      |
| [**StrokesDeleting**](inkoverlay-strokesdeleting.md)     | Se produce antes de que se eliminen los trazos de la [**propiedad Ink.**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_ink)<br/>                                                                                                                                                           |
| [**SystemGesture**](inkcollector-systemgesture.md)       | Se produce cuando se reconoce un gesto del sistema.<br/>                                                                                                                                                                                                    |
| [**Tableta agregada**](inkcollector-tabletadded.md)           | Se produce cuando [**se agrega un IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) al sistema.<br/>                                                                                                                                                                        |
| [**TabletRemoved**](inkcollector-tabletremoved.md)       | Se produce cuando se [**quita**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) una tableta del sistema.<br/>                                                                                                                                                                         |



 

### <a name="interfaces"></a>Interfaces

La **clase InkOverlay** define estas interfaces.



| Interfaz       | Descripción                                                          |
|:----------------|:---------------------------------------------------------------------|
| **IInkOverlay** | Este objeto implementa la **interfaz COM IInkOverlay.**<br/> |



 

### <a name="methods"></a>Métodos

La **clase InkOverlay** tiene estos métodos.



| Método                                                                              | Descripción                                                                                                                                                |
|:------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Dibujar**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-draw)                                                     | Establece un rectángulo en el que se va a volver a dibujar la entrada de lápiz dentro del **objeto InkOverlay.**<br/>                                                                   |
| [**GetEventInterest**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-geteventinterest)                           | Devuelve el estado actual de un evento de objeto **InkOverlay** determinado, es decir, si el evento se escucha o se usa.<br/>                |
| [**GetGestureStatus**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-getgesturestatus)                           | Devuelve si el **objeto InkOverlay** está interesado en un gesto determinado.<br/>                                                                |
| [**GetWindowInputRectangle**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-getwindowinputrectangle)             | Recupera el rectángulo de ventana, en píxeles, dentro del cual se dibuja la entrada manuscrita.<br/>                                                                           |
| [**HitTestSelection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-hittestselection)                             | Determina qué parte de la selección se alcanzó durante una prueba de selección.<br/>                                                                             |
| [**SetAllTabletsMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setalltabletsmode)                         | Este modo permite que **el objeto InkOverlay** recopile la entrada de lápiz de cualquier tableta conectada al tablet PC.<br/>                                            |
| [**SetEventInterest**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-seteventinterest)                           | Establece si se debe escuchar o usar un evento específico.<br/>                                                                                   |
| [**SetGestureStatus**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setgesturestatus)                           | Establece el interés del objeto **InkOverlay** en un gesto conocido.<br/>                                                                              |
| [**SetSingleTabletIntegratedMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setsingletabletintegratedmode) | Este modo permite que el **objeto InkOverlay** recopile la entrada de lápiz de una sola tableta. El objeto **InkOverlay** omite la entrada de lápiz de otras tabletas.<br/> |
| [**SetWindowInputRectangle**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setwindowinputrectangle)             | Establece el rectángulo de la ventana, en píxeles, que se usará para asignar la entrada manuscrita dibujada a la ventana.<br/>                                                                    |



 

### <a name="properties"></a>Propiedades

La **clase InkOverlay** tiene estas propiedades.



| Propiedad                                                                                       | Tipo de acceso           | Descripción                                                                                                                                                                                  |
|:-----------------------------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AttachMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_attachmode)<br/>                                         | Lectura/escritura<br/> | Obtiene o establece el valor que especifica si el **objeto InkOverlay** está asociado detrás o delante de la ventana conocida.<br/>                                                       |
| [**AutoRedraw**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_autoredraw)<br/>                                       | Lectura/escritura<br/> | Obtiene o establece un valor que especifica si **InkOverlay** vuelve a dibujar la entrada de lápiz cuando se invalida la ventana.<br/>                                                                   |
| [**CollectingInk**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectingink)<br/>                                 | Solo lectura<br/>  | Obtiene un valor que especifica si la entrada de lápiz se dibuja actualmente en un **objeto InkOverlay.**<br/>                                                                                     |
| [**CollectionMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectionmode)<br/>                               | Lectura/escritura<br/> | Obtiene o establece el modo de colección que determina si la entrada de lápiz, los gestos o ambos se reconocen cuando el usuario escribe.<br/>                                                                |
| [**Cursores**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_cursors)<br/>                                             | Solo lectura<br/>  | Obtiene la [**colección Cursors**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursors) que está disponible para su uso en la región de entrada de entrada.<br/>                                                                                |
| [**DefaultDrawingAttributes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_defaultdrawingattributes)<br/>           | Lectura/escritura<br/> | Obtiene o establece el objeto [**InkDrawingAttributes**](inkdrawingattributes-class.md) predeterminado, que especifica los atributos de dibujo que se usan al dibujar y mostrar lápiz.<br/> |
| [**DesiredPacketDescription**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_desiredpacketdescription)<br/>           | Lectura/escritura<br/> | Obtiene o establece el interés en aspectos del paquete asociado a la entrada de lápiz dibujada en el **objeto InkOverlay.**<br/>                                                                            |
| [**DynamicRendering**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_dynamicrendering)<br/>                             | Lectura/escritura<br/> | Obtiene o establece un valor que indica si la entrada de lápiz se representa a medida que se dibuja.<br/>                                                                                                       |
| [**EditingMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_editingmode)<br/>                                       | Lectura/escritura<br/> | Obtiene o establece un valor que indica si **InkOverlay** está en modo de entrada de lápiz, en modo de eliminación o en modo de selección o edición.<br/>                                                          |
| [**habilitado**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_enabled)<br/>                                             | Lectura/escritura<br/> | Obtiene o establece un valor que especifica si el **objeto InkOverlay** recopila entradas de lápiz.<br/>                                                                                         |
| [**EraserMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_erasermode)<br/>                                         | Lectura/escritura<br/> | Obtiene o establece un valor que indica si la entrada de lápiz se borra por trazo o por punto.<br/>                                                                                                  |
| [**EraserWidth**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_eraserwidth)<br/>                                       | Lectura/escritura<br/> | Obtiene o establece un valor que especifica el ancho de la punta del lápiz de borrador.<br/>                                                                                                              |
| [**Manejar**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_hwnd)<br/>                                                 | Lectura/escritura<br/> | Obtiene o establece el identificador de la ventana a la que está asociado **el objeto InkOverlay.**<br/>                                                                                             |
| [**Entrada de lápiz**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_ink)<br/>                                                       | Lectura/escritura<br/> | Obtiene o establece el [**objeto InkDisp**](inkdisp-class.md) asociado al **objeto InkOverlay.**<br/>                                                                       |
| [**MarginX**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_marginx)<br/>                                             | Lectura/escritura<br/> | Obtiene o establece los márgenes a lo largo del eje X, en píxeles.<br/>                                                                                                                             |
| [**MarginY**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_marginy)<br/>                                             | Lectura/escritura<br/> | Obtiene o establece los márgenes a lo largo del eje Y, en píxeles.<br/>                                                                                                                             |
| [**MouseIcon**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_mouseicon)<br/>                                         | Lectura/escritura<br/> | Obtiene o establece el icono del mouse personalizado actual.<br/>                                                                                                                                       |
| [**Mousepointer**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_mousepointer)<br/>                                   | Lectura/escritura<br/> | Obtiene o establece un valor que indica el tipo de puntero del mouse que aparece cuando el mouse está sobre una parte determinada del objeto.<br/>                                                |
| [**Representador**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_renderer)<br/>                                           | Lectura/escritura<br/> | Obtiene o establece el [**objeto InkRenderer**](inkrenderer-class.md) que se usa para dibujar lápiz.<br/>                                                                                        |
| [**Número de selección**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection)<br/>                                           | Lectura/escritura<br/> | Obtiene o establece la [colección InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) que está seleccionada actualmente dentro del control **InkOverlay.**<br/>                                                 |
| [**SupportHighContrastInk**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_supporthighcontrastink)<br/>               | Lectura/escritura<br/> | Obtiene o establece un valor que especifica si la entrada de lápiz se representa como un solo color cuando el sistema está contraste alto modo.<br/>                                                           |
| [**SupportHighContrastSelectionUI**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_supporthighcontrastselectionui)<br/> | Lectura/escritura<br/> | Obtiene o establece un valor que especifica si toda la interfaz de usuario de selección se dibuja en contraste alto cuando el sistema está en contraste alto seleccionado.<br/>                                                  |
| [**Tablet**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_tablet)<br/>                                                  | Solo lectura<br/>  | Obtiene el dispositivo de tableta que el **objeto InkOverlay** usa actualmente para recopilar la entrada.<br/>                                                                                        |



 

## <a name="mfc-implementation-notes"></a>Notas de implementación de MFC

Si ha adjuntado el objeto InkOverlay a un objeto CView, suelte el objeto InkOverlay en respuesta al mensaje WM DESTROY, como se muestra \_ en el ejemplo siguiente:


```C++
BOOL CRecognitionAlternatesSampleCppView::OnWndMsg(UINT msg, WPARAM wp, PARAM lp, LRESULT *pLR)
{
    if(WM_DESTROY == msg)
        m_spInkOverlay.Release();
    return CView::OnWndMsg(msg, wp, lp, pLR);
}
```



## <a name="remarks"></a>Comentarios

Se puede crear una instancia de este objeto llamando al [**método CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) en C++.

El **objeto InkOverlay** es adecuado para la toma de notas y la transcripción básica. El uso previsto principal de este objeto es mostrar la entrada de lápiz como entrada de lápiz.

En general, la interfaz de usuario en tiempo de ejecución para este objeto es una ventana transparente con entrada de lápiz opaca.

Los [**eventos MouseDown**](inkcollector-mousedown.md), [**MouseMove,**](inkcollector-mousemove.md) [**MouseUp**](inkcollector-mouseup.md)y [**MouseWheel**](inkcollector-mousewheel.md) devuelven coordenadas x e y en píxeles, y no las unidades HIMETRIC asociadas al espacio de entrada de lápiz. Esto se debe a que estos eventos reemplazan los eventos del mouse de aplicaciones que no son conscientes del lápiz y estas aplicaciones solo entienden píxeles.

> [!Caution]  
> Si va a establecer la propiedad [**AttachMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_attachmode) del objeto **InkOverlay** en InFront, cree el objeto **InkOverlay** en el subproceso en el que se ejecuta el formulario. La aplicación puede dejar de responder si el **objeto InkOverlay** se crea en otro subproceso y su **propiedad AttachMode** está establecida en InFront.

 

> [!Note]  
> El **objeto InkOverlay** no se puede liberar de forma segura en un subproceso que no es de interfaz de usuario.

 

Para mejorar el rendimiento de la aplicación, elimine el **objeto InkOverlay** cuando ya no sea necesario.

Si ha adjuntado el objeto InkOverlay a un objeto CView, suelte el objeto InkOverlay en respuesta al mensaje WM DESTROY, como se muestra \_ en el ejemplo siguiente:


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
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                       |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Msgniut.h (también requiere Ms ashut \_ i.c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**InkCollector (clase)**](inkcollector-class.md)
</dt> <dt>

[Referencia del control InkPicture](inkpicture-control-reference.md)
</dt> <dt>

[Referencia del control InkEdit](inkedit-control-reference.md)
</dt> </dl>

 

