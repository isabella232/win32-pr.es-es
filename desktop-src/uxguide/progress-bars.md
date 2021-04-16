---
title: Barras de progreso
description: Con una barra de progreso, los usuarios pueden seguir el progreso de una operación larga. Una barra de progreso puede mostrar un porcentaje aproximado de finalización (desterminar) o indicar que una operación está en curso (indeterminado).
ms.assetid: 067961fa-2fb1-4cd1-99a4-cbe2244c3913
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: db8aca7300b309fb6929106cf97329956b7accb0
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "104563299"
---
# <a name="progress-bars"></a>Barras de progreso

> [!NOTE]
> Esta guía de diseño se ha creado para Windows 7 y no se ha actualizado para las versiones más recientes de Windows. Gran parte de la guía se sigue aplicando en principio, pero la presentación y los ejemplos no reflejan nuestra [Guía de diseño actual](/windows/uwp/design/).

Con una barra de progreso, los usuarios pueden seguir el progreso de una operación larga. Una barra de progreso puede mostrar un porcentaje aproximado de finalización (desterminar) o indicar que una operación está en curso (indeterminado).

Los estudios de facilidad de uso han demostrado que los usuarios conocen los tiempos de respuesta de más de un segundo. Por lo tanto, debe considerar la posibilidad de que las operaciones que tardan dos segundos o más en completarse sean largas y necesiten algún tipo de comentario de progreso.

![captura de pantalla de una barra de progreso típica ](images/progress-bars-image1.png)

Barra de progreso típica.

> [!Note]  
> Las instrucciones relacionadas con el [diseño](vis-layout.md) se presentan en un artículo independiente.

 

## <a name="is-this-the-right-control"></a>¿Es este el control adecuado?

Para decidirte, intenta responder a estas preguntas:

-   **¿Se completará la operación en unos cinco segundos o menos?** Si es así, use un [indicador de actividad](inter-mouse.md) en su lugar, ya que mostrar una barra de progreso para este tipo de duración corta sería distraer. Si la operación normalmente tarda cinco segundos o menos, pero a veces toma más, comienza con un puntero ocupado y lo convierte en una barra de progreso después de cinco segundos.
-   **¿Se usa una barra de progreso indeterminada para esperar a que el usuario complete una tarea?** En ese caso, no uses una barra de progreso. Las barras de progreso se usan para el progreso del equipo, no el del usuario.
-   **¿Es una barra de progreso indeterminada combinada con una animación?** Si es así, use solo la animación en su lugar. La barra de progreso indeterminada es realmente una animación genérica y no agrega ningún valor a la animación.
-   **¿La operación es una tarea en segundo plano muy larga (más de dos minutos) en la que los usuarios están más interesados en la finalización que el progreso?** En ese caso, utilice en su lugar las [notificaciones](mess-notif.md) . En este caso, los usuarios realizan otras tareas mientras tanto como no supervisan el progreso. El uso de una notificación permite a los usuarios realizar otras tareas sin interrupción. Algunos ejemplos de estas operaciones largas son la impresión, la copia de seguridad, los análisis del sistema y las transferencias de datos masivas o las conversiones.
-   **Una vez completada la operación, ¿los usuarios podrán reproducir los resultados?** Si es así, use un control deslizante en su lugar. Algunos ejemplos de estas operaciones incluyen la grabación y reproducción de vídeo y audio.

    ![captura de pantalla del reproductor de media y el control deslizante ](images/progress-bars-image2.png)

    En este ejemplo, se usa un control deslizante para indicar el progreso mientras se reproduce el sonido. Esto permite a los usuarios reproducir los resultados más adelante.

## <a name="design-concepts"></a>Conceptos de diseño

Durante una operación larga, los usuarios necesitan una idea general de lo que está haciendo la operación. También necesitan saber:

-   Que se ha iniciado una operación larga.
-   Se está llevando a cabo este progreso y la operación finalizará finalmente (y, por lo tanto, no se bloquea).
-   Porcentaje aproximado de la operación que se ha completado (y, por tanto, el porcentaje restante).
-   Si deben cancelar la operación si no merece la pena esperar.
-   Si deben continuar esperando o hacer otra cosa mientras se completa la operación.

**Use las barras de progreso de depuración para las operaciones que requieren una cantidad de tiempo limitada,** incluso si esa cantidad de tiempo no se puede predecir con precisión. Las barras de progreso indeterminadas muestran que se está realizando el progreso, pero no proporcionan ninguna otra información. No elija una barra de progreso indeterminada basada únicamente en la falta de precisión.

