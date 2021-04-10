---
title: Estados de agente
description: Estados de agente
ms.assetid: 8c3c5b12-81af-4ba5-b834-9f0a7ff5d075
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c371b1a2126129c03f16ce7fc7c2f95cca955a2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268431"
---
# <a name="agent-states"></a>Estados de agente

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

Los servicios de animación de agente de Microsoft reproducen automáticamente algunas animaciones. Por ejemplo, cuando se usan los comandos [**moveTo**](moveto-method.md) o [**GestureAt**](gestureat-method.md) , los servicios de animación reproducen una animación adecuada. Del mismo modo, después del tiempo de espera de inactividad, los servicios reproducen animaciones automáticamente. Para admitir estos Estados, puede definir animaciones adecuadas y, a continuación, asignarlas a los Estados. Todavía puede reproducir cualquier animación que defina directamente mediante el método [**Play**](play-method.md) , incluso si la asigna a un estado.

Puede asignar varias animaciones al mismo estado y los servicios de animación elegirán una de las animaciones de forma aleatoria. Esto permite que el personaje muestre una variedad mucho más natural en su comportamiento.

Aunque las animaciones que se asignan a los Estados pueden incluir fotogramas de bifurcación, evite animaciones de bucle (animaciones que se bifurcan siempre). De lo contrario, tendrá que usar el método [**Stop**](play-method.md) para poder reproducir otra animación.

Es importante definir y asignar al menos una animación para cada Estado que se produce para el carácter. Si no proporciona estas animaciones y asignaciones de estado, es posible que el carácter no parezca que se comporte correctamente al usuario. Sin embargo, si no se produce un estado para un carácter determinado, no es necesario asignar una animación a ese estado. Por ejemplo, si la aplicación host nunca llama al método [**moveTo**](moveto-method.md) , puede omitir la creación y asignación de animaciones de estado en **movimiento** .



| Estado              | Ejemplo de uso                                                                         |
|--------------------|----------------------------------------------------------------------------------------|
| **GesturingDown**  | Cuando se procesa el método de animación [**GestureAt**](gestureat-method.md) .          |
| **GesturingLeft**  | Cuando se procesa el método de animación [**GestureAt**](gestureat-method.md) .          |
| **GesturingRight** | Cuando se procesa el método de animación [**GestureAt**](gestureat-method.md) .          |
| **GesturingUp**    | Cuando se procesa el método de animación [**GestureAt**](gestureat-method.md) .          |
| **Oído**        | Cuando se detecta el inicio de la entrada oral.                                        |
| **Conde**         | Cuando el usuario o la aplicación ocultan el carácter.                                  |
| **IdlingLevel1**   | Cuando el carácter comienza el estado de **ralentí** .                                        |
| **IdlingLevel2**   | Cuando el carácter comienza el segundo estado de **ralentí** .                           |
| **IdlingLevel3**   | Cuando el carácter comienza el estado final del nivel de **ralentí** .                            |
| **Escucha**      | Cuando el carácter comienza a escuchar (el usuario presiona la tecla de acceso rápido entrada de voz). |
| **MovingDown**     | Cuando se procesa el método de animación [**moveTo**](moveto-method.md) .                |
| **MovingLeft**     | Cuando se procesa el método de animación [**moveTo**](moveto-method.md) .                |
| **MovingRight**    | Cuando se procesa el método de animación [**moveTo**](moveto-method.md) .                |
| **MovingUp**       | Cuando se procesa el método de animación [**moveTo**](moveto-method.md) .                |
| **Mostrando**        | Cuando el usuario o la aplicación muestren el carácter.                                  |
| **Habla**       | Cuando se procesa el método de animación [**Speak**](speak-method.md) .                  |



 

### <a name="the-hearing-and-listening-states"></a>Estados de audición y escucha

