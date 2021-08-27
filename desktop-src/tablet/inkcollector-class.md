---
description: Representa el objeto que se usa para capturar la entrada de lápiz de los dispositivos de tableta disponibles.
ms.assetid: 189f430e-9d00-4e29-bb8c-8ac195896793
title: Clase InkCollector (Msyecciónut.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkCollector
- InkCollector.IInkCollector
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: 02ecf89a1ce8db89105ac9fa0243552efaf5218da98f6d3b0fdfbd58f874d449
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118718181"
---
# <a name="inkcollector-class"></a>InkCollector (clase)

Representa el objeto que se usa para capturar la entrada de lápiz de los dispositivos de tableta disponibles.

La creación del control **InkCollector** detrás de un control transparente (por ejemplo, un Control GroupBox con la propiedad TRANSPARENT de **WS \_ EX) \_** impedirá que **InkCollector** recopile la entrada de lápiz.

**InkCollector** tiene estos tipos de miembros:

-   [Eventos](#events)
-   [Interfaces](#interfaces)
-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="events"></a>Eventos

La **clase InkCollector** tiene estos eventos.



| Evento                                                     | Descripción                                                                                                                                                                                                                                                   |
|:----------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CursorButtonDown**](inkcollector-cursorbuttondown.md) | Se produce cuando **InkCollector detecta** un botón de cursor que está apagado.<br/>                                                                                                                                                                             |
| [**CursorButtonUp**](inkcollector-cursorbuttonup.md)     | Se produce cuando **InkCollector detecta** un botón de cursor que está en marcha.<br/>                                                                                                                                                                               |
| [**CursorDown**](inkcollector-cursordown.md)             | Se produce cuando la punta del cursor se pone en contacto con la superficie digitalizadora de la tableta.<br/>                                                                                                                                                                                 |
| [**CursorInRange**](inkcollector-cursorinrange.md)       | Se produce cuando un cursor entra en el intervalo de detección físico (proximidad) del contexto de la tableta.<br/>                                                                                                                                                        |
| [**CursorOutOfRange**](inkcollector-cursoroutofrange.md) | Se produce cuando el cursor sale del intervalo de detección físico (proximidad) del contexto de la tableta.<br/>                                                                                                                                                      |
| [**Doubleclick**](inkcollector-doubleclick.md)           | Se produce cuando se hace doble clic en el objeto **InkCollector.**<br/>                                                                                                                                                                                         |
| [**Gesto**](inkcollector-gesture.md)                   | Se produce cuando se reconoce un gesto específico de la aplicación.<br/>                                                                                                                                                                                         |
| [**Mousedown**](inkcollector-mousedown.md)               | Se produce cuando el puntero del mouse está sobre el **objeto InkCollector** y se presiona un botón del mouse.<br/>                                                                                                                                                   |
| [**Mousemove**](inkcollector-mousemove.md)               | Se produce cuando el puntero del mouse se mueve sobre el **objeto InkCollector.**<br/>                                                                                                                                                                           |
| [**MouseUp**](inkcollector-mouseup.md)                   | Se produce cuando el puntero del mouse está sobre el **objeto InkCollector** y se libera un botón del mouse.<br/>                                                                                                                                                  |
| [**Mousewheel**](inkcollector-mousewheel.md)             | Se produce cuando la rueda del mouse se mueve mientras el **objeto InkCollector** tiene el foco.<br/>                                                                                                                                                                     |
| [**NewInAirPackets**](inkcollector-newinairpackets.md)   | Se produce cuando se ve un paquete en el aire, lo que sucede cuando un usuario mueve un lápiz cerca de la tableta y el cursor está dentro de la ventana del objeto **InkCollector** o el usuario mueve un mouse dentro de la ventana asociada del objeto **InkCollector.**<br/> |
| [**NewPackets**](inkcollector-newpackets.md)             | Se produce cuando el **objeto InkCollector** recibe paquetes.<br/>                                                                                                                                                                                          |
| [**Golpe**](inkcollector-stroke.md)                     | Se produce cuando el usuario termina de dibujar un nuevo trazo en cualquier tableta.<br/>                                                                                                                                                                                  |
| [**SystemGesture**](inkcollector-systemgesture.md)       | Se produce cuando se reconoce un gesto del sistema.<br/>                                                                                                                                                                                                        |
| [**Tableta agregada**](inkcollector-tabletadded.md)           | Se produce cuando [**se agrega**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) una tableta al sistema.<br/>                                                                                                                                                                                 |
| [**TabletRemoved**](inkcollector-tabletremoved.md)       | Se produce cuando se [**quita**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) una tableta del sistema.<br/>                                                                                                                                                                             |



 

### <a name="interfaces"></a>Interfaces

La **clase InkCollector** define estas interfaces.



| Interfaz         | Descripción                                                            |
|:------------------|:-----------------------------------------------------------------------|
| **IInkCollector** | Este objeto implementa la **interfaz COM IInkCollector.**<br/> |



 

### <a name="methods"></a>Métodos

La **clase InkCollector** tiene estos métodos.



| Método                                                                              | Descripción                                                                                                                                                    |
|:------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetEventInterest**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-geteventinterest)                           | Recupera el estado actual de un evento de objeto **InkCollector** determinado, es decir, si el evento se escucha o se usa.<br/>                |
| [**GetGestureStatus**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-getgesturestatus)                           | Recupera si el **objeto InkCollector** está interesado en un gesto determinado.<br/>                                                                |
| [**GetWindowInputRectangle**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-getwindowinputrectangle)             | Recupera el rectángulo de ventana, en píxeles, dentro del cual se dibuja la entrada manuscrita.<br/>                                                                               |
| [**SetAllTabletsMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setalltabletsmode)                         | Este modo permite que **el objeto InkCollector** recopile la entrada de lápiz de cualquier tableta conectada al tablet PC.<br/>                                              |
| [**SetEventInterest**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-seteventinterest)                           | Modifica un valor que indica si se debe escuchar o usar un evento específico.<br/>                                                            |
| [**SetGestureStatus**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setgesturestatus)                           | Modifica el interés del objeto **InkCollector** en un gesto conocido.<br/>                                                                            |
| [**SetSingleTabletIntegratedMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setsingletabletintegratedmode) | Este modo permite que el **objeto InkCollector** recopile la entrada de lápiz de una sola tableta. El objeto **InkCollector** omite la entrada de lápiz de otras tabletas.<br/> |
| [**SetWindowInputRectangle**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setwindowinputrectangle)             | Modifica el rectángulo de la ventana, en píxeles, para usarlo para asignar la entrada manuscrita dibujada a la ventana.<br/>                                                                    |



 

### <a name="properties"></a>Propiedades

La **clase InkCollector** tiene estas propiedades.



| Propiedad                                                                             | Tipo de acceso          | Descripción                                                                                                                                                                                  |
|:-------------------------------------------------------------------------------------|:---------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Volver a dibujar automáticamente**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_autoredraw)<br/>                             | Solo lectura<br/> | Obtiene o establece un valor que especifica si **InkCollector** vuelve a dibujar la entrada de lápiz cuando se invalida la ventana.<br/>                                                                 |
| [**CollectingInk**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectingink)<br/>                       | Solo lectura<br/> | Obtiene un valor que especifica si la entrada de lápiz se está dibujando actualmente en un **objeto InkCollector.**<br/>                                                                                   |
| [**CollectionMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectionmode)<br/>                     | Solo lectura<br/> | Obtiene o establece el modo de colección que determina si la entrada de lápiz, los gestos o ambos se reconocen cuando el usuario escribe.<br/>                                                                |
| [**Cursores**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_cursors)<br/>                                   | Solo lectura<br/> | Obtiene la [**colección Cursors**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursors) que está disponible para su uso en la región de entrada de entrada.<br/>                                                                                |
| [**DefaultDrawingAttributes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_defaultdrawingattributes)<br/> | Solo lectura<br/> | Obtiene o establece el objeto [**InkDrawingAttributes**](inkdrawingattributes-class.md) predeterminado, que especifica los atributos de dibujo que se usan al dibujar y mostrar la entrada de lápiz.<br/> |
| [**DesiredPacketDescription**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_desiredpacketdescription)<br/> | Solo lectura<br/> | Obtiene o establece el interés en aspectos del paquete asociado a la entrada de lápiz dibujada en el **objeto InkCollector.**<br/>                                                                          |
| [**DynamicRendering**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_dynamicrendering)<br/>                   | Solo lectura<br/> | Obtiene o establece un valor que indica si la entrada de lápiz se representa a medida que se dibuja.<br/>                                                                                                       |
| [**habilitado**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_enabled)<br/>                                   | Solo lectura<br/> | Obtiene o establece un valor que especifica si el **objeto InkCollector** recopila entradas de lápiz.<br/>                                                                                       |
| [**Manejar**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_hwnd)<br/>                                       | Solo lectura<br/> | Obtiene o establece el identificador de la ventana a la que está asociado el **objeto InkCollector.**<br/>                                                                                           |
| [**Entrada de lápiz**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_ink)<br/>                                           | Solo lectura<br/> | Obtiene o establece el [**objeto InkDisp**](inkdisp-class.md) asociado al **objeto InkCollector.**<br/>                                                                     |
| [**MarginX**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_marginx)<br/>                                   | Solo lectura<br/> | Obtiene o establece los márgenes a lo largo del eje X, en píxeles.<br/>                                                                                                                             |
| [**MarginY**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_marginy)<br/>                                   | Solo lectura<br/> | Obtiene o establece los márgenes a lo largo del eje Y, en píxeles.<br/>                                                                                                                             |
| [**MouseIcon**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_mouseicon)<br/>                               | Solo lectura<br/> | Obtiene o establece el icono del mouse personalizado actual.<br/>                                                                                                                                       |
| [**Mousepointer**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_mousepointer)<br/>                         | Solo lectura<br/> | Obtiene o establece un valor que indica el tipo de puntero del mouse que aparece cuando el mouse está sobre una parte determinada del objeto.<br/>                                                |
| [**Representador**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_renderer)<br/>                                 | Solo lectura<br/> | Obtiene o establece el [**objeto InkRenderer**](inkrenderer-class.md) que se usa para dibujar lápiz.<br/>                                                                                        |
| [**SupportHighContrastInk**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_supporthighcontrastink)<br/>     | Solo lectura<br/> | Obtiene o establece un valor que especifica si la entrada de lápiz se representa como un solo color cuando el sistema está contraste alto modo.<br/>                                                           |
| [**Tablet**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_tablet)<br/>                                        | Solo lectura<br/> | Obtiene el dispositivo de tableta que **el objeto InkCollector** está usando actualmente para recopilar la entrada.<br/>                                                                                      |



 

