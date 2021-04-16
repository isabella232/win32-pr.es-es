---
description: Representa el objeto que se usa para capturar la tinta de los dispositivos de tableta disponibles.
ms.assetid: 189f430e-9d00-4e29-bb8c-8ac195896793
title: InkCollector (clase) (Msinkaut. h)
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
ms.openlocfilehash: 17eff388a759b9b0873929447e4c8fe008e2fba5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540398"
---
# <a name="inkcollector-class"></a>InkCollector (clase)

Representa el objeto que se usa para capturar la tinta de los dispositivos de tableta disponibles.

La creación del control **InkCollector** detrás de un control transparente (como GroupBox con el conjunto de propiedades **\_ \_ transparentes WS ex** ) impedirá que **InkCollector** recopile la tinta.

**InkCollector** tiene estos tipos de miembros:

-   [Eventos](#events)
-   [Interfaces](#interfaces)
-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="events"></a>Events

La clase **InkCollector** tiene estos eventos.



| Evento                                                     | Descripción                                                                                                                                                                                                                                                   |
|:----------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CursorButtonDown**](inkcollector-cursorbuttondown.md) | Se produce cuando **InkCollector** detecta un botón de cursor que está inactivo.<br/>                                                                                                                                                                             |
| [**CursorButtonUp**](inkcollector-cursorbuttonup.md)     | Se produce cuando **InkCollector** detecta un botón de cursor que está activo.<br/>                                                                                                                                                                               |
| [**CursorDown**](inkcollector-cursordown.md)             | Se produce cuando la sugerencia del cursor se pone en contacto con la superficie de la tableta de la digitalización.<br/>                                                                                                                                                                                 |
| [**CursorInRange**](inkcollector-cursorinrange.md)       | Se produce cuando un cursor entra en el intervalo de detección física (proximidad) del contexto de la tableta.<br/>                                                                                                                                                        |
| [**CursorOutOfRange**](inkcollector-cursoroutofrange.md) | Se produce cuando el cursor deja el intervalo de detección física (proximidad) del contexto de la tableta.<br/>                                                                                                                                                      |
| [**DoubleClick**](inkcollector-doubleclick.md)           | Se produce cuando se hace doble clic en el objeto **InkCollector** .<br/>                                                                                                                                                                                         |
| [**Gesto**](inkcollector-gesture.md)                   | Se produce cuando se reconoce un gesto específico de la aplicación.<br/>                                                                                                                                                                                         |
| [**Eventos**](inkcollector-mousedown.md)               | Se produce cuando el puntero del mouse se encuentra sobre el objeto **InkCollector** y se presiona un botón del mouse.<br/>                                                                                                                                                   |
| [**MouseMove**](inkcollector-mousemove.md)               | Se produce cuando el puntero del mouse se mueve sobre el objeto **InkCollector** .<br/>                                                                                                                                                                           |
| [**MouseUp**](inkcollector-mouseup.md)                   | Se produce cuando el puntero del mouse se encuentra sobre el objeto **InkCollector** y se suelta un botón del mouse.<br/>                                                                                                                                                  |
| [**Rueda**](inkcollector-mousewheel.md)             | Se produce cuando se mueve la rueda del mouse mientras el objeto **InkCollector** tiene el foco.<br/>                                                                                                                                                                     |
| [**NewInAirPackets**](inkcollector-newinairpackets.md)   | Se produce cuando se detecta un paquete en el aire, lo que ocurre cuando un usuario mueve un lápiz cerca de la tableta y el cursor se encuentra dentro de la ventana del objeto **InkCollector** o el usuario mueve el mouse dentro de la ventana asociada del objeto **InkCollector** .<br/> |
| [**NewPackets**](inkcollector-newpackets.md)             | Se produce cuando el objeto **InkCollector** recibe paquetes.<br/>                                                                                                                                                                                          |
| [**Stroke**](inkcollector-stroke.md)                     | Se produce cuando el usuario termina de dibujar un nuevo trazo en cualquier tableta.<br/>                                                                                                                                                                                  |
| [**SystemGesture**](inkcollector-systemgesture.md)       | Se produce cuando se reconoce un gesto del sistema.<br/>                                                                                                                                                                                                        |
| [**TabletAdded**](inkcollector-tabletadded.md)           | Se produce cuando se agrega una [**tableta**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) al sistema.<br/>                                                                                                                                                                                 |
| [**TabletRemoved**](inkcollector-tabletremoved.md)       | Se produce cuando se quita una [**tableta**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) del sistema.<br/>                                                                                                                                                                             |



 

### <a name="interfaces"></a>Interfaces

La clase **InkCollector** define estas interfaces.



| Interfaz         | Descripción                                                            |
|:------------------|:-----------------------------------------------------------------------|
| **IInkCollector** | Este objeto implementa la interfaz com **IInkCollector** .<br/> |



 

### <a name="methods"></a>Métodos

La clase **InkCollector** tiene estos métodos.



| Método                                                                              | Descripción                                                                                                                                                    |
|:------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetEventInterest**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-geteventinterest)                           | Recupera el estado actual de un evento de objeto **InkCollector** determinado, es decir, si se está realizando la escucha o el uso del evento.<br/>                |
| [**GetGestureStatus**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-getgesturestatus)                           | Recupera si el objeto **InkCollector** está interesado en un gesto determinado.<br/>                                                                |
| [**GetWindowInputRectangle**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-getwindowinputrectangle)             | Recupera el rectángulo de ventana, en píxeles, en el que se dibuja la entrada de lápiz.<br/>                                                                               |
| [**SetAllTabletsMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setalltabletsmode)                         | Este modo permite que el objeto **InkCollector** recopile tinta de cualquier tableta conectada al Tablet PC.<br/>                                              |
| [**SetEventInterest**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-seteventinterest)                           | Modifica un valor que indica si se debe escuchar o usar un evento concreto.<br/>                                                            |
| [**SetGestureStatus**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setgesturestatus)                           | Modifica el interés del objeto **InkCollector** en un gesto conocido.<br/>                                                                            |
| [**SetSingleTabletIntegratedMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setsingletabletintegratedmode) | Este modo permite que el objeto **InkCollector** recopile la tinta de una sola tableta. El objeto **InkCollector** omite la tinta de otras tabletas.<br/> |
| [**SetWindowInputRectangle**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setwindowinputrectangle)             | Modifica el rectángulo de la ventana, en píxeles, que se va a usar para asignar la entrada de lápiz dibujada a la ventana.<br/>                                                                    |



 

