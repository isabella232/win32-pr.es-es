---
description: La aplicación incorpora un diseño y uso óptimos del lápiz de Tablet PC mediante el envío de mensajes de mouse de Microsoft Windows y eventos del sistema.
ms.assetid: ccd45b68-f037-43da-a7d0-1df9439afd11
title: Eventos del sistema y mensajes del mouse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45c068e30db6ca1a85429667e2a8f1f93c505299
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678488"
---
# <a name="system-events-and-mouse-messages"></a>Eventos del sistema y mensajes del mouse

La aplicación incorpora un diseño y uso óptimos del lápiz de Tablet PC mediante el envío de mensajes de mouse de Microsoft Windows y eventos del sistema. Las aplicaciones reciben ambos conjuntos de eventos para cada acción o movimiento del lápiz. A continuación, la aplicación elige el evento adecuado para usarlo en función del contexto de la acción. Los mensajes del mouse de Windows funcionan bien para señalar y seleccionar actividades, y deben usarse para actividades que impliquen interacción con los elementos de la interfaz de usuario (IU). Los eventos de lápiz funcionan bien para la aplicación de tinta en tiempo real, las acciones del lápiz y la escritura a mano.

> [!Note]  
> Los eventos de lápiz y los mensajes del mouse se envían a una aplicación, independientemente de si se usa el lápiz o el mouse.

 

## <a name="distinguishing-pen-input-from-mouse-and-touch"></a>Distinguir la entrada manuscrita de mouse y Touch

Cuando la aplicación recibe un mensaje de mouse (como WM \_ LBUTTONDOWN), puede llamar a la función [**GetMessageExtraInfo**](/windows/win32/api/winuser/nf-winuser-getmessageextrainfo) para evaluar si el mensaje se originó en un lápiz o un dispositivo de mouse.

El valor devuelto de [**GetMessageExtraInfo**](/windows/win32/api/winuser/nf-winuser-getmessageextrainfo) debe estar marcado con máscara en 0xFFFFFF00 y, a continuación, compararse con 0xFF515700. Las siguientes definiciones pueden ser más claras:


```C++
#define MI_WP_SIGNATURE<entity type="nbsp"/> 0xFF515700
#define SIGNATURE_MASK<entity type="nbsp"/><entity type="nbsp"/> 0xFFFFFF00
#define IsPenEvent(dw)<entity type="nbsp"/><entity type="nbsp"/> (((dw) & SIGNATURE_MASK) == MI_WP_SIGNATURE
```



Si la comparación es verdadera, este mensaje del mouse lo generó un lápiz de Tablet PC o una pantalla táctil. En todos los demás casos, puede suponer que este mensaje fue generado por un dispositivo de mouse.

Los 8 bits inferiores devueltos de [**GetMessageExtraInfo**](/windows/win32/api/winuser/nf-winuser-getmessageextrainfo) son variables. De esos bits, 7 (el 7 inferior, enmascarado por 0x7F) se usa para representar el identificador de cursor, cero para el mouse o un valor de variable para el ID. de lápiz. Además, en Windows Vista, el octavo bit, enmascarado por 0x80, se usa para diferenciar la entrada táctil de la entrada manuscrita (0 = PEN, 1 = Touch).

## <a name="supported-system-gestures"></a>Gestos del sistema admitidos

En la tabla siguiente se enumeran los gestos del sistema incluidos actualmente en Windows XP Tablet PC Edition, se detallan las acciones del lápiz y los eventos del sistema correspondientes, y se muestra cómo se relacionan con las acciones tradicionales del mouse.



