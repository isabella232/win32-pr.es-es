---
title: Barras de progreso
description: Con una barra de progreso, los usuarios pueden seguir el progreso de una operación larga. Una barra de progreso puede mostrar un porcentaje aproximado de finalización (determinación) o indicar que una operación está en curso (indeterminada).
ms.assetid: 067961fa-2fb1-4cd1-99a4-cbe2244c3913
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: a87ddece61276e5ac651f0610f34409477e18f53
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127262383"
---
# <a name="progress-bars"></a>Barras de progreso

> [!NOTE]
> Esta guía de diseño se creó para Windows 7 y no se ha actualizado para las versiones más recientes de Windows. Gran parte de las instrucciones se siguen aplicando en principio, pero la presentación y los ejemplos no reflejan nuestra [guía de diseño actual.](/windows/uwp/design/)

Con una barra de progreso, los usuarios pueden seguir el progreso de una operación larga. Una barra de progreso puede mostrar un porcentaje aproximado de finalización (determinación) o indicar que una operación está en curso (indeterminada).

Los estudios de facilidad de uso han demostrado que los usuarios son conscientes de los tiempos de respuesta de más de un segundo. Por lo tanto, debe considerar que las operaciones que tardan dos segundos o más en completarse son largas y necesitan algún tipo de comentarios de progreso.

![captura de pantalla de una barra de progreso típica ](images/progress-bars-image1.png)

Una barra de progreso típica.

> [!Note]  
> Las instrucciones relacionadas [con el diseño](vis-layout.md) se presentan en un artículo independiente.

 

## <a name="is-this-the-right-control"></a>¿Es este el control adecuado?

Para decidirte, intenta responder a estas preguntas:

-   **¿Se completará la operación en unos cinco segundos o menos?** Si es así, use un [indicador de actividad](inter-mouse.md) en su lugar, ya que mostrar una barra de progreso durante una duración tan corta sería distraer. Si la operación normalmente tarda cinco segundos o menos, pero a veces tarda más, comience con un puntero ocupado y convierta en una barra de progreso después de cinco segundos.
-   **¿Se usa una barra de progreso indeterminada para esperar a que el usuario complete una tarea?** En ese caso, no uses una barra de progreso. Las barras de progreso se usan para el progreso del equipo, no el del usuario.
-   **¿Se combina una barra de progreso indeterminada con una animación?** Si es así, use solo la animación en su lugar. La barra de progreso indeterminada es efectivamente una animación genérica y no agrega ningún valor a la animación.
-   **¿La operación es una tarea en segundo plano muy larga (más de dos minutos) para la que los usuarios están más interesados en la finalización que en el progreso?** Si es así, use [una notificación en](mess-notif.md) su lugar. En este caso, los usuarios hacen otras tareas mientras tanto y no supervisan el progreso. El uso de una notificación permite a los usuarios realizar otras tareas sin interrupciones. Entre los ejemplos de estas operaciones largas se incluyen la impresión, la copia de seguridad, los exámenes del sistema y las conversiones o transferencias masivas de datos.
-   **Una vez completada la operación, ¿podrán los usuarios reproducir los resultados?** Si es así, use un control deslizante en su lugar. Entre los ejemplos de estas operaciones se incluyen la grabación y reproducción de vídeo y audio.

    ![captura de pantalla del reproductor multimedia y el control deslizante ](images/progress-bars-image2.png)

    En este ejemplo, se usa un control deslizante para indicar el progreso mientras se reproduce el sonido. Esto permite a los usuarios reproducir los resultados más adelante.

## <a name="design-concepts"></a>Conceptos de diseño

Durante una operación larga, los usuarios necesitan una idea general de lo que está haciendo la operación. También deben saber lo siguiente:

-   Que se ha iniciado una operación larga.
-   Ese progreso se está haciendo y que la operación se completará finalmente (y, por lo tanto, no se ha bloqueado).
-   Porcentaje aproximado de la operación que se ha completado (y, por tanto, el porcentaje restante).
-   Si deben cancelar la operación si no merece la pena seguir esperando.
-   Si deben seguir esperando o hacer otra cosa mientras se completa la operación.

**Use barras de progreso determinadas para** las operaciones que requieren una cantidad limitada de tiempo, incluso si esa cantidad de tiempo no se puede predecir con precisión. Las barras de progreso indeterminado muestran que se está haciendo el progreso, pero no proporcionan ninguna otra información. No elija una barra de progreso indeterminada solo en función de la posible falta de precisión.

