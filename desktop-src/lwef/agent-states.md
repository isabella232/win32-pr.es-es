---
title: Estados del agente
description: Estados del agente
ms.assetid: 8c3c5b12-81af-4ba5-b834-9f0a7ff5d075
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbfb927cbe9ad703e733caa827df7c5a63bac67b93d49edbb8f59884c89b6ee7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976805"
---
# <a name="agent-states"></a>Estados del agente

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

Los servicios de animación de Microsoft Agent reproducen automáticamente determinadas animaciones. Por ejemplo, cuando se usan comandos [**MoveTo**](moveto-method.md) [**o GestureAt,**](gestureat-method.md) los servicios de animación reproducen una animación adecuada. De forma similar, después del tiempo de espera de inactividad, los servicios reproducen automáticamente animaciones. Para admitir estos estados, puede definir las animaciones adecuadas y, a continuación, asignarlas a los estados. Todavía puede reproducir cualquier animación que defina directamente mediante el [**método Play,**](play-method.md) incluso si la asigna a un estado.

Puede asignar varias animaciones al mismo estado y los servicios de animación elegirán aleatoriamente una de las animaciones. Esto permite que el carácter presente una variedad mucho más natural en su comportamiento.

Aunque las animaciones que asigne a los estados pueden incluir fotogramas de bifurcación, evite las animaciones de bucle (animaciones que se bifurcan para siempre). De lo contrario, tendrá que usar el [**método Stop**](play-method.md) para poder reproducir otra animación.

Es importante definir y asignar al menos una animación para cada estado que se produce para el carácter. Si no proporciona estas animaciones y asignaciones de estado, es posible que el carácter no parezca comportarse correctamente para el usuario. Sin embargo, si no se produce un estado para un carácter determinado, no es necesario asignar una animación a ese estado. Por ejemplo, si la aplicación host nunca llama al [**método MoveTo,**](moveto-method.md) puede omitir la creación y asignación de animaciones **de** estado de movimiento.



| Estado              | Ejemplo de uso                                                                         |
|--------------------|----------------------------------------------------------------------------------------|
| **GesturingDown**  | Cuando se [**procesa el método de**](gestureat-method.md) animación GestureAt.          |
| **GesturingLeft**  | Cuando se [**procesa el método de**](gestureat-method.md) animación GestureAt.          |
| **GesturingRight** | Cuando se [**procesa el método de**](gestureat-method.md) animación GestureAt.          |
| **GesturingUp**    | Cuando se [**procesa el método de**](gestureat-method.md) animación GestureAt.          |
| **Oído**        | Cuando se detecta el principio de la entrada hablada.                                        |
| **Escondiendo**         | Cuando el usuario o la aplicación ocultan el carácter.                                  |
| **IdlingLevel1**   | Cuando el carácter comienza el **estado idling.**                                        |
| **IdlingLevel2**   | Cuando el carácter comienza el segundo **estado de nivel de idling.**                           |
| **IdlingLevel3**   | Cuando el carácter comienza el estado final **del nivel de idling.**                            |
| **Escuchar**      | Cuando el carácter empieza a escuchar (el usuario presiona primero la tecla de acceso directo de entrada de voz). |
| **MovingDown**     | Cuando se procesa el método de animación [**MoveTo.**](moveto-method.md)                |
| **MovingLeft**     | Cuando se procesa el método de animación [**MoveTo.**](moveto-method.md)                |
| **MovingRight**    | Cuando se procesa el método de animación [**MoveTo.**](moveto-method.md)                |
| **MovingUp**       | Cuando se procesa el método de animación [**MoveTo.**](moveto-method.md)                |
| **Mostrando**        | Cuando el usuario o la aplicación muestran el carácter.                                  |
| **Hablando**       | Cuando se procesa el método de animación [**Speak.**](speak-method.md)                  |



 

### <a name="the-hearing-and-listening-states"></a>Estados de escucha y escucha