## <a name="remarks"></a>Comentarios

Se puede crear una instancia de este objeto llamando al [**método CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) en C++.

El **objeto InkCollector** recopila solo la entrada de lápiz y los gestos que se introducen en la ventana específica a la que está asociado. El único propósito de **InkCollector** es recopilar la entrada de lápiz del hardware (por ejemplo, a través de un objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) e [**IInkTablet)**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) y entregarla a una aplicación. Básicamente actúa como el origen que distribuye la entrada de lápiz en uno o varios objetos [**InkDisp**](inkdisp-class.md) diferentes, que actúan como contenedor que contiene la entrada de lápiz distribuida.

Para usar **un InkCollector,** se crea, se le dice en qué ventana se va a recopilar la entrada de lápiz dibujada y se habilita. Una vez habilitada, se puede establecer para recopilar solo en uno de los tres modos (el modo se especifica en la [**enumeración InkCollectionMode):**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode)

-   InkOnly, en el que se crea un objeto [**IInkStrokeDisp.**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
-   GestureOnly, en el que se crea un objeto [**IInkGesture.**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture)
-   InkAndGesture, en el que se crean un trazo, un gesto o posiblemente ambos, en función de cómo la aplicación controle los eventos.

Esto significa que, para cada movimiento de un cursor que está dentro del intervalo de una tableta, **InkCollector** siempre recopila un trazo o un gesto y, a veces, ambos. La compatibilidad con gestos se basa en el reconocedor de gestos de Microsoft.

**InkCollector controla toda** la entrada de tableta. La entrada de lápiz se puede recopilar de todas las tabletas conectadas (incluido el mouse) simultáneamente. Los cambios en [**los objetos IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) e [**IInkCursorButton**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursorbutton) pueden hacer que el objeto **InkCollector** desenvía un evento.

**InkCollector también** administra la lista de cursores que encuentra durante su existencia. Cuando **InkCollector encuentra** un nuevo cursor, el [**evento CursorInRange**](inkcollector-cursorinrange.md) se genera con el parámetro *newCursor* establecido **en VARIANT \_ TRUE.** Las aplicaciones usan **InkCollector para** administrar nuevos cursores.

Se puede asociar más de un **InkCollector** a un identificador de ventana determinado, incluso si sus áreas de colección, establecidas en el constructor o con el [**método SetWindowInputRectangle,**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setwindowinputrectangle) se superponen. Sin embargo, la única manera en que funciona este escenario es si **inkCollector** llama a [**SetSingleTabletIntegratedMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setsingletabletintegratedmode) y usa una tableta única. Este comportamiento facilita el almacenamiento de entrada de lápiz en un objeto independiente para cada tableta.

Se produce un error si el rectángulo de entrada de ventana de un **InkCollectors** habilitado (establecido con la propiedad [**Enabled)**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_enabled) se superpone al rectángulo de entrada de ventana de otro **InkCollector habilitado.**

> [!Note]  
> La superposición puede producirse sin un error siempre y cuando solo uno de los rectángulos de entrada esté habilitado en cualquier momento conocido.

 

Los [**eventos MouseDown**](inkcollector-mousedown.md), [**MouseMove,**](inkcollector-mousemove.md) [**MouseUp**](inkcollector-mouseup.md)y [**MouseWheel**](inkcollector-mousewheel.md) devuelven coordenadas x e y en píxeles, y no las unidades HIMETRIC asociadas al espacio de entrada de lápiz. Esto se debe a que estos eventos reemplazan los eventos del mouse de aplicaciones que no son conscientes del lápiz y estas aplicaciones solo entienden píxeles.

> [!Note]  
> El **objeto InkCollector** no se puede liberar de forma segura en un subproceso que no es de interfaz de usuario.

 

Para mejorar el rendimiento de la aplicación, elimine el objeto **InkCollector** cuando ya no sea necesario.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                       |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Msgniut.h (también requiere Ms ashut \_ i.c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Referencia del control InkEdit](inkedit-control-reference.md)
</dt> <dt>

[**InkDisp (clase)**](inkdisp-class.md)
</dt> <dt>

[**InkOverlay (clase)**](inkoverlay-class.md)
</dt> <dt>

[Referencia del control InkPicture](inkpicture-control-reference.md)
</dt> </dl>

 