Por ejemplo, suponga que una operación requiere cinco pasos y cada uno de ellos requiere una cantidad limitada de tiempo, pero la cantidad de tiempo de cada paso puede variar considerablemente. En este caso, use una barra de progreso determinada y muestre el progreso cuando cada paso se complete proporcionalmente a la cantidad de tiempo que tarda normalmente cada paso. Use una barra de progreso indeterminada solo si una barra de progreso determinada haría que los usuarios concluyesen incorrectamente que la operación se ha bloqueado.

**Si solo hace una cosa...**

Asegúrese de proporcionar comentarios sobre el progreso de las operaciones largas y de que la información anterior se comunica claramente. Use barras de progreso determinadas siempre que sea posible.

## <a name="usage-patterns"></a>Patrones de uso

Las barras de progreso tienen varios patrones de uso:

### <a name="determinate-progress-bars"></a>Determinación de las barras de progreso




| Etiqueta | Value |
|--------|-------|
| <strong>Barras de progreso determinación modales</strong><br /> Indique el progreso de una operación rellenando de izquierda a derecha y rellenando completamente cuando se completa la operación. <br /> | Dado que estos comentarios son <a href="glossary.md">modales,</a>los usuarios no pueden realizar otras tareas en la ventana (o su elemento primario si se muestra en un cuadro de diálogo modal) hasta que se complete la operación. <br /><img src="images/progress-bars-image3.png" alt="Screen shot of progress bar in modal window " /><br /> En este ejemplo, la barra de progreso proporciona comentarios durante la configuración. <br /> | 
| <strong>Barras de progreso determinación modales con un botón Cancelar o Detener</strong><br /> Permitir que los usuarios detengan la operación, quizás porque la operación está tardando demasiado o no merece la pena esperar.<br /> | <img src="images/progress-bars-image4.png" alt="Screen shot of progress bar with Stop button " /><br /> En este ejemplo, los usuarios pueden hacer clic en Detener para detener la operación y dejar el entorno en su estado actual.<br /> | 
| <strong>Barras de progreso determinación modales con un botón Cancelar o Detener y animación</strong><br /> Permitir a los usuarios detener la operación e incluir una animación para ayudar a los usuarios a visualizar el efecto de una operación.<br /> | <img src="images/progress-bars-image5.png" alt="Screen shot of progress bar with animation " /><br /> En este ejemplo, los usuarios pueden hacer clic en Detener para detener la operación y dejar el entorno en su estado actual.<br /> | 
| <strong>Barras de progreso doble determinación modales</strong><br /> Indique el progreso de una operación de varios pasos mostrando el progreso del paso actual en la primera barra de progreso y el progreso general en la segunda barra.<br /> | Dado que la primera barra de progreso proporciona poca información adicional y puede ser bastante distraída, no se recomienda este patrón. En su lugar, haga que todos los pasos de la operación compartan una parte del progreso y que una sola barra de progreso se complete una vez. <br /><img src="images/progress-bars-image6.png" alt="Screen shot of current and overall progress bars " /><br /> En este ejemplo, la primera barra de progreso muestra el progreso del paso actual y la segunda barra de progreso muestra el progreso general.<br /><blockquote>[!Note]<br />Este patrón suele ser innecesario y debe evitarse.</blockquote><br /><br /> | 
| <strong>Barras de progreso determinadas de modeless</strong><br /> Indique el progreso de una operación rellenando de izquierda a derecha y rellenando completamente cuando se completa la operación.<br /> | A diferencia de las barras de progreso modales, los usuarios pueden realizar otras tareas mientras la operación está en curso. Estas barras de progreso se pueden mostrar en contexto o en una barra de estado. <br /><img src="images/progress-bars-image7.png" alt="Screen shot of progress bar on status bar " /><br /> En este ejemplo, Windows Internet ExplorerWindows Internet Explorer muestra su progreso para cargar una página web en la barra de estado. Los usuarios pueden realizar otras tareas mientras se carga la página.<br /> | 




 

### <a name="indeterminate-progress-bars"></a>Barras de progreso indeterminado