La animación que asigna al estado **Listening se** reproduce cuando el usuario presiona la tecla de acceso activa push-to-talk para la entrada de voz. Cree y asigne una animación corta que haga que el carácter parezca agradable. De forma similar, defina su **animación Devolución** para  que tenga una duración corta para que el carácter reproduce su animación de estado de audiencia cuando el usuario habla. Una **animación** de estado de audiencia también debe ser breve y estar diseñada para que el usuario sepa que el carácter escucha activamente lo que dice el usuario. Las inclinaciones de la cabeza u otros gestos ligeros son adecuados. Para proporcionar variabilidad natural, proporcione varias **animaciones de** estado de la audiencia.

### <a name="the-gesturing-states"></a>Los estados de gesturing

Solo debe crear y asignar animaciones de estado **Gesturing** si tiene previsto usar el [**método GestureAt.**](gestureat-method.md) **Las animaciones de** estado de gesturing se reproducen cuando Microsoft Agent procesa una llamada al **método GestureAt.** Si define superposiciones de superposición para las animaciones de estado **Gesturing,** el carácter puede hablar mientras hace gestos.

Los servicios de animación determinan la ubicación del carácter y su relación con la ubicación de las coordenadas especificadas en el método y reproducen una animación adecuada. La dirección de gesturing siempre es con respecto al carácter; Por ejemplo, **GestureRight** debe ser un gesto a la derecha del carácter.

### <a name="the-showing-and-hiding-states"></a>Estados que se muestran y ocultan

Los **estados Mostrar** **y Ocultar** reproducen las animaciones asignadas cuando el usuario o la aplicación host solicitan mostrar u ocultar el carácter. Estos estados también establecen correctamente el estado Visible del **marco de** caracteres. Al definir animaciones para estos estados, tenga en cuenta que un carácter puede aparecer o salir en cualquier ubicación de la pantalla. Dado que el usuario puede mostrar u ocultar cualquier carácter, siempre admite al menos una animación para estos estados.

Las animaciones que se asignan al estado **Mostrando** suelen terminar con un marco que contiene la imagen de posición neutra del carácter. Por el contrario, **ocultar** animaciones de estado normalmente comienza con la posición neutra. **Mostrar** y **ocultar** animaciones de estado puede incluir un marco vacío al principio o al final, respectivamente, para proporcionar una transición desde el estado actual del carácter.

### <a name="the-idling-states"></a>Estados de idling

Los **estados de idling** son progresivas. Los servicios de animación comienzan a usar las asignaciones de nivel 1 para el primer período de inactividad y usan las animaciones de nivel 2 para el segundo. Después de esto, el ciclo de inactividad progresa hasta las animaciones asignadas de nivel 3 y permanece en este estado hasta que se cancela, como cuando se inicia una nueva solicitud de animación.

Diseñe animaciones para los **estados idling** para comunicar el estado del carácter, pero no para distraer al usuario. Las animaciones deben reflejar adecuadamente la capacidad de respuesta del carácter de manera sutil pero clara. Por ejemplo, la creación de un parpadeo o la creación de un parpadeo son animaciones buenas para asignar al **estado IdlingLevel1.** Las animaciones de lectura funcionan bien para el **estado IdlingLevel2.** El modo de estar en modo de vida o escuchar música con cascos son buenos ejemplos de animaciones que se asignan al **estado IdlingLevel3.** Las animaciones que incluyen muchos o grandes movimientos no son adecuadas para las animaciones inactivas porque dibujan la atención del usuario. Dado **que las animaciones** de estado de idling se reproducen con frecuencia, proporcione varias animaciones de estado **idling,** especialmente para los estados **IdlingLevel1** **e IdlingLevel2.**

Tenga en cuenta que una aplicación puede desactivar el procesamiento de inactividad automático de un carácter y administrar el propio estado de **idling del** carácter. Los estados **de Idling** del agente están diseñados para ayudarle a evitar cualquier situación en la que el carácter no tenga animación que reproducir. Una imagen de carácter que no cambia después de un breve período de tiempo es como una aplicación que muestra un puntero de espera durante mucho tiempo, lo que resta importancia a la sensación de inactividad e inactividad. Mantener la esperanza no requiere mucho: a veces, solo un parpadeo animado, un desenlazo visible o un cambio de cuerpo.

