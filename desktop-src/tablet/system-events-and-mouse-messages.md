---
description: La aplicación incorpora un diseño y un uso óptimos del lápiz de tableta mediante el envío de mensajes Windows de Microsoft y eventos del sistema.
ms.assetid: ccd45b68-f037-43da-a7d0-1df9439afd11
title: Eventos del sistema y mensajes del mouse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d118b4cc0de115ddcf57fcebbbcea9923656fdad5bb11f31173fb03f4edfb1d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119335115"
---
# <a name="system-events-and-mouse-messages"></a>Eventos del sistema y mensajes del mouse

La aplicación incorpora un diseño y un uso óptimos del lápiz de tableta mediante el envío de mensajes Windows de Microsoft y eventos del sistema. Las aplicaciones reciben ambos conjuntos de eventos para cada movimiento o acción de lápiz. A continuación, la aplicación elige el evento adecuado que se usará en función del contexto de la acción. Windows mensajes del mouse funcionan bien para señalar y seleccionar actividades, y debe usarlos para actividades que implican la interacción con elementos de la interfaz de usuario (UI). Los eventos de lápiz funcionan bien para la aplicación de entrada de lápiz en tiempo real, las acciones de lápiz y la escritura a mano.

> [!Note]  
> Tanto los eventos de lápiz como los mensajes del mouse se envían a una aplicación, independientemente de si se usa el lápiz o el mouse.

 

## <a name="distinguishing-pen-input-from-mouse-and-touch"></a>Distinguir la entrada de lápiz del mouse y la entrada táctil

Cuando la aplicación recibe un mensaje del mouse (como WM LBUTTONDOWN), puede llamar a la función \_ [**GetMessageExtraInfo**](/windows/win32/api/winuser/nf-winuser-getmessageextrainfo) para evaluar si el mensaje se originó en un lápiz o un dispositivo del mouse.

El valor devuelto por [**GetMessageExtraInfo**](/windows/win32/api/winuser/nf-winuser-getmessageextrainfo) debe comprobarse con máscara en 0xFFFFFF00 y, a continuación, se debe comparar con 0xFF515700. Las siguientes definiciones pueden hacer esto más claro:


```C++
#define MI_WP_SIGNATURE<entity type="nbsp"/> 0xFF515700
#define SIGNATURE_MASK<entity type="nbsp"/><entity type="nbsp"/> 0xFFFFFF00
#define IsPenEvent(dw)<entity type="nbsp"/><entity type="nbsp"/> (((dw) & SIGNATURE_MASK) == MI_WP_SIGNATURE
```



Si la comparación es verdadera, este mensaje del mouse se generó mediante un lápiz de Tablet PC o una pantalla táctil. En todos los demás casos, puede suponer que este mensaje lo generó un dispositivo del mouse.

Los 8 bits inferiores devueltos [**por GetMessageExtraInfo**](/windows/win32/api/winuser/nf-winuser-getmessageextrainfo) son variables. De esos bits, 7 (los 7 inferiores, enmascarados por 0x7F) se usan para representar el identificador del cursor, cero para el mouse o un valor de variable para el identificador del lápiz. Además, en Windows Vista, el octavo bit, enmascarado por 0x80, se usa para diferenciar la entrada táctil de la entrada de lápiz (0 = lápiz, 1 = entrada táctil).

## <a name="supported-system-gestures"></a>Gestos del sistema admitidos

En la tabla siguiente se enumeran los gestos del sistema incluidos actualmente en Windows XP Tablet PC Edition, se detallan las acciones de lápiz correspondientes y los eventos del sistema, y se muestra cómo se relacionan con las acciones tradicionales del mouse.