Por ejemplo, supongamos que una operación requiere cinco pasos y cada uno de esos pasos requiere una cantidad limitada de tiempo, pero la cantidad de tiempo para cada paso puede variar en gran medida. En este caso, use una barra de progreso de determinación y muestre el progreso cuando cada paso se complete proporcionalmente a la cantidad de tiempo que normalmente tarda cada paso. Use una barra de progreso indeterminada solo si una barra de progreso de determinante haría que los usuarios concluiran incorrectamente que la operación se ha bloqueado.

**Si solo hace algo...**

Asegúrese de proporcionar comentarios sobre el progreso de las operaciones largas y de que la información anterior se comunica claramente. Use las barras de progreso de determine siempre que sea posible.

## <a name="usage-patterns"></a>Patrones de uso

Las barras de progreso tienen varios patrones de uso:

### <a name="determinate-progress-bars"></a>Desterminar barras de progreso



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Barras de progreso de determinación modal</strong><br/> Indicar el progreso de una operación rellenando de izquierda a derecha y rellenando completamente cuando se complete la operación. <br/></td>
<td>Dado que estos comentarios son <a href="glossary.md">modales</a>, los usuarios no pueden realizar otras tareas en la ventana (o en su elemento primario si se muestran en un cuadro de diálogo modal) hasta que se complete la operación. <br/> <img src="images/progress-bars-image3.png" alt="Screen shot of progress bar in modal window " /><br/> En este ejemplo, la barra de progreso proporciona comentarios durante la configuración. <br/></td>
</tr>
<tr class="even">
<td><strong>Barras de progreso de determinación modal con un botón Cancelar o detener</strong><br/> Permitir a los usuarios detener la operación, quizás porque la operación está tardando demasiado o no merece la pena esperar.<br/></td>
<td><img src="images/progress-bars-image4.png" alt="Screen shot of progress bar with Stop button " /><br/> En este ejemplo, los usuarios pueden hacer clic en detener para detener la operación y dejar el entorno en su estado actual.<br/></td>
</tr>
<tr class="odd">
<td><strong>Desterminación modal de barras de progreso con un botón Cancelar o detener y una animación</strong><br/> Permitir a los usuarios detener la operación e incluir una animación para ayudar a los usuarios a visualizar el efecto de una operación.<br/></td>
<td><img src="images/progress-bars-image5.png" alt="Screen shot of progress bar with animation " /><br/> En este ejemplo, los usuarios pueden hacer clic en detener para detener la operación y dejar el entorno en su estado actual.<br/></td>
</tr>
<tr class="even">
<td><strong>Dos barras de progreso modal determinan</strong><br/> Indicar el progreso de una operación de varios pasos mostrando el progreso del paso actual en la primera barra de progreso y el progreso general en la segunda barra.<br/></td>
<td>Dado que la primera barra de progreso proporciona poca información adicional y puede ser muy lenta, no se recomienda este patrón. En su lugar, haga que todos los pasos de la operación compartan una parte del progreso y que una sola barra de progreso vaya a finalización una vez. <br/> <img src="images/progress-bars-image6.png" alt="Screen shot of current and overall progress bars " /><br/> En este ejemplo, la primera barra de progreso muestra el progreso del paso actual y la segunda barra de progreso muestra el progreso general.<br/>
<blockquote>
[!Note]<br />
Este patrón normalmente no es necesario y se debe evitar.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><strong>Barras de progreso de desterminación de modelo no modal</strong><br/> Indicar el progreso de una operación rellenando de izquierda a derecha y rellenando completamente cuando se complete la operación.<br/></td>
<td>A diferencia de las barras de progreso modal, los usuarios pueden realizar otras tareas mientras la operación está en curso. Estas barras de progreso se pueden mostrar en contexto o en una barra de estado. <br/> <img src="images/progress-bars-image7.png" alt="Screen shot of progress bar on status bar " /><br/> En este ejemplo, Windows Internet ExplorerWindows Internet Explorer muestra su progreso para cargar una página web en la barra de estado. Los usuarios pueden realizar otras tareas mientras se carga la página.<br/></td>
</tr>
</tbody>
</table>



 

### <a name="indeterminate-progress-bars"></a>Barras de progreso indeterminadas