### <a name="properties"></a>Propiedades

La clase **InkCollector** tiene estas propiedades.



| Propiedad                                                                             | Tipo de acceso          | Descripción                                                                                                                                                                                  |
|:-------------------------------------------------------------------------------------|:---------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AutoRedraw**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_autoredraw)<br/>                             | Solo lectura<br/> | Obtiene o establece un valor que especifica si **InkCollector** vuelve a dibujar la tinta cuando se invalida la ventana.<br/>                                                                 |
| [**CollectingInk**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectingink)<br/>                       | Solo lectura<br/> | Obtiene un valor que especifica si la entrada de lápiz se está dibujando actualmente en un objeto **InkCollector** .<br/>                                                                                   |
| [**Si CollectionMode es**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectionmode)<br/>                     | Solo lectura<br/> | Obtiene o establece el modo de recopilación que determina si se reconocen las entradas de lápiz, los movimientos o ambos a medida que el usuario escribe.<br/>                                                                |
| [**Cursores**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_cursors)<br/>                                   | Solo lectura<br/> | Obtiene la colección de [**cursores**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursors) que está disponible para su uso en la región de entrada manuscrita.<br/>                                                                                |
| [**DefaultDrawingAttributes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_defaultdrawingattributes)<br/> | Solo lectura<br/> | Obtiene o establece el objeto [**InkDrawingAttributes**](inkdrawingattributes-class.md) predeterminado, que especifica los atributos de dibujo que se usan al dibujar y mostrar la entrada de lápiz.<br/> |
| [**DesiredPacketDescription**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_desiredpacketdescription)<br/> | Solo lectura<br/> | Obtiene o establece el interés de los aspectos del paquete asociado a la entrada de lápiz dibujada en el objeto **InkCollector** .<br/>                                                                          |
| [**DynamicRendering**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_dynamicrendering)<br/>                   | Solo lectura<br/> | Obtiene o establece un valor que indica si la entrada de lápiz se representa a medida que se dibuja.<br/>                                                                                                       |
| [**habilitado**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_enabled)<br/>                                   | Solo lectura<br/> | Obtiene o establece un valor que especifica si el objeto **InkCollector** recopila entradas manuscritas.<br/>                                                                                       |
| [**Handle**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_hwnd)<br/>                                       | Solo lectura<br/> | Obtiene o establece el identificador de la ventana a la que se adjunta el objeto **InkCollector** .<br/>                                                                                           |
| [**Entrada de lápiz**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_ink)<br/>                                           | Solo lectura<br/> | Obtiene o establece el objeto [**InkDisp**](inkdisp-class.md) asociado con el objeto **InkCollector** .<br/>                                                                     |
| [**MarginX**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_marginx)<br/>                                   | Solo lectura<br/> | Obtiene o establece los márgenes a lo largo del eje x, en píxeles.<br/>                                                                                                                             |
| [**Margen**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_marginy)<br/>                                   | Solo lectura<br/> | Obtiene o establece los márgenes a lo largo del eje y, en píxeles.<br/>                                                                                                                             |
| [**MouseIcon**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_mouseicon)<br/>                               | Solo lectura<br/> | Obtiene o establece el icono actual del mouse.<br/>                                                                                                                                       |
| [**MousePointer**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_mousepointer)<br/>                         | Solo lectura<br/> | Obtiene o establece un valor que indica el tipo de puntero del mouse que aparece cuando el mouse está encima de una parte determinada del objeto.<br/>                                                |
| [**Representador**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_renderer)<br/>                                 | Solo lectura<br/> | Obtiene o establece el objeto [**InkRenderer**](inkrenderer-class.md) que se usa para dibujar la entrada de lápiz.<br/>                                                                                        |
| [**SupportHighContrastInk**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_supporthighcontrastink)<br/>     | Solo lectura<br/> | Obtiene o establece un valor que especifica si la entrada de lápiz se representa como un solo color cuando el sistema está en modo de contraste alto.<br/>                                                           |
| [**Tablet**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_tablet)<br/>                                        | Solo lectura<br/> | Obtiene el dispositivo de tableta que el objeto **InkCollector** está usando actualmente para recopilar la entrada.<br/>                                                                                      |



 