| Gesto de lápiz                                  | Acción del mouse                                                    | Descripción del gesto del lápiz                                                                                                                                                                                                             | Mensajes de evento                                                                                                                       | Mensajes del mouse                                                                                                                        | Comportamientos en Windows aplicaciones basadas en aplicaciones                                                                                                                                          |
|----------------------------------------------|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Pulsar<br/>                               | Clic con el botón izquierdo<br/>                                           | Pulse una vez en la pantalla con el lápiz.<br/>                                                                                                                                                                                        | ISG \_ TAP se envía cuando se eleva el lápiz.<br/>                                                                                         | WM \_ LBUTTONDOWN y WM \_ LBUTTONUP se envían cuando se eleva el lápiz.<br/>                                                                    | Elija el comando en el menú o la barra de herramientas, tome medidas si el comando ha elegido, establezca el punto de inserción (IP) y muestre los comentarios de selección.<br/>                                                |
| Presionar dos veces<br/>                        | Doble clic<br/>                                         | Pulse la pantalla dos veces en sucesión rápida.<br/>                                                                                                                                                                                    | ISG \_ DOUBLETAP enviado en la segunda pulsación (abajo). Evento TAP de ISG \_ enviado en la primera pulsación.<br/>                                           | WM \_ LBUTTONDBLCLK enviado en la segunda pulsación (abajo). WM \_ LBUTTONDOWN y WM \_ LBUTTONUP se envían en la primera pulsación (arriba) como para una sola pulsación.<br/> | Seleccione word, abra el archivo o la carpeta.<br/>                                                                                                                                     |
| Pulsar y sostener<br/>                    | Haga clic con el botón secundario en<br/>                                          | Pulse la pantalla y mantenga presionado hasta que aparezca un icono del mouse y, a continuación, mueva el lápiz para mostrar un menú contextual. Una aplicación podría optar por realizar una acción diferente de mostrar un menú contextual cuando se eleva el lápiz.<br/> | ISG \_ HOLDENTER se envía cuando el lápiz ha estado lo suficientemente abajo. ISG \_ RIGHTTAP se envía cuando se eleva el lápiz y se hace clic con el botón derecho.<br/> | WM \_ RBUTTONDOWN y WM RBUTTONUP se envían cuando se hace clic con el botón derecho (cuando se eleva \_ el lápiz).<br/>                                       | Mostrar menú contextual.<br/>                                                                                                                                                   |
| Hold-through<br/>                      | Clic con el botón izquierdo<br/>                                           | Pulse la pantalla y mantenga presionado hasta que aparezca el icono del mouse y desaparezca. Es probable que los usuarios lo hagan cuando presionan y mantienen presionado el número de accidentes, y quieren volver a pulsar.<br/>                                                 | ISG \_ TAP se envía cuando se eleva el lápiz.<br/>                                                                                         | WM \_ LBUTTONDOWN y WM \_ LBUTTONUP se envían cuando se eleva el lápiz.<br/>                                                                 | Haga clic con el botón izquierdo durante mucho tiempo. No existe ningún equivalente del mouse. Se trata de una reserva para cuando un usuario realiza operaciones de presión y retención durante mucho tiempo. El evento vuelve a ser una pulsación.<br/> |
| Arrastrar<br/>                              | Arrastrar a la izquierda<br/>                                            | Pulse en la pantalla para seleccionar el objeto que se va a mover y, a continuación, arrastre después de seleccionar el objeto.<br/>                                                                                                                     | ISG \_ DRAG enviado cuando se inicia la arrastre.<br/>                                                                                          | WM LBUTTONDOWN se envía cuando se inicia la arrastre, seguido de una serie de mensajes de movimiento del mouse y seguido de un \_ evento \_ WM LBUTTONUP.<br/> | Arrastre y seleccione, como en Microsoft Word al empezar con una dirección IP; seleccionar varias palabras; arrastrar, como al arrastrar un objeto en Windows; Desplazamiento.<br/>                            |
| Mantenga presionado seguido de un arrastre.<br/> | Arrastrar con el botón derecho<br/>                                           | Pulse en la pantalla para seleccionar el objeto que se va a mover. Mantenga presionado hasta que aparezca el icono del mouse y, a continuación, arrastre para mover el objeto. Eleva el lápiz para mostrar un menú contextual.<br/>                                                   | ISG \_ HOLDENTER se envía cuando el lápiz ha estado sin escribir durante algún tiempo. ISG \_ RIGHTDRAG enviado cuando se inicia la arrastre.<br/>                           | WM RBUTTONDOWN se envía cuando se inicia la arrastre, seguido de una serie de mensajes de movimiento del \_ mouse, seguidos de un evento \_ WM RBUTTONUP.<br/>     | Arrastrar, como al arrastrar un objeto o selección seguido de un menú contextual.<br/>                                                                                             |
| Mantener el puntero del lápiz<br/>                         | Mantener el mouse sobre el mouse<br/>                                          | Mantenga el lápiz estable a una distancia pequeña de la pantalla.<br/>                                                                                                                                                                 | Evento HOVERENTER de ISG \_ enviado inicialmente. Cuando se completa el intervalo de desplazamiento, se \_ envía ISG HOVERLEAVEis.<br/>                           | Ningún mensaje del mouse equivalente.<br/>                                                                                               | Mostrar información sobre herramientas, efectos de reversión y otros comportamientos del mouse.<br/>                                                                                                     |
| Agite en el aire<br/>                      | Mostrar **panel de entrada de Tablet PC**. Ningún equivalente del mouse.<br/> | Mueva el lápiz rápidamente de lado a lado, manteniendo la propina anterior, pero dentro del intervalo de la pantalla.<br/>                                                                                                                          | El evento no se pasa a la aplicación.<br/>                                                                                   | Ningún mensaje del mouse equivalente.<br/>                                                                                               | Nuevo, específico de Tablet PC.<br/>                                                                                                                                           |



 

## <a name="specifying-stylus-and-touch-interactions"></a>Especificación de interacciones táctiles y de lápiz

De forma predeterminada, la ventana recibirá todos los eventos de gesto del sistema y usará el modelo de interacción predeterminado. Algunas partes de este modelo pueden interferir con la aplicación, por lo que puede deshabilitarlas de forma selectiva respondiendo al mensaje [**WM \_ TABLET \_ QUERYSYSTEMGESTURESTATUS**](wm-tablet-querysystemgesturestatus-message.md) en WndProc.

 

 