|                                                                                                                                                                                         |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Barras de progreso indeterminadas modales**<br/> para indicar que una operación está en curso, muestre una animación que se recorra continuamente en la barra de izquierda a derecha. <br/>   | Solo se usa para las operaciones cuyo progreso general no se puede determinar, por lo que no hay ninguna noción de integridad. las barras de progreso de determinan son preferibles porque indican el porcentaje aproximado de la operación que se ha completado y ayudan a los usuarios a determinar si la operación merece la pena seguir esperando. también se distraen menos visualmente. <br/> ![captura de pantalla de barra de progreso modal e indeterminada](images/progress-bars-image8.png)<br/> En este ejemplo, Windows Update usa una barra de progreso indeterminada modal para indicar el progreso mientras busca actualizaciones.<br/> |
| **Barras de progreso indeterminadas no modales**<br/> para indicar que una operación está en curso, muestre una animación que se recorra continuamente en la barra de izquierda a derecha.<br/> | A diferencia de las barras de progreso modales, los usuarios pueden realizar otras tareas mientras el procesamiento está en curso. Estas barras de progreso se pueden mostrar en contexto o en una barra de estado. <br/> ![captura de pantalla de la barra de progreso fino en la ventana de Outlook ](images/progress-bars-image9.png)<br/> En este ejemplo, Microsoft Outlook usa una barra de progreso indeterminada no modal al rellenar las propiedades de contacto. Los usuarios pueden seguir usando la ventana de propiedades mientras el trabajo está en curso.<br/>                                                                                                                    |



 

### <a name="meters"></a>Metros



|                                                                                          |                                                                                                                                                                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Metros**<br/> indicar un porcentaje que no está relacionado con el progreso. <br/> | Este patrón no es una barra de progreso, pero se implementa mediante el control de barra de progreso. los medidores tienen una apariencia distinta para diferenciarlos de las barras de progreso auténticas. <br/> ![captura de pantalla de medidor que muestra el espacio libre en disco ](images/progress-bars-image10.png)<br/> En este ejemplo, el medidor muestra el porcentaje de espacio de la unidad de disco utilizado.<br/> |



 

## <a name="guidelines"></a>Directrices

### <a name="general"></a>General

-   **Proporcionar comentarios sobre el progreso al realizar una operación larga.** Los usuarios nunca deben adivinar si se realiza el progreso.
-   **Indique claramente el progreso real.** La barra de progreso debe avanzar si se está realizando el progreso. Si el intervalo de tiempos de finalización esperados es grande, considere la posibilidad de usar una escala no lineal para indicar el progreso de las horas más largas. No quiere que los usuarios terminen de que el programa se ha bloqueado cuando no lo ha hecho.
-   **Indique claramente la falta de progreso.** La barra de progreso no debe avanzar si no se realiza ningún progreso. No quiere que los usuarios esperen indefinidamente para una operación que nunca se va a completar.
-   **Proporcione detalles de progreso útiles.** Proporcione información de progreso adicional, pero solo si los usuarios pueden hacer algo con ella. Asegúrese de que el texto se muestra el tiempo suficiente para que los usuarios puedan leerlo.

    ![captura de pantalla de la barra de progreso que muestra la velocidad de transferencia ](images/progress-bars-image11.png)

    En este ejemplo, los usuarios pueden ver la velocidad de transferencia. La tasa de transferencia baja sugiere aquí la necesidad de usar una conexión de red de ancho de banda alto.

-   **No proporcione detalles innecesarios.** Por lo general, los usuarios no tienen cuidado con los detalles de la operación que se realiza. Por ejemplo, los usuarios de un programa de instalación no se interesan del archivo específico que se está copiando o de que los componentes del sistema se están registrando porque no tienen ninguna expectativa sobre estos detalles. Normalmente, una barra de progreso bien etiquetada solo proporciona información suficiente, por lo que debe proporcionar información de progreso adicional solo si los usuarios pueden hacer algo con ella. Proporcionar detalles que los usuarios no preocupan por la experiencia del usuario en exceso y técnica. Si necesita información más detallada para la depuración, no la muestre en las compilaciones de versión.

    **Correcto:**

    ![captura de pantalla del progreso de la instalación ](images/progress-bars-image12.png)

    En este ejemplo, la barra de progreso etiquetada es todo lo que se necesita.

    **Correcto:**

    ![captura de pantalla de la barra de progreso que muestra la velocidad de transferencia ](images/progress-bars-image11.png)

    En este ejemplo, el explorador de Windows está copiando los archivos seleccionados por el usuario, por lo que es significativo mostrar los nombres de archivo que se van a copiar.

    **Incorrecto:**

    ![captura de pantalla del progreso del registro ](images/progress-bars-image13.png)

    En este ejemplo, un programa de instalación proporciona detalles que no tienen sentido para el usuario.