|   Tipo de barra de progreso  | Descripción             |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Barras de progreso indeterminado modales**<br/> indica que una operación está en curso al mostrar una animación que se recorrerá continuamente en la barra de izquierda a derecha. <br/>   | Se usa solo para operaciones cuyo progreso general no se puede determinar, por lo que no hay ninguna noción de integridad. Es preferible determinar las barras de progreso porque indican el porcentaje aproximado de la operación que se ha completado y ayudan a los usuarios a determinar si la operación merece la pena seguir esperando. también son menos distraídas visualmente. <br/> ![captura de pantalla de la barra de progreso modal e indeterminada](images/progress-bars-image8.png)<br/> En este ejemplo, Windows update usa una barra de progreso indeterminada modal para indicar el progreso mientras busca actualizaciones.<br/> |
| **Barras de progreso indeterminadas modeless**<br/> indica que una operación está en curso al mostrar una animación que se recorrerá continuamente en la barra de izquierda a derecha.<br/> | A diferencia de las barras de progreso modal, los usuarios pueden realizar otras tareas mientras el procesamiento está en curso. estas barras de progreso se pueden mostrar en contexto o en una barra de estado. <br/> ![captura de pantalla de la barra de progreso fino en la ventana de Outlook ](images/progress-bars-image9.png)<br/> En este ejemplo, Microsoft Outlook una barra de progreso indeterminada modeless al rellenar las propiedades de contacto. Los usuarios pueden seguir usando la ventana de propiedades mientras este trabajo está en curso.<br/>                                                                                                                    |



 

### <a name="meters"></a>Metros



|   Tipo                                                                                       |   Descripción                                                                                                                                                                                                                                                                                                                                                                 |
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Metros**<br/> indican un porcentaje que no está relacionado con el progreso. <br/> | Este patrón no es una barra de progreso, pero se implementa mediante el control de barra de progreso. Los medidores tienen un aspecto distinto para diferenciarlos de las barras de progreso verdaderas. <br/> ![captura de pantalla del medidor que muestra espacio libre en disco ](images/progress-bars-image10.png)<br/> En este ejemplo, el medidor muestra el porcentaje de espacio de unidad de disco usado.<br/> |



 

## <a name="guidelines"></a>Directrices

### <a name="general"></a>General

-   **Proporcionar comentarios sobre el progreso al realizar una operación larga.** Los usuarios nunca deben tener que adivinar si se está avanzando.
-   **Indique claramente el progreso real.** La barra de progreso debe avanzar si se realiza el progreso. Si el intervalo de tiempos de finalización esperados es grande, considere la posibilidad de usar una escala no lineal para indicar el progreso durante los tiempos más largos. No quiere que los usuarios concluyan que el programa se ha bloqueado cuando no lo ha hecho.
-   **Indique claramente la falta de progreso.** La barra de progreso no debe avanzar si no se realiza ningún progreso. No quiere que los usuarios esperen indefinidamente a una operación que nunca se va a completar.
-   **Proporcione detalles de progreso útiles.** Proporcione información de progreso adicional, pero solo si los usuarios pueden hacer algo con ella. Asegúrese de que el texto se muestra el tiempo suficiente para que los usuarios puedan leerlo.

    ![captura de pantalla de la barra de progreso que muestra la velocidad de transferencia ](images/progress-bars-image11.png)

    En este ejemplo, los usuarios pueden ver la tasa de transferencia. La baja velocidad de transferencia aquí sugiere la necesidad de usar una conexión de red de ancho de banda alto.

-   **No proporcione detalles innecesarios.** Por lo general, a los usuarios no les importan los detalles de la operación que se realiza. Por ejemplo, a los usuarios de un programa de instalación no les importa el archivo específico que se copia o que los componentes del sistema se están registrando porque no tienen expectativas sobre estos detalles. Normalmente, una barra de progreso bien etiquetada solo proporciona información suficiente, así que proporcione información de progreso adicional solo si los usuarios pueden hacer algo con ella. Proporcionar detalles que a los usuarios no les importan hace que la experiencia del usuario sea demasiado complicada y técnica. Si necesita información más detallada para la depuración, no la muestre en las compilaciones de versión.

    **Correcto:**

    ![captura de pantalla del progreso de la instalación ](images/progress-bars-image12.png)

    En este ejemplo, la barra de progreso etiquetada es todo lo que se necesita.

    **Correcto:**

    ![captura de pantalla de la barra de progreso que muestra la velocidad de transferencia ](images/progress-bars-image11.png)

    En este ejemplo, Windows Explorer copia los archivos seleccionados por el usuario, por lo que mostrar los nombres de archivo que se copian es significativo.

    **Incorrecto:**

    ![captura de pantalla del progreso del registro ](images/progress-bars-image13.png)

    En este ejemplo, un programa de instalación proporciona detalles que no tienen sentido para el usuario.

