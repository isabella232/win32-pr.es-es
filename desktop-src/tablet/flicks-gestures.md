---
description: Windows Vista incluye un conjunto de ocho gestos de gestos básicos. Los gestos son movimientos de lápiz rápidos y lineales asociados a acciones y comandos de desplazamiento.
ms.assetid: 004c7d76-90a9-4506-a70b-dbf8f9e1c616
title: Gestos de gestos de gestos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f85d519f47b265779741b2f98fcb1b2f5d69df5b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360315"
---
# <a name="flicks-gestures"></a>Gestos de gestos de gestos

Windows Vista incluye un conjunto de ocho *gestos de gestos de gestos básicos.* Los gestos son movimientos de lápiz rápidos y lineales asociados a acciones y comandos de desplazamiento.

## <a name="flick-details"></a>Detalles de flick

La característica de gestos proporciona al usuario una nueva manera de interactuar con tablet PC, ya que permite realizar acciones comunes mediante gestos rápidos con el lápiz. Los gestos coexisten y no interrumpen las acciones normales del usuario, como pulsar a la izquierda y a la derecha, desplazarse e invocar.

Un *gesto de gesto* de gesto de lápiz unidireccional que requiere que el usuario se pondrá en contacto con el digitalizador en un movimiento rápido. Un gesto se caracteriza por una alta velocidad y un alto grado de recta. Un gesto se identifica por su dirección. Los gestos se pueden realizar en ocho direcciones correspondientes a las direcciones cardinal y secundaria de la brújula.

Una *acción* o *acción de gesto es* la acción o el acceso directo que se realiza en respuesta a un gesto. Los gestos se asignan a acciones. En la ilustración siguiente se muestra un diagrama de ocho gestos de lápiz que corresponden a sus acciones de gesto.

![ilustración que muestra el mapa de gestos](images/2647eb2d-36d0-4610-b923-fa3530d1e640.jpg)

A medida que el usuario mueve el lápiz sobre el digitalizador de un tablet PC, el hardware genera paquetes de lápiz que se enruta al subsistema de entrada de lápiz de la plataforma tablet PC. Normalmente, si el lápiz se usa como sustituto del mouse, el subsistema de entrada de lápiz toma estos paquetes de lápiz y los envía, posiblemente con modificaciones, al componente Windows responsable de procesar la entrada del mouse. Si el lápiz se usa en una superficie de entrada manuscrita, se representa la entrada manuscrita en lugar de los paquetes del mouse que se generan.

La rutina de detección de gestos se implementa en el subsistema de entrada de lápiz. La detección de gestos comienza en el pen-down y continúa hasta que:

1) la secuencia de paquetes recibidos se determina que no es un gesto o

2) se produce un pen-up.

Mientras se produce la detección de gestos, los paquetes de lápiz se retenen y no se envían al sistema. Esto debe hacerse porque el envío de paquetes puede interferir con la acción de gesto que se realiza. Por ejemplo, el envío de paquetes durante un gesto que se asigna a una acción de copia descartaría lo que se seleccionó, lo que significa que no habría nada que copiar en el momento en que se envió la acción.

A medida que los paquetes fluyen al subsistema de entrada de lápiz, la rutina de detección de gestos calcula las métricas sobre la longitud, la velocidad, el tiempo y la curva del movimiento que se realiza. Con cada paquete que llega, la rutina de detección actualiza cada una de estas métricas. En cuanto cualquiera de las métricas queda fuera de lo que constituiría un gesto, la detección de gestos finaliza y los paquetes se envían a través de .

## <a name="where-flicks-are-detected"></a>Dónde se detectan los gestos

Los gestos de gestos de gestos se hacen posibles por el hecho de que los arrastres se realizan normalmente con bastante lentitud. El usuario debe dirigirse primero al punto inicial del arrastre, realizar el arrastre y, a continuación, dirigirse al punto final. Normalmente, esto puede tardar demasiado tiempo en calificarse como un gesto. Sin embargo, al invocar superficies, los trazos rápidos que se calificarían como gestos se suceden con frecuencia. cruzar un 't' es un ejemplo común. Por lo tanto, de forma predeterminada, la detección de gestos se apaga sobre las superficies de entrada de entrada y se activa en todo el sistema.

## <a name="focus-issues"></a>Problemas de foco

Una vez detectado un gesto, comienza una secuencia de eventos que, en última instancia, conduce al sistema a realizar una acción determinada en respuesta al gesto que se produjo. En primer lugar, la rutina de detección dentro del subsistema de entrada de lápiz determina a qué ventana se debe enviar el gesto. Suele ser la ventana que tiene el foco, pero hay excepciones. Para los gestos de desplazamiento, el gesto se envía a la ventana en la que se produjo el gesto. Tenga en cuenta que esta no es necesariamente la ventana con el foco. Cuando se envía un gesto a una ventana que no tiene el foco, el foco no cambia a esa ventana.