## <a name="remarks"></a>Observaciones

Se puede crear una instancia de este objeto llamando al método [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) en C++.

El objeto **InkCollector** solo recopila entradas de lápiz y movimientos que se escriben en la ventana específica a la que está asociada. El único propósito de **InkCollector** es recopilar la tinta del hardware (por ejemplo, a través de un objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) y [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) ) y entregarla a una aplicación. Básicamente actúa como el origen que distribuye la entrada manuscrita en uno o varios objetos [**InkDisp**](inkdisp-class.md) diferentes, que actúan como contenedor que contiene la tinta distribuida.

Para usar **InkCollector**, debe crearlo, indicarle en qué ventana se va a recopilar la tinta dibujada y habilitarla. Una vez habilitado, se puede establecer para que se recopile solo en uno de los tres modos (el modo se especifica en la enumeración [**InkCollectionMode**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode) ):

-   InkOnly, en la que se crea un objeto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) .
-   GestureOnly, en la que se crea un objeto [**IInkGesture**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture) .
-   InkAndGesture, en el que se crean un trazo, un gesto o potencialmente ambos, en función de cómo controle la aplicación los eventos.

Esto significa que, para cada movimiento de un cursor que se encuentra dentro del intervalo de una tableta, **InkCollector** siempre recopila un trazo o un gesto y, en ocasiones, ambos. La compatibilidad con gestos está integrada en el reconocedor de gestos de Microsoft.

**InkCollector** controla todas las entradas de Tablet PC. La tinta se puede recopilar de todas las tabletas conectadas (incluido el mouse) simultáneamente. Los cambios en los objetos [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) y [**IInkCursorButton**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursorbutton) pueden hacer que el objeto **InkCollector** desencadene un evento.

**InkCollector** también administra la lista de cursores que encuentra durante su existencia. Cuando **InkCollector** encuentra un nuevo cursor, el evento [**CursorInRange**](inkcollector-cursorinrange.md) se activa con el parámetro *newCursor* establecido en **Variant \_ true**. Las aplicaciones usan **InkCollector** para administrar nuevos cursores.

Se puede asociar más de un objeto **InkCollector** a un identificador de ventana determinado, incluso si sus áreas de colección, establecidas en el constructor o con el método [**SetWindowInputRectangle**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setwindowinputrectangle) , se superponen. Sin embargo, la única manera en que funciona este escenario es si cada **InkCollector** llama a [**SetSingleTabletIntegratedMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setsingletabletintegratedmode) y usa una tableta única. Este comportamiento facilita la tarea de almacenar entradas manuscritas en un objeto independiente para cada tableta.

Se produce un error si el rectángulo de entrada de la ventana de un **InkCollectors** habilitado (establecido con la propiedad [**habilitada**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_enabled) ) se superpone al rectángulo de entrada de la ventana de otro **InkCollector** habilitado.

> [!Note]  
> La superposición puede producirse sin un error, siempre que solo uno de los rectángulos de entrada esté habilitado en cualquier momento conocido.

 

Los eventos [**MouseDown**](inkcollector-mousedown.md), [**MouseMove**](inkcollector-mousemove.md), [**MouseUp**](inkcollector-mouseup.md)y [**MouseWheel**](inkcollector-mousewheel.md) devuelven coordenadas x e y en píxeles, y no las unidades HIMETRIC asociadas al espacio de la tinta. Esto se debe a que estos eventos reemplazan los eventos de mouse de las aplicaciones que no reconocen el lápiz y estas aplicaciones entienden solo los píxeles.

> [!Note]  
> El objeto **InkCollector** no se puede liberar de forma segura en un subproceso que no sea de interfaz de usuario.

 

Para mejorar el rendimiento de la aplicación, elimine el objeto **InkCollector** cuando ya no lo necesite.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/>                                                       |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                           |
| Encabezado<br/>                   | <dl> <dt>Msinkaut. h (también requiere Msinkaut \_ i. c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Referencia de control InkEdit](inkedit-control-reference.md)
</dt> <dt>

[**Clase InkDisp**](inkdisp-class.md)
</dt> <dt>

[**InkOverlay (clase)**](inkoverlay-class.md)
</dt> <dt>

[Referencia del control InkPicture](inkpicture-control-reference.md)
</dt> </dl>

 