-   **Proporcionar animaciones útiles.** Si se realizan bien, las animaciones mejoran la experiencia del usuario al ayudar a los usuarios a visualizar la operación. Las animaciones buenas tienen más impacto que el texto por sí solas. Por ejemplo, la barra de progreso del comando Outlook Delete muestra el papelera de reciclaje para el destino si los archivos se pueden recuperar, pero no papelera de reciclaje si los archivos no se pueden recuperar.

    ![captura de pantalla del progreso de la eliminación ](images/progress-bars-image14.png)

    En este ejemplo, la falta de un papelera de reciclaje refuerza que los archivos se eliminan permanentemente. Esta información adicional no se comunicaría de forma tan eficaz con texto solo.

-   **No use animaciones innecesarias.** Las animaciones pueden ser confusas porque normalmente se ejecutan en un subproceso independiente de la tarea real y, por tanto, pueden sugerir progreso incluso si la operación se ha bloqueado. Además, si la operación es más lenta de lo esperado, los usuarios a veces asumen que la animación forma parte del motivo. Por lo tanto, solo use animaciones cuando haya una justificación clara; no los use para intentar atener a los usuarios.
-   **Coloque las animaciones centradas sobre la barra de progreso.** Coloque la animación encima de las etiquetas de la barra de progreso, si tiene alguna. Si hay un botón Cancelar o Detener a la derecha de la barra de progreso, incluya el botón al determinar el centro.
-   **Reproducir un efecto de sonido al finalizar una operación solo si es muy larga (más de dos minutos), poco frecuente e importante.** Si es probable que el usuario se aleje de una operación importante mientras se está procesando, un efecto de sonido restaura la atención del usuario. El uso de un efecto de sonido tras la finalización en otras circunstancias sería una molestia que distrae.
-   **No robo el foco de entrada para mostrar una actualización de progreso o finalización.** A menudo, los usuarios cambian a otros programas mientras esperan y no quieren que se interrumpan. Las tareas en segundo plano deben permanecer en segundo plano.
-   **No se preocupe por el soporte técnico.** Dado que los comentarios proporcionados por las barras de progreso no son necesariamente precisos y son fugaces, las barras de progreso no son un buen mecanismo para proporcionar información de soporte técnico. Por lo tanto, si se puede producir un error en la operación (como con un programa de instalación), no proporcione información de progreso adicional que solo sea útil para el soporte técnico. En su lugar, proporcione un mecanismo alternativo, como un archivo de registro, para registrar información de soporte técnico.

    **Incorrecto:**

    ![captura de pantalla de la barra de progreso que muestra el nombre del servidor ](images/progress-bars-image15.png)

    En este ejemplo, la barra de progreso muestra los detalles destinados al soporte técnico.

-   **No coloque el porcentaje completo ni ningún otro texto en una barra de progreso.** Este texto no es accesible y no es compatible con el uso de temas.

    **Incorrecto:**

    ![captura de pantalla de la barra de progreso con texto en la barra ](images/progress-bars-image16.png)

    En este ejemplo, no se puede acceder al texto de porcentaje de la barra de progreso.

-   **No combine una barra de progreso con un puntero ocupado.** Use uno u otro, pero no ambos al mismo tiempo.
-   **No use barras de progreso vertical.** Las barras de progreso horizontal tienen una asignación más natural y un mejor flujo.

### <a name="determinate-progress-bars"></a>Barras de progreso determinadas