La animación que asigna al estado **escuchando** se reproduce cuando el usuario presiona la tecla de acceso de entrada de voz para la entrada de voz. Cree y asigne una animación corta que haga que el carácter mire Attentive. Del mismo modo, defina que la animación **devuelta** tenga una duración corta para que el carácter reproduzca la animación del estado de la **audición** cuando el usuario hable. Una animación del estado de la **audición** también debe ser breve y estar diseñada para que el usuario sepa que el carácter está escuchando activamente en lo que el usuario dice. Las inclinaciones de cabeza u otros gestos ligeros son adecuados. Para proporcionar variabilidad natural, proporcione varias animaciones de estado de **audición** .

### <a name="the-gesturing-states"></a>Estados de gesturing

Solo tiene que crear y asignar animaciones de estado de **gesturing** si tiene previsto usar el método [**GestureAt**](gestureat-method.md) . Las animaciones de estado **gesturing** se reproducen cuando el agente de Microsoft procesa una llamada al método **GestureAt** . Si define superposiciones de la boca para las animaciones de estado de **gesturing** , el carácter puede hablar como gestos.

Los servicios de animación determinan la ubicación del carácter y su relación con la ubicación de las coordenadas especificadas en el método y reproducen una animación adecuada. La dirección gesturing siempre es con respecto al carácter; por ejemplo, **GestureRight** debe ser un gesto en el derecho del carácter.

### <a name="the-showing-and-hiding-states"></a>Estados de mostrar y ocultar

Los Estados de **visualización** y **ocultación** reproducen las animaciones asignadas cuando el usuario o la aplicación host solicita Mostrar u ocultar el carácter. Estos Estados también establecen correctamente el estado **visible** del marco de caracteres. Al definir animaciones para estos Estados, tenga en cuenta que un carácter puede aparecer o desformar parte de cualquier ubicación de la pantalla. Dado que el usuario puede mostrar u ocultar cualquier carácter, admita siempre al menos una animación para estos Estados.

Las animaciones que se asignan al estado **que se muestra** normalmente finalizan con un marco que contiene la imagen de posición neutra del carácter. Por el contrario, **ocultar** las animaciones de estado normalmente comienza con la posición neutra. La **visualización** y **ocultación** de animaciones de estado pueden incluir un marco vacío al principio o al final, respectivamente, para proporcionar una transición desde el estado actual del carácter.

### <a name="the-idling-states"></a>Estados de ralentí

Los Estados de **ralentí** son progresivos. Los servicios de animación comienzan a usar las asignaciones de nivel 1 para el primer período de inactividad y usan las animaciones de nivel 2 para el segundo. Después, el ciclo inactivo progresa hasta el nivel 3 de las animaciones asignadas y permanece en este estado hasta que se cancela, como cuando comienza una nueva solicitud de animación.

Diseña animaciones para los Estados de **ralentí** para comunicar el estado del carácter, pero no para distraer al usuario. Las animaciones deberían reflejar correctamente la capacidad de respuesta del carácter en formas sutiles pero claras. Por ejemplo, glancing o parpadeo son buenas animaciones que se asignan al estado **IdlingLevel1** . Las animaciones de lectura funcionan bien con el estado **IdlingLevel2** . La suspensión o la escucha de música con auriculares son buenos ejemplos de animaciones que se asignan al estado **IdlingLevel3** . Las animaciones que incluyen muchos o grandes movimientos no se adaptan bien a las animaciones inactivas porque dibujan la atención del usuario. Dado que las animaciones de estado de **ralentí** se reproducen con frecuencia, proporcionan varias animaciones de estado de **ralentí** , especialmente para los Estados **IdlingLevel1** y **IdlingLevel2** .

Tenga en cuenta que una aplicación puede desactivar el procesamiento de inactividad automático para un carácter y administrar el estado de **ralentí** del carácter. Los Estados de **ralentí** del agente están diseñados para ayudarle a evitar cualquier situación en la que el carácter no tiene ninguna animación que reproducir. Una imagen de caracteres que no cambia después de un breve período de tiempo es como una aplicación que muestra un puntero de espera durante mucho tiempo, lo que resta de la sensación de increíble e interactividad. Mantener la ilusión no tarda mucho: a veces, solo un parpadeo animado, una respiración visible o un desplazamiento del cuerpo.