-   **Proporcionar animaciones útiles.** Si se hace bien, las animaciones mejoran la experiencia del usuario ayudando a los usuarios a visualizar la operación. Las animaciones buenas tienen más impacto que el texto por sí solo. Por ejemplo, la barra de progreso del comando eliminar de Outlook muestra la papelera de reciclaje del destino si se pueden recuperar los archivos, pero no la papelera de reciclaje si no se pueden recuperar los archivos.

    ![captura de pantalla del progreso de la eliminación ](images/progress-bars-image14.png)

    En este ejemplo, la falta de una papelera de reciclaje refuerza que los archivos se eliminen de forma permanente. Esta información adicional no se comunicará tan eficazmente usando solo texto.

-   **No use animaciones innecesarias.** Las animaciones pueden ser engañosas porque normalmente se ejecutan en un subproceso independiente de la tarea real y, por tanto, pueden sugerir el progreso incluso si la operación se ha bloqueado. Además, si la operación es más lenta de lo esperado, a veces los usuarios suponen que la animación forma parte de la razón. Por consiguiente, solo se usan animaciones cuando hay una justificación clara; no las use para intentar entretener a los usuarios.
-   **Coloque animaciones centradas en la barra de progreso.** Coloque la animación encima de las etiquetas de la barra de progreso, si tiene alguna. Si hay un botón Cancelar o detener a la derecha de la barra de progreso, incluya el botón al determinar el centro.
-   **Reproducir un efecto de sonido al finalizar una operación solo si es muy larga (más de dos minutos), poco frecuente y importante.** Si es probable que el usuario salga de una operación importante mientras se está procesando, un efecto sonoro restaura la atención del usuario. El uso de un efecto sonoro en el momento de la finalización en otras circunstancias sería la molestia.
-   **No robe el foco de entrada para mostrar una actualización o finalización de progreso.** A menudo, los usuarios cambian a otros programas mientras esperan y no quieren que se interrumpan. Las tareas en segundo plano deben permanecer en segundo plano.
-   **No se preocupe por el soporte técnico.** Dado que los comentarios proporcionados por las barras de progreso no son necesariamente precisos y se deshacen, las barras de progreso no son un buen mecanismo para proporcionar información de soporte técnico. Por consiguiente, si la operación puede producir un error (como con un programa de instalación), no proporcione información de progreso adicional que solo sea útil para el soporte técnico. En su lugar, proporcione un mecanismo alternativo, como un archivo de registro para registrar la información de soporte técnico.

    **Incorrecto:**

    ![captura de pantalla de la barra de progreso que muestra el nombre del servidor ](images/progress-bars-image15.png)

    En este ejemplo, la barra de progreso muestra detalles destinada a soporte técnico.

-   **No ponga el porcentaje completo ni cualquier otro texto en una barra de progreso.** Dicho texto no es accesible y no es compatible con el uso de temas.

    **Incorrecto:**

    ![captura de pantalla de la barra de progreso con texto en la barra ](images/progress-bars-image16.png)

    En este ejemplo, no se puede tener acceso al texto porcentual en la barra de progreso.

-   **No combine una barra de progreso con un puntero ocupado.** Use uno u otro, pero no ambos al mismo tiempo.
-   **No use barras de progreso verticales.** Las barras de progreso horizontales tienen una asignación más natural y un mejor flujo.

### <a name="determinate-progress-bars"></a>Desterminar barras de progreso