-   **Use barras de progreso determinadas para las** operaciones que requieren una cantidad limitada de tiempo, incluso si esa cantidad de tiempo no se puede predecir con precisión. Las barras de progreso indeterminado muestran que se está avanzando, pero no proporcionan ninguna otra información. No elija una barra de progreso indeterminada solo en función de la posible falta de precisión por sí sola.
-   **Indique claramente la fase de progreso.** La barra de progreso debe ser capaz de indicar si la operación está al principio, al medio o al final de una operación. Por ejemplo, las barras de progreso que se lanzan inmediatamente al 99 por ciento de finalización y, a continuación, permanecen allí durante mucho tiempo son especialmente poco formatosas y pesadas. En estos casos, la barra de progreso debe establecerse inicialmente en como máximo el 33 por ciento para indicar que la operación todavía está en la fase inicial.
-   **Indique claramente la finalización.** No permita que una barra de progreso vaya al 100 % a menos que se haya completado la operación.
-   **Proporcione una estimación del tiempo restante si puede hacerlo con precisión.** Las estimaciones de tiempo restante que son precisas son útiles, pero las estimaciones que están muy lejos de la marca o que se recuperan significativamente no son útiles. Es posible que tenga que realizar algún procesamiento para poder proporcionar estimaciones precisas. Si es así, no muestre estimaciones potencialmente inexactas durante este período inicial.
-   **No reinicie el progreso.** Una barra de progreso pierde su valor si se reinicia (quizás porque se completa un paso de la operación) porque los usuarios no tienen forma de saber cuándo se completará la operación. En su lugar, haga que todos los pasos de la operación compartan una parte del progreso y que la barra de progreso se complete una vez.

    **Incorrecto:**

    ![captura de pantalla de la barra de progreso que se reinició ](images/progress-bars-image17.png)

    En este ejemplo, la operación se ha movido al paso de copia de archivos y se ha restablecido la barra de progreso de ese paso. Ahora los usuarios no tienen idea de cuánto progreso se ha realizado o cuánto tiempo queda.

-   **No haga una copia de seguridad del progreso.** Al igual que con un reinicio, una barra de progreso pierde su valor si hace una copia de seguridad. Aumente siempre el progreso de forma monónica. Sin embargo, puede tener una estimación de tiempo restante que aumente (así como disminuya) porque la tasa de progreso puede variar.

### <a name="indeterminate-progress-bars"></a>Barras de progreso indeterminado

-   **Use barras de progreso indeterminadas solo para las operaciones cuyo progreso general no se puede determinar.** Use barras de progreso indeterminadas para las operaciones que requieren una cantidad de tiempo sin enlazar o que acceden a un número desconocido de objetos. Use tiempos de espera para proporcionar límites a las operaciones basadas en el tiempo.
-   **Convierta en una barra de progreso determinada una vez que se pueda determinar el progreso general.** Por ejemplo, si tarda mucho más de dos segundos en determinar el número de objetos, puede usar una barra de progreso indeterminada mientras se cuentan los objetos y, a continuación, convertir en una barra de progreso determinada.
-   **No combine barras de progreso indeterminados con el porcentaje completado o el tiempo restante de las estimaciones.** Si puede proporcionar esta información, use una barra de progreso determinada en su lugar.
-   **No combine barras de progreso indeterminadas con animaciones.** Una barra de progreso indeterminada es efectivamente una animación genérica, por lo que debe usar una o la otra, pero nunca ambas.

    **Correcto:**

    ![captura de pantalla del progreso en la detección del servidor ](images/progress-bars-image18.png)

    En este ejemplo, solo se usa una animación para mostrar que una operación está en curso.

### <a name="modeless-progress-bars"></a>Barras de progreso modeless

-   **Si los usuarios pueden hacer algo productivo mientras la operación está en curso, proporcione comentarios modelados.** Es posible que tenga que deshabilitar un subconjunto de funcionalidades que requiera que se complete la operación.
-   **Si la ventana tiene una barra de direcciones, muestre el progreso del modelo en la barra de direcciones.**

    ![captura de pantalla de la barra de progreso como parte de la barra de direcciones ](images/progress-bars-image19.png)

    En este ejemplo, el progreso del modelo se muestra en la barra de direcciones.

-   De lo **contrario, si la ventana tiene una barra de estado, muestre el progreso del modelo en la barra de estado.** Coloque el texto correspondiente a su izquierda en la barra de estado.

    ![captura de pantalla de la barra de progreso como parte de la barra de estado ](images/progress-bars-image7.png)

    En este ejemplo, el progreso del modelo se muestra en la barra de estado.

### <a name="modal-progress-bars"></a>Barras de progreso modal

