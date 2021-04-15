---
description: Windows Vista incluye un conjunto de ocho gestos básicos de gestos. Los gestos son movimientos de lápiz rápidos y lineales asociados a acciones y comandos de desplazamiento.
ms.assetid: 004c7d76-90a9-4506-a70b-dbf8f9e1c616
title: Gestos de gestos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f85d519f47b265779741b2f98fcb1b2f5d69df5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104554798"
---
# <a name="flicks-gestures"></a>Gestos de gestos

Windows Vista incluye un conjunto de ocho *gestos básicos de gestos*. Los gestos son movimientos de lápiz rápidos y lineales asociados a acciones y comandos de desplazamiento.

## <a name="flick-details"></a>Detalles de los gestos

La característica de gestos proporciona al usuario una nueva forma de interactuar con Tablet PC al permitir que se realicen acciones comunes realizando gestos rápidos con el lápiz. Los gestos coexisten con y no interrumpen las acciones normales del usuario, como los grifos de izquierda y derecha, el desplazamiento y la entrada de lápiz.

Un *gesto* es un gesto de lápiz unidireccional que requiere que el usuario se ponga en contacto con el digitalizador en un movimiento de gesto rápido. Un gesto se caracteriza por alta velocidad y un alto grado de recta. Un gesto se identifica por su dirección. Los gestos se pueden realizar en ocho direcciones correspondientes a las direcciones de brújula cardinal y secundaria.

Una acción de *acción* o *gesto* es la acción o el acceso directo que se realiza en respuesta a un gesto. Los gestos se asignan a acciones. En la ilustración siguiente se muestra un diagrama de ocho gestos de lápiz que corresponden a sus acciones de gesto.

![Ilustración que muestra el mapa de gestos](images/2647eb2d-36d0-4610-b923-fa3530d1e640.jpg)

Cuando el usuario mueve el lápiz sobre el digitalizador de un Tablet PC, el hardware genera paquetes de lápiz que se enrutan al subsistema de entrada manuscrita de la plataforma de Tablet PC. Normalmente, si el lápiz se usa como sustituto del mouse, el subsistema de entrada del lápiz toma estos paquetes de lápiz y los envía, posiblemente con modificaciones, a user32, el componente de Windows responsable de procesar la entrada del mouse. Si el lápiz se usa en una superficie de entrada manuscrita, se representa la entrada de lápiz en lugar de los paquetes de mouse que se generan.

La rutina de detección de gestos se implementa en el subsistema de entrada del lápiz. La detección de gestos comienza en el lápiz y continúa hasta:

1) la secuencia de paquetes recibidos se determina que no es un gesto o

2) se produce un seguimiento.

Mientras se está produciendo la detección de gestos, los paquetes de lápiz se retienen y no se envían al sistema. Esto debe hacerse porque el envío de paquetes puede interferir con la acción de gesto que se realiza. Por ejemplo, el envío de paquetes durante un gesto que se asigna a una acción de copia descartaría lo que se ha seleccionado, lo que significa que no hay nada que copiar en el momento en que se envió la acción.

A medida que los paquetes fluyen en el subsistema de entrada del lápiz, la rutina de detección de gestos calcula las métricas en la longitud, velocidad, tiempo y curvatura del movimiento que se está realizando. Con cada paquete que llega, la rutina de detección actualiza cada una de estas métricas. En cuanto cualquiera de las métricas queda fuera de lo que constituye un gesto, la detección de gestos finaliza y los paquetes se envían a través de.

## <a name="where-flicks-are-detected"></a>Dónde se detectan los gestos

Los gestos de gestos se hacen posibles por el hecho de que los arrastres se suelen realizar con bastante lentitud. En primer lugar, el usuario debe tener como destino el punto inicial del arrastre, realizar el arrastre y, a continuación, destinarlo al extremo. Normalmente, esto tardará demasiado en calificarse como un gesto. Sin embargo, en las superficies de entrada manuscrita los trazos rápidos que se calificarían como gestos se producen con frecuencia; cruzar un ' t ' es un ejemplo común. Por lo tanto, de forma predeterminada, la detección de gestos se desactiva sobre las superficies de entrada manuscrita y se activa en todo el sistema.

## <a name="focus-issues"></a>Problemas de foco

Una vez detectado un gesto, comienza una secuencia de eventos que, en última instancia, conduce al sistema realizando una acción determinada en respuesta al gesto que se ha producido. En primer lugar, la rutina de detección dentro del subsistema de entrada del lápiz determina a qué ventana se debe enviar el gesto. Suele ser la ventana que tiene el foco, pero hay excepciones. En el caso de los gestos de desplazamiento, el gesto se envía a la ventana en la que se produjo el gesto. Tenga en cuenta que esto no es necesariamente la ventana que tiene el foco. Cuando se envía un gesto a una ventana que no tiene el foco, el foco no cambia a esa ventana.