-   **Use las barras de progreso de depuración para las operaciones que requieren una cantidad de tiempo limitada,** incluso si esa cantidad de tiempo no se puede predecir con precisión. Las barras de progreso indeterminadas muestran que se está realizando el progreso, pero no proporcionan ninguna otra información. No elija una barra de progreso indeterminada basada únicamente en la falta de precisión.
-   **Indique claramente la fase de progreso.** La barra de progreso debe ser capaz de indicar si la operación se encuentra en el principio, el centro o el final de una operación. Por ejemplo, las barras de progreso que se transfieren inmediatamente al final del 99 por ciento, permanecen allí durante mucho tiempo y, en particular, son informativas y molestas. En estos casos, la barra de progreso debe establecerse inicialmente en un 33 por ciento como máximo para indicar que la operación todavía está en la fase de inicio.
-   **Indique claramente la finalización.** No permita que una barra de progreso vaya al 100 por ciento, a menos que la operación se haya completado.
-   **Proporcione una estimación de tiempo restante si puede hacerlo con precisión.** Las estimaciones de tiempo restantes que son exactas son útiles, pero las estimaciones que no son muy útiles para la marca o el rebote no resultan de gran utilidad. Es posible que deba realizar algún procesamiento antes de que pueda proporcionar estimaciones precisas. Si es así, no muestre estimaciones potencialmente inexactas durante este período inicial.
-   **No reinicie el progreso.** Una barra de progreso pierde su valor si se reinicia (quizás porque se completa un paso de la operación) porque los usuarios no tienen forma de saber cuándo se completará la operación. En su lugar, haga que todos los pasos de la operación compartan una parte del progreso y que la barra de progreso vaya a finalización una vez.

    **Incorrecto:**

    ![captura de pantalla de la barra de progreso que se reinició ](images/progress-bars-image17.png)

    En este ejemplo, la operación se ha desplazado al paso de copiar archivos y restablecer la barra de progreso para ese paso. Ahora los usuarios no saben cuánto progreso se ha realizado o cuánto tiempo queda.

-   **No realice una copia de seguridad del progreso.** Al igual que con un reinicio, una barra de progreso pierde su valor si realiza una copia de seguridad. Aumente siempre el progreso de una vez. Sin embargo, puede tener una estimación de tiempo restante que aumenta (y disminuye) porque la tasa de progreso puede variar.

### <a name="indeterminate-progress-bars"></a>Barras de progreso indeterminadas

-   **Use barras de progreso indeterminadas solo para las operaciones cuyo progreso general no se puede determinar.** Use barras de progreso indeterminadas para las operaciones que requieren un período de tiempo ilimitado o que tengan acceso a un número desconocido de objetos. Utilice los tiempos de espera para proporcionar límites a las operaciones basadas en el tiempo.
-   **Convierta en una barra de progreso de determinación una vez que se pueda determinar el progreso general.** Por ejemplo, si se tarda mucho más de dos segundos en determinar el número de objetos, puede usar una barra de progreso indeterminada mientras se cuentan los objetos y, después, convertirlo en una barra de progreso de determinación.
-   **No combine barras de progreso indeterminadas con las estimaciones de porcentaje completado o tiempo restante.** Si puede proporcionar esta información, utilice en su lugar una barra de progreso de finalización.
-   **No combine barras de progreso indeterminadas con animaciones.** Una barra de progreso indeterminada es realmente una animación genérica, por lo que debe usar una u otra, pero nunca ambas.

    **Correcto:**

    ![captura de pantalla del progreso en la detección del servidor ](images/progress-bars-image18.png)

    En este ejemplo, solo se utiliza una animación para mostrar que una operación está en curso.

### <a name="modeless-progress-bars"></a>Barras de progreso no modales

-   **Si los usuarios pueden hacer algo productivo mientras la operación está en curso, proporcione comentarios de modelo no modal.** Es posible que tenga que deshabilitar un subconjunto de funcionalidad que requiere que se complete la operación.
-   **Si la ventana tiene una barra de direcciones, muestre el progreso no modal en la barra de direcciones.**

    ![captura de pantalla de la barra de progreso como parte de la barra de direcciones ](images/progress-bars-image19.png)

    En este ejemplo, el progreso no modal se muestra en la barra de direcciones.

-   De lo contrario, **si la ventana tiene una barra de estado, muestra el progreso no modal en la barra de estado.** Coloque el texto correspondiente a su izquierda en la barra de estado.

    ![captura de pantalla de la barra de progreso como parte de la barra de estado ](images/progress-bars-image7.png)

    En este ejemplo, el progreso no modal se muestra en la barra de estado.

### <a name="modal-progress-bars"></a>Barras de progreso modal