### <a name="the-speaking-state"></a>El estado hablando

Los servicios de animación usan el estado **hablando** cuando no se encuentra una animación de hablar para la animación actual. Asigne una animación de hablar simple a este estado. Por ejemplo, puede usar un solo fotograma compuesto por la posición neutra del carácter con superposiciones de la boca.

### <a name="the-moving-states"></a>Estados en movimiento

Los Estados **móviles** se reproducen cuando una aplicación llama al método [**moveTo**](moveto-method.md) . Los servicios de animación determinan la animación que se reproducirá en función de la ubicación actual del carácter y las coordenadas especificadas. La dirección del movimiento se basa en la posición del carácter. Por lo tanto, la animación que se asigna a la animación **MovingLeft** se debe basar en la izquierda del carácter. Si no usa el método **moveTo** , puede omitir la creación y asignación de una animación.

**Mover** las animaciones de Estado debe animar el carácter en su posición de movimiento. El último fotograma de esta animación se muestra cuando el fotograma del carácter se mueve en la pantalla. No se admite la animación del carácter mientras se mueve el marco.

### <a name="standard-animation-set"></a>Conjunto de animaciones estándar

Aunque puede diseñar un carácter personalizado para que tenga las animaciones que desea usar, el agente de Microsoft define un conjunto de animaciones estándar. Los caracteres que se ajustan a esta definición se pueden seleccionar como carácter predeterminado.

En la tabla siguiente se enumeran las animaciones incluidas en el conjunto de animaciones estándar. Incluso si va a crear un carácter personalizado, es posible que desee utilizar la lista como guía para diseñar sus propios caracteres. Los caracteres que admiten el conjunto de animaciones estándar deben admitir al menos las siguientes animaciones.