-   **Coloque barras de progreso modales en páginas de progreso o cuadros** de diálogo de [progreso](win-dialog-box.md).
-   **Proporcione un botón de comando para detener la operación si tarda más de unos segundos en completarse o tiene la posibilidad de que nunca se complete.** Etiquete el botón Cancelar si la cancelación devuelve el entorno a su estado anterior (sin efectos secundarios). De lo contrario, etiquete el botón Detener para indicar que deja intacta la operación parcialmente completada. Puede cambiar la etiqueta del botón de Cancelar a Detener en medio de la operación si en algún momento no es posible devolver el entorno a su estado anterior. Centre el botón de comando verticalmente con la barra de progreso en lugar de alinear sus superiores.

    **Correcto:**

    ![captura de pantalla del progreso de la espera de red ](images/progress-bars-image20.png)

    En este ejemplo, detener la conexión de red no tiene ningún efecto secundario, por lo que se usa Cancelar.

    **Correcto:**

    ![captura de pantalla de la barra de progreso que muestra el tiempo de copia a la izquierda ](images/progress-bars-image21.png)

    En este ejemplo, detener la copia deja los archivos copiados, por lo que el botón de comando tiene la etiqueta Detener.

    **Incorrecto:**

    ![captura de pantalla de la barra de progreso de búsqueda y el botón detener ](images/progress-bars-image22.png)

    En este ejemplo, detener la búsqueda no deja ningún efecto secundario, por lo que el botón de comando debe etiquetarse como Cancelar.

### <a name="time-remaining"></a>Tiempo restante

Para las barras de progreso determinadas:

-   **Use los siguientes formatos de hora.** Comience con el primero de los siguientes formatos, donde la unidad de tiempo más grande no es cero y, a continuación, cambie al siguiente formato una vez que la unidad de tiempo más grande se convierta en cero.

    **Para las barras de progreso:**

    **Si la información relacionada se muestra en formato de dos puntos:**

    Tiempo restante: h horas, m minutos

    Tiempo restante: m minutos, s segundos

    Tiempo restante: s segundos

    **Si el espacio de pantalla es premium:**

    h hrs, m mins remaining

    m mins, s secs restantes

    s segundos restantes

    **Lo contrario:**

    h hours, m minutes remaining

    m minutes, s seconds remaining

    s segundos restantes

    **Para las barras de título:**

    hh:mm restante

    mm:ss restante

    0:ss restantes

    Este formato compacto muestra primero la información más importante para que no se trunca en la barra de tareas.

-   **Realice estimaciones precisas, pero no dé una precisión falsa.** Si la unidad más grande es horas, dé minutos (si es significativo), pero no segundos.

    **Incorrecto:**

    hh hours, mm minutes, ss seconds

-   **Mantenga actualizada la estimación.** El tiempo de actualización restante calcula al menos cada 5 segundos.
-   **Céntrate en el tiempo restante,** ya que es la información que más preocupa a los usuarios. Proporcionar tiempo total transcurrido solo cuando haya escenarios en los que el tiempo transcurrido sea útil (por ejemplo, cuando es probable que se repita la tarea). Si la estimación de tiempo restante está asociada a una barra de progreso, no tiene el porcentaje de texto completo porque esa información la transmite la propia barra de progreso.
-   **Ser gramaticalmente correcto.** Use unidades singulares cuando el número sea uno.

    **Incorrecto:**

    1 minuto, 1 segundo

-   **Use mayúsculas de estilo de frase.**

### <a name="progress-bar-colors"></a>Colores de la barra de progreso

-   **Use barras de progreso de color rojo o amarillo solo para indicar el estado del progreso, no los resultados finales de una tarea.** Una barra de progreso roja o amarilla indica que los usuarios deben realizar alguna acción para completar la tarea. Si la condición no se puede recuperar, deje la barra de progreso en verde y muestre un mensaje de error.
-   **Active la barra de progreso en rojo cuando haya una condición recuperable por el usuario que impida realizar más progresos.** Muestre un mensaje para explicar el problema y recomendar una solución.
-   Active la barra de progreso de color amarillo para indicar que el usuario ha pausado la tarea o que hay una condición que está **impediendo** el progreso, pero el progreso sigue teniendo lugar (como, por ejemplo, con una conectividad de red deficiente). Si el usuario se ha pausado, cambie la etiqueta del botón Pausar a Reanudar. Si se impide el progreso, muestre un mensaje para explicar el problema y recomendar una solución.

### <a name="meters"></a>Metros

-   **Use barras de progreso solo para el progreso.** Use medidores para indicar porcentajes que no están relacionados con el progreso.

## <a name="recommended-sizing-and-spacing"></a>Tamaño y espaciado recomendados