-   **Coloque barras de progreso modales en las páginas de progreso o en los cuadros de diálogo de** [progreso](win-dialog-box.md).
-   **Proporcione un botón de comando para detener la operación si se tardan más de unos segundos en completarse, o si tiene la posibilidad de que nunca se complete.** Etiquete el botón Cancelar si la cancelación devuelve el entorno a su estado anterior (sin dejar efectos secundarios); de lo contrario, etiquete el botón detener para indicar que deja intacta la operación completada parcialmente. Puede cambiar la etiqueta del botón de cancelar para detenerla en medio de la operación si en algún momento no es posible devolver el entorno a su estado anterior. Centre el botón de comando verticalmente con la barra de progreso en lugar de alinear su parte superior.

    **Correcto:**

    ![captura de pantalla del progreso de la espera de la red ](images/progress-bars-image20.png)

    En este ejemplo, la detención de la conexión de red no tiene ningún efecto secundario, por lo que se usa CANCEL.

    **Correcto:**

    ![captura de pantalla de la barra de progreso que muestra el tiempo de copia restante ](images/progress-bars-image21.png)

    En este ejemplo, la detención de la copia deja los archivos copiados, por lo que el botón de comando tiene la etiqueta STOP.

    **Incorrecto:**

    ![captura de pantalla de la barra de progreso de la búsqueda y el botón detener ](images/progress-bars-image22.png)

    En este ejemplo, la detención de la búsqueda no deja ningún efecto secundario, por lo que el botón de comando debe etiquetarse como cancelar.

### <a name="time-remaining"></a>Tiempo restante

Para las barras de progreso de determinación:

-   **Use los siguientes formatos de hora.** Comience con el primero de los siguientes formatos en los que la unidad de tiempo más grande no sea cero y, a continuación, cambie al formato siguiente una vez que la unidad de tiempo más grande sea cero.

    **Para barras de progreso:**

    **Si la información relacionada se muestra en un formato de dos puntos:**

    Tiempo restante: h horas, m minutos

    Tiempo restante: m minutos, s segundos

    Tiempo restante: s segundos

    **Si el espacio de la pantalla es Premium:**

    horas h, m min.

    m min, s segundos restantes

    s segundos restantes

    **Casos**

    h horas, m minutos restantes

    m minutos, s segundos restantes

    s segundos restantes

    **Para las barras de título:**

    HH: mm restantes

    mm: SS restante

    0: SS restante

    Este formato compacto muestra la información más importante en primer lugar para que no se trunque en la barra de tareas.

-   **Realizar estimaciones precisas, pero no proporcionar una precisión falsa.** Si la unidad más grande es horas, dé unos minutos (si es significativo) pero no los segundos.

    **Incorrecto:**

    HH horas, mm minutos, SS segundos

-   **Mantenga la estimación actualizada.** Las estimaciones restantes de tiempo de actualización al menos cada 5 segundos.
-   **Céntrese en el tiempo restante** , ya que es la información que los usuarios más le interesan. Proporcione el tiempo total transcurrido solo cuando haya escenarios en los que el tiempo transcurrido sea útil (por ejemplo, cuando sea probable que se repita la tarea). Si la estimación de tiempo restante está asociada a una barra de progreso, no hay ningún texto de porcentaje completo porque esa información se transmite por la barra de progreso.
-   **Ser gramaticalmente correcto.** Use unidades singulares cuando el número sea uno.

    **Incorrecto:**

    1 minutos, 1 segundo

-   **Use mayúsculas de estilo de frase.**

### <a name="progress-bar-colors"></a>Colores de la barra de progreso

-   **Use barras de progreso rojo o amarillo solo para indicar el estado de progreso, no los resultados finales de una tarea.** Una barra de progreso roja o amarilla indica que los usuarios deben realizar alguna acción para completar la tarea. Si la condición no se recupera, deje la barra de progreso verde y muestre un mensaje de error.
-   **Active la barra de progreso en rojo cuando haya una condición recuperable del usuario que Evite realizar un progreso posterior.** Muestre un mensaje para explicar el problema y recomendar una solución.
-   **Convierta la barra de progreso en amarillo para indicar que el usuario ha pausado la tarea o que hay una condición que impide el progreso** , pero sigue teniendo lugar el progreso (como, por ejemplo, con una conectividad de red deficiente). Si el usuario está en pausa, cambie la etiqueta del botón pausa a reanudar. Si se impide el progreso, muestre un mensaje para explicar el problema y recomendar una solución.

### <a name="meters"></a>Metros

-   **Use barras de progreso solo para el progreso.** Use medidores para indicar los porcentajes que no están relacionados con el progreso.

## <a name="recommended-sizing-and-spacing"></a>Ajuste de tamaño y espaciado recomendados