## <a name="flick-actions"></a>Acciones de gesto

Una vez que se determina la ventana de destino, esa ventana puede controlar el propio gesto en función del comportamiento de los eventos predeterminados o programados. Las aplicaciones pueden responder a la acción más adecuada en función de la aplicación y la dirección y posición del gesto. Por ejemplo, en una aplicación de asignación, los gestos de arriba y abajo pueden acercar o alejar en lugar de desplazarse verticalmente, como cabría esperar del comportamiento predeterminado.

Para avisar a una aplicación de que se ha producido un gesto, se le envía un mensaje de ventana. Este mensaje de ventana contiene tanto el punto de inicio del gesto como la dirección del gesto. Si la aplicación controla este mensaje de ventana, no se lleva a cabo ninguna otra acción por parte del subsistema de entrada manuscrita.

Una vez detectado un gesto, en la pantalla se muestra información visual que representa la acción de gesto. Estos comentarios sirven para dos propósitos. En primer lugar, confirma que el usuario ha realizado correctamente el gesto. En segundo lugar, recuerda al usuario qué acción se ha realizado, lo que ayuda al usuario a conectar la dirección del gesto con su acción asociada.

Los comentarios de gestos se componen de dos partes: un icono que representa la acción y una etiqueta que contiene el nombre de la acción. La etiqueta se muestra debajo del icono. Los comentarios se muestran inmediatamente después de que se detecta el gesto. Aunque las aplicaciones pueden personalizar su comportamiento en respuesta a los gestos controlando el mensaje de la ventana de gestos, la aplicación no puede deshabilitar o modificar los comentarios de gestos.

Se espera que la mayoría de las aplicaciones no tengan en cuenta los gestos y, por tanto, no controlarán el mensaje de ventana descrito anteriormente. Si no se controla el mensaje, el subsistema de entrada del lápiz realizará una acción posterior. En primer lugar, busca la acción asociada con la dirección del gesto detectado. Después, realizará los pasos (descritos en la tabla siguiente) para hacer que la ventana de destino realice esta acción. Para muchas de las acciones de gestos esto implica el envío de un comando de aplicación, pero algunas acciones que se implementan no.

## <a name="processing-application-commands"></a>Procesar comandos de la aplicación

La aplicación debe responder a cualquiera de los comandos de la aplicación que podrían asignarse potencialmente a un gesto de gestos. Si una aplicación no puede responder al [**mensaje de \_ \_ gestos de Tablet PC de WM**](wm-tablet-flick-message.md), Windows Vista realiza un seguimiento mediante el envío de la notificación de [**WM \_ APPCOMMAND**](/windows/desktop/inputdev/wm-appcommand) aplicable, seguida de una notificación [**\_ KEYDOWN de WM**](/windows/desktop/inputdev/wm-keydown) .

A continuación se muestra una lista de los comandos de la aplicación que se pueden asignar a los gestos, con el mensaje de pulsación de la copia de seguridad que se puede enviar.



| Get-Help                                  | Pulsación de seguridad  |
|------------------------------------------|-------------------|
| APPCOMMAND \_ explorador \_ hacia atrás<br/> | None<br/>   |
| APPCOMMAND el \_ explorador \_ hacia delante<br/>  | None<br/>   |
| copia de APPCOMMAND \_<br/>              | Ctrl+C<br/> |
| APPCOMMAND \_ pegar<br/>             | Ctrl+V<br/> |
| deshacer APPCOMMAND \_<br/>              | Ctrl+Z<br/> |
| APPCOMMAND \_ eliminar<br/>            | Supr<br/>    |
| APPCOMMAND \_ cortar<br/>               | Ctrl+X<br/> |
| APPCOMMAND \_ abrir<br/>              | Ctrl+O<br/> |
| APPCOMMAND \_ Imprimir<br/>             | Ctrl+P<br/> |
| APPCOMMAND \_ Guardar<br/>              | Ctrl+S<br/> |
| rehacer APPCOMMAND \_<br/>              | Ctrl+Y<br/> |
| APPCOMMAND \_ cerrar<br/>             |                   |



 

Los comandos de edición como copiar, pegar, cortar y eliminar pueden dirigirse contra una selección o con el objeto situado en la base del gesto de gestos. Si no hay ninguna selección, puede usar los datos de la [**estructura de \_ punto de gesto**](/windows/desktop/api/tabflicks/ns-tabflicks-flick_point) para determinar qué objeto, si existe, podría haber sido el destino del comando de edición.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de la API de gestos](flicks-api-reference.md)
</dt> <dt>

[Responder a gestos de gestos](/previous-versions//dd356077(v=vs.85))
</dt> </dl>

 