| Animación                        | Ejemplo de uso                                                                                           | Animación de ejemplo                                                                                                                                                                                                      |
|----------------------------------|----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Confirmación**                  | Cuando el carácter confirma la solicitud del usuario.                                                      | El carácter nodos o parpadea el gesto "Aceptar". Tenga en cuenta que esta animación debe devolver el carácter a su posición neutra.<br/>                                                                                  |
| **Alerta**<sup>1, 2</sup>          | Cuando el carácter está esperando instrucciones, normalmente se reproduce después de que el usuario activa el modo de escucha. | Caras de carácter frontal, respirar, parpadeo en ocasiones, pero con claridad en espera de instrucciones.                                                                                                                             |
| **Anuncio**<sup>1, 2</sup>       | Cuando el carácter ha encontrado información para el usuario.                                                   | Los gestos de caracteres elevan eyebrows y Handan o abren un sobre.                                                                                                                                                  |
| **Blink**                        | Cuando el carácter deja de hablar o está inactivo.                                                            | De forma natural, los ojos parpadean.                                                                                                                                                                                       |
| **Confundir**<sup>1, 2</sup>       | Cuando el carácter no comprenda lo que hay que hacer.                                                        | Encabezado de arañazos de caracteres.                                                                                                                                                                                              |
| **Felicitación**<sup>1, 2</sup>   | Cuando el carácter o el usuario completa una tarea (una forma más segura de la animación de **confirmación** ).          | El carácter realiza el gesto de felicitación, transmite "sí".                                                                                                                                                              |
| **Rechazar**<sup>1, 2</sup>        | Cuando el carácter no puede hacer ni rechazar la solicitud del usuario.                                             | El repasa el carácter Head, transmite "no puede hacerlo".                                                                                                                                                                            |
| **DoMagic1**                     | Carácter se prepara para mostrar algo.                                                                 | Olas de caracteres o mágicas.                                                                                                                                                                                         |
| **DoMagic2**                     | El carácter finaliza la presentación de algo.                                                                | El carácter finaliza el gesto mágico.                                                                                                                                                                                     |
| **DontRecognize**<sup>1, 2</sup>  | Cuando el carácter no reconoció la solicitud del usuario.                                                  | El carácter está disponible para auriculares.                                                                                                                                                                                           |
| **Explicación**<sup>1, 2</sup>        | Cuando el carácter explica algo al usuario.                                                       | Gestos de caracteres como si se explicara algo.                                                                                                                                                                         |
| **GestureDown**<sup>1, 2</sup>    | Cuando el carácter debe apuntar a algo por debajo de él.                                                 | Los puntos de carácter hacia abajo.                                                                                                                                                                                                 |
| **GestureLeft**<sup>1, 2</sup>    | Cuando el carácter debe apuntar a un elemento de la izquierda.                                              | Los puntos de carácter con mano izquierda o se transforma en una flecha que apunta hacia la izquierda.                                                                                                                                                 |
| **GestureRight**<sup>1, 2</sup>   | Cuando el carácter necesita apuntar a un elemento de su derecha.                                             | Los puntos de carácter con mano derecha o de transformación en una flecha que apunta hacia la derecha.                                                                                                                                               |
| **GestureUp**<sup>1, 2</sup>      | Cuando el carácter debe apuntar a algo encima de él.                                                 | Los puntos de carácter.                                                                                                                                                                                                   |
| **GetAttention**                 | Cuando el carácter debe notificar al usuario sobre algo importante.                                   | La mano de los caracteres se pone al día o se salta hacia arriba y hacia abajo.                                                                                                                                                                            |
| **GetAttentionContinued**        | Para enfatizar la importancia de la notificación.                                                         | Continuación o repetición del gesto inicial.                                                                                                                                                                       |
| **GetAttentionReturn**           | Cuando el carácter completa la animación **GetAttention** o **GetAttentionContinued** .                | El carácter vuelve a su posición neutra.                                                                                                                                                                             |
| **Saluda**<sup>1, 2</sup>          | Cuando el usuario inicia el sistema.                                                                      | Sonrisas de caracteres y olas.                                                                                                                                                                                            |
| **Hearing1**                     | Cuando el carácter oye el inicio de un utterance hablado (escuchando activamente).                           | El carácter se inclina hacia delante y nodos, o bien convierte el encabezado en la respuesta a la entrada de voz. Nota: esta animación se repite en un marco intermedio que se produce después de que el carácter se mueve a una posición adecuada.<br/>   |
| **Hearing2**                     | Cuando el carácter oye el inicio de un utterance hablado (escuchando activamente).                           | Otra variación del tipo de animación que se usa en **Hearing1** Nota: esta animación se repite en un marco intermedio que se produce después de que el carácter se mueve a una posición adecuada.<br/>                      |
| **Ocultar**                         | Cuando el usuario descarta el carácter.                                                                   | El carácter quita el contenido de la pantalla.                                                                                                                                                                                    |
| **Idle1 \_ 1**                     | Cuando el carácter no tiene ninguna tarea y el usuario no está interactuando con el carácter.                       | El carácter parpadea o busca, permanece o se vuelve a la posición neutra.                                                                                                                                   |
| **Idle1 \_ 2**                     | Cuando el carácter no tiene ninguna tarea y el usuario no está interactuando con el carácter.                       | Otra variación del tipo de animación que se usa en **Idle1 \_ 1**.                                                                                                                                                       |
| **Idle2 \_ 1**                     | Cuando el carácter ha estado inactivo durante algún tiempo.                                                          | La Yawns de caracteres o lee la revista que permanece o vuelve a la posición neutra.                                                                                                                                   |
| **Idle2 \_ 2**                     | Cuando el carácter ha estado inactivo durante algún tiempo.                                                          | Otra variación del tipo de animación que se usa en **Idle2 \_ 1**.                                                                                                                                                       |
| **Idle3 \_ 1**                     | Cuando el carácter ha estado inactivo durante mucho tiempo.                                                        | Carácter Yawns.                                                                                                                                                                                                       |
| **Idle3 \_ 2**                     | Cuando el carácter ha estado inactivo durante mucho tiempo.                                                        | Los caracteres se suspenden o se colocan en auriculares para escuchar música. Nota: esta animación se repite en un marco intermedio que se produce después de que el carácter se mueve a una posición adecuada.<br/>                          |
| **LookDown**                     | Cuando el carácter tiene que buscarse.                                                                   | El carácter se ve desactivado.                                                                                                                                                                                                  |
| **LookLeft**                     | Cuando el carácter debe parecerse a la izquierda.                                                                   | El carácter se parece a la izquierda.                                                                                                                                                                                           |
| **LookRight**                    | Cuando el carácter debe ser correcto.                                                                  | El carácter se parece a la derecha.                                                                                                                                                                                          |
| **Buscar**                       | Cuando es necesario buscar el carácter.                                                                     | El carácter busca.                                                                                                                                                                                                    |
| **Bajar**                     | Cuando el carácter se prepara para moverse hacia abajo.                                                                | Las transiciones de caracteres a una posición hacia abajo o de desplazamiento.                                                                                                                                                               |
| **MoveLeft**                     | Cuando el carácter se prepara para moverse a la izquierda.                                                                | Transiciones de caracteres a una posición izquierda de caminar y volar.                                                                                                                                                               |
| **Anula**                    | Cuando el carácter se prepara para moverse hacia la derecha.                                                               | Transiciones de caracteres a una posición derecha de caminar y volar.                                                                                                                                                              |
| **MoveUp**                       | Cuando el carácter se prepara para subir.                                                                  | Transiciones de caracteres a una posición de caminar/volar arriba.                                                                                                                                                                 |
| <sup>1 y 2</sup>        | Cuando el carácter está satisfecho con la solicitud o la elección del usuario.                                         | Sonrisas de caracteres.                                                                                                                                                                                                      |
| **Proceso**                      | Cuando el carácter realiza algún tipo de tarea genérica.                                                   | El carácter presiona botones o usa algún tipo de herramienta.                                                                                                                                                                   |
| **Processing**                   | Cuando el carácter está ocupado trabajando en una tarea genérica.                                                    | Los garabatos de carácter están en el Bloc de papel o utilizan algún tipo de herramienta. Nota: esta animación se repite en un marco intermedio que se produce después de que el carácter se mueve a una posición adecuada.<br/>                      |
| **Lectura**                         | Cuando el carácter Lee algo para el usuario.                                                          | El carácter muestra el libro o el papel, Lee y vuelve a buscar al usuario.                                                                                                                                                       |
| **ReadContinued**                | Cuando el carácter se lee más en el usuario.                                                            | Vuelve a leer los caracteres y vuelve a buscar el usuario.                                                                                                                                                                        |
| **ReadReturn**                   | Cuando el carácter completa la animación de **lectura** o **ReadContinued** .                                | El carácter vuelve a su posición neutra.                                                                                                                                                                             |
| **Leía**                      | Cuando el carácter Lee algo pero no puede aceptar la entrada.                                              | Lecturas de caracteres de un trozo de papel. Nota: esta animación se repite en algunos fotogramas intermedios que se producen después de que el carácter se mueve a una posición adecuada.<br/>                                           |
| **RestPose**                     | Cuando el carácter habla de su posición neutra.                                                     | El carácter está con una postura relajada pero Attentive.                                                                                                                                                                   |
| **Sad**<sup>1, 2</sup>            | Cuando el carácter está decepcionado con la elección del usuario.                                               | La desaprobación de los caracteres o parece decepcionado.                                                                                                                                                                                |
| **Búsqueda**                       | Cuando el carácter busca algo.                                                                   | Los caracteres se ordenan aleatoriamente a través del cajón de archivos u otro contenedor que busca algo.                                                                                                                                       |
| **Buscándol**                    | Cuando el carácter busca información especificada por el usuario.                                              | Los caracteres se ordenan aleatoriamente a través del cajón de archivos u otro contenedor que busca algo. Nota: esta animación se repite en algunos fotogramas intermedios que se producen después de que el carácter se mueve a una posición adecuada.<br/> |
| **Mostrar**                         | Cuando el carácter comienza o se devuelve después de la citada.                                            | El carácter emerge en una sopla de humo, en la pantalla o en los recorridos en pantalla.                                                                                                                                                    |
| **StartListening**<sup>1, 2</sup> | Cuando el carácter está escuchando.                                                                         | El carácter coloca mano en lengüeta.                                                                                                                                                                                            |
| **StopListening**<sup>1, 2</sup>  | Cuando el carácter deja de escuchar.                                                                      | El carácter coloca los oídos a mano.                                                                                                                                                                                        |
| **Sugerir**<sup>1,2</sup>        | Cuando el carácter tiene una sugerencia o una sugerencia para el usuario.                                                 | Aparece una bombilla junto a carácter.                                                                                                                                                                                  |
| **Sorpresa**<sup>1, 2</sup>      | Cuando el carácter se sorprende por la acción o la elección del usuario.                                          | Caracteres anchos de los ojos, abre la boca.                                                                                                                                                                                    |
| **Piense** en <sup>1, 2</sup>          | Cuando el carácter está pensando en algo.                                                          | El carácter busca y mantiene la mano en el encabezado.                                                                                                                                                                             |
| **Descierto**<sup>1, 2</sup>      | Cuando el carácter necesita que el usuario confirme una solicitud.                                                  | El carácter se parece a cuestionario, transmite ("¿está seguro?")                                                                                                                                                                   |
| **Ola**<sup>1, 2</sup>           | Cuando el usuario elige apagar el servidor o el sistema.                                                 | Olas de caracteres: Adiós o Hola.                                                                                                                                                                                     |
| **Escritura**                        | Cuando el carácter está escuchando instrucciones del usuario.                                          | El carácter muestra papel, escribe y vuelve a buscar al usuario.                                                                                                                                                              |
| **WriteContinued**               | Cuando el carácter sigue escuchando instrucciones del usuario.                                   | Escrituras de caracteres en una pieza de papel y se vuelve a buscar en el usuario.                                                                                                                                                           |
| **WriteReturn**                  | Cuando el carácter completa la animación de **escritura** o **WriteContinued** .                              | El carácter vuelve a su posición neutra.                                                                                                                                                                             |
| **Escribir**                      | Cuando el carácter escribe información para el usuario.                                                  | Escrituras de caracteres en papel. Nota: esta animación se repite.<br/>                                                                                                                                             |



 

  La animación requiere superposiciones de la boca y un marco de habla definido.

  La animación requiere una animación de devolución asignada basada en la bifurcación de salida o en una animación de devolución explícita.

Además, un carácter debe tener las siguientes asignaciones de estado.



| Estado          | Animaciones requeridas                           |
|----------------|-----------------------------------------------|
| GesturingDown  | GestureDown                                   |
| GesturingLeft  | GestureLeft                                   |
| GesturingRight | GestureRight                                  |
| GesturingUp    | GestureUp                                     |
| Oído        | Hearing1, Hearing2                            |
| Conde         | Ocultar                                          |
| IdlingLevel1   | Parpadeo, Idle1 \_ 1, Idle1 \_ 2                     |
| IdlingLevel2   | Blink, Idle1 \_ 1, Idle1 \_ 2, Idle2 \_ 1, Idle2 \_ 2 |
| IdlingLevel3   | Idle3 \_ 1, Idle3 \_ 2                            |
| Escucha      | Alerta                                         |
| MovingDown     | Bajar                                      |
| MovingLeft     | MoveLeft                                      |
| MovingRight    | Anula                                     |
| MovingUp       | MoveUp                                        |
| Mostrando        | Mostrar                                          |
| Habla       | RestPose                                      |



 

 

 