![diagrama que muestra el tamaño y el espaciado de la barra de progreso ](images/progress-bars-image23.png)

Tamaño y espaciado recomendados para las barras de progreso.

-   Use siempre el alto de la barra de progreso recomendado.
    -   **Excepción:** Puede usar un alto diferente si la ventana primaria no admite el alto recomendado.
-   Use el ancho mínimo si desea que la barra de progreso sea discreta.
-   No use anchos más largos que el máximo recomendado. La barra de progreso no tiene que rellenar el espacio disponible.
-   Centrar la barra de progreso horizontalmente si la ventana es mucho más ancha que el ancho máximo recomendado.

## <a name="labels"></a>Etiquetas

### <a name="progress-bar-labels"></a>Etiquetas de barra de progreso

-   **Use una etiqueta concisa con un control de texto estático para indicar lo que está haciendo la operación.** Inicie la etiqueta con un verbo (por ejemplo, Copiar) y termine con puntos suspensivos. Esta etiqueta puede cambiar dinámicamente si la operación tiene varios pasos o está procesando varios objetos.
-   No asigne una clave de [acceso única porque](glossary.md) el control no es interactivo.
-   Use [el uso de mayúsculas y mayúsculas de estilo oración.](glossary.md)
-   Si el usuario no inició directamente la operación, puede incluir una etiqueta adicional para proporcionar el contexto y lamentar la interrupción. Inicie esta etiqueta adicional con la frase Please wait while (Espere mientras). Esta etiqueta no debe cambiar durante la operación.

    ![captura de pantalla de la barra de progreso con etiqueta ](images/progress-bars-image24.png)

    En este ejemplo, se pide al usuario que espere porque el usuario no inició directamente la operación.

-   Coloque la etiqueta encima de la barra de progreso y alinee la etiqueta con el borde izquierdo de la barra de progreso.

### <a name="progress-bar-details"></a>Detalles de la barra de progreso

-   Proporcione detalles en texto estático, precedidos de los datos con una etiqueta que termine con dos puntos. Especifique unidades (segundos, kilobytes, entre otras) después del texto de detalles.

    **Correcto:**

    ![captura de pantalla de la barra de progreso que muestra la velocidad de transferencia ](images/progress-bars-image11.png)

    En este ejemplo, los detalles están etiquetados correctamente.

    **Incorrecto:**

    ![captura de pantalla de la barra de progreso sin la etiqueta adecuada ](images/progress-bars-image25.png)

    En este ejemplo, los detalles no están etiquetados, por lo que se requiere que los usuarios determinen su significado.

-   Use [mayúsculas de estilo oración.](glossary.md)
-   Coloque los detalles debajo de la barra de progreso y alinee la etiqueta con el borde izquierdo de la barra de progreso.
-   No dé el porcentaje completado o restante porque esa información la transmite la propia barra de progreso.

### <a name="cancel-button"></a>Botón Cancelar

-   Etiquete el botón Cancelar si la cancelación devuelve el entorno a su estado anterior (sin ningún efecto secundario); De lo contrario, etiquete el botón Detener para indicar que deja intacta la operación parcialmente completada.
-   Puede cambiar la etiqueta del botón de Cancelar a Detener en medio de la operación si en algún momento no es posible devolver el entorno a su estado anterior.

### <a name="progress-dialog-box-titles"></a>Títulos del cuadro de diálogo Progreso

-   Si la barra de progreso se muestra en un cuadro de diálogo modal, el título del cuadro de diálogo debe ser el nombre del programa o el nombre de la operación. No use lo que debe ser la etiqueta de la barra de progreso para el título del cuadro de diálogo.

    **Correcto:**

    ![captura de pantalla del título de la barra de progreso con el nombre de la tarea ](images/progress-bars-image26.png)

    En este ejemplo, el nombre de la tarea se usa para el título del cuadro de diálogo.

    **Incorrecto:**

    ![captura de pantalla del título redundante del cuadro de diálogo ](images/progress-bars-image27.png)

    En este ejemplo, el texto del título del cuadro de diálogo es una nueva declaración de la etiqueta de la barra de progreso. En su lugar, se debe usar el nombre del programa.

-   Si la barra de progreso se muestra en un cuadro de diálogo de modelado, optimice el título para mostrarlo en la barra de tareas colocando primero la información distintiva de forma concisa. Ejemplo: "66 % completado".

 