![diagrama que muestra el tamaño y el espaciado de la barra de progreso ](images/progress-bars-image23.png)

Ajuste de tamaño y espaciado recomendados para las barras de progreso.

-   Use siempre el alto de la barra de progreso recomendado.
    -   **Excepción:** Puede usar un alto diferente si la ventana primaria no admite el alto recomendado.
-   Use el ancho mínimo si desea que la barra de progreso sea discreta.
-   No use anchos mayores que el máximo recomendado. La barra de progreso no tiene que rellenar el espacio disponible.
-   Centrar la barra de progreso horizontalmente si la ventana es mucho más ancha que el ancho máximo recomendado.

## <a name="labels"></a>Etiquetas

### <a name="progress-bar-labels"></a>Etiquetas de la barra de progreso

-   **Use una etiqueta concisa con un control de texto estático para indicar lo que está haciendo la operación.** Inicie la etiqueta con un verbo (por ejemplo, copiando) y termine con puntos suspensivos. Esta etiqueta puede cambiar dinámicamente si la operación tiene varios pasos o si está procesando varios objetos.
-   No asigne una [clave de acceso](glossary.md) única porque el control no es interactivo.
-   Usar [mayúsculas y minúsculas en el estilo de oraciones](glossary.md).
-   Si el usuario no inició directamente la operación, puede incluir una etiqueta adicional para asignar el contexto y la disculpa de la interrupción. Inicie esta etiqueta adicional con la frase, espere mientras. Esta etiqueta no debe cambiar durante la operación.

    ![captura de pantalla de la barra de progreso con la etiqueta ](images/progress-bars-image24.png)

    En este ejemplo, se le pide al usuario que espere porque el usuario no inició directamente la operación.

-   Coloque la etiqueta encima de la barra de progreso y alinee la etiqueta con el borde izquierdo de la barra de progreso.

### <a name="progress-bar-details"></a>Detalles de la barra de progreso

-   Proporcione los detalles en texto estático, precediendo a los datos con una etiqueta que termina con un signo de dos puntos. Especificar unidades (segundos, kilobytes, etc.) después del texto de detalles.

    **Correcto:**

    ![captura de pantalla de la barra de progreso que muestra la velocidad de transferencia ](images/progress-bars-image11.png)

    En este ejemplo, los detalles están correctamente etiquetados.

    **Incorrecto:**

    ![captura de pantalla de la barra de progreso sin la etiqueta adecuada ](images/progress-bars-image25.png)

    En este ejemplo, los detalles no se etiquetan, lo que requiere que los usuarios determinen su significado.

-   Usar [mayúsculas y minúsculas en el estilo de oraciones](glossary.md).
-   Coloque los detalles debajo de la barra de progreso y alinee la etiqueta con el borde izquierdo de la barra de progreso.
-   No dé al porcentaje completado o restante porque esa información la transmite la propia barra de progreso.

### <a name="cancel-button"></a>Botón Cancelar

-   Etiquete el botón Cancelar si la cancelación devuelve el entorno a su estado anterior (sin dejar ningún efecto secundario); de lo contrario, etiquete el botón detener para indicar que deja intacta la operación parcialmente completada.
-   Puede cambiar la etiqueta del botón de cancelar para detenerla en medio de la operación si en algún momento no es posible devolver el entorno a su estado anterior.

### <a name="progress-dialog-box-titles"></a>Títulos del cuadro de diálogo progreso

-   Si la barra de progreso se muestra en un cuadro de diálogo modal, el título del cuadro de diálogo debe ser el nombre del programa o el nombre de la operación. No use lo que debe ser la etiqueta de la barra de progreso para el título del cuadro de diálogo.

    **Correcto:**

    ![captura de pantalla del título de la barra de progreso con el nombre de la tarea ](images/progress-bars-image26.png)

    En este ejemplo, el nombre de la tarea se usa para el título del cuadro de diálogo.

    **Incorrecto:**

    ![captura de pantalla del título de cuadro de diálogo redundante ](images/progress-bars-image27.png)

    En este ejemplo, el texto del título del cuadro de diálogo es una resituación de la etiqueta de la barra de progreso. En su lugar, se debe usar el nombre del programa.

-   Si la barra de progreso se muestra en un cuadro de diálogo no modal, optimice el título para que se muestre en la barra de tareas; para ello, coloque primero la información distintiva. Ejemplo: "66% completado".

 