### <a name="the-speaking-state"></a>El estado de habla

Los servicios de animación usan el **estado Speaking** cuando no se encuentra una animación de habla para la animación actual. Asigne una animación de habla simple a este estado. Por ejemplo, puede usar un único fotograma que consta de la posición neutra del carácter con superposiciones de máscara.

### <a name="the-moving-states"></a>Estados móviles

Los **estados móviles** se reproducen cuando una aplicación llama al método [**MoveTo.**](moveto-method.md) Los servicios de animación determinan qué animación se va a reproducir en función de la ubicación actual del carácter y las coordenadas especificadas. La dirección del movimiento se basa en la posición del carácter. Por lo tanto, la animación que asigne a la **animación MovingLeft** debe basarse en la izquierda del carácter. Si no usa el método **MoveTo,** puede omitir la creación y asignación de una animación.

**Las** animaciones de estado de movimiento deben animar el carácter en su posición de movimiento. El último fotograma de esta animación se muestra cuando el fotograma del carácter se mueve en la pantalla. No hay compatibilidad para animar el carácter mientras se mueve su marco.

### <a name="standard-animation-set"></a>Conjunto de animación estándar

Aunque puede diseñar un carácter personalizado para que tenga las animaciones que desea usar, Microsoft Agent define un conjunto de animaciones estándar. Los caracteres que se ajustan a esta definición se pueden seleccionar como un carácter predeterminado.

En la tabla siguiente se enumeran las animaciones incluidas en el conjunto de animaciones estándar. Incluso si va a crear un carácter personalizado, puede usar la lista como guía para diseñar sus propios caracteres. Los caracteres que admiten el conjunto de animaciones estándar deben admitir al menos las animaciones siguientes.