| Movimiento del lápiz                                  | Acción del mouse                                                    | Descripción del gesto del lápiz                                                                                                                                                                                                             | Mensajes de eventos                                                                                                                       | Mensajes del mouse                                                                                                                        | Comportamientos en aplicaciones basadas en Windows                                                                                                                                          |
|----------------------------------------------|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Pulsar<br/>                               | Clic con el botón izquierdo<br/>                                           | Puntee en la pantalla una vez con el lápiz.<br/>                                                                                                                                                                                        | ISG \_ TAP se envía cuando se levanta el lápiz.<br/>                                                                                         | WM \_ LBUTTONDOWN y WM \_ LBUTTONUP se envían al levantar el lápiz.<br/>                                                                    | Elija comando desde el menú o la barra de herramientas, tomar medidas si elige comando, establecer punto de inserción (IP) y mostrar comentarios de selección.<br/>                                                |
| Presionar dos veces<br/>                        | Doble clic<br/>                                         | Puntee en pantalla dos veces en rápida sucesión.<br/>                                                                                                                                                                                    | ISG \_ DOUBLETAP enviado en la segunda pulsación (Down). \_Evento TAP de ISG enviado en el primer punteo.<br/>                                           | WM \_ LBUTTONDBLCLK enviado en la segunda pulsación (Down). WM \_ LBUTTONDOWN y WM \_ LBUTTONUP envían el primer punteo (up) como para una sola derivación.<br/> | Seleccione Word, abrir archivo o carpeta.<br/>                                                                                                                                     |
| Pulsar y sostener<br/>                    | Haga clic con el botón secundario en<br/>                                          | Puntee en la pantalla y manténgala hasta que aparezca un icono del mouse y, a continuación, levante el lápiz para mostrar un menú contextual. Una aplicación podría elegir realizar una acción diferente de mostrar un menú contextual cuando se levanta el lápiz.<br/> | ISG \_ HOLDENTER se envía cuando el lápiz está inactivo durante el tiempo suficiente. ISG \_ RIGHTTAP se envía cuando se levanta el lápiz y se produce un clic con el botón secundario.<br/> | WM \_ RBUTTONDOWN y WM \_ RBUTTONUP se envían cuando se produce un clic con el botón derecho (cuando se levanta el lápiz).<br/>                                       | Mostrar menú contextual.<br/>                                                                                                                                                   |
| Tiempo de espera<br/>                      | Clic con el botón izquierdo<br/>                                           | Puntee en la pantalla y manténgala hasta que aparezca el icono del mouse y desaparezca. Es probable que los usuarios realicen esta tarea cuando produzcan un error en el recuento de esperas y se mantenga presionado y quiera revertir a tocar.<br/>                                                 | ISG \_ TAP se envía cuando se levanta el lápiz.<br/>                                                                                         | WM \_ LBUTTONDOWN y WM \_ LBUTTONUP envían cuando se levanta el lápiz.<br/>                                                                 | Haga clic con el botón primario durante mucho tiempo. No existe ningún equivalente del mouse. Se trata de una reserva para cuando un usuario realiza las operaciones de mantener presionado durante mucho tiempo. El evento vuelve a ser una derivación.<br/> |
| Arrastrar<br/>                              | Arrastrar a la izquierda<br/>                                            | Puntee en la pantalla para seleccionar el objeto que se va a desplace y, a continuación, arrastre después de seleccionar el objeto.<br/>                                                                                                                     | ISG \_ : arrastre se envía cuando se inicia la acción de arrastrar.<br/>                                                                                          | WM \_ LBUTTONDOWN se envía cuando se inicia la acción de arrastrar, seguido de una serie de mensajes de movimiento del mouse y seguido de un \_ evento LBUTTONUP de WM.<br/> | Arrastrar y seleccionar, como en Microsoft Word al comenzar con una dirección IP; seleccionar varias palabras; arrastrar, como cuando se arrastra un objeto en Windows; desplazamiento.<br/>                            |
| Mantener presionado seguido de un arrastre<br/> | Arrastrar a la derecha<br/>                                           | Puntee en la pantalla para seleccionar el objeto que se va a desplace. Espere hasta que aparezca el icono del mouse y, a continuación, arrastre para desplace el objeto. Levante el lápiz para mostrar un menú contextual.<br/>                                                   | ISG \_ HOLDENTER se envía cuando el lápiz está inactivo durante algún tiempo. ISG \_ RIGHTDRAG se envía cuando se inicia la acción de arrastrar.<br/>                           | WM \_ RBUTTONDOWN se envía cuando se inicia la acción de arrastrar, seguido de una serie de mensajes de movimiento del mouse, seguidos de un \_ evento RBUTTONUP de WM.<br/>     | Arrastre, como al arrastrar un objeto o una selección, seguido de un menú contextual.<br/>                                                                                             |
| Mantener el lápiz<br/>                         | Mantener el mouse<br/>                                          | Sostenga el lápiz a una distancia pequeña de la pantalla.<br/>                                                                                                                                                                 | El \_ evento ISG HOVERENTER se envió inicialmente. Cuando se completa el intervalo de activación, se \_ envía ISG HOVERLEAVEis.<br/>                           | Ningún mensaje de mouse equivalente.<br/>                                                                                               | Mostrar información sobre herramientas, efectos de desplazamiento y otros comportamientos de desplazamiento del mouse.<br/>                                                                                                     |
| Sacudida en el aire<br/>                      | Mostrar el **Panel de entrada de Tablet PC**. Sin equivalentes del mouse.<br/> | Mueva el lápiz rápidamente de lado a lado, manteniendo presionada la punta, pero dentro del intervalo de la pantalla.<br/>                                                                                                                          | El evento no se pasa a la aplicación.<br/>                                                                                   | Ningún mensaje de mouse equivalente.<br/>                                                                                               | Nuevo, específico de Tablet PC.<br/>                                                                                                                                           |



 

## <a name="specifying-stylus-and-touch-interactions"></a>Especificar interacciones táctiles y de lápiz

De forma predeterminada, la ventana recibirá todos los eventos de gesto del sistema y usará el modelo de interacción predeterminado. Algunas partes de este modelo pueden interferir con la aplicación, por lo que puede deshabilitarlas de forma selectiva al responder al [**\_ mensaje de \_ QUERYSYSTEMGESTURESTATUS**](wm-tablet-querysystemgesturestatus-message.md) de la tableta de WM en el WndProc.

 

 