## <a name="flick-actions"></a>Acciones de gesto

Una vez que se determina la ventana de destino, esa ventana puede controlar el gesto en función del comportamiento de evento predeterminado o programado. Las aplicaciones pueden responder a la acción más adecuada en función de la aplicación y la dirección y la posición del gesto. Por ejemplo, en una aplicación de asignación, los gestos de subir y bajar podrían acercar o alejar en lugar de desplazarse verticalmente, como se esperaría del comportamiento predeterminado.

Para alertar a una aplicación de que se ha producido un gesto, se le envía un mensaje de ventana. Este mensaje de ventana contiene el punto inicial del gesto y la dirección del gesto. Si la aplicación controla este mensaje de ventana, el subsistema de entrada de lápiz no toma ninguna otra acción.

Una vez detectado un gesto, los comentarios visuales que representan la acción de gesto se muestran en la pantalla. Estos comentarios tienen dos propósitos. En primer lugar, confirma para el usuario que el gesto se ha realizado correctamente. En segundo lugar, recuerda al usuario qué acción se realizó, lo que ayuda al usuario a conectar la dirección del gesto con su acción asociada.

Los comentarios de gestos constan de dos partes; un icono que representa la acción y una etiqueta que contiene el nombre de la acción. La etiqueta se muestra debajo del icono. Los comentarios se muestran inmediatamente después de detectar el gesto. Aunque las aplicaciones pueden personalizar su comportamiento en respuesta a los gestos controlando el mensaje de la ventana de gestos, la aplicación no puede deshabilitar ni modificar los comentarios de los gestos.

Se espera que la mayoría de las aplicaciones no sean conscientes de los gestos y, por tanto, no controlarán el mensaje de ventana descrito anteriormente. Si no se controla el mensaje, el subsistema de entrada de lápiz realizará una acción adicional. En primer lugar, busca la acción asociada a la dirección del gesto detectado. A continuación, se realizarán los pasos (descritos en la tabla siguiente) para que la ventana de destino realice esta acción. Para muchas de las acciones de gestos, esto implica el envío de un comando de aplicación, pero determinadas acciones que se implementan no.

## <a name="processing-application-commands"></a>Procesar comandos de aplicación

La aplicación debe responder a cualquiera de los comandos de aplicación que podrían asignarse a un gesto de gesto de gesto. Si una aplicación no responde al mensaje [**WM \_ TABLET \_ FLICK**](wm-tablet-flick-message.md), Windows Vista realiza el seguimiento mediante el envío de la notificación [**\_ APPCOMMAND**](/windows/desktop/inputdev/wm-appcommand) de WM aplicable, seguida de una notificación [**WM \_ KEYDOWN.**](/windows/desktop/inputdev/wm-keydown)

A continuación se muestra una lista de comandos de aplicación que se pueden asignar a los gestos, con el mensaje de pulsación de tecla de copia de seguridad que se podría enviar.



| Comando                                  | Pulsación de tecla de copia de seguridad  |
|------------------------------------------|-------------------|
| APPCOMMAND \_ BROWSER \_ BACKWARD<br/> | None<br/>   |
| APPCOMMAND \_ BROWSER \_ FORWARD<br/>  | None<br/>   |
| COPIA DE \_ APPCOMMAND<br/>              | Ctrl+C<br/> |
| APPCOMMAND \_ PASTE<br/>             | Ctrl+V<br/> |
| APPCOMMAND \_ UNDO<br/>              | Ctrl+Z<br/> |
| APPCOMMAND \_ DELETE<br/>            | Supr<br/>    |
| APPCOMMAND \_ CUT<br/>               | Ctrl+X<br/> |
| APPCOMMAND \_ OPEN<br/>              | Ctrl+O<br/> |
| APPCOMMAND \_ PRINT<br/>             | Ctrl+P<br/> |
| APPCOMMAND \_ SAVE<br/>              | Ctrl+S<br/> |
| APPCOMMAND \_ REDO<br/>              | Ctrl+Y<br/> |
| APPCOMMAND \_ CLOSE<br/>             |                   |



 

Los comandos de edición, como Copiar, Pegar, Cortar y Eliminar, pueden dirigirse a una selección o al objeto ubicado en la base del gesto de gesto. Si no hay ninguna selección, puede usar los datos de la estructura [**FLICK \_ POINT**](/windows/desktop/api/tabflicks/ns-tabflicks-flick_point) para determinar cuál, si existe, el objeto podría haber sido el destino del comando de edición.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de LA API de Flicks](flicks-api-reference.md)
</dt> <dt>

[Respuesta a gestos de gesto](/previous-versions//dd356077(v=vs.85))
</dt> </dl>

 