| Animación                        | Ejemplo de uso                                                                                           | Animación de ejemplo                                                                                                                                                                                                      |
|----------------------------------|----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Confirmación**                  | Cuando el carácter confirma la solicitud del usuario.                                                      | Gesto de mano de "Aceptar" con los gestos de carácter. Tenga en cuenta que esta animación debe devolver el carácter a su posición neutra.<br/>                                                                                  |
| **Alerta**<sup>1,2</sup>          | Cuando el carácter está esperando instrucciones, normalmente se reproduce después de que el usuario activa el modo de escucha. | Caras de caracteres delante, con dificultades, parpadeando ocasionalmente, pero con una instrucción claramente en espera.                                                                                                                             |
| **Anuncio**<sup>de 1,2</sup>       | Cuando el carácter ha encontrado información para el usuario.                                                   | Gestos de caracteres al elevar gestos y manos o abre un sobre.                                                                                                                                                  |
| **Blink**                        | Cuando el carácter termina de hablar o está inactivo.                                                            | El carácter parpadea de forma natural.                                                                                                                                                                                       |
| **Confuso**<sup>1,2</sup>       | Cuando el carácter no entiende qué hacer.                                                        | El carácter se rasca la cabeza.                                                                                                                                                                                              |
| <sup>1,2</sup>   | Cuando el carácter o el usuario completan una tarea (una forma más fuerte de la **animación Confirmar).**          | El carácter realiza un gesto de enhorabubundo y transmite "Sí!".                                                                                                                                                              |
| **Disminución**<sup>de 1,2</sup>        | Cuando el carácter no puede hacer o rechazar la solicitud del usuario.                                             | El carácter agite la cabeza y transmite "no se puede hacer".                                                                                                                                                                            |
| **DoMagic1**                     | El carácter se prepara para mostrar algo.                                                                 | Ondas de caracteres con las manos o la varita.                                                                                                                                                                                         |
| **DoMagic2**                     | El carácter completa la presentación de algo.                                                                | El carácter completa el gesto mágico.                                                                                                                                                                                     |
| **No reconoce**<sup>1,2</sup>  | Cuando el carácter no reconoce la solicitud del usuario.                                                  | El carácter se mantiene de mano a oído.                                                                                                                                                                                           |
| **Explicación**<sup>1,2</sup>        | Cuando el carácter explica algo al usuario.                                                       | Gestos de caracteres como si explicara algo.                                                                                                                                                                         |
| **GestureDown**<sup>1,2</sup>    | Cuando el carácter necesita apuntar a algo debajo de él.                                                 | Puntos de carácter hacia abajo.                                                                                                                                                                                                 |
| **GestureLeft**<sup>1,2</sup>    | Cuando el carácter necesita apuntar a algo a su izquierda.                                              | Puntos de caracteres con la mano izquierda o se transforma en una flecha que apunta a la izquierda.                                                                                                                                                 |
| **GestureRight**<sup>1,2</sup>   | Cuando el carácter necesita apuntar a algo a su derecha.                                             | Los puntos de caracteres con la mano derecha o se transforman en una flecha que apunta a la derecha.                                                                                                                                               |
| **GestureUp**<sup>1,2</sup>      | Cuando el carácter necesita apuntar a algo por encima de él.                                                 | El carácter apunta hacia arriba.                                                                                                                                                                                                   |
| **GetAttention**                 | Cuando el carácter necesita notificar al usuario sobre algo importante.                                   | Los caracteres ondea las manos o saltan hacia arriba y hacia abajo.                                                                                                                                                                            |
| **GetAttentionContinued**        | Para resaltar la importancia de la notificación.                                                         | Continuación o repetición del gesto inicial.                                                                                                                                                                       |
| **GetAttentionReturn**           | Cuando el carácter completa la **animación GetAttention** o **GetAttentionContinued.**                | El carácter vuelve a su posición neutra.                                                                                                                                                                             |
| **Greet**<sup>1,2</sup>          | Cuando el usuario inicia el sistema.                                                                      | Sonrientes y ondas de caracteres.                                                                                                                                                                                            |
| **Audiencia1**                     | Cuando el carácter escucha el inicio de una expresión hablada (escucha activa).                           | El carácter se inclina hacia delante y hacia delante, o gira la cabeza mostrando la respuesta a la entrada de voz. Nota: Esta animación recorre en bucle algún fotograma intermedio que se produce después de que el carácter se mueve a una posición adecuada.<br/>   |
| **Audiencia2**                     | Cuando el carácter escucha el inicio de una expresión hablada (escucha activa).                           | Otra variación del tipo de animación que se usa en **Hearing1** Nota: esta animación se desplaza a algún fotograma intermedio que se produce después de que el carácter se mueve a una posición adecuada.<br/>                      |
| **Ocultar**                         | Cuando el usuario descarta el carácter.                                                                   | El carácter se quita de la pantalla.                                                                                                                                                                                    |
| **Idle1 \_ 1**                     | Cuando el carácter no tiene ninguna tarea y el usuario no interactúa con el carácter.                       | El carácter parpadea o mira alrededor, permanece en la posición neutra o vuelve a ella.                                                                                                                                   |
| **Idle1 \_ 2**                     | Cuando el carácter no tiene ninguna tarea y el usuario no interactúa con el carácter.                       | Otra variación del tipo de animación utilizado en **Idle1 \_ 1**.                                                                                                                                                       |
| **Idle2 \_ 1**                     | Cuando el carácter ha estado inactivo durante algún tiempo.                                                          | El carácter hace unwn o lee la revista que permanece en la posición neutra o vuelve a la posición neutra.                                                                                                                                   |
| **Idle2 \_ 2**                     | Cuando el carácter ha estado inactivo durante algún tiempo.                                                          | Otra variación del tipo de animación usada en **Idle2 \_ 1**.                                                                                                                                                       |
| **Idle3 \_ 1**                     | Cuando el carácter ha estado inactivo durante mucho tiempo.                                                        | Yawns de caracteres.                                                                                                                                                                                                       |
| **Idle3 \_ 2**                     | Cuando el carácter ha estado inactivo durante mucho tiempo.                                                        | El carácter se pone en suspensión o se pone en los micrófonos para escuchar música. Nota: Esta animación recorre en bucle algún fotograma intermedio que se produce después de que el carácter se mueve a una posición adecuada.<br/>                          |
| **LookDown**                     | Cuando el carácter necesita mirar hacia abajo.                                                                   | El carácter mira hacia abajo.                                                                                                                                                                                                  |
| **LookLeft**                     | Cuando el carácter tiene que mirar a la izquierda.                                                                   | El carácter se ve a la izquierda.                                                                                                                                                                                           |
| **LookRight**                    | Cuando el carácter debe tener un aspecto correcto.                                                                  | El carácter se ve a la derecha.                                                                                                                                                                                          |
| **Búsqueda**                       | Cuando es necesario buscar el carácter.                                                                     | El carácter busca.                                                                                                                                                                                                    |
| **MoveDown**                     | Cuando el carácter se prepara para bajar.                                                                | Las transiciones de caracteres a una posición a pie o hacia abajo.                                                                                                                                                               |
| **MoveLeft**                     | Cuando el carácter se prepara para moverse a la izquierda.                                                                | Transiciones de caracteres a una posición a la izquierda a pie o a la izquierda.                                                                                                                                                               |
| **MoveRight**                    | Cuando el carácter se prepara para moverse a la derecha.                                                               | Las transiciones de caracteres a una posición derecha a pie o en vuelo.                                                                                                                                                              |
| **MoveUp**                       | Cuando el carácter se prepara para moverse hacia arriba.                                                                  | Las transiciones de caracteres a una posición a pie o en vuelo hacia arriba.                                                                                                                                                                 |
| **Complacida**<sup>1,2</sup>        | Cuando el carácter se complace con la solicitud o la elección del usuario.                                         | Sonrisas de caracteres.                                                                                                                                                                                                      |
| **Process**                      | Cuando el carácter realiza algún tipo de tarea genérica.                                                   | El carácter presiona los botones o usa algún tipo de herramienta.                                                                                                                                                                   |
| **Procesamiento**                   | Cuando el carácter está ocupado trabajando en una tarea genérica.                                                    | Los caracteres se escriben en el panel de papel o usan algún tipo de herramienta. Nota: Esta animación recorre en bucle algún fotograma intermedio que se produce después de que el carácter se mueve a una posición adecuada.<br/>                      |
| **Lectura**                         | Cuando el carácter lee algo al usuario.                                                          | El carácter muestra el libro o el papel, las lecturas y la mirada hacia atrás del usuario.                                                                                                                                                       |
| **ReadContinued**                | Cuando el carácter lee más al usuario.                                                            | El carácter vuelve a leer y, a continuación, vuelve a mirar al usuario.                                                                                                                                                                        |
| **ReadReturn**                   | Cuando el carácter completa la animación **Read** **o ReadContinued.**                                | El carácter vuelve a su posición neutra.                                                                                                                                                                             |
| **Lectura**                      | Cuando el carácter lee algo, pero no puede aceptar la entrada.                                              | El carácter se lee de un fragmento de papel. Nota: Esta animación recorre en bucle algunos fotogramas intermedios que se producen después de que el carácter se mueve a una posición adecuada.<br/>                                           |
| **RestPose**                     | Cuando el carácter habla desde su posición neutra.                                                     | El carácter se mantiene con una posición relajada pero relajada.                                                                                                                                                                   |
| **Lamentablemente**<sup>1,2</sup>            | Cuando el carácter está satisfecho con la elección del usuario.                                               | Los caracteres se desaprobarán o parecen desaprobados.                                                                                                                                                                                |
| **Búsqueda**                       | Cuando el carácter busca algo.                                                                   | El orden aleatorio de caracteres a través del cajón de archivos u otro contenedor busca algo.                                                                                                                                       |
| **Buscando**                    | Cuando el carácter busca información especificada por el usuario.                                              | El orden aleatorio de caracteres a través del cajón de archivos u otro contenedor busca algo. Nota: Esta animación recorre en bucle algunos fotogramas intermedios que se producen después de que el carácter se mueve a una posición adecuada.<br/> |
| **Mostrar**                         | Cuando el carácter se inicia o vuelve después de ser invocado.                                            | El carácter aparece en un almodo de humo, haces de entrada o paseos en pantalla.                                                                                                                                                    |
| **StartListening**<sup>1,2</sup> | Cuando el carácter está escuchando.                                                                         | El carácter coloca mano a oído.                                                                                                                                                                                            |
| **StopListening**<sup>1,2</sup>  | Cuando el carácter deja de escuchar.                                                                      | El carácter coloca las manos sobre las manos.                                                                                                                                                                                        |
| **Sugerencia**<sup>1,2</sup>        | Cuando el carácter tiene una sugerencia o sugerencia para el usuario.                                                 | La bombilla aparece junto al carácter.                                                                                                                                                                                  |
| **Sorpresa**<sup>1,2</sup>      | Cuando el carácter se sorprenda por la acción o la elección del usuario.                                          | El carácter amplía los ojos y abre la cara.                                                                                                                                                                                    |
| **Think**<sup>1,2</sup>          | Cuando el carácter está pensando en algo.                                                          | El carácter busca y mantiene la mano sobre la cabeza.                                                                                                                                                                             |
| <sup>1,2 incierta</sup>      | Cuando el carácter necesita que el usuario confirme una solicitud.                                                  | El carácter tiene un aspecto cuestionario, transmite ("¿Está seguro?"")                                                                                                                                                                   |
| **Wave**<sup>1,2</sup>           | Cuando el usuario decide apagar el servidor o el sistema.                                                 | Adiós a las ondas de caracteres o hola.                                                                                                                                                                                     |
| **Escritura**                        | Cuando el carácter escucha instrucciones del usuario.                                          | El carácter muestra papel, escribe y vuelve a mirar al usuario.                                                                                                                                                              |
| **WriteContinued**               | Cuando el carácter sigue escuchando instrucciones del usuario.                                   | El carácter escribe en un papel y vuelve a mirar al usuario.                                                                                                                                                           |
| **WriteReturn**                  | Cuando el carácter completa la animación **Write** **o WriteContinued.**                              | El carácter vuelve a su posición neutra.                                                                                                                                                                             |
| **Escritura**                      | Cuando el carácter escribe información para el usuario.                                                  | Escrituras de caracteres en papel. Nota: Esta animación recorre bucles.<br/>                                                                                                                                             |



 

  La animación requiere superposiciones de máscara y un marco de habla definido.

  La animación requiere una animación Return asignada en función de su bifurcación de salida o una animación Return explícita.

Además, un carácter debe tener las siguientes asignaciones de estado.



| Estado          | Animaciones necesarias                           |
|----------------|-----------------------------------------------|
| GesturingDown  | GestureDown                                   |
| GesturingLeft  | GestureLeft                                   |
| GesturingRight | GestureRight                                  |
| GesturingUp    | GestureUp                                     |
| Oído        | Hearing1, Hearing2                            |
| Escondiendo         | Ocultar                                          |
| IdlingLevel1   | Blink, Idle1 \_ 1, Idle1 \_ 2                     |
| IdlingLevel2   | Blink, Idle1 \_ 1, Idle1 \_ 2, Idle2 \_ 1, Idle2 \_ 2 |
| IdlingLevel3   | Idle3 \_ 1, Idle3 \_ 2                            |
| Escuchar      | Alerta                                         |
| MovingDown     | MoveDown                                      |
| MovingLeft     | MoveLeft                                      |
| MovingRight    | MoveRight                                     |
| MovingUp       | MoveUp                                        |
| Mostrando        | Mostrar                                          |
| Hablando       | RestPose                                      |



 

 

 





